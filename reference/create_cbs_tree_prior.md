# Create a Coalescent Bayesian Skyline tree prior

Create a Coalescent Bayesian Skyline tree prior

## Usage

``` r
create_cbs_tree_prior(
  id = NA,
  group_sizes_dimension = 5,
  b_pop_sizes_param = beautier::create_b_pop_sizes_param(),
  pop_sizes_scaler_scale_factor = ""
)
```

## Arguments

- id:

  an alignment's IDs. An ID can be extracted from its FASTA filename
  with
  [`get_alignment_ids_from_fasta_filenames`](https://docs.ropensci.org/beautier/reference/get_alignment_ids_from_fasta_filenames.md))

- group_sizes_dimension:

  the group sizes' dimension, as used by the CBS tree prior (see
  `create_cbs_tree_prior`)

- b_pop_sizes_param:

  a Bayesian population size parameter, as created by
  [create_b_pop_sizes_param](https://docs.ropensci.org/beautier/reference/create_b_pop_sizes_param.md)

- pop_sizes_scaler_scale_factor:

  the scale factor used by the population sizes scaler operator

## Value

a Coalescent Bayesian Skyline tree_prior

## See also

An alignment ID can be extracted from its FASTA filename using
[`get_alignment_id`](https://docs.ropensci.org/beautier/reference/get_alignment_id.md)

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  cbs_tree_prior <- create_cbs_tree_prior()

  beast2_input_file <- get_beautier_tempfilename()
  create_beast2_input_file(
    input_filename = get_beautier_path("test_output_6.fas"),
    beast2_input_file,
    tree_prior = cbs_tree_prior
  )
  file.remove(beast2_input_file)

  remove_beautier_folder()
}
```
