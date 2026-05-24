<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 6.6.1</strong></p>

<span id="sol-ex-eigenvalues-exercise-001" label="sol--ex:eigenvalues-exercise-001"></span> (See <a href="../exercises-eigenvalues/#ex-eigenvalues-exercise-001" data-reference-type="ref+Label" data-reference="ex:eigenvalues-exercise-001">Exercise 6.1</a>.) To decide whether the matrix $A = \left ( \begin{array}{ccc} 2 & 1 & 1 \\ 0 & 1 & 0 \\ 1 & -1 & 2 \end{array} \right )$ is diagonalizable, we follow <a href="../eigenvalues-diagonalization/#met-diagonalizability" data-reference-type="ref+Label" data-reference="met:diagonalizability">Method 6.15</a>.

We first compute the characteristic polynomial and eigenvalues. We compute $\chi_A(t) = \det(A - t \cdot \mathrm{id}_3)$, cf. <a href="../eigenvalues-characteristic-polynomial/#dlm-eigenvalues-definitionlemma-001" data-reference-type="ref+Label" data-reference="dlm:eigenvalues-definitionlemma-001">Definition and Lemma 6.5</a>. Expanding the determinant of
<div class="arithmatex" markdown="1">
\[
A - t \cdot \mathrm{id}_3 = \left ( \begin{array}{ccc} 2-t & 1 & 1 \\ 0 & 1-t & 0 \\ 1 & -1 & 2-t \end{array} \right ),
\]
</div>
by developing along the second row (<a href="../determinants-further-properties/#prop-cofactor-expansion" data-reference-type="ref+Label" data-reference="prop:cofactor-expansion">Proposition 5.23</a>), we get
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

Finally, we check diagonalizability. By <a href="../eigenvalues-diagonalization/#met-diagonalizability" data-reference-type="ref+Label" data-reference="met:diagonalizability">Method 6.15</a>, $A$ is diagonalizable if and only if $\dim E_1 + \dim E_3 = 3$. We have $\dim E_1 = 1$ and $\dim E_3 = 1$, so $\dim E_1 + \dim E_3 = 2 \ne 3$. Therefore, $A$ is not diagonalizable.

Indeed, the eigenvalue $\lambda_1 = 1$ has algebraic multiplicity 2 but its eigenspace has dimension only 1, which is the obstruction to diagonalizability, cf. also <a href="../eigenvalues-diagonalization/#lem-eigenvalues-lemma-001" data-reference-type="ref+Label" data-reference="lem:eigenvalues-lemma-001">Lemma 6.18</a>.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 6.6.2</strong></p>

<span id="sol-exercise-eigenvalues-2x2" label="sol--exercise.eigenvalues.2x2"></span> (See <a href="../exercises-eigenvalues/#exercise-eigenvalues-2x2" data-reference-type="ref+Label" data-reference="exercise.eigenvalues.2x2">Exercise 6.2</a>.) For $A = \left ( \begin{array}{cc} a & b \\ c & d \end{array} \right )$ we have $A - t\,\mathrm{id}_2 = \left ( \begin{array}{cc} a-t & b \\ c & d-t \end{array} \right )$.

By definition (<a href="../eigenvalues-characteristic-polynomial/#dlm-eigenvalues-definitionlemma-001" data-reference-type="ref+Label" data-reference="dlm:eigenvalues-definitionlemma-001">Definition and Lemma 6.5</a>):
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
where $\mathrm{tr}(A)=a+d$ is the trace (see <a href="../exercises-maps/#trace" data-reference-type="ref+Label" data-reference="trace">Exercise 4.24</a>).

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

<span id="sol-ex-eigenvalues-exercise-002" label="sol--ex:eigenvalues-exercise-002"></span> (See <a href="../exercises-eigenvalues/#ex-eigenvalues-exercise-002" data-reference-type="ref+Label" data-reference="ex:eigenvalues-exercise-002">Exercise 6.3</a>.) We compute $\chi_A(t)$, eigenvalues, eigenspaces, and diagonalizability for each matrix, following <a href="../eigenvalues-characteristic-polynomial/#dlm-eigenvalues-definitionlemma-001" data-reference-type="ref+Label" data-reference="dlm:eigenvalues-definitionlemma-001">Definition and Lemma 6.5</a> and <a href="../eigenvalues-diagonalization/#met-diagonalizability" data-reference-type="ref+Label" data-reference="met:diagonalizability">Method 6.15</a>.

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
So the eigenvalues of $A$ are $4$ and $-2$. Since these are two distinct eigenvalues, $A$ is diagonalizable by <a href="../eigenvalues-diagonalization/#cor-diag-max" data-reference-type="ref+Label" data-reference="cor:diag-max">Corollary 6.16</a>. One computes the eigenspaces and thus an eigenbasis for example using Gaussian elimination. For $\lambda=4$, $A-4\,\mathrm{id}_2 = \left ( \begin{array}{cc} -1 & 5 \\ 1 & -5 \end{array} \right ) \leadsto x=5y,$ so $E_4 = L((5,1))$.

    For $\lambda=-2$, $A+2\,\mathrm{id}_2 = \left ( \begin{array}{cc} 5 & 5 \\ 1 & 1 \end{array} \right ) \leadsto x=-y,$ so $E_{-2} = L((-1,1))$. An eigenbasis for $A$ is $\bigl((5,1),(-1,1)\bigr)$ (cf. <a href="../eigenvalues-diagonalization/#def-eigenbasis" data-reference-type="ref+Label" data-reference="def:eigenbasis">Definition 6.17</a>).

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
The eigenvalues are $2$ and $-1$ (the latter with algebraic multiplicity 2). Since there are only 2 (not 3) distinct eigenvalues We cannot use <a href="../eigenvalues-diagonalization/#cor-diag-max" data-reference-type="ref+Label" data-reference="cor:diag-max">Corollary 6.16</a> to decide diagonalizability, so we need to compute the eigenspaces. For $\lambda=2$:
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

<span id="sol-ex-eigenvalues-exercise-003" label="sol--ex:eigenvalues-exercise-003"></span> (See <a href="../exercises-eigenvalues/#ex-eigenvalues-exercise-003" data-reference-type="ref+Label" data-reference="ex:eigenvalues-exercise-003">Exercise 6.4</a>.) Consider
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{ccc} 1 & 0 & 0 \\ 1 & 1 & 2 \\ 1 & 0 & 1 \end{array} \right ).
\]
</div>
We compute the characteristic polynomial using <a href="../eigenvalues-characteristic-polynomial/#dlm-eigenvalues-definitionlemma-001" data-reference-type="ref+Label" data-reference="dlm:eigenvalues-definitionlemma-001">Definition and Lemma 6.5</a>:
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

By <a href="../eigenvalues-diagonalization/#met-diagonalizability" data-reference-type="ref+Label" data-reference="met:diagonalizability">Method 6.15</a>, diagonalizability would require the sum of dimensions of eigenspaces to be $3$. Here there is only one eigenspace and its dimension is $1$, so $A$ is *not* diagonalizable. Consequently, there is no basis of ${\bf R}^3$ in which the associated matrix of $A$ is diagonal.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 6.6.5</strong></p>

<span id="sol-ex-eigenvalues-5-1" label="sol--ex:eigenvalues-5-1"></span> (See <a href="../exercises-eigenvalues/#ex-eigenvalues-5-1" data-reference-type="ref+Label" data-reference="ex:eigenvalues-5-1">Exercise 6.5</a>.) The condition $\ker f = L((1,1,1))$ implies that $f(1,1,1)=(0,0,0)$, which we can also rewrite as
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
It turns out that $K^{-1}$ is easier to compute than $K$. It is given by expressing the $v_i$ in their coordinates in the standard basis vectors, e.g. $v_1 \mapsto {\mathrm {id}}(v_1) = (1,0,1) = 1 e_1 + 0 e_2 + 1 e_3$. This implies $K^{-1} = \left ( \begin{array}{ccc} 1 & 2 & 1 \\ 0 & 0 & 1 \\ 1 & -3 & 1 \end{array} \right )$. We can use this to compute $K = (K^{-1})^{-1})$, cf.. This inverse (of $K^{-1}$) can be computed using <a href="../maps-inverses/#thm-invertible-elimination" data-reference-type="ref+Label" data-reference="thm:invertible-elimination">Theorem 4.81</a>, which gives $K = \frac 15 \left ( \begin{array}{ccc} 3 & -5 & 2 \\ 1 & 0 & -1 \\ 0 & 5 & 0 \end{array} \right )$. Then, one computes the product
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

<span id="sol-ex-eigenvalues-exercise-004" label="sol--ex:eigenvalues-exercise-004"></span> (See <a href="../exercises-eigenvalues/#ex-eigenvalues-exercise-004" data-reference-type="ref+Label" data-reference="ex:eigenvalues-exercise-004">Exercise 6.6</a>.) For
<div class="arithmatex" markdown="1">
\[
A_a = \left ( \begin{array}{ccc} a & 0 & 0 \\ a-2 & 1 & 1 \\ 0 & 1 & 1 \end{array} \right ),
\]
</div>
we compute the characteristic polynomial (<a href="../eigenvalues-characteristic-polynomial/#dlm-eigenvalues-definitionlemma-001" data-reference-type="ref+Label" data-reference="dlm:eigenvalues-definitionlemma-001">Definition and Lemma 6.5</a>):
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

1.  If $a\neq 0,2$, there are three distinct eigenvalues, hence $A_a$ is diagonalizable (<a href="../eigenvalues-diagonalization/#cor-diag-max" data-reference-type="ref+Label" data-reference="cor:diag-max">Corollary 6.16</a>).

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
For $\lambda=0$, one gets $E_0=L((0,1,-1))$, thus $\dim E_0=1$. So $\dim E_2+\dim E_0=3$, and by <a href="../eigenvalues-diagonalization/#met-diagonalizability" data-reference-type="ref+Label" data-reference="met:diagonalizability">Method 6.15</a>, $A_2$ is diagonalizable.

In conclusion, $A_a$ is diagonalizable precisely if $a \ne 0$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 6.6.7</strong></p>

<span id="sol-ex-eigenvalues-5-2" label="sol--ex:eigenvalues-5-2"></span> (See <a href="../exercises-eigenvalues/#ex-eigenvalues-5-2" data-reference-type="ref+Label" data-reference="ex:eigenvalues-5-2">Exercise 6.7</a>.) We have $\det (A_a - t {\mathrm {id}}_3) = \det \left ( \begin{array}{ccc} 4-t & 0 & 4 \\ a & 2-t & a \\ -2 & 0 & -2-t \end{array} \right )$. It is convenient to develop along the second column (<a href="../determinants-further-properties/#prop-cofactor-expansion" data-reference-type="ref+Label" data-reference="prop:cofactor-expansion">Proposition 5.23</a>), since it has two zeros; other developments are possible and give the same result, but are more tedious to perform. This gives
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
According to <a href="../eigenvalues-diagonalization/#met-diagonalizability" data-reference-type="ref+Label" data-reference="met:diagonalizability">Method 6.15</a>, $A_a$ will be diagonalizable precisely if $\dim E_2 = 2$. We compute $E_2$ by bringing $A_a - 2 {\mathrm {id}}$ into reduced row echelon form:
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

<span id="sol-ex-eigenvalues-exercise-005" label="sol--ex:eigenvalues-exercise-005"></span> (See <a href="../exercises-eigenvalues/#ex-eigenvalues-exercise-005" data-reference-type="ref+Label" data-reference="ex:eigenvalues-exercise-005">Exercise 6.8</a>.) If $A = \left ( \begin{array}{ccc} 1 & 1 & 1 \\ 0 & 2 & 0 \\ 1 & -1 & 1 \end{array} \right )$ and $B = \left ( \begin{array}{ccc} 2 & 1 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 0 \end{array} \right ).$ represent the same linear map (with respect to different bases), there needs to be a base change matrix $P$ such that $B = P^{-1}AP$. This will imply that $A$ and $B$ have the same characteristic polynomial, and in particular the same eigenvalues (see <a href="../eigenvalues-diagonalization/#prop-similarity-necessary-conditions" data-reference-type="ref+Label" data-reference="prop:similarity-necessary-conditions">Proposition 6.24</a>). We compute
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
and by <a href="../eigenvalues-diagonalization/#met-diagonalizability" data-reference-type="ref+Label" data-reference="met:diagonalizability">Method 6.15</a>, $A$ is diagonalizable.

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

<span id="sol-ex-eigenvalues-exercise-006" label="sol--ex:eigenvalues-exercise-006"></span> (See <a href="../exercises-eigenvalues/#ex-eigenvalues-exercise-006" data-reference-type="ref+Label" data-reference="ex:eigenvalues-exercise-006">Exercise 6.9</a>.) For
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
(<a href="../eigenvalues-characteristic-polynomial/#thm-eigenvalues-theorem-001" data-reference-type="ref+Label" data-reference="thm:eigenvalues-theorem-001">Theorem 6.8</a>). (Alternatively, one may also compute the rank of $A_t$ and check when it is $\le 2$.) By developing along the first row (<a href="../determinants-further-properties/#prop-cofactor-expansion" data-reference-type="ref+Label" data-reference="prop:cofactor-expansion">Proposition 5.23</a>), we compute
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

<span id="sol-ex-eigenvalues-exercise-007" label="sol--ex:eigenvalues-exercise-007"></span> (See <a href="../exercises-eigenvalues/#ex-eigenvalues-exercise-007" data-reference-type="ref+Label" data-reference="ex:eigenvalues-exercise-007">Exercise 6.10</a>.) Let
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{cc} -4 & 8 \\ 1 & -2 \end{array} \right ),
\qquad
F : {\mathrm {Mat}}_{2\times 2} \to {\mathrm {Mat}}_{2\times 2},\ X\mapsto AX.
\]
</div>
This map is indeed linear by <a href="../maps-composing/#lem-matrix-multiplication-properties" data-reference-type="ref+Label" data-reference="lem:matrix-multiplication-properties">Lemma 4.60</a>. Fixing the basis $\underline E := (E_{11},E_{12},E_{21},E_{22})$, we compute:
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

<span id="sol-ex-eigenvalues-5-4-3" label="sol--ex:eigenvalues-5-4-3"></span> (See <a href="../exercises-eigenvalues/#ex-eigenvalues-5-4-3" data-reference-type="ref+Label" data-reference="ex:eigenvalues-5-4-3">Exercise 6.11</a>.) If $A$ and $B$ represent the same map, then $A = PBP^{-1}$ for some invertible matrix $P$. By <a href="../determinants-further-properties/#prop-product-formula" data-reference-type="ref+Label" data-reference="prop:product-formula">Proposition 5.18</a>, this implies that $\det A = \det P \det B \det P^{-1} = \det B$. In short, $A$ and $B$ have to have the same determinant. This is true: $\det A = \det B = 9$.

In addition, again by <a href="../determinants-further-properties/#prop-product-formula" data-reference-type="ref+Label" data-reference="prop:product-formula">Proposition 5.18</a>, $A$ and $B$ have to have the same characteristic polynomial:
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

<span id="sol-ex-eigenvalues-5-4-4" label="sol--ex:eigenvalues-5-4-4"></span> (See <a href="../exercises-eigenvalues/#ex-eigenvalues-5-4-4" data-reference-type="ref+Label" data-reference="ex:eigenvalues-5-4-4">Exercise 6.12</a>.) The matrix $A$ has eigenvalues $1$ and $2$. The eigenspaces are computed as $E_1 = L(1,0,0)$ and $E_2 = L(1,1,0)$. Their dimensions sum up to 2, which is strictly less than 3, so that $A$ is *not* diagonalizable.

The matrix $A^2$ therefore has $2^2 = 4$ as an eigenvalue. Since similar matrices have the same eigenvalues (<a href="../eigenvalues-diagonalization/#prop-similarity-necessary-conditions" data-reference-type="ref+Label" data-reference="prop:similarity-necessary-conditions">Proposition 6.24</a>), $A$ is *not* similar to $A^2$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 6.6.13</strong></p>

<span id="sol-ex-eigenvalues-5-5" label="sol--ex:eigenvalues-5-5"></span> (See <a href="../exercises-eigenvalues/#ex-eigenvalues-5-5" data-reference-type="ref+Label" data-reference="ex:eigenvalues-5-5">Exercise 6.13</a>.) We first check that $v_1, v_2, v_3$ are a basis of ${\bf R}^3$. Indeed, one can compute
<div class="arithmatex" markdown="1">
\[
\det \left ( \begin{array}{ccc} 1 & 0 & 1 \\ 1 & 1 & 1 \\ 1 & 1 & 2 \end{array} \right ) = 1 \ne 0,
\]
</div>
so the rank is 3 and the vectors do form a basis.

The condition that $v_3$ be an eigenvector for the eigenvalue 4 means $f(v_3) = 4v_3 = (4,4,8)$. Acccording to <a href="../maps-linear-maps-defined-on-basis-vectors/#prop-linear-map-defined-on-basis" data-reference-type="ref+Label" data-reference="prop:linear-map-defined-on-basis">Proposition 4.40</a>, there is a unique linear map $f$ whose value on $v_1, v_2, v_3$ is prescribed.

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

Thus, since $f$ is linear (this is the key point!, cf. <a href="../maps-definition-and-first-examples/#def-linear-map" data-reference-type="ref+Label" data-reference="def:linear-map">Definition 4.1</a>), we have
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

<span id="sol-ex-eigenvalues-5-7" label="sol--ex:eigenvalues-5-7"></span> (See <a href="../exercises-eigenvalues/#ex-eigenvalues-5-7" data-reference-type="ref+Label" data-reference="ex:eigenvalues-5-7">Exercise 6.14</a>.) By <a href="../determinants-invertibility-and-determinants/#thm-det-zero-niff-invertible" data-reference-type="ref+Label" data-reference="thm:det-zero-niff-invertible">Theorem 5.15</a>, $A$ is invertible precisely iff $\det A = 0$. We compute the determinant, for example using Sarrus’ rule (<a href="../determinants-determinants-of-larger-matrices/#lem-sarrus-rule" data-reference-type="ref+Label" data-reference="lem:Sarrus-rule">Lemma 5.11</a>), as $\det A = 0 - 24 + 6t-10t -0+30 = 6-4t$. Thus, the condition $\det A = 6-4t = 0$ amounts to $t = \frac 32$. The matrix $A$ is therefore not invertible precisely if $t = \frac 32$.

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

<span id="sol-ex-eigenvalues-5-9" label="sol--ex:eigenvalues-5-9"></span> (See <a href="../exercises-eigenvalues/#ex-eigenvalues-5-9" data-reference-type="ref+Label" data-reference="ex:eigenvalues-5-9">Exercise 6.15</a>.) The kernel of $A$ is different from $\{0\}$ precisely if $A$ is not invertible or, equivalently, if $\det A = 0$. For example using Sarrus’ rule (<a href="../determinants-determinants-of-larger-matrices/#lem-sarrus-rule" data-reference-type="ref+Label" data-reference="lem:Sarrus-rule">Lemma 5.11</a>), we have $\det A = 2t-6$, so $t = 3$.

For $t=3$, we have $\chi_A(t) = -t^3+6t^2-8t = -t(t^2-6t+8) = -t(t-2)(t-4)$. The eigenvalues are then 0, 2 and 4.

The eigenspaces are $E_0 = \ker A = L(1,-5,2)$, $E_2 = \ker (A-2{\mathrm {id}}) = L(1,1,0)$ and $E_4 = \ker (A-4{\mathrm {id}}) = L(-1,1,2)$. The matrix $P = \left ( \begin{array}{ccc} 1 & 1 & -1 \\ -5 & 1 & 1 \\ 2 & 0 & 2 \end{array} \right )$ (whose columns are the three eigenvectors comprising an eigenbasis) is then such that $PAP^{-1} = \left ( \begin{array}{ccc} 0 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 4 \end{array} \right )$.

If $B$ satisfies $\chi_B(t)=\chi_A(t)=-t(t-2)(t-4)$, its eigenvalues are 0, 2 and 4. These are 3 distinct eigenvalues (i.e., equal to the size of the matrix), so $B$ is diagonalizable.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 6.6.16</strong></p>

<span id="sol-ex-eigenvalues-5-10" label="sol--ex:eigenvalues-5-10"></span> (See <a href="../exercises-eigenvalues/#ex-eigenvalues-5-10" data-reference-type="ref+Label" data-reference="ex:eigenvalues-5-10">Exercise 6.16</a>.) We compute $\det A = -4t-2$, this is 0 precisely if $t=-\frac 12$. Thus, $A$ is non-invertible for $t=-\frac 12$ and invertible otherwise.

We compute the characteristic polynomial. It is helpful to develop the determinant of $A - \lambda {\mathrm {id}}$ along the second column (<a href="../determinants-further-properties/#prop-cofactor-expansion" data-reference-type="ref+Label" data-reference="prop:cofactor-expansion">Proposition 5.23</a>), since there are two 0’s in this column, simplifying the formula:
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

For $t=-\frac 12$, we compute the eigenspaces for the eigenvalues $\lambda_1 = 2$ and $\lambda_2 = 0$. These are both 1-dimensional, respectively given by $E_2 = L(0,1,0)$ and $E_0 = L(2,-3,4)$. The sum of their dimensions is 2, which is less than 3, so $A$ is not diagonalizable (<a href="../eigenvalues-diagonalization/#met-diagonalizability" data-reference-type="ref+Label" data-reference="met:diagonalizability">Method 6.15</a>).

</div>
