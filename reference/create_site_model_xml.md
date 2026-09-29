# Internal function to creates the XML text for the `siteModel` tag of a BEAST2 parameter file.

Creates the XML text for the `siteModel` tag of a BEAST2 parameter file,
which is part of the `distribution` node for the `treeLikelihood` ID.

## Usage

``` r
create_site_model_xml(inference_model)
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

the site model as XML text

## Details

The `siteModel` tag has these elements:


      <siteModel[...]>

          [parameters]

          <substModel[...]>
            [...]
          </substModel>
      </siteModel>

The `parameter` section is created by
[create_site_model_parameters_xml](https://docs.ropensci.org/beautier/reference/create_site_model_parameters_xml.md)
The `substModel` section is created by
[create_subst_model_xml](https://docs.ropensci.org/beautier/reference/create_subst_model_xml.md)

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()
 # <distribution id="posterior"[...]">
 #     <distribution id="likelihood" [...]>
 #       <siteModel...>
 #         [parameters]
 #       </siteModel>
 #     </distribution>
 # </distribution>

check_empty_beautier_folder()
```
