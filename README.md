# Hypothesis Testing: Student Performance

A focused statistical analysis project examining differences in Mathematics and Language scores across gender and parental education groups using descriptive analysis, hypothesis testing, and effect sizes.

## Project Overview

This project examines student scores in Mathematics and Language. It focuses on whether average scores differ between male and female students and across parental education groups.

The analysis uses descriptive statistics and boxplots to explore the data. Hypothesis tests check whether the differences are statistically significant, while effect sizes show how large these differences are.

## Dataset

It contains 972 score records for 486 students. Each student has one Mathematics score and one Language score.

The main variables are:

- Student ID
- Gender
- Parental level of education
- Subject
- Score

Parental education has four categories: high school, associate’s degree, bachelor’s degree, and master’s degree. Scores range from 0 to 100. No missing values were found.

## Research Questions

This project focuses on the following questions:
- Do Mathematics scores differ between male and female students?
- Do Language scores differ between male and female students?
- Do scores differ across parental education levels?
- Which parental education groups have significantly different scores?

## Methods

The analysis follows a simple workflow:
- Data inspection and basic checks
- Descriptive statistics by subject, gender, and parental education
- Boxplots to compare score distributions
- Welch’s t-tests to compare gender groups
- One-way ANOVA to compare parental education groups
- Tukey HSD tests to find which education groups differ
- Cohen’s d and eta squared to measure the size of the differences

Mathematics and Language scores are analyzed separately.

## Key Findings

1. Male students had higher average Mathematics scores than female students: 68.95 compared with 63.86. The difference was statistically significant, but the effect size was fairly small (Cohen’s d = 0.34).
2. Female students had higher average Language scores than male students: 73.00 compared with 64.93. The difference was statistically significant, with a medium effect size (Cohen’s d = 0.58).
3. Average scores differed across parental education groups in both subjects. The effect size was larger for Language than for Mathematics.
4. In Mathematics, students in the high school parental education group had significantly lower scores than students in the other three groups. The other group comparisons were not statistically significant.
5. In Language, the high school group also had significantly lower scores than the other three groups. The master’s degree group had significantly higher scores than the associate’s degree group.

## Statistical Tests

Four main hypothesis tests were used with a significance level of α = 0.05.

| Comparison | Test | p-value | Effect Size |
| --- | --- | ---: | ---: |
| Mathematics scores by gender | Welch’s t-test | 1.78e-04 | Cohen’s d = 0.34 |
| Language scores by gender | Welch’s t-test | 3.47e-10 | Cohen’s d = 0.58 |
| Mathematics scores by parental education | One-way ANOVA | 3.75e-04 | η² = 0.037 |
| Language scores by parental education | One-way ANOVA | 6.62e-09 | η² = 0.081 |

All four tests were statistically significant. However, the effect sizes were small to medium, so the differences should not be described as large.

Tukey HSD tests were used after ANOVA to check which parental education groups differed from each other. These tests also account for multiple group comparisons within each subject.

## Tools Used
- Python
- pandas
- matplotlib
- seaborn
- SciPy
- Pingouin
- statsmodels
- Poetry
- Jupyter Notebook

## How to Run

- Clone the repository and install dependencies with Poetry.

```bash
poetry install
poetry run jupyter notebook
```
