# Facebook Social Network Analysis: Network Recommendation System

## Overview

This project explores the "Facebook Users" dataset to gain insights into social media network behavior. By analyzing patterns and properties of the graph network, we developed a network recommendation system that can predict and suggest potential connections between users.

## Background

With approximately 3 billion monthly active users, Facebook serves as a crucial hub for information sharing worldwide. This project analyzes the complex networks formed by users' connections to understand social preferences and information flow, ultimately building a recommendation system for new connections.

## Dataset
The "Facebook Users" dataset is an anonymized directed social graph containing almost 2 million nodes and over 9 million edges. Due to computational limitations, we performed random walk sampling to reduce the dataset to 50,000 nodes and 241,276 edges while preserving the original graph's properties.

## Key Objectives

- Understand the graph properties of a social network
-  Determine if the network exhibits small-world characteristics
-   Design a link prediction model that recommends connections between users

## Dependencies
- networkx
- pandas
- numpy
- matplotlib
- math
- random
- seaborn
- sklearn
- scipy

## Methodology
### Data Preprocessing

- Data Sampling: Random walk sampling to reduce computational load while preserving network properties
-  Labelling: Created balanced dataset with existing edges (1) and non-existing edges (0)
- Feature Engineering: Constructed features including:
  - Shortest Path
  - Follow Back
  - Preferential Attachment
  - Cosine Similarity
  - Jaccard Similarity
  - Eigenvector Centrality
  - PageRank
  - Hyperlink-Induced Topic Search (HITS)
  - Resource Allocation Index
  - Link Weight
- Dimension Reduction: Applied PCA to reduce 22 predictors to 15 dimensions

### Link Prediction Models
We implemented and compared three classification models using the predictors derived from PCA:

- Support Vector Machine (SVM)
- Random Forest (RF)
- K-Nearest Neighbors (KNN)

## Link Prediction Results

- Random Forest: Best performer with 98.34% accuracy, 99.44% specificity, and 97.24% sensitivity
- KNN: 95.77% accuracy, 99.39% specificity, and 92.14% sensitivity
- SVM: 91.20% accuracy, 99.54% specificity, and 82.83% sensitivity

## Network Properties

- The network follows power law distribution for both in-degree and out-degree
- Verified small-world properties with higher clustering coefficient (0.2) compared to random networks (0.05)
- Average shortest path length (7.47) significantly lower than random networks (79.81)

## Limitations

- Dataset lacks demographic and user interest information
- Sampling may lose information from the original network
- Potential collinearity between network property features

## Future Work

- Expand the model with additional user information (demographics, interests)
- Explore additional classification models (XGBoost, Logistic Regression)
- Implement RFECV (Recursive Feature Elimination with Cross Validation) for feature selection

## Contributors

- Xavier Felixan MIJAATA (57195713)
- Jawad MAHMUD (57274243)
- Pongamorn TRAKARNKULPHUN (57587131)

## Acknowledgements

City University of Hong Kong

SDSC3016: Social Network Analysis

Prof. KE Qing
