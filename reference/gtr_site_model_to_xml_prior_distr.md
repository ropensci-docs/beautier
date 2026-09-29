# Internal function

Converts a GTR site model to XML, used in the `prior` section

## Usage

``` r
gtr_site_model_to_xml_prior_distr(site_model, beauti_options)
```

## Arguments

- site_model:

  a site model, as returned by
  [`create_site_model`](https://docs.ropensci.org/beautier/reference/create_site_model.md)

- beauti_options:

  one BEAUti options object, as returned by
  [`create_beauti_options`](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)

## Value

the site model as XML text

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
gtr_site_model_to_xml_prior_distr(
  site_model = create_gtr_site_model(
    id = 1,
    rate_ac_prior_distr = create_uniform_distr(id = 2),
    rate_ag_prior_distr = create_uniform_distr(id = 3),
    rate_at_prior_distr = create_uniform_distr(id = 4),
    rate_cg_prior_distr = create_uniform_distr(id = 5),
    rate_gt_prior_distr = create_uniform_distr(id = 6)
  ),
  beauti_options = beautier::create_beauti_options()
)
#>  [1] "<prior id=\"RateACPrior.s:1\" name=\"distribution\" x=\"@rateAC.s:1\">"
#>  [2] "    <Uniform id=\"Uniform.2\" name=\"distr\" upper=\"Infinity\"/>"     
#>  [3] "</prior>"                                                              
#>  [4] "<prior id=\"RateAGPrior.s:1\" name=\"distribution\" x=\"@rateAG.s:1\">"
#>  [5] "    <Uniform id=\"Uniform.3\" name=\"distr\" upper=\"Infinity\"/>"     
#>  [6] "</prior>"                                                              
#>  [7] "<prior id=\"RateATPrior.s:1\" name=\"distribution\" x=\"@rateAT.s:1\">"
#>  [8] "    <Uniform id=\"Uniform.4\" name=\"distr\" upper=\"Infinity\"/>"     
#>  [9] "</prior>"                                                              
#> [10] "<prior id=\"RateCGPrior.s:1\" name=\"distribution\" x=\"@rateCG.s:1\">"
#> [11] "    <Uniform id=\"Uniform.5\" name=\"distr\" upper=\"Infinity\"/>"     
#> [12] "</prior>"                                                              
#> [13] "<prior id=\"RateGTPrior.s:1\" name=\"distribution\" x=\"@rateGT.s:1\">"
#> [14] "    <Uniform id=\"Uniform.6\" name=\"distr\" upper=\"Infinity\"/>"     
#> [15] "</prior>"                                                              
```
