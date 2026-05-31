# BigBasket Market Basket Analysis

## Overview

This project performs Market Basket Analysis (MBA) using the BigBasket product dataset. The objective is to discover relationships between product categories and identify patterns that can help in cross-selling, recommendation systems, and retail analytics.

Since the dataset does not contain real customer transaction histories, pseudo-transactions were created by grouping products based on brand and sub-category relationships.

---

## Dataset

Dataset Used:

[BigBasket Entire Product List Dataset](https://www.kaggle.com/datasets/surajjha101/bigbasket-entire-product-list-28k-datapoints?utm_source=chatgpt.com)

Dataset Features:

* Product Name
* Category
* Sub Category
* Brand
* Sale Price
* Market Price
* Rating
* Description

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* MLXtend
* NetworkX

---

## Workflow

```text id="i18s2v"
Dataset Loading
    ↓
Data Cleaning
    ↓
Pseudo Transaction Creation
    ↓
Transaction Encoding
    ↓
Apriori Algorithm
    ↓
Frequent Itemset Mining
    ↓
Association Rule Generation
    ↓
Visualization
    ↓
Business Insights
```

---

## Market Basket Analysis Process

### 1. Transaction Creation

Since real transaction data was unavailable, transactions were simulated using:

```text id="x4m9c1"
Brand → Grouped Sub Categories
```

This allowed the creation of meaningful baskets for association rule mining.

---

### 2. Frequent Itemset Mining

The Apriori algorithm was used to identify frequently occurring product combinations using support values.

Metrics used:

* Support
* Confidence
* Lift

---

### 3. Association Rule Mining

Association rules were generated to identify strong product relationships.

Example:

```text id="zv8kcn"
If customer buys Men's Grooming
→ likely to buy Fragrances & Deos
```

---

## Key Insights

### Strong Product Associations

| Antecedent                   | Consequent        | Lift  |
| ---------------------------- | ----------------- | ----- |
| Men's Grooming               | Fragrances & Deos | 10.22 |
| Hair Care + Bath & Hand Wash | Skin Care         | 8.67  |
| Skin Care + Bath & Hand Wash | Hair Care         | 7.99  |
| Hair Care + Skin Care        | Bath & Hand Wash  | 7.98  |
| Hair Care                    | Skin Care         | 5.19  |

---

## Visualizations Included

* Top Frequent Itemsets
* Association Network Graph
* Support vs Confidence Scatter Plot
* Association Heatmap

---

## Business Applications

* Cross-selling
* Product bundling
* Retail recommendation systems
* Shelf placement optimization
* Personalized marketing
* Customer behavior analysis

---

## Limitations

```text id="h15v1i"
The dataset does not contain real customer purchase transactions.
```

Therefore, pseudo-transactions were generated for analytical purposes.

---

## Results

The project successfully identified meaningful associations between product categories and demonstrated how Market Basket Analysis can be applied in retail analytics even with limited transaction-level data.

---

## Future Improvements

* Use real customer transaction datasets
* Implement FP-Growth algorithm
* Build recommendation engine
* Add interactive dashboards
* Deploy analytics application

---

## How to Run

Install dependencies:

```bash id="mjlwmv"
pip install pandas numpy matplotlib seaborn mlxtend networkx
```

Run the notebook step by step to:

* Load dataset
* Generate transactions
* Mine association rules
* Visualize relationships
* Generate business insights

---

## Conclusion

This project demonstrates the use of association rule mining techniques on retail product data to uncover hidden product relationships and generate actionable business insights for e-commerce and retail platforms like BigBasket.
