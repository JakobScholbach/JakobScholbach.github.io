---
title: Linear Maps on Basis Vectors
---

# Linear maps defined on basis vectors

An arbitrary map
<div class="arithmatex" markdown="1">
\[
f : V \to W
\]
</div>
encodes a lot of information: one needs to specify $f(v)$ for *every* $v \in V$. For *linear* maps, this simplifies drastically:

<div class="proposition" markdown="1">


<p class="env-number"><strong>Proposition 4.40</strong> (Related exercises: <a href="../exercises-eigenvalues/#ex-eigenvalues-5-5">Exercise 6.13</a>, <a href="../exercises-maps/#ex-maps-3-20">Exercise 4.44</a>, <a href="../exercises-maps/#ex-maps-exercise-014">Exercise 4.18</a>)</p>

<span id="prop-linear-map-defined-on-basis" label="prop:linear-map-defined-on-basis"></span> Let $v_1, \dots, v_n$ be a basis of a vector space $V$. Let $W$ be another vector space and $w_1, \dots, w_n$ arbitrary vectors (they need not be linearly independent, or span $W$ etc.) Then there is a *unique* linear map $f: V \to W$ such that
<div class="arithmatex" markdown="1">
\[
f(v_i) = w_i.
\]
</div>

<p class="env-number equation-number"><strong>(4.41)</strong></p>

<span id="eqn-asdjaksdjl" label="eqn--asdjaksdjl"></span>

</div>

<div class="proof" markdown="1">

*Proof.* Recall <a href="../spaces-bases/#prop-basis-coordinate-system" data-reference-type="ref+Label" data-reference="prop:basis-coordinate-system">Proposition 3.64</a>: given a basis $v_1, \dots, v_n$ of a vector space, any vector $v \in V$ can be *uniquely* expressed as a linear combination
<div class="arithmatex" markdown="1">
\[
v = b_1 v_1 + \dots + b_n b_n = \sum_{i=1}^n b_i v_i,
\]
</div>
i.e., we can express $v$ in such a form and the real numbers $b_i$ are uniquely determined by $v$. Moreover, we can think of these numbers $b_1, \dots, b_n$ as the coordinates of $v$ (with respect to our coordinate system given by the basis). Namely, given another vector $v' = \sum_{i=1}^n b'_i v_i$ and some $a \in {\bf R}$, we have
<div class="arithmatex" markdown="1">
\[
\begin{align*}
v+v' & = \sum_{i=1}^n (b_i + b'_i) v_i \\ av & = \sum_{i=1}^n (ab_i) v_i.
\end{align*}
\]
</div>
Now, given $v \in V$, we *define*
<div class="arithmatex" markdown="1">
\[
f(v) := \sum_{i=1}^n b_i w_i.
\]
</div>

<p class="env-number equation-number"><strong>(4.42)</strong></p>

<span id="eqn-blahblbla" label="eqn--blahblbla"></span> In particular, for $v = v_i$, this satisfies $f(v_i) = w_i$. The map $f$ is linear; this follows from the preceding discussion.

Conversely, if a linear map $f$ satisfies $f(v_i) = w_i$, for $v$ as above, it necessarily satisfies
<div class="arithmatex" markdown="1">
\[
f(v) = f (\sum_{i=1}^n b_i v_i) = \sum_{i=1}^n b_i f(v_i) = \sum_{i=1}^n b_i w_i.
\]
</div>
So, the map defined in is the only linear map satisfying . ◻

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 4.43</strong> (Related exercises: <a href="../exercises-maps/#ex-maps-exercise-005">Exercise 4.5</a>)</p>

<span id="ex-example-map-basis" label="ex:example-map-basis"></span> We consider $V = {\bf R}^3$, with the basis
<div class="arithmatex" markdown="1">
\[
v_1 = e_1 = (1,0,0), v_2=e_2 = (0,1,0), v_3 = (0,1,-1).
\]
</div>
(Note that $e_1, e_2$ are part of the standard basis of ${\bf R}^3$.) According to <a href="#prop-linear-map-defined-on-basis" data-reference-type="ref+Label" data-reference="prop:linear-map-defined-on-basis">Proposition 4.40</a>, there is a unique linear map $f: {\bf R}^3 \to {\bf R}^3$ such that
<div class="arithmatex" markdown="1">
\[
f(v_1) = (2,-1,0), f(v_2) = (1,-1,1), f(v_3) = (0,2,2).
\]
</div>
We determine $f(e_3)$, where $e_3 = (0,0,1)$ is the third standard basis vector. We have
<div class="arithmatex" markdown="1">
\[
e_3 = v_2-v_3.
\]
</div>
Thus
<div class="arithmatex" markdown="1">
\[
f(e_3) = f(v_2-v_3) = f(v_2)-f(v_3) = (1,-1,1)-(0,2,2) = (1,-3,-1).
\]
</div>
Thus, with respect to the *standard basis* $e_1, e_2, e_3$ (which is distinct from the one above!), the matrix of $f$ is given by
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{ccc} 2 & 1 & 1 \\ -1 & -1 & -3 \\ 0 & 1 & -1 \end{array} \right ).
\]
</div>
That is, $f$ agrees with the map
<div class="arithmatex" markdown="1">
\[
f: {\bf R}^3 \to {\bf R}^3, v \mapsto Av.
\]
</div>

</div>
