# Create a Coalescent Exponential Population tree prior

Create a Coalescent Exponential Population tree prior

## Usage

``` r
create_cep_tree_prior(
  id = NA,
  pop_size_distr = beautier::create_one_div_x_distr(),
  growth_rate_distr = beautier::create_laplace_distr()
)
```

## Arguments

- id:

  the ID of the alignment

- pop_size_distr:

  the population distribution, as created by a
  [`create_distr`](https://docs.ropensci.org/beautier/reference/create_distr.md)
  function

- growth_rate_distr:

  the growth rate distribution, as created by a
  [`create_distr`](https://docs.ropensci.org/beautier/reference/create_distr.md)
  function

## Value

a Coalescent Exponential Population tree_prior

## See also

An alignment ID can be extracted from its FASTA filename using
[`get_alignment_id`](https://docs.ropensci.org/beautier/reference/get_alignment_id.md)

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  cep_tree_prior <- create_cep_tree_prior()

  beast2_input_file <- get_beautier_tempfilename()
  create_beast2_input_file(
    input_filename = get_fasta_filename(),
    beast2_input_file,
    tree_prior = cep_tree_prior
  )
  file.remove(beast2_input_file)

  remove_beautier_folder()
}
```
