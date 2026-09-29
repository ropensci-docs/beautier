# Create a JC69 site model

Create a JC69 site model

## Usage

``` r
create_jc69_site_model(
  id = NA,
  gamma_site_model = beautier::create_gamma_site_model()
)
```

## Arguments

- id:

  the IDs of the alignment (can be extracted from the FASTA filename
  using
  [`get_alignment_id`](https://docs.ropensci.org/beautier/reference/get_alignment_id.md))

- gamma_site_model:

  a gamma site model, as created by
  [create_gamma_site_model](https://docs.ropensci.org/beautier/reference/create_gamma_site_model.md)

## Value

a JC69 site_model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  jc69_site_model <- create_jc69_site_model()

  output_filename <- get_beautier_tempfilename()
  create_beast2_input_file(
    input_filename = get_fasta_filename(),
    output_filename = output_filename,
    site_model = jc69_site_model
  )
  file.remove(output_filename)

  remove_beautier_folder()
}
```
