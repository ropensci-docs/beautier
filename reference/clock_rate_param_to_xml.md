# Internal function

Converts a `clockRate` parameter to XML

## Usage

``` r
clock_rate_param_to_xml(
  clock_rate_param,
  beauti_options = beautier::create_beauti_options()
)
```

## Arguments

- clock_rate_param:

  a `clockRate` parameter, a numeric value, as created by
  [create_clock_rate_param](https://docs.ropensci.org/beautier/reference/create_clock_rate_param.md)

- beauti_options:

  one BEAUti options object, as returned by
  [`create_beauti_options`](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)

## Value

the parameter as XML text

## Author

Richèl J.C. Bilderbeek
