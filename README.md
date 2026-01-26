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

bias-reduction-word-embeddings/
├── README.md
├── debias_embeddings.py
├── utils.py
├── glove.6B.50d.txt
├── requirements.txt
└── examples/
    └── demo.ipynb


## Key Takeaways

- Word embeddings encode implicit societal biases  
- Bias can be quantified using vector projections  
- Neutralization reduces bias for gender-neutral terms  
- Equalization enforces fairness between gendered pairs  
- Ethical NLP systems require explicit bias mitigation strategies

## Dependencies

### Requirements
- Python 3.7+
- NumPy

---

## Usage

1. Download `glove.6B.50d.txt`
2. Place it in the project root directory
3. Run the script or notebook:

## Limitations

- Only addresses binary gender bias  
- Uses static embeddings (GloVe)  
- Does not handle contextual embeddings (e.g., BERT)  
- Debiasing is applied at the embedding level only  

---

## Future Work

- Extend to intersectional bias  
- Apply methods to contextual embeddings  
- Evaluate fairness on downstream NLP tasks  
- Visualize embedding space before and after debiasing  

---

## License

This project is intended for **educational and research purposes**.  
Free to use and modify with proper attribution.
