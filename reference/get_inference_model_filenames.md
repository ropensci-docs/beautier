# Get the filenames stored in an inference model.

If there is no name for a `tipdates` file specified (as done by setting
`inference_model$tipdates_filename` to
[NA](https://rdrr.io/r/base/NA.html), there will be one filename less
returned

## Usage

``` r
get_inference_model_filenames(inference_model)
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

the filenames stored in an inference model

## Examples

``` r
check_empty_beautier_folder()

inference_model <- create_inference_model()
filenames <- get_inference_model_filenames(inference_model)

check_empty_beautier_folder()
```
