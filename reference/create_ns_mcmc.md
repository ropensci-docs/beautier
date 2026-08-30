# Create an MCMC object to estimate the marginal likelihood using Nested Sampling.

This will result in a BEAST run that estimates the marginal likelihood
until convergence is achieved. In this context, `chain_length` is only
an upper bound to the length of that run.

## Usage

``` r
create_ns_mcmc(
  chain_length = 1e+07,
  store_every = -1,
  pre_burnin = 0,
  n_init_attempts = 3,
  particle_count = 1,
  sub_chain_length = 5000,
  epsilon = "1e-12",
  tracelog = create_tracelog(),
  screenlog = create_screenlog(),
  treelog = create_treelog()
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

## References

\* \[1\] Patricio Maturana Russel, Brendon J Brewer, Steffen Klaere,
Remco R Bouckaert; Model Selection and Parameter Inference in
Phylogenetics Using Nested Sampling, Systematic Biology, 2018, syy050,
https://doi.org/10.1093/sysbio/syy050

## See also

Use
[`create_mcmc`](https://docs.ropensci.org/beautier/reference/create_mcmc.md)
to create a regular MCMC. Use
[`create_test_ns_mcmc`](https://docs.ropensci.org/beautier/reference/create_test_ns_mcmc.md)
to create an NS MCMC for testing, with, among others, a short MCMC chain
length. Use
[`check_ns_mcmc`](https://docs.ropensci.org/beautier/reference/check_ns_mcmc.md)
to check that an NS MCMC object is valid.

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  mcmc <- create_ns_mcmc(
    chain_length = 1e7,
    store_every = 1000,
    particle_count = 1,
    sub_chain_length = 1000,
    epsilon = 1e-12
  )

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
