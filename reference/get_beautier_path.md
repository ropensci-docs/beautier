# Get the full path of a file in the `inst/extdata` folder

Get the full path of a file in the `inst/extdata` folder

## Usage

``` r
get_beautier_path(filename)
```

## Arguments

- filename:

  the file's name, without the path

## Value

the full path of the filename

## See also

for more files, use
[`get_beautier_paths`](https://docs.ropensci.org/beautier/reference/get_beautier_paths.md)

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

get_beautier_path("test_output_0.fas")
#> [1] "/github/home/R/x86_64-pc-linux-gnu-library/4.6/beautier/extdata/test_output_0.fas"
get_beautier_path("anthus_aco.fas")
#> [1] "/github/home/R/x86_64-pc-linux-gnu-library/4.6/beautier/extdata/anthus_aco.fas"
get_beautier_path("anthus_nd2.fas")
#> [1] "/github/home/R/x86_64-pc-linux-gnu-library/4.6/beautier/extdata/anthus_nd2.fas"

check_empty_beautier_folder()
```
