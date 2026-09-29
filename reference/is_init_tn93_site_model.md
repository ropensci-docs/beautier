# Determine if x is an initialized tn93 site model as created by [`create_tn93_site_model`](https://docs.ropensci.org/beautier/reference/create_tn93_site_model.md)

Determine if x is an initialized tn93 site model as created by
[`create_tn93_site_model`](https://docs.ropensci.org/beautier/reference/create_tn93_site_model.md)

## Usage

``` r
is_init_tn93_site_model(x)
```

## Arguments

- x:

  the object to check if it is an initialized TN93 site model

## Value

TRUE if x is an initialized TN93 site model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

tn93_site_model <- create_tn93_site_model()
# FALSE: not yet initialized
is_init_tn93_site_model(tn93_site_model)
#> [1] FALSE
tn93_site_model <- init_tn93_site_model(tn93_site_model)
# TRUE: now it is initialized
is_init_tn93_site_model(tn93_site_model)
#> [1] TRUE

check_empty_beautier_folder()
```
