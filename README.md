LLM-Enabled Instagram Fake Account Detection (Bot / Scam / Spam)

An end-to-end multi-class classification pipeline that combines semantic embeddings from Instagram bios with structured profile metadata to detect and categorize accounts into Bot, Scam, and Spam.
The project focuses on strong ML fundamentals: clean preprocessing, reproducible evaluation, and robust model selection with ensemble learning.

Project Overview

Social media profiles contain both:

Unstructured signals (bio text, self-description patterns)

Structured signals (followers/following counts, post stats, account attributes)

This project fuses both signal types:

Extracts bio embeddings using an LLM/embedding model

Engineers/cleans structured features

Trains and evaluates multiple ML models

Selects a best-performing ensemble (stacking)

Key Features

Feature fusion: structured metadata + high-dimensional bio embeddings

Preprocessing pipeline:

missing value handling (mean/median imputation)

categorical encoding

z-score scaling for numeric features

Model benchmarking:

Logistic Regression

SVM (RBF)

Random Forest

XGBoost

Ensembles:

hard voting

soft voting

stacking (best-performing)

Reproducible evaluation:

stratified train/test split (80/20)

stratified k-fold cross-validation

metrics: Accuracy + ROC-AUC (one-vs-rest)

Results (Summary)

Best model: Tuned stacking ensemble

Test Accuracy: 98.41%

Strong ROC-AUC for top models (AUC > 0.98)

Note: Results depend on dataset composition and labeling quality. Always validate on a holdout set and check class-wise performance.

Tech Stack

Python

scikit-learn

XGBoost

Embedding model (LLM-based or sentence embedding model)

pandas, numpy
