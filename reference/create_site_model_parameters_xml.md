# Internal function to creates the XML text for the `parameter`s within the `siteModel` section of a BEAST2 parameter file.

Internal function to creates the XML text for the `parameter`s within
the `siteModel` section, which is part of the `siteModel` section of a
BEAST2 parameter file.

## Usage

``` r
create_site_model_parameters_xml(inference_model)
```

## Arguments

- inference_model:

  a Bayesian phylogenetic inference model. An inference model is the
  complete model setup in which a site model, clock model, tree prior
  and more are specified. Use
  [create_inference_model](https://docs.ropensci.org/beautier/reference/create_inference_model.md)
  to create an inference model. Use
  [check_inference_model](https://docs.ropensci.org/beautier/reference/check_inference_model.md)
  to check if an inference model is valid. Use
  [rename_inference_model_filenames](https://docs.ropensci.org/beautier/reference/rename_inference_model_filenames.md)
  to rename the files in an inference model.

## Value

the site model as XML text

## Details

The `parameter`s sections has these elements:


       [parameters]

`[parameters]` can be a combination of these:


      <parameter id="mutationRate.s[...]>
      <parameter id="gammaShape.s[...]>
      <parameter id="proportionInvariant.s[...]>

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()
```
