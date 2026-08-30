# Creates the site models' XML for the tracelog section

Creates the site models' XML for the tracelog section

## Usage

``` r
site_models_to_xml_tracelog(site_models)
```

## Arguments

- site_models:

  one or more site models, as returned by
  [`create_site_model`](https://docs.ropensci.org/beautier/reference/create_site_model.md)

## Value

lines of XML text

## See also

the complete tracelog section is created by
[`create_tracelog_xml`](https://docs.ropensci.org/beautier/reference/create_tracelog_xml.md)

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# <logger id="tracelog" ...>
#'   # Here
# </logger>

check_empty_beautier_folder()
```
