---
title: Systems: Matrices
---

# Matrices

It is time to use some better tools to do the bookkeeping needed to solve linear systems. Matrices help doing that. Later on (§<a href="../maps-definition-and-first-examples/#sect-linear-maps" data-reference-type="ref" data-reference="sect--linear-maps">Chapter 4</a>), we will use matrices in a much more profound way.

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 2.20</strong></p>

<span id="def-systems-definition-006" label="def:systems-definition-006"></span> A *matrix* is a rectangular array of numbers. We speak of an $m \times n$-matrix (or $m$-by-$n$ matrix) if it has $m$ rows and $n$ columns, respectively. If $m=n$, we also call it a *square matrix*.

An $1 \times n$-matrix (i.e., $m=1$ and $n$ is arbitrary) is called a *row vector*. Similarly, an $m \times 1$-matrix is called a *column vector*.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 2.21</strong></p>

<span id="ex-systems-example-007" label="ex:systems-example-007"></span> It is customary to denote matrices by capital letters. For example,
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{cc} 3 & 4 \\ 0 & -7 \end{array} \right )
\]
</div>
is a $2 \times 2$-matrix (or square matrix of size 2).
<div class="arithmatex" markdown="1">
\[
B = \left ( \begin{array}{ccc} 1 & -2 & 0 \\ 1 & 0 & 3 \end{array} \right )
\]
</div>
is a $2 \times 3$-matrix and
<div class="arithmatex" markdown="1">
\[
C = \left ( \begin{array}{cc} 1 & -2 \\ 0 & 1 \\ 0 & -3 \end{array} \right )
\]
</div>
is a $3 \times 2$-matrix.

The entries of a matrix may also be variables. For example
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{c} x_1 \\ x_2 \end{array} \right )
\]
</div>
is a column vector (or a $2 \times 1$-matrix), whose entries are two variables; $\left ( \begin{array}{cc} x_1 & x_2 \end{array} \right )$ is a row vector (or a $1 \times 2$-matrix).

</div>

<div class="notation" markdown="1">


<p class="env-number"><strong>Notation 2.22</strong></p>

<span id="not-matrix-notation" label="not:matrix-notation"></span> A matrix whose entries are unspecified numbers is denoted like so:
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{ccccc} a_{11} & a_{12} & a_{13} & \dots & a_{1n} \\ a_{21} & a_{22} & a_{23} & \dots & a_{2n} \\ \vdots & \vdots & \vdots & \ddots & \vdots \\ a_{m1} & a_{m2} & a_{m3} & \dots & a_{mn}\\ \end{array} \right ).
\]
</div>
Thus, the number $a_{ij}$ is the entry in the $i$-th row and the $j$-th column. A more compressed notation expressing the same is
<div class="arithmatex" markdown="1">
\[
A = (a_{ij})_{i=1, \dots, m, j = 1, \dots, n}
\]
</div>
or even just
<div class="arithmatex" markdown="1">
\[
A = (a_{ij}).
\]
</div>

</div>

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 2.23</strong> (Related exercises: <a href="../exercises-maps/#ex-maps-partial-2026-1">Exercise 4.46</a>)</p>

<span id="def-matrix-to-system" label="def:matrix-to-system"></span> Let
<div class="arithmatex" markdown="1">
\[
\begin{align}
a_{11} x_1 + a_{12} x_2 + \dots + a_{1n} x_n & = b_1 \\
a_{21} x_1 + a_{22} x_2 + \dots + a_{2n} x_n & = b_2 \nonumber \\
\vdots  \nonumber\\
a_{m1} x_1 + a_{m2} x_2 + \dots + a_{mn} x_n & = b_m  \nonumber
\end{align}
\]
</div>

<p class="env-number equation-number"><strong>(2.24)</strong></p>

<span id="eqn-linear-system-large" label="eqn--linear.system.large"></span> be a linear system (consisting of $m$ equations, in the unknowns $x_1, \dots, x_n$; the numbers $a_{ij}$ are the coefficients, the numbers $b_1, \dots, b_n$ are the constants).

The *matrix associated to this system* is the following $m \times (n+1)$-matrix (the vertical bar is just there to remind ourselves that the last column corresponds to the constants in the equations above; one also speaks of an *augmented matrix*)
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{cccc|c} a_{11} & a_{12} & \dots & a_{1n} & b_1 \\ a_{21} & a_{22} & \dots & a_{2n} & b_2 \\ \vdots & \vdots & \ddots & \vdots & \vdots \\ a_{m1} & a_{m2} & \dots & a_{mn} & b_m \\ \end{array} \right ).
\]
</div>

<p class="env-number equation-number"><strong>(2.25)</strong></p>

<span id="eqn-matrix-large" label="eqn--matrix.large"></span> In other words, the matrix is the rectangular array containing the coefficients and the constants of the individual equations, and suppresses the mention of the variables.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 2.26</strong></p>

<span id="ex-systems-example-008" label="ex:systems-example-008"></span> The matrix associated to the system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x+y&=4 \\
x-y&=1
\end{align*}
\]
</div>
is the $2 \times 3$-matrix
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cc|c} 1 & 1 & 4 \\ 1 & -1 & 1 \end{array} \right ).
\]
</div>

</div>

Of course, the process of associating a matrix to a linear system can be reversed since any $m \times (n+1)$-matrix gives rise to a linear system: the matrix gives rise to the linear system . For example, the $2 \times 3$- matrix
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cc|c} 1 & -2 & 0 \\ 1 & 0 & 3 \end{array} \right )
\]
</div>
gives rise to the linear sytem
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x - 2y & = 0 \\
x & = 3.
\end{align*}
\]
</div>
