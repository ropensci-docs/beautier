# Deprecated function

Internal function to creates the gamma site models section in the
distribution section of a BEAST2 XML parameter file

## Usage

``` r
gamma_site_models_to_xml_prior_distr(
  site_models,
  beauti_options = beautier::create_beauti_options()
)
```

## Arguments

- site_models:

  one or more site models, as returned by
  [`create_site_model`](https://docs.ropensci.org/beautier/reference/create_site_model.md)

- beauti_options:

  one BEAUti options object, as returned by
  [`create_beauti_options`](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)

## Value

lines of XML text

## Author

Richèl J.C. Bilderbeek
