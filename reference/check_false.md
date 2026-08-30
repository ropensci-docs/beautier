# Determine if \`x\` is one FALSE

Determine if \`x\` is one FALSE

## Usage

``` r
check_false(
  x,
  ...,
  allow_na = FALSE,
  allow_null = FALSE,
  arg = rlang::caller_arg(x),
  call = rlang::caller_env()
)
```

## Arguments

- x:

  the object to be determined to be one FALSE

- ...:

  other arguments, no idea why this is needed

- allow_na:

  set to TRUE to allow NA to be valid

- allow_null:

  set to TRUE to allow NULL to be valid

- arg:

  no idea why this is needed

- call:

  no idea why this is needed

## Value

Nothing. Will raise an exception if the value is not one FALSE

## Note

From
\[\`https://github.com/r-lib/rlang\`\](https://github.com/r-lib/rlang),
file \`R/import-standalone-type-check.R\`

## Author

\[\`olivroy\`\](https://github.com/olivroy) and Richèl J.C. Bilderbeek

## Examples

``` r
check_false(FALSE)
```
