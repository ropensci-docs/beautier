# Internal function

Converts a mu parameter to XML

## Usage

``` r
parameter_to_xml_mu(
  parameter,
  beauti_options = beautier::create_beauti_options()
)
```

## Arguments

- parameter:

  a mu parameter, a numeric value. For advanced usage, use the structure
  as created by
  [`create_mu_param`](https://docs.ropensci.org/beautier/reference/create_mu_param.md))

- beauti_options:

  one BEAUti options object, as returned by
  [`create_beauti_options`](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)

## Value

the parameter as XML text

## Author

Richèl J.C. Bilderbeek
