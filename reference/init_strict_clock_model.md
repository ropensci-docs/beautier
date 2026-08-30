# Initializes a strict clock model

Initializes a strict clock model

## Usage

``` r
init_strict_clock_model(strict_clock_model, distr_id = 0, param_id = 0)
```

## Arguments

- strict_clock_model:

  a strict clock model, as returned by
  [`create_strict_clock_model`](https://docs.ropensci.org/beautier/reference/create_strict_clock_model.md)

- distr_id:

  a distributions' ID

- param_id:

  a parameter's ID

## Value

an initialized strict clock model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

strict_clock_model <- create_strict_clock_model()
# FALSE: not yet initialized
is_init_strict_clock_model(strict_clock_model)
#> [1] FALSE
strict_clock_model <- init_strict_clock_model(strict_clock_model)
# TRUE: initialized
is_init_strict_clock_model(strict_clock_model)
#> [1] TRUE

check_empty_beautier_folder()
```
