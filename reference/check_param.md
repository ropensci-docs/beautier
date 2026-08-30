# Check if the parameter is a valid parameter

Calls `stop` if the parameter is invalid

## Usage

``` r
check_param(param)
```

## Arguments

- param:

  a parameter, as can be created by
  [`create_param`](https://docs.ropensci.org/beautier/reference/create_param.md).

## Value

nothing

## See also

Use
[create_param](https://docs.ropensci.org/beautier/reference/create_param.md)
to create a valid parameter

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

check_param(create_alpha_param())
check_param(create_beta_param())

check_empty_beautier_folder()
```
