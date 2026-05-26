<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.1</strong></p>

<span id="sol-ex-exotic-scalar-multiplication" label="sol--ex:exotic-scalar-multiplication"></span> (See <a href="../exercises-spaces/#ex-exotic-scalar-multiplication" data-reference-type="ref+Label" data-reference="ex:exotic-scalar-multiplication">Exercise 3.1</a>.) To decide whether we get a vector space, we need to check the axioms of a vector space (<a href="../spaces-definition-solution-of-homogeneous/#def-vector-space" data-reference-type="ref+Label" data-reference="def:vector-space">Definition 3.10</a>), especially

- $(r+s)v=rv+sv$ (<a href="../spaces-definition-solution-of-homogeneous/#def-vector-space" data-reference-type="ref+Label" data-reference="def:vector-space">Definition 3.10</a><a href="../spaces-definition-solution-of-homogeneous/#item-distributive-law" data-reference-type="ref" data-reference="item--distributive law">4.</a>),

- $(rs)v=r(sv)$ (<a href="../spaces-definition-solution-of-homogeneous/#def-vector-space" data-reference-type="ref+Label" data-reference="def:vector-space">Definition 3.10</a><a href="../spaces-definition-solution-of-homogeneous/#item-multiplication-law" data-reference-type="ref" data-reference="item--multiplication.law">6.</a>),

- and $1v=v$ (item 7 in <a href="../spaces-definition-solution-of-homogeneous/#def-vector-space" data-reference-type="ref+Label" data-reference="def:vector-space">Definition 3.10</a>).

1.  $r\cdot(x,y,z)=(rx,y,rz)$. Let $v=(x,y,z)$. Then
<div class="arithmatex" markdown="1">
\[
    (r+s)\cdot v=((r+s)x,y,(r+s)z),
\]
</div>
while
<div class="arithmatex" markdown="1">
\[
    r\cdot v+s\cdot v=(rx,y,rz)+(sx,y,sz)=((r+s)x,2y,(r+s)z).
\]
</div>
In general these are different (e.g. if $y\neq 0$), so
<div class="arithmatex" markdown="1">
\[
    (r+s)v\neq rv+sv.
\]
</div>
Thus axiom <a href="../spaces-definition-solution-of-homogeneous/#def-vector-space" data-reference-type="ref+Label" data-reference="def:vector-space">Definition 3.10</a><a href="../spaces-definition-solution-of-homogeneous/#item-distributive-law" data-reference-type="ref" data-reference="item--distributive law">4.</a> fails. Hence this is *not* a vector space structure.

2.  $r\cdot(x,y,z)=(0,0,0)$. For any nonzero $v\in V$, we have $1\cdot v=(0,0,0)\neq v$. So the identity axiom $1v=v$ from <a href="../spaces-definition-solution-of-homogeneous/#def-vector-space" data-reference-type="ref+Label" data-reference="def:vector-space">Definition 3.10</a> fails. Hence this is *not* a vector space structure.

3.  $r\cdot(x,y,z)=(r^2x,r^2y,r^2z)$.

    Here, for every $v=(x,y,z)\in V$,
<div class="arithmatex" markdown="1">
\[
    1\cdot v=(1^2x,1^2y,1^2z)=(x,y,z)=v,
\]
</div>
so the axiom $1v=v$ (item 7 in <a href="../spaces-definition-solution-of-homogeneous/#def-vector-space" data-reference-type="ref+Label" data-reference="def:vector-space">Definition 3.10</a>) is satisfied. In addition, <a href="../spaces-definition-solution-of-homogeneous/#def-vector-space" data-reference-type="ref+Label" data-reference="def:vector-space">Definition 3.10</a><a href="../spaces-definition-solution-of-homogeneous/#item-multiplication-law" data-reference-type="ref" data-reference="item--multiplication.law">6.</a> does hold here. We now consider the distributivity axiom:
<div class="arithmatex" markdown="1">
\[
    (r+s)\cdot v=((r+s)^2x,(r+s)^2y,(r+s)^2z),
\]
</div>
while
<div class="arithmatex" markdown="1">
\[
    r\cdot v+s\cdot v=(r^2x,r^2y,r^2z)+(s^2x,s^2y,s^2z)=((r^2+s^2)x,(r^2+s^2)y,(r^2+s^2)z).
\]
</div>
In general these are different (e.g. $r=s=1$ and $v\neq 0$), so
<div class="arithmatex" markdown="1">
\[
    (r+s)v\neq rv+sv.
\]
</div>
Hence <a href="../spaces-definition-solution-of-homogeneous/#def-vector-space" data-reference-type="ref+Label" data-reference="def:vector-space">Definition 3.10</a><a href="../spaces-definition-solution-of-homogeneous/#item-distributive-law" data-reference-type="ref" data-reference="item--distributive law">4.</a> fails, so this is *not* a vector space structure.

Therefore, in all three cases, $V$ is *not* a vector space.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.2</strong></p>

<span id="sol-ex-subspace-statements" label="sol--ex:subspace-statements"></span> (See <a href="../exercises-spaces/#ex-subspace-statements" data-reference-type="ref+Label" data-reference="ex:subspace-statements">Exercise 3.2</a>.) Recall <a href="../spaces-definition-solution-of-homogeneous/#def-subspace" data-reference-type="ref+Label" data-reference="def:subspace">Definition 3.17</a>: a subspace $V \subset {\bf R}^2$ must (i) contain the zero vector, (ii) be closed under addition, and (iii) be closed under scalar multiplication.

1.  *Correct.* By condition (i), $V$ contains the zero vector $(0,0)$, so $V$ contains at least one element.

2.  *Incorrect.* The trivial subspace $V = \{(0,0)\}$ is a subspace of ${\bf R}^2$ (all three conditions are satisfied) and contains exactly one element.

3.  *Correct.* Condition (i) of <a href="../spaces-definition-solution-of-homogeneous/#def-subspace" data-reference-type="ref+Label" data-reference="def:subspace">Definition 3.17</a> states that the zero vector must belong to $V$.

4.  *Correct.* Let $v, w \in V$. By condition (iii), $(-1) \cdot w \in V$, i.e. $-w \in V$. Then by condition (ii), $v + (-w) = v - w \in V$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.3</strong></p>

<span id="sol-differentiable-functions" label="sol--differentiable functions"></span> (See <a href="../exercises-spaces/#differentiable-functions" data-reference-type="ref+Label" data-reference="differentiable functions">Exercise 3.3</a>.) Let $D := \{ f : {\bf R} \to {\bf R} \mid f \text{ is differentiable} \}$, with sum and scalar multiple as in <a href="../spaces-further-examples/#sum-functions" data-reference-type="eqref" data-reference="sum functions">Equation (3.23)</a> and <a href="../spaces-further-examples/#scalar-multiple-functions" data-reference-type="eqref" data-reference="scalar multiple functions">Equation (3.24)</a>. Following the structure of <a href="../spaces-further-examples/#dlm-polynomials-vector-space" data-reference-type="ref+Label" data-reference="dlm:polynomials-vector-space">Definition and Lemma 3.22</a>, we check the conditions of being a subvector space of the space of *all* functions $f : {\bf R} \to {\bf R}$. We note that the space of all functions does form a vector space. Its vector space axioms (commutativity and associativity of addition, distributivity, etc.) are inherited pointwise from ${\bf R}$: for any $x \in {\bf R}$, the values $f(x), g(x), h(x)$ are real numbers satisfying all these properties, hence so do the functions $f, g, h$.

We verify the conditions of <a href="../spaces-definition-solution-of-homogeneous/#def-subspace" data-reference-type="ref+Label" data-reference="def:subspace">Definition 3.17</a>, thereby confirming that $D$ is a vector space.

- *Closure under addition.* If $f, g \in D$, then both $f$ and $g$ are differentiable. By the sum rule from calculus, $f + g$ is differentiable with $(f+g)' = f' + g'$. Hence $f + g \in D$.

- *Closure under scalar multiplication.* If $f \in D$ and $r \in {\bf R}$, then by the constant multiple rule, $rf$ is differentiable with $(rf)' = r f'$. Hence $rf \in D$.

- *Zero vector.* The zero vector is the zero function $f(x) = 0$, which is differentiable (with derivative $0$), so $0 \in D$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.4</strong></p>

<span id="sol-ex-union-subspaces" label="sol--ex:union-subspaces"></span> (See <a href="../exercises-spaces/#ex-union-subspaces" data-reference-type="ref+Label" data-reference="ex:union-subspaces">Exercise 3.4</a>.) *Union that is not a subspace.* Take $V = L((1,0))$ (the $x$-axis) and $W = L((0,1))$ (the $y$-axis). Both are subspaces of ${\bf R}^2$. We have $(1,0) \in V \subset V \cup W$ and $(0,1) \in W \subset V \cup W$, but
<div class="arithmatex" markdown="1">
\[
(1,0) + (0,1) = (1,1) \notin V \cup W,
\]
</div>
since $(1,1)$ is not a scalar multiple of $(1,0)$ and not a scalar multiple of $(0,1)$. Hence $V \cup W$ is not closed under addition, so it is not a subspace.

*Union that is a subspace.* Take $V = \{(0,0)\}$ (the trivial subspace) and $W$ any subspace of ${\bf R}^2$. Then $V \cup W = W$, which is a subspace. Another possibility is to take $V = W$ for any subspace $V$, or also to take $V = \bf R^2$ and any subspace $W \subset \bf R^2$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.5</strong></p>

<span id="sol-ex-span-r4" label="sol--ex:span-r4"></span> (See <a href="../exercises-spaces/#ex-span-r4" data-reference-type="ref+Label" data-reference="ex:span-r4">Exercise 3.5</a>.) By definition of the span (<a href="../spaces-linear-combinations/#lem-span-subspace" data-reference-type="ref+Label" data-reference="lem:span-subspace">Lemma 3.34</a>), in each case we need to solve $\lambda_1 v_1 + \lambda_2 v_2 = w$. Then $w$ lies in the span of $v_1$ and $v_2$ precisely if there is a solution $(\lambda_1, \lambda_2)$ of that system.

1.  $w=(2,-1,0,1)$, $v_1=(1,0,0,1)$, $v_2=(0,1,0,1)$. Inspecting the four components of the equation $\lambda_1 v_1 + \lambda_2 v_2 = w$ we get the linear system
<div class="arithmatex" markdown="1">
\[
    \lambda_1 = 2, \quad \lambda_2 = -1, \quad 0 = 0, \quad \lambda_1 + \lambda_2 = 1.
\]
</div>
The last equation: $2 + (-1) = 1$ holds. The system is consistent, so $w \in L(v_1, v_2)$ with, namely $w = 2v_1 - v_2$.

2.  For $w=(1,2,15,11)$, $v_1=(2,-1,0,2)$, $v_2=(1,-1,-3,1)$. The system $\lambda_1 v_1 + \lambda_2 v_2 = w$ is:
<div class="arithmatex" markdown="1">
\[
    \begin{align*}
    2\lambda_1 + \lambda_2  &= 1,  \\
    -\lambda_1 - \lambda_2  &= 2,  \\
    -3\lambda_2             &= 15, \\
    2\lambda_1 + \lambda_2  &= 11.
    \end{align*}
\]
</div>
Equation (3) gives $\lambda_2 = -5$; equation (1) then gives $\lambda_1 = 3$. But equation (4) requires $2(3)+(-5)=1\neq 11$. The system is inconsistent, so $w \notin L(v_1,v_2)$.

3.  $w=(2,5,8,3)$, $v_1=(2,-1,0,5)$, $v_2=(-1,2,2,-3)$.

    The system $\lambda_1 v_1 + \lambda_2 v_2 = w$ is:
<div class="arithmatex" markdown="1">
\[
    \begin{align*}
    2\lambda_1 - \lambda_2  &= 2, \\
    -\lambda_1 + 2\lambda_2 &= 5, \\
    2\lambda_2              &= 8, \\
    5\lambda_1 - 3\lambda_2 &= 3.
    \end{align*}
\]
</div>
One solves this similarly as above and finds that the system has the solution $\lambda_1 = 3$, $\lambda_2 = 4$. Hence $w \in L(v_1, v_2)$ with
<div class="arithmatex" markdown="1">
\[
    w = 3v_1 + 4v_2.
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.6</strong></p>

<span id="sol-ex-spanning-r4" label="sol--ex:spanning-r4"></span> (See <a href="../exercises-spaces/#ex-spanning-r4" data-reference-type="ref+Label" data-reference="ex:spanning-r4">Exercise 3.6</a>.) By <a href="../spaces-dimension/#cor-indep-span" data-reference-type="ref+Label" data-reference="cor:indep-span">Corollary 3.73</a>, four vectors in ${\bf R}^4$ span ${\bf R}^4$ if and only if they are linearly independent, which by <a href="../spaces-linear-independence/#met-check-linear-independence" data-reference-type="ref+Label" data-reference="met:check-linear-independence">Method 3.56</a> is equivalent to the matrix formed by the vectors (as rows) having rank 4 after Gaussian elimination (<a href="../systems-gaussian-elimination/#met-gaussian-algorithm" data-reference-type="ref+Label" data-reference="met:gaussian-algorithm">Method 2.29</a>).

1.  Form the matrix with rows $(1,1,1,1)$, $(0,1,1,1)$, $(0,0,1,1)$, $(0,0,0,1)$:
<div class="arithmatex" markdown="1">
\[
    \begin{pmatrix} 1&1&1&1 \\ 0&1&1&1 \\ 0&0&1&1 \\ 0&0&0&1 \end{pmatrix}.
\]
</div>
This matrix is already in row-echelon form (<a href="../systems-gaussian-elimination/#def-row-echelon-form" data-reference-type="ref+Label" data-reference="def:row-echelon-form">Definition 2.27</a>) with 4 pivot rows, so its rank equals 4. Hence the four vectors are linearly independent and *do span* ${\bf R}^4$.

2.  Form the matrix with rows $(1,3,-5,0)$, $(-2,1,0,0)$, $(0,2,1,-1)$, $(1,-4,5,0)$ and apply elementary row operations (<a href="../systems-gaussian-elimination/#def-elementary-row-operations" data-reference-type="ref+Label" data-reference="def:elementary-row-operations">Definition 2.28</a>):
<div class="arithmatex" markdown="1">
\[
    \begin{pmatrix} 1&3&-5&0 \\ -2&1&0&0 \\ 0&2&1&-1 \\ 1&-4&5&0 \end{pmatrix}
    \xrightarrow{R_2+2R_1,\; R_4-R_1}
    \begin{pmatrix} 1&3&-5&0 \\ 0&7&-10&0 \\ 0&2&1&-1 \\ 0&-7&10&0 \end{pmatrix}
    \xrightarrow{R_4+R_2}
    \begin{pmatrix} 1&3&-5&0 \\ 0&7&-10&0 \\ 0&2&1&-1 \\ 0&0&0&0 \end{pmatrix}
    \xrightarrow{7R_3-2R_2}
    \begin{pmatrix} 1&3&-5&0 \\ 0&7&-10&0 \\ 0&0&27&-7 \\ 0&0&0&0 \end{pmatrix}.
\]
</div>
The resulting row-echelon matrix has only 3 non-zero rows, so the rank equals 3 $< 4$. Hence the four vectors are linearly dependent and *do not span* ${\bf R}^4$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.7</strong></p>

<span id="sol-ex-linear-independence" label="sol--ex:linear-independence"></span> (See <a href="../exercises-spaces/#ex-linear-independence" data-reference-type="ref+Label" data-reference="ex:linear-independence">Exercise 3.7</a>.) By <a href="../spaces-linear-independence/#def-linearly-independent" data-reference-type="ref+Label" data-reference="def:linearly-independent">Definition 3.49</a> and <a href="../spaces-linear-independence/#met-check-linear-independence" data-reference-type="ref+Label" data-reference="met:check-linear-independence">Method 3.56</a>, we form the matrix with the given vectors as rows and apply Gaussian elimination (<a href="../systems-gaussian-elimination/#met-gaussian-algorithm" data-reference-type="ref+Label" data-reference="met:gaussian-algorithm">Method 2.29</a>, <a href="../systems-gaussian-elimination/#def-elementary-row-operations" data-reference-type="ref+Label" data-reference="def:elementary-row-operations">Definition 2.28</a>). The vectors are linearly independent if and only if the resulting row-echelon matrix (<a href="../systems-gaussian-elimination/#def-row-echelon-form" data-reference-type="ref+Label" data-reference="def:row-echelon-form">Definition 2.27</a>) has no zero rows.

1.  $v_1=(1,-1,0)$, $v_2=(3,2,-1)$, $v_3=(3,5,-2)$ in ${\bf R}^3$:
<div class="arithmatex" markdown="1">
\[
    \begin{pmatrix} 1&-1&0 \\ 3&2&-1 \\ 3&5&-2 \end{pmatrix}
    \xrightarrow{R_2-3R_1,\; R_3-3R_1}
    \begin{pmatrix} 1&-1&0 \\ 0&5&-1 \\ 0&8&-2 \end{pmatrix}
    \xrightarrow{5R_3-8R_2}
    \begin{pmatrix} 1&-1&0 \\ 0&5&-1 \\ 0&0&-2 \end{pmatrix}.
\]
</div>
There is no zero row, so the vectors are *linearly independent*.

2.  $v_1=(1,1,1)$, $v_2=(1,-1,1)$, $v_3=(0,0,1)$ in ${\bf R}^3$:
<div class="arithmatex" markdown="1">
\[
    \begin{pmatrix} 1&1&1 \\ 1&-1&1 \\ 0&0&1 \end{pmatrix}
    \xrightarrow{R_2-R_1}
    \begin{pmatrix} 1&1&1 \\ 0&-2&0 \\ 0&0&1 \end{pmatrix}.
\]
</div>
Again, there is no zero row, so the vectors are *linearly independent*.

3.  
<div class="arithmatex" markdown="1">
\[
    \begin{pmatrix} 1&-1&1&-1 \\ 2&0&1&0 \\ 0&-2&1&-2 \end{pmatrix}
    \xrightarrow{R_2-2R_1}
    \begin{pmatrix} 1&-1&1&-1 \\ 0&2&-1&2 \\ 0&-2&1&-2 \end{pmatrix}
    \xrightarrow{R_3+R_2}
    \begin{pmatrix} 1&-1&1&-1 \\ 0&2&-1&2 \\ 0&0&0&0 \end{pmatrix}.
\]
</div>
The presence of the zero row at the en means that the vectors are *linearly dependent*.

4.  $(1,1,0,0)$, $(1,0,1,0)$, $(0,0,1,1)$, $(0,1,0,1)$ in ${\bf R}^4$:
<div class="arithmatex" markdown="1">
\[
    \begin{pmatrix} 1&1&0&0 \\ 1&0&1&0 \\ 0&0&1&1 \\ 0&1&0&1 \end{pmatrix}
    \xrightarrow{R_2-R_1}
    \begin{pmatrix} 1&1&0&0 \\ 0&-1&1&0 \\ 0&0&1&1 \\ 0&1&0&1 \end{pmatrix}
    \xrightarrow{R_4+R_2}
    \begin{pmatrix} 1&1&0&0 \\ 0&-1&1&0 \\ 0&0&1&1 \\ 0&0&1&1 \end{pmatrix}
    \xrightarrow{R_4-R_3}
    \begin{pmatrix} 1&1&0&0 \\ 0&-1&1&0 \\ 0&0&1&1 \\ 0&0&0&0 \end{pmatrix}.
\]
</div>
Again, the vectors are *linearly dependent*.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.8</strong></p>

<span id="sol-ex-three-vectors-r2" label="sol--ex:three-vectors-r2"></span> (See <a href="../exercises-spaces/#ex-three-vectors-r2" data-reference-type="ref+Label" data-reference="ex:three-vectors-r2">Exercise 3.8</a>.) Since $\dim {\bf R}^2 = 2$, any three vectors in ${\bf R}^2$ are automatically linearly dependent: by <a href="../spaces-dimension/#thm-basis-theorem" data-reference-type="ref+Label" data-reference="thm:basis-theorem">Theorem 3.71</a><a href="../spaces-dimension/#item-independent-add" data-reference-type="ref" data-reference="item--independent.add">2.</a>, a linearly independent set can have at most $\dim V = 2$ elements, so the last condition of the exercise is satisfied for *any* choice of three vectors in ${\bf R}^2$. It therefore suffices to find three vectors that are pairwise linearly independent. By <a href="../spaces-linear-independence/#def-linearly-independent" data-reference-type="ref+Label" data-reference="def:linearly-independent">Definition 3.49</a>, two vectors are linearly independent if and only if neither is a scalar multiple of the other. A natural starting point is $v_1 = (1,0)$ and $v_2 = (0,1)$ (the standard basis vectors, clearly not scalar multiples of each other). For $v_3$ we need a vector that is not a scalar multiple of $v_1$ or of $v_2$; one such choice is $v_3 = v_1 + v_2 = (1,1)$, which also makes the dependence relation among the triple transparent.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.9</strong></p>

<span id="sol-ex-polynomial-subspaces" label="sol--ex:polynomial-subspaces"></span> (See <a href="../exercises-spaces/#ex-polynomial-subspaces" data-reference-type="ref+Label" data-reference="ex:polynomial-subspaces">Exercise 3.9</a>.) We check the three conditions of <a href="../spaces-definition-solution-of-homogeneous/#def-subspace" data-reference-type="ref+Label" data-reference="def:subspace">Definition 3.17</a> for each subset of $V = {\bf R}[x]^{\le 3}$ (<a href="../spaces-further-examples/#dlm-polynomials-vector-space" data-reference-type="ref+Label" data-reference="dlm:polynomials-vector-space">Definition and Lemma 3.22</a>).

1.  $S_1 = \{ f \in V \mid f(2) = 1 \}$. is *not* a subspace since the zero polynomial satisfies $0(2) = 0 \neq 1$, so $0 \notin S_1$. Condition (1) of <a href="../spaces-definition-solution-of-homogeneous/#def-subspace" data-reference-type="ref+Label" data-reference="def:subspace">Definition 3.17</a> fails.

2.  $S_2 = \{ x \cdot f \mid f \in {\bf R}[x]^{\le 2} \}$ is a subspace. Writing $f = a_0 + a_1 x + a_2 x^2$, we get $xf = a_0 x + a_1 x^2 + a_2 x^3$, so $S_2 = L(x, x^2, x^3)$. By <a href="../spaces-linear-combinations/#lem-span-subspace" data-reference-type="ref+Label" data-reference="lem:span-subspace">Lemma 3.34</a>, every span is a subspace.

3.  $S_3 = \{ x \cdot f + (1-x) \cdot g \mid f, g \in {\bf R}[x]^{\le 2} \}$ also *is a subspace.* We verify <a href="../spaces-definition-solution-of-homogeneous/#def-subspace" data-reference-type="ref+Label" data-reference="def:subspace">Definition 3.17</a> directly:

    - $0 \in S_3$: take $f = g = 0$.

    - Closure under addition: $(xf_1 + (1-x)g_1) + (xf_2 + (1-x)g_2) = x(f_1+f_2) + (1-x)(g_1+g_2) \in S_3$.

    - Closure under scalar multiplication: $c(xf + (1-x)g) = x(cf) + (1-x)(cg) \in S_3$.

    (In fact one has $S_3 = V$: writing $xf + (1-x)g = g + x(f-g)$, any $h \in V$ can be achieved by choosing $g$ as the constant-through-degree-2 part and $f-g$ as needed.)

4.  $S_4 = \{ f \in {\bf R}[x]^{\le 3} \mid f(0) = 0 \}$. *Is a subspace.* We verify <a href="../spaces-definition-solution-of-homogeneous/#def-subspace" data-reference-type="ref+Label" data-reference="def:subspace">Definition 3.17</a>:

    - $0 \in S_4$: $0(0) = 0$ holds true.

    - Closure under addition: $(f+g)(0) = f(0) + g(0) = 0 + 0 = 0$, so $f + g \in S_4$ for $f, g \in S_4$.

    - Closure under scalar multiplication: $(cf)(0) = c \cdot f(0) = 0$.

    (Equivalently, $f(0)=0$ means the constant term of $f$ is zero, so $S_4 = L(x, x^2, x^3)$.)

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.10</strong></p>

<span id="sol-ex-poly-span-1" label="sol--ex poly span 1"></span> (See <a href="../exercises-spaces/#ex-poly-span-1" data-reference-type="ref+Label" data-reference="ex poly span 1">Exercise 3.10</a>.) We seek $a, b, c \in {\bf R}$ such that $a(x+1) + b(x-1) + c(x^2-1) = p(x)$ (<a href="../spaces-linear-combinations/#def-spaces-definition-008" data-reference-type="ref+Label" data-reference="def:spaces-definition-008">Definition 3.31</a>). Expanding the left side and collecting by degree:
<div class="arithmatex" markdown="1">
\[
a(x+1) + b(x-1) + c(x^2-1) = cx^2 + (a+b)x + (a-b-c).
\]
</div>
Thus, if $p(x) = p_2 x^2 + p_1 x + p_0$, then we need $c = p_2$, $a+b = p_1$, and $a-b-c = p_0$. I.e. $a = \tfrac{1}{2}(p_1 + p_0 + c)$ and $b = \tfrac{1}{2}(p_1 - p_0 - c)$. This leads to the following expressions for $p$ as a linear combination of the three given polynomials:

1.  
<div class="arithmatex" markdown="1">
\[
    x^2+4x-2 = \tfrac{3}{2}(x+1) + \tfrac{5}{2}(x-1) + (x^2-1).
\]
</div>

2.  
<div class="arithmatex" markdown="1">
\[
    x = \tfrac{1}{2}(x+1) + \tfrac{1}{2}(x-1).
\]
</div>

3.  
<div class="arithmatex" markdown="1">
\[
    40-x^2 = \tfrac{39}{2}(x+1) - \tfrac{39}{2}(x-1) - (x^2-1).
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.11</strong></p>

<span id="sol-ex-poly-span-2" label="sol--ex poly span 2"></span> (See <a href="../exercises-spaces/#ex-poly-span-2" data-reference-type="ref+Label" data-reference="ex poly span 2">Exercise 3.11</a>.) The sentence is *incorrect*, since the coefficient $\tfrac{x}{4}$ is *not* a scalar. By <a href="../spaces-linear-combinations/#def-spaces-definition-008" data-reference-type="ref+Label" data-reference="def:spaces-definition-008">Definition 3.31</a>, a linear combination of vectors $v_1, \dots, v_m$ is an expression $a_1 v_1 + \dots + a_m v_m$ where the coefficients $a_i$ are *real numbers*. The expression $\tfrac{x}{4} \cdot x^2 + 3 \cdot x + 1$ uses $\tfrac{x}{4}$ as the coefficient of $x^2$, but $\tfrac{x}{4}$ is a polynomial in $x$, not a real number. It is therefore not a valid scalar coefficient.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.12</strong></p>

<span id="sol-base-change-matrix" label="sol--base change matrix"></span> (See <a href="../exercises-spaces/#base-change-matrix" data-reference-type="ref+Label" data-reference="base change matrix">Exercise 3.12</a>.) From <a href="../spaces-bases/#ex-three-vectors-basis" data-reference-type="ref+Label" data-reference="ex:three-vectors-basis">Example 3.63</a> the basis is $v_1=(0,2,1)$, $v_2=(1,0,2)$, $v_3=(-1,1,1)$. We seek coefficients $\alpha_i,\beta_i,\gamma_i$ with $e_i = \alpha_i v_1 + \beta_i v_2 + \gamma_i v_3$ for each $i$ (<a href="../spaces-bases/#def-basis" data-reference-type="ref+Label" data-reference="def:basis">Definition 3.61</a>, <a href="../spaces-linear-combinations/#def-spaces-definition-008" data-reference-type="ref+Label" data-reference="def:spaces-definition-008">Definition 3.31</a>). All three systems share the same coefficient matrix (columns $v_1,v_2,v_3$), so we row-reduce the augmented matrix $[v_1 \ v_2 \  v_3 \mid e_1 \  e_2 \ e_3]$ in one pass (<a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>):
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left ( \begin{array}{ccc|ccc} 0 & 1 & -1 & 1 & 0 & 0 \\ 2 & 0 & 1 & 0 & 1 & 0 \\ 1 & 2 & 1 & 0 & 0 & 1 \end{array} \right )
&\xrightarrow{R_1 \leftrightarrow R_3}
\left ( \begin{array}{ccc|ccc} 1 & 2 & 1 & 0 & 0 & 1 \\ 2 & 0 & 1 & 0 & 1 & 0 \\ 0 & 1 & -1 & 1 & 0 & 0 \end{array} \right ) \\
&\xrightarrow{R_2 - 2R_1}
\left ( \begin{array}{ccc|ccc} 1 & 2 & 1 & 0 & 0 & 1 \\ 0 & -4 & -1 & 0 & 1 & -2 \\ 0 & 1 & -1 & 1 & 0 & 0 \end{array} \right ) \\
&\xrightarrow{4R_3 + R_2}
\left ( \begin{array}{ccc|ccc} 1 & 2 & 1 & 0 & 0 & 1 \\ 0 & -4 & -1 & 0 & 1 & -2 \\ 0 & 0 & -5 & 4 & 1 & -2 \end{array} \right ).
\end{align*}
\]
</div>
Back-substituting ($R_3 \div (-5)$, then $R_2$, then $R_1$) yields the reduced form
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc|ccc} 1 & 0 & 0 & \tfrac{2}{5} & \tfrac{3}{5} & -\tfrac{1}{5} \\[2pt] 0 & 1 & 0 & \tfrac{1}{5} & -\tfrac{1}{5} & \tfrac{2}{5} \\[2pt] 0 & 0 & 1 & -\tfrac{4}{5} & -\tfrac{1}{5} & \tfrac{2}{5} \end{array} \right ).
\]
</div>
(In terminology that will be introduced later on, the right hand part of the above matrix is a so-called *base change matrix* from the basis $v_1,v_2,v_3$ to the standard basis $e_1,e_2,e_3$, see <a href="../maps-change-of-basis/#ex-base-change-matrix" data-reference-type="ref+Label" data-reference="ex:base-change-matrix">Example 4.85</a>.) Reading off the right-hand columns:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
e_1 &= \tfrac{2}{5}\,v_1 + \tfrac{1}{5}\,v_2 - \tfrac{4}{5}\,v_3, \\
e_2 &= \tfrac{3}{5}\,v_1 - \tfrac{1}{5}\,v_2 - \tfrac{1}{5}\,v_3, \\
e_3 &= -\tfrac{1}{5}\,v_1 + \tfrac{2}{5}\,v_2 + \tfrac{2}{5}\,v_3.
\end{align*}
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.13</strong></p>

<span id="sol-ex-spaces-2-1" label="sol--ex:spaces-2-1"></span> (See <a href="../exercises-spaces/#ex-spaces-2-1" data-reference-type="ref+Label" data-reference="ex:spaces-2-1">Exercise 3.13</a>.) A linear combination of $A$ and $B$ is of the form
<div class="arithmatex" markdown="1">
\[
\alpha A + \beta B = \alpha \left ( \begin{array}{cc} 1 & 1 \\ 2 & 2 \end{array} \right ) + \beta \left ( \begin{array}{cc} 3 & 2 \\ 3 & 5 \end{array} \right )
\]
</div>
with $\alpha, \beta \in {\bf R}$. Computing the left hand side, we need to find $\alpha$ and $\beta$ such that
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cc} \alpha & \alpha \\ 2 \alpha & 2 \alpha \end{array} \right ) + \left ( \begin{array}{cc} 3 \beta & 2 \beta \\ 3 \beta & 5 \beta \end{array} \right ) = \left ( \begin{array}{cc} \alpha + 3\beta & \alpha + 2 \beta \\ 2\alpha+3\beta & 2\alpha+5\beta \end{array} \right ) = \left ( \begin{array}{cc} -1 & 0 \\ 2 & 4 \end{array} \right ).
\]
</div>
Comparing the entries of the matrix, this gives the linear system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\alpha + 3 \beta & = -1 \\
\alpha + 2 \beta & = 0\\
2\alpha + 3\beta & = 2\\
2\alpha + 5 \beta & = 4.
\end{align*}
\]
</div>
The second gives $\alpha = -2\beta$, inserting into the first gives $-2 \beta+3 \beta = -1$, which means $\beta = -1$. However, inserting into the third equation gives $-4\beta + 3 \beta = 2$, so that $\beta = -2$, contradicting the previous equation. Thus, there is no solution, so $C$ is *not* a linear combination of $A$ and $B$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.14</strong></p>

<span id="sol-ex-matrix-subspace" label="sol--ex:matrix-subspace"></span> (See <a href="../exercises-spaces/#ex-matrix-subspace" data-reference-type="ref+Label" data-reference="ex:matrix-subspace">Exercise 3.14</a>.)

1.  *$T$ is a subspace.* The two defining constraints
<div class="arithmatex" markdown="1">
\[
    x_1 + x_4 + x_6 = 0, \qquad x_1 + x_4 + x_3 + x_5 = 0
\]
</div>
are homogeneous linear equations in the six entries of the matrix (<a href="../systems-linear-systems/#def-homogeneous-linear-system" data-reference-type="ref+Label" data-reference="def:homogeneous-linear-system">Definition 2.13</a>). Identifying $\mathrm{Mat}_{2\times3}$ with ${\bf R}^6$, $T$ is the solution set of a homogeneous linear system, hence a subspace by <a href="../spaces-definition-solution-of-homogeneous/#prop-homogeneous-system-subspace" data-reference-type="ref+Label" data-reference="prop:homogeneous-system-subspace">Proposition 3.18</a>.

2.  *All matrices in $T$.* Solving the two equations for the dependent variables (<a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>):
<div class="arithmatex" markdown="1">
\[
    x_6 = -x_1 - x_4, \qquad x_5 = -x_1 - x_4 - x_3.
\]
</div>
The free variables are $x_1, x_2, x_3, x_4$. Setting $x_1=a$, $x_2=b$, $x_3=c$, $x_4=d$ gives
<div class="arithmatex" markdown="1">
\[
    T = \left\{ \begin{pmatrix} a & b & c \\ d & -a-d-c & -a-d \end{pmatrix} \;\middle|\; a,b,c,d \in {\bf R} \right\}.
\]
</div>

3.  *Spanning set.* Separating the four free parameters:
<div class="arithmatex" markdown="1">
\[
    \begin{align*}
    \begin{pmatrix} a & b & c \\ d & -a-d-c & -a-d \end{pmatrix}
    = a\,v_1 + b\,v_2 + c\,v_3 + d\,v_4,
    \end{align*}
\]
</div>
where
<div class="arithmatex" markdown="1">
\[
    v_1 = \begin{pmatrix} 1 & 0 & 0 \\ 0 & -1 & -1 \end{pmatrix}, \quad
    v_2 = \begin{pmatrix} 0 & 1 & 0 \\ 0 &  0 &  0 \end{pmatrix}, \quad
    v_3 = \begin{pmatrix} 0 & 0 & 1 \\ 0 & -1 &  0 \end{pmatrix}, \quad
    v_4 = \begin{pmatrix} 0 & 0 & 0 \\ 1 & -1 & -1 \end{pmatrix}.
\]
</div>
Hence $T = L(v_1, v_2, v_3, v_4)$ (<a href="../spaces-linear-combinations/#lem-span-subspace" data-reference-type="ref+Label" data-reference="lem:span-subspace">Lemma 3.34</a>). These four matrices are linearly independent (each has a non-zero entry in a position where the others are zero), so they also form a basis of $T$ with $\dim T = 4$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.15</strong></p>

<span id="sol-ex-spaces-2-2" label="sol--ex:spaces-2-2"></span> (See <a href="../exercises-spaces/#ex-spaces-2-2" data-reference-type="ref+Label" data-reference="ex:spaces-2-2">Exercise 3.15</a>.) The system $x + y + z+t=0$ corresponds to the matrix
<div class="arithmatex" markdown="1">
\[
( 1 \ 1 \ 1 \ 1 ).
\]
</div>
This matrix is already in reduced row echelon form (<a href="../systems-gaussian-elimination/#def-row-echelon-form" data-reference-type="ref+Label" data-reference="def:row-echelon-form">Definition 2.27</a>): the leading one is for the variable $x$, the variables $y, z, t$ are free variables. Thus,
<div class="arithmatex" markdown="1">
\[
S = \{(-\alpha - \beta - \gamma , \alpha, \beta, \gamma) \ | \ \alpha, \beta, \gamma \in {\bf R} \}.
\]
</div>
We have
<div class="arithmatex" markdown="1">
\[
\begin{align*}
S & = \{(-\alpha, \alpha, 0,0) + (-\beta, 0, \beta, 0) + (-\gamma, 0, 0, \gamma) \ | \ \alpha, \beta, \gamma \in {\bf R}\}  \\
& = \{\alpha(-1, 1, 0,0) + \beta (-1, 0, 1, 0) + \gamma(-1, 0, 0, 1) \ | \ \alpha, \beta, \gamma \in {\bf R}\}  \\
& = L((-1,1,0,0), (-1,0,1,0), (-1,0,0,1)).
\end{align*}
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.16</strong></p>

<span id="sol-ex-spaces-2-3" label="sol--ex:spaces-2-3"></span> (See <a href="../exercises-spaces/#ex-spaces-2-3" data-reference-type="ref+Label" data-reference="ex:spaces-2-3">Exercise 3.16</a>.) By definition (cf. <a href="../spaces-linear-combinations/#lem-span-subspace" data-reference-type="ref+Label" data-reference="lem:span-subspace">Lemma 3.34</a>), $S$ consists of all the linear combinations of the three given vectors. These can be written as
<div class="arithmatex" markdown="1">
\[
a (1,-1,0,1) + b(2,1,-2,0)+c(0,0,1,1) = (a+2b,-a+b,-2b+c,a+c)
\]
</div>
for arbitrary $a,b,c \in {\bf R}$. The intersection (cf. <a href="../spaces-intersection/#lem-spaces-lemma-003" data-reference-type="ref+Label" data-reference="lem:spaces-lemma-003">Lemma 3.19</a>) is given by vectors as above satisfying the linear system determining $T$, i.e.,
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x_1 &= a+2b\\
x_2 & = -a+b \\
x_3 &= -2b+c \\
x_4 & = a+c
\end{align*}
\]
</div>
such that
<div class="arithmatex" markdown="1">
\[
\begin{align*}
2(a+2b)-(-a+b)-3(a+c) & = 0\\
2(a+2b)+(-2b+c)+(a+c) & = 0.
\end{align*}
\]
</div>
Simplifying these equations gives
<div class="arithmatex" markdown="1">
\[
\begin{align*}
3b-3c & = 0\\
3a+2b+2c & = 0.
\end{align*}
\]
</div>
Thus $b=c$ and $3a+4c=0$, i.e., $a = -\frac 43c$, and $c$ is a free variable. (Alternatively, the above system is associated to the matrix $\left ( \begin{array}{ccc} 0 & 3 & -3 \\ 3 & 2 & 2 \end{array} \right )$, which can be brought into reduced row echelon form.) Thus,
<div class="arithmatex" markdown="1">
\[
\begin{align*}
S \cap T & = \{-\frac 43 c(1,-1,0,1) + c(2,1,-2,0)+c(0,0,1,1) \ | \ c \in {\bf R} \} \\
& = \{ c \left ( (-\frac 43, \frac 43, 0, -\frac 43) + (2,1,-2,0)+(0,0,1,1) \right ) \ | \ c \in {\bf R} \} \\
& = \{ c ( \frac 23, \frac 73, -1, - \frac 13) \ | \ c \in {\bf R} \} \\
& = L(( \frac 23, \frac 73, -1, - \frac 13)).
\end{align*}
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.17</strong></p>

<span id="sol-ex-intersection-tw" label="sol--ex:intersection-tw"></span> (See <a href="../exercises-spaces/#ex-intersection-tw" data-reference-type="ref+Label" data-reference="ex:intersection-tw">Exercise 3.17</a>.) $T$ is a subspace by <a href="../spaces-definition-solution-of-homogeneous/#prop-homogeneous-system-subspace" data-reference-type="ref+Label" data-reference="prop:homogeneous-system-subspace">Proposition 3.18</a> (<a href="../systems-linear-systems/#def-homogeneous-linear-system" data-reference-type="ref+Label" data-reference="def:homogeneous-linear-system">Definition 2.13</a>). To find $T \cap W$ we parametrise $W$ and then impose $T$’s equations (<a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>).

A general element of $W$ is
<div class="arithmatex" markdown="1">
\[
w = a(1,0,1,0) + b(2,0,0,0) + c(0,-3,-1,-1) = (a+2b,\,-3c,\,a-c,\,-c)
\]
</div>
for $a,b,c \in {\bf R}$. Requiring $w \in T$:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x_1 - x_2 = 0 &\;\Longrightarrow\; (a+2b) - (-3c) = 0 \;\Longrightarrow\; a + 2b + 3c = 0, \\
x_1 + x_2 + x_3 = 0 &\;\Longrightarrow\; (a+2b) + (-3c) + (a-c) = 0 \;\Longrightarrow\; a + b - 2c = 0.
\end{align*}
\]
</div>
Row-reducing this $2\times 3$ system in $a,b,c$:
<div class="arithmatex" markdown="1">
\[
\begin{pmatrix} 1 & 2 & 3 \\ 1 & 1 & -2 \end{pmatrix}
\xrightarrow{R_2 - R_1}
\begin{pmatrix} 1 & 2 & 3 \\ 0 & -1 & -5 \end{pmatrix}
\xrightarrow{R_1 + 2R_2}
\begin{pmatrix} 1 & 0 & -7 \\ 0 & -1 & -5 \end{pmatrix}.
\]
</div>
So $c$ is free, $b = -5c$, $a = 7c$. Substituting back:
<div class="arithmatex" markdown="1">
\[
w = 7c(1,0,1,0) - 5c(2,0,0,0) + c(0,-3,-1,-1) = c(-3,-3,6,-1).
\]
</div>
Hence
<div class="arithmatex" markdown="1">
\[
T \cap W = L\!\bigl((-3,-3,6,-1)\bigr),
\]
</div>
which has <a href="../spaces-bases/#def-basis" data-reference-type="ref+Label" data-reference="def:basis">Definition 3.61</a>: $\{(-3,-3,6,-1)\}$ is a basis, and $\dim(T \cap W) = 1$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.18</strong></p>

<span id="sol-ex-r2-spanning" label="sol--ex:r2-spanning"></span> (See <a href="../exercises-spaces/#ex-r2-spanning" data-reference-type="ref+Label" data-reference="ex:r2-spanning">Exercise 3.18</a>.) By <a href="../spaces-dimension/#cor-indep-span" data-reference-type="ref+Label" data-reference="cor:indep-span">Corollary 3.73</a>, two vectors in ${\bf R}^2$ span ${\bf R}^2$ if and only if they are linearly independent (<a href="../spaces-linear-independence/#def-linearly-independent" data-reference-type="ref+Label" data-reference="def:linearly-independent">Definition 3.49</a>). Two vectors in ${\bf R}^2$ are linearly dependent if and only if one of them is a scalar multiple of the other.

- The vectors $(1,1)$ and $(2,-1)$ are not scalar multiples of each other, confirming that ${\bf R}^2 = L((1,1),(2,-1))$.

- The vectors $(0,-2)$ and $(1,1)$ are also not scalar multiples of each other, so again ${\bf R}^2 = L((0,-2),(1,1))$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.19</strong></p>

<span id="sol-ex-linear-combination-r3" label="sol--ex:linear-combination-r3"></span> (See <a href="../exercises-spaces/#ex-linear-combination-r3" data-reference-type="ref+Label" data-reference="ex:linear-combination-r3">Exercise 3.19</a>.) We ask whether there exist $a_1, a_2, a_3 \in {\bf R}$ with $a_1 v_1 + a_2 v_2 + a_3 v_3 = (1,5,0)$ (<a href="../spaces-linear-combinations/#def-spaces-definition-008" data-reference-type="ref+Label" data-reference="def:spaces-definition-008">Definition 3.31</a>). This is the linear system (<a href="../systems-linear-systems/#def-systems-definition-002" data-reference-type="ref+Label" data-reference="def:systems-definition-002">Definition 2.7</a>) with augmented matrix
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc|c} 1 & 2 & 0 & 1 \\ 1 & 0 & 3 & 5 \\ 0 & 1 & -1 & 0 \end{array} \right )
\xrightarrow{R_2 - R_1}
\left ( \begin{array}{ccc|c} 1 & 2 & 0 & 1 \\ 0 & -2 & 3 & 4 \\ 0 & 1 & -1 & 0 \end{array} \right )
\xrightarrow{2R_3 + R_2}
\left ( \begin{array}{ccc|c} 1 & 2 & 0 & 1 \\ 0 & -2 & 3 & 4 \\ 0 & 0 & 1 & 4 \end{array} \right ).
\]
</div>
Back-substitution gives $a_3 = 4$, then $a_2 = 4$, then $a_1 = -7$. The system is consistent, so *yes*, $(1,5,0)$ is a linear combination:
<div class="arithmatex" markdown="1">
\[
(1,5,0) = -7\,v_1 + 4\,v_2 + 4\,v_3.
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.20</strong></p>

<span id="sol-ex-polynomial-basis-change" label="sol--ex:polynomial-basis-change"></span> (See <a href="../exercises-spaces/#ex-polynomial-basis-change" data-reference-type="ref+Label" data-reference="ex:polynomial-basis-change">Exercise 3.20</a>.) As was noted in <a href="../spaces-dimension/#ex-spaces-example-024" data-reference-type="ref+Label" data-reference="ex:spaces-example-024">Example 3.75</a>, the polynomials $1,(x-1),(x-1)^2,(x-1)^3,(x-1)^4$ form a basis of ${\bf R}[x]^{\le 4}$. Hence every polynomial of degree $\le 4$ has a unique such expansion. We use the substitution $y = x-1$ (i.e. $x = 1+y$) and expand via the binomial theorem (alternatively, the exercise may also be solved similarly as in <a href="#sol-ex-poly-span-1" data-reference-type="ref+Label" data-reference="sol--ex poly span 1">Solution 3.10</a>).

1.  $f(x) = x^4 = (1+y)^4 = 1 + 4y + 6y^2 + 4y^3 + y^4$, so
<div class="arithmatex" markdown="1">
\[
    x^4 = 1 + 4(x-1) + 6(x-1)^2 + 4(x-1)^3 + (x-1)^4.
\]
</div>

2.  $f(x) = x^3 = (1+y)^3 = 1 + 3y + 3y^2 + y^3$, so
<div class="arithmatex" markdown="1">
\[
    x^3 = 1 + 3(x-1) + 3(x-1)^2 + (x-1)^3.
\]
</div>

3.  $f(x) = x^3 - 3x^2 + 4x + 2$. Using the expansions above together with $x^2 = 1 + 2(x-1) + (x-1)^2$ and $x = 1+(x-1)$:
<div class="arithmatex" markdown="1">
\[
    \begin{align*}
    f &= \bigl[1 + 3(x-1) + 3(x-1)^2 + (x-1)^3\bigr] \\
    &\quad{} - 3\bigl[1 + 2(x-1) + (x-1)^2\bigr] \\
    &\quad{} + 4\bigl[1 + (x-1)\bigr] + 2.
    \end{align*}
\]
</div>
Collecting by degree: constant $1-3+4+2 = 4$; degree 1: $3-6+4 = 1$; degree 2: $3-3 = 0$; degree 3: $1$. Hence
<div class="arithmatex" markdown="1">
\[
    x^3-3x^2+4x+2 = 4 + (x-1) + (x-1)^3.
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.21</strong></p>

<span id="sol-ex-polynomial-basis-ab" label="sol--ex:polynomial-basis-ab"></span> (See <a href="../exercises-spaces/#ex-polynomial-basis-ab" data-reference-type="ref+Label" data-reference="ex:polynomial-basis-ab">Exercise 3.21</a>.) By <a href="../spaces-bases/#def-basis" data-reference-type="ref+Label" data-reference="def:basis">Definition 3.61</a> we must show that $\{x-a, x-b\}$ is linearly independent and spans ${\bf R}[x]^{\le 1}$.

*Linear independence (<a href="../spaces-linear-independence/#def-linearly-independent" data-reference-type="ref+Label" data-reference="def:linearly-independent">Definition 3.49</a>).* Suppose $\lambda(x-a) + \mu(x-b) = 0$ in ${\bf R}[x]^{\le 1}$. Collecting by degree:
<div class="arithmatex" markdown="1">
\[
(\lambda+\mu)\,x + (-\lambda a - \mu b) = 0.
\]
</div>
Since the zero polynomial has all coefficients zero:
<div class="arithmatex" markdown="1">
\[
\lambda + \mu = 0 \quad\text{and}\quad \lambda a + \mu b = 0.
\]
</div>
From the first equation $\mu = -\lambda$; substituting into the second gives $\lambda(a-b) = 0$. Since $a \neq b$ we conclude $\lambda = 0$ and hence $\mu = 0$. Thus $x-a$ and $x-b$ are linearly independent.

*Spanning.* We have $\dim {\bf R}[x]^{\le 1} = 2$ (the standard basis $\{1, x\}$ has two elements). Since $\{x-a, x-b\}$ consists of exactly 2 linearly independent vectors in a 2-dimensional space, it is a basis by <a href="../spaces-dimension/#cor-indep-span" data-reference-type="ref+Label" data-reference="cor:indep-span">Corollary 3.73</a>, and in particular spans ${\bf R}[x]^{\le 1}$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.22</strong></p>

<span id="sol-ex-basis-w1-r4" label="sol--ex:basis-w1-r4"></span> (See <a href="../exercises-spaces/#ex-basis-w1-r4" data-reference-type="ref+Label" data-reference="ex:basis-w1-r4">Exercise 3.22</a>.) *Basis and dimension of $W_1$.* $W_1$ is the solution set of the homogeneous system (<a href="../systems-linear-systems/#def-homogeneous-linear-system" data-reference-type="ref+Label" data-reference="def:homogeneous-linear-system">Definition 2.13</a>) $y+t=0$, $y+z=0$, so it is a subspace by <a href="../spaces-definition-solution-of-homogeneous/#prop-homogeneous-system-subspace" data-reference-type="ref+Label" data-reference="prop:homogeneous-system-subspace">Proposition 3.18</a>. Solving (<a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>): the dependent variables are $z = -y$ and $t = -y$, while $x$ and $y$ are free. Setting $(x,y) = (1,0)$ and $(0,1)$ in turn:
<div class="arithmatex" markdown="1">
\[
W_1 = \bigl\{(x,y,-y,-y) \mid x,y \in {\bf R}\bigr\} = L\bigl((1,0,0,0),\,(0,1,-1,-1)\bigr).
\]
</div>
The two generators are clearly linearly independent (<a href="../spaces-linear-independence/#def-linearly-independent" data-reference-type="ref+Label" data-reference="def:linearly-independent">Definition 3.49</a>), so
<div class="arithmatex" markdown="1">
\[
\mathcal{B}_1 = \{(1,0,0,0),\,(0,1,-1,-1)\}
\]
</div>
is a basis (<a href="../spaces-bases/#def-basis" data-reference-type="ref+Label" data-reference="def:basis">Definition 3.61</a>) of $W_1$ and $\dim W_1 = 2$ (<a href="../spaces-dimension/#def-dimension" data-reference-type="ref+Label" data-reference="def:dimension">Definition 3.66</a>).

*$W_1 \cap W_2$.* A general element of $W_2 = L((0,1,-1,0))$ is $\lambda(0,1,-1,0)$ for $\lambda \in {\bf R}$. Imposing the first condition of $W_1$:
<div class="arithmatex" markdown="1">
\[
y + t = \lambda + 0 = \lambda = 0.
\]
</div>
Hence $\lambda = 0$, and $W_1 \cap W_2 = \{0\}$ is the trivial subspace.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.23</strong></p>

<span id="sol-ex-wk-basis" label="sol--ex:wk-basis"></span> (See <a href="../exercises-spaces/#ex-wk-basis" data-reference-type="ref+Label" data-reference="ex:wk-basis">Exercise 3.23</a>.) *Part 1: Basis and dimension of $W_k$.* We write the generators of $W_k = L((1,0,-1,0),(1,1,0,1),(1,2,k,1))$ (cf. <a href="../spaces-linear-combinations/#def-generating-system" data-reference-type="ref+Label" data-reference="def:generating-system">Definition 3.42</a>) as rows of a matrix and apply the Gaussian algorithm (<a href="../systems-gaussian-elimination/#met-gaussian-algorithm" data-reference-type="ref+Label" data-reference="met:gaussian-algorithm">Method 2.29</a>):
<div class="arithmatex" markdown="1">
\[
\begin{pmatrix}1&0&-1&0\\1&1&0&1\\1&2&k&1\end{pmatrix}
\xrightarrow{R_2-R_1,\,R_3-R_1}
\begin{pmatrix}1&0&-1&0\\0&1&1&1\\0&2&k+1&1\end{pmatrix}
\xrightarrow{R_3-2R_2}
\begin{pmatrix}1&0&-1&0\\0&1&1&1\\0&0&k-1&-1\end{pmatrix}.
\]
</div>
The third row $(0,0,k-1,-1)$ is nonzero for *every* $k \in {\bf R}$ (since its last entry $-1 \ne 0$, regardless of $k$). Hence the matrix is in row echelon form (<a href="../systems-gaussian-elimination/#def-row-echelon-form" data-reference-type="ref+Label" data-reference="def:row-echelon-form">Definition 2.27</a>) with three pivot rows, so the rank equals 3 for all $k$. Equivalently, the three vectors are linearly independent (<a href="../spaces-linear-independence/#met-check-linear-independence" data-reference-type="ref+Label" data-reference="met:check-linear-independence">Method 3.56</a>), so $\dim W_k = 3$ for all $k \in {\bf R}$. Since the three vectors also span $W_k$, they form a basis (<a href="../spaces-bases/#def-basis" data-reference-type="ref+Label" data-reference="def:basis">Definition 3.61</a>):
<div class="arithmatex" markdown="1">
\[
\mathcal{B}_k = \{(1,0,-1,0),\,(0,1,1,1),\,(0,0,k-1,-1)\} \quad (k \ne 1),
\]
</div>
and for $k = 1$ the basis is $\{(1,0,-1,0),(0,1,1,1),(0,0,0,-1)\}$.

*Part 2: Membership of $(-1,1,1,1)$ in $W_k$.* We ask whether $(-1,1,1,1) = \alpha(1,0,-1,0)+\beta(1,1,0,1)+\gamma(1,2,k,1)$ for some $\alpha,\beta,\gamma \in {\bf R}$. This corresponds to the augmented matrix (<a href="#def-augmented-matrix" data-reference-type="ref+Label" data-reference="def:augmented-matrix">[def:augmented-matrix]</a>)
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc|c} 1 & 1 & 1 & -1 \\ 0 & 1 & 2 & 1 \\ -1 & 0 & k & 1 \\ 0 & 1 & 1 & 1 \end{array} \right )
\xrightarrow{R_3+R_1}
\left ( \begin{array}{ccc|c} 1 & 1 & 1 & -1 \\ 0 & 1 & 2 & 1 \\ 0 & 1 & k+1 & 0 \\ 0 & 1 & 1 & 1 \end{array} \right )
\xrightarrow{R_3-R_2,\,R_4-R_2}
\left ( \begin{array}{ccc|c} 1 & 1 & 1 & -1 \\ 0 & 1 & 2 & 1 \\ 0 & 0 & k-1 & -1 \\ 0 & 0 & -1 & 0 \end{array} \right ).
\]
</div>
Row 4 gives $-\gamma = 0$, i.e. $\gamma = 0$. Substituting into row 3: $(k-1)\cdot 0 = -1$, i.e. $0 = -1$, a contradiction. Therefore $(-1,1,1,1) \notin W_k$ for *any* $k \in {\bf R}$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.24</strong></p>

<span id="sol-ex-mat-subspace-dim" label="sol--ex:mat-subspace-dim"></span> (See <a href="../exercises-spaces/#ex-mat-subspace-dim" data-reference-type="ref+Label" data-reference="ex:mat-subspace-dim">Exercise 3.24</a>.) *Part 1: $W$ is a subspace with $\dim W = 2$.* Every element of $W$ decomposes as
<div class="arithmatex" markdown="1">
\[
\begin{pmatrix}a & a+b & b \\ 0 & 0 & b\end{pmatrix}
= a\underbrace{\begin{pmatrix}1 & 1 & 0 \\ 0 & 0 & 0\end{pmatrix}}_{=:E_1}
+ b\underbrace{\begin{pmatrix}0 & 1 & 1 \\ 0 & 0 & 1\end{pmatrix}}_{=:E_2},
\]
</div>
so $W = L(E_1, E_2)$ (<a href="../spaces-linear-combinations/#def-generating-system" data-reference-type="ref+Label" data-reference="def:generating-system">Definition 3.42</a>). We verify the subspace conditions (<a href="../spaces-definition-solution-of-homogeneous/#def-subspace" data-reference-type="ref+Label" data-reference="def:subspace">Definition 3.17</a>): the zero matrix arises with $a=b=0$; sums and scalar multiples correspond to replacing $(a,b)$ by $(a+a', b+b')$ and $(ra, rb)$, which stays in $W$.

To find the dimension, we check that $E_1, E_2$ are linearly independent (<a href="../spaces-linear-independence/#def-linearly-independent" data-reference-type="ref+Label" data-reference="def:linearly-independent">Definition 3.49</a>): $\alpha E_1 + \beta E_2 = 0$ gives $\alpha = 0$ (from position $(1,1)$) and then $\beta = 0$ (from position $(1,3)$). Hence $\{E_1, E_2\}$ is a basis (<a href="../spaces-bases/#def-basis" data-reference-type="ref+Label" data-reference="def:basis">Definition 3.61</a>) and $\dim W = 2$ (<a href="../spaces-dimension/#def-dimension" data-reference-type="ref+Label" data-reference="def:dimension">Definition 3.66</a>).

*Part 2: $V \cap W = V$, so $\dim(V \cap W) = 1$.* A matrix belongs to $V \cap W$ if and only if it has the form $\begin{pmatrix}a&a+b&b\\0&0&b\end{pmatrix}$ (from $W$) and simultaneously $\begin{pmatrix}c&0&-c\\0&0&-c\end{pmatrix}$ (from $V$). Matching entries gives $a = c$, $b = -c$, and $a+b = c+(-c) = 0$ – which is automatically satisfied. Hence every element of $V$ lies in $W$, i.e., $V \subset W$, so $V \cap W = V$. A basis of $V \cap W$ is
<div class="arithmatex" markdown="1">
\[
\left\{ \begin{pmatrix}1 & 0 & -1 \\ 0 & 0 & -1\end{pmatrix} \right\},
\]
</div>
and $\dim(V \cap W) = 1$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.25</strong></p>

<span id="sol-ex-spaces-2-4" label="sol--ex:spaces-2-4"></span> (See <a href="../exercises-spaces/#ex-spaces-2-4" data-reference-type="ref+Label" data-reference="ex:spaces-2-4">Exercise 3.25</a>.) We have to find a vector $v \in W_1$ that is also contained in $W_2$. This means that
<div class="arithmatex" markdown="1">
\[
v = a (1,0,1)+b(2,1,0) = (a+2b,b,a)
\]
</div>

<p class="env-number equation-number"><strong>(3.82)</strong></p>

<span id="eqn-sol-blah" label="eqn--sol.blah"></span> for some $a, b \in {\bf R}$ and at the same time
<div class="arithmatex" markdown="1">
\[
v = \alpha(-1,-1,1) + \beta(0,3,0) = (-\alpha, -\alpha + 3 \beta, \alpha)
\]
</div>
for some $\alpha, \beta \in {\bf R}$. Comparing the two vectors gives the following linear system, where $a, b, \alpha, \beta$ are the unknowns:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
a + 2 b & = -\alpha \\
b & = -\alpha + 3\beta \\
a & = \alpha.
\end{align*}
\]
</div>
We solve this system: the last equation gives $a = \alpha$ and, from the first equation, $b = -\alpha$. The second equation implies $\beta = 0$. There is no condition on $\alpha$, this $\alpha = r$ for an arbitrary real number $r \in {\bf R}$.

Instead of solving the above system by hand, we may also use Gaussian elimination to solve this linear system. The matrix is the following (where the columns are for $a, b, \alpha, \beta$, in that order):
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left ( \begin{array}{cccc} 1 & 2 & 1 & 0 \\ 0 & 1 & 1 & -3 \\ 1 & 0 & -1 & 0 \end{array} \right ) \leadsto
& \left ( \begin{array}{cccc} 1 & 2 & 1 & 0 \\ 0 & 1 & 1 & -3 \\ 0 & -2 & -2 & 0 \end{array} \right ) \leadsto
\left ( \begin{array}{cccc} 1 & 2 & 1 & 0 \\ 0 & 1 & 1 & -3 \\ 0 & 0 & 0 & -6 \end{array} \right ) \\ & \leadsto
\left ( \begin{array}{cccc} 1 & 2 & 1 & 0 \\ 0 & 1 & 1 & -3 \\ 0 & 0 & 0 & 1 \end{array} \right ).
\end{align*}
\]
</div>
The three leading ones are for the variables $a, b, \beta$, and $\alpha$ is a free variable, so let $\alpha = r$, where $r \in {\bf R}$ is an arbitrary real number. This gives again $\beta = 0$, $b + r - 3\beta = 0$, so that $b = - r$ and $a = r$.

Thus the intersection $W_1 \cap W_2$ consists of the vectors
<div class="arithmatex" markdown="1">
\[
v = \alpha (1,0,1) + (-\alpha)(2,1,0) = \alpha(-1,-1,1) + 0 (0,3,0) = (-\alpha, -\alpha, \alpha).
\]
</div>
Thus,
<div class="arithmatex" markdown="1">
\[
W_1 \cap W_2 = L((1,-1,1)),
\]
</div>
so a basis of $W_1 \cap W_2$ consists of (the single vector) $(1,-1,1)$, and in particular
<div class="arithmatex" markdown="1">
\[
\dim W_1 \cap W_2 = 1.
\]
</div>

We now consider $W_1 + W_2$. According to <a href="../spaces-linear-combinations/#def-sum-of-vector-spaces" data-reference-type="ref+Label" data-reference="def:sum-of-vector-spaces">Definition 3.36</a>,
<div class="arithmatex" markdown="1">
\[
W_1 + W_2 = \{w_1 + w_2 \ | \ w_1 \in W_1, w_2 \in W_2 \},
\]
</div>
i.e., of arbitrary sums whose two summands are in $W_1$, respectively $W_2$.

As was noted in the proof of <a href="../spaces-dimension/#cor-dim-sum-inequality" data-reference-type="ref+Label" data-reference="cor:dim-sum-inequality">Corollary 3.76</a>, if $V_1 = L(v_1, \dots, v_n)$ and $V_2 = L(w_1, \dots, w_m)$ are two subspaces of a vector space $V$, then the sum
<div class="arithmatex" markdown="1">
\[
V_1 + V_2 = L(v_1, \dots, v_n, w_1, \dots, w_m).
\]
</div>

For the subspaces $W_1, W_2$ above, this means that we determine the span
<div class="arithmatex" markdown="1">
\[
L(\underbrace{(1,0,1)}_{v_1}, \underbrace{(2,1,0)}_{v_2}, \underbrace{(-1,-1,1)}_{w_1}, \underbrace{(0,3,0)}_{w_2}).
\]
</div>
By <a href="../spaces-bases/#def-basis" data-reference-type="ref+Label" data-reference="def:basis">Definition 3.61</a><a href="../spaces-dimension/#item-generators-remove" data-reference-type="ref" data-reference="item--generators.remove">1.</a>, we obtain a basis of $W_1 + W_2$ by (possibly) removing several of these four vectors. To determine which ones these are, we apply <a href="../spaces-linear-independence/#met-check-linear-independence" data-reference-type="ref+Label" data-reference="met:check-linear-independence">Method 3.56</a> and <a href="../spaces-linear-combinations/#met-check-generating-system" data-reference-type="ref+Label" data-reference="met:check-generating-system">Method 3.46</a>. The matrix built out of the four vectors is
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{c} v_1 \\ v_2 \\ w_1 \\ w_2 \end{array} \right ) = \left ( \begin{array}{ccc} 1 & 0 & 1 \\ 2 & 1 & 0 \\ \hline -1 & -1 & 1 \\ 0 & 3 & 0 \end{array} \right ) \leadsto \left ( \begin{array}{ccc} 1 & 0 & 1 \\ 0 & 1 & -2 \\ \hline 0 & -1 & 2 \\ 0 & 3 & 0 \end{array} \right ) \leadsto
\left ( \begin{array}{ccc} 1 & 0 & 1 \\ 0 & 1 & -2 \\ \hline \underline{0} & \underline{0} & \underline{0} \\ 0 & 0 & 6 \end{array} \right ).
\]
</div>
Note that in this process we only added multiples of some rows to another row, but did not interchange any rows. Since we have the zero vector (underlined) in the third row, the vector $w_1$ is a linear combination of $v_1$ and $v_2$. The vectors $v_1, v_2, w_2$ are however linearly independent. Thus, they form a basis of $W_1 + W_2$. In particular, $\dim (W_1 + W_2) = 3$.

An alternative way to determine at least the dimension of $W_1 + W_2$ is to use <a href="../spaces-dimension/#thm-dim-cap-sum" data-reference-type="ref+Label" data-reference="thm:dim-cap-sum">Theorem 3.77</a>:
<div class="arithmatex" markdown="1">
\[
\dim (W_1 + W_2) = \dim W_1 + \dim W_2 - \dim (W_1 \cap W_2).
\]
</div>
Using again <a href="../spaces-linear-independence/#met-check-linear-independence" data-reference-type="ref+Label" data-reference="met:check-linear-independence">Method 3.56</a>, one can check that $v_1, v_2$ is a basis of $W_1$, so that $\dim W_1 = 2$ and similarly that $w_1, w_2$ form a basis of $W_2$, so that $\dim W_2 = 2$. Thus, using the first part of the exercise, we confirm $\dim (W_1 + W_2) = 3$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.26</strong></p>

<span id="sol-ex-sum-intersection-r4" label="sol--ex:sum-intersection-r4"></span> (See <a href="../exercises-spaces/#ex-sum-intersection-r4" data-reference-type="ref+Label" data-reference="ex:sum-intersection-r4">Exercise 3.26</a>.) Denote $v_1=(1,1,1,2)$, $v_2=(2,0,3,5)$, $w_1=(1,1,0,1)$, $w_2=(0,2,-2,-2)$.

*Bases and dimensions of $W_1$, $W_2$.* Row-reducing the generator matrices (<a href="../systems-gaussian-elimination/#met-gaussian-algorithm" data-reference-type="ref+Label" data-reference="met:gaussian-algorithm">Method 2.29</a>) gives
<div class="arithmatex" markdown="1">
\[
\begin{pmatrix}1&1&1&2\\2&0&3&5\end{pmatrix}
\xrightarrow{R_2-2R_1}
\begin{pmatrix}1&1&1&2\\0&-2&1&1\end{pmatrix},
\qquad
\begin{pmatrix}1&1&0&1\\0&2&-2&-2\end{pmatrix}
\]
</div>
both already in row echelon form (<a href="../systems-gaussian-elimination/#def-row-echelon-form" data-reference-type="ref+Label" data-reference="def:row-echelon-form">Definition 2.27</a>) with two nonzero rows, so $\dim W_1 = \dim W_2 = 2$ and $\{v_1,v_2\}$, $\{w_1,w_2\}$ are bases (<a href="../spaces-bases/#def-basis" data-reference-type="ref+Label" data-reference="def:basis">Definition 3.61</a>).

*$W_1 + W_2$.* Row-reducing the matrix of all four generators (<a href="../spaces-linear-combinations/#def-sum-of-vector-spaces" data-reference-type="ref+Label" data-reference="def:sum-of-vector-spaces">Definition 3.36</a>):
<div class="arithmatex" markdown="1">
\[
\begin{pmatrix}1&1&1&2\\2&0&3&5\\1&1&0&1\\0&2&-2&-2\end{pmatrix}
\xrightarrow{R_2-2R_1,\,R_3-R_1}
\begin{pmatrix}1&1&1&2\\0&-2&1&1\\0&0&-1&-1\\0&2&-2&-2\end{pmatrix}
\xrightarrow{R_4+R_2,\,R_4-R_3}
\begin{pmatrix}1&1&1&2\\0&-2&1&1\\0&0&-1&-1\\0&0&0&0\end{pmatrix}.
\]
</div>
The rank is 3, so $\dim(W_1+W_2) = 3$ with basis $\{(1,1,1,2),(0,-2,1,1),(0,0,-1,-1)\}$.

*$W_1 \cap W_2$.* By the dimension formula (<a href="../spaces-dimension/#thm-dim-cap-sum" data-reference-type="ref+Label" data-reference="thm:dim-cap-sum">Theorem 3.77</a>):
<div class="arithmatex" markdown="1">
\[
\dim(W_1 \cap W_2) = \dim W_1 + \dim W_2 - \dim(W_1+W_2) = 2+2-3 = 1.
\]
</div>
To find a generator, we solve $\alpha v_1 + \beta v_2 = \gamma w_1 + \delta w_2$, i.e., $\alpha v_1 + \beta v_2 - \gamma w_1 - \delta w_2 = 0$:
<div class="arithmatex" markdown="1">
\[
\begin{pmatrix}1&2&-1&0\\1&0&-1&-2\\1&3&0&2\\2&5&-1&2\end{pmatrix}
\xrightarrow{R_2-R_1,\,R_3-R_1,\,R_4-2R_1}
\begin{pmatrix}1&2&-1&0\\0&-2&0&-2\\0&1&1&2\\0&1&1&2\end{pmatrix}
\xrightarrow{R_4-R_3,\,2R_3+R_2}
\begin{pmatrix}1&2&-1&0\\0&-2&0&-2\\0&0&2&2\\0&0&0&0\end{pmatrix}.
\]
</div>
Setting the free variable $\delta=1$: row 3 gives $\gamma=-1$, row 2 gives $\beta=-1$, row 1 gives $\alpha=1$. The corresponding vector in $W_1$ is
<div class="arithmatex" markdown="1">
\[
\alpha v_1 + \beta v_2 = (1,1,1,2) - (2,0,3,5) = (-1,1,-2,-3).
\]
</div>
Hence $W_1 \cap W_2 = L((-1,1,-2,-3))$ with basis $\{(-1,1,-2,-3)\}$ and $\dim(W_1\cap W_2)=1$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.27</strong></p>

<span id="sol-ex-spaces-2-5" label="sol--ex:spaces-2-5"></span> (See <a href="../exercises-spaces/#ex-spaces-2-5" data-reference-type="ref+Label" data-reference="ex:spaces-2-5">Exercise 3.27</a>.) We will show that $v_1, v_2, v_3$ are linearly independent (in ${\bf R}^4$ and therefore also in the subspace $W$) and therefore form a basis of $W$. We use <a href="../spaces-linear-independence/#met-check-linear-independence" data-reference-type="ref+Label" data-reference="met:check-linear-independence">Method 3.56</a>:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left ( \begin{array}{c} v_1 \\ v_2 \\ v_3 \end{array} \right ) = & \left ( \begin{array}{cccc} 1 & 0 & 1 & 0 \\ 2 & 0 & 1 & 1 \\ 0 & 0 & 1 & 3 \end{array} \right ) \leadsto \left ( \begin{array}{cccc} 1 & 0 & 1 & 0 \\ 0 & 0 & -1 & 1 \\ 0 & 0 & 1 & 3 \end{array} \right )
\leadsto \left ( \begin{array}{cccc} 1 & 0 & 1 & 0 \\ 0 & 0 & 1 & -1 \\ 0 & 0 & 0 & 4 \end{array} \right )\\
\leadsto & \left ( \begin{array}{cccc} 1 & 0 & 1 & 0 \\ 0 & 0 & 1 & -1 \\ 0 & 0 & 0 & 1 \end{array} \right )
\end{align*}
\]
</div>
This matrix has three leading ones, so the vectors are linearly independent as claimed.

We “guess” $v = (1, 2, 3, 4)$ and check that these vectors $v_1, v_2, v_3, v$ are linearly independent. By <a href="../spaces-linear-independence/#lem-independent-linear-combination" data-reference-type="ref+Label" data-reference="lem:independent-linear-combination">Lemma 3.54</a>, this will then imply that $v$ is not a linear combination of the other vectors, so that $W \subsetneq L(v_1, v_2, v_3, v)$. We use <a href="../spaces-linear-independence/#met-check-linear-independence" data-reference-type="ref+Label" data-reference="met:check-linear-independence">Method 3.56</a>:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left ( \begin{array}{cccc} 1 & 0 & 1 & 0 \\ 2 & 0 & 1 & 1 \\ 0 & 0 & 1 & 3 \\ 1 & 2 & 3 & 4 \end{array} \right ) & \leadsto
\left ( \begin{array}{cccc} 1 & 0 & 1 & 0 \\ 0 & 0 & -1 & 1 \\ 0 & 0 & 1 & 3 \\ 0 & 2 & 2 & 4 \end{array} \right ) \leadsto
\left ( \begin{array}{cccc} 1 & 0 & 1 & 0 \\ 0 & 0 & -1 & 1 \\ 0 & 0 & 1 & 3 \\ 0 & 1 & 1 & 2 \end{array} \right ) \\
& \leadsto
\left ( \begin{array}{cccc} \underline1 & 0 & 1 & 0 \\ 0 & 0 & 0 & \underline4 \\ 0 & 0 & \underline1 & 3 \\ 0 & \underline1 & 1 & 2 \end{array} \right )
\end{align*}
\]
</div>
After dividing the second row by 4, we can interchange rows and get a row echelon matrix with four leading ones (underlined). Thus, $v_1, v_2, v_3, v$ are linearly independent. Therefore, they form in fact a basis of ${\bf R}^4$, and we know by <a href="../spaces-bases/#def-basis" data-reference-type="ref+Label" data-reference="def:basis">Definition 3.61</a><a href="../spaces-dimension/#item-dim-subspace" data-reference-type="ref" data-reference="item--dim.subspace">3.</a> that therefore
<div class="arithmatex" markdown="1">
\[
W \subsetneq {\bf R}^4 = L(v_1, v_2, v_3, v).
\]
</div>

<div class="remark" markdown="1">


<p class="env-number"><strong>Remark 3.83</strong></p>

<span id="rem-solutions-remark-001" label="rem:solutions-remark-001"></span> A more systematic way of solving the second part of the exercise, without guessing, is to use <a href="../spaces-bases/#def-basis" data-reference-type="ref+Label" data-reference="def:basis">Definition 3.61</a>: we can take the standard basis of ${\bf R}^4$, and for (at least) one of the four standard basis vectors $e_1, e_2, e_3, e_4$ we will have that this standard basis vector together with $v_1, v_2, v_3$ form a basis of ${\bf R}^4$. We can then use <a href="../spaces-linear-independence/#met-check-linear-independence" data-reference-type="ref+Label" data-reference="met:check-linear-independence">Method 3.56</a> to see that, for example, $v_1, v_2, v_3, e_1$ are linearly independent and therefore form a basis of ${\bf R}^4$, so that in particular $W \subsetneq L(v_1, v_2, v_3, e_1)$.

</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.28</strong></p>

<span id="sol-ex-spaces-2-6" label="sol--ex:spaces-2-6"></span> (See <a href="../exercises-spaces/#ex-spaces-2-6" data-reference-type="ref+Label" data-reference="ex:spaces-2-6">Exercise 3.28</a>.) We bring the matrix formed by these vectors in row-echelon form:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left ( \begin{array}{cccc} 1 & 0 & -1 & 2 \\ 1 & 0 & 0 & 1 \\ 2 & 0 & -1 & 3 \\ 4 & t & -2 & 6 \end{array} \right ) & \leadsto
\left ( \begin{array}{cccc} 1 & 0 & -1 & 2 \\ 0 & 0 & 1 & -1 \\ 0 & 0 & 1 & -1 \\ 0 & t & 2 & -2 \end{array} \right ) \\
&\leadsto \left ( \begin{array}{cccc} 1 & 0 & -1 & 2 \\ 0 & t & 2 & -2 \\ 0 & 0 & 1 & -1 \\ 0 & 0 & 1 & -1 \end{array} \right ) \\
& \leadsto \left ( \begin{array}{cccc} 1 & 0 & -1 & 2 \\ 0 & t & 2 & -2 \\ 0 & 0 & 1 & -1 \\ 0 & 0 & 0 & 0 \end{array} \right ).
\end{align*}
\]
</div>
If $t \ne 0$, then division by $t$ is an elementary operation (<a href="../systems-gaussian-elimination/#def-elementary-row-operations" data-reference-type="ref+Label" data-reference="def:elementary-row-operations">Definition 2.28</a>), which then yields a matrix with three leading ones. Thus, the space $U_t$ which is spanned by these vectors has dimension 3 in this case. If $t = 0$, we continue simplifying the matrix into row echelon form:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left ( \begin{array}{cccc} 1 & 0 & -1 & 2 \\ 0 & t & 2 & -2 \\ 0 & 0 & 1 & -1 \\ 0 & 0 & 0 & 0 \end{array} \right ) & =
\left ( \begin{array}{cccc} 1 & 0 & -1 & 2 \\ 0 & 0 & 2 & -2 \\ 0 & 0 & 1 & -1 \\ 0 & 0 & 0 & 0 \end{array} \right ) \\
& \leadsto \left ( \begin{array}{cccc} 1 & 0 & -1 & 2 \\ 0 & 0 & 1 & -1 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{array} \right ).
\end{align*}
\]
</div>
This has two leading ones, thus $\dim U_t = 2$ in this case.

We now consider $t = 1$. The subspace $U := U_1$ then has a basis consisting of the non-zero rows if the matrix above, i.e., it has a basis consisting of the vectors
<div class="arithmatex" markdown="1">
\[
(1,0,-1,2), (0,1,2,-2), (0,0,1,-1).
\]
</div>

In order to determine a basis of $W$, we form the matrix associated to these homogeneous equations, and apply Gaussian elimination (<a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>):
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc} 1 & 1 & 1 & 0 \\ 1 & 0 & 0 & -3 \end{array} \right ) \leadsto \left ( \begin{array}{cccc} 1 & 1 & 1 & 0 \\ 0 & -1 & -1 & -3 \end{array} \right ).
\]
</div>
This has two columns not having a leading one, namely the last two. These are the free variables, say $x_3 = a$, $x_4 = b$ for $a , b \in {\bf R}$. To determine a basis of $W$, we therefore have to consider the system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x_1 + x_2 + a & = 0\\
x_2 + a + 3b & = 0
\end{align*}
\]
</div>
This gives $x_2 = -a-3b$, and $x_1 - 3b=0$ so that $x_1 = 3b$. Thus, a basis of $W$ is given by the two vectors
<div class="arithmatex" markdown="1">
\[
(0,-1,1,0) \text{ and }(3,-3,0,1).
\]
</div>

In order to determine the intersection $U \cap W$ (cf. <a href="../spaces-intersection/#lem-spaces-lemma-003" data-reference-type="ref+Label" data-reference="lem:spaces-lemma-003">Lemma 3.19</a>), consider a generic vector of $U$, i.e., one of the form
<div class="arithmatex" markdown="1">
\[
\begin{align*}
v & = a(1,0,-1,2) + b(0,1,2,-2) + c(0,0,1,-1) \\
&= (a,b,-a+2b+c,2a-2b-c).
\end{align*}
\]
</div>
We require it to satisfy the equations describing $W$:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
a+b+(-a+2b+c) & = 0\\
a-3(2a-2b-c) & = 0.
\end{align*}
\]
</div>
Simplifying these expressions gives the system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
3b+c & = 0\\
-5a+6b+3c & = 0.
\end{align*}
\]
</div>
Therefore $c = -3b$, plugging this into the second equation gives, after simplifying, $-5a-3b = 0$ or $a = -\frac35b$. Thus, our vector $v \in U$ belongs to $W$ precisely if it can be written as
<div class="arithmatex" markdown="1">
\[
\begin{align*}
 & -\frac 35 b(1,0,-1,2)+b(0,1,2,-2)+(-3b)(0,0,1,-1)  \\
=  & (-\frac 3bb, b, \frac35b+2b-3b,-\frac 65b-2b+3b) \\
= & b(-\frac 35, 1, -\frac25, -\frac15),
\end{align*}
\]
</div>
where $b \in {\bf R}$ is arbitrary. Thus, a basis of $U \cap W$ is this vector
<div class="arithmatex" markdown="1">
\[
(-\frac 35, 1, -\frac 25, -\frac 15).
\]
</div>
In particular, $\dim U \cap W = 1$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.29</strong></p>

<span id="sol-ex-ut-basis-r4" label="sol--ex:ut-basis-r4"></span> (See <a href="../exercises-spaces/#ex-ut-basis-r4" data-reference-type="ref+Label" data-reference="ex:ut-basis-r4">Exercise 3.29</a>.) *Part 1: Values of $t$ with $\dim U_t = 2$.* We row-reduce the matrix with $v_1,v_2,v_3,v_4$ as rows (<a href="../systems-gaussian-elimination/#met-gaussian-algorithm" data-reference-type="ref+Label" data-reference="met:gaussian-algorithm">Method 2.29</a>):
<div class="arithmatex" markdown="1">
\[
\begin{pmatrix}1&0&0&1\\-1&1&2&3\\0&1&2&4\\t&2&4&8\end{pmatrix}
\xrightarrow{R_2+R_1,\,R_4-tR_1}
\begin{pmatrix}1&0&0&1\\0&1&2&4\\0&1&2&4\\0&2&4&8-t\end{pmatrix}
\xrightarrow{R_3-R_2,\,R_4-2R_2}
\begin{pmatrix}1&0&0&1\\0&1&2&4\\0&0&0&0\\0&0&0&-t\end{pmatrix}.
\]
</div>
The last row $(0,0,0,-t)$ is zero if and only if $t=0$. Hence $\dim U_t = 2$ if and only if $t = 0$. (For $t \ne 0$ the rank is 3 and $\dim U_t = 3$.)

*Part 2: $\dim U_1$.* With $t = 1 \ne 0$, we have $\dim U_1 = 1$, as was noted above.

*Part 3: Basis of $W$ and of $W \cap U_1$.* $W$ is the solution set of the homogeneous system (<a href="../spaces-definition-solution-of-homogeneous/#prop-homogeneous-system-subspace" data-reference-type="ref+Label" data-reference="prop:homogeneous-system-subspace">Proposition 3.18</a>) $x_1 - x_2 = 0$, $x_2 - x_3 = 0$. These equations say $x_1 = x_2 = x_3$, so the free variables are $x_1$ and $x_4$:
<div class="arithmatex" markdown="1">
\[
(x_1, x_2, x_3, x_4) = x_1(1,1,1,0) + x_4(0,0,0,1).
\]
</div>
Thus $\{(1,1,1,0),(0,0,0,1)\}$ is a basis (<a href="../spaces-bases/#def-basis" data-reference-type="ref+Label" data-reference="def:basis">Definition 3.61</a>) of $W$ and $\dim W = 2$ (<a href="../spaces-dimension/#def-dimension" data-reference-type="ref+Label" data-reference="def:dimension">Definition 3.66</a>).

For $W \cap U_1$, we reduce the $t=1$ row echelon form to RREF:
<div class="arithmatex" markdown="1">
\[
\begin{pmatrix}1&0&0&1\\0&1&2&4\\0&0&0&1\\0&0&0&0\end{pmatrix}
\xrightarrow{R_1-R_3,\,R_2-4R_3}
\begin{pmatrix}1&0&0&0\\0&1&2&0\\0&0&0&1\\0&0&0&0\end{pmatrix},
\]
</div>
so $U_1 = \{(\alpha,\beta,2\beta,\gamma) \mid \alpha,\beta,\gamma \in {\bf R}\}$. Imposing the conditions of $W$ (i.e., $x_1=x_2=x_3$) gives $\beta = \alpha$ and $2\beta = \alpha$, hence $2\alpha = \alpha$, so $\alpha = 0$. The intersection is therefore $\{(0,0,0,\gamma) \mid \gamma \in {\bf R}\}$, with basis $\{(0,0,0,1)\}$ and $\dim(W \cap U_1) = 1$.

</div>
