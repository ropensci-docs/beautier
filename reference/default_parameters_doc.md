# Documentation of parameters (for example, `create_param`. This function does nothing. It is intended to inherit documentation from.

Documentation of parameters (for example, `create_param`. This function
does nothing. It is intended to inherit documentation from.

## Usage

``` r
default_parameters_doc(dimension, estimate, id, lower, name, upper, value, ...)
```

## Arguments

- dimension:

  the number of dimensions, for example, as used in
  [create_freq_param](https://docs.ropensci.org/beautier/reference/create_freq_param.md)

- estimate:

  TRUE if this parameter is to be estimated by BEAST2, FALSE otherwise

- id:

  the parameter's ID

- lower:

  lowest possible value of the parameter. If the parameter is estimated,
  `lower` must be less than `value`

- name:

  the parameters' name. Valid names can be found in `get_param_names`

- upper:

  upper value of the parameter

- value:

  value of the parameter

- ...:

  specific parameter parameters

## Note

This is an internal function, so it should be marked with `@export`.
This is not done, as this will disallow all functions to find the
documentation parameters

## Author

Richèl J.C. Bilderbeek
