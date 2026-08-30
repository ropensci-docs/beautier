# Create a parameter called mu

Create a parameter called mu

## Usage

``` r
create_mu_param(id = NA, value = 0)
```

## Arguments

- id:

  the parameter's ID

- value:

  value of the parameter

## Value

a parameter called mu

## Note

this parameter is used in a Laplace distribution (as returned by
[`create_laplace_distr`](https://docs.ropensci.org/beautier/reference/create_laplace_distr.md)).
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
  mu_param <- create_mu_param()

  # Use the parameter in a distribution
  laplace_distr <- create_laplace_distr(
    mu = mu_param
  )

  # Use the distribution to create a BEAST2 input file
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
