# Apriori Algorithm for Market Basket Analysis

This project implements the Apriori Algorithm for market basket analysis using the dataset `amazon_transactions.csv`. The goal is to find frequent itemsets from transactional data and help understand customer purchasing patterns.

## Table of Contents
- [Introduction](#introduction)
- [Technologies Used](#technologies-used)
- [Setup](#setup)
- [How to Run the Project](#how-to-run-the-project)
- [Explaining the Code](#explaining-the-code)
  - [Data Preprocessing](#data-preprocessing)
  - [Item Frequency Count](#item-frequency-count)
  - [Applying Apriori Algorithm](#applying-apriori-algorithm)
- [Results](#results)

## Introduction
Market basket analysis is a popular data mining technique used to identify associations between items in transactional data. This project uses the Apriori algorithm to find frequent itemsets in the `amazon_transactions.csv` dataset, which contains transaction data from a fictional e-commerce platform.

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- mlxtend (for Apriori algorithm)

## Setup

1. Clone the repository:
    ```bash
    git clone https://github.com/thapasagarsagar/Apriori-ALgorithm.git
    ```

2. Navigate to the project directory:
    ```bash
    cd market-basket-analysis-apriori
    ```

3. Install required libraries:
    ```bash
    pip install -r requirements.txt
    ```

4. Place the `amazon_transactions.csv` dataset in the project folder.

## How to Run the Project

1. Open the project in your preferred IDE.
2. Run the Python script:
    ```bash
    python apriori_algorithm.py
    ```

The script will output the frequent itemsets found in the transaction data and their support values.

## Explaining the Code

### Data Preprocessing
The first step involves reading and preprocessing the transactional data. The dataset is converted into a list of lists, where each sublist represents a transaction.

```python
market = []
for i in range(0, datasets.shape[0]):
    cus = []
    for j in datasets.columns:
        if type(datasets[j][i]) == str:
            cus.append(datasets[j][i])
    market.append(cus)
