# Creates the XML text for the \`logger\` tag with ID \`treelog\`. This section has these elements: “\` \<logger id="treelog.t:test_output_0" spec="Logger" fileName="my_treelog.trees" logEvery="345000" mode="tree" sanitiseHeaders="true" sort="smart"\> \# nolint indeed long \<log id="TreeWithMetaDataLogger.t:test_output_0" spec="beast.evolution.tree.TreeWithMetaDataLogger" tree="@Tree.t:test_output_0"/\> \# nolint indeed long \</logger\> “\`

Creates the XML text for the \`logger\` tag with ID \`treelog\`. This
section has these elements: “\` \<logger id="treelog.t:test_output_0"
spec="Logger" fileName="my_treelog.trees" logEvery="345000" mode="tree"
sanitiseHeaders="true" sort="smart"\> \# nolint indeed long \<log
id="TreeWithMetaDataLogger.t:test_output_0"
spec="beast.evolution.tree.TreeWithMetaDataLogger"
tree="@Tree.t:test_output_0"/\> \# nolint indeed long \</logger\> “\`

## Usage

``` r
create_treelog_xml(inference_model)
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

## Author

Richèl J.C. Bilderbeek
