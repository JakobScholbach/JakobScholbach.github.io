---
title: Summary
---

# Summary of some computational methods

<div class="task" markdown="1">


<p class="env-number"><strong>Task 7.61</strong> (Related exercises: <a href="../exercises-euclid/#ex-euclid-6-13">Exercise 7.17</a>, <a href="../exercises-euclid/#ex-euclid-6-20">Exercise 7.24</a>, <a href="../exercises-euclid/#ex-euclid-6-22">Exercise 7.26</a>, <a href="../exercises-euclid/#ex-euclid-polynomials-gs">Exercise 7.1</a>, <a href="../exercises-euclid/#ex-euclid-u-r4-orth">Exercise 7.16</a>)</p>

<span id="tas-compute-orthonormal-basis" label="tas:compute-orthonormal-basis"></span> Compute an orthonormal basis of a subspace $U \subset {\bf R}^n$.

*Method:* First compute any (not necessarily orthonormal) basis of $U$. Then orthonormalize that basis using the Gram–Schmidt algorithm (<a href="../euclid-euclidean-spaces/#prop-gram-schmidt-orthogonalization" data-reference-type="ref+Label" data-reference="prop:gram-schmidt-orthogonalization">Proposition 7.32</a>).

</div>

<div class="task" markdown="1">


<p class="env-number"><strong>Task 7.62</strong> (Related exercises: <a href="../exercises-euclid/#ex-euclid-6-1">Exercise 7.2</a>, <a href="../exercises-euclid/#ex-euclid-6-13">Exercise 7.17</a>, <a href="../exercises-euclid/#ex-euclid-6-2">Exercise 7.4</a>, <a href="../exercises-euclid/#ex-euclid-6-6">Exercise 7.7</a>, <a href="../exercises-euclid/#ex-euclid-r4-projection">Exercise 7.3</a>, <a href="../exercises-euclid/#ex-euclid-u-r4-orth">Exercise 7.16</a>)</p>

<span id="tas-compute-orthogonal-projection" label="tas:compute-orthogonal-projection"></span> Given $x \in {\bf R}^n$ and a subspace $U \subset {\bf R}^n$, compute the orthogonal projection $p_U(x)$.

*Method:* Compute an orthonormal basis $u_1, \dots, u_k$ of $U$ (cf. <a href="#tas-compute-orthonormal-basis" data-reference-type="ref+Label" data-reference="tas:compute-orthonormal-basis">Task 7.61</a>), then use
<div class="arithmatex" markdown="1">
\[
p_U(x) = \sum_{i=1}^k {\left \langle x, u_i \right \rangle} u_i.
\]
</div>

One may also compute $U^\bot$ (cf. <a href="#tas-compute-orthogonal-complement" data-reference-type="ref+Label" data-reference="tas:compute-orthogonal-complement">Task 7.63</a>), then compute $p_{U^\bot}(x)$, and finally $p_U(x) = x-p_{U^\bot}(x)$. This may be easier in practice, especially if $\dim U > \dim U^\bot$.

</div>

<div class="task" markdown="1">


<p class="env-number"><strong>Task 7.63</strong> (Related exercises: <a href="../exercises-euclid/#ex-euclid-6-1">Exercise 7.2</a>, <a href="../exercises-euclid/#ex-euclid-6-13">Exercise 7.17</a>, <a href="../exercises-euclid/#ex-euclid-6-2">Exercise 7.4</a>, <a href="../exercises-euclid/#ex-euclid-6-20">Exercise 7.24</a>, <a href="../exercises-euclid/#ex-euclid-6-22">Exercise 7.26</a>, <a href="../exercises-euclid/#ex-euclid-6-3">Exercise 7.5</a>, <a href="../exercises-euclid/#ex-euclid-r4-projection">Exercise 7.3</a>, <a href="../exercises-euclid/#ex-euclid-u-r4-orth">Exercise 7.16</a>)</p>

<span id="tas-compute-orthogonal-complement" label="tas:compute-orthogonal-complement"></span> Compute the orthogonal complement $U^\bot$ of a given a subspace $U \subset {\bf R}^n$.

*Method:* Compute a basis $u_1, \dots, u_k$ of $U$. Then solve the homogeneous system
<div class="arithmatex" markdown="1">
\[
{\left \langle x, u_1 \right \rangle} = 0, \dots, {\left \langle x, u_k \right \rangle} = 0.
\]
</div>
Equivalently, form the matrix
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{c} u_1 \\ \dots \\ u_k \end{array} \right )
\]
</div>
(whose rows are the basis vectors $u_1$ etc.), and compute its kernel.

</div>

The next two tasks are related to the different representations of lines.

<div class="task" markdown="1">


<p class="env-number"><strong>Task 7.64</strong> (Related exercises: <a href="../exercises-euclid/#ex-euclid-lines-plane">Exercise 7.14</a>)</p>

<span id="tas-line-cartesian-to-parametric" label="tas:line-cartesian-to-parametric"></span> Convert a line $L$ from cartesian equations (as in <a href="../euclid-affine-subspaces/#def-cartesian-equation-line" data-reference-type="ref+Label" data-reference="def:cartesian-equation-line">Definition 7.53</a>) to a vector/parametric equation (as in <a href="../euclid-affine-subspaces/#def-parametric-equation-line" data-reference-type="ref+Label" data-reference="def:parametric-equation-line">Definition 7.50</a>).

*Method:* Pick two distinct points $p, q$ satisfying the cartesian equations. Then write
<div class="arithmatex" markdown="1">
\[
L = p + L(p-q).
\]
</div>
Choosing different points instead of $p, q$ will give different vector equations; but if $L = p' + L(p'-q')$, the two vectors $p-q$ and $p'-q'$ will necessarily be (non-zero) multiples of each other (by <a href="../euclid-affine-subspaces/#lem-base-affine-subspace" data-reference-type="ref+Label" data-reference="lem:base-affine-subspace">Lemma 7.41</a>).

</div>

<div class="task" markdown="1">


<p class="env-number"><strong>Task 7.65</strong></p>

<span id="tas-line-parametric-to-cartesian" label="tas:line-parametric-to-cartesian"></span> Convert a line from vector equation form (<a href="../euclid-affine-subspaces/#def-parametric-equation-line" data-reference-type="ref+Label" data-reference="def:parametric-equation-line">Definition 7.50</a>) $L = v+L(w)$ into cartesian equations.

*Method:* Express one coordinate in terms of the free parameter and substitute into the other coordinate equations.

</div>

<div class="task" markdown="1">


<p class="env-number"><strong>Task 7.66</strong> (Related exercises: <a href="../exercises-euclid/#ex-euclid-6-15">Exercise 7.19</a>, <a href="../exercises-euclid/#ex-euclid-6-23">Exercise 7.27</a>)</p>

<span id="tas-plane-through-three-points" label="tas:plane-through-three-points"></span> Compute a cartesian equation for the plane $P$ containing three non-collinear points $p, q, r \in {\bf R}^3$.

*Method:* First write
<div class="arithmatex" markdown="1">
\[
P = p + L(q-p, r-p).
\]
</div>
Then compute a normal vector to $L(q-p, r-p)$ and write the corresponding cartesian equation. As in <a href="#tas-line-cartesian-to-parametric" data-reference-type="ref+Label" data-reference="tas:line-cartesian-to-parametric">Task 7.64</a>, different choices of $p, q, r$ may give different intermediate vectors, but they span the same underlying subspace.

</div>

<div class="task" markdown="1">


<p class="env-number"><strong>Task 7.67</strong> (Related exercises: <a href="../exercises-euclid/#ex-euclid-6-21">Exercise 7.25</a>, <a href="../exercises-euclid/#ex-euclid-lines-plane">Exercise 7.14</a>)</p>

<span id="tas-plane-through-line-and-point" label="tas:plane-through-line-and-point"></span> Given a line $L$ and a point $r \notin L$, find the plane $P$ containing $L$ and $r$.

*Method:* Choose two distinct points $p, q \in L$, then apply <a href="#tas-plane-through-three-points" data-reference-type="ref+Label" data-reference="tas:plane-through-three-points">Task 7.66</a> to the three points $p, q, r$.

</div>

<div class="task" markdown="1">


<p class="env-number"><strong>Task 7.68</strong> (Related exercises: <a href="../exercises-euclid/#ex-euclid-6-18">Exercise 7.22</a>, <a href="../exercises-euclid/#ex-euclid-6-21">Exercise 7.25</a>, <a href="../exercises-euclid/#ex-euclid-6-23">Exercise 7.27</a>)</p>

<span id="tas-line-in-plane-orthogonal-to-line" label="tas:line-in-plane-orthogonal-to-line"></span> Given a plane $P = \{x \mid {\left \langle x, a \right \rangle} = d \}$, a line $L = v + L(w) \subset P$, and a point $p \in P$, find the line $M \subset P$ through $p$ orthogonal to $L$.

*Method:* Write $M = p + L(w')$. Determine $w'$ by imposing $w' \bot a$ and $w' \bot w$, i.e., compute
<div class="arithmatex" markdown="1">
\[
w' \in (L(a,w))^\bot
\]
</div>
as in <a href="#tas-compute-orthogonal-complement" data-reference-type="ref+Label" data-reference="tas:compute-orthogonal-complement">Task 7.63</a>.

</div>

<div class="task" markdown="1">


<p class="env-number"><strong>Task 7.69</strong> (Related exercises: <a href="../exercises-euclid/#ex-euclid-6-15">Exercise 7.19</a>, <a href="../exercises-euclid/#ex-euclid-lines-plane">Exercise 7.14</a>)</p>

<span id="tas-plane-vector-to-cartesian" label="tas:plane-vector-to-cartesian"></span> Given a plane in vector form $P = v + L(w_1, w_2)$, compute a cartesian equation
<div class="arithmatex" markdown="1">
\[
P = \{x \in {\bf R}^3 \mid {\left \langle x, a \right \rangle} = d \}.
\]
</div>

*Method:* Compute $W=L(w_1,w_2)$ and then $W^\bot$. Choose any non-zero $a \in W^\bot$, and set
<div class="arithmatex" markdown="1">
\[
d={\left \langle a, v \right \rangle}.
\]
</div>
Note: a presentation of $P$ as above is not unique, but another presentation as $P = \{x \in {\bf R}^3 | {\left \langle x, a' \right \rangle} = d'\}$ will be such that $a = \lambda a'$ for some $\lambda \in {\bf R}, \lambda \ne 0$, and $d = \lambda d'$.

</div>

<div class="task" markdown="1">


<p class="env-number"><strong>Task 7.70</strong> (Related exercises: <a href="../exercises-euclid/#ex-euclid-6-21">Exercise 7.25</a>, <a href="../exercises-euclid/#ex-euclid-6-7">Exercise 7.8</a>)</p>

<span id="tas-check-lines-parallel" label="tas:check-lines-parallel"></span> Decide whether two lines are parallel.

*Method:* If the lines are in parametric form ($L = v+L(w)$ and $L' = v'+L(w')$), check whether $w$ and $w'$ are linearly dependent. If the lines are given in cartesian form, first convert them via <a href="#tas-line-cartesian-to-parametric" data-reference-type="ref+Label" data-reference="tas:line-cartesian-to-parametric">Task 7.64</a>.

</div>

<div class="task" markdown="1">


<p class="env-number"><strong>Task 7.71</strong> (Related exercises: <a href="../exercises-euclid/#ex-euclid-6-14">Exercise 7.18</a>, <a href="../exercises-euclid/#ex-euclid-6-16">Exercise 7.20</a>, <a href="../exercises-euclid/#ex-euclid-6-19">Exercise 7.23</a>, <a href="../exercises-euclid/#ex-euclid-6-8">Exercise 7.9</a>)</p>

<span id="tas-check-lines-skew" label="tas:check-lines-skew"></span> Decide whether two lines $L = v+L(w)$ and $L' = v'+L(w')$ are skew.

*Method:* Verify both conditions: (a) $w$ and $w'$ are linearly independent, and (b) $L \cap L' = \emptyset$. For condition (b), it is often convenient to use cartesian equations first (cf. <a href="#tas-line-parametric-to-cartesian" data-reference-type="ref+Label" data-reference="tas:line-parametric-to-cartesian">Task 7.65</a>).

</div>

<div class="task" markdown="1">


<p class="env-number"><strong>Task 7.72</strong> (Related exercises: <a href="../exercises-euclid/#ex-euclid-6-12">Exercise 7.13</a>, <a href="../exercises-euclid/#ex-euclid-6-14">Exercise 7.18</a>, <a href="../exercises-euclid/#ex-euclid-6-19">Exercise 7.23</a>, <a href="../exercises-euclid/#ex-euclid-6-23">Exercise 7.27</a>, <a href="../exercises-euclid/#ex-euclid-6-9">Exercise 7.10</a>)</p>

<span id="tas-check-line-parallel-plane" label="tas:check-line-parallel-plane"></span> Decide whether a line $L = v+L(w)$ is parallel to a plane $P$.

*Method:* If $P = v' + L(w'_1,w'_2)$, check whether $w$ is a linear combination of $w'_1,w'_2$ (equivalently, $W \subset W'$). If $P = \{x \mid {\left \langle x, a \right \rangle}=d\}$, check whether ${\left \langle w,a \right \rangle}=0$.

</div>

<div class="task" markdown="1">


<p class="env-number"><strong>Task 7.73</strong></p>

<span id="tas-check-line-orthogonal-plane" label="tas:check-line-orthogonal-plane"></span> Decide whether a line $L = v+L(w)$ is orthogonal to a plane $P$.

*Method:* If $P = \{x \mid {\left \langle x, a \right \rangle}=d\}$, check whether $w$ and $a$ are linearly dependent. If $P = v'+L(w'_1,w'_2)$, check whether ${\left \langle w,w'_1 \right \rangle}=0$ and ${\left \langle w,w'_2 \right \rangle}=0$.

</div>

<div class="task" markdown="1">


<p class="env-number"><strong>Task 7.74</strong> (Related exercises: <a href="../exercises-euclid/#ex-euclid-6-12">Exercise 7.13</a>, <a href="../exercises-euclid/#ex-euclid-6-19">Exercise 7.23</a>, <a href="../exercises-euclid/#ex-euclid-6-7">Exercise 7.8</a>, <a href="../exercises-euclid/#ex-euclid-6-8">Exercise 7.9</a>)</p>

<span id="tas-compute-distance-affine-subspaces" label="tas:compute-distance-affine-subspaces"></span> Compute the distance of two affine subspaces $X = v + W$ and $X' = v' + W'$ (including the point case $W=\{0\}$).

*Method:* Use one of the following equivalent approaches:

- apply <a href="../euclid-distances/#thm-distance-affine-subspaces" data-reference-type="ref+Label" data-reference="thm:distance-affine-subspaces">Theorem 7.59</a> via part <a href="../euclid-distances/#item-min-e" data-reference-type="ref" data-reference="item--min.e">1.</a>: compute $Z = W+W'$, $d := v-v'$, and compute the orthogonal projection $m = p_{Z^\bot}(d)$, or equivalently $m = d-p_Z(d)$ (cf. <a href="#tas-compute-orthogonal-projection" data-reference-type="ref+Label" data-reference="tas:compute-orthogonal-projection">Task 7.62</a>). Let $x$ be a general point in $X$, $x'$ a general point in $X'$, and solve the linear system $x-x'=m$, – or –,

- apply <a href="../euclid-distances/#thm-distance-affine-subspaces" data-reference-type="ref+Label" data-reference="thm:distance-affine-subspaces">Theorem 7.59</a> via part <a href="../euclid-distances/#item-min-c" data-reference-type="ref" data-reference="item--min.c">4.</a>: again let $x$ be a general point in $X$, $x'$ a general point in $X'$, compute $x-x'$ and solve the homogeneous linear system given by ${\left \langle x, w \right \rangle} = 0$ and ${\left \langle x, w' \right \rangle} = 0$, where $w$ runs through a set of vectors spanning $W$, and $w'$ runs through a set of vectors spanning $W'$.

</div>
