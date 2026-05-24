---
title: Systems: Gaussian Elimination
---

# Gaussian elimination

<a href="../systems-elementary-operations/#thm-elementary-equivalent" data-reference-type="ref+Label" data-reference="thm:elementary-equivalent">Theorem 2.18</a> is a useful insight, but it lacks an important feature: it does not directly instruct us how to simplify any given linear system. (In <a href="../systems-elementary-operations/#ex-example-elementary-operations" data-reference-type="ref+Label" data-reference="ex:example-elementary-operations">Example 2.19</a>, we did end up with a particularly simple linear system, but we did not have any a priori guarantee for this to happen. If we had chosen some “stupid” elementary operations instead, we would not have simplified the system.) *Gaussian elimination* is an algorithmic process that does just that: it is a simple procedure that is guaranteed to yield the simplest possible equivalent form of any given linear system.

In view of the correspondence between linear systems and matrices, we will first phrase this process in terms of matrices, and then translate it back to the problem of solving linear systems.

Among the myriad of all possible matrices, the following matrices are the “nice guys”.

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 2.27</strong> (Related exercises: <a href="../exercises-spaces/#ex-linear-independence">Exercise 3.7</a>, <a href="../exercises-spaces/#ex-spaces-2-2">Exercise 3.15</a>, <a href="../exercises-spaces/#ex-spanning-r4">Exercise 3.6</a>, <a href="../exercises-spaces/#ex-sum-intersection-r4">Exercise 3.26</a>, <a href="../exercises-spaces/#ex-wk-basis">Exercise 3.23</a>)</p>

<span id="def-row-echelon-form" label="def:row-echelon-form"></span> A matrix is in *row-echelon form* (or is called a *row-echelon matrix*) if the following conditions are satisfied:

1.  If there are any zero rows (i.e., consisting only of zeros), then these are at the bottom of the matrix.

2.  In a non-zero row, the first non-zero (starting from the left) is a 1. (It is called the *leading 1*.)

3.  Each leading 1 is to the right of all the leading 1’s in the rows above it.

If, *in addition* to the above conditions, each leading 1 is the *only* non-zero entry in its column, then the matrix is in *reduced row-echelon form*.

Maybe saying more than a thousand words is this picture of a row-echelon form. Here, the asterisks indicate an arbitrary number. If, in addition, all the underlined asterisks are zero, then the matrix is a reduced row-echelon matrix.

<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccccccc} 0 & 1 & * & \underline * & \underline * & * & \underline * \\ 0 & 0 & 0 & 1 & \underline * & * & \underline * \\ 0 & 0 & 0 & 0 & 1 & * & \underline * \\ 0 & 0 & 0 & 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 & 0 & 0 \\ \end{array} \right ).
\]
</div>

</div>

In view of the correspondence between linear systems and matrices, we transport the language of elementary operations (<a href="../systems-elementary-operations/#def-elementary-operations-system" data-reference-type="ref+Label" data-reference="def:elementary-operations-system">Definition 2.17</a>) to matrices as follows.

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 2.28</strong> (Related exercises: <a href="../exercises-spaces/#ex-linear-independence">Exercise 3.7</a>, <a href="../exercises-maps/#ex-maps-exercise-004">Exercise 4.4</a>, <a href="../exercises-maps/#ex-maps-exercise-007">Exercise 4.7</a>, <a href="../exercises-systems/#ex-maps-exercise-008">Exercise 2.25</a>, <a href="../exercises-maps/#ex-maps-partial-2026-2">Exercise 4.47</a>, <a href="../exercises-spaces/#ex-spaces-2-6">Exercise 3.28</a>, <a href="../exercises-spaces/#ex-spanning-r4">Exercise 3.6</a>)</p>

<span id="def-elementary-row-operations" label="def:elementary-row-operations"></span> The following operations on a given matrix $A$ are called *elementary row operations*:

1.  interchange any two rows,

2.  multiply any row by a *non-zero* (!) number,

3.  add a multiple of any row to a *different* (!) row.

</div>

<div class="method" markdown="1">


<p class="env-number"><strong>Method 2.29</strong> (Related exercises: <a href="../exercises-spaces/#ex-linear-independence">Exercise 3.7</a>, <a href="../exercises-maps/#ex-maps-exercise-004">Exercise 4.4</a>, <a href="../exercises-maps/#ex-maps-partial-2026-2">Exercise 4.47</a>, <a href="../exercises-spaces/#ex-spanning-r4">Exercise 3.6</a>, <a href="../exercises-spaces/#ex-sum-intersection-r4">Exercise 3.26</a>, <a href="../exercises-systems/#ex-systems-1-b">Exercise 2.12</a>, <a href="../exercises-spaces/#ex-ut-basis-r4">Exercise 3.29</a>, <a href="../exercises-spaces/#ex-wk-basis">Exercise 3.23</a>)</p>

<span id="met-gaussian-algorithm" label="met:gaussian-algorithm"></span> (*Gaussian algorithm* or *Gaussian eliminiation*) Every matrix can be brought to reduced row-echelon form by a sequence of elementary row operations. This can be achieved using the following algorithmic process:

1.  If the matrix consists only of zeros, stop: then the matrix is in reduced row-echelon form.

2.  Otherwise, find the first column from the left having a non-zero entry. Call this entry $a$. Interchange this row (elementary operation <a href="../systems-elementary-operations/#item-change" data-reference-type="ref" data-reference="item--change">1.</a>) so that it is in the top position.

3.  Multiply the new top row by $\frac 1 a$ (elementary operation <a href="../systems-elementary-operations/#item-multiply" data-reference-type="ref" data-reference="item--multiply">2.</a>; note this is possible since $a \ne 0$, see also <a href="../systems-linear-equations/#rem-field" data-reference-type="ref+Label" data-reference="rem:field">Remark 2.5</a>). Thus the first row has a leading 1.

4.  By adding appropriate multiples of the first row to the remaining rows (elementary operation <a href="../systems-elementary-operations/#item-add" data-reference-type="ref" data-reference="item--add">3.</a>), ensure that the entry between the leading 1 are all zero.

From this point on, the first row is not touched anymore, and the four steps above are applied to the matrix consisting of the remaining rows.

This produces a (possibly not reduced) row-echelon form. It can be finally brought into reduced row-echelon form by adding appropriate multiples of rows with leading 1’s to the rows above them (elementary operation <a href="../systems-elementary-operations/#item-add" data-reference-type="ref" data-reference="item--add">3.</a>), beginning at the bottom.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 2.30</strong></p>

<span id="ex-43-matrix" label="ex:43-matrix"></span> We apply the Gaussian algorithm to the matrix
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc} 1 & 2 & 5 & 7 \\ 2 & 1 & 4 & 2 \\ 5 & 4 & 13 & 11 \end{array} \right ).
\]
</div>

The first three steps don’t change the matrix (since the top-left entry is already 1). Step (4): add $-2$ times the first row to the second row; and add $-5$ times the first row to the third, which gives
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc} 1 & 2 & 5 & 7 \\ 0 & \underline{-3} & -6 & -12 \\ 0 & -6 & -12 & -24 \end{array} \right )
\]
</div>
The remaining steps only affect the second and third row. Step (2) picks the second row, and $a = -3$ (underlined). It is already in the top position (the first row being discarded for the remainder of the algorithm), so Step (2) does not change the matrix. Step (3) gives the matrix
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc} 1 & 2 & 5 & 7 \\ 0 & 1 & 2 & 4 \\ 0 & -6 & -12 & -24 \end{array} \right )
\]
</div>
Step (4) adds $-6$ times the second row to the third, which gives
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc} 1 & 2 & 5 & 7 \\ 0 & 1 & 2 & 4 \\ 0 & 0 & 0 & 0 \end{array} \right ).
\]
</div>
At this point also the second row is discarded, which leaves only the last row, which consists of zeros. By Step (1), the algorithm stops at this point.

This matrix is in row-echelon form, but not yet reduced. To reduce it, add $-2$ times the second row to the first, which gives
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc} 1 & 0 & 1 & -1 \\ 0 & 1 & 2 & 4 \\ 0 & 0 & 0 & 0 \end{array} \right )
\]
</div>

</div>

When applied to matrices associated to linear systems, Gaussian eliminiation becomes very useful for solving linear systems:

<div class="method" markdown="1">


<p class="env-number"><strong>Method 2.31</strong> (Related exercises: <a href="../exercises-spaces/#base-change-matrix">Exercise 3.12</a>, <a href="../exercises-spaces/#ex-basis-w1-r4">Exercise 3.22</a>, <a href="../exercises-euclid/#ex-euclid-6-2">Exercise 7.4</a>, <a href="../exercises-euclid/#ex-euclid-6-22">Exercise 7.26</a>, <a href="../exercises-spaces/#ex-intersection-tw">Exercise 3.17</a>, <a href="../exercises-maps/#ex-maps-3-2">Exercise 4.9</a>, <a href="../exercises-maps/#ex-maps-3-6">Exercise 4.16</a>, <a href="../exercises-maps/#ex-maps-exercise-003">Exercise 4.3</a>, <a href="../exercises-maps/#ex-maps-exercise-004">Exercise 4.4</a>, <a href="../exercises-systems/#ex-maps-exercise-008">Exercise 2.25</a>, <a href="../exercises-maps/#ex-maps-exercise-010">Exercise 4.9</a>, <a href="../exercises-maps/#ex-maps-partial-2026-1">Exercise 4.46</a>, <a href="../exercises-maps/#ex-maps-partial-2026-2">Exercise 4.47</a>, <a href="../exercises-spaces/#ex-matrix-subspace">Exercise 3.14</a>, <a href="../exercises-spaces/#ex-spaces-2-6">Exercise 3.28</a>, <a href="../exercises-systems/#ex-systems-1-b">Exercise 2.12</a>)</p>

<span id="met-gaussian-elimination-solve" label="met:gaussian-elimination-solve"></span>

1.  Form the augmented matrix corresponding to the given linear system.

2.  Perform Gaussian elimination to that matrix (<a href="#met-gaussian-algorithm" data-reference-type="ref+Label" data-reference="met:gaussian-algorithm">Method 2.29</a>), giving a reduced row-echelon matrix.

3.  If a row of the form
<div class="arithmatex" markdown="1">
\[
    0 \ 0 \ \dots \ 0 \ 1
\]
</div>
occurs, the system has *no* solutions.

4.  Otherwise, we call the variables corresponding to the columns *not* containing a leading 1 *free variables*. The values of these variables can be chosen to be *arbitrary* real numbers. The variables that correspond to columns that do contain a leading 1 are uniquely specified by these free variables. Their values can be determined by solving the equations corresponding to the row-echelon matrix for the leading variables.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 2.32</strong></p>

<span id="ex-systems-example-010" label="ex:systems-example-010"></span> Consider the system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x + 2y + 5 z & =  7 \\
2x + y + 4 z & = 2 \\
5 x + 4 y + 13 z & = 11.
\end{align*}
\]
</div>
The augmented matrix associated to this is the one in <a href="#ex-43-matrix" data-reference-type="ref+Label" data-reference="ex:43-matrix">Example 2.30</a>. Gaussian algorithm brings it into the reduced row-echelon form
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc} 1 & 0 & 1 & -1 \\ 0 & 1 & 2 & 4 \\ 0 & 0 & 0 & 0 \end{array} \right ).
\]
</div>
This matrix corresponds to the linear system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x + z & =  -1 \\
y + 2z & = 4 \\
0 & = 0.
\end{align*}
\]
</div>
According to <a href="../systems-elementary-operations/#thm-elementary-equivalent" data-reference-type="ref+Label" data-reference="thm:elementary-equivalent">Theorem 2.18</a>, this linear system has the same solution set as the original one.

The leading variables are $x$ and $y$, so that $z$ is a free variable. Solving the second equation for $y$ then gives
<div class="arithmatex" markdown="1">
\[
y = 4-2z,
\]
</div>
and similarly
<div class="arithmatex" markdown="1">
\[
x = -1-z.
\]
</div>
We obtain that the solution set to the original linear system consists of triples of the form
<div class="arithmatex" markdown="1">
\[
(x = -1-z, y = 4-2z, z),
\]
</div>
in which $z$ is an arbitrary number (and $x$ and $y$ are determined by $z$ as indicated).

</div>
