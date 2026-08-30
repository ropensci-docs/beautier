# Documentation of general function arguments. This function does nothing. It is intended to inherit function argument documentation.

Documentation of general function arguments. This function does nothing.
It is intended to inherit function argument documentation.

## Usage

``` r
default_params_doc(
  alignment_id,
  allow_empty_str,
  allow_na,
  alpha_parameter,
  b_pop_sizes_param,
  b_pop_sizes_parameter,
  bd_tree_prior,
  beautier_folder,
  cbs_tree_prior,
  beast2_input_filename,
  beast2_version,
  beauti_options,
  beta_parameter,
  ccp_tree_prior,
  cep_tree_prior,
  chain_length,
  clock_model,
  clock_model_name,
  clock_model_names,
  clock_models,
  clock_prior_distr_id,
  clock_rate_param,
  crown_age,
  crown_ages,
  distr_id,
  fasta_filename,
  fasta_filenames,
  filename,
  fixed_crown_age,
  fixed_crown_ages,
  freq_param,
  gamma_distr,
  gamma_site_model,
  group_sizes_dimension,
  gtr_site_model,
  has_non_strict_clock_model,
  has_tip_dating,
  hky_site_model,
  id,
  ids,
  inference_model,
  inference_models,
  initial_phylogenies,
  input_filename,
  input_filenames,
  is_monophyletic,
  jc69_site_model,
  kappa_param,
  log_every,
  m_param,
  mcmc,
  mode,
  mrca_prior,
  mrca_priors,
  mrca_prior_name,
  n_init_attempts,
  output_filename,
  param,
  param_id,
  phylogeny,
  pop_sizes_scaler_scale_factor,
  pre_burnin,
  rate_scaler_factor,
  rename_fun,
  rln_clock_model,
  sample_from_prior,
  sanitise_headers,
  screenlog,
  sequence_length,
  site_model,
  site_model_name,
  site_model_names,
  site_models,
  sort,
  store_every,
  strict_clock_model,
  taxa_names,
  tipdates_filename,
  tn93_site_model,
  tracelog,
  treelog,
  tree_prior,
  tree_prior_name,
  tree_prior_names,
  tree_priors,
  verbose,
  yule_tree_prior
)
```

## Arguments

- alignment_id:

  ID of the alignment, as returned by
  [get_alignment_id](https://docs.ropensci.org/beautier/reference/get_alignment_id.md).
  Keep at `NA` to have it initialized automatically

- allow_empty_str:

  allow a string to be empty

- allow_na:

  allow [NA](https://rdrr.io/r/base/NA.html)

- alpha_parameter:

  an alpha parameter, as created by
  [create_alpha_param](https://docs.ropensci.org/beautier/reference/create_alpha_param.md)

- b_pop_sizes_param:

  a Bayesian population size parameter, as created by
  [create_b_pop_sizes_param](https://docs.ropensci.org/beautier/reference/create_b_pop_sizes_param.md)

- b_pop_sizes_parameter:

  a Bayesian population size parameter, as created by
  [create_b_pop_sizes_param](https://docs.ropensci.org/beautier/reference/create_b_pop_sizes_param.md)

- bd_tree_prior:

  a Birth-Death tree prior, as created by
  [`create_bd_tree_prior`](https://docs.ropensci.org/beautier/reference/create_bd_tree_prior.md)

- beautier_folder:

  the path to the
  [beautier](https://docs.ropensci.org/beautier/reference/beautier-package.md)
  temporary files folder

- cbs_tree_prior:

  a Coalescent Bayesian Skyline tree prior, as returned by
  [`create_cbs_tree_prior`](https://docs.ropensci.org/beautier/reference/create_cbs_tree_prior.md)

- beast2_input_filename:

  path to a BEAST2 XML input file

- beast2_version:

  BEAST2 version, for example, `"2.5"`

- beauti_options:

  one BEAUti options object, as returned by
  [`create_beauti_options`](https://docs.ropensci.org/beautier/reference/create_beauti_options.md)

- beta_parameter:

  a beta parameter, as created by
  [create_beta_param](https://docs.ropensci.org/beautier/reference/create_beta_param.md)

- ccp_tree_prior:

  a Coalescent Constant Population tree prior, as returned by
  [`create_ccp_tree_prior`](https://docs.ropensci.org/beautier/reference/create_ccp_tree_prior.md)

- cep_tree_prior:

  a Coalescent Exponential Population tree prior, as returned by
  [`create_cep_tree_prior`](https://docs.ropensci.org/beautier/reference/create_cep_tree_prior.md)

- chain_length:

  length of the MCMC chain

- clock_model:

  a clock model, as returned by
  [`create_clock_model`](https://docs.ropensci.org/beautier/reference/create_clock_model.md)

- clock_model_name:

  name of a clock model, must be a name as returned by
  [`get_clock_model_names`](https://docs.ropensci.org/beautier/reference/get_clock_model_names.md)

- clock_model_names:

  one or more names of a clock model, must be name among those returned
  by
  [`get_clock_model_names`](https://docs.ropensci.org/beautier/reference/get_clock_model_names.md)

- clock_models:

  a list of one or more clock models, as returned by
  [`create_clock_model`](https://docs.ropensci.org/beautier/reference/create_clock_model.md)

- clock_prior_distr_id:

  ID of an MRCA clock model's distribution. Keep at `NA` to have it
  initialized automatically

- clock_rate_param:

  a `clockRate` parameter, a numeric value, as created by
  [create_clock_rate_param](https://docs.ropensci.org/beautier/reference/create_clock_rate_param.md)

- crown_age:

  the crown age of the phylogeny

- crown_ages:

  the crown ages of the phylogenies. Set to NA if the crown age needs to
  be estimated

- distr_id:

  a distributions' ID

- fasta_filename:

  a FASTA filename. Use
  [`get_fasta_filename`](https://docs.ropensci.org/beautier/reference/get_fasta_filename.md)
  to obtain a testing FASTA filename. Note that BEAST2 also supports
  missing data, by using a dash (`-`) or question mark (`?`) as a
  sequence.

- fasta_filenames:

  One or more FASTA filenames. Use
  [`get_fasta_filename`](https://docs.ropensci.org/beautier/reference/get_fasta_filename.md)
  to obtain a testing FASTA filename.

- filename:

  a filename, as can be checked by
  [check_filename](https://docs.ropensci.org/beautier/reference/check_filename.md)

- fixed_crown_age:

  determines if the phylogeny's crown age is fixed. If FALSE, crown age
  is estimated by BEAST2. If TRUE, the crown age is fixed to the crown
  age of the initial phylogeny.

- fixed_crown_ages:

  one or more booleans to determine if the phylogenies' crown ages are
  fixed. If FALSE, crown age is estimated by BEAST2. If TRUE, the crown
  age is fixed to the crown age of the initial phylogeny.

- freq_param:

  a \`freq\` parameter, as created by
  [create_freq_param](https://docs.ropensci.org/beautier/reference/create_freq_param.md)

- gamma_distr:

  a gamma distribution, as created by
  [`create_gamma_distr`](https://docs.ropensci.org/beautier/reference/create_gamma_distr.md))

- gamma_site_model:

  a site model's gamma site model, as returned by
  [`create_gamma_site_model`](https://docs.ropensci.org/beautier/reference/create_gamma_site_model.md)

- group_sizes_dimension:

  the group sizes' dimension, as used by the CBS tree prior (see
  [`create_cbs_tree_prior`](https://docs.ropensci.org/beautier/reference/create_cbs_tree_prior.md))

- gtr_site_model:

  a GTR site model, as returned by
  [`create_gtr_site_model`](https://docs.ropensci.org/beautier/reference/create_gtr_site_model.md)

- has_non_strict_clock_model:

  boolean to indicate that the is already at least one non-strict (i.e.
  relaxed log-normal) clock model

- has_tip_dating:

  TRUE if the user has supplied tip dates, FALSE otherwise

- hky_site_model:

  an HKY site model, as returned by
  [`create_hky_site_model`](https://docs.ropensci.org/beautier/reference/create_hky_site_model.md)

- id:

  an alignment's IDs. An ID can be extracted from its FASTA filename
  with
  [`get_alignment_ids_from_fasta_filenames`](https://docs.ropensci.org/beautier/reference/get_alignment_ids_from_fasta_filenames.md))

- ids:

  one or more alignments' IDs. IDs can be extracted from their FASTA
  filenames with
  [`get_alignment_ids_from_fasta_filenames`](https://docs.ropensci.org/beautier/reference/get_alignment_ids_from_fasta_filenames.md))

- inference_model:

  a Bayesian phylogenetic inference model. An inference model is the
  complete model setup in which a site model, clock model, tree prior
  and more are specified. Use
  [create_inference_model](https://docs.ropensci.org/beautier/reference/create_inference_model.md)
  to create an inference model. Use
  [check_inference_model](https://docs.ropensci.org/beautier/reference/check_inference_model.md)
  to check if an inference model is valid. Use
  [rename_inference_model_filenames](https://docs.ropensci.org/beautier/reference/rename_inference_model_filenames.md)
  to rename the files in an inference model.

- inference_models:

  a list of one or more inference models, as can be created by
  [create_inference_model](https://docs.ropensci.org/beautier/reference/create_inference_model.md)

- initial_phylogenies:

  one or more MCMC chain's initial phylogenies. Each one set to `NA`
  will result in BEAST2 using a random phylogeny. Else the phylogeny is
  assumed to be of class `phylo` from the `ape` package

- input_filename:

  A FASTA filename. Use
  [`get_fasta_filename`](https://docs.ropensci.org/beautier/reference/get_fasta_filename.md)
  to obtain a testing FASTA filename.

- input_filenames:

  One or more FASTA filenames. Use
  [`get_fasta_filename`](https://docs.ropensci.org/beautier/reference/get_fasta_filename.md)
  to obtain a testing FASTA filename.

- is_monophyletic:

  boolean to indicate monophyly is assumed in a Most Recent Common
  Ancestor prior, as returned by
  [`create_mrca_prior`](https://docs.ropensci.org/beautier/reference/create_mrca_prior.md)

- jc69_site_model:

  a JC69 site model, as returned by
  [`create_jc69_site_model`](https://docs.ropensci.org/beautier/reference/create_jc69_site_model.md)

- kappa_param:

  a kappa parameter, as created by
  [create_kappa_param](https://docs.ropensci.org/beautier/reference/create_kappa_param.md)

- log_every:

  number of MCMC states between writing to file

- m_param:

  an m parameter, as created by
  [create_m_param](https://docs.ropensci.org/beautier/reference/create_m_param.md)

- mcmc:

  one MCMC. Use
  [`create_mcmc`](https://docs.ropensci.org/beautier/reference/create_mcmc.md)
  to create an MCMC. Use
  [`create_ns_mcmc`](https://docs.ropensci.org/beautier/reference/create_ns_mcmc.md)
  to create an MCMC for a Nested Sampling run. Use
  [`check_mcmc`](https://docs.ropensci.org/beautier/reference/check_mcmc.md)
  to check if an MCMC is valid. Use
  [`rename_mcmc_filenames`](https://docs.ropensci.org/beautier/reference/rename_mcmc_filenames.md)
  to rename the filenames in an MCMC.

- mode:

  mode how to log. Valid values are the ones returned by
  [get_log_modes](https://docs.ropensci.org/beautier/reference/get_log_modes.md)

- mrca_prior:

  a Most Recent Common Ancestor prior, as returned by
  [`create_mrca_prior`](https://docs.ropensci.org/beautier/reference/create_mrca_prior.md)

- mrca_priors:

  a list of one or more Most Recent Common Ancestor priors, as returned
  by
  [`create_mrca_prior`](https://docs.ropensci.org/beautier/reference/create_mrca_prior.md)

- mrca_prior_name:

  the unique name of the MRCA prior, for example a genus, family, order
  or even class name. Leave at [NA](https://rdrr.io/r/base/NA.html) to
  have it named automatically.

- n_init_attempts:

  number of initialization attempts before failing

- output_filename:

  Name of the XML parameter file created by this function. BEAST2 uses
  this file as input.

- param:

  a parameter, as can be created by
  [`create_param`](https://docs.ropensci.org/beautier/reference/create_param.md).

- param_id:

  a parameter's ID

- phylogeny:

  a phylogeny of type `phylo` from the `ape` package

- pop_sizes_scaler_scale_factor:

  the scale factor used by the population sizes scaler operator

- pre_burnin:

  number of burn in samples taken before entering the main loop

- rate_scaler_factor:

  the strict clock model's operator scaler for the rate. Use an empty
  string to indicate the default.

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

- rln_clock_model:

  a Relaxed Log-Normal clock model, as returned by
  [`create_rln_clock_model`](https://docs.ropensci.org/beautier/reference/create_rln_clock_model.md)

- sample_from_prior:

  set to [TRUE](https://rdrr.io/r/base/logical.html) to sample from the
  prior

- sanitise_headers:

  set to [TRUE](https://rdrr.io/r/base/logical.html) to sanitise the
  headers of the log file

- screenlog:

  a `screenlog`, as created by
  [create_screenlog](https://docs.ropensci.org/beautier/reference/create_screenlog.md)

- sequence_length:

  a DNA sequence length, in base pairs

- site_model:

  a site model, as returned by
  [`create_site_model`](https://docs.ropensci.org/beautier/reference/create_site_model.md)

- site_model_name:

  name of a site model, must be a name as returned by
  [`get_site_model_names`](https://docs.ropensci.org/beautier/reference/get_site_model_names.md)

- site_model_names:

  one or more names of a site model, must be name among those returned
  by
  [`get_site_model_names`](https://docs.ropensci.org/beautier/reference/get_site_model_names.md)

- site_models:

  one or more site models, as returned by
  [`create_site_model`](https://docs.ropensci.org/beautier/reference/create_site_model.md)

- sort:

  how to sort the log. Valid values are the ones returned by
  [get_log_sorts](https://docs.ropensci.org/beautier/reference/get_log_sorts.md)

- store_every:

  number of states the MCMC will process before the posterior's state
  will be saved to file. Use -1 or `NA` to use the default frequency.

- strict_clock_model:

  a strict clock model, as returned by
  [`create_strict_clock_model`](https://docs.ropensci.org/beautier/reference/create_strict_clock_model.md)

- taxa_names:

  names of the taxa, as returned by
  [`get_taxa_names`](https://docs.ropensci.org/beautier/reference/get_taxa_names.md).
  Keep at `NA` to have it initialized automatically, using all taxa in
  the alignment

- tipdates_filename:

  name of the file containing the tip dates. This file is assumed to
  have two columns, separated by a tab. The first column contains the
  taxa names, the second column contains the date.

- tn93_site_model:

  a TN93 site model, as returned by
  [`create_tn93_site_model`](https://docs.ropensci.org/beautier/reference/create_tn93_site_model.md)

- tracelog:

  a `tracelog`, as created by
  [create_tracelog](https://docs.ropensci.org/beautier/reference/create_tracelog.md)

- treelog:

  a `treelog`, as created by
  [create_treelog](https://docs.ropensci.org/beautier/reference/create_treelog.md)

- tree_prior:

  a tree priors, as returned by
  [`create_tree_prior`](https://docs.ropensci.org/beautier/reference/create_tree_prior.md)

- tree_prior_name:

  name of a tree prior, must be a name as returned by
  [`get_tree_prior_names`](https://docs.ropensci.org/beautier/reference/get_tree_prior_names.md)

- tree_prior_names:

  one or more names of a tree prior, must be a name among those returned
  by
  [`get_tree_prior_names`](https://docs.ropensci.org/beautier/reference/get_tree_prior_names.md)

- tree_priors:

  one or more tree priors, as returned by
  [`create_tree_prior`](https://docs.ropensci.org/beautier/reference/create_tree_prior.md)

- verbose:

  if TRUE, additional information is displayed, that is potentially
  useful in debugging

- yule_tree_prior:

  a Yule tree_prior, as created by
  [`create_yule_tree_prior`](https://docs.ropensci.org/beautier/reference/create_yule_tree_prior.md)

## Note

This is an internal function, so it should be marked with `@export`.
This is not done, as this will disallow all functions to find the
documentation parameters

## Author

Richèl J.C. Bilderbeek
