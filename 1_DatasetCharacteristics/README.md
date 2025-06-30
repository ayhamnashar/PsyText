
# Dataset Characteristics

**[Notebook](exploratory_data_analysis.ipynb)**

# 🧠 Hate Speech Detection – Exploratory Data Analysis (EDA)

This document provides a structured overview of the exploratory data analysis performed on the **Hate Speech and Offensive Language Dataset**, used for training and evaluating machine learning models in the task of hate speech classification.

---

## 📊 Dataset Overview

The dataset consists of tweets annotated for hate speech, offensive language, or neither. Key details:

- **Source**: [Hate Speech and Offensive Language Dataset (Davidson et al., 2017)](https://arxiv.org/abs/1703.04009)  
- **Number of Samples**: ~25,000  
- **Number of Features**: Common features include `tweet`, `class`, and optional metadata like `user`, `count`, etc.  
- **Label Distribution**: The `class` column is multiclass:
  - `0` = Hate Speech  
  - `1` = Offensive Language  
  - `2` = Neither  

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

- **Findings**: Minimal or no missing values were observed.  
- ✅ Dataset is clean and suitable for preprocessing.

---

## 📈 Feature Distributions

A breakdown of major feature distributions:

- **Label Balance**:
```python
sns.countplot(x='class', data=df)
```
The dataset is **imbalanced**, with the majority of tweets labeled as offensive language.

- **Tweet Length Distribution**:
```python
df['tweet_length'] = df['tweet'].apply(len)
sns.histplot(df['tweet_length'], bins=50)
```
Tweet lengths are short, consistent with Twitter’s character limit. Most tweets range from 20 to 120 characters.

---

## ⚠️ Possible Biases

Potential sources of bias considered:

- **Class Imbalance**: Overrepresentation of offensive language may affect classifier fairness.  
- **Linguistic Bias**: Certain dialects or slang could be misclassified as hate speech.  
- **Annotation Subjectivity**: Judging offensiveness is inherently subjective, potentially introducing human labeling bias.

Careful model evaluation with fairness metrics is recommended due to these concerns.

---

## 🔗 Correlations

A correlation heatmap was generated to analyze relationships between numerical features (e.g., retweet count, user-level metadata):

```python
sns.heatmap(df.corr(numeric_only=True), annot=True)
```

- Weak linear correlations between label and numeric metadata.
- For semantic patterns, advanced NLP techniques (e.g., embeddings, transformers) will be required.

---

## 📌 Conclusion

The dataset is clean and well-structured for hate speech classification. While traditional correlations are weak, deep learning models like BERT can capture complex patterns in language that distinguish between hate speech, offensive content, and neutral language. Next steps include preprocessing, class rebalancing, and training using modern NLP models.
