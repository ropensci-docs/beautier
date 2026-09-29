# Determine if the file is a BEAST2 input file that has tip dating

Determine if the file is a BEAST2 input file that has tip dating

## Usage

``` r
is_beast2_input_file_with_tipdates(beast2_input_filename)
```

## Arguments

- beast2_input_filename:

  path to a BEAST2 XML input file

## Value

TRUE if x is the BEAST2 input file has tip dating, FALSE otherwise

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

is_beast2_input_file_with_tipdates(
  get_beautier_path("babette_issue_109_expected_v2_6.xml")
) # TRUE
#> [1] TRUE

check_empty_beautier_folder()
```
