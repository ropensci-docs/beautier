# Is an XML closing tag with short closing text in one of the lines of the text?

Is an XML closing tag with short closing text in one of the lines of the
text?

## Usage

``` r
has_xml_short_closing_tag(lines)
```

## Arguments

- lines:

  lines of an XML text

## Value

TRUE if there is an XML tag that also closes present in the lines of
text, FALSE otherwise

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# TRUE
has_xml_short_closing_tag("<my_tag id=1/>")
#> [1] TRUE
# FALSE
has_xml_short_closing_tag("<my_tag id=1>text</my_tag>")
#> [1] FALSE

check_empty_beautier_folder()
```
