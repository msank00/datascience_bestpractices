# Techinical Mistakes while Model Building

- Create a `non-reproducible` data preparation steps
- Evaluate a model based on performance of training set
- Didn't notice `large outlier`
- Dropped missing values when it made sense to flag them
- Flagged missing values when it made sense to drop them
- Set missing values to Zero
- Not comparing a complex model to a **simple baseline**
- Failed to understand nuances of data collection
- Build model for **wrong point in time**
- Deleted records with missing values
- Predicted the wrong outcome
- Made **faulty assumptions** about `time zones`
- Made **faulty assumptions** about `data format`
- Made **faulty assumptions** about `data source`
- Included `anachronistic` (belonging to a period other than that being portrayed) variables
- Treated categorical variables as continuous
- Treated continuous variables as categorical
- Filtered training set to **incorrect population**
- Forgot to include `y-variable` in the training set
- Didn't look at **number of missing** values in column
- Not filtering for **duplicates** in the dataset
- Accidently included `ID` field as predictors
- Failing to bin or account for **rare categories**
- Using proxies of outcomes as predictors
- Incorrect handling of `missing values`
- Capped outliers in a way that didn't make sense with data
- **Misunderstanding of variable** relationships due to incomplete EDA
- Failed to create calculated variables from raw data
- Building model on the wrong population

#### Reference
- [tweet_Caitlin_Hudon](https://twitter.com/beeonaposy/status/1122964504910938121)
- [ICLR2019_Workshop_on_Debug_ML](https://github.com/debug-ml-iclr2019/debug-ml-iclr2019.github.io)


