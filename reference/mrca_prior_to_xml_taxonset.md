# Creates the `taxonset` section in the prior section of the distribution section of a BEAST2 XML parameter file.

Creates the `taxonset` section in the prior section of the distribution
section of a BEAST2 XML parameter file.

## Usage

``` r
mrca_prior_to_xml_taxonset(mrca_prior, taxa_names_with_ids = NULL)
```

## Arguments

- mrca_prior:

  a Most Recent Common Ancestor prior, as returned by
  [`create_mrca_prior`](https://docs.ropensci.org/beautier/reference/create_mrca_prior.md)

- taxa_names_with_ids:

  taxa names that already have received an ID. Causes the XML to `idref`
  these

## Value

lines of XML text

## Details

` <taxonset id="all" spec="TaxonSet"> <taxon id="626029_aco" spec="Taxon"/> <taxon id="630116_aco" spec="Taxon"/> <taxon id="630210_aco" spec="Taxon"/> <taxon id="B25702_aco" spec="Taxon"/> <taxon id="61430_aco" spec="Taxon"/> </taxonset> `

## Author

Richèl J.C. Bilderbeek
