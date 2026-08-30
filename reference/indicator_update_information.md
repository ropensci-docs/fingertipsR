# Indicator update information

Outputs a data frame which provides a date of when an indicator was last
update

## Usage

``` r
indicator_update_information(
  IndicatorID,
  ProfileID = NULL,
  proxy_settings = fingertips_proxy_settings(),
  path
)
```

## Arguments

- IndicatorID:

  Integer, id of the indicators of interest

- ProfileID:

  Integer (optional), whether to restrict the indicators to a particular
  profile

- proxy_settings:

  string; whether to use Internet Explorer proxy settings "default" or
  "none". Setting this manually will decrease runtime; default
  determined automatically.

- path:

  String; Fingertips API address. Function will default to the correct
  address

## Value

The date of latest data update for selected indicators

## Examples

``` r
if (FALSE) { # \dontrun{
# Returns metadata for indicator ID 90362 and 92901
indicatorIDs <- c(90362, 92901)
indicator_update_information(indicatorIDs)} # }
```
