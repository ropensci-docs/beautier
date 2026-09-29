# Internal function

Converts a gamma distribution to XML

## Usage

``` r
gamma_distr_to_xml(
  gamma_distr,
  beauti_options = beautier::create_beauti_options()
)
```

## Arguments

- gamma_distr:

  a gamma distribution, as created by
  [`create_gamma_distr`](https://docs.ropensci.org/beautier/reference/create_gamma_distr.md))

- beauti_options:

  one BEAUti options object, as returned by
  [`create_beauti_options`](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)

## Value

the distribution as XML text

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# gamma distribution must be initialized
gamma_distr_to_xml(
  gamma_distr = create_gamma_distr(
    id = "0",
    alpha = create_alpha_param(id = "2", value = "0.5396"),
    beta = create_beta_param(id = "3", value = "0.3819")
  )
)
#> [1] "<Gamma id=\"Gamma.0\" name=\"distr\">"                                                     
#> [2] "    <parameter id=\"RealParameter.2\" estimate=\"false\" name=\"alpha\">0.5396</parameter>"
#> [3] "    <parameter id=\"RealParameter.3\" estimate=\"false\" name=\"beta\">0.3819</parameter>" 
#> [4] "</Gamma>"                                                                                  

check_empty_beautier_folder()
```
