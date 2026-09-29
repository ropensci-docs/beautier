# Internal function

Converts a \`bPopSizes\` parameter to XML

## Usage

``` r
b_pop_sizes_param_to_xml(
  b_pop_sizes_param,
  beauti_options = beautier::create_beauti_options()
)
```

## Arguments

- b_pop_sizes_param:

  a Bayesian population size parameter, as created by
  [create_b_pop_sizes_param](https://docs.ropensci.org/beautier/reference/create_b_pop_sizes_param.md)

- beauti_options:

  one BEAUti options object, as returned by
  [`create_beauti_options`](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)

## Value

the parameter as XML text

## Author

Richèl J.C. Bilderbeek
