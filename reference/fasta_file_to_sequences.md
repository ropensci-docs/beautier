# Convert a FASTA file to a table of sequences

Convert a FASTA file to a table of sequences

## Usage

``` r
fasta_file_to_sequences(fasta_filename)
```

## Arguments

- fasta_filename:

  One existing FASTA filenames

## Value

a table of sequences

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

fasta_file_to_sequences(fasta_filename = get_fasta_filename())
#>               sequences
#> t4 aacgacccgcgatcggggat
#> t1 acttgttgcgactgcgcctg
#> t5 acttgttgcgactgagcctg
#> t2 acttattgcgactgaggccg
#> t3 acttaatgcgaatgagcccg

check_empty_beautier_folder()
```
