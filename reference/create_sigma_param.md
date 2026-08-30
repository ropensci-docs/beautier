# Create a parameter called sigma

Create a parameter called sigma

## Usage

``` r
create_sigma_param(id = NA, value = 1)
```

## Arguments

- id:

  the parameter's ID

- value:

  value of the parameter

## Value

a parameter called sigma

## Note

this parameter is used in a normal distribution (as returned by
[`create_normal_distr`](https://docs.ropensci.org/beautier/reference/create_normal_distr.md))

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
  sigma_param <- create_sigma_param()

  # Use the parameter in a distribution
  normal_distr <- create_normal_distr(
    sigma = sigma_param
  )

  # Use the distribution to create a BEAST2 input file
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
