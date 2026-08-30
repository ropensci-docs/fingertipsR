# High level statistics on Fingertips data

A sentence that summarises the number of indicators, unique indicators
and profiles

## Usage

``` r
fingertips_stats(proxy_settings = fingertips_proxy_settings())
```

## Arguments

- proxy_settings:

  string; whether to use Internet Explorer proxy settings "default" or
  "none". Setting this manually will decrease runtime; default
  determined automatically.

## Value

A string that summarises the high level statistics of indicators and
profiles in Fingertips

## Examples

``` r
if (FALSE) { # \dontrun{
# Returns a sentence describing number of indicators and profiles in Fingertips
fingertips_stats()} # }
```
