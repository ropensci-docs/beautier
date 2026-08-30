# Create a beta distribution

Create a beta distribution

## Usage

``` r
create_beta_distr(
  id = NA,
  alpha = 0,
  beta = 1,
  value = NA,
  lower = NA,
  upper = NA
)
```

## Arguments

- id:

  the distribution's ID

- alpha:

  the alpha shape parameter, a numeric value. The value of alpha must be
  at least 0.0. For advanced usage, use the structure as returned by
  [`create_alpha_param`](https://docs.ropensci.org/beautier/reference/create_alpha_param.md).

- beta:

  the beta shape parameter, a numeric value. The value of beta must be
  at least 1.0. For advanced usage, use the structure as returned by
  [`create_beta_param`](https://docs.ropensci.org/beautier/reference/create_beta_param.md).

- value:

  the initial value for the MCMC

- lower:

  the lower bound, the lowest possible value

- upper:

  an upper limit of the uniform distribution. If the upper limits needs
  to be infinity, set `upper` to `Inf`.

## Value

a beta distribution

## See also

the function
[`create_distr`](https://docs.ropensci.org/beautier/reference/create_distr.md)
shows an overview of all supported distributions

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  beta_distr <- create_beta_distr()

  beast2_input_file <- get_beautier_tempfilename()
  create_beast2_input_file(
    input_filename = get_fasta_filename(),
    beast2_input_file,
    tree_prior = create_yule_tree_prior(
      birth_rate_distr = beta_distr
    )
  )
  file.remove(beast2_input_file)

  remove_beautier_folder()
}
```
