# Cross-Restaurant Statistical Analysis of Complaint Patterns

A statistical study of customer feedback across four French restaurants using Aspect-Based Sentiment Analysis (ABSA) to determine whether customer complaint patterns are universal across restaurants or specific to individual businesses.

> **Research Question:**  
> Do restaurants share common customer complaint patterns, or does each restaurant develop its own unique profile of strengths and weaknesses?

---

## Project Highlights

- Random sample of **800 customer reviews** (200 per restaurant)
- **4 French restaurants** randomly selected from the Yelp Open Dataset
- **15,000+ aspect-level opinions** extracted using a hybrid ABSA pipeline
- **200+ raw aspect terms** grouped into **16 standardized business categories**
- Statistical comparison of complaint and satisfaction patterns across restaurants

---

# Statistical Results

To determine whether customer complaint patterns differ across restaurants, several statistical analyses were performed.

## 1. Complaint Category Distribution

A **Chi-square Test of Independence** was applied to compare the distribution of negative aspect categories across the four restaurants.

### Results

| Statistic | Value |
|-----------|------:|
| Chi-square (χ²) | 35.99 |
| Degrees of freedom | 36 |
| p-value | 0.469 |
| Cramer's V | 0.118 |

The assumptions of the Chi-square test were verified before hypothesis testing:

- Minimum expected frequency = **5.68**
- Cells with expected frequency < 5 = **0%**

Since all expected frequencies exceeded the recommended threshold, the Chi-square approximation was considered valid.

### Interpretation

The test found **no statistically significant association** between restaurant and complaint category distribution (**p = 0.469**).

This indicates that customers tend to complain about the **same types of issues**, regardless of which restaurant they visited.

Furthermore, the effect size was small (**Cramer's V = 0.118**), suggesting only a weak relationship between restaurant identity and complaint profile.

---

## Typical Complaint Profile

After normalizing complaint frequencies within each restaurant, the average complaint profile was computed.

| Complaint Category | Mean Share |
|-------------------|-----------:|
| Specific Dish | 13.7% |
| Food Quality | 13.2% |
| Service | 12.7% |
| Restaurant General | 12.1% |
| Staff Behavior | 10.9% |
| Price Value | 5.8% |
| Drinks | 5.6% |
| Seating Comfort | 5.4% |
| Menu Variety | 5.4% |
| Atmosphere | 4.3% |
| Other Operational | 3.9% |
| Waiting Time | 3.7% |
| Desserts | 3.2% |

These results demonstrate that customer complaints are concentrated around a small set of recurring operational issues, particularly food quality, specific dishes, and service.

---

## Complaint Intensity

Although restaurants shared similar complaint categories, they differed in the **amount of negative feedback** received.

| Restaurant | Negative Aspect Mentions per Review |
|------------|------------------------------------:|
| Lilette | 2.19 |
| Pacific Crepes | 2.64 |
| Meauxbar | 3.08 |
| Piquant | 4.05 |

This suggests that while customers complain about similar issues across restaurants, some restaurants generate substantially more complaints per review than others.

---

## Evidence Supporting the Research Question

The statistical evidence suggests that customer complaint patterns are **largely universal rather than restaurant-specific**.

This conclusion is supported by:

- **Non-significant Chi-square test** (χ² = 35.99, p = 0.469), indicating no significant differences in complaint category distributions.
- **Small effect size** (Cramer's V = 0.118), showing only a weak association between restaurant and complaint profile.
- **Highly consistent normalized complaint profiles**, where the same categories (Specific Dish, Food Quality, Service, Restaurant General, and Staff Behavior) dominate across all restaurants.
- **Differences in complaint intensity**, indicating that restaurants differ more in how often customers complain than in what they complain about.

Overall, the findings suggest that improving food quality, individual dishes, and service is likely to benefit restaurants regardless of their individual characteristics.

# Research Pipeline

The complete analytical workflow consists of five stages:

1. Extract aspect-level opinions from customer reviews using a hybrid ABSA system.
2. Normalize 2000+ extracted aspects into 16 standardized business categories.
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
