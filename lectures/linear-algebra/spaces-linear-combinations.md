---
title: Linear Combinations
---

# Linear combinations

In the sequel, $V$ will always denote a vector space, for example $V = {\bf R}^n$.

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 3.31</strong> (Related exercises: <a href="../exercises-spaces/#base-change-matrix">Exercise 3.12</a>, <a href="../exercises-spaces/#ex-poly-span-1">Exercise 3.10</a>, <a href="../exercises-spaces/#ex-poly-span-2">Exercise 3.11</a>, <a href="../exercises-spaces/#ex-linear-combination-r3">Exercise 3.19</a>)</p>

<span id="def-spaces-definition-008" label="def:spaces-definition-008"></span> A *linear combination* of vectors $v_1, \dots, v_m \in V$ is a vector of the form
<div class="arithmatex" markdown="1">
\[
a_1 v_1 + \dots + a_m v_m,
\]
</div>
where the $a_1, \dots, a_m$ are arbitrary real numbers.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 3.32</strong></p>

<span id="ex-spaces-example-010" label="ex:spaces-example-010"></span> If $m = 1$ in the above definition, there is only one vector $v := v_1$. A linear combination of a single vector $v$ is therefore any vector of the form $a v$, with an arbitrary $a \in {\bf R}$. In other words it is an arbitrary scalar multiple of that vector.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 3.33</strong></p>

<span id="ex-span-2" label="ex:span-2"></span> More interesting things start happening for two vectors and more. As an example, consider $v_1 = (1, 0, 0)$ and $v_2 = (0, 1, 0)$ in the vector space ${\bf R}^3$. Then $(3, 2, 0)$ is a linear combination of these since
<div class="arithmatex" markdown="1">
\[
(3, 2, 0) = 3 \cdot (1,0,0) + 2 \cdot (0, 1, 0).
\]
</div>
On the other hand, $(0, 0, 1)$ is *not* a linear combination of $v_1$ and $v_2$: for arbitrary $a_1, a_2 \in {\bf R}$, we compute
<div class="arithmatex" markdown="1">
\[
a_1 v_1 + a_2 v_2 = (a_1, 0,0) + (0, a_2, 0) = (a_1, a_2, 0).
\]
</div>
No matter how we choose $a_1$ and $a_2$, we always have
<div class="arithmatex" markdown="1">
\[
(a_1, a_2, 0) \ne (0, 0, 1),
\]
</div>
since the third components of these two vectors are always different. In fact, the linear combinations of $v_1$ and $v_2$ are *precisely* the vectors $(x, y, z)$ that satisfy $z = 0$.

<div class="center" markdown="1">

![image](figures/png/spaces/spaces-fig-09.png)

</div>

</div>

Given two vectors $v_1, v_2 \in {\bf R}^3$, we will see later (<a href="../spaces-dimension/#thm-basis-theorem" data-reference-type="ref+Label" data-reference="thm:basis-theorem">Theorem 3.71</a>) that there will always be some vector $w \in {\bf R}^3$ (in fact infinitely many) that is *not* a linear combination of $v_1$ and $v_2$. In the above example any vector $w = (x,y,z)$ with $z \ne 0$ has that property. Continuing with that example, the $x-y$-plane inside ${\bf R}^3$, i.e., $V := \{(x,y,z) \ | \ x, y \in {\bf R}, z = 0\} = \{(x,y,0) \ | \ x, y \in {\bf R} \}$ is a subspace of ${\bf R}^3$: it contains $(0,0,0)$ and given any two vectors $v, w \in V$ we have $v+w \in V$ and given $r \in {\bf R}$, $r v \in V$ (convince yourself this is true!). We can alternatively use <a href="../spaces-definition-solution-of-homogeneous/#prop-homogeneous-system-subspace" data-reference-type="ref+Label" data-reference="prop:homogeneous-system-subspace">Proposition 3.18</a> to see this is a subspace: $V$ is the solution space of the equation $z = 0$ (in the three variables $x, y, z$), which is a homogeneous linear equation. The following statement asserts that we always obtain a subspace in this manner.

<div class="lemma" markdown="1">


<p class="env-number"><strong>Lemma 3.34</strong> (Related exercises: <a href="../exercises-maps/#ex-maps-partial-2026-1">Exercise 4.46</a>, <a href="../exercises-spaces/#ex-matrix-subspace">Exercise 3.14</a>, <a href="../exercises-spaces/#ex-polynomial-subspaces">Exercise 3.9</a>, <a href="../exercises-spaces/#ex-spaces-2-3">Exercise 3.16</a>, <a href="../exercises-spaces/#ex-span-r4">Exercise 3.5</a>)</p>

<span id="lem-span-subspace" label="lem:span-subspace"></span> Let $V$ be a vector space and $v_1, \dots, v_m \in V$ be any vectors. The set
<div class="arithmatex" markdown="1">
\[
L(v_1, \dots, v_m) := \{ a_1 v_1 + \dots + a_m v_m \ | \ a_1, \dots, a_m \in {\bf R}\}
\]
</div>
of *all* linear combinations of $v_1, \dots, v_m$ is a subspace of $V$. It is called the *span* (or sometimes also the *linear hull*) of these vectors.

</div>

<div class="proof" markdown="1">

*Proof.* We check the three conditions in <a href="../spaces-definition-solution-of-homogeneous/#def-subspace" data-reference-type="ref+Label" data-reference="def:subspace">Definition 3.17</a>. Let us abbreviate $L := L(v_1, \dots, v_m)$.

1.  The zero vector $0 \in L$ since $0 \cdot v_1 + \dots 0 \cdot v_m = 0 \cdot (v_1 + \dots + v_m) = 0$, using properties <a href="../spaces-definition-solution-of-homogeneous/#item-distributive-law" data-reference-type="ref" data-reference="item--distributive law">4.</a> and <a href="../spaces-definition-solution-of-homogeneous/#item-product-0" data-reference-type="ref" data-reference="item--product 0">8.</a> in the definitions of a vector space.

2.  Given two vectors $w, u \in L$, we check $w+u \in L$. Since $w \in L$ there are some real numbers $a_1, \dots, a_m$ such that $w = a_1 v_1 + \dots + a_m v_m = \sum_{i=1}^m a_i v_i$. Likewise there are real numbers $b_1, \dots, b_m$ with $u = \sum_{i=1}^m b_i v_i$. This implies
<div class="arithmatex" markdown="1">
\[
    \begin{align*}
    w+u & = \sum_{i=1}^m a_i v_i + \sum_{i=1}^m b_i v_i \\
     & = \sum_{i=1}^m (a_i + b_i) v_i \\ 
     & \in L.
    \end{align*}
\]
</div>

3.  Given $w \in L$ and $r \in {\bf R}$, one checks similarly that $rw \in L$ (, verify that!).

 ◻

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 3.35</strong></p>

<span id="ex-spaces-example-012" label="ex:spaces-example-012"></span> In <a href="#ex-span-2" data-reference-type="ref+Label" data-reference="ex:span-2">Example 3.33</a>, we have
<div class="arithmatex" markdown="1">
\[
L((1,0,0), (0,1,0)) = \{(x,y,0) \ | \ x, y, \in {\bf R} \}.
\]
</div>

</div>

<a href="../exercises-spaces/#ex-poly-span-1" data-reference-type="ref+Label" data-reference="ex poly span 1">Exercise 3.10</a> and <a href="../exercises-spaces/#ex-poly-span-2" data-reference-type="ref+Label" data-reference="ex poly span 2">Exercise 3.11</a> discuss linear combinations in the vector space ${\bf R}[x]^{\le 3}$. The span is closely related to another construction that produces new vector spaces out of given ones:

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 3.36</strong> (Related exercises: <a href="../exercises-spaces/#ex-spaces-2-4">Exercise 3.25</a>, <a href="../exercises-spaces/#ex-sum-intersection-r4">Exercise 3.26</a>)</p>

<span id="def-sum-of-vector-spaces" label="def:sum-of-vector-spaces"></span> Let $V$ be a vector space and $A, B \subset V$ be two subspaces. The *sum* of $A$ and $B$ is defined as
<div class="arithmatex" markdown="1">
\[
A + B := \{ v+ w \ | \ v \in A, w \in B \}.
\]
</div>
I.e., it consists of *all* possible ways to sum an element in $A$ and an element in $B$. More generally, given subspaces $A_1, \dots, A_n$ of $V$, their sum is defined as
<div class="arithmatex" markdown="1">
\[
A_1 + \dots + A_n := \{ v_1 + \dots + v_n \ | v_1 \in A_1, \dots, v_n \in A_n \}.
\]
</div>

</div>

<div class="lemma" markdown="1">


<p class="env-number"><strong>Lemma 3.37</strong></p>

<span id="lem-spaces-lemma-005" label="lem:spaces-lemma-005"></span> The sum $A+B$ is then again a subspace of $V$.

</div>

The proof of this is very similar to the one of <a href="#lem-span-subspace" data-reference-type="ref+Label" data-reference="lem:span-subspace">Lemma 3.34</a> and will be omitted.

<div class="remark" markdown="1">


<p class="env-number"><strong>Remark 3.38</strong></p>

<span id="rem-spaces-remark-005" label="rem:spaces-remark-005"></span> Given some vectors $v_1, \dots, v_n \in V$, we have
<div class="arithmatex" markdown="1">
\[
L(v_1, \dots, v_n) = L(v_1) + \dots + L(v_n).
\]
</div>
Indeed, both sets are precisely the vectors of the form $a_1 v_1 + \dots + a_n v_n$ for arbitrary $a_i \in {\bf R}$.

</div>

<div class="remark" markdown="1">


<p class="env-number"><strong>Remark 3.39</strong></p>

<span id="rem-spaces-remark-006" label="rem:spaces-remark-006"></span> The sum is *completely different* from the union $A \cup B$ of the two subspaces. We have seen in <a href="../spaces-definition-solution-of-homogeneous/#ex-non-vector-spaces" data-reference-type="ref+Label" data-reference="ex:non-vector-spaces">Example 3.13</a> that the union is (in general) not even a subspace (just a subset). We have
<div class="arithmatex" markdown="1">
\[
A \cup B \subset A + B,
\]
</div>
but these two subsets are distinct (unless $A$ or $B$ only consists of the zero vector). To see this inclusion, note that $A \subset A + B$. Indeed, the zero vector $0 \in B$ (since it is a subspace!), and for any $v \in A$, we have $v = v + 0 \in A + B$. Similarly, $B \subset A + B$, and therefore $A \cup B \subset A + B$.

</div>

<div class="remark" markdown="1">


<p class="env-number"><strong>Remark 3.40</strong></p>

<span id="rem-spaces-remark-007" label="rem:spaces-remark-007"></span> The sum $A+B$ is *different* from the direct sum $A \oplus B$. This is already clear from the definition: while the sum makes use of the ambient vector space $V$, the direct sum $A \oplus B$ is insensitive to $A$ and $B$ both lying in $V$. Also, it does not “see” to what extent $A$ and $B$ may overlap.

</div>

In a spirit similar to <a href="../spaces-intersection/#q-dimension-intersection" data-reference-type="ref+Label" data-reference="q:dimension-intersection">Question 3.21</a> we can ask the following question:

<div class="question" markdown="1">


<p class="env-number"><strong>Question 3.41</strong></p>

<span id="q-dimension-sum" label="q:dimension-sum"></span> Given two subspaces $A, B \subset V$ of some larger vector space, how much “bigger” than $A$ and $B$ is the sum $A + B$?

</div>

It turns out that <a href="../spaces-intersection/#q-dimension-intersection" data-reference-type="ref+Label" data-reference="q:dimension-intersection">Question 3.21</a> are closely related. Loosely speaking, one can say that $A + B$ “gets bigger” the same way as $A \cap B$ “gets smaller”. To give a precise meaning to this one needs the concept of the dimension of a vector space. Understanding the dimension of a vector space requires combining two preliminary notions, that of a generating system and that of linear independence below (<a href="../spaces-linear-independence/#def-linearly-independent" data-reference-type="ref+Label" data-reference="def:linearly-independent">Definition 3.49</a>).

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 3.42</strong> (Related exercises: <a href="../exercises-spaces/#ex-mat-subspace-dim">Exercise 3.24</a>, <a href="../exercises-spaces/#ex-wk-basis">Exercise 3.23</a>)</p>

<span id="def-generating-system" label="def:generating-system"></span> A collection $v_1, \dots, v_n$ of vectors is a *generating system* if
<div class="arithmatex" markdown="1">
\[
L(v_1, \dots, v_n) = V
\]
</div>
or, equivalently, if *every* vector $w \in V$ is an appropriate linear combination of these vectors. We also say that these vectors *span* $V$ if this is the case.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 3.43</strong></p>

<span id="ex-standard-basis-generate" label="ex:standard-basis-generate"></span> The vectors $e_1 := (1, 0, \dots, 0)$, $e_2 = (0, 1, 0, \dots, 0)$ up to $e_n = (0, \dots, 0, 1)$ are a generating system. Indeed, each vector $x = (x_1, \dots, x_n) \in {\bf R}^n$ is a linear combination of these, namely
<div class="arithmatex" markdown="1">
\[
x = x_1 \cdot e_1 + \dots + x_n \cdot e_n.
\]
</div>

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 3.44</strong></p>

<span id="ex-spaces-example-014" label="ex:spaces-example-014"></span> We have observed in <a href="#ex-span-2" data-reference-type="ref+Label" data-reference="ex:span-2">Example 3.33</a> that the vectors $e_1 = (1, 0, 0)$ and $e_2 = (0, 1, 0)$ in ${\bf R}^3$ are *not* a generating system since they only span the subspace
<div class="arithmatex" markdown="1">
\[
L(e_1, e_2) = \{ (x, y, 0) \ | \ x, y \in {\bf R} \}
\]
</div>
which is not the entire ${\bf R}^3$ (e.g., $(0,0,1)$ is missing).

</div>

The following example shows that three arbitrary vectors in ${\bf R}^3$ need not form a generating set.

<div class="example" markdown="1">


<p class="env-number"><strong>Example 3.45</strong></p>

<span id="ex-three-vectors-no-span" label="ex:three-vectors-no-span"></span> Consider the vectors $v_1 := e_1 = (1, 0, 0)$, $v_2 = (0, 1, 1)$ and $v_3 = (2, 1, 1)$. These three vectors do *not* form a generating set of ${\bf R}^3$. In order to show this and to also understand which vectors are precisely in the span $L(v_1, v_2, v_3)$, we consider the following equation, where $w = (x, y, z) \in {\bf R}^3$ is a vector and $a_1, a_2, a_3 \in {\bf R}$:
<div class="arithmatex" markdown="1">
\[
w = a_1 v_1 + a_2 v_2 + a_3 v_3.
\]
</div>
Those vectors $w$ that can be written in such a form are in the span, those where no such equation holds are not in the span! This is an equation between two vectors in ${\bf R}^3$, i.e., ordered triples. Two such triples are the same precisely if their three components are the same. This leads to the following linear system:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
a_1 \cdot 1 + a_2 \cdot 0 + a_3 \cdot 2 & = x, \\
a_1 \cdot 0 + a_2 \cdot 1 + a_3 \cdot 1 & = y, \\
a_1 \cdot 0 + a_2 \cdot 1 + a_3 \cdot 1 & = z.
\end{align*}
\]
</div>
In this system $a_1, a_2, a_3$ are the variables, and $x, y, z$ are parameters (on which the solutions of the system will depend). We form the matrix associated to this linear system, which is
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc|c} 1 & 0 & 2 & x \\ 0 & 1 & 1 & y \\ 0 & 1 & 1 & z \end{array} \right ).
\]
</div>
We apply Gaussian elimination to that matrix, i.e., subtract the second row from the third:
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc|c} 1 & 0 & 2 & x \\ 0 & 1 & 1 & y \\ 0 & 0 & 0 & z-y \end{array} \right ).
\]
</div>
We now distinguish two cases:

- $z-y = 0$ (i.e., $y=z$): in this case the matrix is already in reduced row echelon form (<a href="../systems-gaussian-elimination/#def-row-echelon-form" data-reference-type="ref+Label" data-reference="def:row-echelon-form">Definition 2.27</a>). The system has solutions, namely the variable $a_3$ is a free variable, so its value be chosen arbitrarily. Then $a_1$ and $a_2$ are uniquely determined by $a_3$ by the equations
<div class="arithmatex" markdown="1">
\[
  \begin{align*}
  a_1 + 2 a_3 & = x, \\
  a_2 + a_3 & = y, \\
  \end{align*}
\]
</div>
  which gives $a_1 = x - 2a_3$ and $a_2 = y - a_3$. Therefore, for arbitrary $x, y \in {\bf R}$, the vectors
<div class="arithmatex" markdown="1">
\[
  w = (x, y, y) \in L(v_1, v_2, v_3)
\]
</div>
  are in the span. They can be expressed as linear combinations
<div class="arithmatex" markdown="1">
\[
  w = (x - 2a) v_1 + (y-a) v_2 + a v_3,
\]
</div>
  for an arbitrary $a \in {\bf R}$ (this was the $a_3$ before).

- $z - y \ne 0$ (i.e., $y \ne z$). In this case, we can divide the last equation by $z-y$, which gives the following reduced row-echelon matrix
<div class="arithmatex" markdown="1">
\[
  \left ( \begin{array}{ccc|c} 1 & 0 & 2 & x \\ 0 & 1 & 1 & y \\ 0 & 0 & 0 & 1 \end{array} \right ).
\]
</div>
  According to <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>, the system has *no* solution in this case. Thus, vectors of the form
<div class="arithmatex" markdown="1">
\[
  w = (x, y, z) \ \text{ with } y \ne z
\]
</div>
  are *not* in the span: $w \notin L(v_1, v_2, v_3)$.

</div>

The following method gives a criterion to check whether a given set of vectors generates ${\bf R}^n$. We will prove this statement later (<a href="../maps-inverses/#thm-invertible-elimination" data-reference-type="ref+Label" data-reference="thm:invertible-elimination">Theorem 4.81</a>).

<div class="method" markdown="1">


<p class="env-number"><strong>Method 3.46</strong> (Related exercises: <a href="../exercises-maps/#ex-maps-3-5">Exercise 4.15</a>, <a href="../exercises-spaces/#ex-spaces-2-4">Exercise 3.25</a>)</p>

<span id="met-check-generating-system" label="met:check-generating-system"></span> Let $v_1, \dots, v_m \in {\bf R}^n$ be some vectors. Form the matrix
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{c} v_1 \\ v_2 \\ \vdots \\ v_m \end{array} \right )
\]
</div>
(i.e., each the $i$-th row of $A$ is precisely the vector $v_i$, so that $A = (v_{ij})$ if $v_i = (v_{i1}, \dots, v_{in})$.) Bring this matrix into row-echelon form by Gaussian elimination (<a href="../systems-gaussian-elimination/#met-gaussian-algorithm" data-reference-type="ref+Label" data-reference="met:gaussian-algorithm">Method 2.29</a>). Call this resulting matrix $B$. If $B$ contains $n$ leading ones, then $v_1, \dots, v_m$ span ${\bf R}^n$. Otherwise, they don’t span ${\bf R}^n$.

</div>

<div class="corollary" markdown="1">


<p class="env-number"><strong>Corollary 3.47</strong></p>

<span id="cor-spaces-corollary-001" label="cor:spaces-corollary-001"></span> Fewer than $n$ vectors can *never* span ${\bf R}^n$ (since in any event $B$ can at most contain $m$ leading ones).

</div>
