# Create a Laplace distribution

Create a Laplace distribution

## Usage

``` r
create_laplace_distr(
  id = NA,
  mu = 0,
  scale = 1,
  value = NA,
  lower = NA,
  upper = NA
)
```

## Arguments

- id:

  the distribution's ID

- mu:

  the mu parameter, a numeric value. For advanced usage, use the
  structure as returned by
  [`create_mu_param`](https://docs.ropensci.org/beautier/reference/create_mu_param.md)

- scale:

  the scale parameter, a numeric value. For advanced usage, use the
  structure as returned by
  [`create_scale_param`](https://docs.ropensci.org/beautier/reference/create_scale_param.md)

- value:

  the initial value for the MCMC

- lower:

  the lower bound, the lowest possible value

- upper:

  an upper limit of the uniform distribution. If the upper limits needs
  to be infinity, set `upper` to `Inf`.

## Value

a Laplace distribution

## See also

the function
[`create_distr`](https://docs.ropensci.org/beautier/reference/create_distr.md)
shows an overview of all supported distributions

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  laplace_distr <- create_laplace_distr()

  beast2_input_file <- get_beautier_tempfilename()
  create_beast2_input_file(
    input_filename = get_fasta_filename(),
    beast2_input_file,
    tree_prior = create_yule_tree_prior(
      birth_rate_distr = laplace_distr
    )
  )
  file.remove(beast2_input_file)

  remove_beautier_folder()
}
```
