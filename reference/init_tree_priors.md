# Initializes all tree priors

Initializes all tree priors

## Usage

``` r
init_tree_priors(tree_priors, ids, distr_id = 0, param_id = 0)
```

## Arguments

- tree_priors:

  one or more tree priors, as returned by
  [`create_tree_prior`](https://docs.ropensci.org/beautier/reference/create_tree_prior.md)

- ids:

  one or more alignments' IDs. IDs can be extracted from their FASTA
  filenames with
  [`get_alignment_ids_from_fasta_filenames`](https://docs.ropensci.org/beautier/reference/get_alignment_ids_from_fasta_filenames.md))

- distr_id:

  the first distributions' ID

- param_id:

  the first parameter's ID

## Value

a list of initialized tree priors

## Author

Richèl J.C. Bilderbeek
