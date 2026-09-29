# Determine if the object is a valid site_model

Determine if the object is a valid site_model

## Usage

``` r
is_site_model(x)
```

## Arguments

- x:

  an object, to be determined if it is a site_model

## Value

TRUE if the site_model is a valid site_model, FALSE otherwise

## See also

A site model can be created using
[`create_site_model`](https://docs.ropensci.org/beautier/reference/create_site_model.md)

## Examples

``` r
check_empty_beautier_folder()

# TRUE
is_site_model(create_gtr_site_model())
#> [1] TRUE
is_site_model(create_hky_site_model())
#> [1] TRUE
is_site_model(create_jc69_site_model())
#> [1] TRUE
is_site_model(create_tn93_site_model())
#> [1] TRUE

# FALSE
is_site_model(NA)
#> [1] FALSE
is_site_model(NULL)
#> [1] FALSE
is_site_model("nonsense")
#> [1] FALSE
is_site_model(create_strict_clock_model())
#> [1] FALSE
is_site_model(create_bd_tree_prior())
#> [1] FALSE
is_site_model(create_mcmc())
#> [1] FALSE

check_empty_beautier_folder()
```
