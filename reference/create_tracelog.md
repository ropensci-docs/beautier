# Create a `tracelog` object

Create a `tracelog` object

## Usage

``` r
create_tracelog(
  filename = NA,
  log_every = 1000,
  mode = "autodetect",
  sanitise_headers = TRUE,
  sort = "smart"
)
```

## Arguments

- filename:

  name of the file to store the posterior traces. Use
  [NA](https://rdrr.io/r/base/NA.html) to use the filename
  `[alignment_id].log`, where `alignment_id` is obtained using
  [get_alignment_id](https://docs.ropensci.org/beautier/reference/get_alignment_id.md)

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

a `tracelog` object

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
create_tracelog()
#> $filename
#> [1] NA
#> 
#> $log_every
#> [1] 1000
#> 
#> $mode
#> [1] "autodetect"
#> 
#> $sanitise_headers
#> [1] TRUE
#> 
#> $sort
#> [1] "smart"
#> 
```
