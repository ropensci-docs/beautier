# Create the `<beast ...>` XML

The `<beast ...>` XML is the XML at the start of a BEAST2 XML input
file, directly after the general XML declaration (as created by
[create_xml_declaration](https://docs.ropensci.org/beautier/reference/create_xml_declaration.md)).

## Usage

``` r
create_beast2_beast_xml(beauti_options)
```

## Arguments

- beauti_options:

  one BEAUti options object, as returned by
  [`create_beauti_options`](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)

## Value

the XML

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
remove_beautier_folder()

create_beast2_beast_xml(
  beauti_options = create_beauti_options_v2_6()
)
#> [1] "<beast beautitemplate='Standard' beautistatus='' namespace=\"beast.core:beast.evolution.alignment:beast.evolution.tree.coalescent:beast.core.util:beast.evolution.nuc:beast.evolution.operators:beast.evolution.sitemodel:beast.evolution.substitutionmodel:beast.evolution.likelihood\" required=\"\" version=\"2.6\">"

check_empty_beautier_folder()
```
