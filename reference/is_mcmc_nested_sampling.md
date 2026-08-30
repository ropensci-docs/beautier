# Determine if the object is a valid Nested-Sampling MCMC, as used in \[1\]

Determine if the object is a valid Nested-Sampling MCMC, as used in
\[1\]

## Usage

``` r
is_mcmc_nested_sampling(x)
```

## Arguments

- x:

  an object, to be determined if it is a valid MCMC

## Value

TRUE if x is a valid Nested-Sampling MCMC, FALSE otherwise

## References

\* \[1\] Patricio Maturana Russel, Brendon J Brewer, Steffen Klaere,
Remco R Bouckaert; Model Selection and Parameter Inference in
Phylogenetics Using Nested Sampling, Systematic Biology, 2018, syy050,
https://doi.org/10.1093/sysbio/syy050

## See also

Use
[create_ns_mcmc](https://docs.ropensci.org/beautier/reference/create_ns_mcmc.md)
to create an NS MCMC

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {
  check_empty_beautier_folder()

  # TRUE
  is_nested_sampling_mcmc(create_ns_mcmc())
  # FALSE
  is_nested_sampling_mcmc(create_mcmc())
  is_nested_sampling_mcmc("nonsense")

  check_empty_beautier_folder()
}
```
