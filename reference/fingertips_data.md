# Fingertips data

Outputs a data frame of data from
[Fingertips](https://fingertips.phe.org.uk/). Note, this function can
take up to a few minutes to run (depending on internet connection speeds
and parameter selection).

## Usage

``` r
fingertips_data(
  IndicatorID = NULL,
  AreaCode = NULL,
  DomainID = NULL,
  ProfileID = NULL,
  AreaTypeID,
  ParentAreaTypeID = NULL,
  categorytype = FALSE,
  rank = FALSE,
  url_only = FALSE,
  proxy_settings = fingertips_proxy_settings(),
  path
)
```

## Arguments

- IndicatorID:

  Numeric vector, id of the indicator of interest

- AreaCode:

  Character vector, ONS area code of area of interest

- DomainID:

  Numeric vector, id of domains of interest

- ProfileID:

  Numeric vector, id of profiles of interest. Indicator polarity can
  vary between profiles therefore if using one of the comparison fields
  it is recommended to complete this field as well as IndicatorID. If
  IndicatorID is populated, ProfileID can be ignored or must be the same
  length as IndicatorID (but can contain NAs).

- AreaTypeID:

  Numeric vector, the Fingertips ID for the area type. This argument
  accepts "All", which returns data for all available area types for the
  indicator(s), though this can take a long time to run

- ParentAreaTypeID:

  Numeric vector, the comparator area type for the data extracted; if
  NULL the function will use the first record for the specified
  \`AreaTypeID\` from the area_types() function

- categorytype:

  TRUE or FALSE, determines whether the final table includes
  categorytype data where it exists. Default to FALSE

- rank:

  TRUE or FALSE, the rank of the area compared to other areas for that
  combination of indicator, sex, age, categorytype and category along
  with the indicator's polarity. 1 is lowest NAs will be bottom and ties
  will return the average position. The total count of areas with a
  non-NA value are returned also in AreaValuesCount

- url_only:

  TRUE or FALSE, return only the url of the api call as a character
  vector

- proxy_settings:

  string; whether to use Internet Explorer proxy settings "default" or
  "none". Setting this manually will decrease runtime; default
  determined automatically.

- path:

  String; Fingertips API address. Function will default to the correct
  address

## Value

A data frame of data extracted from the Fingertips API

## Details

Note, polarity of an indicator is not automatically returned (eg,
whether a low value is good, bad or neither). Use the rank field for
this to be returned (though it adds a lot of time to the query)

Some indicators may have different comparisons due to indicator polarity
differences between profiles on the website. It is recommended to check
the website to ensure consistency between your data extract here and the
polarity required

## See also

Other data extract functions:
[`fingertips_redred()`](https://docs.ropensci.org/fingertipsR/reference/fingertips_redred.md)

## Examples

``` r
if (FALSE) { # \dontrun{
# Returns data for the two selected domains at county and unitary authority geography
doms <- c(1000049,1938132983)
fingdata <- fingertips_data(DomainID = doms, AreaTypeID = 502)

# Returns data at local authority district geography (AreaTypeID = 501)
# for the indicator with the id 22401
fingdata <- fingertips_data(22401, AreaTypeID = 501)

# Returns data for all available area types for an indicator
fingdata <- fingertips_data(90362, AreaTypeID = "All")} # }
```
