# Obtain the crown age of a phylogeny.

The crown age of a phylogeny is the time between the present and the
moment of at which the first diversification (resulting in two lineages)
happened.

## Usage

``` r
get_crown_age(phylogeny)
```

## Arguments

- phylogeny:

  The phylogeny to obtain the crown age of

## Value

the crown age of the phylogeny

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

phylogeny <- ape::read.tree(text = "(a:15,b:15):1;")
get_crown_age(phylogeny = phylogeny)
#> [1] 15

check_empty_beautier_folder()
```
