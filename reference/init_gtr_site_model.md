# Initializes a GTR site model

Initializes a GTR site model

## Usage

``` r
init_gtr_site_model(gtr_site_model, distr_id = 0, param_id = 0)
```

## Arguments

- gtr_site_model:

  a GTR site model, as returned by
  [`create_gtr_site_model`](https://docs.ropensci.org/beautier/reference/create_gtr_site_model.md)

- distr_id:

  a distributions' ID

- param_id:

  a parameter's ID

## Value

an initialized GTR site model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

gtr_site_model <- create_gtr_site_model()
# FALSE
is_init_gtr_site_model(gtr_site_model)
#> [1] FALSE
gtr_site_model <- init_gtr_site_model(gtr_site_model)
# TRUE
is_init_gtr_site_model(gtr_site_model)
#> [1] TRUE

check_empty_beautier_folder()
```
