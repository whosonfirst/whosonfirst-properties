# reversegeo

## latitude

Typically derived from [mapshaper](https://www.mapshaper.org/), `reversegeo:latitude` represents the latitude value to use when reverse geocoding a record.

## longitude

Typically derived from [mapshaper](https://www.mapshaper.org/), `reversegeo:longitude` represents the longitude value to use when reverse geocoding a record.

## geometry

This optional string property indicates which of the feature's named geometries to use for point-in-polygon reverse geocoding tasks. The property value names a polygon [source](https://github.com/whosonfirst/whosonfirst-sources/blob/master/sources/README.md) prefix, which is typically stored in an alt-geometry file.

The `reversegeo:geometry` value is represented as `{source}` in the following filename expansion:

    85922583-alt-{source}-extras.geojson
