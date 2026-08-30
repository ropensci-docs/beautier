# Creates the tree priors' XML for the tracelog section

Creates the tree priors' XML for the tracelog section

## Usage

``` r
tree_priors_to_xml_tracelog(tree_priors)
```

## Arguments

- tree_priors:

  one or more tree priors, as returned by
  [`create_tree_prior`](https://docs.ropensci.org/beautier/reference/create_tree_prior.md)

## Value

lines of XML text

## See also

the complete tracelog section is created by
[`create_tracelog_xml`](https://docs.ropensci.org/beautier/reference/create_tracelog_xml.md)

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
