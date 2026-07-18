# ABM — Group 04

Analyzing the Impact of Social Media Sentiment on Investor
Herding Behavior in Financial Markets Using Agent-Based Modeling

## Requirements
- NetLogo 7.0.3
- Python 3.10+
- Libraries: pandas, transformers, torch, yfinance

## How to Run

### Step 1: Generate sentiment data
Open `notebooks/crypto_sentiment_pipeline_group04.ipynb` in Google Colab.
Run Cells 1–8 in order.
This produces `daily_sentiment_with_btc.csv` and `tweet_agents.csv`.

### Step 2: Run the NetLogo model
1. Open `netlogo/ABM_combined_final.nlogo` in NetLogo 7.0.3
2. Place CSV files in the same folder as the .nlogo file
3. Set scenario chooser to `dataset`
4. Click Setup → Go

### Step 3: Run BehaviorSpace experiments
Tools → BehaviorSpace → select experiment → Run

## Dataset
Cryptocurrency Tweets dataset (107,324 tweets, June 2022–May 2023)

## Authors
Group 04 — FM 4054 Agent-Based Modeling
University of Colombo
