# Function to create the BEAUti options for version 2.4.

Function to create the BEAUti options for version 2.4, by calling
[create_beauti_options](https://docs.ropensci.org/beautier/reference/create_beauti_options.md).

## Usage

``` r
create_beauti_options_v2_4()
```

## Value

a BEAUti options structure

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {
  check_empty_beautier_folder()

  beauti_options <- create_beauti_options_v2_4()
  xml <- create_beast2_input(
    get_fasta_filename(),
    beauti_options = beauti_options
  )

  check_empty_beautier_folder()
}
```
