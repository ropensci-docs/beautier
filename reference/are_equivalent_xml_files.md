# Internal function

Internal function used for debugging to determine if XML files result in
equivalent trees

## Usage

``` r
are_equivalent_xml_files(filename_1, filename_2, section = NA)
```

## Arguments

- filename_1:

  name of a first XML file

- filename_2:

  name of a second XML file

- section:

  the name of the XML section, use NA to check the whole file

## Value

TRUE if the two XML files result in equivalent trees, FALSE otherwise

## See also

to check for equality, use `are_equal_xml_files`

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

are_equivalent_xml_files(
  filename_1 = get_beautier_path("2_4.xml"),
  filename_2 = get_beautier_path("2_6_0.xml")
)
#> [1] FALSE

check_empty_beautier_folder()
```
