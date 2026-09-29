# Determine if the object is a valid GTR site model, as created by [`create_gtr_site_model`](https://docs.ropensci.org/beautier/reference/create_gtr_site_model.md)

Determine if the object is a valid GTR site model, as created by
[`create_gtr_site_model`](https://docs.ropensci.org/beautier/reference/create_gtr_site_model.md)

## Usage

``` r
is_gtr_site_model(x)
```

## Arguments

- x:

  an object, to be determined if it is a valid GTR site model

## Value

TRUE if x is a valid GTR site model, FALSE otherwise

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# site models
is_gtr_site_model(create_gtr_site_model())
#> [1] TRUE
is_gtr_site_model(create_hky_site_model())
#> [1] FALSE
is_gtr_site_model(create_jc69_site_model())
#> [1] FALSE
is_gtr_site_model(create_tn93_site_model())
#> [1] FALSE

# other models
is_gtr_site_model(NA)
#> [1] FALSE
is_gtr_site_model(NULL)
#> [1] FALSE
is_gtr_site_model("nonsense")
#> [1] FALSE
is_gtr_site_model(create_strict_clock_model())
#> [1] FALSE
is_gtr_site_model(create_bd_tree_prior())
#> [1] FALSE
is_gtr_site_model(create_mcmc())
#> [1] FALSE

check_empty_beautier_folder()
```
