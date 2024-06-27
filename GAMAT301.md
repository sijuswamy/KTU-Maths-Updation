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
### Topic 3: Discrete-Time Markov Processes

**Introduction**  
Discrete-time Markov processes are stochastic models where the probability of moving to a future state depends only on the current state and not on the sequence of events that preceded it. They are widely used in modeling systems that evolve in discrete steps, such as queues, networks, and biological systems.

**Definition**  
A discrete-time Markov process $\{X_n\}_{n \in \mathbb{N}}$ is characterized by:
- A set of states $S$.
- Transition probabilities $P(X_{n+1} = j \mid X_n = i)$, which denote the probability of moving to state $j$ at time $n+1$ given the process is in state $i$ at time $n$.

**Key Properties**
- **Markov Property:** The future state depends only on the current state, not on the sequence of states that preceded it.
- **Transition Matrix:** Represents all transition probabilities between states.

**Discrete-Time Markov Chain**  
A Markov chain is a special case of a discrete-time Markov process where the state space $S$ is finite or countably infinite.

**Problems**

1. **Problem 1:** Consider a simple two-state Markov chain with transition matrix:
   
   $P = \begin{pmatrix}
   0.8 & 0.2 \\\
   0.3 & 0.7
   \end{pmatrix}$
   
   Calculate $P(X_3 = 2 \mid X_0 = 1)$.

2. **Problem 2:** For a three-state Markov chain with transition matrix:
   $$
   P = \begin{bmatrix}
   0.4 & 0.3 & 0.3 \\
   0.1 & 0.6 & 0.3 \\
   0.2 & 0.5 & 0.3
   \end{bmatrix}
   $$
   Find $P(X_2 = 3 \mid X_0 = 1)$.

3. **Problem 3:** Define an absorbing Markov chain with transition matrix:
   $$ P = \begin{bmatrix}
   1 & 0 & 0 \\
   0.2 & 0 & 0.8 \\
   0 & 0 & 1
   \end{bmatrix}
   $$
   Calculate the expected number of steps to reach absorption starting from state 2.

**Solutions (Python)**

```python
import numpy as np

# Problem 1
P1 = np.array([[0.8, 0.2], [0.3, 0.7]])
P1_3_2 = np.linalg.matrix_power(P1, 3)[1, 1]
solution1 = P1_3_2

# Problem 2
P2 = np.array([[0.4, 0.3, 0.3], [0.1, 0.6, 0.3], [0.2, 0.5, 0.3]])
P2_2_3 = np.linalg.matrix_power(P2, 2)[0, 2]
solution2 = P2_2_3

# Problem 3
P3 = np.array([[1, 0, 0], [0.2, 0, 0.8], [0, 0, 1]])
absorbing_states = [0, 2]
Q = P3[np.ix_(absorbing_states, absorbing_states)]
N = np.linalg.inv(np.eye(Q.shape[0]) - Q)
expected_steps = N[1, 1]
solution3 = expected_steps

solutions = {
    "Problem 1": solution1,
    "Problem 2": solution2,
    "Problem 3": solution3
}
solutions
```
