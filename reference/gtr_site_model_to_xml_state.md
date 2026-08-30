# Converts a site model to XML, used in the `state` section

Converts a site model to XML, used in the `state` section

## Usage

``` r
gtr_site_model_to_xml_state(
  site_model,
  beauti_options = beautier::create_beauti_options()
)
```

## Arguments

- site_model:

  a site model, as returned by
  [`create_site_model`](https://docs.ropensci.org/beautier/reference/create_site_model.md)

- beauti_options:

  one BEAUti options object, as returned by
  [`create_beauti_options`](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)

## Value

the site model as XML text

## Author

Richèl J.C. Bilderbeek
