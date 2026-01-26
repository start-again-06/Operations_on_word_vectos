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

## System Design

The system is designed as a **modular NLP pipeline** that analyzes and mitigates gender bias in static word embeddings.  
Each component is responsible for a well-defined stage of the debiasing process, enabling clarity, extensibility, and reproducibility.

---

### High-Level Architecture
([https://github.com/start-again-06/Operations_on_word_vectos/blob/main/High%20Level%20Architecture](url))


### Component Breakdown

#### 1. Embedding Loader
- Loads pre-trained GloVe vectors into memory
- Maps words to fixed-length dense vectors
- Acts as the foundational representation layer

**File:** `debias_embeddings.py`

---

#### 2. Similarity Engine
- Computes cosine similarity between word vectors
- Enables semantic comparison and analogy reasoning

**Functions:**
- `cosine_similarity()`
- `complete_analogy()`

**File:** `utils.py`

---

#### 3. Bias Analyzer
- Constructs a **gender bias direction vector**
- Projects word vectors onto the bias axis
- Quantifies alignment with societal gender bias

**Example:**

#### 4. Debiasing Module

##### Neutralization
- Removes gender components from gender-neutral words
- Ensures embeddings are orthogonal to the bias axis

##### Equalization
- Forces gendered word pairs to be symmetrically positioned
- Preserves semantics while enforcing fairness

**File:** `debias_embeddings.py`

---

#### 5. Evaluation Layer
- Measures cosine similarity before and after debiasing
- Validates effectiveness of bias mitigation techniques
- Outputs numerical bias reduction metrics

---

### Design Principles

- **Modularity:** Each component can be extended or replaced independently
- **Transparency:** All bias operations are mathematically interpretable
- **Reproducibility:** Uses fixed pre-trained embeddings
- **Ethical-by-Design:** Explicit bias detection and correction

---

### Scalability & Extensions

- Can be extended to:
  - Contextual embeddings (BERT, RoBERTa)
  - Multiple bias dimensions (race, age, profession)
  - Downstream task evaluation (classification fairness)
- Visualization modules can be added for embedding space analysis

---

### Constraints

- Static embeddings only
- Binary gender assumption
- No real-time or streaming support

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
