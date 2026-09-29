# Determines if the name is a valid distribution name

Determines if the name is a valid distribution name

## Usage

``` r
is_distr_name(name)
```

## Arguments

- name:

  the name to be tested

## Value

TRUE if the name is a valid distribution name, FALSE otherwise

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# TRUE
is_distr_name("uniform")
#> [1] TRUE
is_distr_name("normal")
#> [1] TRUE
is_distr_name("one_div_x")
#> [1] TRUE
is_distr_name("log_normal")
#> [1] TRUE
is_distr_name("exponential")
#> [1] TRUE
is_distr_name("gamma")
#> [1] TRUE
is_distr_name("beta")
#> [1] TRUE
is_distr_name("laplace")
#> [1] TRUE
is_distr_name("inv_gamma")
#> [1] TRUE
is_distr_name("poisson")
#> [1] TRUE
# FALSE
is_distr_name("nonsense")
#> [1] FALSE

check_empty_beautier_folder()
```
