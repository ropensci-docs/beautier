# Create a parameter called alpha

Create a parameter called alpha

## Usage

``` r
create_alpha_param(id = NA, value = 0)
```

## Arguments

- id:

  the parameter's ID

- value:

  value of the parameter

## Value

a parameter called alpha

## Note

this parameter is used in a beta distribution (as returned by
[`create_beta_distr`](https://docs.ropensci.org/beautier/reference/create_beta_distr.md))
and gamma distribution (as returned by
[`create_gamma_distr`](https://docs.ropensci.org/beautier/reference/create_gamma_distr.md))
and inverse-gamma distribution (as returned by
[`create_inv_gamma_distr`](https://docs.ropensci.org/beautier/reference/create_inv_gamma_distr.md)).
It cannot be estimated (as a hyper parameter) yet.

## See also

the function
[`create_param`](https://docs.ropensci.org/beautier/reference/create_param.md)
contains a list of all parameters that can be created

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  # Create the parameter
  alpha_param <- create_alpha_param()

  # Use the parameter in a distribution
  beta_distr <- create_beta_distr(
    alpha = alpha_param
  )

  # Use the distribution to create a BEAST2 input file
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
