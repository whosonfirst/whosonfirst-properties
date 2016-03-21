# mz

## is_current

This is a "helper" property to wrap up / hide the semantics of whether something is "open" or "existing". For example, a venue that is no longer in operation or a country (like Yugoslavia) that has dissolved in to smaller nations.

## is_funky

* `-1` is unknown, or TBD (needs the love and care of a human)
* `0` is false
* `1` is true

## is_hard

Things like historic districts or similar with fixed, undisputed boundaries.

## is_landuse_aoi

## is_official

Is this considered "official" by someone or something you pay taxes to?

## max_zoom

## min_zoom

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
