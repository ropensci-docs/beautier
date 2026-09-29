# Create a Most Recent Common Ancestor prior

Create a Most Recent Common Ancestor prior

## Usage

``` r
create_mrca_prior(
  alignment_id = NA,
  taxa_names = NA,
  is_monophyletic = FALSE,
  mrca_distr = NA,
  name = NA,
  clock_prior_distr_id = NA
)
```

## Arguments

- alignment_id:

  ID of the alignment, as returned by
  [get_alignment_id](https://docs.ropensci.org/beautier/reference/get_alignment_id.md).
  Keep at `NA` to have it initialized automatically

- taxa_names:

  names of the taxa, as returned by
  [`get_taxa_names`](https://docs.ropensci.org/beautier/reference/get_taxa_names.md).
  Keep at `NA` to have it initialized automatically, using all taxa in
  the alignment

- is_monophyletic:

  boolean to indicate monophyly is assumed in a Most Recent Common
  Ancestor prior, as returned by `create_mrca_prior`

- mrca_distr:

  the distribution used by the MRCA prior. Can be NA (the default) or
  any distribution returned by
  [`create_distr`](https://docs.ropensci.org/beautier/reference/create_distr.md)

- name:

  the unique name of the MRCA prior, for example a genus, family, order
  or even class name. Leave at [NA](https://rdrr.io/r/base/NA.html) to
  have it named automatically.

- clock_prior_distr_id:

  ID of an MRCA clock model's distribution. Keep at `NA` to have it
  initialized automatically

## Value

an MRCA prior

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

fasta_filename <- get_beautier_path("anthus_aco.fas")

 # The first two taxa are sister species
 mrca_prior <- create_mrca_prior(
   taxa_names = get_taxa_names(filename = fasta_filename)[1:2]
 )

 # The taxa are monophyletic
 mrca_prior <- create_mrca_prior(
   taxa_names = get_taxa_names(filename = fasta_filename),
   is_monophyletic = TRUE
 )

 # Set the crown age to 10
 mrca_prior <- create_mrca_prior(
   taxa_names = get_taxa_names(fasta_filename),
   mrca_distr = create_normal_distr(mean = 10, sigma = 0.1)
 )

check_empty_beautier_folder()
```
