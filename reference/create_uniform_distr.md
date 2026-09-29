# Create a uniform distribution

Create a uniform distribution

## Usage

``` r
create_uniform_distr(id = NA, value = NA, lower = NA, upper = Inf)
```

## Arguments

- id:

  the distribution's ID

- value:

  the initial value for the MCMC

- lower:

  the lower bound, the lowest possible value

- upper:

  an upper limit of the uniform distribution. If the upper limits needs
  to be infinity, set `upper` to `Inf`.

## Value

a uniform distribution

## See also

the function
[`create_distr`](https://docs.ropensci.org/beautier/reference/create_distr.md)
shows an overview of all supported distributions

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_ci()) {

  uniform_distr <- create_uniform_distr()

  beast2_input_file <- get_beautier_tempfilename()
  create_beast2_input_file(
    input_filename = get_fasta_filename(),
    beast2_input_file,
    tree_prior = create_yule_tree_prior(
      birth_rate_distr = uniform_distr
    )
  )
  file.remove(beast2_input_file)

  remove_beautier_folder()
}
```
