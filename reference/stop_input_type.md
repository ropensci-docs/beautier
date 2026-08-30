# Stops on the input type.

Stops on the input type.

## Usage

``` r
stop_input_type(
  x,
  what,
  ...,
  allow_na = FALSE,
  allow_null = FALSE,
  show_value = TRUE,
  arg = rlang::caller_arg(x),
  call = rlang::caller_env()
)
```

## Arguments

- x:

  The object type which does not conform to \`what\`. Its
  \`obj_type_friendly()\` is taken and mentioned in the error message.

- what:

  The friendly expected type as a string. Can be a character vector of
  expected types, in which case the error message mentions all of them
  in an "or" enumeration.

- ...:

  Arguments passed to
  [abort](https://rlang.r-lib.org/reference/abort.html).

- allow_na:

  allow NA to be valid

- allow_null:

  allow NULL to be valid

- show_value:

  set to TRUE to show the value

- arg:

  No idea what this does

- call:

  No idea what this does

## Note

adapted from
\[\`r-lib\`\](https://github.com/r-lib/rlang/blob/main/R/standalone-obj-type.R)

## Author

\[\`olivroy\`\](https://github.com/olivroy)
