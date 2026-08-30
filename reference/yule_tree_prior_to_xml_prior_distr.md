# Creates the `prior` section in the prior section of the prior section of the distribution section of a BEAST2 XML parameter file for a Yule tree prior

Creates the `prior` section in the prior section of the prior section of
the distribution section of a BEAST2 XML parameter file for a Yule tree
prior

## Usage

``` r
yule_tree_prior_to_xml_prior_distr(
  yule_tree_prior,
  beauti_options = beautier::create_beauti_options()
)
```

## Arguments

- yule_tree_prior:

  a Yule tree_prior, as created by
  [`create_yule_tree_prior`](https://docs.ropensci.org/beautier/reference/create_yule_tree_prior.md)

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
