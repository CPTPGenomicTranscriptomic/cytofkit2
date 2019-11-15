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
if(!require(reticulate)){
  install.packages("reticulate")
}
if(!require(plotly)){
  install.packages("plotly")
}
if(!require(shinydashboard)){
  install.packages("shinydashboard")
}
if(!require(shinyalert)){
  install.packages("shinyalert")
}
if(!require(shinyWidgets)){
  install.packages("shinyWidgets")
}
if(!require(plyr)){
  install.packages("plyr")
}
if(!require(umap)){
  install.packages("umap")
}
devtools::install_github("CPTPGenomicTranscriptomic/cytofkit2")
```


#### 3. Launch the application

After successfully installing the cytofkit2 package, you can copy/paste the following command lines in a Rstudio console to open the cytofkit GUI:

``` r
library("cytofkit2")
cytofkit_shiny_dashboard()
```
A webpage should be open and looking like this!

![alt text](https://github.com/CPTPGenomicTranscriptomic/cytofkit2/blob/master/cytofkit2_interface.png)


#### 4. Choose your analysis set up

Upload from one to multiple \*.fcs files. The files must have the .fcs extension to appear in the selection browser.

The blue progress bar should move until the message \"upload complete\" appears.

The select your interesting markers.

Update the project name to avoid the overwriting of older results.

As you can upload multiple FCS files these files muste be merge before visualization. Choose between the 4 merge methods:
 * ceil: which samples up to a user specified number of cells without replacement from each FCS file.
 * all: which takes all cells from each FCS file.
 * min: which samples the minimum number of cells among all the selected FCS files from each FCS file.
 * fixed: which samples an user specified number of cells (with replacement when the total number of cell in the file is less than the specified number) from each FCS file.

Choose between the 4 transformation methods:
* cytofAsinh: transformed using either negative value pruned inverse hyperbolic sine transformation
* autoLgcl: automatic logicle transformation.
* Fixedlogicle: fixed logicle transformation.

Submit. Wait for computation.

Save results.

Results visualization analysis.

