# Price Optimization & Customer Clustering with Genetic Algorithms

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/YOUR_GITHUB_USERNAME/YOUR_REPO_NAME/main?labpath=AI_P6_f.ipynb)  
> **Note:** Please replace `YOUR_GITHUB_USERNAME` and `YOUR_REPO_NAME` in the link above with your actual GitHub details.

## Overview 📝

This project explores price optimization for a supermarket dataset using a **Genetic Algorithm (GA)** to maximize profit. It also involves customer segmentation through two different clustering techniques: **K-Means** and a **Genetic Algorithm**, comparing their effectiveness.

The core objectives are:
1. To develop a Genetic Algorithm that finds the best **discount rate** and **sales multiplier** to maximize total profit.
2. To segment customers into distinct groups to understand their purchasing behavior using the **K-Means clustering** algorithm.
3. To implement a separate **Genetic Algorithm for clustering** and compare its performance against K-Means based on the Mean Squared Error (MSE).

---

## Methodologies ⚙️

Two primary Python scripts were developed to achieve the project's goals.

### 1. Profit Optimization with GA & K-Means Clustering

This approach combines a Genetic Algorithm for optimization with K-Means for customer analysis. The GA's fitness function is total profit, which it aims to maximize by evolving chromosomes representing the `discount` and `sales_multiplier`.

#### Key Components
* **Genetic Algorithm**: Optimizes two business parameters to maximize profit.
* **K-Means Clustering**: Segments customers based on their sales, quantity, discount, and profit data.
* **Linear Regression**: Predicts future sales based on training data.

#### Genetic Algorithm Implementation

The `GeneticAlgorithm` class evolves a population of potential solutions (chromosomes) through selection, crossover, and mutation:

```python
import random

class GeneticAlgorithm:
    def __init__(self, population_size, mutation_rate, crossover_rate, data):
        self.population_size = population_size
        self.mutation_rate = mutation_rate
        self.crossover_rate = crossover_rate
        self.data = data
        self.population = self.initialize_population()

    def initialize_population(self):
        population = []
        for _ in range(self.population_size):
            chromosome = {
                'discount': random.uniform(0, 0.8),
                'sales_multiplier': random.uniform(0.5, 1.5)
            }
            population.append(chromosome)
        return population

    def fitness(self, chromosome):
        total_profit = 0
        for index, row in self.data.iterrows():
            discount = chromosome['discount']
            sales_multiplier = chromosome['sales_multiplier']
            profit_row = row['Profit'] * sales_multiplier * (1 - discount)
            total_profit += profit_row
        return total_profit

    def evolve(self, generations):
        best_fitness_history = []
        for generation in range(generations):
            # Selection, Crossover, and Mutation steps happen here
            # ...
            best_chromosome = max(self.population, key=self.fitness)
            best_fitness = self.fitness(best_chromosome)
            best_fitness_history.append(best_fitness)
        return best_fitness_history

    def fitness(self, chromosome):
        total_profit = 0
        for index, row in self.data.iterrows():
            discount = chromosome['discount']
            sales_multiplier = chromosome['sales_multiplier']
            profit_row = row['Profit'] * sales_multiplier * (1 - discount)
            total_profit += profit_row
        return total_profit

    def evolve(self, generations):
        best_fitness_history = []
        for generation in range(generations):
            # Selection, Crossover, and Mutation steps happen here
            # ...
            best_chromosome = max(self.population, key=self.fitness)
            best_fitness = self.fitness(best_chromosome)
            best_fitness_history.append(best_fitness)
        return best_fitness_history


