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
What is the matrix associated to that system? Using <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>, find all solutions of that system.

</div>

<div class="exercise" markdown="1">

Consider the (augmented) matrix
<div class="arithmatex" markdown="1">
\[
A := \left ( \begin{array}{cccccc|c} 1 & 0 & 3 & 0 & 0 & 0 & 1 \\ 0 & 1 & 2 & 4 & 1 & 0 & 0 \\ 0 & 0 & 0 & 2 & 1 & 0 & 2 \\ 0 & 0 & 0 & 0 & 0 & 1 & 3 \\ 0 & 0 & 0 & 0 & 0 & 0 & 0 \end{array} \right ).
\]
</div>
What type of matrix is that? (I.e., what $m \times n$-matrix.) If $A = (a_{ij})$, what is $a_{13}$ and $a_{31}$? What is the linear system associated to that matrix? (Hint: one equation reads “$\dots = 3$”. For consistency, call the variables $x_1, x_2, \dots, x_6$.)

Is the matrix in row-echelon form? Is it in reduced row-echelon form? If not, use the Gaussian algorithm (<a href="../systems-gaussian-elimination/#met-gaussian-algorithm" data-reference-type="ref+Label" data-reference="met:gaussian-algorithm">Method 2.29</a>) in order to transform it into reduced row-echelon form. Name the columns which contain a leading 1 (Hint: there are 4 of them). Which variables are free, which variables are not free? Use <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a> and solve the linear system associated to that augmented matrix.

</div>

<div class="exercise" markdown="1">

Using <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>, find all solutions of the following systems
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

<span id="ex-equation-no-solutions" label="ex:equation-no-solutions"></span> (See <a href="../solutions-systems-of-linear-equations/#sol-ex-equation-no-solutions" data-reference-type="ref+Label" data-reference="sol--ex:equation-no-solutions">Solution 2.7.1</a>.) Let
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

<span id="ex-systems-1-a" label="ex:systems-1-a"></span> (See <a href="../solutions-systems-of-linear-equations/#sol-ex-systems-1-a" data-reference-type="ref+Label" data-reference="sol--ex:systems-1-a">Solution 2.7.2</a>.) Find the solutions of the system
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

<span id="ex-systems-1-b" label="ex:systems-1-b"></span> (See <a href="../solutions-systems-of-linear-equations/#sol-ex-systems-1-b" data-reference-type="ref+Label" data-reference="sol--ex:systems-1-b">Solution 2.7.3</a>.) Find the solutions of the following linear system in the variables $x_1, \dots, x_4$:
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

<span id="ex-systems-1-c" label="ex:systems-1-c"></span> (See <a href="../solutions-systems-of-linear-equations/#sol-ex-systems-1-c" data-reference-type="ref+Label" data-reference="sol--ex:systems-1-c">Solution 2.7.4</a>.) Solve the following linear system, where $h$ is a parameter and $x,y,z$ are the unknowns:
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

<span id="ex-systems-1-d" label="ex:systems-1-d"></span> (See <a href="../solutions-systems-of-linear-equations/#sol-ex-systems-1-d" data-reference-type="ref+Label" data-reference="sol--ex:systems-1-d">Solution 2.7.5</a>.) Consider the linear system (in the unknowns $x_1, x_2, x_3$):
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

<span id="ex-systems-1-e" label="ex:systems-1-e"></span> (See <a href="../solutions-systems-of-linear-equations/#sol-ex-systems-1-e" data-reference-type="ref+Label" data-reference="sol--ex:systems-1-e">Solution 2.7.6</a>.) Do there exist $q, t \in {\bf R}$ such that the vector
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

<span id="ex-systems-1-f" label="ex:systems-1-f"></span> (See <a href="../solutions-systems-of-linear-equations/#sol-ex-systems-1-f" data-reference-type="ref+Label" data-reference="sol--ex:systems-1-f">Solution 2.7.7</a>.) Find a polynomial
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

<span id="ex-maps-exercise-008" label="ex:maps-exercise-008"></span> (See <a href="../solutions-systems-of-linear-equations/#sol-ex-maps-exercise-008" data-reference-type="ref+Label" data-reference="sol--ex:maps-exercise-008">Solution 2.7.8</a>.) For any $\lambda \in {\bf R}$ solve the system (in the unknowns $x_1, x_2, x_3$)
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
