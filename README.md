<img src="images/title_photo.jpg" style>
<h1 align="center">Predicting Wine Quality From Physical and Chemical Properties</h1>

<br>
<a href="https://nbviewer.org/github/BrianMillerS/wine_quality_classification/blob/main/wine_score_classification.ipynb" target="_blank">Jupyter Notebook Viewer</a>
<br>

## Table of contents
- [Project Overview](#Project-Overview)
- [Description of the Data](#Description-of-the-Data)
- [Methods Overview](#methods-overview)
- [Technologies](#technologies)
- [Project Description](#project-description)
- [Project Results](#project-results)

## Project Overview
Predicting wine quality based on physical and chemical traits using machine learning. We experimented with four models: XGBoost, Random Forest, Logistic Regression, and Naive Bayes. XGBoost outperformed other models due to its superior handling of complex variable interactions and its flexibility in fine-tuning, achieving an accuracy of 0.85 and an F1 Score of 0.86. Interestingy, higher alcohol content is a major indicator of quality, alongside factors like sulphate content and acidity, which contribute significantly to a wine's aroma and flavor.

## Description of the Data
The data was downloaded from <a href="https://archive.ics.uci.edu/dataset/186/wine+quality" target="_blank">UC Irvine’s curated repository</a> of datasets for machine learning. The data consisted of a single table with 1600 rows, each containing data on a specific portuguese red wine variant. Along with the wine’s quality score (the median score from three professional wine tasters) the table also had eleven other columns with measured physicochemical properties.

## Methods Overview
[(Back to top)](#table-of-contents)
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

## Technologies:
[(Back to top)](#table-of-contents)
+ matplotlib
+ seaborn
+ scipy
+ sklearn


## Project Description:
[(Back to top)](#table-of-contents)

This project explores the intriguing question of whether wine quality can be predicted from its physical and chemical properties. Utilizing a dataset that encapsulates various aspects of wine, the analysis delves into understanding what factors contribute to a wine's quality. Through a thorough Exploratory Data Analysis, the project identifies key variables and their relationships. Significant methodologies include ANOVA for feature selection and an extensive model-building phase with Logistic Regression, Naive Bayes, Random Forest, and XGBoost. The project stands out for its meticulous approach to parameter tuning and model evaluation, striving to achieve the most accurate predictions.


<img src="images/variable_distributions.png" style>

<img src="images/data_binning.png" style>

<img src="images/RF_building_a_forest_explained.png" style>

<img src="images/RF_parameter_tuning_explained.png" style>

## Project Results:
[(Back to top)](#table-of-contents)

The results of this project provide insightful conclusions into wine quality prediction. The various models implemented showed differing levels of efficacy, with the Random Forest and XGBoost models standing out for their high accuracy and interpretability. The findings highlight the importance of specific wine properties in determining quality and offer a robust framework for future predictive analysis in the domain. Detailed results include model comparison tables, ROC curves, confusion matrices, and feature importance graphs, underscoring the comprehensive nature of this analysis.

<img src="images/results_summary_table.png" style>

<img src="images/RF_results.png" style>

<img src="images/XGB_results.png" style>

<img src="images/XBG_roc.png" style>
<img src="images/XGB_confusion.png" style>
<img src="images/XGB_correlation.png" style>
<img src="images/XGB_gain.png" style>



