# Get the full paths of files in the `inst/extdata` folder

Get the full paths of files in the `inst/extdata` folder

## Usage

``` r
get_beautier_paths(filenames)
```

## Arguments

- filenames:

  the files' names, without the path

## Value

the filenames' full paths

## See also

Use
[get_beautier_path](https://docs.ropensci.org/beautier/reference/get_beautier_path.md)
to get the path of one file

for one file, use
[`get_beautier_path`](https://docs.ropensci.org/beautier/reference/get_beautier_path.md)

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

 get_beautier_paths(
   c("test_output_0.fas", "anthus_aco.fas", "anthus_nd2.fas")
 )
#> [1] "/github/home/R/x86_64-pc-linux-gnu-library/4.6/beautier/extdata/test_output_0.fas"
#> [2] "/github/home/R/x86_64-pc-linux-gnu-library/4.6/beautier/extdata/anthus_aco.fas"   
#> [3] "/github/home/R/x86_64-pc-linux-gnu-library/4.6/beautier/extdata/anthus_nd2.fas"   

check_empty_beautier_folder()
```
