# Function to check if a file exists. Calls `stop` if the file is absent

Function to check if a file exists. Calls `stop` if the file is absent

## Usage

``` r
check_file_exists(filename, filename_description = NA)
```

## Arguments

- filename:

  name of the file

- filename_description:

  description of the filename

## Value

nothing. Will `stop` if the file is absent, with a proper error message

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
check_empty_beautier_folder()

check_file_exists(get_beautier_path("anthus_aco_sub.fas"))

check_empty_beautier_folder()
```
