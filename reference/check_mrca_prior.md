# Check if the MRCA prior is a valid MRCA prior.

Calls `stop` if the MRCA prior is invalid.

## Usage

``` r
check_mrca_prior(mrca_prior)
```

## Arguments

- mrca_prior:

  a Most Recent Common Ancestor prior, as returned by
  [`create_mrca_prior`](https://docs.ropensci.org/beautier/reference/create_mrca_prior.md)

## Value

nothing

## See also

Use
[create_mrca_prior](https://docs.ropensci.org/beautier/reference/create_mrca_prior.md)
to create a valid MRCA prior

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

fasta_filename <- get_beautier_path("anthus_aco.fas")
mrca_prior <- create_mrca_prior(
  alignment_id = get_alignment_id(fasta_filename = fasta_filename),
  taxa_names = get_taxa_names(filename = fasta_filename)
)
mrca_prior <- create_mrca_prior(
 alignment_id = get_alignment_id(fasta_filename = fasta_filename),
 taxa_names = get_taxa_names(filename = fasta_filename)
)
check_mrca_prior(mrca_prior)

check_empty_beautier_folder()
```
