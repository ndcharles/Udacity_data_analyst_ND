# Exploration of Prosper Loan Dataset
## by Ndidi Charles Nweke


## Dataset

The dataset consists of 113937 rows and 81 columns of loan data. It is financial dataset related to loan, borrowers, investors, interest rates and more.

Dataset can be accessed [here](https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv)

## Summary of Findings

> The highest charged-off loan is a $25,000 3 year loan to a self-employed borrowed for Other reasons. Their income range is $1 - 24,999 and their stated monthly income is 0.083333 but they are to pay $1047.64/month for the loan. Loan-Income-Ratio is over 1200000%

It all started with the question: Why would someone borrow money and refuse to pay back?

Of 81 variables, 22 were selected to help us answer the question at hand. 

In conclusion, given a loan term of 1, 3 and 5 years, 77.0% of borrowers settled for 3 years duration, 21.5% settled for 5 years and the remaining 1.4% was for those of 1 year duration. In an attempt to understand why people don't pay back their loans, we assumed that it is due to little income, being unemployed and also not being given enough time.

Finally, from the analysis so far, it is observed that, the duration has little to nothing to do with the borrower's ability to pay back the loan. Rather, the higher the ratio of the borrower's monthly loan repayment to their monthly income, the higher the likelihood of them having difficulty paying back. A close look at the average of the good and bad loan details below will help understand how a very large percentage of the bad borrower's income went to service debt.

| | Good loans | Bad loans |
| ----- | ----- | ----- |
| Monthly loan payment ($) | 279 | 239 |
| Stated monthly income (\$) | 5820 | 4550 |
| Loan-income-ratio (%) | 414 | 2838 |

This was further explored using the loan-income-ratio vs employment status to see their influence on the loan staus. It was then noticed that there is a large variation of loan-income-ratio amongst those tagged as unemployed, self-employed, retired and some employed who had bad loans.


## Key Insights for Presentation

The objective here is to understand "What factors affect a borrower’s ability to pay back a loan?" -- Loan Status. The focus was on exploring several features that could affect the Loan Status like Loan term, Stated Monthly Income, monthly loan payment, Income range and employment status to see how they contribute to borrower's ability to pay back a loan.

I looked at the distribution of loan status, the Employment status. Then the correlation of the Stated monthly Income, Monthly repayment and the loan term. I went further to create the loan-income-ratio column which combines monthly income and monthly loan payment. 

The plot of loan-income-ratio, loan terms and loan status showed that, irrespective of the duration, the higher the monthly payment to income, the lesser the likelihood of the borrower completing their payment. To prove this further, a plot of loan-income-ratio, employment status and loan status was created which showed that the borrowers who defaulted were those taking loans that would take almost 400% of their monthly income.