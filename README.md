# Sentiment Analysis Project

This project performs sentiment analysis on a dataset of tweets using a BERT pre-trained model. The analysis classifies text into different emotions, including "Very Sad," "Sad," "Neutral," "Happy," and "Very Happy."

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Model](#model)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)

## Introduction
Sentiment analysis is a powerful tool used to determine the emotional tone behind a body of text. In this project, we use a BERT-based model to classify tweets into five emotion categories: "Very Sad," "Sad," "Neutral," "Happy," and "Very Happy."

## Dataset
The dataset used in this project consists of tweets, each labeled with various features such as year, month, day, time, platform, and sentiment. The original sentiment labels (e.g., "1 star" to "5 stars") were converted to emotions for more intuitive analysis.

### Data Preprocessing
The dataset was preprocessed by dropping irrelevant columns and applying the sentiment analysis model to the text column to generate emotion labels.

## Model
The sentiment analysis model used in this project is based on the BERT architecture, specifically the `nlptown/bert-base-multilingual-uncased-sentiment` model from Hugging Face. The model predicts a sentiment score that is then mapped to an emotion using a predefined dictionary.

## Installation
To run this project locally, you'll need to have Python installed along with the necessary libraries. You can install the required dependencies using pip:

```bash
pip install pandas transformers
```

## Usage
1. Clone this repository:
    ```bash
    git clone https://github.com/yourusername/sentiment-analysis.git
    cd sentiment-analysis
    ```

2. Place your dataset in the project directory and ensure it's named `sentiment_analysis.csv`.

3. Run the sentiment analysis script:
    ```bash
    python sentiment_analysis.py
    ```

4. The script will output the dataset with emotion labels and save it to `sentiment_analysis_results.csv`.

## Results
The output of the analysis is a CSV file where each tweet is associated with an emotion label, providing insights into the overall sentiment of the dataset.

### Example of Results
Here’s an example of the dataset before and after applying sentiment analysis:

**Before:**
| Text | Year | Month | Day | Time of Tweet | Platform | Sentiment |
|------|------|-------|-----|---------------|----------|-----------|
| "I love this product!" | 2023 | 01 | 15 | 12:30 PM | Twitter | 5 stars |
| "This is the worst experience ever." | 2023 | 01 | 15 | 01:00 PM | Twitter | 1 star |

**After:**
| Text | Emotion |
|------|---------|
| "I love this product!" | Very Happy |
| "This is the worst experience ever." | Very Sad |

## Contributing
If you'd like to contribute to this project, please fork the repository and submit a pull request. We welcome any improvements or suggestions!



