# Determine if x is an initialized HKY site model as created by [`create_hky_site_model`](https://docs.ropensci.org/beautier/reference/create_hky_site_model.md)

Determine if x is an initialized HKY site model as created by
[`create_hky_site_model`](https://docs.ropensci.org/beautier/reference/create_hky_site_model.md)

## Usage

``` r
is_init_hky_site_model(x)
```

## Arguments

- x:

  the object to check if it is an initialized HKY site model

## Value

TRUE if x is an initialized HKY site model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

hky_site_model <- create_hky_site_model()
# FALSE: not yet initialized
is_init_hky_site_model(hky_site_model)
#> [1] FALSE
hky_site_model <- init_hky_site_model(hky_site_model)
# TRUE: now it is initialized
is_init_hky_site_model(hky_site_model)
#> [1] TRUE

check_empty_beautier_folder()
```
