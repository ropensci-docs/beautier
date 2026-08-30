# Initializes all clock models

Initializes all clock models

## Usage

``` r
init_clock_models(fasta_filenames, clock_models, distr_id = 0, param_id = 0)
```

## Arguments

- fasta_filenames:

  One or more FASTA filenames. Use
  [`get_fasta_filename`](https://docs.ropensci.org/beautier/reference/get_fasta_filename.md)
  to obtain a testing FASTA filename.

- clock_models:

  a list of one or more clock models, as returned by
  [`create_clock_model`](https://docs.ropensci.org/beautier/reference/create_clock_model.md)

- distr_id:

  the first distributions' ID

- param_id:

  the first parameter's ID

## Value

a list of initialized clock models

## Author

Richèl J.C. Bilderbeek
