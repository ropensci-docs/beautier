# Convert a CCP tree prior to the XML as part of the `state` section

Convert a CCP tree prior to the XML as part of the `state` section

## Usage

``` r
ccp_tree_prior_to_xml_state(inference_model)
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

XML as text

## Examples

``` r
check_empty_beautier_folder()

# Need an ID and inital value
inference_model <- create_inference_model(
  tree_prior = create_ccp_tree_prior(
    id = "anthus_nd2_sub",
    pop_size_distr = create_normal_distr(
      id = 123,
      value = 3.14
    )
  )
)

ccp_tree_prior_to_xml_state(inference_model)
#> [1] "<parameter id=\"popSize.t:anthus_nd2_sub\" name=\"stateNode\">3.14</parameter>"

check_empty_beautier_folder()
```
