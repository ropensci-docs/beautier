# Determine if XML files result in equal trees

Determine if XML files result in equal trees

## Usage

``` r
are_equal_xml_files(filename_1, filename_2, section)
```

## Arguments

- filename_1:

  name of a first XML file

- filename_2:

  name of a second XML file

- section:

  name of an XML section. Assumes that there is one line that starts
  with `<section` (excluding whitespace) and one line that is
  `</section>` (also excluding whitespace)

## Value

TRUE if the two sections of the XML files are equal, FALSE otherwise

## See also

to check for equivalence, use
[`are_equivalent_xml_files`](https://docs.ropensci.org/beautier/reference/are_equivalent_xml_files.md)

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

are_equal_xml_files(
  filename_1 = get_beautier_path("2_4.xml"),
  filename_2 = get_beautier_path("2_6_0.xml"),
  section = "taxonset"
)
#> [1] FALSE

check_empty_beautier_folder()
```
