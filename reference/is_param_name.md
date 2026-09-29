# Determines if the name is a valid parameter name

Determines if the name is a valid parameter name

## Usage

``` r
is_param_name(name)
```

## Arguments

- name:

  the name to be tested

## Value

TRUE if the name is a valid parameter name, FALSE otherwise

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# TRUE
is_param_name("alpha")
#> [1] TRUE
is_param_name("beta")
#> [1] TRUE
is_param_name("clock_rate")
#> [1] TRUE
is_param_name("kappa_1")
#> [1] TRUE
is_param_name("kappa_2")
#> [1] TRUE
is_param_name("lambda")
#> [1] TRUE
is_param_name("m")
#> [1] TRUE
is_param_name("mean")
#> [1] TRUE
is_param_name("mu")
#> [1] TRUE
is_param_name("rate_ac")
#> [1] TRUE
is_param_name("rate_ag")
#> [1] TRUE
is_param_name("rate_at")
#> [1] TRUE
is_param_name("rate_cg")
#> [1] TRUE
is_param_name("rate_ct")
#> [1] TRUE
is_param_name("rate_gt")
#> [1] TRUE
is_param_name("s")
#> [1] TRUE
is_param_name("scale")
#> [1] TRUE
is_param_name("sigma")
#> [1] TRUE

# FALSE
is_param_name("nonsense")
#> [1] FALSE
is_param_name(NA)
#> [1] FALSE
is_param_name(NULL)
#> [1] FALSE
is_param_name("")
#> [1] FALSE
is_param_name(c())
#> [1] FALSE

check_empty_beautier_folder()
```
