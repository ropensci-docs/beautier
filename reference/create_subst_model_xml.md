# Internal function to create the `substModel` section

Internal function to create the `substModel` section

## Usage

``` r
create_subst_model_xml(inference_model)
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

the `substModel` section as XML text

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# Inference model must be initialized
inference_model <- create_inference_model(
  site_model = create_jc69_site_model(id = 123)
)
create_subst_model_xml(
  inference_model = inference_model
)
#> [1] "<substModel id=\"JC69.s:123\" spec=\"JukesCantor\"/>"

check_empty_beautier_folder()
```
