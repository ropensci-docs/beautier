# Creates the '`run`' section of a BEAST2 XML parameter file

Creates the '`run`' section of a BEAST2 XML parameter file, without
being indented.

## Usage

``` r
create_beast2_input_run(
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

The `run` tag has these elements:


       <run[...]>
           <state[...]>
           [...]
           </state>
           <init[...]>
           [...]
           </init>
           <distribution[...]>
           [...]
           </distribution>
           [operator ids]
           [loggers]
        </run>

## See also

Use
[create_beast2_input_state](https://docs.ropensci.org/beautier/reference/create_beast2_input_state.md)
to create the XML text of the `state` tag. Use
[create_beast2_input_init](https://docs.ropensci.org/beautier/reference/create_beast2_input_init.md)
to create the XML text of the `init` tag. Use
[create_beast2_input_distr](https://docs.ropensci.org/beautier/reference/create_beast2_input_distr.md)
to create the XML text of the `distribution` tag. Use
[create_beast2_input_operators](https://docs.ropensci.org/beautier/reference/create_beast2_input_operators.md)
to create the XML text of the `[operator ids]` section. Use
[create_loggers_xml](https://docs.ropensci.org/beautier/reference/create_loggers_xml.md)
to create the XML text of the `[loggers]` part.

## Author

Richèl J.C. Bilderbeek
