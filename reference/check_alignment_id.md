# Check if the `alignment_id` is valid.

Will [stop](https://rdrr.io/r/base/stop.html) if not.

## Usage

``` r
check_alignment_id(alignment_id)
```

## Arguments

- alignment_id:

  ID of the alignment, as returned by
  [get_alignment_id](https://docs.ropensci.org/beautier/reference/get_alignment_id.md).
  Keep at `NA` to have it initialized automatically

## Value

nothing, will [stop](https://rdrr.io/r/base/stop.html) if needed

## Examples

``` r
check_empty_beautier_folder()

# anthus_aco_sub
alignment_id <- get_alignment_id("/home/homer/anthus_aco_sub.fas")
check_alignment_id(alignment_id)

check_empty_beautier_folder()
```
