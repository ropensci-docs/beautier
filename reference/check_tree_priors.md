# Check if the object is a list of one or more tree priors.

Will [stop](https://rdrr.io/r/base/stop.html) if the object is not a
list of one or more tree priors.

## Usage

``` r
check_tree_priors(tree_priors)
```

## Arguments

- tree_priors:

  the object to be checked if it is a list of one or more valid tree
  priors

## Value

nothing. Will [stop](https://rdrr.io/r/base/stop.html) if the object is
not a list of one or more tree priors.

## See also

Use
[create_tree_prior](https://docs.ropensci.org/beautier/reference/create_tree_prior.md)
to create a valid tree prior

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

check_tree_priors(create_yule_tree_prior())
check_tree_priors(list(create_yule_tree_prior()))
check_tree_priors(list(create_yule_tree_prior(), create_bd_tree_prior()))

check_empty_beautier_folder()
```
