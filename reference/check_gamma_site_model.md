# Checks if the parameter is a valid gamma site model

Checks if the parameter is a valid gamma site model

## Usage

``` r
check_gamma_site_model(gamma_site_model)
```

## Arguments

- gamma_site_model:

  a site model's gamma site model, as returned by
  [`create_gamma_site_model`](https://docs.ropensci.org/beautier/reference/create_gamma_site_model.md)

## Value

nothing. Will call `stop` if the argument is not a valid gamma site
model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

check_gamma_site_model(create_gamma_site_model())

check_empty_beautier_folder()
```
