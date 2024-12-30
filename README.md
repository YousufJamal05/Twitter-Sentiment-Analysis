# Twitter Sentiment Analysis

![Python](https://img.shields.io/badge/Python-3.x-blue) ![TwitterAPI](https://img.shields.io/badge/Tweepy-4.x-orange) ![NetworkX](https://img.shields.io/badge/NetworkX-2.x-green)

Analyze the overall sentiment of tweets on a specific topic and visualize user interactions with sentiment-weighted edges.

## Features
- Fetch recent tweets on a given query using the Twitter API.
- Perform sentiment analysis on tweets using **TextBlob**.
- Construct a directed graph of user interactions (e.g., mentions).
- Calculate and display the overall sentiment score and type (positive, neutral, negative).
- Visualize the interactions graph with sentiment-weighted edges.

## Requirements
Before running the project, ensure you have the following dependencies installed:

- Python 3.x
- Tweepy
- TextBlob
- NetworkX
- Matplotlib

You can install them via pip:

```bash
pip install tweepy textblob networkx matplotlib
```

## Setup
-  Clone this repository:
```bash
git clone https://github.com/YousufJamal05/twitter-sentiment-analysis.git
cd twitter-sentiment-analysis
```

-  Obtain Twitter API keys:
Create a Twitter Developer account and generate your API keys and tokens. Add them to the script:

```bash
API_KEY = "your-api-key"
API_SECRET = "your-api-secret"
ACCESS_TOKEN = "your-access-token"
ACCESS_TOKEN_SECRET = "your-access-token-secret"
BEARER_TOKEN = "your-bearer-token"
```
-  Run the script:
```bash
python twitter_sentiment_analysis.py
```
## How It Works
Authenticate with the Twitter API
The script uses your credentials to access the Twitter API and fetch recent tweets related to the provided query.

### Fetch Tweets
Specify your query (e.g., "crypto OR #cryptocurrency OR blockchain") to collect recent tweets mentioning these terms.

### Sentiment Analysis
Uses TextBlob to calculate a sentiment polarity score for each tweet.
Sentiments are categorized as:
Positive: Polarity > 0
Neutral: Polarity = 0
Negative: Polarity < 0

### Graph Construction
Builds a graph using NetworkX where nodes represent users and edges represent mentions.
Edge weights reflect the sentiment polarity of the interaction.

### Visualization
Visualizes the graph using Matplotlib, with edge colors indicating sentiment weights.

### Output
Displays the overall sentiment score and type (positive, neutral, or negative) of the community.
Example Output
```bash
Logged in as: YourTwitterHandle

Overall Sentiment Analysis:
  Sentiment Score: 0.35
  Sentiment Type: Positive
```

### Graph:
A visualization of the user interactions with sentiment-weighted edges.
