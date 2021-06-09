
<!-- README.md is generated from README.Rmd. Please edit that file -->

# eurostat R package fork: sans sf edition

R tools to access open data from
[Eurostat](https://ec.europa.eu/eurostat). Data search, download,
manipulation and visualization.

This fork follows the main [rOpenGov
repository](https://github.com/rOpenGov/eurostat) with one crucial
difference: **dependency and functionalities related to sf package have
been removed**. This is to increase the package’s usefulness in systems
where installing the sf package could cause issues.

This fork uses version number x.x.x.9000 to differentiate it from the
main branch version.

### Installation and use

``` r
# Install from GitHub
library(devtools)
devtools::install_github("pitkant/eurostat")
```

The package provides several different ways to get datasets from
Eurostat. Searching for data is one way, if you know what to look for.

``` r
# Load the package
library(eurostat)

# Perform a simple search and print a table
passengers <- search_eurostat("passenger transport")
knitr::kable(head(passengers))
```

| title                                                              | code          | type    | last update of data | last table structure change | data start | data end | values |
|:-------------------------------------------------------------------|:--------------|:--------|:--------------------|:----------------------------|:-----------|:---------|:-------|
| Air passenger transport                                            | enps_avia_pa  | dataset | 16.04.2021          | NA                          | 2005       | 2020     | NA     |
| Volume of passenger transport relative to GDP                      | tran_hv_pstra | dataset | 01.09.2020          | 08.02.2021                  | 1990       | 2018     | NA     |
| Modal split of passenger transport                                 | tran_hv_psmod | dataset | 01.09.2020          | 08.02.2021                  | 1990       | 2018     | NA     |
| Air passenger transport by reporting country                       | avia_paoc     | dataset | 26.05.2021          | 26.05.2021                  | 1993       | 2021Q1   | NA     |
| Air passenger transport by main airports in each reporting country | avia_paoa     | dataset | 26.05.2021          | 07.05.2021                  | 1993       | 2021Q1   | NA     |
| Air passenger transport between reporting countries                | avia_paocc    | dataset | 26.05.2021          | 26.05.2021                  | 1993       | 2021Q1   | NA     |

See the
[Tutorial](https://ropengov.github.io/eurostat/articles/website/eurostat_tutorial.html)
and other resources at the [package
homepage](https://ropengov.github.io/eurostat/) for more information and
examples.

### Recommended packages

It is recommended to install the `giscoR` package
(<https://dieghernan.github.io/giscoR/>). This is another API package
that provides R tools for Eurostat geographic data to support geospatial
analysis and visualization.

### Contribute

Please make contributions, open issues and pull requests in the main
branch: <https://github.com/ropengov/eurostat/>

### Acknowledgements

**Kindly cite this work** as follows: [Leo
Lahti](https://github.com/antagomir), Przemyslaw Biecek, Markus Kainu
and Janne Huovari. Retrieval and analysis of Eurostat open data with the
eurostat package. [R Journal 9(1):385-392,
2017](https://journal.r-project.org/archive/2017/RJ-2017-019/index.html).
R package version 3.7.5. URL: <https://ropengov.github.io/eurostat/>

We are grateful to all
[contributors](https://github.com/ropengov/eurostat/graphs/contributors),
including Daniel Antal, Joona Lehtomäki, Francois Briatte, and Oliver
Reiter, and for the [Eurostat](https://ec.europa.eu/eurostat/) open data
portal! This project is part of [rOpenGov](http://ropengov.org).

### Disclaimer

This package is in no way officially related to or endorsed by Eurostat.
