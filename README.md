# Data-Processing-and-Statistical-Analysis
Python implementation of data preprocessing , outlier handling, visualization and manual statistical analysis.

## Overview

This project demonstrates end-to-end data preprocessing, statistical analysis, and feature selection using Python. The implementation emphasizes manual computation of statistical measures to build a strong foundational understanding of data handling and analysis techniques.

All tasks are implemented using Pandas, NumPy, and Matplotlib only, with no reliance on built-in statistical functions for core calculations.

### Tech Stack

* Python

* Pandas

* NumPy

* Matplotlib

### Dataset  :- 
https://docs.google.com/spreadsheets/d/1I8au5XscPaAG1ToqTRPe-g0EH-7SuRTxxtrzTitwsxU/edit?gid=1569661010#gid=1569661010

The dataset is loaded using Pandas as provided in the starter script.
All preprocessing and analysis steps strictly follow the given script structure to ensure reproducibility and correctness.

## Project Workflow
### 1. Handling Missing Values
   * Identified missing values across all columns.
   
   * Computed the percentage of missing values per feature.
   
   * Imputed missing values in numerical columns using the median.


### 2. Outlier Detection and Treatment
  * Detected outliers in the yield column using the Interquartile Range (IQR) method.
 
  * Calculated lower and upper bounds for outlier detection.
  #### Applied outlier capping:
  * Values below the lower bound were replaced with the lower bound.
  * Values above the upper bound were replaced with the upper bound.


### 3. Data Visualization
  * Created boxplots to visualize the yield distribution:

#### Before outlier treatment
After outlier treatment
  * Implemented a custom histogram function to visualize the distribution of any selected numerical feature.

### 4. Statistical Functions Implemented from Scratch

The following statistical functions were implemented manually, without using built-in NumPy or Pandas statistical utilities:

* manual_variance(column) :- 
Computes variance using the mathematical definition.

* manual_covariance(x, y) :- 
Computes covariance between two numerical features.

* manual_correlation(x, y) :- 
Computes Pearson correlation using the manually calculated covariance and variance.

### 5. Feature Selection

* Computed the correlation matrix for all numerical features using the custom correlation function.

* Identified highly correlated feature pairs (correlation > 0.90).

* Dropped redundant features to reduce multicollinearity.

* Printed the names of all dropped features.



## Final Output

* A fully cleaned and processed DataFrame with:

* Missing values handled

* Outliers treated

* Reduced feature redundancy

* The final DataFrame is printed at the end of the script.
