# Create a BEAST2 input file from an inference model

Create a BEAST2 input file from an inference model

## Usage

``` r
create_beast2_input_file_from_model(
  input_filename,
  output_filename,
  inference_model = beautier::create_inference_model()
)
```

## Arguments

- input_filename:

  A FASTA filename. Use
  [`get_fasta_filename`](https://docs.ropensci.org/beautier/reference/get_fasta_filename.md)
  to obtain a testing FASTA filename.

- output_filename:

  Name of the XML parameter file created by this function. BEAST2 uses
  this file as input.

- inference_model:

  a Bayesian phylogenetic inference model. An inference model is the
  complete model setup in which a site model, clock model, tree prior
  and more are specified. Use
  [create_inference_model](https://docs.ropensci.org/beautier/reference/create_inference_model.md)
  to create an inference model. Use
  [check_inference_model](https://docs.ropensci.org/beautier/reference/check_inference_model.md)
  to check if an inference model is valid. Use
  [rename_inference_model_filenames](https://docs.ropensci.org/beautier/reference/rename_inference_model_filenames.md)
  to rename the files in an inference model.

## Value

nothing

## See also

use
[create_beast2_input_from_model](https://docs.ropensci.org/beautier/reference/create_beast2_input_from_model.md)
to get the BEAST2 input file as text

See
[`create_site_model`](https://docs.ropensci.org/beautier/reference/create_site_model.md)
for examples with different site models. See
[`create_clock_model`](https://docs.ropensci.org/beautier/reference/create_clock_model.md)
for examples with clock models. See
[`create_tree_prior`](https://docs.ropensci.org/beautier/reference/create_tree_prior.md)
for examples with different tree priors. See
[`create_mcmc`](https://docs.ropensci.org/beautier/reference/create_mcmc.md)
for examples with a different MCMC setup. Use
[create_beast2_input_file](https://docs.ropensci.org/beautier/reference/create_beast2_input_file.md)
to do the same with the elements of an inference model.

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {
  check_empty_beautier_folder()

  output_filename <- get_beautier_tempfilename()
  create_beast2_input_file_from_model(
    input_filename = get_fasta_filename(),
    output_filename = output_filename,
    inference_model = create_inference_model()
  )
  file.remove(output_filename)

  remove_beautier_folder()
  check_empty_beautier_folder()
}
```
