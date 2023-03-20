# das-fiberoptic

## Description

Distributed Acoustic Sensing (DAS) is a technology that enables continuous, real-time measurements along the entire length of a fiber optic cable. When there are acoustic disturbances in the ocean, strain is produced along the cable which creates patterns in time and distance dimensions that differ based on the source of the disturbance. Our goal is to identify all instances of fin whale vocalizations, cluster them together, and visualize these results to identify patterns in the behavioral. 

## Configuration

1. Create the conda environment using the `environment.yml` file provided and activate it:

   ```{bash}
   > conda env create -f ooi_dev.yml
   > conda activate ooi-dev

   ```

2. Configure module discovery using the `setup.py` file (this will help us find modules written in sub-diretories):

   ```{bash}
   pip install -e .
   ```

## Project Usage Guide

Based on the questions that you are looking to answer, there are different ways of accessing and utilizing the code. We provide some insight into the use cases for the various Notebooks below:

- **Note:**
  - Notebooks labelled (a) use full length of the cable in each input image
  - Notebooks labelled (b) and (c) use chunked cable images (10 chunks over the entire cable) with (b) using latent embedding size as 16 and (c) using embedding size as 32 in the autoencoder notebooks.
  - We have completed the project right till GMM clustering for (b). The (a) and (c) notebooks are retained in the repository in case any further work is desired to be done on different data and embedding sizes.

If you are interested in the patterns of Fin Whale vocalizations in the chunked November 2021 data set:

- `05_b_Heatmap Visualization.ipynb` contains code to display a heat map over distance and time domain of the data for embedding length 16 of chunked data over the distance dimension

If you are interested in visualizing the clusters of the data:

- `04_b_GMM Clustering Full Dataset 16 Embedded.ipynb` creates and visualizes the clusters for the entire data with the cable length broken into 10 chunks and a latent embedding size of 16.
- Note the comments in the code and follow their instructions based on whether you desire to load in current clustering results or create your own.

 If you are interested in training the Autoencoder:
 
 - `03_b_PyTorch Autoencoder Training- all data distance chunked - embedding 16.ipynb` has code to train the Autoencoder model whose embedded layer is the basis for our clustering algorithm

 If you are interested in clustering and training an Autoencoder:

- `02_b_Data Acquisition - cable length chunked.ipynb` has code to pull and prepare a dataset from Azure
- `02_Data Acquisition and Processing - from piweb.ipynb` has code to pull and process data from the piweb website which was given to us before azure acces

 Finally,

- 01_Data Processing Exploration.ipynb contains some data exploration code

## Acknowledgements

We want to thank Dr Shima Abadi, Dr William Wilcock and John Ragland from the Ocean Data Lab for their guidance and support throughout the project, and Dr Megan Hazen and the MSDS staff for facilitating this venture.
