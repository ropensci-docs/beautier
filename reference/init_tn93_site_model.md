# Initializes a TN93 site model

Initializes a TN93 site model

## Usage

``` r
init_tn93_site_model(tn93_site_model, distr_id = 0, param_id = 0)
```

## Arguments

- tn93_site_model:

  a TN93 site model, as returned by
  [`create_tn93_site_model`](https://docs.ropensci.org/beautier/reference/create_tn93_site_model.md)

- distr_id:

  a distributions' ID

- param_id:

  a parameter's ID

## Value

an initialized TN93 site model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

tn93_site_model <- create_tn93_site_model()
is_init_tn93_site_model(tn93_site_model)
#> [1] FALSE
tn93_site_model <- init_tn93_site_model(tn93_site_model)
is_init_tn93_site_model(tn93_site_model)
#> [1] TRUE

check_empty_beautier_folder()
```
