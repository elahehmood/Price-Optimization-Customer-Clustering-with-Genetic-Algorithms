# Optimization of Pricing and Customer Segmentation using Genetic Algorithm and K-Means

## Abstract 📄

This project explores the use of **Genetic Algorithms (GA)** and **K-Means clustering** to optimize customer pricing strategies and analyze purchasing behaviors. Using a supermarket sales dataset, we aim to identify optimal discounts and sales multipliers that maximize profit, while also segmenting customers into meaningful groups.  
The combined use of evolutionary computation and clustering demonstrates how intelligent algorithms can improve business decision-making and commercial performance.

**Keywords**: Genetic Algorithm, K-Means, Customer Segmentation, Profit Optimization, Pricing Strategy

---

## Table of Contents 📋

* [Introduction](#introduction-)
* [Genetic Algorithm for Profit Optimization](#genetic-algorithm-for-profit-optimization-)
* [Customer Segmentation with K-Means](#customer-segmentation-with-k-means-)
* [Comparison of Approaches](#comparison-of-approaches-)
* [Conclusion & Future Work](#conclusion--future-work-)
* [References](#references-)

---

## Introduction 💡

In today’s competitive sales market, optimizing pricing and understanding customer behavior are essential for maximizing profitability. This project applies computational intelligence techniques — primarily **Genetic Algorithms** and **K-Means clustering** — to:  

* Optimize discount and sales multipliers for improved profit.  
* Segment customers based on purchasing behavior.  
* Provide insights into how pricing strategies influence customer clusters.  

The combination of **profit optimization** and **behavioral analysis** enables businesses to make data-driven decisions that can directly impact performance.

---

## Genetic Algorithm for Profit Optimization 🧬

The **Genetic Algorithm (GA)** is implemented to search for the best combination of **discount rates** and **sales multipliers**.  

### Key Steps
- **Initialization**: Generate an initial population of solutions (discount + multiplier).  
- **Fitness Function**: Evaluate each solution based on total profit.  
- **Selection, Crossover, Mutation**: Apply evolutionary operators to improve solutions across generations.  
- **Termination**: After several generations, the best solution is returned as the optimized pricing strategy.  

### Results
- GA consistently found combinations of discounts and multipliers that **maximized profit**.  
- Visualizations of GA progress showed steady improvement of the fitness score across generations.  

---

## Customer Segmentation with K-Means 📊

To complement GA optimization, **K-Means clustering** was applied to segment customers based on features such as **sales, quantity, discount, and profit**.

### Process
- Preprocessing: Missing values handled, categorical variables encoded.  
- Feature scaling using **StandardScaler**.  
- Clustering with **K-Means** to group customers into clusters with similar purchasing behaviors.  

### Insights
- Different clusters represented distinct customer groups (e.g., discount-sensitive, high-profit, bulk buyers).  
- Clustering results help in tailoring marketing strategies for each segment.  

---

## Comparison of Approaches ⚖️

| Aspect                     | Genetic Algorithm | K-Means Clustering |
|----------------------------|------------------|--------------------|
| **Primary Goal**           | Profit maximization | Customer segmentation |
| **Optimization Target**    | Discounts & multipliers | Cluster assignments |
| **Evaluation Metric**      | Total profit (fitness) | Mean Squared Error (MSE) |
| **Application**            | Pricing strategy | Marketing & customer grouping |

Both methods complement each other: GA identifies **optimal pricing strategies**, while K-Means provides **behavioral insights** into how different customers respond to pricing.

---

## Conclusion & Future Work 🏁

### Conclusion
- Genetic Algorithms successfully optimized **discount and sales multipliers**, improving profitability.  
- K-Means clustering provided meaningful **customer segments**, useful for targeted marketing.  
- Combined, these techniques show strong potential for **data-driven business optimization**.  

### Future Work
- Test on larger and more diverse datasets.  
- Integrate **regression models** or **deep learning** for improved sales prediction.  
- Explore **real-time optimization systems** for dynamic pricing.  
- Combine clustering insights directly with GA for **personalized discounts per customer segment**.  
---

## 📓 Jupyter Notebook

You can explore the full analysis in the Jupyter Notebook:

[Optimization with Genetic Algorithm and K-Means.ipynb](Optimization-with-Genetic-Algorithm-and-K-Means.ipynb)

### Run Online 🚀

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/elahehmoood/Price-Optimization-Customer-Clustering-with-Genetic-Algorithms/blob/main/Optimization-with-Genetic-Algorithm-and-K-Means.ipynb)


[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/elahehmoood/Price-Optimization-Customer-Clustering-with-Genetic-Algorithms/HEAD?labpath=Optimization-with-Genetic-Algorithm-and-K-Means.ipynb)

---

## References 📚

* Holland, J.H. (1992). *Adaptation in Natural and Artificial Systems*. MIT Press.  
* Goldberg, D.E. (1989). *Genetic Algorithms in Search, Optimization, and Machine Learning*. Addison-Wesley.  
* Jain, A.K. (2010). *Data clustering: 50 years beyond K-Means*. Pattern Recognition Letters.  
* Mitchell, M. (1998). *An Introduction to Genetic Algorithms*. MIT Press.  
