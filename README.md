# Marketing Attribution

## Overview

This project explores machine learning and deep learning approaches to multi-touch attribution (MTA) in digital marketing.

The analysis focuses on two main objectives:

1. **Conversion Prediction**: Predict whether a customer journey results in a conversion based on its marketing touchpoints.

2. **Marketing Attribution**: Estimate the contribution of individual touchpoints and marketing channels to predicted conversions.

The project combines traditional machine learning, recurrent neural networks, and model-based attribution techniques to analyze sequential customer interactions.

A key focus is the development and comparison of GRU-based neural network architectures, followed by Shapley value-based attribution using a trained Dual-Attention GRU (DAGRU) model.

## Objectives

### 1. Conversion Prediction

Develop and evaluate predictive models that capture relationships between marketing touchpoints and conversion outcomes.

The analysis includes:

- Logistic Regression as a baseline model

- GRU-based neural networks for sequential customer journey modeling

- Investigation of sampling strategies and class imbalance handling

- Hyperparameter optimization and comparison of neural network architectures

- Evaluation using classification metrics, including PR-AUC, ROC-AUC and Log Loss

### 2. Marketing Attribution

Investigate how different attribution methods distribute conversion credits across marketing channels.

The analysis includes:

- Last-Touch Attribution as a rule-based reference

- Shapley Value-based Attribution using a trained Dual-Attention GRU (DAGRU) model

- Comparison of attribution results across methods

The objective is to explore how model-based attribution differs from conventional rule-based approaches.

## Modeling Approach

The project combines traditional machine learning and deep learning to investigate conversion prediction and marketing attribution.

- **Baseline Modeling**: Logistic Regression provides a reference for evaluating the performance of more complex neural network architectures.

- **Sequential Modeling**: GRU-based neural networks are used to capture dependencies between marketing touchpoints within customer journeys.

- **Class Imbalance**: Sampling strategies are investigated using a GRU-based proxy model to address the imbalance between converting and non-converting journeys.

- **Model Optimization**: Different GRU architectures are optimized and compared to evaluate their predictive performance.

- **Model-Based Attribution**: Shapley values are used to estimate touchpoint contributions based on predictions from a trained Dual-Attention GRU model.

## Project Structure

The `notebooks/` directory contains the complete analytical workflow, organized into five stages:

| Notebooks | Description |
|---|---|
| `01–02` | Data preparation and exploratory data analysis |
| `03` | Logistic Regression baseline for conversion prediction |
| `04` | Sampling strategy evaluation using a GRU proxy model |
| `05–07` | GRU architecture development and hyperparameter tuning |
| `08–10` | Training of three GRU-based model architectures |
| `11` | Model evaluation and comparison using PR-AUC, ROC-AUC, and Log Loss |
| `12` | Shapley value-based attribution and marketing channel analysis |

Each notebook documents a specific stage of the modeling and attribution process.
   
## Tech Stack
- Python
- pandas
- NumPy
- scikit-learn
- Keras
- Matplotlib
- Seaborn
- PyTorch
- Google Colab


## Limitations

The attribution analysis estimates contributions to model predictions rather than causal marketing effects.

Shapley attribution relies on a touchpoint-deletion approach. The resulting attribution shares should therefore be interpreted as model-based estimates rather than direct measures of incremental 
