# Get the alignment IDs from one or more files.

This is done in the same way as BEAST2 does by default The file
extension will be used to determine which type of file is worked on.

## Usage

``` r
get_alignment_ids(filenames)
```

## Arguments

- filenames:

  names of the files to be checked

## Value

the IDs extracted from the one or more files

## See also

Use
[get_alignment_ids_from_fasta_filenames](https://docs.ropensci.org/beautier/reference/get_alignment_ids_from_fasta_filenames.md)
to get the alignment IDs from files known to be FASTA files

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

get_alignment_ids(
  get_beautier_paths(c("anthus_aco.fas", "anthus_nd2.fas"))
)
#> [1] "anthus_aco" "anthus_nd2"

check_empty_beautier_folder()
```
