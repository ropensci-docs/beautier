# Internal function

Creates the `rateCategories` state node, such as:
` "<stateNode id=\"rateCategories.c:[id]\" spec=\"parameter.IntegerParameter\" dimension=\"[dimension]\"> 1 </stateNode>" `

## Usage

``` r
create_rate_categories_state_node_xml(inference_model)
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

the following XML:
` "<stateNode id=\"rateCategories.c:[id]\" spec=\"parameter.IntegerParameter\" dimension=\"[dimension]\"> 1 </stateNode>" `

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

create_rate_categories_state_node_xml(
  create_inference_model(
    clock_model = create_rln_clock_model(
      id = 314,
      dimension = 1
    )
  )
)
#> [1] "<stateNode id=\"rateCategories.c:314\" spec=\"parameter.IntegerParameter\" dimension=\"1\">1</stateNode>"

check_empty_beautier_folder()
```
