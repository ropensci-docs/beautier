# Check there are no files in the default [beautier](https://docs.ropensci.org/beautier/reference/beautier-package.md) folder

Check there are no files in the default
[beautier](https://docs.ropensci.org/beautier/reference/beautier-package.md)
folder. The goal is to make sure no temporary files are left undeleted.
Will [stop](https://rdrr.io/r/base/stop.html) if there are files in the
[beautier](https://docs.ropensci.org/beautier/reference/beautier-package.md)
folder.

## Usage

``` r
remove_beautier_folder()
```

## Value

No return value, called for side effects.

## See also

use remove_beautier_folder to remove the default \`beautier\` folder

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

remove_beautier_folder()

check_empty_beautier_folder()
```
