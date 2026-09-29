# Internal function

Converts a kappa 2 parameter to XML

## Usage

``` r
parameter_to_xml_kappa_2(
  parameter,
  beauti_options = beautier::create_beauti_options()
)
```

## Arguments

- parameter:

  a kappa 2 parameter, a numeric value. For advanced usage, use the
  structure as created by
  [`create_kappa_2_param`](https://docs.ropensci.org/beautier/reference/create_kappa_2_param.md))

- beauti_options:

  one BEAUti options object, as returned by
  [`create_beauti_options`](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)

## Value

the parameter as XML text

## Author

Richèl J.C. Bilderbeek
