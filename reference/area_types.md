# Area types

Outputs a data frame of area type ids, their descriptions, and how they
map to parent area types. To understand more on mappings of areas, see
the Where to start section of the Life Expectancy vignette.

## Usage

``` r
area_types(
  AreaTypeName = NULL,
  AreaTypeID = NULL,
  ProfileID = NULL,
  proxy_settings = fingertips_proxy_settings(),
  path
)
```

## Arguments

- AreaTypeName:

  Character vector, description of the area type; default is NULL

- AreaTypeID:

  Numeric vector, the Fingertips ID for the area type; default is NULL

- ProfileID:

  Numeric vector, id of profiles of interest

- proxy_settings:

  string; whether to use Internet Explorer proxy settings "default" or
  "none". Setting this manually will decrease runtime; default
  determined automatically.

- path:

  String; Fingertips API address. Function will default to the correct
  address

## Value

A data frame of area type ids and their descriptions

## See also

[`indicators`](https://docs.ropensci.org/fingertipsR/reference/indicators.md)
for indicator lookups,
[`profiles`](https://docs.ropensci.org/fingertipsR/reference/profiles.md)
for profile lookups,
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
[`category_types()`](https://docs.ropensci.org/fingertipsR/reference/category_types.md),
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
# Returns a data frame with all levels of area and how they map to one another
area_types()

# Returns a data frame of county and unitary authority mappings
area_types("counties")

# Returns a data frame of both counties, district
# and unitary authorities and their respective mappings
areas <- c("counties", "district")
area_types(areas)

# Uses AreaTypeID to filter area types
area_types(AreaTypeID = 7)} # }
```
