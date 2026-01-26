# Bias Reduction in Word Embeddings

A practical NLP project that demonstrates how **gender bias emerges in word embeddings** and how it can be **measured and mitigated** using vector space operations.  
The implementation uses **pre-trained GloVe embeddings** and follows debiasing principles introduced in the **DeepLearning.AI Natural Language Processing curriculum**.

---

## Features

- Cosine similarity computation between word vectors
- Word analogy completion using vector arithmetic
- Gender bias direction construction
- Neutralization of gender-neutral words
- Equalization of gendered word pairs
- Quantitative comparison before and after debiasing

---

## Dataset

### GloVe Word Embeddings

- **File:** `glove.6B.50d.txt`
- **Description:**  
  Pre-trained 50-dimensional word vectors trained on 6 billion tokens from Wikipedia and Gigaword.
- **Usage:**  
  Loaded into a `word_to_vec_map` dictionary for fast vector lookup.

---

## Project Structure


Description:
Pre-trained 50-dimensional word vectors trained on 6 billion tokens from Wikipedia and Gigaword.

Usage:
Loaded into a word_to_vec_map dictionary for fast vector lookup.

