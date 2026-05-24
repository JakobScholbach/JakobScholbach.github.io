---
title: Systems: Elementary Operations
---

# Elementary operations

The combination of geometric intuition with algebraic computations is very useful. However, the former is of limited use when it comes to systems with three variables, and hardly useful anymore for systems involving four or more variables. We will therefore develop notions and techniques that enable us to handle linear systems more systematically.

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 2.15</strong></p>

<span id="def-systems-definition-004" label="def:systems-definition-004"></span> We say that two linear systems are *equivalent* if they have the same solution sets.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 2.16</strong></p>

<span id="ex-systems-example-005" label="ex:systems-example-005"></span> In <a href="../systems-linear-systems/#ex-system-2-unique" data-reference-type="ref+Label" data-reference="ex:system-2-unique">Example 2.8</a>, we considered the system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x+y & = 4 \\
x-y & =1
\end{align*}
\]
</div>
and found that it has a unique solution, namely
<div class="arithmatex" markdown="1">
\[
(x = \frac 5 2, y = \frac 3 2).
\]
</div>
Thus the previous system is equivalent to the system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x&=\frac 5 2 \\
y&=\frac 3 2.
\end{align*}
\]
</div>

</div>

Of course, in comparison to the original system, the latter system is much easier to understand, since one can simply read off the solution without any effort. The purpose of elementary operations is to transform a given system into an equivalent system of which the solutions can be read off.

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 2.17</strong></p>

<span id="def-elementary-operations-system" label="def:elementary-operations-system"></span> Given a linear system, the following operations are called *elementary operations*:

1.  <span id="item-change" label="item--change"></span> interchange two equations,

2.  <span id="item-multiply" label="item--multiply"></span> multiply one equation by a *non-zero* (!) number,

3.  <span id="item-add" label="item--add"></span> add a multiple of one equation to a *different* (!) equation.

</div>

These operations are called “elementary” since they are so simple to perform. Their utility comes partly from the following fact:

<div class="theorem" markdown="1">


<p class="env-number"><strong>Theorem 2.18</strong></p>

<span id="thm-elementary-equivalent" label="thm:elementary-equivalent"></span> Consider a linear system. This linear system is equivalent to (i.e., has the same solutions as) any linear system obtained by performing any number of elementary operations.

</div>

This theorem, which we will prove later on (<a href="../maps-inverses/#cor-equivalent-systems" data-reference-type="ref+Label" data-reference="cor:equivalent-systems">Corollary 4.78</a>) when we have more tools at our disposal may sound a little abstract at first sight. It is however actually simple to comprehend and, very importantly, extremely useful in practice.

<div class="example" markdown="1">


<p class="env-number"><strong>Example 2.19</strong></p>

<span id="ex-example-elementary-operations" label="ex:example-elementary-operations"></span> Consider the system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x + 2z & = -1 \\
-2x - 3z & = 1 \\
2 y & = -2.\\
\end{align*}
\]
</div>
We add twice the first equation to the second (elementary operation <a href="#item-add" data-reference-type="ref" data-reference="item--add">3.</a>):
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x + 2z & = -1 \\
z & = -1 \\
2 y & = -2.\\
\end{align*}
\]
</div>
We interchange the second and third equation (elementary operation <a href="#item-change" data-reference-type="ref" data-reference="item--change">1.</a>):
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x + 2z & = -1 \\
2 y & = -2\\
z & = -1. \\
\end{align*}
\]
</div>
We multiply the second equation by $\frac 1 2$ (in other words, we divide it by 2; elementary operation <a href="#item-multiply" data-reference-type="ref" data-reference="item--multiply">2.</a>):
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x + 2z & = -1 \\
 y & = -1\\
z & = -1. \\
\end{align*}
\]
</div>
We add $(-2)$ times the third equation to the first (elementary operation <a href="#item-add" data-reference-type="ref" data-reference="item--add">3.</a>)
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x & = 1 \\
 y & = -1\\
z & = -1. \\
\end{align*}
\]
</div>
These steps are combinations of elementary operations. According to <a href="#thm-elementary-equivalent" data-reference-type="ref+Label" data-reference="thm:elementary-equivalent">Theorem 2.18</a>, the original system is equivalent (i.e., has the same solutions) as the final one. The benefit is, of course, that the solutions of the final system are trivial to comprehend: it has exactly one solution, the triple
<div class="arithmatex" markdown="1">
\[
(x = 1, y = -1, z = -1).
\]
</div>
Thus, the original system also has exactly that one solution.

</div>
