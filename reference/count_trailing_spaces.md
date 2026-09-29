# Count the number of spaces before the first character

Count the number of spaces before the first character

## Usage

``` r
count_trailing_spaces(line)
```

## Arguments

- line:

  line of text

## Value

the number of spaces before the first character

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# 0
count_trailing_spaces("x")
#> [1] 0
# 1
count_trailing_spaces(" y")
#> [1] 1
# 2
count_trailing_spaces("  <")
#> [1] 2
# 0
count_trailing_spaces("")
#> [1] 0
# 1
count_trailing_spaces(" ")
#> [1] 1
# 2
count_trailing_spaces("  ")
#> [1] 2

check_empty_beautier_folder()
```
