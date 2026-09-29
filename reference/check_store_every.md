# Check if `store_every` holds a valid value

Will [stop](https://rdrr.io/r/base/stop.html) if not

## Usage

``` r
check_store_every(store_every)
```

## Arguments

- store_every:

  number of states the MCMC will process before the posterior's state
  will be saved to file. Use -1 or `NA` to use the default frequency.

## Value

No return value, called for side effects
