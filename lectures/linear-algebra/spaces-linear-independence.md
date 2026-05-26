---
title: Linear Independence
---

# Linear independence

Let $v_1, \dots, v_m \in V$ be $m$ vectors in some vector space. Then we have
<div class="arithmatex" markdown="1">
\[
0 \cdot v_1 + \dots + 0 \cdot v_m = 0 \cdot (v_1 + \dots + v_m) = 0.
\]
</div>

<p class="env-number equation-number"><strong>(3.48)</strong></p>

<span id="0-combiniation" label="0.combiniation"></span> This follows from the distributive law and the scalar multiplication of any vector with 0, cf. <a href="../spaces-definition-solution-of-homogeneous/#item-distributive-law" data-reference-type="ref" data-reference="item--distributive law">4.</a> and <a href="../spaces-definition-solution-of-homogeneous/#item-product-0" data-reference-type="ref" data-reference="item--product 0">8.</a> in <a href="../spaces-definition-solution-of-homogeneous/#def-vector-space" data-reference-type="ref+Label" data-reference="def:vector-space">Definition 3.10</a>. So, there is always a “trivial” way to obtain the zero vector from $v_1, \dots, v_m$. We can ask if there are other ways of achieving the zero vector.

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 3.49</strong> (Related exercises: <a href="../exercises-spaces/#ex-basis-w1-r4">Exercise 3.22</a>, <a href="../exercises-spaces/#ex-linear-independence">Exercise 3.7</a>, <a href="../exercises-maps/#ex-maps-exercise-006">Exercise 4.6</a>, <a href="../exercises-spaces/#ex-mat-subspace-dim">Exercise 3.24</a>, <a href="../exercises-spaces/#ex-polynomial-basis-ab">Exercise 3.21</a>, <a href="../exercises-spaces/#ex-r2-spanning">Exercise 3.18</a>, <a href="../exercises-systems/#ex-systems-param-ab">Exercise 2.9</a>, <a href="../exercises-spaces/#ex-three-vectors-r2">Exercise 3.8</a>)</p>

<span id="def-linearly-independent" label="def:linearly-independent"></span> We say $v_1, \dots, v_m$ are *linearly dependent* if there is a *non-zero* linear combination of these that gives the zero vector. I.e., if there are $a_1, \dots, a_m \in {\bf R}$ of *which at least one is non-zero*, such that
<div class="arithmatex" markdown="1">
\[
a_1 v_1 + \dots + a_m v_m = 0.
\]
</div>

<p class="env-number equation-number"><strong>(3.50)</strong></p>

<span id="eqn-lin-dep-def" label="eqn--lin dep def"></span>

If this is not the case, then we say the vectors are *linearly independent*.

</div>

Thus, they are linearly independent if the zero linear combination in <a href="#0-combiniation" data-reference-type="eqref" data-reference="0.combiniation">Equation (3.48)</a> is the *only* way to obtain the zero vector as a linear combination of $v_1, \dots, v_m$.

<div class="example" markdown="1">


<p class="env-number"><strong>Example 3.51</strong></p>

<span id="ex-standard-basis-linearly-independent" label="ex:standard-basis-linearly-independent"></span> The vectors $e_1 = (1, 0, 0)$, $e_2 = (0,1,0)$ and $e_3=(0,0,1) \in {\bf R}^3$ are linearly independent. To see this, suppose some linear combination equals the zero vector: if
<div class="arithmatex" markdown="1">
\[
a_1 e_1 + a_2 e_2 + a_3 e_3  = (0,0,0)
\]
</div>
then we compute the left hand side as
<div class="arithmatex" markdown="1">
\[
(a_1, 0,0 ) + (0, a_2, 0) + (0,0,a_3) = (a_1, a_2, a_3),
\]
</div>
so the above equation forces $a_1 = a_2 = a_3 = 0$. This shows that the vectors are linearly independent.

More generally, the same argument shows that
<div class="arithmatex" markdown="1">
\[
e_1 = (1, 0, \dots, 0), e_2 = (0, 1, 0, \dots 0), \dots, e_n = (0, \dots, 0,  1) \in {\bf R}^n
\]
</div>
are linearly independent.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 3.52</strong></p>

<span id="ex-three-vectors-linearly-dependent" label="ex:three-vectors-linearly-dependent"></span> We revisit the vectors $v_1 := e_1 = (1, 0, 0)$, $v_2 = (0, 1, 1)$ and $v_3 = (2, 1, 1) \in {\bf R}^3$ of <a href="../spaces-linear-combinations/#ex-three-vectors-no-span" data-reference-type="ref+Label" data-reference="ex:three-vectors-no-span">Example 3.45</a>. These vectors are *not* linearly independent. Indeed, we observe that $v_3 = 2 v_1 + v_2$, so that
<div class="arithmatex" markdown="1">
\[
2 v_1 + v_2 - v_3 = 0.
\]
</div>

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 3.53</strong></p>

<span id="ex-spaces-example-018" label="ex:spaces-example-018"></span> The polynomials $1 + x$, $3x+x^2$, $2+x-x^2$ are linearly independent vectors in ${\bf R}[x]^{\le 2}$. To see this, suppose that a linear combination of them equals the zero vector (i.e., the constant polynomial 0):
<div class="arithmatex" markdown="1">
\[
\begin{align*}
0 & = a_1 (1+x) + a_2 (3x+x^2) + a_3 (2+x-x^2) \\
 & = a_1 + 2 a_3 + (a_1 + 3a_2 + a_3) x + (a_2 - a_3) x^2.
\end{align*}
\]
</div>
Since this must hold for all $x \in {\bf R}$, this forces the following homogeneous linear system:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
0 & = a_1 + 2 a_3 \\
0 & = a_1 + 3a_2 + a_3 \\
0 & = a_2 - a_3.
\end{align*}
\]
</div>
Solving this system (do it ) one sees that this only has the trivial solution $a_1 = a_2 = a_3 = 0$. Thus, the polynomials are linearly independent.

</div>

The following statement says in some sense that a family of vectors is linearly independent if there is no redundancy among them.

<div class="lemma" markdown="1">


<p class="env-number"><strong>Lemma 3.54</strong> (Related exercises: <a href="../exercises-spaces/#ex-spaces-2-5">Exercise 3.27</a>)</p>

<span id="lem-independent-linear-combination" label="lem:independent-linear-combination"></span> Let $v_1, \dots, v_m \in V$ be some vectors. They are linearly dependent exactly if (at least) *one* of these vectors can be expressed as a linear combination of the others, i.e., some
<div class="arithmatex" markdown="1">
\[
v_i = a_1 v_1 + \dots + a_{i-1} v_{i-1} + a_{i+1} v_{i+1} + \dots + a_m v_m
\]
</div>

<p class="env-number equation-number"><strong>(3.55)</strong></p>

<span id="eqn-lin-dep" label="eqn--lin dep"></span> for an appropriate $i$ and appropriate coefficients $a_1$ etc.

</div>

<div class="proof" markdown="1">

*Proof.* If holds, then
<div class="arithmatex" markdown="1">
\[
a_1 v_1 + \dots + a_{i-1} v_{i-1} + (-1) v_i + a_{i+1} v_{i+1} + \dots + a_m v_m =0,
\]
</div>
so they are linearly dependent.

Conversely, if holds, then pick some $i$ such that $a_i \ne 0$ (by assumption this is possible). Then one can subtract $a_i v_i$ and divide by $- a_i$ (which is nonzero, crucially!), giving
<div class="arithmatex" markdown="1">
\[
v_i = \frac{-a_1}{a_i} v_1 + \dots + \frac{-a_{i-1}}{a_i} v_{i-1} + \frac{-a_{i+1}}{a_i}  v_{i+1} + \dots + \frac{-a_m}{a_i} v_m.
\]
</div>
This is an equation of the form . ◻

</div>

The following method decides whether a given set of vectors is linearly independent in ${\bf R}^n$. A proof is conveniently done using later results, such as <a href="../maps-inverses/#lem-row-product-invertible" data-reference-type="ref+Label" data-reference="lem:row-product-invertible">Lemma 4.77</a>.

<div class="method" markdown="1">


<p class="env-number"><strong>Method 3.56</strong> (Related exercises: <a href="../exercises-spaces/#ex-linear-independence">Exercise 3.7</a>, <a href="../exercises-maps/#ex-maps-3-5">Exercise 4.15</a>, <a href="../exercises-spaces/#ex-spaces-2-4">Exercise 3.25</a>, <a href="../exercises-spaces/#ex-spaces-2-5">Exercise 3.27</a>, <a href="../exercises-spaces/#ex-spanning-r4">Exercise 3.6</a>, <a href="../exercises-spaces/#ex-wk-basis">Exercise 3.23</a>)</p>

<span id="met-check-linear-independence" label="met:check-linear-independence"></span> Let $v_1, \dots, v_m \in {\bf R}^n$ be some vectors. Form the matrix
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{c} v_1 \\ v_2 \\ \vdots \\ v_m \end{array} \right )
\]
</div>
(i.e., each the $i$-th row of $A$ is precisely the vector $v_i$, so that $A = (v_{ij})$ if $v_i = (v_{i1}, \dots, v_{in})$.) Bring this matrix into row-echelon form using Gaussian elimination (<a href="../systems-gaussian-elimination/#met-gaussian-algorithm" data-reference-type="ref+Label" data-reference="met:gaussian-algorithm">Method 2.29</a>). Call this resulting matrix $B$. If $B$ contains $m$ leading ones, then $v_1, \dots, v_m$ are linearly independent. Otherwise, they are linearly dependent.

</div>

<div class="corollary" markdown="1">


<p class="env-number"><strong>Corollary 3.57</strong></p>

<span id="cor-spaces-corollary-002" label="cor:spaces-corollary-002"></span> More than $n$ vectors can *never* be linearly independent in ${\bf R}^n$ (i.e., for $m > n$, any vectors $v_1, \dots, v_m$ will be linearly dependent, since the matrix $B$ can contain at most $n$ leading ones, being in reduced row-echelon form).

</div>

<div class="remark" markdown="1">


<p class="env-number"><strong>Remark 3.58</strong></p>

<span id="rem-spaces-remark-008" label="rem:spaces-remark-008"></span> This method is very similar to <a href="../spaces-linear-combinations/#met-check-generating-system" data-reference-type="ref+Label" data-reference="met:check-generating-system">Method 3.46</a>, except that there we asked $B$ to contain $n$ leading ones: this guarantees that $v_1, \dots, v_m$ span ${\bf R}^n$. Having as many leading ones as there are vectors, i.e., $m$ leading ones, instead guarantees that the vectors are linearly independent.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 3.59</strong></p>

<span id="ex-three-vectors-linearly-dependent-02" label="ex:three-vectors-linearly-dependent-02"></span> We revisit the vectors $v_1 := e_1 = (1, 0, 0)$, $v_2 = (0, 1, 1)$ and $v_3 = (2, 1, 1) \in {\bf R}^3$ of <a href="#ex-three-vectors-linearly-dependent-02" data-reference-type="ref+Label" data-reference="ex:three-vectors-linearly-dependent-02">Example 3.59</a>. The matrix having these vectors as rows is
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc} 1 & 0 & 0 \\ 0 & 1 & 1 \\ 2 & 1 & 1 \end{array} \right ) .
\]
</div>
We bring it into reduced row echelon form like so:
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc} 1 & 0 & 0 \\ 0 & 1 & 1 \\ 2 & 1 & 1 \end{array} \right ) \leadsto \left ( \begin{array}{ccc} 1 & 0 & 0 \\ 0 & 1 & 1 \\ 0 & 1 & 1 \end{array} \right ) \leadsto \left ( \begin{array}{ccc} 1 & 0 & 0 \\ 0 & 1 & 1 \\ 0 & 0 & 0 \end{array} \right ).
\]
</div>
This reduced row-echelon matrix has only 2 leading ones, so the vectors are *not* linearly independent, i.e., they are linearly dependent.

</div>

The importance of linearly independent vectors comes from the following result:

<div class="proposition" markdown="1">


<p class="env-number"><strong>Proposition 3.60</strong></p>

<span id="prop-linearly-independent-unique" label="prop:linearly-independent-unique"></span> Let $v_1, \dots, v_m$ be linearly independent vectors in a vector space $V$. If some vector $v$ can be expressed as an (ostensibly different) linear combination of those, these presentations must be the same. I.e., if
<div class="arithmatex" markdown="1">
\[
\begin{align*}
v & = a_1 v_1 + \dots + a_m v_m \text{ and }\\
v & = b_1 v_1 + \dots + b_m v_m
\end{align*}
\]
</div>
for appropriate real numbers $a_1, \dots, a_m, b_1, \dots, b_m$, then necessarily we have
<div class="arithmatex" markdown="1">
\[
a_1 = b_1, a_2 = b_2, \dots, a_m = b_m.
\]
</div>

</div>

<div class="proof" markdown="1">

*Proof.* Subtracting these two equations from one another (and using the commutativity of addition, and the law of distributivity, cf. <a href="../spaces-definition-solution-of-homogeneous/#def-vector-space" data-reference-type="ref+Label" data-reference="def:vector-space">Definition 3.10</a>), we obtain
<div class="arithmatex" markdown="1">
\[
\begin{align*}
0 & = v - v \\
& = (a_1 - b_1) v_1 + \dots + (a_m - b_m) v_m.
\end{align*}
\]
</div>
Since the vectors are linearly independent, this implies $a_1 - b_1 = 0$ etc., so that $a_1 = b_1$ etc. ◻

</div>
