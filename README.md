Bias Reduction in Word Embeddings

A practical NLP project that demonstrates how gender bias emerges in word embeddings and how it can be measured, analyzed, and mitigated using vector space operations.
The implementation uses pre-trained GloVe embeddings and follows debiasing principles introduced in the DeepLearning.AI Natural Language Processing curriculum.

Features

Cosine Similarity Analysis

Measure semantic similarity between word vectors

Word Analogy Resolution

Solve analogies using vector arithmetic

Bias Direction Construction

Identify gender bias axes in embedding space

Neutralization

Remove gender bias from gender-neutral words

Equalization

Balance gendered word pairs symmetrically

Quantitative Bias Evaluation

Compare bias scores before and after debiasing

Dataset
GloVe Word Embeddings

File: glove.6B.50d.txt

Description:
Pre-trained 50-dimensional word vectors trained on 6 billion tokens from Wikipedia and Gigaword.

Usage:
Loaded into a word_to_vec_map dictionary for fast vector lookup.

