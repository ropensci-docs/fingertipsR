# Retrieve data from a given Fingertips API url

Retrieve data from a given Fingertips API url

## Usage

``` r
get_fingertips_api(
  api_path,
  content_type = "text",
  col_types,
  proxy_settings = fingertips_proxy_settings()
)
```

## Arguments

- api_path:

  string; the API url to retrieve data from

- content_type:

  string; "text" or "parsed"

- col_types:

  character; vector of column classes

- proxy_settings:

  string; whether to use Internet Explorer proxy settings ("default") or
  "none"

## Examples

``` r
df <- get_fingertips_api(
  api_path = paste0(
    fingertips_endpoint(),
    "/area/parent_areas?child_area_code=E12000005&parent_area_type_ids=15"))
#> Error: The API is currently unavailable.
```
