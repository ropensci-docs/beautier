# Internal function

Converts an kappa parameter to XML

## Usage

``` r
kappa_param_to_xml(
  kappa_param,
  beauti_options = beautier::create_beauti_options()
)
```

## Arguments

- kappa_param:

  a kappa parameter, as created by
  [create_kappa_param](https://docs.ropensci.org/beautier/reference/create_kappa_param.md)

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

# The kappa parameter must be initialized, i.e. have an ID
kappa_param_to_xml(kappa_param = create_kappa_param(id = "1"))
#> [1] "<parameter id=\"kappa.s:1\" lower=\"0.0\" name=\"stateNode\">2.0</parameter>"

check_empty_beautier_folder()
```
