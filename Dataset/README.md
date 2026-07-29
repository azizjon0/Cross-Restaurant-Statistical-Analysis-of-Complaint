# Dataset

This dataset was created from the Yelp Open Dataset.

To reduce selection bias, four French restaurants were randomly selected from a pool of 121 French restaurants available in the dataset. For each restaurant, 200 reviews were randomly sampled, resulting in a balanced dataset of 800 customer reviews.

The reviews were processed using my Hybrid ABSA System:

https://github.com/azizjon0/Hybrid-ABSA-System

The annotation pipeline combines two approaches:

- **SetFit ABSA** automatically labels high-confidence samples.
- **LLM (via API)** is used only for low-confidence or ambiguous predictions.

The overall performance of the annotation system is:

| Metric | Score |
|---------|------:|
| Accuracy | 0.90 |
| Recall | 0.89 |
| F1-score | 0.88 |

## Important Note

The purpose of this dataset is to compare a small sample of restaurants.

The findings presented in this repository **should not be interpreted as representative of all French restaurants**. Only four restaurants were randomly selected, and therefore the statistical conclusions apply only to this sample.

The project investigates whether these randomly selected restaurants exhibit similar customer complaint patterns, rather than making general claims about the entire restaurant industry.