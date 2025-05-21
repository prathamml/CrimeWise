# CrimeWise – Scalable Crime Categorization Using PySpark & ML

## 🔍 Overview
CrimeWise is a scalable machine learning pipeline for automated classification of crime descriptions into predefined categories. Designed using PySpark for handling large-scale data, the system aims to support law enforcement by improving response accuracy and resource allocation through predictive crime categorization.
This project achieves 99.53% classification accuracy using TF-IDF and Naive Bayes, and integrates performance metrics visualization via Power BI for effective insights.

## ⚙️ Implementation Pipeline
The implementation follows a structured approach—from data ingestion to result visualization:

📁 Step 1: Data Extraction
Load crime dataset from Kaggle.
Extract key columns:
Category (target label)
Descript (crime description)

🧹 Step 2: Data Preprocessing & Feature Engineering
Text Tokenization: Using RegexTokenizer to tokenize crime descriptions.
Stopword Removal: Using StopWordsRemover to eliminate common words.
Vectorization:
CountVectorizer for bag-of-words representation
TF-IDF for term frequency weighting
Word2Vec for word embeddings
Label Encoding: Convert string labels into numeric form using StringIndexer.

🧠 Step 3: Model Training & Evaluation
Trained five different model combinations:
| Model Type          | Feature Representation |
| ------------------- | ---------------------- |
| Logistic Regression | CountVectorizer        |
| Logistic Regression | TF-IDF                 |
| Logistic Regression | Word2Vec               |
| Naive Bayes         | CountVectorizer        |
| Naive Bayes         | TF-IDF                 |

Metrics Evaluated:
Accuracy, Precision, Recall, F1-score, AUC-ROC

📊 Step 4: Result Interpretation & Visualization
Best result: TF-IDF + Naive Bayes with 99.53% accuracy.
Performance metrics visualized using Power BI dashboard.
Compared model trade-offs and practical implications for large-scale deployment.

## 🧭 System Flow Diagram
![image](https://github.com/user-attachments/assets/4a2809d6-cc09-4b1d-91f1-e46252acfe7e)

## 📈 Power BI Dashboard Snapshot
![image](https://github.com/user-attachments/assets/e7981915-23a7-45f7-b3bd-58e20dcaa1f7)

##📦 Tech Stack
Language: Python
Framework: PySpark (Apache Spark MLlib)
Visualization: Power BI
Tools: Jupyter Notebook, Pandas, Matplotlib (for initial plots)

## 🔚 Final Thoughts
CrimeWise demonstrates a scalable, interpretable, and efficient ML pipeline to solve real-world problems like crime categorization, with potential applications for public safety, resource optimization, and predictive policing.

