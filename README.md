

# Telugu and Nepali Text Classification

This project focuses on text classification tasks using **Telugu** and **Nepali** social media comments and posts. The goal is to classify the text as either **abusive** or **non-abusive** using different machine learning and deep learning models. The models are trained using **mBERT-generated embeddings** and evaluated on various metrics, including accuracy, precision, recall, and F1-score.

## **Preprocessing Steps**

### **Telugu Text Preprocessing**
1. **Unicode Normalization**: The Telugu text is normalized using the NFKC form to ensure consistent encoding and representation of characters.
2. **Cleaning**: All non-Telugu characters, special symbols, emojis, and irrelevant punctuation are removed. Only Telugu characters in the Unicode range (`\u0C00-\u0C7F`) are retained, and extra spaces and newlines are eliminated.
3. **Tokenization**: The **mBERT tokenizer** is used to tokenize the cleaned text into subword units and generate **768-dimensional embeddings**.
4. **Lowercasing**: Any Latin-script text (e.g., foreign words or usernames) is converted to lowercase.
5. **Stopword Removal**: A stopword list is applied to remove common words that do not contribute to the meaning of the text.

### **Nepali Text Preprocessing**
1. **Unicode Normalization**: Nepali text is normalized using the NFKC form to handle inconsistencies in encoding.
2. **Cleaning**: Non-Nepali characters, emojis, and punctuation are removed, leaving only Nepali characters within the Unicode range (`\u0900-\u097F`).
3. **Tokenization**: **mBERT** tokenizes the cleaned Nepali text and generates **768-dimensional embeddings** for each token.
4. **Lowercasing**: Latin-script text (such as hashtags and foreign names) is converted to lowercase.
5. **Stopword Removal**: Common Nepali stopwords are removed using a custom stopword list.

## **Models Used**
This project includes the following classification models for text classification:
- **Logistic Regression**
- **Support Vector Machine (SVM)**
- **Random Forest**
- **Neural Network (MLP)**
- **Convolutional Neural Network (CNN)**
- **Long Short-Term Memory (LSTM)**

Each model is trained using **768-dimensional mBERT embeddings** of the preprocessed text data. The performance of these models is evaluated on both Telugu and Nepali datasets using **accuracy**, **precision**, **recall**, and **F1-score**.

