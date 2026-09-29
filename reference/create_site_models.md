# Creates all supported site models which is a list of the types returned by [`create_gtr_site_model`](https://docs.ropensci.org/beautier/reference/create_gtr_site_model.md), [`create_hky_site_model`](https://docs.ropensci.org/beautier/reference/create_hky_site_model.md), [`create_jc69_site_model`](https://docs.ropensci.org/beautier/reference/create_jc69_site_model.md) and [`create_tn93_site_model`](https://docs.ropensci.org/beautier/reference/create_tn93_site_model.md)

Creates all supported site models which is a list of the types returned
by
[`create_gtr_site_model`](https://docs.ropensci.org/beautier/reference/create_gtr_site_model.md),
[`create_hky_site_model`](https://docs.ropensci.org/beautier/reference/create_hky_site_model.md),
[`create_jc69_site_model`](https://docs.ropensci.org/beautier/reference/create_jc69_site_model.md)
and
[`create_tn93_site_model`](https://docs.ropensci.org/beautier/reference/create_tn93_site_model.md)

## Usage

``` r
create_site_models()
```

## Value

a list of site_models

## See also

Use
[create_site_model](https://docs.ropensci.org/beautier/reference/create_site_model.md)
to create a site model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# All created site models are a kind of site model
site_models <- create_site_models()

# TRUE
is_gtr_site_model(site_models[[1]])
#> [1] TRUE
is_hky_site_model(site_models[[2]])
#> [1] TRUE
is_jc69_site_model(site_models[[3]])
#> [1] TRUE
is_tn93_site_model(site_models[[4]])
#> [1] TRUE

check_empty_beautier_folder()
```
