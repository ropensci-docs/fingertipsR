# Deprivation deciles

Outputs a data frame allocating deprivation decile to area code based on
the Indices of Multiple Deprivation (IMD) produced by Department of
Communities and Local Government

## Usage

``` r
deprivation_decile(
  AreaTypeID,
  Year = 2019,
  proxy_settings = fingertips_proxy_settings(),
  path
)
```

## Arguments

- AreaTypeID:

  Integer value; this function uses the IndicatorIDs 91872, 93275 and
  93553, please use the
  [`indicator_areatypes()`](https://docs.ropensci.org/fingertipsR/reference/indicator_areatypes.md)
  function to see what AreaTypeIDs are available

- Year:

  Integer value, representing the year of IMD release to be applied,
  limited to 2015 or 2019

- proxy_settings:

  string; whether to use Internet Explorer proxy settings "default" or
  "none". Setting this manually will decrease runtime; default
  determined automatically.

- path:

  String; Fingertips API address. Function will default to the correct
  address

## Value

A lookup table providing deprivation decile and area code

## Details

This function uses the fingertips_data function to filter for the Index
of multiple deprivation score for the year and area supplied, and
returns the area code, along with the score and the deprivation decile,
which is calculated using the ntile function from dplyr

## See also

[`indicators`](https://docs.ropensci.org/fingertipsR/reference/indicators.md)
for indicator lookups,
[`profiles`](https://docs.ropensci.org/fingertipsR/reference/profiles.md)
for profile lookups,
[`indicator_metadata`](https://docs.ropensci.org/fingertipsR/reference/indicator_metadata.md)
for the metadata for each indicator,
[`area_types`](https://docs.ropensci.org/fingertipsR/reference/area_types.md)
for area types and their parent mappings,
[`category_types`](https://docs.ropensci.org/fingertipsR/reference/category_types.md)
for category lookups,
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
[`category_types()`](https://docs.ropensci.org/fingertipsR/reference/category_types.md),
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
# Return 2019 deprivation scores for Upper tier local authorities (post 4/23)
deprivation_decile(502, 2019)} # }
```
