# Check if the rename function is a valid filename rename function

Will [stop](https://rdrr.io/r/base/stop.html) if not

## Usage

``` r
check_rename_fun(rename_fun)
```

## Arguments

- rename_fun:

  a function to rename a filename, as can be checked by
  check_rename_fun. This function should have one argument, which will
  be a filename or [NA](https://rdrr.io/r/base/NA.html). The function
  should [return](https://rdrr.io/r/base/function.html) one filename
  (when passed one filename) or one [NA](https://rdrr.io/r/base/NA.html)
  (when passed one [NA](https://rdrr.io/r/base/NA.html)). Example rename
  functions are:

  - [get_remove_dir_fun](https://docs.ropensci.org/beautier/reference/get_remove_dir_fun.md)
    get a function that removes the directory paths from the filenames,
    in effect turning these into local files

  - [get_replace_dir_fun](https://docs.ropensci.org/beautier/reference/get_replace_dir_fun.md)
    get a function that replaces the directory paths from the filenames

  - [get_remove_hex_fun](https://docs.ropensci.org/beautier/reference/get_remove_hex_fun.md)
    get a function that removes the hex string from filenames. For
    example, `tracelog_82c1a522040.log` becomes `tracelog.log`

## Value

No return value, called for side effects

## Author

Richèl J.C. Bilderbeek
