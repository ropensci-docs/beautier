# Internal function

Creates the `ucldMean.c` parameter with the name `stateNode`, such as:
` <parameter id=\"ucldMean.c:[id]\" spec=\"parameter.RealParameter\" name=\"stateNode\">1.0</parameter> `

## Usage

``` r
create_ucld_mean_state_node_param_xml(inference_model)
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

the XML
` <parameter id=\"ucldMean.c:[id]\" spec=\"parameter.RealParameter\" name=\"stateNode\">1.0</parameter> `

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

create_ucld_mean_state_node_param_xml(
  create_inference_model(
    clock_model = create_rln_clock_model(id = 314),
    beauti_options = create_beauti_options_v2_6()
  )
)
#> [1] "<parameter id=\"ucldMean.c:314\" spec=\"parameter.RealParameter\" name=\"stateNode\">1.0</parameter>"

check_empty_beautier_folder()
```
