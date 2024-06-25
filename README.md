# Spam Detection in SMS Messages

This project presents an analysis of SMS Spam Messages sourced from the UCI dataset, utilising fundamental NLP techniques for data preprocessing. Implemented in R, it explores a range of machine learning models to investigate their impact on classification accuracy and model efficacy in categorising messages as spam or ham (non-spam). By evaluating the performance metrics of each model, we aim to identify the optimal method optimal for spam detection.

## Installation

This script requires R and the following libraries:

- e1071 (build Naive Bayes and SVM models)
- ggplot2 (statistical data visualisation)
- ranger (build optimised random forests)
- rpart (build decision trees)
- textstem (text processing such as lemmatisation)
- tm (text processing such as removing redundant characters)
- wordcloud (generate word clouds)

```bash
install_packages("e1071")
install_packages("ggplot2")
install_packages("ranger") 
install_packages("rpart")
install_packages("textstem")
install_packages("tm") 
install_packages("wordcloud")
```

## Usage

To view the project, follow these steps:
- Clone the repository or download it as a zip folder and extract all files.
- Ensure you have installed the required libraries.
- Run the Spam_Detection.Rmd Markdown script.

## Methodology

**Data Collection**
- The SMS Spam Messages dataset is publicly available and can be downloaded from [Kaggle](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset).

**Data Preprocessing**
   - Read in the SMS Spam Messages dataset (spam.csv), which contains 5,572 messages of various lengths.
   - Split the dataset into training and test sets.
   - Carry out standard NLP methods such as removing punctuation, stop words, and perform lemmatisation.
   - Convert dataset into a feature matrix for model interpretation.

**Data Visualisation**
   - View message lengths by numbers of characters and words.
   - Examine numeric and non-alphanumeric characters.
   - Generate word clouds to see the most common words across spam and ham messages.

**Model Selection**

Several model architectures were considered:
   - Model 1: Naive Bayes Classifier.
   - Model 2: Decision Tree.
   - Model 3: Random Forest.
   - Model 4: SVM (Linear Kernel).

**Evaluation Metrics**
   - The primary metric used to evaluate model performance was accuracy on the test set.
   - Confusion matrices, sensitivity, and specificity among other metrics were also computed to assess the model's ability to correctly classify each message.

## Results
Despite **SVM (linear kernel)** showing strong performance with **99.28%** accuracy on the SMS Spam Detection dataset, its reliability is limited by data dating back to 2006–2007 from the UK, Singapore, and the US. The dataset's reliance on user-reported data introduces bias and restricts its applicability beyond specific regional contexts. To improve model generalisability, a more diverse and current dataset is essential.

## References
- Almeida, T.A., & Hidalgo, J.M.G. (2011). UCI Machine Learning Repository: SMS Spam Collection Data Set. [Kaggle](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset)/[Original Link](https://archive.ics.uci.edu/ml/datasets/SMS+Spam+Collection).
