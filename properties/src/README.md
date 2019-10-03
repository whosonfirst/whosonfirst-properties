# src

## geom
The data source of a record's geometry. Valid property values are listed in the [`whosonfirst-sources`](https://github.com/whosonfirst/whosonfirst-sources/tree/master/sources) repository.

_Example: `"src:geom":"quattroshapes"`_

## geom_alt
The data source of a record's alt-geometry. Valid property values are listed in the [`whosonfirst-sources`](https://github.com/whosonfirst/whosonfirst-sources/tree/master/sources) repository.

_Example: `"src:geom_alt":"naturalearth"`_

## geom_via
A value representing the original geometry's source. Typically used when a source geometry is clipped, simplified, or slightly modified.",

For example, if a source geometry needs to be simplified using Mapshaper, "whosonfirst" will be promoted to the `src:geom` property and `"src:geom_via":"os"` would be added to signify what original geometry source was used.

_Example: `"src:geom_via":"os"`_

## lbl
The source of a record's `lbl` properties. Valid property values are generally hand-curated, but are sometimes derived from [`Mapshaper`](https://github.com/mbloch/mapshaper). Some sources are listed in the [`whosonfirst-sources`](https://github.com/whosonfirst/whosonfirst-sources/tree/master/sources) repository.

Other iterations of the `lbl` property can include `lbl_centroid` and `centroid_lbl`; these properties are specific to the label centroid of a given feature.

_Example: `"src:lbl":"mapshaper"` and `"src:lbl_centroid_":"whosonfirst"`_

## population
The source of a record's population value, which is stored in the wof:population property. Property values are a source name.

_Example: `"src:population":"statoids"`_

## population_date
The date representing when a record's population value was catalogued. Property values follow the _YYYY-MM-DD_ format.

_Example: `"src:population_date":"2010-04-01"`_

