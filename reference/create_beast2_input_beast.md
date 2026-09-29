# Creates the XML text for the `beast` tag of a BEAST2 parameter file.

Creates the XML text for the `beast` tag of a BEAST2 parameter file,
which is directly after the XML declaration (created by
[create_xml_declaration](https://docs.ropensci.org/beautier/reference/create_xml_declaration.md).

## Usage

``` r
create_beast2_input_beast(
  input_filename,
  inference_model = beautier::create_inference_model()
)
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

lines of XML text

## Details

The `beast` tag has these elements:


      <beast[...]>
          <data
          [...]
          </data>
          [map names]
          <run[...]>
          [...]
          </run>
      </beast>

## See also

Use
[create_beast2_input_from_model](https://docs.ropensci.org/beautier/reference/create_beast2_input_from_model.md)
to create the complete XML text. Use
[create_beast2_input_data](https://docs.ropensci.org/beautier/reference/create_beast2_input_data.md)
to create the XML text for the `data` tag only. Use
[create_beast2_input_map](https://docs.ropensci.org/beautier/reference/create_beast2_input_map.md)
to create the XML text for the `[map names]` part. Use
[create_beast2_input_run](https://docs.ropensci.org/beautier/reference/create_beast2_input_run.md)
to create the XML text for the `run` tag only.

## Author

Richèl J.C. Bilderbeek
