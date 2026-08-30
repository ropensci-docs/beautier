# Determines if the name is a valid clock model name

Determines if the name is a valid clock model name

## Usage

``` r
is_clock_model_name(name)
```

## Arguments

- name:

  the name to be tested

## Value

TRUE if the name is a valid clock_model name, FALSE otherwise

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# TRUE
is_clock_model_name("relaxed_log_normal")
#> [1] TRUE
is_clock_model_name("strict")
#> [1] TRUE

check_empty_beautier_folder()
```
