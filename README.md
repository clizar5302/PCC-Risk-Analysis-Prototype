# Extended Risk Score Calculator

## Overview
The **Extended Risk Score Calculator** is a Python program designed to assess the financial risk associated with customers based on several key metrics. By evaluating factors such as aging dates, eligibility percentages, availability, accounts receivable (AR) turn days, dilution rates, and risk ratings, this program generates an Extended Risk Score for each customer. 

This project aims to help financial institutions make informed decisions by identifying the riskiest customers and providing normalized risk scores for further analysis.

## Features
- Calculate an **Extended Risk Score** for each customer based on various criteria.
- Sort and display the top 5 riskiest customers based on the Extended Risk Score.
- Provide insights on loan balances, AR turn days, dilution, and historical averages.
- Normalize the Extended Risk Score using a sigmoid function for better interpretability.

## Requirements
To run this program, you need:
- Python 3.x
- Pandas
- NumPy
- Any additional libraries as specified in the code

You can install the required libraries using pip:
pip install pandas numpy

## Usage

1. Import the necessary libraries:
2. Load your data into a Pandas DataFrame.
3. Define the function to calculate the Extended Risk Score.
4. Run the score calculation and sorting logic as provided in the main script.
5. Review the results, including the top 5 riskiest customers and normalized risk scores.

## Results

The program outputs:

- The top 5 customers based on their Extended Risk Score.
  - The normalized risk scores for a better understanding of risk levels.
- The top 5 customers in order of:
  1. Size of loan
  2. AR Turn Days
  3. AR Turn Days compared with AR Turn Historical Average
  4. Dilution
  5. Dilution compared with Historical Average

## Example

Here’s a brief example of how the calculation is performed:
```bash
current_date = datetime.now()
df['Extended Risk Score'] = df.apply(lambda row: calculate_risk_score(row, current_date), axis=1)

