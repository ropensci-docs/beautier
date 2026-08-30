# Create a parameter called \`b_pop_sizes\`.

Create a parameter called \`b_pop_sizes\`.

## Usage

``` r
create_b_pop_sizes_param(id = NA, value = 1, upper = "380000.0")
```

## Arguments

- id:

  the parameter's ID

- value:

  value of the parameter

- upper:

  upper value of the parameter

## Value

a parameter called b_pop_sizes

## Note

this parameter is used in a CBS model, as created by
[create_cbs_tree_prior](https://docs.ropensci.org/beautier/reference/create_cbs_tree_prior.md)

## See also

the function
[`create_param`](https://docs.ropensci.org/beautier/reference/create_param.md)
contains a list of all parameters that can be created

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
# Create the parameter
b_pop_sizes_param <- create_b_pop_sizes_param()
```
