# Are the clock models Relaxed Log-Normal clock models?

Are the clock models Relaxed Log-Normal clock models?

## Usage

``` r
are_rln_clock_models(clock_models)
```

## Arguments

- clock_models:

  a list of one or more clock models, as returned by
  [`create_clock_model`](https://docs.ropensci.org/beautier/reference/create_clock_model.md)

## Value

vector of booleans with the same length as the number of clock models in
`clock_models`. Each nth element is TRUE if the nth element in
`clock_models` is a relaxed log-normal clock model, FALSE otherwise

## Author

Richèl J.C. Bilderbeek
