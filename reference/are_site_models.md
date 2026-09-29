# Determine if x consists out of site_models objects

Determine if x consists out of site_models objects

## Usage

``` r
are_site_models(x)
```

## Arguments

- x:

  the object to check if it consists out of site_models objects

## Value

TRUE if x, or all elements of x, are site_model objects

## See also

Use
[create_site_model](https://docs.ropensci.org/beautier/reference/create_site_model.md)
to create a site model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

jc69_site_model <- create_jc69_site_model()
gtr_site_model <- create_gtr_site_model()
both_site_models <- list(jc69_site_model, gtr_site_model)

# TRUE
are_site_models(jc69_site_model)
#> [1] TRUE

# TRUE
are_site_models(gtr_site_model)
#> [1] TRUE

# TRUE
are_site_models(both_site_models)
#> [1] TRUE

check_empty_beautier_folder()
```
