# Determine if \`x\` is one string

Determine if \`x\` is one string

## Usage

``` r
check_string(
  x,
  ...,
  allow_empty = TRUE,
  allow_na = FALSE,
  allow_null = FALSE,
  arg = rlang::caller_arg(x),
  call = rlang::caller_env()
)
```

## Arguments

- x:

  the object to be determined to be one string

- ...:

  other arguments, no idea why this is needed

- allow_empty:

  set to TRUE to allow an empty string to be valid

- allow_na:

  set to TRUE to allow NA to be valid

- allow_null:

  set to TRUE to allow NULL to be valid

- arg:

  no idea why this is needed

- call:

  no idea why this is needed

## Value

Nothing. Will raise an exception if the value is not one string

## Note

From
\[r-lib\](https://github.com/r-lib/rlang/blob/main/R/standalone-types-check.R)

## Author

\[\`olivroy\`\](https://github.com/olivroy) and Richèl J.C. Bilderbeek

## Examples

``` r
check_string("This is a string")
```
