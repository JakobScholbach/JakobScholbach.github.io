---
title: Determinants
---

# Determinants

## Determinants of $2 \times 2$-matrices

We begin with the definition of determinants of $2 \times 2$-matrices.

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 5.1</strong></p>

<span id="def-det-2-x-2" label="def:det-2-x-2"></span> Let
<div class="arithmatex" markdown="1">
\[
A  = \left ( \begin{array}{cc} a & b \\ c & d \end{array} \right )
\]
</div>
be a $2 \times 2$-matrix. The *determinant* of $A$ is defined as
<div class="arithmatex" markdown="1">
\[
\det A := ad - bc.
\]
</div>

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 5.2</strong></p>

<span id="ex-determinants-example-001" label="ex:determinants-example-001"></span>

- $\det \left ( \begin{array}{cc} 4 & 7 \\ 2 & -1 \end{array} \right ) = 4 \cdot (-1) - 7 \cdot 2 = -18$.

- $\det \left ( \begin{array}{cc} 1 & r \\ 0 & 1 \end{array} \right ) = 1 \cdot 1 - r \cdot 0 = 1$. In particular, $\det {\mathrm {id}}_2 = 1$.

- Consider a matrix $A = \left ( \begin{array}{cc} a & b \\ ra & rb \end{array} \right )$ whose second column is a multiple of the first (so that the columns are linearly dependent). Then
<div class="arithmatex" markdown="1">
\[
  \det \left ( \begin{array}{cc} a & b \\ ra & rb \end{array} \right ) = a rb - bra = 0.
\]
</div>
  According to <a href="../maps/#cor-rows-columns-independent" data-reference-type="ref+Label" data-reference="cor:rows-columns-independent">Corollary 4.94</a>, $A$ is *not* invertible. This is an example of the fact alluded to above (cf. <a href="#thm-det-zero-niff-invertible" data-reference-type="ref+Label" data-reference="thm:det-zero-niff-invertible">Theorem 5.15</a>).

</div>

Determinants carry the following geometric meaning. Recall that the *absolute value* of a real number $r$ is defined as
<div class="arithmatex" markdown="1">
\[
|r| := \left \{ \begin{array}{ll} r & r \ge 0 \\ -r & r < 0. \end{array} \right .
\]
</div>
For example, $|4| = 4$ and $|-5| = 5$.

<div class="lemma" markdown="1">


<p class="env-number"><strong>Lemma 5.3</strong></p>

<span id="lem-abs-val-det" label="lem:abs-val-det"></span> Let
<div class="arithmatex" markdown="1">
\[
A = (v \ v') = \left ( \begin{array}{cc} x & x' \\ y & y' \end{array} \right )
\]
</div>
be a $2 \times 2$-matrix, where $v$ and $v' \in {\bf R}^2$ are the two columns of $A$. Then
<div class="arithmatex" markdown="1">
\[
| \det (A) | = \text{area}(v_1, v_2),
\]
</div>
where the right hand side denotes the area of the parallelogram spanned by the two vectors $v_1, v_2$.

</div>

<div class="proof" markdown="1">

*Proof.* We illustrate this geometrically in the case where all entries of $A$ are positive and the vectors $v$ and $v'$ lie as depicted, i.e., the angle from $v$ to $v'$ goes, informally speaking, counterclockwise. The area of the black rectangle is $(x+x')(y+y')$. The area of the two triangles whose long side is $v$ (resp. parallel to it), is $\frac{xy}2$, so the area of these two triangles together is $xy$. Likewise the total area of the triangles (parallel to) $v'$ is $x'y'$. Finally, the area of the rectangle at the bottom right, resp. top left corner of the large rectangle is $x'y$. Therefore, the area of the parallelogram is
<div class="arithmatex" markdown="1">
\[
\begin{align*}
(x+x')(y+y') - xy - x'y' - 2x'y & = xy+x'y+xy'+x'y'-xy-x'y'-2x'y \\ & = xy' - x'y \\ &= \det A.
\end{align*}
\]
</div>

<div class="center" markdown="1">

![image](figures/png/determinants/determinants-fig-01.png)

</div>

 ◻

</div>

<a href="#lem-abs-val-det" data-reference-type="ref+Label" data-reference="lem:abs-val-det">Lemma 5.3</a> does not give any information about the sign of the determinant. Regarding that, we observe the following:

<div class="lemma" markdown="1">


<p class="env-number"><strong>Lemma 5.4</strong></p>

<span id="lem-swap-2-x-2" label="lem:swap-2-x-2"></span> Let $A = \left ( \begin{array}{cc} x_1 & x_2 \\ y_1 & y_2 \end{array} \right )$ and let
<div class="arithmatex" markdown="1">
\[
\begin{align*}
A' & := \left ( \begin{array}{cc} x_2 & x_1 \\ y_2 & y_1 \end{array} \right )\\
A'' &:= \left ( \begin{array}{cc} y_1 & y_2 \\ x_1 & x_2 \end{array} \right )
\end{align*}
\]
</div>
be the matrices obtained from $A$ by swapping the two columns, resp. the two rows. Then
<div class="arithmatex" markdown="1">
\[
\det A'' = \det A' = - \det A.
\]
</div>
In other words, swapping two rows or two columns will change the sign of the determinant.

</div>

<div class="proof" markdown="1">

*Proof.* This is directly clear from the definition. For example,
<div class="arithmatex" markdown="1">
\[
\det A' = x_2 y_1 - y_2 x_1 = -(x_1 y_2 - x_2 y_1) = - \det A.
\]
</div>
 ◻

</div>

Thus, the determinant (as opposed to only its absolute value) records the area of the parallelogram spanned by the vectors and also the orientation.

## Determinants of larger matrices

There are various (equivalent) approaches to defining determinants of larger matrices. The following one is satisfactory from both a conceptual and a practical standpoint.

<div class="theorem" markdown="1">


<p class="env-number"><strong>Theorem 5.5</strong></p>

<span id="thm-det-universal-property" label="thm:det-universal-property"></span> There is a *unique* function, called the *determinant*,
<div class="arithmatex" markdown="1">
\[
\det : {\mathrm {Mat}}_{n \times n} \to {\bf R}
\]
</div>
with the following properties (throughout $A \in {\mathrm {Mat}}_{n \times n})$:

1.  $\det ({\mathrm {id}}_n) = 1$,

2.  If $A'$ results from $A$ by interchanging two rows, then
<div class="arithmatex" markdown="1">
\[
    \det(A') = -\det(A).
\]
</div>

<p class="env-number equation-number"><strong>(5.6)</strong></p>

<span id="eqn-det-alternating" label="eqn--det alternating"></span>

3.  Let us write a matrix as $\left ( \begin{array}{c} v_1 \\ \vdots \\ v_n \end{array} \right )$, i.e., $v_i \in {\bf R}^n$ is the $i$-th row of the matrix. Then for any $w \in {\bf R}^n$ and any $r \in {\bf R}$:
<div class="arithmatex" markdown="1">
\[
    \det (\left ( \begin{array}{c} v_1 \\ \vdots \\ r v_i + w \\ \vdots \\ v_n \end{array} \right )) = 
        r \det (\left ( \begin{array}{c} v_1 \\ \vdots \\ v_i \\ \vdots \\ v_n \end{array} \right )) + 
        \det (\left ( \begin{array}{c} v_1 \\ \vdots \\ w \\ \vdots \\ v_n \end{array} \right )).
\]
</div>

</div>

<div class="remark" markdown="1">


<p class="env-number"><strong>Remark 5.7</strong></p>

<span id="rem-determinants-remark-001" label="rem:determinants-remark-001"></span> The above operations are somewhat like elementary operations (<a href="../systems-gaussian-elimination/#def-elementary-row-operations" data-reference-type="ref+Label" data-reference="def:elementary-row-operations">Definition 2.28</a>): if we take $w = 0$ above, then the formula says that multiplying any one row by $r$ (which may be zero, unlike in <a href="../systems-gaussian-elimination/#def-elementary-row-operations" data-reference-type="ref+Label" data-reference="def:elementary-row-operations">Definition 2.28</a>), then the determinant also gets multiplied by $r$. In particular, if $A$ has a zero row, then
<div class="arithmatex" markdown="1">
\[
\det A = 0.
\]
</div>

<p class="env-number equation-number"><strong>(5.8)</strong></p>

<span id="eqn-det-zero-row" label="eqn--det zero row"></span>

</div>

<div class="remark" markdown="1">


<p class="env-number"><strong>Remark 5.9</strong></p>

<span id="rem-det-zero-equal-rows" label="rem:det-zero-equal-rows"></span> We also have
<div class="arithmatex" markdown="1">
\[
\det A = 0
\]
</div>
whenever two rows of $A$ are equal: indeed, the matrix $A'$ obtained by interchanging these rows is equal to $A$, i.e., $A' = A$, so that $\det A = \det A'$. However, according to , we also have $\det A' = - \det A$. Taking this together, we have
<div class="arithmatex" markdown="1">
\[
\det A = - \det A
\]
</div>
and this is only possible if $\det A = 0$.

</div>

<div class="remark" markdown="1">


<p class="env-number"><strong>Remark 5.10</strong></p>

<span id="rem-determinants-remark-003" label="rem:determinants-remark-003"></span> The preceding remark also implies that for $i \ne j$ and $r \in {\bf R}$
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\det \left ( \begin{array}{c} v_1 \\ \vdots \\ v_i + r v_j \\ \vdots \\ v_n \end{array} \right ) & =  
\det \left ( \begin{array}{c} v_1 \\ \vdots \\ v_i \\ \vdots \\ v_n \end{array} \right ) +
r \det \left ( \begin{array}{c} v_1 \\ \vdots \\ v_j \\ \vdots \\ v_n \end{array} \right ) & \text{where $v_j$ is in the $i$-th row!} \\
& = \det \left ( \begin{array}{c} v_1 \\ \vdots \\ v_i \\ \vdots \\ v_n \end{array} \right ) + r \left ( \begin{array}{c} \vdots \\ v_j \\ \vdots \\ v_j \\ \vdots \end{array} \right ) \\
& =  \det \left ( \begin{array}{c} v_1 \\ \vdots \\ v_i \\ \vdots \\ v_n \end{array} \right ) & \text{by the above remark.}
\end{align*}
\]
</div>
In other words, adding an arbitrary multiple of some row to another row does not affect the determinant.

</div>

In order to get a feeling for this theorem, let us apply it to a concrete matrix, say
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{ccc} -2 & 1 & 8 \\ 1 & 3 & 5 \\ 0 & 2 & 4 \end{array} \right ).
\]
</div>
Taking the theorem for granted, we will compute $\det A$ by stepwise applying the above rules and keeping track of how the determinant changes.

<div class="arithmatex" markdown="1">
\[
\begin{align*}
\underbrace{\left ( \begin{array}{ccc} -2 & 1 & 8 \\ 1 & 3 & 5 \\ 0 & 2 & 4 \end{array} \right )}_{=A}
\leadsto & \underbrace{\left ( \begin{array}{ccc} 0 & 7 & 18 \\ 1 & 3 & 5 \\ 0 & 2 & 4 \end{array} \right )}_{=A_1} 
\leadsto \underbrace{\left ( \begin{array}{ccc} 0 & 1 & 6 \\ 1 & 3 & 5 \\ 0 & 2 & 4 \end{array} \right )}_{=A_2}
\leadsto \underbrace{\left ( \begin{array}{ccc} 0 & 1 & 6 \\ 1 & 3 & 5 \\ 0 & 0 & -8 \end{array} \right )}_{=A_3} \\
\leadsto & \underbrace{\left ( \begin{array}{ccc} 0 & 1 & 6 \\ 1 & 3 & 5 \\ 0 & 0 & 1 \end{array} \right )}_{=A_4}
\leadsto \underbrace{\left ( \begin{array}{ccc} 0 & 1 & 6 \\ 1 & 3 & 5 \\ 0 & 0 & 1 \end{array} \right )}_{=A_5}
\leadsto \underbrace{\left ( \begin{array}{ccc} 0 & 1 & 0 \\ 1 & 3 & 0 \\ 0 & 0 & 1 \end{array} \right )}_{=A_6} \\
\leadsto & \underbrace{\left ( \begin{array}{ccc} 0 & 1 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 1 \end{array} \right )}_{=A_7} 
\leadsto \underbrace{\left ( \begin{array}{ccc} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{array} \right )}_{=A_8 = {\mathrm {id}}_3}
\end{align*}
\]
</div>
From $A$ to $A_1$ to $A_2$ to $A_3$, we have added appropriate multiples of some row to another one, so that
<div class="arithmatex" markdown="1">
\[
\det A = \det A_1 = \det A_2 = \det A_3.
\]
</div>
We obtain $A_4$ from $A_3$ by multiplying the last row with $- \frac 18$, so that $\det A_4 = -\frac 18 \det A_3$. From $A_4$ to $A_5$ to $A_6$ to $A_7$, we again added appropriate multiples to some other rows, so that
<div class="arithmatex" markdown="1">
\[
\det A_4 = \det A_5 = \det A_6 = \det A_7.
\]
</div>
Finally, $A_8$ is obtained from $A_7$ by swapping the first two rows, so that
<div class="arithmatex" markdown="1">
\[
1 = \det A_8 = - \det A_7.
\]
</div>
Taking this all together we see that
<div class="arithmatex" markdown="1">
\[
\det A = \det A_3 = -8 \det A_4 = - 8 \det A_7 = + 8 \det A_8 = 8.
\]
</div>
This shows that the above abstract description of the determinant can be used to compute determinants in practice.

<div class="proof" markdown="1">

*Proof.* (of <a href="#thm-det-universal-property" data-reference-type="ref+Label" data-reference="thm:det-universal-property">Theorem 5.5</a>) We only sketch the proof idea: one basically proceeds, for a general square matrix, similarly to the computation above: one uses Gaussian elimination, i.e., elementary row operations to bring a given square matrix $A$ into reduced row-echelon form, say $A \leadsto A'$. The properties in <a href="#thm-det-universal-property" data-reference-type="ref+Label" data-reference="thm:det-universal-property">Theorem 5.5</a> then imply how to compute $\det A$ in terms of $\det A'$. If the resulting matrix $A'$ has a zero row, then $\det A' = 0$. If it has no zero row, then $A' = {\mathrm {id}}$, and $\det A' = 1$. ◻

</div>

### Small matrices

For practical purposes, it is useful to have an explicit formula at hand for small matrices:

For a $1 \times 1$-matrix $A$, i.e., $A = (a)$, we have
<div class="arithmatex" markdown="1">
\[
\det A = a.
\]
</div>

The determinant of $2 \times 2$-matrices defined in <a href="#def-det-2-x-2" data-reference-type="ref+Label" data-reference="def:det-2-x-2">Definition 5.1</a> satisfies the properties listed in <a href="#thm-det-universal-property" data-reference-type="ref+Label" data-reference="thm:det-universal-property">Theorem 5.5</a>.

- $\det {\mathrm {id}}_2 = \det \left ( \begin{array}{cc} 1 & 0 \\ 0 & 1 \end{array} \right ) = 1 \cdot 1 - 0 \cdot 0 = 1$.

- Swapping two rows yields a sign change in the determinant (<a href="#lem-swap-2-x-2" data-reference-type="ref+Label" data-reference="lem:swap-2-x-2">Lemma 5.4</a>).

- 
<div class="arithmatex" markdown="1">
\[
  \begin{align*}
  \det \left ( \begin{array}{cc} a & b \\ c + r e & d + rf \end{array} \right ) & = a(d+rf) - b(c+re) \\ & = ad-bc + r(af-be) \\ & = \det \left ( \begin{array}{cc} a & b \\ c & d \end{array} \right ) + r \det \left ( \begin{array}{cc} a & b \\ e & f \end{array} \right ).
  \end{align*}
\]
</div>

Thus, the definition of $\det$ for general matrices agrees with the one in <a href="#def-det-2-x-2" data-reference-type="ref+Label" data-reference="def:det-2-x-2">Definition 5.1</a>.

<div class="lemma" markdown="1">


<p class="env-number"><strong>Lemma 5.11</strong></p>

<span id="lem-sarrus-rule" label="lem:Sarrus-rule"></span> For a $3 \times 3$-matrix one can show that the determinant is given by the so-called *Sarrus’ rule*:
<div class="arithmatex" markdown="1">
\[
\det \left ( \begin{array}{ccc} a & b & c \\ d & e & f \\ g & h & i \end{array} \right ) = aei + bfg + cdh - ceg - bdi - afh.
\]
</div>

<p class="env-number equation-number"><strong>(5.12)</strong></p>

<span id="eqn-sarrus" label="eqn--Sarrus"></span>

</div>

<div class="proof" markdown="1">

*Proof.* One can prove by direct computation, that the function defined in satisfies the conditions in <a href="#thm-det-universal-property" data-reference-type="ref+Label" data-reference="thm:det-universal-property">Theorem 5.5</a>. ◻

</div>

A way to remember this formula is to write
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccccc} a & b & c & a & b \\ d & e & f & d & e \\ g & h & i & g & h \end{array} \right )
\]
</div>
and take products of entries along the top-left-to-bottom-right diagonals with a positive sign, and the top-right-to-bottom-left diagonals with a negative sign:

<div class="center" markdown="1">

![image](figures/png/determinants/determinants-fig-02.png)

</div>

<div class="warning" markdown="1">

Sarrus’ rule does not apply to larger matrices. Instead, for matrices of size $4 \times 4$, one can prove that $\det A$ is the sum of 24 expressions, each of which is a product of 4 entries of $A$. See <a href="#ex-determinants-exercise-004" data-reference-type="ref+Label" data-reference="ex:determinants-exercise-004">Exercise 5.4</a> for a fully worked computation of a determinant of a $4 \times 4$-matrix using different methods.

</div>

## Invertibility and determinants

We can use the properties of the determinant in <a href="#thm-det-universal-property" data-reference-type="ref+Label" data-reference="thm:det-universal-property">Theorem 5.5</a> (and its proof) to obtain a useful criterion to decide when a matrix is invertible. Determinants can also be used to compute the inverse of an invertible matrix, however this is only of theoretical significance due to the complexity of the ensuing (iterative) algorithm.

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 5.14</strong></p>

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


<p class="env-number"><strong>Theorem 5.15</strong></p>

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

*Proof.* We revisit the proof of <a href="#thm-det-universal-property" data-reference-type="ref+Label" data-reference="thm:det-universal-property">Theorem 5.5</a>: say $A \leadsto A'$, a reduced row echelon matrix, by means of elementary operations (Gaussian elimination). In this process, one does not multiply any row by zero, so that $\det A = 0$ if and only if $\det A' = 0$. We also know that $A' = UA$, where $U$ is an invertible matrix (namely, a product of elementary matrices). Moreover, $A'$ is invertible if and only if $A$ is invertible (since $U$ is invertible). We therefore have
<div class="arithmatex" markdown="1">
\[
A \text{ is invertible} \Leftrightarrow A' \text{ is invertible} \stackrel ? \Leftrightarrow \det A' \ne 0 \Leftrightarrow \det A \ne 0
\]
</div>
and it remains to show the middle equivalence.

The matrix $A'$ is in reduced row echelon form. Thus, either $A' = {\mathrm {id}}$ or $A'$ contains a zero row. In the first event, $A'$ is invertible, and $\det A' = 1 \ne 0$. In the second event, $A'$ is not invertible (by <a href="../maps/#cor-rows-columns-independent" data-reference-type="ref+Label" data-reference="cor:rows-columns-independent">Corollary 4.94</a>) and $\det A' = 0$ as was noted around .

We skip the proof of the adjugate formula, cf. . ◻

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 5.17</strong></p>

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

## Further properties of determinants

<div class="proposition" markdown="1">


<p class="env-number"><strong>Proposition 5.18</strong></p>

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

*Proof.* We don’t include a full proof, but only observe that one checks this by direct computation when $A$ is an elementary matrix. This implies the formula if $A$ is invertible, since then $A$ is a product of elementary matrices. If $A$ is not invertible, then one shows that $AB$ is also not invertible (for any $B$), and therefore both $\det A = 0$ and $\det (AB) = 0$, so the formula holds in this case too. See, e.g., for a proof. ◻

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


<p class="env-number"><strong>Proposition 5.20</strong></p>

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
i.e., the determinant does not change when passing from $A$ to its transpose (<a href="../maps/#def-transpose" data-reference-type="ref+Label" data-reference="def:transpose">Definition 4.89</a>).

</div>

<div class="proof" markdown="1">

*Proof.* For small matrices (of size at most $3 \times 3$), this can be proved directly from the formulae in §<a href="#sect-small-matrices" data-reference-type="ref" data-reference="sect--small matrices">1.2.1</a>.

In general, one may argue like this: if $A$ is not invertible, then $A^T$ is not invertible either (by <a href="../maps/#lem-properties-transposition" data-reference-type="ref+Label" data-reference="lem:properties-transposition">Lemma 4.91</a>). In this case, both sides of the equation are zero. If $A$ is invertible, it is a product of elementary matrices: $A = U_1 \dots U_n$. We then have $A^T = U_n^T \dots U_1^T$. By the product formula (<a href="#prop-product-formula" data-reference-type="ref+Label" data-reference="prop:product-formula">Proposition 5.18</a>), we may therefore assume $A$ is an elementary matrix. In this case, one checks the claim by inspection:

- for $A = \left ( \begin{array}{ccccccc} 1 & & & & & & \\ & \ddots & & & & & \\ & & 0 & & 1 & & \\ & & & \ddots & & & \\ & & 1 & & 0 & & \\ & & & & & \ddots & \\ & & & & & & 1 \end{array} \right )$, we have $A^T = A$, so the claim clearly holds.

- Likewise, for $A = \left ( \begin{array}{ccccccc} 1 & & & & & & \\ & \ddots & & & & & \\ & & 1 & & & & \\ & & & r & & & \\ & & & & 1 & & \\ & & & & & \ddots & \\ & & & & & & 1 \end{array} \right )$, we have $A = A^T$, so again the claim holds obviously.

- The matrix ${\left ( \begin{array}{ccccccc} 1 & & & & & & \\ & \ddots & & & & & \\ & & 1 & & & & \\ & & & \ddots & & & \\ & & r & & 1 & & \\ & & & & & \ddots & \\ & & & & & & 1 \end{array} \right )}$ is a lower triangular matrix, and its transpose an upper triangular matrix. Both have determinant 1 according to <a href="#prop-det-triangular-matrix" data-reference-type="ref+Label" data-reference="prop:det-triangular-matrix">Proposition 5.20</a>.

 ◻

</div>

<div class="remark" markdown="1">


<p class="env-number"><strong>Remark 5.22</strong></p>

<span id="rem-determinants-remark-005" label="rem:determinants-remark-005"></span> We introduced the determinant using *row* operations. The preceding result implies that one can replace the word “row” in all of the above by the word “column”. Applying that, say, to <a href="#rem-det-zero-equal-rows" data-reference-type="ref+Label" data-reference="rem:det-zero-equal-rows">Remark 5.9</a> we obtain that $\det A = 0$ if $A$ has two identical columns.

</div>

<div class="proposition" markdown="1">


<p class="env-number"><strong>Proposition 5.23</strong></p>

<span id="prop-cofactor-expansion" label="prop:cofactor-expansion"></span> Let $A  = (a_{ij}) \in {\mathrm {Mat}}_{n \times n}$. Then, for any $i$, one can compute the determinant using “*cofactor expansion*” along the $i$-th row. That is, the following identity holds, where $c_{ij}$ are the cofactors of $A$ (<a href="#def-cofactors" data-reference-type="ref+Label" data-reference="def:cofactors">Definition 5.14</a>):
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

For a proof of this, see, e.g. .

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

## Exercises

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 5.1</strong></p>

<span id="ex-determinants-exercise-001" label="ex:determinants-exercise-001"></span> (See <a href="#sol-ex-determinants-exercise-001" data-reference-type="ref+Label" data-reference="sol--ex:determinants-exercise-001">Solution 5.6.1</a>.) For which values of $a, b \in {\bf R}$ is the following matrix invertible? In this event, what is its inverse?
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{ccc} a & b & 3 \\ 2 & 1 & -1 \\ 1 & -1 & 4 \end{array} \right ).
\]
</div>

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 5.2</strong></p>

<span id="ex-determinants-exercise-002" label="ex:determinants-exercise-002"></span> (See <a href="#sol-ex-determinants-exercise-002" data-reference-type="ref+Label" data-reference="sol--ex:determinants-exercise-002">Solution 5.6.2</a>.) Let $A$ be a square matrix such that $A^2 = {\mathrm {id}}$ (the identity matrix). Prove that $\det(A) = \pm 1$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 5.3</strong></p>

<span id="ex-determinants-exercise-003" label="ex:determinants-exercise-003"></span> (See <a href="#sol-ex-determinants-exercise-003" data-reference-type="ref+Label" data-reference="sol--ex:determinants-exercise-003">Solution 5.6.3</a>.) Compute the determinant of a *rotation matrix* (cf. <a href="../maps/#ex-rotation-matrix-general" data-reference-type="ref+Label" data-reference="ex:rotation-matrix-general">Example 4.18</a>),
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{cc} \cos r & -\sin r \\ \sin r & \cos r \end{array} \right ).
\]
</div>

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 5.4</strong></p>

<span id="ex-determinants-exercise-004" label="ex:determinants-exercise-004"></span> (See <a href="#sol-ex-determinants-exercise-004" data-reference-type="ref+Label" data-reference="sol--ex:determinants-exercise-004">Solution 5.6.4</a>.) Compute the determinant of
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc} 2 & 0 & 1 & 4 \\ -1 & 3 & 0 & 2 \\ 1 & 0 & 2 & -3 \\ 0 & -2 & 5 & 1 \end{array} \right ).
\]
</div>

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 5.5</strong></p>

<span id="ex-determinants-4-1" label="ex:determinants-4-1"></span> (See <a href="#sol-ex-determinants-4-1" data-reference-type="ref+Label" data-reference="sol--ex:determinants-4-1">Solution 5.6.5</a>.) Compute the determinant of $\left ( \begin{array}{ccc} 3 & 0 & 0 \\ 1 & 4 & 0 \\ 2 & -3 & 5 \end{array} \right )$ in three ways:

- by using <a href="#thm-det-universal-property" data-reference-type="ref+Label" data-reference="thm:det-universal-property">Theorem 5.5</a>,

- by using Sarrus’s rule, ,

- by using <a href="#prop-det-triangular-matrix" data-reference-type="ref+Label" data-reference="prop:det-triangular-matrix">Proposition 5.20</a>.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 5.6</strong></p>

<span id="ex-determinants-4-2" label="ex:determinants-4-2"></span> (See <a href="#sol-ex-determinants-4-2" data-reference-type="ref+Label" data-reference="sol--ex:determinants-4-2">Solution 5.6.6</a>.) Compute the determinants of the following matrices. You should be able to do this very quickly:
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc} 1 & 5 & 8 \\ 40 & -9 & 1 \\ 0 & 0 & 0 \end{array} \right ) \ \text{and } \ \left ( \begin{array}{ccc} 1 & 5 & 8 \\ 40 & -9 & 1 \\ 1 & 5 & 8 \end{array} \right ).
\]
</div>

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 5.7</strong></p>

<span id="ex-determinants-exercise-005" label="ex:determinants-exercise-005"></span> (See <a href="#sol-ex-determinants-exercise-005" data-reference-type="ref+Label" data-reference="sol--ex:determinants-exercise-005">Solution 5.6.7</a>.) Compute the determinants of
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc} 3 & 26 & -9 & 3 \\ 0 & 3 & 1 & 28 \\ 0 & 0 & 2 & 71 \\ 0 & 0 & 0 & 3 \end{array} \right ) \ \text{and } \left ( \begin{array}{ccc} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{array} \right ).
\]
</div>

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 5.8</strong></p>

<span id="ex-determinants-exercise-006" label="ex:determinants-exercise-006"></span> (See <a href="#sol-ex-determinants-exercise-006" data-reference-type="ref+Label" data-reference="sol--ex:determinants-exercise-006">Solution 5.6.8</a>.) Compute the inverses of
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cc} 10 & 9 \\ 11 & 10 \end{array} \right ) \ \text{and } \ \left ( \begin{array}{ccc} 5 & 2 & -1 \\ 0 & 0 & 1 \\ 6 & 2 & 3 \end{array} \right ).
\]
</div>

</div>

## Solutions to the exercises

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 5.6.1</strong></p>

<span id="sol-ex-determinants-exercise-001" label="sol--ex:determinants-exercise-001"></span> (See <a href="#ex-determinants-exercise-001" data-reference-type="ref+Label" data-reference="ex:determinants-exercise-001">Exercise 5.1</a>.) By <a href="#thm-det-zero-niff-invertible" data-reference-type="ref+Label" data-reference="thm:det-zero-niff-invertible">Theorem 5.15</a>, the matrix $A$ is invertible if and only if $\det A \ne 0$. Using Sarrus’ rule, cf. <a href="#lem-sarrus-rule" data-reference-type="ref+Label" data-reference="lem:Sarrus-rule">Lemma 5.11</a>, we compute
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\det A & = a \cdot 1 \cdot 4 + b \cdot (-1) \cdot 1 + 3 \cdot 2 \cdot (-1) \\
& \phantom{=} - 3 \cdot 1 \cdot 1 - b \cdot 2 \cdot 4 - a \cdot (-1) \cdot (-1) \\
& = 4a - b - 6 - 3 - 8b - a \\
& = 3a - 9b - 9 \\
& = 3(a-3b-3).
\end{align*}
\]
</div>
Therefore, $A$ is invertible precisely for
<div class="arithmatex" markdown="1">
\[
a - 3b - 3 \ne 0.
\]
</div>

In this case, the inverse can be computed using the adjugate formula from , where the adjugate is defined in <a href="#def-cofactors" data-reference-type="ref+Label" data-reference="def:cofactors">Definition 5.14</a>. The cofactors are
<div class="arithmatex" markdown="1">
\[
\begin{align*}
c_{11} & = \det \left ( \begin{array}{cc} 1 & -1 \\ -1 & 4 \end{array} \right ) = 3,
&
c_{12} & = - \det \left ( \begin{array}{cc} 2 & -1 \\ 1 & 4 \end{array} \right ) = -9,
&
c_{13} & = \det \left ( \begin{array}{cc} 2 & 1 \\ 1 & -1 \end{array} \right ) = -3.
\end{align*}
\]
</div>

etc. One obtains the adjugate matrix:
<div class="arithmatex" markdown="1">
\[
\mathrm{adj}(A) = \left ( \begin{array}{ccc} 3 & -4b-3 & -b-3 \\ -9 & 4a-3 & a+6 \\ -3 & a+b & a-2b \end{array} \right ),
\]
</div>
and therefore
<div class="arithmatex" markdown="1">
\[
A^{-1} = \frac{1}{3a-9b-9} \left ( \begin{array}{ccc} 3 & -4b-3 & -b-3 \\ -9 & 4a-3 & a+6 \\ -3 & a+b & a-2b \end{array} \right ).
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 5.6.2</strong></p>

<span id="sol-ex-determinants-exercise-002" label="sol--ex:determinants-exercise-002"></span> (See <a href="#ex-determinants-exercise-002" data-reference-type="ref+Label" data-reference="ex:determinants-exercise-002">Exercise 5.2</a>.) From $A^2 = {\mathrm {id}}$ and the product formula in <a href="#prop-product-formula" data-reference-type="ref+Label" data-reference="prop:product-formula">Proposition 5.18</a>, we get
<div class="arithmatex" markdown="1">
\[
\det(A^2) = \det(A)\det(A) = (\det A)^2.
\]
</div>
On the other hand,
<div class="arithmatex" markdown="1">
\[
\det(A^2) = \det({\mathrm {id}}).
\]
</div>
By <a href="#thm-det-universal-property" data-reference-type="ref+Label" data-reference="thm:det-universal-property">Theorem 5.5</a>, we have $\det({\mathrm {id}})=1$. Therefore
<div class="arithmatex" markdown="1">
\[
(\det A)^2 = 1.
\]
</div>
Since $\det A \in {\bf R}$, this implies
<div class="arithmatex" markdown="1">
\[
\det A = \pm 1.
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 5.6.3</strong></p>

<span id="sol-ex-determinants-exercise-003" label="sol--ex:determinants-exercise-003"></span> (See <a href="#ex-determinants-exercise-003" data-reference-type="ref+Label" data-reference="ex:determinants-exercise-003">Exercise 5.3</a>.) Using the $2 \times 2$ determinant formula from <a href="#def-det-2-x-2" data-reference-type="ref+Label" data-reference="def:det-2-x-2">Definition 5.1</a>, we get
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\det A & = \det \left ( \begin{array}{cc} \cos r & -\sin r \\ \sin r & \cos r \end{array} \right ) \\
& = (\cos r)(\cos r) - (-\sin r)(\sin r) \\
& = \cos^2 r + \sin^2 r \\
& = 1.
\end{align*}
\]
</div>
So every rotation matrix has determinant $1$. (In particular, by <a href="#thm-det-zero-niff-invertible" data-reference-type="ref+Label" data-reference="thm:det-zero-niff-invertible">Theorem 5.15</a>, every rotation matrix is invertible.)

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 5.6.4</strong></p>

<span id="sol-ex-determinants-exercise-004" label="sol--ex:determinants-exercise-004"></span> (See <a href="#ex-determinants-exercise-004" data-reference-type="ref+Label" data-reference="ex:determinants-exercise-004">Exercise 5.4</a>.) We compute the determinant of
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{cccc} 2 & 0 & 1 & 4 \\ -1 & 3 & 0 & 2 \\ 1 & 0 & 2 & -3 \\ 0 & -2 & 5 & 1 \end{array} \right )
\]
</div>
in two different ways.

**First method (using <a href="#thm-det-universal-property" data-reference-type="ref+Label" data-reference="thm:det-universal-property">Theorem 5.5</a>):** Set $A_0 := A$. Using row additions (which do not change the determinant, cf. <a href="#thm-det-universal-property" data-reference-type="ref+Label" data-reference="thm:det-universal-property">Theorem 5.5</a>) we will bring $A$ to a diagonal form: we consider
<div class="arithmatex" markdown="1">
\[
\begin{align*}
A_1 &:= \left ( \begin{array}{cccc} 2 & 0 & 1 & 4 \\ 0 & 3 & \frac 12 & 4 \\ 0 & 0 & \frac 32 & -5 \\ 0 & -2 & 5 & 1 \end{array} \right ) \\[-0.5mm]
&\text{(obtained from $A_0$ by }R_2\leadsto R_2+\frac12R_1,\; R_3\leadsto R_3-\frac12R_1\text{)}, \\
A_2 &:= \left ( \begin{array}{cccc} 2 & 0 & 1 & 4 \\ 0 & 3 & \frac 12 & 4 \\ 0 & 0 & \frac 32 & -5 \\ 0 & 0 & \frac {16}3 & \frac {11}3 \end{array} \right )
\quad\text{(from $A_1$ by }R_4\leadsto R_4+\frac23R_2\text{)}, \\
A_3 &:= \left ( \begin{array}{cccc} 2 & 0 & 1 & 4 \\ 0 & 3 & \frac 12 & 4 \\ 0 & 0 & \frac 32 & -5 \\ 0 & 0 & 0 & \frac {193}9 \end{array} \right )
\quad\text{(from $A_2$ by }R_4\leadsto R_4-\frac{32}9R_3\text{)}.
\end{align*}
\]
</div>
Now eliminate the entries above the pivots in columns 3 and 4:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
&A_4 := \left ( \begin{array}{cccc} 2 & 0 & 0 & \frac{22}3 \\ 0 & 3 & 0 & \frac{17}3 \\ 0 & 0 & \frac32 & -5 \\ 0 & 0 & 0 & \frac{193}9 \end{array} \right )
\quad\text{(from $A_3$ by }R_2\leadsto R_2-\frac13R_3,\; R_1\leadsto R_1-\frac23R_3\text{)}, \\
&A_5 := \left ( \begin{array}{cccc} 2 & 0 & 0 & 0 \\ 0 & 3 & 0 & 0 \\ 0 & 0 & \frac32 & 0 \\ 0 & 0 & 0 & \frac{193}9 \end{array} \right )
\quad\text{(from $A_4$ by }R_1\leadsto R_1-\frac{66}{193}R_4,\; R_2\leadsto R_2-\frac{51}{193}R_4,\; R_3\leadsto R_3+\frac{45}{193}R_4\text{)}.
\end{align*}
\]
</div>
All these steps are row additions, so
<div class="arithmatex" markdown="1">
\[
\det A_0 = \det A_1 = \dots = \det A_5.
\]
</div>
For the diagonal matrix $A_5$, multilinearity in the rows and $\det({\mathrm{id}})=1$ from <a href="#thm-det-universal-property" data-reference-type="ref+Label" data-reference="thm:det-universal-property">Theorem 5.5</a> give
<div class="arithmatex" markdown="1">
\[
\det A_5 = 2 \cdot 3 \cdot \frac32 \cdot \frac{193}9 = 193.
\]
</div>
Hence
<div class="arithmatex" markdown="1">
\[
\det A = 193.
\]
</div>

**Second method (using cofactor expansion, <a href="#prop-cofactor-expansion" data-reference-type="ref+Label" data-reference="prop:cofactor-expansion">Proposition 5.23</a>):** Expand along the second column (which is the most efficient choice, since this column contains two zeros), and use Sarrus’ rule (<a href="#lem-sarrus-rule" data-reference-type="ref+Label" data-reference="lem:Sarrus-rule">Lemma 5.11</a>) to compute the $3 \times 3$-determinants:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\det A
&= (+3) \det \left ( \begin{array}{ccc} 2 & 1 & 4 \\ 1 & 2 & -3 \\ 0 & 5 & 1 \end{array} \right )
+ (+2) \det \left ( \begin{array}{ccc} 2 & 1 & 4 \\ -1 & 0 & 2 \\ 1 & 2 & -3 \end{array} \right ) \\
&= 3 \cdot 47 + 2 \cdot 26 \\
&= 141 + 52 \\
&= 193.
\end{align*}
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 5.6.5</strong></p>

<span id="sol-ex-determinants-4-1" label="sol--ex:determinants-4-1"></span> (See <a href="#ex-determinants-4-1" data-reference-type="ref+Label" data-reference="ex:determinants-4-1">Exercise 5.5</a>.) According to <a href="#prop-det-triangular-matrix" data-reference-type="ref+Label" data-reference="prop:det-triangular-matrix">Proposition 5.20</a>, the determinant is the product of the diagonal entries, i.e., it equals $3 \cdot 4 \cdot 5 = 60$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 5.6.6</strong></p>

<span id="sol-ex-determinants-4-2" label="sol--ex:determinants-4-2"></span> (See <a href="#ex-determinants-4-2" data-reference-type="ref+Label" data-reference="ex:determinants-4-2">Exercise 5.6</a>.) The matrix $\left ( \begin{array}{ccc} 1 & 5 & 8 \\ 40 & -9 & 1 \\ 0 & 0 & 0 \end{array} \right )$ has a zero row, so the determinant is $0$ (cf. <a href="#rem-determinants-remark-001" data-reference-type="ref+Label" data-reference="rem:determinants-remark-001">Remark 5.7</a>). The second matrix, $\left ( \begin{array}{ccc} 1 & 5 & 8 \\ 40 & -9 & 1 \\ 1 & 5 & 8 \end{array} \right )$ has two equal rows, so the determinant is $0$ (cf. <a href="#rem-det-zero-equal-rows" data-reference-type="ref+Label" data-reference="rem:det-zero-equal-rows">Remark 5.9</a>).

Equivalently, both matrices are non-invertible (their rows are linearly dependent), and by <a href="#thm-det-zero-niff-invertible" data-reference-type="ref+Label" data-reference="thm:det-zero-niff-invertible">Theorem 5.15</a> their determinants must be zero.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 5.6.7</strong></p>

<span id="sol-ex-determinants-exercise-005" label="sol--ex:determinants-exercise-005"></span> (See <a href="#ex-determinants-exercise-005" data-reference-type="ref+Label" data-reference="ex:determinants-exercise-005">Exercise 5.7</a>.) The first matrix
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{cccc} 3 & 26 & -9 & 3 \\ 0 & 3 & 1 & 28 \\ 0 & 0 & 2 & 71 \\ 0 & 0 & 0 & 3 \end{array} \right ),
\]
</div>
is an upper triangular matrix, so we can use <a href="#prop-det-triangular-matrix" data-reference-type="ref+Label" data-reference="prop:det-triangular-matrix">Proposition 5.20</a> to compute its determinant:
<div class="arithmatex" markdown="1">
\[
\det A = 3 \cdot 3 \cdot 2 \cdot 3 = 54.
\]
</div>

For the second matrix,
<div class="arithmatex" markdown="1">
\[
B = \left ( \begin{array}{ccc} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{array} \right ),
\]
</div>
we use Sarrus’ rule (<a href="#lem-sarrus-rule" data-reference-type="ref+Label" data-reference="lem:Sarrus-rule">Lemma 5.11</a>):
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\det B
&= 1\cdot 5\cdot 9 + 2\cdot 6\cdot 7 + 3\cdot 4\cdot 8
- 3\cdot 5\cdot 7 - 2\cdot 4\cdot 9 - 1\cdot 6\cdot 8 \\
&= 45 + 84 + 96 - 105 - 72 - 48 \\
&= 0.
\end{align*}
\]
</div>
Hence the determinants are $54$ and $0$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 5.6.8</strong></p>

<span id="sol-ex-determinants-exercise-006" label="sol--ex:determinants-exercise-006"></span> (See <a href="#ex-determinants-exercise-006" data-reference-type="ref+Label" data-reference="ex:determinants-exercise-006">Exercise 5.8</a>.) By <a href="#thm-det-zero-niff-invertible" data-reference-type="ref+Label" data-reference="thm:det-zero-niff-invertible">Theorem 5.15</a> and , $A^{-1} = \frac{1}{\det A}\,\mathrm{adj}(A).$ For
<div class="arithmatex" markdown="1">
\[
A_1 = \left ( \begin{array}{cc} 10 & 9 \\ 11 & 10 \end{array} \right ),
\]
</div>
we have
<div class="arithmatex" markdown="1">
\[
\det A_1 = 10\cdot 10 - 9\cdot 11 = 1,
\]
</div>
and by the $2\times2$ inverse formula (cf. <a href="#ex-determinants-example-002" data-reference-type="ref+Label" data-reference="ex:determinants-example-002">Example 5.17</a>)
<div class="arithmatex" markdown="1">
\[
A_1^{-1} = \left ( \begin{array}{cc} 10 & -9 \\ -11 & 10 \end{array} \right ).
\]
</div>
For
<div class="arithmatex" markdown="1">
\[
A_2 = \left ( \begin{array}{ccc} 5 & 2 & -1 \\ 0 & 0 & 1 \\ 6 & 2 & 3 \end{array} \right ),
\]
</div>
we have $\det A_2 = 2 \ne 0$, and a brief cofactor computation gives
<div class="arithmatex" markdown="1">
\[
\mathrm{adj}(A_2)=\left ( \begin{array}{ccc} -2 & -8 & 2 \\ 6 & 21 & -5 \\ 0 & 2 & 0 \end{array} \right ).
\]
</div>
Hence
<div class="arithmatex" markdown="1">
\[
A_2^{-1}=\frac12\left ( \begin{array}{ccc} -2 & -8 & 2 \\ 6 & 21 & -5 \\ 0 & 2 & 0 \end{array} \right )
= \left ( \begin{array}{ccc} -1 & -4 & 1 \\ 3 & \frac{21}{2} & -\frac52 \\ 0 & 1 & 0 \end{array} \right ).
\]
</div>
This exercise can also be solved without using the adjugate formula, as follows: by <a href="../maps/#thm-invertible-elimination" data-reference-type="ref+Label" data-reference="thm:invertible-elimination">Theorem 4.81</a> (similarly to <a href="../maps/#ex-maps-example-025" data-reference-type="ref+Label" data-reference="ex:maps-example-025">Example 4.82</a>), we can compute $A^{-1}$ by reducing $(A \ | \ {\mathrm{id}})$ to $({\mathrm{id}} \ | \ A^{-1})$. For $A_2$:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left ( \begin{array}{ccc|ccc} 5 & 2 & -1 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 & 1 & 0 \\ 6 & 2 & 3 & 0 & 0 & 1 \end{array} \right )
&\leadsto
\left ( \begin{array}{ccc|ccc} 5 & 2 & -1 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 & 1 & 0 \\ 0 & -\frac25 & \frac{21}{5} & -\frac65 & 0 & 1 \end{array} \right ) \\
&\leadsto
\left ( \begin{array}{ccc|ccc} 5 & 2 & -1 & 1 & 0 & 0 \\ 0 & -\frac25 & \frac{21}{5} & -\frac65 & 0 & 1 \\ 0 & 0 & 1 & 0 & 1 & 0 \end{array} \right ) \\
&\leadsto
\left ( \begin{array}{ccc|ccc} 5 & 2 & -1 & 1 & 0 & 0 \\ 0 & 1 & -\frac{21}{2} & 3 & 0 & -\frac52 \\ 0 & 0 & 1 & 0 & 1 & 0 \end{array} \right ) \\
&\leadsto
\left ( \begin{array}{ccc|ccc} 1 & 0 & 0 & -1 & -4 & 1 \\ 0 & 1 & 0 & 3 & \frac{21}{2} & -\frac52 \\ 0 & 0 & 1 & 0 & 1 & 0 \end{array} \right ).
\end{align*}
\]
</div>
Therefore,
<div class="arithmatex" markdown="1">
\[
A_2^{-1}=\left ( \begin{array}{ccc} -1 & -4 & 1 \\ 3 & \frac{21}{2} & -\frac52 \\ 0 & 1 & 0 \end{array} \right ),
\]
</div>
in agreement with Method 1.

</div>
