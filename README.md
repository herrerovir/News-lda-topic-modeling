# 📰🔎 Topic Modeling on News Snippets Using LDA

This repository presents an unsupervised NLP project that uncovers hidden themes in a collection of news snippets using Latent Dirichlet Allocation (LDA). The project explores how topic modeling can be used to organize and interpret large amounts of textual data effectively.

## 📚 Table of Contents

- [Introduction](#introduction)
- [Goal](#goal)
- [Project Overview](#project-overview)
- [Dependencies](#dependencies)
- [How to Run the Project](#how-to-run-the-project)
- [Repository Structure](#repository-structure)
- [Technical Skills](#technical-skills)
- [LDA Model](#lda-model)
- [Results](#results)

## 📌 Introduction

Topic modeling is an unsupervised machine learning technique that helps discover the hidden thematic structure in a large collection of documents. Instead of reading each document individually, topic models automatically identify clusters of words that frequently occur together, which represent “topics.” This enables us to summarize, explore, and organize large amounts of unstructured text data in a meaningful way.

One of the most popular topic modeling methods is **Latent Dirichlet Allocation (LDA)**. It represents each document as a mixture of topics and each topic as a mixture of words, capturing the underlying themes within the text collection.

## 🎯 Goal

The goal of this project is to automatically discover the underlying topics in a small corpus of news snippets and cluster each document based on these topics. This showcases fundamental NLP techniques and serves as a foundational template for topic modeling tasks on larger or more complex corpora.

## 🧐 Project Overview

- **Data preprocessing**: Clean and prepare raw text by tokenizing, removing stopwords, and normalizing words.
- **Dictionary and BoW creation**: Convert text into numerical format for modeling.
- **LDA topic modeling**: Train a model to find latent topics.
- **Topic distribution extraction**: Represent documents as topic vectors.
- **Clustering documents**: Group documents by similar topics.
- **Visualization**: Display clusters in 2D for easy interpretation.


## 🔗 Dependencies

- Python 3.6+
- NLTK
- Gensim
- PyLDAvis
- Pprint
- Collections
- Json
- Matplotlib
- Seaborn

## ▶️ How to Run the Project

1. Clone the repository:

   ```shell
   git clone https://github.com/herrerovir/News-lda-topic-modeling.git
   cd News-lda-topic-modeling

   ```

2. Install dependencies:

   ```shell
   pip install -r requirements.txt
   ```

3. Launch Jupyter Notebook:

   ```shell
   jupyter notebook
   ```

4. Open and run the notebook `notebooks/News-lda-topic-modeling.ipynb` to start training and evaluating the model.

## 🗂️ Repository Structure

```
News-lda-topic-modeling/
│
├── model/                                     # Trained LDA model files
│   └── best-lda-model.model
│   └── best-lda-model.model.expElogbeta.npy
│   └── best-lda-model.model.id2word
│   └── best-lda-model.model.state
│
├── notebooks/                                 # Main notebook for model training and analysis
│   └── Cnn-cifar-10-image-classifier.ipynb
│
├── results/                                   # Model results
│   └── documents/
│       └── document-dominant-topics           
│       └── document-topic-distributions
│       └── lda-model-doc-clusters          
│
│   └── figures/
│       └── Documents-per-dominant-topic
│       └── lda-visualizations
│       └── Top-10-words-topic-0
│       └── Top-10-words-topic-1
│       └── Top-10-words-topic-2
│       └── Wordcloud-topic-0
│       └── Wordcloud-topic-1
│       └── Wordcloud-topic-2
│
│   └── metrics/
│       └── best-lda-model
│       └── lda-coherence-scores

│   └── topics/
│       └── lda-model-topic-keywords
|       └── lda-model-topic-labels
│
├── requirements.txt                           # Python dependencies
│ 
└── README.md                                  # Project documentation
```

## 🛠️ Technical Skills

- Natural Language Processing (NLP)
- Unsupervised Learning
- Probabilistic Topic Modeling (LDA)
- Text Preprocessing & Tokenization
- Word Clouds and Topic Visualization
- Coherence Score Evaluation
- Data Visualization with Matplotlib & Seaborn

## 🧠 LDA Model

The project applies Latent Dirichlet Allocation (LDA), a probabilistic topic modeling technique that uncovers latent themes within a collection of documents.

LDA models each document as a mixture of topics, and each topic as a distribution over words. Through training, the algorithm identifies patterns in word usage across the corpus, grouping frequently co-occurring terms into coherent topics.

Each document is then represented by a topic distribution, while each topic is defined by a set of high-probability keywords. Several models were trained using different numbers of topics; the version with three topics achieved the highest coherence score and produced the most interpretable results.

The model was implemented using Gensim, with PyLDAvis used to visualize topic composition.


## 📊 Results

This project used Latent Dirichlet Allocation (LDA) to uncover major themes in a corpus of news articles. After testing multiple topic counts, a 3-topic model achieved the highest coherence score of 0.6217, suggesting a strong balance between topic clarity and distinctiveness.

Manual inspection and keyword analysis led to the following labeled topics:

- Topic 0 – Local Events: Cultural festivals, community news, and startup activity.
- Topic 1 – Public Affairs: Health updates, technology developments, and public responses.
- Topic 2 – Urban Development: Government policies, infrastructure, and environmental issues.

Documents were grouped by their dominant topic, forming clearly interpretable clusters. This combination of modeling and manual analysis demonstrates that topic modeling can effectively structure unorganized news data into meaningful categories, making it easier to explore and understand.
