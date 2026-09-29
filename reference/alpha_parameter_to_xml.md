# Internal function

Converts an alpha parameter to XML

## Usage

``` r
alpha_parameter_to_xml(alpha_parameter, beauti_options)
```

## Arguments

- alpha_parameter:

  an alpha parameter, as created by
  [create_alpha_param](https://docs.ropensci.org/beautier/reference/create_alpha_param.md)

- beauti_options:

  one BEAUti options object, as returned by
  [`create_beauti_options`](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)

## Value

the parameter as XML text

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
remove_beautier_folder()
check_empty_beautier_folder()

# The alpha parameter must be initialized, i.e. have an ID
alpha_parameter_to_xml(
  alpha_parameter = create_alpha_param(id = "1"),
  beauti_options = beautier::create_beauti_options()
)
#> [1] "<parameter id=\"RealParameter.1\" estimate=\"false\" name=\"alpha\">0</parameter>"

check_empty_beautier_folder()
```
