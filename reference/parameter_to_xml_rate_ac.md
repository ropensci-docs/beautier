# Internal function

Converts a 'rate AC' parameter to XML

## Usage

``` r
parameter_to_xml_rate_ac(
  parameter,
  beauti_options = beautier::create_beauti_options(),
  which_name = "state_node"
)
```

## Arguments

- parameter:

  a 'rate AC' parameter, a numeric value. For advanced usage, use the
  structure as created by
  [`create_rate_ac_param`](https://docs.ropensci.org/beautier/reference/create_rate_ac_param.md))

- beauti_options:

  one BEAUti options object, as returned by
  [`create_beauti_options`](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)

- which_name:

  the name, can be `state_node` or `rate_name`

## Value

the parameter as XML text

## Author

Richèl J.C. Bilderbeek
