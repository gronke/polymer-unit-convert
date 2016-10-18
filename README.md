Polymer Element: unit-convert
=============================

Converts input data from a known unit to another (e.g. `meters -> miles`, `hours -> minutes`). Can also deal with complex units and abbreviations like `km/h -> mph`.

Supported Units
---------------

#### Distance

- meter
- mile
- nautical_mile
- yard

#### Time

- hour

Abbreviations
-------------

#### Simple

| Abbreviation | Expansion       |
| ------------ | --------------- |
| `km`         | `kilometer`     |
| `m`          | `meter`         |
| `kt`         | `knots`         |
| `h`          | `hour`          |
| `min`        | `minute`        |
| `s`          | `second`        |
| `sec`        | `second`        |
| `n.m.`       | `nautical_mile` |
| `yd.`        | `yard           |

#### Complex

| Abbreviation | Expansion            |
| ------------ | -------------------- |
| `mph`        | `mile/hour`          |
| `knots`      | `nautical_mile/hour` |

Dependencies
------------

Depends on [polymer-unit-prefix](https://github.com/gronke/polymer-unit-prefix) that handles the quantization of units like milli-/mi

Examples
--------

#### Convert from hours to minutes

```html
<unit-convert from="hour" to="minute" value="24" result="{{result}}" />
<!-- result: 1440 -->
```

#### Convert complex unit mph to km/h

```html
<unit-convert-complex from="mph" to="km/h" value="70" decimals="2" result="{{result}}" />
<!-- result: 112.65 -->
```
