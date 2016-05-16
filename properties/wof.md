# wof

`wof` stands for Who's On First

## belongsto

The (unique) set of all ancestors, as an array (list) of WOF IDs.

## breaches

Records of the same placetype that intersect the current record, as an array (list) of WOF IDs.

## concordances

A hash containing identifiers from other data sources. See also: [other people's concordances](https://github.com/whosonfirst/tools-other-peoples-concordances)

## country

A two-letter country code from ISO 3166.

## geomhash

An MD5 string of the geometry JSON.

## hierarchy

A list of hashes, where each object is the list of ancestors.

## id

The record's numeric integer identifier.

## lang

One or more [ISO-639-3](http://www.i18nguy.com/unicode/language-identifiers.html) language identifiers. These represent the common, or preferred, languages spoken in the location of the corresponding WOF record.

## lang_x_official

One or more [ISO-639-3](http://www.i18nguy.com/unicode/language-identifiers.html) language identifiers. These represent the officially recognized languages of the location of the corresponding WOF record.

## lang_x_spoken

One or more [ISO-639-3](http://www.i18nguy.com/unicode/language-identifiers.html) language identifiers. These represent the languages, inclusive of official languages, spoken in the location of the corresponding WOF record.

## created

A Unix epoch timestamp integer.

## lastmodified

A Unix epoch timestamp integer.

## name

An English UTF-7 transliterated representation of the name. See also: [whosonfirst-names](https://github.com/whosonfirst/whosonfirst-names)

## parent_id

An integer WOF ID of the direct parent record.

## placetype

A string [placetype](https://github.com/whosonfirst/whosonfirst-placetypes).

## superseded_by

An array (a list) of WOF IDs that have superseded the WOF record.

## supersedes

An array (a list) of WOF IDs that the record supersedes.

## tags

An array (a list) of tags.
