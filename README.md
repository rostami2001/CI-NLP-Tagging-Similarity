# CI-NLP-Tagging-Similarity

This project was completed as part of the **Computational Intelligence** course during the Winter of 2024 at Ferdowsi University of Mashhad.

## Overview

The goal of this project is to design and implement a system that uses Natural Language Processing (NLP) techniques to:
- Preprocess textual data from Stack Overflow questions
- Generate semantic embeddings using Word2Vec
- Retrieve similar questions based on semantic similarity
- Automatically predict tags for new questions using a K-Nearest Neighbors (KNN) model

## Dataset

The dataset consists of 60,000 Stack Overflow questions, split into:
- **Training set**: Used to train the Word2Vec and KNN models
- **Validation set**: Used for evaluation

Columns include:
- `Title`: Question title
- `Body`: Full question content (HTML cleaned)
- `Tags`: Topic tags for the question

## Implementation

### Phase 1: Preprocessing
- Clean HTML tags, numbers, and punctuation
- Remove stopwords and lemmatize tokens
- Save cleaned data for later use

### Phase 2: Word2Vec & Similarity Retrieval
- Train a Word2Vec model on tokenized titles and bodies
- Visualize word and document vectors in 3D using PCA
- Retrieve similar questions for a given query using cosine similarity

### Phase 3: Tagging
- Preprocess validation data
- Train a KNN model on semantic vectors of training data
- Predict tags for validation questions based on nearest neighbors
- Evaluate accuracy based on overlap with true tags

## Results

- Word2Vec embeddings successfully captured semantic relationships between words
- Document clustering showed meaningful groupings of similar questions
- The KNN tag prediction model achieved **82% accuracy** in predicting at least one correct tag per question

## Files

- `project_5.py`: Main Python script
- `project5.pdf`: Project description (Persian)
- `document-5.pdf`: Project report (Persian)
