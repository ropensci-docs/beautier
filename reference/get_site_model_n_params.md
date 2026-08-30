# Get the number of distributions a site model has

Get the number of distributions a site model has

## Usage

``` r
get_site_model_n_params(site_model)
```

## Arguments

- site_model:

  a site model, as returned by
  [`create_site_model`](https://docs.ropensci.org/beautier/reference/create_site_model.md)

## Value

the number of parameters a site model has

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# Ten
get_site_model_n_params(create_gtr_site_model())
#> [1] 10

# Two
get_site_model_n_params(create_hky_site_model())
#> [1] 2

# Zero
get_site_model_n_params(create_jc69_site_model())
#> [1] 0

# Four
get_site_model_n_params(create_tn93_site_model())
#> [1] 4

check_empty_beautier_folder()
```
