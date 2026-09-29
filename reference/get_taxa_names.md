# Extract the names of taxa from a file

Extract the names of taxa from a file

## Usage

``` r
get_taxa_names(filename)
```

## Arguments

- filename:

  name of a FASTA file

## Value

the taxa names

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

get_taxa_names(get_beautier_path("anthus_aco_sub.fas"))
#> [1] "61430_aco"  "626029_aco" "630116_aco" "630210_aco" "B25702_aco"

check_empty_beautier_folder()
```
