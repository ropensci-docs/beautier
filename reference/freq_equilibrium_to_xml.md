# Creates the `freq_equilibrium` as XML

Creates the `freq_equilibrium` as XML

## Usage

``` r
freq_equilibrium_to_xml(freq_equilibrium, id)
```

## Arguments

- freq_equilibrium:

  a `freq_equilibrium` name

- id:

  a site model's name

## Value

the `freq_equilibrium` as XML

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

freq_equilibrium_to_xml(freq_equilibrium = "estimated", id = "my_id")
#> [1] "<frequencies id=\"estimatedFreqs.s:my_id\" spec=\"Frequencies\" frequencies=\"@freqParameter.s:my_id\"/>"

check_empty_beautier_folder()
```
