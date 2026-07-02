# Sentiment Analysis Project

This project is a notebook-based sentiment analysis prototype that uses Google's Gemini model to classify tweet sentiment as Positive, Negative, or Neutral. The workflow is implemented in the notebook [Sentiment_analytyics.ipynb](Sentiment_analytyics.ipynb) and is designed for use in Google Colab.

## Project Overview

The notebook demonstrates how to:
- load a tweet dataset,
- configure a Gemini API connection,
- initialize a generative model,
- create a text prompt for sentiment classification,
- classify a sample tweet and display the result.

This is a practical example of using an LLM for text classification instead of relying only on traditional rule-based or lexicon-based sentiment models.

## What the Notebook Contains

The notebook includes the following main steps:
1. Importing required Python libraries.
2. Loading the dataset from a CSV file.
3. Preparing the dataset columns for tweet analysis.
4. Configuring the Gemini API using a Google AI Studio API key.
5. Initializing the Gemini model.
6. Selecting a sample tweet from the dataset.
7. Sending a prompt to the model for sentiment classification.
8. Displaying the model response and the final sentiment label.

## Expected Input Data

The notebook expects a CSV file named twitter_training.csv. The data is loaded with columns such as:
- Tweet ID
- Entity
- Sentiment
- Tweet Content

If the file is not available in the Colab environment, the notebook prompts the user to upload it.

## Technology Stack

- Python
- pandas
- Google Colab
- Google Generative AI SDK
- Gemini model

## Prerequisites

Before running the notebook, make sure you have:
- a Google account,
- access to Google AI Studio,
- a valid Gemini API key,
- internet access,
- the dataset file available in the runtime environment.

## How to Run the Notebook

1. Open [Sentiment_analytyics.ipynb](Sentiment_analytyics.ipynb) in Google Colab or Jupyter Notebook.
2. Upload the dataset if it is not already present.
3. Add your Gemini API key to Colab secrets as GOOGLE_API_KEY.
4. Run the cells in order from top to bottom.
5. Review the output for the sample tweet classification.

## Implementation Flow

### 1. Data Loading
The notebook begins by importing pandas and checking whether the dataset file is present. If not, it asks the user to upload it.

### 2. API Configuration
The notebook imports the Google Generative AI library and configures the SDK using the API key stored in Colab secrets.

### 3. Model Initialization
A Gemini model is initialized for generating sentiment predictions.

### 4. Prompt-Based Classification
The notebook builds a prompt that contains:
- the target entity,
- the tweet content,
- a request to classify the sentiment.

### 5. Result Display
The response from the model is printed and then interpreted as the final sentiment label.

## Verification Summary

The notebook file was verified successfully as a valid Jupyter notebook JSON file. It contains 12 cells, including code and markdown sections, and its main workflow is consistent with the documented sentiment analysis implementation.

## Notes and Limitations

- This is a prototype and currently demonstrates classification for one sample tweet.
- The results depend on the quality of the prompt and the model response.
- A valid API key and quota are required to run the notebook successfully.
- For larger datasets, the workflow should be extended to process all rows in a loop or batch.

## Suggested Improvements

To turn this prototype into a stronger project, you can add:
- batch sentiment classification for the entire dataset,
- saving the results to CSV or Excel,
- comparison with traditional models such as VADER or BERT,
- visualization of sentiment distribution,
- a simple dashboard for analysis.
