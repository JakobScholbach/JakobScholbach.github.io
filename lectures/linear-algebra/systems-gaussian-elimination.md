---
title: Systems: Gaussian Elimination
---

# Gaussian elimination

<a href="../systems-elementary-operations/#thm-elementary-equivalent" data-reference-type="ref+Label" data-reference="thm:elementary-equivalent">Theorem 2.18</a> is a useful insight, but it lacks an important feature: it does not directly instruct us how to simplify any given linear system. (In <a href="../systems-elementary-operations/#ex-example-elementary-operations" data-reference-type="ref+Label" data-reference="ex:example-elementary-operations">Example 2.19</a>, we did end up with a particularly simple linear system, but we did not have any a priori guarantee for this to happen. If we had chosen some “stupid” elementary operations instead, we would not have simplified the system.) *Gaussian elimination* is an algorithmic process that does just that: it is a simple procedure that is guaranteed to yield the simplest possible equivalent form of any given linear system.

In view of the correspondence between linear systems and matrices, we will first phrase this process in terms of matrices, and then translate it back to the problem of solving linear systems.

Among the myriad of all possible matrices, the following matrices are the “nice guys”.

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 2.27</strong></p>

<span id="def-row-echelon-form" label="def:row-echelon-form"></span> A matrix is in *row-echelon form* (or is called a *row-echelon matrix*) if the following conditions are satisfied:

1.  If there are any zero rows (i.e., consisting only of zeros), then these are at the bottom of the matrix.

2.  In a non-zero row, the first non-zero (starting from the left) is a 1. (It is called the *leading 1*.)

3.  Each leading 1 is to the right of all the leading 1’s in the rows above it.

If, *in addition* to the above conditions, each leading 1 is the *only* non-zero entry in its column, then the matrix is in *reduced row-echelon form*.

Maybe saying more than a thousand words is this picture of a row-echelon form. Here, the asterisks indicate an arbitrary number. If, in addition, all the underlined asterisks are zero, then the matrix is a reduced row-echelon matrix.

<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccccccc} 0 & 1 & * & \underline * & \underline * & * & \underline * \\ 0 & 0 & 0 & 1 & \underline * & * & \underline * \\ 0 & 0 & 0 & 0 & 1 & * & \underline * \\ 0 & 0 & 0 & 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 & 0 & 0 \\ \end{array} \right ).
\]
</div>

</div>

In view of the correspondence between linear systems and matrices, we transport the language of elementary operations (<a href="../systems-elementary-operations/#def-elementary-operations-system" data-reference-type="ref+Label" data-reference="def:elementary-operations-system">Definition 2.17</a>) to matrices as follows.

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 2.28</strong> (Related exercises: <a href="../maps/#ex-maps-exercise-004">Exercise 4.4</a>, <a href="../maps/#ex-maps-exercise-007">Exercise 4.7</a>, <a href="#ex-maps-exercise-008">Exercise 2.25</a>, <a href="../maps/#ex-maps-partial-2026-2">Exercise 4.47</a>)</p>

<span id="def-elementary-row-operations" label="def:elementary-row-operations"></span> The following operations on a given matrix $A$ are called *elementary row operations*:

1.  interchange any two rows,

2.  multiply any row by a *non-zero* (!) number,

3.  add a multiple of any row to a *different* (!) row.

</div>

<div class="method" markdown="1">


<p class="env-number"><strong>Method 2.29</strong> (Related exercises: <a href="../maps/#ex-maps-exercise-004">Exercise 4.4</a>, <a href="../maps/#ex-maps-partial-2026-2">Exercise 4.47</a>, <a href="#ex-systems-1-b">Exercise 2.12</a>)</p>

<span id="met-gaussian-algorithm" label="met:gaussian-algorithm"></span> (*Gaussian algorithm* or *Gaussian eliminiation*) Every matrix can be brought to reduced row-echelon form by a sequence of elementary row operations. This can be achieved using the following algorithmic process:

1.  If the matrix consists only of zeros, stop: then the matrix is in reduced row-echelon form.

2.  Otherwise, find the first column from the left having a non-zero entry. Call this entry $a$. Interchange this row (elementary operation <a href="../systems-elementary-operations/#item-change" data-reference-type="ref" data-reference="item--change">1.</a>) so that it is in the top position.

3.  Multiply the new top row by $\frac 1 a$ (elementary operation <a href="../systems-elementary-operations/#item-multiply" data-reference-type="ref" data-reference="item--multiply">2.</a>; note this is possible since $a \ne 0$, see also <a href="../systems-linear-equations/#rem-field" data-reference-type="ref+Label" data-reference="rem:field">Remark 2.5</a>). Thus the first row has a leading 1.

4.  By adding appropriate multiples of the first row to the remaining rows (elementary operation <a href="../systems-elementary-operations/#item-add" data-reference-type="ref" data-reference="item--add">3.</a>), ensure that the entry between the leading 1 are all zero.

From this point on, the first row is not touched anymore, and the four steps above are applied to the matrix consisting of the remaining rows.

This produces a (possibly not reduced) row-echelon form. It can be finally brought into reduced row-echelon form by adding appropriate multiples of rows with leading 1’s to the rows above them (elementary operation <a href="../systems-elementary-operations/#item-add" data-reference-type="ref" data-reference="item--add">3.</a>), beginning at the bottom.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 2.30</strong></p>

<span id="ex-43-matrix" label="ex:43-matrix"></span> We apply the Gaussian algorithm to the matrix
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc} 1 & 2 & 5 & 7 \\ 2 & 1 & 4 & 2 \\ 5 & 4 & 13 & 11 \end{array} \right ).
\]
</div>

The first three steps don’t change the matrix (since the top-left entry is already 1). Step (4): add $-2$ times the first row to the second row; and add $-5$ times the first row to the third, which gives
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc} 1 & 2 & 5 & 7 \\ 0 & \underline{-3} & -6 & -12 \\ 0 & -6 & -12 & -24 \end{array} \right )
\]
</div>
The remaining steps only affect the second and third row. Step (2) picks the second row, and $a = -3$ (underlined). It is already in the top position (the first row being discarded for the remainder of the algorithm), so Step (2) does not change the matrix. Step (3) gives the matrix
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc} 1 & 2 & 5 & 7 \\ 0 & 1 & 2 & 4 \\ 0 & -6 & -12 & -24 \end{array} \right )
\]
</div>
Step (4) adds $-6$ times the second row to the third, which gives
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc} 1 & 2 & 5 & 7 \\ 0 & 1 & 2 & 4 \\ 0 & 0 & 0 & 0 \end{array} \right ).
\]
</div>
At this point also the second row is discarded, which leaves only the last row, which consists of zeros. By Step (1), the algorithm stops at this point.

This matrix is in row-echelon form, but not yet reduced. To reduce it, add $-2$ times the second row to the first, which gives
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc} 1 & 0 & 1 & -1 \\ 0 & 1 & 2 & 4 \\ 0 & 0 & 0 & 0 \end{array} \right )
\]
</div>

</div>

When applied to matrices associated to linear systems, Gaussian eliminiation becomes very useful for solving linear systems:

<div class="method" markdown="1">


<p class="env-number"><strong>Method 2.31</strong> (Related exercises: <a href="../euclid/#ex-euclid-6-2">Exercise 7.4</a>, <a href="../euclid/#ex-euclid-6-22">Exercise 7.26</a>, <a href="../maps/#ex-maps-3-2">Exercise 4.9</a>, <a href="../maps/#ex-maps-3-6">Exercise 4.16</a>, <a href="../maps/#ex-maps-exercise-003">Exercise 4.3</a>, <a href="../maps/#ex-maps-exercise-004">Exercise 4.4</a>, <a href="#ex-maps-exercise-008">Exercise 2.25</a>, <a href="../maps/#ex-maps-exercise-010">Exercise 4.9</a>, <a href="../maps/#ex-maps-partial-2026-1">Exercise 4.46</a>, <a href="../maps/#ex-maps-partial-2026-2">Exercise 4.47</a>, <a href="#ex-systems-1-b">Exercise 2.12</a>)</p>

<span id="met-gaussian-elimination-solve" label="met:gaussian-elimination-solve"></span>

1.  Form the augmented matrix corresponding to the given linear system.

2.  Perform Gaussian elimination to that matrix (<a href="#met-gaussian-algorithm" data-reference-type="ref+Label" data-reference="met:gaussian-algorithm">Method 2.29</a>), giving a reduced row-echelon matrix.

3.  If a row of the form
<div class="arithmatex" markdown="1">
\[
    0 \ 0 \ \dots \ 0 \ 1
\]
</div>
    occurs, the system has *no* solutions.

4.  Otherwise, we call the variables corresponding to the columns *not* containing a leading 1 *free variables*. The values of these variables can be chosen to be *arbitrary* real numbers. The variables that correspond to columns that do contain a leading 1 are uniquely specified by these free variables. Their values can be determined by solving the equations corresponding to the row-echelon matrix for the leading variables.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 2.32</strong></p>

<span id="ex-systems-example-010" label="ex:systems-example-010"></span> Consider the system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x + 2y + 5 z & =  7 \\
2x + y + 4 z & = 2 \\
5 x + 4 y + 13 z & = 11.
\end{align*}
\]
</div>
The augmented matrix associated to this is the one in <a href="#ex-43-matrix" data-reference-type="ref+Label" data-reference="ex:43-matrix">Example 2.30</a>. Gaussian algorithm brings it into the reduced row-echelon form
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc} 1 & 0 & 1 & -1 \\ 0 & 1 & 2 & 4 \\ 0 & 0 & 0 & 0 \end{array} \right ).
\]
</div>
This matrix corresponds to the linear system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x + z & =  -1 \\
y + 2z & = 4 \\
0 & = 0.
\end{align*}
\]
</div>
According to <a href="../systems-elementary-operations/#thm-elementary-equivalent" data-reference-type="ref+Label" data-reference="thm:elementary-equivalent">Theorem 2.18</a>, this linear system has the same solution set as the original one.

The leading variables are $x$ and $y$, so that $z$ is a free variable. Solving the second equation for $y$ then gives
<div class="arithmatex" markdown="1">
\[
y = 4-2z,
\]
</div>
and similarly
<div class="arithmatex" markdown="1">
\[
x = -1-z.
\]
</div>
We obtain that the solution set to the original linear system consists of triples of the form
<div class="arithmatex" markdown="1">
\[
(x = -1-z, y = 4-2z, z),
\]
</div>
in which $z$ is an arbitrary number (and $x$ and $y$ are determined by $z$ as indicated).

</div>

# Exercises

<div class="exercise" markdown="1">

Describe all the solutions of the equation
<div class="arithmatex" markdown="1">
\[
x + y = 3.
\]
</div>
Draw a picture of that solution set. Is it a homogeneous equation?

</div>

<div class="exercise" markdown="1">

Consider the equation
<div class="arithmatex" markdown="1">
\[
x = 3.
\]
</div>
What is its solution set?

Consider the same equation, but now with two variables $x$ and $y$ being present (so we could rewrite the equation as $x + 0 \cdot y = 3$ in order to emphasize the presence of $y$). What is the solution set this time?

</div>

<div class="exercise" markdown="1">

Consider the system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
2x_1 - x_2 + x_3 + x_4 & = 1 \\
5x_2 - 3 x_3 - 5 x_4 & = -3 \\
3x_1 - 4 x_2 +3x_3 + 4x_4 &=  3.
\end{align*}
\]
</div>
What is the matrix associated to that system? Using <a href="#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>, find all solutions of that system.

</div>

<div class="exercise" markdown="1">

Consider the (augmented) matrix
<div class="arithmatex" markdown="1">
\[
A := \left ( \begin{array}{cccccc|c} 1 & 0 & 3 & 0 & 0 & 0 & 1 \\ 0 & 1 & 2 & 4 & 1 & 0 & 0 \\ 0 & 0 & 0 & 2 & 1 & 0 & 2 \\ 0 & 0 & 0 & 0 & 0 & 1 & 3 \\ 0 & 0 & 0 & 0 & 0 & 0 & 0 \end{array} \right ).
\]
</div>
What type of matrix is that? (I.e., what $m \times n$-matrix.) If $A = (a_{ij})$, what is $a_{13}$ and $a_{31}$? What is the linear system associated to that matrix? (Hint: one equation reads “$\dots = 3$”. For consistency, call the variables $x_1, x_2, \dots, x_6$.)

Is the matrix in row-echelon form? Is it in reduced row-echelon form? If not, use the Gaussian algorithm (<a href="#met-gaussian-algorithm" data-reference-type="ref+Label" data-reference="met:gaussian-algorithm">Method 2.29</a>) in order to transform it into reduced row-echelon form. Name the columns which contain a leading 1 (Hint: there are 4 of them). Which variables are free, which variables are not free? Use <a href="#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a> and solve the linear system associated to that augmented matrix.

</div>

<div class="exercise" markdown="1">

Using <a href="#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>, find all solutions of the following systems
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x + y - z & = 1 \\
3x-y+2z & = 5 \\
4x + z & = 6.
\end{align*}
\]
</div>
and
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x+y-z & = 1 \\
3x-y+2z & = 0 \\
x + y - 2 z & = 2.
\end{align*}
\]
</div>

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 2.6</strong></p>

<span id="ex-equation-no-solutions" label="ex:equation-no-solutions"></span> (See <a href="#sol-ex-equation-no-solutions" data-reference-type="ref+Label" data-reference="sol--ex:equation-no-solutions">Solution 2.7.1</a>.) Let
<div class="arithmatex" markdown="1">
\[
ax+by=c
\]
</div>
be a linear equation. For which values of $a$, $b$ and $c$ does this equation have no solution? For which values of $a$, $b$ and $c$ does it have infinitely many solutions?

</div>

<div class="exercise" markdown="1">

Compute the reduced row-echelon form of the matrices associated to the linear systems in <a href="../systems-linear-systems/#ex-system-2-unique" data-reference-type="ref+Label" data-reference="ex:system-2-unique">Example 2.8</a>, <a href="../systems-linear-systems/#ex-system-2-no" data-reference-type="ref+Label" data-reference="ex:system-2-no">Example 2.10</a> and <a href="../systems-linear-systems/#ex-system-2-infinite" data-reference-type="ref+Label" data-reference="ex:system-2-infinite">Example 2.11</a>.

</div>

<div class="exercise" markdown="1">

Consider the system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x + y & = 1 \\
x - y & = b,
\end{align*}
\]
</div>
where $b$ is a real number. What is its solution set? Illustrate the system geometrically for $b = 0$ and for $b=1$.

</div>

<div class="exercise" markdown="1">

Consider the system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
ax + by & = 1 \\
x - y & = 2.
\end{align*}
\]
</div>
Here $x$ and $y$ are the variables and $a$ and $b$ are the coefficients.

1.  For which values of $a$ and $b$ does the system above have no solution?

2.  For which values does it have exactly one solution?

3.  For which values does it have infinitely many solutions?

Explain your findings algebraically and geometrically.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 2.10</strong></p>

<span id="ex-systems-1-a" label="ex:systems-1-a"></span> (See <a href="#sol-ex-systems-1-a" data-reference-type="ref+Label" data-reference="sol--ex:systems-1-a">Solution 2.7.2</a>.) Find the solutions of the system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x_1 + 2x_2 - x_3 & = 0 \\
-2x_1 - 3 x_2 + x_3 & = 1 \\
x_2 - x_3 & = 1.
\end{align*}
\]
</div>

</div>

<div class="exercise" markdown="1">

The linear system in the variables $x_1, x_2, x_3, x_4$ associated to the matrix
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} 2 & -1 & 1 & -1 & 1 \\ 0 & 1 & -3 & 1 & 3 \\ 2 & 1 & -4 & 1 & 6 \\ 2 & 0 & -2 & 1 & 2 \\ \end{array} \right )
\]
</div>
has only one solution. Find it!

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 2.12</strong></p>

<span id="ex-systems-1-b" label="ex:systems-1-b"></span> (See <a href="#sol-ex-systems-1-b" data-reference-type="ref+Label" data-reference="sol--ex:systems-1-b">Solution 2.7.3</a>.) Find the solutions of the following linear system in the variables $x_1, \dots, x_4$:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x_1 - x_2 + x_3 & = -2 \\
x_3 - x_4 & = 1 \\
x_1 - x_2 + x_4 & = -3 \\
x_1 - x_2 + 3 x_3 - 2 x_4 & = 0.
\end{align*}
\]
</div>

</div>

<div class="exercise" markdown="1">

Solve the following linear system, where $h$ is a parameter, and $x, y$ are the unknowns:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x + h y & = 4 \\
3x+6y & = 8.
\end{align*}
\]
</div>
For selected values of $h$, illustrate the solution set graphically.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 2.14</strong></p>

<span id="ex-systems-1-c" label="ex:systems-1-c"></span> (See <a href="#sol-ex-systems-1-c" data-reference-type="ref+Label" data-reference="sol--ex:systems-1-c">Solution 2.7.4</a>.) Solve the following linear system, where $h$ is a parameter and $x,y,z$ are the unknowns:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
(4-h) x - 2 y - z & = 1\\
-2x + (1-h) y+2z & = 2 \\
-x + 2 y + (4-h) z & = 1.
\end{align*}
\]
</div>

</div>

<div class="exercise" markdown="1">

For any $t \in {\bf R}$ consider the homogeneous linear system associated to the matrix
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} 2 & 0 & 1 & -t & 0 \\ 1 & -2 & 0 & 3 & 0 \\ 4 & -4 & t & 5 & 0 \end{array} \right ).
\]
</div>

1.  Solve the system for $t = 0$.

2.  Solve the system for all $t \in {\bf R}$.

</div>

<div class="exercise" markdown="1">

Solve the system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x_1 - x_3 + 2 x_4 & = 0 \\
x_2 + 2 x_3 - 2 x_4 & = 0 \\
x_1 + x_2 + x_3 &= 0.
\end{align*}
\]
</div>

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 2.17</strong></p>

<span id="ex-systems-1-d" label="ex:systems-1-d"></span> (See <a href="#sol-ex-systems-1-d" data-reference-type="ref+Label" data-reference="sol--ex:systems-1-d">Solution 2.7.5</a>.) Consider the linear system (in the unknowns $x_1, x_2, x_3$):
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x_1 + x_2 + x_3 & = 1 \\
x_1 - x_3 & = 0.
\end{align*}
\]
</div>
Is there any $t \in {\bf R}$ such that $(1-t,2+3t,4t)$ is a solution of that system?

</div>

<div class="exercise" markdown="1">

Consider the following linear system (in the unknowns $x_1, x_2, x_3$):
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x_1 - x_2 + 3 x_3 & = 0 \\
x_1 - x_2 & = 1.
\end{align*}
\]
</div>
Show that there is exactly one $t \in {\bf R}$ such that the vector $(3+t, 2+t, \frac 23 + t)$ is a solution of that system.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 2.19</strong></p>

<span id="ex-systems-1-e" label="ex:systems-1-e"></span> (See <a href="#sol-ex-systems-1-e" data-reference-type="ref+Label" data-reference="sol--ex:systems-1-e">Solution 2.7.6</a>.) Do there exist $q, t \in {\bf R}$ such that the vector
<div class="arithmatex" markdown="1">
\[
(x_1, x_2, x_3) = (1+t, t+q, -t+2q+1)
\]
</div>
satisfies
<div class="arithmatex" markdown="1">
\[
3x_1 + 2x_2 -x_3 = 5?
\]
</div>

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 2.20</strong></p>

<span id="ex-systems-1-f" label="ex:systems-1-f"></span> (See <a href="#sol-ex-systems-1-f" data-reference-type="ref+Label" data-reference="sol--ex:systems-1-f">Solution 2.7.7</a>.) Find a polynomial
<div class="arithmatex" markdown="1">
\[
p(x) = a_0 + a_1x+a_2 x^2 + a_3 x^3
\]
</div>
such that $p(1) = 0$ and $p(2) = 3$. Is there a unique such polynomial?

</div>

<div class="exercise" markdown="1">

Find the solution of the linear system associated to the following augmented matrix:
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} 1 & 1 & 2 & 3 & 1 \\ 2 & 0 & 1 & 2 & 1 \\ 1 & 3 & 5 & 7 & 2 \end{array} \right ).
\]
</div>

</div>

<div class="exercise" markdown="1">

For any $\alpha \in {\bf R}$ find the solutions of the system associated to the matrix
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} 1 & 1 & 2 & 3 & -1 \\ 2 & 0 & 1 & 2 & \alpha \\ 1 & 3 & 5 & 7 & 0 \end{array} \right ).
\]
</div>

</div>

<div class="exercise" markdown="1">

Consider the following linear system in the unknowns $x, y, z$, which depends on the parameter $\alpha \in {\bf R}$:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
2x-y+z & = 1 \\
(\alpha+2) x - 2y+\alpha z & = -\alpha.
\end{align*}
\]
</div>
Determine the solution set of this system for each value of $\alpha$.

</div>

<div class="exercise" markdown="1">

The following extended exercise showcases the usage of linear algebra in network analysis. An idealized city consists of the following streets $U$ to $Z$, with four intersection points $A$ to $D$. The streets are all one-way streets:

<div class="center" markdown="1">

![image](figures/png/systems/systems-fig-05.png)

</div>

At the point labelled $A$, 500 cars per hour drive into the city, and at $B$, 400 cars exit the city, while at $C$ 100 cars exit the city per hour.

Describe the possible scenarios regarding the numbers of cars driving through the streets $U$, $V$, $W$, $X$, $Y$ and $Z$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 2.25</strong></p>

<span id="ex-maps-exercise-008" label="ex:maps-exercise-008"></span> (See <a href="#sol-ex-maps-exercise-008" data-reference-type="ref+Label" data-reference="sol--ex:maps-exercise-008">Solution 2.7.8</a>.) For any $\lambda \in {\bf R}$ solve the system (in the unknowns $x_1, x_2, x_3$)
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\lambda x_1 & = 0 \\
\lambda x_2 + (1+\lambda) x_3 & = 1 \\
\lambda x_1 + x_2 + 2x_3 & = 3.
\end{align*}
\]
</div>

</div>

# Solutions to the exercises

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.7.1</strong></p>

<span id="sol-ex-equation-no-solutions" label="sol--ex:equation-no-solutions"></span> (See <a href="#ex-equation-no-solutions" data-reference-type="ref+Label" data-reference="ex:equation-no-solutions">Exercise 2.6</a>.) If $a \ne 0$ *or* $b \ne 0$, then the equation $ax+by = c$ has infinitely many solutions. Indeed, if, say $a \ne 0$, we can subtract $by$ and divide by $a$, which gives $x = \frac{c-by}a$. Thus, for any $y \in {\bf R}$, the pair $(x=\frac{c-by}a, y)$ is a solution. A similar analysis works if $b \ne 0$. It remains to consider the case in which $a=0$ and $b=0$. In this case the solution set of the equation depends on $c$:

- If $c = 0$, then *any* pair $(x,y)$ is a solution. Indeed: $0 x + 0y= 0$ holds true then. Thus, if $a=b=c=0$, there are infinitely many solutions.

- If $c \ne 0$, the equation $0x+0y = c$ has no solution, since the left hand side is always 0, while the right hand side is nonzero. So, in the case $a=b=0$ but $c \ne 0$, there is *no* solution.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.7.2</strong></p>

<span id="sol-ex-systems-1-a" label="sol--ex:systems-1-a"></span> (See <a href="#ex-systems-1-a" data-reference-type="ref+Label" data-reference="ex:systems-1-a">Exercise 2.10</a>.) The matrix associated to the system is as follows, and we bring it to reduced row echelon form:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left ( \begin{array}{ccc|c} 1 & 2 & -1 & 0 \\ -2 & -3 & 1 & 1 \\ 0 & 1 & -1 & 1 \end{array} \right ) \leadsto & 
\left ( \begin{array}{ccc|c} 1 & 2 & -1 & 0 \\ 0 & 1 & -1 & 1 \\ 0 & 1 & -1 & 1 \end{array} \right ) \\
\leadsto & 
\left ( \begin{array}{ccc|c} 1 & 2 & -1 & 0 \\ 0 & 1 & -1 & 1 \\ 0 & 0 & 0 & 0 \end{array} \right ) 
\leadsto 
\left ( \begin{array}{ccc|c} \underline 1 & 0 & +1 & -2 \\ 0 & \underline 1 & -1 & 1 \\ 0 & 0 & 0 & 0 \end{array} \right )
\end{align*}
\]
</div>
We have two leading ones (underlined), so the third unknown $x_3$ is a free variable and $x_1$ and $x_2$ are non-free, and we have $x_2 = 1+x_3$ and $x_1 = -2 -x_3$. Thus, the solution set is
<div class="arithmatex" markdown="1">
\[
\{(-2-x_3, 1+x_3, x_3) \ | \ x_3 \in {\bf R} \}.
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.7.3</strong></p>

<span id="sol-ex-systems-1-b" label="sol--ex:systems-1-b"></span> (See <a href="#ex-systems-1-b" data-reference-type="ref+Label" data-reference="ex:systems-1-b">Exercise 2.12</a>.) We apply <a href="#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>. The matrix associated to the system is
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} 1 & -1 & 1 & 0 & -2 \\ 0 & 0 & 1 & -1 & 1 \\ 1 & -1 & 0 & 1 & -3 \\ 1 & -1 & 3 & -2 & 0 \end{array} \right ).
\]
</div>
We compute the reduced row-echelon form of that matrix using Gaussian eliminiation (<a href="#met-gaussian-algorithm" data-reference-type="ref+Label" data-reference="met:gaussian-algorithm">Method 2.29</a>): we subtract the first row from the third, which gives
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} 1 & -1 & 1 & 0 & -2 \\ 0 & 0 & 1 & -1 & 1 \\ 0 & 0 & -1 & 1 & -1 \\ 1 & -1 & 3 & -2 & 0 \end{array} \right ).
\]
</div>
We then subtract the first row from the fourth:
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} 1 & -1 & 1 & 0 & -2 \\ 0 & 0 & 1 & -1 & 1 \\ 0 & 0 & -1 & 1 & -1 \\ 0 & 0 & 2 & -2 & 2 \end{array} \right ).
\]
</div>
We add the second line to the third:
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} 1 & -1 & 1 & 0 & -2 \\ 0 & 0 & 1 & -1 & 1 \\ 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 2 & -2 & 2 \end{array} \right ).
\]
</div>
We then add $(-2)$ times the second line to the fourth (equivalently, subtract $2$ times the second line from the fourth):
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} {\underline 1} & -1 & 1 & 0 & -2 \\ 0 & 0 & {\underline 1} & -1 & 1 \\ 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 \end{array} \right ).
\]
</div>
This matrix is in row-echelon form, with the leading 1’s being underlined above. We finally bring it into reduced row-echelon form by subtracting the second from the first line, which gives
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} {\underline 1} & -1 & 0 & 1 & -3 \\ 0 & 0 & {\underline 1} & -1 & 1 \\ 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 \end{array} \right ).
\]
</div>
The matrix has no entry of the form $0 \ \dots \ 0 \ 1$, so the system does have a solution. The first column of the matrix corresponds to the variable $x_1$ etc., so that the free variables are $x_2$ and $x_4$. We let $x_2 = \alpha$, $x_4 = \beta$, where $\alpha$ and $\beta$ are arbitrary real numbers. The non-free variables $x_1$ and $x_3$ are uniquely determined by $\alpha$ and $\beta$. To compute them, we use the equations obtained by the matrix
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x_3 - \beta & = 1 \\
x_1 -\alpha + \beta & = -3
\end{align*}
\]
</div>
which we solve as $x_3 = 1 + \beta$ and $x_1 = \alpha-\beta-3$. Thus, the solution set is
<div class="arithmatex" markdown="1">
\[
\{(\alpha - \beta - 3, \alpha, 1+\beta, \beta) \ | \ \alpha, \beta \in {\bf R}\}.
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.7.4</strong></p>

<span id="sol-ex-systems-1-c" label="sol--ex:systems-1-c"></span> (See <a href="#ex-systems-1-c" data-reference-type="ref+Label" data-reference="ex:systems-1-c">Exercise 2.14</a>.) Hint: we will apply Gaussian elimination, but it simplifies the calculations to do a certain change of rows first. (Why is that allowed?)

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.7.5</strong></p>

<span id="sol-ex-systems-1-d" label="sol--ex:systems-1-d"></span> (See <a href="#ex-systems-1-d" data-reference-type="ref+Label" data-reference="ex:systems-1-d">Exercise 2.17</a>.) Suppose $x_1 = 1-t$, $x_2 = 2+3t$ and $x_3 = 4t$. We have to determine whether there is some $t\in {\bf R}$ such that for these choices of $x_1, x_2, x_3$, we have a solution of the given system, i.e., whether
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x_1 + x_2 + x_3 & = (1-t)+(2+3t)+4t & = 1 \\
x_1 - x_3 & = 1-t-4t & = 0.
\end{align*}
\]
</div>
Simplifying these equations gives the system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
6t + 3 & = 0 \\
1-5t & = 0.
\end{align*}
\]
</div>
This system has no solutions, so there is no $t \in {\bf R}$ such that the vector $(1-t, 2+3t, 4t)$ is a solution to the original system.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.7.6</strong></p>

<span id="sol-ex-systems-1-e" label="sol--ex:systems-1-e"></span> (See <a href="#ex-systems-1-e" data-reference-type="ref+Label" data-reference="ex:systems-1-e">Exercise 2.19</a>.) We substitute $x_1 = 1+t$, $x_2 = t+q$ and $x_3 = -t+2q+1$ into the given equation and get the equation
<div class="arithmatex" markdown="1">
\[
3(1+t)+2(t+q)-(-t+2q+1)=5.
\]
</div>
This simplifies to
<div class="arithmatex" markdown="1">
\[
6t+2=5
\]
</div>
which has the solution $t = -\frac 12$. Since the variable $q$ does not appear in that equation it is a free variable. Thus, for all $q \in {\bf R}$, the vector
<div class="arithmatex" markdown="1">
\[
(x_1 = 1-\frac 12, x_2 = -\frac 12 + q, x_3 = \frac 12 + 2q+1) = (\frac 12, -\frac 12+q, \frac 32 + 2q)
\]
</div>
satisfies the requested conditions. Note that these are infinitely many solutions.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.7.7</strong></p>

<span id="sol-ex-systems-1-f" label="sol--ex:systems-1-f"></span> (See <a href="#ex-systems-1-f" data-reference-type="ref+Label" data-reference="ex:systems-1-f">Exercise 2.20</a>.) We have to find $a_0, \dots, a_3$, so these are the unknowns. The conditions amount to the linear (!) system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
p(1) & = a_0 + a_1 + a_2 + a_3 & = 0 \\
p(2) & = a_0 + a_1 \cdot 2+ a_2 \cdot 2^2 + a_3 \cdot 2^3 & = 3.
\end{align*}
\]
</div>
This can be rewritten as
<div class="arithmatex" markdown="1">
\[
\begin{align*}
a_0 + a_1 + a_2 + a_3 & = 0 \\
a_0 + 2 a_1 + 4 a_2 + 8 a_3 & = 3.
\end{align*}
\]
</div>
Using Gaussian elimination to solve this: the associated matrix is
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} 1 & 1 & 1 & 1 & 0 \\ 1 & 2 & 4 & 8 & 3 \end{array} \right ).
\]
</div>
Subtracting the first from the second row gives
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} 1 & 1 & 1 & 1 & 0 \\ 0 & 1 & 3 & 7 & 3 \end{array} \right ).
\]
</div>
Subtracting the second from the first yields a reduced row echelon matrix:
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} 1 & 0 & -2 & -6 & -3 \\ 0 & 1 & 3 & 7 & 3 \end{array} \right ).
\]
</div>
The variables $a_0$ and $a_1$ correspond to the leading 1’s, the variables $a_2$ and $a_3$ are therefore free variables. Thus, there are infintely many solutions. One solution, for $a_2 = a_3 = 0$ is
<div class="arithmatex" markdown="1">
\[
a_0 = -3, \ a_1 = 3,
\]
</div>
so that
<div class="arithmatex" markdown="1">
\[
p(x) = -3 + 3x
\]
</div>
is a solution to the problem. Another solution would be $a_2 = a_3 = 1$, which gives $a_1 = -7$ and $a_0 = 5$, i.e.,
<div class="arithmatex" markdown="1">
\[
p(x) = 5 - 7 x + x^2 + x^3.
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.7.8</strong></p>

<span id="sol-ex-maps-exercise-008" label="sol--ex:maps-exercise-008"></span> (See <a href="#ex-maps-exercise-008" data-reference-type="ref+Label" data-reference="ex:maps-exercise-008">Exercise 2.25</a>.) We solve, for each $\lambda\in\mathbf R$, the system by Gaussian elimination (<a href="#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>):
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc|c} \lambda & 0 & 0 & 0\\ 0 & \lambda & 1+\lambda & 1\\ \lambda & 1 & 2 & 3 \end{array} \right )
\xrightarrow{R_3\leftarrow R_3-R_1}
\left ( \begin{array}{ccc|c} \lambda & 0 & 0 & 0\\ 0 & \lambda & 1+\lambda & 1\\ 0 & 1 & 2 & 3 \end{array} \right ).
\]
</div>
We would like to divide the first row by $\lambda$, which however is only a legitimate row operation (<a href="#def-elementary-row-operations" data-reference-type="ref+Label" data-reference="def:elementary-row-operations">Definition 2.28</a>) if $\lambda \ne 0$. So we distinguish two cases:

- *Case $\lambda=0$.* The matrix becomes
<div class="arithmatex" markdown="1">
\[
  \left ( \begin{array}{ccc|c} 0 & 0 & 0 & 0\\ 0 & 0 & 1 & 1\\ 0 & 1 & 2 & 3 \end{array} \right ),
\]
</div>
  so $x_3=1$, $x_2=1$, and $x_1$ is free. Hence the solution set is $\{(t, 1, 1) \mid t \in \mathbf R\}$.

- *Case $\lambda\neq0$.* Divide row 2 by $\lambda$ and eliminate the $1$ in row 3, column 2:
<div class="arithmatex" markdown="1">
\[
  \left ( \begin{array}{ccc|c} \lambda & 0 & 0 & 0\\ 0 & 1 & \frac{1+\lambda}{\lambda} & \frac1\lambda\\ 0 & 1 & 2 & 3 \end{array} \right )
      \xrightarrow{R_3\leftarrow R_3-R_2}
      \left ( \begin{array}{ccc|c} \lambda & 0 & 0 & 0\\ 0 & 1 & \frac{1+\lambda}{\lambda} & \frac1\lambda\\ 0 & 0 & \frac{\lambda-1}{\lambda} & \frac{3\lambda-1}{\lambda} \end{array} \right ).
\]
</div>
  The next possible division is by $\lambda-1$, so we split again:

  - If $\lambda=1$, the last row is $0\;0\;0\mid2$, so there is no solution.

  - If $\lambda\neq1$, then
<div class="arithmatex" markdown="1">
\[
    x_1=0,\qquad x_3=\frac{3\lambda-1}{\lambda-1}=\frac{1-3\lambda}{1-\lambda},\qquad x_2=3-2x_3.
\]
</div>
    So the solution is unique.

*Summary:*

- If $\lambda=0$: infinitely many solutions, namely $(t,1,1)$ with $t\in\mathbf R$.

- If $\lambda=1$: no solution.

- If $\lambda\neq0,1$: unique solution $\left(0,\,3-2\frac{1-3\lambda}{1-\lambda},\,\frac{1-3\lambda}{1-\lambda}\right)$.

</div>
