# Cross-Restaurant Statistical Analysis of Complaint Patterns

A statistical analysis of customer reviews from four restaurants using Aspect-Based Sentiment Analysis (ABSA), investigating whether complaint patterns are universal across restaurants or business-specific.

**TL;DR:** [ONE-LINE HEADLINE FINDING — e.g. "Waiting Time and Price Value complaints were consistent across all four restaurants (p < 0.05), while Staff Behavior sentiment varied significantly by location — suggesting service culture, not food quality, drives restaurant-specific reputation."]

---

## Key Findings

> Fill this in with your actual notebook 02 results before publishing — this section is what recruiters read first.

- **Universal patterns:** [Which categories showed similar sentiment/frequency across all 4 restaurants?]
- **Restaurant-specific patterns:** [Which categories differed significantly, and which restaurant(s) drove the difference?]
- **Statistical tests used:** [e.g. Chi-square test of independence for category-by-restaurant distributions; Mann-Whitney U / Kruskal-Wallis for sentiment score comparisons] — report test statistic and p-value for the headline result(s).
- **Business implication:** [What would a multi-location restaurant group actually do with this? e.g. "fix X chain-wide, audit Y per-location."]

![Category comparison chart](assets/category_comparison.png)
*Replace with your actual chart from `assets/` — a positive-rate-by-category-by-restaurant grouped bar chart works well here.*

---

## Project Overview

This repository contains an end-to-end analytical pipeline:

1. Extract aspect-level opinions from customer reviews using a hybrid BERT + LLM ABSA pipeline.
2. Categorize 200+ unique raw aspects into 16 standardized business categories.
3. Perform exploratory data analysis on aspect frequency and sentiment distribution.
4. Compare restaurants statistically to test for significant differences.
5. Identify which complaint patterns are common across businesses versus restaurant-specific.

## Repository Structure

```
Cross-Restaurant-Statistical-Analysis-of-Complaint/
│
├── Notebooks/
│   ├── 00_Aspect_Categorization.ipynb
│   ├── 01_Exploratory_Data_Analysis.ipynb
│   └── 02_Cross-restaurant-statistical-analysis-of-complaint.ipynb
│
├── Dataset/
├── assets/
└── README.md
```

## Notebooks

### 00 — Aspect Categorization
After processing reviews through the hybrid ABSA pipeline, 200+ unique aspect terms were extracted. An LLM grouped these into 16 standardized categories, including Food Quality, Service, Atmosphere, Drinks, Desserts, Staff Behavior, Waiting Time, Reservation, Price Value, and Cleanliness.

### 01 — Exploratory Data Analysis
Review statistics, aspect frequency, sentiment distribution, category popularity, and positive rate by category, providing a baseline view of the data before formal testing.

### 02 — Cross-Restaurant Statistical Analysis
The main research notebook: comparison of aspect distributions and positive/negative rates across restaurants, statistical hypothesis testing, restaurant similarity analysis, and business insights derived from the results.

## Dataset

Customer reviews from four French restaurants, ~200 randomly sampled reviews per restaurant. Reviews were processed through a hybrid ABSA pipeline (BERT classifier + LLM fallback for low-confidence cases) followed by LLM-assisted aspect categorization.

## Limitations

- Sample size (~200 reviews/restaurant) limits statistical power for some per-category comparisons, particularly where a category has few mentions at a given restaurant.
- [Add any other caveats specific to your test choices, e.g. multiple-comparisons correction if you ran many category-level tests.]

## Technologies

Python · Pandas · NumPy · Matplotlib · Seaborn · SciPy · Statsmodels · OpenAI API

## Related Work

Built on the [Hybrid BERT + LLM ABSA Pipeline](LINK_TO_YOUR_ABSA_REPO) used to generate the underlying aspect-sentiment predictions for this analysis.

## Research Goal

Determine whether different restaurants exhibit similar customer feedback patterns and identify which problems are common across businesses versus restaurant-specific.

## Author

Azizjon Achilov
