# Data Query and Analysis Process

## Overview
This document outlines the process used in `data_query.ipynb` and `data_analysis.ipynb` files for querying and analyzing a credit card fraud dataset. The process covers setting up a Kaggle API for data download, preprocessing steps including scaling and handling missing values, and applying balancing techniques like SMOTE and RandomUnderSampler.

## Dataset Description
The dataset consists of credit card transactions from European cardholders in September 2013. It includes both normal and fraudulent transactions. The features are mostly numerical, derived from PCA, except for the 'Time' and 'Amount' features.

## Pseudo-Code for Data Query Process

```latex
\documentclass{article}
\usepackage{algorithm}
\usepackage{algpseudocode}

\begin{document}
\begin{algorithm}
\caption{Data Query and Preprocessing for Credit Card Fraud Analysis}\label{alg:data_query}
\begin{algorithmic}

\State Set API credentials and configure Kaggle API environment.
\State Download dataset from Kaggle competition.
\State Unzip the downloaded dataset.
\State Read training and testing datasets into dataframes.

\Function{PreprocessData}{$data$}
    \State Scale 'Amount' feature using RobustScaler.
    \State Drop 'Time', 'id', and 'Amount' columns.
    \State \Return Processed $data$
\EndFunction

\State $train \gets$ \Call{PreprocessData}{train}
\State $test \gets$ \Call{PreprocessData}{test}

\State Check for missing values in $train$.
\State Generate visualizations (KDE plots, box plots, heatmaps) for analysis.

\Comment{Balancing the dataset using SMOTE}
\State Apply SMOTE for oversampling and balance the dataset.
\State Visualize the balanced dataset and its correlation matrix.

\Comment{Balancing the dataset using RandomUnderSampler}
\State Apply RandomUnderSampler for undersampling and balance the dataset.
\State Visualize the balanced dataset and its correlation matrix.

\end{algorithmic}
\end{algorithm}
\end{document}

'''
