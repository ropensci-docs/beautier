# Create a Poisson distribution

Create a Poisson distribution

## Usage

``` r
create_poisson_distr(id = NA, lambda = 0, value = NA, lower = NA, upper = NA)
```

## Arguments

- id:

  the distribution's ID

- lambda:

  the lambda parameter, a numeric value. For advanced usage, use the
  structure as returned by
  [`create_lambda_param`](https://docs.ropensci.org/beautier/reference/create_lambda_param.md)

- value:

  the initial value for the MCMC

- lower:

  the lower bound, the lowest possible value

- upper:

  an upper limit of the uniform distribution. If the upper limits needs
  to be infinity, set `upper` to `Inf`.

## Value

a Poisson distribution

## See also

the function
[`create_distr`](https://docs.ropensci.org/beautier/reference/create_distr.md)
shows an overview of all supported distributions

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  poisson_distr <- create_poisson_distr()

  beast2_input_file <- get_beautier_tempfilename()
  create_beast2_input_file(
    input_filename = get_fasta_filename(),
    beast2_input_file,
    tree_prior = create_yule_tree_prior(
      birth_rate_distr = poisson_distr
    )
  )
  file.remove(beast2_input_file)

  remove_beautier_folder()
}
```
