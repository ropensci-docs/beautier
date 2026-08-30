# Determines if the inference model has an MRCA prior.

Will [stop](https://rdrr.io/r/base/stop.html) if the inference model is
invalid

## Usage

``` r
has_mrca_prior(inference_model)
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

TRUE if the inference model has an MRCA prior, FALSE otherwise

## Note

MRCA: 'Most Recent Common Ancestor'

## See also

- [`create_inference_model`](https://docs.ropensci.org/beautier/reference/create_inference_model.md):
  create an inference model

- [`create_mrca_prior`](https://docs.ropensci.org/beautier/reference/create_mrca_prior.md):
  create an MRCA prior

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# No MRCA prior
inference_model <- create_inference_model(
  mrca_prior = NA
)
has_mrca_prior(inference_model) # Returns FALSE
#> [1] FALSE

# A default MRCA prior
inference_model <- create_inference_model(
  mrca_prior = create_mrca_prior()
)
has_mrca_prior(inference_model) # Returns TRUE
#> [1] TRUE

check_empty_beautier_folder()
```
