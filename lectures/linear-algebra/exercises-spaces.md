<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.1</strong></p>

<span id="ex-exotic-scalar-multiplication" label="ex:exotic-scalar-multiplication"></span> (See <a href="../solutions-vector-spaces/#sol-ex-exotic-scalar-multiplication" data-reference-type="ref+Label" data-reference="sol--ex:exotic-scalar-multiplication">Solution 3.10.1</a>.) Let $V = \{ (x, y, z) \ | \ x, y, z \in {\bf R} \}$. (Thus, $V = {\bf R}^3$.) We use the regular addition of vectors. However, in contrast to the regular scalar multiplication (<a href="../spaces-R2R3Rn/#def-scalar-multiplication" data-reference-type="ref+Label" data-reference="def:scalar-multiplication">Definition 3.7</a>), we now use the following. Decide in each case whether this turns $V$ into a vector space:

- $r \cdot (x, y, z) = (rx, y, rz)$,

- $r \cdot (x, y, z) = (0,0,0)$,

- $r \cdot (x,y,z) = (r^2x, r^2y, r^2z)$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.2</strong></p>

<span id="ex-subspace-statements" label="ex:subspace-statements"></span> (See <a href="../solutions-vector-spaces/#sol-ex-subspace-statements" data-reference-type="ref+Label" data-reference="sol--ex:subspace-statements">Solution 3.10.2</a>.) Let $V \subset {\bf R}^2$ be a subspace. Which of the following statements are correct?

1.  $V$ contains at least one element.

2.  $V$ contains at least two elements.

3.  $V$ contains the zero vector $(0,0)$.

4.  If $v, w \in V$ then also $v - w \in V$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.3</strong></p>

<span id="differentiable-functions" label="differentiable functions"></span> (See <a href="../solutions-vector-spaces/#sol-differentiable-functions" data-reference-type="ref+Label" data-reference="sol--differentiable functions">Solution 3.10.3</a>.) Using basic properties of differentiable functions from your calculus class, show that the space
<div class="arithmatex" markdown="1">
\[
\{ f : {\bf R} \to {\bf R} \ | \ f \text{ is differentiable}\}
\]
</div>
is a vector space (with the sum and scalar multiple defined as in <a href="../spaces-further-examples/#sum-functions" data-reference-type="eqref" data-reference="sum functions">Equation (3.23)</a> and <a href="../spaces-further-examples/#scalar-multiple-functions" data-reference-type="eqref" data-reference="scalar multiple functions">Equation (3.24)</a>).

Hint: structure your thinking as in <a href="../spaces-further-examples/#dlm-polynomials-vector-space" data-reference-type="ref+Label" data-reference="dlm:polynomials-vector-space">Definition and Lemma 3.22</a>.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.4</strong></p>

<span id="ex-union-subspaces" label="ex:union-subspaces"></span> (See <a href="../solutions-vector-spaces/#sol-ex-union-subspaces" data-reference-type="ref+Label" data-reference="sol--ex:union-subspaces">Solution 3.10.4</a>.) Give an example of two subspaces $V, W \subset {\bf R}^2$ such that their *union*
<div class="arithmatex" markdown="1">
\[
V \cup W = \{ x = (x_1, x_2) \in {\bf R}^2 \ | \ x \in V \text{ or } x \in W \}
\]
</div>
is *not* a subspace.

Hint: <a href="../spaces-definition-solution-of-homogeneous/#ex-non-vector-spaces" data-reference-type="ref+Label" data-reference="ex:non-vector-spaces">Example 3.13</a>.

Also give an example of two subspaces $V, W \subset {\bf R}^2$, where the union $V \cup W$ is a subspace.

Hint: be very lazy and minimalistic. What is the smallest subspace you can come up with?

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.5</strong></p>

<span id="ex-span-r4" label="ex:span-r4"></span> (See <a href="../solutions-vector-spaces/#sol-ex-span-r4" data-reference-type="ref+Label" data-reference="sol--ex:span-r4">Solution 3.10.5</a>.) Determine in each case whether $w \in {\bf R}^4$ lies in the span of $v_1$ and $v_2$. If so, name at least one linear combination of $v_1$ and $v_2$ that equals $w$; otherwise explain why there is no such linear combination.

1.  $w = (2, -1,0,1)$, $v_1 = (1,0,0,1)$, $v_2 = (0,1,0,1)$

2.  $w = (1,2,15,11)$, $v_1 = (2,-1,0,2)$, $v_2=(1,-1,-3,1)$

3.  $w = (2,5,8,3)$, $v_1 = (2,-1,0,5)$, $v_2 = (-1, 2, 2, -3)$

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.6</strong></p>

<span id="ex-spanning-r4" label="ex:spanning-r4"></span> (See <a href="../solutions-vector-spaces/#sol-ex-spanning-r4" data-reference-type="ref+Label" data-reference="sol--ex:spanning-r4">Solution 3.10.6</a>.) Determine whether the following vectors span ${\bf R}^4$:

1.  $(1,1,1,1)$, $(0,1,1,1)$, $(0,0,1,1)$, $(0,0,0,1)$

2.  $(1,3,-5,0)$, $(-2, 1,0,0)$, $(0,2,1,-1)$, $(1, -4, 5, 0)$

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.7</strong></p>

<span id="ex-linear-independence" label="ex:linear-independence"></span> (See <a href="../solutions-vector-spaces/#sol-ex-linear-independence" data-reference-type="ref+Label" data-reference="sol--ex:linear-independence">Solution 3.10.7</a>.) Determine whether the following vectors are linearly independent:

1.  $v_1 = (1, -1, 0)$, $v_2=(3,2,-1)$, $v_3 = (3,5,-2)$ in $V = {\bf R}^3$,

2.  $v_1 = (1,1,1)$, $v_2 = (1,-1,1)$, $v_3 = (0,0,1)$ in $V = {\bf R}^3$,

3.  $(1,-1,1,-1)$, $(2,0,1,0)$, $(0,-2,1,-2)$ in ${\bf R}^4$,

4.  $(1,1,0,0)$, $(1,0,1,0)$, $(0,0,1,1)$ and $(0,1,0,1)$ in ${\bf R}^4$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.8</strong></p>

<span id="ex-three-vectors-r2" label="ex:three-vectors-r2"></span> (See <a href="../solutions-vector-spaces/#sol-ex-three-vectors-r2" data-reference-type="ref+Label" data-reference="sol--ex:three-vectors-r2">Solution 3.10.8</a>.) Name three vectors $v_1, v_2, v_3 \in {\bf R}^2$ such that:

- $v_1, v_2$ are linearly independent,

- $v_1, v_3$ are linearly independent, and

- $v_2, v_3$ are linearly independent, but

- $v_1, v_2, v_3$ are *not* linearly independent.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.9</strong></p>

<span id="ex-polynomial-subspaces" label="ex:polynomial-subspaces"></span> (See <a href="../solutions-vector-spaces/#sol-ex-polynomial-subspaces" data-reference-type="ref+Label" data-reference="sol--ex:polynomial-subspaces">Solution 3.10.9</a>.) Consider the vector space $V = {\bf R}[x]^{\le 3}$ of polynomials of degree at most 3. Decide which of the following subsets of $V$ is a subspace:

1.  $\{ f \ | \ f \in V, f(2) = 1 \}$,

2.  $\{ x \cdot f \ | \ f \in {\bf R}[x]^{\le 2} \}$,

3.  $\{ x \cdot f + (1-x) g \ | \ f, g \in {\bf R}[x]^{\le 2} \}$,

4.  $\{ f \ | \ f\in {\bf R}[x]^{\le 3}, f(0) = 0\}$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.10</strong></p>

<span id="ex-poly-span-1" label="ex poly span 1"></span> (See <a href="../solutions-vector-spaces/#sol-ex-poly-span-1" data-reference-type="ref+Label" data-reference="sol--ex poly span 1">Solution 3.10.10</a>.) Express the following polynomials as linear combinations of $x+1$, $x-1$ and $x^2-1$ (in ${\bf R}[x]^{\le 2})$: $x^2 + 4x-2$, $x$, $40-x^2$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.11</strong></p>

<span id="ex-poly-span-2" label="ex poly span 2"></span> (See <a href="../solutions-vector-spaces/#sol-ex-poly-span-2" data-reference-type="ref+Label" data-reference="sol--ex poly span 2">Solution 3.10.11</a>.) Is the following sentence correct? “In ${\bf R}[x]^{\le 3}$, the polynomial $f(x) = \frac 1 4 x^3 + 3x +1$ is a linear combination of the polynomials $x^2$, $x$ and $1$ since $f(x) = \frac x 4 \cdot x^2 + 3 \cdot x + 1$.”

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.12</strong></p>

<span id="base-change-matrix" label="base change matrix"></span> (See <a href="../solutions-vector-spaces/#sol-base-change-matrix" data-reference-type="ref+Label" data-reference="sol--base change matrix">Solution 3.10.12</a>.) Express each of the three standard basis vectors $e_1, e_2, e_3$ as a linear combination of the basis vectors in <a href="../spaces-bases/#ex-three-vectors-basis" data-reference-type="ref+Label" data-reference="ex:three-vectors-basis">Example 3.63</a>.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.13</strong></p>

<span id="ex-spaces-2-1" label="ex:spaces-2-1"></span> (See <a href="../solutions-vector-spaces/#sol-ex-spaces-2-1" data-reference-type="ref+Label" data-reference="sol--ex:spaces-2-1">Solution 3.10.13</a>.) Consider $A = \left ( \begin{array}{cc} 1 & 1 \\ 2 & 2 \end{array} \right )$ and $B = \left ( \begin{array}{cc} 3 & 2 \\ 3 & 5 \end{array} \right )$ in the vector space of $2 \times 2$-matrices. Is $C = \left ( \begin{array}{cc} -1 & 0 \\ 2 & 4 \end{array} \right )$ a linear combination of $A$ and $B$?

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.14</strong></p>

<span id="ex-matrix-subspace" label="ex:matrix-subspace"></span> (See <a href="../solutions-vector-spaces/#sol-ex-matrix-subspace" data-reference-type="ref+Label" data-reference="sol--ex:matrix-subspace">Solution 3.10.14</a>.) In the vector space ${\mathrm {Mat}}_{2 \times 3}$ of $2 \times 3$-matrices, we consider the set
<div class="arithmatex" markdown="1">
\[
T = \left \{ \left ( \begin{array}{ccc} x_1 & x_2 & x_3 \\ x_4 & x_5 & x_6 \end{array} \right ) \ | \ x_1 + x_4 + x_6 = 0, x_1 + x_4 + x_3 + x_5 = 0 \right \}.
\]
</div>

1.  Decide whether $T$ is a subspace of ${\mathrm {Mat}}_{2 \times 3}$.

2.  Find all the vectors (i.e., matrices) in $T$.

3.  Find some vectors such that $T = L(v_1, v_2, v_3, v_4)$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.15</strong></p>

<span id="ex-spaces-2-2" label="ex:spaces-2-2"></span> (See <a href="../solutions-vector-spaces/#sol-ex-spaces-2-2" data-reference-type="ref+Label" data-reference="sol--ex:spaces-2-2">Solution 3.10.15</a>.) In ${\bf R}^4$ consider the subset
<div class="arithmatex" markdown="1">
\[
S = \{(x,y,z,t) \ | \ x+y+z+t = 0 \}.
\]
</div>

1.  Decide whether $S$ is a subspace of ${\bf R}^4$.

2.  Find all the vectors in $S$.

3.  Find some vectors such that $S = L(v_1, v_2, v_3)$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.16</strong></p>

<span id="ex-spaces-2-3" label="ex:spaces-2-3"></span> (See <a href="../solutions-vector-spaces/#sol-ex-spaces-2-3" data-reference-type="ref+Label" data-reference="sol--ex:spaces-2-3">Solution 3.10.16</a>.) Consider the following two subspaces of ${\bf R}^4$:
<div class="arithmatex" markdown="1">
\[
S = L((1,-1,0,1), (2,1,-2,0),(0,0,1,1))
\]
</div>
and $T$, which is the solution set of the system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
2x_1-x_2-3x_4 & = 0 \\
2x_1 + x_3 + x_4 & = 0.
\end{align*}
\]
</div>
Determine $S \cap T$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.17</strong></p>

<span id="ex-intersection-tw" label="ex:intersection-tw"></span> (See <a href="../solutions-vector-spaces/#sol-ex-intersection-tw" data-reference-type="ref+Label" data-reference="sol--ex:intersection-tw">Solution 3.10.17</a>.) Consider the following two subspaces of ${\bf R}^4$:
<div class="arithmatex" markdown="1">
\[
W = L((1,0,1,0), (2,0,0,0), (0,-3,-1,-1))
\]
</div>
and $T$ given by the solution set of the system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x_1-x_2 & = 0 \\
x_1+x_2+x_3&= 0.
\end{align*}
\]
</div>
Determine $T \cap W$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.18</strong></p>

<span id="ex-r2-spanning" label="ex:r2-spanning"></span> (See <a href="../solutions-vector-spaces/#sol-ex-r2-spanning" data-reference-type="ref+Label" data-reference="sol--ex:r2-spanning">Solution 3.10.18</a>.) Show that

- ${\bf R}^2 = L((1,1), (2,-1))$,

- ${\bf R}^2 = L((0,-2), (1,1))$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.19</strong></p>

<span id="ex-linear-combination-r3" label="ex:linear-combination-r3"></span> (See <a href="../solutions-vector-spaces/#sol-ex-linear-combination-r3" data-reference-type="ref+Label" data-reference="sol--ex:linear-combination-r3">Solution 3.10.19</a>.) Is $(1,5,0) \in {\bf R}^3$ a linear combination of $v_1 = (1,1,0)$, $v_2 = (2,0,1)$ and $v_3 = (0,3,-1)$?

(I.e., are there $a_1, a_2, a_3 \in {\bf R}$ such that $\alpha_1 v_1 + a_2 v_2 + a_3 v_3 = (1,5,0)$?)

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.20</strong></p>

<span id="ex-polynomial-basis-change" label="ex:polynomial-basis-change"></span> (See <a href="../solutions-vector-spaces/#sol-ex-polynomial-basis-change" data-reference-type="ref+Label" data-reference="sol--ex:polynomial-basis-change">Solution 3.10.20</a>.) Express the following polynomials as $f(x) = \sum_{i=0}^4 a_i (x-1)^i$:

1.  $f(x) = x^4$,

2.  $f(x) = x^3$,

3.  $f(x) = x^3 - 3x^2 + 4x+2$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.21</strong></p>

<span id="ex-polynomial-basis-ab" label="ex:polynomial-basis-ab"></span> (See <a href="../solutions-vector-spaces/#sol-ex-polynomial-basis-ab" data-reference-type="ref+Label" data-reference="sol--ex:polynomial-basis-ab">Solution 3.10.21</a>.) Let $a, b \in {\bf R}$ be two *distinct* numbers. Show that the polynomials $x-a$ and $x-b$ are a basis of ${\bf R}[x]^{\le 1}$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.22</strong></p>

<span id="ex-basis-w1-r4" label="ex:basis-w1-r4"></span> (See <a href="../solutions-vector-spaces/#sol-ex-basis-w1-r4" data-reference-type="ref+Label" data-reference="sol--ex:basis-w1-r4">Solution 3.10.22</a>.) In ${\bf R}^4 = \{(x,y,z,t) \ | \ x,y,z,t \in {\bf R} \}$ consider the subspace $W_1 \subset {\bf R}^4$ given by the solutions of the system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
y+t&=0, \\
y+z&=0.
\end{align*}
\]
</div>
Also consider the subspace $W_2 = L((0,1,-1,0))$.

Determine a basis and the dimension of $W_1$. Describe $W_1 \cap W_2$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.23</strong></p>

<span id="ex-wk-basis" label="ex:wk-basis"></span> (See <a href="../solutions-vector-spaces/#sol-ex-wk-basis" data-reference-type="ref+Label" data-reference="sol--ex:wk-basis">Solution 3.10.23</a>.) Let $k \in {\bf R}$ be an arbitrary real number. Consider the subspace
<div class="arithmatex" markdown="1">
\[
W_k := L((1,0,-1,0), (1,1,0,1), (1,2,k,1)) \subset {\bf R}^4.
\]
</div>

1.  For all $k \in {\bf R}$, find a basis of $W_k$ and determine $\dim W_k$.

2.  For which $k \in {\bf R}$ is $(-1,1,1,1) \in W_k$?

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.24</strong></p>

<span id="ex-mat-subspace-dim" label="ex:mat-subspace-dim"></span> (See <a href="../solutions-vector-spaces/#sol-ex-mat-subspace-dim" data-reference-type="ref+Label" data-reference="sol--ex:mat-subspace-dim">Solution 3.10.24</a>.) Recall that the dimension of the space ${\mathrm {Mat}}_{2 \times 3}$ of $2 \times 3$-matrices is 6.

1.  Consider $W = \left \{ \left ( \begin{array}{ccc} a & a+b & b \\ 0 & 0 & b \end{array} \right ) \ | \ a, b \in {\bf R} \right \}$. Confirm that $W$ is a subspace of ${\mathrm {Mat}}_{2 \times 3}$. Determine $\dim W$.

2.  Let $V := \left \{ \left ( \begin{array}{ccc} c & 0 & -c \\ 0 & 0 & -c \end{array} \right ) \ | \ c \in {\bf R} \right \}$. Determine (i.e., determine a basis and the dimension of) $V \cap W$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.25</strong></p>

<span id="ex-spaces-2-4" label="ex:spaces-2-4"></span> (See <a href="../solutions-vector-spaces/#sol-ex-spaces-2-4" data-reference-type="ref+Label" data-reference="sol--ex:spaces-2-4">Solution 3.10.25</a>.) Consider the following subspaces of ${\bf R}^3$:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
W_1 & := L((1,0,1), (2,1,0)) \\
W_2 & := L((-1,1,1), (0,3,0)).
\end{align*}
\]
</div>

1.  Determine (i.e., determine a basis and the dimension of) $W_1 \cap W_2$.

2.  Determine $W_1 + W_2$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.26</strong></p>

<span id="ex-sum-intersection-r4" label="ex:sum-intersection-r4"></span> (See <a href="../solutions-vector-spaces/#sol-ex-sum-intersection-r4" data-reference-type="ref+Label" data-reference="sol--ex:sum-intersection-r4">Solution 3.10.26</a>.) Consider the following subspaces of ${\bf R}^4$:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
W_1 & := L((1,1,1,2), (2,0,3,5)) \\
W_2 & := L((1,1,0,1),(0,2,-2,-2)).
\end{align*}
\]
</div>
As in the previous exercise, determine $W_1 \cap W_2$ and $W_1 + W_2$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.27</strong></p>

<span id="ex-spaces-2-5" label="ex:spaces-2-5"></span> (See <a href="../solutions-vector-spaces/#sol-ex-spaces-2-5" data-reference-type="ref+Label" data-reference="sol--ex:spaces-2-5">Solution 3.10.27</a>.) Consider the subspace
<div class="arithmatex" markdown="1">
\[
W = L(\underbrace{(1,0,1,0)}_{=v_1}, \underbrace{(2,0,1,1)}_{=v_2}, \underbrace{(0,0,1,3)}_{=v_3}).
\]
</div>

1.  Find a basis of $W$ and determine $\dim W$.

2.  Find a vector $v \in {\bf R}^4$ such that
<div class="arithmatex" markdown="1">
\[
    W \subsetneq L(v_1, v_2, v_3, v).
\]
</div>
What is $\dim L(v_1, v_2, v_3, v)$?

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.28</strong></p>

<span id="ex-spaces-2-6" label="ex:spaces-2-6"></span> (See <a href="../solutions-vector-spaces/#sol-ex-spaces-2-6" data-reference-type="ref+Label" data-reference="sol--ex:spaces-2-6">Solution 3.10.28</a>.) Consider the vectors in ${\bf R}^4$, where $t \in {\bf R}$:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
u_1 &= (1,0,-1,2) \\
u_2 &=(1,0,0,1) \\
u_3&=(2,0,-1,3)\\
u_4&=(4,t,-2,6).
\end{align*}
\]
</div>

1.  Let $U_t = L(u_1, u_2, u_3, u_4)$ be the subspace spanned by these vectors (where the last vector depends on $t \in {\bf R}$). Find the values of $t$ such that
<div class="arithmatex" markdown="1">
\[
    \dim U_t = 2.
\]
</div>

2.  Consider $t = 1$ from now on. Verify $\dim U_1 = 3$ and find a basis of $U_1$.

3.  Let $W \subset {\bf R}^4$ be the subspace given by the equations
<div class="arithmatex" markdown="1">
\[
    \begin{align*}
    x_1+x_2+x_3 &= 0 \\ x_1 - 3x_4 &= 0.
    \end{align*}
\]
</div>
Determine $\dim W$ and $\dim U_1 \cap W$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 3.29</strong></p>

<span id="ex-ut-basis-r4" label="ex:ut-basis-r4"></span> (See <a href="../solutions-vector-spaces/#sol-ex-ut-basis-r4" data-reference-type="ref+Label" data-reference="sol--ex:ut-basis-r4">Solution 3.10.29</a>.) Consider the subspace $U_t \subset {\bf R}^4$ spanned by the four vectors
<div class="arithmatex" markdown="1">
\[
\begin{align*}
v_1 & = (1,0, 0, 1) \\
v_2 &= (-1,1,2,3) \\
v_3 &=(0,1,2,4) \\
v_4 &=(t,2,4,8).
\end{align*}
\]
</div>
Here, $t \in {\bf R}$ is an arbitrary real number.

1.  Find the values of $t$, such that $\dim U_t = 2$.

2.  Consider from now on $t = 1$. Determine $\dim U_1$.

3.  Let $W \subset {\bf R}^4$ be the subspace given by the equations
<div class="arithmatex" markdown="1">
\[
    \begin{align*}
    x_1 - x_2 & =0\\ x_2 - x_3 & = 0.
    \end{align*}
\]
</div>
Determine a basis and the dimension of $W$ and of $W \cap U_1$.

</div>
