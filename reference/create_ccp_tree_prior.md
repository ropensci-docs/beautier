# Create a Coalescent Constant Population tree prior

Create a Coalescent Constant Population tree prior

## Usage

``` r
create_ccp_tree_prior(
  id = NA,
  pop_size_distr = beautier::create_one_div_x_distr(value = 0.3)
)
```

## Arguments

- id:

  the ID of the alignment

- pop_size_distr:

  the population distribution, as created by a
  [`create_distr`](https://docs.ropensci.org/beautier/reference/create_distr.md)
  function

## Value

a Coalescent Constant Population tree_prior

## See also

An alignment ID can be extracted from its FASTA filename using
[`get_alignment_id`](https://docs.ropensci.org/beautier/reference/get_alignment_id.md)

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  ccp_tree_prior <- create_ccp_tree_prior()

  beast2_input_file <- get_beautier_tempfilename()
  create_beast2_input_file(
    input_filename = get_fasta_filename(),
    beast2_input_file,
    tree_prior = ccp_tree_prior
  )
  file.remove(beast2_input_file)

  remove_beautier_folder()
}
```
