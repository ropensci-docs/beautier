# Checks if the input is a phylogeny

Checks if the input is a phylogeny

## Usage

``` r
is_phylo(x)
```

## Arguments

- x:

  input to be checked

## Value

TRUE or FALSE

## See also

Use
[check_phylogeny](https://docs.ropensci.org/beautier/reference/check_phylogeny.md)
to check for a phylogeny

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# TRUE
phylogeny <- ape::read.tree(text = "(a:15,b:15):1;")
is_phylo(phylogeny)
#> [1] TRUE

# FALSE
is_phylo("nonsense")
#> [1] FALSE
is_phylo(NA)
#> [1] FALSE
is_phylo(NULL)
#> [1] FALSE

check_empty_beautier_folder()
```
