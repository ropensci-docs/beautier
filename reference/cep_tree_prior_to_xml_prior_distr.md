# Creates the tree prior section in the prior section of the prior section of the distribution section of a BEAST2 XML parameter file for a Coalescent Exponential Population tree prior

Creates the tree prior section in the prior section of the prior section
of the distribution section of a BEAST2 XML parameter file for a
Coalescent Exponential Population tree prior

## Usage

``` r
cep_tree_prior_to_xml_prior_distr(cep_tree_prior, beauti_options)
```

## Arguments

- cep_tree_prior:

  a Coalescent Exponential Population tree prior, as returned by
  [`create_cep_tree_prior`](https://docs.ropensci.org/beautier/reference/create_cep_tree_prior.md)

- beauti_options:

  one BEAUti options object, as returned by
  [`create_beauti_options`](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)

## Value

lines of XML text

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

check_empty_beautier_folder()
```
