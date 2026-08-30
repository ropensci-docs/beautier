# Read a tip dates file

Read a tip dates file

## Usage

``` r
read_tipdates_file(tipdates_filename)
```

## Arguments

- tipdates_filename:

  name of the file containing the tip dates. This file is assumed to
  have two columns, separated by a tab. The first column contains the
  taxa names, the second column contains the date.

## Value

the tip dates as a tibble, with column names \`taxon\` and \`time\`. The
\`time\` column creates strings instead of numbers, to allow using the
literally same values from the tip dates file in the BEAST2 XML input
file (i.e. avoid rounding errors)

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
read_tipdates_file(get_beautier_path("babette_issue_109.tsv"))
#> # A tibble: 6 × 2
#>   taxon                  time            
#>   <chr>                  <chr>           
#> 1 MK388093.1:ACT/04-2013 2013.25         
#> 2 MK388094.1:SA/12-2013  2013.91666666667
#> 3 MK388095.1:ACT/04-2013 2013.25         
#> 4 MK388096.1:NSW/02-2013 2013.08333333333
#> 5 MK388097.1:SA/07-2012  2012.5          
#> 6 MK388098.1:ACT/04-2014 2014.25         
```
