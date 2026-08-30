# Internal function

Converts an \`s_param\` to XML

## Usage

``` r
s_parameter_to_xml(parameter, beauti_options)
```

## Arguments

- parameter:

  a s parameter, a numeric value. For advanced usage, use the structure
  as created by
  [`create_s_param`](https://docs.ropensci.org/beautier/reference/create_s_param.md))

- beauti_options:

  one BEAUti options object, as returned by
  [`create_beauti_options`](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)

## Value

the parameter as XML text

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
s_parameter_to_xml(
  create_s_param(id = 4, value = 1.25),
  beauti_options = create_beauti_options_v2_4()
)
#> [1] "<parameter id=\"RealParameter.4\" estimate=\"false\" name=\"S\">1.25</parameter>"
s_parameter_to_xml(
  create_s_param(id = 4, value = 1.25),
  beauti_options = create_beauti_options_v2_6()
)
#> [1] "<parameter id=\"RealParameter.4\" spec=\"parameter.RealParameter\" estimate=\"false\" name=\"S\">1.25</parameter>"
```
