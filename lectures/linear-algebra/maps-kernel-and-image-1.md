---
title: Kernel and Image (1)
---

# Outlook: current research

Since matrix multiplication is such a key asset, it is of great interest to perform this process as efficiently as possible. Given two $2 \times 2$-matrices $A$ and $B$, the computation of $AB$ by just following the definition takes 8 multiplications, namely
<div class="arithmatex" markdown="1">
\[
a_{ie} b_{ej}
\]
</div>
for each of the indices $i, j, e$ being either 1 or 2. In the 1960’s an algorithm (<https://en.wikipedia.org/wiki/Strassen_algorithm>) was found that only requires 7 multiplications. By applying that algorithm iteratively for larger matrices, this gives a decidedly better algorithm. Current research is using methods of artificial intelligence to try and come up with similar methods for $3 \times 3$- and other matrices. Check out this interesting lay-accessible article on recent trends: <https://www.quantamagazine.org/ai-reveals-new-possibilities-in-matrix-multiplication-20221123/>!

# Kernel and image of a linear map

The kernel and the image of a linear map are an important measure how, roughly speaking, interesting this map is. E.g., the zero map ${\bf R}^2 \to {\bf R}^2$, $\left ( \begin{array}{c} x \\ y \end{array} \right )  \mapsto \left ( \begin{array}{c} 0 \\ 0 \end{array} \right )$ is certainly very boring in the sense that it only produces the zero vector in ${\bf R}^2$. By contrast, say, a rotation (by a fixed angle $r$) in ${\bf R}^2$ is more interesting, since any point in ${\bf R}^2$ can be obtained from another point by rotating by that angle $r$.

In order to introduce kernel and image, we need the following general notions related to maps between sets.

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 4.20</strong></p>

<span id="def-inj-surj-bij" label="def:inj-surj-bij"></span> <span id="def-preimage" label="def:preimage"></span> <span id="def-image" label="def:image"></span> Let $f : X \to Y$ be a function between two sets.

- The *preimage* of some element $y \in Y$ is
<div class="arithmatex" markdown="1">
\[
  f^{-1}(y) := \{ x \in X \ | \ f(x) = y\} \ (\subset X).
\]
</div>

- The *image* of $f$ is defined as
<div class="arithmatex" markdown="1">
\[
  {\operatorname{im}\ } (f) := f(X) := \{ f(x) \ | \ x \in X \} \ (\subset Y).
\]
</div>

- $f$ is called *injective* (or *one-to-one*) if for each $y$, the preimage $f^{-1}(y)$ contains *at most* one element.

- $f$ is called *surjective* (or *onto*) if for each $y$, $f^{-1}(y)$ contains *at least* one element. Equivalently, $f$ is surjective if ${\operatorname{im}\ } (f) = Y$.

- $f$ is called *bijective* if it is both injective and surjective. In other words, if for each $y \in Y$, $f^{-1}(y)$ contains exactly one element.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 4.21</strong></p>

<span id="ex-maps-example-011" label="ex:maps-example-011"></span> While in the applications below, we will often consider $X$ and $Y$ to be vector spaces, <a href="#def-inj-surj-bij" data-reference-type="ref+Label" data-reference="def:inj-surj-bij">Definition 4.20</a> applies to maps between arbitrary sets. For example, consider a group of $n$ people $\{P_1, \dots, P_n \}$. Consider the function
<div class="arithmatex" markdown="1">
\[
m : \{P_1, \dots, P_n \} \to \{1, 2, \dots, 12\}
\]
</div>
that assigns to each person their month of birth. This function is surjective if for each month, one of the persons is born in that month. It is injective, if in each month only one birthday party is happening. It is bijective if both conditions are true, i.e., in every month there is exactly one birthday party (for one of the persons).

</div>

In the example above, the map $m$ can only be bijective if $n = 12$, i.e., if the size of the two sets is the same. For linear maps (between vector spaces) we want to articulate a similar idea, but simply saying that the size of the vector spaces are the same is insufficient, since ${\bf R}$, ${\bf R}^2$, ${\bf R}^3$ etc. all have infinitely many elements. Rather, we will see in <a href="../maps-kernel-and-image-2/#cor-maps-dim" data-reference-type="ref+Label" data-reference="cor:maps-dim">Corollary 4.28</a> that the dimension of a vector space is the correct notion of size.

<div class="definition" markdown="1">


<p class="env-number"><strong>Definition 4.22</strong> (Related exercises: <a href="../exercises-maps/#ex-maps-3-1">Exercise 4.8</a>, <a href="../exercises-maps/#ex-maps-3-2">Exercise 4.9</a>, <a href="../exercises-maps/#ex-maps-exercise-003">Exercise 4.3</a>, <a href="../exercises-maps/#ex-maps-exercise-010">Exercise 4.9</a>, <a href="../exercises-maps/#ex-maps-exercise-016">Exercise 4.22</a>)</p>

<span id="def-kernel" label="def:kernel"></span> Let $f : V \to W$ be a linear map. The *kernel* of $f$ is defined as
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\ker (f) & := f^{-1}(0_W) \\ & = \{ v\in V \ | \ f(v) = 0_W \}.
\end{align*}
\]
</div>

</div>

Note that $\ker (f) \subset V$ and ${\operatorname{im}\ } (f) \subset W$. In fact, these are not just arbitrary subsets:

<div class="proposition" markdown="1">


<p class="env-number"><strong>Proposition 4.23</strong> (Related exercises: <a href="../exercises-maps/#ex-maps-exercise-011">Exercise 4.11</a>, <a href="../exercises-maps/#ex-maps-exercise-012">Exercise 4.12</a>)</p>

<span id="prop-ker-im-subspace" label="prop:ker-im-subspace"></span> For a *linear* map $f: V \to W$, $\ker f$ is a sub*space* of $V$, while ${\operatorname{im}\ } f$ is a sub*space* of $W$.

</div>

<div class="proof" markdown="1">

*Proof.* We only check the conditions in <a href="../spaces-definition-solution-of-homogeneous/#def-subspace" data-reference-type="ref+Label" data-reference="def:subspace">Definition 3.17</a> for the kernel. (The case of the image is similar.)

- $0_V \in \ker f$: this means that $f(0_V) = 0_W$, which holds by <a href="../maps-definition-and-first-examples/#rem-linear-map-basic" data-reference-type="ref+Label" data-reference="rem:linear-map-basic">Remark 4.4</a>.

- For $v, v' \in \ker f$ we check $v+v' \in \ker f$: this means $f(v+v') = 0_W$. Indeed, using that $f$ is linear we have
<div class="arithmatex" markdown="1">
\[
  f(v+v') = f(v) + f(v') = 0_W + 0_W = 0_W.
\]
</div>

- For $v \in \ker f$ and $a \in {\bf R}$, we check $av \in \ker f$: as before, using the linearity of $f$, we have
<div class="arithmatex" markdown="1">
\[
  f(av) = af(v) = a\cdot 0_W = 0_W.
\]
</div>

 ◻

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 4.24</strong></p>

<span id="ex-maps-example-012" label="ex:maps-example-012"></span> We consider the matrix
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{ccc} 1 & 2 & 0 \\ 2 & 4 & 0 \end{array} \right )
\]
</div>
and the associated linear map
<div class="arithmatex" markdown="1">
\[
f : {\bf R}^3 \to {\bf R}^2, v = \left ( \begin{array}{c} x \\ y \\ z \end{array} \right ) \mapsto Av = \left ( \begin{array}{c} x+2y \\ 2x+4y \end{array} \right ).
\]
</div>
The kernel of $f$ consists of vectors $v$ such that
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x+2y & = 0 \\ 2x+4y & =0.
\end{align*}
\]
</div>
This tells us that the kernel of $f$, or equivalently the solutions of this system (in the unknowns $x, y$ and $z$!), is
<div class="arithmatex" markdown="1">
\[
\ker f = \left \{\left ( \begin{array}{c} -2y \\ y \\ z \end{array} \right ) \in {\bf R}^3 \ | \ y, z \in {\bf R} \right \}.
\]
</div>
A basis of $\ker f$ is given by the two vectors $\left ( \begin{array}{c} -2 \\ 1 \\ 0 \end{array} \right )$ and $\left ( \begin{array}{c} 0 \\ 0 \\ 1 \end{array} \right )$.

The image of $f$ consists of all vectors of the form
<div class="arithmatex" markdown="1">
\[
v = \left ( \begin{array}{c} v_1 \\ v_2 \end{array} \right ) = \left ( \begin{array}{c} x+2y \\ 2x+4y \end{array} \right ),
\]
</div>
with arbitrary $x, y \in {\bf R}$. (Also, the $z$ is arbitrary, but it does not show up in $f$.) This means that $v_2 = 2 v_1$, and $v_1$ is an arbitrary real number. Thus
<div class="arithmatex" markdown="1">
\[
{\operatorname{im}\ } f = \left \{ \left ( \begin{array}{c} v_1 \\ 2v_1 \end{array} \right ) \ | \ v_1 \in {\bf R} \right \} \subset {\bf R}^2.
\]
</div>
A basis of ${\operatorname{im}\ } f$ is thus given by the vector $\left ( \begin{array}{c} 1 \\ 2 \end{array} \right )$.

</div>

Our goal below is to develop an algorithmic method that determine bases of $\ker f$, ${\operatorname{im}\ } f$. For now, just observe that in the example above
<div class="arithmatex" markdown="1">
\[
\dim (\ker f) + \dim ({\operatorname{im}\ } f) = 2 + 1 = 3 = \dim {\bf R}^3.
\]
</div>
This is an example of the rank-nullity theorem (<a href="#thm-rank-nullity-theorem" data-reference-type="ref+Label" data-reference="thm:rank-nullity-theorem">Theorem 4.26</a>) below.

Injectivity of *linear* maps can be measured in terms of the kernel:

<div class="lemma" markdown="1">


<p class="env-number"><strong>Lemma 4.25</strong> (Related exercises: <a href="../exercises-maps/#ex-maps-3-7">Exercise 4.17</a>)</p>

<span id="lem-injective-ker" label="lem:injective-ker"></span> Let $f : V \to W$ be a linear map. Then the following are equivalent (i.e., one condition holds if and only if the other holds):

1.  $f$ is injective,

2.  $\ker f = \{0_V\}$.

</div>

<div class="proof" markdown="1">

*Proof.* Suppose $f$ is injective, we prove $\ker f = \{0\}$. Since $f(0) = 0$ by linearity (<a href="../maps-definition-and-first-examples/#rem-linear-map-basic" data-reference-type="ref+Label" data-reference="rem:linear-map-basic">Remark 4.4</a>), we have $0 \in \ker f$. If $v \in \ker f$, then $f(v) = 0_W$, so both $v$ and $0_V$ are in the preimage of $0_W$. By the injectivity of $f$, this forces $v = 0$.

Conversely, suppose $\ker f = 0$. Suppose two vectors $v, v' \in V$ are in the preimage of some $w \in W$, i.e., $f(v) = f(v') = w$. Then, by linearity of $f$
<div class="arithmatex" markdown="1">
\[
f(v-v') = f(v+(-1)v') = f(v) + (-1) f(v') = f(v) - f(v') = 0.
\]
</div>
Thus, $v-v' \in \ker f$, which means by assumption that $v-v'=0$. That is: $v = v'$. Therefore $f$ is injective. ◻

</div>

<div class="theorem" markdown="1">


<p class="env-number"><strong>Theorem 4.26</strong> (Related exercises: <a href="../exercises-maps/#ex-maps-3-20">Exercise 4.44</a>, <a href="../exercises-maps/#ex-maps-3-3">Exercise 4.10</a>, <a href="../exercises-maps/#ex-maps-3-4">Exercise 4.13</a>, <a href="../exercises-maps/#ex-maps-3-6">Exercise 4.16</a>, <a href="../exercises-maps/#ex-maps-3-7">Exercise 4.17</a>, <a href="../exercises-maps/#ex-maps-exercise-003">Exercise 4.3</a>)</p>

<span id="thm-rank-nullity-theorem" label="thm:rank-nullity-theorem"></span> (*Rank-nullity theorem*) Let $f: V \to W$ be a map between (finite-dimensional) vector spaces. Then
<div class="arithmatex" markdown="1">
\[
\dim (\ker f) + \dim ({\operatorname{im}\ } f) = \dim V.
\]
</div>
The *rank* of $f$ is defined to be
<div class="arithmatex" markdown="1">
\[
{\operatorname {rk}} f := \dim ({\operatorname{im}\ } f),
\]
</div>
while the *nullity* of $f$ is defined to be $\dim (\ker f)$.

</div>

A proof of this theorem appears in any linear algebra textbook, e.g. (Nicholson 1995, Theorem 7.2.4). As a remark on the proof, we note that one can prove the following fact, which is very useful in its own right.

<div class="theorem" markdown="1">


<p class="env-number"><strong>Theorem 4.27</strong></p>

<span id="thm-maps-theorem-002" label="thm:maps-theorem-002"></span> Let $f: V \to W$ be a linear map. Let
<div class="arithmatex" markdown="1">
\[
v_1, \dots, v_r, v_{r+1}, \dots v_n
\]
</div>
be a basis of $V$ such that
<div class="arithmatex" markdown="1">
\[
v_1, \dots, v_r
\]
</div>
is a basis of $\ker f$. Then $f(v_{r+1}), \dots, f(v_n)$ is a basis of ${\operatorname{im}\ } f$.

</div>

<div id="refs" class="references csl-bib-body hanging-indent">

<div id="ref-Nicholson:Linear" class="csl-entry">

Nicholson, W. K. 1995. *Linear Algebra with Applications*. Mathematics Series. PWS Publishing Company. <https://lyryx.com/linear-algebra-applications/>.

</div>

</div>
