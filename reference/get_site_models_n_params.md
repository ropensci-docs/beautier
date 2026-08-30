# Get the number of distributions one or more site models have

Get the number of distributions one or more site models have

## Usage

``` r
get_site_models_n_params(site_models)
```

## Arguments

- site_models:

  one or more site models, as returned by
  [`create_site_model`](https://docs.ropensci.org/beautier/reference/create_site_model.md)

## Value

the number of parameters the site models have

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# Ten
get_site_models_n_params(list(create_gtr_site_model()))
#> [1] 10

# Two
get_site_models_n_params(list(create_hky_site_model()))
#> [1] 2

# Zero
get_site_models_n_params(list(create_jc69_site_model()))
#> [1] 0

# Four
get_site_models_n_params(list(create_tn93_site_model()))
#> [1] 4

check_empty_beautier_folder()
```
