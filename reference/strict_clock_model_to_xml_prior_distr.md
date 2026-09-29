# Internal function

Internal function to converts a strict clock model to the `prior`
section of the XML as text

## Usage

``` r
strict_clock_model_to_xml_prior_distr(inference_model)
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

## Examples

``` r
check_empty_beautier_folder()
 # <distribution id="posterior" spec="util.CompoundDistribution">
 #     <distribution id="prior" spec="util.CompoundDistribution">
 #       HERE, where the ID of the distribution is 'prior'
 #     </distribution>
 #     <distribution id="likelihood" ...>
 #     </distribution>
 # </distribution>
strict_clock_model_to_xml_prior_distr(
  inference_model = create_inference_model()
)
#> NULL
check_empty_beautier_folder()
```
