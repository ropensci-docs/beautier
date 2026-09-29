# Internal function to create the `branchRateModel` section of the XML as text.

Creates the `branchRateModel` section of the XML as text.

## Usage

``` r
create_branch_rate_model_xml(inference_model)
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

a character vector of XML strings

## Details

The `distribution` tag (with ID equals `treeLikelihood`) has these
elements:


      <branchRateModel[...]>
        [...]
      </branchRateModel>

When there is a strict clock,
[create_strict_clock_branch_rate_model_xml](https://docs.ropensci.org/beautier/reference/create_strict_clock_branch_rate_model_xml.md)
is called. When there is an RLN clock,
[create_rln_clock_branch_rate_model_xml](https://docs.ropensci.org/beautier/reference/create_rln_clock_branch_rate_model_xml.md)
is called.

Zooming out:


      <beast[...]>
        <run[...]>
          <distribution id="posterior"[...]>
            <distribution id="likelihood"[...]>
              <distribution id="treeLikelihood"[...]>
                 [...]

                 [this section]
              </distribution>
            </distribution>
          </distribution>
        </run>
      </beast>

## Author

Richèl J.C. Bilderbeek
