# Determines if the name is a valid tree prior name

Determines if the name is a valid tree prior name

## Usage

``` r
is_tree_prior_name(name)
```

## Arguments

- name:

  the name to be tested

## Value

TRUE if the name is a valid tree_prior name, FALSE otherwise

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# TRUE
is_tree_prior_name("birth_death")
#> [1] TRUE
is_tree_prior_name("coalescent_bayesian_skyline")
#> [1] TRUE
is_tree_prior_name("coalescent_constant_population")
#> [1] TRUE
is_tree_prior_name("coalescent_exp_population")
#> [1] TRUE
is_tree_prior_name("yule")
#> [1] TRUE
# FALSE
is_tree_prior_name("nonsense")
#> [1] FALSE

check_empty_beautier_folder()
```
