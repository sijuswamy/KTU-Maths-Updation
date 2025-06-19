# Module 2: Mathematical Foundations of AI and Data Science

In this module, we will explore the mathematical backbone of modern AI and Data Science: Linear Algebra. We will see how data is represented as matrices and how decomposing these matrices helps us uncover hidden patterns and simplify complex data.

---

### 1. Data and its Representation

Before we can analyze data, we need to understand what it is and how it's stored. In machine learning, data is almost always organized into a structured format.

#### Interactive Activity: Data Collection

To understand this, let's create our own dataset. Please fill out this Google Form with some basic, anonymous details.

> **Instructor's Note:** Create a simple Google Form with the following fields:
> *   Gender (Options: Male, Female, Other)
> *   Age (Numeric)
> *   Height (in cm, Numeric)
> *   Weight (in kg, Numeric)
> *   Briefly state your expectation for this course (Text)

Once the data is collected, it can be viewed in a Google Sheet. It will look something like this:

| Timestamp           | Gender | Age | Height | Weight | Expectation                                |
| ------------------- | ------ | --- | ------ | ------ | ------------------------------------------ |
| 2023/10/27 10:01 AM | Male   | 20  | 175    | 70     | To learn how to build AI models.           |
| 2023/10/27 10:01 AM | Female | 19  | 162    | 55     | Understand the math behind AI.             |
| 2023/10/27 10:02 AM | Male   | 21  | 180    | 85     | To get a good job in the data science field. |
| ...                 | ...    | ... | ...    | ...    | ...                                        |

This spreadsheet is, for all practical purposes, a **matrix**.

*   **Samples (Rows):** Each row in the sheet represents a single observation or data point. In this case, each row is a student. These are also called *instances* or *records*.
*   **Features (Columns):** Each column represents a specific attribute or property of our samples. 'Gender', 'Age', and 'Height' are all features. These are also called *variables* or *attributes*.

So, our data is an `m x n` matrix, where `m` is the number of students (samples) and `n` is the number of attributes (features).

#### Data Types

Notice that the features are of different types:
*   **Numerical (Continuous):** Can take any value within a range (e.g., `Height`, `Weight`).
*   **Numerical (Discrete):** Can only take integer values (e.g., `Age`).
*   **Categorical:** Represents distinct categories (e.g., `Gender`).
*   **Text:** Free-form text (e.g., `Expectation`).

Computers, and especially linear algebra, work with numbers. Therefore, a crucial step in any ML pipeline is to convert non-numeric data (like 'Gender' and 'Expectation') into a numerical format. This process is called **vectorization**. For example, 'Gender' could be mapped as `Male=0`, `Female=1`, `Other=2`. Text requires more complex techniques.

---

### 2. Matrix Decomposition: The "Why"

**Matrix Decomposition** (or factorization) is the process of breaking down a matrix into its constituent parts—a product of simpler, more fundamental matrices.

> **Analogy:** Think of prime factorization. The number `12` doesn't tell us much on its own. But its factorization, `2 × 2 × 3`, reveals its fundamental building blocks. Similarly, decomposing a matrix reveals its fundamental properties, such as its dominant directions, its rank, and how it transforms space.

**Why is this relevant?**
In data science, our data matrix often contains redundant information, noise, and complex relationships. Decomposition helps us:
*   **Simplify the data:** By identifying the most important patterns.
*   **Reduce noise:** By isolating and removing the less important components.
*   **Extract meaningful features:** By finding the "latent" or hidden structure in the data.
*   **Solve systems of equations more efficiently.**

We will focus on two key decomposition techniques: **Singular Value Decomposition (SVD)** and its application in **Principal Component Analysis (PCA)**.

---

### 3. Singular Value Decomposition (SVD)

SVD is arguably the most powerful and general matrix decomposition method. It states that *any* `m x n` matrix `A` can be factored into three other matrices:

$$ A = U \Sigma V^T $$



#### Visual Example: Image Compression

The most intuitive way to understand SVD is through image compression.
1.  A grayscale image is just a matrix of pixel intensities (e.g., a 512x512 matrix).
2.  We perform SVD on this image matrix `A` to get `U`, `Σ`, and `Vᵀ`.
3.  The matrix `Σ` contains the **singular values** ($\sigma_1, \sigma_2, ...$) along its diagonal, sorted in descending order of importance. The first few singular values capture the most significant, large-scale features of the image, while later ones represent finer details and noise.
4.  We can reconstruct an approximation of the image by using only the top `k` singular values (and the first `k` columns of `U` and `V`).

$$ A_k = U_k \Sigma_k V_k^T $$

As we increase `k`, the reconstructed image gets closer to the original, but we need to store more data. SVD allows us to find a sweet spot between image quality and storage size.


*With just a few singular values (k=20), we get a good approximation of the original image.*

#### The Mathematical Formulation and Terms

For an `m x n` matrix `A`:
*   **U:** An `m x m` **orthogonal matrix**. Its columns are the **left-singular vectors**. They form an orthonormal basis for the column space of A.
*   **Σ (Sigma):** An `m x n` **diagonal matrix**. The diagonal entries $\sigma_1, \sigma_2, ...$ are the **singular values** of A. They are always non-negative and are sorted in descending order ($\sigma_1 \ge \sigma_2 \ge ... \ge 0$).
*   **Vᵀ:** An `n x n` **orthogonal matrix** (transpose of V). The columns of V (rows of Vᵀ) are the **right-singular vectors**. They form an orthonormal basis for the row space of A.

#### Solved Example (Simple 2x2 Matrix)

Let's find the SVD for $ A = \begin{pmatrix} 3 & 0 \\ 4 & 5 \end{pmatrix} $.

**Step 1: Find V by working with $A^T A$.**
$ A^T A = \begin{pmatrix} 3 & 4 \\ 0 & 5 \end{pmatrix} \begin{pmatrix} 3 & 0 \\ 4 & 5 \end{pmatrix} = \begin{pmatrix} 25 & 20 \\ 20 & 25 \end{pmatrix} $
Now, find the eigenvalues ($\lambda$) and eigenvectors ($v$) of $A^T A$.
The characteristic equation is $(25-\lambda)^2 - 20^2 = 0 \implies (25-\lambda-20)(25-\lambda+20) = 0 \implies (5-\lambda)(45-\lambda) = 0$.
So, the eigenvalues are $\lambda_1 = 45, \lambda_2 = 5$.

The corresponding (normalized) eigenvectors are $ v_1 = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ 1 \end{pmatrix} $ and $ v_2 = \frac{1}{\sqrt{2}} \begin{pmatrix} -1 \\ 1 \end{pmatrix} $.
These form the columns of V: $ V = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 & -1 \\ 1 & 1 \end{pmatrix} $.

**Step 2: Find Σ.**
The singular values are the square roots of the eigenvalues:
$\sigma_1 = \sqrt{45} = 3\sqrt{5}$
$\sigma_2 = \sqrt{5}$
So, $ \Sigma = \begin{pmatrix} 3\sqrt{5} & 0 \\ 0 & \sqrt{5} \end{pmatrix} $.

**Step 3: Find U.**
The columns of U are given by $u_i = \frac{1}{\sigma_i} A v_i$.
$ u_1 = \frac{1}{3\sqrt{5}} \begin{pmatrix} 3 & 0 \\ 4 & 5 \end{pmatrix} \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ 1 \end{pmatrix} = \frac{1}{3\sqrt{10}} \begin{pmatrix} 3 \\ 9 \end{pmatrix} = \frac{1}{\sqrt{10}} \begin{pmatrix} 1 \\ 3 \end{pmatrix} $.
$ u_2 = \frac{1}{\sqrt{5}} \begin{pmatrix} 3 & 0 \\ 4 & 5 \end{pmatrix} \frac{1}{\sqrt{2}} \begin{pmatrix} -1 \\ 1 \end{pmatrix} = \frac{1}{\sqrt{10}} \begin{pmatrix} -3 \\ 1 \end{pmatrix} $.
So, $ U = \frac{1}{\sqrt{10}} \begin{pmatrix} 1 & -3 \\ 3 & 1 \end{pmatrix} $.

**Final Result:** $ A = U \Sigma V^T = \left(\frac{1}{\sqrt{10}} \begin{pmatrix} 1 & -3 \\ 3 & 1 \end{pmatrix}\right) \begin{pmatrix} 3\sqrt{5} & 0 \\ 0 & \sqrt{5} \end{pmatrix} \left(\frac{1}{\sqrt{2}} \begin{pmatrix} 1 & 1 \\ -1 & 1 \end{pmatrix}\right) $.

#### The Geometry of SVD

SVD tells us that any linear transformation `A` can be broken down into a sequence of three fundamental geometric operations:
1.  **A Rotation (Vᵀ):** It takes the standard input basis vectors and rotates them to align with the principal directions (eigenvectors of $A^TA$).
2.  **A Scaling (Σ):** It stretches or shrinks the space along these new rotated axes, with the scaling factors being the singular values.
3.  **Another Rotation (U):** It rotates the scaled result into the final output coordinate system.



---

### 4. Principal Component Analysis (PCA)

#### The Curse of Dimensionality

Imagine you have a dataset with 2 features. You can plot it on a 2D plane. If you have 3 features, you can visualize it in 3D space. What about 100 features? Or 10,000?

The **Curse of Dimensionality** refers to various problems that arise when working with high-dimensional data:
*   **Data becomes sparse:** The volume of the space increases exponentially with the number of dimensions. To maintain the same data density, you would need an exponentially larger number of samples.
*   **Computational cost:** More dimensions mean more calculations, making algorithms slower.
*   **Overfitting:** Models can easily find spurious patterns in high-dimensional noise, leading to poor generalization.

We need a way to reduce the number of dimensions while preserving as much of the useful information as possible. This is where PCA comes in.

#### PCA: The Solution

**Principal Component Analysis (PCA)** is a dimensionality reduction technique that transforms a dataset into a new coordinate system. The axes of this new system are the **Principal Components (PCs)**.

*   **Principal Component 1 (PC1):** The direction in the data with the **maximum variance**. It captures the most information.
*   **Principal Component 2 (PC2):** The direction with the second-most variance, which is also **orthogonal (perpendicular)** to PC1.
*   ...and so on. Each subsequent PC captures the maximum remaining variance while being orthogonal to all previous PCs.

These PCs are **latent vectors**—they are not any of the original features but are linear combinations of them. By keeping only the first few PCs, we can reduce the dimensionality of our data while retaining most of its original variance (information).



#### The PCA Algorithm (with a Simple Example)

Let's find the principal components for the following data matrix:
$ X = \begin{pmatrix} 1 & 1 \\ 2 & 3 \\ 3 & 2 \end{pmatrix} $

**Step 1: Standardize the Data**
First, find the mean of each column (feature):
Mean of X1 = (1+2+3)/3 = 2
Mean of X2 = (1+3+2)/3 = 2
Subtract the mean from each data point:
$$ X_{centered} = \begin{pmatrix} 1-2 & 1-2 \\ 2-2 & 3-2 \\ 3-2 & 2-2 \end{pmatrix} = \begin{pmatrix} -1 & -1 \\ 0 & 1 \\ 1 & 0 \end{pmatrix} $$
*(For simplicity, we'll skip division by standard deviation here, but it's crucial in real applications).*

**Step 2: Calculate the Covariance Matrix**
The covariance matrix `C` is given by $C = \frac{1}{N-1} X_{centered}^T X_{centered}$.
$ C = \frac{1}{2} \begin{pmatrix} -1 & 0 & 1 \\ -1 & 1 & 0 \end{pmatrix} \begin{pmatrix} -1 & -1 \\ 0 & 1 \\ 1 & 0 \end{pmatrix} = \frac{1}{2} \begin{pmatrix} 2 & 1 \\ 1 & 2 \end{pmatrix} = \begin{pmatrix} 1 & 0.5 \\ 0.5 & 1 \end{pmatrix} $

**Step 3: Find Eigenvalues and Eigenvectors of the Covariance Matrix**
We solve the characteristic equation for `C`: $(1-\lambda)^2 - 0.5^2 = 0$.
This gives eigenvalues $\lambda_1 = 1.5$ and $\lambda_2 = 0.5$.

The corresponding (normalized) eigenvectors are:
*   For $\lambda_1 = 1.5$: $ v_1 = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 \\ 1 \end{pmatrix} $ (This is **PC1**)
*   For $\lambda_2 = 0.5$: $ v_2 = \frac{1}{\sqrt{2}} \begin{pmatrix} -1 \\ 1 \end{pmatrix} $ (This is **PC2**)

**Step 4: Interpret the Results**
The principal components are the eigenvectors of the covariance matrix.
*   **PC1** points in the direction `(1, 1)`, and it explains a proportion of the variance equal to $\frac{\lambda_1}{\lambda_1+\lambda_2} = \frac{1.5}{2.0} = 75\%$.
*   **PC2** points in the direction `(-1, 1)`, and it explains the remaining $25\%$ of the variance.

To reduce our 2D data to 1D, we would project the centered data onto PC1, as it captures the most information.

---

> **Note:** From this module, theory questions like the SVD and PCA algorithm and problems to find the U, Σ, and Vᵀ matrices (from SVD) and to find the principal components of matrices (from PCA) will be used for both internal and end semester assessments.
