# Live profiles

Outputs a data frame of live profiles that data are available for in
Fingertips <http://fingertips.phe.org.uk/>

## Usage

``` r
profiles(
  ProfileID = NULL,
  ProfileName = NULL,
  proxy_settings = fingertips_proxy_settings(),
  path
)
```

## Arguments

- ProfileID:

  Numeric vector, id of profiles of interest

- ProfileName:

  Character vector, full name of profile(s)

- proxy_settings:

  string; whether to use Internet Explorer proxy settings "default" or
  "none". Setting this manually will decrease runtime; default
  determined automatically.

- path:

  String; Fingertips API address. Function will default to the correct
  address

## Value

A data frame of live profile ids and names along with their domain names
and ids.

## See also

[`area_types`](https://docs.ropensci.org/fingertipsR/reference/area_types.md)
for area type and their parent mappings,
[`indicators`](https://docs.ropensci.org/fingertipsR/reference/indicators.md)
for indicator lookups,
[`indicator_metadata`](https://docs.ropensci.org/fingertipsR/reference/indicator_metadata.md)
for indicator metadata,
[`deprivation_decile`](https://docs.ropensci.org/fingertipsR/reference/deprivation_decile.md)
for deprivation decile lookups,
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
[`indicator_metadata()`](https://docs.ropensci.org/fingertipsR/reference/indicator_metadata.md),
[`indicator_order()`](https://docs.ropensci.org/fingertipsR/reference/indicator_order.md),
[`indicators()`](https://docs.ropensci.org/fingertipsR/reference/indicators.md),
[`indicators_unique()`](https://docs.ropensci.org/fingertipsR/reference/indicators_unique.md),
[`nearest_neighbours()`](https://docs.ropensci.org/fingertipsR/reference/nearest_neighbours.md)

## Examples

``` r
if (FALSE) { # \dontrun{
# Returns a complete data frame of domains and their profiles
profiles()

# Returns a data frame of all of the domains in the Public Health Outcomes Framework
profiles(ProfileName = "Public Health Outcomes Framework")} # }
```
