# Internal function

Converts a Bayesian population sizes parameter to XML

## Usage

``` r
b_pop_sizes_parameter_to_xml(
  b_pop_sizes_parameter,
  beauti_options = beautier::create_beauti_options()
)
```

## Arguments

- b_pop_sizes_parameter:

  a Bayesian population size parameter, as created by
  [create_b_pop_sizes_param](https://docs.ropensci.org/beautier/reference/create_b_pop_sizes_param.md)

- beauti_options:

  one BEAUti options object, as returned by
  [`create_beauti_options`](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)

## Value

the parameter as XML text

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
b_pop_sizes_parameter_to_xml(
  b_pop_sizes_parameter = create_b_pop_sizes_param(id = 42),
  beauti_options = beautier::create_beauti_options()
)
#> [1] "<parameter id=\"bPopSizes.t:42\" dimension=\"5\" lower=\"0.0\" name=\"stateNode\" upper=\"380000.0\">380.0</parameter>"
b_pop_sizes_parameter_to_xml(
  b_pop_sizes_parameter = create_b_pop_sizes_param(id = 42, upper = Inf),
  beauti_options = beautier::create_beauti_options()
)
#> [1] "<parameter id=\"bPopSizes.t:42\" dimension=\"5\" lower=\"0.0\" name=\"stateNode\">380.0</parameter>"
```
