# Conclude the ID from a FASTA filename.

This is done in the same way as BEAST2 will do so.

## Usage

``` r
get_alignment_id(fasta_filename, capitalize_first_char_id = FALSE)
```

## Arguments

- fasta_filename:

  a FASTA filename. Use
  [`get_fasta_filename`](https://docs.ropensci.org/beautier/reference/get_fasta_filename.md)
  to obtain a testing FASTA filename. Note that BEAST2 also supports
  missing data, by using a dash (`-`) or question mark (`?`) as a
  sequence.

- capitalize_first_char_id:

  if TRUE, the first character will be capitalized

## Value

an alignment's ID

## See also

Use
[check_alignment_id](https://docs.ropensci.org/beautier/reference/check_alignment_id.md)
to check if an alignment ID is valid.

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# Path need not exist, use UNIX path as example
# anthus_aco_sub
alignment_id <- get_alignment_id("/home/homer/anthus_aco_sub.fas")
check_alignment_id(alignment_id)

check_empty_beautier_folder()
```
