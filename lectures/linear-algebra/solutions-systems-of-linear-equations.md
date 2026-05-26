<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.1</strong></p>

<span id="sol-ex-systems-line-xy3" label="sol--ex:systems-line-xy3"></span> (See <a href="../exercises-systems/#ex-systems-line-xy3" data-reference-type="ref+Label" data-reference="ex:systems-line-xy3">Exercise 2.1</a>.) By <a href="../systems-linear-equations/#def-systems-definition-001" data-reference-type="ref+Label" data-reference="def:systems-definition-001">Definition 2.1</a>, the equation $x+y=3$ is a linear equation in two variables. Solving for $y$ gives $y = 3-x$, so for every $x \in \mathbf{R}$ the pair $(x,\, 3-x)$ is a solution. The solution set is
<div class="arithmatex" markdown="1">
\[
\{ (x,\, 3-x) \mid x \in \mathbf{R} \}.
\]
</div>
Geometrically this is a straight line in the $xy$-plane with slope $-1$, passing through the points $(0,3)$ and $(3,0)$:

<div class="center" markdown="1">

</div>

The equation is *not* homogeneous (see <a href="../systems-linear-systems/#def-homogeneous-linear-system" data-reference-type="ref+Label" data-reference="def:homogeneous-linear-system">Definition 2.13</a>), because the right-hand side equals $3 \ne 0$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.2</strong></p>

<span id="sol-ex-systems-line-x3-vars" label="sol--ex:systems-line-x3-vars"></span> (See <a href="../exercises-systems/#ex-systems-line-x3-vars" data-reference-type="ref+Label" data-reference="ex:systems-line-x3-vars">Exercise 2.2</a>.) By <a href="../systems-linear-equations/#def-systems-definition-001" data-reference-type="ref+Label" data-reference="def:systems-definition-001">Definition 2.1</a>, the equation $x = 3$ is a linear equation.

*One variable.* Here the only unknown is $x$, and the equation uniquely determines it: $x = 3$. The solution set is therefore
<div class="arithmatex" markdown="1">
\[
\{3\} \subset \mathbf{R},
\]
</div>
a single point on the real line.

*Two variables.* When we think of the equation as $x + 0 \cdot y = 3$ in the unknowns $x$ and $y$, the variable $y$ does not appear and can take any value in $\mathbf{R}$. For each $y \in \mathbf{R}$ the pair $(3, y)$ is a solution, so the solution set is
<div class="arithmatex" markdown="1">
\[
\{(3,\, y) \mid y \in \mathbf{R}\} \subset \mathbf{R}^2.
\]
</div>
Geometrically this is the vertical line $x = 3$ in the $xy$-plane:

<div class="center" markdown="1">

</div>

Note that the solution set in the two-variable case is much larger than in the one-variable case: adding a variable introduces a whole new dimension of solutions.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.3</strong></p>

<span id="sol-ex-systems-gauss-4vars" label="sol--ex:systems-gauss-4vars"></span> (See <a href="../exercises-systems/#ex-systems-gauss-4vars" data-reference-type="ref+Label" data-reference="ex:systems-gauss-4vars">Exercise 2.3</a>.) The augmented matrix associated to the system is (see <a href="../systems-matrices/#def-matrix-to-system" data-reference-type="ref+Label" data-reference="def:matrix-to-system">Definition 2.23</a>)
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} 2 & -1 & 1 & 1 & 1 \\ 0 & 5 & -3 & -5 & -3 \\ 3 & -4 & 3 & 4 & 3 \end{array} \right ).
\]
</div>
We bring this matrix to reduced row-echelon form using <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>. Subtracting the first row from the third gives $R_3 = (1, -3, 2, 3 \mid 2)$, and swapping this with the first row yields
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} 1 & -3 & 2 & 3 & 2 \\ 0 & 5 & -3 & -5 & -3 \\ 2 & -1 & 1 & 1 & 1 \end{array} \right ).
\]
</div>
Subtracting $2$ times the first row from the third eliminates $x_1$:
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} 1 & -3 & 2 & 3 & 2 \\ 0 & 5 & -3 & -5 & -3 \\ 0 & 5 & -3 & -5 & -3 \end{array} \right ).
\]
</div>
The third row equals the second, so subtracting the second row from the third produces a zero row. Dividing the second row by $5$ creates the next leading $1$:
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} 1 & -3 & 2 & 3 & 2 \\ 0 & 1 & -\tfrac{3}{5} & -1 & -\tfrac{3}{5} \\ 0 & 0 & 0 & 0 & 0 \end{array} \right ).
\]
</div>
Adding $3$ times the second row to the first eliminates $x_2$ from the first row and yields the reduced row-echelon form (see <a href="../systems-gaussian-elimination/#def-row-echelon-form" data-reference-type="ref+Label" data-reference="def:row-echelon-form">Definition 2.27</a>):
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} \underline{1} & 0 & \tfrac{1}{5} & 0 & \tfrac{1}{5} \\[4pt] 0 & \underline{1} & -\tfrac{3}{5} & -1 & -\tfrac{3}{5} \\[4pt] 0 & 0 & 0 & 0 & 0 \end{array} \right ).
\]
</div>
There are two leading ones (underlined), in columns $1$ and $2$, so $x_1$ and $x_2$ are non-free, while $x_3$ and $x_4$ are free variables. Setting $x_3 = s$ and $x_4 = t$ with $s, t \in \mathbf{R}$, the non-zero rows give
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x_1 &= \tfrac{1}{5} - \tfrac{s}{5}, \\
x_2 &= -\tfrac{3}{5} + \tfrac{3s}{5} + t.
\end{align*}
\]
</div>
The solution set is therefore
<div class="arithmatex" markdown="1">
\[
\left\{ \Bigl(\tfrac{1-s}{5},\; \tfrac{3(s-1)}{5} + t,\; s,\; t\Bigr) \;\middle|\; s, t \in \mathbf{R} \right\}.
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.4</strong></p>

<span id="sol-ex-systems-matrix-5x7" label="sol--ex:systems-matrix-5x7"></span> (See <a href="../exercises-systems/#ex-systems-matrix-5x7" data-reference-type="ref+Label" data-reference="ex:systems-matrix-5x7">Exercise 2.4</a>.) The matrix $A$ has $5$ rows and $7$ columns, so it is a $5\times 7$ matrix (according to the terminology introduced in <a href="../systems-matrices/#def-systems-definition-006" data-reference-type="ref+Label" data-reference="def:systems-definition-006">Definition 2.20</a>). The coefficient part has $6$ columns (corresponding to the six unknowns $x_1,\ldots,x_6$) and one augmented column, so $A$ is used as an augmented matrix for a linear system with $5$ equations in $6$ unknowns (see <a href="../systems-matrices/#def-matrix-to-system" data-reference-type="ref+Label" data-reference="def:matrix-to-system">Definition 2.23</a>).

The entries are $a_{13} = 3$ (row $1$, column $3$) and $a_{31} = 0$ (row $3$, column $1$).

The associated linear system is (see <a href="../systems-matrices/#def-matrix-to-system" data-reference-type="ref+Label" data-reference="def:matrix-to-system">Definition 2.23</a>):
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x_1 + 3x_3 &= 1, \\
x_2 + 2x_3 + 4x_4 + x_5 &= 0, \\
2x_4 + x_5 &= 2, \\
x_6 &= 3, \\
0 &= 0.
\end{align*}
\]
</div>
(The fifth equation $0=0$ is trivially satisfied and imposes no constraint.)

The matrix is in *row-echelon form* (see <a href="../systems-gaussian-elimination/#def-row-echelon-form" data-reference-type="ref+Label" data-reference="def:row-echelon-form">Definition 2.27</a>): the zero row is at the bottom, and the leading entries in rows $1$–$4$ lie in columns $1,2,4,6$, which are strictly increasing from left to right.

It is *not* in reduced row-echelon form, because (i) row $3$ has leading entry $2$, not $1$, and (ii) column $4$ contains a nonzero entry ($4$) in row $2$ above the leading entry of row $3$.

We apply the Gaussian algorithm (<a href="../systems-gaussian-elimination/#met-gaussian-algorithm" data-reference-type="ref+Label" data-reference="met:gaussian-algorithm">Method 2.29</a>) to reach *reduced* row echelon form. First, scale row $3$ by $\tfrac{1}{2}$:
<div class="arithmatex" markdown="1">
\[
A \xrightarrow{\frac{1}{2}R_3\to R_3}
\left ( \begin{array}{cccccc|c} 1 & 0 & 3 & 0 & 0 & 0 & 1 \\ 0 & 1 & 2 & 4 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 & \tfrac{1}{2} & 0 & 1 \\ 0 & 0 & 0 & 0 & 0 & 1 & 3 \\ 0 & 0 & 0 & 0 & 0 & 0 & 0 \end{array} \right ).
\]
</div>
Then eliminate $x_4$ from row $2$ via $R_2 \to R_2 - 4R_3$:
<div class="arithmatex" markdown="1">
\[
\xrightarrow{R_2-4R_3\to R_2}
\left ( \begin{array}{cccccc|c} \underline{1} & 0 & 3 & 0 & 0 & 0 & 1 \\ 0 & \underline{1} & 2 & 0 & -1 & 0 & -4 \\ 0 & 0 & 0 & \underline{1} & \tfrac{1}{2} & 0 & 1 \\ 0 & 0 & 0 & 0 & 0 & \underline{1} & 3 \\ 0 & 0 & 0 & 0 & 0 & 0 & 0 \end{array} \right ).
\]
</div>
This is the reduced row-echelon form: each leading $1$ (underlined) is the only nonzero entry in its column.

The leading $1$s are in columns $1, 2, 4, 6$ (four of them). Hence the *pivot variables* are $x_1, x_2, x_4, x_6$, and the *free variables* are $x_3$ and $x_5$.

We read off the solution using <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>. Set $x_3 = s$ and $x_5 = t$ with $s,t\in\mathbf{R}$. Then:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x_1 &= 1 - 3s, \\
x_2 &= -4 - 2s + t, \\
x_4 &= 1 - \tfrac{t}{2}, \\
x_6 &= 3.
\end{align*}
\]
</div>
The solution set is
<div class="arithmatex" markdown="1">
\[
\bigl\{\,(1-3s,\; -4-2s+t,\; s,\; 1-\tfrac{t}{2},\; t,\; 3)\;\bigm|\; s,t\in\mathbf{R}\,\bigr\}.
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.5</strong></p>

<span id="sol-ex-systems-two-systems" label="sol--ex:systems-two-systems"></span> (See <a href="../exercises-systems/#ex-systems-two-systems" data-reference-type="ref+Label" data-reference="ex:systems-two-systems">Exercise 2.5</a>.) We apply <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a> to each system. The augmented matrix for the first system is (see <a href="../systems-matrices/#def-matrix-to-system" data-reference-type="ref+Label" data-reference="def:matrix-to-system">Definition 2.23</a>)
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc|c} 1 & 1 & -1 & 1 \\ 3 & -1 & 2 & 5 \\ 4 & 0 & 1 & 6 \end{array} \right ).
\]
</div>
Eliminating $x$ from rows $2$ and $3$:
<div class="arithmatex" markdown="1">
\[
\xrightarrow{R_2-3R_1\to R_2,\;R_3-4R_1\to R_3}
\left ( \begin{array}{ccc|c} 1 & 1 & -1 & 1 \\ 0 & -4 & 5 & 2 \\ 0 & -4 & 5 & 2 \end{array} \right ).
\]
</div>
The second and third rows are identical, so subtracting row $2$ from row $3$ produces a zero row. Dividing row $2$ by $-4$ creates the next leading $1$:
<div class="arithmatex" markdown="1">
\[
\xrightarrow{R_3-R_2\to R_3,\;-\frac{1}{4}R_2\to R_2}
\left ( \begin{array}{ccc|c} 1 & 1 & -1 & 1 \\ 0 & 1 & -\tfrac{5}{4} & -\tfrac{1}{2} \\ 0 & 0 & 0 & 0 \end{array} \right ).
\]
</div>
Subtracting row $2$ from row $1$ yields the reduced row-echelon form (see <a href="../systems-gaussian-elimination/#def-row-echelon-form" data-reference-type="ref+Label" data-reference="def:row-echelon-form">Definition 2.27</a>):
<div class="arithmatex" markdown="1">
\[
\xrightarrow{R_1-R_2\to R_1}
\left ( \begin{array}{ccc|c} \underline{1} & 0 & \tfrac{1}{4} & \tfrac{3}{2} \\[4pt] 0 & \underline{1} & -\tfrac{5}{4} & -\tfrac{1}{2} \\[4pt] 0 & 0 & 0 & 0 \end{array} \right ).
\]
</div>
The pivot variables are $x$ and $y$; the variable $z$ is free. Setting $z = t$ with $t \in \mathbf{R}$:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x &= \tfrac{3}{2} - \tfrac{t}{4}, \\
y &= -\tfrac{1}{2} + \tfrac{5t}{4}.
\end{align*}
\]
</div>
The solution set is $\bigl\{\,\bigl(\tfrac{3}{2}-\tfrac{t}{4},\;-\tfrac{1}{2}+\tfrac{5t}{4},\;t\bigr)\bigm|\;t\in\mathbf{R}\,\bigr\}$.

We proceed similarly with the second system. The augmented matrix is
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left ( \begin{array}{ccc|c} 1 & 1 & -1 & 1 \\ 3 & -1 & 2 & 0 \\ 1 & 1 & -2 & 2 \end{array} \right ) & \xrightarrow{R_2-3R_1\to R_2,\;R_3-R_1\to R_3} & 
\left ( \begin{array}{ccc|c} 1 & 1 & -1 & 1 \\ 0 & -4 & 5 & -3 \\ 0 & 0 & -1 & 1 \end{array} \right ) \\
& \xrightarrow{-R_3\to R_3} &
\left ( \begin{array}{ccc|c} 1 & 1 & -1 & 1 \\ 0 & -4 & 5 & -3 \\ 0 & 0 & 1 & -1 \end{array} \right ) \\
& \xrightarrow{R_2-5R_3\to R_2,\;R_1+R_3\to R_1} & 
\left ( \begin{array}{ccc|c} 1 & 1 & 0 & 0 \\ 0 & -4 & 0 & 2 \\ 0 & 0 & 1 & -1 \end{array} \right ).
\end{align*}
\]
</div>
Scale row $2$ and eliminate $y$ from row $1$:
<div class="arithmatex" markdown="1">
\[
\xrightarrow{-\frac{1}{4}R_2\to R_2}
\left ( \begin{array}{ccc|c} 1 & 1 & 0 & 0 \\ 0 & 1 & 0 & -\tfrac{1}{2} \\ 0 & 0 & 1 & -1 \end{array} \right )
\xrightarrow{R_1-R_2\to R_1}
\left ( \begin{array}{ccc|c} \underline{1} & 0 & 0 & \tfrac{1}{2} \\[4pt] 0 & \underline{1} & 0 & -\tfrac{1}{2} \\[4pt] 0 & 0 & \underline{1} & -1 \end{array} \right ).
\]
</div>
All three variables are pivot variables; there are no free variables. The system has the unique solution $(x, y, z) = \bigl(\tfrac{1}{2},\;-\tfrac{1}{2},\;-1\bigr)$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.6</strong></p>

<span id="sol-ex-equation-no-solutions" label="sol--ex:equation-no-solutions"></span> (See <a href="../exercises-systems/#ex-equation-no-solutions" data-reference-type="ref+Label" data-reference="ex:equation-no-solutions">Exercise 2.6</a>.) If $a \ne 0$ *or* $b \ne 0$, then the equation $ax+by = c$ has infinitely many solutions. Indeed, if, say $a \ne 0$, we can subtract $by$ and divide by $a$, which gives $x = \frac{c-by}a$. Thus, for any $y \in {\bf R}$, the pair $(x=\frac{c-by}a, y)$ is a solution. A similar analysis works if $b \ne 0$. It remains to consider the case in which $a=0$ and $b=0$. In this case the solution set of the equation depends on $c$:

- If $c = 0$, then *any* pair $(x,y)$ is a solution. Indeed: $0 x + 0y= 0$ holds true then. Thus, if $a=b=c=0$, there are infinitely many solutions.

- If $c \ne 0$, the equation $0x+0y = c$ has no solution, since the left hand side is always 0, while the right hand side is nonzero. So, in the case $a=b=0$ but $c \ne 0$, there is *no* solution.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.7</strong></p>

<span id="sol-ex-systems-rref-from-exa" label="sol--ex:systems-rref-from-exa"></span> (See <a href="../exercises-systems/#ex-systems-rref-from-exa" data-reference-type="ref+Label" data-reference="ex:systems-rref-from-exa">Exercise 2.7</a>.) We apply <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a> to bring each augmented matrix (see <a href="../systems-matrices/#def-matrix-to-system" data-reference-type="ref+Label" data-reference="def:matrix-to-system">Definition 2.23</a>) to reduced row-echelon form (see <a href="../systems-gaussian-elimination/#def-row-echelon-form" data-reference-type="ref+Label" data-reference="def:row-echelon-form">Definition 2.27</a>).

We consider the system from <a href="../systems-linear-systems/#ex-system-2-unique" data-reference-type="ref+Label" data-reference="ex:system-2-unique">Example 2.8</a>: $x+y=4$, $x-y=1$. We bring the augmented matrix to reduced row-echelon form:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
    \left ( \begin{array}{cc|c} 1 & 1 & 4 \\ 1 & -1 & 1 \end{array} \right )
%Subtract row~$1$ from row~$2$, then scale row~$2$ by $-\tfrac{1}{2}$:
& \xrightarrow{R_2 - R_1 \to R_2} & 
\left ( \begin{array}{cc|c} 1 & 1 & 4 \\ 0 & -2 & -3 \end{array} \right ) \\
& \xrightarrow{-\frac{1}{2}R_2 \to R_2} & 
\left ( \begin{array}{cc|c} 1 & 1 & 4 \\ 0 & 1 & \tfrac{3}{2} \end{array} \right ) \\
%Eliminate $y$ from row~$1$:
& \xrightarrow{R_1 - R_2 \to R_1} & 
\left ( \begin{array}{cc|c} \underline{1} & 0 & \tfrac{5}{2} \\[4pt] 0 & \underline{1} & \tfrac{3}{2} \end{array} \right ).
\end{align*}
\]
</div>
Both variables are pivot variables; the system has the unique solution $(x, y) = \bigl(\tfrac{5}{2}, \tfrac{3}{2}\bigr)$.

We now consider the system from <a href="../systems-linear-systems/#ex-system-2-no" data-reference-type="ref+Label" data-reference="ex:system-2-no">Example 2.10</a>: $x+y=4$, $x+y=1$. Again we bring the augmented matrix to reduced row-echelon form:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left ( \begin{array}{cc|c} 1 & 1 & 4 \\ 1 & 1 & 1 \end{array} \right ) & 
%Subtract row~$1$ from row~$2$, then scale row~$2$ by $-\tfrac{1}{3}$:
\xrightarrow{R_2 - R_1 \to R_2} & 
\left ( \begin{array}{cc|c} 1 & 1 & 4 \\ 0 & 0 & -3 \end{array} \right ) \\
&
\xrightarrow{-\frac{1}{3}R_2 \to R_2}
&
\left ( \begin{array}{cc|c} \underline{1} & 1 & 4 \\ 0 & 0 & \underline{1} \end{array} \right ).
\end{align*}
\]
</div>
The last row encodes $0 = 1$, which is a contradiction (cf. <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>, specifically <a href="../systems-gaussian-elimination/#item-gaussian-solve-3" data-reference-type="ref+Label" data-reference="item--gaussian-solve-3">3.</a> there). The system has no solution.

We now consider the system from <a href="../systems-linear-systems/#ex-system-2-infinite" data-reference-type="ref+Label" data-reference="ex:system-2-infinite">Example 2.11</a>: $x+y=4$, $-2x-2y=-8$. The augmented matrix is
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cc|c} 1 & 1 & 4 \\ -2 & -2 & -8 \end{array} \right )
\xrightarrow{R_2 + 2R_1 \to R_2}
\left ( \begin{array}{cc|c} \underline{1} & 1 & 4 \\ 0 & 0 & 0 \end{array} \right ).
\]
</div>
This is already in reduced row-echelon form. The variable $x$ is a pivot variable; $y$ is free. Setting $y = t$ with $t \in \mathbf{R}$, the solution set is
<div class="arithmatex" markdown="1">
\[
\{(4 - t,\, t) \mid t \in \mathbf{R}\}.
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.8</strong></p>

<span id="sol-ex-systems-param-b" label="sol--ex:systems-param-b"></span> (See <a href="../exercises-systems/#ex-systems-param-b" data-reference-type="ref+Label" data-reference="ex:systems-param-b">Exercise 2.8</a>.) By <a href="../systems-matrices/#def-matrix-to-system" data-reference-type="ref+Label" data-reference="def:matrix-to-system">Definition 2.23</a>, the augmented matrix of the system is
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cc|c} 1 & 1 & 1 \\ 1 & -1 & b \end{array} \right ).
\]
</div>
We apply Gaussian elimination (<a href="../systems-gaussian-elimination/#met-gaussian-algorithm" data-reference-type="ref+Label" data-reference="met:gaussian-algorithm">Method 2.29</a>) and perform elementary row operations to bring the matrix to reduced row echelon form:
<div class="arithmatex" markdown="1">
\[
\xrightarrow{R_2 - R_1 \to R_2}
\left ( \begin{array}{cc|c} \underline{1} & 1 & 1 \\ 0 & -2 & b-1 \end{array} \right ) %.$$
%Dividing row~$2$ by $-2$ gives a leading $1$:
%$$
\xrightarrow{-\tfrac{1}{2}R_2 \to R_2}
\left ( \begin{array}{cc|c} \underline{1} & 1 & 1 \\ 0 & \underline{1} & \tfrac{1-b}{2} \end{array} \right ) %.$$
%Subtracting row~$2$ from row~$1$ yields the reduced row-echelon form (see \Cref{def:row-echelon-form}):
%$$
\xrightarrow{R_1 - R_2 \to R_1}
\left ( \begin{array}{cc|c} \underline{1} & 0 & \tfrac{1+b}{2} \\ 0 & \underline{1} & \tfrac{1-b}{2} \end{array} \right ).
\]
</div>
Both variables are pivot variables; there are no free variables. By <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>, the system has a unique solution for every $b \in \mathbf{R}$:
<div class="arithmatex" markdown="1">
\[
x = \tfrac{1+b}{2}, \qquad y = \tfrac{1-b}{2}.
\]
</div>

*Geometric illustration.* Each equation represents a line in the $xy$-plane. The first equation $x+y=1$ always gives the same line (slope $-1$, passing through $(0,1)$ and $(1,0)$). The second equation $x-y=b$ gives a family of parallel lines (slope $1$); a change of the parameter $b$ amounts to a shift of this line. Since the two lines have different slopes ($-1$ and $1$), they always intersect in exactly one point, confirming the unique solution for all $b$.

<div class="center" markdown="1">

</div>

For $b=0$: the unique solution is $\bigl(\tfrac{1}{2}, \tfrac{1}{2}\bigr)$ (intersection of $x+y=1$ and $x-y=0$). For $b=1$: the unique solution is $(1, 0)$ (intersection of $x+y=1$ and $x-y=1$).

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.9</strong></p>

<span id="sol-ex-systems-param-ab" label="sol--ex:systems-param-ab"></span> (See <a href="../exercises-systems/#ex-systems-param-ab" data-reference-type="ref+Label" data-reference="ex:systems-param-ab">Exercise 2.9</a>.) By <a href="../systems-matrices/#def-matrix-to-system" data-reference-type="ref+Label" data-reference="def:matrix-to-system">Definition 2.23</a>, the augmented matrix of the system is
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cc|c} a & b & 1 \\ 1 & -1 & 2 \end{array} \right ).
\]
</div>
Our goal is to use elementary row operations to bring this matrix to reduced row-echelon form. We swap rows $1$ and $2$ (see <a href="../systems-gaussian-elimination/#def-elementary-row-operations" data-reference-type="ref+Label" data-reference="def:elementary-row-operations">Definition 2.28</a>) to obtain a leading $1$ in the first row:
<div class="arithmatex" markdown="1">
\[
\xrightarrow{R_1 \leftrightarrow R_2}
\left ( \begin{array}{cc|c} \underline{1} & -1 & 2 \\ a & b & 1 \end{array} \right ).
\]
</div>
Subtracting $a$ times row $1$ from row $2$ eliminates $x$ from row $2$:
<div class="arithmatex" markdown="1">
\[
\xrightarrow{R_2 - aR_1 \to R_2}
\left ( \begin{array}{cc|c} \underline{1} & -1 & 2 \\ 0 & a+b & 1-2a \end{array} \right ).
\]
</div>
In order to arrive at a row echelon form, we need to have “1” or “0” in place of the entry “$a+b$”. So, we now distinguish cases depending on $a+b$.

1.  This is the case $a + b \neq 0$. In this case we can divide row $2$ by $a+b$:
<div class="arithmatex" markdown="1">
\[
    \xrightarrow{\tfrac{1}{a+b}R_2 \to R_2}
    \left ( \begin{array}{cc|c} \underline{1} & -1 & 2 \\ 0 & \underline{1} & \tfrac{1-2a}{a+b} \end{array} \right ).
\]
</div>
Add row $2$ to row $1$:
<div class="arithmatex" markdown="1">
\[
    \xrightarrow{R_1 + R_2 \to R_1}
    \left ( \begin{array}{cc|c} \underline{1} & 0 & \tfrac{2b+1}{a+b} \\ 0 & \underline{1} & \tfrac{1-2a}{a+b} \end{array} \right ).
\]
</div>
This is the reduced row-echelon form (<a href="../systems-gaussian-elimination/#def-row-echelon-form" data-reference-type="ref+Label" data-reference="def:row-echelon-form">Definition 2.27</a>). Both variables are pivot variables; by <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a> the system has a unique solution:
<div class="arithmatex" markdown="1">
\[
    x = \frac{2b+1}{a+b}, \qquad y = \frac{1-2a}{a+b}.
\]
</div>

2.  This is the case $a + b = 0$, i.e., $b = -a$. The matrix reads
<div class="arithmatex" markdown="1">
\[
    \left ( \begin{array}{cc|c} 1 & -1 & 2 \\ 0 & 0 & 1-2a \end{array} \right ).
\]
</div>
In order to decide whether <a href="../systems-gaussian-elimination/#item-gaussian-solve-3" data-reference-type="ref+Label" data-reference="item--gaussian-solve-3">3.</a> of <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a> applies, we again distinguish two cases:

    1.  This is the subcase $a \neq \tfrac{1}{2}$ (so $1 - 2a \neq 0$). The second row encodes $0 = 1-2a \neq 0$, a contradiction. The system has *no solution*.

    2.  This is the subcase $a = \tfrac{1}{2}$, $b = -\tfrac{1}{2}$. The second row is $0 = 0$ and vanishes. The variable $y$ is free; set $y = t$ with $t \in \mathbf{R}$. Then $x = 2 + t$, giving *infinitely many solutions*:
<div class="arithmatex" markdown="1">
\[
        \{(2+t,\, t) \mid t \in \mathbf{R}\}.
\]
</div>

*Summary.* The system has:

- a *unique solution* if and only if $a + b \neq 0$;

- *no solution* if and only if $a + b = 0$ and $a \neq \tfrac{1}{2}$;

- *infinitely many solutions* if and only if $a = \tfrac{1}{2}$ and $b = -\tfrac{1}{2}$.

*Geometric explanation.* The second equation $x - y = 2$ always defines the same line $\ell_2$ (slope $1$, passing through $(2,0)$ and $(0,-2)$). The first equation $ax + by = 1$ defines a line $\ell_1$ provided $(a,b) \neq (0,0)$; if $a = b = 0$ it reads $0 = 1$, which has no solution (this falls under sub-case 2a since $a+b=0$ and $a \neq \frac12$).

The two lines $\ell_1$ and $\ell_2$ are parallel precisely when $(a,b)$ is a scalar multiple of $(1,-1)$, i.e., $b = -a$ (equivalently $a+b=0$; in terminology introduced later, in <a href="../spaces-linear-independence/#def-linearly-independent" data-reference-type="ref+Label" data-reference="def:linearly-independent">Definition 3.49</a> the vector $(a,b)$ is called linearly dependent of $(1,1)$):

- If $a + b \neq 0$, the lines are not parallel and intersect in exactly one point: unique solution.

- If $a + b = 0$ and $a \neq \tfrac{1}{2}$, the lines are parallel but distinct: no solution.

- If $a = \tfrac{1}{2}$, $b = -\tfrac{1}{2}$, then $\ell_1$ is $\tfrac{1}{2}x - \tfrac{1}{2}y = 1$, i.e., $x - y = 2$, which is the same as $\ell_2$: infinitely many solutions.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.10</strong></p>

<span id="sol-ex-systems-1-a" label="sol--ex:systems-1-a"></span> (See <a href="../exercises-systems/#ex-systems-1-a" data-reference-type="ref+Label" data-reference="ex:systems-1-a">Exercise 2.10</a>.) The matrix associated to the system is as follows, and we bring it to reduced row echelon form:
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


<p class="env-number"><strong>Solution 2.11</strong></p>

<span id="sol-ex-systems-unique-4x5" label="sol--ex:systems-unique-4x5"></span> (See <a href="../exercises-systems/#ex-systems-unique-4x5" data-reference-type="ref+Label" data-reference="ex:systems-unique-4x5">Exercise 2.11</a>.) We apply <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>. We compute the reduced row-echelon form of the augmented matrix using Gaussian elimination (<a href="../systems-gaussian-elimination/#met-gaussian-algorithm" data-reference-type="ref+Label" data-reference="met:gaussian-algorithm">Method 2.29</a>). We subtract the first row from the third and from the fourth:
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} 2 & -1 & 1 & -1 & 1 \\ 0 & 1 & -3 & 1 & 3 \\ 0 & 2 & -5 & 2 & 5 \\ 0 & 1 & -3 & 2 & 1 \\ \end{array} \right ).
\]
</div>
We subtract twice the second row from the third, and subtract the second row from the fourth:
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} 2 & -1 & 1 & -1 & 1 \\ 0 & 1 & -3 & 1 & 3 \\ 0 & 0 & 1 & 0 & -1 \\ 0 & 0 & 0 & 1 & -2 \\ \end{array} \right ).
\]
</div>
This matrix is in row-echelon form (<a href="../systems-gaussian-elimination/#def-row-echelon-form" data-reference-type="ref+Label" data-reference="def:row-echelon-form">Definition 2.27</a>). We now eliminate the remaining non-pivot entries. We subtract the third row from the first and add three times the third row to the second:
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} 2 & -1 & 0 & -1 & 2 \\ 0 & 1 & 0 & 1 & 0 \\ 0 & 0 & 1 & 0 & -1 \\ 0 & 0 & 0 & 1 & -2 \\ \end{array} \right ).
\]
</div>
We add the fourth row to the first and subtract the fourth row from the second:
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} 2 & -1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 & 2 \\ 0 & 0 & 1 & 0 & -1 \\ 0 & 0 & 0 & 1 & -2 \\ \end{array} \right ).
\]
</div>
We add the second row to the first:
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} 2 & 0 & 0 & 0 & 2 \\ 0 & 1 & 0 & 0 & 2 \\ 0 & 0 & 1 & 0 & -1 \\ 0 & 0 & 0 & 1 & -2 \\ \end{array} \right ).
\]
</div>
Finally, we multiply the first row by $\tfrac{1}{2}$:
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} {\underline 1} & 0 & 0 & 0 & 1 \\ 0 & {\underline 1} & 0 & 0 & 2 \\ 0 & 0 & {\underline 1} & 0 & -1 \\ 0 & 0 & 0 & {\underline 1} & -2 \\ \end{array} \right ).
\]
</div>
This is the reduced row-echelon form, with all four variables $x_1, x_2, x_3, x_4$ being pivot variables (there are no free variables). The unique solution is
<div class="arithmatex" markdown="1">
\[
(x_1, x_2, x_3, x_4) = (1, 2, -1, -2).
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.12</strong></p>

<span id="sol-ex-systems-1-b" label="sol--ex:systems-1-b"></span> (See <a href="../exercises-systems/#ex-systems-1-b" data-reference-type="ref+Label" data-reference="ex:systems-1-b">Exercise 2.12</a>.) We apply <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>. The matrix associated to the system is
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


<p class="env-number"><strong>Solution 2.13</strong></p>

<span id="sol-ex-systems-param-h" label="sol--ex:systems-param-h"></span> (See <a href="../exercises-systems/#ex-systems-param-h" data-reference-type="ref+Label" data-reference="ex:systems-param-h">Exercise 2.13</a>.) By <a href="../systems-matrices/#def-matrix-to-system" data-reference-type="ref+Label" data-reference="def:matrix-to-system">Definition 2.23</a>, the augmented matrix of the system is
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cc|c} 1 & h & 4 \\ 3 & 6 & 8 \end{array} \right ).
\]
</div>
We apply <a href="../systems-gaussian-elimination/#met-gaussian-algorithm" data-reference-type="ref+Label" data-reference="met:gaussian-algorithm">Method 2.29</a>. Subtracting $3$ times row $1$ from row $2$ eliminates $x$:
<div class="arithmatex" markdown="1">
\[
\xrightarrow{R_2 - 3R_1 \to R_2}
\left ( \begin{array}{cc|c} 1 & h & 4 \\ 0 & 6-3h & -4 \end{array} \right ).
\]
</div>
We now distinguish cases depending on the value of $6 - 3h = 3(2-h)$.

1.  We consider the case $6 - 3h \neq 0$, i.e., $h \neq 2$. In this case we can divide row $2$ by $3(2-h)$:
<div class="arithmatex" markdown="1">
\[
    \xrightarrow{\tfrac{1}{3(2-h)}R_2 \to R_2}
    \left ( \begin{array}{cc|c} \underline{1} & h & 4 \\ 0 & \underline{1} & \tfrac{-4}{3(2-h)} \end{array} \right ) %.$$
    %Subtract $h$ times row~$2$ from row~$1$:
    %$$
    \xrightarrow{R_1 - hR_2 \to R_1}
    \left ( \begin{array}{cc|c} \underline{1} & 0 & \tfrac{8(3-h)}{3(2-h)} \\ 0 & \underline{1} & \tfrac{-4}{3(2-h)} \end{array} \right ).
\]
</div>
This is the reduced row-echelon form (<a href="../systems-gaussian-elimination/#def-row-echelon-form" data-reference-type="ref+Label" data-reference="def:row-echelon-form">Definition 2.27</a>). Both variables are pivot variables; by <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a> the system has the unique solution
<div class="arithmatex" markdown="1">
\[
    x = \frac{8(3-h)}{3(2-h)}, \qquad y = \frac{-4}{3(2-h)}.
\]
</div>

2.  We now consider the case $h=2$. The matrix becomes
<div class="arithmatex" markdown="1">
\[
    \left ( \begin{array}{cc|c} 1 & 2 & 4 \\ 0 & 0 & -4 \end{array} \right ).
\]
</div>
The second row encodes $0 = -4$, a contradiction. The system has *no solution*.

Thus, the system has a unique solution if $h \neq 2$, and no solution if $h = 2$.

*Geometric illustration.* The second equation $3x + 6y = 8$ always defines the fixed line $\ell_2\colon y = \tfrac{4}{3} - \tfrac{x}{2}$ (slope $-\tfrac{1}{2}$). The first equation $x + hy = 4$ defines a line $\ell_1$ with slope $-\tfrac{1}{h}$ (for $h \neq 0$); for $h = 0$ it is the vertical line $x = 4$.

For $h \neq 2$, the lines $\ell_1$ and $\ell_2$ are not parallel (their slopes differ), so they intersect in exactly one point: unique solution. For $h = 2$, both lines have slope $-\tfrac{1}{2}$; the first is $x + 2y = 4$ and the second is $x + 2y = \tfrac{8}{3}$. Since $4 \neq \tfrac{8}{3}$, the lines are parallel and distinct: no solution.

<div class="center" markdown="1">

</div>

For $h = 3$: the unique solution is $\bigl(0,\,\tfrac{4}{3}\bigr)$ (intersection of $\ell_1\colon x+3y=4$ and $\ell_2\colon 3x+6y=8$). For $h = 2$: the lines $x+2y=4$ and $3x+6y=8$ are parallel; no solution.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.14</strong></p>

<span id="sol-ex-systems-homogeneous-t" label="sol--ex:systems-homogeneous-t"></span> (See <a href="../exercises-systems/#ex-systems-homogeneous-t" data-reference-type="ref+Label" data-reference="ex:systems-homogeneous-t">Exercise 2.14</a>.) By <a href="../systems-linear-systems/#def-homogeneous-linear-system" data-reference-type="ref+Label" data-reference="def:homogeneous-linear-system">Definition 2.13</a> this is a homogeneous system; in particular the trivial solution $(x_1,x_2,x_3,x_4)=(0,0,0,0)$ always exists (<a href="../systems-linear-systems/#rem-trivial-solution" data-reference-type="ref+Label" data-reference="rem:trivial-solution">Remark 2.14</a>). (Later on, in <a href="../spaces-definition-solution-of-homogeneous/#prop-homogeneous-system-subspace" data-reference-type="ref+Label" data-reference="prop:homogeneous-system-subspace">Proposition 3.18</a>, we will observe that the solution set of a homogeneous system in four variables is a sub-vector space of $\mathbf{R}^4$).

For $t=0$, we perform Gaussian elimination similarly as in the exercises above. One has
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} 2 & 0 & 1 & 0 & 0 \\ 1 & -2 & 0 & 3 & 0 \\ 4 & -4 & 0 & 5 & 0 \end{array} \right ) \leadsto 

\left ( \begin{array}{cccc|c} {\underline 1} & 0 & 0 & -\tfrac{1}{2} & 0 \\ 0 & {\underline 1} & 0 & -\tfrac{7}{4} & 0 \\ 0 & 0 & {\underline 1} & 1 & 0 \end{array} \right ).
\]
</div>
This is the reduced row-echelon form of the above matrix. The pivot variables are $x_1, x_2, x_3$; the free variable is $x_4$. Setting $x_4 = s$ and applying <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>:
<div class="arithmatex" markdown="1">
\[
x_1 = \tfrac{1}{2}s, \quad x_2 = \tfrac{7}{4}s, \quad x_3 = -s.
\]
</div>
The solution set is $\bigl\{s\cdot\bigl(\tfrac{1}{2},\, \tfrac{7}{4},\, -1,\, 1\bigr) \mid s \in \mathbf{R}\bigr\}$.

We now consider general $t$. We swap row $1$ and row $2$ and eliminate the first column:
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} 2 & 0 & 1 & -t & 0 \\ 1 & -2 & 0 & 3 & 0 \\ 4 & -4 & t & 5 & 0 \end{array} \right )
\xrightarrow{R_1 \leftrightarrow R_2}
\left ( \begin{array}{cccc|c} 1 & -2 & 0 & 3 & 0 \\ 2 & 0 & 1 & -t & 0 \\ 4 & -4 & t & 5 & 0 \end{array} \right )
\]
</div>
<div class="arithmatex" markdown="1">
\[
\xrightarrow{\substack{R_2 - 2R_1 \to R_2 \\ R_3 - 4R_1 \to R_3}}
\left ( \begin{array}{cccc|c} 1 & -2 & 0 & 3 & 0 \\ 0 & 4 & 1 & -t-6 & 0 \\ 0 & 4 & t & -7 & 0 \end{array} \right )
\xrightarrow{R_3 - R_2 \to R_3}
\left ( \begin{array}{cccc|c} 1 & -2 & 0 & 3 & 0 \\ 0 & 4 & 1 & -t-6 & 0 \\ 0 & 0 & t-1 & t-1 & 0 \end{array} \right ).
\]
</div>
We distinguish cases depending on $t-1$.

**Case 1: $t = 1$.** Row $3$ becomes all zeros. Scaling row $2$ by $\tfrac{1}{4}$ and then eliminating:
<div class="arithmatex" markdown="1">
\[
\xrightarrow{\frac{1}{4}R_2 \to R_2}
\left ( \begin{array}{cccc|c} 1 & -2 & 0 & 3 & 0 \\ 0 & 1 & \tfrac{1}{4} & -\tfrac{7}{4} & 0 \\ 0 & 0 & 0 & 0 & 0 \end{array} \right )
\xrightarrow{R_1 + 2R_2 \to R_1}
\left ( \begin{array}{cccc|c} {\underline 1} & 0 & \tfrac{1}{2} & -\tfrac{1}{2} & 0 \\ 0 & {\underline 1} & \tfrac{1}{4} & -\tfrac{7}{4} & 0 \\ 0 & 0 & 0 & 0 & 0 \end{array} \right ).
\]
</div>
Pivot variables are $x_1, x_2$; free variables are $x_3 = s$ and $x_4 = r$. By <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>: $x_1 = -\tfrac{1}{2}s + \tfrac{1}{2}r$ and $x_2 = -\tfrac{1}{4}s + \tfrac{7}{4}r$. The solution set is
<div class="arithmatex" markdown="1">
\[
\Bigl\{s\cdot\Bigl(-\tfrac{1}{2},\,-\tfrac{1}{4},\,1,\,0\Bigr) + r\cdot\Bigl(\tfrac{1}{2},\,\tfrac{7}{4},\,0,\,1\Bigr) \;\Big|\; s,r\in\mathbf{R}\Bigr\}.
\]
</div>
We observe that we have two free variables; in terminology introduced later on (<a href="../spaces-dimension/#def-dimension" data-reference-type="ref+Label" data-reference="def:dimension">Definition 3.66</a>) we will say that the solution set is a two-dimensional subspace of $\mathbf{R}^4$.

**Case 2: $t \neq 1$.** Divide row $3$ by $t-1$, then eliminate:
<div class="arithmatex" markdown="1">
\[
\xrightarrow{\frac{1}{t-1}R_3 \to R_3}
\left ( \begin{array}{cccc|c} 1 & -2 & 0 & 3 & 0 \\ 0 & 4 & 1 & -t-6 & 0 \\ 0 & 0 & 1 & 1 & 0 \end{array} \right )
\xrightarrow{R_2 - R_3 \to R_2}
\left ( \begin{array}{cccc|c} 1 & -2 & 0 & 3 & 0 \\ 0 & 4 & 0 & -t-7 & 0 \\ 0 & 0 & 1 & 1 & 0 \end{array} \right ).
\]
</div>
Scale row $2$ by $\tfrac{1}{4}$ and eliminate column $2$:
<div class="arithmatex" markdown="1">
\[
\xrightarrow{\frac{1}{4}R_2 \to R_2}
\left ( \begin{array}{cccc|c} 1 & -2 & 0 & 3 & 0 \\ 0 & 1 & 0 & \frac{-t-7}{4} & 0 \\ 0 & 0 & 1 & 1 & 0 \end{array} \right )
\xrightarrow{R_1 + 2R_2 \to R_1}
\left ( \begin{array}{cccc|c} {\underline 1} & 0 & 0 & \frac{-1-t}{2} & 0 \\ 0 & {\underline 1} & 0 & \frac{-t-7}{4} & 0 \\ 0 & 0 & {\underline 1} & 1 & 0 \end{array} \right ).
\]
</div>
Pivot variables are $x_1, x_2, x_3$; free variable is $x_4 = s$. By <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>: $x_1 = \tfrac{1+t}{2}s$, $x_2 = \tfrac{t+7}{4}s$, $x_3 = -s$. The solution set is
<div class="arithmatex" markdown="1">
\[
\Bigl\{s\cdot\Bigl(\tfrac{1+t}{2},\,\tfrac{t+7}{4},\,-1,\,1\Bigr) \;\Big|\; s\in\mathbf{R}\Bigr\}.
\]
</div>
Unlike before, we have one free variable only, so the solution set is a one-dimensional subspace of $\mathbf{R}^4$.

*Summary.* For $t\neq 1$ the solution set is the span of a single vector (one-dimensional), while for $t=1$ it is the span of two linearly independent vectors (two-dimensional). In both cases the trivial solution, i.e., the zero vector $0$ is included.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.15</strong></p>

<span id="sol-ex-systems-homogeneous-3eqs" label="sol--ex:systems-homogeneous-3eqs"></span> (See <a href="../exercises-systems/#ex-systems-homogeneous-3eqs" data-reference-type="ref+Label" data-reference="ex:systems-homogeneous-3eqs">Exercise 2.15</a>.) By <a href="../systems-linear-systems/#def-homogeneous-linear-system" data-reference-type="ref+Label" data-reference="def:homogeneous-linear-system">Definition 2.13</a> this is a homogeneous system, so the trivial solution always exists (<a href="../systems-linear-systems/#rem-trivial-solution" data-reference-type="ref+Label" data-reference="rem:trivial-solution">Remark 2.14</a>). We form the augmented matrix and apply Gaussian elimination (<a href="../systems-gaussian-elimination/#met-gaussian-algorithm" data-reference-type="ref+Label" data-reference="met:gaussian-algorithm">Method 2.29</a>):
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} 1 & 0 & -1 & 2 & 0 \\ 0 & 1 & 2 & -2 & 0 \\ 1 & 1 & 1 & 0 & 0 \end{array} \right ).
\]
</div>
Subtract row $1$ from row $3$:
<div class="arithmatex" markdown="1">
\[
\xrightarrow{R_3 - R_1 \to R_3}
\left ( \begin{array}{cccc|c} 1 & 0 & -1 & 2 & 0 \\ 0 & 1 & 2 & -2 & 0 \\ 0 & 1 & 2 & -2 & 0 \end{array} \right ).
\]
</div>
Subtract row $2$ from row $3$:
<div class="arithmatex" markdown="1">
\[
\xrightarrow{R_3 - R_2 \to R_3}
\left ( \begin{array}{cccc|c} {\underline 1} & 0 & -1 & 2 & 0 \\ 0 & {\underline 1} & 2 & -2 & 0 \\ 0 & 0 & 0 & 0 & 0 \end{array} \right ).
\]
</div>
This is already the reduced row-echelon form (<a href="../systems-gaussian-elimination/#def-row-echelon-form" data-reference-type="ref+Label" data-reference="def:row-echelon-form">Definition 2.27</a>). The pivot variables are $x_1$ and $x_2$; the free variables are $x_3$ and $x_4$.

Setting $x_3 = s$ and $x_4 = t$ with $s, t \in \mathbf{R}$, <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a> gives
<div class="arithmatex" markdown="1">
\[
x_1 = x_3 - 2x_4 = s - 2t, \qquad x_2 = -2x_3 + 2x_4 = -2s + 2t.
\]
</div>
The solution set is
<div class="arithmatex" markdown="1">
\[
\bigl\{(s-2t,\,-2s+2t,\,s,\,t) \mid s,t\in\mathbf{R}\bigr\}
= \bigl\{s(1,-2,1,0)+t(-2,2,0,1) \mid s,t\in\mathbf{R}\bigr\}.
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.16</strong></p>

<span id="sol-ex-systems-1-d" label="sol--ex:systems-1-d"></span> (See <a href="../exercises-systems/#ex-systems-1-d" data-reference-type="ref+Label" data-reference="ex:systems-1-d">Exercise 2.16</a>.) Suppose $x_1 = 1-t$, $x_2 = 2+3t$ and $x_3 = 4t$. We have to determine whether there is some $t\in {\bf R}$ such that for these choices of $x_1, x_2, x_3$, we have a solution of the given system, i.e., whether
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


<p class="env-number"><strong>Solution 2.17</strong></p>

<span id="sol-ex-systems-unique-param-t" label="sol--ex:systems-unique-param-t"></span> (See <a href="../exercises-systems/#ex-systems-unique-param-t" data-reference-type="ref+Label" data-reference="ex:systems-unique-param-t">Exercise 2.17</a>.) We substitute $x_1 = 3+t$, $x_2 = 2+t$, $x_3 = \tfrac{2}{3}+t$ into both equations and determine for which $t \in \mathbf{R}$ both are satisfied simultaneously. We begin by considering the first equation:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x_1 - x_2 + 3x_3
&= (3+t)-(2+t)+3\!\left(\tfrac{2}{3}+t\right) \\
&= 1 + 2 + 3t \\
&= 3 + 3t.
\end{align*}
\]
</div>
Setting this equal to $0$ gives $3+3t = 0$, i.e., $t = -1$. The second equation reads
<div class="arithmatex" markdown="1">
\[
x_1 - x_2 = (3+t)-(2+t) = 1.
\]
</div>
This equals $1$ for *every* $t \in \mathbf{R}$, so the second equation imposes no restriction on $t$.

The first equation uniquely determines $t = -1$, while the second is satisfied for all $t$. Hence there is exactly one value $t = -1$ such that $(3+t, 2+t, \tfrac{2}{3}+t)$ is a solution of the system. For this value the solution vector is
<div class="arithmatex" markdown="1">
\[
(x_1, x_2, x_3) = \bigl(2,\; 1,\; -\tfrac{1}{3}\bigr).
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.18</strong></p>

<span id="sol-ex-systems-1-e" label="sol--ex:systems-1-e"></span> (See <a href="../exercises-systems/#ex-systems-1-e" data-reference-type="ref+Label" data-reference="ex:systems-1-e">Exercise 2.18</a>.) We substitute $x_1 = 1+t$, $x_2 = t+q$ and $x_3 = -t+2q+1$ into the given equation and get the equation
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
satisfies the requested conditions. (Note that these are infinitely many solutions.)

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.19</strong></p>

<span id="sol-ex-systems-1-f" label="sol--ex:systems-1-f"></span> (See <a href="../exercises-systems/#ex-systems-1-f" data-reference-type="ref+Label" data-reference="ex:systems-1-f">Exercise 2.19</a>.) We have to find $a_0, \dots, a_3$, so these are the unknowns. The conditions amount to the linear (!) system
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


<p class="env-number"><strong>Solution 2.20</strong></p>

<span id="sol-ex-systems-aug-3x5" label="sol--ex:systems-aug-3x5"></span> (See <a href="../exercises-systems/#ex-systems-aug-3x5" data-reference-type="ref+Label" data-reference="ex:systems-aug-3x5">Exercise 2.20</a>.) We apply <a href="../systems-gaussian-elimination/#met-gaussian-algorithm" data-reference-type="ref+Label" data-reference="met:gaussian-algorithm">Method 2.29</a> to the given augmented matrix. Subtracting twice the first row from the second, and subtracting the first row from the third, gives
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left ( \begin{array}{cccc|c} 1 & 1 & 2 & 3 & 1 \\ 2 & 0 & 1 & 2 & 1 \\ 1 & 3 & 5 & 7 & 2 \end{array} \right )
& \xrightarrow{R_2 \leftarrow R_2-2R_1,\; R_3 \leftarrow R_3-R_1}
\left ( \begin{array}{cccc|c} 1 & 1 & 2 & 3 & 1 \\ 0 & -2 & -3 & -4 & -1 \\ 0 & 2 & 3 & 4 & 1 \end{array} \right ) \\
%Adding the second row to the third yields a zero row:
%$$
& \xrightarrow{R_3 \leftarrow R_3+R_2}
\left ( \begin{array}{cccc|c} 1 & 1 & 2 & 3 & 1 \\ 0 & -2 & -3 & -4 & -1 \\ 0 & 0 & 0 & 0 & 0 \end{array} \right ) \\
%Multiplying the second row by $-\tfrac{1}{2}$ gives the row-echelon form (see \Cref{def:row-echelon-form}):
% $$
\xrightarrow{R_2 \leftarrow -\frac{1}{2}R_2}
\left ( \begin{array}{cccc|c} 1 & 1 & 2 & 3 & 1 \\ 0 & 1 & \tfrac{3}{2} & 2 & \tfrac{1}{2} \\ 0 & 0 & 0 & 0 & 0 \end{array} \right ).
\end{align*}
\]
</div>
This matrix is in row-echelon form (see <a href="../systems-gaussian-elimination/#def-row-echelon-form" data-reference-type="ref+Label" data-reference="def:row-echelon-form">Definition 2.27</a>). In order to get to reduced row-echelon form we continue like so:
<div class="arithmatex" markdown="1">
\[
\xrightarrow{R_1 \leftarrow R_1-R_2}
\left ( \begin{array}{cccc|c} 1 & 0 & \tfrac{1}{2} & 1 & \tfrac{1}{2} \\ 0 & 1 & \tfrac{3}{2} & 2 & \tfrac{1}{2} \\ 0 & 0 & 0 & 0 & 0 \end{array} \right ).
\]
</div>
By <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>, the pivot columns are $1$ and $2$, so $x_1$ and $x_2$ are the leading variables, while $x_3$ and $x_4$ are free variables. Setting $x_3 = s$ and $x_4 = t$ with $s, t \in {\bf R}$, the two non-trivial rows give
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x_1 &= \tfrac{1}{2} - \tfrac{1}{2}s - t, \\
x_2 &= \tfrac{1}{2} - \tfrac{3}{2}s - 2t.
\end{align*}
\]
</div>
The solution set is therefore
<div class="arithmatex" markdown="1">
\[
\left\{
\begin{pmatrix} \tfrac{1}{2} \\ \tfrac{1}{2} \\ 0 \\ 0 \end{pmatrix}
+ s \begin{pmatrix} -\tfrac{1}{2} \\ -\tfrac{3}{2} \\ 1 \\ 0 \end{pmatrix}
+ t \begin{pmatrix} -1 \\ -2 \\ 0 \\ 1 \end{pmatrix}
: s, t \in {\bf R}
\right\}.
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.21</strong></p>

<span id="sol-ex-systems-alpha-matrix" label="sol--ex:systems-alpha-matrix"></span> (See <a href="../exercises-systems/#ex-systems-alpha-matrix" data-reference-type="ref+Label" data-reference="ex:systems-alpha-matrix">Exercise 2.21</a>.) We apply <a href="../systems-gaussian-elimination/#met-gaussian-algorithm" data-reference-type="ref+Label" data-reference="met:gaussian-algorithm">Method 2.29</a> to the given augmented matrix. Subtracting twice the first row from the second, and subtracting the first row from the third, gives
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc|c} 1 & 1 & 2 & 3 & -1 \\ 2 & 0 & 1 & 2 & \alpha \\ 1 & 3 & 5 & 7 & 0 \end{array} \right )
\xrightarrow{R_2 \leftarrow R_2-2R_1,\; R_3 \leftarrow R_3-R_1}
\left ( \begin{array}{cccc|c} 1 & 1 & 2 & 3 & -1 \\ 0 & -2 & -3 & -4 & \alpha+2 \\ 0 & 2 & 3 & 4 & 1 \end{array} \right ).
\]
</div>
Adding the second row to the third:
<div class="arithmatex" markdown="1">
\[
\xrightarrow{R_3 \leftarrow R_3+R_2}
\left ( \begin{array}{cccc|c} 1 & 1 & 2 & 3 & -1 \\ 0 & -2 & -3 & -4 & \alpha+2 \\ 0 & 0 & 0 & 0 & \alpha+3 \end{array} \right ).
\]
</div>
The last row encodes the equation $0 = \alpha+3$, which requires $\alpha = -3$ for any solution to exist (compare <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>, <a href="../systems-gaussian-elimination/#item-gaussian-solve-3" data-reference-type="ref+Label" data-reference="item--gaussian-solve-3">3.</a> there).

- *Case $\alpha \neq -3$.* The last row gives the contradiction $0 = \alpha+3 \neq 0$, so the system has no solution.

- *Case $\alpha = -3$.* The last row vanishes. With $\alpha+2 = -1$, the matrix becomes
<div class="arithmatex" markdown="1">
\[
  \left ( \begin{array}{cccc|c} 1 & 1 & 2 & 3 & -1 \\ 0 & -2 & -3 & -4 & -1 \\ 0 & 0 & 0 & 0 & 0 \end{array} \right ).
\]
</div>
  Multiplying the second row by $-\tfrac{1}{2}$ and then subtracting it from the first produces the reduced row-echelon form (see <a href="../systems-gaussian-elimination/#def-row-echelon-form" data-reference-type="ref+Label" data-reference="def:row-echelon-form">Definition 2.27</a>):
<div class="arithmatex" markdown="1">
\[
  \xrightarrow{R_2 \leftarrow -\frac{1}{2}R_2}
    \left ( \begin{array}{cccc|c} 1 & 1 & 2 & 3 & -1 \\ 0 & 1 & \tfrac{3}{2} & 2 & \tfrac{1}{2} \\ 0 & 0 & 0 & 0 & 0 \end{array} \right )
    \xrightarrow{R_1 \leftarrow R_1-R_2}
    \left ( \begin{array}{cccc|c} 1 & 0 & \tfrac{1}{2} & 1 & -\tfrac{3}{2} \\ 0 & 1 & \tfrac{3}{2} & 2 & \tfrac{1}{2} \\ 0 & 0 & 0 & 0 & 0 \end{array} \right ).
\]
</div>
  By <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>, $x_1$ and $x_2$ are leading variables while $x_3 = s$ and $x_4 = t$ are free. The two non-trivial rows give
<div class="arithmatex" markdown="1">
\[
  \begin{align*}
    x_1 &= -\tfrac{3}{2} - \tfrac{1}{2}s - t, \\
    x_2 &= \tfrac{1}{2} - \tfrac{3}{2}s - 2t.
  \end{align*}
\]
</div>
  The solution set is therefore
<div class="arithmatex" markdown="1">
\[
  \left\{
    \begin{pmatrix} -\tfrac{3}{2} \\ \tfrac{1}{2} \\ 0 \\ 0 \end{pmatrix}
    + s \begin{pmatrix} -\tfrac{1}{2} \\ -\tfrac{3}{2} \\ 1 \\ 0 \end{pmatrix}
    + t \begin{pmatrix} -1 \\ -2 \\ 0 \\ 1 \end{pmatrix}
    : s, t \in {\bf R}
    \right\}.
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.22</strong></p>

<span id="sol-ex-systems-alpha-2eqs" label="sol--ex:systems-alpha-2eqs"></span> (See <a href="../exercises-systems/#ex-systems-alpha-2eqs" data-reference-type="ref+Label" data-reference="ex:systems-alpha-2eqs">Exercise 2.22</a>.) We apply <a href="../systems-gaussian-elimination/#met-gaussian-algorithm" data-reference-type="ref+Label" data-reference="met:gaussian-algorithm">Method 2.29</a> to the augmented matrix of the system. Dividing the first row by $2$ and then subtracting $(\alpha+2)$ times the first row from the second gives
<div class="arithmatex" markdown="1">
\[
\begin{align*}
  \left ( \begin{array}{ccc|c} 2 & -1 & 1 & 1 \\ \alpha+2 & -2 & \alpha & -\alpha \end{array} \right )
& \xrightarrow{R_1 \leftarrow \frac{1}{2}R_1}
\left ( \begin{array}{ccc|c} 1 & -\tfrac{1}{2} & \tfrac{1}{2} & \tfrac{1}{2} \\ \alpha+2 & -2 & \alpha & -\alpha \end{array} \right ) \\
& \xrightarrow{R_2 \leftarrow R_2 - (\alpha+2)R_1}
\left ( \begin{array}{ccc|c} 1 & -\tfrac{1}{2} & \tfrac{1}{2} & \tfrac{1}{2} \\ 0 & \tfrac{\alpha-2}{2} & \tfrac{\alpha-2}{2} & \tfrac{-3\alpha-2}{2} \end{array} \right ).
\end{align*}
\]
</div>
The second row encodes the equation $\tfrac{\alpha-2}{2}(y + z) = \tfrac{-3\alpha-2}{2}$, which forces a case split on $\alpha = 2$:

- *Case $\alpha = 2$.* The second row becomes $0 \cdot y + 0 \cdot z = -4$, i.e., $0 = -4$, a contradiction. The system has *no solution*.

- *Case $\alpha \neq 2$.* We may divide the second row by $\tfrac{\alpha-2}{2}$ and then eliminate the $-\tfrac{1}{2}$ entry in the first row (<a href="../systems-gaussian-elimination/#def-elementary-row-operations" data-reference-type="ref+Label" data-reference="def:elementary-row-operations">Definition 2.28</a>):
<div class="arithmatex" markdown="1">
\[
  \xrightarrow{R_2 \leftarrow \frac{2}{\alpha-2}R_2}
    \left ( \begin{array}{ccc|c} 1 & -\tfrac{1}{2} & \tfrac{1}{2} & \tfrac{1}{2} \\ 0 & 1 & 1 & \tfrac{-3\alpha-2}{\alpha-2} \end{array} \right )
    \xrightarrow{R_1 \leftarrow R_1 + \frac{1}{2}R_2}
    \left ( \begin{array}{ccc|c} 1 & 0 & 1 & \tfrac{-(\alpha+2)}{\alpha-2} \\ 0 & 1 & 1 & \tfrac{-3\alpha-2}{\alpha-2} \end{array} \right ).
\]
</div>
  By <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>, $z$ is free; setting $z = t$ gives
<div class="arithmatex" markdown="1">
\[
  \begin{align*}
    x &= \tfrac{-(\alpha+2)}{\alpha-2} - t, \\
    y &= \tfrac{-3\alpha-2}{\alpha-2} - t.
  \end{align*}
\]
</div>
  The system has infinitely many solutions, forming the line
<div class="arithmatex" markdown="1">
\[
  \left\{
    \begin{pmatrix} \tfrac{-(\alpha+2)}{\alpha-2} \\ \tfrac{-3\alpha-2}{\alpha-2} \\ 0 \end{pmatrix}
    + t \begin{pmatrix} -1 \\ -1 \\ 1 \end{pmatrix}
    : t \in {\bf R}
    \right\} \subset {\bf R}^3.
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.23</strong></p>

<span id="sol-ex-systems-network" label="sol--ex:systems-network"></span> (See <a href="../exercises-systems/#ex-systems-network" data-reference-type="ref+Label" data-reference="ex:systems-network">Exercise 2.23</a>.)

*Setting up the system.* Let $U, V, W, X, Y, Z \geq 0$ denote the number of cars per hour flowing through the respective streets. Since each intersection neither creates nor destroys cars, inflow must equal outflow at each node:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
A\colon &\quad U + V + X = 500, \\
B\colon &\quad U + W + Z = 400, \\
C\colon &\quad X + Y = Z + 100, \\
D\colon &\quad V = W + Y.
\end{align*}
\]
</div>
Rewriting with all unknowns on the left and forming the augmented matrix (columns ordered $U, V, W, X, Y, Z$):
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccccc|c} 1 & 1 & 0 & 1 & 0 & 0 & 500 \\ 1 & 0 & 1 & 0 & 0 & 1 & 400 \\ 0 & 0 & 0 & 1 & 1 & -1 & 100 \\ 0 & 1 & -1 & 0 & -1 & 0 & 0 \end{array} \right ).
\]
</div>

*Gaussian elimination.* We apply <a href="../systems-gaussian-elimination/#met-gaussian-algorithm" data-reference-type="ref+Label" data-reference="met:gaussian-algorithm">Method 2.29</a>. Subtracting the first row from the second eliminates $U$ from row $2$; then adding the (updated) second row to the fourth eliminates $V$ from row $4$:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\xrightarrow{R_2 \leftarrow R_2 - R_1} &
\left ( \begin{array}{cccccc|c} 1 & 1 & 0 & 1 & 0 & 0 & 500 \\ 0 & -1 & 1 & -1 & 0 & 1 & -100 \\ 0 & 0 & 0 & 1 & 1 & -1 & 100 \\ 0 & 1 & -1 & 0 & -1 & 0 & 0 \end{array} \right ) \\
\xrightarrow{R_4 \leftarrow R_4 + R_2} & 
\left ( \begin{array}{cccccc|c} 1 & 1 & 0 & 1 & 0 & 0 & 500 \\ 0 & -1 & 1 & -1 & 0 & 1 & -100 \\ 0 & 0 & 0 & 1 & 1 & -1 & 100 \\ 0 & 0 & 0 & -1 & -1 & 1 & -100 \end{array} \right ) 
% Adding the third row to the fourth yields a zero row:
%$$
\xrightarrow{R_4 \leftarrow R_4 + R_3} & 
\left ( \begin{array}{cccccc|c} 1 & 1 & 0 & 1 & 0 & 0 & 500 \\ 0 & -1 & 1 & -1 & 0 & 1 & -100 \\ 0 & 0 & 0 & 1 & 1 & -1 & 100 \\ 0 & 0 & 0 & 0 & 0 & 0 & 0 \end{array} \right ).
\end{align*}
\]
</div>
This is in row-echelon form (<a href="../systems-gaussian-elimination/#def-row-echelon-form" data-reference-type="ref+Label" data-reference="def:row-echelon-form">Definition 2.27</a>).

*Reading off the solution.* By <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>, the pivot columns are $1$, $2$, $4$, so $U$, $V$, $X$ are the non-free variables, while $W = s$, $Y = t$, $Z = r$ are free ($s, t, r \in {\bf R}$). The three non-trivial rows give
<div class="arithmatex" markdown="1">
\[
\begin{align*}
X &= 100 - t + r.
V &= 100 + s - X + Z = s + t, \\
U &= 500 - V - X = 400 - s - r. \\
\end{align*}
\]
</div>
The solution set is
<div class="arithmatex" markdown="1">
\[
\left\{
\begin{pmatrix} 400 \\ 0 \\ 0 \\ 100 \\ 0 \\ 0 \end{pmatrix}
+ s \begin{pmatrix} -1 \\ 1 \\ 1 \\ 0 \\ 0 \\ 0 \end{pmatrix}
+ t \begin{pmatrix} 0 \\ 1 \\ 0 \\ -1 \\ 1 \\ 0 \end{pmatrix}
+ r \begin{pmatrix} -1 \\ 0 \\ 0 \\ 1 \\ 0 \\ 1 \end{pmatrix}
: s, t, r \in {\bf R}
\right\} \subset {\bf R}^6,
\]
</div>
where the entries correspond to $(U, V, W, X, Y, Z)$. The physically admissible scenarios are those in which all six flow values are non-negative; these are the parameter triples $(s, t, r)$ additionally satisfying $s, t, r \geq 0$, $s + r \leq 400$, and $r - t \leq 100$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 2.24</strong></p>

<span id="sol-ex-maps-exercise-008" label="sol--ex:maps-exercise-008"></span> (See <a href="../exercises-systems/#ex-maps-exercise-008" data-reference-type="ref+Label" data-reference="ex:maps-exercise-008">Exercise 2.24</a>.) We solve, for each $\lambda\in\mathbf R$, the system by Gaussian elimination (<a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>):
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
