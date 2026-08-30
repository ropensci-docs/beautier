# Determines if the environment is Travis CI

Determines if the environment is Travis CI

## Usage

``` r
is_on_travis()
```

## Value

[TRUE](https://rdrr.io/r/base/logical.html) if run on Travis CI,
[FALSE](https://rdrr.io/r/base/logical.html) otherwise

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
  if (is_on_ci()) {
    message("Running on Travis CI")
  }
```
