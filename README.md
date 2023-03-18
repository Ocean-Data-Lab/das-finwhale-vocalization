# das-fiberoptic

## Description
Distributed Acoustic Sensing (DAS) is a technology that enables continuous, real-time measurements along the entire length of a fiber optic cable. When there are acoustic disturbances in the ocean, strain is produced along the cable which creates patterns in time and distance dimensions that differ based on the source of the disturbance. Our goal is to identify all instances of fin whale vocalizations, cluster them together, and visualize these results to identify patterns in the behavioral. 

## Configuration

1. Create the conda environment using the `environment.yml` file provided and activate it:

   ```{bash}
   > conda env create -f environemt.yml
   > conda activate das-fiberoptic

   ```

2. Configure module discovery using the `setup.py` file (this will help us find modules written in sub-diretories):

   ```{bash}
   pip install -e .
   ```

## Project Usage Guide

Based on the questions that you are looking to answer, there are different ways of accessing and utilizing the code. We provide some insight into the use cases for the various Notebooks below:

If you are interested in the patterns of Fin Whale vocalizations in the original November 2021 data set:
- 06_Heatmap Visualization.ipynb contains code to display a heat map over distance and time domain of the data.

If you are interested in visualizing the clusters of the data:
 - 05_GMM Clustering.ipynb creates and visualizes the clusters. Note the comments in the code and follow their instructions based on whether you desire to load in current clustering results or create your own.

 If you are interested in training the Autoencoder:
 - 04_PyTorch Autoencoder.ipynb has code to train the Autoencoder model whose embedded layer is the basis for our clustering algorithm.

 If you are interested in clustering and training an Autoencoder:
 - 03_2_Prepare_dataset_Azure has code to pull and prepare a dataset from Azure.
 - 03_Data Acquisition and Processing.ipynb contains code to acquire and prepare local data.

 Finally,
- 00_hunter_eda_optasense.ipynb and 01_Data Processing Exploration.ipynb contains some data exploration code.

## Acknowledgements
We want to thank Dr Shima Abadi, Dr William Wilcock and John Ragland from the Ocean Data Lab for their guidance and support throughout the project, and Dr Megan Hazen and the MSDS staff for facilitating this venture.
