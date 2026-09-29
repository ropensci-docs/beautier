# Create a parameter called 'rate CG'

Create a parameter called 'rate CG'

## Usage

``` r
create_rate_cg_param(id = NA, estimate = TRUE, value = "1.0", lower = "0.0")
```

## Arguments

- id:

  the parameter's ID

- estimate:

  TRUE if this parameter is to be estimated by BEAST2, FALSE otherwise

- value:

  value of the parameter

- lower:

  lowest possible value of the parameter. If the parameter is estimated,
  `lower` must be less than `value`

## Value

a parameter called 'rate CG'

## See also

the function
[`create_param`](https://docs.ropensci.org/beautier/reference/create_param.md)
contains a list of all parameters that can be created

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  # Create parameter
  rate_cg_param <- create_rate_cg_param(value = 1, estimate = FALSE)

  # Use the parameter to create a BEAST2 input file
  beast2_input_file <- get_beautier_tempfilename()
  create_beast2_input_file(
    input_filename = get_fasta_filename(),
    beast2_input_file,
    site_model = create_gtr_site_model(
      rate_cg_param = rate_cg_param
    )
  )
  file.remove(beast2_input_file)

  remove_beautier_folder()
}
```
