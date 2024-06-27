# $\color{blue}{\text{Mathematics for Computing and Information Sciences-I}}$

**Expected Cognitive Domain Level**- Understanding and Application

**Knowledge Category:** Procedure and Modelling

**Expected Affective Domain Level:**- Appreciate the analytical power of Calculus tools 

----
# Module-1 Foundations of Calculus
- **Reference text:** [Thomas calculus] Section 2.2 (page 66-93)
- Hour 1- Re-visiting the concept of limit studied in Higher secondary classes 
  - Main points to be highlighted along with the formal definition
    1. The limit is a value one *expect* that function would have at the point $x=a$, based on the values of that function at *close vicinity* of $x=a$, but regardless of the value of $f(x)$ at $x=a$, if $f(a)$ is defined at all.
    Use the link <https://en.wikipedia.org/wiki/Limit_of_a_function#/media/File:Epsilon-delta_limit.svg> for   geometrical explanation for a better understanding.
    2. For the existence of limit at $x=a$, $f(a^+)=f(a^-)$. Use this property geometrically to check existence of limit at $x=0$ of the unit step function and similar examples from the text book.

 An interesting video session is available at:<https://youtu.be/riXcZT2ICjA?si=4ZnbpClt7DjPV0pL>
 
- Practice more problems from the prescribed textbook to reinforce concept of limit using limit laws and L-Hopital rule.
- Intuitively introduce the concept of continuity geometrically as *breakless graph* ie. the expected value of $f(x)$ in the close vicinity is same as $f(a)$
- Formally define continuity and practice more problems from the prescribed textbook
- Introduce the concept of rate of change with *physical examples* like velocity, acceleration etc.
- Visualize the rate of change - first order (velocity), curvature, second order( acceleration) etc., Use Geogebra/ Cocalc or good video sessions.
- Re-visit the definition of derivative as a limit.
- Demonstrate derivative as slope- Use the parabola $f(x)=x^2$ about points $0$ and $3$.
- Practice more problems related to derivative of various types of functions, implicit differentiation, tangent, tangent line and normal to a given curve.
- Summarize the concept that the tangent traces the shape of the curve and normal captures the vision.
- Demonstrate the the linear approximation (linearization) through demonstration of $f(x)=x^3+2x+5$ about $x=5$. Compare linear approximations using univariate Taylor series of $f(x)=e^x,f(x)=\sin x $.
- Demonstrate the concave, convex and neither concave nor convex functions in two dimensions.

# Module-2 Foundations of Multi variable calculus

- Introduce the Graphs, level curves and contour of functions through examples like $f(x)=x^2+y^2,f(x)=x^2-5y^2, f(x,y)=\dfrac{xy}{x^2+y^2}$ using Geogebra or Cocalc.
- Limit of multivariable functions as extension of single variable limit- Better to demonstrate the multivariate limits of functions like- $f(x,y)=x^2+y^2$.
- Continuity of functions can be demonstrated using simple bi-variate function. Discontinuity points will be termed as holes in plane.
- Demonstrate the partial derivative as rate of change of one variable keeping other variable as constant. Better to introduce the possibility of vector representation of partial derivative.
- Higher order partial derivatives and its uses in Computational Modelling.

# Module-3 Calculus for analysis and un-constrained optimization

- Representation of composition of functions- using simple functions like $f(x)=x^2, g(x)=\sin(x), f\circ g=\sin(x^2)$. Demonstrate the impact of change in input variable $x$ on $f(x),g(x)$ and $f\circ g$- Represent this change in composition function using chain rule.
- Extend the concept of chain rule to multivariable functions.
- Gradient as the vector form of derivative of multi-variable functions.
- Demonstrate that the gradient at point is normal to the tangent plane.
- Directional derivative as impact of change in one vector on another function with reference to an offset.
- Introduce the concept of un-constrained optimization in calculus approach- extension of second derivative test to muti-variable calculus.
- Introduce the relative maxima and relative minima as local maxima and maxima with proper examples like hills and valleys in Google earth ore other simple examples.
- Demonstrate the local extrema and global extrema using suitable functions.
- Practice more problems in local maxima and minima.

# Module-4 Calculus for Constrained Optimization

- Introduce the concept of constrained optimization as the diffusion of constraint to the objective function using elimination of variable technique. e.g. $f(x)=x^2+y^2$ subject to the constrains $g(x,y)=x+y-1$.
- Introduce the concept of Lagrange multiplier as combining constraints with objective function.
- Explain equivalence of solution obtained through both the methods.
- introduce the concept of iterative minimization through Steepest descend and demonstrate the steepest descend approach in the solution of $f(x)=x^2$ at $x=0$.
- Introduce the mathematical modelling of LPP using real world problem
- Give more importance to the solution space, feasible solution and the simplex procedure to find optimal solution of the objective function.

>**Assessments:**
 1. Assignment- Give application level questions with some `Python` based visualization or computation (preferable). In that case we can map the COs to PO5- use of modern tools.
 2. Internal tests- For internal tests 80% of questions will be direct and will be at most K3 (from the prescribed textbooks). 15% questions will be of application type but similar to the problems discussed in the class/ assignments and 5% of questions will be challenging (questions from the reference textbooks).
 3. ESE- For the ESE, follow the same pattern of internal tests. 
