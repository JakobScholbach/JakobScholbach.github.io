---
title: Inverses
---

# Inverses

Given a linear map $f : V \to W$ it is a natural question whether the process of applying $f$ can be undone. For example, if $f$ encodes a counter-clockwise rotation in the plane by $60^\circ$, it can be undone by rotating clockwise by $60^\circ$. On the other hand, the linear map
<div class="arithmatex" markdown="1">
\[
{\bf R}^2 \to {\bf R}^2, (x, y) \mapsto (x,0)
\]
</div>
cannot be undone, since there is no way of recovering $(x,y)$ only from $x$.

<div class="definitionlemma" markdown="1">


<p class="env-number"><strong>Definition and Lemma 4.63</strong></p>

<span id="dlm-maps-definitionlemma-002" label="dlm:maps-definitionlemma-002"></span> Let $f : V \to W$ be a linear map. Then the following statements are equivalent (i.e., one holds precisely if the other holds):

1.  <span id="item-f-bij" label="item--f bij"></span> $f$ is bijective (<a href="../maps-kernel-and-image-1/#def-inj-surj-bij" data-reference-type="ref+Label" data-reference="def:inj-surj-bij">Definition 4.20</a>),

2.  <span id="item-f-inverse" label="item--f inverse"></span> There is a linear map $g : W \to V$ such that
<div class="arithmatex" markdown="1">
\[
    g \circ f = {\mathrm {id}}_V \text{ and } f \circ g = {\mathrm {id}}_W.
\]
</div>
(By definition of the composition (see also §<a href="../appendix/#sect-notation" data-reference-type="ref" data-reference="sect--notation">Chapter A</a>) this means $g(f(v)) = v$ for all $v \in V$ and $f \circ g = {\mathrm {id}}_{W}$ (i.e., $f(g(w)) = w$ for all $w \in W$.)

If this is the case, we call $f$ an *isomorphism*. In this event, the following statements hold:

- Such a map $g$ is unique. It is also called the *inverse* of $f$ and is denoted by $f^{-1}: W \to V$.

- $\dim V = \dim W$.

</div>

<div class="proof" markdown="1">

*Proof.* We only prove the direction <a href="#item-f-bij" data-reference-type="ref" data-reference="item--f bij">1.</a> $\Rightarrow$ <a href="#item-f-inverse" data-reference-type="ref" data-reference="item--f inverse">2.</a>. By assumption $f$ is bijective, i.e., the preimage $f^{-1}(w)$ consists of precisely one element, say $f^{-1}(w) = \{ v \}$. (That is, only for that vector do we have that $f(v) = w$.) We define a map $g: W \to V$ by $g(w) := v$.

To compute $g(f(v))$ we observe that $f^{-1}(f(v)) = \{ v\}$, since $v$ is the only element of $V$ that is mapped to $f(v)$. Thus $g(f(v))=v$.

To compute $f(g(w))$, say that $f^{-1}(w) = \{v\}$. This means in particular that $f(v) = w$. Then $g(w) = v$ and therefore $f(g(w)) = w$.

We show that $g$ is linear. Let $w, w' \in W$ be given. Let $v, v' \in V$ be the unique elements such that $f(v) = w$, $f(v')=w'$. By definition, this means $g(w)=v$, $g(w') = v'$. Then $w+w' = f(v+v')$, since $f$ is linear. Thus $g(w+w')=v+v'=g(w)+g(w')$. In a similar way, one shows $g(aw)=ag(w)$ for $a \in {\bf R}$.

If $g': W \to V$ is another map with $f(g'(w))=w$, as above, then
<div class="arithmatex" markdown="1">
\[
f(g'(w)) = f(g(w)).
\]
</div>
Since $f$ is injective, this implies $g'(w)=g(w)$. This shows that $g$ is unique.

The last statement holds by <a href="../maps-kernel-and-image-2/#cor-maps-dim" data-reference-type="ref+Label" data-reference="cor:maps-dim">Corollary 4.28</a><a href="../maps-kernel-and-image-2/#item-dim-bij" data-reference-type="ref" data-reference="item--dim bij">3.</a>. ◻

</div>

## Definition and unicity of inverses

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 4.64</strong></p>

<span id="def-invertible-matrix" label="def:invertible-matrix"></span> Let $A$ be an $n \times n$-matrix. Another $n \times n$-matrix $B$ is called an *inverse* of $A$ if
<div class="arithmatex" markdown="1">
\[
AB = {\mathrm {id}} \text{ and } BA = {\mathrm {id}}.
\]
</div>
If such a matrix $B$ exists, $A$ is called *invertible*.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 4.65</strong></p>

<span id="ex-maps-example-022" label="ex:maps-example-022"></span> $A = \left ( \begin{array}{cc} 0 & 1 \\ 1 & 1 \end{array} \right )$ is invertible, since $B = \left ( \begin{array}{cc} -1 & 1 \\ 1 & 0 \end{array} \right )$ is an inverse of $A$:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
AB & = \left ( \begin{array}{cc} 0 & 1 \\ 1 & 1 \end{array} \right ) \left ( \begin{array}{cc} -1 & 1 \\ 1 & 0 \end{array} \right ) = \\
BA & = \left ( \begin{array}{cc} -1 & 1 \\ 1 & 0 \end{array} \right ) \left ( \begin{array}{cc} 0 & 1 \\ 1 & 1 \end{array} \right ) = \\
\end{align*}
\]
</div>

</div>

Not every matrix has an inverse. An $1 \times 1$-matrix $A$, which is just a single real number $a$ is invertible precisely if $a \ne 0$. In this case the $1 \times 1$-matrix with entry $\frac 1a$ is an inverse. For larger matrices, it is not enough to be different from zero in order to be invertible, as the following example shows.

<div class="example" markdown="1">


<p class="env-number"><strong>Example 4.66</strong></p>

<span id="ex-not-invertible" label="ex:not-invertible"></span> The matrix
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{cc} 1 & 2 \\ 2 & 4 \end{array} \right )
\]
</div>
is *not* invertible. We prove this by taking an arbitrary $2 \times 2$-matrix $B = \left ( \begin{array}{cc} a & b \\ c & d \end{array} \right )$ and computing
<div class="arithmatex" markdown="1">
\[
A B = \left ( \begin{array}{cc} a+2c & b+2d \\ 2a+4c & 2b+4d \end{array} \right )
\]
</div>
Thus the condition $AB = {\mathrm {id}} = \left ( \begin{array}{cc} 1 & 0 \\ 0 & 1 \end{array} \right )$ amounts to four equations:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
a+2c & = 1 \\
b+2d& =0 \\
2a + 4c & = 0 \\
2b + 4d & = 1.
\end{align*}
\]
</div>
Indeed, multiplying the first equation by 2 gives $2a+4c=2$, and inserting the third equation gives a contradiction:
<div class="arithmatex" markdown="1">
\[
0 = 2a+4c = 2.
\]
</div>
Hence there is no such matrix $B$, so that $A$ is not invertible. We can observe that both the two rows of $A$ are linearly dependent, and also that the two columns of $A$ are linearly dependent. We will later prove that either of these two conditions are equivalent to $A$ *not* being invertible (<a href="../maps-transpose/#cor-rows-columns-independent" data-reference-type="ref+Label" data-reference="cor:rows-columns-independent">Corollary 4.94</a>).

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 4.67</strong></p>

<span id="ex-maps-example-024" label="ex:maps-example-024"></span> We revisit the reflection, rescaling, rotation and shearing matrices (<a href="../maps-multiplication-of-a-matrix/#ex-reflection-matrix" data-reference-type="ref+Label" data-reference="ex:reflection-matrix">Example 4.13</a> onwards) and compute their inverses:

<div class="center" markdown="1">

| Geometrical description | Matrix $A$ | Inverse matrix $A^{-1}$ |
|:---|:---|:---|
| Reflection at $x$-axis | $\left ( \begin{array}{cc} 1 & 0 \\ 0 & -1 \end{array} \right )$ | $\left ( \begin{array}{cc} 1 & 0 \\ 0 & -1 \end{array} \right )$ |
| Reflection at $y$-axis | $\left ( \begin{array}{cc} -1 & 0 \\ 0 & 1 \end{array} \right )$ | $\left ( \begin{array}{cc} -1 & 0 \\ 0 & 1 \end{array} \right )$ |
| Rescaling | $\left ( \begin{array}{cc} r & 0 \\ 0 & s \end{array} \right )$ | $\left ( \begin{array}{cc} r^{-1} & 0 \\ 0 & s^{-1} \end{array} \right )$ (if $r, s \ne 0$; |
|  | if $r = 0$ or $s = 0$ then $A$ is not invertible) |  |
| Rotation | $\left ( \begin{array}{cc} \cos r & -\sin r \\ \sin r & \cos r \end{array} \right )$ | $\left ( \begin{array}{cc} \cos (-r) & -\sin (-r) \\ \sin (-r) & \cos (-r) \end{array} \right ) = \left ( \begin{array}{cc} \cos r & \sin r \\ -\sin r & \cos r \end{array} \right )$ |
| Shearing | $\left ( \begin{array}{cc} 1 & r \\ 0 & 1 \end{array} \right )$ | $\left ( \begin{array}{cc} 1 & -r \\ 0 & 1 \end{array} \right )$ (for any $r \in {\bf R}$) |

</div>

</div>

<div class="lemma" markdown="1">


<p class="env-number"><strong>Lemma 4.68</strong></p>

<span id="lem-maps-lemma-003" label="lem:maps-lemma-003"></span> Let $A$ be an invertible matrix. Then there is *precisely* one inverse matrix, i.e., if $B$ and $C$ are two inverses (which means $AB=BA={\mathrm {id}}$ and $AC=CA={\mathrm {id}}$), then $B=C$. One therefore speaks of *the* inverse (as opposed to *an* inverse), and writes $A^{-1}$ for the inverse.

</div>

<div class="proof" markdown="1">

*Proof.* Using the associativity of matrix multiplication (marked !), we get the following chain of equalities
<div class="arithmatex" markdown="1">
\[
B = B {\mathrm {id}} = B (A C) \stackrel ! = (BA) C = {\mathrm {id}} C = C.
\]
</div>
Thus $B = C$ as claimed. ◻

</div>

## Linear systems associated to invertible matrices

Inverses of matrices are useful to solve linear systems. This is the content of the following theorem:

<div class="theorem" markdown="1">


<p class="env-number"><strong>Theorem 4.69</strong></p>

<span id="thm-invertible-system" label="thm:invertible-system"></span> Let $A$ be an *invertible* $n \times n$-matrix. We consider the linear system
<div class="arithmatex" markdown="1">
\[
A x = b,
\]
</div>
where $x = \left ( \begin{array}{c} x_1 \\ \vdots \\ x_n \end{array} \right )$ is a vector consisting of $n$ unknowns and $b = \left ( \begin{array}{c} b_1 \\ \vdots \\ b_n \end{array} \right )$ is a vector. This linear system has a *unique* solution, which is given by
<div class="arithmatex" markdown="1">
\[
x = A^{-1} b,
\]
</div>
i.e., the product of the *inverse* of $A$ with the vector $b$.

</div>

<div class="remark" markdown="1">


<p class="env-number"><strong>Remark 4.70</strong></p>

<span id="rem-maps-remark-007" label="rem:maps-remark-007"></span> By <a href="../maps-multiplication-of-a-matrix/#obs-matrix-vector-system" data-reference-type="ref+Label" data-reference="obs:matrix-vector-system">Observation 4.11</a>, if $A = (a_{ij})$, then the equation $Ax = b$ is a shorthand for the linear system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
a_{11} x_1 + \dots + a_{1n} x_n & = b_1 \\
\vdots \\
a_{m1} x_1 + \dots + a_{mn} x_n & = b_m. \\
\end{align*}
\]
</div>

</div>

<div class="proof" markdown="1">

*Proof.* We first check that $A^{-1}b$ is indeed a solution to the equation $Ax = b$:
<div class="arithmatex" markdown="1">
\[
A (A^{-1} b) \stackrel ! = (A A^{-1}) b = {\mathrm {id}}_n b = b.
\]
</div>
At the equation marked ! we have used the associativity of matrix multiplication (where the third matrix is $b$, which is just a column vector, i.e., an $n \times 1$-matrix).

We now check that $A^{-1} b$ is the *only* solution. Suppose then that some vector $y$ is a solution to the system, i.e., $A y = b$. We will show $y = A^{-1} b$ by proving
<div class="arithmatex" markdown="1">
\[
z := A^{-1} b - y = 0.
\]
</div>
Again using the properties of matrix multiplication (<a href="../maps-composing/#lem-matrix-multiplication-properties" data-reference-type="ref+Label" data-reference="lem:matrix-multiplication-properties">Lemma 4.60</a>), we have $A z = A (A^{-1} b - y) = A A^{-1} b - A y = b - b = 0$. Multiplying this with the matrix $A^{-1}$, we obtain our claim:
<div class="arithmatex" markdown="1">
\[
z = A^{-1} A z = A^{-1} 0 = 0.
\]
</div>
 ◻

</div>

## Structural properties of taking the inverse

Below, it is necessary to have a few properties of the operation “take the inverse of an (invertible) matrix” at our disposal. In the following theorem, all matrices are square matrices of the same size. In the right column, we illustrate what they mean for $1 \times 1$-matrices, as a means to remember them. Recall that a $1 \times 1$-matrix $(a)$ is invertible if and only if $a \ne 0$, and its inverse $(a)^{-1}$ is the matrix $(a^{-1})$. (Here, as usual, the *reciprocal* $a^{-1}$ of a non-zero real number $a$ is defined as $a^{-1} := \frac 1 a$.)

<div class="theorem" markdown="1">


<p class="env-number"><strong>Theorem 4.71</strong></p>

<span id="thm-inverses-properties" label="thm:inverses-properties"></span> The following holds:

| Statement for general (square) matrices | For $1 \times 1$-matrices |
|:---|:---|
| ${\mathrm {id}}$ is invertible: ${\mathrm {id}}^{-1} = {\mathrm {id}}$ | $\frac 1 1 = 1$ |
| If $A$ is invertible, then $A^{-1}$ is also invertible: 
<div class="arithmatex" markdown="1">
\[
(A^{-1})^{-1} = A.
\]
</div>

<p class="env-number equation-number"><strong>(4.72)</strong></p>

<span id="eqn-inverse-inverse" label="eqn--inverse.inverse"></span> | $\frac 1 {\frac 1 a} = a$ |
| If $A$ and $B$ are invertible, then $AB$ is invertible: 
<div class="arithmatex" markdown="1">
\[
(AB)^{-1} = B^{-1} A^{-1}.
\]
</div>

<p class="env-number equation-number"><strong>(4.73)</strong></p>

<span id="eqn-products-inverse" label="eqn--products.inverse"></span> | $\frac 1 {ab} = \frac 1 b \frac 1 a$. |
| If $A_1, \dots, A_k$ are invertible, then their product $A_1 A_2 \dots A_k$ is also invertible: 
<div class="arithmatex" markdown="1">
\[
(A_1 \dots A_k)^{-1} = A_k^{-1} \dots A_1^{-1}.
\]
</div>

<p class="env-number equation-number"><strong>(4.74)</strong></p>

<span id="eqn-several-products-inverse" label="eqn--several.products.inverse"></span> | $\frac 1 {a_1 \cdot \dots \cdot a_k} = \frac 1 {a_k} \cdot \dots \cdot \frac 1 {a_1}$ |

</div>

<div class="proof" markdown="1">

*Proof.* We prove to illustrate the technique. We compute
<div class="arithmatex" markdown="1">
\[
\begin{align*}
(AB)(B^{-1}A^{-1}) & = A(BB^{-1})A^{-1} & \text{by associativity} \\
& = AA^{-1} & \text{since }B^{-1}\text{ is inverse of }B \\
& = {\mathrm {id}} & \text{since }A^{-1}\text{ is inverse of }A.
\end{align*}
\]
</div>
Using the same arguments, one checks $(B^{-1}A^{-1})(AB) = {\mathrm {id}}$. Thus, by <a href="#def-invertible-matrix" data-reference-type="ref+Label" data-reference="def:invertible-matrix">Definition 4.64</a>, $B^{-1}A^{-1}$ is the inverse of $AB$. ◻

</div>

<div class="remark" markdown="1">


<p class="env-number"><strong>Remark 4.75</strong></p>

<span id="rem-maps-remark-008" label="rem:maps-remark-008"></span> Among the above formulas, is the most noteworthy one: note that the order of $A$ and $B$ has been changed! (Recall from <a href="../maps-composing/#war-not-commutative" data-reference-type="ref+Label" data-reference="war:not-commutative">Warning 4.55</a> that the order of multiplication is important. Only for $1 \times 1$-matrices, i.e., real numbers the order of multiplication is irrelevant, so that $\frac 1 {ab} = \frac 1 b \frac 1 a = \frac 1 a \frac 1 b$ etc.)

</div>

## Invertible matrices and elementary operations

<div class="lemma" markdown="1">


<p class="env-number"><strong>Lemma 4.76</strong></p>

<span id="lem-elementary-invertible" label="lem:elementary-invertible"></span> Any elementary matrix (<a href="../maps-composing/#def-elementary-matrices" data-reference-type="ref+Label" data-reference="def:elementary-matrices">Definition 4.62</a>) is invertible:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left (E^{(1)}_{i,j} \right)^{-1} & = E^{(1)}_{i,j} \\ 
\left (E^{(2)}_{i,r} \right)^{-1} & = E^{(2)}_{i, r^{-1}} \\
\left (E^{(3)}_{i,j,r} \right )^{-1} & = E^{(3)}_{i, j, -r}.
\end{align*}
\]
</div>

</div>

<div class="proof" markdown="1">

*Proof.* To illustrate this, we check this for the last one, where for simplicity of notation we just treat the case of $2 \times 2$-matrices. I.e., we prove
<div class="arithmatex" markdown="1">
\[
{\left ( \begin{array}{cc} 1 & r \\ 0 & 1 \end{array} \right )}^{-1} = \left ( \begin{array}{cc} 1 & -r \\ 0 & 1 \end{array} \right ).
\]
</div>
To do this, we compute the product
<div class="arithmatex" markdown="1">
\[
{\left ( \begin{array}{cc} 1 & r \\ 0 & 1 \end{array} \right )} \left ( \begin{array}{cc} 1 & -r \\ 0 & 1 \end{array} \right ) = \left ( \begin{array}{cc} {} & {} \\ 1 \cdot (-r) + r 1 & {} \end{array} \right ) = \left ( \begin{array}{cc} 1 & 0 \\ 0 & 1 \end{array} \right ).
\]
</div>
Similarly (or, actually, symmetrically)
<div class="arithmatex" markdown="1">
\[
{\left ( \begin{array}{cc} 1 & r \\ 0 & 1 \end{array} \right )} \left ( \begin{array}{cc} 1 & -r \\ 0 & 1 \end{array} \right ) = \left ( \begin{array}{cc} {} & {} \\ 1 \cdot (-r) + r 1 & {} \end{array} \right ) = \left ( \begin{array}{cc} 1 & 0 \\ 0 & 1 \end{array} \right ).
\]
</div>
 ◻

</div>

<div class="lemma" markdown="1">


<p class="env-number"><strong>Lemma 4.77</strong></p>

<span id="lem-row-product-invertible" label="lem:row-product-invertible"></span> If $A$ is an $m \times n$-matrix and $B$ is obtained from $A$ by means of elementary row operations:
<div class="arithmatex" markdown="1">
\[
A \leadsto B,
\]
</div>
then
<div class="arithmatex" markdown="1">
\[
B = U A
\]
</div>
for an invertible $m \times m$-matrix $U$. (In particular, if $A \leadsto {\mathrm {id}}$, then ${\mathrm {id}} = U A$.)

</div>

<div class="proof" markdown="1">

*Proof.* If $A \leadsto B$ in a single step, this is a combination of <a href="#lem-elementary-invertible" data-reference-type="ref+Label" data-reference="lem:elementary-invertible">Lemma 4.76</a> and <a href="../maps-composing/#prop-multiplication-elementary-matrices" data-reference-type="ref+Label" data-reference="prop:multiplication-elementary-matrices">Proposition 4.61</a>: in this case $U$ is the elementary, and in particular invertible, matrix corresponding to the elementary operation that has been performed.

In general, say $A =: A_0 \leadsto A_1 \leadsto A_2 \leadsto \dots \leadsto A_n = B$, then $A_1 = U_1 A$, $A_2 = U_2 A_1$ etc., so that
<div class="arithmatex" markdown="1">
\[
A_n = U_n A_{n-1} = U_n U_{n-1} A_{n-2} = \dots = \underbrace{U_n U_{n-1} \dots U_1}_{=: U} A,
\]
</div>
where we have used the associativity of matrix multiplication. Being the product of elementary, and in particular invertible matrices, $U$ is then also invertible (<a href="#thm-inverses-properties" data-reference-type="ref+Label" data-reference="thm:inverses-properties">Theorem 4.71</a>). ◻

</div>

We finally prove <a href="../systems-elementary-operations/#thm-elementary-equivalent" data-reference-type="ref+Label" data-reference="thm:elementary-equivalent">Theorem 2.18</a>. You can check that there is no vicious circle!

<div class="corollary" markdown="1">


<p class="env-number"><strong>Corollary 4.78</strong></p>

<span id="cor-equivalent-systems" label="cor:equivalent-systems"></span> Let
<div class="arithmatex" markdown="1">
\[
A x = b
\]
</div>

<p class="env-number equation-number"><strong>(4.79)</strong></p>

<span id="eqn-system-blah-1" label="eqn--system.blah.1"></span> be a linear system. Apply any sequence of elementary row operations to $A$ and to $b$, getting a matrix $A'$ and a vector $b'$. Then the system
<div class="arithmatex" markdown="1">
\[
A' x = b'
\]
</div>

<p class="env-number equation-number"><strong>(4.80)</strong></p>

<span id="eqn-system-blah-2" label="eqn--system.blah.2"></span> is equivalent to , i.e., the solution sets of the two systems are the same.

</div>

<div class="proof" markdown="1">

*Proof.* By <a href="#lem-row-product-invertible" data-reference-type="ref+Label" data-reference="lem:row-product-invertible">Lemma 4.77</a>, there is an invertible matrix $U$ such that $A' = UA$ and $b' = Ub$. If $Ax = b$, then also
<div class="arithmatex" markdown="1">
\[
A'x = (UA)x = U(Ax) = Ub = b'.
\]
</div>
Conversely, if $A'x = b'$, then (crucially using that $U$ is invertible)
<div class="arithmatex" markdown="1">
\[
Ax = U^{-1}UAx = U^{-1}A'x = U^{-1}b' = U^{-1} Ub=b.
\]
</div>
 ◻

</div>

## Invertibility criteria

We can now establish a criterion that determines whether a given matrix $A$ is invertible (and that computes the inverse in case it is). This can then be used in practice to apply <a href="#thm-invertible-system" data-reference-type="ref+Label" data-reference="thm:invertible-system">Theorem 4.69</a>.

Recall that three statements “X”, “Y”, “Z” are *equivalent* if any of them implies the others. For example the statements (where $r$ is a real number)

- $r + 1 \ge 1$

- $r \ge 0$

- $r - 4 \ge -4$

are equivalent. By contrast, the three statements

- $r + 1 \ge 1$

- $r \ge 0$

- $r^2 \ge 0$

are *not* equivalent, since the third does not imply, say, the second: for $r = -1$, the third statement holds, but the second does not. A convenient way to show that three statements are equivalent is to show “X” $\Rightarrow$ “Y”, then “Y” $\Rightarrow$ “Z”, and then “Z” $\Rightarrow$ “X”. Of course, this also works similarly for more than three statements.

<div class="theorem" markdown="1">


<p class="env-number"><strong>Theorem 4.81</strong> (Related exercises: <a href="../exercises-determinants/#ex-determinants-exercise-006">Exercise 5.8</a>, <a href="../exercises-eigenvalues/#ex-eigenvalues-5-1">Exercise 6.5</a>, <a href="../exercises-maps/#ex-maps-3-14">Exercise 4.35</a>, <a href="../exercises-maps/#ex-maps-3-16">Exercise 4.38</a>, <a href="../exercises-maps/#ex-maps-3-19">Exercise 4.43</a>, <a href="../exercises-maps/#ex-maps-example-031">Exercise 4.19</a>)</p>

<span id="thm-invertible-elimination" label="thm:invertible-elimination"></span> The following conditions on a square matrix $A \in {\mathrm {Mat}}_{n \times n}$ are equivalent:

1.  <span id="item-a-invertible" label="item--A invertible"></span> $A$ is invertible.

2.  <span id="item-any-b-exactly-one" label="item--any b exactly one"></span> For *any* $b \in {\bf R}^n$ (regarded as a column vector with $n$ rows), the equation $Ax = b$ (for $x \in {\bf R}^n$ being a column vector consisting of $n$ unknowns $x_1, \dots, x_n$) has *exactly one* solution.

3.  <span id="item-any-b-at-most-one" label="item--any b at most one"></span> For *any* $b \in {\bf R}^n$, the equation $Ax = b$ has *at most one* solution.

4.  <span id="item-only-trivial" label="item--only trivial"></span> The system $Ax = 0$ (0 being the zero row vector consisting of $n$ zeros) has only the trivial solution $x = 0$ (cf. <a href="../systems-linear-systems/#rem-trivial-solution" data-reference-type="ref+Label" data-reference="rem:trivial-solution">Remark 2.14</a>).

5.  <span id="item-ga-id" label="item--GA.id"></span> Using the Gaussian algorithm (<a href="../systems-gaussian-elimination/#met-gaussian-algorithm" data-reference-type="ref+Label" data-reference="met:gaussian-algorithm">Method 2.29</a>), $A$ can be transformed to the identity matrix ${\mathrm {id}}_n$.

6.  <span id="item-product-elementary-matrices" label="item--product elementary matrices"></span> $A$ is a product of (appropriate) elementary matrices.

7.  <span id="item-right-inverse" label="item--right inverse"></span> There is a matrix $B \in {\mathrm {Mat}}_{n \times n}$ such that $AB = {\mathrm {id}}$.

If these conditions are satisfied, the inverse of $A$ can be computed as follows: write the identity $n \times n$-matrix to the right of $A$ (this gives a $n \times (2n)$-matrix):
<div class="arithmatex" markdown="1">
\[
B := (A \ | \ {\mathrm {id}}_n  ) = \left ( \begin{array}{ccc|ccc} a_{11} & \dots & a_{1n} & 1 & \dots & 0 \\ \vdots & \ddots & \vdots & \vdots & \ddots & \vdots\\ a_{n1} & \dots & a_{nn} & 0 & \dots & 1 \end{array} \right ).
\]
</div>
(The bar in the middle is just there for visual purposes, it has no deeper meaning.) Apply Gaussian elimination in order to bring the matrix $B$ to reduced row echelon form, which according to the above gives a matrix of the form
<div class="arithmatex" markdown="1">
\[
({\mathrm {id}}_n \ | \ E).
\]
</div>
Then $E = A^{-1}$, i.e., $E$ is the inverse of $A$.

</div>

<div class="proof" markdown="1">

*Proof.* <a href="#item-a-invertible" data-reference-type="ref" data-reference="item--A invertible">1.</a> $\Rightarrow$ <a href="#item-any-b-exactly-one" data-reference-type="ref" data-reference="item--any b exactly one">2.</a>: This is just the content of <a href="#thm-invertible-system" data-reference-type="ref+Label" data-reference="thm:invertible-system">Theorem 4.69</a>.

The implications <a href="#item-any-b-exactly-one" data-reference-type="ref" data-reference="item--any b exactly one">2.</a> $\Rightarrow$ <a href="#item-any-b-at-most-one" data-reference-type="ref" data-reference="item--any b at most one">3.</a> and <a href="#item-any-b-at-most-one" data-reference-type="ref" data-reference="item--any b at most one">3.</a> $\Rightarrow$ <a href="#item-only-trivial" data-reference-type="ref" data-reference="item--only trivial">4.</a> are clear.

<a href="#item-only-trivial" data-reference-type="ref" data-reference="item--only trivial">4.</a> $\Rightarrow$ <a href="#item-ga-id" data-reference-type="ref" data-reference="item--GA.id">5.</a>: we can bring $A$ into reduced row-echelon form, say, $A \leadsto R$. We need to show that $R = {\mathrm {id}}$. If this is not the case, then $R$ contains a zero row (since $R$ is a *square* matrix). <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a> then tells us that the system $Rx = 0$ has (at least) one free parameter, and therefore the system has not only the zero vector as a solution. The original system $Ax = 0$, which by <a href="#cor-equivalent-systems" data-reference-type="ref+Label" data-reference="cor:equivalent-systems">Corollary 4.78</a> has the same solutions as $Rx = 0$, then also has a non-trivial solution. This is a contradiction to our assumption that $R$ is not the identity matrix.

<a href="#item-ga-id" data-reference-type="ref" data-reference="item--GA.id">5.</a> $\Rightarrow$ <a href="#item-product-elementary-matrices" data-reference-type="ref" data-reference="item--product elementary matrices">6.</a>: by <a href="#lem-row-product-invertible" data-reference-type="ref+Label" data-reference="lem:row-product-invertible">Lemma 4.77</a>, we have $UA={\mathrm {id}}$ for $U$ being a product of elementary matrices, say $U = U_1 \dots U_n$. Then, using , we have
<div class="arithmatex" markdown="1">
\[
A = U^{-1} U A = U^{-1} = U_n^{-1} \dots U_1^{-1},
\]
</div>
and this is also a product of elementary matrices.

<a href="#item-product-elementary-matrices" data-reference-type="ref" data-reference="item--product elementary matrices">6.</a> $\Rightarrow$ <a href="#item-right-inverse" data-reference-type="ref" data-reference="item--right inverse">7.</a>: if $A = U_1 \dots U_n$ for some elementary matrices, then
<div class="arithmatex" markdown="1">
\[
A U_n^{-1} \dots U_1^{-1} = U_1 \dots U_n U_n^{-1} \dots U_1^{-1} = {\mathrm {id}}.
\]
</div>

<a href="#item-right-inverse" data-reference-type="ref" data-reference="item--right inverse">7.</a> $\Rightarrow$ <a href="#item-a-invertible" data-reference-type="ref" data-reference="item--A invertible">1.</a>: suppose $B$ is such that $AB={\mathrm {id}}$. We observe that then the only vector $x \in {\bf R}^n$ such that $B x = 0$ is the zero vector:
<div class="arithmatex" markdown="1">
\[
x = {\mathrm {id}}_n x = AB x = A 0 = 0.
\]
</div>
Applying the implication <a href="#item-only-trivial" data-reference-type="ref" data-reference="item--only trivial">4.</a> $\Rightarrow$ <a href="#item-right-inverse" data-reference-type="ref" data-reference="item--right inverse">7.</a> (which was already proved) to $B$, we obtain a matrix $C$ such that $BC = {\mathrm {id}}$. Therefore
<div class="arithmatex" markdown="1">
\[
A = A {\mathrm {id}}_n = A (BC) = (AB)C = {\mathrm {id}} C = C.
\]
</div>
This means that $BA = {\mathrm {id}}$.

This finishes the proof that all the given statements are equivalent. The statement about the computation of $A^{-1}$ holds since the row operations that bring $A \leadsto {\mathrm {id}}$ also bring the augmented matrix $(A \ | \ {\mathrm {id}})$ to $(UA \ | \ U{\mathrm {id}}) = ({\mathrm {id}} \ | U)$. ◻

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 4.82</strong> (Related exercises: <a href="../exercises-determinants/#ex-determinants-exercise-006">Exercise 5.8</a>)</p>

<span id="ex-maps-example-025" label="ex:maps-example-025"></span> We apply this to $A = \left ( \begin{array}{ccc} 1 & 0 & -1 \\ 3 & 1 & -3 \\ 1 & 2 & -2 \end{array} \right )$:
<div class="arithmatex" markdown="1">
\[
B =
\left ( \begin{array}{ccc|ccc} 1 & 0 & -1 & 1 & 0 & 0 \\ 3 & 1 & -3 & 0 & 1 & 0 \\ 1 & 2 & 2 & 0 & 0 & 1 \end{array} \right ).
\]
</div>
We subtract the first row 3, resp. 2 times from the other ones, which gives
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc|ccc} 1 & 0 & -1 & 1 & 0 & 0 \\ 0 & 1 & 0 & -3 & 1 & 0 \\ 0 & 2 & -1 & -1 & 0 & 1 \end{array} \right ).
\]
</div>
We subtract 2 times the second row from the third:
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc|ccc} 1 & 0 & -1 & 1 & 0 & 0 \\ 0 & 1 & 0 & -3 & 1 & 0 \\ 0 & 0 & -1 & 5 & -2 & 1 \end{array} \right ).
\]
</div>
We bring the matrix into row echelon form by multiplying the last row with $-1$, which yields
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc|ccc} 1 & 0 & -1 & 1 & 0 & 0 \\ 0 & 1 & 0 & -3 & 1 & 0 \\ 0 & 0 & 1 & -5 & 2 & -1 \end{array} \right ).
\]
</div>
Finally, to bring it into reduced row-echelon form, we add the third row to the first, which gives
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc|ccc} 1 & 0 & 0 & -4 & 2 & -1 \\ 0 & 1 & 0 & -3 & 1 & 0 \\ 0 & 0 & 1 & -5 & 2 & -1 \end{array} \right ).
\]
</div>

Thus, according to <a href="#thm-invertible-elimination" data-reference-type="ref+Label" data-reference="thm:invertible-elimination">Theorem 4.81</a>, $A$ is indeed invertible, and its inverse is
<div class="arithmatex" markdown="1">
\[
A^{-1} = \left ( \begin{array}{ccc} -4 & 2 & -1 \\ -3 & 1 & 0 \\ -5 & 2 & -1 \end{array} \right ).
\]
</div>

</div>

<div class="corollary" markdown="1">


<p class="env-number"><strong>Corollary 4.83</strong></p>

<span id="cor-maps-corollary-003" label="cor:maps-corollary-003"></span> If $A$ is a square matrix such that for some other square matrix $B$ we have $AB = {\mathrm {id}}$, then we also have $BA = {\mathrm {id}}$.

</div>

<div class="proof" markdown="1">

*Proof.* We use the theorem to see that $A$ is invertible, and then
<div class="arithmatex" markdown="1">
\[
B = {\mathrm {id}} B = A^{-1}AB=A^{-1}
\]
</div>
And we have seen in above that $A^{-1} A = {\mathrm {id}}$. ◻

</div>
