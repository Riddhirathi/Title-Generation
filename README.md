# Title-Generation

This project focuses on building a deep learning model using LSTM (Long Short-Term Memory) networks for video title prediction. The model is trained on YouTube video titles and utilizes beam search for more coherent and meaningful title generation based on seed words.

## Project Overview

The main objective of this project is to generate meaningful video titles given an initial seed word or phrase. The dataset comprises titles from multiple YouTube datasets (US, CA, GB). 

### Features
- **Bidirectional LSTM**: To capture both forward and backward dependencies in the video titles.
- **Beam Search**: To explore multiple possible sequences for generating the most relevant title.
- **Temperature-based Sampling**: For controlling the randomness and creativity of the generated titles.
- **Data Cleaning and Preprocessing**: Handles non-English titles and noise in the text data.

## Tech Stack
- **Python**: Core programming language for data handling and model implementation.
- **TensorFlow/Keras**: Deep learning framework used to build the LSTM-based model.
- **NLTK**: Natural Language Toolkit used for stopword removal and text preprocessing.
- **Langdetect**: For filtering out non-English video titles from the dataset.
- **Pandas**: Data manipulation library for handling YouTube video datasets.
- **NumPy**: For numerical operations on sequences.

## How It Works
1. **Data Preprocessing**: Titles are cleaned, tokenized, and converted into padded sequences. Non-English titles are filtered out using the `langdetect` library.
2. **Model Training**: A bidirectional LSTM network with embedding layers and dropout is trained on the processed text data.
3. **Text Generation**: Given a seed word or phrase, the model generates a new title using beam search to explore multiple possible outputs and select the best one.
