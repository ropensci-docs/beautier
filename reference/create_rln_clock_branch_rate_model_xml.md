# Internal function

Internal function to call
[create_branch_rate_model_xml](https://docs.ropensci.org/beautier/reference/create_branch_rate_model_xml.md)
for a relaxed log-normal clock.

## Usage

``` r
create_rln_clock_branch_rate_model_xml(inference_model)
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

a character vector of XML strings

## Author

Richèl J.C. Bilderbeek
