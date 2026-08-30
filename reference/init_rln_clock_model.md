# Initializes a Relaxed Log-Normal clock model

Initializes a Relaxed Log-Normal clock model

## Usage

``` r
init_rln_clock_model(rln_clock_model, distr_id = 0, param_id = 0)
```

## Arguments

- rln_clock_model:

  a Relaxed Log-Normal clock model, as returned by
  [`create_rln_clock_model`](https://docs.ropensci.org/beautier/reference/create_rln_clock_model.md)

- distr_id:

  a distributions' ID

- param_id:

  a parameter's ID

## Value

an initialized Relaxed Log-Normal clock model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

rln_clock_model <- create_rln_clock_model()
# FALSE: not yet initialized
is_init_rln_clock_model(rln_clock_model)
#> [1] FALSE
rln_clock_model <- init_rln_clock_model(rln_clock_model)
# Dimension is set to NA by default, for unknown reasons.
# Because 'init_rln_clock_model' does not initialize it (for
# unknown reasons), set it manually
rln_clock_model$dimension <- 42
# TRUE: now it is initialized
is_init_rln_clock_model(rln_clock_model)
#> [1] TRUE

check_empty_beautier_folder()
```
