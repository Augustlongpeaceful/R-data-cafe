README
================
Marc A.T. Teunis
12/4/2019

This tutorial is about creating R-packages. It adheres to the so-called
“Start with Rmd” principle, where you gradually build your analysis in
an RMarkdown file and from there develop an R-package.

The full tutorial is available as `start_with_rmd.pdf` and
`start_with_rmd.Rmd` file inside the folder `./Rmd`

## Contents

1.  Writing functions
2.  “Start with Rmd” - What is it?
3.  Function documentation - `{roxygen2}`
4.  Demo - Building a package `{usethis}`, `{devtools}`

## Prerequisites

  - Windows: Install
    [Rtools](https://cran.r-project.org/bin/windows/Rtools/)
  - Clone Materials from:
    <https://github.com/UtrechtUniversity/R-data-cafe/start_with_rmd>
  - Install packages:

<!-- end list -->

``` r
library(tidyverse)
library(here)
library(usethis)
library(devtools)
```

## Online references

  - <https://emilyriederer.netlify.com/post/rmarkdown-driven-development/>
  - <https://github.com/jennybc/pkg-dev-tutorial>
  - <https://r4ds.had.co.nz/>
  - <http://r-pkgs.had.co.nz/>

\#\# Good functions

  - Do one thing good
  - Have no ‘side-effects’
  - `class(input) = class(output)` (to make the function ‘pipe-able’)

## Function documentation: We could do

``` r
## A function that replaces a string or number to a 
## formal NA (missing value)
## this function takes a R-vector object x as 
## argument and returns a mutated vector in which 
## the indicated string or number is replaced with a 
## formal missing value

# <function definition goes here>
```

BUT: Roxygen rules\!

## ‘Many’ functions?

1.  When you find yourself writing many functions in an Rmd file like
    this
2.  It is time to start building an R-packge.

\#\# Common workflow
