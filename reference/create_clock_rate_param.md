# Create a parameter called `clock_rate`, as needed by [`create_strict_clock_model`](https://docs.ropensci.org/beautier/reference/create_strict_clock_model.md)

Create a parameter called `clock_rate`, as needed by
[`create_strict_clock_model`](https://docs.ropensci.org/beautier/reference/create_strict_clock_model.md)

## Usage

``` r
create_clock_rate_param(value = "1.0", estimate = FALSE, id = NA)
```

## Arguments

- value:

  value of the parameter

- estimate:

  TRUE if this parameter is to be estimated by BEAST2, FALSE otherwise

- id:

  the parameter's ID

## Value

a parameter called rate

## Note

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

  clock_rate_param <- create_clock_rate_param(
    id = "anthus_aco", value = 1.0
  )

  # Use the parameter in a clock model
  strict_clock_model <- create_strict_clock_model(
    clock_rate_param = clock_rate_param
  )

  # Use the distribution to create a BEAST2 input file
  beast2_input_file <- get_beautier_tempfilename()
  create_beast2_input_file(
    input_filename = get_fasta_filename(),
    beast2_input_file,
    clock_model = strict_clock_model
  )
  file.remove(beast2_input_file)

  remove_beautier_folder()
}
```
