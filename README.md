# Customer Support Response Retrieval System

## Overview

This project builds a customer-support response retrieval system that retrieves the most relevant support response for a given customer query.

The system combines:

- TF-IDF lexical similarity
- Multilingual semantic embeddings
- Hybrid similarity scoring
- Confidence-based retrieval
- Golden-set evaluation

## Dataset

The project uses customer-support conversation data containing customer messages and corresponding support responses.

The preprocessing pipeline:

1. Removes duplicate conversation pairs
2. Cleans customer messages
3. Identifies customer-support conversation pairs
4. Removes unsuitable/noisy records
5. Creates training and evaluation data

## Retrieval Approach

### 1. TF-IDF Retrieval

TF-IDF is used to capture lexical similarity between the customer query and historical customer messages.

### 2. Semantic Retrieval

Sentence embeddings are used to capture semantic similarity even when the query and historical message use different wording.

### 3. Hybrid Retrieval

The final retrieval score combines lexical and semantic similarity:

**Hybrid Score = weighted combination of TF-IDF and semantic similarity**

This allows the system to consider both exact terminology and semantic meaning.

## Evaluation

A golden evaluation set was created to assess retrieval quality.

Evaluation artifacts included:

- `golden_set_labeled.csv`
- `golden_evaluation_set.csv`
- `evaluation_results.csv`

The golden set contains 191 examples.

The labeling process was AI-assisted and should therefore be interpreted as an AI-assisted relevance evaluation rather than independent human ground truth.

## Project Structure

```text
customer-support-retrieval/
│
├── customer_support_retrieval.ipynb
├── golden_set_labeled.csv
├── golden_evaluation_set.csv
├── evaluation_results.csv
├── requirements.txt
└── README.md
