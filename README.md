# Cross-Restaurant Statistical Analysis of Complaint Patterns

A statistical analysis of customer reviews from multiple restaurants using Aspect-Based Sentiment Analysis (ABSA).

The project investigates whether restaurants share similar complaint patterns and customer preferences by comparing aspect distributions, sentiment, and statistical characteristics across multiple businesses.

---

## Project Overview

This repository contains an end-to-end analytical pipeline:

1. Extract aspect-level opinions from customer reviews.
2. Categorize hundreds of unique aspects into standardized business categories.
3. Perform exploratory data analysis.
4. Compare restaurants using statistical methods.
5. Identify common and restaurant-specific strengths and weaknesses.

The goal is to understand whether customer feedback follows similar patterns across restaurants or whether each restaurant has unique issues.

---

## Repository Structure

```
Cross-Restaurant-Statistical-Analysis-of-Complaint/
│
├── Notebooks/
│   ├── 00_Aspect_Categorization.ipynb
│   ├── 01_Exploratory_Data_Analysis.ipynb
│   └── 02_Cross-restaurant-statistical-analysis-of-complaint.ipynb
│
└── README.md
```

---

## Notebook Description

### 00 — Aspect Categorization

After processing reviews with a hybrid ABSA pipeline, more than 200 unique aspect terms were extracted.

To simplify further analysis, an LLM was used to group them into 16 standardized categories, including:

- Food Quality
- Service
- Atmosphere
- Drinks
- Desserts
- Staff Behavior
- Waiting Time
- Reservation
- Price Value
- Cleanliness
- and others.

The categorized results are saved and used throughout the remaining analysis.

---

### 01 — Exploratory Data Analysis

Exploratory analysis of the processed dataset including:

- review statistics
- aspect frequency
- sentiment distribution
- category popularity
- positive rate by category
- visualization of customer feedback

This notebook provides an overview of the data before statistical testing.

---

### 02 — Cross-Restaurant Statistical Analysis

The main research notebook.

Includes analyses such as:

- comparison of aspect distributions
- comparison of positive/negative rates
- statistical hypothesis testing
- restaurant similarity analysis
- identification of common complaint patterns
- business insights

---

## Dataset

The analysis uses customer reviews collected from four French restaurants.

Each restaurant contains approximately 200 randomly sampled reviews.

Reviews were processed using a Hybrid ABSA pipeline followed by LLM-assisted aspect categorization.

---

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Statsmodels
- OpenAI API

---

## Research Goal

Determine whether different restaurants exhibit similar customer feedback patterns and identify which problems are common across businesses versus restaurant-specific.

---

## Author

Azizjon Achilov