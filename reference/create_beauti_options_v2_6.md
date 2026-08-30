# Function to create the BEAUti options for version 2.6.

Function to create the BEAUti options for version 2.6, by calling
[create_beauti_options](https://docs.ropensci.org/beautier/reference/create_beauti_options.md).

## Usage

``` r
create_beauti_options_v2_6(
  beast2_version = "2.6",
  sequence_indent = 8,
  nucleotides_uppercase = FALSE,
  status = "",
  namespace = beautier::get_default_beast_namespace_v2_6(),
  required = "",
  add_operator_schedule = TRUE
)
```

## Arguments

- beast2_version:

  the BEAST2 version

- sequence_indent:

  the number of spaces the XML `sequence` lines are indented

- nucleotides_uppercase:

  must the nucleotides of the DNA sequence be in uppercase?

- status:

  the BEAUti status

- namespace:

  the \`namespace\` XML element in the \`beast\` XML tag.

- required:

  things that may be required, for example `BEAST v2.5.0`

- add_operator_schedule:

  set to TRUE to add the Operator Schedule to the BEAST2 XML input file

## Value

a BEAUti options structure

## See also

see
[create_beauti_options_v2_4](https://docs.ropensci.org/beautier/reference/create_beauti_options_v2_4.md)
for using the older v2.4

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  check_empty_beautier_folder()

  beauti_options <- create_beauti_options_v2_6()
  xml <- create_beast2_input(
    get_fasta_filename(),
    beauti_options = beauti_options
  )

  check_empty_beautier_folder()
}
```
