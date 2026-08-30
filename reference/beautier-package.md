# `beautier`: A package to create a `BEAST2` input file.

`beautier` allows to create a `BEAST2` input file, using an R interface.
`beautier` closely follows the interface of `BEAUti 2`, a GUI tool
bundled with `BEAST2`, including its default settings.

## Details

See the documentation of `create_inference_model` to see the features of
BEAST2 that `beautier` supports.

## See also

These are packages associated with `beautier`:

- The package `beastier` can run BEAST2 from R

- The package `tracerer` can parse BEAST2 output files from R

- The package `mauricer` manages BEAST2 packages from R

- The package `babette` combines the functionality of `beautier`,
  `beastier`, `mauricer` and `tracerer` into a single workflow

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  check_empty_beautier_folder()

  # Get an example FASTA file
  input_filename <- get_fasta_filename()

  # The file created by beautier, a BEAST2 input file
  output_filename <- get_beautier_tempfilename()

  # Use the default BEAUti settings to create a BEAST2 input file
  create_beast2_input_file_from_model(
    input_filename,
    output_filename,
    inference_model = create_inference_model()
  )

  # Remove the folder that contains the beautier temporary files
  remove_beautier_folder()
  check_empty_beautier_folder()
}
```
