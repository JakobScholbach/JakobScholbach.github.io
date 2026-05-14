---
title: Systems: Linear Systems
---

# Systems of linear equations

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 2.7</strong></p>

<span id="def-systems-definition-002" label="def:systems-definition-002"></span> A *system of linear equations* is a collection of linear equations (involving the same variables). It is also sometimes called a *linear system* or even just a *system*.

</div>

The interest in linear systems lies in finding those tuples of numbers satisfying *all* equations at once (as opposed to just one of them, say). We will start with two equations in two variables.

<div class="example" markdown="1">


<p class="env-number"><strong>Example 2.8</strong></p>

<span id="ex-system-2-unique" label="ex:system-2-unique"></span> The equations
<div class="arithmatex" markdown="1">
\[
\begin{align}
x+y&=4 \\
x-y&=1. \nonumber
\end{align}
\]
</div>

<p class="env-number equation-number"><strong>(2.9)</strong></p>

<span id="system-2-unique-eqn" label="system.2.unique.eqn"></span> form a system of linear equations (in the variables $x$ and $y$).

We solve this system algebraically by subtracting $y$ in the first equation, which gives
<div class="arithmatex" markdown="1">
\[
x = -y + 4,
\]
</div>
and substituting this into the second equation, which gives
<div class="arithmatex" markdown="1">
\[
(-y+4)-y=1,
\]
</div>
or
<div class="arithmatex" markdown="1">
\[
-2y+4=1
\]
</div>
or
<div class="arithmatex" markdown="1">
\[
-2y=-3
\]
</div>
or finally
<div class="arithmatex" markdown="1">
\[
y = \frac 3 2.
\]
</div>
Inserting this back above, gives
<div class="arithmatex" markdown="1">
\[
x = - \frac 3 2 + 4 = \frac 5 2.
\]
</div>
Note that again each equation holds (for given values of $x$ and $y$) precisely if the preceding one holds. Thus, the original system has the same solution set as the last two equation (together). This system of equations therefore has a *unique* solution, namely
<div class="arithmatex" markdown="1">
\[
(x = \frac 5 2, y = \frac 3 2).
\]
</div>
To say the same using different symbols: the solution set of the system <a href="#system-2-unique-eqn" data-reference-type="eqref" data-reference="system.2.unique.eqn">Equation (2.9)</a> is a set consisting of a single element:
<div class="arithmatex" markdown="1">
\[
\{(\frac 5 2, \frac 3 2) \}
\]
</div>

It is very useful to also understand this process geometrically, which we do by plotting the two lines that are the solutions of the individual equations:

<div class="center" markdown="1">

![image](figures/png/systems/systems-fig-02.png)

</div>

The algebraic computation of having precisely one solution is matched by the fact that two non-parallel lines in the plane (which are the solution sets of the individual equations) exact in precisely one point.

</div>

The above linear system <a href="#system-2-unique-eqn" data-reference-type="eqref" data-reference="system.2.unique.eqn">Equation (2.9)</a> had exactly one solution. This need not always be the case, as the following examples show:

<div class="example" markdown="1">


<p class="env-number"><strong>Example 2.10</strong></p>

<span id="ex-system-2-no" label="ex:system-2-no"></span> The system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x + y & = 4\\
x + y & = 1
\end{align*}
\]
</div>
has *no solution*. This can be seen algebraically  and also geometrically:

<div class="center" markdown="1">

![image](figures/png/systems/systems-fig-03.png)

</div>

The system has no solution, which is paralleled by the fact that two *parallel, but distinct* lines in the plane do not intersect.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 2.11</strong></p>

<span id="ex-system-2-infinite" label="ex:system-2-infinite"></span> The system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x + y & = 4 \\
-2x -2y & = -8
\end{align*}
\]
</div>
has infinitely many solutions, namely all pairs of the form
<div class="arithmatex" markdown="1">
\[
(x, y = 4-x),
\]
</div>
with an arbitrary real number $x$. Geometrically, this is explained by taking the “intersection” of the same line twice.

<div class="center" markdown="1">

![image](figures/png/systems/systems-fig-04.png)

</div>

In other words, even though there are two equations above, they both have the same solution set. Thus, in some sense one of the equations is redundant, i.e., the solution set of the entire system equals the solution set of either of the equations individually.

</div>

<div class="summary" markdown="1">


<p class="env-number"><strong>Summary 2.12</strong></p>

<span id="sum-intersection-lines" label="sum:intersection-lines"></span> The solution set of an equation of the form
<div class="arithmatex" markdown="1">
\[
ax+by = c
\]
</div>
is a line (unless both $a$ and $b$ are zero).

The solution set of a system of equations of the form
<div class="arithmatex" markdown="1">
\[
ax+by = c
\]
</div>
<div class="arithmatex" markdown="1">
\[
dx+ey = f
\]
</div>
can take three forms:\

| number of solutions | geometric explanation |
|:---|:---|
| exactly one solution | the unique intersection point of two non-parallel lines |
| no solution | two distinct parallel lines don’t intersect |
| infinitely many solutions | a line intersects itself in infinitely many points |

</div>

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 2.13</strong></p>

<span id="def-homogeneous-linear-system" label="def:homogeneous-linear-system"></span> A *homogeneous linear system* is one in which the constant terms in all equations are zero. (I.e., in the notation in below, $b_1 = \dots = b_n = 0$.)

</div>

<div class="remark" markdown="1">


<p class="env-number"><strong>Remark 2.14</strong></p>

<span id="rem-trivial-solution" label="rem:trivial-solution"></span> For a homogeneous linear system, there is always *at least* one solution namely
<div class="arithmatex" markdown="1">
\[
(x_1 = 0, \dots, x_n = 0).
\]
</div>
This solution is called the *trivial solution*.

</div>
