# Get the number of distributions a site model has

Get the number of distributions a site model has

## Usage

``` r
get_gamma_site_model_n_params(gamma_site_model)
```

## Arguments

- gamma_site_model:

  a site model's gamma site model, as returned by
  [`create_gamma_site_model`](https://docs.ropensci.org/beautier/reference/create_gamma_site_model.md)

## Value

the number of parameters a site model has

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# 0 parameters
get_gamma_site_model_n_params(
  create_gamma_site_model(gamma_cat_count = 0)
)
#> [1] 0

# 0 parameters
get_gamma_site_model_n_params(
  create_gamma_site_model(gamma_cat_count = 1)
)
#> [1] 0

# 1 parameter
get_gamma_site_model_n_params(
    create_gamma_site_model(
    gamma_cat_count = 2,
    gamma_shape_prior_distr = create_exp_distr()
  )
)
#> [1] 1

check_empty_beautier_folder()
```
