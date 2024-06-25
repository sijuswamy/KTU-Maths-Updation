
----
# Module-1: Fundamentals of Linear Algebra 
>Systems of linear equations, Solution by Gauss elimination, Row echelon form and rank of a matrix, Vector Space ($\mathbb{R}^n$ , $\mathbb{A}_{m \times n}$
), Subspace, Linear Independence, Span, Basis and Dimension, Coordinates and change of basis, Fundamental theorem for linear systems.
**Expected Cognitive Domain Level**- Understanding

**Knowledge Category:** Procedure and Modelling

**Expected Affective Domain Level:**- Appreciate the Mathematical Background of Linear systems

## Directions for Course Delivery

Introduce the concept of matrix and its applications through an excel sheet structure. It is better to create a Google form and give the students to fill out the forms with the basic details like- Name, Age, Gender, marks in Physics, Chemistry & Mathematics and expectation about the course. Introduce the concept of dataset, features (columns), samples / vectors as (rows). Various data types like name as string, age as numerical variable, gender as categorical variable etc., Presense of non numerical columns demands transformations from character/ string to numerical values. In essence the students should get the concept that matrix is both a data representation and analytics tool.

- Introduce the system of linear equations using a simple linear equation in two space- eg., $$2x+y=11; 2x-y=10.$$
Solve these equations in both algebraic and geometric methods (use Desmos or Cocalc). Explore the fact that the *determinant* of the coefficents of the system determine whether the lines are parallel or not.
- Representation of the linear system as linear combination of column vectors with unknowns as coefficients- for example the above system can be represented as

 $$
x\begin{pmatrix}
2\\
2
\end{pmatrix}+y
\begin{pmatrix}
1\\
-1
\end{pmatrix}=
\begin{pmatrix}
11\\
10\end{pmatrix}
$$

- Introduce the precedure for solving a system of linear equations using Gauss elimination method.
- Present the linear system $$2x+y=11; 4x+2y=10.$$ and try to solve it using Gauss elimination method. Demonstrate the fact that the solution leads to a mathematical falaci. This will leads to frame a systematic method to check consistency of the system. Now introduce the concept of rank as number of linearly independent rows.
- Present the row reduced echelon form form to find rank of a matrix.
- Introduce the concept of vector space/ linear space- using the $\mathbb{R}^2$ as an example. (include 3b1b video link)
- Explain the connection between geometry and algebra by representing  $a\hat{i}+b\hat{j}+c\hat{k}$  as a vector in three space- $\begin{pmatrix} a\\\ b \\\ c
\end{pmatrix}$
- Extend the vector space example to $\mathbb{R}^n$ and $\mathbb{C}^n$ over the field $\mathbb{R}$.
- Introduce the collection of all square matrices with real values as avector space with operations matrix addition and scalar multiplication over the field $\mathbb{R}$.
- Give the collection of all polynomials of degree upto $n$ with real coefficients *addition* and $scalar multiplication*.
- Introduce Spaning set, maximally independent spanning set (basis) and dimension of the vector space.
- Introduce the concept of sub space of a vector space as subset which is closed under the operation *linear combination*.
- Four fundamental subspaces of a vector space- Range space, Null space  and its dimensions.
- Fundamental theorem of linear algebra (Rank nullity theorem): For a matrix $\mathbf{A}$ of dimension $m\times n$, $$\rho(A)+\text{nullity}(A)=n$$
----
# Module 2: Spectral Decomposition
>Eigen values and eigen vectors, Diagonalization of matrices. 

- Introduce the eigen vectors as invarient vectors under a linear transformation and corresponding eigen value as the scaling measure.
- Mathematical model for eigen vectors as  $\mathbf{X}$ satisfy $\mathbf{AX}=\lambda \mathbf{X}$. (Refer 3b1b video lessons for demonstration)
- Explain the mathematical procedure to find eigen values and eigen vectors of a matrix of order upto 3:
- Eigen values are the solutions of the homogeneous system- $det\left(\mathbf{A}-\lambda \mathbf{I}\right)=0$.
- Properties of eigen values
- Eigen vectors as the solution of the system $\left(\mathbf{A}-\lambda \mathbf{I}\right)\mathbf{X}=0$ corresponding to each $\lambda$.
- algebraic and geometric multiplicity of eigen values and its interpretation.
- Diagonal form of a matrix using spectral decomposition.
>**Note:** For the formative assessment, give problems to find eigen values, eigen vectors, AM & GM and diagonal form of simple real matrices of order upto 3.
----
# Module- 3: Inner product space and its derivables-Introducing the concept of distance into vector space

>Length and dot product in R^n – Norm, Length, distance,dot product, Angle , Inner product space, Orthogonal projection, Orthogonal and orthonormal sets , The least
squares problem, Orthogonal Subspaces.

- Define the operator inner product as extension of dot product and define distance in terms of inner product.
- Definition of norm and normed space.
- Examples of normed space- $\mathbb{R}^n$ with Euclidian distance as norm.
- Introduce Orthogonol projection with a simple example of free fall body.
- Introduce the concept of orthogonal and orthonormal sets using eigen vectors of real symmetric matrices. ( select example from a RGB image)
- Introduce the concept of least square error and finding closed form solution of simple systems using the formula $\mathbf{X}=\left(A^T A\right)^{-1}A^Tb$ by extending simple vector solutions.
- Introduce the concept of orthogonal subspaces and its use in solution of system of equations. Mention examples like Fourier matrix and its simple uses.

# Module -4: Linear Transformations and its applications
>Linear Transformations, Kernal of Linear Transformations and its applications.

- Introduce the concept of linear transformation using the matrix multiplication of a vector with $2\times 2$ unit matrix, then change the diogonal values and demonstrate the impact of these operations using colcalc/ python (code will be provide)
- Linear transformation, matrix of transformation and its on-to one correspondance
- Range and Kernal of a linear transformation.
- Rank-nullity theorem (simple cases) for linear transformation.
- Composition of linear transformation and its matrix representation.
- Geometry of linear transformation in 2 space
- Demonstration of matrix kernal operation in Digital image processiong and convolution (not for examination)
>**Note:** From this module include problems to verify given transformation $LT$ is linear, range space, kernal and its dimesions for internal and End semester evaluations. 
