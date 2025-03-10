# Fine-Tuning BART, GPT-2, T5, and PEGASUS for Text Summarization

## 1. Introduction

Text summarization is a crucial task in Natural Language Processing (NLP) that aims to generate concise and meaningful summaries from long-form text. This project focuses on fine-tuning transformer-based models, including BART, GPT-2, T5, and PEGASUS, using the CNN/DailyMail dataset for abstractive text summarization.

## 2. Objectives

Fine-tune state-of-the-art transformer models for summarization.

Evaluate model performance on a standard benchmark dataset.

Optimize training using Hugging Face's Trainer API.

Compare results across multiple models.

## 3. Dataset

### 3.1 Dataset Overview

The CNN/DailyMail dataset contains news articles and their corresponding summaries. It is widely used for abstractive summarization.

### 3.2 Data Preprocessing

The dataset was loaded using Hugging Face's datasets library.

Text was tokenized using pre-trained tokenizers specific to each model.

Labels were assigned as tokenized versions of reference summaries.

Data was mapped into a format suitable for training.

## 4. Model Selection

The following transformer models were selected for fine-tuning:

BART (facebook/bart-large-cnn)

GPT-2 (gpt2-medium)

T5 (t5-small)

PEGASUS (google/pegasus-xsum)

These models are well-suited for sequence-to-sequence tasks like text summarization.

## 5. Model Fine-Tuning

### 5.1 Training Configuration

Fine-tuning was performed using Hugging Face's Trainer API with the following hyperparameters:

Epochs: 1

Batch size: 4 per device

Gradient accumulation: 16 steps

Evaluation frequency: every 500 steps

Weight decay: 0.01

Logging frequency: every 10 steps

### 5.2 Training Execution

Models were loaded using AutoModelForSeq2SeqLM.

Tokenizers were applied using AutoTokenizer.

Training was conducted using Hugging Face’s Trainer API, optimizing computational efficiency.
