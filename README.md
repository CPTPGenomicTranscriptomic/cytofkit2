cytofkit2: an integrated mass cytometry data analysis pipeline
============

**NOTE**: <u>This is the development version of cytofkit2 package</u>

### cytofkit2

This package is designed to facilitate the analysis workflow of mass cytometry data with automatic subset identification and mapping of cellular progression. Both command line and a GUI client are provided for executing the workflow easily.

### Installation

#### 1. Install R and Rstudio

If you have never used R, please install R and Rstudio following the steps below:

- Download the proper R version for your operation system from [R download page](http://cran.stat.nus.edu.sg).

- Double-click the downloaded R installation file, install with all the defaults.

- Download the proper Rstudio version for your operation system from [here](https://www.rstudio.com/products/rstudio/download/).

- Double-click the downloaded Rstudio installation file, install with all the defaults.


<u>**Special Notes for Mac Users**</u>

For Mac OS X 10.8 or later, you need to install XQuartz to support the GUI:

* Download the disk image (dmg) file for [XQuartz](http://xquartz.macosforge.org).

* Open the dmg file by double-clicking on it, you'll find XQuartz.pkg, double-click on it to run the installer, clicking through all the defaults.

* After the installer runs, you'll have to **restart your mac computer**.


#### 2. Install cytofkit2 package

Installation :

``` r
if(!require(devtools)){
  install.packages("devtools") # If not already installed
}
devtools::install_github("CPTPGenomicTranscriptomic/cytofkit2")
```

### Usage

After successfully installing the cytofkit2 package, you can copy/paste the following command lines in a Rstudio console to open the cytofkit GUI:

``` r
library("cytofkit2")
cytofkit_shiny_dashboard()
```
