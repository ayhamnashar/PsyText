# Literature Review – Fake News Detection

Approaches or solutions that have been tried before on similar projects.

**Summary of Each Work**:

- **Source 1**: [BERT for Detecting Fake News in Social Media]

  - **Link**: [https://aclanthology.org/2020.trac-1.15/](https://aclanthology.org/2020.trac-1.15/)  
  - **Objective**: To explore the use of pretrained language models like BERT for detecting fake news.  
  - **Methods**: Fine-tuned BERT on a dataset of social media posts and compared it with LSTM and logistic regression baselines.  
  - **Outcomes**: BERT outperformed all baselines significantly, especially in terms of accuracy and F1-score.  
  - **Relation to the Project**: Justifies the use of transformer-based models like BERT within the TensorFlow ecosystem for this task.

- **Source 2**: [LIAR: A Benchmark Dataset for Fake News Detection]

  - **Link**: [https://aclanthology.org/P17-2067/](https://aclanthology.org/P17-2067/)  
  - **Objective**: To introduce and benchmark the LIAR dataset, a large-scale dataset for fake news detection with six graded truth labels.  
  - **Methods**: Utilized deep learning models such as CNNs and GRUs to classify short political statements.  
  - **Outcomes**: Showed that existing models often misclassify nuanced linguistic data and highlighted dataset difficulty.  
  - **Relation to the Project**: The LIAR dataset is suitable for model training and testing; also motivates the exploration of more powerful models like transformers.

- **Source 3**: [Fake News Detection on Social Media: A Data Mining Perspective]

  - **Link**: [https://arxiv.org/abs/1708.01967](https://arxiv.org/abs/1708.01967)  
  - **Objective**: To provide a comprehensive overview of techniques for detecting fake news using data mining and machine learning approaches.  
  - **Methods**: Categorizes approaches into content-based (text analysis, NLP) and social context-based methods (user behavior, network propagation).  
  - **Outcomes**: Found that NLP-based content analysis can be effective for early detection, but models struggle to generalize across domains.  
  - **Relation to the Project**: Offers insight into foundational techniques and emphasizes the importance of considering both content and metadata.
