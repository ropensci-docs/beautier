# Get the XML closing tag

Get the XML closing tag

## Usage

``` r
get_xml_closing_tag(text)
```

## Arguments

- text:

  lines of XML to extract the XML closing tag from

## Value

the closing tag if found, else NA

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# my_tag
get_xml_closing_tag("<my_tag text=something></my_tag>")
#> [1] "my_tag"

# Will return NA
get_xml_closing_tag("<my_tag text=something/>")
#> [1] NA
get_xml_closing_tag("no_xml")
#> [1] NA

check_empty_beautier_folder()
```
