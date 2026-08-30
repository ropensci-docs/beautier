# Create a parameter called lambda

Create a parameter called lambda

## Usage

``` r
create_lambda_param(id = NA, value = 0)
```

## Arguments

- id:

  the parameter's ID

- value:

  value of the parameter

## Value

a parameter called lambda

## Note

this parameter is used in a Poisson distribution (as returned by
[`create_poisson_distr`](https://docs.ropensci.org/beautier/reference/create_poisson_distr.md))

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
  lambda_param <- create_lambda_param()

  # Use the parameter in a distribution
  poisson_distr <- create_poisson_distr(
    lambda = lambda_param
  )

  # Use the distribution to create a BEAST2 input file
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
