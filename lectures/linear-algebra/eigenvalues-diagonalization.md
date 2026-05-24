---
title: Diagonalization
---

# Diagonalizing matrices

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


<p class="env-number"><strong>Method 6.15</strong> (Related exercises: <a href="../exercises-eigenvalues/#ex-eigenvalues-5-10">Exercise 6.16</a>, <a href="../exercises-eigenvalues/#ex-eigenvalues-5-2">Exercise 6.7</a>, <a href="../exercises-eigenvalues/#ex-eigenvalues-exercise-001">Exercise 6.1</a>, <a href="../exercises-eigenvalues/#ex-eigenvalues-exercise-002">Exercise 6.3</a>, <a href="../exercises-eigenvalues/#ex-eigenvalues-exercise-003">Exercise 6.4</a>, <a href="../exercises-eigenvalues/#ex-eigenvalues-exercise-004">Exercise 6.6</a>, <a href="../exercises-eigenvalues/#ex-eigenvalues-exercise-005">Exercise 6.8</a>)</p>

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


<p class="env-number"><strong>Corollary 6.16</strong> (Related exercises: <a href="../exercises-eigenvalues/#ex-eigenvalues-exercise-002">Exercise 6.3</a>, <a href="../exercises-eigenvalues/#ex-eigenvalues-exercise-004">Exercise 6.6</a>)</p>

<span id="cor-diag-max" label="cor:diag-max"></span> If an $n \times n$-matrix has $n$ distinct eigenvalues, then it is diagonalizable.

</div>

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 6.17</strong> (Related exercises: <a href="../exercises-eigenvalues/#ex-eigenvalues-exercise-002">Exercise 6.3</a>)</p>

<span id="def-eigenbasis" label="def:eigenbasis"></span> Let $A \in {\mathrm {Mat}}_{n \times n}$ be given. A basis $v_1, \dots, v_n$ of ${\bf R}^n$ is called an *eigenbasis* for $A$ if each $v_i$ is an eigenvector (for a certain eigenvalue) of $A$.

</div>

<div class="lemma" markdown="1">


<p class="env-number"><strong>Lemma 6.18</strong> (Related exercises: <a href="../exercises-eigenvalues/#ex-eigenvalues-exercise-001">Exercise 6.1</a>)</p>

<span id="lem-eigenvalues-lemma-001" label="lem:eigenvalues-lemma-001"></span> For $A \in {\mathrm {Mat}}_{n \times n}$ the following two statements are equivalent:

1.  $A$ is diagonalizable.

2.  $A$ admits an eigenbasis, i.e., there is an eigenbasis (of ${\bf R}^n$) for $A$.

</div>

One proves this by observing that if $PAP^{-1}$ is a diagonal matrix, then $P$ is a base-change matrix between the standard basis and an eigenbasis.

<div class="example" markdown="1">


<p class="env-number"><strong>Example 6.19</strong></p>

<span id="ex-eigenvalues-example-007" label="ex:eigenvalues-example-007"></span> The matrix $A = \left ( \begin{array}{cc} 0 & -1 \\ -2 & 0 \end{array} \right )$ in <a href="../eigenvalues-eigenspaces/#ex-diagonalizable-2-x-2" data-reference-type="ref+Label" data-reference="ex:diagonalizable-2-x-2">Example 6.13</a> has two distinct eigenvalues, and is therefore diagonalizable (<a href="#cor-diag-max" data-reference-type="ref+Label" data-reference="cor:diag-max">Corollary 6.16</a>). An eigenbasis for $A$ is
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
E_i = \{ v \in { {\bf C}}^2 \ | \ (A - i \cdot {\mathrm {id}}) v = 0 \}.
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
E_i = \{ (iz, z) \ | \ z \in { {\bf C}} \},
\]
</div>
i.e., as a complex vector space, $E_i$ is 1-dimensional and a basis of it is the vector $(i,1)$.

Similarly,
<div class="arithmatex" markdown="1">
\[
E_{-i} = \{ v\in { {\bf C}}^2 \ | \ (A + i \cdot {\mathrm {id}})v = 0\}.
\]
</div>
Computing this leads to the linear system
<div class="arithmatex" markdown="1">
\[
(A + i \cdot {\mathrm {id}}) v = \left ( \begin{array}{cc} +i & -1 \\ 1 & +i \end{array} \right ) \left ( \begin{array}{c} z_1 \\ z_2 \end{array} \right ) = \left ( \begin{array}{c} iz_1-z_2 \\ z_1+iz_2 \end{array} \right ) \stackrel ! = \left ( \begin{array}{c} 0 \\ 0 \end{array} \right ).
\]
</div>
This gives $z_1 = -iz_2$, so that $E_{-i} = \{(-iz, z) \ | \ z \in { {\bf C}}\}$, and a basis of it is the (single) vector $(-i, 1)$. Thus, the matrix $P$ above is
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


<p class="env-number"><strong>Proposition 6.24</strong> (Related exercises: <a href="../exercises-eigenvalues/#ex-eigenvalues-5-4-4">Exercise 6.12</a>, <a href="../exercises-eigenvalues/#ex-eigenvalues-exercise-005">Exercise 6.8</a>)</p>

<span id="prop-similarity-necessary-conditions" label="prop:similarity-necessary-conditions"></span> If $A$ and $B$ are similar, then the following holds:

1.  $\det A = \det B$,

2.  $\mathrm{tr} A = \mathrm{tr} B$ (the traces, see <a href="../exercises-maps/#trace" data-reference-type="ref+Label" data-reference="trace">Exercise 4.24</a>),

3.  $\chi_A(t) = \chi_B(t)$,

4.  $A$ and $B$ have the same eigenvalues. The eigenspaces are related like so: if $B=PAP^{-1}$, then
<div class="arithmatex" markdown="1">
\[
    E_\lambda(B)=P(E_\lambda(A))\quad\text{for every }\lambda.
\]
</div>

</div>

<div class="proof" markdown="1">

*Proof.* Let $B=PAP^{-1}$ with $P$ invertible. For the determinant, using multiplicativity of the determinant (<a href="../determinants-further-properties/#prop-product-formula" data-reference-type="ref+Label" data-reference="prop:product-formula">Proposition 5.18</a>):
<div class="arithmatex" markdown="1">
\[
\det B=\det(PAP^{-1})=\det P\,\det A\,\det(P^{-1})=\det A.
\]
</div>
For the trace, we use the statement proved in <a href="../exercises-maps/#trace" data-reference-type="ref+Label" data-reference="trace">Exercise 4.24</a> (marked \* below):
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
