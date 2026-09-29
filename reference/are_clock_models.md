# Determine if x consists out of clock_models objects

Determine if x consists out of clock_models objects

## Usage

``` r
are_clock_models(x)
```

## Arguments

- x:

  the object to check if it consists out of clock_models objects

## Value

TRUE if x, or all elements of x, are clock_model objects

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

rln_clock_model <- create_rln_clock_model()
strict_clock_model <- create_strict_clock_model()
both_clock_models <- list(rln_clock_model, strict_clock_model)
# TRUE
are_clock_models(rln_clock_model)
#> [1] TRUE
are_clock_models(strict_clock_model)
#> [1] TRUE
are_clock_models(both_clock_models)
#> [1] TRUE

# FALSE
are_clock_models(NA)
#> [1] FALSE
are_clock_models(NULL)
#> [1] FALSE
are_clock_models("nonsense")
#> [1] FALSE
are_clock_models(create_jc69_site_model())
#> [1] FALSE

check_empty_beautier_folder()
```
