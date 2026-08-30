# Internal function

Creates the `tracelog` section of the `logger` section of a BEAST2 XML
parameter file

## Usage

``` r
create_tracelog_xml(input_filename, inference_model)
```

## Arguments

- input_filename:

  A FASTA filename. Use
  [`get_fasta_filename`](https://docs.ropensci.org/beautier/reference/get_fasta_filename.md)
  to obtain a testing FASTA filename.

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
