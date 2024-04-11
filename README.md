
# Disaster_Automated_Form_Filling


# Tweet Preprocessing 

Python script provides a comprehensive set of functions for preprocessing Twitter data. It's designed to clean and normalize tweet text, making it suitable for further analysis or machine learning tasks.

## Features

- Remove Unicode characters
- Remove hashtags from words
- Remove @user mentions
- Remove URLs and links
- Remove emojis and emoticons
- Normalize punctuation (e.g., multiple exclamation marks)
- Remove stopwords
- Convert text to lowercase
- Remove short words (2-3 letters)
- Identify and extract location entities

## Dependencies

- NLTK
- spaCy
- locationtagger

## Setup

1. Clone the repository:
ggit clone https://github.com/NGswati/Disaster_Automated_Form_Filling
.git
cd Disaster_Automated_Form_Filling
unzip zip se project.zip

3. Install the required dependencies:
pip install nltk spacy locationtagger

4. Download necessary NLTK data:
import nltk
nltk.download(['punkt', 'stopwords', 'maxent_ne_chunker', 'words', 'treebank', 'maxent_treebank_pos_tagger', 'averaged_perceptron_tagger'])

Download spaCy model:
Copypython -m spacy download en_core_web_sm


## Usage

Place your input CSV file in the same directory as the script.
Update the input and output file names in the script:
pythonCopyfile_ = open("your_input_file.csv", "r", encoding="utf8", errors='replace').read()
pythonCopywith open("your_output_file.csv", "w", encoding="utf8", errors='replace') as file:
Run the script:
python tweet_preprocessing.py

The processed tweets will be saved in the output file specified.

## Customization
You can customize the preprocessing steps by modifying the processing_functions list in the script. Add or remove functions as needed for your specific use case.

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

This README provides a comprehensive overview of the tweet preprocessing tool, including its features, setup instructions, and usage guide. It's formatted in a way that's easy to read on GitHub and provides potential users with all the necessary information to get started with the tool.


# Disaster Tweet Classification

A comprehensive machine learning project for classifying disaster-related tweets using various algorithms.

## Table of Contents
- [Features](#features)
- [Dependencies](#dependencies)
- [Setup](#setup)
- [Usage](#usage)
- [Data](#data)
- [Models](#models)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Features

- Data preprocessing and TF-IDF vectorization
- Implementation of multiple classification algorithms
- Comparison of model performances

## Dependencies

- pandas
- scikit-learn
- nltk
- tensorflow
- keras
- lightgbm
- xgboost

## Setup

1. Clone the repository:
git clone https://github.com/NGswati/Disaster_Automated_Form_Filling
.git
cd Disaster_Automated_Form_Filling
cd Classification_models.ipynb
3. Install the required dependencies:
pip install -r requirements.txt


## Usage

Update the csv_file_path variable in the script with the path to your dataset.
Run the script:
python disaster_classification.py


## Data
The script expects a CSV file with the following columns:

tweets: containing the tweet text
category: containing the category label for each tweet

## Models
The following models are implemented and compared:

Decision Tree
Random Forest
SGD Classifier
Naive Bayes (Multinomial)
Logistic Regression
Deep Neural Network (DNN)
Long Short-Term Memory (LSTM)
AdaBoost
LightGBM
XGBoost

## Results
The script outputs accuracy scores and classification reports for each model. Example output:
Model: Decision Tree
Accuracy: 0.85
...

Model: LSTM
Accuracy: 0.92
...
## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## Fork the project
Create your feature branch (git checkout -b feature/AmazingFeature)
Commit your changes (git commit -m 'Add some AmazingFeature')
Push to the branch (git push origin feature/AmazingFeature)
Open a Pull Request

## License
This project is licensed under the MIT License - see the LICENSE file for details.
This README follows GitHub's recommended format, including a table of contents, clear sections, and co


# Disaster Assessment Question Answering System
Python script implements a question answering system for disaster assessment, designed to process tweets and answer questions based on the tweet content.

## Features

- Parses tweets from a file
- Processes questions and extracts relevant information
- Uses natural language processing techniques to analyze text
- Implements various rules for different question types (what, when, where, why)
- Scores and ranks potential answers
- Outputs the best answer for each question

## Dependencies

- nltk
- spacy
- string

## Setup

1. Clone the repository:
git clone https://github.com/NGswati/Disaster_Automated_Form_Filling
.git
cd Disaster_Automated_Form_Filling
unzip Disaster_Automated_Form_Filling.zip


3. Install the required dependencies:
pip install nltk spacy

4. Download the necessary NLTK and spaCy data:
import nltk
nltk.download('punkt')
nltk.download('averaged_perceptron_tagger')
nltk.download('stopwords')
import spacy
spacy.cli.download("en_core_web_sm")

5. Prepare the input files:

Tweet file: A CSV file containing the tweets
Question file: A CSV file containing the questions
Semantic class files: Text files containing lists of names, locations, months, etc.



## Usage

Update the file paths in the main() function:

- input_path: Path to the directory containing input files
- semantic_classes(): Path to the directory containing semantic class files
- questions_file: Path to the questions CSV file
- tweet_dict: Path to the tweets CSV file


## Run the script:
python disaster_qa.py

The script will process each question and output the question ID along with the best answer found.

## Functions

parse_tweet(): Parses the tweet file
cat_tweet(): Categorizes tweets 
extract_emphasized_phrases(): Extracts important phrases from questions
AddTagPOS(): Adds part-of-speech tags to tweets
semantic_classes(): Loads semantic class data
when_rule(), what_rule(), why_rule(), where_rule(): Implement scoring rules for different question types
wordMatch(): Calculates word matching score between question and potential answer
data_forward(): Main processing function for questions and answers

## Note
This script is designed for a specific format of input data and may require modifications to work with different data structures or sources.
