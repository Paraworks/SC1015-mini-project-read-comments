# About
Many social media platforms are filled with a large number of harmful comments, and we cannot rely solely on single label(whether they are harmful) to judge these comments. Since such a simple binary judgment would compromise the fairness of the review process, we will attempt multi-label prediction to pursue better performance.

# Problem Definition
I.What are the predictive performances of different models on multi-label text comments?
II.Can we create a suitable prediction program so that users can determine whether comments are toxic based on the model?

# Introduction

In this project, we will analyze a dataset containing comments that may be toxic. Our goal is to train a model that can effectively predict whether a comment is harmful. We will be using the sklearn library to preprocess the dataset, create features, train the model, and evaluate the performance. We will compare the performance of different models for both multi-label prediction and single-label prediction.

# [Dataset](https://www.kaggle.com/datasets/fizzbuzz/cleaned-toxic-comments)

The dataset we are using is `train_preprocessed.csv`, which consists of comments and their respective labels. These labels include 'identity_hate', 'insult', 'obscene', 'severe_toxic', 'threat', and 'toxic'. Each comment is annotated with binary values for each label, indicating whether the comment is considered toxic under that category.

# Compare the proformence of different model

In [Models_comparison.ipynb](https://github.com/Paraworks/SC1015-mini-project-detecting_toxic_comments/blob/main/Models_comparison.ipynb),we will verify the feasibility of multi-label prediction. We predicted for different labels and found that both multi-label prediction and single-label prediction have an accuracy of over 90%.

## [mini_proj.ipynb](https://github.com/Paraworks/SC1015-mini-project-detecting_toxic_comments/blob/main/mini_proj.ipynb)
# Preprocessing and Feature Extraction

We will be using the `CountVectorizer` class from the sklearn library to convert the comments into a matrix of token counts. This representation will serve as the input features for our model. The labels will remain unchaned.

# Model Training for EDA

We will be using the `OneVsRestClassifier` from the sklearn library with `LogisticRegression` as the base classifier. This approach enables the model to predict multiple labels for each comment.

# Deep learning model

We will be using tenserflow in order to predict the same dataset in order to see which one is more effective.

# Conclusion

Utilizing a limited training set comprising merely 150,000 data instances, our models have successfully demonstrated a predictive accuracy exceeding 90%.

# [Simple application](https://github.com/Paraworks/SC1015-mini-project-detecting_toxic_comments/blob/main/core.ipynb)

This is a simple executable program that can be used directly to detect whether comments are toxic.By perdicting more than six labels. We can develop a weighted filtering mechanism to screen these harmful comments.



# Members 
Zhang Jiahua
Quan caiyong
Gu Shucheng
# Reference
https://www.kaggle.com/datasets/fizzbuzz/cleaned-toxic-comments
https://www.tensorflow.org
https://scikit-learn.org
