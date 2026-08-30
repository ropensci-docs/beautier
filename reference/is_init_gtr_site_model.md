# Determine if x is an initialized GTR site model as created by [`create_gtr_site_model`](https://docs.ropensci.org/beautier/reference/create_gtr_site_model.md)

Determine if x is an initialized GTR site model as created by
[`create_gtr_site_model`](https://docs.ropensci.org/beautier/reference/create_gtr_site_model.md)

## Usage

``` r
is_init_gtr_site_model(x)
```

## Arguments

- x:

  the object to check if it is an initialized GTR site model

## Value

TRUE if x is an initialized GTR site model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

gtr_site_model <- create_gtr_site_model()
# FALSE: not yet initialized
is_init_gtr_site_model(gtr_site_model)
#> [1] FALSE
gtr_site_model <- init_gtr_site_model(gtr_site_model)
# TRUE: now it is initialized
is_init_gtr_site_model(gtr_site_model)
#> [1] TRUE

check_empty_beautier_folder()
```
