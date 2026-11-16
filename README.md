# 🎬 Movie Review Sentiment Analysis & Recommendation System

A machine learning web application built with **Streamlit** that combines **NLP-powered Movie Review Sentiment Analysis** and a **Content-Based Movie Recommendation Engine** in an interactive user interface.

---

## 🌟 Key Features

### 1. 💬 Movie Review Sentiment Analysis
- Predicts whether an entered movie review is **Positive 😊** or **Negative 😞**.
- Displays real-time prediction confidence and probabilities.
- Employs text preprocessing pipeline: HTML tag removal, punctuation stripping, tokenization, stopword removal, lemmatization, and stemming via **NLTK**.
- Powered by a **Multinomial Naive Bayes (MNB)** classifier with **TF-IDF Vectorization**.
- Includes live evaluation metrics and confusion matrix.

### 2. 🍿 Content-Based Movie Recommendation System
- Recommends top $N$ similar movies based on user search.
- Computes similarity using **Cosine Similarity** over combined metadata (genres, keywords, cast, and director).
- Displays recommendations in a clean, ranked table along with similarity scores.
- Memory-optimized for responsive inference.

### 3. 📊 Model Performance Metrics
Trained and evaluated on balanced benchmark review data:

| Metric | Score |
| :--- | :--- |
| **Accuracy** | **84.11%** |
| **Precision** | **96.14%** |
| **Recall** | **71.64%** |
| **F1 Score** | **82.10%** |

---

## 📁 Repository Structure

```plaintext
movie-review-sentiment-analysis/
│
├── app.py                             # Streamlit web application
├── mnb_model.pkl                      # Trained Multinomial Naive Bayes model
├── mtfidf_vectorizer.pkl              # Fitted TF-IDF Vectorizer
├── movies.pkl                         # Processed movie metadata for recommendations
├── metrics.json                       # Model evaluation metrics & confusion matrix
├── Sentiment_Analysis.ipynb           # Model development & NLP preprocessing notebook
├── movie recommendation system.ipynb  # Recommender system development notebook
├── requirements.txt                   # Project Python dependencies
├── .gitignore                         # Files ignored by Git
└── README.md                          # Project documentation
```

---

## 🛠️ Tech Stack & Libraries

- **Language:** Python
- **Web App:** [Streamlit](https://streamlit.io/)
- **Machine Learning & NLP:** [scikit-learn](https://scikit-learn.org/), [NLTK](https://www.nltk.org/)
- **Data Manipulation & Visualization:** [Pandas](https://pandas.pydata.org/), [NumPy](https://numpy.org/), [Matplotlib](https://matplotlib.org/), [Seaborn](https://seaborn.pydata.org/)

---

## 🚀 Getting Started

Follow these instructions to set up and run the project locally.

### Prerequisites
Make sure you have **Python 3.8+** installed.

### 1. Clone the Repository
```bash
git clone https://github.com/<your-username>/movie-review-sentiment-analysis.git
cd movie-review-sentiment-analysis
```

### 2. Create and Activate a Virtual Environment
- **Windows (Command Prompt / PowerShell):**
  ```powershell
  python -m venv venv
  .\venv\Scripts\activate
  ```
- **macOS / Linux:**
  ```bash
  python3 -m venv venv
  source venv/bin/activate
  ```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Run the Streamlit Application
```bash
streamlit run app.py
```
Open your browser at `http://localhost:8501` to use the application.

---

## 📓 Notebooks

- **`Sentiment_Analysis.ipynb`**: Demonstrates the full sentiment analysis lifecycle: data cleaning, EDA, text preprocessing (tokenization, stopwords, stemming, lemmatization), TF-IDF feature extraction, model comparison, hyperparameter tuning, and model persistence.
- **`movie recommendation system.ipynb`**: Demonstrates content feature extraction, vectorization, and cosine similarity calculation for movie recommendations.

---

## 📄 License
This project is open-source and available under the [MIT License](LICENSE).
