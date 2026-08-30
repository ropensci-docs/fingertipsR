# Nearest neighbours

Outputs a character vector of similar areas for a given area.  
  
**Details**  

- For new upper tier local authorities (post 4/23) the [NHSE Nearest
  Neighbours Model](https://github.com/NHSDigital/ASC_LA_Peer_Groups) is
  used.

- All other local authorities types (lower tier and older upper tier)
  use the [CIPFA's Nearest Neighbours
  Model](https://www.cipfastats.net/resources/nearestneighbours/). Older
  local authority geography types will use older versions of the model.

- Similar areas for Clinical Commissioning Groups are based on [NHS
  England's similar CCG explorer
  tool](https://www.england.nhs.uk/publication/similar-10-ccg-explorer-tool/).

- Currently the function does not have the ability to use the method
  from the [Children's services statistical neighbour benchmarking
  tool](https://www.gov.uk/government/publications/local-authority-interactive-tool-lait).

## Usage

``` r
nearest_neighbours(
  AreaCode,
  AreaTypeID,
  proxy_settings = fingertips_proxy_settings(),
  path
)
```

## Arguments

- AreaCode:

  Character vector, ONS area code of area of interest

- AreaTypeID:

  AreaTypeID of the nearest neighbours (see
  [`nearest_neighbour_areatypeids`](https://docs.ropensci.org/fingertipsR/reference/nearest_neighbour_areatypeids.md))
  for available IDs

- proxy_settings:

  string; whether to use Internet Explorer proxy settings "default" or
  "none". Setting this manually will decrease runtime; default
  determined automatically.

- path:

  String; Fingertips API address. Function will default to the correct
  address

## Value

A character vector of area codes

## See also

[`nearest_neighbour_areatypeids`](https://docs.ropensci.org/fingertipsR/reference/nearest_neighbour_areatypeids.md)
for the AreaTypeIDs available for this function

Other lookup functions:
[`area_types()`](https://docs.ropensci.org/fingertipsR/reference/area_types.md),
[`category_types()`](https://docs.ropensci.org/fingertipsR/reference/category_types.md),
[`deprivation_decile()`](https://docs.ropensci.org/fingertipsR/reference/deprivation_decile.md),
[`indicator_areatypes()`](https://docs.ropensci.org/fingertipsR/reference/indicator_areatypes.md),
[`indicator_metadata()`](https://docs.ropensci.org/fingertipsR/reference/indicator_metadata.md),
[`indicator_order()`](https://docs.ropensci.org/fingertipsR/reference/indicator_order.md),
[`indicators()`](https://docs.ropensci.org/fingertipsR/reference/indicators.md),
[`indicators_unique()`](https://docs.ropensci.org/fingertipsR/reference/indicators_unique.md),
[`profiles()`](https://docs.ropensci.org/fingertipsR/reference/profiles.md)

## Examples

``` r
if (FALSE) { # \dontrun{
nearest_neighbours(AreaCode = "E09000004", AreaTypeID = 502)} # }
```
