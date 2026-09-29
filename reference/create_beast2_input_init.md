# Creates the `init` section of a BEAST2 XML parameter file

Creates the `init` section of a BEAST2 XML parameter file

## Usage

``` r
create_beast2_input_init(inference_model)
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

lines of XML text

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

inference_model <- init_inference_model(
  input_filename = get_fasta_filename(),
  inference_model = create_test_inference_model()
)
xml <- create_beast2_input_init(
  inference_model = inference_model
)

check_empty_beautier_folder()
```
