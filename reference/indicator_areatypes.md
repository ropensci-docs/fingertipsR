# Area types by indicator

Outputs a data frame of indicator ids and the area type ids that exist
for that indicator

## Usage

``` r
indicator_areatypes(
  IndicatorID,
  AreaTypeID,
  proxy_settings = fingertips_proxy_settings(),
  path
)
```

## Arguments

- IndicatorID:

  integer; the Indicator ID (can be ignored or of length 1). Takes
  priority over AreaTypeID if both are entered

- AreaTypeID:

  integer; the Area Type ID (can be ignored or of length 1)

- proxy_settings:

  string; whether to use Internet Explorer proxy settings "default" or
  "none". Setting this manually will decrease runtime; default
  determined automatically.

- path:

  String; Fingertips API address. Function will default to the correct
  address

## Value

A data frame of indicator ids and area type ids

## See also

[`indicators`](https://docs.ropensci.org/fingertipsR/reference/indicators.md)
for indicator lookups,
[`profiles`](https://docs.ropensci.org/fingertipsR/reference/profiles.md)
for profile lookups,
[`deprivation_decile`](https://docs.ropensci.org/fingertipsR/reference/deprivation_decile.md)
for deprivation decile lookups,
[`area_types`](https://docs.ropensci.org/fingertipsR/reference/area_types.md)
for area type lookups,
[`category_types`](https://docs.ropensci.org/fingertipsR/reference/category_types.md)
for category type lookups,
[`indicators_unique`](https://docs.ropensci.org/fingertipsR/reference/indicators_unique.md)
for unique indicatorids and their names,
[`nearest_neighbours`](https://docs.ropensci.org/fingertipsR/reference/nearest_neighbours.md)
for a vector of nearest neighbours for an area and
[`indicator_order`](https://docs.ropensci.org/fingertipsR/reference/indicator_order.md)
for the order indicators are presented on the Fingertips website within
a Domain

Other lookup functions:
[`area_types()`](https://docs.ropensci.org/fingertipsR/reference/area_types.md),
[`category_types()`](https://docs.ropensci.org/fingertipsR/reference/category_types.md),
[`deprivation_decile()`](https://docs.ropensci.org/fingertipsR/reference/deprivation_decile.md),
[`indicator_metadata()`](https://docs.ropensci.org/fingertipsR/reference/indicator_metadata.md),
[`indicator_order()`](https://docs.ropensci.org/fingertipsR/reference/indicator_order.md),
[`indicators()`](https://docs.ropensci.org/fingertipsR/reference/indicators.md),
[`indicators_unique()`](https://docs.ropensci.org/fingertipsR/reference/indicators_unique.md),
[`nearest_neighbours()`](https://docs.ropensci.org/fingertipsR/reference/nearest_neighbours.md),
[`profiles()`](https://docs.ropensci.org/fingertipsR/reference/profiles.md)

## Examples

``` r
if (FALSE) { # \dontrun{
indicator_areatypes(IndicatorID = 90362)} # }
```
