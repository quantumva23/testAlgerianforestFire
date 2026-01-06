This repository contains a production-oriented machine learning system for predicting forest fire severity using environmental and meteorological data.
The project demonstrates the full ML lifecycle — from data preprocessing and model selection to API-based inference and deployment readiness.

The system is implemented using Flask and exposes a RESTful inference interface, enabling real-time predictions in a web environment.

System Design
Client (Web UI / API Consumer)
        |
        v
Flask REST API
        |
        v
Preprocessing Pipeline
        |
        v
Trained Regression Model


Machine Learning Methodology

Models Implemented
Linear Regression
Lasso Regression (L1 Regularization)
Ridge Regression (L2 Regularization)
RidgeCV (Cross-validated Ridge)

Rationale

Regularization mitigates multicollinearity and reduces overfitting
Cross-validation enables data-driven hyperparameter selection
Comparative analysis ensures model stability on unseen data
The final model was selected based on generalization performance rather than training accuracy.

Data Processing Pipeline

-Data cleaning and validation
-Feature normalization using scaling techniques
-Train–test split for unbiased evaluation
-Model persistence using serialization for reproducible inference


API & Application Layer

Flask-based REST API for real-time predictions
Model and scaler loaded once at startup for efficient inference
Web interface for user interaction and result visualization
This design mirrors industry-grade ML serving patterns.

Evaluation Strategy

Models were evaluated using:
Prediction error metrics
Stability of learned coefficients
Performance on held-out data
Regularized regression models demonstrated improved robustness and generalization over baseline linear regression.

Tech Stack

Languages
Python

Machine Learning
Scikit-learn
NumPy
Pandas

Backend
Flask
REST APIs
Visualization

Matplotlib
Seaborn

Deployment
Vercel (deployment-ready)
Pickle for model serialization
