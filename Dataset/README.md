# Dataset

This dataset was created from the **Yelp Open Dataset**.

To reduce selection bias, **four French restaurants** were randomly selected from a pool of **121 French restaurants** available in the dataset. For each restaurant, **200 reviews** were randomly sampled, resulting in a balanced dataset of **800 customer reviews**.

The reviews were annotated using my **Hybrid ABSA System**:

https://github.com/azizjon0/Hybrid-ABSA-System

The annotation pipeline combines two approaches:

- **SetFit ABSA** automatically labels high-confidence predictions.
- **An LLM (via API)** is invoked only for low-confidence or ambiguous predictions.
- The final dataset is produced by the complete hybrid pipeline.

## Annotation Pipeline Performance

The hybrid pipeline was evaluated against manually verified labels and achieved the following performance:

| Metric | Score |
|---------|------:|
| Accuracy | **0.9569** |
| Macro F1-score | **0.9425** |
| Weighted F1-score | **0.9558** |

Compared with the baseline SetFit model, the hybrid pipeline improved overall accuracy from **87.63%** to **95.69%**, an increase of **8.06 percentage points**.
## Annotation Pipeline Performance

The hybrid annotation pipeline was evaluated against manually verified labels.

```
              precision    recall  f1-score   support

negative        0.9447    0.8999    0.9218       779
neutral         0.9708    0.7943    0.8737       418
positive        0.9581    0.9919    0.9747      3204

accuracy                            0.9569      4406
macro avg       0.9684    0.9215    0.9425      4406
weighted avg    0.9570    0.9569    0.9558      4406
```

Compared with the baseline SetFit model, the hybrid pipeline improved overall accuracy from **87.63%** to **95.69%**, corresponding to an improvement of **8.06 percentage points**.

## Important Note

The purpose of this dataset is to compare a small sample of restaurants.

The findings presented in this repository **should not be interpreted as representative of all French restaurants**. Only four restaurants were randomly selected; therefore, the statistical conclusions apply **only to this sample**.

This project investigates whether randomly selected restaurants exhibit similar customer complaint patterns rather than making general claims about the entire French restaurant industry.
