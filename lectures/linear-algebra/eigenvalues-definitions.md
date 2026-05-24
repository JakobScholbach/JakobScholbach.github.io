---
title: Definitions
---

<a id="sect-eigenvalues"></a>
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

We consider some of the linear maps $f : {\bf R}^2 \to {\bf R}^2$ of §<a href="../maps-multiplication-of-a-matrix/#sect-2-x-2-matrices" data-reference-type="ref" data-reference="sect--2 x 2 matrices">Subsection 4.2.1</a>.

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
Here we have used standard properties of matrix multiplication (<a href="../maps-composing/#lem-matrix-multiplication-properties" data-reference-type="ref+Label" data-reference="lem:matrix-multiplication-properties">Lemma 4.60</a>). We seek a *non-zero* vector $v$ satisfying this condition. Such a vector exists if and only if $A - \lambda {\mathrm {id}}$ is *not* invertible.

<div class="example" markdown="1">


<p class="env-number"><strong>Example 6.4</strong></p>

<span id="ex-eigenvalues-example-002" label="ex:eigenvalues-example-002"></span> We consider the shearing matrix $A = \left ( \begin{array}{cc} 1 & r \\ 0 & 1 \end{array} \right )$, where we assume $r \ne 0$ (otherwise $A = {\mathrm {id}}$). We check the invertibility of the matrix:
<div class="arithmatex" markdown="1">
\[
A - \lambda {\mathrm {id}} = \left ( \begin{array}{cc} 1-\lambda & r \\ 0 & 1-\lambda \end{array} \right ).
\]
</div>
It suffices to compute the determinant (<a href="../determinants-invertibility-and-determinants/#thm-det-zero-niff-invertible" data-reference-type="ref+Label" data-reference="thm:det-zero-niff-invertible">Theorem 5.15</a>):
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
