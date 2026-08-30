# Create a `treelog` object to be used in testing

Create a `treelog` object to be used in testing

## Usage

``` r
create_test_treelog(
  filename = beautier::create_temp_treelog_filename(),
  log_every = 1000,
  mode = "tree",
  sanitise_headers = FALSE,
  sort = "none"
)
```

## Arguments

- filename:

  name of the file to store the posterior trees

- log_every:

  number of MCMC states between writing to file

- mode:

  mode how to log. Valid values are the ones returned by
  [get_log_modes](https://docs.ropensci.org/beautier/reference/get_log_modes.md)

- sanitise_headers:

  set to [TRUE](https://rdrr.io/r/base/logical.html) to sanitise the
  headers of the log file

- sort:

  how to sort the log. Valid values are the ones returned by
  [get_log_sorts](https://docs.ropensci.org/beautier/reference/get_log_sorts.md)

## Value

a `treelog` object

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
create_test_treelog()
#> $filename
#> [1] "/github/home/.cache/beautier/treelog_5a544837c34.trees"
#> 
#> $log_every
#> [1] 1000
#> 
#> $mode
#> [1] "tree"
#> 
#> $sanitise_headers
#> [1] FALSE
#> 
#> $sort
#> [1] "none"
#> 
```
