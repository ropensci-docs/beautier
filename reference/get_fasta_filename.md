# Get the path of a FASTA file used in testing

Get the path of a FASTA file used in testing

## Usage

``` r
get_fasta_filename()
```

## Value

the path of a FASTA file used in testing

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  input_filename <- get_fasta_filename()
  output_filename <- get_beautier_tempfilename()

  create_beast2_input_file(
    input_filename = input_filename,
    output_filename = output_filename
  )
  file.remove(output_filename)

  remove_beautier_folder()
}
```
