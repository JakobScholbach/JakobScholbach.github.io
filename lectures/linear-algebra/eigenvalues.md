---
title: Eigenvalues and Eigenvectors
render_with_liquid: false
---

# Eigenvalues and Eigenvectors

Eigenvalues and eigenvectors are an extremely useful concept of linear algebra. Coupled with certain numerical considerations, which are (only slightly!) beyond the scope of this course, eigenvalues have been used, for example, in the early PageRank algorithm employed by Google.

The overall idea of eigenvalues and eigenvectors is this: square matrices of the form
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{ccc} a_{11} & {} & 0 \\ {} & \ddots & {} \\ 0 & {} & a_{nn} \end{array} \right )
\]
</div>
(i.e., the only non-zero entries are on the main diagonal; such matrices are called *diagonal matrices*) are particularly simple to comprehend and to use in computations. For example, products of the can be computed easily:
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc} a_{11} & {} & 0 \\ {} & \ddots & {} \\ 0 & {} & a_{nn} \end{array} \right ) \left ( \begin{array}{ccc} b_{11} & {} & 0 \\ {} & \ddots & {} \\ 0 & {} & b_{nn} \end{array} \right )
= \left ( \begin{array}{ccc} a_{11} b_{11} & {} & 0 \\ {} & \ddots & {} \\ 0 & {} & a_{nn} b_{nn} \end{array} \right ),
\]
</div>
i.e., the (diagonal) entries can just be multiplied one by one, something that clearly goes wrong for products of general matrices. Eigenvalues and eigenvectors can, in certain cases, be used to reduce computations for general matrices to those for diagonal matrices.

## Definitions

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 6.1</strong></p>

<span id="def-eigenthings" label="def:eigenthings"></span> Let $A$ be a *square* matrix. A real number $\lambda$ is called an *eigenvalue* of $A$ if there exists a *nonzero* vector $v \in {\bf R}^n$ that satisfies the equation
<div class="arithmatex" markdown="1">
\[
Av = \lambda v.
\]
</div>
Such a vector $v$ is called an *eigenvector* for the eigenvalue $\lambda$. In other words, multiplying the matrix $A$ by the vector $v$ results in a scaled version of $v$, where the scaling factor is the eigenvalue $\lambda$.

Likewise, for a linear map $f : V \to V$, $\lambda$ is an eigenvalue if there is $v \in V, v \ne 0$ such that
<div class="arithmatex" markdown="1">
\[
f(v) = \lambda v.
\]
</div>

<p class="env-number equation-number"><strong>(6.2)</strong></p>

<span id="eqn-eigenvalue-eq" label="eqn--eigenvalue eq"></span>

</div>

We consider some of the linear maps $f : {\bf R}^2 \to {\bf R}^2$ of §<a href="../maps/#sect-2-x-2-matrices" data-reference-type="ref" data-reference="sect--2 x 2 matrices">Subsection 4.2.1</a>.

<div class="example" markdown="1">


<p class="env-number"><strong>Example 6.3</strong></p>

<span id="ex-eigenvalues-example-001" label="ex:eigenvalues-example-001"></span> If $f$ is the reflection along, say, the $x$-axis, i.e., $f(x, y) = (x, -y)$, then reads
<div class="arithmatex" markdown="1">
\[
(x, -y) = (\lambda x, \lambda y),
\]
</div>
i.e., $x = \lambda x$ and $-y = \lambda y$. The first equation holds if $x = 0$ and $\lambda$ arbitrary or if $\lambda = 1$ and $x$ arbitrary. Similarly, the second forces $y = 0$ or $\lambda = -1$. Since, by definition, we have $(x, y) \ne (0, 0)$, we cannot have both $x = 0$ and $y = 0$. If $x \ne 0$, then $\lambda = 1$, which forces $y = 0$. If $x = 0$, then $y \ne 0$ and therefore $\lambda = -1$. Thus, there are two eigenvalues and eigenvectors are as follows:

- $\lambda = 1$, with eigenvectors $(x, 0)$ for arbitrary $x \in {\bf R}$,

- $\lambda = -1$, with eigenvectors $(0, y)$ for arbitrary $y \in {\bf R}$.

</div>

Before going on, we make the following observation, for any $n \times n$-matrix $A$. The equation
<div class="arithmatex" markdown="1">
\[
A v = \lambda v
\]
</div>
can be rewritten as
<div class="arithmatex" markdown="1">
\[
0 = Av-\lambda v = Av - (\lambda {\mathrm {id}}) v = (A - \lambda {\mathrm {id}}) v.
\]
</div>
Here we have used standard properties of matrix multiplication (<a href="../maps/#lem-matrix-multiplication-properties" data-reference-type="ref+Label" data-reference="lem:matrix-multiplication-properties">Lemma 4.59</a>). We seek a *non-zero* vector $v$ satisfying this condition. Such a vector exists if and only if $A - \lambda {\mathrm {id}}$ is *not* invertible.

<div class="example" markdown="1">


<p class="env-number"><strong>Example 6.4</strong></p>

<span id="ex-eigenvalues-example-002" label="ex:eigenvalues-example-002"></span> We consider the shearing matrix $A = \left ( \begin{array}{cc} 1 & r \\ 0 & 1 \end{array} \right )$, where we assume $r \ne 0$ (otherwise $A = {\mathrm {id}}$). We check the invertibility of the matrix:
<div class="arithmatex" markdown="1">
\[
A - \lambda {\mathrm {id}} = \left ( \begin{array}{cc} 1-\lambda & r \\ 0 & 1-\lambda \end{array} \right ).
\]
</div>
It suffices to compute the determinant (<a href="../determinants/#thm-det-zero-niff-invertible" data-reference-type="ref+Label" data-reference="thm:det-zero-niff-invertible">Theorem 5.15</a>):
<div class="arithmatex" markdown="1">
\[
\det \left ( \begin{array}{cc} 1-\lambda & r \\ 0 & 1-\lambda \end{array} \right ) = (1-\lambda)^2 - r \cdot 0 = (\lambda - 1)^2.
\]
</div>
This is zero precisely if $\lambda = 1$, i.e., $\lambda = 1$ is the only eigenvalue of $A$. Eigenvectors for this eigenvalue are those vectors such that
<div class="arithmatex" markdown="1">
\[
(A - 1 \dot {\mathrm {id}}) \left ( \begin{array}{c} x \\ y \end{array} \right ) = 0,
\]
</div>
i.e., $\left ( \begin{array}{c} ry \\ 0 \end{array} \right ) = \left ( \begin{array}{cc} 0 & r \\ 0 & 0 \end{array} \right ) \left ( \begin{array}{c} x \\ y \end{array} \right ) = 0$. Since we have assumed $r \ne 0$, this implies $y = 0$, and $x$ is arbitrary. Thus, the eigenvectors for $\lambda = 1$ are of the form $\left ( \begin{array}{c} x \\ 0 \end{array} \right )$ for $x \in {\bf R}$.

</div>

## The characteristic polynomial

<div class="definitionlemma" markdown="1">


<p class="env-number"><strong>Definition and Lemma 6.5</strong></p>

<span id="dlm-eigenvalues-definitionlemma-001" label="dlm:eigenvalues-definitionlemma-001"></span> For $A \in {\mathrm {Mat}}_{n \times n}$, the function
<div class="arithmatex" markdown="1">
\[
\chi(t) = \det (A - t \cdot {\mathrm {id}}_n)
\]
</div>
is a polynomial of degree $n$. It is called the *characteristic polynomial* of the matrix $A$. A real number $\lambda$ is an eigenvalue of $A$ if and only if
<div class="arithmatex" markdown="1">
\[
\chi(\lambda) = 0.
\]
</div>

</div>

For example, for $A = \left ( \begin{array}{cc} 1 & r \\ 0 & 1 \end{array} \right )$, $\chi(t) = (t-1)^2$.

<div class="example" markdown="1">


<p class="env-number"><strong>Example 6.6</strong></p>

<span id="ex-concrete-2-x-2-eigenvalues" label="ex:concrete-2-x-2-eigenvalues"></span> We compute the eigenvalues of $A = \begin{pmatrix} 2 & -1 \\ 4 & -3 \end{pmatrix}$ using the characteristic polynomial:
<div class="arithmatex" markdown="1">
\[
\chi_A(t) = \det \left ( \begin{array}{cc} 2-t & -1 \\ 4 & -3-t \end{array} \right ) = (2-t)(-3-t)+4=t^2+t-2.
\]
</div>
The equation $\chi_A(t) = 0$ solves as
<div class="arithmatex" markdown="1">
\[
t_{1/2} = -\frac 12 \pm \sqrt{2 + \frac 14} = -\frac 12 \pm \frac 32,
\]
</div>
i.e., the eigenvalues are $t_1 = -2$, $t_2 = 1$.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 6.7</strong></p>

<span id="ex-eigenvalues-example-004" label="ex:eigenvalues-example-004"></span> We consider the rotation matrix $A = \left ( \begin{array}{cc} \cos r & -\sin r \\ \sin r & \cos r \end{array} \right )$. We have:

- if $r = \dots, -4\pi, -2\pi, 0, 2\pi, \dots$ (i.e., a rotation by a multiple of 360$^\circ$, i.e., no rotation at all), then $A = {\mathrm {id}}_2$, and the only eigenvalue is $\lambda = 1$, and any vector $(x,y) \in {\bf R}^2$ is an eigenvector.

- if $r = \dots, -3\pi, -\pi, \pi, 3\pi, \dots$ (i.e., a rotation by 180$^\circ$ (plus an irrelevant multiple of 360$^\circ$)), the only eigenvalue is $\lambda = -1$, and again any vector in ${\bf R}^2$ is an eigenvector,

- in all other cases, i.e., if the rotation is not by $0^\circ$ or by $180^\circ$, there are *no* eigenvalues (and therefore no eigenvectors).

These statements are clear geometrically: for a rotation other than the special cases, for any vector $v \in {\bf R}^2$ we have that the rotated vector $Av$ lies on a different line, so that it cannot be an eigenvector. To confirm this algebraically, we compute its characteristic polynomial:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\chi(t) &= \det (A - t {\mathrm {id}}) \\
& = \det \left ( \begin{array}{cc} \cos r - t & -\sin r \\ \sin r & \cos r - t \end{array} \right ) \\
& = (\cos r-t)^2 + (\sin r)^2 \\
& = (\cos r)^2 -2t \cos r + t^2 + (\sin r)^2 \\
& = 1 + t^2 - 2t \cos r.
\end{align*}
\]
</div>
We solve this for $t$ using the usual formula:
<div class="arithmatex" markdown="1">
\[
t = 2 \cos r \pm \sqrt{- 1 + (\cos r)^2}.
\]
</div>
We have $0 \le \cos r \le 1$, and $\cos r = 1$ if and only if $r$ is a multiple of $\pi$ (cf. §<a href="../appendix/#sect-trigonometric-functions" data-reference-type="ref" data-reference="sect--trigonometric functions">Chapter B</a>). Thus the term inside the square root is zero in this case, in all other cases it is strictly negative, so that the equation $\chi(t) = 0$ has *no* solution.

</div>

The non-existence of eigenvalues can be salvaged by working with complex numbers, instead of real numbers.

<div class="theorem" markdown="1">


<p class="env-number"><strong>Theorem 6.8</strong></p>

(*Fundamental theorem of algebra*, cf. also §<a href="../c/#sect-the-fundamental-theorem-of-algebra" data-reference-type="ref" data-reference="sect--the_fundamental_theorem_of_algebra">Section 1.2</a> for further discussion) <span id="thm-eigenvalues-theorem-001" label="thm:eigenvalues-theorem-001"></span> For every non-constant polynomial
<div class="arithmatex" markdown="1">
\[
p(t) = a_n x^n + \dots + a_0,
\]
</div>
where the coefficients $a_0, \dots, a_n$ are complex numbers (for example, they can be real numbers), there exists a *complex* number $z \in {{\bf C}}$ such that
<div class="arithmatex" markdown="1">
\[
p(z) = 0.
\]
</div>

</div>

This theorem is famous for the number of entirely different proofs. A completely elementary proof fitting on about two pages is given in .

<div class="example" markdown="1">


<p class="env-number"><strong>Example 6.9</strong></p>

<span id="ex-eigenvalues-example-005" label="ex:eigenvalues-example-005"></span> Consider the rotation matrix
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{cc} 0 & -1 \\ 1 & 0 \end{array} \right )
\]
</div>
describing a (counter-clockwise) rotation by $90^\circ$. Its characteristic polynomial
<div class="arithmatex" markdown="1">
\[
\chi_A(t) = 1 + t^2
\]
</div>
does not have a real zero, i.e., for all real numbers $r$, $\chi_A(r) \ne 0$. However, the complex number $i$, the *imaginary unit*, which satisfies $i^2 = -1$ is a *complex* zero. In addition, $-i$, which also satisfies $(-i)^2 = -1$ is another complex zero.

</div>

It is therefore helpful to consider the concepts of linear algebra not only for real matrices, but for complex matrices. All of the concepts and theorems that we have encountered in this course continue to hold for complex matrices, complex vector spaces etc.

<div class="corollary" markdown="1">


<p class="env-number"><strong>Corollary 6.10</strong></p>

<span id="cor-cx-matrix-eigenvalues" label="cor:cx-matrix-eigenvalues"></span> Any complex square matrix $A \in {\mathrm {Mat}}_{n \times n}$ has at least one (complex) eigenvalue. In particular, any real square matrix has at least one complex eigenvalue (but it may not have a real eigenvalue).

</div>

## Eigenspaces

In the above examples, the set of all eigenvectors for a given eigenvalue has a particularly nice shape. This is a general phenomenon:

<div class="definitionlemma" markdown="1">


<p class="env-number"><strong>Definition and Lemma 6.11</strong></p>

<span id="dlm-eigenspace" label="dlm:eigenspace"></span> Let $A \in {\mathrm {Mat}}_{n \times n}$ be a square matrix and $\lambda \in {\bf R}$ a fixed real number. The set
<div class="arithmatex" markdown="1">
\[
E_\lambda := \{ v \in {\bf R}^n \ | \ A v = \lambda v \}
\]
</div>
is a subspace of ${\bf R}^n$. It is called the *eigenspace* of $A$ with respect to $\lambda$.

</div>

<div class="proof" markdown="1">

*Proof.* The equation $Av = \lambda v$ is equivalent to $(A - \lambda {\mathrm {id}})v = 0$, i.e., we have $E_\lambda = \ker (A - \lambda {\mathrm {id}})$. This is a subspace of ${\bf R}^n$ by <a href="../maps/#prop-ker-im-subspace" data-reference-type="ref+Label" data-reference="prop:ker-im-subspace">Proposition 4.23</a>. ◻

</div>

<div class="remark" markdown="1">


<p class="env-number"><strong>Remark 6.12</strong></p>

<span id="rem-eigenvalues-remark-001" label="rem:eigenvalues-remark-001"></span> If $\lambda$ above is *not* an eigenvalue, then $E_\lambda = \{ 0 \}$, i.e., the zero vector is the only one satisfying $Av = \lambda v$.

If $\lambda$ is an eigenvalue, then $E_\lambda$ consists of all the eigenvectors for the eigenvalue $\lambda$, together with the zero vector (which by definition is not an eigenvector).

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 6.13</strong></p>

<span id="ex-diagonalizable-2-x-2" label="ex:diagonalizable-2-x-2"></span> We compute the eigenspaces of the matrix $A = \left ( \begin{array}{cc} 0 & -1 \\ -2 & 0 \end{array} \right )$. Its characteristic polynomial is
<div class="arithmatex" markdown="1">
\[
\chi_A(t)=\det \left ( \begin{array}{cc} -\lambda & -1 \\ -2 & -\lambda \end{array} \right ) = \lambda^2 - 2.
\]
</div>
Its zeros, i.e., the eigenvalues of $A$ are $\lambda_{1/2} = \pm \sqrt 2$. The eigenspace for $\sqrt 2$ is the solution space of the homogeneous system
<div class="arithmatex" markdown="1">
\[
\underbrace{\left ( \begin{array}{cc} -\sqrt 2 & -1 \\ -2 & -\sqrt 2 \end{array} \right )}_{= A - \sqrt 2 \cdot {\mathrm {id}} =: B} \left ( \begin{array}{c} x \\ y \end{array} \right ) = 0.
\]
</div>
We solve this by reducing the matrix $B$ to row-echelon form
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cc} -\sqrt 2 & -1 \\ -2 & -\sqrt 2 \end{array} \right ) \leadsto \left ( \begin{array}{cc} 1 & \frac 1{\sqrt 2} \\ -2 & -\sqrt 2 \end{array} \right ) 
\leadsto \left ( \begin{array}{cc} 1 & \frac {\sqrt 2}2 \\ 0 & 0 \end{array} \right ).
\]
</div>
Thus, $y$ is a free variable and $x = - \frac{\sqrt 2}2 y$. Thus $E_{\sqrt 2}$ has dimension 1, a basis vector is $(-\frac{\sqrt 2}2, 1)$. Similarly, one computes the eigenspace for $\lambda = -\sqrt 2$:
<div class="arithmatex" markdown="1">
\[
B = A + \sqrt 2 \cdot {\mathrm {id}} = \left ( \begin{array}{cc} \sqrt 2 & -1 \\ -2 & \sqrt 2 \end{array} \right ) \leadsto 
\left ( \begin{array}{cc} 1 & -\frac{1}{\sqrt 2} \\ -2 & \sqrt 2 \end{array} \right ) \leadsto
\left ( \begin{array}{cc} 1 & -\frac{\sqrt 2}{2} \\ 0 & 0 \end{array} \right ),
\]
</div>
so the eigenspace $E_{-\sqrt 2}$ is again one-dimensional, and a basis vector is $(\frac{\sqrt 2}2, 1)$. Here is a plot showing the two eigenspaces: the map $v \mapsto Av$ will stretch the vectors in $E_{\sqrt 2}$ by a factor of $\sqrt 2$, while those on the eigenspace $E_{-\sqrt 2}$ will be flipped and stretched by a factor of $\sqrt 2$:

<div class="center" markdown="1">

![image](figures/png/eigenvalues/eigenvalues-fig-01.png)

</div>

</div>

## Diagonalizing matrices

As was mentioned above, diagonal matrices are particularly easy to compute with. This raises the question if (and how) it is possible to “bring” a given matrix $A$ into such an easy form.

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 6.14</strong></p>

<span id="def-diagonalizable" label="def:diagonalizable"></span> A square matrix $A$ is called *diagonalizable* if there is an invertible matrix $P \in {\mathrm {Mat}}_{n \times n}$ such that
<div class="arithmatex" markdown="1">
\[
PAP^{-1} = D,
\]
</div>
where $D=\left ( \begin{array}{ccc} d_{11} & {} & 0 \\ {} & \ddots & {} \\ 0 & {} & d_{nn} \end{array} \right )$ is a diagonal matrix.

</div>

An example showing the relevance of this notion is this: in the context of differential equations, one needs to compute the *exponential* of a square matrix $A$, which is defined as
<div class="arithmatex" markdown="1">
\[
\exp A = 1 + A + \frac {A^2} 2 + \frac {A^3} 6 + \frac{A^4} {24} + \dots.
\]
</div>
Here $A^3 = A \cdot A \cdot A$ etc. Instead of computing all these powers of $A$ one after another, one can use the above definition: if $A$ is diagonalizable, i.e., $PAP^{-1} = D$, then $A = (P^{-1}P)A(P^{-1}P) = P^{-1}(PAP^{-1})P = P^{-1}DP$. Then,
<div class="arithmatex" markdown="1">
\[
A^2 = P^{-1}DP \cdot P^{-1}D P = P^{-1}D^2 P, A^3 = P^{-1}D^3 P
\]
</div>
etc. Computing the powers of $D$, as opposed to those of $A$ is easy: one just needs to raise the diagonal entries to the corresponding power.

<div class="method" markdown="1">


<p class="env-number"><strong>Method 6.15</strong></p>

<span id="met-diagonalizability" label="met:diagonalizability"></span> In order to diagonalize a square matrix $A \in {\mathrm {Mat}}_{n \times n}$, i.e., to determine whether $P$ above exists, and to compute $D$, one proceeds as follows:

- Compute the eigenvalues of $A$, for example by finding the zeros of the characteristic polynomial. Denote them by $\lambda_1, \dots, \lambda_k$. Denote the eigenspaces by $E_{\lambda_k}$.

- The matrix $A$ is diagonalizable precisely if
<div class="arithmatex" markdown="1">
\[
  \sum_{i=1}^k \dim E_{\lambda_i} = n,
\]
</div>
  i.e., if the dimensions of the eigenspaces sum up to the size of the matrix $A$.

- In this event, one may choose $P$ to be the $n \times n$-matrix whose columns are the basis vectors of all the eigenspaces (for the various eigenvalues $\lambda_1, \dots, \lambda_k$). The matrix $D$ is the diagonal matrix whose diagonal entries are
<div class="arithmatex" markdown="1">
\[
  \underbrace{\lambda_1, \dots, \lambda_1}_{\dim E_1 \text{ times }}, \dots, \underbrace{\lambda_k, \dots, \lambda_k}_{\dim E_k \text{ times }}.
\]
</div>

</div>

One can show that above, one always has $k \le n$. One does this by proving that the sum of the subspaces $E_{\lambda_1}, \dots, E_{\lambda_k}$ is a *direct sum*, so that
<div class="arithmatex" markdown="1">
\[
\begin{align*}
n = \dim {\bf R}^n \ge & \dim (E_{\lambda_1} + \dots + E_{\lambda_k}) \\
& = \dim (E_{\lambda_1} \oplus \dots \oplus E_{\lambda_k}) \\
& = \dim (E_{\lambda_1}) + \dots + \dim (E_{\lambda_k}) \\
& \ge \underbrace{1 + \dots + 1}_{k \text{ summands}} \\
& = k.
\end{align*}
\]
</div>
This implies the following:

<div class="corollary" markdown="1">


<p class="env-number"><strong>Corollary 6.16</strong></p>

<span id="cor-diag-max" label="cor:diag-max"></span> If an $n \times n$-matrix has $n$ distinct eigenvalues, then it is diagonalizable.

</div>

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 6.17</strong></p>

<span id="def-eigenbasis" label="def:eigenbasis"></span> Let $A \in {\mathrm {Mat}}_{n \times n}$ be given. A basis $v_1, \dots, v_n$ of ${\bf R}^n$ is called an *eigenbasis* for $A$ if each $v_i$ is an eigenvector (for a certain eigenvalue) of $A$.

</div>

<div class="lemma" markdown="1">


<p class="env-number"><strong>Lemma 6.18</strong></p>

<span id="lem-eigenvalues-lemma-001" label="lem:eigenvalues-lemma-001"></span> For $A \in {\mathrm {Mat}}_{n \times n}$ the following two statements are equivalent:

1.  $A$ is diagonalizable.

2.  $A$ admits an eigenbasis, i.e., there is an eigenbasis (of ${\bf R}^n$) for $A$.

</div>

One proves this by observing that if $PAP^{-1}$ is a diagonal matrix, then $P$ is a base-change matrix between the standard basis and an eigenbasis.

<div class="example" markdown="1">


<p class="env-number"><strong>Example 6.19</strong></p>

<span id="ex-eigenvalues-example-007" label="ex:eigenvalues-example-007"></span> The matrix $A = \left ( \begin{array}{cc} 0 & -1 \\ -2 & 0 \end{array} \right )$ in <a href="#ex-diagonalizable-2-x-2" data-reference-type="ref+Label" data-reference="ex:diagonalizable-2-x-2">Example 6.13</a> has two distinct eigenvalues, and is therefore diagonalizable (<a href="#cor-diag-max" data-reference-type="ref+Label" data-reference="cor:diag-max">Corollary 6.16</a>). An eigenbasis for $A$ is
<div class="arithmatex" markdown="1">
\[
v_1 = (\sqrt 2, 1), v_2 = (-\sqrt 2, 1).
\]
</div>

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 6.20</strong></p>

<span id="ex-eigenvalues-example-008" label="ex:eigenvalues-example-008"></span> We consider the *shearing matrix*
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{cc} 1 & 1 \\ 0 & 1 \end{array} \right ).
\]
</div>
Its characteristic polynomial is $\chi_A(t) = (1-t)^2$, whose only zero is $t = 1$. Thus, $A$ has this eigenvalue only: $\lambda = 1$. We compute the eigenspace: consider the matrix $B := A - \lambda {\mathrm {id}} = \left ( \begin{array}{cc} 0 & 1 \\ 0 & 0 \end{array} \right )$. Writing, as usual, $v = \left ( \begin{array}{c} x \\ y \end{array} \right ) \in {\bf R}^2$, the space of solutions of the homogeneous system
<div class="arithmatex" markdown="1">
\[
B v = \left ( \begin{array}{c} y \\ 0 \end{array} \right ) = 0
\]
</div>
is our eigenspace, namely
<div class="arithmatex" markdown="1">
\[
E_1 = \{v \in {\bf R}^2 \ | B v = 0 \} = \{ (x, 0) \ | \ x \in {\bf R} \}.
\]
</div>
This space is 1-dimensional, and has a basis consisting of the (single) vector $(1,0)$. Thus, $A$ is *not* diagonalizable.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 6.21</strong></p>

<span id="ex-rotation-matrix-eigenvalues" label="ex:rotation-matrix-eigenvalues"></span> We continue the discussion of the rotation matrix $A = \left ( \begin{array}{cc} 0 & -1 \\ 1 & 0 \end{array} \right )$. Its (complex) eigenvalues are $\lambda_1 = i$, $\lambda_2 = -i$. According to <a href="#cor-diag-max" data-reference-type="ref+Label" data-reference="cor:diag-max">Corollary 6.16</a>, $A$ is diagonalizable. We compute the eigenspaces, where we regard $A$ as a complex matrix:
<div class="arithmatex" markdown="1">
\[
E_i = \{ v \in {{\bf C}}^2 \ | \ (A - i \cdot {\mathrm {id}}) v = 0 \}.
\]
</div>
If $v = \left ( \begin{array}{c} z_1 \\ z_2 \end{array} \right )$, then
<div class="arithmatex" markdown="1">
\[
(A - i \cdot {\mathrm {id}}) v = \left ( \begin{array}{cc} -i & -1 \\ 1 & -i \end{array} \right ) \left ( \begin{array}{c} z_1 \\ z_2 \end{array} \right ) = \left ( \begin{array}{c} -iz_1-z_2 \\ z_1-iz_2 \end{array} \right ) \stackrel ! = \left ( \begin{array}{c} 0 \\ 0 \end{array} \right ).
\]
</div>
This means $z_1 = i z_2$ from the second equation; the first is then also satisfied since $-iz_1 - z_2 = -i(iz_2) - z_2=z_2-z_2 = 0$. Thus
<div class="arithmatex" markdown="1">
\[
E_i = \{ (iz, z) \ | \ z \in {{\bf C}} \},
\]
</div>
i.e., as a complex vector space, $E_i$ is 1-dimensional and a basis of it is the vector $(i,1)$.

Similarly,
<div class="arithmatex" markdown="1">
\[
E_{-i} = \{ v\in {{\bf C}}^2 \ | \ (A + i \cdot {\mathrm {id}})v = 0\}.
\]
</div>
Computing this leads to the linear system
<div class="arithmatex" markdown="1">
\[
(A + i \cdot {\mathrm {id}}) v = \left ( \begin{array}{cc} +i & -1 \\ 1 & +i \end{array} \right ) \left ( \begin{array}{c} z_1 \\ z_2 \end{array} \right ) = \left ( \begin{array}{c} iz_1-z_2 \\ z_1+iz_2 \end{array} \right ) \stackrel ! = \left ( \begin{array}{c} 0 \\ 0 \end{array} \right ).
\]
</div>
This gives $z_1 = -iz_2$, so that $E_{-i} = \{(-iz, z) \ | \ z \in {{\bf C}}\}$, and a basis of it is the (single) vector $(-i, 1)$. Thus, the matrix $P$ above is
<div class="arithmatex" markdown="1">
\[
P = \left ( \begin{array}{cc} i & -i \\ 1 & 1 \end{array} \right ).
\]
</div>

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 6.22</strong></p>

<span id="ex-eigenvalues-example-010" label="ex:eigenvalues-example-010"></span> For $A = \left ( \begin{array}{cc} 1 & 0 \\ 0 & 0 \end{array} \right )$, $\lambda = 0$ is an eigenvalue (and $\left ( \begin{array}{c} 0 \\ 1 \end{array} \right )$ an 0-eigenvector) and $\lambda = 1$ is another eigenvalue (and $\left ( \begin{array}{c} 1 \\ 0 \end{array} \right )$ an 1-eigenvector).

</div>

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 6.23</strong></p>

<span id="def-similar" label="def:similar"></span> We say that two square matrices $A, B \in {\mathrm {Mat}}_{n \times n}$ are *similar* if there is an invertible matrix $P$ such that $PAP^{-1} = B$.

</div>

The question whether a given matrix $A$ is diagonalizable is a special case of the following more general question: given two square matrices $A, B$, are they similar in the sense of the above definition?

<div class="proposition" markdown="1">


<p class="env-number"><strong>Proposition 6.24</strong></p>

<span id="prop-similarity-necessary-conditions" label="prop:similarity-necessary-conditions"></span> If $A$ and $B$ are similar, then the following holds:

1.  $\det A = \det B$,

2.  $\mathrm{tr} A = \mathrm{tr} B$ (the traces, see <a href="../maps/#trace" data-reference-type="ref+Label" data-reference="trace">Exercise 4.24</a>),

3.  $\chi_A(t) = \chi_B(t)$,

4.  $A$ and $B$ have the same eigenvalues. The eigenspaces are related like so: if $B=PAP^{-1}$, then
<div class="arithmatex" markdown="1">
\[
    E_\lambda(B)=P(E_\lambda(A))\quad\text{for every }\lambda.
\]
</div>

</div>

<div class="proof" markdown="1">

*Proof.* Let $B=PAP^{-1}$ with $P$ invertible. For the determinant, using multiplicativity of the determinant (<a href="../determinants/#prop-product-formula" data-reference-type="ref+Label" data-reference="prop:product-formula">Proposition 5.18</a>):
<div class="arithmatex" markdown="1">
\[
\det B=\det(PAP^{-1})=\det P\,\det A\,\det(P^{-1})=\det A.
\]
</div>
For the trace, we use the statement proved in <a href="../maps/#trace" data-reference-type="ref+Label" data-reference="trace">Exercise 4.24</a> (marked \* below):
<div class="arithmatex" markdown="1">
\[
\mathrm{tr}(B)=\mathrm{tr}(P(AP^{-1})) \stackrel *=\mathrm{tr}((AP^{-1})P)=\mathrm{tr}(A).
\]
</div>
For the characteristic polynomial the argument is similar as for the determinant:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\chi_B(t)
&=\det(B-t\,\mathrm{id})
=\det(PAP^{-1}-t\,\mathrm{id}) \\
&=\det\bigl(P(A-t\,\mathrm{id})P^{-1}\bigr)
=\det P\,\det(A-t\,\mathrm{id})\,\det(P^{-1}) \\
&=\det(A-t\,\mathrm{id})
=\chi_A(t).
\end{align*}
\]
</div>
Hence $A$ and $B$ have the same characteristic polynomial, and therefore the same eigenvalues.

Finally, let $\lambda\in{\bf R}$. If $v\in E_\lambda(A)$, then $Av=\lambda v$, so
<div class="arithmatex" markdown="1">
\[
B(Pv)=PAP^{-1}(Pv)=PAv=\lambda Pv,
\]
</div>
hence $Pv\in E_\lambda(B)$. Thus $P(E_\lambda(A))\subseteq E_\lambda(B)$. Conversely, if $w\in E_\lambda(B)$, then $Bw=\lambda w$, and multiplying by $P^{-1}$ gives
<div class="arithmatex" markdown="1">
\[
A(P^{-1}w)=\lambda (P^{-1}w),
\]
</div>
so $P^{-1}w\in E_\lambda(A)$, i.e. $w\in P(E_\lambda(A))$. Therefore $E_\lambda(B)=P(E_\lambda(A))$. ◻

</div>

<div class="remark" markdown="1">

Conversely, it is not true that if the above conditions hold, then $A$ and $B$ are similar: The matrices
<div class="arithmatex" markdown="1">
\[
A=
\begin{pmatrix}
0&1&0&0\\
0&0&1&0\\
0&0&0&0\\
0&0&0&0
\end{pmatrix},
\qquad
B=
\begin{pmatrix}
0&1&0&0\\
0&0&0&0\\
0&0&0&1\\
0&0&0&0
\end{pmatrix}
\]
</div>
both have 0 as their only eigenvalue. The eigenspaces $E_0(A)$ and $E_0(B)$ are both 2-dimensional, but $A$ and $B$ are not similar, as one can see by observing that $A^2 \ne 0$ while $B^2 = 0$. And if $B = PAP^{-1}$, then $B^2 = PAP^{-1}PAP^{-1} = PA^2P^{-1}$ and likewise $B^3 = PA^3P^{-1}$, giving a contradiction. A sufficient condition for similarity can be expressed in terms of the so-called *Jordan normal form*, which we will not discuss in this course.

</div>

## Exercises

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.1</strong></p>

<span id="ex-eigenvalues-exercise-001" label="ex:eigenvalues-exercise-001"></span> (See <a href="#sol-ex-eigenvalues-exercise-001" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-exercise-001">Solution 6.6.1</a>.) Is the following matrix diagonalizable?
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{ccc} 2 & 1 & 1 \\ 0 & 1 & 0 \\ 1 & -1 & 2 \end{array} \right ).
\]
</div>

Hint: you will find that the eigenvalues of $A$ are among the numbers $0, 1, 2, 3$. You will be able to choose basis vectors of the eigenspaces all of whose coordinates are $-1, 0, 1$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.2</strong></p>

<span id="exercise-eigenvalues-2x2" label="exercise.eigenvalues.2x2"></span> (See <a href="#sol-exercise-eigenvalues-2x2" data-reference-type="ref+Label" data-reference="sol--exercise.eigenvalues.2x2">Solution 6.6.2</a>.) Let $A = \left ( \begin{array}{cc} a & b \\ c & d \end{array} \right )$. Show that:

- $\chi_A(t) = t^2 - {{\mathrm {tr}}} (A) t + \det A = t^2 - (a+d) t + (ad-bc)$. Here ${{\mathrm {tr}}} (A)$ is the *trace* of $A$, cf. <a href="../maps/#trace" data-reference-type="ref+Label" data-reference="trace">Exercise 4.24</a>.

- The eigenvalues of $A$ are
<div class="arithmatex" markdown="1">
\[
  \lambda_{1/2} = \frac{a+d}2 \pm \sqrt{\frac{(a-b)^2}4+4bc}.
\]
</div>

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.3</strong></p>

<span id="ex-eigenvalues-exercise-002" label="ex:eigenvalues-exercise-002"></span> (See <a href="#sol-ex-eigenvalues-exercise-002" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-exercise-002">Solution 6.6.3</a>.) For each of the following matrices, compute $\chi_A(t)$, the eigenvalues of $A$, the eigenspaces for these eigenvalues. Also decide whether $A$ is diagonalizable and compute an eigenbasis if one exists.

1.  $A = \left ( \begin{array}{cc} 3 & 5 \\ 1 & -1 \end{array} \right )$

2.  $A = \left ( \begin{array}{ccc} 0 & 1 & 0 \\ 3 & 0 & 1 \\ 2 & 0 & 0 \end{array} \right )$

3.  $A = \left ( \begin{array}{ccc} 1 & 0 & 0 \\ 0 & 0 & \frac 32 \\ 0 & 0 & 1 \end{array} \right )$

4.  $A = \left ( \begin{array}{ccc} 0 & 1 & 0 \\ 0 & 0 & 1 \\ 0 & 0 & 0 \end{array} \right )$

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.4</strong></p>

<span id="ex-eigenvalues-exercise-003" label="ex:eigenvalues-exercise-003"></span> (See <a href="#sol-ex-eigenvalues-exercise-003" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-exercise-003">Solution 6.6.4</a>.) Consider the matrix $A = \left ( \begin{array}{ccc} 1 & 0 & 0 \\ 1 & 1 & 2 \\ 1 & 0 & 1 \end{array} \right )$. Compute its characteristic polynomial, its eigenvalues and its eigenspaces. Is $A$ diagonalizable? If so, find a basis of ${\bf R}^3$ such that the associated matrix is a diagonal matrix, as in <a href="#def-diagonalizable" data-reference-type="ref+Label" data-reference="def:diagonalizable">Definition 6.14</a>.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.5</strong></p>

<span id="ex-eigenvalues-5-1" label="ex:eigenvalues-5-1"></span> (See <a href="#sol-ex-eigenvalues-5-1" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-5-1">Solution 6.6.5</a>.) Let
<div class="arithmatex" markdown="1">
\[
f: {\bf R}^3 \to {\bf R}^3
\]
</div>
be the linear map such that $f(1,0,1)=(2,0,2)$, $\ker f = L((1,1,1))$ and $f(2,0,-3)=(-2,0,3)$. Compute the matrix of $f$ with respect to the standard basis.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.6</strong></p>

<span id="ex-eigenvalues-exercise-004" label="ex:eigenvalues-exercise-004"></span> (See <a href="#sol-ex-eigenvalues-exercise-004" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-exercise-004">Solution 6.6.6</a>.) For which $a \in {\bf R}$ is the matrix
<div class="arithmatex" markdown="1">
\[
A_a = \left ( \begin{array}{ccc} a & 0 & 0 \\ a-2 & 1 & 1 \\ 0 & 1 & 1 \end{array} \right )
\]
</div>
diagonalizable?

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.7</strong></p>

<span id="ex-eigenvalues-5-2" label="ex:eigenvalues-5-2"></span> (See <a href="#sol-ex-eigenvalues-5-2" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-5-2">Solution 6.6.7</a>.) For a parameter $a \in {\bf R}$, let
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

<span id="ex-eigenvalues-exercise-005" label="ex:eigenvalues-exercise-005"></span> (See <a href="#sol-ex-eigenvalues-exercise-005" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-exercise-005">Solution 6.6.8</a>.) Consider the matrices
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

<span id="ex-eigenvalues-exercise-006" label="ex:eigenvalues-exercise-006"></span> (See <a href="#sol-ex-eigenvalues-exercise-006" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-exercise-006">Solution 6.6.9</a>.) For a parameter $t \in {\bf R}$, consider the matrix
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

<span id="ex-eigenvalues-exercise-007" label="ex:eigenvalues-exercise-007"></span> (See <a href="#sol-ex-eigenvalues-exercise-007" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-exercise-007">Solution 6.6.10</a>.) Consider the space ${\mathrm {Mat}}_{2 \times 2}$ of $2 \times 2$-vector spaces. Consider $A = \left ( \begin{array}{cc} -4 & 8 \\ 1 & -2 \end{array} \right )$ and the map
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

<span id="rem-eigenvalues-remark-002" label="rem:eigenvalues-remark-002"></span> The linearity of $F$ is a consequence of <a href="../maps/#lem-matrix-multiplication-properties" data-reference-type="ref+Label" data-reference="lem:matrix-multiplication-properties">Lemma 4.59</a>. It is also very similar to <a href="../maps/#prop-matrix-linear-map" data-reference-type="ref+Label" data-reference="prop:matrix-linear-map">Proposition 4.19</a>.

</div>

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.11</strong></p>

<span id="ex-eigenvalues-5-4-3" label="ex:eigenvalues-5-4-3"></span> (See <a href="#sol-ex-eigenvalues-5-4-3" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-5-4-3">Solution 6.6.11</a>.) Consider the two matrices
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{ccc} 1 & 0 & 2 \\ 0 & 3 & 0 \\ 0 & 0 & 3 \end{array} \right ) \text{ and } B = \left ( \begin{array}{ccc} 1 & 0 & 0 \\ 0 & 3 & 2 \\ 0 & 0 & 3 \end{array} \right ).
\]
</div>
Do they represent the same linear map $f : {\bf R}^3 \to {\bf R}^3$ (with respect to different bases)?

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.12</strong></p>

<span id="ex-eigenvalues-5-4-4" label="ex:eigenvalues-5-4-4"></span> (See <a href="#sol-ex-eigenvalues-5-4-4" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-5-4-4">Solution 6.6.12</a>.) Let $A = \left ( \begin{array}{ccc} 1 & 1 & 1 \\ 0 & 2 & 1 \\ 0 & 0 & 2 \end{array} \right )$. Determine the eigenvalues of $A$ and the corresponding eigenspaces. Is $A$ diagonalizable? Is $A^2$ *similar* to $A$? I.e., does $A^2$ represent the same linear map ${\bf R}^3 \to {\bf R}^3$ as $A$?

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.13</strong></p>

<span id="ex-eigenvalues-5-5" label="ex:eigenvalues-5-5"></span> (See <a href="#sol-ex-eigenvalues-5-5" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-5-5">Solution 6.6.13</a>.) Consider the vectors $v_1 = (1,0,1)$, $v_2 = (1,1,1)$ and $v_3=(1,1,2)$.

1.  Explain why there is a unique linear map $f : {\bf R}^3 \to {\bf R}^3$ such that $f(v_1)=(0,0,0)$, $f(v_2)=(1,0,3)$ and $v_3$ is an eigenvector of eigenvalue 4.

2.  Compute the matrix $A$ of $f$ with respect to the basis $v_1, v_2, v_3$ (both on the domain and on the codomain).

3.  Compute the matrix $B$ of $f$ with respect to the standard basis (both for the domain and the codomain).

4.  For $t \in {\bf R}$, consider the vector $v_t = (2,t,5)$. For which values of $t$ is $v_t \in {\operatorname{im}\ } f$?

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 6.14</strong></p>

<span id="ex-eigenvalues-5-7" label="ex:eigenvalues-5-7"></span> (See <a href="#sol-ex-eigenvalues-5-7" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-5-7">Solution 6.6.14</a>.) Consider the matrix
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

<span id="ex-eigenvalues-5-9" label="ex:eigenvalues-5-9"></span> (See <a href="#sol-ex-eigenvalues-5-9" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-5-9">Solution 6.6.15</a>.) Consider the matrix
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

<span id="ex-eigenvalues-5-10" label="ex:eigenvalues-5-10"></span> (See <a href="#sol-ex-eigenvalues-5-10" data-reference-type="ref+Label" data-reference="sol--ex:eigenvalues-5-10">Solution 6.6.16</a>.) Consider the matrix $A = \begin{pmatrix}
1 & 0 & t \\
1 & 2 & 1 \\
2 & 0 & -1
\end{pmatrix}$

1.  For what value of $t \in {\bf R}$ is the matrix $A$ *non-*invertible?

2.  For each $t \in {\bf R}$, determine the eigenvalues of $A$. Specify for which values $t \in {\bf R}$ all the eigenvalues of $A$ are real numbers.

3.  Determine for which $t \in {\bf R}$ there are eigenvalues with multiplicity $> 1$.

4.  For the value of $t$ found in the first part of the exercise: compute a basis of all eigenspaces and decide whether $A$ is diagonalizable.

</div>

## Solutions to the exercises

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 6.6.1</strong></p>

<span id="sol-ex-eigenvalues-exercise-001" label="sol--ex:eigenvalues-exercise-001"></span> (See <a href="#ex-eigenvalues-exercise-001" data-reference-type="ref+Label" data-reference="ex:eigenvalues-exercise-001">Exercise 6.1</a>.) To decide whether the matrix $A = \left ( \begin{array}{ccc} 2 & 1 & 1 \\ 0 & 1 & 0 \\ 1 & -1 & 2 \end{array} \right )$ is diagonalizable, we follow <a href="#met-diagonalizability" data-reference-type="ref+Label" data-reference="met:diagonalizability">Method 6.15</a>.

We first compute the characteristic polynomial and eigenvalues. We compute $\chi_A(t) = \det(A - t \cdot \mathrm{id}_3)$, cf. <a href="#dlm-eigenvalues-definitionlemma-001" data-reference-type="ref+Label" data-reference="dlm:eigenvalues-definitionlemma-001">Definition and Lemma 6.5</a>. Expanding the determinant of
<div class="arithmatex" markdown="1">
\[
A - t \cdot \mathrm{id}_3 = \left ( \begin{array}{ccc} 2-t & 1 & 1 \\ 0 & 1-t & 0 \\ 1 & -1 & 2-t \end{array} \right ),
\]
</div>
by developing along the second row (<a href="../determinants/#prop-cofactor-expansion" data-reference-type="ref+Label" data-reference="prop:cofactor-expansion">Proposition 5.23</a>), we get
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\chi_A(t) & = (1-t) \det \left ( \begin{array}{cc} 2-t & 1 \\ 1 & 2-t \end{array} \right ) \\
& = (1-t)\bigl[(2-t)^2 - 1\bigr] \\
& = (1-t)(3 - 4t + t^2) \\
& = (1-t)(t-1)(t-3) \\
& = -(t-1)^2(t-3).
\end{align*}
\]
</div>
The eigenvalues are $\lambda_1 = 1$ (with algebraic multiplicity 2) and $\lambda_2 = 3$ (with algebraic multiplicity 1).

We now compute the eigenspaces. For $\lambda_2 = 3$: we solve $(A - 3\,\mathrm{id}_3)v = 0$:
<div class="arithmatex" markdown="1">
\[
A - 3\,\mathrm{id}_3 = \left ( \begin{array}{ccc} -1 & 1 & 1 \\ 0 & -2 & 0 \\ 1 & -1 & -1 \end{array} \right ) \leadsto \left ( \begin{array}{ccc} 1 & 0 & -1 \\ 0 & 1 & 0 \\ 0 & 0 & 0 \end{array} \right ).
\]
</div>
So $E_3 = \ker(A - 3\,\mathrm{id}_3) = L\bigl((1, 0, 1)\bigr)$, which has dimension 1.

For $\lambda_1 = 1$: we solve $(A - \mathrm{id}_3)v = 0$:
<div class="arithmatex" markdown="1">
\[
A - \mathrm{id}_3 = \left ( \begin{array}{ccc} 1 & 1 & 1 \\ 0 & 0 & 0 \\ 1 & -1 & 1 \end{array} \right ) \leadsto \left ( \begin{array}{ccc} 1 & 0 & 1 \\ 0 & 1 & 0 \\ 0 & 0 & 0 \end{array} \right ).
\]
</div>
So $E_1 = \ker(A - \mathrm{id}_3) = L\bigl((-1, 0, 1)\bigr)$. Hence the rank is 2, so $\dim E_1 = 1$.

Finally, we check diagonalizability. By <a href="#met-diagonalizability" data-reference-type="ref+Label" data-reference="met:diagonalizability">Method 6.15</a>, $A$ is diagonalizable if and only if $\dim E_1 + \dim E_3 = 3$. We have $\dim E_1 = 1$ and $\dim E_3 = 1$, so $\dim E_1 + \dim E_3 = 2 \ne 3$. Therefore, $A$ is not diagonalizable.

Indeed, the eigenvalue $\lambda_1 = 1$ has algebraic multiplicity 2 but its eigenspace has dimension only 1, which is the obstruction to diagonalizability, cf. also <a href="#lem-eigenvalues-lemma-001" data-reference-type="ref+Label" data-reference="lem:eigenvalues-lemma-001">Lemma 6.18</a>.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 6.6.2</strong></p>

<span id="sol-exercise-eigenvalues-2x2" label="sol--exercise.eigenvalues.2x2"></span> (See <a href="#exercise-eigenvalues-2x2" data-reference-type="ref+Label" data-reference="exercise.eigenvalues.2x2">Exercise 6.2</a>.) For $A = \left ( \begin{array}{cc} a & b \\ c & d \end{array} \right )$ we have $A - t\,\mathrm{id}_2 = \left ( \begin{array}{cc} a-t & b \\ c & d-t \end{array} \right )$.

By definition (<a href="#dlm-eigenvalues-definitionlemma-001" data-reference-type="ref+Label" data-reference="dlm:eigenvalues-definitionlemma-001">Definition and Lemma 6.5</a>):
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\chi_A(t) & = \det \left ( \begin{array}{cc} a-t & b \\ c & d-t \end{array} \right ) \\
& = (a-t)(d-t) - bc \\
& = t^2 - (a+d)t + (ad-bc) \\
& = t^2 - \mathrm{tr}(A) t + \det A,
\end{align*}
\]
</div>
where $\mathrm{tr}(A)=a+d$ is the trace (see <a href="../maps/#trace" data-reference-type="ref+Label" data-reference="trace">Exercise 4.24</a>).

The eigenvalues are the roots of $\chi_A(t)=0$, hence
<div class="arithmatex" markdown="1">
\[
t^2 - (a+d)t + (ad-bc) = 0.
\]
</div>
By the quadratic formula,
<div class="arithmatex" markdown="1">
\[
\lambda_{1,2}
= \frac{a+d}{2} \pm \sqrt{\left(\frac{a+d}{2}\right)^2 - (ad-bc)}
= \frac{a+d}{2} \pm \sqrt{\frac{(a-d)^2}{4}+bc}.
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 6.6.3</strong></p>

<span id="sol-ex-eigenvalues-exercise-002" label="sol--ex:eigenvalues-exercise-002"></span> (See <a href="#ex-eigenvalues-exercise-002" data-reference-type="ref+Label" data-reference="ex:eigenvalues-exercise-002">Exercise 6.3</a>.) We compute $\chi_A(t)$, eigenvalues, eigenspaces, and diagonalizability for each matrix, following <a href="#dlm-eigenvalues-definitionlemma-001" data-reference-type="ref+Label" data-reference="dlm:eigenvalues-definitionlemma-001">Definition and Lemma 6.5</a> and <a href="#met-diagonalizability" data-reference-type="ref+Label" data-reference="met:diagonalizability">Method 6.15</a>.

1.  $A = \left ( \begin{array}{cc} 3 & 5 \\ 1 & -1 \end{array} \right )$.

<div class="arithmatex" markdown="1">
\[
    \begin{align*}
    \chi_A(t) & = \det \left ( \begin{array}{cc} 3-t & 5 \\ 1 & -1-t \end{array} \right )
    = (3-t)(-1-t)-5 \\
    & = t^2-2t-8 = (t-4)(t+2).
    \end{align*}
\]
</div>
    So the eigenvalues of $A$ are $4$ and $-2$. Since these are two distinct eigenvalues, $A$ is diagonalizable by <a href="#cor-diag-max" data-reference-type="ref+Label" data-reference="cor:diag-max">Corollary 6.16</a>. One computes the eigenspaces and thus an eigenbasis for example using Gaussian elimination. For $\lambda=4$, $A-4\,\mathrm{id}_2 = \left ( \begin{array}{cc} -1 & 5 \\ 1 & -5 \end{array} \right ) \leadsto x=5y,$ so $E_4 = L((5,1))$.

    For $\lambda=-2$, $A+2\,\mathrm{id}_2 = \left ( \begin{array}{cc} 5 & 5 \\ 1 & 1 \end{array} \right ) \leadsto x=-y,$ so $E_{-2} = L((-1,1))$. An eigenbasis for $A$ is $\bigl((5,1),(-1,1)\bigr)$ (cf. <a href="#def-eigenbasis" data-reference-type="ref+Label" data-reference="def:eigenbasis">Definition 6.17</a>).

2.  For the given matrix $A$, we get
<div class="arithmatex" markdown="1">
\[
    \begin{align*}
    \chi_A(t) & = \det \left ( \begin{array}{ccc} -t & 1 & 0 \\ 3 & -t & 1 \\ 2 & 0 & -t \end{array} \right ) \\
    & = (-t)\det\left ( \begin{array}{cc} -t & 1 \\ 0 & -t \end{array} \right )
    - \det\left ( \begin{array}{cc} 3 & 1 \\ 2 & -t \end{array} \right ) \\
    & = -t^3 + 3t + 2 = -(t-2)(t+1)^2.
    \end{align*}
\]
</div>
    The eigenvalues are $2$ and $-1$ (the latter with algebraic multiplicity 2). Since there are only 2 (not 3) distinct eigenvalues We cannot use <a href="#cor-diag-max" data-reference-type="ref+Label" data-reference="cor:diag-max">Corollary 6.16</a> to decide diagonalizability, so we need to compute the eigenspaces. For $\lambda=2$:
<div class="arithmatex" markdown="1">
\[
    A-2\,\mathrm{id}_3 = \left ( \begin{array}{ccc} -2 & 1 & 0 \\ 3 & -2 & 1 \\ 2 & 0 & -2 \end{array} \right ) \leadsto E_2 = L((1,2,1)).
\]
</div>

    For $\lambda=-1$:
<div class="arithmatex" markdown="1">
\[
    A+\mathrm{id}_3 = \left ( \begin{array}{ccc} 1 & 1 & 0 \\ 3 & 1 & 1 \\ 2 & 0 & 1 \end{array} \right ) \leadsto E_{-1} = L((-1,1,2)).
\]
</div>
    Hence $\dim E_2 + \dim E_{-1} = 1+1=2<3$, so $A$ is not diagonalizable; i.e., does not have an eigenbasis.

3.  The matrix $A = \left ( \begin{array}{ccc} 1 & 0 & 0 \\ 0 & 0 & \frac 32 \\ 0 & 0 & 1 \end{array} \right )$ is an upper triangular matrix. Thus the eigenvalues are diagonal entries: $1,0,1$. Thus
<div class="arithmatex" markdown="1">
\[
    \chi_A(t) = (1-t)^2(-t).
\]
</div>

    For $\lambda=1$:
<div class="arithmatex" markdown="1">
\[
    A-\mathrm{id}_3 = \left ( \begin{array}{ccc} 0 & 0 & 0 \\ 0 & -1 & \frac 32 \\ 0 & 0 & 0 \end{array} \right ),
\]
</div>
    so $y=\frac 32 z$, with $x,z$ free. Therefore
<div class="arithmatex" markdown="1">
\[
    E_1 = L((1,0,0),(0,3,2)), \quad \dim E_1=2.
\]
</div>

    For $\lambda=0$ we solve $Av=0$, which gives $x=0$ and $z=0$, so
<div class="arithmatex" markdown="1">
\[
    E_0 = L((0,1,0)), \quad \dim E_0=1.
\]
</div>

    Hence $\dim E_1 + \dim E_0 = 3$, so $A$ is diagonalizable. An eigenbasis is $\bigl((1,0,0),(0,3,2),(0,1,0)\bigr).$

4.  The matrix $A = \left ( \begin{array}{ccc} 0 & 1 & 0 \\ 0 & 0 & 1 \\ 0 & 0 & 0 \end{array} \right )$. is again upper triangular, so the only eigenvalue is $0$ (algebraic multiplicity 3), and
<div class="arithmatex" markdown="1">
\[
    \chi_A(t) = (-t)^3.
\]
</div>
    The eigenspace is $E_0=\ker A$. From
<div class="arithmatex" markdown="1">
\[
    A\left ( \begin{array}{c} x \\ y \\ z \end{array} \right )
    = \left ( \begin{array}{c} y \\ z \\ 0 \end{array} \right ) = 0,
\]
</div>
    we get $y=z=0$, $x$ free. So
<div class="arithmatex" markdown="1">
\[
    E_0 = L((1,0,0)), \quad \dim E_0=1.
\]
</div>

    Since $\dim E_0=1<3$, $A$ is not diagonalizable, and there is no eigenbasis.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 6.6.4</strong></p>

<span id="sol-ex-eigenvalues-exercise-003" label="sol--ex:eigenvalues-exercise-003"></span> (See <a href="#ex-eigenvalues-exercise-003" data-reference-type="ref+Label" data-reference="ex:eigenvalues-exercise-003">Exercise 6.4</a>.) Consider
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{ccc} 1 & 0 & 0 \\ 1 & 1 & 2 \\ 1 & 0 & 1 \end{array} \right ).
\]
</div>
We compute the characteristic polynomial using <a href="#dlm-eigenvalues-definitionlemma-001" data-reference-type="ref+Label" data-reference="dlm:eigenvalues-definitionlemma-001">Definition and Lemma 6.5</a>:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\chi_A(t) & = \det(A-t\,\mathrm{id}_3) \\
& = \det \left ( \begin{array}{ccc} 1-t & 0 & 0 \\ 1 & 1-t & 2 \\ 1 & 0 & 1-t \end{array} \right ) \\
& = (1-t)\det \left ( \begin{array}{cc} 1-t & 2 \\ 0 & 1-t \end{array} \right ) \\
& = (1-t)^3.
\end{align*}
\]
</div>
Hence the only eigenvalue is $\lambda=1$, with algebraic multiplicity $3$. The eigenspace is
<div class="arithmatex" markdown="1">
\[
E_1 = \ker(A-\mathrm{id}_3),
\]
</div>
and
<div class="arithmatex" markdown="1">
\[
A-\mathrm{id}_3
= \left ( \begin{array}{ccc} 0 & 0 & 0 \\ 1 & 0 & 2 \\ 1 & 0 & 0 \end{array} \right )
\leadsto
\left ( \begin{array}{ccc} 1 & 0 & 0 \\ 0 & 0 & 1 \\ 0 & 0 & 0 \end{array} \right ).
\]
</div>
So the equations are $x=0$ and $z=0$, while $y$ is free. Therefore
<div class="arithmatex" markdown="1">
\[
E_1 = L((0,1,0)), \qquad \dim E_1 = 1.
\]
</div>

By <a href="#met-diagonalizability" data-reference-type="ref+Label" data-reference="met:diagonalizability">Method 6.15</a>, diagonalizability would require the sum of dimensions of eigenspaces to be $3$. Here there is only one eigenspace and its dimension is $1$, so $A$ is *not* diagonalizable. Consequently, there is no basis of ${\bf R}^3$ in which the associated matrix of $A$ is diagonal.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 6.6.5</strong></p>

<span id="sol-ex-eigenvalues-5-1" label="sol--ex:eigenvalues-5-1"></span> (See <a href="#ex-eigenvalues-5-1" data-reference-type="ref+Label" data-reference="ex:eigenvalues-5-1">Exercise 6.5</a>.) The condition $\ker f = L((1,1,1))$ implies that $f(1,1,1)=(0,0,0)$, which we can also rewrite as
<div class="arithmatex" markdown="1">
\[
f((1,1,1)) = 0 \cdot (1,1,1).
\]
</div>
Thus, this vector is an eigenvector for $f$, with eigenvalue 0. We therefore have three eigenvectors as follows:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
v_1 = (1,0,1) & \mapsto 2 (1,0,1)\\
v_2 = (2,0,-3) & \mapsto -1 (2,0,-3) \\
v_3 = (1,1,1) & \mapsto 0 (1,1,1).
\end{align*}
\]
</div>
We check that these three vectors form a basis of ${\bf R}^3$ (note that this is therefore an example of an eigenbasis). To this end, we compute the rank of
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc} 1 & 0 & 1 \\ 2 & 0 & -3 \\ 1 & 1 & 1 \end{array} \right ) \leadsto \left ( \begin{array}{ccc} 1 & 0 & 1 \\ 0 & 0 & -5 \\ 0 & 1 & 0 \end{array} \right ).
\]
</div>
This implies that the matrix has rank three, and therefore the three vectors form a basis of ${\bf R}^3$. The matrix of $f$ with respect to the basis $\underline v = \{v_1, v_2, v_3\}$ is
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc} 2 & 0 & 0 \\ 0 & -1 & 0 \\ 0 & 0 & 0 \end{array} \right ).
\]
</div>
In order to compute the matrix of $f$ with respect to the standard basis $\underline e = \{e_1, e_2, e_3 \}$, we use the usual diagram:
<div class="arithmatex" markdown="1">
\[
{\bf R}^3_{\underline e} \xrightarrow[K]{\mathrm {id}} {\bf R}^3_{\underline v} \xrightarrow[\scriptsize {\left ( \begin{array}{ccc} 2 & 0 & 0 \\ 0 & -1 & 0 \\ 0 & 0 & 0 \end{array} \right )}]{f} 
{\bf R}^3_{\underline v} \xrightarrow[K^{-1}]{\mathrm {id}}
{\bf R}^3_{\underline e}.
\]
</div>
It turns out that $K^{-1}$ is easier to compute than $K$. It is given by expressing the $v_i$ in their coordinates in the standard basis vectors, e.g. $v_1 \mapsto {\mathrm {id}}(v_1) = (1,0,1) = 1 e_1 + 0 e_2 + 1 e_3$. This implies $K^{-1} = \left ( \begin{array}{ccc} 1 & 2 & 1 \\ 0 & 0 & 1 \\ 1 & -3 & 1 \end{array} \right )$. We can use this to compute $K = (K^{-1})^{-1})$, cf.. This inverse (of $K^{-1}$) can be computed using <a href="../maps/#thm-invertible-elimination" data-reference-type="ref+Label" data-reference="thm:invertible-elimination">Theorem 4.80</a>, which gives $K = \frac 15 \left ( \begin{array}{ccc} 3 & -5 & 2 \\ 1 & 0 & -1 \\ 0 & 5 & 0 \end{array} \right )$. Then, one computes the product
<div class="arithmatex" markdown="1">
\[
K^{-1} \left ( \begin{array}{ccc} 2 & 0 & 0 \\ 0 & -1 & 0 \\ 0 & 0 & 0 \end{array} \right ) K = \frac 15 \left ( \begin{array}{ccc} 4 & -10 & 6 \\ 0 & 0 & 0 \\ 9 & -10 & 1 \end{array} \right ).
\]
</div>
This is the basis of $f$ with respect to the standard basis.

This is a typical example of the situation that one basis of ${\bf R}^3$ may be more adapted to describing a linear map than another one. An eigenbasis, such as $v_1, v_2, v_3$ gives a particularly simple matrix.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 6.6.6</strong></p>

<span id="sol-ex-eigenvalues-exercise-004" label="sol--ex:eigenvalues-exercise-004"></span> (See <a href="#ex-eigenvalues-exercise-004" data-reference-type="ref+Label" data-reference="ex:eigenvalues-exercise-004">Exercise 6.6</a>.) For
<div class="arithmatex" markdown="1">
\[
A_a = \left ( \begin{array}{ccc} a & 0 & 0 \\ a-2 & 1 & 1 \\ 0 & 1 & 1 \end{array} \right ),
\]
</div>
we compute the characteristic polynomial (<a href="#dlm-eigenvalues-definitionlemma-001" data-reference-type="ref+Label" data-reference="dlm:eigenvalues-definitionlemma-001">Definition and Lemma 6.5</a>):
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\chi_{A_a}(t)
&= \det(A_a - t\,\mathrm{id}_3) \\
&= \det \left ( \begin{array}{ccc} a-t & 0 & 0 \\ a-2 & 1-t & 1 \\ 0 & 1 & 1-t \end{array} \right ) \\
&= (a-t)\det \left ( \begin{array}{cc} 1-t & 1 \\ 1 & 1-t \end{array} \right ) \\
&= (a-t)\bigl((1-t)^2-1\bigr)
= (a-t)\,t\,(t-2).
\end{align*}
\]
</div>
So the eigenvalues are $a,0,2$ (with multiplicities depending on $a$). We distinguish several cases:

1.  If $a\neq 0,2$, there are three distinct eigenvalues, hence $A_a$ is diagonalizable (<a href="#cor-diag-max" data-reference-type="ref+Label" data-reference="cor:diag-max">Corollary 6.16</a>).

2.  If $a=0$, then $A_0 = \left ( \begin{array}{ccc} 0 & 0 & 0 \\ -2 & 1 & 1 \\ 0 & 1 & 1 \end{array} \right ).$ To decide diagonalizability, we note that the eigenspace of $\lambda=2$ is one-dimensional, since the algebraic multiplicity of $\lambda=2$ is 1. We now compute the eigenspace for $\lambda=0$:
<div class="arithmatex" markdown="1">
\[
    A_0 - 0 \,\mathrm{id}_3 = A_0 = \left ( \begin{array}{ccc} 0 & 0 & 0 \\ -2 & 1 & 1 \\ 0 & 1 & 1 \end{array} \right ) \leadsto \left ( \begin{array}{ccc} -2 & 1 & 1 \\ 0 & 1 & 1 \\ 0 & 0 & 0 \end{array} \right ).
\]
</div>
    This gives $x = \frac{1}{2}y + \frac{1}{2}z$ and $y + z = 0$, so $y = -z$. Thus $x = 0$ and $E_0=L((0,1,-1))$, so $\dim E_0=1$ while the algebraic multiplicity of $0$ is $2$. Therefore $A_0$ is not diagonalizable.

3.  If $a=2$, then
<div class="arithmatex" markdown="1">
\[
    A_2 = \left ( \begin{array}{ccc} 2 & 0 & 0 \\ 0 & 1 & 1 \\ 0 & 1 & 1 \end{array} \right ).
\]
</div>
    This time, the algebraic multiplicity of $\lambda = 0$ is 1, so it remains to compute the eigenspace for $\lambda = 2$:
<div class="arithmatex" markdown="1">
\[
    A_2-2\,\mathrm{id}_3
    = \left ( \begin{array}{ccc} 0 & 0 & 0 \\ 0 & -1 & 1 \\ 0 & 1 & -1 \end{array} \right ),
\]
</div>
    so $y=z$ and $x$ is free; hence
<div class="arithmatex" markdown="1">
\[
    E_2 = L((1,0,0),(0,1,1)), \qquad \dim E_2=2.
\]
</div>
    For $\lambda=0$, one gets $E_0=L((0,1,-1))$, thus $\dim E_0=1$. So $\dim E_2+\dim E_0=3$, and by <a href="#met-diagonalizability" data-reference-type="ref+Label" data-reference="met:diagonalizability">Method 6.15</a>, $A_2$ is diagonalizable.

In conclusion, $A_a$ is diagonalizable precisely if $a \ne 0$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 6.6.7</strong></p>

<span id="sol-ex-eigenvalues-5-2" label="sol--ex:eigenvalues-5-2"></span> (See <a href="#ex-eigenvalues-5-2" data-reference-type="ref+Label" data-reference="ex:eigenvalues-5-2">Exercise 6.7</a>.) We have $\det (A_a - t {\mathrm {id}}_3) = \det \left ( \begin{array}{ccc} 4-t & 0 & 4 \\ a & 2-t & a \\ -2 & 0 & -2-t \end{array} \right )$. It is convenient to develop along the second column (<a href="../determinants/#prop-cofactor-expansion" data-reference-type="ref+Label" data-reference="prop:cofactor-expansion">Proposition 5.23</a>), since it has two zeros; other developments are possible and give the same result, but are more tedious to perform. This gives
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\det (A_a - t {\mathrm {id}}_3) & = (2-t) \det \left ( \begin{array}{cc} 4-t & 4 \\ -2 & -2-t \end{array} \right ) \\
& = (2-t)\bigl[(4-t)(-2-t) + 8\bigr] \\
& = (2-t)\bigl[-8-4t+2t+t^2 + 8\bigr] \\
& = (2-t)(t^2-2t) \\
& = (2-t) \cdot t(t-2) \\
& = -(t-2)^2 t.
\end{align*}
\]
</div>
The roots of this polynomial, i.e., the eigenvalues are $2$ and 0 (regardless of the value of $a$). The exponent of $t-2$ in the above polynomial is 2, the one for $t$ is 1. This implies that
<div class="arithmatex" markdown="1">
\[
\begin{align*}
1 \le \dim E_0 \le 1 & \ \text{for all } t \in {\bf R} \\ 
1 \le \dim E_2 \le 2 & \ \text{for all } t \in {\bf R}.
\end{align*}
\]
</div>
According to <a href="#met-diagonalizability" data-reference-type="ref+Label" data-reference="met:diagonalizability">Method 6.15</a>, $A_a$ will be diagonalizable precisely if $\dim E_2 = 2$. We compute $E_2$ by bringing $A_a - 2 {\mathrm {id}}$ into reduced row echelon form:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left ( \begin{array}{ccc} 4-2 & 0 & 4 \\ a & 2-2 & a \\ -2 & 0 & -2-2 \end{array} \right ) & = 
\left ( \begin{array}{ccc} 2 & 0 & 4 \\ a & 0 & a \\ -2 & 0 & -4 \end{array} \right ) \leadsto 
\left ( \begin{array}{ccc} 2 & 0 & 4 \\ a & 0 & a \\ 0 & 0 & 0 \end{array} \right )  \\
& \leadsto \left ( \begin{array}{ccc} 1 & 0 & 2 \\ a & 0 & a \\ 0 & 0 & 0 \end{array} \right )  
\leadsto \left ( \begin{array}{ccc} 1 & 0 & 2 \\ 0 & 0 & a-2a \\ 0 & 0 & 0 \end{array} \right ) \\
& = \left ( \begin{array}{ccc} 1 & 0 & 2 \\ 0 & 0 & -a \\ 0 & 0 & 0 \end{array} \right ).
\end{align*}
\]
</div>
This matrix has rank 1, or equivalently $\dim E_2 = 2$, if and only if $a=0$. Thus, the matrix $A_a$ is diagonalizable precisely if $a=0$. The second part of the exercise then has only to be done for $a=0$, i.e. $A := A_0 = \left ( \begin{array}{ccc} 4 & 0 & 4 \\ 0 & 2 & 0 \\ -2 & 0 & -2 \end{array} \right )$. This can be dealt with as in the previous exercises.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 6.6.8</strong></p>

<span id="sol-ex-eigenvalues-exercise-005" label="sol--ex:eigenvalues-exercise-005"></span> (See <a href="#ex-eigenvalues-exercise-005" data-reference-type="ref+Label" data-reference="ex:eigenvalues-exercise-005">Exercise 6.8</a>.) If $A = \left ( \begin{array}{ccc} 1 & 1 & 1 \\ 0 & 2 & 0 \\ 1 & -1 & 1 \end{array} \right )$ and $B = \left ( \begin{array}{ccc} 2 & 1 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 0 \end{array} \right ).$ represent the same linear map (with respect to different bases), there needs to be a base change matrix $P$ such that $B = P^{-1}AP$. This will imply that $A$ and $B$ have the same characteristic polynomial, and in particular the same eigenvalues (see <a href="#prop-similarity-necessary-conditions" data-reference-type="ref+Label" data-reference="prop:similarity-necessary-conditions">Proposition 6.24</a>). We compute
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\chi_A(t)
&= \det(A-t\,\mathrm{id}_3) \\
&= \det \left ( \begin{array}{ccc} 1-t & 1 & 1 \\ 0 & 2-t & 0 \\ 1 & -1 & 1-t \end{array} \right ) \\
&= (2-t)\det \left ( \begin{array}{cc} 1-t & 1 \\ 1 & 1-t \end{array} \right ) \\
&= (2-t)\bigl((1-t)^2-1\bigr)
= -t(t-2)^2.
\end{align*}
\]
</div>
Hence the eigenvalues are $0$ and $2$ (with algebraic multiplicity $2$ for $2$). The matrix $B$ is upper triangular, so
<div class="arithmatex" markdown="1">
\[
\chi_B(t) = (2-t)^2(-t) = -t(t-2)^2 = \chi_A(t).
\]
</div>
Thus $A$ and $B$ have the same characteristic polynomial and the same eigenvalues. So, from considering only the characteristic polynomial we cannot conclude that $A$ and $B$ do not represent the same linear map with respect to different bases.

We proceed by computing the eigenspaces. In fact, again if $B = P^{-1}AP$, then the eigenspaces (for any $\lambda \in \mathbf{R}$) of $A$ and $B$ are the same. We begin by computing the eigenspaces for $A$. For $\lambda=0$, we solve $Av=0$:
<div class="arithmatex" markdown="1">
\[
\left\{\begin{array}{l}
x+y+z=0 \\
2y=0 \\
x-y+z=0
\end{array}\right.
\iff
\left\{\begin{array}{l}
y=0 \\
x=-z
\end{array}\right.,
\]
</div>
so $E_0(A)=L((1,0,-1))$. For $\lambda=2$, we solve $(A-2\,\mathrm{id}_3)v=0$:
<div class="arithmatex" markdown="1">
\[
A-2\,\mathrm{id}_3 = \left ( \begin{array}{ccc} -1 & 1 & 1 \\ 0 & 0 & 0 \\ 1 & -1 & -1 \end{array} \right ),
\]
</div>
which gives $-x+y+z=0$, i.e. $y=x-z$. Therefore
<div class="arithmatex" markdown="1">
\[
E_2(A) = L((1,1,0),(0,-1,1)), \qquad \dim E_2(A)=2.
\]
</div>
So
<div class="arithmatex" markdown="1">
\[
\dim E_0(A)+\dim E_2(A)=1+2=3,
\]
</div>
and by <a href="#met-diagonalizability" data-reference-type="ref+Label" data-reference="met:diagonalizability">Method 6.15</a>, $A$ is diagonalizable.

For $\lambda=0$:
<div class="arithmatex" markdown="1">
\[
Bv=0
\iff
\left\{\begin{array}{l}
2x+y=0 \\
2y=0
\end{array}\right.
\iff x=y=0,
\]
</div>
so $E_0(B)=L((0,0,1))$. For $\lambda=2$:
<div class="arithmatex" markdown="1">
\[
B-2\,\mathrm{id}_3 = \left ( \begin{array}{ccc} 0 & 1 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & -2 \end{array} \right ),
\]
</div>
so $y=0$, $z=0$, $x$ free, and
<div class="arithmatex" markdown="1">
\[
E_2(B)=L((1,0,0)), \qquad \dim E_2(B)=1.
\]
</div>
Hence
<div class="arithmatex" markdown="1">
\[
\dim E_0(B)+\dim E_2(B)=1+1=2<3,
\]
</div>
so $B$ is not diagonalizable.

In particular, the eigenspaces of $A$ and $B$ are not the same, which implies that $A$ and $B$ do *not* represent the same linear map with respect to different bases.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 6.6.9</strong></p>

<span id="sol-ex-eigenvalues-exercise-006" label="sol--ex:eigenvalues-exercise-006"></span> (See <a href="#ex-eigenvalues-exercise-006" data-reference-type="ref+Label" data-reference="ex:eigenvalues-exercise-006">Exercise 6.9</a>.) For
<div class="arithmatex" markdown="1">
\[
A_t = \left ( \begin{array}{ccc} -1 & 2 & t \\ 2 & 0 & -2 \\ t & -2 & -1 \end{array} \right ),
\]
</div>
the value $0$ is an eigenvalue precisely when
<div class="arithmatex" markdown="1">
\[
\det(A_t)=0
\]
</div>
(<a href="#thm-eigenvalues-theorem-001" data-reference-type="ref+Label" data-reference="thm:eigenvalues-theorem-001">Theorem 6.8</a>). (Alternatively, one may also compute the rank of $A_t$ and check when it is $\le 2$.) By developing along the first row (<a href="../determinants/#prop-cofactor-expansion" data-reference-type="ref+Label" data-reference="prop:cofactor-expansion">Proposition 5.23</a>), we compute
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\det(A_t)
&= -1\det\left ( \begin{array}{cc} 0 & -2 \\ -2 & -1 \end{array} \right )
-2\det\left ( \begin{array}{cc} 2 & -2 \\ t & -1 \end{array} \right )
+t\det\left ( \begin{array}{cc} 2 & 0 \\ t & -2 \end{array} \right ) \\
&= 4 + (-4t+4) -4t \\
&= 8(1-t).
\end{align*}
\]
</div>
Hence $0$ is an eigenvalue if and only if $t=1$.

So we now consider
<div class="arithmatex" markdown="1">
\[
A_1=\left ( \begin{array}{ccc} -1 & 2 & 1 \\ 2 & 0 & -2 \\ 1 & -2 & -1 \end{array} \right ).
\]
</div>
Its characteristic polynomial is
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\chi_{A_1}(\lambda)
&=\det(A_1-\lambda\,\mathrm{id}_3) = -\lambda(\lambda+4)(\lambda-2).
\end{align*}
\]
</div>
Therefore the eigenvalues are $\lambda_1=0$, $\lambda_2=2$, $\lambda_3=-4.$ For $\lambda=0$, solve $A_1v=0$:
<div class="arithmatex" markdown="1">
\[
\left\{\begin{array}{l}
-x+2y+z=0 \\
2x-2z=0
\end{array}\right.
\Rightarrow x=z,\ y=0,
\]
</div>
so $E_0=L((1,0,1))$. Similarly, one computes the eigenspaces $E_2=L((-1,-2,1))$ and $E_{-4}=L((-1,1,1))$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 6.6.10</strong></p>

<span id="sol-ex-eigenvalues-exercise-007" label="sol--ex:eigenvalues-exercise-007"></span> (See <a href="#ex-eigenvalues-exercise-007" data-reference-type="ref+Label" data-reference="ex:eigenvalues-exercise-007">Exercise 6.10</a>.) Let
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{cc} -4 & 8 \\ 1 & -2 \end{array} \right ),
\qquad
F : {\mathrm {Mat}}_{2\times 2} \to {\mathrm {Mat}}_{2\times 2},\ X\mapsto AX.
\]
</div>
This map is indeed linear by <a href="../maps/#lem-matrix-multiplication-properties" data-reference-type="ref+Label" data-reference="lem:matrix-multiplication-properties">Lemma 4.59</a>. Fixing the basis $\underline E := (E_{11},E_{12},E_{21},E_{22})$, we compute:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
F(E_{11}) &= AE_{11} = \left ( \begin{array}{cc} -4&0\\1&0 \end{array} \right ) = -4E_{11}+E_{21},\\
F(E_{12}) &= AE_{12} = \left ( \begin{array}{cc} 0&-4\\0&1 \end{array} \right ) = -4E_{12}+E_{22},\\
F(E_{21}) &= AE_{21} = \left ( \begin{array}{cc} 8&0\\-2&0 \end{array} \right ) = 8E_{11}-2E_{21},\\
F(E_{22}) &= AE_{22} = \left ( \begin{array}{cc} 0&8\\0&-2 \end{array} \right ) = 8E_{12}-2E_{22}.
\end{align*}
\]
</div>
Therefore the matrix of $F$ with respect to this basis (in the domain and codomain) is
<div class="arithmatex" markdown="1">
\[
M := \left ( \begin{array}{cccc} -4 & 0 & 8 & 0 \\ 0 & -4 & 0 & 8 \\ 1 & 0 & -2 & 0 \\ 0 & 1 & 0 & -2 \end{array} \right ).
\]
</div>

We now compute $\ker F$ and $\operatorname{im} F$ by Gaussian elimination on this $4\times 4$ matrix. Set
<div class="arithmatex" markdown="1">
\[
M
\leadsto
\left ( \begin{array}{cccc} 1 & 0 & -2 & 0 \\ 0 & 1 & 0 & -2 \\ 0 & -4 & 0 & 8 \\ -4 & 0 & 8 & 0 \end{array} \right )
\leadsto
\left ( \begin{array}{cccc} 1 & 0 & -2 & 0 \\ 0 & 1 & 0 & -2 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{array} \right ).
\]
</div>
Hence, for coordinates $(x_1,x_2,x_3,x_4)$ in the basis $\underline E=(E_{11},E_{12},E_{21},E_{22})$, the kernel equations are $x_1-2x_3=0$ and $x_2-2x_4=0$. So
<div class="arithmatex" markdown="1">
\[
\ker F
=L\bigl((2,0,1,0),(0,2,0,1)\bigr)
=L(2E_{11}+E_{21},\ 2E_{12}+E_{22})
=L\left(\left ( \begin{array}{cc} 2 & 0 \\ 1 & 0 \end{array} \right ),\left ( \begin{array}{cc} 0 & 2 \\ 0 & 1 \end{array} \right )\right)
.
\]
</div>
From the same row-reduction we read $\operatorname{rank} M=2$ and pivot columns $1,2$. Therefore
<div class="arithmatex" markdown="1">
\[
\operatorname{im} F
=L\bigl(c_1,c_2\bigr)
=L\bigl((-4,0,1,0),(0,-4,0,1)\bigr)
=L(-4E_{11}+E_{21},\ -4E_{12}+E_{22})
=L\left(\left ( \begin{array}{cc} -4 & 0 \\ 1 & 0 \end{array} \right ),\left ( \begin{array}{cc} 0 & -4 \\ 0 & 1 \end{array} \right )\right),
\]
</div>
where $c_1,c_2$ are the first two columns of $M$.

For eigenvalues and eigenspaces, note that the eigenvector condition $F(X)=\lambda X$ is equivalent to $Au=\lambda u\ \text{and}\ Av=\lambda v$. Indeed, this holds since $A(u \ v) = (Au \ Av)$, for a $2\times 2$ matrix with columns $u,v$. So $u,v$ must be eigenvectors for $A$ (for some eigenvalue $\lambda$). Now
<div class="arithmatex" markdown="1">
\[
\chi_A(t)=\det(A-t\,\mathrm{id}_2)
=\det\left ( \begin{array}{cc} -4-t&8\\1&-2-t \end{array} \right )
=t(t+6),
\]
</div>
so the eigenvalues of $A$ are $0$ and $-6$. Therefore the eigenvalues of $F$ are also $0$ and $-6$.

For $\lambda=0$, the eigenspace is exactly $\ker F$, hence
<div class="arithmatex" markdown="1">
\[
E_0(F)
=L\left(\left ( \begin{array}{cc} 2 & 0 \\ 1 & 0 \end{array} \right ),\left ( \begin{array}{cc} 0 & 2 \\ 0 & 1 \end{array} \right )\right)
=L(2E_{11}+E_{21},\ 2E_{12}+E_{22}).
\]
</div>
For $\lambda=-6$, first compute
<div class="arithmatex" markdown="1">
\[
E_{-6}(A)=L\left(\left ( \begin{array}{c} -4\\1 \end{array} \right )\right).
\]
</div>
Thus both columns of $X$ must belong to the 1-dimensional subspace of $\mathbf R^2$ spanned by this vector, so
<div class="arithmatex" markdown="1">
\[
E_{-6}(F)
=L\left(\left ( \begin{array}{cc} -4 & 0 \\ 1 & 0 \end{array} \right ),\left ( \begin{array}{cc} 0 & -4 \\ 0 & 1 \end{array} \right )\right)
=L(-4E_{11}+E_{21},\ -4E_{12}+E_{22}).
\]
</div>
So, at the end of the computation, the eigenspaces of $F$ are explicitly
<div class="arithmatex" markdown="1">
\[
E_0(F)=L\left(\left ( \begin{array}{cc} 2 & 0 \\ 1 & 0 \end{array} \right ),\left ( \begin{array}{cc} 0 & 2 \\ 0 & 1 \end{array} \right )\right),
\qquad
E_{-6}(F)=L\left(\left ( \begin{array}{cc} -4 & 0 \\ 1 & 0 \end{array} \right ),\left ( \begin{array}{cc} 0 & -4 \\ 0 & 1 \end{array} \right )\right).
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 6.6.11</strong></p>

<span id="sol-ex-eigenvalues-5-4-3" label="sol--ex:eigenvalues-5-4-3"></span> (See <a href="#ex-eigenvalues-5-4-3" data-reference-type="ref+Label" data-reference="ex:eigenvalues-5-4-3">Exercise 6.11</a>.) If $A$ and $B$ represent the same map, then $A = PBP^{-1}$ for some invertible matrix $P$. By <a href="../determinants/#prop-product-formula" data-reference-type="ref+Label" data-reference="prop:product-formula">Proposition 5.18</a>, this implies that $\det A = \det P \det B \det P^{-1} = \det B$. In short, $A$ and $B$ have to have the same determinant. This is true: $\det A = \det B = 9$.

In addition, again by <a href="../determinants/#prop-product-formula" data-reference-type="ref+Label" data-reference="prop:product-formula">Proposition 5.18</a>, $A$ and $B$ have to have the same characteristic polynomial:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\chi_A(t) & = \det (A - t{\mathrm {id}}) \\
& = \det \left ( \begin{array}{ccc} 1-t & 0 & 2 \\ 0 & 3-t & 0 \\ 0 & 0 & 3-t \end{array} \right ) \\
& = (1-t)(3-t)^2 \\
& = \det (B-t{\mathrm {id}}) = \chi_B(t).
\end{align*}
\]
</div>
Again, this is true.

Finally, the dimensions of the eigenspaces of the eigenvalues ($1$ and $3$) need to be equal. For $A$, the eigenspace $E_{1, A}$ for the eigenvalue $\lambda = 1$ has $\dim E_{1,A} = 2$ (as one computes!). For $B$ instead, $\dim E_{1, B} = 1$. Therefore $A$ and $B$ do *not* represent the same linear map.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 6.6.12</strong></p>

<span id="sol-ex-eigenvalues-5-4-4" label="sol--ex:eigenvalues-5-4-4"></span> (See <a href="#ex-eigenvalues-5-4-4" data-reference-type="ref+Label" data-reference="ex:eigenvalues-5-4-4">Exercise 6.12</a>.) The matrix $A$ has eigenvalues $1$ and $2$. The eigenspaces are computed as $E_1 = L(1,0,0)$ and $E_2 = L(1,1,0)$. Their dimensions sum up to 2, which is strictly less than 3, so that $A$ is *not* diagonalizable.

The matrix $A^2$ therefore has $2^2 = 4$ as an eigenvalue. Since similar matrices have the same eigenvalues (<a href="#prop-similarity-necessary-conditions" data-reference-type="ref+Label" data-reference="prop:similarity-necessary-conditions">Proposition 6.24</a>), $A$ is *not* similar to $A^2$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 6.6.13</strong></p>

<span id="sol-ex-eigenvalues-5-5" label="sol--ex:eigenvalues-5-5"></span> (See <a href="#ex-eigenvalues-5-5" data-reference-type="ref+Label" data-reference="ex:eigenvalues-5-5">Exercise 6.13</a>.) We first check that $v_1, v_2, v_3$ are a basis of ${\bf R}^3$. Indeed, one can compute
<div class="arithmatex" markdown="1">
\[
\det \left ( \begin{array}{ccc} 1 & 0 & 1 \\ 1 & 1 & 1 \\ 1 & 1 & 2 \end{array} \right ) = 1 \ne 0,
\]
</div>
so the rank is 3 and the vectors do form a basis.

The condition that $v_3$ be an eigenvector for the eigenvalue 4 means $f(v_3) = 4v_3 = (4,4,8)$. Acccording to <a href="../maps/#prop-linear-map-defined-on-basis" data-reference-type="ref+Label" data-reference="prop:linear-map-defined-on-basis">Proposition 4.39</a>, there is a unique linear map $f$ whose value on $v_1, v_2, v_3$ is prescribed.

We now compute $A$. We have to express $f(v_i)$ as a linear combination in terms of $v_1, v_2, v_3$:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
f(v_1) & = (0,0,0) = 0 v_1 + 0v_2 + 0v_3 \\
f(v_2) & = (1,0,3) = a v_1 + bv_2+cv_3 \\
f(v_3) & = (4,4,8) = 0 v_1 + 0v_2 + 4 v_3.
\end{align*}
\]
</div>
We compute $a,b,c$ above by solving the system
<div class="arithmatex" markdown="1">
\[
(1,0,3) = (a+b+c, b+c, a+b+2c).
\]
</div>
Thus $b=-c$, $1=a$ and then $c=2$. Thus
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{ccc} 0 & 1 & 0 \\ 0 & -2 & 0 \\ 0 & 2 & 4 \end{array} \right ).
\]
</div>

In order to compute $B$ we could use the base change matrix, but it is also possible to compute $B$ directly. We will express the standard basis vectors $(1,0,0)$ as a linear combination of the $v_1, v_2, v_3$:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
av_1 +bv_2 +cv_3 
& = a(1,0,1)  + b(1,1,1)+c(1,1,2) \\
& =(a+b+c,b+c,a+b+2c).
\end{align*}
\]
</div>
Thus, the equation $(1,0,0) = av_1+bv_2 +cv_3$ amounts to the linear system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
1 & = a+b+c \\
0 &= b+c \\
0 &= a+b+2c
\end{align*}
\]
</div>
One solves this: $a=1$, $b=1$, $c=-1$. Similarly, one solves the linear system $(0,1,0) = av_1+bv_2+cv_3$. Its solution is $a=-1$, $b=1$, $c=0$. Finally, for $(0,0,1)=av_1+bv_2+cv_3$ one gets the solution $a=0$, $b=-1$, $c=1$.

Thus, since $f$ is linear (this is the key point!, cf. <a href="../maps/#def-linear-map" data-reference-type="ref+Label" data-reference="def:linear-map">Definition 4.1</a>), we have
<div class="arithmatex" markdown="1">
\[
\begin{align*}
f(1,0,0) & = f(v_1+v_2-v_3) \\
& = f(v_1) +f(v_2)-f(v_3) \\
&= (0,0,0)+(1,0,3)-4(1,1,2) \\
&=(-3,-4,-5).
\end{align*}
\]
</div>
Likewise
<div class="arithmatex" markdown="1">
\[
\begin{align*}
f(0,1,0) &= f(-v_1+v_2) = -f(v_1)+f(v_2) = (1,0,3) \\
f(0,0,1)& =f(-v_2+v_3) = -f(v_2)+f(v_3) = (3,4,5) \\
\end{align*}
\]
</div>
Therefore (writing $f(1,0,0)$ as the first column etc.), we get
<div class="arithmatex" markdown="1">
\[
B = \left ( \begin{array}{ccc} -3 & 1 & 3 \\ -4 & 0 & 4 \\ -5 & 3 & 5 \end{array} \right ).
\]
</div>

The vector $v_t$ belongs to the image precisely if is a linear combination of the vectors $f(v_1) = 0$, $f(v_2)=(1,0,3)$ and $f(v_3) = (4,4,8)$. This translates into the linear system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
a+3b & = 2\\
4b&=t\\
3a+5b&= 5.
\end{align*}
\]
</div>
One solves the first and third equation to $a = \frac 54$, $b=\frac 14$. Therefore, the system has a solution precisely if $t=1$. (Alternatively, one may also solve the linear system $B \left ( \begin{array}{c} x \\ y \\ z \end{array} \right ) = \left ( \begin{array}{c} 2 \\ t \\ 5 \end{array} \right )$.)

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 6.6.14</strong></p>

<span id="sol-ex-eigenvalues-5-7" label="sol--ex:eigenvalues-5-7"></span> (See <a href="#ex-eigenvalues-5-7" data-reference-type="ref+Label" data-reference="ex:eigenvalues-5-7">Exercise 6.14</a>.) By <a href="../determinants/#thm-det-zero-niff-invertible" data-reference-type="ref+Label" data-reference="thm:det-zero-niff-invertible">Theorem 5.15</a>, $A$ is invertible precisely iff $\det A = 0$. We compute the determinant, for example using Sarrus’ rule (<a href="../determinants/#lem-sarrus-rule" data-reference-type="ref+Label" data-reference="lem:Sarrus-rule">Lemma 5.11</a>), as $\det A = 0 - 24 + 6t-10t -0+30 = 6-4t$. Thus, the condition $\det A = 6-4t = 0$ amounts to $t = \frac 32$. The matrix $A$ is therefore not invertible precisely if $t = \frac 32$.

We compute the eigenvalues of $A = \left ( \begin{array}{ccc} 0 & 2 & 2 \\ -3 & -5 & 6 \\ -2 & -2 & 5 \end{array} \right )$ by computing its characteristic polynomial. It is given by
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\chi_A(t) & = t(5+t)(5-t)-24+12+4(-5-t)-12t+6(5-t) \\
& = -t^3 + 3t-2.
\end{align*}
\]
</div>
One zero of this polynomial is $t = 1$. Dividing the above polynomial by $t-1$ gives $-t^2 -t+2$, which has zeroes 1 and $-2$, respectively. Thus
<div class="arithmatex" markdown="1">
\[
\chi_A(t) = -(t-1)^2 (t+2).
\]
</div>
The eigenvalues of $A$ are therefore $\lambda = 1$ and $\lambda = -2$.

We compute the eigenspaces by bringing $A - \lambda {\mathrm {id}}$ into row echelon form
<div class="arithmatex" markdown="1">
\[
\begin{align*}
A - (-2) {\mathrm {id}} & = \left ( \begin{array}{ccc} 2 & 2 & 2 \\ -3 & -3 & 6 \\ -2 & -2 & 3 \end{array} \right ) \leadsto \left ( \begin{array}{ccc} 1 & 1 & 1 \\ 1 & 1 & -2 \\ 2 & 2 & -3 \end{array} \right ) \\
& \leadsto \left ( \begin{array}{ccc} 1 & 1 & 1 \\ 0 & 0 & 1 \\ 0 & 0 & 1 \end{array} \right ) \leadsto \left ( \begin{array}{ccc} 1 & 1 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 0 \end{array} \right ).
\end{align*}
\]
</div>
This matrix has rank 2, and its kernel is thus 1-dimensional. It is spanned by $(1,-1,0)$. Similarly
<div class="arithmatex" markdown="1">
\[
\begin{align*}
A - {\mathrm {id}} & = \left ( \begin{array}{ccc} -1 & 2 & 2 \\ -3 & -3 & 6 \\ -2 & -2 & 4 \end{array} \right ) \leadsto \left ( \begin{array}{ccc} 1 & -2 & -2 \\ 0 & 1 & 0 \\ 0 & 1 & 0 \end{array} \right ) \\
& \leadsto \left ( \begin{array}{ccc} 1 & 0 & -2 \\ 0 & 1 & 0 \\ 0 & 0 & 0 \end{array} \right ).
\end{align*}
\]
</div>
This again has rank 2, so that the eigenspace $E_1$ is again 1-dimensional. It is spanned by $(2,0,1)$.

Since $v =(2,0,a)$ was requested to be an eigenvector, it will be in one of the two eigenspaces. One sees it must lie in $E_1$, and $(2,0,a)$ lies in $E_1$ precisely if $a=1$. Thus $v=(2,0,1)$, and its eigenvalue is 1.

The matrix $A$ is not diagonalizable, since $\dim E_2 + \dim E_1 = 2 < 3$.

The matrix $A$ is not similar to $A^2$ since similar matrices have the same determinant. Above we computed $\det A = 6-4t$, so for $t = 2$ we have $\det A = -2$, so that $\det A^2 = (-2)^2 = 4 \ne \det A$.

These computations can also be performed using any computer algebra software such as Wolfram Alpha:

- <https://www.wolframalpha.com/input?i=Characteristic+polynomial+%28%280%2C2%2C2%29%2C%28-3%2C-5%2C6%29%2C%28-2%2C-2%2C5%29%29> (characteristic polynomial)

- <https://www.wolframalpha.com/input?i=Ker+%28+%28%280%2C2%2C2%29%2C%28-3%2C-5%2C6%29%2C%28-2%2C-2%2C5%29%29+-+%28%281%2C0%2C0%29%2C%280%2C1%2C0%29%2C%280%2C0%2C1%29%29%29> (eigenspace)

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 6.6.15</strong></p>

<span id="sol-ex-eigenvalues-5-9" label="sol--ex:eigenvalues-5-9"></span> (See <a href="#ex-eigenvalues-5-9" data-reference-type="ref+Label" data-reference="ex:eigenvalues-5-9">Exercise 6.15</a>.) The kernel of $A$ is different from $\{0\}$ precisely if $A$ is not invertible or, equivalently, if $\det A = 0$. For example using Sarrus’ rule (<a href="../determinants/#lem-sarrus-rule" data-reference-type="ref+Label" data-reference="lem:Sarrus-rule">Lemma 5.11</a>), we have $\det A = 2t-6$, so $t = 3$.

For $t=3$, we have $\chi_A(t) = -t^3+6t^2-8t = -t(t^2-6t+8) = -t(t-2)(t-4)$. The eigenvalues are then 0, 2 and 4.

The eigenspaces are $E_0 = \ker A = L(1,-5,2)$, $E_2 = \ker (A-2{\mathrm {id}}) = L(1,1,0)$ and $E_4 = \ker (A-4{\mathrm {id}}) = L(-1,1,2)$. The matrix $P = \left ( \begin{array}{ccc} 1 & 1 & -1 \\ -5 & 1 & 1 \\ 2 & 0 & 2 \end{array} \right )$ (whose columns are the three eigenvectors comprising an eigenbasis) is then such that $PAP^{-1} = \left ( \begin{array}{ccc} 0 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 4 \end{array} \right )$.

If $B$ satisfies $\chi_B(t)=\chi_A(t)=-t(t-2)(t-4)$, its eigenvalues are 0, 2 and 4. These are 3 distinct eigenvalues (i.e., equal to the size of the matrix), so $B$ is diagonalizable.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 6.6.16</strong></p>

<span id="sol-ex-eigenvalues-5-10" label="sol--ex:eigenvalues-5-10"></span> (See <a href="#ex-eigenvalues-5-10" data-reference-type="ref+Label" data-reference="ex:eigenvalues-5-10">Exercise 6.16</a>.) We compute $\det A = -4t-2$, this is 0 precisely if $t=-\frac 12$. Thus, $A$ is non-invertible for $t=-\frac 12$ and invertible otherwise.

We compute the characteristic polynomial. It is helpful to develop the determinant of $A - \lambda {\mathrm {id}}$ along the second column (<a href="../determinants/#prop-cofactor-expansion" data-reference-type="ref+Label" data-reference="prop:cofactor-expansion">Proposition 5.23</a>), since there are two 0’s in this column, simplifying the formula:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\det (A-\lambda {\mathrm {id}}) & = (2-\lambda) \det \left ( \begin{array}{cc} 1-\lambda & t \\ 2 & -1-\lambda \end{array} \right ) \\
& = (2-\lambda)(\lambda^2 - 2t - 1).
\end{align*}
\]
</div>
The eigenvalues of $A$ are therefore $\lambda_1 = 2$ and $\lambda_{2/3} = \pm \sqrt{2t+1}$. The latter two eigenvalues are real numbers precisely if $2t+1 \ge 0$, i.e., if $t \ge -\frac 12$.

An eigenvalue appears with multiplicity 2 in the above characteristic polynomial precisely if either $2t+1=0$ (so that $\lambda_2=\lambda_3$), i.e., $t=-\frac 12$, or if $\sqrt{2t+1} = 2$, i.e., if $t=\frac 32$.

For $t=-\frac 12$, we compute the eigenspaces for the eigenvalues $\lambda_1 = 2$ and $\lambda_2 = 0$. These are both 1-dimensional, respectively given by $E_2 = L(0,1,0)$ and $E_0 = L(2,-3,4)$. The sum of their dimensions is 2, which is less than 3, so $A$ is not diagonalizable (<a href="#met-diagonalizability" data-reference-type="ref+Label" data-reference="met:diagonalizability">Method 6.15</a>).

</div>
