---
title: Bases
---

# Bases

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 3.61</strong> (Related exercises: <a href="../exercises-spaces/#base-change-matrix">Exercise 3.12</a>, <a href="../exercises-spaces/#ex-basis-w1-r4">Exercise 3.22</a>, <a href="../exercises-spaces/#ex-intersection-tw">Exercise 3.17</a>, <a href="../exercises-maps/#ex-maps-exercise-006">Exercise 4.6</a>, <a href="../exercises-spaces/#ex-mat-subspace-dim">Exercise 3.24</a>, <a href="../exercises-spaces/#ex-polynomial-basis-ab">Exercise 3.21</a>, <a href="../exercises-spaces/#ex-spaces-2-4">Exercise 3.25</a>, <a href="../exercises-spaces/#ex-spaces-2-5">Exercise 3.27</a>, <a href="../exercises-spaces/#ex-sum-intersection-r4">Exercise 3.26</a>, <a href="../exercises-spaces/#ex-ut-basis-r4">Exercise 3.29</a>, <a href="../exercises-spaces/#ex-wk-basis">Exercise 3.23</a>)</p>

<span id="def-basis" label="def:basis"></span> A collection of vectors in a vector space
<div class="arithmatex" markdown="1">
\[
v_1, \dots, v_m \in V
\]
</div>
is called a *basis* if they span $V$ and if they are linearly independent.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 3.62</strong> (Related exercises: <a href="../exercises-maps/#ex-maps-exercise-003">Exercise 4.3</a>, <a href="../exercises-maps/#ex-maps-exercise-015">Exercise 4.21</a>)</p>

<span id="ex-standard-basis" label="ex:standard-basis"></span> The vectors
<div class="arithmatex" markdown="1">
\[
e_1 = (1, 0, \dots, 0), e_2 = (0, 1, 0, \dots 0), \dots, e_n = (0, \dots, 0,  1) \in {\bf R}^n
\]
</div>
are a basis, called the *standard basis*. Indeed, we have observed in <a href="../spaces-linear-combinations/#ex-standard-basis-generate" data-reference-type="ref+Label" data-reference="ex:standard-basis-generate">Example 3.43</a> and <a href="../spaces-linear-independence/#ex-standard-basis-linearly-independent" data-reference-type="ref+Label" data-reference="ex:standard-basis-linearly-independent">Example 3.51</a> that they span ${\bf R}^n$ and that they are linearly independent.

We try and modify this basis a little bit and see what happens. If we omit one of the vectors and only consider, say
<div class="arithmatex" markdown="1">
\[
e_2 = (0, 1, 0, \dots 0), \dots, e_n = (0, \dots, 0,  1) \in {\bf R}^n
\]
</div>
these do not form a basis: while they are still linearly independent, they do not span ${\bf R}^n$.

On the other hand, we now consider
<div class="arithmatex" markdown="1">
\[
e_1, \dots, e_n, v,
\]
</div>
for an arbitrary vector $v \in {\bf R}^n$. These do not form a basis: while they span ${\bf R}^n$ (even without the $v$), they are not linearly independent. Indeed, since $e_1, \dots, e_n$ span ${\bf R}^n$, this means that
<div class="arithmatex" markdown="1">
\[
v = a_1 e_1 + \dots + a_n e_n
\]
</div>
for appropriate $a_1, \dots, a_n \in {\bf R}$. According to <a href="../spaces-linear-independence/#lem-independent-linear-combination" data-reference-type="ref+Label" data-reference="lem:independent-linear-combination">Lemma 3.54</a>, this means that $e_1, \dots, e_n, v$ are linearly dependent.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 3.63</strong> (Related exercises: <a href="../exercises-spaces/#base-change-matrix">Exercise 3.12</a>)</p>

<span id="ex-three-vectors-basis" label="ex:three-vectors-basis"></span> The vectors
<div class="arithmatex" markdown="1">
\[
v_1 = (0, 2, 1), v_2 = (1, 0, 2), v_3 = (-1, 1, 1)
\]
</div>
form a basis of ${\bf R}^3$. To see this, we apply <a href="../spaces-linear-independence/#met-check-linear-independence" data-reference-type="ref+Label" data-reference="met:check-linear-independence">Method 3.56</a> and <a href="../spaces-linear-combinations/#met-check-generating-system" data-reference-type="ref+Label" data-reference="met:check-generating-system">Method 3.46</a>:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left ( \begin{array}{ccc} 0 & 2 & 1 \\ 1 & 0 & 2 \\ -1 & 1 & 1 \end{array} \right ) \leadsto &
\left ( \begin{array}{ccc} 1 & 0 & 2 \\ 0 & 2 & 1 \\ -1 & 1 & 1 \end{array} \right ) \leadsto 
\left ( \begin{array}{ccc} 1 & 0 & 2 \\ 0 & 2 & 1 \\ 0 & 1 & 3 \end{array} \right ) \\ \leadsto &
\left ( \begin{array}{ccc} 1 & 0 & 2 \\ 0 & 2 & 1 \\ 0 & 0 & \frac 52 \end{array} \right ) \leadsto 
\left ( \begin{array}{ccc} 1 & 0 & 2 \\ 0 & 1 & \frac 1 2 \\ 0 & 0 & 1 \end{array} \right ).
\end{align*}
\]
</div>
This matrix has three leading ones, so the vectors are linearly independent and span ${\bf R}^3$, so they form a basis.

Note that this is a *different* basis than $e_1, e_2, e_3$ considered above.

</div>

The following result, which is simply a combination of the definition of generating systems and <a href="../spaces-linear-independence/#prop-linearly-independent-unique" data-reference-type="ref+Label" data-reference="prop:linearly-independent-unique">Proposition 3.60</a>, is often described by saying that a basis gives rise to a *coordinate system* in a vector space.

<div class="proposition" markdown="1">


<p class="env-number"><strong>Proposition 3.64</strong> (Related exercises: <a href="../exercises-maps/#ex-maps-exercise-011">Exercise 4.11</a>)</p>

<span id="prop-basis-coordinate-system" label="prop:basis-coordinate-system"></span> Let $v_1, \dots, v_m$ be a basis of a vector space $V$. Then each vector $v \in V$ can be written in a *unique* way as a linear combination
<div class="arithmatex" markdown="1">
\[
v=a_1 v_1 + \dots + a_m v_m.
\]
</div>
For some other vector $w = b_1 v_1 + \dots+ b_m v_m$, we have
<div class="arithmatex" markdown="1">
\[
v+w = (a_1+b_1) v_1 + \dots + (a_m + b_m) v_m.
\]
</div>

</div>
