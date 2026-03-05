# Market Mix Modelling (MMM) Project

## Overview
This project demonstrates a simplified implementation of **Market Mix Modelling (MMM)** using Python. The objective is to analyze how different marketing channels influence sales to estimate the contribution of each channel to overall business Performance .

Market Mix Modelling is widely used by companies to measure the effectiveness of marketing investments and optimize marketing budget allocation.

#

## Problem Statement
Companies invest heavily in multiple marketing channels such as TV, digital media and radio advertising. However, it is often difficult to determine which channels contribute most to sales.

The goal of this project is to : 

* Understand the relationship between marketing spends and sales.
* Quantify the contribution of each marketing channel.
* Estimate marketing ROI
* Provide insights for marketing budget optimization

#

## DATASET

A *synthetic dataset* was generated to simulate real-world marketing data.

The dataset includes weekly observations of :

* TV advertising spread
* Digital advertising spend
* Radio advertising spend
* Competitor advertising activity
* Product price
* Seasonality
* Sales

Synthetic data was used because real marketing datasets are usually confidential.


## Methodology 
**1. Exploratory Data Analysis (EDA)**

EDA was performed to understand patterns and relationships in the dataset.

Technique used :
* Correlation Heatmap

  ![image](images/heatmap.png)

#

**2.Adstock Transformation**


Advertising effects do not occur only in the current period. Instead, they persist over time and gradually decay.

To capture this carryover effect, **Adstock transformation** was applied to marketing channels.

<img width="618" height="346" alt="image" src="https://github.com/prankush-sharma/MMM-Project/blob/main/images/addstock_output.png" />

#

**3.Regression Modeling**

An **Ordinary Least Square(OLS) regression** model was built to estimate the impact of marketing activities on sales.

* TV advertising(adstock)
* Digital advertising(adstock)
* Radio advertising(adstock)
* Competitor advertising
* Price
* Seasonality

Target variables :
*Sales

<img width="472" height="287" alt="image" src="https://github.com/prankush-sharma/MMM-Project/blob/main/images/regression_coefficient.png" />

#

**4. Multicollinearity Check**

Variance Inflation Factor(VIF) was used to check for multicollinearity among predictors to ensure reliable regression estimates.

<img width="472" height="287" alt="image" src="https://github.com/prankush-sharma/MMM-Project/blob/main/images/vif.png" />

#

**5. Contribution Analysis**
Contribution Analysis was performed to estimate the share of total sales driven by each marketing channel.

This helps identify which channel are most effective in generating demand.

<img width="472" height="400" alt="image" src="https://github.com/prankush-sharma/MMM-Project/blob/main/images/Contribution.png" />

#

**6. Marketing ROI Analysis**

Marketing ROI was calculated to evaluate the efficiency of marketing investments.

ROI helps determine which marketing channels generate the highest return.

<img width="472" height="400" alt="image" src="https://github.com/prankush-sharma/MMM-Project/blob/main/images/ROI.png" />


#

**7.Model Evaluation**

Model Performance was evaluated using :
* R-squared
* Actual vs Predicted Sales Comparison

<img width="472" height="400" alt="image" src="https://github.com/prankush-sharma/MMM-Project/blob/main/images/actual_predicted.png" />


This results show that the model captures a significant poriton of the variation in sales.



## Project Workflow

Data Generation  
↓  
Exploratory Data Analysis  
↓  
Adstock Transformation  
↓  
Regression Modeling  
↓  
Multicollinearity Check (VIF)  
↓  
Contribution Analysis  
↓  
Marketing ROI   
↓  
Model Evaluation


## Future Improvement

* Incorporate real-world marketing datasets.
* Implement marketing budget optimization.
