# Financial Sentiment Analysis with ChatGPT
This repository contains the code and supplementary materials for our research paper on financial sentiment analysis, where we explore the capabilities of ChatGPT 3.5 in the context of the foreign exchange (forex) market.

- Paper Title:Transforming Sentiment Analysis in the Financial Domain with ChatGPT
- Authors: Georgios Fatouros, John Soldatos, Kalliopi Kouroumali, Georgios Makridis and Dimosthenis Kyriazis

## Prerequisites

- Python 3.x

## Setup

1. Clone the repository to your local machine.
2. Install the required Python libraries using pip:
   ```bash
   pip install requirements.txt
   ```

## Data

1. `sentiment_annotated_with_texts.csv`: Sentiment Annotated dataset of Forex news. Includes sentiment predictions from FinBERT. For more info check https://zenodo.org/records/7976208.
2. `prompts.json`: Includes the different prompts presented in the paper.
3. `sentiment_predictions_single_article.csv`: Contains the predictions from the prompts processing single headlines.
4. `sentiment_predictions_allday_articles.csv`: Contains the predictions from the prompts processing all the headlines per day (GPT-P5 and GPT-P6).



## Running the prompts.py 

To run the script and evaluate ChatGPT's performance on a sample row from the dataset.

Add your OpenAI API key to the `prompts.py` script:
Replace <ADD YOUR API KEY> in the script with your actual OpenAI API key.


```bash
python3 prompts.py
```

The script will print the sentiment predictions of ChatGPT for the specified row and compare them against the true sentiment and FinBERT's predictions.


## Running the results.py 
The script will print the comparative performance results of the models/prompts presented in the paper .

```bash
python3 results.py
```

## Helper Functions
`sentiment_to_numeric`: Converts sentiment labels to numeric values.
`get_sentiment`: Fetches sentiment predictions from ChatGPT based on the specified prompt.

