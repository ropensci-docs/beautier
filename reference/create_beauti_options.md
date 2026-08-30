# Function to create a set of \`BEAUti\` options.

\`BEAUti\` options are settings that differ between \`BEAUti\` version.
The use of these options is mostly for testing older versions Whatever
option chosen here, the created XML file will be valid.

## Usage

``` r
create_beauti_options(
  capitalize_first_char_id = FALSE,
  nucleotides_uppercase = FALSE,
  beast2_version = "2.4",
  required = "",
  sequence_indent = 20,
  status = "",
  namespace = beautier::get_default_beast_namespace_v2_4(),
  add_operator_schedule = FALSE
)
```

## Arguments

- capitalize_first_char_id:

  must the ID of alignment start with a capital? TRUE if yes, FALSE if
  it can be left lower case (if it is lowercase)

- nucleotides_uppercase:

  must the nucleotides of the DNA sequence be in uppercase?

- beast2_version:

  the BEAST2 version

- required:

  things that may be required, for example `BEAST v2.5.0`

- sequence_indent:

  the number of spaces the XML `sequence` lines are indented

- status:

  the BEAUti status

- namespace:

  the \`namespace\` XML element in the \`beast\` XML tag.

- add_operator_schedule:

  set to TRUE to add the Operator Schedule to the BEAST2 XML input file

## Value

a BEAUti options structure

## Details

Available BEAUti options are:  
\*
[create_beauti_options_v2_4](https://docs.ropensci.org/beautier/reference/create_beauti_options_v2_4.md)
\*
[create_beauti_options_v2_6](https://docs.ropensci.org/beautier/reference/create_beauti_options_v2_6.md)

\`beautier\` uses v2.4 by default, as this is when the first tests were
written.

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  check_empty_beautier_folder()

  beauti_options <- beautier::create_beauti_options_v2_4()
  xml <- create_beast2_input(
    get_fasta_filename(),
    beauti_options = beauti_options
  )

  check_empty_beautier_folder()
}
```
