# General function to create a site model.

General function to create a site model.

## Usage

``` r
create_site_model(
  name,
  id,
  gamma_site_model = beautier::create_gamma_site_model(),
  ...
)
```

## Arguments

- name:

  the site model name. Valid names can be found in
  `get_site_model_names`

- id:

  the IDs of the alignment (can be extracted from the FASTA filename
  using
  [`get_alignment_id`](https://docs.ropensci.org/beautier/reference/get_alignment_id.md))

- gamma_site_model:

  a gamma site model, as created by
  [create_gamma_site_model](https://docs.ropensci.org/beautier/reference/create_gamma_site_model.md)

- ...:

  specific site model parameters

## Value

a site_model

## Note

Prefer using the named functions
[`create_gtr_site_model`](https://docs.ropensci.org/beautier/reference/create_gtr_site_model.md),
[`create_hky_site_model`](https://docs.ropensci.org/beautier/reference/create_hky_site_model.md),,
[`create_jc69_site_model`](https://docs.ropensci.org/beautier/reference/create_jc69_site_model.md),
and
[`create_tn93_site_model`](https://docs.ropensci.org/beautier/reference/create_tn93_site_model.md)

## See also

See
[`create_gtr_site_model`](https://docs.ropensci.org/beautier/reference/create_gtr_site_model.md)
for more examples with a GTR site model. See
[`create_hky_site_model`](https://docs.ropensci.org/beautier/reference/create_hky_site_model.md)
for more examples with an HKY site model. See
[`create_jc69_site_model`](https://docs.ropensci.org/beautier/reference/create_jc69_site_model.md)
for more examples with a JC69 site model. See
[`create_tn93_site_model`](https://docs.ropensci.org/beautier/reference/create_tn93_site_model.md)
for more examples with a TN93 site model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  check_empty_beautier_folder()

  input_filename <- get_fasta_filename()
  gtr_site_model <- create_gtr_site_model()
  hk_site_model <- create_hky_site_model()
  jc69_site_model <- create_jc69_site_model()
  tn93_site_model <- create_tn93_site_model()

  # Can use any site model
  output_filename <- get_beautier_tempfilename()
  create_beast2_input_file(
    input_filename = input_filename,
    output_filename = output_filename,
    site_model = jc69_site_model
  )
  file.remove(output_filename)

  remove_beautier_folder()
  check_empty_beautier_folder()
}
```
