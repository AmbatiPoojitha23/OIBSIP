# Task 4 — Sentiment Analysis

## 📌 Project Overview

This project focuses on building a Machine Learning model to classify text into three sentiment categories:

* Positive
* Negative
* Neutral

The objective is to analyze customer/public feedback and automatically identify the sentiment expressed in text.

## 🎯 Objective

Build a sentiment classification system using Natural Language Processing (NLP) and Machine Learning techniques. The project demonstrates text preprocessing, feature extraction using TF-IDF, model training, evaluation, visualization, and error analysis.

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* NLTK
* Matplotlib
* Seaborn
* WordCloud
* Jupyter Notebook

## 📂 Dataset

The project uses `sentiment_dataset.csv`.

The dataset contains:

* **1,100 text records**
* **2 columns**

  * `text` — customer/review text
  * `sentiment` — sentiment label

The sentiment labels are:

* `positive`
* `negative`
* `neutral`

## 🔄 Project Workflow

### 1. Data Loading and Inspection

The dataset is loaded using Pandas and inspected for:

* Dataset shape
* Data types
* Missing values
* Duplicate records
* Sentiment class distribution

Duplicate and missing records are removed before further processing.

### 2. Text Preprocessing

The following preprocessing steps are applied:

1. Lowercasing text
2. Removing punctuation
3. Removing digits
4. Tokenization
5. Stopword removal
6. Stemming using NLTK's Porter Stemmer

The cleaned text is then used for feature extraction.

### 3. TF-IDF Feature Extraction

TF-IDF (Term Frequency-Inverse Document Frequency) converts text into numerical features that Machine Learning algorithms can understand.

TF-IDF gives higher importance to words that are frequent in a particular document but relatively rare across the entire dataset.

The project uses:

* Maximum 5,000 features
* Unigrams and bigrams
* Minimum document frequency of 2

### 4. Train/Test Split

The dataset is divided into:

* **80% Training Data**
* **20% Testing Data**

Stratified splitting is used to maintain the sentiment distribution in both datasets.

### 5. Machine Learning Models

Three classification models are trained:

#### Multinomial Naive Bayes

A fast probabilistic classifier commonly used for text classification.

#### Logistic Regression

A linear classification algorithm that performs well with high-dimensional TF-IDF text features.

#### Linear SVM

A Support Vector Machine classifier suitable for sparse, high-dimensional text data.

### 6. Model Evaluation

The models are evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

The models are compared using their performance metrics to identify the best-performing classifier.

## 📊 Visualizations

The project includes the following visualizations:

### Sentiment Distribution

Shows the number of positive, negative, and neutral reviews.

![Sentiment Distribution](sentiment_distribution.png)

### WordCloud

Word clouds are generated separately for positive, negative, and neutral reviews to identify frequently occurring words.

![Word Clouds](wordclouds.png)

### Confusion Matrices

Confusion matrices are used to compare actual and predicted sentiment classes for each Machine Learning model.

![Confusion Matrices](confusion_matrices.png)

### Model Comparison

A comparison chart is used to compare Accuracy, Precision, Recall, and F1-score across the trained models.

![Model Comparison](model_comparison.png)

## 🔍 Error Analysis

Five misclassified examples are examined from the test dataset.

Common reasons for misclassification include:

* Ambiguous text
* Short reviews
* Mixed sentiments
* Similar vocabulary between sentiment classes
* Difficulty understanding sarcasm or implicit sentiment
* Vocabulary overlap after stemming

These limitations demonstrate that traditional TF-IDF-based models mainly rely on word statistics and do not fully understand sentence context.

## 🏆 Conclusion

This project demonstrates how NLP and Machine Learning can be used to automatically classify customer or public feedback into positive, negative, and neutral categories.

Naive Bayes provides a fast and effective baseline, while Logistic Regression and Linear SVM provide strong performance on TF-IDF features.

The best-performing model is selected based on the weighted F1-score obtained during evaluation.

## 🌍 Real-World Applications

Sentiment analysis can be used for:

* Customer feedback analysis
* Product review analysis
* Social media monitoring
* App reviews
* Customer support ticket classification
* Brand reputation monitoring
* Market research

## 📁 Files

| File                             | Description                    |
| -------------------------------- | ------------------------------ |
| `Task4_Sentiment_Analysis.ipynb` | Complete Jupyter Notebook      |
| `sentiment_dataset.csv`          | Sentiment analysis dataset     |
| `sentiment_distribution.png`     | Sentiment distribution chart   |
| `wordclouds.png`                 | Word clouds for each sentiment |
| `confusion_matrices.png`         | Model confusion matrices       |
| `model_comparison.png`           | Model performance comparison   |

## 👩‍💻 Author

**Ambati Poojitha**

B.Tech — Computer Science and Engineering
2022–2026

## ⭐ Project Type

Oasis Infobyte Data Science Internship — Task 4
