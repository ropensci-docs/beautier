# Creates the `data` section of a BEAST2 XML parameter file

Creates the `data` section of a BEAST2 XML parameter file

## Usage

``` r
create_beast2_input_data(
  input_filename,
  beauti_options = beautier::create_beauti_options()
)
```

## Arguments

- input_filename:

  A FASTA filename. Use
  [`get_fasta_filename`](https://docs.ropensci.org/beautier/reference/get_fasta_filename.md)
  to obtain a testing FASTA filename.

- beauti_options:

  one BEAUti options object, as returned by
  [`create_beauti_options`](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)

## Value

lines of XML text

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

create_beast2_input_data(
  input_filename = get_fasta_filename(),
  beauti_options = create_beauti_options_v2_4()
)
#> [1] "    <data"                                                                                                 
#> [2] "id=\"test_output_0\""                                                                                      
#> [3] "name=\"alignment\">"                                                                                       
#> [4] "                    <sequence id=\"seq_t1\" taxon=\"t1\" totalcount=\"4\" value=\"acttgttgcgactgcgcctg\"/>"
#> [5] "                    <sequence id=\"seq_t2\" taxon=\"t2\" totalcount=\"4\" value=\"acttattgcgactgaggccg\"/>"
#> [6] "                    <sequence id=\"seq_t3\" taxon=\"t3\" totalcount=\"4\" value=\"acttaatgcgaatgagcccg\"/>"
#> [7] "                    <sequence id=\"seq_t4\" taxon=\"t4\" totalcount=\"4\" value=\"aacgacccgcgatcggggat\"/>"
#> [8] "                    <sequence id=\"seq_t5\" taxon=\"t5\" totalcount=\"4\" value=\"acttgttgcgactgagcctg\"/>"
#> [9] "                </data>"                                                                                   

check_empty_beautier_folder()
```
