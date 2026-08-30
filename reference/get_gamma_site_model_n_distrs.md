# Get the number of distributions in a gamma site model

Get the number of distributions in a gamma site model

## Usage

``` r
get_gamma_site_model_n_distrs(gamma_site_model)
```

## Arguments

- gamma_site_model:

  a site model's gamma site model, as returned by
  [`create_gamma_site_model`](https://docs.ropensci.org/beautier/reference/create_gamma_site_model.md)

## Value

the number of distributions a gamma site model has

## See also

Use
[create_gamma_site_model](https://docs.ropensci.org/beautier/reference/create_gamma_site_model.md)
to create a gamma site model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# zero distributions
gamma_site_model <- create_gamma_site_model()
get_gamma_site_model_n_distrs(
  gamma_site_model
)
#> [1] 0

gamma_site_model <- create_gamma_site_model(
 gamma_cat_count = 2,
 gamma_shape_prior_distr = create_exp_distr()
)

# one distribution
get_gamma_site_model_n_distrs(gamma_site_model)
#> [1] 1

check_empty_beautier_folder()
```
