---
title: Distances
---

# Distance between two affine subspaces

<div class="theorem" markdown="1">


<p class="env-number"><strong>Theorem 7.59</strong> (Related exercises: <a href="../exercises-euclid/#ex-euclid-6-19">Exercise 7.23</a>)</p>

<span id="thm-distance-affine-subspaces" label="thm:distance-affine-subspaces"></span> Let $X = v+ W$, $X' = v' + W'$ be two affine subspaces. Let us write $d := v-v'$ and $Z := W + W'$ (<a href="../spaces-linear-combinations/#def-sum-of-vector-spaces" data-reference-type="ref+Label" data-reference="def:sum-of-vector-spaces">Definition 3.36</a>). Let
<div class="arithmatex" markdown="1">
\[
m := p_{Z^\bot}(d) = d - p_Z(d)
\]
</div>
be the orthogonal projection of $d$ onto $Z^\bot$ (<a href="../euclid-euclidean-spaces/#cor-two-projections" data-reference-type="ref+Label" data-reference="cor:two-projections">Corollary 7.34</a>).

For two points $x \in X$ and $x' \in X'$ the following are equivalent:

1.  <span id="item-min-e" label="item--min.e"></span> $x - x' = m$.

2.  <span id="item-min-b" label="item--min.b"></span> $d(x,x') = |\hspace{-0.5mm}| {m} |\hspace{-0.5mm}|$.

3.  <span id="item-min-a" label="item--min.a"></span> $x$ and $x'$ realize the minimal distance of $X$ and $X'$, i.e., $d(x, x') = d(X, X')$.

4.  <span id="item-min-c" label="item--min.c"></span> The vector $x - x'$ is orthogonal to $W$ and to $W'$ (i.e., $x-x'$ is orthogonal to any $w \in W$, $w' \in W'$).

In particular, $X$ intersects $X'$ if and only if $d \in Z$.

</div>

<div class="proof" markdown="1">

*Proof.* Here is a picture of the geometric ideas in the proof. For simplicity of the picture, we choose $v' = 0$, so that $X' = W'$ and $d = v$.

<div class="center" markdown="1">

![image](figures/png/euclid/euclid-fig-08.png)

</div>

<a href="#item-min-e" data-reference-type="ref" data-reference="item--min.e">1.</a> $\Rightarrow$ <a href="#item-min-b" data-reference-type="ref" data-reference="item--min.b">2.</a> is obvious since $d(x,x') = |\hspace{-0.5mm}| {x-x'} |\hspace{-0.5mm}|$.

We next prove the equivalence <a href="#item-min-a" data-reference-type="ref" data-reference="item--min.a">3.</a> $\Leftrightarrow$ <a href="#item-min-b" data-reference-type="ref" data-reference="item--min.b">2.</a>. We write a point $x \in X$ as $x = v + w$ with an arbitrary vector $w \in W$. Likewise, $x' = v' + w'$. We then have
<div class="arithmatex" markdown="1">
\[
d(x,x') = |\hspace{-0.5mm}| {x-x'} |\hspace{-0.5mm}| = |\hspace{-0.5mm}| {v-v' + w-w'} |\hspace{-0.5mm}| = |\hspace{-0.5mm}| {d + w-w'} |\hspace{-0.5mm}|.
\]
</div>
The vector $w-w'$ is an arbitrary vector in the sum $Z = W + W'$ (notice that for any $w' \in W'$, also $-w' \in W'$).

Therefore, we are seeking the point $z \in Z = W + W'$ such that $|\hspace{-0.5mm}| {d+z} |\hspace{-0.5mm}|$ is minimal. This is just the distance of the affine subspace $d + Z$ to the origin. According to <a href="../euclid-affine-subspaces/#prop-min-affine-subspace" data-reference-type="ref+Label" data-reference="prop:min-affine-subspace">Proposition 7.45</a>, this distance is given by $|\hspace{-0.5mm}| {m} |\hspace{-0.5mm}| = |\hspace{-0.5mm}| {p_{Z^\bot}(d)} |\hspace{-0.5mm}| = |\hspace{-0.5mm}| {d - p_Z(d)} |\hspace{-0.5mm}|$, and $m$ is the unique vector in $Z$ realizing that minimal distance. This shows the equivalence of <a href="#item-min-a" data-reference-type="ref" data-reference="item--min.a">3.</a> and <a href="#item-min-b" data-reference-type="ref" data-reference="item--min.b">2.</a>.

<a href="#item-min-a" data-reference-type="ref" data-reference="item--min.a">3.</a> $\Rightarrow$ <a href="#item-min-c" data-reference-type="ref" data-reference="item--min.c">4.</a>: let $x \in X$ and $x' \in X'$ be two points realizing that minimal distance: $d(x,x') = |\hspace{-0.5mm}| {m} |\hspace{-0.5mm}|$. In particular, this means that $x' \in X'$ is the point realizing the minimal distance to $x$. Again by <a href="../euclid-affine-subspaces/#prop-min-affine-subspace" data-reference-type="ref+Label" data-reference="prop:min-affine-subspace">Proposition 7.45</a>, $x'-x$ is therefore orthogonal to $W'$. Switching the role of $X$ and $X'$ we obtain similarly that $x-x'$ is orthogonal to $W$.

<a href="#item-min-c" data-reference-type="ref" data-reference="item--min.c">4.</a> $\Rightarrow$ <a href="#item-min-e" data-reference-type="ref" data-reference="item--min.e">1.</a>: Our assumption means that
<div class="arithmatex" markdown="1">
\[
x - x' \in W^\bot \cap W'^\bot = (W + W')^\bot = Z^\bot.
\]
</div>
To see the latter equality note that some vector is orthogonal to $W + W'$ precisely if it is orthogonal to $W$ and to $W'$, by the bilinearity of ${\left \langle -, - \right \rangle}$. We use this remark as follows: from
<div class="arithmatex" markdown="1">
\[
x - x' = v+w - v' - w'
\]
</div>
we get
<div class="arithmatex" markdown="1">
\[
\begin{align*}
d = v-v' & = \underbrace{x-x'}_{\in Z^\bot} + \underbrace{w' - w}_{\in Z}.
\end{align*}
\]
</div>
By the unicity of the representation of $d$ as a sum of a vector in $Z^\bot$ and one in $Z$, this means that $x-x' = p_{Z^\bot}(d) = m$. ◻

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 7.60</strong></p>

<span id="ex-euclid-example-018" label="ex:euclid-example-018"></span> We consider the two lines in ${\bf R}^3$
<div class="arithmatex" markdown="1">
\[
\begin{align*}
X & = (2,-1,3) + L(1,1,-2) = v + W\\
X' & = (-3,0,0) + L(0,2,4) = v' + W'.
\end{align*}
\]
</div>
The general vectors of $X$ and $X'$ are of the following form, for $a, b \in {\bf R}$.
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x &=  (2,-1,3) + a(1,1,-2) & = (2+a,-1+a,3-2a) \\
x'& = (-3,0,0) + b(0,2,4) & = (-3,2b,4b) \\
x-x' & & = (5+a,-1+a-2b,3-2a-4b)
\end{align*}
\]
</div>
We compute the minimal distance of $X$ and $X'$ by considering the condition $x - x' \bot (1,1,-2)$ and $x - x' \bot (0,2,4)$. This gives the following homogeneous linear system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
0 & = (5+a)+(-1+a-2b)-2(3-2a-4b) & = -2+6a+6b \\
0 & = 2(-1+a-2b)+4(3-2a-4b) & = 10-6a -20 b.\\
\end{align*}
\]
</div>
This can be solved to $b = \frac 47$ and $a = - \frac 5 {21}$. The points $x$ and $x'$ and their distance is then readily computed.

</div>
