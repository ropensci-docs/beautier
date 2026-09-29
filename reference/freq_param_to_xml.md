# Internal function

Converts a \`freq\` parameter to XML

## Usage

``` r
freq_param_to_xml(
  freq_param,
  beauti_options = beautier::create_beauti_options()
)
```

## Arguments

- freq_param:

  a \`freq\` parameter, as created by
  [create_freq_param](https://docs.ropensci.org/beautier/reference/create_freq_param.md)

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

# The freq parameter must be initialized, i.e. have an ID
freq_param_to_xml(freq_param = create_freq_param(id = "1"))
#> [1] "<parameter id=\"freqParameter.s:1\" dimension=\"4\" lower=\"0.0\" name=\"stateNode\" upper=\"1.0\">0.25</parameter>"

check_empty_beautier_folder()
```
