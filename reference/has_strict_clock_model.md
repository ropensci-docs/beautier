# Determine if the `inference_model` uses a strict clock model.

Determine if the `inference_model` uses a strict clock model

## Usage

``` r
has_strict_clock_model(inference_model)
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

TRUE if the `inference_model` uses a strict clock model, FALSE otherwise

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# Yes, has a strict clock model
has_strict_clock_model(
  create_inference_model(clock_model = create_strict_clock_model())
)
#> [1] TRUE

# No strict clock model
has_strict_clock_model(
  create_inference_model(clock_model = create_rln_clock_model())
)
#> [1] FALSE

check_empty_beautier_folder()
```
