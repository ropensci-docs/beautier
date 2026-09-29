# Get the alignment ID from one or more FASTA filenames.

This is done in the same way as BEAST2 does by default. The files are
assumed to be FASTA. If this is not the case, there may be any kind of
error message when calling this function.

## Usage

``` r
get_alignment_ids_from_fasta_filenames(fasta_filenames)
```

## Arguments

- fasta_filenames:

  One or more FASTA filenames. Use
  [`get_fasta_filename`](https://docs.ropensci.org/beautier/reference/get_fasta_filename.md)
  to obtain a testing FASTA filename.

## Value

the IDs from one or more FASTA files

## See also

Use
[get_alignment_ids](https://docs.ropensci.org/beautier/reference/get_alignment_ids.md)
to get the alignment IDs from multiple kids of files. Use
[are_fasta_filenames](https://docs.ropensci.org/beautier/reference/are_fasta_filenames.md)
to see if the filenames all have a common FASTA filename extension.

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

get_alignment_ids_from_fasta_filenames(
  get_beautier_paths(c("anthus_aco.fas", "anthus_nd2.fas"))
)
#> [1] "anthus_aco" "anthus_nd2"

check_empty_beautier_folder()
```
