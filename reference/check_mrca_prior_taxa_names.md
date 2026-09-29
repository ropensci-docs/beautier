# Check the MRCA prior's taxon names are valid.

Will [stop](https://rdrr.io/r/base/stop.html) if not.

## Usage

``` r
check_mrca_prior_taxa_names(taxa_names)
```

## Arguments

- taxa_names:

  names of the taxa, as returned by
  [`get_taxa_names`](https://docs.ropensci.org/beautier/reference/get_taxa_names.md).
  Keep at `NA` to have it initialized automatically, using all taxa in
  the alignment

## Value

No return value, called for side effects
