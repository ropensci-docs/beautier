# Create a Birth-Death tree prior

Create a Birth-Death tree prior

## Usage

``` r
create_bd_tree_prior(
  id = NA,
  birth_rate_distr = create_uniform_distr(),
  death_rate_distr = create_uniform_distr()
)
```

## Arguments

- id:

  the ID of the alignment

- birth_rate_distr:

  the birth rate distribution, as created by a
  [`create_distr`](https://docs.ropensci.org/beautier/reference/create_distr.md)
  function

- death_rate_distr:

  the death rate distribution, as created by a
  [`create_distr`](https://docs.ropensci.org/beautier/reference/create_distr.md)
  function

## Value

a Birth-Death tree_prior

## See also

An alignment ID can be extracted from its FASTA filename using
[`get_alignment_id`](https://docs.ropensci.org/beautier/reference/get_alignment_id.md)

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  bd_tree_prior <- create_bd_tree_prior()

  beast2_input_file <- get_beautier_tempfilename()
  create_beast2_input_file(
    input_filename = get_fasta_filename(),
    beast2_input_file,
    tree_prior = bd_tree_prior
  )
  file.remove(beast2_input_file)

  remove_beautier_folder()
}
```
