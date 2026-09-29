# Initializes all site models

Initializes all site models

## Usage

``` r
init_site_models(site_models, ids, distr_id = 0, param_id = 0)
```

## Arguments

- site_models:

  one or more site models, as returned by
  [`create_site_model`](https://docs.ropensci.org/beautier/reference/create_site_model.md)

- ids:

  one or more alignments' IDs. IDs can be extracted from their FASTA
  filenames with
  [`get_alignment_ids_from_fasta_filenames`](https://docs.ropensci.org/beautier/reference/get_alignment_ids_from_fasta_filenames.md))

- distr_id:

  the first distributions' ID

- param_id:

  the first parameter's ID

## Value

a list of initialized site models

## Author

Richèl J.C. Bilderbeek
