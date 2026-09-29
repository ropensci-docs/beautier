# Create a `screenlog` object

Create a `screenlog` object

## Usage

``` r
create_screenlog(
  filename = "",
  log_every = 1000,
  mode = "autodetect",
  sanitise_headers = FALSE,
  sort = "none"
)
```

## Arguments

- filename:

  name of the file to store the posterior screens phylogenies to. By
  default, this is `$(screen).screens`

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

a `screenlog` object

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

create_screenlog()
#> $filename
#> [1] ""
#> 
#> $log_every
#> [1] 1000
#> 
#> $mode
#> [1] "autodetect"
#> 
#> $sanitise_headers
#> [1] FALSE
#> 
#> $sort
#> [1] "none"
#> 

check_empty_beautier_folder()
```
