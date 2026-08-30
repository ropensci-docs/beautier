# Determine of the object is an empty (`NA`) or valid MRCA prior.

Determine of the object is an empty (`NA`) or valid MRCA prior.

## Usage

``` r
is_mrca_prior(mrca_prior)
```

## Arguments

- mrca_prior:

  a Most Recent Common Ancestor prior, as returned by
  [`create_mrca_prior`](https://docs.ropensci.org/beautier/reference/create_mrca_prior.md)

## Value

TRUE if `x` is an MRCA prior, FALSE otherwise

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# TRUE
is_mrca_prior(create_mrca_prior())
#> [1] TRUE
# Also 'NA' is a valid MRCA prior,
# denoting that there no MRCA priors
is_mrca_prior(NA)
#> [1] TRUE

# FALSE
is_mrca_prior(NULL)
#> [1] FALSE
is_mrca_prior("nonsense")
#> [1] FALSE

check_empty_beautier_folder()
```
