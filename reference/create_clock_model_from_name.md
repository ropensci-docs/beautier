# Create a clock model from name

Create a clock model from name

## Usage

``` r
create_clock_model_from_name(clock_model_name)
```

## Arguments

- clock_model_name:

  name of a clock model, must be a name as returned by
  [`get_clock_model_names`](https://docs.ropensci.org/beautier/reference/get_clock_model_names.md)

## Value

a clock model, as can be created by
[create_clock_model](https://docs.ropensci.org/beautier/reference/create_clock_model.md)

## See also

Use
[`create_clock_model`](https://docs.ropensci.org/beautier/reference/create_clock_model.md)
to create a clock model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

create_clock_model_from_name(get_clock_model_names()[1])
#> $name
#> [1] "relaxed_log_normal"
#> 
#> $id
#> [1] NA
#> 
#> $ucldstdev_distr
#> $ucldstdev_distr$name
#> [1] "gamma"
#> 
#> $ucldstdev_distr$id
#> [1] NA
#> 
#> $ucldstdev_distr$value
#> [1] NA
#> 
#> $ucldstdev_distr$lower
#> [1] NA
#> 
#> $ucldstdev_distr$upper
#> [1] NA
#> 
#> $ucldstdev_distr$alpha
#> $ucldstdev_distr$alpha$name
#> [1] "alpha"
#> 
#> $ucldstdev_distr$alpha$id
#> [1] NA
#> 
#> $ucldstdev_distr$alpha$value
#> [1] 0.5396
#> 
#> $ucldstdev_distr$alpha$estimate
#> [1] FALSE
#> 
#> 
#> $ucldstdev_distr$beta
#> $ucldstdev_distr$beta$name
#> [1] "beta"
#> 
#> $ucldstdev_distr$beta$id
#> [1] NA
#> 
#> $ucldstdev_distr$beta$value
#> [1] 0.3819
#> 
#> $ucldstdev_distr$beta$estimate
#> [1] FALSE
#> 
#> 
#> 
#> $mean_rate_prior_distr
#> $mean_rate_prior_distr$name
#> [1] "uniform"
#> 
#> $mean_rate_prior_distr$id
#> [1] NA
#> 
#> $mean_rate_prior_distr$value
#> [1] NA
#> 
#> $mean_rate_prior_distr$lower
#> [1] NA
#> 
#> $mean_rate_prior_distr$upper
#> [1] Inf
#> 
#> 
#> $mparam_id
#> [1] NA
#> 
#> $mean_clock_rate
#> [1] "1.0"
#> 
#> $n_rate_categories
#> [1] -1
#> 
#> $normalize_mean_clock_rate
#> [1] FALSE
#> 
#> $dimension
#> [1] NA
#> 
#> $rate_scaler_factor
#> [1] 0.75
#> 

check_empty_beautier_folder()
```
