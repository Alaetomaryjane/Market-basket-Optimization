# Market Basket Optimization using Apriori Algorithm
This project aims to uncover links and connections between items frequently bought together in retail settings. Utilizing Market Basket Analysis, a well-known method in data mining, helps businesses optimize sales strategies by understanding customer purchasing behavior.

## Table of Contents

- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Data Preprocessing](#data-preprocessing)
- [Market Basket Analysis](#market-basket-analysis)
- [Visualization](#visualization)
- [Evaluation](#evaluation)
- [Conclusion](#conclusion)

## Project Overview

Market Basket Optimization aims to uncover associations between products by analyzing transactions. These insights enable businesses to understand common purchasing patterns, design cross-selling strategies, and improve overall customer experience. The project leverages the **Apriori algorithm** to find frequent itemsets and extract valuable association rules from the dataset.

## Data Source

The dataset `market_basket_dataset.csv` contains transaction data, where each transaction is associated with a `BillNo` and the items purchased (`Itemname`). The data is cleaned and transformed to perform association rule mining.

## Data Preprocessing

1. **Data Inspection**: 
   - The dataset is loaded and inspected for any missing values or anomalies.
   - Unique values per column are checked for better understanding of the data distribution.

2. **Grouping Transactions**: 
   - Transactions are grouped by the `BillNo` to gather all items purchased together.
   - A one-hot encoding technique is applied to transform the data for market basket analysis.

3. **One-Hot Encoding**:
   - The `TransactionEncoder` from the `mlxtend` library is used to convert the transactional data into a binary matrix, where each row represents a transaction and each column represents whether an item was purchased.

## Market Basket Analysis

### Frequent Itemsets using Apriori Algorithm

The **Apriori algorithm** is applied to discover frequent itemsets that have a minimum support of 5%:

The top frequent itemsets reveal combinations of products that are often purchased together. The results help to identify potential product groupings that can be used for marketing and product placement strategies.

### Association Rules

Association rules are generated using the **confidence** and **lift** metrics to understand the strength of relationships between item pairs. For example:

- **Rule: Milk ⇒ Oranges**
  - **Confidence**: 50% (when Milk is bought, there is a 50% chance that Oranges are also purchased)
  - **Lift**: 2.64 (customers who buy Milk are 2.64 times more likely to buy Oranges)

## Visualization

1. **Top 10 Frequent Itemsets**:
   - A bar chart is created to visualize the top 10 frequent itemsets with the highest support.

![image](https://github.com/user-attachments/assets/9e7e93af-c1ae-420c-b748-ab2f6717e67b)

2. **Cross-Selling Matrix**:
   - A cross-selling matrix shows how often items are bought together, providing useful insights into cross-sell opportunities. This matrix is visualized as a heatmap to illustrate the relationships between different items.

![image](https://github.com/user-attachments/assets/be73b51b-0c12-47ab-b119-c296d73d5068)


## Evaluation Summary

Apriori algorithm effectively identifies the most frequent itemsets and the association rules extracted provide practical insight into how items are purchased together

## Conclusion

This project demonstrates the application of the Apriori algorithm for market basket optimization. The association rules and cross-selling matrix provide valuable insights for retailers to identify product combinations, optimize product placements, and enhance sales strategies.
