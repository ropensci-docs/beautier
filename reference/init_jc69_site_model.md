# Initializes a JC69 site model

Initializes a JC69 site model

## Usage

``` r
init_jc69_site_model(jc69_site_model, distr_id = 0, param_id = 0)
```

## Arguments

- jc69_site_model:

  a JC69 site model, as returned by
  [`create_jc69_site_model`](https://docs.ropensci.org/beautier/reference/create_jc69_site_model.md)

- distr_id:

  a distributions' ID

- param_id:

  a parameter's ID

## Value

an initialized HKY site model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

hky_site_model <- create_hky_site_model()
is_init_hky_site_model(hky_site_model)
#> [1] FALSE
hky_site_model <- init_hky_site_model(hky_site_model)
is_init_hky_site_model(hky_site_model)
#> [1] TRUE

check_empty_beautier_folder()
```
