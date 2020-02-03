# Bayesian Modeling on Recipe and Customer Review Data

## Problem Discription
This project is to use Bayesian Machine Learning to build predictive models on recipes and customer reviews datasets. By predicting fundamental recipe properties, such as calories and cooking time, and understanding users’ behavior and preferences, this project generates insights of restuarants' performance and knowledge to encourage healthy dietary choices. 
We aimed to answer three specific questions:  
1. Classify customer reviews to two categories (high or low), based on minutes to cook, number of steps, number of ingredients, calories and six nutrition facts (total fat, sugar, sodium, protein, saturated_fat, carbohydrates) of a recipe. 
2. Predict calories of a recipe, using these six nutrition facts. 
3. Predict how many minutes a recipe takes to prepare, using the number of steps, number of ingredients, calories and six nutrition facts.

## Data Discription
With the two raw datasets consisting of 180K+ recipes and 700K+ recipe reviews from Kaggle (https://kaggle.com/shuyangli94/food-com-recipes-and-user-interactions), we selected features related to nutritional information, customers’ ratings and cooking complexity. For computational efficiency, we subsetted the original datasets by randomly sampling 100,000 observations to our training dataset, on top of dropping all of the missing values and meaningless rows.

## Two Versions of Bayesian Modeling Approach
### MCMC Sampling Approach in R

### Variational Inference Approach in Python
