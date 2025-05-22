# Dataset Characteristics

**[Notebook](exploratory_data_analysis.ipynb)**


# 🧠 Fake News Detection – Exploratory Data Analysis (EDA)

This document provides a structured overview of the exploratory data analysis performed on the **WELFake** dataset, used for training and evaluating machine learning models in the task of fake news classification.

---

## 📊 Dataset Overview

The dataset consists of a collection of labeled news articles designed for fake news detection. Key details:

- **Source**: WELFake dataset  
- **Number of Samples**: ~72,000  
- **Number of Features**: 4 (title, text, label, and id)  
- **Label Distribution**: The `label` column is binary, where:  
  - `0` = Fake  
  - `1` = Real  

Example row:
```python
df.head()
```

---

## ❓ Missing Values

Missing values were checked across all columns.

```python
df.isnull().sum()
```

- **Findings**: No missing values were found in the dataset.  
- ✅ Clean dataset ready for preprocessing.

---

## 📈 Feature Distributions

A breakdown of major feature distributions:

- **Label Balance**:
```python
sns.countplot(x='label', data=df)
```
The dataset is relatively **balanced** between fake and real news.

- **Text Length Distribution**:
```python
df['text_length'] = df['text'].apply(len)
sns.histplot(df['text_length'], bins=50)
```
Most articles fall within a moderate length range, with outliers present on both ends.

---

## ⚠️ Possible Biases

Potential sources of bias considered:

- **Source Bias**: Limited source diversity might affect generalization.  
- **Length Bias**: Fake vs. real articles may have different average lengths.  
- **Lexical Bias**: Certain words may be overrepresented in one class.

Due to the absence of metadata like author or publication, deeper source-level bias could not be analyzed.

---

## 🔗 Correlations

A correlation heatmap was generated to analyze relationships between numerical features:

```python
sns.heatmap(df.corr(), annot=True)
```

- The `label` column has no strong linear correlation with available features.  
- NLP techniques (e.g., TF-IDF, word embeddings) will be required for more meaningful feature extraction.

---

## 📌 Conclusion

The dataset is clean and well-suited for text classification tasks. Although linear correlations are minimal, deep NLP modeling such as BERT or LSTM will help uncover more meaningful patterns between text and labels. Next steps involve preprocessing, feature engineering, and model development using TensorFlow.
