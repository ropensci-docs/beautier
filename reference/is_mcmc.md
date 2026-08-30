# Determine if the object is a valid MCMC

Determine if the object is a valid MCMC

## Usage

``` r
is_mcmc(x)
```

## Arguments

- x:

  an object, to be determined if it is a valid MCMC

## Value

TRUE if x is a valid MCMC, FALSE otherwise

## See also

Use
[`create_mcmc`](https://docs.ropensci.org/beautier/reference/create_mcmc.md)
to create an MCMC

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {
  check_empty_beautier_folder()

  # Returns TRUE
  is_mcmc(create_mcmc())
  is_mcmc(create_ns_mcmc())

  # Returns FALSE
  is_mcmc("nonsense")
  is_mcmc(NULL)
  is_mcmc(NA)
  is_mcmc("")
  is_mcmc(c())

  check_empty_beautier_folder()
}
```
