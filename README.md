# Analyzing the Impact of Social Media Sentiment on Investor Herding Behavior in Financial Markets Using Agent-Based Modeling

**Course:** FM 4054 – Agent-Based Modeling  
**Institution:** Department of Mathematics, University of Colombo  
**Group:** Group 04

---

## Project Overview

This project investigates how social media sentiment influences investor herding behavior and cryptocurrency price dynamics using an Agent-Based Model (ABM).

Historical cryptocurrency tweets are analyzed using the FinBERT language model to estimate sentiment. The resulting sentiment data are integrated into a NetLogo simulation consisting of Fundamentalist and Chartist investors to study how information diffusion affects market behaviour.

---

## Repository Structure

```text
ABM_Group04/
│
├── analysis/         Python scripts for result analysis
├── data/             Processed datasets
├── experiments/      BehaviorSpace experiment outputs
├── figures/          Figures used in the report
├── model/            NetLogo model
├── notebooks/        Python preprocessing notebook
├── reports/          Final report
├── requirements.txt
└── README.md
```

---

## Software Requirements

- NetLogo 7.0.3
- Python 3.10 or later
- Google Colab or Jupyter Notebook

### Python Libraries

Install the required libraries using

```bash
pip install -r requirements.txt
```

---

## Dataset

The original Cryptocurrency Tweets dataset is **not included** in this repository due to its large file size.

Download the dataset from:

**Kaggle Dataset**

> **[[Paste Kaggle Dataset Link Here]](https://www.kaggle.com/datasets/infsceps/cryptocurrency-tweets?select=Merged_Twitter_Data_IDsRemoved.csv)**

After downloading, place the dataset in the location expected by the preprocessing notebook (or update the file path accordingly).

---

## Running the Project

### Step 1 — Generate Sentiment Data

Open

```
notebooks/crypto_sentiment_pipeline_group 04.ipynb
```

Run all notebook cells sequentially.

The notebook performs:

- Data cleaning
- Tweet preprocessing
- FinBERT sentiment analysis
- Daily sentiment aggregation
- Bitcoin price retrieval
- Tweet-agent selection
- Final CSV validation

---

### Step 2 — Generated CSV Files

Running the notebook produces the following files.

| File | Description | Used by NetLogo |
|------|-------------|-----------------|
| `tweets_cleaned.csv` | Cleaned tweet dataset | No |
| `tweets_scored_checkpoint.csv` | Intermediate checkpoint created during FinBERT processing | No |
| `tweets_scored.csv` | Tweet-level sentiment scores | No |
| `daily_sentiment.csv` | Daily aggregated sentiment | No |
| `daily_sentiment_with_btc.csv` | Daily sentiment merged with Bitcoin closing prices | Yes |
| `tweet_agents.csv` | Tweet-agent dataset containing sentiment, normalized reach and engagement | Yes |

Only the following files are required to run the NetLogo model:

- `daily_sentiment_with_btc.csv`
- `tweet_agents.csv`

---

### Step 3 — Run the NetLogo Model

1. Open

```
model/ABM_combined_final.nlogo
```

using NetLogo 7.0.3.

2. Copy

- `daily_sentiment_with_btc.csv`
- `tweet_agents.csv`

into the same folder as the NetLogo model.

3. Select **dataset** from the Scenario chooser.

4. Click **Setup**.

5. Click **Go**.

---

### Step 4 — Run BehaviorSpace Experiments

Open

```
Tools → BehaviorSpace
```

Select the required experiment and click **Run**.

---

## Reproducibility Notes

- Run notebook cells in order.
- Do not rename the generated CSV columns.
- Keep the final CSV files in the same folder as the NetLogo model.
- Use NetLogo version **7.0.3**.
- Internet access is required when downloading the FinBERT model and Bitcoin price data for the first time.

---

## Repository Contents

This repository contains

- NetLogo simulation model
- Python preprocessing notebook
- Processed datasets
- BehaviorSpace experiment outputs
- Analysis scripts
- Figures
- Final report

---

## Authors

**Group 04**

FM 4054 – Agent-Based Modeling

Department of Mathematics

University of Colombo
