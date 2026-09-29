# Internal function

Converts a kappa 1 parameter to XML

## Usage

``` r
parameter_to_xml_kappa_1(
  parameter,
  beauti_options = beautier::create_beauti_options()
)
```

## Arguments

- parameter:

  a kappa 1 parameter, a numeric value. For advanced usage, use the
  structure as created by
  [`create_kappa_1_param`](https://docs.ropensci.org/beautier/reference/create_kappa_1_param.md))

- beauti_options:

  one BEAUti options object, as returned by
  [`create_beauti_options`](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)

## Value

the parameter as XML text

## Author

Richèl J.C. Bilderbeek
