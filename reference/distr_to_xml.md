# Internal function

Converts a distribution to XML

## Usage

``` r
distr_to_xml(distr, beauti_options)
```

## Arguments

- distr:

  a distribution, as created by
  [`create_distr`](https://docs.ropensci.org/beautier/reference/create_distr.md))

- beauti_options:

  one BEAUti options object, as returned by
  [`create_beauti_options`](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)

## Value

the distribution as XML text

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

distr_to_xml(
  create_uniform_distr(id = 1),
  beauti_options = beautier::create_beauti_options()
)
#> [1] "<Uniform id=\"Uniform.1\" name=\"distr\" upper=\"Infinity\"/>"

check_empty_beautier_folder()
```
