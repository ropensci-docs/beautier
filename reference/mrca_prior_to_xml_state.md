# Internal function to create the XML of an MRCA prior, as used in the `state` section

Internal function to create the XML of an MRCA prior, as used in the
`state` section

## Usage

``` r
mrca_prior_to_xml_state(inference_model)
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

the tree prior as XML text

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

mrca_prior_to_xml_state(
  inference_model = create_inference_model(
    mrca_prior = create_mrca_prior(
      alignment_id = "test_output_0",
      mrca_distr = create_normal_distr(id = 42)
    ),
    clock_model = create_strict_clock_model()
  )
)
#> [1] "<parameter id=\"clockRate.c:test_output_0\" name=\"stateNode\">1.0</parameter>"

check_empty_beautier_folder()
```
