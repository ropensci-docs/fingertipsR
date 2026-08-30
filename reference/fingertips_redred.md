# Red significance and red trend

Filters data returned by the fingertips_data function for values for
areas that are trending statistically significantly worse and the spot
value is significantly worse than the comparator (England or Parent)
value in the latest year of that indicator

## Usage

``` r
fingertips_redred(Comparator = "England", ...)
```

## Arguments

- Comparator:

  String, either "England" or "Parent" to determine which field to
  compare the spot value significance to

- ...:

  Parameters provided to fingertips_data()

## Value

A data frame of data extracted from the Fingertips API

## See also

Other data extract functions:
[`fingertips_data()`](https://docs.ropensci.org/fingertipsR/reference/fingertips_data.md)

## Examples

``` r
if (FALSE) { # \dontrun{
# Returns data for the two selected domains at county and unitary authority geography
reddata <- fingertips_redred(ProfileID = 26, AreaTypeID = 502)} # }
```
