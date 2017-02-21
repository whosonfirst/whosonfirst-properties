# mz

## hierarchy_label


## hours

A simplified encoding of a venue's hours of operation. This is not designed to capture every edge case or exception, just daily hours with open/close times. The value is encoded as a dictionary with three-letter day abbreviations (`sun`, `mon`, `tue`, `wed`, `thu`, `fri`, `sat`) as keys. Each day value is a dictionary with `open` and `close` keys, and values are composed of 24-hour format time like `09:30` or `16:45`.

#### Example:
```
"mz:hours": {
	"mon": {
		"open": "07:30",
		"close": "19:00"
	},
	"tue": {
		"open": "08:30",
		"close": "22:00"
	}
}
```

## is_approximate

This means that the geometry for this record is approximate in nature and probably derived from one of its ancestors. Technically the geometry may be incorrect but the rule of thumb is that it is still less-incorrect than no geometry or "spanning the entire globe".

## is_current

This is a "helper" property to wrap up / hide the semantics of whether something is "open" or "existing". For example, a venue that is no longer in operation or a country (like Yugoslavia) that has dissolved in to smaller nations.

* `0` signifies a non-current record
* `1` signifies a current record

Therefore, any record with a date in the `edtf:cessation` or `edtf:deprecated` fields _should_ have a `mz:is_current` field value of `0`.

## is_funky

* `-1` is unknown, or TBD (needs the love and care of a human)
* `0` is false
* `1` is true

## is_hard_boundary

Things like historic districts or similar with fixed, undisputed boundaries.

* `0` is false
* `1` is true

## is_landuse_aoi

This is used to signify an area of interest. Labelling is supressed if a value of '1' is given.

* `0` is false
* `1` is true

## is_official

Is this considered "official" by someone or something you pay taxes to?

* `0` is false
* `1` is true

## max_zoom

Float values (though in practice mosts are integer values) that match to web map zoom schema. Common range is 0.0 to 18.0, though they can be greater.

## min_zoom

Float values (though in practice mosts are integer values) that match to web map zoom schema. Common range is 0.0 to 18.0, though they can be greater.

## tier_local

Some estimation of coverage (including descendants) and completeness, based on total number of geotagged photos.

```
1: 0-2500 (Arcata, California; Larkspur, CA; Suitland, MD)
2: 2501-15000 (Daily City, California; Eureka, California; Bowie MD; Vienna, VA; Hyattsville, MD)
3: 15001-55000 (San Mateo, Mill Valley, Hayward; Alexandria, VA; Silver Spring, MD)
4: 55001-175000 (Oakland, California; Palo Alto, Santa Cruz; Arlington, VA)
5: 175001-550000 (San Jose, California; Baltimore, MD)
6: 550001-1200000 (Los Angeles, California; Washington, DC)
7: 1200001-2500000 (SF, NYC, London, Paris)
```
