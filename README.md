# BBC-news-classification-word2vec
BBC News article classification using Word2Vec embeddings — comparing full text vs extractive summarization impact on model performance.

## BBC News Classification — Word2Vec

This project classifies BBC News articles into 5 categories (business, entertainment, 
politics, sport, tech) using Word2Vec embeddings and traditional ML classifiers.

### Research Question
Does text summarization improve or worsen classification performance compared to full article text?

### Approach
- Text preprocessing — lowercasing, stopword removal, lemmatization
- Extractive summarization using LSA (sumy library)
- Word2Vec vectorization (gensim) — two separate models for each track
- Three classifiers trained and compared — Logistic Regression, SVM, Random Forest
- Full evaluation — accuracy, F1, confusion matrix, error analysis

### Key Results
| Model               | Original Acc | Summary Acc |
|---------------------|-------------|-------------|
| Logistic Regression | 93.0%       | 29.8%       |
| SVM                 | 91.8%       | 28.6%       |
| Random Forest       | 94.6%       | 50.9%       |

### Conclusion
Summarization consistently worsened performance across all models. Full text provides 
richer semantic context for Word2Vec, resulting in more accurate classification.

### Dataset
BBC News Dataset — 2,225 articles across 5 categories (2004–2005)
Available on Kaggle: https://www.kaggle.com/datasets/shivamkushwaha/bbc-full-text-document-classification

### Tech Stack
Python · Jupyter Notebook · gensim · scikit-learn · nltk · sumy · matplotlib · seaborn
