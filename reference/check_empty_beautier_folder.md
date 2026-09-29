# Internal function

Internal function to verify that, if there are \`beautier\` temporary
files created, these are also cleaned up, as by CRAN policy.

## Usage

``` r
check_empty_beautier_folder(beautier_folder = beautier::get_beautier_folder())
```

## Arguments

- beautier_folder:

  the path to the
  [beautier](https://docs.ropensci.org/beautier/reference/beautier-package.md)
  temporary files folder

## Value

No return value, called for side effects.

## Details

If the \`beautier\` folder does not exist, this function does nothing.
If there are folder and/or files in the \`beautier\` folder, an error is
given.

## See also

use
[remove_beautier_folder](https://docs.ropensci.org/beautier/reference/remove_beautier_folder.md)
to remove the default \`beautier\` folder

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
remove_beautier_folder()

check_empty_beautier_folder()

remove_beautier_folder()
```
