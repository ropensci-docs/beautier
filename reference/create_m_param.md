# Create a parameter called m

Create a parameter called m

## Usage

``` r
create_m_param(id = NA, estimate = FALSE, lower = NA, upper = NA, value = 0)
```

## Arguments

- id:

  the parameter's ID

- estimate:

  TRUE if this parameter is to be estimated by BEAST2, FALSE otherwise

- lower:

  lowest possible value of the parameter. If the parameter is estimated,
  `lower` must be less than `value`

- upper:

  upper value of the parameter

- value:

  value of the parameter

## Value

a parameter called m

## Note

this parameter is used in a log-normal distribution (as returned by
[`create_log_normal_distr`](https://docs.ropensci.org/beautier/reference/create_log_normal_distr.md))
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
  m_param <- create_m_param()

  # Use the parameter in a distribution
  log_normal_distr <- create_log_normal_distr(
    m = m_param
  )

  # Use the distribution to create a BEAST2 input file
  beast2_input_file <- get_beautier_tempfilename()
  create_beast2_input_file(
    input_filename = get_fasta_filename(),
    beast2_input_file,
    tree_prior = create_yule_tree_prior(
      birth_rate_distr = log_normal_distr
    )
  )
  file.remove(beast2_input_file)

  remove_beautier_folder()

}
```
