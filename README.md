# Bayesian Modeling on Recipe and Customer Review Data
## Problem Discription
This project is to use Bayesian Machine Learning to build predictive models on recipes and customer reviews datasets. By predicting fundamental recipe properties, such as calories and cooking time, and understanding users’ behavior and preferences, this project generates insights of restuarants' performance and knowledge to encourage healthy dietary choices. 
We aimed to answer three specific questions:  
1. Classify customer reviews to two categories (high or low), based on minutes to cook, number of steps, number of ingredients, calories and six nutrition facts (total fat, sugar, sodium, protein, saturated_fat, carbohydrates) of a recipe. 
2. Predict calories of a recipe, using these six nutrition facts. 
3. Predict how many minutes a recipe takes to prepare, using the number of steps, number of ingredients, calories and six nutrition facts.
## Data Discription
With the two raw datasets consisting of 180K+ recipes and 700K+ recipe reviews from Kaggle (https://kaggle.com/shuyangli94/food-com-recipes-and-user-interactions), we selected features related to nutritional information, customers’ ratings and cooking complexity. For computational efficiency, we subsetted the original datasets by randomly sampling 100,000 observations to our training dataset, on top of dropping all of the missing values and meaningless rows.
## Two Versions of Approach

### MCMC Sampling Approach in R
Using 'JAGS' package, we first specified the prior distributions of parameters and the likelihood function/model of response variable in our models, then run MCMC sampler on each model, and after conducting model selection and performance estimation from results of convergence diagnose(trace plots, gelman diagnose) and DIC values, we plotted the posterior density distributions of each parameters. Detailed modeling process in 'report_r.html' and 'code_r.Rmd'.

### Variational Inference Approach in Python
For the fact that the datasets in this project were extremely large in size, MCMC sampling method was found to struggle. We used approximation with Variational Inference in Python to train these models on larger datasets, for improvement on data reliability. Detailed information in 'report_python.pdf' and 'code_python.ipynb'.
