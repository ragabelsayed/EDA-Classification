## **Machine Learning-based Classifier for [Datasets](https://www.kaggle.com/datasets/tariqmassaoudi/hespress)**

**Task Summary:**
In this project, we built a machine learning-based classifier to categorize datasets into different topics. The datasets contain information about Stories and including 'id', 'title', 'date', 'author', 'story', and 'topic'. The goal of this task was to train a classifier to automatically predict the topic of an article based on its content (text).

**Training Process:**
1. **Data Preparation and Splitting:**
   - Loaded the combined dataset containing story and their corresponding topics.
   - Split the data into training (80%) and test (20%) sets using scikit-learn's `train_test_split` function. The last 20% of each file was used as the test set to ensure a representative evaluation.

2. **Text Preprocessing:**
   - Preprocessed the text data by converting the stories' textual content into numerical representations using TF-IDF (Term Frequency-Inverse Document Frequency) vectorization. This process transformed the text into numerical features, which the classifier can understand.

3. **Classifier Selection and Training:**
   - Chose the Multinomial Naive Bayes classifier as the model for this multi-class classification task. The Naive Bayes algorithm is known to work well with text data.
   - Initialized the Multinomial Naive Bayes classifier using scikit-learn's `MultinomialNB`.
   - Trained the classifier on the training data using the `fit` method, which learned the underlying patterns and relationships between the text features and their corresponding topics.

4. **Model Evaluation:**
   - Evaluated the classifier's performance on the test set to assess its accuracy in predicting story topics.
   - Made predictions on the test set using the trained classifier's `predict` method.
   - Calculated various performance metrics for each class (topic) and the overall test data using scikit-learn's `classification_report` and `accuracy_score` functions.

5. **Interpretation of Metrics:**
   - Precision, Recall, and F1-score were calculated for each class (topic) in the dataset. These metrics provide insights into the classifier's ability to correctly predict stories for each topic and its ability to find all articles belonging to each class.
   - Accuracy was calculated to measure the overall correct predictions out of all predictions. It provides an overall performance measure for the entire test set.

6. **Enhancements for Better Results:**
   - Proposed several enhancements that can be explored to achieve better classifier performance, including hyperparameter tuning, using advanced classifiers, feature engineering, handling imbalanced data, ensemble methods, incorporating domain-specific features, and error analysis.
