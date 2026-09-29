# Determine if the MRCA priors' taxa names are present in the FASTA files

Determine if the MRCA priors' taxa names are present in the FASTA files

## Usage

``` r
are_mrca_taxon_names_in_fasta(mrca_prior, fasta_filename)
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

TRUE if the MRCA priors' taxa names are present in the FASTA files.
FALSE otherwise.

## Author

Richèl J.C. Bilderbeek
