# General function to create a clock model

General function to create a clock model

## Usage

``` r
create_clock_model(name, id, ...)
```

## Arguments

- name:

  the clock model name. Valid names can be found in
  `get_clock_model_names`

- id:

  a clock model's ID

- ...:

  specific clock model parameters

## Value

a valid clock model

## Note

Prefer using the named function
[`create_rln_clock_model`](https://docs.ropensci.org/beautier/reference/create_rln_clock_model.md)
and
[`create_strict_clock_model`](https://docs.ropensci.org/beautier/reference/create_strict_clock_model.md)

## See also

An alignment ID can be extracted from its FASTA filename using
[`get_alignment_id`](https://docs.ropensci.org/beautier/reference/get_alignment_id.md).
For more examples about creating a relaxed log-normal clock model, see
[`create_rln_clock_model`](https://docs.ropensci.org/beautier/reference/create_rln_clock_model.md).
For more examples about creating a strict clock model, see
[`create_strict_clock_model`](https://docs.ropensci.org/beautier/reference/create_strict_clock_model.md).

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {
  # Can use any of these models
  strict_clock_model <- create_strict_clock_model()
  rln_clock_model <- create_rln_clock_model()

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
