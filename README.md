# whosonfirst-properties

Where things come from in Who's On First.

Click [here](properties/) to see a full list of Who's On First property prefixes.

### Adding a new property

1. Create a new property .json file using the [template file](properties_template.json).
2. Fill out all required properties and optional properties, if available.

### Properties

While a property .json file in the `whosonfirst-properties` repository does not require all properties listed below, the more information we are able to gather about a property, the better. When adding a new property, please provide as much current, available information about that specific property as possible.

* `"id":` A unique numeric integer identifier, typically derived from [Brooklyn Integers](https://www.brooklynintegers.com) (_integer, required property_).

* `"name":` The name of a given property. For example, the `qs:name` property would be `name` to represent the "name" property derived from "Quattroshapes" (_string, required property_).

* `"prefix":` The [source](https://www.github.com/whosonfirst/whosonfirst-sources) that Who's On First derived this property from. For example, the `qs:name` property prefix would be `qs` to represent "Quattroshapes". This value is typically two to ten characters in length (_string, required property_) and must be unique (not shared with another source).

* `"description":` A one to two sentence description of the property value (_string, optional property_).

* `"type":` The property value type - string, list, dictionary, float, or integer.

## See also

* https://github.com/whosonfirst
* https://github.com/whosonfirst/whosonfirst-data/issues/100