# Indicator order number

Outputs a tibble of indicator ids and their sequence number for the
provided domain and area type. This enables the user to order the
indicators as they are ordered on the Fingertips website.

## Usage

``` r
indicator_order(
  DomainID,
  AreaTypeID,
  ParentAreaTypeID,
  proxy_settings = fingertips_proxy_settings(),
  path
)
```

## Arguments

- DomainID:

  Numeric vector, id of domains of interest

- AreaTypeID:

  Numeric vector, the Fingertips ID for the area type. This argument
  accepts "All", which returns data for all available area types for the
  indicator(s), though this can take a long time to run

- ParentAreaTypeID:

  Numeric vector, the comparator area type for the data extracted; if
  NULL the function will use the first record for the specified
  \`AreaTypeID\` from the area_types() function

- proxy_settings:

  string; whether to use Internet Explorer proxy settings "default" or
  "none". Setting this manually will decrease runtime; default
  determined automatically.

- path:

  String; Fingertips API address. Function will default to the correct
  address

## Value

A data frame of indicator ids and sequence number

## See also

[`indicators`](https://docs.ropensci.org/fingertipsR/reference/indicators.md)
for indicators and their parent domains and profiles,
[`area_types`](https://docs.ropensci.org/fingertipsR/reference/area_types.md)
for area type and their parent mappings,
[`indicator_metadata`](https://docs.ropensci.org/fingertipsR/reference/indicator_metadata.md)
for indicator metadata,
[`profiles`](https://docs.ropensci.org/fingertipsR/reference/profiles.md)
for profile lookups,
[`deprivation_decile`](https://docs.ropensci.org/fingertipsR/reference/deprivation_decile.md)
for deprivation decile lookups,
[`category_types`](https://docs.ropensci.org/fingertipsR/reference/category_types.md)
for category lookups,
[`indicator_areatypes`](https://docs.ropensci.org/fingertipsR/reference/indicator_areatypes.md)
for indicators by area types lookups and
[`nearest_neighbours`](https://docs.ropensci.org/fingertipsR/reference/nearest_neighbours.md)
for a vector of nearest neighbours for an area

Other lookup functions:
[`area_types()`](https://docs.ropensci.org/fingertipsR/reference/area_types.md),
[`category_types()`](https://docs.ropensci.org/fingertipsR/reference/category_types.md),
[`deprivation_decile()`](https://docs.ropensci.org/fingertipsR/reference/deprivation_decile.md),
[`indicator_areatypes()`](https://docs.ropensci.org/fingertipsR/reference/indicator_areatypes.md),
[`indicator_metadata()`](https://docs.ropensci.org/fingertipsR/reference/indicator_metadata.md),
[`indicators()`](https://docs.ropensci.org/fingertipsR/reference/indicators.md),
[`indicators_unique()`](https://docs.ropensci.org/fingertipsR/reference/indicators_unique.md),
[`nearest_neighbours()`](https://docs.ropensci.org/fingertipsR/reference/nearest_neighbours.md),
[`profiles()`](https://docs.ropensci.org/fingertipsR/reference/profiles.md)

## Examples

``` r
if (FALSE) { # \dontrun{
indicator_order(DomainID = 1000049, AreaTypeID = 502, ParentAreaTypeID = 6)} # }
```
