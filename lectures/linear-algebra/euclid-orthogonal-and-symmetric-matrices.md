---
title: Orthogonal and Symmetric Matrices
---

# Orthogonal and symmetric matrices

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 7.36</strong></p>

<span id="def-euclid-definition-007" label="def:euclid-definition-007"></span> A real square matrix $A \in {\mathrm {Mat}}_{n \times n}$ is called *orthogonal* if
<div class="arithmatex" markdown="1">
\[
AA^T = {\mathrm {id}}.
\]
</div>

</div>

This is equivalent to saying that $A$ is invertible and $A^{-1} = A^T$. The following lemma explains the name “orthogonal”.

<div class="lemma" markdown="1">


<p class="env-number"><strong>Lemma 7.37</strong></p>

<span id="lem-euclid-lemma-004" label="lem:euclid-lemma-004"></span> For a square matrix $A \in {\mathrm {Mat}}_{n \times n}$, the following are equivalent:

1.  $A$ is orthogonal,

2.  the $n$ rows are an orthonormal basis of ${\bf R}^n$,

3.  the $n$ columns are an orthonormal basis of ${\bf R}^n$.

</div>

<div class="proof" markdown="1">

*Proof.* If $e_i$ is the $i$-th standard basis vector, we know that $Ae_i$ is the $i$-th column $A$. We compute
<div class="arithmatex" markdown="1">
\[
{\left \langle Ae_i, Ae_j \right \rangle} = (Ae_i)^T(Ae_j) = e_i^T A^T A e_j.
\]
</div>

The vector $A^T A e_j$ is the $j$-th column of $A^T A$, and the number $e_i^T A^T A e_j$ is the $i$-th entry of that vector. Thus, saying that the above expression equals 1 for $i=j$ and 0 otherwise is equivalent to requiring $A^T A = {\mathrm {id}}$. ◻

</div>

<div class="theorem" markdown="1">


<p class="env-number"><strong>Theorem 7.38</strong> (Related exercises: <a href="../exercises-euclid/#ex-euclid-6-10">Exercise 7.11</a>)</p>

<span id="thm-symmetric-orthogonally-diagonalizable" label="thm:symmetric-orthogonally-diagonalizable"></span> The following conditions are equivalent for an $n \times n$-matrix $A$:

1.  <span id="item-a-symmetric" label="item--A.symmetric"></span> $A$ is symmetric,

2.  <span id="item-a-orthdia" label="item--A.orthdia"></span> $A$ is *orthogonally diagonalizable*, i.e., there is an *orthogonal matrix* $P$ such that $P^{-1}AP$ is a diagonal matrix,

3.  $A$ has an orthonormal eigenbasis.

If these equivalent conditions hold, then the columns of $P$ form an orthonormal eigenbasis and vice versa. (Note that $P^{-1} = P^T$ can be computed without computing, properly speaking, the inverse of $P$.)

</div>

The implication <a href="#item-a-symmetric" data-reference-type="ref" data-reference="item--A.symmetric">1.</a> $\Rightarrow$ <a href="#item-a-orthdia" data-reference-type="ref" data-reference="item--A.orthdia">2.</a> in particular says:
<div class="arithmatex" markdown="1">
\[
A \text{ symmetric} \Rightarrow A \text{ diagonalizable}.
\]
</div>

For a proof of this theorem, see, e.g. (Nicholson 1995, Theorem 8.2.2). The vectors of an orthonormal eigenbasis are also called the *principal axes* of $A$. The theorem is sometimes called the *principal axes theorem*. We only point out that the difficult direction is to show that <a href="#item-a-symmetric" data-reference-type="ref" data-reference="item--A.symmetric">1.</a> $\Rightarrow$ <a href="#item-a-orthdia" data-reference-type="ref" data-reference="item--A.orthdia">2.</a>. One does this by proving that a *symmetric* real matrix has only real eigenvalues (as opposed to complex). For $2 \times 2$-matrices, one can see this by direct computation (see also <a href="../exercises-eigenvalues/#exercise-eigenvalues-2x2" data-reference-type="ref+Label" data-reference="exercise.eigenvalues.2x2">Exercise 6.2</a>): the characteristic polynomial of a symmetric $2 \times 2$-matrix $A = \left ( \begin{array}{cc} a & b \\ b & d \end{array} \right )$ is
<div class="arithmatex" markdown="1">
\[
\chi_A(t) = \det (A-t{\mathrm {id}}) = (a-t)(d-t) - b^2 = t^2 + (-a-d) t + ad-b^2.
\]
</div>
The zeroes of this polynomial are given by
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\lambda_{1/2} & = \frac{a+d}2 \pm \sqrt{\frac{(a+d)^2}4-ad+b^2} \\
& = \frac{a+d}2 \pm \sqrt{\frac{a^2 + d^2}4 + \frac{ad}2 - ad + b^2} \\
& = \frac{a+d}2 \pm \sqrt{\frac{(a-d)^2}4 + b^2}.
\end{align*}
\]
</div>
The expression in the square root is always non-negative, so that $\lambda_{1/2}$ are real numbers.

As an example of a non-symmetric matrix with imaginary eigenvalues, we have seen in <a href="../eigenvalues-diagonalization/#ex-rotation-matrix-eigenvalues" data-reference-type="ref+Label" data-reference="ex:rotation-matrix-eigenvalues">Example 6.21</a> that the matrix $A = \left ( \begin{array}{cc} 0 & -1 \\ 1 & 0 \end{array} \right )$ has the eigenvalues $\lambda_{1/2} = \pm i$.

<div class="example" markdown="1">


<p class="env-number"><strong>Example 7.39</strong></p>

<span id="ex-euclid-example-011" label="ex:euclid-example-011"></span> The matrix $A = \left ( \begin{array}{ccc} 5 & -4 & 2 \\ -4 & 5 & 2 \\ 2 & 2 & -1 \end{array} \right )$ is symmetric. We compute an orthonormal eigenbasis by first computing the eigenvalues:
<div class="arithmatex" markdown="1">
\[
\chi_A(t) = -t^3 + 9 t^2 + 9 t - 81.
\]
</div>
The eigenvalues and an eigenvector for them are as follows:

- $\lambda_1 = 9$, $v_1 = (-1,1,0)$,

- $\lambda_2 = 3$, $v_2 = (1,1,1)$,

- $\lambda_3 = -3$, $v_3 = (-1,-1,2)$.

These three vectors are orthogonal; this is seen by direct computation. Alternatively, since the eigenvalues are all distinct, they are automatically orthogonal (<a href="../exercises-euclid/#eigenvectors-orthogonal" data-reference-type="ref+Label" data-reference="eigenvectors.orthogonal">Exercise 7.12</a>). They are however not normal, dividing by their norm gives an orthonormal eigenbasis:
<div class="arithmatex" markdown="1">
\[
\frac 1{\sqrt 2} \left ( \begin{array}{c} -1 \\ 1 \\ 0 \end{array} \right ), \frac1{\sqrt 3} \left ( \begin{array}{c} 1 \\ 1 \\ 1 \end{array} \right ), \frac1{\sqrt 6} \left ( \begin{array}{c} 1 \\ 1 \\ -2 \end{array} \right ).
\]
</div>

</div>

<div id="refs" class="references csl-bib-body hanging-indent">

<div id="ref-Nicholson:Linear" class="csl-entry">

Nicholson, W. K. 1995. *Linear Algebra with Applications*. Mathematics Series. PWS Publishing Company. <https://lyryx.com/linear-algebra-applications/>.

</div>

</div>
