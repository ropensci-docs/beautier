# Checks if all filenames have a FASTA filename extension

Checks if all filenames have a FASTA filename extension

## Usage

``` r
are_fasta_filenames(filenames)
```

## Arguments

- filenames:

  filenames

## Value

TRUE if all filenames have a FASTA filename extension

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

# TRUE
are_fasta_filenames("1.fas")
#> [1] TRUE
are_fasta_filenames("1.fasta")
#> [1] TRUE
are_fasta_filenames("1.FAS")
#> [1] TRUE
are_fasta_filenames("1.FASTA")
#> [1] TRUE
are_fasta_filenames(c("1.fas", "2.fas"))
#> [1] TRUE

# FALSE
are_fasta_filenames("")
#> [1] FALSE
are_fasta_filenames(NA)
#> [1] FALSE
are_fasta_filenames(NULL)
#> [1] FALSE
are_fasta_filenames(Inf)
#> [1] FALSE
are_fasta_filenames("1.fasX")
#> [1] FALSE
are_fasta_filenames(c("1.fas", "2.exe"))
#> [1] FALSE
are_fasta_filenames(c("1.bat", "2.exe"))
#> [1] FALSE

check_empty_beautier_folder()
```
