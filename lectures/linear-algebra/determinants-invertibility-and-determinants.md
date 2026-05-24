---
title: Invertibility and Determinants
---

# Invertibility and determinants

We can use the properties of the determinant in <a href="../determinants-determinants-of-larger-matrices/#thm-det-universal-property" data-reference-type="ref+Label" data-reference="thm:det-universal-property">Theorem 5.5</a> (and its proof) to obtain a useful criterion to decide when a matrix is invertible. Determinants can also be used to compute the inverse of an invertible matrix, however this is only of theoretical significance due to the complexity of the ensuing (iterative) algorithm.

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 5.14</strong> (Related exercises: <a href="../exercises-determinants/#ex-determinants-exercise-001">Exercise 5.1</a>)</p>

<span id="def-cofactors" label="def:cofactors"></span> Let $A \in {\mathrm {Mat}}_{n \times n}$. For $1 \le i, j \le n$, denote by $A_{ij}$ that is obtained from $A$ by deleting the $i$-th row and the $j$-th column. The number
<div class="arithmatex" markdown="1">
\[
c_{ij} := (-1)^{i+j} \det A_{ij}
\]
</div>
is called the $(i,j)$-*cofactor* of $A$.

The *adjugate* of $A$ is the $n \times n$-matrix defined as
<div class="arithmatex" markdown="1">
\[
\mathrm{adj}(A) = (c_{ij}(A))^T = (c_{ji}(A)).
\]
</div>

</div>

<div class="theorem" markdown="1">


<p class="env-number"><strong>Theorem 5.15</strong> (Related exercises: <a href="../exercises-determinants/#ex-determinants-4-2">Exercise 5.6</a>, <a href="../exercises-determinants/#ex-determinants-exercise-001">Exercise 5.1</a>, <a href="../exercises-determinants/#ex-determinants-exercise-003">Exercise 5.3</a>, <a href="../exercises-determinants/#ex-determinants-exercise-006">Exercise 5.8</a>, <a href="../exercises-eigenvalues/#ex-eigenvalues-5-7">Exercise 6.14</a>)</p>

<span id="thm-det-zero-niff-invertible" label="thm:det-zero-niff-invertible"></span> An $n \times n$-matrix $A$ is invertible if and only if
<div class="arithmatex" markdown="1">
\[
\det A \ne 0.
\]
</div>
If this is the case, then the inverse can be computed using the so-called *adjugate formula*:
<div class="arithmatex" markdown="1">
\[
A^{-1} = \frac 1 {\det A} \mathrm{adj}(A).
\]
</div>

<p class="env-number equation-number"><strong>(5.16)</strong></p>

<span id="eqn-eqn-adjugate-formula" label="eqn--eqn:adjugate-formula"></span>

</div>

<div class="proof" markdown="1">

*Proof.* We revisit the proof of <a href="../determinants-determinants-of-larger-matrices/#thm-det-universal-property" data-reference-type="ref+Label" data-reference="thm:det-universal-property">Theorem 5.5</a>: say $A \leadsto A'$, a reduced row echelon matrix, by means of elementary operations (Gaussian elimination). In this process, one does not multiply any row by zero, so that $\det A = 0$ if and only if $\det A' = 0$. We also know that $A' = UA$, where $U$ is an invertible matrix (namely, a product of elementary matrices). Moreover, $A'$ is invertible if and only if $A$ is invertible (since $U$ is invertible). We therefore have
<div class="arithmatex" markdown="1">
\[
A \text{ is invertible} \Leftrightarrow A' \text{ is invertible} \stackrel ? \Leftrightarrow \det A' \ne 0 \Leftrightarrow \det A \ne 0
\]
</div>
and it remains to show the middle equivalence.

The matrix $A'$ is in reduced row echelon form. Thus, either $A' = {\mathrm {id}}$ or $A'$ contains a zero row. In the first event, $A'$ is invertible, and $\det A' = 1 \ne 0$. In the second event, $A'$ is not invertible (by <a href="../maps-transpose/#cor-rows-columns-independent" data-reference-type="ref+Label" data-reference="cor:rows-columns-independent">Corollary 4.94</a>) and $\det A' = 0$ as was noted around .

We skip the proof of the adjugate formula, cf. (Nicholson 1995, Theorem 3.2.4). ◻

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 5.17</strong> (Related exercises: <a href="../exercises-determinants/#ex-determinants-exercise-006">Exercise 5.8</a>)</p>

<span id="ex-determinants-example-002" label="ex:determinants-example-002"></span> For a $2 \times 2$-matrix $A = \left ( \begin{array}{cc} a & b \\ c & d \end{array} \right )$, the adjugate matrix is
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cc} d & -b \\ -c & a \end{array} \right ).
\]
</div>
Therefore, the inverse can be computed as
<div class="arithmatex" markdown="1">
\[
A^{-1} = \frac 1 {ad-bc} \left ( \begin{array}{cc} d & -b \\ -c & a \end{array} \right ).
\]
</div>

</div>

<div id="refs" class="references csl-bib-body hanging-indent">

<div id="ref-Nicholson:Linear" class="csl-entry">

Nicholson, W. K. 1995. *Linear Algebra with Applications*. Mathematics Series. PWS Publishing Company. <https://lyryx.com/linear-algebra-applications/>.

</div>

</div>
