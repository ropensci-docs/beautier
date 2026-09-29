# Internal function

Converts a TN93 site model to XML, used in the `prior` section

## Usage

``` r
tn93_site_model_to_xml_prior_distr(site_model, beauti_options)
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
tn93_site_model_to_xml_prior_distr(
  site_model = create_tn93_site_model(
    id = 1,
    kappa_1_prior_distr = create_uniform_distr(id = 2),
    kappa_2_prior_distr = create_uniform_distr(id = 3)
  ),
  beauti_options = beautier::create_beauti_options()
)
#> [1] "<prior id=\"kappa1Prior.s:1\" name=\"distribution\" x=\"@kappa1.s:1\">"
#> [2] "    <Uniform id=\"Uniform.2\" name=\"distr\" upper=\"Infinity\"/>"     
#> [3] "</prior>"                                                              
#> [4] "<prior id=\"kappa2Prior.s:1\" name=\"distribution\" x=\"@kappa2.s:1\">"
#> [5] "    <Uniform id=\"Uniform.3\" name=\"distr\" upper=\"Infinity\"/>"     
#> [6] "</prior>"                                                              
```
