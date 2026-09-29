# Determine if the `inference_model` uses tip dating.

Determine if the `inference_model` uses tip dating

## Usage

``` r
has_tip_dating(inference_model)
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

TRUE if the `inference_model` uses tip dating, FALSE otherwise

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# Yes, has tip dating
has_strict_clock_model(
  create_inference_model(
    tipdates_filename = get_beautier_path("test_output_0_tipdates.tsv")
  )
)
#> [1] TRUE

# No tip dating
has_strict_clock_model(
  create_inference_model()
)
#> [1] TRUE

check_empty_beautier_folder()
```
