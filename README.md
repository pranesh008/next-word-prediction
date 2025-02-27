# Next Word Prediction using Trigram Model

## Overview
This project implements a Next Word Prediction system using a trigram language model. The system processes a given corpus, cleans and tokenizes the text, constructs a trigram-based language model, and predicts the next word based on user input.

## Features
- Preprocesses text by normalizing, removing punctuation, and performing lemmatization.
- Constructs a trigram-based language model using `nltk`.
- Predicts the next word based on user input using a Conditional Frequency Distribution (CFD).
- Allows users to generate additional words iteratively.

## Technologies Used
- Python
- Natural Language Toolkit (NLTK)
- Regular Expressions (re)
- Random module for weighted probability selection

## Installation
### Prerequisites
Ensure you have Python installed along with the following dependencies:
```sh
pip install nltk
```

### NLTK Downloads
Run the following commands to download necessary NLTK resources:
```python
import nltk
nltk.download('punkt')
nltk.download('wordnet')
```

## How to Use
1. Place your corpus text file in the same directory as the script and name it `corpus.txt`.
2. Run the script:
```sh
python next_word_prediction.py
```
3. Enter a phrase when prompted.
4. The model will predict the next word(s) based on the trained trigram model.
5. You can choose to generate additional words iteratively.

## Project Structure
```
├── next_word_prediction.py  # Main script
├── corpus.txt               # Input text file (must be provided)
└── README.md                # Project documentation
```

## Code Explanation
### Text Preprocessing
- The `filter(text)` function normalizes text, removes HTML tags, punctuation, and converts it to lowercase.
- The `clean(text)` function tokenizes words and applies lemmatization.

### Model Building
- The `n_gram_model(text)` function constructs a trigram-based model using Conditional Frequency Distribution (CFD) to store word probabilities.

### Prediction
- The `predict(model, user_input)` function predicts the most likely next word based on input, using weighted random selection from the trigram model.
- The user is prompted to continue generating additional words.

## Example Output
```
Enter a phrase: machine learning is
Trigram model predictions: ['fun', 'useful', 'challenging']
machine learning is fun
Do you want to generate another word? (type 'y' for yes or 'n' for no): y
machine learning is fun and
```

## Future Improvements
- Extend to larger n-grams (e.g., 4-gram, 5-gram models).
- Implement deep learning models (LSTMs, Transformers) for improved accuracy.
- Integrate with a chatbot or real-time typing assistant.

## License
This project is open-source under the MIT License.

## Author
Pranesh Puri

