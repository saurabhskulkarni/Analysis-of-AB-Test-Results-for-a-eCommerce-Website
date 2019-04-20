
# Analyze A/B Test Results

This project is a part of Udacity's Data Analyst Nanodegree Program. 

In this project, the result of an A/B test that was run by an e-commerce website is analyzed. A new web page was developed by the company in order to try and increase the number of users who decide to pay for the product. 

The goal of this project is to analyze the data to determine if the new web page should be implemented or not. 

## Getting Started

### Prerequisites

In order to run this code, you will need Python 3+ and csv files that contains data to analyze. 

You will need the following Python libraries. 

- Pandas
- Numpy
- Matplotlib
- Random

### Installation

To run this notebook:

1. Download the .ipynb Jupyter notebook file. 
2. Download the data files ab_data.csv and countries.csv.
3. Make sure all three files are in the same folder. 
4. Open an instance of Jupyter notebook from the folder where you saved all three files. 


### Goal of this notebook

Show a simple example of a A/B test and the use of probability in Python to analyze the test. It contains the following:

**Calculation of probabilities for conversion rate (users converting from old webpage to new)**

- Basic probability calculations and data handling
- Comparing probability of conversion between the two pages

**Hypothesis testing**

- Defining null and alternative hypothesis
- Simulating difference in probabilities of both pages using random binomial distribution 
- Use of statsmodels for logistic regression
- Obtain p-value to test signficance

**Adding country/location to the factors under analysis and test significance**

- Testing significance of factors (interaction and individual) after adding country as factor


### Analysis and Conclusion

- The probability of receiving the new page is 0.5 


- Initial analysis based on just probabilities did not give us conclusive evidence. The probability of conversion in control group (the group that receives old webpage) is higher than treatment group (group that receives new webpage). The probability of conversion regardless of page that user receives is 0.119. 


- We defined the null and alternative hypothesis based on difference of probabilities of conversion of old and new page. 


- We simulated 10000 with a new and old page convert rate under null hypothesis. 


- We then calculated the difference in conversion rates from the simulated values.


- We then had 10000 simulated difference in conversion rates and we stored these differences (values) in a variable.


- We plotted the distribution on these differences on a histogram and calculated p-value. The p-value calculated was 0.905. We failed to reject null hypothesis (which is: there is no difference in probabilities between conversion rates). 


- Failing to reject null hypothesis indicates that there is no difference in conversion rates between old and new page. 


- We then used z-score from statsmodels to explore similar results. Assuming 95% significance level and p-value, we failed to reject null hypothesis. 


- We also used logisitic regression to fit a model and see if there is significant difference in conversion rates. The p-value was found to be not statistically significant. 


- We also explored the possibility of influence of location on test results. We explore this by adding this factor to our model. We found that this factor affected the response (p value was less than significance level). 

