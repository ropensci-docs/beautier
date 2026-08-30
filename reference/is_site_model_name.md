# Determines if the name is a valid site_model name

Determines if the name is a valid site_model name

## Usage

``` r
is_site_model_name(name)
```

## Arguments

- name:

  the name to be tested

## Value

TRUE if the name is a valid site_model name, FALSE otherwise

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# TRUE
is_site_model_name("JC69")
#> [1] TRUE
is_site_model_name("HKY")
#> [1] TRUE
is_site_model_name("TN93")
#> [1] TRUE
is_site_model_name("GTR")
#> [1] TRUE
# FALSE
is_site_model_name("nonsense")
#> [1] FALSE

check_empty_beautier_folder()
```
