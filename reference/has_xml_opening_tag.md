# Is an XML opening tag with value 'section' present among the lines of the text?

Is an XML opening tag with value 'section' present among the lines of
the text?

## Usage

``` r
has_xml_opening_tag(lines, section = NA)
```

## Arguments

- lines:

  lines of an XML text

- section:

  if NA, this function returns TRUE if there is any XML opening tag. If
  `section` is set to a certain word, this function returns TRUE if that
  tag matches `section`

## Value

lines of XML text

## Author

Richèl J.C. Bilderbeek
