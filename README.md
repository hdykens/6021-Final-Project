# Machine Learning I Final Project💤📱
## By: Jacob Ellis, Maddie Smith, Jack Brennan, Anna Phillips, and Hannah Dykens
### Is phone usage/doom scrolling a significant predictor in the hours of sleep someone will get?
### What predictors are significant in predicting a bin of sleep hours for a person?

### 📁[`CDC_YRBS_EDA`](./CDC_YRBS_EDA)
*NOTE: Not used for subsequently for this project.*

Very preliminary Exploratory Data Analysis (EDA) for CDC Youth Risk Behavior Surveillance System. At the start of the project, our main focus was to see how doom scrolling affects sleep. We ultimately decided there was not enough data regarding phone usage with only one question (Q77 in the [CDC codebook](https://www.cdc.gov/yrbs/files/2025/2025-YRBS-Data-Users-Guide-Final.pdf)) asking about how often the respondent uses social media. Thus, we decided the Kaggle dataset below would be better. 

### 📁[`Kaggle_cleaning_eda`](./Kaggle_cleaning_eda)
Expansive EDA on the Kaggle data titled ["Sleep & Doomscrolling Habits Dataset"](https://www.kaggle.com/datasets/harpartapsingh13/sleep-and-doomscrolling-habits-dataset/data) from Kaggle. This is a fully synthetic dataset since health data is very protected.

### 📁[`Models`](./Models)
[`Sleep_LR_V1.ipynb`](Sleep_LR_V1.ipynb) provides initial data cleaning and implementation of a **linear regression** using almost all coefficients as predictors for sleep hours per night. Overall, the model seemed to predict most sleep hours to be between 6.5 to 8 when actual sleep hours were mostly between 6 and 9.5. This was strange and indicated to us that lasso regularization may be helpful to eliminate noisy coefficients.

[`Sleep_MNR_V1.ipynb`](Sleep_MNR_V1.ipynb) provides initial data cleaning and implementation of both **one vs. rest and multinomial regression** using almost all coefficients as predictors for sleep quality score. The issue here was that the data was heavily skewed towards higher sleep qualities. Grouping the lower quality sleep scores that were not as frequent did not seem to help by much. The best model selected was one vs. rest with a higher macro F1 by ~ 0.05 and a lower test log loss by ~ 0.07 from predicting that all participants have a the most common sleep quality score (the baseline). This indicates that this model may need lasso regularization to be better than the baseline.

### 📁[`Lasso Regularization`](./Lasso Regularization)
[`Linear Regression.ipynb`](Linear Regression.ipynb) 

### [`.gitignore`](.gitignore)
This is a standard .gitignore file that we have not edited.




