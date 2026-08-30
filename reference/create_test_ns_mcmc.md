# Create an NS MCMC object for testing

Create an NS MCMC object for testing

## Usage

``` r
create_test_ns_mcmc(
  chain_length = 2000,
  store_every = 1000,
  pre_burnin = 0,
  n_init_attempts = 3,
  particle_count = 1,
  sub_chain_length = 500,
  epsilon = 1e-12,
  tracelog = beautier::create_test_tracelog(),
  screenlog = beautier::create_test_screenlog(),
  treelog = beautier::create_test_treelog()
)
```

## Arguments

- chain_length:

  upper bound to the length of the MCMC chain

- store_every:

  number of states the MCMC will process before the posterior's state
  will be saved to file. Use -1 or `NA` to use the default frequency.

- pre_burnin:

  number of burn in samples taken before entering the main loop

- n_init_attempts:

  number of initialization attempts before failing

- particle_count:

  number of particles

- sub_chain_length:

  sub-chain length

- epsilon:

  epsilon

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

an MCMC object

## See also

Use
[`create_ns_mcmc`](https://docs.ropensci.org/beautier/reference/create_ns_mcmc.md)
to create a default nested sampling MCMC

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  mcmc <- create_test_ns_mcmc()
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
