# $\color{blue}{\text{Mathematics for Computer and Information Science-3}}$

**Expected Cognitive Domain Level**- Understanding and Application

**Knowledge Category:** Procedure and Modelling

**Expected Affective Domain Level:**- Appreciate the Mathematical Background of Probabilistic Models and applications


>**Course Objective:** This second year course is the foundation for advanced topics in Computer Science like Machine Learning, Data Science, Quantum Computing etc. Up on successful completion of this course, the student will be able to understand the relevance of approximate solutions in unbounded input spaces. The key concept is to formulate a distribution from a data and use it for analysis and prediction.

>**How to introduce the course?** Refresh the concept of random experiment, sample space and probability as a measure of uncertainty through a simple random experiment of *tossing two coins simultaneously*. Tabulate the events, frequency and probability for each event. Use this table introduce the concept of distribution in two ways- the frequency distribution and probability distribution. Convey the important idea that creating a relative measure is better than absolute measure while analysis. So, Probability distribution tell us more about the random experiment.

----
## Module-1: Descrete distributions and applications

## Module-2: Continuous distributions and applications


## Module 3: Foundations of Random Process

>**Limit Theorems and its uses**

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

All the above-mentioned problems can be solved using `Python` scripts as follows. Here we pass the expected value and the bound as an ordered pair.
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
### Topic 3: Strong Law of Large Numbers

The Strong Law of Large Numbers (SLLN) is a fundamental theorem in probability theory that describes the behaviour of the sample average of a sequence of independent and identically distributed random variables.

#### Introduction

The Strong Law of Large Numbers states that for a sequence of i.i.d. random variables  $\{X_n\}_{n=1}^{\infty}$, if  $E[X_1] = \mu$, then with probability 1:$$\lim_{n \to \infty}\frac{1}{n}\sum_{i=1}^{n}X_i = \mu$$.

#### Key Concepts

1. **Independence:** Each random variable $X_i$ in the sequence is independent of others.
   
2. **Identically Distributed (i.i.d.):** Each $X_i$ follows the same probability distribution.

**Example-1: Rolling a Fair Die many times**
Consider an experiment where you roll a fair six-sided die repeatedly. Let  $X_i$ denote the outcome of the $i$-th roll, which is an integer between 1 and 6. Each $X_i$ is an independent and identically distributed (i.i.d.) random variable with an expected value $E[X_i] = 3.5$ (the mean of a fair die).

>**Objective of the demonstration:**
Demonstrate how the sample mean of the die rolls converges to the expected value \( 3.5 \) as the number of rolls \( n \) increases, according to the Strong Law of Large Numbers.
#### Python Implementation

```python
import numpy as np
import matplotlib.pyplot as plt
import ipywidgets as widgets
from IPython.display import display

# Function to update plot based on number of trials
def update_plot(num_trials):
    np.random.seed(42)  # For reproducibility
    max_rolls = 1000  # Maximum number of rolls

    # Simulate die rolls
    die_rolls = np.random.randint(1, 7, size=(num_trials, max_rolls))

    # Calculate cumulative means
    cumulative_means = np.cumsum(die_rolls, axis=1) / np.arange(1, max_rolls + 1)

    # Plotting
    plt.figure(figsize=(10, 6))
    for i in range(num_trials):
        plt.plot(np.arange(1, max_rolls + 1), cumulative_means[i], alpha=0.1, color='blue')

    plt.plot(np.arange(1, max_rolls + 1), np.mean(die_rolls, axis=0), color='red', linewidth=2, label='Average')
    plt.axhline(y=3.5, color='green', linestyle='--', label='True Mean')
    plt.title('Strong Law of Large Numbers: Convergence of Sample Mean')
    plt.xlabel('Number of Rolls')
    plt.ylabel('Sample Mean')
    plt.legend()
    plt.grid(True)
    plt.ylim(1, 6)
    plt.show()

# Create slider widget
num_trials_slider = widgets.IntSlider(value=100, min=10, max=1000, step=10, description='Number of Trials:')

# Display slider and plot
widgets.interactive(update_plot, num_trials=num_trials_slider)
```


>**Demonstrations:**
><https://colab.research.google.com/drive/1nFX0TuYGczqD0ilK6ZOYgpcZEIBggr5i>

#### Example: Coin Flipping Experiment

Consider an experiment where a fair coin is flipped repeatedly. Let \( X_i \) denote the outcome of the \( i \)-th flip (1 for heads, 0 for tails). Each \( X_i \) is i.i.d. with \( E[X_i] = 0.5 \).

#### Problems

1. **Problem 1:** For a fair coin flipped \( n \) times, use the Strong Law of Large Numbers to find the probability that the proportion of heads converges to 0.5 as \( n \) grows large.

2. **Problem 2:** Apply the Strong Law of Large Numbers to analyze the convergence behavior of the average score in a sequence of i.i.d. random variables.

#### Solutions (Python)

```python
import numpy as np

# Problem 1: Simulating coin flips and applying SLLN
n_trials = 100000
n_flips = 100
coin_flips = np.random.randint(0, 2, size=(n_trials, n_flips))
heads_proportion = np.mean(coin_flips, axis=1)
heads_convergence = np.mean(heads_proportion)

solution1 = heads_convergence

# Problem 2: Analyzing convergence of average score
n_samples = 1000
mean_values = np.random.normal(loc=0, scale=1, size=n_samples)
average_score_convergence = np.mean(mean_values)

solution2 = average_score_convergence

solutions = {
    "Problem 1": solution1,
    "Problem 2": solution2
}
solutions
```
### Introduction to the Central Limit Theorem

The Central Limit Theorem (CLT) is a fundamental theorem in probability theory that explains why many distributions tend to be close to the normal distribution. It states that the distribution of the sum (or average) of a large number of independent, identically distributed random variables approaches a normal distribution, regardless of the original distribution of the variables.

#### Statement of the Central Limit Theorem

Let \( X_1, X_2, \ldots, X_n \) be a sequence of independent and identically distributed random variables with mean \( \mu \) and finite variance \( \sigma^2 \). Then, as \( n \) approaches infinity, the distribution of the standardized sum of these random variables approaches a standard normal distribution. Mathematically, this can be expressed as:

\[ \frac{1}{\sqrt{n}} \left( \sum_{i=1}^n X_i - n\mu \right) \xrightarrow{d} \mathcal{N}(0, \sigma^2) \]

or equivalently,

\[ \frac{\sum_{i=1}^n X_i - n\mu}{\sigma \sqrt{n}} \xrightarrow{d} \mathcal{N}(0, 1) \]

where \( \xrightarrow{d} \) denotes convergence in distribution.

#### Practical Application in Computer Science

In computer science, the Central Limit Theorem is crucial for various applications, including:

1. **Algorithm Analysis:** Estimating the average case performance of algorithms.
2. **Machine Learning:** Understanding the distribution of sample means in training datasets.
3. **Quality Assurance:** Monitoring and controlling the quality of software processes.
4. **Network Traffic:** Modeling and predicting network load and data packet transmission times.

### Example: Analysing Network Traffic

Consider the scenario where we are analysing the time taken for data packets to travel across a network. The travel times are influenced by various factors and may follow different distributions. However, by using the Central Limit Theorem, we can approximate the distribution of the average travel time for a large number of packets as a normal distribution.

**Python Implementation with Interactive Demonstrations**

We will simulate the travel times of data packets across a network using a uniform distribution and demonstrate the Central Limit Theorem by showing how the sample mean distribution approaches a normal distribution as the sample size increases.

```python
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import ipywidgets as widgets
from IPython.display import display

# Function to update plot based on sample size
def update_plot(sample_size):
    np.random.seed(42)  # For reproducibility
    num_samples = 1000  # Number of samples

    # Simulate travel times (uniform distribution between 1 and 10 milliseconds)
    travel_times = np.random.uniform(1, 10, size=(num_samples, sample_size))

    # Calculate sample means
    sample_means = np.mean(travel_times, axis=1)

    # Plotting
    plt.figure(figsize=(12, 6))
    sns.histplot(sample_means, kde=True, color='blue')
    plt.title(f'Central Limit Theorem: Distribution of Sample Means (Sample Size = {sample_size})')
    plt.xlabel('Sample Mean')
    plt.ylabel('Frequency')
    plt.grid(True)
    plt.show()

# Create slider widget for sample size
sample_size_slider = widgets.IntSlider(value=10, min=10, max=500, step=10, description='Sample Size:')

# Display slider and plot
widgets.interactive(update_plot, sample_size=sample_size_slider)
```
**Examples:**

1. >Let $X$ be the number of times that a fair coin, flipped 40 times, lands heads. Find the probability that $X = 20$. Use the normal approximation and then compare it to the exact solution.
   


### Introduction to Stochastic Processes in Computer Science

Stochastic processes are essential tools in computer science, providing a mathematical framework to model and analyze systems that involve randomness or uncertainty. Understanding stochastic processes is crucial as they underpin algorithms, simulations, and models used across various domains in computer science.

**What is a Stochastic Process?**

A stochastic process is a collection of random variables indexed by time or space, where each variable represents the state of a system at a specific instance. It allows us to describe how a system evolves probabilistically over time or space.

**Key Concepts and Definitions**

1. **Random Variable**:(Revisit module 2)
   - **Definition**: A variable whose values are outcomes of a random phenomenon. In stochastic processes, random variables can represent states of a system, outcomes of experiments, or measurements from sensors.

2. **Stochastic Process**:
   - **Definition**: A family of random variables indexed by a parameter (often time). For a stochastic process \( \{X_t\}_{t \in T} \), each \( X_t \) represents the state of the system at time \( t \).

3. **Discrete-Time vs. Continuous-Time Processes**:
   - **Discrete-Time**: Time progresses in discrete steps (e.g., seconds, hours).
   - **Continuous-Time**: Time changes continuously (e.g., milliseconds, real-valued intervals).

4. **Markov Property**:
   - **Definition**: A stochastic process has the Markov property if the future state depends only on the present state and not on how the system arrived at the present state.
   - **Intuition**: Think of predictive text algorithms that suggest the next word based solely on the current word, disregarding previous words.

### Applications in Computer Science

- **Algorithm Design**: Stochastic processes help design algorithms that optimize under uncertain conditions, such as in optimization problems with random variables.
- **Machine Learning**: Many machine learning algorithms use stochastic processes to model data with inherent uncertainty or to explore probabilistic patterns.
- **Networking and Systems**: Modelling network traffic, system reliability, and performance metrics often involves stochastic processes to predict and optimize system behaviour.

**Importance in Computer Science:**

Stochastic processes provide a rigorous framework for:
- Predicting and optimizing systems under uncertainty.
- Simulating complex systems and analysing their behaviour.
- Making informed decisions in algorithm design and optimization.

Understanding stochastic processes equips computer science students with essential tools to tackle real-world problems involving randomness and uncertainty, making it indispensable in their professional toolkit.


## Module-4: Discrete-Time Markov Processes

**Introduction**  
Discrete-time Markov processes are stochastic models where the probability of moving to a future state depends only on the current state and not on the sequence of events that preceded it. They are widely used in modelling systems that evolve in discrete steps, such as queues, networks, and biological systems. A suitable example to introduce Markov processes and Markov chains in computer science could revolve around modelling user behaviour in web navigation or predicting text sequences. Here’s an example related to predicting user behaviour on a website is given below:
> **Presentation of the context:**
Imagine you are tasked with analysing how users navigate through a website. You want to predict the next page a user will visit based on their current page. This scenario can be effectively modelled using a Markov chain.

> **Background:** Suppose a website has three main pages: Home, Products, and Contact. Based on historical data, you observe the following transition probabilities between these pages:
- From Home, 60% of users go to Products and 40% go to Contact.
- From Products, 70% of users stay on Products, 20% go to Home, and 10% go to Contact.
- From Contact, 50% of users go to Home and 50% go to Products.

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
