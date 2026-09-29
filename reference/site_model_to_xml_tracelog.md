# Creates the site model's XML for the tracelog section

Creates the site model's XML for the tracelog section

## Usage

``` r
site_model_to_xml_tracelog(site_model)
```

## Arguments

- site_model:

  a site model, as returned by
  [`create_site_model`](https://docs.ropensci.org/beautier/reference/create_site_model.md)

## Value

lines of XML text

## See also

all site models' tracelog section is created by
[`site_models_to_xml_tracelog`](https://docs.ropensci.org/beautier/reference/site_models_to_xml_tracelog.md)

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
