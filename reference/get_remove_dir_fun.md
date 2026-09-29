# Get a function that, from a filename, returns the part without the directory.

Or: get a function that returns the local version of a filename. Also,
the function will return [NA](https://rdrr.io/r/base/NA.html) if the
filename is [NA](https://rdrr.io/r/base/NA.html)

## Usage

``` r
get_remove_dir_fun()
```

## Value

a function to remove the folder name from a path

## See also

see
[check_rename_fun](https://docs.ropensci.org/beautier/reference/check_rename_fun.md)
for an overview of file renaming functions

## Author

Richèl J.C. Bilderbeek
