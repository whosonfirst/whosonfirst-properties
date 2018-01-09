# Existential flags

There are currently (5) existential flags for WOF documents that map to the "standard places response" (SPR) interface.

Detailed rules for each flag are discussed below but at a high level it breaks down like this:

## Flags

### is_current

`is_current` serves as a short-hand filter for pruning or limiting results. Its value is dependent on placetype and derived for other properties in a record. For example both a venue that has a closed (is no longer open for business) and a neighbourhood that has been marked as deprecated (because of bunk data) will be marked as no longer current or `mz:is_current=0`.

### is_ceased

`is_ceased` indicates that the place in question is no longer a present concern. For example a venue (business) that has closed and the former Yugoslavia will both be flagged as `mz:is_ceased=1`. Generally this value is derived by testing for the presence of the `edtf:ceased` property.

### is_deprecated

`is_deprecated` indicates that a record is not longer considered valid and should not be used anymore. Many records that are deprecated will also be superseded by a valid record but that is not required. Genereally this value is derived by testing for the presence of the `edtf:deprecated` property.

TODO : Discuss "uuuu"

### is_superseded

`is_superseded` indicates that a record has been superseded by another record. There are many reasons why one record may supersede another record ranging from a "major" lifecycle change or a record being deprecated. Generally this value is derived by testing for presence of and a non-zero length of the `wof:superseded_by` property.

Lifecycle changes are documented in: [ LINK ]

It is important to note that a record may be both superseded and superseding at the same time.

### is_superseding

`is_superseding` indicates that a record is superseding one or more records. As with the `is_superseded` property here are many reasons why a record many supersede another. Generally this value is derived by testing for the the presence of and a non-zero length of the `wof:supersedes` property.

It is important to note that a record may be both superseded and superseding at the same time.

## Flag values

### -1

Unknown.

### 0

False

### 1

True

## Unsupported flags (as of this writing)

The following flags are currently _not_ part of the standard existential flags. Each is described in the [whosonfirst-properties/properties/mz]() documented.

* mz:is_approximate

* mz:is_funky

* mz:is_official

All of these properties are manually assigned rather than derived. None of these properties are required and may not be present in a WOF document.

## Interfaces

Currently the SPR interface and corresponding existential flags are only implemented in the Go language.

### SPR

The relevant section of the SPR interface, as defined in the [go-whosonfirst-spr]()  package, looks like this:

```
type StandardPlacesResult interface {
     	...
	IsCurrent() flags.ExistentialFlag
	IsCeased() flags.ExistentialFlag
	IsDeprecated() flags.ExistentialFlag
	IsSuperseded() flags.ExistentialFlag
	IsSuperseding() flags.ExistentialFlag
}	
```

### Existential Flags

The interface for existential flags (as returned by the SPR interface), as defined in the [go-whosonfirst-flags]() package, looks like this:

```
type ExistentialFlag interface {
	StringFlag() string
	Flag() int64
	IsTrue() bool
	IsFalse() bool
	IsKnown() bool
	MatchesAny(...ExistentialFlag) bool
	MatchesAll(...ExistentialFlag) bool
	String() string
}
```

### Examples

#### Who's On First GeoJSON files

The [go-whosonfirst-geojson-v2]() defines the following SPR (and existential flags) for Who's On First GeoJSON files:

https://github.com/whosonfirst/go-whosonfirst-geojson-v2/blob/master/properties/whosonfirst/whosonfirst.go#L179-L284

#### Plain old GeoJSON files

The [go-whosonfirst-geojson-v2]() defines the following SPR (and existential flags) for plain old GeoJSON files:

https://github.com/whosonfirst/go-whosonfirst-geojson-v2/blob/master/feature/geojson.go#L220-L238

(Hint: everything returns `-1`)

## Rules

### IsCurrent()

1. If the `mz:is_current` property is present return that
2. If the `IsDeprecated()` method returns a flag whose `IsTrue()` and `IsKnown()` methods return true return an existential flag of `0`
3. Is the `IsCeased()` method returns a flag  whose `IsTrue()` and `IsKnown()` methods return true return an existential flag of `0`
4. If the `IsSuperseded()` method returns a flag  whose `IsTrue()` and `IsKnown()` methods return true return an existential flag of `0`
5. Otherwise return an existential flag of `-1`

### is_ceased

1. If the `edtf:deprecated` property is present
1b. and its value is `u` return an existential flag of `-1`
1c. and its value is `uuuu` return an existential flag of `-1`
2d. and is not empty return and existential flag of `1`
2. Otherwise return an existential flag of `0`

### is_deprecated

1. If the `edtf:deprecated` property is present
1b. and its value is `u` return an existential flag of `-1`
1c. and its value is `uuuu` return an existential flag of `-1`
2d. and is not empty return and existential flag of `1`
2. Otherwise return an existential flag of `0`

### is_superseded

1. If the `wof:superseded_by` property is present and is an array and contains one or more WOF ID, return an existential flag of `1`
2. Otherwise return an existential flag of `0`

### is_superseding

1. If the `wof:supersedes` property is present and is an array and contains one or more WOF ID, return an existential flag of `1`
2. Otherwise return an existential flag of `0`

### Extended DateTime Format (EDTF)

The choice and use of EDTF for dates is discussed in detail in the [whosonfirst-dates]() repository. The thing to note for the purpose of this document is that dates in many WOF records MAY have a value of `uuuu` which is EDTF shorthand for unknown or undefined. It should not be confused with a valid EDTF date string.