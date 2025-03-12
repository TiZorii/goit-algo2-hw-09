# Homework on "Local Search, Heuristics, and Simulated Annealing"

Welcome! 🧠

Today, you will practice using three different local optimization approaches to minimize the Sphere function: Hill Climbing, Random Local Search, and Simulated Annealing.

You will master the principles of these algorithms, including how to set parameters such as the number of iterations, sensitivity to improvements (epsilon), and the temperature schedule (for simulated annealing).

This task will help you understand the differences between the methods, their strengths and weaknesses, and evaluate the effectiveness of these approaches in finding approximate minima in a multidimensional space.

Let’s get started?! 💪🏼

## Task Description

Implement a program to minimize the Sphere function \( f(x) = \sum_{i=1}^{n} x_i^2 \), using three different approaches to local optimization:

1. **Hill Climbing** algorithm
2. **Random Local Search**
3. **Simulated Annealing**

### Technical Requirements
The boundaries of the function are defined as \( x_i \in [-5, 5] \) for each parameter \( x_i \).

The algorithms should return the optimal point (a list of coordinates \( x \)) and the function value at this point.

Implement three optimization methods:

- `hill_climbing` – Hill Climbing algorithm
- `random_local_search` – Random Local Search
- `simulated_annealing` – Simulated Annealing

Each algorithm should accept an `iterations` parameter that defines the maximum number of iterations to perform.

The algorithms should finish execution under one of the following conditions:

1. The change in the objective function value or the position of the point in the solution space between two consecutive iterations becomes smaller than epsilon, where epsilon is the accuracy parameter and determines the algorithm's sensitivity to minor improvements.
   
2. For the simulated annealing algorithm, the temperature is considered: if the temperature decreases to a value smaller than epsilon, the algorithm terminates as this indicates that the algorithm's search capacity is exhausted.

### Acceptance Criteria
📌 The acceptance criteria are a mandatory condition for the mentor to consider the homework. If any of the criteria are not met, the mentor will send the task back for revision without evaluation. If you need clarification or get stuck on any step, feel free to reach out to the mentor on Slack.

The algorithms work within the specified range \( x_i \in [-5, 5] \). The program finds an approximation to the global minimum of the function. The results from all three algorithms are presented in text form in a clear format.

### Program Template

```python
import random 
import math

# Definition of the Sphere function
def sphere_function(x): 
    return sum(xi ** 2 for xi in x)

# Hill Climbing
def hill_climbing(func, bounds, iterations=1000, epsilon=1e-6): 
    pass

# Random Local Search
def random_local_search(func, bounds, iterations=1000, epsilon=1e-6): 
    pass

# Simulated Annealing
def simulated_annealing(func, bounds, iterations=1000, temp=1000, cooling_rate=0.95, epsilon=1e-6): 
    pass

if __name__ == "__main__":

    # Boundaries for the function
    bounds = [(-5, 5), (-5, 5)]

    # Running the algorithms
    print("Hill Climbing:")
    hc_solution, hc_value = hill_climbing(sphere_function, bounds) 
    print("Solution:", hc_solution, "Value:", hc_value)

    print("\nRandom Local Search:")
    rls_solution, rls_value = random_local_search(sphere_function, bounds) 
    print("Solution:", rls_solution, "Value:", rls_value)

    print("\nSimulated Annealing:")
    sa_solution, sa_value = simulated_annealing(sphere_function, bounds) 
    print("Solution:", sa_solution, "Value:", sa_value)
```
### Sample Output

```python
Hill Climbing: Розв'язок: [0.0005376968388007969, 0.0007843237077809137]
Значення: 9.042815690435702e-07

Random Local Search: Розв'язок: [0.030871215407484165, 0.10545563391334589]
Значення: 0.012073922664800917

Simulated Annealing: Розв'язок: [0.024585173708439823, -0.00484719941675793]
Значення: 0.0006279261084599791
```
