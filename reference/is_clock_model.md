# Determine if the object is a valid clock_model

Determine if the object is a valid clock_model

## Usage

``` r
is_clock_model(x)
```

## Arguments

- x:

  an object, to be determined if it is a clock_model

## Value

TRUE if the clock_model is a valid clock_model, FALSE otherwise

## See also

see
[`create_clock_model`](https://docs.ropensci.org/beautier/reference/create_clock_model.md)
for an overview of functions to create valid clock model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# TRUE
is_clock_model(create_strict_clock_model())
#> [1] TRUE
is_clock_model(create_rln_clock_model())
#> [1] TRUE

# FALSE
is_clock_model(NA)
#> [1] FALSE
is_clock_model(NULL)
#> [1] FALSE
is_clock_model("nonsense")
#> [1] FALSE
is_clock_model(create_jc69_site_model())
#> [1] FALSE
is_clock_model(create_mcmc())
#> [1] FALSE

check_empty_beautier_folder()
```
