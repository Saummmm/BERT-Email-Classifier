# BERT Email Classifier

A BERT-based multi-class email classification system that automatically organizes incoming emails into semantic categories such as **Work**, **Promotions**, **Social/Blog**, and **School**. This project demonstrates the effectiveness of fine-tuning a transformer-based NLP model for real-world email management tasks.

---

## Overview

Email inboxes quickly become cluttered when messages from different contexts (work, school, promotions, social updates) are mixed together. While existing email providers offer basic filtering, they often rely heavily on sender metadata and rigid category definitions.

This project implements a **content-based email classification system** using **Bidirectional Encoder Representations from Transformers (BERT)**. The model analyzes the semantic context of each email and assigns it to the most appropriate category, enabling a cleaner, more organized inbox.

The system achieves an **overall F1 score of 0.992**, outperforming traditional machine-learning baselines such as Naive Bayes and Support Vector Machines :contentReference[oaicite:1]{index=1}.

---

## Key Features

- Multi-class email classification using BERT
- Content-based classification (not dependent on sender metadata)
- High accuracy across multiple real-world email categories
- End-to-end training, evaluation, and inference implemented in a Jupyter Notebook
- Comparison with traditional ML classifiers (Naive Bayes, SVM)

---

## Dataset

The model was trained and evaluated using a **combined dataset of 7,668 real emails**, collected from a team member’s inbox and external sources :contentReference[oaicite:2]{index=2}.

### Included Datasets

- **`current.csv`**
  - University emails (Western University)
  - External blog-style emails
- **`emailsPromo.csv`**
  - Promotional emails (discounts, offers, newsletters)
- **`emailsWork.csv`**
  - Job search and professional emails (LinkedIn, Indeed, Glassdoor)

The dataset is slightly imbalanced, with *Work* emails forming the largest class and *Blog/Personal* emails forming the smallest.

---

## Repository Structure
- **`index.ipynb`** — Main notebook containing the full pipeline:
  - data preprocessing
  - tokenization
  - BERT fine-tuning
  - evaluation
  - inference
- **`CS 4442B - Final Project Report.pdf`** — Detailed methodology, experiments, and analysis.
- **CSV files** — Training and evaluation datasets.

---

## Methodology

- **Model**: BERT (fine-tuned for sequence classification)
- **Task**: Multi-class email classification
- **Evaluation Metrics**:
  - Accuracy
  - Precision
  - Recall
  - F1 Score

BERT was selected due to its strong performance in contextual language understanding and sequence classification tasks. The model was fine-tuned on labeled email data over multiple epochs to optimize classification performance :contentReference[oaicite:3]{index=3}.

---

## Results

### Training Performance

- **Final training F1 score**: 0.992
- **Final training loss**: 0.0453

### Test Accuracy by Class

| Email Category | Accuracy |
|----------------|----------|
| School         | 100.0%   |
| Work           | 99.5%    |
| Promotions     | 97.8%    |
| Blog / Social  | 99.4%    |

### Model Comparison

| Model         | Accuracy |
|---------------|----------|
| SVM           | 0.976    |
| Naive Bayes  | 0.989    |
| **BERT**      | **0.992** |

BERT outperformed both traditional classifiers, demonstrating superior feature extraction and contextual understanding for email content :contentReference[oaicite:4]{index=4}.

---

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/Saummmm/BERT-Email-Classifier.git
   cd BERT-Email-Classifier
