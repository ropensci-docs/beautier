# Check if the site model is a valid site model

Calls `stop` if the site models are invalid

## Usage

``` r
check_site_model(site_model)
```

## Arguments

- site_model:

  a site model, as returned by
  [`create_site_model`](https://docs.ropensci.org/beautier/reference/create_site_model.md)

## Value

nothing

## See also

Use
[create_site_model](https://docs.ropensci.org/beautier/reference/create_site_model.md)
to create a valid site model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

check_site_model(create_jc69_site_model())
check_site_model(create_hky_site_model())
check_site_model(create_tn93_site_model())
check_site_model(create_gtr_site_model())

# Can use list of one site model
check_site_model(list(create_jc69_site_model()))
#> NULL

check_empty_beautier_folder()
```
