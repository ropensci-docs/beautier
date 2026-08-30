# Extract the number of taxa from a file

Extract the number of taxa from a file

## Usage

``` r
get_n_taxa(filename)
```

## Arguments

- filename:

  name of a FASTA file

## Value

the number of taxa

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

fasta_filename <- get_beautier_path("test_output_5.fas")
# 5
get_n_taxa(fasta_filename)
#> [1] 5

check_empty_beautier_folder()
```
