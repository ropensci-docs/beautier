# Create an MCMC configuration for testing.

Create an MCMC configuration for testing.

## Usage

``` r
create_test_mcmc(
  chain_length = 3000,
  store_every = 1000,
  pre_burnin = 0,
  n_init_attempts = 10,
  sample_from_prior = FALSE,
  tracelog = beautier::create_test_tracelog(),
  screenlog = beautier::create_test_screenlog(),
  treelog = beautier::create_test_treelog()
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

## See also

Use
[`create_mcmc`](https://docs.ropensci.org/beautier/reference/create_mcmc.md)
to create a default BEAST2 MCMC

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  # Create an MCMC chain with 50 states
  mcmc <- create_test_mcmc()

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
