---
title: "README for Gene Expression Statistical Analysis Project"
author: "Rishwanth Mithra"
date: "`r Sys.Date()`"
output: github_document
---

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
