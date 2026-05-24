---
title: Characteristic Polynomial
---

# The characteristic polynomial

<div class="definitionlemma" markdown="1">


<p class="env-number"><strong>Definition and Lemma 6.5</strong> (Related exercises: <a href="../exercises-eigenvalues/#ex-eigenvalues-exercise-001">Exercise 6.1</a>, <a href="../exercises-eigenvalues/#ex-eigenvalues-exercise-002">Exercise 6.3</a>, <a href="../exercises-eigenvalues/#ex-eigenvalues-exercise-003">Exercise 6.4</a>, <a href="../exercises-eigenvalues/#ex-eigenvalues-exercise-004">Exercise 6.6</a>, <a href="../exercises-eigenvalues/#exercise-eigenvalues-2x2">Exercise 6.2</a>)</p>

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


<p class="env-number"><strong>Theorem 6.8</strong> (Related exercises: <a href="../exercises-eigenvalues/#ex-eigenvalues-exercise-006">Exercise 6.9</a>)</p>

(*Fundamental theorem of algebra*, cf. also §<a href="../c/#sect-the-fundamental-theorem-of-algebra" data-reference-type="ref" data-reference="sect--the_fundamental_theorem_of_algebra">Section 1.2</a> for further discussion) <span id="thm-eigenvalues-theorem-001" label="thm:eigenvalues-theorem-001"></span> For every non-constant polynomial
<div class="arithmatex" markdown="1">
\[
p(t) = a_n x^n + \dots + a_0,
\]
</div>
where the coefficients $a_0, \dots, a_n$ are complex numbers (for example, they can be real numbers), there exists a *complex* number $z \in { {\bf C}}$ such that
<div class="arithmatex" markdown="1">
\[
p(z) = 0.
\]
</div>

</div>

This theorem is famous for the number of entirely different proofs. A completely elementary proof fitting on about two pages is given in (Oliveira 2011).

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

<div id="refs" class="references csl-bib-body hanging-indent">

<div id="ref-Oliveira" class="csl-entry">

Oliveira, Oswaldo Rio Branco de. 2011. *The Fundamental Theorem of Algebra: A Most Elementary Proof*. <https://doi.org/10.4169/amer.math.monthly.119.09.753>.

</div>

</div>
