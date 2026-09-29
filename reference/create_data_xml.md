# Create the `<data ..>` XML

Create the `<data ..>` XML

## Usage

``` r
create_data_xml(id, beast2_version)
```

## Arguments

- id:

  an alignment's IDs. An ID can be extracted from its FASTA filename
  with
  [`get_alignment_ids_from_fasta_filenames`](https://docs.ropensci.org/beautier/reference/get_alignment_ids_from_fasta_filenames.md))

- beast2_version:

  BEAST2 version, for example, `"2.5"`

## Value

lines of XML text

## Author

Richèl J.C. Bilderbeek
