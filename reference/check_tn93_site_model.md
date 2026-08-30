# Check if the `tn93_site_model` is a valid TN93 nucleotide substitution model.

Use
[create_tn93_site_model](https://docs.ropensci.org/beautier/reference/create_tn93_site_model.md)
to create a valid TN93 nucleotide substitution model.

## Usage

``` r
check_tn93_site_model(tn93_site_model)
```

## Arguments

- tn93_site_model:

  a TN93 site model, as returned by
  [`create_tn93_site_model`](https://docs.ropensci.org/beautier/reference/create_tn93_site_model.md)

## Value

No return value, called for side effects

## Examples

``` r
check_empty_beautier_folder()

check_tn93_site_model(create_tn93_site_model())

check_empty_beautier_folder()
```
