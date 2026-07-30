# Cross-Restaurant Statistical Analysis of Complaint Patterns

A statistical study of customer feedback across four French restaurants using Aspect-Based Sentiment Analysis (ABSA) to determine whether customer complaint patterns are universal across restaurants or specific to individual businesses.

> **Research Question:**  
> Do restaurants share common customer complaint patterns, or does each restaurant develop its own unique profile of strengths and weaknesses?

---

## Project Highlights

- Random sample of **800 customer reviews** (200 per restaurant)
- **4 French restaurants** randomly selected from the Yelp Open Dataset
- **4,000+ aspect-level opinions** extracted using a hybrid ABSA pipeline
- **200+ raw aspect terms** grouped into **16 standardized business categories**
- Statistical comparison of complaint and satisfaction patterns across restaurants

---

## Key Findings

> Replace this section with the final statistical results from Notebook 02 before publishing.

- **Universal patterns**
  - [Example: Waiting Time and Price Value showed similar complaint patterns across all restaurants.]

- **Restaurant-specific patterns**
  - [Example: Staff Behavior and Service Quality differed significantly between restaurants.]

- **Statistical evidence**
  - Chi-square Test
  - Kruskal-Wallis Test
  - Effect sizes where appropriate

- **Business implication**
  - Chain-wide operational improvements should focus on universal issues, while restaurant-specific categories require location-level interventions.

![Category comparison](assets/imagine1.png)

*Example visualization comparing positive sentiment rates across restaurants.*

---

# Research Pipeline

The complete analytical workflow consists of five stages:

1. Extract aspect-level opinions from customer reviews using a hybrid ABSA system.
2. Normalize 200+ extracted aspects into 16 standardized business categories.
3. Perform exploratory data analysis of aspect frequency and sentiment.
4. Apply statistical tests to compare restaurants.
5. Identify universal versus restaurant-specific customer experience patterns.

---

# Repository Structure

```text
Cross-Restaurant-Statistical-Analysis-of-Complaint/
│
├── Dataset/
│
├── Notebooks/
│   ├── 00_Aspect_Categorization.ipynb
│   ├── 01_Exploratory_Data_Analysis.ipynb
│   └── 02_Cross_Restaurant_Statistical_Analysis.ipynb
│
├── assets/
│
└── README.md
```

---

# Notebook Overview

## 00 — Aspect Categorization

The hybrid ABSA pipeline extracted over 200 unique aspect expressions from customer reviews. Since these expressions often describe similar business concepts (e.g., *waiter*, *server*, *staff member*), an LLM was used to group them into 16 standardized business categories for downstream analysis.

Examples include:

- Food Quality
- Service
- Staff Behavior
- Waiting Time
- Atmosphere
- Price Value
- Reservation
- Drinks
- Desserts
- Cleanliness

---

## 01 — Exploratory Data Analysis

Explores the dataset before hypothesis testing.

The notebook includes:

- Review statistics
- Aspect frequency
- Sentiment distribution
- Category popularity
- Positive rate by category
- Restaurant profiles

---

## 02 — Cross-Restaurant Statistical Analysis

The primary research notebook.

Analyses include:

- Restaurant comparison
- Statistical hypothesis testing
- Category distribution analysis
- Sentiment comparison
- Restaurant similarity analysis
- Business recommendations

---

# Dataset

The dataset was created from the **Yelp Open Dataset**.

To reduce selection bias:

- Four French restaurants were randomly selected from 121 available French restaurants.
- 200 customer reviews were randomly sampled from each restaurant.
- The final dataset contains approximately **800 reviews**.

Reviews were processed using a hybrid ABSA pipeline combining:

- SetFit ABSA for high-confidence predictions
- LLM reasoning for low-confidence cases

The extracted aspects were subsequently grouped into standardized business categories using an LLM.

---

# Statistical Methods

The project applies statistical methods to compare customer feedback patterns across restaurants, including:

- Chi-square Test of Independence
- Kruskal-Wallis Test
- Mann-Whitney U Test (where applicable)
- Jensen-Shannon Distance
- Mean Absolute Error (restaurant profile similarity)

---

# Limitations

- Only four restaurants were analyzed.
- Approximately 200 reviews were sampled per restaurant.
- Results should **not** be interpreted as representative of all French restaurants.
- Categories with few observations have limited statistical power.

---

# Technologies

- Python
- Pandas
- NumPy
- SciPy
- Statsmodels
- Matplotlib
- Seaborn
- OpenAI API

---

# Related Project

This analysis is built upon the Hybrid ABSA pipeline used to generate the aspect-level annotations:

**Hybrid ABSA System**
https://github.com/azizjon0/Hybrid-ABSA-System

---

# Research Objective

The objective of this project is to determine whether customer complaint patterns are shared across restaurants or whether each restaurant develops a unique profile of customer experience.

The findings can help restaurant owners distinguish between:

- operational issues common across businesses,
- and problems requiring restaurant-specific interventions.

---

# Author

**Azizjon Achilov**

Artificial Intelligence Student • Machine Learning • NLP • Statistical Analysis
