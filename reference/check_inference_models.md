# Check if the `inference_model` is a valid BEAUti inference model.

Calls `stop` if not.

## Usage

``` r
check_inference_models(inference_models)
```

## Arguments

- inference_models:

  a list of one or more inference models, as can be created by
  [create_inference_model](https://docs.ropensci.org/beautier/reference/create_inference_model.md)

## Value

nothing

## See also

Use
[create_inference_model](https://docs.ropensci.org/beautier/reference/create_inference_model.md)
to create a valid BEAST2 options object

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

check_inference_models(list(create_inference_model()))

check_empty_beautier_folder()
```
