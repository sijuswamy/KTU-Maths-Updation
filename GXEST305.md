# $\color{blue}{\text{Introduction to Artificial Intelligence and Data Science}}$ (Common to Groups B, C & D)

----
## Module-1 Introduction to AI and Machine Learning
Basics of Machine Learning - types of Machine Learning systems-challenges in ML- Supervised learning model example- regression models- Classification model example- Logistic regression-unsupervised model example- K-means clustering. Artificial Neural Network- Perceptron- Universal Approximation Theorem (statement only)- Multi-Layer Perceptron- Deep Neural Network- demonstration of regression and classification problems using MLP.

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
- Introduce the concept of Singular Value Decomposition (SVD) with a suitable example and formulate the mathematical approach.
- Define the terms in SVD and solve a simple example with three dimensional matrix.
- Demonstrate the SVD as an image compression model with a suitable example.
- Introduce the curse of dimensionality reduction and present the PCA
- Explain the significance of principal components as latent vectors with proper explanation
- Provide matrices upto third order to find principal components.
>**Note:** From this module, theory questions like the SVD and PCA algorithm and problems to find $U$ matrix, $V$ matrix and $\Sigma$ (from SVD) and to find the principal compnents of matrices (from PCA) will be used for both internal and end semester assessments.
