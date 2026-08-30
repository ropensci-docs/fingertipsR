# Live indicators

Outputs a data frame of indicators (their id and name only). Note, this
function can take up to a few minutes to run (depending on internet
connection speeds)

## Usage

``` r
indicators_unique(
  ProfileID = NULL,
  DomainID = NULL,
  proxy_settings = fingertips_proxy_settings(),
  path
)
```

## Arguments

- ProfileID:

  Numeric vector, id of profiles of interest

- DomainID:

  Numeric vector, id of domains of interest

- proxy_settings:

  string; whether to use Internet Explorer proxy settings "default" or
  "none". Setting this manually will decrease runtime; default
  determined automatically.

- path:

  String; Fingertips API address. Function will default to the correct
  address

## Value

A data frame of indicator ids and names

## See also

[`indicators`](https://docs.ropensci.org/fingertipsR/reference/indicators.md)
for indicators and their parent domains and profiles,
[`area_types`](https://docs.ropensci.org/fingertipsR/reference/area_types.md)
for area type and their parent mappings,
[`indicator_metadata`](https://docs.ropensci.org/fingertipsR/reference/indicator_metadata.md)
for indicator metadata and
[`profiles`](https://docs.ropensci.org/fingertipsR/reference/profiles.md)
for profile lookups and
[`deprivation_decile`](https://docs.ropensci.org/fingertipsR/reference/deprivation_decile.md)
for deprivation decile lookups and
[`category_types`](https://docs.ropensci.org/fingertipsR/reference/category_types.md)
for category lookups,
[`indicator_areatypes`](https://docs.ropensci.org/fingertipsR/reference/indicator_areatypes.md)
for indicators by area types lookups and
[`indicator_order`](https://docs.ropensci.org/fingertipsR/reference/indicator_order.md)
for the order indicators are presented on the Fingertips website within
a Domain

Other lookup functions:
[`area_types()`](https://docs.ropensci.org/fingertipsR/reference/area_types.md),
[`category_types()`](https://docs.ropensci.org/fingertipsR/reference/category_types.md),
[`deprivation_decile()`](https://docs.ropensci.org/fingertipsR/reference/deprivation_decile.md),
[`indicator_areatypes()`](https://docs.ropensci.org/fingertipsR/reference/indicator_areatypes.md),
[`indicator_metadata()`](https://docs.ropensci.org/fingertipsR/reference/indicator_metadata.md),
[`indicator_order()`](https://docs.ropensci.org/fingertipsR/reference/indicator_order.md),
[`indicators()`](https://docs.ropensci.org/fingertipsR/reference/indicators.md),
[`nearest_neighbours()`](https://docs.ropensci.org/fingertipsR/reference/nearest_neighbours.md),
[`profiles()`](https://docs.ropensci.org/fingertipsR/reference/profiles.md)

## Examples

``` r
if (FALSE) { # \dontrun{
indicators_unique(ProfileID = 21)} # }
```
