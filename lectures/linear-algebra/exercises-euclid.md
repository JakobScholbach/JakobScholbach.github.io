<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.1</strong></p>

<span id="ex-euclid-polynomials-gs" label="ex:euclid-polynomials-gs"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-polynomials-gs" data-reference-type="ref+Label" data-reference="sol--ex:euclid-polynomials-gs">Solution 7.1</a>.) Let $V = P_{\le 2} = \{ at^2 + bt+c \ | \ a,b,c \in {\bf R} \}$ be the vector space of (real) polynomials of degree $\le 2$. We consider the scalar product in <a href="../euclid-euclidean-spaces/#ex-examples-scalar-product" data-reference-type="ref+Label" data-reference="ex:examples-scalar-product">Example 7.16</a><a href="../euclid-euclidean-spaces/#item-functions" data-reference-type="ref" data-reference="item--functions">3.</a>, i.e.,
<div class="arithmatex" markdown="1">
\[
{\left \langle p, q \right \rangle} = \int_{-1}^1 p(x)q(x) dx.
\]
</div>

- Let $e_1 = 1$, $e_2 = t$ and $e_3 = t^2$. (These vectors form a basis of $P_{\le 2}$.) Compute ${\left \langle e_i, e_j \right \rangle}$ for $1 \le i,j \le 3$. (This requires knowledge of basic integration techniques.)

- Apply the Gram–Schmidt orthogonalization procedure to this basis.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.2</strong></p>

<span id="ex-euclid-6-1" label="ex:euclid-6-1"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-6-1" data-reference-type="ref+Label" data-reference="sol--ex:euclid-6-1">Solution 7.3</a>.) Consider the subspace $U \subset {\bf R}^3$ given by the solutions of the homogeneous linear system
<div class="arithmatex" markdown="1">
\[
x-y+3z=0.
\]
</div>

1.  Find a basis of $U$.

2.  Compute a basis of $U^\bot$. What is $\dim U^\bot$?

3.  Consider $t=(0,1,5)$. Find its orthogonal projection onto $U$ (recall from <a href="../euclid-euclidean-spaces/#cor-two-projections" data-reference-type="ref+Label" data-reference="cor:two-projections">Corollary 7.34</a> that $t = t_U + t_\bot$ with uniquely determined vectors $t_U \in U$ and $t_\bot \in U^\bot$. The orthogonal projection of $t$ onto $U$ is then the vector $t_U$.)

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.3</strong></p>

<span id="ex-euclid-r4-projection" label="ex:euclid-r4-projection"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-r4-projection" data-reference-type="ref+Label" data-reference="sol--ex:euclid-r4-projection">Solution 7.2</a>.) Consider the subspace $W \subset {\bf R}^4$ given by the equations
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x-t & = 0\\
y+z-t & = 0\\
\end{align*}
\]
</div>
(where $x,y,z,t$ are the coordinates of ${\bf R}^4$).

1.  Compute a basis of $W$ and of $W^\bot$.

2.  Compute the orthogonal projection of $t=(1,5,1,6)$ onto $W$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.4</strong></p>

<span id="ex-euclid-6-2" label="ex:euclid-6-2"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-6-2" data-reference-type="ref+Label" data-reference="sol--ex:euclid-6-2">Solution 7.4</a>.) Consider the subspace $U \subset {\bf R}^3$ given by the equations
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x & = 0\\
x+y+z & = 0\\
\end{align*}
\]
</div>
(where $x,y,z$ are the coordinates of ${\bf R}^3$).

1.  Compute a basis of $U$ and of $U^\bot$.

2.  Compute the orthogonal projection of $t=(5,1,3)$ onto $U$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.5</strong></p>

<span id="ex-euclid-6-3" label="ex:euclid-6-3"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-6-3" data-reference-type="ref+Label" data-reference="sol--ex:euclid-6-3">Solution 7.5</a>.) Compute the orthogonal complement of $T = L((1,0,-3))$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.6</strong></p>

<span id="ex-euclid-6-4" label="ex:euclid-6-4"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-6-4" data-reference-type="ref+Label" data-reference="sol--ex:euclid-6-4">Solution 7.6</a>.) Is there a subspace $U \subset {\bf R}^3$ such that

1.  the orthogonal projection of $t=(1,1,0)$ onto $U$ is given by $(1,5,6)$?

2.  the orthogonal projection of $t=(2,0,1)$ onto $U$ is given by $(1,1,1)$?

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.7</strong></p>

<span id="ex-euclid-6-6" label="ex:euclid-6-6"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-6-6" data-reference-type="ref+Label" data-reference="sol--ex:euclid-6-6">Solution 7.7</a>.) Let $L = \left ( \begin{array}{c} 1 \\ 3 \\ 5 \end{array} \right ) + L (\left ( \begin{array}{c} 1 \\ 1 \\ 4 \end{array} \right ))$. Compute the closest point of $L$ to the origin, and its distance to the origin.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.8</strong></p>

<span id="ex-euclid-6-7" label="ex:euclid-6-7"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-6-7" data-reference-type="ref+Label" data-reference="sol--ex:euclid-6-7">Solution 7.8</a>.) Consider the two lines $L: x=1+t,y=t,z=2+t, t \in {\bf R}$ and $L':x-3=y-1=z-3$. Are they parallel? Compute the distance between $L$ and $L'$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.9</strong></p>

<span id="ex-euclid-6-8" label="ex:euclid-6-8"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-6-8" data-reference-type="ref+Label" data-reference="sol--ex:euclid-6-8">Solution 7.9</a>.) Are the lines
<div class="arithmatex" markdown="1">
\[
L: x = y-1=-z  \text{ and } L' :x-2=-y=\frac z2
\]
</div>
identical, parallel, or skew? Compute their distance.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.10</strong></p>

<span id="ex-euclid-6-9" label="ex:euclid-6-9"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-6-9" data-reference-type="ref+Label" data-reference="sol--ex:euclid-6-9">Solution 7.10</a>.) Let $P$ be the plane given by the equation
<div class="arithmatex" markdown="1">
\[
4x+5y+10z-20 = 0.
\]
</div>
Let $L$ be the line given by the equations $x = 0, y = 5 - z$.

1.  Sketch $P$ and $L$.

2.  Compute the orthogonal complement of the underlying vector space $W$ of $P$.

3.  Compute the point of $P$ that is closest to the origin and its distance to the origin.

4.  Are $P$ and $L$ parallel?

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.11</strong></p>

<span id="ex-euclid-6-10" label="ex:euclid-6-10"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-6-10" data-reference-type="ref+Label" data-reference="sol--ex:euclid-6-10">Solution 7.11</a>.) Which of the following matrices is orthogonally diagonalizable? If so, find a orthonormal eigenbasis of ${\bf R}^2$.

1.  $A = \left ( \begin{array}{cc} 1 & 2 \\ 2 & 1 \end{array} \right )$

2.  $A = \left ( \begin{array}{cc} 1 & 2 \\ -2 & 1 \end{array} \right )$

3.  $A = \left ( \begin{array}{cc} 0 & 0 \\ 0 & 0 \end{array} \right )$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.12</strong></p>

<span id="ex-euclid-6-11" label="ex:euclid-6-11"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-6-11" data-reference-type="ref+Label" data-reference="sol--ex:euclid-6-11">Solution 7.12</a>.) <span id="eigenvectors-orthogonal" label="eigenvectors.orthogonal"></span> Let $A$ be a symmetric matrix and $\lambda \ne \mu$ two *distinct* eigenvalues of $A$, with eigenvectors $v$ and $w$, respectively. Then $v \bot w$, i.e., eigenvectors of *distinct* eigenvalues are orthogonal.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.13</strong></p>

<span id="ex-euclid-6-12" label="ex:euclid-6-12"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-6-12" data-reference-type="ref+Label" data-reference="sol--ex:euclid-6-12">Solution 7.13</a>.) Let $P \subset {\bf R}^4$ by the hyperplane given by
<div class="arithmatex" markdown="1">
\[
2 x_1 + x_3 - x_4 = 4,
\]
</div>
where $(x_1, \dots, x_4)$ are the coordinates of ${\bf R}^4$. For a parameter $t \in {\bf R}$, let $L_t$ be the line
<div class="arithmatex" markdown="1">
\[
L_t = (1,0,0,-2t) + L(t, 1, 0, -1).
\]
</div>

- For which $t \in {\bf R}$ is $L_t$ parallel to $P$?

- Let now $t = -\frac 12$ and consider the line $L = L_{-\frac 12}$. Determine the pair(s) of points $(p, l)$ such that $p \in P$ and $l \in L$ such that their distance is minimal.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.14</strong></p>

<span id="ex-euclid-lines-plane" label="ex:euclid-lines-plane"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-lines-plane" data-reference-type="ref+Label" data-reference="sol--ex:euclid-lines-plane">Solution 7.14</a>.) Let $L \subset {\bf R}^3$ be the line defined be the system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x+z & = 1\\
y+z & = -2.
\end{align*}
\]
</div>
Let $L'$ be the line in ${\bf R}^3$ passing through the points $(0,0,1)$ and $(0,1,1)$.

- Present $L$ as $L=v+W$ for a subspace $W \subset {\bf R}^3$. Do the same for $L'$.

- Are $L$ and $L'$ a) identical, b) parallel, c) skew or d) intersecting?

- Compute the Cartseian equation (i.e., in the form $ax+by+cz=d$, for appropriate values of $a, \dots, d$) of the plane $P \subset {\bf R}^3$ that contains $L$ and is parallel to $L'$.

- Let $l = (2,-1,-1) \in L$. Compute a point $l' \in L'$ such that the line passing through $l$ and $l'$ is parallel to the plane given by the equation $x+z-1=0$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.15</strong></p>

<span id="ex-euclid-poly-operator" label="ex:euclid-poly-operator"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-poly-operator" data-reference-type="ref+Label" data-reference="sol--ex:euclid-poly-operator">Solution 7.15</a>.) Let $V = P_{\le 2}$ be the vector space of polynomials of degree $\le 2$. We write elements of $V$ as $p(t)=a+bt+ct^2$, where $a,b,c\in{\bf R}$. Define
<div class="arithmatex" markdown="1">
\[
{\left \langle p, q \right \rangle} := \int_{-1}^1 p(t) q(t) dt.
\]
</div>

- Confirm that ${\left \langle -, - \right \rangle}$ is a scalar product on $V$.

- Compute an orthonormal basis of $V$.

- Consider the map
<div class="arithmatex" markdown="1">
\[
  f : V \to V, f(p) := t \frac{\partial p}{\partial t}
\]
</div>
  (i.e., it maps a polynomial $p$ to the product of the indeterminate $t$ with the derivative of $p$ with respect to the variable $t$). Confirm that this map is linear. Compute the matrix of $f$ with respect to the standard basis $e_1 = 1$, $e_2 = t$ and $e_3 = t^2$. Is this basis an eigenbasis for $f$? Compute $\dim \ker f$ and $\dim {\operatorname{im}\ } f$.

- Does the map $f$ have an orthonormal eigenbasis?

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.16</strong></p>

<span id="ex-euclid-u-r4-orth" label="ex:euclid-u-r4-orth"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-u-r4-orth" data-reference-type="ref+Label" data-reference="sol--ex:euclid-u-r4-orth">Solution 7.16</a>.) Consider the subspace $U \subset{\bf R}^4$ given by the solutions of the equation
<div class="arithmatex" markdown="1">
\[
x_1-x_2+x_3+2x_4 = 0.
\]
</div>
(As usual $x_1, \dots, x_4$ are the coordinates of ${\bf R}^4$.)

1.  Find a basis of $U$. What is $\dim U$?

2.  Compute an orthonormal basis of $U$.

3.  Compute the orthogonal projection of $v=(2,3,0,0)$ and of $w=(2,5,3,0)$ onto $U$.

4.  Compute $U^\bot$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.17</strong></p>

<span id="ex-euclid-6-13" label="ex:euclid-6-13"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-6-13" data-reference-type="ref+Label" data-reference="sol--ex:euclid-6-13">Solution 7.17</a>.) In the Euclidean space ${\bf R}^4$, endowed with the standard scalar product, let $U$ be the subspace spanned by the vectors $u_1 = (1,2,0,-1)$, $u_2 = (0,-4,3,4)$.

1.  Compute an orthogonal basis of $U$.

2.  Compute a basis of $U^\perp$.

3.  Compute the orthogonal projection of $v = (0,5,3,4)$ onto $U$.

4.  Let $w = (2,-1,0,2)$. Decide whether there is a subspace $L \subset {\bf R}^4$ such that the orthogonal projection of $w$ onto $L$ is the vector $\ell = (1,1,2,0)$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.18</strong></p>

<span id="ex-euclid-6-14" label="ex:euclid-6-14"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-6-14" data-reference-type="ref+Label" data-reference="sol--ex:euclid-6-14">Solution 7.18</a>.) Consider the following two lines in ${\bf R}^3$, where $x, y, z$ are the coordinates:
<div class="arithmatex" markdown="1">
\[
L: \left\{\begin{aligned}
& x + y - 1 = 0\\
& 2x - z - 1 = 0
\end{aligned}\right. \qquad
M: \left\{\begin{aligned}
& x - 2y - 1 = 0\\
& y - z + 2 = 0
\end{aligned}\right.
\]
</div>

1.  Determine whether $L$ and $M$ are the same line, parallel, or skew.

2.  Compute the cartesian equation of the plane that contains the line $M$ and that is parallel to $L$. (Recall that a cartesian equation is of the form $\langle x, a \rangle = d$ for an appropriate vector $a$ and an appropriate $d \in {\bf R}$.)

3.  <span id="item-ex-6-14-c" label="item--ex 6.14 c"></span> Given the point $l = (0,1,-1) \in L$ compute a point $m \in M$ such that the line passing through $l$ and $m$ is parallel to the plane defined by the equation $3x - z = 0$.

4.  Consider the family of planes $\pi_\alpha: z = \alpha$, for some parameter $\alpha \in {\bf R}$. Let $r_\alpha = L \cap \pi_\alpha$ and $s_\alpha = M \cap \pi_\alpha$. Let $m_\alpha$ be the midpoint of the segment with endpoints $r_\alpha$ and $s_\alpha$. Verify that the points $m_\alpha$ are all lying on the same line. Moreover, determine the parametric equation of that line.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.19</strong></p>

<span id="ex-euclid-6-15" label="ex:euclid-6-15"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-6-15" data-reference-type="ref+Label" data-reference="sol--ex:euclid-6-15">Solution 7.19</a>.) Consider the points $p = (3,1,0)$, $q = (0,1,3)$ and $r = (-3,0,-3) \in {\bf R}^3$. Let $L$ be the line passing through $p$ and $q$.

1.  Determine the parametric equation of $L$, i.e., express $L$ in the form $L = v + W$, for an appropriate vector $v \in {\bf R}^3$ and a subspace $W \subset {\bf R}^3$.

2.  Verify that $r$ does not lie on $L$. Give the plane $P$ containing $p, q, r$ both in vector and in cartesian form.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.20</strong></p>

<span id="ex-euclid-6-16" label="ex:euclid-6-16"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-6-16" data-reference-type="ref+Label" data-reference="sol--ex:euclid-6-16">Solution 7.20</a>.) Consider the line $L = (3,1,0) + L(1,0,-1)$. Is there a plane containing $L$ and the line $M$ given by the systen $x + z = 2$, $x - 2 y = 2$ (with $x, y, z$ being the coordinates of ${\bf R}^3$)?

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.21</strong></p>

<span id="ex-euclid-6-17" label="ex:euclid-6-17"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-6-17" data-reference-type="ref+Label" data-reference="sol--ex:euclid-6-17">Solution 7.21</a>.) Consider the line $L = (3,1,0) + L(1,0,-1)$. Let $p = (-1,-1,-1)$. Describe all the points $q \in {\bf R}^3$ such that the line $M$ passing through $p$ and $q$ intersects $L$ orthogonally (i.e., intersects it, and does so orthogonally).

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.22</strong></p>

<span id="ex-euclid-6-18" label="ex:euclid-6-18"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-6-18" data-reference-type="ref+Label" data-reference="sol--ex:euclid-6-18">Solution 7.22</a>.) Consider the plane $P = \{x \in {\bf R}^3, 3x - 4y+z = 2\}$ and the point $p = (0,1,6) \in P$, as well as the line $L = (0,0,2) + L(1, 1, 1) \subset P$, compute the line $M \subset P$ that is orthogonal to $L$ and contains the point $p$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.23</strong></p>

<span id="ex-euclid-6-19" label="ex:euclid-6-19"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-6-19" data-reference-type="ref+Label" data-reference="sol--ex:euclid-6-19">Solution 7.23</a>.) Consider the lines (in ${\bf R}^3$)
<div class="arithmatex" markdown="1">
\[
\begin{align*}
L_1 : \ & 2x-y=-3 \\ & y+z=-2
\end{align*}
\]
</div>
and
<div class="arithmatex" markdown="1">
\[
\begin{align*}
L_2 : \ & x=t \\ & y = 2 \\ & z = 4-t, t \in {\bf R}.
\end{align*}
\]
</div>

1.  Determine their relative position (skew, parallel etc.)

2.  Find the plane $\pi$ parallel to $L_1$ and containing $L_2$.

3.  Compute the distance between $\pi$ and $L_1$.

4.  Find points $p_1 \in L_1$, $p_2 \in L_2$ such that
<div class="arithmatex" markdown="1">
\[
    |\hspace{-0.5mm}| {p_1-p_2} |\hspace{-0.5mm}| = d(p_1, p_2) = d(L_1, L_2),
\]
</div>
i.e., two points that realize the minimal distance between $L_1$ and $L_2$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.24</strong></p>

<span id="ex-euclid-6-20" label="ex:euclid-6-20"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-6-20" data-reference-type="ref+Label" data-reference="sol--ex:euclid-6-20">Solution 7.24</a>.) We endow ${\bf R}^4$ with its usual scalar product. We consider the subspace $U \subset {\bf R}^4$ defined by the equations
<div class="arithmatex" markdown="1">
\[
\left\{\begin{aligned}
& x_1 + x_3 = 0 \\
& 2x_1 + x_2 - x_4 = 0
\end{aligned}\right.
\]
</div>

1.  Compute an orthogonal basis of $U$.

2.  Given the vector $w_1 = (1,1,-1,-1)$ find a vector $w_2$ that is orthogonal to $w_1$ and such that the vector space $W := L(w_1, w_2)$ satisfies $W = U^\perp$.

3.  Write down a system of linear equations in the unknowns $x_1, x_2, x_3, x_4$ whose solution set is the subspace $W = U^\perp$.

4.  Given the vector $v = (3,1,-1,1)$ find a vector $u \in U$ such that the vector $v+u$ has minimal norm.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.25</strong></p>

<span id="ex-euclid-6-21" label="ex:euclid-6-21"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-6-21" data-reference-type="ref+Label" data-reference="sol--ex:euclid-6-21">Solution 7.25</a>.) Consider the lines (contained in ${\bf R}^3$)
<div class="arithmatex" markdown="1">
\[
L: \left\{\begin{aligned}
& x - 2y + 4 = 0\\
& y + z -3 = 0
\end{aligned}\right. \qquad
M: \left\{\begin{aligned}
& x+2z-5 = 0\\
& x-2y + 1 = 0
\end{aligned}\right.
\]
</div>

1.  Verify that $L$ and $M$ are parallel and write down the cartesian equation of the plane containing $L$ and $M$.

2.  Given the point $p  = (0,2,1) \in L$ find the point $q \in M$ such that the line passing through $p$ and $q$ is orthogonal to $L$ and to $M$.

3.  Write down the cartesian equation of the plane $X$ containing the line $L$ and passing through the point $r = (-1,1,0)$.

4.  Write down the parametric equation of the line $N$ contained in the plane $X$, passing through $r = (-1,1,0)$ and orthogonal to the line $L$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.26</strong></p>

<span id="ex-euclid-6-22" label="ex:euclid-6-22"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-6-22" data-reference-type="ref+Label" data-reference="sol--ex:euclid-6-22">Solution 7.26</a>.) Let $U \subset {\bf R}^4$ be the subspace defined by the equations
<div class="arithmatex" markdown="1">
\[
U: \left\{\begin{aligned}
& x_1 - 2x_2 + x_4 = 0 \\
& 3x_2 + x_3 - 2x_4 = 0 \\
& 3x_1 + 2x_3 + t\,x_4 = 0
\end{aligned}\right.
\]
</div>

1.  Find the value of $t$ for which $U$ has dimension 2. For this value of $t$, compute a basis of $U$.

2.  Apply the Gram–Schmidt method to the basis computed in part (a) in order to compute an orthogonal basis of $U$.

3.  For the value of $t$ computed in part (a), compute a basis of $U^\perp$.

4.  Given $v = (3,2,2,-2) \in {\bf R}^4$ compute the cartesian equation of a subspace $W$ of dimension $3$ such that the orthogonal projection of $v$ onto $W$ is equal to the vector $w  = (1,2,1,1)$.

</div>

<div class="exercise" markdown="1">


<p class="env-number"><strong>Exercise 7.27</strong></p>

<span id="ex-euclid-6-23" label="ex:euclid-6-23"></span> (See <a href="../solutions-euclidean-spaces/#sol-ex-euclid-6-23" data-reference-type="ref+Label" data-reference="sol--ex:euclid-6-23">Solution 7.27</a>.) We consider the following points (in ${\bf R}^3$) $A = (6,-1,-4)$, $B = (1,1,-1)$ and the plane $X: 2x - y - 2z = 3$.

1.  Verify that $B \in X$. Let $C$ be the orthogonal projection of $A$ onto the plane $X$. Compute $C$.

2.  Compute the cartesian equation of the plane containing the triangle $\triangle ABC$.

3.  Compute the parametric equation of the line that a) passes through $B$, b) is contained in the plane $X$ and c) is orthogonal to the line passing through $A$ and $B$.

4.  Compute the value of the parameter $t$ such that the line $M_t: \left\{\begin{aligned}
    & t\,x - y + 2 = 0 \\
    & x + z + 1 = 0
    \end{aligned}\right.$ is parallel to the plane $X$.

</div>
