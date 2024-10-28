
# Introduction
This document outlines the workflow and methods used for analyzing a gene expression dataset with both supervised and unsupervised machine learning techniques. The analysis aims to classify samples based on gene expression levels and predict patient predisposition to invasive or non-invasive forms of cancer.

The following sections cover the methods for handling missing values, data reduction, clustering, and classification. The code provided can be replicated in R, and instructions for each step are included.

# Project Setup

```{r setup, include=FALSE}
# Load necessary libraries
library(caTools)
library(DMwR2)
library(tidyr)
library(dplyr)
library(MASS)
library(randomForest)
library(e1071)
library(caret)
library(class)
```

## Data Preparation
Load the gene expression dataset and conduct an initial review:

1.Identify and handle missing values.

2.Use k-NN imputation for filling missing entries, as it produced the lowest misclassification error during model testing.

# Load dataset and check dimensions
InitialData <- read.csv("your_dataset.csv")
str(InitialData)

# Handle missing values using k-NN Imputation
InitialData <- knnImputation(InitialData)
}
