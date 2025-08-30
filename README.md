### Spam Classifier
This project provides a machine learning solution to classify SMS messages as "spam" or "ham" using a Naive Bayes model.

#### Methodology
1.  **Data Cleaning**: Dropped irrelevant columns, renamed the remaining ones, and removed duplicate entries. The 'target' column was converted to a numerical format for model processing.
2.  **Exploratory Data Analysis (EDA)**: Analyzed message length, word count, and sentence count. The data was found to be imbalanced, with 'spam' messages generally being longer than 'ham' messages.
3.  **Text Preprocessing**: The text data was cleaned and prepared for the model through lowercasing, tokenization, removing special characters and stop words, and stemming. The **TfidfVectorizer** was used to convert the text into numerical features.
4.  **Model Building**: The preprocessed data was split into training and testing sets. Three Naive Bayes classifiers—GaussianNB, MultinomialNB, and BernoulliNB—were evaluated. **BernoulliNB** achieved the best precision score, which is a key metric for imbalanced datasets like this one.
5.  **Deployment**: The trained `MultinomialNB` model and the `TfidfVectorizer` were saved as pickle files (`model.pkl` and `vectorizer.pkl`) for easy deployment.

This project offers a robust and effective approach to spam detection in SMS messages.
