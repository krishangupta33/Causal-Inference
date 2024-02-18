# Causal-Inference

Refer: https://causalml.readthedocs.io/en/latest/about.html

## What is Causal Machine Learning?

Causal machine learning is a branch of machine learning that focuses on understanding the cause and effect relationships in data. It goes beyond just predicting outcomes based on patterns in the data, and tries to understand how changing one variable can affect an outcome. Suppose we are trying to predict a student’s test score based on how many hours they study and how much sleep they get. Traditional machine learning models would find patterns in the data, like students who study more or sleep more tend to get higher scores. But what if you want to know what would happen if a student studied an extra hour each day? Or slept an extra hour each night? Modeling these potential outcomes or counterfactuals is where causal machine learning comes in. It tries to understand cause-and-effect relationships - how much changing one variable (like study hours or sleep hours) will affect the outcome (the test score). This is useful in many fields, including economics, healthcare, and policy making, where understanding the impact of interventions is crucial. While traditional machine learning is great for prediction, causal machine learning helps us understand the difference in outcomes due to interventions.


## Steps to Perform Causal Inference

1. Load your dataset into a pandas DataFrame (df)
2. Create a CausalModel
    - Provide the dataframe as data
    - Define the treatment column names, an array of strings (I recommend using only one treatment)
    - Define the outcome_name, a string - y or target or label
    - Define common causes, an array of names of the columns, strings
    - You could try instruments / effect_modifiers as well, an array of names of the columns, strings (not mandatory)
3. View the model
4. Identify the effect
5. Estimate the effect
6. Refute the estimate (not mandatory)

### After performing these steps in the same notebook, you can manipulate the treatment column and observe different results. 