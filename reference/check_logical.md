# Determine if \`x\` is one logical value

Determine if \`x\` is one logical value

## Usage

``` r
check_logical(
  x,
  ...,
  allow_null = FALSE,
  arg = rlang::caller_arg(x),
  call = rlang::caller_env()
)
```

## Arguments

- x:

  the object to be determined to be one logical value

- ...:

  other arguments, no idea why this is needed

- allow_null:

  set to TRUE to allow NULL to be valid

- arg:

  no idea why this is needed

- call:

  no idea why this is needed

## Value

Nothing. Will raise an exception if the value is not one logical value

## Note

From
\[r-lib\](https://github.com/r-lib/rlang/blob/main/R/standalone-types-check.R)

## Author

\[\`olivroy\`\](https://github.com/olivroy) and Richèl J.C. Bilderbeek

## Examples

``` r
check_logical(TRUE)
check_logical(FALSE)
check_logical(NA)
```
