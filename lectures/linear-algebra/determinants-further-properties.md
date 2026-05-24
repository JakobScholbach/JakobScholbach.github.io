---
title: Further Properties
---

# Further properties of determinants

<div class="proposition" markdown="1">


<p class="env-number"><strong>Proposition 5.18</strong> (Related exercises: <a href="../exercises-determinants/#ex-determinants-exercise-002">Exercise 5.2</a>, <a href="../exercises-eigenvalues/#ex-eigenvalues-5-4-3">Exercise 6.11</a>)</p>

(*Product formula*) <span id="prop-product-formula" label="prop:product-formula"></span> For two $n \times n$-matrices $A, B$, we have the following formula:
<div class="arithmatex" markdown="1">
\[
\det (AB) = \det A \cdot \det B.
\]
</div>
I.e., the determinant of a product (of square matrices of the same size) is the product of the two individual determinants.

</div>

In particular, this shows
<div class="arithmatex" markdown="1">
\[
\det (AB) = \det (BA),
\]
</div>
even though $AB \ne BA$!

<div class="proof" markdown="1">

*Proof.* We don’t include a full proof, but only observe that one checks this by direct computation when $A$ is an elementary matrix. This implies the formula if $A$ is invertible, since then $A$ is a product of elementary matrices. If $A$ is not invertible, then one shows that $AB$ is also not invertible (for any $B$), and therefore both $\det A = 0$ and $\det (AB) = 0$, so the formula holds in this case too. See, e.g., (Nicholson 1995, Theorem 3.2.1) for a proof. ◻

</div>

<div class="remark" markdown="1">


<p class="env-number"><strong>Remark 5.19</strong></p>

<span id="rem-determinants-remark-004" label="rem:determinants-remark-004"></span> The determinant is therefore multiplicative, but it is *not* additive: one has
<div class="arithmatex" markdown="1">
\[
\det (A + B) \ne \det A + \det B,
\]
</div>
e.g.
<div class="arithmatex" markdown="1">
\[
\det \left ( \begin{array}{cc} 2 & 0 \\ 0 & 2 \end{array} \right ) = 4 \ne 1 + 1 = \det \left ( \begin{array}{cc} 1 & 0 \\ 0 & 1 \end{array} \right ) + \det \left ( \begin{array}{cc} 1 & 0 \\ 0 & 1 \end{array} \right ).
\]
</div>

</div>

<div class="proposition" markdown="1">


<p class="env-number"><strong>Proposition 5.20</strong> (Related exercises: <a href="../exercises-determinants/#ex-determinants-4-1">Exercise 5.5</a>, <a href="../exercises-determinants/#ex-determinants-exercise-005">Exercise 5.7</a>)</p>

<span id="prop-det-triangular-matrix" label="prop:det-triangular-matrix"></span> Let $A$ be an *upper triangular matrix* or a *lower triangular matrix*, i.e., of the form
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{cccc} a_{11} & * & \dots & * \\ 0 & \ddots & \ddots & \vdots \\ \vdots & \ddots & \ddots & * \\ 0 & \dots & 0 & a_{nn} \end{array} \right ),
\]
</div>
resp.
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{cccc} a_{11} & 0 & \dots & 0 \\ * & \ddots & \ddots & \vdots \\ \vdots & \ddots & \ddots & \vdots \\ * & \dots & * & a_{nn} \end{array} \right ).
\]
</div>
Here \* stands for an arbitrary entry. Then
<div class="arithmatex" markdown="1">
\[
\det A = a_{11} \cdot \dots \cdot a_{nn}.
\]
</div>

</div>

<div class="proof" markdown="1">

*Proof.* If one of the entries on the main diagonal, i.e., $a_{11}, \dots, a_{nn}$ is zero, then the columns of $A$ are linearly dependent, so that $A$ is not invertible and $\det A = 0$. If instead all $a_{ii} \ne 0$, we can divide the $i$-th row by $a_{ii}$, and assume the entries on the main diagonal are all 1. Then, adding appropriate multiples of the rows to the rows above (resp. below in the case of a lower triangular matrix), which does not affect the determinant, gives $A \leadsto {\mathrm {id}}$, so that $\det A = 1$, so the claim holds in this case. ◻

</div>

<div class="proposition" markdown="1">


<p class="env-number"><strong>Proposition 5.21</strong></p>

<span id="prop-determinants-proposition-003" label="prop:determinants-proposition-003"></span> For $A \in {\mathrm {Mat}}_{n \times n}$, we have
<div class="arithmatex" markdown="1">
\[
\det A = \det (A^T),
\]
</div>
i.e., the determinant does not change when passing from $A$ to its transpose (<a href="../maps-transpose/#def-transpose" data-reference-type="ref+Label" data-reference="def:transpose">Definition 4.89</a>).

</div>

<div class="proof" markdown="1">

*Proof.* For small matrices (of size at most $3 \times 3$), this can be proved directly from the formulae in §<a href="../determinants-determinants-of-larger-matrices/#sect-small-matrices" data-reference-type="ref" data-reference="sect--small matrices">Subsection 5.2.1</a>.

In general, one may argue like this: if $A$ is not invertible, then $A^T$ is not invertible either (by <a href="../maps-transpose/#lem-properties-transposition" data-reference-type="ref+Label" data-reference="lem:properties-transposition">Lemma 4.91</a>). In this case, both sides of the equation are zero. If $A$ is invertible, it is a product of elementary matrices: $A = U_1 \dots U_n$. We then have $A^T = U_n^T \dots U_1^T$. By the product formula (<a href="#prop-product-formula" data-reference-type="ref+Label" data-reference="prop:product-formula">Proposition 5.18</a>), we may therefore assume $A$ is an elementary matrix. In this case, one checks the claim by inspection:

- for $A = \left ( \begin{array}{ccccccc} 1 & & & & & & \\ & \ddots & & & & & \\ & & 0 & & 1 & & \\ & & & \ddots & & & \\ & & 1 & & 0 & & \\ & & & & & \ddots & \\ & & & & & & 1 \end{array} \right )$, we have $A^T = A$, so the claim clearly holds.

- Likewise, for $A = \left ( \begin{array}{ccccccc} 1 & & & & & & \\ & \ddots & & & & & \\ & & 1 & & & & \\ & & & r & & & \\ & & & & 1 & & \\ & & & & & \ddots & \\ & & & & & & 1 \end{array} \right )$, we have $A = A^T$, so again the claim holds obviously.

- The matrix ${\left ( \begin{array}{ccccccc} 1 & & & & & & \\ & \ddots & & & & & \\ & & 1 & & & & \\ & & & \ddots & & & \\ & & r & & 1 & & \\ & & & & & \ddots & \\ & & & & & & 1 \end{array} \right )}$ is a lower triangular matrix, and its transpose an upper triangular matrix. Both have determinant 1 according to <a href="#prop-det-triangular-matrix" data-reference-type="ref+Label" data-reference="prop:det-triangular-matrix">Proposition 5.20</a>.

 ◻

</div>

<div class="remark" markdown="1">


<p class="env-number"><strong>Remark 5.22</strong></p>

<span id="rem-determinants-remark-005" label="rem:determinants-remark-005"></span> We introduced the determinant using *row* operations. The preceding result implies that one can replace the word “row” in all of the above by the word “column”. Applying that, say, to <a href="../determinants-determinants-of-larger-matrices/#rem-det-zero-equal-rows" data-reference-type="ref+Label" data-reference="rem:det-zero-equal-rows">Remark 5.9</a> we obtain that $\det A = 0$ if $A$ has two identical columns.

</div>

<div class="proposition" markdown="1">


<p class="env-number"><strong>Proposition 5.23</strong> (Related exercises: <a href="../exercises-determinants/#ex-determinants-exercise-004">Exercise 5.4</a>, <a href="../exercises-eigenvalues/#ex-eigenvalues-5-10">Exercise 6.16</a>, <a href="../exercises-eigenvalues/#ex-eigenvalues-5-2">Exercise 6.7</a>, <a href="../exercises-eigenvalues/#ex-eigenvalues-exercise-001">Exercise 6.1</a>, <a href="../exercises-eigenvalues/#ex-eigenvalues-exercise-006">Exercise 6.9</a>)</p>

<span id="prop-cofactor-expansion" label="prop:cofactor-expansion"></span> Let $A  = (a_{ij}) \in {\mathrm {Mat}}_{n \times n}$. Then, for any $i$, one can compute the determinant using “*cofactor expansion*” along the $i$-th row. That is, the following identity holds, where $c_{ij}$ are the cofactors of $A$ (<a href="../determinants-invertibility-and-determinants/#def-cofactors" data-reference-type="ref+Label" data-reference="def:cofactors">Definition 5.14</a>):
<div class="arithmatex" markdown="1">
\[
\det A = a_{i1} c_{i1} + \dots + a_{in} c_{in}.
\]
</div>
Similarly, one can compute it using cofactor expansion along the $j$-th column, for any $j$:
<div class="arithmatex" markdown="1">
\[
\det A = a_{1j} c_{1j} + \dots + a_{nj} c_{nj}.
\]
</div>

</div>

For a proof of this, see, e.g. (Nicholson 1995, sec. 3.6).

<div class="example" markdown="1">


<p class="env-number"><strong>Example 5.24</strong></p>

<span id="ex-determinants-example-003" label="ex:determinants-example-003"></span> For example, we expand the determinant along the second row:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\det \left ( \begin{array}{ccc} 2 & 3 & 7 \\ -4 & 0 & 6 \\ 1 & 5 & 0 \end{array} \right ) & = a_{21} c_{21} + a_{22} c_{22} + a_{23} c_{23} \\
& = (-4) (-1)^{1+2} \det \left ( \begin{array}{cc} 3 & 7 \\ 5 & 0 \end{array} \right ) + 0 (-1)^{2+2} \det \left ( \begin{array}{cc} 2 & 7 \\ 1 & 0 \end{array} \right ) \\
& + 6 (-1)^{2+3} \det \left ( \begin{array}{cc} 2 & 3 \\ 1 & 5 \end{array} \right ) \\
& = 4 \cdot (-35) + 0 - 6 \cdot 7 \\
& = -182.
\end{align*}
\]
</div>
The choice of the second row (as opposed to the others) is arbitrary, and the result is the same if we choose another row. However, the presence of the $a_{22} = 0$ simplifies the computation.

</div>

<div id="refs" class="references csl-bib-body hanging-indent">

<div id="ref-Nicholson:Linear" class="csl-entry">

Nicholson, W. K. 1995. *Linear Algebra with Applications*. Mathematics Series. PWS Publishing Company. <https://lyryx.com/linear-algebra-applications/>.

</div>

</div>
