# Determine if an MRCA prior's alignment IDs are present in the FASTA files

Determine if an MRCA prior's alignment IDs are present in the FASTA
files

## Usage

``` r
is_mrca_align_ids_in_fastas(mrca_prior, fasta_filenames)
```

## Arguments

- mrca_prior:

  a Most Recent Common Ancestor prior, as returned by
  [`create_mrca_prior`](https://docs.ropensci.org/beautier/reference/create_mrca_prior.md)

- fasta_filenames:

  One or more FASTA filenames. Use
  [`get_fasta_filename`](https://docs.ropensci.org/beautier/reference/get_fasta_filename.md)
  to obtain a testing FASTA filename.

## Value

TRUE if the MRCA prior's alignment IDs is present in the FASTA files.
Returns FALSE otherwise

## Author

Richèl J.C. Bilderbeek
