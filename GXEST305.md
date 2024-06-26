# $\color{blue}{\text{Introduction to Artificial Intelligence and Data Science}}$ (Common to Groups B, C & D)

----
## Module-1 Introduction to AI and Machine Learning
>Basics of Machine Learning - types of Machine Learning systems-challenges in ML- Supervised learning model example- regression models- Classification model example- Logistic regression-unsupervised model example- K-means clustering. Artificial Neural Network- Perceptron- Universal Approximation Theorem (statement only)- Multi-Layer Perceptron- Deep Neural Network- demonstration of regression and classification problems using MLP.

- Introduce the concept of machine learning with proper example and illustrations
- Explain different types of machine learning- Supervised, unsupervised and Reinforcement learning with proper contexts (Use branch specific examples).
- Introduce linear regression as an example of supervised learning technique- use statistical or least square method to find the coefficients in the linear legression equation, $y=\beta_0+\beta_1 x$ ( Use microsoft excel utility for demonstration).
- Introduce the concept of classification with a simple example where the output variable takes only two values- $0$ and $1$. First try the regression, then explain the inappropriateness of the regression model with some predictions based on the model. Demonstrate the sigmoid function- $\sigma(x)=\dfrac{1}{1+e^{-z}}$ where $z=\beta_0+\beta_1 x$. Explain the concept of logit function and its role in converting continuous variable to probability measure.
- Introduce the concept of K-means clustering as an unsupervised learning method using the `iris` dataset (choose two features). Better to visualize the clusters formed. Instructor should compare the number of clusters suggested by the ML algorithm and the actual number of clusters (for the iris dataset, there are only three classes but the clustering algorithm may suggest more clusters!)
- Introduce a perceptrone and a simple ANN in comparison with human neuron emphasizing the beauty of the architecture in terms of incorporating mathematical tools for iterative optimization (Explain the input to intermediate layer as linear combination of inputs, activation function and its role in capturing non-linearity, backpropagation as the error minimization using calculus tools.The blackbox nature of the neural network should be scientifically unraveled).
- The universal Approximation Theorem should be introduced as a proof or guaranty that  any problem can be solved successfully using ANN.
- Demonstrate the classification of MNIST dataset using a Multilayer Perceptron.
>**Note:** From this module , theory questions like the types of machine learning, steps in linear and logistic regression, simple problems to cluster a tabular data  with at most two features and 10 samples and basics of ANN will be used for both internal and end semester assessments.
----

# Module-2: Mathematical Foundations of AI and Data science:

>Role of linear algebra in Data representation and analysis – Matrix decomposition- Singular Value Decomposition (SVD)- Spectral decomposition- Dimensionality reduction technique-Principal Component Analysis (PCA).

- Introduce the concept of data and its representation interactively. The instructor is advised to circulate a Google form link that capture basic details of the students like Name, Gender, Age, Height, Weight and expectation about the engineering programme. The collected data will be shown to the students as the Google sheet and explain that the data is stored as matrix with columns as features and rows as samples. Various data types should be explained in this context.
- Introduce the concept of matrix decomposition and its relevence using a practical example.
- Introduce the concept of Singular Value Decomposition (SVD) with a suitable example and formulate the mathematical approach. Better to explain the concept visually using an image compression example.
- Define the terms in SVD and solve a simple example with three dimensional matrix. Explain the geometry of SVD as - Rotattion - scaling- Rotation in succession.
- Introduce the curse of dimensionality and present the PCA as a solution that transfer the given data into a new cordinate system.
- Explain the significance of principal components as latent vectors with proper explanation.
- Create principal components of matrices of order upto 3.
>**Note:** From this module, theory questions like the SVD and PCA algorithm and problems to find $U$ matrix, $V$ matrix and $\Sigma$ (from SVD) and to find the principal compnents of matrices (from PCA) will be used for both internal and end semester assessments.
----

# Module-3: Applied Probability and Statistics for AI and Data Science
>Basics of probability-random variables and statistical measures - rules in probability- Bayes theorem and its applications- statistical estimation-Maximum Likelihood Estimator (MLE) - statistical summaries- Correlation analysis- linear correlation (direct problems only)- regression analysis- linear regression (using least square method).

- Introduce the concept of random variable with a coin toss experiment.
- Define the expectation as a weighted average with weight as probability and variance as the variability in the distribution about the expected measures.
- Explain the rules in probability- sum rule, conditional probability, multiplication rule and its applications.
- Bayes' theorem and its application. Instructor should emphazise the advantage of Bayes' probability in informed decision making.
- Introduce the concept of estimation as a realistic approximation.
- Present the concept of joint distribution of iid random variables and introduce the MLE as a method of estimating the parameters of an assumed probability distribution, given some observed data.
- Introduce the concept of correlation with proper demonstration and give an insight on linear and non-linear association of input and response variables.
- Present the statistical formula to find correlation coeffcient of a bivariate data.The instructor should explain the difference between correlation and covariance with suitable examples.
- Introduce the statistical formula for linear regression using least square method.
- Measures of fit of regression models- Mean square error, $R^2$ value and $F-$ test.
- Compare the regression obtained through Machine Learning algorithm and Statistical methods. For this the instructor is advised to demonstrate the regression coefficients of both ML approach (using `LinearRegression()` model from `scikitlearn` library  and a simple MLP) and the least square model using `statmodels` library. By this the students should realize the fact that ML models performs at par with traditional statistical models. For a smaller dataset, statistical models are advisable but for large dataset with many features, the ML approach is desirable.
>**Note:** From this module, theory question related to MLE and problems from basic probability, Bayes' theorem, correlation analysis and  linear regression with maximum 10 samples will be used for both internal and end semester assessments.
---

# Module-4: Basics of Data Science
>Benefits of data science-use of statistics and Machine Learning in Data Science- data science process - applications of Machine Learning in Data Science- modelling process- demonstration of ML applications in data science- Big Data and Data Science. (For visualization the software tools like Tableau, PowerBI, R or Python can be used. For Machine Learning implementation, Python, MATLAB or R can be used.)

- Introduce the need of scientific approach to analyse data with suitable examples like- stock market data, streamflow data, whether data etc. Through this session the students should realize the fact that what we see in the spread sheets are just representation. To get meaningful insight, one should use appropriate tools systematically.  The instructor should use suitable insightful visulaizations to achieve this objective.
- Present the the statistical measures like mean, variance, interquartile range etc. are used for better insights from the data.
- Introduce Machine Learning as a tool to get better insights from the given dataset.
- Introduce various steps in data science process with proper illustration. Emphasize each step in this process especially data cleaning and EDA.
- Explore interconnections between statistical summaries and visualizations. For example boxplot and five point statistical summary, data distribution and density plot etc.
- Introduce the Machine Learning model design and development in data science perspective.
- Demonstrate at least three ML applications in datascience through proper branch specific case studies.

>**Note:** From this module, theory questions related to data science process, machine learning modelling process, important visualization methods and applications of ML in data science will be used for both internal and end semester assessments.
