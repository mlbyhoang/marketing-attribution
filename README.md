# Multi-touch Attribution

## Overview

This project explores machine learning and deep learning approaches to multi-touch attribution (MTA) in digital marketing.

The analysis focuses on two main objectives:

1. **Conversion Prediction**: Predict whether a customer journey results in a conversion based on its marketing touchpoints.

2. **Marketing Attribution**: Estimate the contribution of individual touchpoints and marketing channels to predicted conversions.

The project combines traditional machine learning, recurrent neural networks, and model-based attribution techniques to analyze sequential customer interactions.

## Objectives

### 1. Conversion Prediction

Develop and evaluate predictive models that capture relationships between marketing touchpoints and conversion outcomes.

The analysis includes:

Logistic Regression as a baseline model

GRU-based neural networks for sequential customer journey modeling

Hyperparameter tuning and model comparison

Evaluation using classification metrics, including PR-AUC and ROC-AUC

### 2. Marketing Attribution

Investigate how different attribution methods distribute conversion credits across marketing channels.

The analysis includes:

First-Touch Attribution

Last-Touch Attribution

Linear Attribution

Shapley Value-based Attribution using a trained Dual-Attention GRU (DAGRU) model

Comparison of attribution results across methods

Methodology

The project follows a structured analytical workflow:

Data Preparation: Preprocessing and encoding customer journey sequences and touchpoint features.

Exploratory Data Analysis: Examining conversion patterns and customer journey characteristics.

Baseline Modeling: Establishing a reference using Logistic Regression.

Deep Learning: Developing GRU-based models to capture sequential dependencies.

Model Optimization: Tuning model configurations and evaluating alternative architectures.

Model Evaluation: Comparing predictive performance across models.

Shapley Attribution: Estimating model-based touchpoint contributions and aggregating them by marketing channel.

## Tech Stack
- Python
- Pandas
- NumPy
- scikit-learn
- Jupyter Lab
- matplotlib
- searborn
- pytorch

## Project Structure

The notebooks/ directory contains the individual stages of the analysis, from data preparation and exploratory analysis to model development, evaluation, and attribution.

## Limitations

The attribution analysis estimates contributions to model predictions rather than causal marketing effects.

Shapley attribution relies on a touchpoint-deletion approach. The resulting attribution shares should therefore be interpreted as model-based estimates rather than direct measures of incremental 
