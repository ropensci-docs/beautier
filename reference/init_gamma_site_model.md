# Initializes a gamma site model

Initializes a gamma site model

## Usage

``` r
init_gamma_site_model(gamma_site_model, distr_id = 0, param_id = 0)
```

## Arguments

- gamma_site_model:

  a site model's gamma site model, as returned by
  [`create_gamma_site_model`](https://docs.ropensci.org/beautier/reference/create_gamma_site_model.md)

- distr_id:

  the first distributions' ID

- param_id:

  the first parameter's ID

## Value

an initialized gamma site model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

gamma_site_model <- create_gamma_site_model(
  gamma_cat_count = 2,
  gamma_shape_prior_distr = create_one_div_x_distr(id = NA)
)
# FALSE: not yet initialized
is_init_gamma_site_model(gamma_site_model)
#> [1] FALSE
gamma_site_model <- init_gamma_site_model(gamma_site_model)
# TRUE: now it is initialized
is_init_gamma_site_model(gamma_site_model)
#> [1] TRUE

check_empty_beautier_folder()
```
