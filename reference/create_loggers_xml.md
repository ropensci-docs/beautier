# Creates the three logger sections of a BEAST2 XML parameter file

The logger section has these elements:


     <logger id="tracelog" [...]>
         [...]
     </logger>
     <logger id="screenlog" [...]>
         [...]
     </logger>
     <logger id="treelog.t:[alignment ID]"  [...]>
         [...]
     </logger>

## Usage

``` r
create_loggers_xml(input_filename, inference_model)
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

## See also

Use
[create_tracelog_xml](https://docs.ropensci.org/beautier/reference/create_tracelog_xml.md)
to create the XML text of the logger with the `tracelog` ID. Use
[create_screenlog_xml](https://docs.ropensci.org/beautier/reference/create_screenlog_xml.md)
to create the XML text of the logger with the `screenlog` ID. Use
[create_treelog_xml](https://docs.ropensci.org/beautier/reference/create_treelog_xml.md)
to create the XML text of the loggers with the `treelog` ID.

## Author

Richèl J.C. Bilderbeek
