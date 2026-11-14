# Commonwealth Bank — Introduction to Data Science Job Simulation

This repository documents the four activities in the Forage Commonwealth Bank Data Science Job Simulation.

## Repository contents

- `Task-1-Data-Aggregation-and-Analysis/analysis.ipynb` — pandas analysis for the supermarket transaction questions.
- `Task-2-Data-Anonymisation/anonymisation.ipynb` — customer-data minimisation and generalisation workflow.
- `Task-3-Data-Analysis-Approach/social_media_analysis.ipynb` — exploratory analysis of the supplied simulated social-media dataset.
- `requirements.txt` — Python dependencies.
- `.gitignore` — excludes private customer files and local data.

## Task 1 — Data Aggregation and Analysis

The notebook answers the simulation's three business questions by filtering and aggregating the supermarket transaction data:

| Business question | Result from the submitted analysis |
|---|---:|
| Cash-purchased apples across all locations | **117 apples** |
| Total spending on apples | **2,051.73** |
| Non-member spending at Bakershire | **2,857.51** |

The original workbook contained 50,783 transactions across 48 stores. The source transaction workbook is not included in this initial GitHub upload; place the supplied `supermarket_transactions.xlsx` beside the notebook locally to run it.

## Task 2 — Data Anonymisation

The workflow covers removal of direct identifiers and payment details, age and salary banding, UUID replacement, and removal of additional location/employer fields. The original input `mobile_customers.xlsx` and generated `anonymised_customers.csv` are intentionally excluded because they contain customer-level personal or sensitive information. The notebook expects the original workbook locally and writes its output locally; do not publish customer-level records.

These transformations reduce identifiability but do not prove that a dataset is fully anonymous.

## Task 3 — Propose Data Analysis Approaches

The notebook loads the `Social_Media_Posts` sheet from `commonwealth_bank_social_media_dataset.xlsx`. This workbook contains 60 simulated posts, not actual Commonwealth Bank customer or social-media records. The source workbook was not included in this initial GitHub upload; place it beside the notebook locally to run the analysis.

Findings previously calculated from the supplied simulated workbook:
- 26 positive, 15 neutral, 11 negative and 8 mixed posts.
- 11 posts marked as needing a response.
- Digital banking was the most frequent topic (13 posts).
- Fraud & scams had the highest total engagement in this sample (36,283).

## Task 4 — Designing a Database

The activity involved preparing a database design for submission in the provided dashboard. This repository does not claim that a live SQL database was implemented.

## Setup

```bash
pip install -r requirements.txt
jupyter notebook
```

## Tools and concepts

Python, pandas, Jupyter Notebook, Excel, data aggregation, exploratory data analysis, data minimisation, generalisation, de-identification, sentiment labels, customer intent, and database-design concepts.
