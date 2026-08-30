# Get the number of distributions a site model has

Get the number of distributions a site model has

## Usage

``` r
get_site_model_n_distrs(site_model)
```

## Arguments

- site_model:

  a site model, as returned by
  [`create_site_model`](https://docs.ropensci.org/beautier/reference/create_site_model.md)

## Value

the number of distributions a site model has

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# 5: rates AC, AG, AT, CG and GT
get_site_model_n_distrs(create_gtr_site_model())
#> [1] 5

# 1: kappa
get_site_model_n_distrs(create_hky_site_model())
#> [1] 1

# 0: npne
get_site_model_n_distrs(create_jc69_site_model())
#> [1] 0

# 2: kappa 1 and kappa 2
get_site_model_n_distrs(create_tn93_site_model())
#> [1] 2

check_empty_beautier_folder()
```
