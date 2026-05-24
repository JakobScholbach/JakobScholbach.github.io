---
title: Composing Linear Maps
---

# Composing linear maps and multiplying matrices

The following lemma, while simple to prove, is of fundamental importance:

<div class="definitionlemma" markdown="1">


<p class="env-number"><strong>Definition and Lemma 4.47</strong></p>

<span id="dlm-maps-definitionlemma-001" label="dlm:maps-definitionlemma-001"></span> Let $f : U \to V$ and $g: V \to W$ be two linear maps between three vector spaces $U$, $V$ and $W$. Then the *composition* of $g$ and $f$ is the map defined as
<div class="arithmatex" markdown="1">
\[
g \circ f : U \to W, u \mapsto g(f(u)).
\]
</div>
This map is again linear.

</div>

<div class="proof" markdown="1">

*Proof.* We check the two conditions in <a href="../maps-definition-and-first-examples/#def-linear-map" data-reference-type="ref+Label" data-reference="def:linear-map">Definition 4.1</a>: for $u, u' \in U$ and $a \in {\bf R}$, we have, using the linearity of $f$ and $g$:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
(g \circ f)(u+u') & = g(f(u+u')) \\
& = g(f(u) + f(u')) \\ & = g(f(u)) + g(f(u')) \\ & = (g \circ f)(u) + (g \circ f)(u') \\
(g \circ f)(au) & = g(f(au)) \\ & = g(af(u)) \\ & = a g(f(u)) \\ & = a (g \circ f)(u).
\end{align*}
\]
</div>
 ◻

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 4.48</strong></p>

<span id="ex-maps-example-018" label="ex:maps-example-018"></span> The maps $f : {\bf R}^2 \to {\bf R}$, $(x, y) \mapsto x$ and $g : {\bf R} \to {\bf R}^3$, $x \mapsto (x,0,x)$ are both linear. The composition $g \circ f$ is the map
<div class="arithmatex" markdown="1">
\[
g \circ f, (x, y) \mapsto g(f(x,y)) = g(x) = (x, 0, x).
\]
</div>

We may also consider $h : {\bf R} \to {\bf R}^2$, $x \mapsto (x, x)$. Then the composite
<div class="arithmatex" markdown="1">
\[
h \circ f, (x, y) \mapsto h(f(x,y)) = h(x) = (x, x).
\]
</div>
The other composite is also defined, it is
<div class="arithmatex" markdown="1">
\[
f \circ h : {\bf R} \to {\bf R}, x \mapsto f(h(x)) = f(x,x) = x.
\]
</div>
(By comparison, the composition $f \circ g$ is not defined, since $g$ takes values in ${\bf R}^3$, but $f$ is defined on ${\bf R}^2$.)

</div>

We now relate this composition of abstract maps to something more concrete, the product of matrices.

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 4.49</strong> (Related exercises: <a href="../exercises-maps/#ex-maps-exercise-016">Exercise 4.22</a>, <a href="../exercises-maps/#ex-maps-exercise-019">Exercise 4.26</a>, <a href="../exercises-maps/#matrices-commute">Exercise 4.20</a>, <a href="../exercises-maps/#trace">Exercise 4.24</a>)</p>

<span id="def-product-matrices" label="def:product-matrices"></span> If $A = (a_{ij})$ is a $m \times n$-matrix and $B = (b_{ij})$ is an $n \times k$-matrix, then the *product* $AB$ (also sometimes denoted by $A \cdot B$) is the $m \times k$-matrix whose entry in the $i$-th row and $j$-th column is the following (see §<a href="../appendix/#sect-notation" data-reference-type="ref" data-reference="sect--notation">Chapter A</a> for the sum notation $\sum$):
<div class="arithmatex" markdown="1">
\[
\sum_{e = 1}^n a_{ie} b_{ej} = a_{i1} b_{1j} + a_{i2} b_{2j} + \dots + a_{in} b_{nj}.
\]
</div>
In other “words”
<div class="arithmatex" markdown="1">
\[
AB := (\sum_{e = 1}^n a_{ie} b_{ej}).
\]
</div>
I.e., one picks the $i$-th row of $A$ and the $j$-th column of $B$; one traverses these and multiplies the corresponding entries together one by one and finally adds up these products.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 4.50</strong></p>

<span id="ex-maps-example-019" label="ex:maps-example-019"></span>
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left ( \begin{array}{cc} 1 & 2 \\ 3 & 4 \end{array} \right ) \left ( \begin{array}{cc} -1 & 0 \\ 6 & -2 \end{array} \right ) & = \left ( \begin{array}{cc} 1 \cdot (-1) + 2 \cdot 6 & 1 \cdot 0 + 2 \cdot (-2) \\ 3 \cdot (-1) + 4 \cdot 6 & 3 \cdot 0 + 4 \cdot (-2) \end{array} \right ) \\
& = \left ( \begin{array}{cc} 11 & -4 \\ 21 & -8 \end{array} \right ), \\
\left ( \begin{array}{ccc} 1 & -1 & 2 \\ 1 & 3 & -2 \end{array} \right ) \left ( \begin{array}{cc} 0 & 1 \\ 1 & 2 \\ 2 & 3 \end{array} \right ) & = \\
& = \\
\left ( \begin{array}{cc} 0 & 1 \\ 1 & 2 \\ 2 & 3 \end{array} \right ) \left ( \begin{array}{ccc} 1 & -1 & 2 \\ 1 & 3 & -2 \end{array} \right ) & = \\
& = \\
\left ( \begin{array}{cc} 1 & x \\ 0 & 1 \end{array} \right ) \left ( \begin{array}{cc} 1 & y \\ 0 & 1 \end{array} \right ) & = \\
& =
\end{align*}
\]
</div>
Note that the second product is a $2 \times 2$-matrix while the product of the *same* matrices in the other order is a $3 \times 3$-matrix!

The product $AB$ is *only* defined if the number of columns of $A$ is the same as the number of rows of $B$. For example,
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc} 0 & 1 & 1 \\ 2 & 2 & 3 \end{array} \right ) \left ( \begin{array}{cc} 3 & 4 \\ 5 & 6 \end{array} \right )
\]
</div>
is *not* defined, i.e., it is a meaningless expression.

</div>

<div class="remark" markdown="1">


<p class="env-number"><strong>Remark 4.51</strong></p>

<span id="rem-maps-remark-004" label="rem:maps-remark-004"></span> In the case when $B$ is a column vector with $n$ entries, we can regard it as an $n \times 1$-matrix. In this case the product $A B$ defined in <a href="#def-product-matrices" data-reference-type="ref+Label" data-reference="def:product-matrices">Definition 4.49</a> is an $m \times 1$-matrix, which agrees with the column vector $AB$ as defined in <a href="../maps-multiplication-of-a-matrix/#def-product-matrix-vector" data-reference-type="ref+Label" data-reference="def:product-matrix-vector">Definition 4.9</a>, so the product considered now is a generalization of that previous construction. In general, if $B$ is an $n \times k$-matrix, we can write it as
<div class="arithmatex" markdown="1">
\[
B = (b_1 \ b_2 \ \dots \ b_n),
\]
</div>
where the $b_1, \dots, b_n$ are the columns of $B$. Then
<div class="arithmatex" markdown="1">
\[
AB = (Ab_1 \ Ab_2 \ \dots \ Ab_n).
\]
</div>

</div>

In <a href="../maps-multiplication-of-a-matrix/#prop-matrix-linear-map" data-reference-type="ref+Label" data-reference="prop:matrix-linear-map">Proposition 4.19</a>, we associated to an $m \times n$-matrix $A$ a linear map
<div class="arithmatex" markdown="1">
\[
f : {\bf R}^n \to {\bf R}^m, v \mapsto Av.
\]
</div>
Let us also be given an $n \times l$-matrix $B$, to which we can assign the linear map
<div class="arithmatex" markdown="1">
\[
g : {\bf R}^l \to {\bf R}^n, u \mapsto Bu.
\]
</div>

<div class="proposition" markdown="1">


<p class="env-number"><strong>Proposition 4.52</strong> (Related exercises: <a href="../exercises-maps/#ex-maps-exercise-016">Exercise 4.22</a>)</p>

<span id="prop-composition-matrices" label="prop:composition-matrices"></span> In the above situation, the compositition $f \circ g : {\bf R}^l \to {\bf R}^n$ is the map given by multiplication by the matrix $AB$, i.e., the linear map
<div class="arithmatex" markdown="1">
\[
u \mapsto (AB)u.
\]
</div>

</div>

<div class="proof" markdown="1">

*Proof.* Let us write $C = AB$ for the product of $A$ and $B$. It is an $m \times l$-matrix. If we write $C = (c_{ij})$, we have
<div class="arithmatex" markdown="1">
\[
c_{ij} = \sum_{r=1}^n a_{ir} b_{rj}.
\]
</div>

<p class="env-number equation-number"><strong>(4.53)</strong></p>

<span id="eqn-asdkajsdlakdsj" label="eqn--asdkajsdlakdsj"></span>

We have to compare two linear maps, ${\bf R}^l \to {\bf R}^n$, namely $f \circ g$ and $u \mapsto Cu = (AB)u$. According to <a href="../maps-linear-maps-defined-on-basis-vectors/#prop-linear-map-defined-on-basis" data-reference-type="ref+Label" data-reference="prop:linear-map-defined-on-basis">Proposition 4.40</a>, it suffices to show that these two maps give the same values when we evaluate them on some basis of ${\bf R}^n$, for which we take the standard basis $e_1, \dots, e_n$. As was noted in , the product $C e_i$ is precisely the $i$-th column of $C$. That is,
<div class="arithmatex" markdown="1">
\[
C e_i = \left ( \begin{array}{c} c_{1i} \\ \vdots \\ c_{mi} \end{array} \right ) = c_{1i} e_1 + \dots + c_{mi} e_m = \sum_{s=1}^m c_{si} e_s = \sum_{s=1}^m \sum_{r=1}^n a_{sr} b_{ri} e_s.
\]
</div>
Similarly,
<div class="arithmatex" markdown="1">
\[
f(e_i) = A e_i = \sum_{s=1}^m a_{si} e_s
\]
</div>
and
<div class="arithmatex" markdown="1">
\[
g(e_i) = B e_i = \sum_{r=1}^n b_{ri} e_r.
\]
</div>
Here, as usual, $e_1, \dots$ denotes the standard basis vectors of ${\bf R}^n$, ${\bf R}^m$ and ${\bf R}^l$. We now compute
<div class="arithmatex" markdown="1">
\[
\begin{align*}
(f \circ g)(e_i) & = f(g(e_i)) \\
& = f (\sum_{r=1}^n b_{ri} e_r) \\
& = \sum_{r=1}^n b_{ri} f(e_r) & (f \text{ is linear})\\
& = \sum_{r=1}^n b_{ri} \sum_{s=1}^m a_{sr} e_s \\
& = \sum_{r=1}^n \sum_{s=1}^m b_{ri} a_{sr} e_s \\
& = \sum_{s=1}^m \sum_{r=1}^n a_{sr} b_{ri} e_s \\
& = \sum_{s=1}^m c_{si} e_s. & \text{ by \refeq{asdkajsdlakdsj}}.
\end{align*}
\]
</div>
 ◻

</div>

With similar arguments, one proves the following:

<div class="proposition" markdown="1">


<p class="env-number"><strong>Proposition 4.54</strong></p>

<span id="prop-maps-proposition-008" label="prop:maps-proposition-008"></span> Let $f : U \to V$ and $g : V \to W$ be two linear maps, and let $u_1, \dots, u_l$, $v_1, \dots, v_m$ and $w_1, \dots, w_n$ be bases of these vector spaces. Finally, let $A$ be the matrix of $f$ with respect to these bases (of $U$ and $V$) and $B$ the matrix of $g$ with respect to these bases (of $V$ and $W$). Then $BA$ is the matrix of $g \circ f$ with respect to the bases (of $U$ and $W$).

</div>

## Properties of matrix multiplication

### Dependence on the order of factors

A key property of matrix multiplication is that the product of two matrices depends on the *order* of the factors.

<div class="warning" markdown="1">


<p class="env-number"><strong>Warning 4.55</strong> (Related exercises: <a href="../exercises-maps/#matrices-commute">Exercise 4.20</a>, <a href="../exercises-maps/#trace">Exercise 4.24</a>)</p>

<span id="war-not-commutative" label="war:not-commutative"></span> For two $n \times n$-matrices $A$ and $B$, their product depends on the order of the two matrices. In other words, in general
<div class="arithmatex" markdown="1">
\[
AB \ne BA !
\]
</div>
Mark these words! It is a common misconception among linear algebra-learners to think that $AB$ would (always) be equal to $BA$.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 4.56</strong></p>

<span id="ex-maps-example-020" label="ex:maps-example-020"></span> Examples are not hard to come by:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left ( \begin{array}{cc} 1 & 1 \\ 0 & 1 \end{array} \right ) \left ( \begin{array}{cc} 1 & 0 \\ 1 & 1 \end{array} \right ) & = 
\left ( \begin{array}{cc} 2 & 1 \\ 1 & 1 \end{array} \right ) \\
\left ( \begin{array}{cc} 1 & 0 \\ 1 & 1 \end{array} \right ) \left ( \begin{array}{cc} 1 & 1 \\ 0 & 1 \end{array} \right ) & = 
\left ( \begin{array}{cc} 1 & 1 \\ 1 & 2 \end{array} \right ) \\
\end{align*}
\]
</div>
So that
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cc} 1 & 1 \\ 0 & 1 \end{array} \right ) \left ( \begin{array}{cc} 1 & 0 \\ 1 & 1 \end{array} \right )  \ne \left ( \begin{array}{cc} 1 & 0 \\ 1 & 1 \end{array} \right ) \left ( \begin{array}{cc} 1 & 1 \\ 0 & 1 \end{array} \right ) !
\]
</div>

</div>

<div class="remark" markdown="1">


<p class="env-number"><strong>Remark 4.57</strong></p>

<span id="rem-maps-remark-005" label="rem:maps-remark-005"></span> The phenomenon $AB \ne BA$ may be best understood in the light of composition of (linear) maps: if $f : {\bf R}^n \to {\bf R}^n$ and $g : {\bf R}^n \to {\bf R}^n$ is another linear map, then in general we have
<div class="arithmatex" markdown="1">
\[
g \circ f \ne f \circ g.
\]
</div>
To take a concrete example, consider the linear map $f : {\bf R}^2 \to {\bf R}^2$ given by reflecting along the $x$-axis, and $g : {\bf R}^2 \to {\bf R}^2$ the linear map given by rotating counter-clockwise (around the origin) by $90^\circ$.

<div class="center" markdown="1">

![image](figures/png/maps/maps-fig-08.png)

</div>

Let us conclude this discussion by noting that this issue is not specific to linear algebra, but is a common phenomenon in daily life: there is (often) no reason to expect that doing (the same) two actions in different order give the same result:

- You first do sports, then take a shower.

- You first take a shower, then do sports.

In the first scenario you may feel refreshed, in the second one a little sweaty...

</div>

### Further properties of matrix multiplication

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 4.58</strong> (Related exercises: <a href="../exercises-maps/#ex-maps-exercise-018">Exercise 4.25</a>)</p>

<span id="def-identity-matrix" label="def:identity-matrix"></span> The *identity matrix* is the square matrix
<div class="arithmatex" markdown="1">
\[
{\mathrm {id}} = \left ( \begin{array}{cccc} 1 & 0 & \dots & 0 \\ 0 & 1 & \dots & 0 \\ \vdots & & \ddots & \vdots \\ 0 & \dots & 0 & 1 \end{array} \right ).
\]
</div>
I.e., it is a square matrix whose entries on the “north-west – south-east” diagonal (which is called the *main diagonal*) are all 1, and the remaining entries are zero. If it is important to specify the size, one also writes ${\mathrm {id}}_n$.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 4.59</strong></p>

<span id="ex-maps-example-021" label="ex:maps-example-021"></span> If $n=1$, then ${\mathrm {id}}_1$ is just the $1 \times 1$-matrix whose only entry is 1. ${\mathrm {id}}_2 = \left ( \begin{array}{cc} 1 & 0 \\ 0 & 1 \end{array} \right )$.

</div>

The first two identities in the next lemma assert that the identity matrix takes the role of the number 1 when it comes to multiplying matrices.

<div class="lemma" markdown="1">


<p class="env-number"><strong>Lemma 4.60</strong> (Related exercises: <a href="../exercises-eigenvalues/#ex-eigenvalues-exercise-007">Exercise 6.10</a>, <a href="../exercises-maps/#ex-maps-3-18">Exercise 4.41</a>, <a href="../exercises-maps/#ex-maps-exercise-018">Exercise 4.25</a>, <a href="../exercises-maps/#matrices-commute">Exercise 4.20</a>)</p>

<span id="lem-matrix-multiplication-properties" label="lem:matrix-multiplication-properties"></span> Matrix multiplication satisfies the following identities, where $A$, $B$ and $C$ are matrices (of a size such that the products and sums below are defined), and $r \in {\bf R}$:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
{\mathrm {id}} A & = A \\
A {\mathrm {id}} & = A \\
A (B+C) & = AB + AC & \text{(distributivity)} \\
(A+B) C &= AC + BC \\
(AB)C &= A(BC) & \text{(associativity)} \\
r(AB) &= (rA)B = A (rB) & \text{(matrix vs.~scalar multiplication)}
\end{align*}
\]
</div>

</div>

<div class="proof" markdown="1">

*Proof.* These identities follow from similar identities for the multiplication and addition of real numbers.

To illustrate the principle, we consider the first distributivity law above. Let $A = (a_{ij})$ be an $m \times n$-matrix and $B, C$ two $n \times k$-matrices, $B = (b_{ij})$ and $C = (c_{ij})$. Then $B+C = (b_{ij}+c_{ij})$ so that
<div class="arithmatex" markdown="1">
\[
\begin{align*}
A(B+C) & = (\sum_{e = 1}^n a_{ie} (b_{ej} + c_{ej})) \\
& \stackrel ! = (\sum_{e = 1}^n a_{ie} b_{ej} + a_{ie} c_{ej}) \\
& = (\sum_{e = 1}^n a_{ie} b_{ej}) + (\sum_{e=1}^n a_{ie} c_{ej}) \\
& = AB + AC.
\end{align*}
\]
</div>
At the equality marked ! we have used the distributivity law for real numbers, i.e., the identity $e(f+g) = ef+eg$ for any $e, f, g \in {\bf R}$. ◻

</div>

### Multiplication with elementary matrices

We recast the elementary row operations of matrices (<a href="../systems-gaussian-elimination/#def-elementary-row-operations" data-reference-type="ref+Label" data-reference="def:elementary-row-operations">Definition 2.28</a>) in terms of multiplication with appropriate matrices. Below, we use the (standard) convention that an “invisible” entry in a matrix is zero, e.g. ${\mathrm {id}}_2 = \left ( \begin{array}{cc} 1 & 0 \\ 0 & 1 \end{array} \right )$ will be written as $\left ( \begin{array}{cc} 1 & {} \\ {} & 1 \end{array} \right )$ etc.

<div class="proposition" markdown="1">


<p class="env-number"><strong>Proposition 4.61</strong></p>

<span id="prop-multiplication-elementary-matrices" label="prop:multiplication-elementary-matrices"></span> Let $A$ be an $m \times n$-matrix.

1.  Let $A'$ be the matrix obtained by interchanging the $i$-th and the $j$-th row. Then
<div class="arithmatex" markdown="1">
\[
    A' = \underbrace{\left ( \begin{array}{ccccccc} 1 & & & & & & \\ & \ddots & & & & & \\ & & 0 & & 1 & & \\ & & & \ddots & & & \\ & & 1 & & 0 & & \\ & & & & & \ddots & \\ & & & & & & 1 \end{array} \right )}_{E^{(1)}_{i,j}} A.
\]
</div>
(The first matrix is the $m \times m$-matrix obtained from ${\mathrm {id}}_m$ by exchanging the $i$-th and the $j$-th row.)

2.  Let $A'$ be the matrix obtained by multiplying the $i$-th row with a real number $r$. Then
<div class="arithmatex" markdown="1">
\[
    A' =   \underbrace{\left ( \begin{array}{ccccccc} 1 & & & & & & \\ & \ddots & & & & & \\ & & 1 & & & & \\ & & & r & & & \\ & & & & 1 & & \\ & & & & & \ddots & \\ & & & & & & 1 \end{array} \right )}_{E^{(2)}_{i,r}} A .
\]
</div>
(The first matrix is the $m \times m$-matrix obtained from ${\mathrm {id}}_m$ by replacing the $(i,i)$-entry by $r$.)

3.  Let $A'$ be the matrix obtained by adding the $r$-th multiple of the $j$-th row to the $i$-th row. Then
<div class="arithmatex" markdown="1">
\[
    A' = \underbrace{\left ( \begin{array}{ccccccc} 1 & & & & & & \\ & \ddots & & & & & \\ & & 1 & & & & \\ & & & \ddots & & & \\ & & r & & 1 & & \\ & & & & & \ddots & \\ & & & & & & 1 \end{array} \right )}_{E^{(3)}_{i,j,r}} A.
\]
</div>
(The first matrix is the $m \times m$-matrix obtained from ${\mathrm {id}}_m$ by replacing the $(i,j)$-entry by $r$.)

</div>

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 4.62</strong> (Related exercises: <a href="../exercises-maps/#matrices-commute">Exercise 4.20</a>)</p>

<span id="def-elementary-matrices" label="def:elementary-matrices"></span> The matrices $E^{(1)}_{i,j}$, $E^{(2)}_{i,r}$ and $E^{(3)}_{i,j,r}$ (for any appropriate $i$, $j$ and any $r \in {\bf R}$, where $r \ne 0$ in $E^{(2)}_{i,r}$) appearing in the statement above are called *elementary matrices*.

</div>

<div class="proof" markdown="1">

*Proof.* This is a more cumbersome to write down precisely than to convince oneself by unwinding the definition. We check the third statement. If $B=(b_{ij})$ is the above matrix as stated, we have that $b_{ii} = 1$ and $b_{ij} = r$ and all other entries are zero. Let us write $C = BA$, $C = (c_{ij})$. Then, by definition,
<div class="arithmatex" markdown="1">
\[
c_{st} = \sum_{e=1}^m b_{se} a_{et}.
\]
</div>
We compute this sum:

- if $s \ne i$, then the only $b_{se}$ that is non-zero is $b_{ss} = 1$, so that
<div class="arithmatex" markdown="1">
\[
  c_{st} = b_{ss} a_{st} = a_{st}.
\]
</div>

- For $s = i$, the only coefficients $b_{se}$ that are non-zero are $b_{ss} = 1$ and $b_{sj} = r$. Thus, the sum above consists of two terms, and therefore
<div class="arithmatex" markdown="1">
\[
  c_{st} = b_{ss} a_{st} + b_{sj} a_{jt} = a_{st} + r a_{jt}.
\]
</div>

Thus the $i$-th row of $C$ equals the matrix $A'$ as in the statement above. ◻

</div>
