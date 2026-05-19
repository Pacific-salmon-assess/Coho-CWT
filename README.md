# Coho Salmon CWT Release & Recovery Analysis



## Overview

This repository contains data and code for analyzing and visualizing Coho salmon coded-wire tag (CWT) release and recovery data across British Columbia and Alaska.

The dataset includes:

All available CWT releases for Coho salmon from:
Johnstone Strait
Central Coast
North Coast
Haida Gwaii
Skeena
Nass
Alaska regions
All corresponding recoveries of these tagged fish across fisheries and geographic regions

The goal of this project is to explore spatiotemporal patterns in ocean distribution and fishery exploitation of Coho salmon stocks, with a particular focus on data-deficient Central Coast stocks.




# Coho CWT Analysis

This repository contains R scripts for analyzing coho salmon coded-wire tag release and recovery data.

## Data

The data files are too large to store directly on GitHub.

Download the data from this Google Drive folder:

https://drive.google.com/drive/folders/1552FV2cC8LJkCo0L0AC9Tq79C_-I8v2d?usp=drive_link

After downloading the files, place them in a folder called:

data/raw/

## How to run the code

1. Download this GitHub repository.
2. Download the data from the Google Drive link above.
3. Put the data files into `data/raw/`.
4. Open the R script.
5. Run the script in RStudio.





## Data Sources

All data were obtained from the Fisheries and Oceans Canada (DFO) Mark Recovery Program (MRP) Coded Wire Tag (CWT) database.

Queries were conducted with the following criteria:

Species: Coho salmon
PSC Stock groupings:
SKNA (Skeena)
NASS (Nass)
CCST (Central Coast)
NCST (North Coast)
QCIG (Haida Gwaii)
JNSTG (Johnstone Strait)
All Alaska regions
Recovery region: All available regions
Fields requested: All available data columns
Data Extraction

Four separate queries were used to construct the dataset:

Canadian releases – All release data for specified BC regions
Alaska releases – All release data for Alaska regions
Canadian recoveries – All recoveries associated with Canadian releases
Alaska recoveries – All recoveries associated with Alaska releases

All four resulting datasets are included in this repository.

## Objectives

The primary objective of this work is to support the development of a spatiotemporal modeling framework to estimate:

Ocean distribution of Coho salmon stocks
Fishery-specific exploitation rates over time

A key focus is on Central Coast stocks, which are relatively data-limited.

This project aims to determine whether:

Ocean distribution and fishery encounter patterns of Central Coast stocks
Are analogous to better-sampled (“indicator”) stocks from adjacent regions

If strong similarities exist, these indicator stocks may be used as proxies to infer exploitation rates for Central Coast Coho salmon.

## Repository Contents
### Data:
Raw CWT release and recovery datasets derived from DFO MRP queries
Separate files for Canadian and Alaska releases and recoveries


### Code:

R scripts for:

Data cleaning and wrangling
Merging release and recovery datasets
Summarizing encounter and recovery statistics
Generating tables and visualizations
Multivariate analysis (e.g., PCA)


## Methods Summary

The workflow implemented in this repository includes:

### Data Processing:
Filtering and standardizing release and recovery records
Aggregating data by release region, recovery region, and time period
Calculating proportions and encounter rates
### Exploratory Analysis:
Summary statistics of recoveries by fishery and region
Visualization of spatial and temporal patterns in recoveries and removals
### Multivariate Analysis:
Principal Components Analysis (PCA) to evaluate similarity in recovery distributions among stocks
Identification of potential indicator stocks based on shared recovery patterns


## Outputs

The code produces:

Summary tables of release and recovery statistics
Visualizations of spatiotemporal recovery patterns
PCA plots comparing stock-specific recovery distributions

These outputs provide a foundation for evaluating coherence among stocks and identifying candidates for proxy-based inference.

## Future Work

This repository represents the data assembly and exploratory analysis stage of a larger project.

Next steps include:

Development of a spatiotemporal statistical model
Estimation of fishery-specific exploitation rates for Central Coast Coho salmon
Evaluation of uncertainty and model performance


## Notes
CWT data coverage varies across regions and time, which may influence interpretation
Some stock groupings represent aggregated management units rather than individual river systems
