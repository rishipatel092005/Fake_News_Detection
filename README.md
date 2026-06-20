# News Credibility Classifier using Machine Learning

## Overview
This project focuses on detecting whether a news article is **Fake or Real** using Natural Language Processing (NLP) and Machine Learning techniques.  
The system takes textual input (news headline or article) and predicts its authenticity along with a confidence score.

---

## Problem Statement
With the rapid spread of misinformation online, it has become important to automatically verify the authenticity of news.  
This project aims to build a classification model that can assist in identifying fake news based on textual patterns.

---

## Tech Stack
- Python  
- Scikit-learn  
- Pandas, NumPy  
- NLP techniques (Tokenization, Stemming, TF-IDF)

---

## Dataset
- Dataset used: **LIAR dataset**
- Originally contains multiple classes (True, Mostly-True, Half-True, etc.)
- Converted into **binary classification**:
  - True → Real News  
  - False → Fake News  

- Used only relevant columns:
  - Statement (text)
  - Label (True/False)

---

## Methodology

### 1. Data Preprocessing
- Removed unnecessary characters and noise  
- Tokenization of text  
- Applied stemming to reduce words to root form  

### 2. Feature Extraction
- Used **TF-IDF (Term Frequency - Inverse Document Frequency)**  
- Converted text data into numerical vectors  

### 3. Model Training
Trained and compared multiple models:
- Logistic Regression  
- Naive Bayes  
- Support Vector Machine (SVM)  
- Random Forest  

### 4. Model Selection
- Compared models using F1-score and accuracy  
- **Logistic Regression** performed best and was selected  

### 5. Prediction System
- Saved trained model  
- Takes user input (news text)  
- Outputs:
  - Prediction (Fake / Real)  
  - Probability score  

---

## Project Workflow
Input News → Preprocessing → TF-IDF → Model → Prediction

---

## Results
- Achieved approximately **70% accuracy**  
- Evaluated using:
  - F1 Score  
  - Confusion Matrix  

---

## Project Structure
- `DataPrep.py` → Data cleaning and preprocessing  
- `FeatureSelection.py` → Feature extraction using TF-IDF  
- `classifier.py` → Model training and evaluation  
- `prediction.py` → Final prediction system  

---

## Setup

Install required libraries:
pip install scikit-learn numpy scipy pandas
## Libraries Used
- pandas → data handling and preprocessing  
- numpy → numerical operations  
- scikit-learn → machine learning models (Logistic Regression, SVM, Naive Bayes)  
- scipy → scientific computations  
- nltk (optional if used) → text preprocessing (tokenization, stemming)

```md
  ## Project Flow
+----------------------+
|   Input News Text    |
| (Headline/Article)   |
+----------+-----------+
           |
           v
+------------------------------+
|     Text Preprocessing       |
| - Remove noise (URLs, etc.)  |
| - Tokenization               |
| - Stopword removal           |
| - Stemming                   |
+--------------+---------------+
               |
               v
+------------------------------+
|   Feature Extraction (TF-IDF)|
| Convert text → numerical data|
+--------------+---------------+
               |
               v
+------------------------------+
|        Model Training        |
| - Logistic Regression       |
| - Naive Bayes               |
| - SVM                       |
| - Random Forest             |
+--------------+---------------+
               |
               v
+------------------------------+
|  Model Evaluation & Selection|
| - Accuracy                  |
| - F1 Score                  |
| - Confusion Matrix          |
| Select Best Model           |
+--------------+---------------+
               |
               v
+------------------------------+
|      Prediction System       |
| Takes new input text         |
+--------------+---------------+
               |
               v
+------------------------------+
|            Output            |
| Fake / Real + Probability   |
+------------------------------+


