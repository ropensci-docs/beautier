# Check if the tip dates file is valid

Check if the tip dates file is valid

## Usage

``` r
check_tipdates_file(tipdates_filename)
```

## Arguments

- tipdates_filename:

  name of the file containing the tip dates. This file is assumed to
  have two columns, separated by a tab. The first column contains the
  taxa names, the second column contains the date.

## Value

nothing

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

check_tipdates_file(
  get_beautier_path("babette_issue_109.tsv")
) # OK

try(
  check_tipdates_file(
    get_beautier_path("babette_issue_109_no_tabs.tsv")
  ) # ERROR
)
#> Error in check_tipdates_file(get_beautier_path("babette_issue_109_no_tabs.tsv")) : 
#>   Tipdating filename at path '/github/home/R/x86_64-pc-linux-gnu-library/4.6/beautier/extdata/babette_issue_109_no_tabs.tsv' is not a tab-separated file. 
#> Tip: edit the file to have tabs as a column separator and try again

try(
  check_tipdates_file(
    get_beautier_path("babette_issue_109_with_header.tsv")
  ) # ERROR
)
#> Error in check_tipdates_file(get_beautier_path("babette_issue_109_with_header.tsv")) : 
#>   Tipdating filename at path '/github/home/R/x86_64-pc-linux-gnu-library/4.6/beautier/extdata/babette_issue_109_with_header.tsv' has a header. 
#> Tip: remove the first line of this file and try again

check_empty_beautier_folder()
```
