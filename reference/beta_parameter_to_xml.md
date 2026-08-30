# Internal function

Converts a beta parameter to XML

## Usage

``` r
beta_parameter_to_xml(
  beta_parameter,
  beauti_options = beautier::create_beauti_options()
)
```

## Arguments

- beta_parameter:

  a beta parameter, as created by
  [create_beta_param](https://docs.ropensci.org/beautier/reference/create_beta_param.md)

- beauti_options:

  one BEAUti options object, as returned by
  [`create_beauti_options`](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)

## Value

the parameter as XML text

## Author

Richèl J.C. Bilderbeek
