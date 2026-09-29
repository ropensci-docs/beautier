# Internal function

Internal debug function to compare the actually created lines to
expected lines using any diff tool

## Usage

``` r
compare_lines(
  lines,
  expected,
  section = NA,
  created_lines_filename = beautier::get_beautier_tempfilename(pattern = "created",
    fileext = ".xml"),
  expected_lines_filename = beautier::get_beautier_tempfilename(pattern = "expected",
    fileext = ".xml")
)
```

## Arguments

- lines:

  the created lines

- expected:

  the expected/goal/target lines

- section:

  the XML section. Leave at NA to compare all lines

- created_lines_filename:

  name of the file where the (section of the) created lines are stored

- expected_lines_filename:

  name of the file where the (section of the) expected lines are stored

## Value

nothing. Instead, two files are created, with the names
`created_lines_filename` and `expected_lines_filename` that contain the
section under investigation, so that a diff tool can compare these

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# Creates temporary files in beautier folder
compare_lines(
  lines = readLines(get_beautier_path("bd_2_4.xml")),
  expected = readLines(get_beautier_path("bd_2_4.xml"))
)

remove_beautier_folder()
check_empty_beautier_folder()
```
