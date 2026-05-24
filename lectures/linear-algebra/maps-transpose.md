---
title: Transposition
---

# Transposition of matrices

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 4.89</strong> (Related exercises: <a href="../exercises-maps/#ex-maps-exercise-017">Exercise 4.23</a>, <a href="../exercises-maps/#trace">Exercise 4.24</a>)</p>

<span id="def-transpose" label="def:transpose"></span> If $A$ is an $m \times n$-matrix, then the *transpose* (denoted $A^T$) is the $n \times m$-matrix obtained by $A$ by reflecting the entries along the main diagonal. More formally, if $A = (a_{ij})$, then
<div class="arithmatex" markdown="1">
\[
A^T := (a_{ji}).
\]
</div>

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 4.90</strong></p>

<span id="ex-maps-example-030" label="ex:maps-example-030"></span> For $A = \left ( \begin{array}{cc} 1 & 2 \\ 3 & 4 \\ 5 & 6 \end{array} \right )$,
<div class="arithmatex" markdown="1">
\[
A^T = \left ( \begin{array}{ccc} 1 & 3 & 5 \\ 2 & 4 & 6 \end{array} \right ).
\]
</div>
The transpose of a column vector is a row vector and vice versa. For example, for $v = \left ( \begin{array}{c} x \\ y \end{array} \right )$,
<div class="arithmatex" markdown="1">
\[
v^T = \left ( \begin{array}{cc} x & y \end{array} \right ).
\]
</div>

</div>

We have the following basic computation rules involving the transpose.

<div class="lemma" markdown="1">


<p class="env-number"><strong>Lemma 4.91</strong> (Related exercises: <a href="../exercises-maps/#ex-maps-exercise-017">Exercise 4.23</a>)</p>

<span id="lem-properties-transposition" label="lem:properties-transposition"></span> Let $A$ be an $m \times n$-matrix and $r \in {\bf R}$ a real number.

1.  $(A^T)^T = A$, i.e., the transpose of the transpose equals the original matrix,

2.  For another matrix $B$ of the same size as $A$, $(A + B)^T = A^T + B^T$.

3.  For an $n \times k$-matrix $B$, the transpose of the matrix product $AB$ is the products of the transposes *in the opposite order*:
<div class="arithmatex" markdown="1">
\[
    (AB)^T = B^T A^T.
\]
</div>

<p class="env-number equation-number"><strong>(4.92)</strong></p>

<span id="eqn-transpose-product" label="eqn--transpose.product"></span>

4.  If a square matrix $A$ is invertible, then $A^T$ is also invertible with inverse
<div class="arithmatex" markdown="1">
\[
    (A^T)^{-1} = (A^{-1})^T.
\]
</div>

<p class="env-number equation-number"><strong>(4.93)</strong></p>

<span id="eqn-transpose-inverse" label="eqn--transpose.inverse"></span>

</div>

<div class="proof" markdown="1">

*Proof.* The first two rules are quite immediate to check (and hardly surprising). The first one can also be seen by noting that doing twice the reflection of the entries along the main diagonal gives back the original matrix.

The equation is also directly following from the definitions: let $A = (a_{ij})$, $B = (b_{ij})$. Let us write $C = AB = (c_{ij})$. Then $c_{ij} = \sum_{e=1}^n a_{ie} b_{ej}$. Thus $C^T = (c_{ji}) = \sum_{e=1}^n a_{je} b_{ei}$. This equals the $(i,j)$-entry of $B^T A^T$.

For , we compute using :
<div class="arithmatex" markdown="1">
\[
\begin{align*}
A^T (A^{-1})^T  & = (A^{-1} A)^T \\
& = {\mathrm {id}}^T \\
& = {\mathrm {id}}.
\end{align*}
\]
</div>
Similarly, again using by :
<div class="arithmatex" markdown="1">
\[
\begin{align*}
(A^{-1})^T A^T & = (A A^{-1})^T \\
& = {\mathrm {id}}^T \\
& = {\mathrm {id}}.
\end{align*}
\]
</div>
Thus the product of $A^T$ and $(A^{-1})^T$ (in the two possible orders) equals ${\mathrm {id}}$, so they are inverse to each other. ◻

</div>

The usage of transposes helps us prove another set of equivalent characterizations:

<div class="corollary" markdown="1">


<p class="env-number"><strong>Corollary 4.94</strong> (Related exercises: <a href="../exercises-maps/#ex-maps-exercise-013">Exercise 4.14</a>)</p>

<span id="cor-rows-columns-independent" label="cor:rows-columns-independent"></span> Let $A \in {\mathrm {Mat}}_{n \times n}$ be a square matrix. Then the following are equivalent:

1.  <span id="item-a-inv" label="item--A inv"></span> $A$ is invertible.

2.  <span id="item-col-lin-indep" label="item--col lin indep"></span> The $n$ columns of $A$ are linearly independent.

3.  <span id="item-col-rank" label="item--col rank"></span> The rank of $A$ is $n$.

4.  <span id="item-row-lin-indep" label="item--row lin indep"></span> The $n$ rows of $A$ are linearly independent.

</div>

<div class="proof" markdown="1">

*Proof.* <a href="#item-a-inv" data-reference-type="ref" data-reference="item--A inv">1.</a> $\Leftrightarrow$ <a href="#item-col-lin-indep" data-reference-type="ref" data-reference="item--col lin indep">2.</a>: According to <a href="../maps-inverses/#thm-invertible-elimination" data-reference-type="ref+Label" data-reference="thm:invertible-elimination">Theorem 4.81</a>, $A$ is invertible precisely if the only solution to the system $Ax = 0$ is the zero vector $x = 0$. Recalling that for $x = \left ( \begin{array}{c} x_1 \\ \vdots \\ x_n \end{array} \right )$ we have
<div class="arithmatex" markdown="1">
\[
Ax = x_1 c_1 + \dots + x_n c_n,
\]
</div>
where $A = (c_1 \ \dots \ c_n)$ are the columns of $A$, we see that the above condition is equivalent to the columns being linearly independent.

<a href="#item-col-lin-indep" data-reference-type="ref" data-reference="item--col lin indep">2.</a> $\Leftrightarrow$ <a href="#item-col-rank" data-reference-type="ref" data-reference="item--col rank">3.</a>: The rank is, by definition, the dimension of the column space, i.e., the subspace of ${\bf R}^n$ generated by the columns $c_1, \dots, c_n$. In order to show that these vectors span ${\bf R}^n$, let $b \in {\bf R}^n$. By the invertibility of $A$, we know that the system $Ax = b$ has a (unique) solution $x$. Therefore $Ax = \sum_{k=1}^n x_i c_i = b$.

<a href="#item-a-inv" data-reference-type="ref" data-reference="item--A inv">1.</a> $\Leftrightarrow$ <a href="#item-row-lin-indep" data-reference-type="ref" data-reference="item--row lin indep">4.</a>: $A$ is invertible if and only if the transpose $A^T$ is invertible. Now use that the rows of $A^T$ are the columns of $A$, and apply the (already proved) equivalence <a href="#item-a-inv" data-reference-type="ref" data-reference="item--A inv">1.</a> $\Leftrightarrow$ <a href="#item-col-lin-indep" data-reference-type="ref" data-reference="item--col lin indep">2.</a>. ◻

</div>
