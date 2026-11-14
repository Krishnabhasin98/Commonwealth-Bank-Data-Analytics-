# Commonwealth Bank — Introduction to Data Science Job Simulation

The official simulation outlines four activities:

1. **Data Aggregation and Analysis** — analyse a supermarket transaction dataset, answer specific business questions, and document the calculations.
2. **Data Anonymisation** — remove or transform personal information while retaining useful analytical attributes.
3. **Propose Data Analysis Approaches** — consider what insights can be derived from Commonwealth Bank social-media/X data, including structured and unstructured information and API-related fields.
4. **Designing a Database** — propose a structured way to organise social-media information. In this learner's activity, the design was prepared for submission/pasting into the provided dashboard; this repository does **not** claim that a live SQL database was implemented.

## 2. Repository contents

```text
Commonwealth-Bank-Data-Science-Job-Simulation/
│
├── Task-1-Data-Aggregation-and-Analysis/
│   ├── Commonwealth_Bank_Data_Analysis.ipynb
│   ├── supermarket_transactions.xlsx
│   └── Commonwealth_Bank_Data_Analysis.xlsx
│
├── Task-2-Data-Anonymisation/
│   └── Commonwealth_Bank_Data_Anonymisation.ipynb
│
├── Task-3-Data-Analysis-Approach/
│   ├── Commonwealth_Bank_Social_Media_Analysis.ipynb
│   └── commonwealth_bank_social_media_dataset.xlsx
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## 3. Task 1 — Data Aggregation and Analysis

### Objective

The simulation asks the learner to analyse a supermarket transaction dataset, answer business questions using filters and aggregations, and document the formulas/methodology in a spreadsheet.

### Dataset

- **Rows:** 50,783 transactions
- **Columns:** 12
- **Stores:** 48
- **Date range:** 16 June 2019 – 15 June 2022
- **Payment methods represented:** cash, contactless, debit card and credit card

### Work performed

The notebook loads the transaction workbook with pandas, inspects the dataset structure, and examines product, payment-method, store and customer-type distributions. It then filters the transaction data and sums the relevant fields to answer three questions. The accompanying Excel workbook records an executive summary, filtering criteria, metrics and aggregation methods.

### Results from the submitted notebook

| Business question                                               | Method                                                                           |         Result |
| --------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------: |
| How many apples were purchased using cash across all locations? | Filter `product_name = apple` and `payment_method = cash`; sum `quantity`        | **117 apples** |
| What was the total spending on apples across all locations?     | Filter `product_name = apple`; sum `total_amount`                                |   **2,051.73** |
| How much did non-member customers spend at Bakershire?          | Filter `store = Bakershire` and `customer_type = non-member`; sum `total_amount` |   **2,857.51** |

---

## 4. Task 2 — Data Anonymisation

### Objective

The activity focuses on protecting customer privacy while retaining fields that may still be useful for analysis. The supplied customer dataset contains personal and payment-related information.

### Dataset profile observed in the notebook

- **Records:** 10,000
- **Original columns:** 19
- **Missing values:** none reported by the notebook's initial inspection
- **Unique original customer IDs:** 10,000

### Transformations performed in the submitted notebook

1. Removed direct identifiers and sensitive payment details, including username, name, address, email, birthdate, credit-card number, security code and expiry.
2. Generalised exact ages into bands: `Up to 25`, `26–35`, `36–45`, `46–55`, and `56+`.
3. Generalised salary into ranges: `0–50K`, `50K–100K`, `100K–150K`, `150K–200K`, and `200K–250K`.
4. Replaced the original customer IDs with newly generated UUIDs.
5. Removed additional location/employer fields (`residence`, `current_location`, `employer`) from the final table.
6. Exported a reduced seven-column dataset in the original working environment.

---

## 5. Task 3 — Propose Data Analysis Approaches

### Objective

The activity introduces the use of social-media information to understand customer interests and engagement. The simulation context refers to Commonwealth Bank's X/Twitter presence and the potential use of API fields. It encourages consideration of structured metrics alongside unstructured post text.

### Supplied dataset

The supplied workbook contains **60 simulated social-media posts** and supporting sheets: a README, data dictionary, analysis prompts and resources. It includes fields such as post time, post type, author type, text, topic, content format, sentiment, likes, replies, reposts, views, link clicks, total engagements, engagement rate, customer intent and whether a response is needed.

### Additional exploratory findings from the supplied simulated posts

| Finding                                | Result |
| -------------------------------------- | -----: |
| Total simulated posts                  | **60** |
| Posts labelled positive                | **26** |
| Posts labelled neutral                 | **15** |
| Posts labelled negative                | **11** |
| Posts labelled mixed                   |  **8** |
| Posts marked as needing a response     | **11** |
| Posts not marked as needing a response | **49** |

**Topic and engagement observations**

- `Digital banking` is the most frequent topic, with **13 posts**.
- `Fraud & scams` has **11 posts** and the highest total engagement in this sample: **36,283 engagements** across those posts.
- `Security education` has the highest average engagement rate among the topics with multiple posts: approximately **3.85%** across five posts.
- `Outage/service issue` has five posts and a lower average engagement rate of approximately **1.35%**.
- The highest-engagement individual post is `SM048` (Fraud & scams), with **210,000 views**, **12,165 total engagements**, and an engagement rate of approximately **5.79%**.

---

## 7. Tools and concepts

- Python
- pandas
- Jupyter Notebook
- Excel / `.xlsx` workbooks
- Data filtering and aggregation
- Data inspection and exploratory analysis
- Data minimisation, generalisation and de-identification concepts
- Social-media metrics, sentiment labels and customer-intent analysis
- Database-design concepts (proposal-level activity only)

## 8. Running the notebooks

Install the common dependencies:

```bash
pip install -r requirements.txt
```

Launch Jupyter:

```bash
jupyter notebook
```

