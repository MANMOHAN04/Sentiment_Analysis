# Sentiment Analysis 

This project implements sentiment analysis on textual data to classify sentiments into Angry, Sad, Neutral, Happy, or Excited categories. It leverages machine learning techniques and natural language processing (NLP) methods to analyze and visualize sentiments effectively.

---

## Problem Statement

- Huge volumes of text data are generated daily (e.g., reviews, tweets).

- Manual sentiment analysis is slow and inefficient.

- Businesses need automated tools to understand opinions and feedback.

- Text data is unstructured and hard to interpret without NLP.

- A sentiment analysis model can help classify text as Positive, Negative, or Neutral.

- Goal: Build an NLP-based system for fast and accurate sentiment classification.

---

## Project Structure

```plaintext

sentiment-analysis/
│
├── assets
│   ├──plots
│
├── data/
│   ├── processed          # Dataset containing text and sentiment labels
│   ├── raw
│
├── reports/
│   
├── src/
│   ├── models/
│   │   ├── best_model_logistic_regression.pkl      
│   │   ├── logistic_regression_20250429_201448.pkl   
│   ├── reports/
│   ├── 01_preprocess.ipynb     
│   ├── 02_model_building_evaluation.ipynb
│   ├── 03_inject_noisy.ipynb
│   ├── 04_model_building_noisy.ipynb
│   ├── 05_retraining_models.py
│
├── web_app/
│   ├── static/
│   │    ├── style.css
│   ├── templates/
│   │    ├── index.html
│   ├──app.py
│
├── .gitattributes
├── .gitignore
├── requirements.txt         # List of dependencies
├── README.md                # Project documentation
└── LICENSE                  # Project license


```




## Dataset Overview

- **Source**: Provided by Md Farmanul Haque, as part of the AI & ML Bootcamp. 
- **Total Rows**: 2,000
- **Columns**: 8
  - Username : The username of the person who posted the comment.
  - Comment : The full text of the comment. This is the main feature for sentiment analysis.
  - Comment_Date : The date the comment was posted (in YYYY-MM-DD format).
  - Likes : Number of likes the comment received — a possible proxy for comment impact.
  - Comment_Length : Word count of the comment — useful for text analytics or modeling.
  - Has_Typo : Binary indicator (0 or 1) showing whether the comment contains typos.
  - Slang_Presence : Binary indicator showing if the comment includes slang.
  - Sentiment : The target label indicating the sentiment expressed in the comment. Example values include "Angry", "Happy", "Sad", "Excited", and "Neutral".

---

## Tools & Libraries Used

- `pandas`, `numpy`, `matplotlib`, `seaborn`, `logging`
- `scikit-learn`: models, preprocessing, metrics
- `Logistic Regression`, `Random Forest Classifier`, `Gradient Boosting Classifier`,`Support Vector Classifier`,`xgBoost Classifier`,`Light GBM Classifier`
- `jupyter`, `notebook`

---

## Setup Instructions

# Step 1: Clone the repository 
- git clone https://github.com/MANMOHAN04/Sentiment_Analysis
- cd sentimentAnalysis

# Step 2: Create and activate a virtual environment 
- python -m venv env
- env\Scripts\activate     # For Windows

# Step 3: Install required dependencies
- pip install -r requirements.txt

# Step 4: Run the training script and deploy
- python src/05_retraining_models.py          # For model retraining.
- python app.py                               # Run the app for deployment.

---

## Author

**Name:** Manmohan Kumar 
**GitLab:** [https://github.com/MANMOHAN04/Sentiment_Analysis](https://github.com/MANMOHAN04/Sentiment_Analysis)

---

## License

This project is licensed under the **MIT License**. See the [LICENSE](./LICENSE) file for full details.
