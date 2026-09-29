# Create clock models from their names

Create clock models from their names

## Usage

``` r
create_clock_models_from_names(clock_model_names)
```

## Arguments

- clock_model_names:

  one or more names of a clock model, must be name among those returned
  by
  [`get_clock_model_names`](https://docs.ropensci.org/beautier/reference/get_clock_model_names.md)

## Value

a list of one or more clock models

## See also

Use
[create_clock_models](https://docs.ropensci.org/beautier/reference/create_clock_models.md)
to get all clock models

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

create_clock_models_from_names(get_clock_model_names())
#> [[1]]
#> [[1]]$name
#> [1] "relaxed_log_normal"
#> 
#> [[1]]$id
#> [1] NA
#> 
#> [[1]]$ucldstdev_distr
#> [[1]]$ucldstdev_distr$name
#> [1] "gamma"
#> 
#> [[1]]$ucldstdev_distr$id
#> [1] NA
#> 
#> [[1]]$ucldstdev_distr$value
#> [1] NA
#> 
#> [[1]]$ucldstdev_distr$lower
#> [1] NA
#> 
#> [[1]]$ucldstdev_distr$upper
#> [1] NA
#> 
#> [[1]]$ucldstdev_distr$alpha
#> [[1]]$ucldstdev_distr$alpha$name
#> [1] "alpha"
#> 
#> [[1]]$ucldstdev_distr$alpha$id
#> [1] NA
#> 
#> [[1]]$ucldstdev_distr$alpha$value
#> [1] 0.5396
#> 
#> [[1]]$ucldstdev_distr$alpha$estimate
#> [1] FALSE
#> 
#> 
#> [[1]]$ucldstdev_distr$beta
#> [[1]]$ucldstdev_distr$beta$name
#> [1] "beta"
#> 
#> [[1]]$ucldstdev_distr$beta$id
#> [1] NA
#> 
#> [[1]]$ucldstdev_distr$beta$value
#> [1] 0.3819
#> 
#> [[1]]$ucldstdev_distr$beta$estimate
#> [1] FALSE
#> 
#> 
#> 
#> [[1]]$mean_rate_prior_distr
#> [[1]]$mean_rate_prior_distr$name
#> [1] "uniform"
#> 
#> [[1]]$mean_rate_prior_distr$id
#> [1] NA
#> 
#> [[1]]$mean_rate_prior_distr$value
#> [1] NA
#> 
#> [[1]]$mean_rate_prior_distr$lower
#> [1] NA
#> 
#> [[1]]$mean_rate_prior_distr$upper
#> [1] Inf
#> 
#> 
#> [[1]]$mparam_id
#> [1] NA
#> 
#> [[1]]$mean_clock_rate
#> [1] "1.0"
#> 
#> [[1]]$n_rate_categories
#> [1] -1
#> 
#> [[1]]$normalize_mean_clock_rate
#> [1] FALSE
#> 
#> [[1]]$dimension
#> [1] NA
#> 
#> [[1]]$rate_scaler_factor
#> [1] 0.75
#> 
#> 
#> [[2]]
#> [[2]]$name
#> [1] "strict"
#> 
#> [[2]]$id
#> [1] NA
#> 
#> [[2]]$clock_rate_param
#> [[2]]$clock_rate_param$name
#> [1] "clock_rate"
#> 
#> [[2]]$clock_rate_param$id
#> [1] NA
#> 
#> [[2]]$clock_rate_param$value
#> [1] "1.0"
#> 
#> [[2]]$clock_rate_param$estimate
#> [1] FALSE
#> 
#> 
#> [[2]]$clock_rate_distr
#> [[2]]$clock_rate_distr$name
#> [1] "uniform"
#> 
#> [[2]]$clock_rate_distr$id
#> [1] NA
#> 
#> [[2]]$clock_rate_distr$value
#> [1] NA
#> 
#> [[2]]$clock_rate_distr$lower
#> [1] NA
#> 
#> [[2]]$clock_rate_distr$upper
#> [1] Inf
#> 
#> 
#> [[2]]$rate_scaler_factor
#> [1] 0.75
#> 
#> 

check_empty_beautier_folder()
```
