# Check if the `beauti_options` is a valid `beauti_options` object.

Calls `stop` if the `beauti_options` object is invalid

## Usage

``` r
check_beauti_options(beauti_options)
```

## Arguments

- beauti_options:

  one BEAUti options object, as returned by
  [`create_beauti_options`](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)

## Value

nothing

## See also

Use
[create_beauti_options](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)
to create a valid BEAUti options setup

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

check_beauti_options(create_beauti_options())

check_empty_beautier_folder()
```
