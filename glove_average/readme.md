# GloVe + Average Word Vectors for Text Summarization

## Overview

This folder contains the implementation of text summarization using **GloVe word embeddings** combined with **average word vectors** to represent sentences. The approach involves converting each sentence into a single vector by averaging the GloVe vectors of the words in the sentence and then applying the **PageRank algorithm** to rank sentences based on their importance.

## Process

1. **Load Data**: The dataset is loaded from a CSV file (`tennis.csv`), which contains article text that will be summarized.
   
2. **Sentence Tokenization**: Each article is split into individual sentences using NLTK’s `sent_tokenize()`.

3. **Preprocessing**: Sentences are cleaned by removing non-alphabetic characters, converting to lowercase, and removing stopwords.

4. **GloVe Embeddings**: Pre-trained GloVe word embeddings (100-dimensional) are loaded to represent words as vectors.

5. **Sentence Vector Creation**:
   - Each sentence is represented as the **average** of its word vectors. If a word is not found in the GloVe dictionary, a zero vector is used.
   
6. **Similarity Matrix**: A cosine similarity matrix is constructed between sentence vectors to measure sentence similarity.

7. **PageRank for Sentence Importance**: The similarity matrix is transformed into a graph, and PageRank is applied to rank sentences based on their importance in the document.

8. **Summary Generation**: The top-ranked sentences are selected to form the final summary.

## How to Run

### 1. Clone the Repository:
```bash
git clone https://github.com/your-username/text-summarization.git
cd text-summarization/glove_average
