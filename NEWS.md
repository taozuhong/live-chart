# 1.6.0

## API

* add `chart.add_unaware_timestamp_collection_by_index(int serie_index, Gee.Collection<double?> collection, int timespan_between_value)` method, to add your own data collection to a serie given its `serie_index` (unlike `chart.add_unaware_timestamp_collection()` which takes the serie as argument)

## Fixes

* Crash when the max value of a serie is 0
* Crash when the chart widget is realized before any data is added

# 1.5.1

## API

* add `chart.add_value_by_index(int serie_index, double value)` method, to add a value to a serie given its `serie_index` (unlike `chart.add_value()` which takes the serie as argument)

# 1.5.0

## New feature

* Configure legend font

```vala
var chart = new LiveChart.Chart(config);
var legend = vhart.legend;

legend.labels.font.size = 12;                      // uint8     In pixels
legend.labels.font.color = {1.0, 0.0, 0.0, 1.0};   // Gdk.RGBA
legend.labels.font.weight = Cairo.FontWeight.BOLD; // Cairo.FontWeight
legend.labels.font.slant =  Cairo.FontSlant.ITALIC;// Cairo.FontSlant
```

* Configure axis labels font
  
```vala
var labels;

labels = config.x_axis.labels;
//or
labels = config.y_axis.labels;

labels.font.size = 12;                      // uint8     In pixels
labels.font.color = {1.0, 0.0, 0.0, 1.0};   // Gdk.RGBA
labels.font.weight = Cairo.FontWeight.BOLD; // Cairo.FontWeight
labels.font.slant =  Cairo.FontSlant.ITALIC;// Cairo.FontSlant
```

* Improved legend labels vertical alignement

# 1.4.0

## New feature

* [70370e](https://github.com/lcallarec/live-chart/commit/70370e76559ee92d4feea58cd8ced0c98d9da95d) Import your own timestamp unaware data collection

# 1.3.3

## API

* [e36b6b](https://github.com/lcallarec/live-chart/commit/e36b6b59d178d8d72316aed040cfc5fa074b7b5a) Can now retrieve underlying `Values` object from `Serie` 
* [6fc2f4](https://github.com/lcallarec/live-chart/commit/6fc2f4451879fb05a511644cc8807a3bb8de4d0f) Can now clear `Values` object from `Serie`

# 1.3.2

## New feature

* Open LiveChart Valadoc to public

## Fixes

* [c77e2c](https://github.com/lcallarec/live-chart/commit/c77e2cbb0dcf7d343806408f3ed52ae9090f01a3) Wrong default Path colors

## Misc

* Improve documentation

## Internals

* Merge source files

# 1.3.1

## Misc

* Create Valadoc

## Internals

* Merge source files
* Remove obsolete Makefile


# 1.3.0

## New features
* [8fe363](https://github.com/lcallarec/live-chart/commit/8fe363eb6aba8acfd00ae3a57108477fdda6b3a1) Configurate main axis (abscissa and ordinate lines) color, line width and dash style

## API change

* [79e96b](https://github.com/lcallarec/live-chart/commit/79e96bf43106d489efa290f57d3575a447ece0aa) Chart config is now a public chart attribute

## Internals

* [db7766](https://github.com/lcallarec/live-chart/commit/db7766b5b5dbf4ca0cb7ea0c9cc474d5231cd36e) Axis class type is replaced with more convenient Path class.

## Misc

* Improve documentation

# 1.2.1

# Internal changes

* [24258e](https://github.com/lcallarec/live-chart/commit/24258e44df775fad92aa432d26cccf9f6bc01160) Internally, structs Axis and Labels are replaced by classes 
* Improve tests

# 1.2.0

## New features

* Configurate guidelines color, line width and dash style
* Guidelines can be hidden independently from the whole grid
* Main axes (abscissa and ordinate lines) can be hidden independently from the whole grid
* Time and value labels can be hidden
* Auto padding configuration is not `nullable`, use `LiveChart.AutoPadding.NONE` instead
* Add license, release badges to README

# 1.1.0

## New features

* Grid and legend can be hidden