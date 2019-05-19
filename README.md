# RCIT and RCoT
This is an R package implementing the Randomized Conditional Independence Test (RCIT) and the Randomized conditional Correlation Test (RCoT). As a general rule, RCoT is superior to RCIT for conditional independence testing.

The academic article describing RCIT and RCoT in detail can be found [here](https://www.degruyter.com/view/j/jci.ahead-of-print/jci-2018-0017/jci-2018-0017.xml?format=INT). Please cite the article if you use any of the code in this repository.

# Installation

The package depends on the MASS and momentchi2 packages on CRAN, so please install these first. Then:

> library(devtools)

> install_github("ericstrobl/RCIT")

> library(RCIT)

> RCIT(rnorm(1000),rnorm(1000),rnorm(1000))

> RCoT(rnorm(1000),rnorm(1000),rnorm(1000))

> RCoT(rnorm(1000),rnorm(1000),matrix(rnorm(2000),1000,2)) # matrices for more than two variables

