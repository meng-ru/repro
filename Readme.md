---
title: "Readme"
author: "Meng Ru"
date: "July 24, 2017"
output: 
  md_document:
    variant: markdown_github
---
```{r, echo = FALSE}
knitr::opts_chunk$set(
  collapse = TRUE,
  comment = "#>",
  fig.path = "README-"
)
```

## Research compendium for a report on 'Genetic Signature' 

### Compendium DOI: 

(waiting for updates)

### Author of this repository:

Meng Ru,
Rachel Jia

### Overview of contents

This repository is built for our research on genetic signature. This contains all data, code, and text associated with the final report The `Rmd` file in the  directory contains details of how all the analyses in the report were conducted, as well as instructions on how to rerun the analysis to reproduce the results. The `.csv` file in the directory directory contains all the raw data. 

### The Docker image 

quoted from [benmarwick/mjbtramp](https://github.com/benmarwick/mjbtramp):

> A Docker image is a lightweight GNU/Linux virtual computer that can be run as a piece of software on Windows and OSX (and other Linux systems). To capture the complete computational environment used for this project we have a Dockerfile that specifies how to make the Docker image that we developed this project in. The Docker image includes all of the software dependencies needed to run the code in this project, as well as the R package and other compendium files. To launch the Docker image for this project, first, install Docker](https://docs.docker.com/installation/) on your computer.

At the Docker prompt, enter:

    docker run -dp 8787:8787 menaru/repro

This will start a server instance of RStudio. Then open your web browser at localhost:8787 or or run `docker-machine ip default` in the shell to find the correct IP address, and log in with rstudio/rstudio.

Once logged in, use the Files pane (bottom right) to navigate to `/repro` (the set work directory), open the folder and you'll see the R markdown document. Knit them to produce the results in the paper. More information about using RStudio in Docker is avaiable at the [Rocker](https://github.com/rocker-org) [wiki](https://github.com/rocker-org/rocker/wiki/Using-the-RStudio-image) pages.
 
### Reference
[benmarwick/mjbtramp](https://github.com/benmarwick/mjbtramp)
