# Medical Word Embeddings

Exploring pretrained GloVe word embeddings to understand semantic and contextual relationships between medical terms using cosine similarity, vector arithmetic, and PCA visualization.

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![NLP](https://img.shields.io/badge/NLP-Word%20Embeddings-green)
![Gensim](https://img.shields.io/badge/Gensim-Embeddings-orange)
![Scikit--learn](https://img.shields.io/badge/Scikit--learn-ML-red)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

## Project Overview

Word embeddings represent words as dense numerical vectors that capture semantic and contextual relationships between words.

In this project, a pretrained **GloVe Wiki-Gigaword 100-dimensional model** was used to explore relationships between medical terms such as `doctor`, `nurse`, `hospital`, `disease`, `cancer`, and `diabetes`.

The project focuses on understanding how embedding spaces can be used to measure word similarity, explore relationships between terms, and visualize high-dimensional word representations.

## Objectives

* Understand the concept of word embeddings.
* Load and explore a pretrained GloVe model.
* Inspect numerical word-vector representations.
* Analyze medical vocabulary.
* Calculate cosine similarity between words.
* Find semantically similar terms.
* Explore relationships using vector arithmetic.
* Visualize embeddings using PCA.
* Build a similarity matrix for medical vocabulary.
* Identify the strongest relationships between selected medical terms.

## Model Used

**GloVe Wiki-Gigaword 100d**

| Property            |                Value |
| ------------------- | -------------------: |
| Vocabulary          |        400,000 words |
| Embedding Dimension |                  100 |
| Model Type          |     Pretrained GloVe |
| Domain              | General English text |

The model was loaded using Gensim's pretrained model interface.

## Project Workflow

### 1. Load Pretrained Embeddings

The pretrained GloVe model was loaded and its vocabulary size and embedding dimension were verified.

### 2. Inspect Word Vectors

Individual words were converted into 100-dimensional numerical vectors.

For example:

```text
doctor → [0.043244, -0.475290, 0.158080, ...]
```

### 3. Medical Vocabulary Analysis

The following medical terms were examined:

```text
doctor
physician
nurse
patient
hospital
clinic
medicine
disease
cancer
diabetes
hypertension
obesity
surgery
health
```

All 14 selected terms were available in the pretrained vocabulary.

### 4. Cosine Similarity

Cosine similarity was used to measure how close two word vectors are in the embedding space.

The analysis showed relationships such as:

```text
doctor ↔ physician     0.7673
doctor ↔ nurse         0.7522
doctor ↔ hospital      0.6901
doctor ↔ diabetes      0.4258
```

### 5. Similar Words

The model was used to retrieve words that were most similar to selected medical terms.

For example, the strongest results for `doctor` included:

```text
physician
nurse
dr.
doctors
patient
medical
surgeon
hospital
```

### 6. Vector Arithmetic

Vector arithmetic was explored to demonstrate relationships encoded in embedding space.

A classic example:

```text
king - man + woman → queen
```

The experiment also tested relationships involving medical terms.

### 7. PCA Visualization

Principal Component Analysis (PCA) was used to reduce the 100-dimensional word vectors to two dimensions for visualization.

This provided a visual representation of the relationships between the selected medical terms.

### 8. Similarity Matrix

A 14 × 14 cosine similarity matrix was created to compare all selected medical terms with each other.

The matrix contained no missing values.

## Key Results

The strongest relationships identified among the selected medical terms were:

| Rank | Word 1       | Word 2       | Similarity |
| ---: | ------------ | ------------ | ---------: |
|    1 | diabetes     | hypertension |     0.8483 |
|    2 | hospital     | clinic       |     0.8140 |
|    3 | diabetes     | obesity      |     0.7994 |
|    4 | disease      | cancer       |     0.7854 |
|    5 | cancer       | diabetes     |     0.7788 |
|    6 | doctor       | physician    |     0.7673 |
|    7 | doctor       | nurse        |     0.7522 |
|    8 | disease      | diabetes     |     0.7332 |
|    9 | doctor       | patient      |     0.7074 |
|   10 | hypertension | obesity      |     0.6951 |

## Quality Assurance

The final quality checks confirmed:

| Check               |    Result |
| ------------------- | --------: |
| Medical terms       |        14 |
| Embedding dimension |       100 |
| Similarity matrix   |   14 × 14 |
| Missing values      |         0 |
| Minimum similarity  |    0.1553 |
| Maximum similarity  | 1.0000002 |

The maximum value slightly above 1 is a result of floating-point numerical precision.

## Important Interpretation

The similarity scores represent **semantic and contextual similarity learned from the GloVe training corpus**.

They should not be interpreted as:

* Clinical evidence
* Disease causation
* Medical recommendations
* Synonym relationships in every case

For example, the high similarity between `diabetes` and `hypertension` indicates that the terms have similar representations in the embedding space. It does not establish a clinical or causal relationship.

## Limitations

* GloVe is a general-purpose pretrained embedding model rather than a medical-specific model.
* The embeddings are static, so the same word has one representation regardless of context.
* Similarity does not always mean synonymy.
* The model may contain biases present in its training corpus.
* The project focuses on semantic analysis rather than a downstream medical NLP task.

## Technologies

* Python
* Gensim
* NumPy
* Pandas
* Scikit-learn
* Matplotlib
* GloVe Wiki-Gigaword

## Learning Outcomes

Through this project, I developed practical understanding of:

* Word embeddings
* Dense vector representations
* Pretrained embedding models
* Cosine similarity
* Semantic relationships
* Vector arithmetic
* PCA dimensionality reduction
* Similarity matrices
* Basic NLP visualization and analysis

## AI Assistance

AI tools were used during the project for:

* Understanding NLP and word embedding concepts
* Project planning and step-by-step guidance
* Code assistance and debugging
* Explaining model outputs
* Improving project documentation

The notebook was executed and the reported results were verified from the actual model outputs.

## Conclusion

This project provided a practical introduction to word embeddings by applying a pretrained GloVe model to medical vocabulary.

The analysis demonstrated how words can be represented as dense vectors and how cosine similarity, vector arithmetic, PCA, and similarity matrices can be used to investigate relationships between words.

The project also highlighted an important limitation: general-purpose embeddings capture linguistic patterns rather than providing reliable clinical knowledge.


