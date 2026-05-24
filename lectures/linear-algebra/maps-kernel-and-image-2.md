---
title: Kernel and Image (2)
---

The following facts are immediate consequences of the rank-nullity theorem.

<div class="corollary" markdown="1">


<p class="env-number"><strong>Corollary 4.28</strong> (Related exercises: <a href="../exercises-maps/#ex-maps-exercise-014">Exercise 4.18</a>)</p>

<span id="cor-maps-dim" label="cor:maps-dim"></span> Let $f : V \to W$ be a linear map between finite-dimensional vector spaces.

1.  If $f$ is injective then $\dim V \le \dim W$ (since then $\ker f = \{0\}$, i.e., $\dim \ker f = 0$).

2.  If $f$ is surjective then $\dim V \ge \dim W$ (since them ${\operatorname{im}\ } f = W$, so $\dim {\operatorname{im}\ } f = \dim W$).

3.  <span id="item-dim-bij" label="item--dim bij"></span> If $f$ is bijective then $\dim V = \dim W$.

4.  The preceding three statements can in general not be reversed: if, say, $\dim V \le \dim W$, $f$ need not be injective. For example the zero map $V \to W$, $v \mapsto 0$ is *never* injective if $V \ne \{ 0\}$.

5.  <span id="item-inj-iff-surj" label="item--inj iff surj"></span> Suppose in addition that $\dim V = \dim W$. In this case $f$ is injective precisely if $f$ is surjective. (If $f$ is injective, then $\dim {\operatorname{im}\ } f = \dim V = \dim W$, so that ${\operatorname{im}\ } f = W$ by <a href="../spaces-dimension/#thm-basis-theorem" data-reference-type="ref+Label" data-reference="thm:basis-theorem">Theorem 3.71</a><a href="../spaces-dimension/#item-dim-subspace" data-reference-type="ref" data-reference="item--dim.subspace">3.</a>. Similarly, if $f$ is surjective, then $\dim {\operatorname{im}\ } f = \dim W = \dim V$, so $\dim \ker f = 0$, so that $\ker f = \{ 0\}$.)

</div>

An important case of this theorem is where $f : {\bf R}^n \to {\bf R}^m$ is the linear map given by multiplication with a fixed $m \times n$-matrix $A$. We call the *rank* of $A$, resp. the *nullity* the rank, resp. nullity of that linear map. The rank is denoted by ${\operatorname {rk}} A$. These are two highly important numbers associated to a matrix, so we want to have a device for computing them. This is based on the following computation: recall from <a href="../spaces-bases/#ex-standard-basis" data-reference-type="ref+Label" data-reference="ex:standard-basis">Example 3.62</a> the standard basis vectors
<div class="arithmatex" markdown="1">
\[
e_1 = (1, 0, \dots, 0), e_2 = (0, 1, 0, \dots 0), \dots, e_n = (0, \dots, 0,  1) \in {\bf R}^n.
\]
</div>
We will in the sequel write them as column vectors, so $e_1 = \left ( \begin{array}{c} 1 \\ 0 \\ \vdots \\ 0 \end{array} \right )$ etc. Then we have
<div class="arithmatex" markdown="1">
\[
f(e_i) = A e_i = \left ( \begin{array}{c} a_{11} \cdot 0 + \dots + a_{1i} \cdot 1 + \dots + a_{1n} \cdot 0 \\ \vdots \\ a_{m1} \cdot 0 + \dots + a_{mi} \cdot 1 + \dots + a_{mn} \cdot 0 \end{array} \right ) = \left ( \begin{array}{c} a_{1i} \\ \vdots \\ a_{mi} \end{array} \right ).
\]
</div>
<div class="arithmatex" markdown="1">
\[
A e_i = \left ( \begin{array}{c} a_{1i} \\ \vdots \\ a_{mi} \end{array} \right ).
\]
</div>

<p class="env-number equation-number"><strong>(4.29)</strong></p>

<span id="eqn-a-e-i" label="eqn--A e_i"></span> In other words, the product $A e_i$ is precisely the $i$-th column of the matrix $A$!

Since any vector $v \in {\bf R}^n$ is a linear combination of the $e_i$, we have, for appropriate $b_1, \dots, b_n \in {\bf R}$
<div class="arithmatex" markdown="1">
\[
f(v) = f(\sum_{i=1}^n b_i e_i) = \sum_{i=1}^n b_i f(e_i).
\]
</div>
Thus, $f(v)$ is a linear combination of the columns of $A$. This proves the following statement:

<div class="proposition" markdown="1">


<p class="env-number"><strong>Proposition 4.30</strong> (Related exercises: <a href="../exercises-maps/#ex-maps-3-7">Exercise 4.17</a>)</p>

<span id="prop-image-column-space" label="prop:image-column-space"></span> Let $A$ be an $m \times n$-matrix and $f : {\bf R}^n \to {\bf R}^m$ the linear map given by multiplication with $A$. We write
<div class="arithmatex" markdown="1">
\[
A = (c_1 \ c_2 \ \dots c_n),
\]
</div>
i.e., the $c_i (\in {\bf R}^m)$ is the $i$-th column of $A$. Then
<div class="arithmatex" markdown="1">
\[
{\operatorname{im}\ } f = L(c_1, \dots, c_n).
\]
</div>
This subspace of ${\bf R}^m$ is also called the *column space* of $A$.

</div>

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 4.31</strong></p>

<span id="def-maps-definition-005" label="def:maps-definition-005"></span> The *row space* of $A$ is the subspace of ${\bf R}^n$ spanned by the rows of the matrix $A$.

</div>

We can compute the rank of $A$, i.e., $\dim {\operatorname{im}\ } f$, as follows:

<div class="proposition" markdown="1">


<p class="env-number"><strong>Proposition 4.32</strong> (Related exercises: <a href="../exercises-maps/#ex-maps-3-3">Exercise 4.10</a>, <a href="../exercises-maps/#ex-maps-3-4">Exercise 4.13</a>, <a href="../exercises-maps/#ex-maps-3-6">Exercise 4.16</a>, <a href="../exercises-maps/#ex-maps-exercise-003">Exercise 4.3</a>, <a href="../exercises-maps/#ex-maps-exercise-004">Exercise 4.4</a>, <a href="../exercises-maps/#ex-maps-exercise-007">Exercise 4.7</a>, <a href="../exercises-maps/#ex-maps-exercise-013">Exercise 4.14</a>, <a href="../exercises-maps/#ex-maps-exercise-014">Exercise 4.18</a>)</p>

<span id="prop-basis-row-column-space" label="prop:basis-row-column-space"></span> Let $A$ be an $m \times n$-matrix. Suppose $B$ is a (possibly non-reduced) row-echelon matrix obtained from $A$ by means of elementary row operations (<a href="../systems-gaussian-elimination/#def-elementary-row-operations" data-reference-type="ref+Label" data-reference="def:elementary-row-operations">Definition 2.28</a>).

1.  <span id="item-blah-x1" label="item--blah.x1"></span> Then the non-zero rows of $B$ form a basis of the row space of $A$.

2.  <span id="item-blah-x2" label="item--blah.x2"></span> If the leading ones of $B$ lie in the columns $j_1, \dots, j_r$, then these columns of $A$ form a basis of the column space of $A$.

3.  <span id="item-blah-x3" label="item--blah.x3"></span> The following numbers are all the same: a) ${\operatorname {rk}} A$, b) the dimension of the column space, c) the dimension of the row space of $A$, d) the number of leading ones in $B$.

4.  <span id="item-blah-x4" label="item--blah.x4"></span> The nullity of $A$ equals $n$ (the number of columns of $A$) minus any of the quantities in the previous point.

</div>

<div class="proof" markdown="1">

*Proof.* Parts <a href="#item-blah-x1" data-reference-type="ref" data-reference="item--blah.x1">1.</a> and <a href="#item-blah-x2" data-reference-type="ref" data-reference="item--blah.x2">2.</a> can be proven by showing that the row and column space of $A$ do not change when one performs an elementary row operation to $A$. We skip this part of the proof (e.g., see (Nicholson 1995, Lemma 5.4.1) for a proof).

<a href="#item-blah-x3" data-reference-type="ref" data-reference="item--blah.x3">3.</a> follows from the first two: by definition, ${\operatorname {rk}} A = \dim {\operatorname{im}\ } f$ equals, by <a href="#prop-image-column-space" data-reference-type="ref+Label" data-reference="prop:image-column-space">Proposition 4.30</a>, the dimension of the column space. By the second statement, this is equal to the number of leading ones in $B$. Since $B$ is a row-echelon matrix, this is also the number of non-zero rows, i.e., by the first statement, the dimension of the row space.

Finally, <a href="#item-blah-x4" data-reference-type="ref" data-reference="item--blah.x4">4.</a> is a consequence of the rank-nullity-theorem. ◻

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 4.33</strong></p>

<span id="ex-dim-ker-im-example" label="ex:dim-ker-im-example"></span> Consider the matrix
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{cccc} 1 & 2 & 2 & -1 \\ 3 & 6 & 5 & 0 \\ 1 & 2 & 1 & 2 \end{array} \right )
\]
</div>
and the linear map
<div class="arithmatex" markdown="1">
\[
f : {\bf R}^4 \to {\bf R}^3, v \mapsto Av.
\]
</div>
The row space is the subspace of ${\bf R}^4$ spanned by the vectors $(1 \ 2 \ 2 \ -1)$ etc., while the column space is the subspace of ${\bf R}^3$ spanned by the vectors $\left ( \begin{array}{c} 1 \\ 3 \\ 1 \end{array} \right )$ etc. We compute a basis of these two spaces as follows:
<div class="arithmatex" markdown="1">
\[
A \leadsto \left ( \begin{array}{cccc} 1 & 2 & 2 & -1 \\ 0 & 0 & -1 & 3 \\ 0 & 0 & -1 & 3 \end{array} \right )  \leadsto \left ( \begin{array}{cccc} 1 & 2 & 2 & -1 \\ 0 & 0 & -1 & 3 \\ 0 & 0 & 0 & 0 \end{array} \right ) \leadsto \left ( \begin{array}{cccc} 1 & 2 & 2 & -1 \\ 0 & 0 & 1 & -3 \\ 0 & 0 & 0 & 0 \end{array} \right ).
\]
</div>
Thus, the vectors $(1, 2, 2, -1)$ and $(0, 0, 1, -3)$ form a basis of the row space. In particular, its dimension is two. The first and third row of $A$ form a basis of the column space of $A$, i.e.,
<div class="arithmatex" markdown="1">
\[
{\operatorname{im}\ } f = L(\left ( \begin{array}{c} 1 \\ 3 \\ 1 \end{array} \right ), \left ( \begin{array}{c} 2 \\ 5 \\ 1 \end{array} \right )).
\]
</div>
Thus
<div class="arithmatex" markdown="1">
\[
\dim {\operatorname{im}\ } f = {\operatorname {rk}} f = {\operatorname {rk}} A = 2.
\]
</div>
According to the rank-nullity theorem (<a href="../maps-kernel-and-image-1/#thm-rank-nullity-theorem" data-reference-type="ref+Label" data-reference="thm:rank-nullity-theorem">Theorem 4.26</a>),
<div class="arithmatex" markdown="1">
\[
\dim \ker f = \dim {\bf R}^4 - \dim {\operatorname{im}\ } f = 4 - 2 = 2,
\]
</div>
(i.e., the nullity of $f$ or of $A$ is 2). In order to determine a basis of $\ker f$, we denote the coordinates in ${\bf R}^4$ by $x_1, \dots, x_4$. Then, according to Gaussian elimination, the variables $x_2$ and $x_4$ are free variables, and $x_3 = 3 x_4$ from the second row above, and then $x_1 = -2x_2 - 2x_3 + x_4 = -2x_2 -5x_4$. Thus a basis of $\ker f$ is given by the vectors
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{c} -2 \\ 1 \\ 0 \\ 0 \end{array} \right ), \left ( \begin{array}{c} -5 \\ 0 \\ 3 \\ 1 \end{array} \right ).
\]
</div>
This reconfirms that $\dim \ker f = 2$.

</div>

<div class="remark" markdown="1">


<p class="env-number"><strong>Remark 4.34</strong></p>

<span id="rem-maps-remark-002" label="rem:maps-remark-002"></span> Even though the dimension of the row space and the column space are the same, these vector spaces themselves are *not* the same. In fact, they are not even comparable, given that the row space is a subspace of ${\bf R}^n$, while the column space is a subspace of ${\bf R}^m$.

</div>

Here is another consequence of the rank-nullity theorem.

<div class="theorem" markdown="1">


<p class="env-number"><strong>Theorem 4.35</strong></p>

(stated above in <a href="../spaces-dimension/#thm-dim-cap-sum" data-reference-type="ref+Label" data-reference="thm:dim-cap-sum">Theorem 3.77</a>) <span id="thm-dim-cap-sum-revisited" label="thm:dim-cap-sum-revisited"></span> Suppose $A, B \subset V$ are two subspaces of a vector space. Then
<div class="arithmatex" markdown="1">
\[
\dim (A \cap B) + \dim (A + B) = \dim A + \dim B.
\]
</div>

<p class="env-number equation-number"><strong>(4.36)</strong></p>

<span id="eqn-dim-cap-sum-revisited" label="eqn.dim.cap.sum.revisited"></span>

</div>

<div class="proof" markdown="1">

*Proof.* The map
<div class="arithmatex" markdown="1">
\[
f : A \oplus B \to V, (a, b) \mapsto a-b
\]
</div>
is linear. Since for every $b \in B$ also $b' := -b$ is contained in $B$, the image of this map is $A + B$. The kernel of $f$ consists of those vectors $(a,b) \in A \oplus B$ such that $a - b = 0$, i.e., $a = b$. This means that $a \in A \cap B$. Therefore, the rank nullity theorem and <a href="../spaces-dimension/#ex-dimensions-examples" data-reference-type="ref+Label" data-reference="ex:dimensions-examples">Example 3.67</a> tell us
<div class="arithmatex" markdown="1">
\[
\dim (A \cap B) + \dim (A + B) = \dim \ker f + \dim {\operatorname{im}\ } f = \dim (A \oplus B) = \dim A + \dim B.
\]
</div>
 ◻

</div>

<div id="refs" class="references csl-bib-body hanging-indent">

<div id="ref-Nicholson:Linear" class="csl-entry">

Nicholson, W. K. 1995. *Linear Algebra with Applications*. Mathematics Series. PWS Publishing Company. <https://lyryx.com/linear-algebra-applications/>.

</div>

</div>
