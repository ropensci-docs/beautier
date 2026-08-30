# Create a site model from name

Create a site model from name

## Usage

``` r
create_site_model_from_name(site_model_name)
```

## Arguments

- site_model_name:

  name of a site model, must be a name as returned by
  [`get_site_model_names`](https://docs.ropensci.org/beautier/reference/get_site_model_names.md)

## Value

a site model

## See also

Use
[create_site_model](https://docs.ropensci.org/beautier/reference/create_site_model.md)
to create a site model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

site_model <- create_site_model_from_name(get_site_model_names()[1])

check_empty_beautier_folder()
```
