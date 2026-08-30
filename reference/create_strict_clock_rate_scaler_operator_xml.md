# Internal function

Creates the `StrictClockRateScaler` operator such as: ` ... `

## Usage

``` r
create_strict_clock_rate_scaler_operator_xml(inference_model)
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

the following XML: ` ... `

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

create_strict_clock_rate_scaler_operator_xml(
  create_inference_model(
    clock_model = create_strict_clock_model(id = 314)
  )
)
#> [1] "<operator id=\"StrictClockRateScaler.c:314\" spec=\"ScaleOperator\" parameter=\"@clockRate.c:314\" scaleFactor=\"0.75\" weight=\"3.0\"/>"

check_empty_beautier_folder()
```
