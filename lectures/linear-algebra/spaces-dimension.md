---
title: Dimension
---

# The dimension of a vector space

We are all used to referring to the space surrounding us as “3-dimensional”, and refer to a plane as “2-dimensional”. In this section, which is crucial to linear algebra and, by extension to all applications of linear algebra in physics, engineering and mathematics itself, we make this statement precise.

<div class="theorem" markdown="1">


<p class="env-number"><strong>Theorem 3.65</strong></p>

<span id="thm-spaces-theorem-001" label="thm:spaces-theorem-001"></span> Let $V$ be a vector space with a basis $v_1, \dots, v_n$. Then any other basis of $V$ also consists of $n$ vectors.

</div>

In other words, the number of vectors in a basis does *not* depend on the basis. (Recall from <a href="../spaces-bases/#ex-three-vectors-basis" data-reference-type="ref+Label" data-reference="ex:three-vectors-basis">Example 3.63</a> that the vectors that form a basis may very well be different.)

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 3.66</strong></p>

<span id="def-spaces-definition-013" label="def:spaces-definition-013"></span> <span id="def-dimension" label="def:dimension"></span> We say that a vector space $V$ has *dimension* $n$ if there is a basis of $V$ with $n$ elements.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 3.67</strong></p>

<span id="ex-dimensions-examples" label="ex:dimensions-examples"></span> The standard basis of ${\bf R}^n$ consists of $n$ elements (<a href="../spaces-bases/#ex-standard-basis" data-reference-type="ref+Label" data-reference="ex:standard-basis">Example 3.62</a>), so that
<div class="arithmatex" markdown="1">
\[
\dim {\bf R}^n = n.
\]
</div>

The space of polynomials of degree at most $d$ has a basis $1, x, x^2, \dots, x^d$. These are $d+1$ polynomials so that
<div class="arithmatex" markdown="1">
\[
\dim {\bf R}[x]^{\le d} = d + 1.
\]
</div>

</div>

<div class="remark" markdown="1">


<p class="env-number"><strong>Remark 3.68</strong> (Related exercises: <a href="../exercises-maps/#ex-maps-partial-2026-1">Exercise 4.46</a>)</p>

<span id="rem-dimension-direct-sum" label="rem:dimension-direct-sum"></span> If $V$ has a basis $v_1, \dots, v_n$ (so that $\dim V = n$) and another vector space $W$ has a basis $w_1, \dots, w_m$ (and $\dim W = m)$, then a basis of the direct sum $V \oplus W$ is given by
<div class="arithmatex" markdown="1">
\[
(v_1, 0), \dots, (v_n, 0), (0, w_1), \dots, (0, w_m).
\]
</div>
These are $n+m$ vectors, so that
<div class="arithmatex" markdown="1">
\[
\dim (V \oplus W) = \dim V + \dim W.
\]
</div>

</div>

<div class="theorem" markdown="1">


<p class="env-number"><strong>Theorem 3.69</strong></p>

<span id="thm-spaces-theorem-002" label="thm:spaces-theorem-002"></span> Every vector space has a basis.

</div>

<div class="remark" markdown="1">


<p class="env-number"><strong>Remark 3.70</strong></p>

<span id="rem-spaces-remark-009" label="rem:spaces-remark-009"></span> In this course, we only consider vector spaces with a basis consisting of finitely many vectors, as in <a href="../spaces-bases/#def-basis" data-reference-type="ref+Label" data-reference="def:basis">Definition 3.61</a>. We call such vector spaces *finite-dimensional*.

An example of a vector space not having a finite basis (i.e., an *infinite-dimensional* vector space) is ${\bf R}[x]$ (for which a basis is given by the polynomials $1, x, x^2, x^3, \dots$).

</div>

The following theorem addresses the question how linearly independent sets can be extended to a basis.

<div class="theorem" markdown="1">


<p class="env-number"><strong>Theorem 3.71</strong> (Related exercises: <a href="../exercises-maps/#ex-maps-3-16">Exercise 4.38</a>, <a href="../exercises-maps/#ex-maps-3-20">Exercise 4.44</a>, <a href="../exercises-maps/#ex-maps-3-6">Exercise 4.16</a>, <a href="../exercises-maps/#ex-maps-exercise-011">Exercise 4.11</a>, <a href="../exercises-maps/#ex-maps-partial-2026-1">Exercise 4.46</a>, <a href="../exercises-spaces/#ex-three-vectors-r2">Exercise 3.8</a>)</p>

<span id="thm-basis-theorem" label="thm:basis-theorem"></span>

1.  <span id="item-generators-remove" label="item--generators.remove"></span> Suppose that some vector space $V$ is spanned by $m$ vectors $v_1, \dots, v_m$ (<a href="../spaces-linear-combinations/#def-generating-system" data-reference-type="ref+Label" data-reference="def:generating-system">Definition 3.42</a>). Then a basis of $V$ can be obtained by removing certain vectors among the $v_1, \dots, v_m$. In particular, this says that $V$ *has* a basis and that
<div class="arithmatex" markdown="1">
\[
    \dim V \le m
\]
</div>
(and so, in particular that $V$ is finite-dimensional.)

2.  <span id="item-independent-add" label="item--independent.add"></span> Every linearly independent set of vectors can be enlarged to a basis by adding appropriate vectors from any given basis of $V$. (I.e., if $v_1, \dots, v_n$ are linearly independent, and $w_1, \dots, w_m$ is any basis of $V$, then the $v_1, \dots, v_n$ together with certain vectors among the $w_1, \dots, w_m$ form a basis.) In particular, if $v_1, \dots, v_n$ are linearly independent, then
<div class="arithmatex" markdown="1">
\[
    \dim V \ge n.
\]
</div>

3.  <span id="item-dim-subspace" label="item--dim.subspace"></span> If $W \subset V$ is a subspace, then $\dim W \le \dim V$. (In particular, if $V$ is finite-dimensional, then so is $W$.) Moreover, we have $\dim W = \dim V$ precisely if $W = V$.

4.  For a subspace $W \subset V$, any basis of $W$ can be extended to a basis of $V$.

</div>

<div class="proof" markdown="1">

*Proof.* This is proved in any linear algebra textbook, e.g., (Nicholson 1995, Theorem 6.4.1) or (Bottacin 2021, sec. 1.3). ◻

</div>



<iframe src="../visualizations/linear-independence-3d.html" style="width:100%;height:520px;border:none;border-radius:6px;" loading="lazy"></iframe>

Linear indepdendence, span and basis property of several vectors in $\bf R^3$

<div class="example" markdown="1">


<p class="env-number"><strong>Example 3.72</strong></p>

<span id="ex-spaces-example-023" label="ex:spaces-example-023"></span> In $V = {\bf R}^3$, consider the four vectors $v_1 = (1,1,-1)$, $v_2 = (2,0,1)$, $v_3= (-1,1,-2)$, $v_4 = (1,2,1)$. We apply <a href="../spaces-linear-combinations/#met-check-generating-system" data-reference-type="ref+Label" data-reference="met:check-generating-system">Method 3.46</a> and <a href="../spaces-linear-independence/#met-check-linear-independence" data-reference-type="ref+Label" data-reference="met:check-linear-independence">Method 3.56</a> by forming the associated matrix and bringing it into row echelon form:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left ( \begin{array}{c} v_1 \\ v_2 \\ v_3 \\ v_4 \end{array} \right ) & = \left ( \begin{array}{ccc} 1 & 1 & -1 \\ 2 & 0 & 1 \\ -1 & 1 & -2 \\ 1 & 2 & 1 \end{array} \right ) \leadsto 
\left ( \begin{array}{ccc} 1 & 1 & -1 \\ 0 & -2 & 3 \\ 0 & 2 & -3 \\ 0 & 1 & 2 \end{array} \right ) 
\\ & \leadsto
\left ( \begin{array}{ccc} 1 & 1 & -1 \\ 0 & 1 & -\frac 32 \\ 0 & 0 & 0 \\ 0 & 0 & \frac 72 \end{array} \right ) \leadsto
\left ( \begin{array}{ccc} 1 & 1 & -1 \\ 0 & 1 & -\frac 32 \\ 0 & 0 & 0 \\ 0 & 0 & 1 \end{array} \right )
\end{align*}
\]
</div>
(First step: add certain multiples of the first row to the others, second step: multiply second row by $- \frac 12$ and add multiples to the third and last row, third step: divide the last row by $\frac 72$.) We can swap the last two rows and obtain a row echelon matrix. This matrix has *three* leading ones, so that the four vectors generate ${\bf R}^3$ but are not linearly independent. (We also know $\dim V = 3$, so these four vectors can not be linearly independent by <a href="#thm-basis-theorem" data-reference-type="ref+Label" data-reference="thm:basis-theorem">Theorem 3.71</a><a href="#item-independent-add" data-reference-type="ref" data-reference="item--independent.add">2.</a>.) According to <a href="#thm-basis-theorem" data-reference-type="ref+Label" data-reference="thm:basis-theorem">Theorem 3.71</a><a href="#item-generators-remove" data-reference-type="ref" data-reference="item--generators.remove">1.</a>, we can obtain a basis by removing certain vectors among these. Notice that one may not (in general) remove just any arbitrary of the four vectors. In this example,

- the first three vectors $v_1, v_2, v_3$ do *not* form a basis,

- however $v_1, v_2, v_4$ *do* form a basis.

Indeed, this holds since in the above matrix, we remove either the last row, which brings us to
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{c} v_1 \\ v_2 \\ v_3 \end{array} \right ) \leadsto \left ( \begin{array}{ccc} 1 & 1 & -1 \\ 0 & 1 & -\frac 32 \\ 0 & 0 & 0 \end{array} \right ).
\]
</div>
This tells us that these three vectors are (still) not linearly independent (and don’t span ${\bf R}^3$). By contrast, removing the third row, gives
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{c} v_1 \\ v_2 \\ v_4 \end{array} \right ) \leadsto \left ( \begin{array}{ccc} 1 & 1 & -1 \\ 0 & 1 & -\frac 32 \\ 0 & 0 & 1 \end{array} \right )
\]
</div>
which has three leading ones, so these three vectors form a basis of ${\bf R}^3$.

</div>

<div class="corollary" markdown="1">


<p class="env-number"><strong>Corollary 3.73</strong> (Related exercises: <a href="../exercises-spaces/#ex-polynomial-basis-ab">Exercise 3.21</a>, <a href="../exercises-spaces/#ex-r2-spanning">Exercise 3.18</a>, <a href="../exercises-spaces/#ex-spanning-r4">Exercise 3.6</a>)</p>

<span id="cor-indep-span" label="cor:indep-span"></span> Let $V$ be a vector space with $\dim V = n$. Let $n$ vectors be given: $v_1, \dots, v_n$. These vectors are linearly independent if and only if they span $V$.

</div>

<div class="proof" markdown="1">

*Proof.* This follows from the theorem above. For example, suppose they span $V$. If they are not linearly independent, then some $v_i$ lies in the span of the remaining vectors. Thus $V$ is the span of all vectors but $v_i$ so that $n-1 \ge \dim V$ by <a href="#thm-basis-theorem" data-reference-type="ref+Label" data-reference="thm:basis-theorem">Theorem 3.71</a><a href="#item-generators-remove" data-reference-type="ref" data-reference="item--generators.remove">1.</a>. This is a contradiction to our assumption.

The converse implication is proved similarly. ◻

</div>

<div class="remark" markdown="1">


<p class="env-number"><strong>Remark 3.74</strong></p>

<span id="rem-spaces-remark-010" label="rem:spaces-remark-010"></span> If $V = {\bf R}^n$, then <a href="#cor-indep-span" data-reference-type="ref+Label" data-reference="cor:indep-span">Corollary 3.73</a> aligns well with <a href="../spaces-linear-combinations/#met-check-generating-system" data-reference-type="ref+Label" data-reference="met:check-generating-system">Method 3.46</a> vs. <a href="../spaces-linear-independence/#met-check-linear-independence" data-reference-type="ref+Label" data-reference="met:check-linear-independence">Method 3.56</a>: we consider the matrix
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{c} v_1 \\ v_2 \\ \vdots \\ v_m \end{array} \right ) \leadsto B
\]
</div>
and bring it into row echelon form, denoted $B$. Note that ($A$ and) $B$ are $n \times n$-matrices. Thus, the vectors $v_1, \dots, v_n$ span ${\bf R}^n$ if and only if $B$ has $n$ leading ones, which happens if and only if $v_1, \dots, v_n$ are linearly independent.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 3.75</strong> (Related exercises: <a href="../exercises-spaces/#ex-polynomial-basis-change">Exercise 3.20</a>)</p>

<span id="ex-spaces-example-024" label="ex:spaces-example-024"></span> Let $a \in {\bf R}$ be a fixed real number. Consider the vector space ${\bf R}[x]^{\le d}$. The polynomials
<div class="arithmatex" markdown="1">
\[
v_0 (x) = (x-a)^0 = 1, v_1 (x) = (x-a), \dots, v_{d} (x) = (x-a)^{d}
\]
</div>
are linearly independent. To see this, suppose
<div class="arithmatex" markdown="1">
\[
0 = a_0 v_0 + a_1 v_1 + \dots + a_{d} v_{d}.
\]
</div>
Note that $v_{d}$ has degree $d$, all the remaining ones have degree $\le d-1$. Thus, looking at the coefficient for $x^d$, we see $a_{d} = 0$. Continuing this, we note that
<div class="arithmatex" markdown="1">
\[
0 = a_0 v_0 + a_1 v_1 + \dots + a_{d-1} v_{d-1}
\]
</div>
forces $a_{d-1}=0$ (by looking at the coefficient of $x^{d-1}$). Repeating this argument, one sees that $a_0 = \dots = a_d = 0$.

We know $\dim {\bf R}[x]^{\le d} = d+1$ (<a href="#ex-dimensions-examples" data-reference-type="ref+Label" data-reference="ex:dimensions-examples">Example 3.67</a>). Thus, by <a href="#cor-indep-span" data-reference-type="ref+Label" data-reference="cor:indep-span">Corollary 3.73</a>, these polynomials $v_0, \dots, v_d$ form a basis. According to <a href="../spaces-bases/#prop-basis-coordinate-system" data-reference-type="ref+Label" data-reference="prop:basis-coordinate-system">Proposition 3.64</a>, *any* polynomial $f(x)$ of degree $\le d$ therefore can be *uniquely* written as
<div class="arithmatex" markdown="1">
\[
f(x) = a_0 + a_1(x-a) + \dots + a_d(x-a)^d.
\]
</div>
Thus, every polynomial can be expressed as a sum of powers of $x-a$. (By definition of a polynomial, it can certainly be expressed as a sum of powers of $x-0 = x$.) The precise values of $a_d$ are closely related to the *Taylor series* familiar from analysis.

</div>

## Dimensions of sums and intersections

In this section, we give an answer to <a href="../spaces-intersection/#q-dimension-intersection" data-reference-type="ref+Label" data-reference="q:dimension-intersection">Question 3.21</a> and <a href="../spaces-linear-combinations/#q-dimension-sum" data-reference-type="ref+Label" data-reference="q:dimension-sum">Question 3.41</a>. Colloquially, the possible failure of $A + B$ being “as large as possible” (i.e., having the maximum possible dimension, namely $\dim A + \dim B$) is closely related to the possible failure of $A \cap B$ being “as small as possible.” Before stating that, we note another consequence of <a href="#thm-basis-theorem" data-reference-type="ref+Label" data-reference="thm:basis-theorem">Theorem 3.71</a>.

<div class="corollary" markdown="1">


<p class="env-number"><strong>Corollary 3.76</strong> (Related exercises: <a href="../exercises-spaces/#ex-spaces-2-4">Exercise 3.25</a>)</p>

<span id="cor-dim-sum-inequality" label="cor:dim-sum-inequality"></span> Suppose $A, B \subset V$ are two subspaces with $\dim A = m$ and $\dim B = n$. Then
<div class="arithmatex" markdown="1">
\[
\dim (A + B) \le \dim A + \dim B.
\]
</div>
(Here, at the left + denotes the sum of the two subspaces (<a href="../spaces-linear-combinations/#def-sum-of-vector-spaces" data-reference-type="ref+Label" data-reference="def:sum-of-vector-spaces">Definition 3.36</a>), while at the right it is the sum of the two dimensions.)

</div>

<div class="proof" markdown="1">

*Proof.* If $v_1, \dots, v_m$ is a basis of $A$ and $w_1, \dots, w_n$ is a basis of $B$, then they in particular span $A$, resp. $B$. Thus, $A + B$ is spanned by
<div class="arithmatex" markdown="1">
\[
v_1, \dots, v_m, w_1, \dots, w_n.
\]
</div>
These are $m+n$ vectors. According to <a href="#thm-basis-theorem" data-reference-type="ref+Label" data-reference="thm:basis-theorem">Theorem 3.71</a><a href="#item-generators-remove" data-reference-type="ref" data-reference="item--generators.remove">1.</a>, this implies
<div class="arithmatex" markdown="1">
\[
\dim (A+B) \le m+n.
\]
</div>
 ◻

</div>

<div class="theorem" markdown="1">


<p class="env-number"><strong>Theorem 3.77</strong> (Related exercises: <a href="../exercises-maps/#ex-maps-partial-2026-1">Exercise 4.46</a>, <a href="../exercises-spaces/#ex-spaces-2-4">Exercise 3.25</a>, <a href="../exercises-spaces/#ex-sum-intersection-r4">Exercise 3.26</a>)</p>

<span id="thm-dim-cap-sum" label="thm:dim-cap-sum"></span> Suppose $A, B \subset V$ are two subspaces of a vector space. Then
<div class="arithmatex" markdown="1">
\[
\dim (A \cap B) + \dim (A + B) = \dim A + \dim B.
\]
</div>

<p class="env-number equation-number"><strong>(3.78)</strong></p>

<span id="eqn-dim-cap-sum" label="eqn.dim.cap.sum"></span>

</div>

This is a special case of a more general theorem, the so-called *rank-nullity theorem* (<a href="../maps-kernel-and-image-1/#thm-rank-nullity-theorem" data-reference-type="ref+Label" data-reference="thm:rank-nullity-theorem">Theorem 4.26</a>). We illustrate it at the hand of subspaces in $V = {\bf R}^2$. If $A \subset V$ is a subspace, then exactly one of the following three cases occurs:

- $\dim A = 0$. This means that $A$ just consists of the zero vector: $A = \{ 0 \}$.

- $\dim A = 1$. This means that there is a basis of $A$ consisting of a single vector $v \in A$. Since $v$ is linearly independent, we have $v \ne 0$ (otherwise $1 \cdot v = 0$ is a non-trivial linear combination giving the zero vector). Since $v$ spans $A$, this means $A = \{ a v \ | \ a \in {\bf R}\}$. Thus, $A$ is the line spanned by the (non-zero) vector $v$.

- $\dim A = 2$. In this case we necessarily have $A = {\bf R}^2$ by <a href="#thm-basis-theorem" data-reference-type="ref+Label" data-reference="thm:basis-theorem">Theorem 3.71</a><a href="#item-dim-subspace" data-reference-type="ref" data-reference="item--dim.subspace">3.</a>.

Of course, for another subspace $B$ the same three cases apply. If $A = \{0\}$, then $A \cap B = \{0 \}$ and $A + B = B$, so in this case the dimension formula <a href="#eqn-dim-cap-sum" data-reference-type="eqref" data-reference="eqn.dim.cap.sum">Equation (3.78)</a> just reads
<div class="arithmatex" markdown="1">
\[
\dim (\{0\}) + \dim B = \dim (\{0\}) + \dim B,
\]
</div>
which does not give anything interesting. Similarly, if $A = {\bf R}^2$, then $A \cap B = B$ and $A + B = {\bf R}^2$, so the dimension formula reads
<div class="arithmatex" markdown="1">
\[
\dim B + \dim {\bf R}^2 = \dim {\bf R}^2 + \dim B.
\]
</div>
Again, this is tautological. The interesting case is therefore when $\dim A = 1$ and, by symmetry, $\dim B = 1$. Thus both $A$ and $B$ are lines, passing through the origin, in ${\bf R}^2$. We distinguish two cases:

- $A = B$. In this case $A \cap B = A$, $A + B = A$, so the formula reads
<div class="arithmatex" markdown="1">
\[
  1 + 1 = 1 + 1,
\]
</div>
  which is true.

- $A \ne B$. In this case $A \cap B = \{ 0 \}$, since the lines are distinct and therefore only interesect at the origin. Then the formula says
<div class="arithmatex" markdown="1">
\[
  0 + \dim (A + B) = 1 + 1 = 2.
\]
</div>
  Thus $\dim (A+B) = 2$, which means that $A + B = {\bf R}^2$, again using <a href="#thm-basis-theorem" data-reference-type="ref+Label" data-reference="thm:basis-theorem">Theorem 3.71</a><a href="#item-dim-subspace" data-reference-type="ref" data-reference="item--dim.subspace">3.</a>.

Here is a picture of the two cases:

<div class="center" markdown="1">

|  |  |
|:--:|:--:|
| $A = B$ | $A \ne B$ |
| ![image](figures/png/spaces/spaces-fig-10.png) | ![image](figures/png/spaces/spaces-fig-11.png) |

</div>

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 3.79</strong></p>

<span id="def-spaces-definition-014" label="def:spaces-definition-014"></span> Let $A, B \subset V$ be two subspaces. We say “the sum $A + B$ is a direct sum” if $\dim A + \dim B = \dim A + B$.

</div>

In other words, $\dim (A + B)$ needs to be as large as possible. In the example of two lines, i.e., $\dim A = \dim B = 1$, the sum is direct precisely if $A + B = {\bf R}^2$.

<div class="example" markdown="1">


<p class="env-number"><strong>Example 3.80</strong></p>

<span id="ex-spaces-example-025" label="ex:spaces-example-025"></span> In $V = {\bf R}^3$, consider subspaces $A, B \subset {\bf R}^3$ with $\dim A =1$ and $\dim B = 2$. Thus, geometrically, $A$ is a line passing through the origin and $B$ is a plane passing through the origin. We have
<div class="arithmatex" markdown="1">
\[
0 \subset A \cap B \subset A.
\]
</div>
This means that
<div class="arithmatex" markdown="1">
\[
0 \le \dim (A \cap B) \le \dim A = 1.
\]
</div>
We distinguish two cases:

- $A \subset B$. Equivalently, $A \cap B = A$ or, yet equivalently,
<div class="arithmatex" markdown="1">
\[
  \dim (A \cap B) = 1.
\]
</div>

- $A \nsubset B$. In this case $A \cap B \subsetneq A$. Since $A \cap B$ is a subspace of strictly smaller dimension, this implies $A \cap B = \{ 0\}$. Thus,
<div class="arithmatex" markdown="1">
\[
  \dim (A \cap B) = 0.
\]
</div>

To summarize, a line $A$ and a plane $B$ (both passing through the origin) in ${\bf R}^3$ intersect either in a point or in a line.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 3.81</strong></p>

<span id="ex-spaces-example-026" label="ex:spaces-example-026"></span> Consider $V={\bf R}^3$ and two subspaces $A, B \subset {\bf R}^3$ of dimension 2. Then the formula reads
<div class="arithmatex" markdown="1">
\[
\dim (A \cap B) = 2 + 2 - \dim (A + B).
\]
</div>
We have in any event $A, B \subset A + B \subset {\bf R}^3$, which implies
<div class="arithmatex" markdown="1">
\[
2 \le \dim (A+B) \le 3.
\]
</div>
We consider two cases:

- $A = B$. In this case $A \cap B = A$ and $A + B = A$, which both have dimension 2.

- $A \ne B$. In this case $A \cap B \subsetneq A$, so $A \cap B$ has dimension $< 2$. This means that $\dim (A+B) = 3$, and therefore
<div class="arithmatex" markdown="1">
\[
  \dim (A \cap B) = 1.
\]
</div>

We summarize this as follows: two planes $A$, $B$ passing through the origin in ${\bf R}^3$ intersect either in a plane (this happens precisely if $A = B$), or they interesect in a line (this happens precisely if $A \ne B$).

</div>

If the ambient vector space has dimension $\ge 4$, and $\dim A, \dim B \ge 2$, then the possible dimensions of $\dim (A \cap B)$ and $\dim (A +B)$ are more varied, so we refrain from making a similar list.

<div id="refs" class="references csl-bib-body hanging-indent">

<div id="ref-Bottacin:Linear" class="csl-entry">

Bottacin, F. 2021. *Algebra Lineare e Geometria*. Società Editrice Esculapio; English translation available in moodle. <https://books.google.it/books?id=efxVEAAAQBAJ>.

</div>

<div id="ref-Nicholson:Linear" class="csl-entry">

Nicholson, W. K. 1995. *Linear Algebra with Applications*. Mathematics Series. PWS Publishing Company. <https://lyryx.com/linear-algebra-applications/>.

</div>

</div>
