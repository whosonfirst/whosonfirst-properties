# lbl
Most properties listed below contain explicit, curated values.

## bbox
The `lbl:bbox` is the bounding box area used purely for map labelling and search purposes, and is usually smaller than the `geom:bbox`.

The `lbl:bbox` is human-generated (not derived from Mapshaper).


_Format: "minx, miny, maxx, maxy"_

## latitude
The coordinate that specifies a label's north–south position. Latitude is a decimal number between _-90.0_ and _90.0_.

## longitude
The coordinate that specifies a label's east-west position. Longitude is a decimal number between _-180.0_ and _180.0_.

## min_zoom
When the feature's label should first appear. Float values (though in practice mosts are integer values) that match to web map zoom schema. Common range is _0.0_ to _18.0_, though they can be greater.

## max_zoom
When the feature's label should be removed (or switched to a different representation like exterior ring labels). Float values (though in practice mosts are integer values) that match to web map zoom schema. Common range is _0.0_ to _18.0_, though they can be greater.