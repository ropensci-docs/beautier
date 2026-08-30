# Determine if the object is a valid clock_rate parameter

Determine if the object is a valid clock_rate parameter

## Usage

``` r
is_clock_rate_param(x)
```

## Arguments

- x:

  an object, to be determined if it is a valid clock_rate parameter

## Value

TRUE if x is a valid clock_rate parameter, FALSE otherwise

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

is_clock_rate_param(create_alpha_param())
#> [1] FALSE
is_clock_rate_param(create_beta_param())
#> [1] FALSE
is_clock_rate_param(create_clock_rate_param())
#> [1] TRUE
is_clock_rate_param(create_kappa_1_param())
#> [1] FALSE
is_clock_rate_param(create_kappa_2_param())
#> [1] FALSE
is_clock_rate_param(create_lambda_param())
#> [1] FALSE
is_clock_rate_param(create_m_param())
#> [1] FALSE
is_clock_rate_param(create_mean_param())
#> [1] FALSE
is_clock_rate_param(create_mu_param())
#> [1] FALSE
is_clock_rate_param(create_rate_ac_param())
#> [1] FALSE
is_clock_rate_param(create_rate_ag_param())
#> [1] FALSE
is_clock_rate_param(create_rate_at_param())
#> [1] FALSE
is_clock_rate_param(create_rate_cg_param())
#> [1] FALSE
is_clock_rate_param(create_rate_ct_param())
#> [1] FALSE
is_clock_rate_param(create_rate_gt_param())
#> [1] FALSE
is_clock_rate_param(create_s_param())
#> [1] FALSE
is_clock_rate_param(create_scale_param())
#> [1] FALSE
is_clock_rate_param(create_sigma_param())
#> [1] FALSE

is_clock_rate_param(NA)
#> [1] FALSE
is_clock_rate_param(NULL)
#> [1] FALSE
is_clock_rate_param("nonsense")
#> [1] FALSE
is_clock_rate_param(create_jc69_site_model())
#> [1] FALSE
is_clock_rate_param(create_strict_clock_model())
#> [1] FALSE
is_clock_rate_param(create_yule_tree_prior())
#> [1] FALSE
is_clock_rate_param(create_mcmc())
#> [1] FALSE

check_empty_beautier_folder()
```
