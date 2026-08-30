# Determines if the environment is GitHub Actions

Determines if the environment is GitHub Actions

## Usage

``` r
is_on_github_actions()
```

## Value

[TRUE](https://rdrr.io/r/base/logical.html) if run on GitHub Actions,
[FALSE](https://rdrr.io/r/base/logical.html) otherwise

## Note

It is possible to fake being on GitHub Actions, using:

“\`r Sys.setenv(GITHUB_ACTIONS = "I fake being on GitHub Actions")
is_on_github_actions() \# Will be true “\`

To undo this, do

“\`r Sys.setenv(GITHUB_ACTIONS = "") is_on_github_actions() \# Will be
false “\`

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
if (is_on_github_actions()) {
  message("Running on GitHub Actions")
}
```
