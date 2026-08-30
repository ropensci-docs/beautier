# Check if the `gtr_site_model` is a valid GTR nucleotide substitution model.

Use
[create_gtr_site_model](https://docs.ropensci.org/beautier/reference/create_gtr_site_model.md)
to create a valid GTR nucleotide substitution model.

## Usage

``` r
check_gtr_site_model(gtr_site_model)
```

## Arguments

- gtr_site_model:

  a GTR site model, as returned by
  [`create_gtr_site_model`](https://docs.ropensci.org/beautier/reference/create_gtr_site_model.md)

## Value

TRUE is the `gtr_site_model` is a valid GTR nucleotide substitution
model, FALSE otherwise

## Examples

``` r
check_empty_beautier_folder()

check_gtr_site_model(create_gtr_site_model())
#> [1] TRUE

check_empty_beautier_folder()
```
