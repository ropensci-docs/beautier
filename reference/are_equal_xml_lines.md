# Determine if XML lines result in equal trees

Determine if XML lines result in equal trees

## Usage

``` r
are_equal_xml_lines(lines_1, lines_2, section)
```

## Arguments

- lines_1:

  lines of a first XML file

- lines_2:

  lines of a second XML file

- section:

  name of an XML section. Assumes that there is one line that starts
  with `<section` (excluding whitespace) and one line that is
  `</section>` (also excluding whitespace)

## Value

TRUE if the two sections of the XML files are equal, FALSE otherwise

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

are_equal_xml_lines(
  lines_1 = readLines(get_beautier_path("2_4.xml")),
  lines_2 = readLines(get_beautier_path("2_6_0.xml")),
  section = "taxonset"
)
#> [1] FALSE

check_empty_beautier_folder()
```
