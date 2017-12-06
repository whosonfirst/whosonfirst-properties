# nav

The `nav:latitude` and `nav:longitude` represent the centroid used for turn-by-turn navigation and "snapped" to the nearest road to the record's "entrance" (like the main entrance to a museum).

For a locality this could be city hall or the center of downtown, or the road intersection of the largest roads in the place.

This is a single navigation point for the most important entrance. Future work may add the ability to specify multiple "road access" points with metadata.

## latitude
The coordinate that specifies a navigation point's north–south position. Latitude is a decimal number between _-90.0_ and _90.0_.

## longitude
The coordinate that specifies a navigation point's east-west position. Longitude is a decimal number between _-180.0_ and _180.0_.
