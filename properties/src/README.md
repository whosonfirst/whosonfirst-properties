# src

## geom
The data source of a record's geometry. Valid property values are listed in the [`whosonfirst-sources`](https://github.com/whosonfirst/whosonfirst-sources/tree/master/sources) repository.

_Example: `"src:geom":"quattroshapes"`_

## geom_alt
The data source of a record's alt-geometry. Valid property values are listed in the [`whosonfirst-sources`](https://github.com/whosonfirst/whosonfirst-sources/tree/master/sources) repository.

_Example: `"src:geom\_alt":"naturalearth"`_

## lbl
The source of a record's `lbl` properties. Valid property values are generally derived from [`mapshaper`](https://github.com/mbloch/mapshaper) and is also listed in the [`whosonfirst-sources`](https://github.com/whosonfirst/whosonfirst-sources/tree/master/sources) repository.

Other iterations of the `lbl` property can include `lbl:centroid` and `centroid_lbl`; these properties are specific to the label centroid of a given feature.

_Example: `"src:lbl":"mapshaper"` or `"src:lbl:centroid":"mapshaper"`_

## population
The source of a record's population value, which is stored in the wof:population property. Property values are a source name.

_Example: `"src:population":"statoids"`_