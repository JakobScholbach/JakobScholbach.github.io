<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.1</strong></p>

<span id="ex-eigenvalues-exercise-001" label="ex:eigenvalues-exercise-001"></span> (See <a href="../solutions-eigenvalues-and-eigenvectors/#sol-ex-eigenvalues-exercise-001" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-exercise-001">Solution 6.1</a>.) Is the following matrix diagonalizable?
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{ccc} 2 & 1 & 1 \\ 0 & 1 & 0 \\ 1 & -1 & 2 \end{array} \right ).
\]
</div>

Hint: you will find that the eigenvalues of $A$ are among the numbers $0, 1, 2, 3$. You will be able to choose basis vectors of the eigenspaces all of whose coordinates are $-1, 0, 1$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.2</strong></p>

<span id="exercise-eigenvalues-2x2" label="exercise.eigenvalues.2x2"></span> (See <a href="../solutions-eigenvalues-and-eigenvectors/#sol-exercise-eigenvalues-2x2" data-reference-type="ref+Label" data-reference="sol--exercise.eigenvalues.2x2">Solution 6.2</a>.) Let $A = \left ( \begin{array}{cc} a & b \\ c & d \end{array} \right )$. Show that:

- $\chi_A(t) = t^2 - \mathrm {tr} (A) t + \det A = t^2 - (a+d) t + (ad-bc)$. Here $\mathrm {tr} (A)$ is the *trace* of $A$, cf. <a href="../exercises-maps/#trace" data-reference-type="ref+Label" data-reference="trace">Exercise 4.24</a>.

- The eigenvalues of $A$ are
<div class="arithmatex" markdown="1">
\[
  \lambda_{1/2} = \frac{a+d}2 \pm \sqrt{\frac{(a-b)^2}4+4bc}.
\]
</div>

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.3</strong></p>

<span id="ex-eigenvalues-exercise-002" label="ex:eigenvalues-exercise-002"></span> (See <a href="../solutions-eigenvalues-and-eigenvectors/#sol-ex-eigenvalues-exercise-002" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-exercise-002">Solution 6.3</a>.) For each of the following matrices, compute $\chi_A(t)$, the eigenvalues of $A$, the eigenspaces for these eigenvalues. Also decide whether $A$ is diagonalizable and compute an eigenbasis if one exists.

1.  $A = \left ( \begin{array}{cc} 3 & 5 \\ 1 & -1 \end{array} \right )$

2.  $A = \left ( \begin{array}{ccc} 0 & 1 & 0 \\ 3 & 0 & 1 \\ 2 & 0 & 0 \end{array} \right )$

3.  $A = \left ( \begin{array}{ccc} 1 & 0 & 0 \\ 0 & 0 & \frac 32 \\ 0 & 0 & 1 \end{array} \right )$

4.  $A = \left ( \begin{array}{ccc} 0 & 1 & 0 \\ 0 & 0 & 1 \\ 0 & 0 & 0 \end{array} \right )$

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.4</strong></p>

<span id="ex-eigenvalues-exercise-003" label="ex:eigenvalues-exercise-003"></span> (See <a href="../solutions-eigenvalues-and-eigenvectors/#sol-ex-eigenvalues-exercise-003" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-exercise-003">Solution 6.4</a>.) Consider the matrix $A = \left ( \begin{array}{ccc} 1 & 0 & 0 \\ 1 & 1 & 2 \\ 1 & 0 & 1 \end{array} \right )$. Compute its characteristic polynomial, its eigenvalues and its eigenspaces. Is $A$ diagonalizable? If so, find a basis of ${\bf R}^3$ such that the associated matrix is a diagonal matrix, as in <a href="../eigenvalues-diagonalization/#def-diagonalizable" data-reference-type="ref+Label" data-reference="def:diagonalizable">Definition 6.14</a>.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.5</strong></p>

<span id="ex-eigenvalues-5-1" label="ex:eigenvalues-5-1"></span> (See <a href="../solutions-eigenvalues-and-eigenvectors/#sol-ex-eigenvalues-5-1" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-5-1">Solution 6.5</a>.) Let
<div class="arithmatex" markdown="1">
\[
f: {\bf R}^3 \to {\bf R}^3
\]
</div>
be the linear map such that $f(1,0,1)=(2,0,2)$, $\ker f = L((1,1,1))$ and $f(2,0,-3)=(-2,0,3)$. Compute the matrix of $f$ with respect to the standard basis.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.6</strong></p>

<span id="ex-eigenvalues-exercise-004" label="ex:eigenvalues-exercise-004"></span> (See <a href="../solutions-eigenvalues-and-eigenvectors/#sol-ex-eigenvalues-exercise-004" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-exercise-004">Solution 6.6</a>.) For which $a \in {\bf R}$ is the matrix
<div class="arithmatex" markdown="1">
\[
A_a = \left ( \begin{array}{ccc} a & 0 & 0 \\ a-2 & 1 & 1 \\ 0 & 1 & 1 \end{array} \right )
\]
</div>
diagonalizable?

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.7</strong></p>

<span id="ex-eigenvalues-5-2" label="ex:eigenvalues-5-2"></span> (See <a href="../solutions-eigenvalues-and-eigenvectors/#sol-ex-eigenvalues-5-2" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-5-2">Solution 6.7</a>.) For a parameter $a \in {\bf R}$, let
<div class="arithmatex" markdown="1">
\[
A_a = \left ( \begin{array}{ccc} 4 & 0 & 4 \\ a & 2 & a \\ -2 & 0 & -2 \end{array} \right ).
\]
</div>

1.  Compute the characteristic polynomial and the eigenvalues of $A_a$, for all $a \in {\bf R}$.

2.  Compute the values of $a$ for which $A_a$ is diagonalizable. For these $a$, find an invertible matrix $P$ such that $P^{-1} A_a P$ is a diagonal matrix.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.8</strong></p>

<span id="ex-eigenvalues-exercise-005" label="ex:eigenvalues-exercise-005"></span> (See <a href="../solutions-eigenvalues-and-eigenvectors/#sol-ex-eigenvalues-exercise-005" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-exercise-005">Solution 6.8</a>.) Consider the matrices
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{ccc} 1 & 1 & 1 \\ 0 & 2 & 0 \\ 1 & -1 & 1 \end{array} \right ) \ \text{ and } \ B = \left ( \begin{array}{ccc} 2 & 1 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 0 \end{array} \right ).
\]
</div>

1.  Compute the eigenvalues and eigenvectors of $A$ and show $A$ is diagonalizable.

2.  Show that the characteristic polynomials of $A$ and $B$ are the same. Compute the eigenvalues and eigenspaces of $B$. Explain why $A$ and $B$ do *not* represent the same linear map with respect to different bases!

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.9</strong></p>

<span id="ex-eigenvalues-exercise-006" label="ex:eigenvalues-exercise-006"></span> (See <a href="../solutions-eigenvalues-and-eigenvectors/#sol-ex-eigenvalues-exercise-006" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-exercise-006">Solution 6.9</a>.) For a parameter $t \in {\bf R}$, consider the matrix
<div class="arithmatex" markdown="1">
\[
A_t = \left ( \begin{array}{ccc} -1 & 2 & t \\ 2 & 0 & -2 \\ t & -2 & -1 \end{array} \right ).
\]
</div>

1.  For which values of $t$ does $A_t$ have 0 as an eigenvalue?

2.  Compute the eigenvalues and eigenspaces of $A_t$ for those values of $t$ obtained in the previous part.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.10</strong></p>

<span id="ex-eigenvalues-exercise-007" label="ex:eigenvalues-exercise-007"></span> (See <a href="../solutions-eigenvalues-and-eigenvectors/#sol-ex-eigenvalues-exercise-007" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-exercise-007">Solution 6.10</a>.) Consider the space ${\mathrm {Mat}}_{2 \times 2}$ of $2 \times 2$-vector spaces. Consider $A = \left ( \begin{array}{cc} -4 & 8 \\ 1 & -2 \end{array} \right )$ and the map
<div class="arithmatex" markdown="1">
\[
F: {\mathrm {Mat}}_{2 \times 2} \to {\mathrm {Mat}}_{2 \times 2}, X \mapsto AX.
\]
</div>

1.  Is $F$ a linear map? Justify your answer.

2.  Compute the $4 \times 4$-matrix of $F$ with respect to the standard basis of ${\mathrm {Mat}}_{2 \times 2}$, i.e., the matrices
<div class="arithmatex" markdown="1">
\[
    E_{11} = \left ( \begin{array}{cc} 1 & 0 \\ 0 & 0 \end{array} \right ), E_{12} = \left ( \begin{array}{cc} 0 & 1 \\ 0 & 0 \end{array} \right ), E_{21} = \left ( \begin{array}{cc} 0 & 0 \\ 1 & 0 \end{array} \right ), E_{22} = \left ( \begin{array}{cc} 0 & 0 \\ 0 & 1 \end{array} \right ).
\]
</div>

3.  Compute a basis of $\ker F$ and ${\operatorname{im}\ } F$.

4.  Compute the eigenvalues and eigenspaces of $F$.

<div class="remark" markdown="1">


<p class="env-number"><strong>Remark 6.26</strong></p>

<span id="rem-eigenvalues-remark-002" label="rem:eigenvalues-remark-002"></span> The linearity of $F$ is a consequence of <a href="../maps-composing/#lem-matrix-multiplication-properties" data-reference-type="ref+Label" data-reference="lem:matrix-multiplication-properties">Lemma 4.60</a>. It is also very similar to <a href="../maps-multiplication-of-a-matrix/#prop-matrix-linear-map" data-reference-type="ref+Label" data-reference="prop:matrix-linear-map">Proposition 4.19</a>.

</div>

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.11</strong></p>

<span id="ex-eigenvalues-5-4-3" label="ex:eigenvalues-5-4-3"></span> (See <a href="../solutions-eigenvalues-and-eigenvectors/#sol-ex-eigenvalues-5-4-3" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-5-4-3">Solution 6.11</a>.) Consider the two matrices
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{ccc} 1 & 0 & 2 \\ 0 & 3 & 0 \\ 0 & 0 & 3 \end{array} \right ) \text{ and } B = \left ( \begin{array}{ccc} 1 & 0 & 0 \\ 0 & 3 & 2 \\ 0 & 0 & 3 \end{array} \right ).
\]
</div>
Do they represent the same linear map $f : {\bf R}^3 \to {\bf R}^3$ (with respect to different bases)?

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.12</strong></p>

<span id="ex-eigenvalues-5-4-4" label="ex:eigenvalues-5-4-4"></span> (See <a href="../solutions-eigenvalues-and-eigenvectors/#sol-ex-eigenvalues-5-4-4" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-5-4-4">Solution 6.12</a>.) Let $A = \left ( \begin{array}{ccc} 1 & 1 & 1 \\ 0 & 2 & 1 \\ 0 & 0 & 2 \end{array} \right )$. Determine the eigenvalues of $A$ and the corresponding eigenspaces. Is $A$ diagonalizable? Is $A^2$ *similar* to $A$? I.e., does $A^2$ represent the same linear map ${\bf R}^3 \to {\bf R}^3$ as $A$?

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.13</strong></p>

<span id="ex-eigenvalues-5-5" label="ex:eigenvalues-5-5"></span> (See <a href="../solutions-eigenvalues-and-eigenvectors/#sol-ex-eigenvalues-5-5" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-5-5">Solution 6.13</a>.) Consider the vectors $v_1 = (1,0,1)$, $v_2 = (1,1,1)$ and $v_3=(1,1,2)$.

1.  Explain why there is a unique linear map $f : {\bf R}^3 \to {\bf R}^3$ such that $f(v_1)=(0,0,0)$, $f(v_2)=(1,0,3)$ and $v_3$ is an eigenvector of eigenvalue 4.

2.  Compute the matrix $A$ of $f$ with respect to the basis $v_1, v_2, v_3$ (both on the domain and on the codomain).

3.  Compute the matrix $B$ of $f$ with respect to the standard basis (both for the domain and the codomain).

4.  For $t \in {\bf R}$, consider the vector $v_t = (2,t,5)$. For which values of $t$ is $v_t \in {\operatorname{im}\ } f$?

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.14</strong></p>

<span id="ex-eigenvalues-5-7" label="ex:eigenvalues-5-7"></span> (See <a href="../solutions-eigenvalues-and-eigenvectors/#sol-ex-eigenvalues-5-7" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-5-7">Solution 6.14</a>.) Consider the matrix
<div class="arithmatex" markdown="1">
\[
A = \begin{pmatrix}
0 & 2 & t \\
-3 & -5 & 6 \\
-2 & -2 & 5
\end{pmatrix}
\]
</div>

1.  Determine the value of $t$ for which $A$ is *not* invertible.

2.  We now put $t = 2$ for the remainder of this exercise. Determine the value of $a$ for which the vector $v = (2,0,a)$ is an eigenvector of $A$. What is the corresponding eigenvalue?

3.  Determine all the eigenvalues of $A$ and decide whether $A$ is diagonalizable.

4.  Decide whether $A$ is similar to the matrix $A^2$ (justify your response).

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.15</strong></p>

<span id="ex-eigenvalues-5-9" label="ex:eigenvalues-5-9"></span> (See <a href="../solutions-eigenvalues-and-eigenvectors/#sol-ex-eigenvalues-5-9" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-5-9">Solution 6.15</a>.) Consider the matrix
<div class="arithmatex" markdown="1">
\[
A = \begin{pmatrix}
2 & 0 & -1 \\
1 & 1 & 2 \\
-1 & 1 & t
\end{pmatrix}
\]
</div>

1.  Compute the value of $t$ for which the kernel of $A$ is different from $\{0\}$.

2.  For the remainder of the exercise we put $t$ to be equal to the value computed in part (a). Compute the characteristic polynomial and the eigenvalues of $A$.

3.  Find an invertible matrix $P$ such that $P^{-1}AP$ is a diagonal matrix.

4.  Explain why any $3 \times 3$-matrix $B$ such that $\chi_A(t) = \chi_B(t)$ is diagonalizable.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.16</strong></p>

<span id="ex-eigenvalues-5-10" label="ex:eigenvalues-5-10"></span> (See <a href="../solutions-eigenvalues-and-eigenvectors/#sol-ex-eigenvalues-5-10" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-5-10">Solution 6.16</a>.) Consider the matrix $A = \begin{pmatrix}
1 & 0 & t \\
1 & 2 & 1 \\
2 & 0 & -1
\end{pmatrix}$

1.  For what value of $t \in {\bf R}$ is the matrix $A$ *non-*invertible?

2.  For each $t \in {\bf R}$, determine the eigenvalues of $A$. Specify for which values $t \in {\bf R}$ all the eigenvalues of $A$ are real numbers.

3.  Determine for which $t \in {\bf R}$ there are eigenvalues with multiplicity $> 1$.

4.  For the value of $t$ found in the first part of the exercise: compute a basis of all eigenspaces and decide whether $A$ is diagonalizable.

</div>
