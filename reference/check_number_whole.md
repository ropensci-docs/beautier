# Determine if \`x\` is one whole number

Determine if \`x\` is one whole number

## Usage

``` r
check_number_whole(
  x,
  ...,
  min = NULL,
  max = NULL,
  allow_infinite = FALSE,
  allow_na = FALSE,
  allow_null = FALSE,
  arg = rlang::caller_arg(x),
  call = rlang::caller_env()
)
```

## Arguments

- x:

  the object to be determined to be one whole number

- ...:

  other arguments, no idea why this is needed

- min:

  lowest number allowed

- max:

  lowest number allowed

- allow_infinite:

  set to TRUE to allow \`Inf\` to be valid

- allow_na:

  set to TRUE to allow NA to be valid

- allow_null:

  set to TRUE to allow NULL to be valid

- arg:

  no idea why this is needed

- call:

  no idea why this is needed

## Value

Nothing. Will raise an exception if the value is not one whole number

## Note

From
\[r-lib\](https://github.com/r-lib/rlang/blob/main/R/standalone-types-check.R)

## Author

\[\`olivroy\`\](https://github.com/olivroy) and Richèl J.C. Bilderbeek

## Examples

``` r
check_number_whole(1)
check_number_whole(1.0)
```
