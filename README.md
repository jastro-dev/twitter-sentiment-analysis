# Twitter Sentiment Analysis Project

## Overview

This project implements sentiment analysis on Twitter data to classify tweets into positive, negative, or neutral sentiment categories using natural language processing (NLP) techniques. The project progresses from basic data cleaning through increasingly sophisticated machine learning models.

## Project Structure

The development process is documented chronologically across 5 days:

### Day 1-2: Data Preparation

- Initial project setup and data acquisition
- Comprehensive data cleaning including:
  - Removal of URLs, hashtags, mentions, special characters
  - Stop word filtering
  - Text standardization
- Export of cleaned datasets to CSV files

### Day 3: Exploratory Data Analysis

- Analysis of sentiment label distribution
- Word cloud visualization of common terms
- Tweet length distribution analysis
- Additional data cleaning based on EDA insights
- Identification of class imbalance (more positive samples)

### Day 4: Baseline Model

- Implementation of TF-IDF vectorization
- Logistic Regression baseline model
- Model evaluation using:
  - Accuracy
  - Precision
  - Recall
  - F1 Score
- Model persistence using joblib
- Visualization of classification results

### Day 5: Advanced Models

- Random Forest with GloVe embeddings
- BERT implementation with PyTorch
- GPU acceleration using CUDA
- Comparative analysis through confusion matrices
- Model fine-tuning and hyperparameter optimization

## Key Features

- Text preprocessing pipeline
- Multiple model implementations (Logistic Regression, Random Forest, BERT)
- Evaluation metrics and visualizations
- Handling of imbalanced data
- GPU acceleration for deep learning

## Technical Implementation

- Text processing using Regular Expressions and NLTK
- TF-IDF and GloVe for text vectorization
- PyTorch for BERT implementation
- scikit-learn for traditional ML models
- CUDA support for GPU acceleration

## Results

The project demonstrates the progression from simple to complex models:

- Logistic Regression: Established baseline performance
- Random Forest with GloVe: Improved but struggled with neutral sentiments
- BERT: Best performance, especially for neutral and negative sentiment detection

## Future Improvements

- Grid search for BERT hyperparameter optimization
- Implementation of early stopping
- Enhanced interactive visualizations using Plotly
- Further data balancing techniques
