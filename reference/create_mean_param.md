# Create a parameter called mean

Create a parameter called mean

## Usage

``` r
create_mean_param(id = NA, value = 0)
```

## Arguments

- id:

  the parameter's ID

- value:

  value of the parameter

## Value

a parameter called mean

## Note

this parameter is used in an exponential distribution (as returned by
[`create_exp_distr`](https://docs.ropensci.org/beautier/reference/create_exp_distr.md))
and normal distribution (as returned by
[`create_normal_distr`](https://docs.ropensci.org/beautier/reference/create_normal_distr.md)).
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
  mean_param <- create_mean_param(value = 1.0)

  # Use the parameter in a distribution
  exp_distr <- create_exp_distr(
    mean = mean_param
  )

  # Use the distribution to create a BEAST2 input file
  beast2_input_file <- get_beautier_tempfilename()
  create_beast2_input_file(
    input_filename = get_fasta_filename(),
    beast2_input_file,
    tree_prior = create_yule_tree_prior(
      birth_rate_distr = exp_distr
    )
  )
  file.remove(beast2_input_file)

  remove_beautier_folder()
}
```
