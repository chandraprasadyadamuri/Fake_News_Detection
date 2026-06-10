# 📰Fake News Detection System

An advanced **Natural Language Processing (NLP)** and **Machine Learning** project that detects whether a news article is **Real** or **Fake**. The system utilizes text preprocessing, TF-IDF feature extraction, and supervised learning algorithms to classify news content with high accuracy.

---

## 📌 Project Overview

Fake news has become a significant challenge in the digital era. This project aims to automatically identify misleading or fabricated news articles using NLP techniques and machine learning models.

The workflow includes:

* Data collection and labeling
* Text preprocessing and cleaning
* Feature extraction using TF-IDF
* Model training and evaluation
* Real-time prediction on custom news articles

---

## 🚀 Features

* Binary classification of news articles (Real / Fake)
* Advanced NLP preprocessing pipeline
* TF-IDF feature engineering
* Logistic Regression and Passive Aggressive Classifier models
* High classification accuracy (95%+)
* Model serialization using Pickle
* Custom news prediction support

---

## 🛠️ Tech Stack

### Programming Language

* Python 3.x

### Libraries & Frameworks

* Pandas
* NumPy
* Regex (re)
* NLTK
* Scikit-Learn
* Matplotlib
* Seaborn
* Pickle

---

## 📂 Dataset

The project uses two publicly available datasets:

| Dataset  | Description                          |
| -------- | ------------------------------------ |
| Fake.csv | Contains fake news articles          |
| True.csv | Contains verified real news articles |

### Label Encoding

| News Type | Label |
| --------- | ----- |
| Fake News | 1     |
| Real News | 0     |

---

## 🔄 Project Workflow

```text
Raw Datasets
      │
      ▼
Labeling & Data Mixing
      │
      ▼
Text Preprocessing
      │
      ▼
TF-IDF Vectorization
      │
      ▼
Model Training
      │
      ▼
Model Evaluation
      │
      ▼
Pickle Export
      │
      ▼
Real-Time Prediction
```

---

## 🧹 Text Preprocessing Pipeline

The textual data undergoes several cleaning and normalization steps:

### 1. Lowercasing

Converts all text to lowercase for consistency.

### 2. Regular Expression Cleaning

Removes:

* Punctuation
* Numbers
* Special characters
* Emojis
* HTML-like patterns

### 3. Stopword Removal

Eliminates common words using NLTK stopword lists.

Example:

```text
the, is, am, are, was, were, and, but...
```

### 4. Stemming

Applies the Porter Stemmer algorithm to reduce words to their root forms.

Example:

```text
Running → Run
Playing → Play
Studies → Studi
```

---

## ⚙️ Feature Engineering

### Train-Test Split

* 80% Training Data
* 20% Testing Data

### TF-IDF Vectorization

The cleaned text is converted into numerical vectors using:

```python
TfidfVectorizer(max_features=5000)
```

Benefits:

* Captures word importance
* Reduces impact of common words
* Creates sparse numerical representations suitable for machine learning

---

## 🤖 Machine Learning Models

### Logistic Regression

A probabilistic linear classifier used as a strong baseline model.

**Advantages:**

* Fast training
* Interpretable
* High accuracy on text data

---

### Passive Aggressive Classifier

An online learning algorithm particularly effective for:

* Text classification
* Large sparse datasets
* High-dimensional TF-IDF features

**Advantages:**

* Fast updates
* Excellent performance on NLP tasks
* Memory efficient

---

## 📊 Model Performance

The trained models consistently achieve:

| Metric    | Performance |
| --------- | ----------- |
| Accuracy  | 95%+        |
| Precision | High        |
| Recall    | High        |
| F1 Score  | High        |

### Evaluation Methods

* Accuracy Score
* Classification Report
* Confusion Matrix Visualization

Heatmaps generated using Seaborn help visualize classification performance and error distribution.

---

## 📁 Project Structure

```text
Fake_News_Detection/
│
├── Fake.csv
├── True.csv
├── main.ipynb
├── fake_news_pa_model.pkl
├── tfidf_vectorizer.pkl
└── README.md
```

### File Descriptions

| File                   | Purpose                          |
| ---------------------- | -------------------------------- |
| Fake.csv               | Fake news dataset                |
| True.csv               | Real news dataset                |
| main.ipynb             | Complete development notebook    |
| fake_news_pa_model.pkl | Trained Passive Aggressive model |
| tfidf_vectorizer.pkl   | Saved TF-IDF vectorizer          |
| README.md              | Project documentation            |

---

## 💻 Installation

Clone the repository:

```bash
git clone https://github.com/your-username/Fake_News_Detection.git
cd Fake_News_Detection
```

Install dependencies:

```bash
pip install pandas numpy scikit-learn nltk matplotlib seaborn ipykernel
```

---

## ▶️ Running the Project

### Step 1: Open the Notebook

Launch VS Code or Jupyter Notebook and open:

```text
main.ipynb
```

### Step 2: Select Python Environment

Choose the correct Python interpreter/kernel.

### Step 3: Run Cells Sequentially

The notebook will:

* Load datasets
* Perform preprocessing
* Train models
* Evaluate performance
* Save trained artifacts

---

## 🔮 Custom News Prediction

After training, test the model with your own news article:

```python
custom_headline = "Global Markets Steady as Inflation Rates Show Gradual Decline"

custom_body = """
The Federal Reserve reported a minor decrease in core inflation metrics this quarter...
"""

predict_news(custom_headline, custom_body)
```

### Sample Output

```text
[ REAL / TRUE NEWS ]
```

or

```text
[ FAKE NEWS ]
```

---

## 📈 Future Enhancements

* Deep Learning Models (LSTM, GRU)
* Transformer Models (BERT)
* Streamlit Web Application
* Real-Time News Scraping
* REST API Deployment
* Multilingual Fake News Detection

---

## 🎯 Learning Outcomes

This project demonstrates:

* Natural Language Processing
* Data Cleaning & Preparation
* Feature Engineering
* TF-IDF Vectorization
* Machine Learning Classification
* Model Evaluation
* Model Serialization
* End-to-End NLP Pipeline Development

---

## 👨‍💻 Author

**Chandra Prasad**
