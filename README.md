
<!-- README.md is generated from README.Rmd. Please edit that file -->

# criterioncollection R Package

<!-- badges: start -->

[![R-CMD-check](https://github.com/arrismo/CriterionCollection/workflows/R-CMD-check/badge.svg)](https://github.com/arrismo/CriterionCollection/actions)
<!-- badges: end -->

## Overview

The
[`criterioncollection`](https://github.com/arrismo/criterioncollection)
R package is based around a data set of movies included in the Criterion
Collection.

The Criterion Collection is a company dedicated to the restoration and
distribution of films deemed to be important culturally, technically, or
otherwise influential to the medium. Due to this mission, Criterion’s
associations have grown far beyond its primary purpose of distribution.
A film being a part of the Criterion Collection is often seen as a badge
of honor of sorts; the collection is sometimes viewed by cinephiles as a
source of must-watch films.

The goal of this package is thus to make this data for movies widely
seen as important and influential easy to view and analyze.

## Installation

The current version of criterioncollection can be installed from
[GitHub](https://github.com/) with:

``` r
# install.packages("remotes")
remotes::install_github("arrismo/CriterionCollection")
?criterion
```

## Loading and Usage

The current development version of criterioncollection can be used to
access the data. The dataset, criterion, includes columns for
spine_number, year, country, title, and director.

``` r
library(criterioncollection)
View(criterion)
```

You can use the following functions to find films by the director,
spine, or film title. Each function outputs a data frame based on your
input.

``` r
find_by_director("John Woo")
#> [1] "Find_by_director dataframe generated"
#>   spine year   country       title director
#> 8     8 1989 Hong Kong  The Killer John Woo
#> 9     9 1992 Hong Kong Hard Boiled John Woo
find_by_title("Grand Illusion")
#> [1] "Find_by_title dataframe generated"
find_by_spine("1")
#> [1] "Find_by_spine dataframe generated"
find_boxset("Melvin Van Peebles: Essential Films")
#> [1] "Find_boxset dataframe generated"
```

``` r
find_boxset("The Koker Trilogy")
#> [1] "Find_boxset dataframe generated"
```

## References

-   Criterion. *Shop All Films*. The Criterion Collection.
    <https://www.criterion.com/shop/browse/list>.

-   Criterion. *Our Mission*. The Criterion Collection.
    <https://www.criterion.com/about>.

-   Criterion. *Box Sets*. The Criterion Collection.
    <https://www.criterion.com/shop/collection/380-box-sets>
