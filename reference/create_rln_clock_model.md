# Create a relaxed log-normal clock model

Create a relaxed log-normal clock model

## Usage

``` r
create_rln_clock_model(
  id = NA,
  mean_rate_prior_distr = create_uniform_distr(),
  ucldstdev_distr = create_gamma_distr(),
  mparam_id = NA,
  mean_clock_rate = "1.0",
  n_rate_categories = -1,
  normalize_mean_clock_rate = FALSE,
  dimension = NA,
  rate_scaler_factor = 0.75
)
```

## Arguments

- id:

  an alignment's IDs. An ID can be extracted from its FASTA filename
  with
  [`get_alignment_ids_from_fasta_filenames`](https://docs.ropensci.org/beautier/reference/get_alignment_ids_from_fasta_filenames.md))

- mean_rate_prior_distr:

  the mean clock rate prior distribution, as created by a
  [`create_distr`](https://docs.ropensci.org/beautier/reference/create_distr.md)
  function

- ucldstdev_distr:

  the standard deviation of the uncorrelated log-normal distribution, as
  created by a
  [`create_distr`](https://docs.ropensci.org/beautier/reference/create_distr.md)
  function

- mparam_id:

  the ID of the M parameter in the `branchRateModel`, set to NA to have
  it initialized

- mean_clock_rate:

  the mean clock rate, 1.0 by default (is called `ucld_stdev` in XML,
  where `ucld_stdev` is always 0.1)

- n_rate_categories:

  the number of rate categories. -1 is default, 0 denotes as much rates
  as branches

- normalize_mean_clock_rate:

  normalize the mean clock rate

- dimension:

  the dimensionality of the relaxed clock model. Leave NA to let
  beautier calculate it. Else, the dimensionality of the clock equals
  twice the number of taxa minus two.

- rate_scaler_factor:

  the strict clock model's operator scaler for the rate. Use an empty
  string to indicate the default.

## Value

a relaxed log-normal clock_model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  rln_clock_model <- create_rln_clock_model()

  beast2_input_file <- get_beautier_tempfilename()

  create_beast2_input_file(
    get_fasta_filename(),
    beast2_input_file,
    clock_model = rln_clock_model
  )
  file.remove(beast2_input_file)

  remove_beautier_folder()
}
```
