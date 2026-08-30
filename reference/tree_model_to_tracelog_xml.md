# Internal function

Creates the tree models' XML for the tracelog section. That is, all XML
tags that have the word 'tree' in them.

## Usage

``` r
tree_model_to_tracelog_xml(inference_model)
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

## Note

use site_models just because it contains all IDs

## See also

the complete tracelog section is created by
[`create_tracelog_xml`](https://docs.ropensci.org/beautier/reference/create_tracelog_xml.md)

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# <logger id="tracelog" ...>
#'   # Here
# </logger>

check_empty_beautier_folder()
```
