# Unit 1: Introduction to Statistical Learning
## Statistical Learning Problems

1. Identify the risk factors for prostate cancer.
2. Classify a recorded phoneme based on a log-periodogram.
3. Predict whether someone will have a heart attack on the basis of demographic, diet and clinical measurements.
4. Customize an email spam detection system.
5. Identify the numbers in a handwritten zip code.
6. Classify a tissue sample into one of several cancer classes, based on a gene expression profile.
7. Establish the relationship between salary and demographic variables in population survey data.
8. Classify the pixels in a LANDSAT image, by usage.

## Supervised and Unsupervised Learning Problems
### Supervised Learning

- The Outcome measurement $Y$ is also known as dependent variable, response, target.
- The Vector of $p$ predictor measurements $X$ also referred to as inputs, regressors, covariates, features, independent variables.
   - In the **regression problem**, $Y$ is quantitative - Examples: price, blood pressure, etc.
   - In the **classification problem**, $Y$ takes values in a finite, unordered set (survived/died, digit 0-9, cancer class of tissue sample).
- Consider training data $(x_1, y_1), \cdots , (x_N , y_N )$. These are observations (examples, instances) of these measurements.
- **Objectives:** On the basis of the training data we would like to:
    - Accurately predict unseen test cases.
    - Understand which inputs affect the outcome, and how.
    - Assess the quality of our predictions and inferences.

### Unsupervised learning

- There is no outcome variable, just a set of predictors (features) measured on a set of samples.
- The objective is to find groups of samples that behave similarly, find features that behave similarly, find linear combinations of features with the most variation.
- It is difficult to know how well your are doing.
- It is different from supervised learning, but can be useful as a pre-processing step for supervised learning.

## Statistical Learning Versus Machine Learning

- Machine learning arose as a subfield of Artificial Intelligence. Statistical learning arose as a subfield of Statistics.
- There is much overlap — both fields focus on supervised and unsupervised problems:
    - Machine learning has a greater emphasis on large scale applications and prediction accuracy.
    - Statistical learning emphasizes models and their interpretability, and precision and uncertainty.

References
1. Gareth James, Daniela Witten, Trevor Hastie, and Robert TibshiraniAn (2021). Introduction to Statistical Learning with Applications in R (Chapter 1).




