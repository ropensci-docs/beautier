# Determines if the environment is a continuous integration service

Determines if the environment is a continuous integration service

## Usage

``` r
is_on_ci()
```

## Value

[TRUE](https://rdrr.io/r/base/logical.html) if run on AppVeyor or Travis
CI, [FALSE](https://rdrr.io/r/base/logical.html) otherwise

## Note

It is possible to fake being on continuous integration service, in this
case GitHub Actions, using:

“\`r Sys.setenv(GITHUB_ACTIONS = "I fake being on GitHub Actions")
is_on_ci() \# Will be true “\`

To undo this, do

“\`r Sys.setenv(GITHUB_ACTIONS = "") is_on_ci() \# Will be false “\`

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
is_on_ci()
#> [1] FALSE
```
