# Check if the phylogeny is a valid phylogeny object.

Calls `stop` if the phylogeny is invalid

## Usage

``` r
check_phylogeny(phylogeny)
```

## Arguments

- phylogeny:

  a phylogeny of type `phylo` from the `ape` package

## Value

nothing

## See also

Use [`ape::read.tree`](https://rdrr.io/pkg/ape/man/read.tree.html) to
create a phylogeny

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# Must do nothing on phylogenies
phylogeny <- ape::read.tree(text = "(A:1, B:1):1;")
check_phylogeny(phylogeny)
#> NULL

check_empty_beautier_folder()
```
