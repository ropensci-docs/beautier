# Get the filenames stored in an MCMC.

If a filename is set to an empty string, to indicate a certain log file
need not be created, this (non-)filename will not be returned.

## Usage

``` r
get_mcmc_filenames(mcmc)
```

## Arguments

- mcmc:

  one MCMC. Use
  [`create_mcmc`](https://docs.ropensci.org/beautier/reference/create_mcmc.md)
  to create an MCMC. Use
  [`create_ns_mcmc`](https://docs.ropensci.org/beautier/reference/create_ns_mcmc.md)
  to create an MCMC for a Nested Sampling run. Use
  [`check_mcmc`](https://docs.ropensci.org/beautier/reference/check_mcmc.md)
  to check if an MCMC is valid. Use
  [`rename_mcmc_filenames`](https://docs.ropensci.org/beautier/reference/rename_mcmc_filenames.md)
  to rename the filenames in an MCMC.

## Value

the filenames stored in an MCMC

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

mcmc <- create_mcmc()
mcmc$tracelog$filename <- "/home/john/trace.log"
mcmc$screenlog$filename <- "/home/john/screen.log"
mcmc$treelog$filename <- "/home/john/tree.log"

# 3 filenames
filenames <- get_mcmc_filenames(mcmc)

# If there is no need to write to the screenlog file ...
mcmc$screenlog$filename <- ""

# 2 filenames
# ... one file less will be created
filenames <- get_mcmc_filenames(mcmc)

check_empty_beautier_folder()
```
