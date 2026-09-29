# Create an normal distribution

Create an normal distribution

## Usage

``` r
create_normal_distr(
  id = NA,
  mean = 0,
  sigma = 1,
  value = NA,
  lower = NA,
  upper = NA
)
```

## Arguments

- id:

  the distribution's ID

- mean:

  the mean parameter, a numeric value. For advanced usage, use the
  structure as returned by
  [`create_mean_param`](https://docs.ropensci.org/beautier/reference/create_mean_param.md)

- sigma:

  the sigma parameter, a numeric value. For advanced usage, use the
  structure as returned by
  [`create_sigma_param`](https://docs.ropensci.org/beautier/reference/create_sigma_param.md)

- value:

  the initial value for the MCMC

- lower:

  the lower bound, the lowest possible value

- upper:

  an upper limit of the uniform distribution. If the upper limits needs
  to be infinity, set `upper` to `Inf`.

## Value

a normal distribution

## See also

the function
[`create_distr`](https://docs.ropensci.org/beautier/reference/create_distr.md)
shows an overview of all supported distributions

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  normal_distr <- create_normal_distr()

  beast2_input_file <- get_beautier_tempfilename()
  create_beast2_input_file(
    input_filename = get_fasta_filename(),
    beast2_input_file,
    tree_prior = create_yule_tree_prior(
      birth_rate_distr = normal_distr
    )
  )
  file.remove(beast2_input_file)

  remove_beautier_folder()
}
```
