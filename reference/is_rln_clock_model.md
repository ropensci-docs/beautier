# Determine if the object is a valid relaxed log normal clock model

Determine if the object is a valid relaxed log normal clock model

## Usage

``` r
is_rln_clock_model(x)
```

## Arguments

- x:

  an object, to be determined if it is a valid relaxed log normal clock
  model, as created by
  [`create_rln_clock_model`](https://docs.ropensci.org/beautier/reference/create_rln_clock_model.md))

## Value

TRUE if x is a valid relaxed log normal clock model, FALSE otherwise

## See also

[`create_clock_model`](https://docs.ropensci.org/beautier/reference/create_clock_model.md)
shows an overview of functions to create a clock model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# TRUE
is_rln_clock_model(create_strict_clock_model())
#> [1] FALSE
is_rln_clock_model(create_rln_clock_model())
#> [1] TRUE

# FALSE
is_rln_clock_model(NA)
#> [1] FALSE
is_rln_clock_model(NULL)
#> [1] FALSE
is_rln_clock_model("nonsense")
#> [1] FALSE
is_rln_clock_model(create_jc69_site_model())
#> [1] FALSE
is_rln_clock_model(create_mcmc())
#> [1] FALSE

check_empty_beautier_folder()
```
