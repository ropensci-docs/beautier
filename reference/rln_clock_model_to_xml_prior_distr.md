# Internal function

Internal function to converts a relaxed log-normal clock model to the
`prior` section of the XML as text

## Usage

``` r
rln_clock_model_to_xml_prior_distr(inference_model)
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

# Must be an initialized inference model
inference_model <- create_inference_model(
  clock_model = create_rln_clock_model(
    id = "test_output_0",
    ucldstdev_distr = create_gamma_distr(
      id = 0,
      alpha = create_alpha_param(id = 2, value = "0.5396"),
      beta = create_beta_param(id = 3, value = "0.3819")
    ),
    mean_rate_prior_distr = create_uniform_distr(id = 1),
    mparam_id = 1
  )
)

rln_clock_model_to_xml_prior_distr(inference_model)
#> [1] "<prior id=\"ucldStdevPrior.c:test_output_0\" name=\"distribution\" x=\"@ucldStdev.c:test_output_0\">"
#> [2] "    <Gamma id=\"Gamma.0\" name=\"distr\">"                                                           
#> [3] "        <parameter id=\"RealParameter.2\" estimate=\"false\" name=\"alpha\">0.5396</parameter>"      
#> [4] "        <parameter id=\"RealParameter.3\" estimate=\"false\" name=\"beta\">0.3819</parameter>"       
#> [5] "    </Gamma>"                                                                                        
#> [6] "</prior>"                                                                                            

check_empty_beautier_folder()
```
