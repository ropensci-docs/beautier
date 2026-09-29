# Get the number of distributions a site model has

Get the number of distributions a site model has

## Usage

``` r
get_site_models_n_distrs(site_models)
```

## Arguments

- site_models:

  one or more site models, as returned by
  [`create_site_model`](https://docs.ropensci.org/beautier/reference/create_site_model.md)

## Value

the number of distributions the site models have

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# 5
get_site_models_n_distrs(list(create_gtr_site_model()))
#> [1] 5
# 1
get_site_models_n_distrs(list(create_hky_site_model()))
#> [1] 1
# 0
get_site_models_n_distrs(list(create_jc69_site_model()))
#> [1] 0
# 2
get_site_models_n_distrs(list(create_tn93_site_model()))
#> [1] 2

check_empty_beautier_folder()
```
