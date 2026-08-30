# Is object x a gamma site model?

Is object x a gamma site model?

## Usage

``` r
is_gamma_site_model(x)
```

## Arguments

- x:

  the object to be determined if it is a valid gamma site object

## Value

TRUE if x is a valid gamma site object, FALSE otherwise

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# TRUE
is_gamma_site_model(create_gamma_site_model())
#> [1] TRUE

# FALSE
is_gamma_site_model("nonsense")
#> [1] FALSE
is_gamma_site_model(NA)
#> [1] FALSE
is_gamma_site_model(NULL)
#> [1] FALSE
is_gamma_site_model("")
#> [1] FALSE
is_gamma_site_model(c())
#> [1] FALSE

check_empty_beautier_folder()
```
