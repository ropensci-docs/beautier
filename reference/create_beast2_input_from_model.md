# Create a BEAST2 XML input text from an inference model

The main two XML tags are these:


      <?xml[...]?><beast[...]>
      [...]
      </beast>

## Usage

``` r
create_beast2_input_from_model(input_filename, inference_model)
```

## Arguments

- input_filename:

  A FASTA filename. Use
  [`get_fasta_filename`](https://docs.ropensci.org/beautier/reference/get_fasta_filename.md)
  to obtain a testing FASTA filename.

- inference_model:

  a Bayesian phylogenetic inference model. An inference model is the
  complete model setup in which a site model, clock model, tree prior
  and more are specified. Use
  [create_inference_model](https://docs.ropensci.org/beautier/reference/create_inference_model.md)
  to create an inference model. Use
  [check_inference_model](https://docs.ropensci.org/beautier/reference/check_inference_model.md)
  to check if an inference model is valid. Use
  [rename_inference_model_filenames](https://docs.ropensci.org/beautier/reference/rename_inference_model_filenames.md)
  to rename the files in an inference model.

## Value

a character vector of XML strings

## See also

Use
[create_beast2_input_file_from_model](https://docs.ropensci.org/beautier/reference/create_beast2_input_file_from_model.md)
to also save it to file. Use
[create_xml_declaration](https://docs.ropensci.org/beautier/reference/create_xml_declaration.md)
to create the XML text of the XML declaration. Use
[create_beast2_input_beast](https://docs.ropensci.org/beautier/reference/create_beast2_input_beast.md)
to create to create the XML text of the `beast` tag.

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  check_empty_beautier_folder()

  text <- create_beast2_input_from_model(
    input_filename = get_fasta_filename(),
    inference_model = create_inference_model()
  )

  check_empty_beautier_folder()
}
```
