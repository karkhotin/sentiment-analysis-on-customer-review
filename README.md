# Sentiment analysis on customer review
## 📌 Project task
This's is a case study demonstrating Long Short-Term Memory neural network. This project aims to build a sentiment analysis model to classify restaurant reviews from [Yelp dataset](https://www.tensorflow.org/datasets/catalog/yelp_polarity_reviews) into two sentiment categories as positive and negative, providing valuable insights into customer experiences.

## 📚 Dataset
The dataset used for this analysis is the [Yelp dataset](https://www.tensorflow.org/datasets/catalog/yelp_polarity_reviews) . It contains a collection of customer reviews from Yelp, including both the review text and a star rating. For the purpose of this project, the star ratings are converted into sentiment labels as follows:
  - **1:** Positive sentiment (3 or 4 stars)
  - **2:** Negative sentiment (1 or 2 stars)

## 🛠️ Build model
Implement text classification model using a recurrent neural network (LSTM-based architecture). Tokenization is applied to convert input text into sequences of word indices based on a predefined vocabulary. The model structure consists of the following layers:
  - `TextVectorization` - converts raw text into sequences of token indices
  - `Embedding` - captures semantic relationships between words
  - `Bidirectional LSTM` - allows the model to capture context from both the beginning and end of the sequence
  - `Dense` - a fully connected layer
  - `Dense` - applies a sigmoid activation function making the final prediction

The training process contains 9 epochs and calls `EarlyStopping` to prevent overfitting.

## 📊 Results
The model achieved the following performance on the test dataset:
  - **Accuracy** – 92.5%
  - **Loss** – 0.18

The model's ability to predict the sentiment of review was tested on a custom dataset. The model is saved in the folder `LSTMmodel.tf`
