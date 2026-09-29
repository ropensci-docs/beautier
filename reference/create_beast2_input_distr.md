# Creates the distribution section of a BEAST2 XML parameter file.

Creates the distribution section of a BEAST2 XML parameter file.

## Usage

``` r
create_beast2_input_distr(inference_model)
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

this function is not intended for regular use, thus its long name length
is accepted

## See also

[`create_beast2_input`](https://docs.ropensci.org/beautier/reference/create_beast2_input.md)

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

inference_model <- init_inference_model(
  input_filename = get_fasta_filename(),
  inference_model = create_inference_model(
    beauti_options = create_beauti_options_v2_4()
  )
)
create_beast2_input_distr(
  inference_model = inference_model
)
#>  [1] "<distribution id=\"posterior\" spec=\"util.CompoundDistribution\">"                                                                                                                
#>  [2] "    <distribution id=\"prior\" spec=\"util.CompoundDistribution\">"                                                                                                                
#>  [3] "        <distribution id=\"YuleModel.t:test_output_0\" spec=\"beast.evolution.speciation.YuleModel\" birthDiffRate=\"@birthRate.t:test_output_0\" tree=\"@Tree.t:test_output_0\"/>"
#>  [4] "        <prior id=\"YuleBirthRatePrior.t:test_output_0\" name=\"distribution\" x=\"@birthRate.t:test_output_0\">"                                                                  
#>  [5] "            <Uniform id=\"Uniform.100\" name=\"distr\" upper=\"Infinity\"/>"                                                                                                       
#>  [6] "        </prior>"                                                                                                                                                                  
#>  [7] "    </distribution>"                                                                                                                                                               
#>  [8] "    <distribution id=\"likelihood\" spec=\"util.CompoundDistribution\" useThreads=\"true\">"                                                                                       
#>  [9] "        <distribution id=\"treeLikelihood.test_output_0\" spec=\"ThreadedTreeLikelihood\" data=\"@test_output_0\" tree=\"@Tree.t:test_output_0\">"                                 
#> [10] "            <siteModel id=\"SiteModel.s:test_output_0\" spec=\"SiteModel\">"                                                                                                       
#> [11] "                <parameter id=\"mutationRate.s:test_output_0\" estimate=\"false\" name=\"mutationRate\">1.0</parameter>"                                                           
#> [12] "                <parameter id=\"gammaShape.s:test_output_0\" estimate=\"false\" name=\"shape\">1.0</parameter>"                                                                    
#> [13] "                <parameter id=\"proportionInvariant.s:test_output_0\" estimate=\"false\" lower=\"0.0\" name=\"proportionInvariant\" upper=\"1.0\">0.0</parameter>"                 
#> [14] "                <substModel id=\"JC69.s:test_output_0\" spec=\"JukesCantor\"/>"                                                                                                    
#> [15] "            </siteModel>"                                                                                                                                                          
#> [16] "            <branchRateModel id=\"StrictClock.c:test_output_0\" spec=\"beast.evolution.branchratemodel.StrictClockModel\">"                                                        
#> [17] "                <parameter id=\"clockRate.c:test_output_0\" estimate=\"false\" name=\"clock.rate\">1.0</parameter>"                                                                
#> [18] "            </branchRateModel>"                                                                                                                                                    
#> [19] "        </distribution>"                                                                                                                                                           
#> [20] "    </distribution>"                                                                                                                                                               
#> [21] "</distribution>"                                                                                                                                                                   
 # <distribution id="posterior" spec="util.CompoundDistribution">
 #     <distribution id="prior" spec="util.CompoundDistribution">
 #       HERE, where the ID of the distribution is 'prior'
 #     </distribution>
 #     <distribution id="likelihood" ...>
 #     </distribution>
 # </distribution>

check_empty_beautier_folder()
```
