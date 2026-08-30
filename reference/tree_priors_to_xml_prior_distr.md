# Creates the distribution section in the prior section of the distribution section of a BEAST2 XML parameter file.

These lines start with '\<distribution id='

## Usage

``` r
tree_priors_to_xml_prior_distr(tree_priors, beauti_options)
```

## Arguments

- tree_priors:

  one or more tree priors, as returned by
  [`create_tree_prior`](https://docs.ropensci.org/beautier/reference/create_tree_prior.md)

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
