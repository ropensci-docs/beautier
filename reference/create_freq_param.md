# Create a parameter called freq

Create a parameter called freq

## Usage

``` r
create_freq_param(
  id = NA,
  lower = "0.0",
  upper = "1.0",
  value = "0.25",
  estimate = TRUE,
  dimension = 4
)
```

## Arguments

- id:

  the parameter's ID

- lower:

  lowest possible value of the parameter. If the parameter is estimated,
  `lower` must be less than `value`

- upper:

  upper value of the parameter

- value:

  value of the parameter

- estimate:

  TRUE if this parameter is to be estimated by BEAST2, FALSE otherwise

- dimension:

  the number of dimensions, for example, as used in create_freq_param

## Value

a parameter called freq

## Author

Richèl J.C. Bilderbeek
