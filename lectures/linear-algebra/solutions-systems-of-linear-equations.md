<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.7.1</strong></p>

<span id="sol-ex-equation-no-solutions" label="sol--ex:equation-no-solutions"></span> (See <a href="../systems-gaussian-elimination/#ex-equation-no-solutions" data-reference-type="ref+Label" data-reference="ex:equation-no-solutions">Exercise 2.6</a>.) If $a \ne 0$ *or* $b \ne 0$, then the equation $ax+by = c$ has infinitely many solutions. Indeed, if, say $a \ne 0$, we can subtract $by$ and divide by $a$, which gives $x = \frac{c-by}a$. Thus, for any $y \in {\bf R}$, the pair $(x=\frac{c-by}a, y)$ is a solution. A similar analysis works if $b \ne 0$. It remains to consider the case in which $a=0$ and $b=0$. In this case the solution set of the equation depends on $c$:

- If $c = 0$, then *any* pair $(x,y)$ is a solution. Indeed: $0 x + 0y= 0$ holds true then. Thus, if $a=b=c=0$, there are infinitely many solutions.

- If $c \ne 0$, the equation $0x+0y = c$ has no solution, since the left hand side is always 0, while the right hand side is nonzero. So, in the case $a=b=0$ but $c \ne 0$, there is *no* solution.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.7.2</strong></p>

<span id="sol-ex-systems-1-a" label="sol--ex:systems-1-a"></span> (See <a href="../systems-gaussian-elimination/#ex-systems-1-a" data-reference-type="ref+Label" data-reference="ex:systems-1-a">Exercise 2.10</a>.) The matrix associated to the system is as follows, and we bring it to reduced row echelon form:
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

<span id="sol-ex-systems-1-b" label="sol--ex:systems-1-b"></span> (See <a href="../systems-gaussian-elimination/#ex-systems-1-b" data-reference-type="ref+Label" data-reference="ex:systems-1-b">Exercise 2.12</a>.) We apply <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>. The matrix associated to the system is
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} 1 & -1 & 1 & 0 & -2 \\ 0 & 0 & 1 & -1 & 1 \\ 1 & -1 & 0 & 1 & -3 \\ 1 & -1 & 3 & -2 & 0 \end{array} \right ).
\]
</div>
We compute the reduced row-echelon form of that matrix using Gaussian eliminiation (<a href="../systems-gaussian-elimination/#met-gaussian-algorithm" data-reference-type="ref+Label" data-reference="met:gaussian-algorithm">Method 2.29</a>): we subtract the first row from the third, which gives
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

<span id="sol-ex-systems-1-c" label="sol--ex:systems-1-c"></span> (See <a href="../systems-gaussian-elimination/#ex-systems-1-c" data-reference-type="ref+Label" data-reference="ex:systems-1-c">Exercise 2.14</a>.) Hint: we will apply Gaussian elimination, but it simplifies the calculations to do a certain change of rows first. (Why is that allowed?)

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.7.5</strong></p>

<span id="sol-ex-systems-1-d" label="sol--ex:systems-1-d"></span> (See <a href="../systems-gaussian-elimination/#ex-systems-1-d" data-reference-type="ref+Label" data-reference="ex:systems-1-d">Exercise 2.17</a>.) Suppose $x_1 = 1-t$, $x_2 = 2+3t$ and $x_3 = 4t$. We have to determine whether there is some $t\in {\bf R}$ such that for these choices of $x_1, x_2, x_3$, we have a solution of the given system, i.e., whether
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

<span id="sol-ex-systems-1-e" label="sol--ex:systems-1-e"></span> (See <a href="../systems-gaussian-elimination/#ex-systems-1-e" data-reference-type="ref+Label" data-reference="ex:systems-1-e">Exercise 2.19</a>.) We substitute $x_1 = 1+t$, $x_2 = t+q$ and $x_3 = -t+2q+1$ into the given equation and get the equation
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

<span id="sol-ex-systems-1-f" label="sol--ex:systems-1-f"></span> (See <a href="../systems-gaussian-elimination/#ex-systems-1-f" data-reference-type="ref+Label" data-reference="ex:systems-1-f">Exercise 2.20</a>.) We have to find $a_0, \dots, a_3$, so these are the unknowns. The conditions amount to the linear (!) system
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

<span id="sol-ex-maps-exercise-008" label="sol--ex:maps-exercise-008"></span> (See <a href="../systems-gaussian-elimination/#ex-maps-exercise-008" data-reference-type="ref+Label" data-reference="ex:maps-exercise-008">Exercise 2.25</a>.) We solve, for each $\lambda\in\mathbf R$, the system by Gaussian elimination (<a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>):
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc|c} \lambda & 0 & 0 & 0\\ 0 & \lambda & 1+\lambda & 1\\ \lambda & 1 & 2 & 3 \end{array} \right )
\xrightarrow{R_3\leftarrow R_3-R_1}
\left ( \begin{array}{ccc|c} \lambda & 0 & 0 & 0\\ 0 & \lambda & 1+\lambda & 1\\ 0 & 1 & 2 & 3 \end{array} \right ).
\]
</div>
We would like to divide the first row by $\lambda$, which however is only a legitimate row operation (<a href="../systems-gaussian-elimination/#def-elementary-row-operations" data-reference-type="ref+Label" data-reference="def:elementary-row-operations">Definition 2.28</a>) if $\lambda \ne 0$. So we distinguish two cases:

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
