# Sentiment Analysis Using RNN Models
This project implements sentiment analysis on the IMDB movie review dataset using different types of Recurrent Neural Network (RNN) architectures, including Simple RNN, GRU, LSTM, and Bidirectional LSTM. The goal is to classify movie reviews as either positive or negative based on their textual content.

## Dataset
- **Dataset Name**: IMDB Movie Review Dataset
- **Description:**
      - The IMDB dataset contains 50,000 movie reviews, evenly distributed between positive and negative sentiments.
Preprocessed data includes integer encoding of words with the top 5,000 most frequent words retained.
Reviews are padded to a uniform length of 400 words for input compatibility.

## Models Used
- **Simple RNN**: A basic recurrent neural network model using a single RNN layer.
- **GRU (Gated Recurrent Unit):** A variant of RNN designed to address the vanishing gradient problem.
- **LSTM (Long Short-Term Memory):** A specialized RNN designed to capture long-term dependencies in sequential data.
- **Bidirectional LSTM:** An extension of LSTM that processes the input sequence in both forward and backward directions.

## Features
- **Embedding Layer:**
Converts word indices into dense vector representations of a fixed length (32).
- **Sequence Length:**
All input sequences are padded to a maximum length of 400 words.
- **Output Layer:**
A Dense layer with a sigmoid activation function for binary classification (positive or negative sentiment).

## Evaluation Metrics
- **Loss Function:** Binary Crossentropy
Measures the difference between predicted and true labels for binary classification.
- **Optimizer:** Adam
Adaptive learning rate optimizer.
- **Metrics:** Accuracy
Used to evaluate the model's performance on training and test data.

## Training Details
- **Batch Size:** 64
- **Epochs:** 10
- **Validation:** A subset of the training data (64 samples) was used for validation during training.
- **Preprocessing:**
        - Padded sequences ensure uniformity in input length.
        - Vocabulary size limited to the 5,000 most frequent words.

## Conclusion
The project compares the performance of different RNN architectures in classifying sentiments from movie reviews. Each model has its own strengths:
- Simple RNN provides a straightforward approach but may struggle with long-term dependencies.
- GRU and LSTM effectively handle vanishing gradients and long-term dependencies.
- Bidirectional LSTM further enhances the performance by processing the input sequence in both forward and backward directions.
