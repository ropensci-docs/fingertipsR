# Category types

Outputs a data frame of category type ids, their name (along with a
short name)

## Usage

``` r
category_types(proxy_settings = fingertips_proxy_settings(), path)
```

## Arguments

- proxy_settings:

  string; whether to use Internet Explorer proxy settings "default" or
  "none". Setting this manually will decrease runtime; default
  determined automatically.

- path:

  String; Fingertips API address. Function will default to the correct
  address

## Value

A data frame of category type ids and their descriptions

## See also

[`indicators`](https://docs.ropensci.org/fingertipsR/reference/indicators.md)
for indicator lookups,
[`profiles`](https://docs.ropensci.org/fingertipsR/reference/profiles.md)
for profile lookups,
[`deprivation_decile`](https://docs.ropensci.org/fingertipsR/reference/deprivation_decile.md)
for deprivation decile lookups,
[`area_types`](https://docs.ropensci.org/fingertipsR/reference/area_types.md)
for area type lookups,
[`indicator_areatypes`](https://docs.ropensci.org/fingertipsR/reference/indicator_areatypes.md)
for indicators by area types lookups,
[`indicators_unique`](https://docs.ropensci.org/fingertipsR/reference/indicators_unique.md)
for unique indicatorids and their names,
[`nearest_neighbours`](https://docs.ropensci.org/fingertipsR/reference/nearest_neighbours.md)
for a vector of nearest neighbours for an area and
[`indicator_order`](https://docs.ropensci.org/fingertipsR/reference/indicator_order.md)
for the order indicators are presented on the Fingertips website within
a Domain

Other lookup functions:
[`area_types()`](https://docs.ropensci.org/fingertipsR/reference/area_types.md),
[`deprivation_decile()`](https://docs.ropensci.org/fingertipsR/reference/deprivation_decile.md),
[`indicator_areatypes()`](https://docs.ropensci.org/fingertipsR/reference/indicator_areatypes.md),
[`indicator_metadata()`](https://docs.ropensci.org/fingertipsR/reference/indicator_metadata.md),
[`indicator_order()`](https://docs.ropensci.org/fingertipsR/reference/indicator_order.md),
[`indicators()`](https://docs.ropensci.org/fingertipsR/reference/indicators.md),
[`indicators_unique()`](https://docs.ropensci.org/fingertipsR/reference/indicators_unique.md),
[`nearest_neighbours()`](https://docs.ropensci.org/fingertipsR/reference/nearest_neighbours.md),
[`profiles()`](https://docs.ropensci.org/fingertipsR/reference/profiles.md)

## Examples

``` r
if (FALSE) { # \dontrun{
# Returns the deprivation category types
cats <- category_types()
cats[cats$CategoryTypeId == 1,]} # }
```
