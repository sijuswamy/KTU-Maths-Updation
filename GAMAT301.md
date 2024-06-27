# Mathematical Foundations for Algorithm Design, Probabilistic Machine Learning, and Real-Time Modeling

## Module 1: Limit Theorems

### Topic 1: Markov’s Inequality

#### Introduction
Consider a situation where a company wants to ensure that the probability of a system's downtime exceeding a certain threshold is minimal. They need a method to bound this probability using minimal information about the system's distribution.

#### Heuristic Solution
Using Markov’s Inequality, which provides an upper bound on the probability that a non-negative random variable exceeds a given value, we can offer a solution.

#### Statistical Theory
Markov’s Inequality states that for a non-negative random variable $X$ and $a > 0$, $P(X \geq a) \leq \frac{E[X]}{a}$

#### Problems
1. Given $E[X] = 5$, find the upper bound for $P(X \geq 10)$.
 **Solution:**
   Given $E[X] = 5$, find the upper bound for $P(X \geq 10)$.

To solve this, we apply **Markov's Inequality**, which states:
$P(X \geq a) \leq \frac{E[X]}{a}$

Substituting $E[X] = 5$ and $a = 10$:
$P(X \geq 10) \leq \frac{5}{10} = 0.5$

Therefore, the upper bound for $P(X \geq 10)$ is $0.5$ or $50\%$.

This means that the probability of $X$ exceeding $10$ is at most  $0.5$.

2. Simulate the distribution of the sample mean for rolling a die with sample size 50.
3. If $X$ represents the time (in hours) a server is down in a day with $E[X] = 2$, what is the upper bound for $P(X \geq 4)$?
4. For a non-negative random variable with $E[X] = 7$, determine $P(X \geq 14)$.
5. A random variable $X$ has $E[X] = 12$. Find $P(X \geq 15)$.
6. If $E[X] = 3$, what is $P(X \geq 9)$?

#### Solutions (Python)

All the above mentioned problems can be solved using `Python` scripts as follows. Here we pass the expected value and the bound as an ordered pair.
```python
import sympy as sp

def markov_inequality(expected_value, threshold):
    return expected_value / threshold

# Example solutions
problems = [(5, 10), (2, 4), (7, 14), (12, 15), (3, 9)]
solutions = [markov_inequality(e, a) for e, a in problems]
solutions
```
### Topic 2: Chebyshev’s Inequality

#### Introduction
Suppose we want to know how much the return on investment (ROI) of a stock varies from the mean ROI, given we only know the mean and variance of the ROI.

#### Heuristic Solution
Chebyshev’s Inequality helps us determine the probability that a random variable deviates from its mean by more than a certain amount, using its variance.

#### Statistical Theory
Chebyshev’s Inequality states that for any random variable $X$ with mean $\mu$ and variance $\sigma^2$, $P(|X - \mu| \geq k\sigma) \leq \frac{1}{k^2}$

#### Problem Statement
Given $E[X] = 10$ and $Var(X) = 4$, find the upper bound for $P(|X - 10| \geq 4)$.

#### Solution (Python)
```python
def chebyshev_inequality(variance, k):
    return 1 / (k**2)

# Given values
mean = 10
variance = 4
k = 4 / np.sqrt(variance)  # Calculate k such that k*sigma = 4

# Apply Chebyshev's Inequality
upper_bound = chebyshev_inequality(variance, k)
upper_bound
```
#### Problems

1. **Problem 1:** For a random variable with $E[X] = 0$ and $Var(X) = 9$, find the upper bound for $P(|X| \geq 6)$.

2. **Problem 2:** Given $E[X] = 5$ and $Var(X) = 25$, determine the upper bound for $P(|X - 5| \geq 10)$.

3. **Problem 3:** If $E[X] = 8$ and $Var(X) = 16$, find $P(|X - 8| \geq 4)$.

4. **Problem 4:** A random variable $X$ has $E[X] = 12$ and $Var(X) = 36$. Calculate the upper bound for $P(|X - 12| \geq 12)$.

5. **Problem 5:** For $E[X] = 15$ and $Var(X) = 4$, what is $P(|X - 15| \geq 4)$?

#### Solutions (Python)

```python
import numpy as np

def chebyshev_inequality(variance, k):
    return 1 / (k**2)

# Problem 1
mean1 = 0
variance1 = 9
k1 = 6 / np.sqrt(variance1)
solution1 = chebyshev_inequality(variance1, k1)

# Problem 2
mean2 = 5
variance2 = 25
k2 = 10 / np.sqrt(variance2)
solution2 = chebyshev_inequality(variance2, k2)

# Problem 3
mean3 = 8
variance3 = 16
k3 = 4 / np.sqrt(variance3)
solution3 = chebyshev_inequality(variance3, k3)

# Problem 4
mean4 = 12
variance4 = 36
k4 = 12 / np.sqrt(variance4)
solution4 = chebyshev_inequality(variance4, k4)

# Problem 5
mean5 = 15
variance5 = 4
k5 = 4 / np.sqrt(variance5)
solution5 = chebyshev_inequality(variance5, k5)

solutions = [solution1, solution2, solution3, solution4, solution5]
solutions
```
