# Tweet Engagement Prediction Using NLP

This project aims to predict tweet engagement (likes + retweets) using a combination of Natural Language Processing (NLP), feature engineering, and machine learning models. It was developed as part of the NLP course at IÉSEG School of Management.

## 📘 Overview

The dataset includes over 200,000 tweets with metadata such as language, hour of posting, Klout score, sentiment, and more. The project focuses on:

- Text and metadata preprocessing
- Feature extraction and sentiment analysis
- Topic modeling using BERTopic
- Predictive modeling using tree-based regressors

## 🧹 Data Preparation

- Filtered for English tweets
- Dropped missing content
- Created features like:
  - Number of hashtags, mentions, URLs, punctuation
  - Sentiment polarity and subjectivity (TextBlob)
  - Time-of-day and weekday flags
  - Presence of call-to-action words

## 🧠 Topic Modeling

- Applied BERTopic for better context-aware topic grouping
- Automatically identified key themes and tweet clusters

## 🧪 Modeling & Evaluation

We tested several regression models and finalized:

- **Random Forest Regressor**
- **Gradient Boosting Regressor**

**Target**:  
`engagement_score = Likes + RetweetCount`, log-transformed as `log(engagement_score + 1)`

**Final Results**:

| Model           | R²     | RMSE   | MAE   |
|----------------|--------|--------|--------|
| Random Forest  | 0.7305 | 0.6591 | 0.4180 |
| Gradient Boost | 0.4654 | 0.9285 | 0.6547 |

✅ Random Forest outperformed other models and was chosen for final deployment.

## 📂 Files

- `Group_3_NLP_Final.ipynb`: Jupyter notebook with all code
- `Tweets Engagement Predictions Report.docx`: Full project report
- `twitter_dataset.csv`: Cleaned and structured dataset (optional to share)
- `BERTopic_model.pkl`: Topic modeling output (optional)

## 🔧 Tech Stack

- Python · Scikit-learn · Pandas · TextBlob · BERTopic · Matplotlib · Seaborn

## 📚 Acknowledgements

Project by Thi Xuan Nguyen, Quy Dam Son, Tao Zhang. Developed as part of *Fundamentals of NLP* at IÉSEG School of Management.
