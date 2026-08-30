# Checks if `name` is a valid `freq_equilibrium` argument value

Checks if `name` is a valid `freq_equilibrium` argument value

## Usage

``` r
is_freq_equilibrium_name(name)
```

## Arguments

- name:

  the name to check if it is a valid `freq_equilibrium` argument value

## Value

TRUE if the name is a valid `freq_equilibrium` value

## See also

the `freq_equilibrium` argument is used by
[`create_gtr_site_model`](https://docs.ropensci.org/beautier/reference/create_gtr_site_model.md),
[`create_hky_site_model`](https://docs.ropensci.org/beautier/reference/create_hky_site_model.md),
and
[`create_tn93_site_model`](https://docs.ropensci.org/beautier/reference/create_tn93_site_model.md)

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# TRUE
is_freq_equilibrium_name("estimated")
#> [1] TRUE
is_freq_equilibrium_name("empirical")
#> [1] TRUE
is_freq_equilibrium_name("all_equal")
#> [1] TRUE
# FALSE
is_freq_equilibrium_name("nonsense")
#> [1] FALSE

check_empty_beautier_folder()
```
