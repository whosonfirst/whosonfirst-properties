# label

See also: [whosonfirst-names](https://github.com/whosonfirst/whosonfirst-names).

## {lang}_x_colloquial

The colloquial, informal label for a place (inclusive of hierarchy).

_Example: eng_x_colloquial_

```
"label:eng_x_colloquial": "Fairfax, Virginia, USA"
```


## {lang}_x_colloquial_abbreviation

The colloquial, informal abbreviation for a place (inclusive of hierarchy).

_Example: eng_x_colloquial_abbreviation_

```
"label:eng_x_colloquial_abbreviation": "SFO, California, USA"
```


## {lang}_x_historical

The historical label for a place (inclusive of hierarchy).

_Example: zho_x_historical_

```
"label:eng_x_historical": "Yerba Buena, California, USA"
```

## {lang}_x_preferred

The fully qualified "preferred" label for a place (inclusive of hierarchy), in practice a single element list. Used in Pelias and to generate language-specific map labels. The `label:{lang}_x_preferred` property takes precedence over `wof:label`.

_Example: kor_x_preferred_

```
"label:eng_x_preferred": "Fairfax city, Virginia, USA"
```

## {lang}_x_preferred_abbreviation

The "preferred" label for a place name (exclusive of hierarchy), in practice a single element list. Used in Pelias and to generate language-specific map labels.

_Example: kor_x_preferred_abbreviation_

```
"label:eng_x_preferred_abbreviation": ["U.S.A."]
"label:eng_x_preferred_abbreviation": ["Calif."]
"label:eng_x_preferred_abbreviation": ["Va."]
"label:eng_x_preferred_abbreviation": ["Maine"]
"label:eng_x_preferred_abbreviation": ["Ore."]
"label:eng_x_preferred_abbreviation": ["S.F. Int'l Airport"]
```


## {lang}_x_preferred_disambiguation

The "preferred" disambiguation label for a place (exclusive of hierarchy), in practice a single element list. Either append the feature's placetype or append the parent's name in parenthesis.

_Example: kor_x_preferred_disambiguation_

```
"label:eng_x_preferred_disambiguation": ["Fairfax city"]
"label:eng_x_preferred_disambiguation": ["Fairfax county"]
"label:eng_x_preferred_disambiguation": ["Portland (Maine)"]
"label:eng_x_preferred_disambiguation": ["Portland (Oregon)"]
```

## {lang}_x_preferred_longname

The preferred longname label for a place (inclusive of placetype), in practice a single element list. Always append the feature's placetype to the preferred name. We generally prefer the transliterated placetype (eg Oblast) over the translated placetype (Territory), and the placetype should be Title Case. In the case of California we'd expect this value to be California State instead of State of California.

_Example: eng_x_preferred_longname_

```
"label:eng_x_preferred_longname": ["Tomskaja Oblast"]
"label:eng_x_preferred_longname": ["Almeria Province"]
"label:eng_x_preferred_longname": ["California State"]
```

## {lang}_x_preferred_placetype

A feature's "preferred" placetype label (exclusive of place name and hierarchy), in practice a single element list. While `wof:placetype` is an enumerated value, this localized value is a string.

_Example: kor_x_preferred_placetype_

```
"label:eng_x_preferred_placetype": ["parish"]
"label:eng_x_preferred_placetype": ["local government area"]
```

## {lang}_x_preferred_shortcode

A feature's "preferred" localized shortcode that takes precedence over `wof:shortcode` (exclusive of place name and hierarchy), in practice a single element list. 

A short alphabetic code, preferring 3-characters for `country` (e.g. **USA**), 2-characters for `region` (e.g. **CA**), and either 3-character or 2-character for `county` (e.g. **HUM** or **HU**) placetypes. Other placetypes like `venue` can also have shortcodes but their length is not standardized, and they may contain alphanumeric values.

_Example: eng_x_preferred_shortcode_ 

```
"label:eng_x_preferred_shortcode": ["US"]
"label:eng_x_preferred_shortcode": ["CA"]
"label:eng_x_preferred_shortcode": ["ME"]
"label:eng_x_preferred_shortcode": ["OR"]
"label:eng_x_preferred_shortcode": ["VA"]
"label:eng_x_preferred_shortcode": ["SFO"]
"label:eng_x_preferred_shortcode": ["SF"]
"label:eng_x_preferred_shortcode": ["HUM"]
```

_WARNING: do not confuse `{lang}_x_preferred_shortcode` and `wof:shortcode` properties with the deprecated `wof:abbreviation` or `wof:country_alpha3` properties._

## {lang}_x_unknown

Uncommon "unclassified" labels used for a place (inclusive of hierarchy).

_Example: nep_x_unknown_

## {lang}_x_variant

Uncommon "variant" labels used for a place (inclusive of hierarchy). Used in mapping and geocoding software and to generate language-specific map labels.

_Example: deu_x_variant_

## {lang}_x_variant_abbreviation

Uncommon "variant" abbreviations used for a place (exclusive of hierarchy).

_Example: deu_x_variant_abbreviation_

```
"label:eng_x_variant_abbreviation": ["S.F.O. Int'l Airport"]
"label:eng_x_variant_abbreviation": ["S.F."]
"label:eng_x_variant_abbreviation": ["USA", "U.S."]
"label:eng_x_variant_abbreviation": ["Cali."]
```

## {lang}_x_variant_disambiguation


Uncommon "variant" disambiguation labels for a place (exclusive of hierarchy). Either append the feature's placetype or append the parent's name in parenthesis.

_Example: deu_x_variant_disambiguation_

```
"label:eng_x_variant_disambiguation": ["Portland (ME)"]
"label:eng_x_variant_disambiguation": ["Portland (OR)", "Portland (Ore.)"]
```

## {lang}_x_variant_longname

The variant longname labels for a place (inclusive of placetype), as a multi element list. Always append the feature's placetype to the preferred name. The placetype should be Title Case and not include the value of the preferred longname. Common values can include the translated placetype (Territory) instead of the transliterated placetype (eg Oblast).

_Example: eng_x_variant_longname_

```
"label:eng_x_variant_longname": ["Tomskaja Territory, Tomsk Territory"]
"label:eng_x_variant_longname": ["Kronoberg county"]
```


## {lang}_x_variant_placetype

Uncommon "variant" placetype labels (exclusive of hierarchy). While `wof:placetype` is an enumerated value, this value is a string value.

_Example: deu_x_variant_placetype_

```
"label:eng_x_variant_placetype": ["Parish"]
"label:eng_x_variant_placetype": ["LGA", "lga", "L.G.A.", "l.g.a.", "local gov't area"]
```

## {lang}_x_variant_shortcode

Uncommon localized shortcodes (exclusive of hierarchy).

A short alphabetic code, preferring 3-characters for `country` (e.g. **USA**), 2-characters for `region` (e.g. **CA**), and either 3-character or 2-character for `county` (e.g. **HUM** or **HU**) placetypes. Other placetypes like `venue` can also have shortcodes but their length is not standardized, and they may contain alphanumeric values.

_Example: label:deu_x_variant_shortcode_

```
"label:eng_x_variant_shortcode": ["KSFO"]
"label:eng_x_variant_shortcode": ["HU"]
```
