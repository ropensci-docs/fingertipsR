# Indicator metadata

Outputs a data frame containing the metadata for selected indicators.
Note, this function can take up to a few minutes to run (depending on
internet connection speeds)

## Usage

``` r
indicator_metadata(
  IndicatorID = NULL,
  DomainID = NULL,
  ProfileID = NULL,
  proxy_settings = fingertips_proxy_settings(),
  path
)
```

## Arguments

- IndicatorID:

  Numeric vector, id of the indicator of interest. Also accepts "All".

- DomainID:

  Numeric vector, id of domains of interest

- ProfileID:

  Numeric vector, id of profiles of interest. Indicator polarity can
  vary between profiles therefore if using one of the comparison fields
  it is recommended to complete this field as well as IndicatorID. If
  IndicatorID is populated, ProfileID can be ignored or must be the same
  length as IndicatorID (but can contain NAs).

- proxy_settings:

  string; whether to use Internet Explorer proxy settings "default" or
  "none". Setting this manually will decrease runtime; default
  determined automatically.

- path:

  String; Fingertips API address. Function will default to the correct
  address

## Value

The metadata associated with each indicator/domain/profile identified

## See also

[`indicators`](https://docs.ropensci.org/fingertipsR/reference/indicators.md)
for indicator lookups,
[`profiles`](https://docs.ropensci.org/fingertipsR/reference/profiles.md)
for profile lookups,
[`deprivation_decile`](https://docs.ropensci.org/fingertipsR/reference/deprivation_decile.md)
for deprivation lookups,
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
[`deprivation_decile()`](https://docs.ropensci.org/fingertipsR/reference/deprivation_decile.md),
[`indicator_areatypes()`](https://docs.ropensci.org/fingertipsR/reference/indicator_areatypes.md),
[`indicator_order()`](https://docs.ropensci.org/fingertipsR/reference/indicator_order.md),
[`indicators()`](https://docs.ropensci.org/fingertipsR/reference/indicators.md),
[`indicators_unique()`](https://docs.ropensci.org/fingertipsR/reference/indicators_unique.md),
[`nearest_neighbours()`](https://docs.ropensci.org/fingertipsR/reference/nearest_neighbours.md),
[`profiles()`](https://docs.ropensci.org/fingertipsR/reference/profiles.md)

## Examples

``` r
if (FALSE) { # \dontrun{
# Returns metadata for indicator ID 90362 and 92901
indicatorIDs <- c(90362, 92901)
indicator_metadata(indicatorIDs)

# Returns metadata for the indicators within the domain 1000049
indicator_metadata(DomainID = 1000049)

# Returns metadata for the indicators within the profile with the ID 19
indicator_metadata(ProfileID = 19)} # }
```
