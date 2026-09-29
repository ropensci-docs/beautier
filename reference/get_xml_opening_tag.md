# Get the XML opening tag

Get the XML opening tag

## Usage

``` r
get_xml_opening_tag(text)
```

## Arguments

- text:

  text to be determined to be valid

## Value

the opening tag if found, else NA

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# my_tag
get_xml_opening_tag("<my_tag text=something/>")
#> [1] "my_tag"

# NA when there is no opening tag
get_xml_opening_tag("no_xml")
#> [1] NA

check_empty_beautier_folder()
```
