# Check if the supplied object is a valid Bayesian phylogenetic inference model.

Calls `stop` if the supplied object is not a valid Bayesian phylogenetic
inference model.

## Usage

``` r
check_inference_model(inference_model)
```

## Arguments

- inference_model:

  a Bayesian phylogenetic inference model. An inference model is the
  complete model setup in which a site model, clock model, tree prior
  and more are specified. Use
  [create_inference_model](https://docs.ropensci.org/beautier/reference/create_inference_model.md)
  to create an inference model. Use check_inference_model to check if an
  inference model is valid. Use
  [rename_inference_model_filenames](https://docs.ropensci.org/beautier/reference/rename_inference_model_filenames.md)
  to rename the files in an inference model.

## Value

nothing

## See also

Use
[create_inference_model](https://docs.ropensci.org/beautier/reference/create_inference_model.md)
to create a valid Bayesian phylogenetic inference model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

check_inference_model(create_inference_model())

check_empty_beautier_folder()
```
