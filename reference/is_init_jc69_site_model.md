# Determine if x is an initialized JC69 site model as created by [`create_jc69_site_model`](https://docs.ropensci.org/beautier/reference/create_jc69_site_model.md)

Determine if x is an initialized JC69 site model as created by
[`create_jc69_site_model`](https://docs.ropensci.org/beautier/reference/create_jc69_site_model.md)

## Usage

``` r
is_init_jc69_site_model(x)
```

## Arguments

- x:

  the object to check if it is an initialized JC69 site model

## Value

TRUE if x is an initialized JC69 site model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

jc69_site_model <- create_jc69_site_model(
  gamma_site_model = create_gamma_site_model(
    gamma_cat_count = 2,
    gamma_shape_prior_distr = create_normal_distr()
  )
)
# FALSE: not yet initialized
is_init_jc69_site_model(jc69_site_model)
#> [1] FALSE
jc69_site_model <- init_jc69_site_model(jc69_site_model)
# TRUE: now it is initialized
is_init_jc69_site_model(jc69_site_model)
#> [1] TRUE

check_empty_beautier_folder()
```
