# Creates the data section of a BEAST2 XML parameter file

Creates the data section of a BEAST2 XML parameter file

## Usage

``` r
create_beast2_input_data_sequences(
  input_fasta_filename,
  beauti_options = beautier::create_beauti_options()
)
```

## Arguments

- input_fasta_filename:

  one FASTA filename

- beauti_options:

  one BEAUti options object, as returned by
  [`create_beauti_options`](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)

## Value

lines of XML text

## Author

Richèl J.C. Bilderbeek
