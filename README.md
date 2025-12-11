# Food Insecurity Assessment in Kenya Using SatCLIP Embeddings

## Overview

This project applies a geospatial foundation model, SatCLIP, to examine patterns of food insecurity in Kenya using spatial embeddings derived from satellite observations. The analysis integrates SatCLIP’s location encoder with the Integrated Food Security Phase Classification (IPC) dataset to explore how learned geospatial representations relate to acute food insecurity conditions across counties and sub-counties.

## SatCLIP Foundation Model

SatCLIP is a self-supervised geospatial foundation model trained on globally distributed satellite imagery paired with geolocation information. Through contrastive learning, the model learns a latent representation that captures environmental structure, land cover characteristics, and spatial context without requiring labelled data.  
The location encoder produces a fixed-length embedding vector for any geographic coordinate, enabling downstream tasks such as clustering, similarity assessment, or supervised prediction.

In this project, SatCLIP embeddings are generated for administrative units and for a spatial grid covering Kenya, providing a continuous representation of environmental conditions relevant to food security dynamics.

## IPC Phase Data

The Integrated Food Security Phase Classification (IPC) provides a standardized global framework for assessing the severity of acute food insecurity. Each geographic unit is assigned proportions of the population in IPC Phases 1–5, where higher phases represent crisis, emergency, or famine-level conditions.  
IPC data therefore offers a clinically validated, interpretable target variable for assessing vulnerability and modelling food insecurity.

In this analysis, two forms of IPC-derived information are used:

- **Binary crisis indicator (IPC3+):** distinguishing crisis-and-above conditions.  
- **Continuous severity index:** derived from the distribution of population across IPC phases.

These indicators enable both categorical and continuous assessment of food insecurity.

## Integration of SatCLIP and IPC

The study leverages SatCLIP embeddings as spatial predictors of IPC outcomes. The workflow consists of:

1. Generating embeddings for IPC centroids to represent each administrative unit in latent space.  
2. Expanding embeddings to a national grid to obtain spatially dense environmental representations.  
3. Examining similarity among regions using cosine similarity of embeddings.  
4. Relating embeddings to IPC crisis conditions and severity values for exploratory and predictive analysis.

The underlying assumption is that geospatial structure captured by SatCLIP—such as climate regime, land cover patterns, vegetation condition, and terrain context—correlates with structural drivers of food insecurity.  

## Aim of the Analysis

The goal is not to reproduce operational IPC assessments but to evaluate the potential of geospatial foundation models for:

- Characterising the spatial distribution of food insecurity  
- Highlighting similarities and differences between counties  
- Supporting early-warning and vulnerability mapping  
- Providing fine-scale spatial inference beyond administrative boundaries  

This work demonstrates how foundation models can complement traditional food security analysis by enabling scalable, spatially explicit modelling where ground-based data is limited.

## Author

Mary Muthee  
Copernicus Master in Digital Earth  

