# Determine if an MRCA prior's alignment IDs is present in the FASTA file

Determine if an MRCA prior's alignment IDs is present in the FASTA file

## Usage

``` r
is_mrca_align_id_in_fasta(mrca_prior, fasta_filename)
```

## Arguments

- mrca_prior:

  a Most Recent Common Ancestor prior, as returned by
  [`create_mrca_prior`](https://docs.ropensci.org/beautier/reference/create_mrca_prior.md)

- fasta_filename:

  a FASTA filename. Use
  [`get_fasta_filename`](https://docs.ropensci.org/beautier/reference/get_fasta_filename.md)
  to obtain a testing FASTA filename. Note that BEAST2 also supports
  missing data, by using a dash (`-`) or question mark (`?`) as a
  sequence.

## Value

TRUE if the MRCA prior's alignment IDs is present in the FASTA file.
Returns FALSE otherwise

## Author

Richèl J.C. Bilderbeek
