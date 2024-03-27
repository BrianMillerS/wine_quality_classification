<img src="images/title_photo.jpg" style>
<h1 align="center">Predicting Wine Quality From Physical and Chemical Properties</h1>

<br>
<a href="https://nbviewer.org/github/BrianMillerS/wine_quality_classification/blob/main/wine_score_classification.ipynb" target="_blank">Jupyter Notebook Viewer</a>
<br>

# Table of contents
- [Project Overview](#Project-Overview)
- [Description of the Data](#Description-of-the-Data)
- [Methods Overview](#methods-overview)
- [Project Summary](#project-summary)

# Project Overview
Predicting wine quality based on physical and chemical traits using machine learning. I experimented with four models: XGBoost, Random Forest, Logistic Regression, and Naive Bayes. XGBoost outperformed other models due to its superior handling of complex variable interactions and its flexibility in fine-tuning, achieving an accuracy of 0.85 and an F1 Score of 0.86. Interestingy, higher alcohol content is a major indicator of quality, alongside factors like sulphate content and acidity, which contribute significantly to a wine's aroma and flavor.

<img src="images/results_summary_table.png" width="532" height="225">

# Description of the Data
The data was downloaded from <a href="https://archive.ics.uci.edu/dataset/186/wine+quality" target="_blank">UC Irvine’s curated repository</a> of datasets for machine learning. The data consisted of a single table with 1600 rows, each containing data on a specific portuguese red wine variant. Along with the wine’s quality score (the median score from three professional wine tasters) the table also had eleven other columns with measured physicochemical properties.

# Methods Overview
+ Exploratory Data Analysis
  + Checking Data Quality
  + ANOVA for Variable Selection
+ Model Building
  + Logistic Regression
  + Naive Bayes
  + Random Forest
  + XGBoost
+ Model Parameter Tuning
  + Grid Search
  + Iterative Randomized Search
+ Model Evaluation
  + Accuracy
  + F1 Score
  + ROC Curve/ Confusion Matrix
  + Identifying the Most Important Variables for Wine Quality Prediction

# Project Summary
- [Exploratory Data Analysis](#Exploratory-Data-Analysis)
- [Model Building](Model-Building)
- [How Random Forests Work](#How-Random-Forests-Work)
- [Model Parameter Tuning](Model-Parameter-Tuning)
- [Model Evaluation](Model-Evaluation)

<br>  
## Exploratory Data Analysis  
First lets take a look at all of the data in our dataset.   
We have:  
  - 11 prdictor variables  
  - 1 outcome variable (quality)  
<img src="images/variable_distributions.png" style>  
<br>

In order to make this classificaiton problem a little easier we will be binning wines into 'good' and 'bad' as follows:
<br>
<img src="images/data_binning.png" style>
<br>

## Model Building
  - In order to train our models, the data was split into 80% training/ 20% testing
  - Using the default models from Tensorflow here were the results:
<br>
<img src="images/results_summary_table.png" width="532" height="225">
<br>
From this point on in the analyis, we will focus on the two top performing models: Random Forests, and XGBoost

## How Random Forests Work
Given the inter-dependencies of the predictor variables, using tree-based methods might yield the best results. Random Forests and other more comlpex models like XGBoost can leverage the indirect correlations to the outcome variable, enhancing the models performance. 
<br>
<img src="images/RF_building_a_forest_explained.png" style>
<br>

Once a Random Forest is created, there are a few model parameters to keep in mind that we can tweek to improve it's performance.
<br>
<img src="images/RF_parameter_tuning_explained.png" style>
<br>

## Model Parameter Tuning
RF and XGBoost performed the best, let's take both models, tune them, and see if we can improve them further
<br>
A GridSearch was performed on the RF model, this approach is more time and resource intensive, but it is exhaustive, so we will know that we will be getting the bets result. 
<br>
<img src="images/RF_results.png" style>
<br>

<br>
<img src="images/XGB_results.png" style>
<br>

## Model Evaluation

<img src="images/XBG_roc.png" style>
<br>

<img src="images/XGB_confusion.png" style>
<img src="images/XGB_correlation.png" style>
<img src="images/XGB_gain.png" style>



