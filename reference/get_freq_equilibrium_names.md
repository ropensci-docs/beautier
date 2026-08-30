# Returns valid values for the `freq_equilibrium` argument

Returns valid values for the `freq_equilibrium` argument

## Usage

``` r
get_freq_equilibrium_names()
```

## Value

the valid values for the `freq_equilibrium` argument

## See also

the `freq_equilibrium` argument is used in
[`create_gtr_site_model`](https://docs.ropensci.org/beautier/reference/create_gtr_site_model.md),
[`create_hky_site_model`](https://docs.ropensci.org/beautier/reference/create_hky_site_model.md),
and
[`create_tn93_site_model`](https://docs.ropensci.org/beautier/reference/create_tn93_site_model.md)

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

get_freq_equilibrium_names()
#> [1] "estimated" "empirical" "all_equal"

check_empty_beautier_folder()
```
