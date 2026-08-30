# Creates the XML text for the `distribution` tag with the `treeLikelihood` ID, of a BEAST2 parameter file.

Creates the XML text for the `distribution` tag with the
`treeLikelihood` ID, of a BEAST2 parameter file, in an unindented form

## Usage

``` r
create_tree_likelihood_distr_xml(inference_model)
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

The `distribution` tag (with ID equals `treeLikelihood`) has these
elements:


       <distribution id="treeLikelihood"[...]>
          <siteModel[...]>
            [...]
          </siteModel>
          <branchRateModel[...]>
            [...]
          </branchRateModel>
       </distribution>

The `siteModel` section is created by
[create_site_model_xml](https://docs.ropensci.org/beautier/reference/create_site_model_xml.md).
The `branchRateModel` section is created by
[create_branch_rate_model_xml](https://docs.ropensci.org/beautier/reference/create_branch_rate_model_xml.md).

Zooming out:


      <beast[...]>
        <run[...]>
          <distribution id="posterior"[...]>
            <distribution id="likelihood"[...]>
              [this section]
            </distribution>
          </distribution>
        </run>
      </beast>

## Note

this function is not intended for regular use, thus its long name length
is accepted

## See also

this function is called by `create_beast2_input_distr`, together with
`create_beast2_input_distr_prior`

## Author

Richèl J.C. Bilderbeek
