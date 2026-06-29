---
title: Intersections of Subspaces
---

<a id="sect-intersection-of-subspaces"></a>
# Intersection of subspaces

<div class="lemma" markdown="1">


<p class="env-number"><strong>Lemma 3.19</strong> (Related exercises: <a href="../exercises-maps/#ex-maps-partial-2026-1">Exercise 4.46</a>, <a href="../exercises-spaces/#ex-spaces-2-3">Exercise 3.16</a>, <a href="../exercises-spaces/#ex-spaces-2-6">Exercise 3.28</a>)</p>

<span id="lem-spaces-lemma-003" label="lem:spaces-lemma-003"></span> Let $V$ be a vector space and $A, B \subset V$ be two subspaces. Then the *intersection*
<div class="arithmatex" markdown="1">
\[
A \cap B := \{ v \in V \ | \ v \in A \text{ and } v \in B \}
\]
</div>
is also a subspace of $V$. More generally, this holds true for any number of subspaces, i.e., if $A_1, A_2 \dots, A_n \subset V$ are subspaces, then so is their joint intersection
<div class="arithmatex" markdown="1">
\[
A_1 \cap \dots \cap A_n = \{ v \in V \ | \ v \in A_1, v \in A_2, \dots, v \in A_n \}.
\]
</div>

</div>

<div class="proof" markdown="1">

*Proof.* We need to make sure that $A \cap B$ satisfies the conditions in <a href="../spaces-definition-solution-of-homogeneous/#def-subspace" data-reference-type="ref+Label" data-reference="def:subspace">Definition 3.17</a>. This is easy enough. For example, the zero vector $0 \in A \cap B$ since $0 \in A$ (since $A$ is a sub*space*) and also $0 \in B$ (since $B$ is also a subspace). Here is a visualization for sums: if $x, y \in A \cap B$, then $x + y \in A \cap B$ since it is both contained in $A$ and also in $B$.

<div class="center" markdown="1">

![image](figures/png/spaces/spaces-fig-06.png)

</div>

 ◻

</div>

Intersections of subspaces are hugely important to us because of the following example.

<div class="example" markdown="1">


<p class="env-number"><strong>Example 3.20</strong></p>

<span id="ex-spaces-example-007" label="ex:spaces-example-007"></span> Consider once again a homogenous system as in <a href="../spaces-definition-solution-of-homogeneous/#homogeneous-system" data-reference-type="eqref" data-reference="homogeneous.system">Equation (3.14)</a>. Then, of course, each individual equation of that system is in its own right a homogeneous linear equation, for example
<div class="arithmatex" markdown="1">
\[
\begin{align*}
a_{11} x_1 + a_{12} x_2 + \dots + a_{1n} x_n & = 0
\end{align*}
\]
</div>
By the above, the solution set of that equation is a subspace of ${\bf R}^n$, that we denote by $S_1 (\subset {\bf R}^n)$. Likewise this is true for all the other individual equations, so we get some subspaces $S_1, \dots, S_m$, one for each equation. The solution set of the *whole* system is then just
<div class="arithmatex" markdown="1">
\[
S_1 \cap S_2 \cap \dots \cap S_m.
\]
</div>
(Indeed, a vector $(r_1, \dots, r_n) \in {\bf R}^n$ is a solution for the whole system precisely if it is one for the individual equations.)

</div>

An important question that we will eventually be able to make more precise and to answer is this:

<div class="question" markdown="1">


<p class="env-number"><strong>Question 3.21</strong></p>

<span id="q-dimension-intersection" label="q:dimension-intersection"></span> Given two subspaces $A, B$ in some vector space $V$, how “much smaller” can $A \cap B$ be than $A$ and $B$?

</div>

In the above illustration, we will want to articulate the idea that the ambient vector space $V$ is “3-dimensional”, $A$ and $B$ are 2-dimensional (i.e., a plane) and $A \cap B$ is 1-dimensional (i.e., a line). Note that this need not be the case: if $A = B$ is the *same* plane, for example, then certainly $A \cap B = A$ is also 2-dimensional. This relates to the discussion about the intersections of lines in ${\bf R}^2$ in <a href="../systems-linear-systems/#sum-intersection-lines" data-reference-type="ref+Label" data-reference="sum:intersection-lines">Summary 2.12</a>: if $A, B \subset {\bf R}^2$ are “1-dimensional” (i.e., lines), their intersection may still be a line, namely if $A = B$. If the ambient vector space $V$ is even larger, for example $V = {\bf R}^4$ (which has “dimension 4”), then it is no longer reasonable to write down all possible constellations of how $A, B$ lie in $V$.



<a id="vis-dim-sum-intersection"></a>
<iframe src="../visualizations/dim-sum-intersection.html" style="width:100%;height:520px;border:none;border-radius:6px;" loading="lazy"></iframe>


