<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 5.6.1</strong></p>

<span id="sol-ex-determinants-exercise-001" label="sol--ex:determinants-exercise-001"></span> (See <a href="../exercises-determinants/#ex-determinants-exercise-001" data-reference-type="ref+Label" data-reference="ex:determinants-exercise-001">Exercise 5.1</a>.) By <a href="../determinants-invertibility-and-determinants/#thm-det-zero-niff-invertible" data-reference-type="ref+Label" data-reference="thm:det-zero-niff-invertible">Theorem 5.15</a>, the matrix $A$ is invertible if and only if $\det A \ne 0$. Using Sarrus’ rule, cf. <a href="../determinants-determinants-of-larger-matrices/#lem-sarrus-rule" data-reference-type="ref+Label" data-reference="lem:Sarrus-rule">Lemma 5.11</a>, we compute
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

In this case, the inverse can be computed using the adjugate formula from , where the adjugate is defined in <a href="../determinants-invertibility-and-determinants/#def-cofactors" data-reference-type="ref+Label" data-reference="def:cofactors">Definition 5.14</a>. The cofactors are
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

<span id="sol-ex-determinants-exercise-002" label="sol--ex:determinants-exercise-002"></span> (See <a href="../exercises-determinants/#ex-determinants-exercise-002" data-reference-type="ref+Label" data-reference="ex:determinants-exercise-002">Exercise 5.2</a>.) From $A^2 = {\mathrm {id}}$ and the product formula in <a href="../determinants-further-properties/#prop-product-formula" data-reference-type="ref+Label" data-reference="prop:product-formula">Proposition 5.18</a>, we get
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
By <a href="../determinants-determinants-of-larger-matrices/#thm-det-universal-property" data-reference-type="ref+Label" data-reference="thm:det-universal-property">Theorem 5.5</a>, we have $\det({\mathrm {id}})=1$. Therefore
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

<span id="sol-ex-determinants-exercise-003" label="sol--ex:determinants-exercise-003"></span> (See <a href="../exercises-determinants/#ex-determinants-exercise-003" data-reference-type="ref+Label" data-reference="ex:determinants-exercise-003">Exercise 5.3</a>.) Using the $2 \times 2$ determinant formula from <a href="../determinants-determinants-of-2-x-2-matrices/#def-det-2-x-2" data-reference-type="ref+Label" data-reference="def:det-2-x-2">Definition 5.1</a>, we get
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
So every rotation matrix has determinant $1$. (In particular, by <a href="../determinants-invertibility-and-determinants/#thm-det-zero-niff-invertible" data-reference-type="ref+Label" data-reference="thm:det-zero-niff-invertible">Theorem 5.15</a>, every rotation matrix is invertible.)

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 5.6.4</strong></p>

<span id="sol-ex-determinants-exercise-004" label="sol--ex:determinants-exercise-004"></span> (See <a href="../exercises-determinants/#ex-determinants-exercise-004" data-reference-type="ref+Label" data-reference="ex:determinants-exercise-004">Exercise 5.4</a>.) We compute the determinant of
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{cccc} 2 & 0 & 1 & 4 \\ -1 & 3 & 0 & 2 \\ 1 & 0 & 2 & -3 \\ 0 & -2 & 5 & 1 \end{array} \right )
\]
</div>
in two different ways.

**First method (using <a href="../determinants-determinants-of-larger-matrices/#thm-det-universal-property" data-reference-type="ref+Label" data-reference="thm:det-universal-property">Theorem 5.5</a>):** Set $A_0 := A$. Using row additions (which do not change the determinant, cf. <a href="../determinants-determinants-of-larger-matrices/#thm-det-universal-property" data-reference-type="ref+Label" data-reference="thm:det-universal-property">Theorem 5.5</a>) we will bring $A$ to a diagonal form: we consider
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
For the diagonal matrix $A_5$, multilinearity in the rows and $\det({\mathrm{id}})=1$ from <a href="../determinants-determinants-of-larger-matrices/#thm-det-universal-property" data-reference-type="ref+Label" data-reference="thm:det-universal-property">Theorem 5.5</a> give
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

**Second method (using cofactor expansion, <a href="../determinants-further-properties/#prop-cofactor-expansion" data-reference-type="ref+Label" data-reference="prop:cofactor-expansion">Proposition 5.23</a>):** Expand along the second column (which is the most efficient choice, since this column contains two zeros), and use Sarrus’ rule (<a href="../determinants-determinants-of-larger-matrices/#lem-sarrus-rule" data-reference-type="ref+Label" data-reference="lem:Sarrus-rule">Lemma 5.11</a>) to compute the $3 \times 3$-determinants:
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

<span id="sol-ex-determinants-4-1" label="sol--ex:determinants-4-1"></span> (See <a href="../exercises-determinants/#ex-determinants-4-1" data-reference-type="ref+Label" data-reference="ex:determinants-4-1">Exercise 5.5</a>.) According to <a href="../determinants-further-properties/#prop-det-triangular-matrix" data-reference-type="ref+Label" data-reference="prop:det-triangular-matrix">Proposition 5.20</a>, the determinant is the product of the diagonal entries, i.e., it equals $3 \cdot 4 \cdot 5 = 60$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 5.6.6</strong></p>

<span id="sol-ex-determinants-4-2" label="sol--ex:determinants-4-2"></span> (See <a href="../exercises-determinants/#ex-determinants-4-2" data-reference-type="ref+Label" data-reference="ex:determinants-4-2">Exercise 5.6</a>.) The matrix $\left ( \begin{array}{ccc} 1 & 5 & 8 \\ 40 & -9 & 1 \\ 0 & 0 & 0 \end{array} \right )$ has a zero row, so the determinant is $0$ (cf. <a href="../determinants-determinants-of-larger-matrices/#rem-determinants-remark-001" data-reference-type="ref+Label" data-reference="rem:determinants-remark-001">Remark 5.7</a>). The second matrix, $\left ( \begin{array}{ccc} 1 & 5 & 8 \\ 40 & -9 & 1 \\ 1 & 5 & 8 \end{array} \right )$ has two equal rows, so the determinant is $0$ (cf. <a href="../determinants-determinants-of-larger-matrices/#rem-det-zero-equal-rows" data-reference-type="ref+Label" data-reference="rem:det-zero-equal-rows">Remark 5.9</a>).

Equivalently, both matrices are non-invertible (their rows are linearly dependent), and by <a href="../determinants-invertibility-and-determinants/#thm-det-zero-niff-invertible" data-reference-type="ref+Label" data-reference="thm:det-zero-niff-invertible">Theorem 5.15</a> their determinants must be zero.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 5.6.7</strong></p>

<span id="sol-ex-determinants-exercise-005" label="sol--ex:determinants-exercise-005"></span> (See <a href="../exercises-determinants/#ex-determinants-exercise-005" data-reference-type="ref+Label" data-reference="ex:determinants-exercise-005">Exercise 5.7</a>.) The first matrix
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{cccc} 3 & 26 & -9 & 3 \\ 0 & 3 & 1 & 28 \\ 0 & 0 & 2 & 71 \\ 0 & 0 & 0 & 3 \end{array} \right ),
\]
</div>
is an upper triangular matrix, so we can use <a href="../determinants-further-properties/#prop-det-triangular-matrix" data-reference-type="ref+Label" data-reference="prop:det-triangular-matrix">Proposition 5.20</a> to compute its determinant:
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
we use Sarrus’ rule (<a href="../determinants-determinants-of-larger-matrices/#lem-sarrus-rule" data-reference-type="ref+Label" data-reference="lem:Sarrus-rule">Lemma 5.11</a>):
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

<span id="sol-ex-determinants-exercise-006" label="sol--ex:determinants-exercise-006"></span> (See <a href="../exercises-determinants/#ex-determinants-exercise-006" data-reference-type="ref+Label" data-reference="ex:determinants-exercise-006">Exercise 5.8</a>.) By <a href="../determinants-invertibility-and-determinants/#thm-det-zero-niff-invertible" data-reference-type="ref+Label" data-reference="thm:det-zero-niff-invertible">Theorem 5.15</a> and , $A^{-1} = \frac{1}{\det A}\,\mathrm{adj}(A).$ For
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
and by the $2\times2$ inverse formula (cf. <a href="../determinants-invertibility-and-determinants/#ex-determinants-example-002" data-reference-type="ref+Label" data-reference="ex:determinants-example-002">Example 5.17</a>)
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
This exercise can also be solved without using the adjugate formula, as follows: by <a href="../maps-inverses/#thm-invertible-elimination" data-reference-type="ref+Label" data-reference="thm:invertible-elimination">Theorem 4.81</a> (similarly to <a href="../maps-inverses/#ex-maps-example-025" data-reference-type="ref+Label" data-reference="ex:maps-example-025">Example 4.82</a>), we can compute $A^{-1}$ by reducing $(A \ | \ {\mathrm{id}})$ to $({\mathrm{id}} \ | \ A^{-1})$. For $A_2$:
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
