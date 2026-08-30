# Get a function that removes the hex string from filenames.

The default filenames created by
[beautier](https://docs.ropensci.org/beautier/reference/beautier-package.md)
are temporary files, such as
`/home/john/.cache/tracelog_82c5888db98.log` (on Linux), where
`/home/john/.cache` is the location to a temporary folder (on Linux) and
`tracelog_82c5888db98.log` the filename. The filename ends with a hex
string (as is common for temporary files, as
[tempfile](https://rdrr.io/r/base/tempfile.html) does so). Because
[beautier](https://docs.ropensci.org/beautier/reference/beautier-package.md)
puts an underscore between the filename description (`tracelog`) and the
hex string, this function removes both.

## Usage

``` r
get_remove_hex_fun()
```

## Value

a function to remove the hex string from filenames

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

f <- get_remove_hex_fun()
# /home/john/beast2.xml.state
f("/home/john/beast2_186c7404208c.xml.state")
#> [1] "/home/john/beast2.xml.state"

# beast2.xml.state
f("beast2_186c7404208c.xml.state")
#> [1] "beast2.xml.state"

# NA
f(NA)
#> [1] NA

check_empty_beautier_folder()
```
