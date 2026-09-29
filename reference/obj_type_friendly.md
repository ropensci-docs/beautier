# Return English-friendly type

Return English-friendly type

## Usage

``` r
obj_type_friendly(x, value = TRUE)
```

## Arguments

- x:

  Any R object.

- value:

  Whether to describe the value of \`x\`. Special values like \`NA\` or
  \`""\` are always described.

## Value

A string describing the type. Starts with an indefinite article, e.g.
"an integer vector".

## Note

adapted from
\[https://github.com/r-lib/rlang\](https://github.com/r-lib/rlang) file
\`R/standalone-obj-type.R\`

## Author

\[\`olivroy\`\](https://github.com/olivroy)
