# Rename the filenames in an inference model

Rename the filenames in an inference model

## Usage

``` r
rename_inference_model_filenames(inference_model, rename_fun)
```

## Arguments

- inference_model:

  a Bayesian phylogenetic inference model. An inference model is the
  complete model setup in which a site model, clock model, tree prior
  and more are specified. Use
  [create_inference_model](https://docs.ropensci.org/beautier/reference/create_inference_model.md)
  to create an inference model. Use
  [check_inference_model](https://docs.ropensci.org/beautier/reference/check_inference_model.md)
  to check if an inference model is valid. Use
  rename_inference_model_filenames to rename the files in an inference
  model.

- rename_fun:

  a function to rename a filename, as can be checked by
  [check_rename_fun](https://docs.ropensci.org/beautier/reference/check_rename_fun.md).
  This function should have one argument, which will be a filename or
  [NA](https://rdrr.io/r/base/NA.html). The function should
  [return](https://rdrr.io/r/base/function.html) one filename (when
  passed one filename) or one [NA](https://rdrr.io/r/base/NA.html) (when
  passed one [NA](https://rdrr.io/r/base/NA.html)). Example rename
  functions are:

  - [get_remove_dir_fun](https://docs.ropensci.org/beautier/reference/get_remove_dir_fun.md)
    get a function that removes the directory paths from the filenames,
    in effect turning these into local files

  - [get_replace_dir_fun](https://docs.ropensci.org/beautier/reference/get_replace_dir_fun.md)
    get a function that replaces the directory paths from the filenames

  - [get_remove_hex_fun](https://docs.ropensci.org/beautier/reference/get_remove_hex_fun.md)
    get a function that removes the hex string from filenames. For
    example, `tracelog_82c1a522040.log` becomes `tracelog.log`

## Value

an inference model with the renamed filenames

## Examples

``` r
check_empty_beautier_folder()

inference_model <- create_inference_model()
inference_model$mcmc$tracelog$filename <- "trace.log"
inference_model$mcmc$screenlog$filename <- "screen.log"
inference_model$mcmc$treelog$filename <- "tree.log"
inference_model$tipdates_filename <- "tipdates.csv"

# Nah, put the files in a folder
inference_model <- rename_inference_model_filenames(
  inference_model = inference_model,
  rename_fun = get_replace_dir_fun("/home/john")
)

# Nah, put the files in anoth folder
inference_model <- rename_inference_model_filenames(
  inference_model = inference_model,
  rename_fun = get_replace_dir_fun("/home/doe")
)

# Nah, store the files locally
rename_inference_model_filenames(
  inference_model = inference_model,
  rename_fun = get_remove_dir_fun()
)
#> $site_model
#> $site_model$name
#> [1] "JC69"
#> 
#> $site_model$id
#> [1] NA
#> 
#> $site_model$gamma_site_model
#> $site_model$gamma_site_model$gamma_cat_count
#> [1] "0"
#> 
#> $site_model$gamma_site_model$gamma_shape
#> [1] "1.0"
#> 
#> $site_model$gamma_site_model$prop_invariant
#> [1] "0.0"
#> 
#> $site_model$gamma_site_model$gamma_shape_prior_distr
#> [1] NA
#> 
#> $site_model$gamma_site_model$freq_equilibrium
#> [1] "estimated"
#> 
#> $site_model$gamma_site_model$freq_prior_uniform_distr_id
#> [1] 1000
#> 
#> 
#> 
#> $clock_model
#> $clock_model$name
#> [1] "strict"
#> 
#> $clock_model$id
#> [1] NA
#> 
#> $clock_model$clock_rate_param
#> $clock_model$clock_rate_param$name
#> [1] "clock_rate"
#> 
#> $clock_model$clock_rate_param$id
#> [1] NA
#> 
#> $clock_model$clock_rate_param$value
#> [1] "1.0"
#> 
#> $clock_model$clock_rate_param$estimate
#> [1] FALSE
#> 
#> 
#> $clock_model$clock_rate_distr
#> $clock_model$clock_rate_distr$name
#> [1] "uniform"
#> 
#> $clock_model$clock_rate_distr$id
#> [1] NA
#> 
#> $clock_model$clock_rate_distr$value
#> [1] NA
#> 
#> $clock_model$clock_rate_distr$lower
#> [1] NA
#> 
#> $clock_model$clock_rate_distr$upper
#> [1] Inf
#> 
#> 
#> $clock_model$rate_scaler_factor
#> [1] 0.75
#> 
#> 
#> $tree_prior
#> $tree_prior$name
#> [1] "yule"
#> 
#> $tree_prior$id
#> [1] NA
#> 
#> $tree_prior$birth_rate_distr
#> $tree_prior$birth_rate_distr$name
#> [1] "uniform"
#> 
#> $tree_prior$birth_rate_distr$id
#> [1] NA
#> 
#> $tree_prior$birth_rate_distr$value
#> [1] NA
#> 
#> $tree_prior$birth_rate_distr$lower
#> [1] NA
#> 
#> $tree_prior$birth_rate_distr$upper
#> [1] Inf
#> 
#> 
#> 
#> $mrca_prior
#> [1] NA
#> 
#> $mcmc
#> $mcmc$chain_length
#> [1] 1e+07
#> 
#> $mcmc$store_every
#> [1] -1
#> 
#> $mcmc$pre_burnin
#> [1] 0
#> 
#> $mcmc$n_init_attempts
#> [1] 10
#> 
#> $mcmc$sample_from_prior
#> [1] FALSE
#> 
#> $mcmc$tracelog
#> $mcmc$tracelog$filename
#> [1] "trace.log"
#> 
#> $mcmc$tracelog$log_every
#> [1] 1000
#> 
#> $mcmc$tracelog$mode
#> [1] "autodetect"
#> 
#> $mcmc$tracelog$sanitise_headers
#> [1] TRUE
#> 
#> $mcmc$tracelog$sort
#> [1] "smart"
#> 
#> 
#> $mcmc$screenlog
#> $mcmc$screenlog$filename
#> [1] "screen.log"
#> 
#> $mcmc$screenlog$log_every
#> [1] 1000
#> 
#> $mcmc$screenlog$mode
#> [1] "autodetect"
#> 
#> $mcmc$screenlog$sanitise_headers
#> [1] FALSE
#> 
#> $mcmc$screenlog$sort
#> [1] "none"
#> 
#> 
#> $mcmc$treelog
#> $mcmc$treelog$filename
#> [1] "tree.log"
#> 
#> $mcmc$treelog$log_every
#> [1] 1000
#> 
#> $mcmc$treelog$mode
#> [1] "tree"
#> 
#> $mcmc$treelog$sanitise_headers
#> [1] FALSE
#> 
#> $mcmc$treelog$sort
#> [1] "none"
#> 
#> 
#> 
#> $beauti_options
#> $beauti_options$capitalize_first_char_id
#> [1] FALSE
#> 
#> $beauti_options$nucleotides_uppercase
#> [1] FALSE
#> 
#> $beauti_options$beast2_version
#> [1] "2.4"
#> 
#> $beauti_options$required
#> [1] ""
#> 
#> $beauti_options$sequence_indent
#> [1] 20
#> 
#> $beauti_options$status
#> [1] ""
#> 
#> $beauti_options$namespace
#> [1] "beast.core:beast.evolution.alignment:beast.evolution.tree.coalescent:beast.core.util:beast.evolution.nuc:beast.evolution.operators:beast.evolution.sitemodel:beast.evolution.substitutionmodel:beast.evolution.likelihood"
#> 
#> $beauti_options$add_operator_schedule
#> [1] FALSE
#> 
#> 
#> $tipdates_filename
#> [1] "tipdates.csv"
#> 

check_empty_beautier_folder()
```
