# Creates the tree prior's XML for the tracelog section

Creates the tree prior's XML for the tracelog section

## Usage

``` r
tree_prior_to_xml_tracelog(tree_prior)
```

## Arguments

- tree_prior:

  a tree priors, as returned by
  [`create_tree_prior`](https://docs.ropensci.org/beautier/reference/create_tree_prior.md)

## Value

lines of XML text

## See also

all tree priors' tracelog section is created by
[`tree_priors_to_xml_tracelog`](https://docs.ropensci.org/beautier/reference/tree_priors_to_xml_tracelog.md)

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# <logger id="tracelog" ...>
#'   # Here
# </logger>

check_empty_beautier_folder()
```
