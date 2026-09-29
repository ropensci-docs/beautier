# Get the base of the filename base without extension

The path need not to actually exist

## Usage

``` r
get_file_base_sans_ext(filename)
```

## Arguments

- filename:

  A filename

## Value

That filename without its full path and extension

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# Path need not exist, use UNIX path as example
# test
get_file_base_sans_ext("/home/homer/test.txt")
#> [1] "test"

check_empty_beautier_folder()
```
