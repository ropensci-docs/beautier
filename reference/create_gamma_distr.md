# Create a gamma distribution

Create a gamma distribution

## Usage

``` r
create_gamma_distr(
  id = NA,
  alpha = 0.5396,
  beta = 0.3819,
  value = NA,
  lower = NA,
  upper = NA
)
```

## Arguments

- id:

  the distribution's ID

- alpha:

  the alpha shape parameter, a numeric value. For advanced usage, use
  the structure as returned by
  [`create_alpha_param`](https://docs.ropensci.org/beautier/reference/create_alpha_param.md)

- beta:

  the beta shape parameter, a numeric value. For advanced usage, use the
  structure as returned by
  [`create_beta_param`](https://docs.ropensci.org/beautier/reference/create_beta_param.md)

- value:

  the initial value for the MCMC

- lower:

  the lower bound, the lowest possible value

- upper:

  an upper limit of the uniform distribution. If the upper limits needs
  to be infinity, set `upper` to `Inf`.

## Value

a gamma distribution

## See also

the function
[`create_distr`](https://docs.ropensci.org/beautier/reference/create_distr.md)
shows an overview of all supported distributions

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  gamma_distr <- create_gamma_distr(
    alpha = 0.05,
    beta = 10.0
  )

  gtr_site_model <- create_gtr_site_model(
    rate_ac_prior_distr = gamma_distr
  )

  beast2_input_file <- get_beautier_tempfilename()
  create_beast2_input_file(
    input_filename = get_fasta_filename(),
    beast2_input_file,
    site_model = gtr_site_model
  )
  file.remove(beast2_input_file)

  remove_beautier_folder()
}
```
