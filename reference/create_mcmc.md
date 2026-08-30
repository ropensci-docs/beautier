# Create an MCMC configuration.

Create an MCMC configuration, as in the BEAUti MCMC tab.

## Usage

``` r
create_mcmc(
  chain_length = 1e+07,
  store_every = -1,
  pre_burnin = 0,
  n_init_attempts = 10,
  sample_from_prior = FALSE,
  tracelog = beautier::create_tracelog(),
  screenlog = beautier::create_screenlog(),
  treelog = beautier::create_treelog()
)
```

## Arguments

- chain_length:

  length of the MCMC chain

- store_every:

  number of states the MCMC will process before the posterior's state
  will be saved to file. Use -1 or `NA` to use the default frequency.

- pre_burnin:

  number of burn in samples taken before entering the main loop

- n_init_attempts:

  number of initialization attempts before failing

- sample_from_prior:

  set to [TRUE](https://rdrr.io/r/base/logical.html) to sample from the
  prior

- tracelog:

  a `tracelog`, as created by
  [create_tracelog](https://docs.ropensci.org/beautier/reference/create_tracelog.md)

- screenlog:

  a `screenlog`, as created by
  [create_screenlog](https://docs.ropensci.org/beautier/reference/create_screenlog.md)

- treelog:

  a `treelog`, as created by
  [create_treelog](https://docs.ropensci.org/beautier/reference/create_treelog.md)

## Value

an MCMC configuration

## Details

There are four things that can be saved: \* `store_every`: saves the
state of the MCMC to file, as a `.state.xml` file \* `tracelog`: stores
the trace of the state of the MCMC to file. See `create_tracelog` how to
specify the filename \* `screenlog`: stores the screen output to file.
See `create_screenlog` how to specify the filename \* `treelog`: stores
the estimated phylogenies to file. See `create_treelog` how to specify
the filename

## See also

Use
[`create_test_mcmc`](https://docs.ropensci.org/beautier/reference/create_test_mcmc.md)
to create a short regular MCMC, that can be used for testing runs. Use
[`create_ns_mcmc`](https://docs.ropensci.org/beautier/reference/create_ns_mcmc.md)
to create an MCMC for a Nested Sampling run. Use
[`check_mcmc`](https://docs.ropensci.org/beautier/reference/check_mcmc.md)
to check if an MCMC is valid. Use
[`rename_mcmc_filenames`](https://docs.ropensci.org/beautier/reference/rename_mcmc_filenames.md)
to rename the filenames in an MCMC.

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  # Create an MCMC chain with 50 states
  mcmc <- create_mcmc(chain_length = 50000, store_every = 1000)

  beast2_input_file <- get_beautier_tempfilename()
  create_beast2_input_file(
    get_fasta_filename(),
    beast2_input_file,
    mcmc = mcmc
  )
  file.remove(beast2_input_file)

  remove_beautier_folder()
}
```
