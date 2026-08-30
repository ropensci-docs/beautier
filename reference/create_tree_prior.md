# Internal function to create a tree prior

Internal function to create a tree prior

## Usage

``` r
create_tree_prior(name, id, ...)
```

## Arguments

- name:

  the tree prior name. Can be any name in `get_tree_prior_names`

- id:

  the ID of the alignment

- ...:

  specific tree prior parameters

## Value

a tree_prior

## Note

Prefer the use the named functions
[`create_bd_tree_prior`](https://docs.ropensci.org/beautier/reference/create_bd_tree_prior.md),
[`create_cbs_tree_prior`](https://docs.ropensci.org/beautier/reference/create_cbs_tree_prior.md),
[`create_ccp_tree_prior`](https://docs.ropensci.org/beautier/reference/create_ccp_tree_prior.md)
[`create_cep_tree_prior`](https://docs.ropensci.org/beautier/reference/create_cep_tree_prior.md)
and
[`create_yule_tree_prior`](https://docs.ropensci.org/beautier/reference/create_yule_tree_prior.md)
instead

## See also

See
[`create_bd_tree_prior`](https://docs.ropensci.org/beautier/reference/create_bd_tree_prior.md),
[`create_cbs_tree_prior`](https://docs.ropensci.org/beautier/reference/create_cbs_tree_prior.md),
[`create_ccp_tree_prior`](https://docs.ropensci.org/beautier/reference/create_ccp_tree_prior.md)
[`create_cep_tree_prior`](https://docs.ropensci.org/beautier/reference/create_cep_tree_prior.md)
and
[`create_yule_tree_prior`](https://docs.ropensci.org/beautier/reference/create_yule_tree_prior.md)
for more examples using those functions

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  check_empty_beautier_folder()

  beast2_input_file <- get_beautier_tempfilename()

  bd_tree_prior <- create_bd_tree_prior()
  cbs_tree_prior <- create_cbs_tree_prior()
  ccp_tree_prior <- create_ccp_tree_prior()
  cep_tree_prior <- create_cep_tree_prior()
  yule_tree_prior <- create_yule_tree_prior()

  # Use any of the above tree priors
  create_beast2_input_file(
    input_filename = get_fasta_filename(),
    beast2_input_file,
    tree_prior = bd_tree_prior
  )
  file.remove(beast2_input_file)

  remove_beautier_folder()
  check_empty_beautier_folder()
}
```
