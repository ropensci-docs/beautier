# Internal function

Converts an HKY site model to XML, used in the `prior` section

## Usage

``` r
hky_site_model_to_xml_prior_distr(site_model, beauti_options)
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
hky_site_model_to_xml_prior_distr(
  site_model = create_hky_site_model(
    id = 1,
    kappa_prior_distr = create_uniform_distr(id = 2)
  ),
  beauti_options = beautier::create_beauti_options()
)
#> [1] "<prior id=\"KappaPrior.s:1\" name=\"distribution\" x=\"@kappa.s:1\">"
#> [2] "    <Uniform id=\"Uniform.2\" name=\"distr\" upper=\"Infinity\"/>"   
#> [3] "</prior>"                                                            
```
