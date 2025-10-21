🚢 Exploratory Data Analysis (EDA) Report on Titanic Dataset

This report analyzes key variables related to survival on the Titanic, examining distributions, relationships, and data quality issues (outliers).

1. Survival Rate Overview

The Survival Count Plot indicates a significant disparity between passengers who survived (1) and those who did not (0).

Non-Survival (0): ≈ 550 passengers

Survival (1): ≈ 340 passengers

🔹 Insight: Most passengers did not survive, showing that the target variable is imbalanced — an important consideration for modeling.

2. Factors Affecting Survival
🧍 Survival by Sex

The Survival by Sex bar plot clearly shows a strong influence of gender on survival rates, reflecting the "women and children first" protocol.

Males:

Did not survive: ≈ 450

Survived: ≈ 110

Females:

Survived: ≈ 230

Did not survive: ≈ 80

✅ Conclusion: Females had a significantly higher survival rate than males.
Hence, Sex is one of the most important predictors.

🎟️ Survival by Passenger Class (Pclass)

The Survival by Passenger Class plot shows a clear relationship between socio-economic status (represented by class) and survival.

1st Class: Survived ≈ 140 | Not survived ≈ 80

2nd Class: Survived ≈ 90–100 | Not survived ≈ 90–100

3rd Class: Survived ≈ 120 | Not survived ≈ 370

✅ Conclusion:
Survival rate is highest in First Class and lowest in Third Class.
Thus, Pclass is another critical predictor — higher classes offered a clear survival advantage.

👶 Survival by Age Distribution

The Age Distribution by Survival histogram reveals how age impacts survival:

Infants/Children (0–10 yrs): Higher survival rate.

Adults (20–40 yrs): Most numerous group, but non-survival peaks around age 30.

Older Passengers (60+ yrs): Low survival, but fewer passengers overall.

✅ Conclusion:
Age influences survival — younger children had an advantage, while most non-survivors were young to middle-aged adults.

3. Variable Correlation

The Correlation Heatmap illustrates linear relationships between numerical variables and the target Survived.

| Variable   | Correlation with Survived  | Interpretation                                                     |
| ---------- | -------------------------- | ------------------------------------------------------------------ |
| **Pclass** | -0.34 (Strong Negative)    | Lower class number (e.g., 1st class) → higher survival probability |
| **Fare**   | +0.26 (Moderate Positive)  | Higher fare → higher survival probability                          |
| **Parch**  | +0.08 (Weak Positive)      | Slightly higher survival for those with family aboard              |
| **SibSp**  | -0.07 (Weak Negative)      | Slightly lower survival with more siblings/spouses                 |
| **Age**    | -0.04 (Very Weak Negative) | Minimal linear correlation; nonlinear trend for children           |


Other Notable Correlations:

Pclass ↔ Fare: -0.55 → Expected (higher class = higher fare).

SibSp ↔ Parch: +0.41 → Passengers with siblings/spouses often also had parents/children aboard.

Fare is the most problematic variable — should be log-transformed or robust-scaled.

🧾 Summary

Sex and Pclass are the strongest predictors of survival.

Age shows non-linear effects (children more likely to survive).

Fare correlates positively with survival but has many outliers.

The dataset contains imbalanced target values and skewed numeric distributions, requiring preprocessing for fair modeling.