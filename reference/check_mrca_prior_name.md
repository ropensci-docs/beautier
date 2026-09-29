# Check if `mrca_prior_name` is a valid MRCA prior name.

A valid MRCA prior name is either [NA](https://rdrr.io/r/base/NA.html)
or one character string. Will [stop](https://rdrr.io/r/base/stop.html)
if not.

## Usage

``` r
check_mrca_prior_name(mrca_prior_name)
```

## Arguments

- mrca_prior_name:

  the unique name of the MRCA prior, for example a genus, family, order
  or even class name. Leave at [NA](https://rdrr.io/r/base/NA.html) to
  have it named automatically.

## Value

No return value, called for side effects
