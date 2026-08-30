# Internal function

Converts a parameter to XML

## Usage

``` r
parameter_to_xml(parameter, beauti_options)
```

## Arguments

- parameter:

  a parameter, as created by
  [`create_param`](https://docs.ropensci.org/beautier/reference/create_param.md))

- beauti_options:

  one BEAUti options object, as returned by
  [`create_beauti_options`](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)

## Value

the parameter as XML text

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

parameter_to_xml(
  create_alpha_param(id = 1),
  beauti_options = beautier::create_beauti_options()
)
#> [1] "<parameter id=\"RealParameter.1\" estimate=\"false\" name=\"alpha\">0</parameter>"

check_empty_beautier_folder()
```
