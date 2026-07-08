# Semantic Search & Retrieval-Augmented Generation (RAG) Pipeline

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![SentenceTransformers](https://img.shields.io/badge/Sentence--Transformers-all--MiniLM--L6--v2-green)
![FAISS](https://img.shields.io/badge/Vector%20Search-FAISS-red)

**Author:** Shresth Raj  
**Date of Project:** March 2026  

## 🎯 Objective
This project implements a complete **Semantic Search and RAG (Retrieval-Augmented Generation)** pipeline designed to understand user intent based on *meaning* rather than mere keyword matching. By leveraging dense text embeddings and efficient vector similarity search, the pipeline dynamically surfaces the most relevant product context to assist in generating natural, intelligent answers.

## ✨ Key Features
- **Semantic Text Embeddings:** Uses the `all-MiniLM-L6-v2` Sentence-transformer model to represent product reviews and search queries in a high-dimensional vector space.
- **Efficient Vector Search:** Implemented with **FAISS (Facebook AI Similarity Search)** using `IndexFlatIP` for rapid, scalable inner-product (cosine similarity) searches.
- **RAG Generation Layer:** Enriches standard LLM text generation with highly relevant context retrieved dynamically from the user's dataset.
- **Comprehensive EDA:** Explores text data through visualizations including rating distributions, word clouds, text-length histograms, and PCA-based 2D dimensionality reduction.
- **Robust Evaluation:** Evaluates retrieval effectiveness using standard Information Retrieval metrics like Precision@K and Recall@K.

## 🛠 Tech Stack
- **Language:** Python
- **Data Manipulation:** `pandas`, `numpy`
- **Machine Learning & NLP:** `sentence-transformers`, `scikit-learn`, `nltk`
- **Vector Search Engine:** `faiss-cpu`
- **Visualization:** `matplotlib`, `seaborn`, `wordcloud`

## 📊 Dataset
**Flipkart Product Reviews Dataset (`products_reviews.csv`)**
Contains nearly 205,000 product reviews including:
- `product_name`
- `product_price`
- `Rate` (Rating out of 5)
- `Review` (Short review descriptor)
- `Summary` (Detailed review text)
- `Sentiment` (Positive, Negative, Neutral)

## 🚀 Pipeline Overview
1. **Data Loading & Exploration:** Understand raw dataset structures and patterns.
2. **Text Preprocessing & Cleaning:** Filter non-alphanumeric text, remove stop-words, and normalize text for vectorization.
3. **EDA Visualizations:** Uncover actionable insights from sentiment and text characteristics.
4. **Embedding Generation:** Create dense vector representations for the product summaries.
5. **FAISS Indexing:** Build an optimized vector index to query vectors on the fly.
6. **Semantic Search Engine:** Query the FAISS index to return the $k$-nearest neighbors based on meaning.
7. **RAG Pipeline:** Integrate the retrieval mechanism with text generation algorithms.
8. **Evaluation Setup:** Score the retrieval using quantitative metrics.
9. **Business Insights & Suggestions:** Translate numerical/NLP metrics into valuable product recommendations.

## 💻 Getting Started
1. Clone this repository:
   ```bash
   git clone https://github.com/iamshresthraj/Semantic_Search_RAG_Pipeline.git
   cd Semantic_Search_RAG_Pipeline
   ```

2. Install dependencies:
   ```bash
   pip install transformers accelerate sentence-transformers faiss-cpu wordcloud pandas numpy scikit-learn nltk matplotlib seaborn
   ```

3. Open the Jupyter Notebook to run the pipeline:
   ```bash
   jupyter notebook Semantic_Search_RAG_Pipeline.ipynb
   ```

## 📜 License
This project was built for educational and development purposes. Please adhere to the terms of the dataset providers when deploying commercially.
