# Determines if the environment is AppVeyor

Determines if the environment is AppVeyor

## Usage

``` r
is_on_appveyor()
```

## Value

[TRUE](https://rdrr.io/r/base/logical.html) if run on AppVeyor,
[FALSE](https://rdrr.io/r/base/logical.html) otherwise

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
  if (is_on_appveyor()) {
    message("Running on AppVeyor")
  }
```
