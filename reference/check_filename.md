# Check if the \`filename\` is valid

Calls `stop` if the filename is invalid

## Usage

``` r
check_filename(filename, allow_empty_str = FALSE, allow_na = FALSE)
```

## Arguments

- filename:

  a filename, as can be checked by check_filename

- allow_empty_str:

  allow a string to be empty

- allow_na:

  allow [NA](https://rdrr.io/r/base/NA.html)

## Value

The filename (invisibly)

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

check_filename("trace.log")
check_filename("my.trees")

check_empty_beautier_folder()
```
