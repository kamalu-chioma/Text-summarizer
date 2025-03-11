# Text Summarization Using Various Approaches

This repository implements and compares different techniques for text summarization using sentence embeddings and ranking algorithms. The core idea is to represent sentences as vectors and rank them using PageRank, but the methods for vectorization vary across approaches.

## Approaches

### 1. GloVe + Average Word Vectors
- **Description**: This method uses GloVe word embeddings and creates a sentence vector by averaging the word vectors in the sentence.
- **Folder**: `glove_average/`
- **Strength**: Simple and computationally efficient.
- **Weakness**: May lose word order and contextual meaning.

### 2. GloVe + TF-IDF Weighted Averaging
- **Description**: Weigh each word’s vector by its TF-IDF score to give more importance to rare words, then average the weighted vectors.
- **Folder**: `tfidf_weighting/`
- **Strength**: Captures important words and emphasizes rare words.
- **Weakness**: Relies on word frequencies and may not capture deep contextual relationships.

### 3. BERT Embeddings
- **Description**: Uses pre-trained BERT embeddings to represent entire sentences with context-aware vectors.
- **Folder**: `bert_embedding/`
- **Strength**: Deep understanding of context and word meaning.
- **Weakness**: Computationally expensive and requires more resources.

### 4. GloVe + Concatenation of Word Vectors
- **Description**: Instead of averaging, concatenate the word vectors for the first `n` words of the sentence to preserve more individual word information.
- **Folder**: `concatenation/`
- **Strength**: Retains more individual word meaning.
- **Weakness**: Increases dimensionality and can become inefficient for longer sentences.

## How to use

Each folder contains a separate implementation of the summarization technique. You can navigate to the specific folder for each method and run the `main.py` file to test that approach.

1. **Clone the repository**:
   ```bash
   git clone https://github.com/kamalu-chioma/Text-summarizer.git

This repository implements and compares different techniques for text summarization using sentence embeddings and ranking algorithms. The core idea is to represent sentences as vectors and rank them using PageRank, but the methods for vectorization vary across approaches.

## Approaches

### 1. GloVe + Average Word Vectors
- **Description**: This method uses GloVe word embeddings and creates a sentence vector by averaging the word vectors in the sentence.
- **Folder**: `glove_average/`
- **Strength**: Simple and computationally efficient.
- **Weakness**: May lose word order and contextual meaning.

### 2. GloVe + TF-IDF Weighted Averaging
- **Description**: Weigh each word’s vector by its TF-IDF score to give more importance to rare words, then average the weighted vectors.
- **Folder**: `tfidf_weighting/`
- **Strength**: Captures important words and emphasizes rare words.
- **Weakness**: Relies on word frequencies and may not capture deep contextual relationships.

### 3. BERT Embeddings
- **Description**: Uses pre-trained BERT embeddings to represent entire sentences with context-aware vectors.
- **Folder**: `bert_embedding/`
- **Strength**: Deep understanding of context and word meaning.
- **Weakness**: Computationally expensive and requires more resources.

### 4. GloVe + Concatenation of Word Vectors
- **Description**: Instead of averaging, concatenate the word vectors for the first `n` words of the sentence to preserve more individual word information.
- **Folder**: `concatenation/`
- **Strength**: Retains more individual word meaning.
- **Weakness**: Increases dimensionality and can become inefficient for longer sentences.

## How to Use

Each folder contains a **Jupyter Notebook** (`.ipynb`) that implements the summarization technique. You can navigate to the specific folder for each method and run the notebook to test the approach.

1. **Clone the repository**:
   ```bash
   git clone https://github.com/kamalu-chioma/Text-summarizer/.git
