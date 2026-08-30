# Check if the object is a list of one or more site models.

Will [stop](https://rdrr.io/r/base/stop.html) if the object is not a
list of one or more site models.

## Usage

``` r
check_site_models(site_models)
```

## Arguments

- site_models:

  the object to be checked if it is a list of one or more valid site
  models

## Value

nothing. Will [stop](https://rdrr.io/r/base/stop.html) if the object is
not a list of one or more site models.

## See also

Use
[create_site_model](https://docs.ropensci.org/beautier/reference/create_site_model.md)
to create a valid site model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

check_site_models(create_jc69_site_model())
check_site_models(list(create_jc69_site_model()))
check_site_models(
  list(create_jc69_site_model(), create_gtr_site_model())
)

check_empty_beautier_folder()
```
