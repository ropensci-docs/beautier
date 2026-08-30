# Create site models from their names

Create site models from their names

## Usage

``` r
create_site_models_from_names(site_model_names)
```

## Arguments

- site_model_names:

  one or more names of a site model, must be name among those returned
  by
  [`get_site_model_names`](https://docs.ropensci.org/beautier/reference/get_site_model_names.md)

## Value

one or more site models

## See also

Use
[create_site_model](https://docs.ropensci.org/beautier/reference/create_site_model.md)
to create a site model

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

create_site_models_from_names(get_site_model_names())
#> [[1]]
#> [[1]]$name
#> [1] "JC69"
#> 
#> [[1]]$id
#> [1] NA
#> 
#> [[1]]$gamma_site_model
#> [[1]]$gamma_site_model$gamma_cat_count
#> [1] "0"
#> 
#> [[1]]$gamma_site_model$gamma_shape
#> [1] "1.0"
#> 
#> [[1]]$gamma_site_model$prop_invariant
#> [1] "0.0"
#> 
#> [[1]]$gamma_site_model$gamma_shape_prior_distr
#> [1] NA
#> 
#> [[1]]$gamma_site_model$freq_equilibrium
#> [1] "estimated"
#> 
#> [[1]]$gamma_site_model$freq_prior_uniform_distr_id
#> [1] 1000
#> 
#> 
#> 
#> [[2]]
#> [[2]]$name
#> [1] "HKY"
#> 
#> [[2]]$id
#> [1] NA
#> 
#> [[2]]$gamma_site_model
#> [[2]]$gamma_site_model$gamma_cat_count
#> [1] "0"
#> 
#> [[2]]$gamma_site_model$gamma_shape
#> [1] "1.0"
#> 
#> [[2]]$gamma_site_model$prop_invariant
#> [1] "0.0"
#> 
#> [[2]]$gamma_site_model$gamma_shape_prior_distr
#> [1] NA
#> 
#> [[2]]$gamma_site_model$freq_equilibrium
#> [1] "estimated"
#> 
#> [[2]]$gamma_site_model$freq_prior_uniform_distr_id
#> [1] 1000
#> 
#> 
#> [[2]]$kappa_param
#> [[2]]$kappa_param$name
#> [1] "kappa"
#> 
#> [[2]]$kappa_param$id
#> [1] NA
#> 
#> [[2]]$kappa_param$value
#> [1] "2.0"
#> 
#> [[2]]$kappa_param$lower
#> [1] "0.0"
#> 
#> [[2]]$kappa_param$estimate
#> [1] TRUE
#> 
#> 
#> [[2]]$kappa_prior_distr
#> [[2]]$kappa_prior_distr$name
#> [1] "log_normal"
#> 
#> [[2]]$kappa_prior_distr$id
#> [1] NA
#> 
#> [[2]]$kappa_prior_distr$value
#> [1] NA
#> 
#> [[2]]$kappa_prior_distr$lower
#> [1] NA
#> 
#> [[2]]$kappa_prior_distr$upper
#> [1] NA
#> 
#> [[2]]$kappa_prior_distr$m
#> [[2]]$kappa_prior_distr$m$name
#> [1] "m"
#> 
#> [[2]]$kappa_prior_distr$m$id
#> [1] NA
#> 
#> [[2]]$kappa_prior_distr$m$value
#> [1] "1.0"
#> 
#> [[2]]$kappa_prior_distr$m$estimate
#> [1] FALSE
#> 
#> [[2]]$kappa_prior_distr$m$lower
#> [1] NA
#> 
#> [[2]]$kappa_prior_distr$m$upper
#> [1] NA
#> 
#> 
#> [[2]]$kappa_prior_distr$s
#> [[2]]$kappa_prior_distr$s$name
#> [1] "s"
#> 
#> [[2]]$kappa_prior_distr$s$id
#> [1] NA
#> 
#> [[2]]$kappa_prior_distr$s$value
#> [1] 1.25
#> 
#> [[2]]$kappa_prior_distr$s$estimate
#> [1] FALSE
#> 
#> [[2]]$kappa_prior_distr$s$lower
#> [1] 0
#> 
#> [[2]]$kappa_prior_distr$s$upper
#> [1] NA
#> 
#> 
#> 
#> [[2]]$freq_equilibrium
#> [1] "estimated"
#> 
#> [[2]]$freq_param
#> [[2]]$freq_param$name
#> [1] "freqParameter"
#> 
#> [[2]]$freq_param$id
#> [1] NA
#> 
#> [[2]]$freq_param$value
#> [1] "0.25"
#> 
#> [[2]]$freq_param$lower
#> [1] "0.0"
#> 
#> [[2]]$freq_param$upper
#> [1] "1.0"
#> 
#> [[2]]$freq_param$estimate
#> [1] TRUE
#> 
#> [[2]]$freq_param$dimension
#> [1] 4
#> 
#> 
#> 
#> [[3]]
#> [[3]]$name
#> [1] "TN93"
#> 
#> [[3]]$id
#> [1] NA
#> 
#> [[3]]$gamma_site_model
#> [[3]]$gamma_site_model$gamma_cat_count
#> [1] "0"
#> 
#> [[3]]$gamma_site_model$gamma_shape
#> [1] "1.0"
#> 
#> [[3]]$gamma_site_model$prop_invariant
#> [1] "0.0"
#> 
#> [[3]]$gamma_site_model$gamma_shape_prior_distr
#> [1] NA
#> 
#> [[3]]$gamma_site_model$freq_equilibrium
#> [1] "estimated"
#> 
#> [[3]]$gamma_site_model$freq_prior_uniform_distr_id
#> [1] 1000
#> 
#> 
#> [[3]]$kappa_1_prior_distr
#> [[3]]$kappa_1_prior_distr$name
#> [1] "log_normal"
#> 
#> [[3]]$kappa_1_prior_distr$id
#> [1] NA
#> 
#> [[3]]$kappa_1_prior_distr$value
#> [1] NA
#> 
#> [[3]]$kappa_1_prior_distr$lower
#> [1] NA
#> 
#> [[3]]$kappa_1_prior_distr$upper
#> [1] NA
#> 
#> [[3]]$kappa_1_prior_distr$m
#> [[3]]$kappa_1_prior_distr$m$name
#> [1] "m"
#> 
#> [[3]]$kappa_1_prior_distr$m$id
#> [1] NA
#> 
#> [[3]]$kappa_1_prior_distr$m$value
#> [1] 1
#> 
#> [[3]]$kappa_1_prior_distr$m$estimate
#> [1] FALSE
#> 
#> [[3]]$kappa_1_prior_distr$m$lower
#> [1] NA
#> 
#> [[3]]$kappa_1_prior_distr$m$upper
#> [1] NA
#> 
#> 
#> [[3]]$kappa_1_prior_distr$s
#> [[3]]$kappa_1_prior_distr$s$name
#> [1] "s"
#> 
#> [[3]]$kappa_1_prior_distr$s$id
#> [1] NA
#> 
#> [[3]]$kappa_1_prior_distr$s$value
#> [1] 1.25
#> 
#> [[3]]$kappa_1_prior_distr$s$estimate
#> [1] FALSE
#> 
#> [[3]]$kappa_1_prior_distr$s$lower
#> [1] 0
#> 
#> [[3]]$kappa_1_prior_distr$s$upper
#> [1] NA
#> 
#> 
#> 
#> [[3]]$kappa_2_prior_distr
#> [[3]]$kappa_2_prior_distr$name
#> [1] "log_normal"
#> 
#> [[3]]$kappa_2_prior_distr$id
#> [1] NA
#> 
#> [[3]]$kappa_2_prior_distr$value
#> [1] NA
#> 
#> [[3]]$kappa_2_prior_distr$lower
#> [1] NA
#> 
#> [[3]]$kappa_2_prior_distr$upper
#> [1] NA
#> 
#> [[3]]$kappa_2_prior_distr$m
#> [[3]]$kappa_2_prior_distr$m$name
#> [1] "m"
#> 
#> [[3]]$kappa_2_prior_distr$m$id
#> [1] NA
#> 
#> [[3]]$kappa_2_prior_distr$m$value
#> [1] 1
#> 
#> [[3]]$kappa_2_prior_distr$m$estimate
#> [1] FALSE
#> 
#> [[3]]$kappa_2_prior_distr$m$lower
#> [1] NA
#> 
#> [[3]]$kappa_2_prior_distr$m$upper
#> [1] NA
#> 
#> 
#> [[3]]$kappa_2_prior_distr$s
#> [[3]]$kappa_2_prior_distr$s$name
#> [1] "s"
#> 
#> [[3]]$kappa_2_prior_distr$s$id
#> [1] NA
#> 
#> [[3]]$kappa_2_prior_distr$s$value
#> [1] 1.25
#> 
#> [[3]]$kappa_2_prior_distr$s$estimate
#> [1] FALSE
#> 
#> [[3]]$kappa_2_prior_distr$s$lower
#> [1] 0
#> 
#> [[3]]$kappa_2_prior_distr$s$upper
#> [1] NA
#> 
#> 
#> 
#> [[3]]$kappa_1_param
#> [[3]]$kappa_1_param$name
#> [1] "kappa_1"
#> 
#> [[3]]$kappa_1_param$id
#> [1] NA
#> 
#> [[3]]$kappa_1_param$value
#> [1] "2.0"
#> 
#> [[3]]$kappa_1_param$lower
#> [1] "0.0"
#> 
#> [[3]]$kappa_1_param$estimate
#> [1] TRUE
#> 
#> 
#> [[3]]$kappa_2_param
#> [[3]]$kappa_2_param$name
#> [1] "kappa_2"
#> 
#> [[3]]$kappa_2_param$id
#> [1] NA
#> 
#> [[3]]$kappa_2_param$value
#> [1] "2.0"
#> 
#> [[3]]$kappa_2_param$lower
#> [1] "0.0"
#> 
#> [[3]]$kappa_2_param$estimate
#> [1] TRUE
#> 
#> 
#> [[3]]$freq_equilibrium
#> [1] "estimated"
#> 
#> [[3]]$freq_param
#> [[3]]$freq_param$name
#> [1] "freqParameter"
#> 
#> [[3]]$freq_param$id
#> [1] NA
#> 
#> [[3]]$freq_param$value
#> [1] "0.25"
#> 
#> [[3]]$freq_param$lower
#> [1] "0.0"
#> 
#> [[3]]$freq_param$upper
#> [1] "1.0"
#> 
#> [[3]]$freq_param$estimate
#> [1] TRUE
#> 
#> [[3]]$freq_param$dimension
#> [1] 4
#> 
#> 
#> 
#> [[4]]
#> [[4]]$name
#> [1] "GTR"
#> 
#> [[4]]$id
#> [1] NA
#> 
#> [[4]]$gamma_site_model
#> [[4]]$gamma_site_model$gamma_cat_count
#> [1] "0"
#> 
#> [[4]]$gamma_site_model$gamma_shape
#> [1] "1.0"
#> 
#> [[4]]$gamma_site_model$prop_invariant
#> [1] "0.0"
#> 
#> [[4]]$gamma_site_model$gamma_shape_prior_distr
#> [1] NA
#> 
#> [[4]]$gamma_site_model$freq_equilibrium
#> [1] "estimated"
#> 
#> [[4]]$gamma_site_model$freq_prior_uniform_distr_id
#> [1] 1000
#> 
#> 
#> [[4]]$rate_ac_prior_distr
#> [[4]]$rate_ac_prior_distr$name
#> [1] "gamma"
#> 
#> [[4]]$rate_ac_prior_distr$id
#> [1] NA
#> 
#> [[4]]$rate_ac_prior_distr$value
#> [1] NA
#> 
#> [[4]]$rate_ac_prior_distr$lower
#> [1] NA
#> 
#> [[4]]$rate_ac_prior_distr$upper
#> [1] NA
#> 
#> [[4]]$rate_ac_prior_distr$alpha
#> [[4]]$rate_ac_prior_distr$alpha$name
#> [1] "alpha"
#> 
#> [[4]]$rate_ac_prior_distr$alpha$id
#> [1] NA
#> 
#> [[4]]$rate_ac_prior_distr$alpha$value
#> [1] 0.05
#> 
#> [[4]]$rate_ac_prior_distr$alpha$estimate
#> [1] FALSE
#> 
#> 
#> [[4]]$rate_ac_prior_distr$beta
#> [[4]]$rate_ac_prior_distr$beta$name
#> [1] "beta"
#> 
#> [[4]]$rate_ac_prior_distr$beta$id
#> [1] NA
#> 
#> [[4]]$rate_ac_prior_distr$beta$value
#> [1] "10.0"
#> 
#> [[4]]$rate_ac_prior_distr$beta$estimate
#> [1] FALSE
#> 
#> 
#> 
#> [[4]]$rate_ag_prior_distr
#> [[4]]$rate_ag_prior_distr$name
#> [1] "gamma"
#> 
#> [[4]]$rate_ag_prior_distr$id
#> [1] NA
#> 
#> [[4]]$rate_ag_prior_distr$value
#> [1] NA
#> 
#> [[4]]$rate_ag_prior_distr$lower
#> [1] NA
#> 
#> [[4]]$rate_ag_prior_distr$upper
#> [1] NA
#> 
#> [[4]]$rate_ag_prior_distr$alpha
#> [[4]]$rate_ag_prior_distr$alpha$name
#> [1] "alpha"
#> 
#> [[4]]$rate_ag_prior_distr$alpha$id
#> [1] NA
#> 
#> [[4]]$rate_ag_prior_distr$alpha$value
#> [1] 0.05
#> 
#> [[4]]$rate_ag_prior_distr$alpha$estimate
#> [1] FALSE
#> 
#> 
#> [[4]]$rate_ag_prior_distr$beta
#> [[4]]$rate_ag_prior_distr$beta$name
#> [1] "beta"
#> 
#> [[4]]$rate_ag_prior_distr$beta$id
#> [1] NA
#> 
#> [[4]]$rate_ag_prior_distr$beta$value
#> [1] "20.0"
#> 
#> [[4]]$rate_ag_prior_distr$beta$estimate
#> [1] FALSE
#> 
#> 
#> 
#> [[4]]$rate_at_prior_distr
#> [[4]]$rate_at_prior_distr$name
#> [1] "gamma"
#> 
#> [[4]]$rate_at_prior_distr$id
#> [1] NA
#> 
#> [[4]]$rate_at_prior_distr$value
#> [1] NA
#> 
#> [[4]]$rate_at_prior_distr$lower
#> [1] NA
#> 
#> [[4]]$rate_at_prior_distr$upper
#> [1] NA
#> 
#> [[4]]$rate_at_prior_distr$alpha
#> [[4]]$rate_at_prior_distr$alpha$name
#> [1] "alpha"
#> 
#> [[4]]$rate_at_prior_distr$alpha$id
#> [1] NA
#> 
#> [[4]]$rate_at_prior_distr$alpha$value
#> [1] 0.05
#> 
#> [[4]]$rate_at_prior_distr$alpha$estimate
#> [1] FALSE
#> 
#> 
#> [[4]]$rate_at_prior_distr$beta
#> [[4]]$rate_at_prior_distr$beta$name
#> [1] "beta"
#> 
#> [[4]]$rate_at_prior_distr$beta$id
#> [1] NA
#> 
#> [[4]]$rate_at_prior_distr$beta$value
#> [1] "10.0"
#> 
#> [[4]]$rate_at_prior_distr$beta$estimate
#> [1] FALSE
#> 
#> 
#> 
#> [[4]]$rate_cg_prior_distr
#> [[4]]$rate_cg_prior_distr$name
#> [1] "gamma"
#> 
#> [[4]]$rate_cg_prior_distr$id
#> [1] NA
#> 
#> [[4]]$rate_cg_prior_distr$value
#> [1] NA
#> 
#> [[4]]$rate_cg_prior_distr$lower
#> [1] NA
#> 
#> [[4]]$rate_cg_prior_distr$upper
#> [1] NA
#> 
#> [[4]]$rate_cg_prior_distr$alpha
#> [[4]]$rate_cg_prior_distr$alpha$name
#> [1] "alpha"
#> 
#> [[4]]$rate_cg_prior_distr$alpha$id
#> [1] NA
#> 
#> [[4]]$rate_cg_prior_distr$alpha$value
#> [1] 0.05
#> 
#> [[4]]$rate_cg_prior_distr$alpha$estimate
#> [1] FALSE
#> 
#> 
#> [[4]]$rate_cg_prior_distr$beta
#> [[4]]$rate_cg_prior_distr$beta$name
#> [1] "beta"
#> 
#> [[4]]$rate_cg_prior_distr$beta$id
#> [1] NA
#> 
#> [[4]]$rate_cg_prior_distr$beta$value
#> [1] "10.0"
#> 
#> [[4]]$rate_cg_prior_distr$beta$estimate
#> [1] FALSE
#> 
#> 
#> 
#> [[4]]$rate_gt_prior_distr
#> [[4]]$rate_gt_prior_distr$name
#> [1] "gamma"
#> 
#> [[4]]$rate_gt_prior_distr$id
#> [1] NA
#> 
#> [[4]]$rate_gt_prior_distr$value
#> [1] NA
#> 
#> [[4]]$rate_gt_prior_distr$lower
#> [1] NA
#> 
#> [[4]]$rate_gt_prior_distr$upper
#> [1] NA
#> 
#> [[4]]$rate_gt_prior_distr$alpha
#> [[4]]$rate_gt_prior_distr$alpha$name
#> [1] "alpha"
#> 
#> [[4]]$rate_gt_prior_distr$alpha$id
#> [1] NA
#> 
#> [[4]]$rate_gt_prior_distr$alpha$value
#> [1] 0.05
#> 
#> [[4]]$rate_gt_prior_distr$alpha$estimate
#> [1] FALSE
#> 
#> 
#> [[4]]$rate_gt_prior_distr$beta
#> [[4]]$rate_gt_prior_distr$beta$name
#> [1] "beta"
#> 
#> [[4]]$rate_gt_prior_distr$beta$id
#> [1] NA
#> 
#> [[4]]$rate_gt_prior_distr$beta$value
#> [1] "10.0"
#> 
#> [[4]]$rate_gt_prior_distr$beta$estimate
#> [1] FALSE
#> 
#> 
#> 
#> [[4]]$rate_ac_param
#> [[4]]$rate_ac_param$name
#> [1] "rate_ac"
#> 
#> [[4]]$rate_ac_param$id
#> [1] NA
#> 
#> [[4]]$rate_ac_param$value
#> [1] "1.0"
#> 
#> [[4]]$rate_ac_param$estimate
#> [1] TRUE
#> 
#> [[4]]$rate_ac_param$lower
#> [1] "0.0"
#> 
#> 
#> [[4]]$rate_ag_param
#> [[4]]$rate_ag_param$name
#> [1] "rate_ag"
#> 
#> [[4]]$rate_ag_param$id
#> [1] NA
#> 
#> [[4]]$rate_ag_param$value
#> [1] "1.0"
#> 
#> [[4]]$rate_ag_param$estimate
#> [1] TRUE
#> 
#> [[4]]$rate_ag_param$lower
#> [1] "0.0"
#> 
#> 
#> [[4]]$rate_at_param
#> [[4]]$rate_at_param$name
#> [1] "rate_at"
#> 
#> [[4]]$rate_at_param$id
#> [1] NA
#> 
#> [[4]]$rate_at_param$value
#> [1] "1.0"
#> 
#> [[4]]$rate_at_param$estimate
#> [1] TRUE
#> 
#> [[4]]$rate_at_param$lower
#> [1] "0.0"
#> 
#> 
#> [[4]]$rate_cg_param
#> [[4]]$rate_cg_param$name
#> [1] "rate_cg"
#> 
#> [[4]]$rate_cg_param$id
#> [1] NA
#> 
#> [[4]]$rate_cg_param$value
#> [1] "1.0"
#> 
#> [[4]]$rate_cg_param$estimate
#> [1] TRUE
#> 
#> [[4]]$rate_cg_param$lower
#> [1] "0.0"
#> 
#> 
#> [[4]]$rate_ct_param
#> [[4]]$rate_ct_param$name
#> [1] "rate_ct"
#> 
#> [[4]]$rate_ct_param$id
#> [1] NA
#> 
#> [[4]]$rate_ct_param$value
#> [1] "1.0"
#> 
#> [[4]]$rate_ct_param$estimate
#> [1] FALSE
#> 
#> [[4]]$rate_ct_param$lower
#> [1] "0.0"
#> 
#> 
#> [[4]]$rate_gt_param
#> [[4]]$rate_gt_param$name
#> [1] "rate_gt"
#> 
#> [[4]]$rate_gt_param$id
#> [1] NA
#> 
#> [[4]]$rate_gt_param$value
#> [1] "1.0"
#> 
#> [[4]]$rate_gt_param$estimate
#> [1] TRUE
#> 
#> [[4]]$rate_gt_param$lower
#> [1] "0.0"
#> 
#> 
#> [[4]]$freq_equilibrium
#> [1] "estimated"
#> 
#> [[4]]$freq_param
#> [[4]]$freq_param$name
#> [1] "freqParameter"
#> 
#> [[4]]$freq_param$id
#> [1] NA
#> 
#> [[4]]$freq_param$value
#> [1] "0.25"
#> 
#> [[4]]$freq_param$lower
#> [1] "0.0"
#> 
#> [[4]]$freq_param$upper
#> [1] "1.0"
#> 
#> [[4]]$freq_param$estimate
#> [1] TRUE
#> 
#> [[4]]$freq_param$dimension
#> [1] 4
#> 
#> 
#> 

check_empty_beautier_folder()
```
