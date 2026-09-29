# Rename the filenames within an MCMC

Rename the filenames within an MCMC

## Usage

``` r
rename_mcmc_filenames(mcmc, rename_fun)
```

## Arguments

- mcmc:

  one MCMC. Use
  [`create_mcmc`](https://docs.ropensci.org/beautier/reference/create_mcmc.md)
  to create an MCMC. Use
  [`create_ns_mcmc`](https://docs.ropensci.org/beautier/reference/create_ns_mcmc.md)
  to create an MCMC for a Nested Sampling run. Use
  [`check_mcmc`](https://docs.ropensci.org/beautier/reference/check_mcmc.md)
  to check if an MCMC is valid. Use `rename_mcmc_filenames` to rename
  the filenames in an MCMC.

- rename_fun:

  a function to rename a filename, as can be checked by
  [check_rename_fun](https://docs.ropensci.org/beautier/reference/check_rename_fun.md).
  This function should have one argument, which will be a filename or
  [NA](https://rdrr.io/r/base/NA.html). The function should
  [return](https://rdrr.io/r/base/function.html) one filename (when
  passed one filename) or one [NA](https://rdrr.io/r/base/NA.html) (when
  passed one [NA](https://rdrr.io/r/base/NA.html)). Example rename
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

an \`mcmc\` (see
[create_mcmc](https://docs.ropensci.org/beautier/reference/create_mcmc.md))
with renamed filenames

## Examples

``` r
check_empty_beautier_folder()

# Create an MCMC with local filenames
mcmc <- create_mcmc()
mcmc$tracelog$filename <- "trace.log"
mcmc$screenlog$filename <- "screen.log"
mcmc$treelog$filename <- "tree.log"

# Nah, files should be put in '/home/john' folder
mcmc <- rename_mcmc_filenames(
  mcmc = mcmc,
  rename_fun = get_replace_dir_fun("/home/john")
)

# Nah, files should be put in '/home/doe' folder instead
mcmc <- rename_mcmc_filenames(
  mcmc = mcmc,
  rename_fun = get_replace_dir_fun("/home/doe")
)

# Nah, files should be put in local folder instead
mcmc <- rename_mcmc_filenames(
  mcmc = mcmc,
  rename_fun = get_remove_dir_fun()
)

check_empty_beautier_folder()
```
