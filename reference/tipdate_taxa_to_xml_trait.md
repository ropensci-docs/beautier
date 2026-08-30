# Internal function

Internal function to creates the '`trait`' section of a BEAST2 XML
parameter file, which is part of a '`tree`' section, without being
indented.

## Usage

``` r
tipdate_taxa_to_xml_trait(inference_model)
```

## Arguments

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

The `tree` tag has these elements:


    <run[...]>
      <state[...]>
        <tree[...]>
          <trait[...]>
          This part
          </trait>
        </tree>
      </run>
    </state>

## Author

Richèl J.C. Bilderbeek
