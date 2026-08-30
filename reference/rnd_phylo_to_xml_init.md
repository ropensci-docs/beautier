# Creates the XML of a random phylogeny, as used in the `init` section

Creates the XML text for the `beast` tag of a BEAST2 parameter file,
which is directly after the XML declaration (created by
[create_xml_declaration](https://docs.ropensci.org/beautier/reference/create_xml_declaration.md).

## Usage

``` r
rnd_phylo_to_xml_init(inference_model)
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

the phylogeny as XML text

## Details

The `init` tag has these elements:


      <init id=\"RandomTree.t:[...]>
          <populationModel[...]>
          [...]
          </populationModel>
      </init>

## Author

Richèl J.C. Bilderbeek
