# Nearest neighbours area type ids

Outputs a table of AreaTypeIDs available for the nearest_neighbour
function

## Usage

``` r
nearest_neighbour_areatypeids(proxy_settings = fingertips_proxy_settings())
```

## Arguments

- proxy_settings:

  string; whether to use Internet Explorer proxy settings "default" or
  "none". Setting this manually will decrease runtime; default
  determined automatically.

## Value

table of AreaTypeIDs

## See also

[`nearest_neighbours`](https://docs.ropensci.org/fingertipsR/reference/nearest_neighbours.md)
to access the geogaphy codes of the nearest neighbours for a locality

## Examples

``` r
if (FALSE) { # \dontrun{
nearest_neighbour_areatypeids()} # }
```
