# Create a strict clock model

Create a strict clock model

## Usage

``` r
create_strict_clock_model(
  id = NA,
  clock_rate_param = create_clock_rate_param(),
  clock_rate_distr = create_uniform_distr(),
  rate_scaler_factor = 0.75
)
```

## Arguments

- id:

  an alignment's IDs. An ID can be extracted from its FASTA filename
  with
  [`get_alignment_ids_from_fasta_filenames`](https://docs.ropensci.org/beautier/reference/get_alignment_ids_from_fasta_filenames.md))

- clock_rate_param:

  the clock rate's parameter, a numeric value. For advanced usage, use
  the structure as created by the
  [`create_clock_rate_param`](https://docs.ropensci.org/beautier/reference/create_clock_rate_param.md)
  function

- clock_rate_distr:

  the clock rate's distribution, as created by a
  [`create_distr`](https://docs.ropensci.org/beautier/reference/create_distr.md)
  function

- rate_scaler_factor:

  the strict clock model's operator scaler for the rate. Use an empty
  string to indicate the default.

## Value

a strict clock_model

## Note

I am unsure about the relationship between \`clock_rate_param\` and
\`clock_rate_distr\`. Please contact me if you know the most natural
architecture

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {
  strict_clock_model <- create_strict_clock_model(
    clock_rate_param = 1.0,
    clock_rate_distr = create_uniform_distr()
  )

  beast2_input_file <- get_beautier_tempfilename()
  create_beast2_input_file(
    get_fasta_filename(),
    beast2_input_file,
    clock_model = strict_clock_model
  )
  file.remove(beast2_input_file)

  remove_beautier_folder()
}
```
