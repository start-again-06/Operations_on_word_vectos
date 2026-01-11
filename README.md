# 🧠 Bias Reduction in Word Embeddings

This project explores how gender bias manifests in word embeddings and how to mitigate it using vector operations. The implementation is based on GloVe word vectors and is inspired by the DeepLearning.AI NLP course.

---

## 📁 Dataset

- **GloVe Embeddings File**: `glove.6B.50d.txt`  
  Pre-trained 50-dimensional word vectors.

---

## 🔧 Functionality Overview

### ✅ Cosine Similarity

Measures the similarity between two word vectors:

```python
cosine_similarity(word_to_vec_map["father"], word_to_vec_map["mother"])
cosine_similarity(word_to_vec_map["ball"], word_to_vec_map["crocodile"])
cosine_similarity(word_to_vec_map["france"] - word_to_vec_map["paris"],
                  word_to_vec_map["rome"] - word_to_vec_map["italy"])
🔁 Complete Word Analogies
Solves word analogies using vector arithmetic:

complete_analogy("man", "woman", "boy", word_to_vec_map)
complete_analogy("italy", "italian", "spain", word_to_vec_map)
🧭 Bias Direction
Constructs a bias axis (e.g., g = woman - man) and measures alignment of words with this axis:

g = word_to_vec_map['woman'] - word_to_vec_map['man']
cosine_similarity(word_to_vec_map["receptionist"], g)
🧼 Neutralization
Removes the gender component from gender-neutral words:

e_debiased = neutralize("receptionist", g, word_to_vec_map)
cosine_similarity(e_debiased, g)  # Should be near 0
⚖️ Equalization
Equalizes gender-paired words so that they are equidistant from the bias axis:

e1, e2 = equalize(("man", "woman"), g, word_to_vec_map)
cosine_similarity(e1, g)  # ≈ cosine_similarity(e2, g)
📊 Sample Outputs

cosine_similarity(father, mother) = 0.89
cosine_similarity(ball, crocodile) = 0.25
cosine_similarity(france - paris, rome - italy) = 0.82
Analogies:

italy -> italian :: spain -> spanish
man -> woman :: boy -> girl
Bias Scores Before Debiasing:

receptionist  →  0.32
engineer      → -0.05
teacher       →  0.28
After Debiasing:

cosine_similarity(receptionist, gender axis) → 0.00
cosine_similarity(man, gender axis) → 0.46
cosine_similarity(woman, gender axis) → 0.46

📌 Key Takeaways
Word embeddings capture societal biases that can be measured.

Debiasing involves identifying bias axes and projecting/removing components.

Ensuring fair NLP systems requires careful handling of training data and embeddings.

📦 Dependencies
Make sure to install:

To install:

pip install numpy
