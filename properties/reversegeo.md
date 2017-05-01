# reversegeo

## latitude

Typically derived from [mapshaper](https://www.mapshaper.org/), `reversegeo:latitude` represents the latitude value to use when reverse geocoding a record.

## longitude

Typically derived from [mapshaper](https://www.mapshaper.org/), `reversegeo:longitude` represents the longitude value to use when reverse geocoding a record.

## polygon

This property (string value) indicates which polygon geometry to use when reverse geocoding a record.
The property value points to a polygon source, which is typically stored in an alt-geometry record. 

The `reversegeo:polygon` value is represented as **source** in the following filename example:

	85922583-alt-**source**-extras.geojson
