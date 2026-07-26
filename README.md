# RNN-LSTM
🧠 Next Word Prediction using LSTM (Recurrent Neural Network)

📌 Project Overview

This project builds a Next Word Prediction model using a Long Short-Term Memory (LSTM) network. The objective is to train a deep learning model that learns the sequence of words in a text and predicts the most probable next word given a short input sequence.

Unlike traditional machine learning models that treat each observation independently, LSTMs are designed to understand the order and context of sequential data, making them well suited for Natural Language Processing (NLP) tasks.

---

🎯 Business Problem

Many modern applications require intelligent text prediction to improve user experience and typing efficiency. Examples include:

- Mobile keyboard word suggestions
- Search engine query completion
- Chatbot response generation
- Email auto-completion
- Content writing assistance

The goal of this project is to demonstrate how an LSTM model can learn language patterns and generate meaningful next-word predictions.

---

📂 Dataset

A sample text corpus was used to train the language model.

The text was processed into sequences of words so that the model could learn how words naturally follow one another in a sentence.

---

⚙️ Data Preprocessing

Several preprocessing steps were performed before training the model.

• Converted text to lowercase

All words were converted to lowercase to ensure that words such as "Data" and "data" were treated as the same token.

• Removed punctuation

Punctuation marks were removed so that only meaningful textual information remained.

• Removed stop words

Common words that contribute little to learning meaningful language patterns were removed.

• Generated word sequences

The cleaned text was converted into ordered sequences of words. These sequences became the training samples where previous words were used to predict the next word.

• Tokenization

Keras Tokenizer converted every unique word into an integer representation. Neural networks work with numerical values, making tokenization an essential step.

• One-Hot Encoding

Target words were transformed into categorical vectors using one-hot encoding so the model could perform multi-class classification over the vocabulary.

---

🧠 Model Architecture

The neural network consists of the following layers:

- Embedding Layer to convert word indices into dense vector representations.
- First LSTM layer with 150 units to capture sequential relationships.
- Second LSTM layer with 150 units to learn deeper contextual patterns.
- Dense hidden layer with ReLU activation for additional feature learning.
- Output Dense layer with Softmax activation to predict the probability of every word in the vocabulary.

The model was trained for 100 epochs to learn language patterns from the training corpus.

---

📊 Model Outcome

After training, the model successfully learned relationships between words and was able to predict the most likely next word based on an input sequence.

The prediction process involves:

- Accepting a sequence of input words.
- Tokenizing the input.
- Passing the sequence through the trained LSTM model.
- Returning the word with the highest predicted probability.

This demonstrates how recurrent neural networks can capture contextual information and generate meaningful text predictions.

---

🛠️ Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- NLP Preprocessing
- Tokenizer
- LSTM (Recurrent Neural Network)

---

🚀 Key Learning Outcomes

- Understood the importance of text preprocessing for NLP.
- Learned how tokenization converts words into numerical representations.
- Built sequence data suitable for recurrent neural networks.
- Implemented an Embedding layer to learn semantic word representations.
- Designed a stacked LSTM architecture for sequence learning.
- Performed next-word prediction using a trained language model.
- Gained practical experience in building sequence-based deep learning models for NLP applications.
