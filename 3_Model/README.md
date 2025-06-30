# Model Definition and Evaluation

This directory contains the code and results for the model development phase of the project.  
All experiments and analyses are implemented in the [model_definition_evaluation.ipynb](model_definition_evaluation.ipynb) notebook.

## Content and Approach

The modeling and evaluation were carried out as follows:

- **Model Selection:**  
  Both traditional machine learning models (Logistic Regression, Naive Bayes, Linear SVM) and a deep learning approach with Embedding and Bidirectional LSTM were tested. The goal was to improve the baseline and compare different approaches.

- **Feature Engineering:**  
  Tweets were cleaned (lowercasing, removing URLs, usernames, hashtags, special characters, and numbers). For classical models, TF-IDF was used; for the neural network, tokenization and padding were applied.

- **Hyperparameter Tuning:**  
  For classical models, GridSearchCV was used with various parameters. For the neural network, dropout, L2 regularization, embedding dimension, LSTM units, and learning rate were tuned experimentally.

- **Implementation:**  
  Models were implemented in Python using scikit-learn and TensorFlow/Keras. For the neural network, EarlyStopping, ReduceLROnPlateau, and ModelCheckpoint were used.

- **Evaluation Metrics:**  
  Models were evaluated using accuracy, precision, recall, F1-score, and confusion matrix. For the neural network, training and validation curves were also plotted.

- **Comparative Analysis:**  
  The results of the classical models were compared with the neural network. The best performance was documented and it was discussed whether and how the baseline was surpassed.

## Usage

All steps, experiments, and evaluations are documented in [model_definition_evaluation.ipynb](model_definition_evaluation.ipynb).  
Please run the notebook to see the complete results and visualizations.

## Submission

All modeling and evaluation are performed exclusively in the notebook [model_definition_evaluation.ipynb](model_definition_evaluation.ipynb).