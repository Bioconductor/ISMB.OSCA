# ISMB 2023: Orchestrating Large-Scale Single-Cell Analysis with Bioconductor

[Tutorial homepage](https://bioconductor.github.io/ISMB.OSCA/)

## Speakers

* Dario Righelli, University of Padova, Italy
* Marcel Ramos, CUNY Graduate School of Public Health and Health Policy; and Roswell Park Comprehensive Cancer Center, United States
* Ludwig Geistlinger, Harvard Medical School, United States
* Davide Risso, University of Padova, Italy

## Description

In the last few years, the profiling of a large number of genome-wide features
in individual cells has become routine. Consequently, a plethora of tools for
the analysis of single-cell data has been developed, making it hard to understand
the critical steps in the analysis workflow and the best methods for each objective
of one’s study.

This tutorial aims to provide a solid foundation in using Bioconductor tools
for single-cell RNA-seq analysis by walking through various steps of typical
workflows using example datasets.

This tutorial uses as a "text-book" the online book "Orchestrating Single-Cell
Analysis with Bioconductor"
([OSCA](https://bioconductor.org/books/release/OSCA/)), 
started in 2018 and continuously updated by many contributors from the Bioconductor
community. Like the book, this tutorial strives to be of interest to the
experimental biologists wanting to analyze their data and to the bioinformaticians
approaching single-cell data.

## Learning objectives

Attendees will learn how to analyze multi-condition single-cell RNA-seq from
raw data to statistical analyses and result interpretation. Students will learn
where the critical steps and methods choices are and will be able to leverage
large-data resources to analyze datasets comprising millions of cells.

In particular, participants will learn:

* How to access publicly available data, such as those from the Human Cell Atlas.
* How to perform data exploration, normalization, and dimensionality reduction.
* How to identify cell types/states and marker genes.
* How to correct for batch effects and integrate multiple samples.
* How to perform differential expression and differential abundance analysis between conditions.
* How to work with large out-of-memory datasets.

## Time outline

| Activity                     | Time |
|------------------------------|------|
| Introduction and Setup                                          | 9:00-9:30    |
| Introduction to Bioconductor and the SingleCellExperiment class | 9:30-10:00   |
| Exploratory Data Analysis and Quality Control (EDA/QC)          | 10:00-10:45  |
| Coffee break                                                    | 10:45-11:00  |
| Clustering and cell type annotation                             | 11:00-12:00  |
| Multi-sample analyses                                           | 12:00-13:00  |
| Lunch break                                                     | 13:00-14:00  |
| Working with large data                                         | 14:00-15:00  |
| Accessing the Human Cell Atlas (HCA) Data from R/Bioconductor   | 15:00-16:00  |
| Coffee break                                                    | 16:00-16:15  |
| Case study: from data import to DE and DA                       | 16:15-17:00  |
| Case study: discussion                                          | 17:00-18:00  |

## Docker container

To run this tutorial in a
[Docker container](ghcr.io/bioconductor/ismb.osca:latest),
pull the Docker image via

```
docker pull ghcr.io/bioconductor/ismb.osca:latest
``` 

and then run the image via

```
docker run -e PASSWORD=bioc -p 8787:8787 ghcr.io/bioconductor/ismb.osca
```

Once running, navigate to http://localhost:8787/ in your browser and login with
username `rstudio` and password `bioc`.

## Local installation

This tutorial can be installed like an ordinary R package via:

```
if (!require("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

if (!require("remotes", quietly = TRUE))
    install.packages("remotes")

BiocManager::install("Bioconductor/ISMB.OSCA",
                     dependencies = TRUE,
                     build_vignettes = TRUE)
```
