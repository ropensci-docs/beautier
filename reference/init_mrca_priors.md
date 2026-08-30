# Initializes all MRCA priors

Initializes all MRCA priors

## Usage

``` r
init_mrca_priors(mrca_priors, distr_id = 0, param_id = 0, beauti_options)
```

## Arguments

- mrca_priors:

  a list of one or more Most Recent Common Ancestor priors, as returned
  by
  [`create_mrca_prior`](https://docs.ropensci.org/beautier/reference/create_mrca_prior.md)

- distr_id:

  the first distributions' ID

- param_id:

  the first parameter's ID

- beauti_options:

  one BEAUti options object, as returned by
  [`create_beauti_options`](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)

## Value

a list of initialized MRCA priors

## Author

Richèl J.C. Bilderbeek
