<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.10.1</strong></p>

<span id="sol-ex-exotic-scalar-multiplication" label="sol--ex:exotic-scalar-multiplication"></span> (See <a href="../spaces/#ex-exotic-scalar-multiplication" data-reference-type="ref+Label" data-reference="ex:exotic-scalar-multiplication">Exercise 3.1</a>.) To decide whether we get a vector space, we check axioms from <a href="../spaces/#def-vector-space" data-reference-type="ref+Label" data-reference="def:vector-space">Definition 3.10</a>, especially

- $(r+s)v=rv+sv$ (<a href="../spaces/#def-vector-space" data-reference-type="ref+Label" data-reference="def:vector-space">Definition 3.10</a><a href="../spaces/#item-distributive-law" data-reference-type="ref" data-reference="item--distributive law">4.</a>),

- $(rs)v=r(sv)$ (<a href="../spaces/#def-vector-space" data-reference-type="ref+Label" data-reference="def:vector-space">Definition 3.10</a><a href="../spaces/#item-multiplication-law" data-reference-type="ref" data-reference="item--multiplication.law">6.</a>),

- and $1v=v$ (item 7 in <a href="../spaces/#def-vector-space" data-reference-type="ref+Label" data-reference="def:vector-space">Definition 3.10</a>).

1.  $r\cdot(x,y,z)=(rx,y,rz)$. Let $v=(x,y,z)$. Then
<div class="arithmatex" markdown="1">
\[
    (r+s)\cdot v=((r+s)x,y,(r+s)z),
\]
</div>
    while
<div class="arithmatex" markdown="1">
\[
    r\cdot v+s\cdot v=(rx,y,rz)+(sx,y,sz)=((r+s)x,2y,(r+s)z).
\]
</div>
    In general these are different (e.g. if $y\neq 0$), so
<div class="arithmatex" markdown="1">
\[
    (r+s)v\neq rv+sv.
\]
</div>
    Thus axiom <a href="../spaces/#def-vector-space" data-reference-type="ref+Label" data-reference="def:vector-space">Definition 3.10</a><a href="../spaces/#item-distributive-law" data-reference-type="ref" data-reference="item--distributive law">4.</a> fails. Hence this is *not* a vector space structure.

2.  $r\cdot(x,y,z)=(0,0,0)$.

    For any nonzero $v\in V$,
<div class="arithmatex" markdown="1">
\[
    1\cdot v=(0,0,0)\neq v.
\]
</div>
    So the identity axiom $1v=v$ from <a href="../spaces/#def-vector-space" data-reference-type="ref+Label" data-reference="def:vector-space">Definition 3.10</a> fails. Hence this is *not* a vector space structure.

3.  $r\cdot(x,y,z)=(r^2x,r^2y,r^2z)$.

    Here, for every $v=(x,y,z)\in V$,
<div class="arithmatex" markdown="1">
\[
    1\cdot v=(1^2x,1^2y,1^2z)=(x,y,z)=v,
\]
</div>
    so the axiom $1v=v$ (item 7 in <a href="../spaces/#def-vector-space" data-reference-type="ref+Label" data-reference="def:vector-space">Definition 3.10</a>) is satisfied. Also,
<div class="arithmatex" markdown="1">
\[
    (r+s)\cdot v=((r+s)^2x,(r+s)^2y,(r+s)^2z),
\]
</div>
    while
<div class="arithmatex" markdown="1">
\[
    r\cdot v+s\cdot v=(r^2x,r^2y,r^2z)+(s^2x,s^2y,s^2z)=((r^2+s^2)x,(r^2+s^2)y,(r^2+s^2)z).
\]
</div>
    In general these are different (e.g. $r=s=1$ and $v\neq 0$), so
<div class="arithmatex" markdown="1">
\[
    (r+s)v\neq rv+sv.
\]
</div>
    Hence <a href="../spaces/#def-vector-space" data-reference-type="ref+Label" data-reference="def:vector-space">Definition 3.10</a><a href="../spaces/#item-distributive-law" data-reference-type="ref" data-reference="item--distributive law">4.</a> fails. (By contrast, <a href="../spaces/#def-vector-space" data-reference-type="ref+Label" data-reference="def:vector-space">Definition 3.10</a><a href="../spaces/#item-multiplication-law" data-reference-type="ref" data-reference="item--multiplication.law">6.</a> does hold here.) Hence this is *not* a vector space structure.

Therefore, in all three cases, $V$ is *not* a vector space.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.10.2</strong></p>

<span id="sol-ex-spaces-2-1" label="sol--ex:spaces-2-1"></span> (See <a href="../spaces/#ex-spaces-2-1" data-reference-type="ref+Label" data-reference="ex:spaces-2-1">Exercise 3.13</a>.) A linear combination of $A$ and $B$ is of the form
<div class="arithmatex" markdown="1">
\[
\alpha A + \beta B = \alpha \left ( \begin{array}{cc} 1 & 1 \\ 2 & 2 \end{array} \right ) + \beta \left ( \begin{array}{cc} 3 & 2 \\ 3 & 5 \end{array} \right )
\]
</div>
with $\alpha, \beta \in {\bf R}$. Computing the left hand side, we need to find $\alpha$ and $\beta$ such that
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cc} \alpha & \alpha \\ 2 \alpha & 2 \alpha \end{array} \right ) + \left ( \begin{array}{cc} 3 \beta & 2 \beta \\ 3 \beta & 5 \beta \end{array} \right ) = \left ( \begin{array}{cc} \alpha + 3\beta & \alpha + 2 \beta \\ 2\alpha+3\beta & 2\alpha+5\beta \end{array} \right ) = \left ( \begin{array}{cc} -1 & 0 \\ 2 & 4 \end{array} \right ).
\]
</div>
Comparing the entries of the matrix, this gives the linear system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\alpha + 3 \beta & = -1 \\
\alpha + 2 \beta & = 0\\
2\alpha + 3\beta & = 2\\
2\alpha + 5 \beta & = 4.
\end{align*}
\]
</div>
The second gives $\alpha = -2\beta$, inserting into the first gives $-2 \beta+3 \beta = -1$, which means $\beta = -1$. However, inserting into the third equation gives $-4\beta + 3 \beta = 2$, so that $\beta = -2$, contradicting the previous equation. Thus, there is no solution, so $C$ is *not* a linear combination of $A$ and $B$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.10.3</strong></p>

<span id="sol-ex-spaces-2-2" label="sol--ex:spaces-2-2"></span> (See <a href="../spaces/#ex-spaces-2-2" data-reference-type="ref+Label" data-reference="ex:spaces-2-2">Exercise 3.15</a>.) The system $x + y + z+t=0$ corresponds to the matrix
<div class="arithmatex" markdown="1">
\[
( 1 \ 1 \ 1 \ 1 ).
\]
</div>
This matrix is already in reduced row echelon form: the leading one is for the variable $x$, the variables $y, z, t$ are free variables. Thus,
<div class="arithmatex" markdown="1">
\[
S = \{(-\alpha - \beta - \gamma , \alpha, \beta, \gamma) \ | \ \alpha, \beta, \gamma \in {\bf R} \}.
\]
</div>
We have
<div class="arithmatex" markdown="1">
\[
\begin{align*}
S & = \{(-\alpha, \alpha, 0,0) + (-\beta, 0, \beta, 0) + (-\gamma, 0, 0, \gamma) \ | \ \alpha, \beta, \gamma \in {\bf R}\}  \\
& = \{\alpha(-1, 1, 0,0) + \beta (-1, 0, 1, 0) + \gamma(-1, 0, 0, 1) \ | \ \alpha, \beta, \gamma \in {\bf R}\}  \\
& = L((-1,1,0,0), (-1,0,1,0), (-1,0,0,1)).
\end{align*}
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.10.4</strong></p>

<span id="sol-ex-spaces-2-3" label="sol--ex:spaces-2-3"></span> (See <a href="../spaces/#ex-spaces-2-3" data-reference-type="ref+Label" data-reference="ex:spaces-2-3">Exercise 3.16</a>.) By definition, $S$ consists of all the linear combinations of the three given vectors. These can be written as
<div class="arithmatex" markdown="1">
\[
a (1,-1,0,1) + b(2,1,-2,0)+c(0,0,1,1) = (a+2b,-a+b,-2b+c,a+c)
\]
</div>
for arbitrary $a,b,c \in {\bf R}$. The intersection is given by vectors as above satisfying the linear system determining $T$, i.e.,
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x_1 &= a+2b\\
x_2 & = -a+b \\
x_3 &= -2b+c \\
x_4 & = a+c
\end{align*}
\]
</div>
such that
<div class="arithmatex" markdown="1">
\[
\begin{align*}
2(a+2b)-(-a+b)-3(a+c) & = 0\\
2(a+2b)+(-2b+c)+(a+c) & = 0.
\end{align*}
\]
</div>
Simplifying these equations gives
<div class="arithmatex" markdown="1">
\[
\begin{align*}
3b-3c & = 0\\
3a+2b+2c & = 0.
\end{align*}
\]
</div>
Thus $b=c$ and $3a+4c=0$, i.e., $a = -\frac 43c$, and $c$ is a free variable. (Alternatively, the above system is associated to the matrix $\left ( \begin{array}{ccc} 0 & 3 & -3 \\ 3 & 2 & 2 \end{array} \right )$, which can be brought into reduced row echelon form.) Thus,
<div class="arithmatex" markdown="1">
\[
\begin{align*}
S \cap T & = \{-\frac 43 c(1,-1,0,1) + c(2,1,-2,0)+c(0,0,1,1) \ | \ c \in {\bf R} \} \\
& = \{ c \left ( (-\frac 43, \frac 43, 0, -\frac 43) + (2,1,-2,0)+(0,0,1,1) \right ) \ | \ c \in {\bf R} \} \\
& = \{ c ( \frac 23, \frac 73, -1, - \frac 13) \ | \ c \in {\bf R} \} \\
& = L(( \frac 23, \frac 73, -1, - \frac 13)).
\end{align*}
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.10.5</strong></p>

<span id="sol-ex-spaces-2-4" label="sol--ex:spaces-2-4"></span> (See <a href="../spaces/#ex-spaces-2-4" data-reference-type="ref+Label" data-reference="ex:spaces-2-4">Exercise 3.25</a>.) We have to find a vector $v \in W_1$ that is also contained in $W_2$. This means that
<div class="arithmatex" markdown="1">
\[
v = a (1,0,1)+b(2,1,0) = (a+2b,b,a)
\]
</div>

<p class="env-number equation-number"><strong>(3.78)</strong></p>

<span id="eqn-sol-blah" label="eqn--sol.blah"></span> for some $a, b \in {\bf R}$ and at the same time
<div class="arithmatex" markdown="1">
\[
v = \alpha(-1,-1,1) + \beta(0,3,0) = (-\alpha, -\alpha + 3 \beta, \alpha)
\]
</div>
for some $\alpha, \beta \in {\bf R}$. Comparing the two vectors gives the following linear system, where $a, b, \alpha, \beta$ are the unknowns:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
a + 2 b & = -\alpha \\
b & = -\alpha + 3\beta \\
a & = \alpha.
\end{align*}
\]
</div>
We solve this system: the last equation gives $a = \alpha$ and, from the first equation, $b = -\alpha$. The second equation implies $\beta = 0$. There is no condition on $\alpha$, this $\alpha = r$ for an arbitrary real number $r \in {\bf R}$.

Instead of solving the above system by hand, we may also use Gaussian elimination to solve this linear system. The matrix is the following (where the columns are for $a, b, \alpha, \beta$, in that order):
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left ( \begin{array}{cccc} 1 & 2 & 1 & 0 \\ 0 & 1 & 1 & -3 \\ 1 & 0 & -1 & 0 \end{array} \right ) \leadsto
& \left ( \begin{array}{cccc} 1 & 2 & 1 & 0 \\ 0 & 1 & 1 & -3 \\ 0 & -2 & -2 & 0 \end{array} \right ) \leadsto
\left ( \begin{array}{cccc} 1 & 2 & 1 & 0 \\ 0 & 1 & 1 & -3 \\ 0 & 0 & 0 & -6 \end{array} \right ) \\ & \leadsto 
\left ( \begin{array}{cccc} 1 & 2 & 1 & 0 \\ 0 & 1 & 1 & -3 \\ 0 & 0 & 0 & 1 \end{array} \right ).
\end{align*}
\]
</div>
The three leading ones are for the variables $a, b, \beta$, and $\alpha$ is a free variable, so let $\alpha = r$, where $r \in {\bf R}$ is an arbitrary real number. This gives again $\beta = 0$, $b + r - 3\beta = 0$, so that $b = - r$ and $a = r$.

Thus the intersection $W_1 \cap W_2$ consists of the vectors
<div class="arithmatex" markdown="1">
\[
v = \alpha (1,0,1) + (-\alpha)(2,1,0) = \alpha(-1,-1,1) + 0 (0,3,0) = (-\alpha, -\alpha, \alpha).
\]
</div>
Thus,
<div class="arithmatex" markdown="1">
\[
W_1 \cap W_2 = L((1,-1,1)),
\]
</div>
so a basis of $W_1 \cap W_2$ consists of (the single vector) $(1,-1,1)$, and in particular
<div class="arithmatex" markdown="1">
\[
\dim W_1 \cap W_2 = 1.
\]
</div>

We now consider $W_1 + W_2$. According to <a href="../spaces/#def-sum-of-vector-spaces" data-reference-type="ref+Label" data-reference="def:sum-of-vector-spaces">Definition 3.34</a>,
<div class="arithmatex" markdown="1">
\[
W_1 + W_2 = \{w_1 + w_2 \ | \ w_1 \in W_1, w_2 \in W_2 \},
\]
</div>
i.e., of arbitrary sums whose two summands are in $W_1$, respectively $W_2$.

As was noted in the proof of <a href="../spaces/#cor-dim-sum-inequality" data-reference-type="ref+Label" data-reference="cor:dim-sum-inequality">Corollary 3.73</a>, if $V_1 = L(v_1, \dots, v_n)$ and $V_2 = L(w_1, \dots, w_m)$ are two subspaces of a vector space $V$, then the sum
<div class="arithmatex" markdown="1">
\[
V_1 + V_2 = L(v_1, \dots, v_n, w_1, \dots, w_m).
\]
</div>

For the subspaces $W_1, W_2$ above, this means that we determine the span
<div class="arithmatex" markdown="1">
\[
L(\underbrace{(1,0,1)}_{v_1}, \underbrace{(2,1,0)}_{v_2}, \underbrace{(-1,-1,1)}_{w_1}, \underbrace{(0,3,0)}_{w_2}).
\]
</div>
By <a href="#def-basis" data-reference-type="ref+Label" data-reference="def:basis">Definition 3.58</a><a href="../spaces/#item-generators-remove" data-reference-type="ref" data-reference="item--generators.remove">1.</a>, we obtain a basis of $W_1 + W_2$ by (possibly) removing several of these four vectors. To determine which ones these are, we apply <a href="../spaces/#met-check-linear-independence" data-reference-type="ref+Label" data-reference="met:check-linear-independence">Method 3.53</a> and <a href="../spaces/#met-check-generating-system" data-reference-type="ref+Label" data-reference="met:check-generating-system">Method 3.44</a>. The matrix built out of the four vectors is
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{c} v_1 \\ v_2 \\ w_1 \\ w_2 \end{array} \right ) = \left ( \begin{array}{ccc} 1 & 0 & 1 \\ 2 & 1 & 0 \\ \hline -1 & -1 & 1 \\ 0 & 3 & 0 \end{array} \right ) \leadsto \left ( \begin{array}{ccc} 1 & 0 & 1 \\ 0 & 1 & -2 \\ \hline 0 & -1 & 2 \\ 0 & 3 & 0 \end{array} \right ) \leadsto
\left ( \begin{array}{ccc} 1 & 0 & 1 \\ 0 & 1 & -2 \\ \hline \underline{0} & \underline{0} & \underline{0} \\ 0 & 0 & 6 \end{array} \right ).
\]
</div>
Note that in this process we only added multiples of some rows to another row, but did not interchange any rows. Since we have the zero vector (underlined) in the third row, the vector $w_1$ is a linear combination of $v_1$ and $v_2$. The vectors $v_1, v_2, w_2$ are however linearly independent. Thus, they form a basis of $W_1 + W_2$. In particular, $\dim (W_1 + W_2) = 3$.

An alternative way to determine at least the dimension of $W_1 + W_2$ is to use <a href="../spaces/#thm-dim-cap-sum" data-reference-type="ref+Label" data-reference="thm:dim-cap-sum">Theorem 3.74</a>:
<div class="arithmatex" markdown="1">
\[
\dim (W_1 + W_2) = \dim W_1 + \dim W_2 - \dim (W_1 \cap W_2).
\]
</div>
Using again <a href="../spaces/#met-check-linear-independence" data-reference-type="ref+Label" data-reference="met:check-linear-independence">Method 3.53</a>, one can check that $v_1, v_2$ is a basis of $W_1$, so that $\dim W_1 = 2$ and similarly that $w_1, w_2$ form a basis of $W_2$, so that $\dim W_2 = 2$. Thus, using the first part of the exercise, we confirm $\dim (W_1 + W_2) = 3$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.10.6</strong></p>

<span id="sol-ex-spaces-2-5" label="sol--ex:spaces-2-5"></span> (See <a href="../spaces/#ex-spaces-2-5" data-reference-type="ref+Label" data-reference="ex:spaces-2-5">Exercise 3.27</a>.) We will show that $v_1, v_2, v_3$ are linearly independent (in ${\bf R}^4$ and therefore also in the subspace $W$) and therefore form a basis of $W$. We use <a href="../spaces/#met-check-linear-independence" data-reference-type="ref+Label" data-reference="met:check-linear-independence">Method 3.53</a>:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left ( \begin{array}{c} v_1 \\ v_2 \\ v_3 \end{array} \right ) = & \left ( \begin{array}{cccc} 1 & 0 & 1 & 0 \\ 2 & 0 & 1 & 1 \\ 0 & 0 & 1 & 3 \end{array} \right ) \leadsto \left ( \begin{array}{cccc} 1 & 0 & 1 & 0 \\ 0 & 0 & -1 & 1 \\ 0 & 0 & 1 & 3 \end{array} \right ) 
\leadsto \left ( \begin{array}{cccc} 1 & 0 & 1 & 0 \\ 0 & 0 & 1 & -1 \\ 0 & 0 & 0 & 4 \end{array} \right )\\
\leadsto & \left ( \begin{array}{cccc} 1 & 0 & 1 & 0 \\ 0 & 0 & 1 & -1 \\ 0 & 0 & 0 & 1 \end{array} \right )
\end{align*}
\]
</div>
This matrix has three leading ones, so the vectors are linearly independent as claimed.

We “guess” $v = (1, 2, 3, 4)$ and check that these vectors $v_1, v_2, v_3, v$ are linearly independent. By <a href="../spaces/#lem-independent-linear-combination" data-reference-type="ref+Label" data-reference="lem:independent-linear-combination">Lemma 3.51</a>, this will then imply that $v$ is not a linear combination of the other vectors, so that $W \subsetneq L(v_1, v_2, v_3, v)$. We use <a href="../spaces/#met-check-linear-independence" data-reference-type="ref+Label" data-reference="met:check-linear-independence">Method 3.53</a>:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left ( \begin{array}{cccc} 1 & 0 & 1 & 0 \\ 2 & 0 & 1 & 1 \\ 0 & 0 & 1 & 3 \\ 1 & 2 & 3 & 4 \end{array} \right ) & \leadsto
\left ( \begin{array}{cccc} 1 & 0 & 1 & 0 \\ 0 & 0 & -1 & 1 \\ 0 & 0 & 1 & 3 \\ 0 & 2 & 2 & 4 \end{array} \right ) \leadsto
\left ( \begin{array}{cccc} 1 & 0 & 1 & 0 \\ 0 & 0 & -1 & 1 \\ 0 & 0 & 1 & 3 \\ 0 & 1 & 1 & 2 \end{array} \right ) \\
& \leadsto
\left ( \begin{array}{cccc} \underline1 & 0 & 1 & 0 \\ 0 & 0 & 0 & \underline4 \\ 0 & 0 & \underline1 & 3 \\ 0 & \underline1 & 1 & 2 \end{array} \right )
\end{align*}
\]
</div>
After dividing the second row by 4, we can interchange rows and get a row echelon matrix with four leading ones (underlined). Thus, $v_1, v_2, v_3, v$ are linearly independent. Therefore, they form in fact a basis of ${\bf R}^4$, and we know by <a href="#def-basis" data-reference-type="ref+Label" data-reference="def:basis">Definition 3.58</a><a href="../spaces/#item-dim-subspace" data-reference-type="ref" data-reference="item--dim.subspace">3.</a> that therefore
<div class="arithmatex" markdown="1">
\[
W \subsetneq {\bf R}^4 = L(v_1, v_2, v_3, v).
\]
</div>

<div class="remark" markdown="1">


<p class="env-number"><strong>Remark 3.79</strong></p>

<span id="rem-solutions-remark-001" label="rem:solutions-remark-001"></span> A more systematic way of solving the second part of the exercise, without guessing, is to use <a href="#def-basis" data-reference-type="ref+Label" data-reference="def:basis">Definition 3.58</a>: we can take the standard basis of ${\bf R}^4$, and for (at least) one of the four standard basis vectors $e_1, e_2, e_3, e_4$ we will have that this standard basis vector together with $v_1, v_2, v_3$ form a basis of ${\bf R}^4$. We can then use <a href="../spaces/#met-check-linear-independence" data-reference-type="ref+Label" data-reference="met:check-linear-independence">Method 3.53</a> to see that, for example, $v_1, v_2, v_3, e_1$ are linearly independent and therefore form a basis of ${\bf R}^4$, so that in particular $W \subsetneq L(v_1, v_2, v_3, e_1)$.

</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 3.10.7</strong></p>

<span id="sol-ex-spaces-2-6" label="sol--ex:spaces-2-6"></span> (See <a href="../spaces/#ex-spaces-2-6" data-reference-type="ref+Label" data-reference="ex:spaces-2-6">Exercise 3.28</a>.) We bring the matrix formed by these vectors in row-echelon form:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left ( \begin{array}{cccc} 1 & 0 & -1 & 2 \\ 1 & 0 & 0 & 1 \\ 2 & 0 & -1 & 3 \\ 4 & t & -2 & 6 \end{array} \right ) & \leadsto
\left ( \begin{array}{cccc} 1 & 0 & -1 & 2 \\ 0 & 0 & 1 & -1 \\ 0 & 0 & 1 & -1 \\ 0 & t & 2 & -2 \end{array} \right ) \\
&\leadsto \left ( \begin{array}{cccc} 1 & 0 & -1 & 2 \\ 0 & t & 2 & -2 \\ 0 & 0 & 1 & -1 \\ 0 & 0 & 1 & -1 \end{array} \right ) \\
& \leadsto \left ( \begin{array}{cccc} 1 & 0 & -1 & 2 \\ 0 & t & 2 & -2 \\ 0 & 0 & 1 & -1 \\ 0 & 0 & 0 & 0 \end{array} \right ).
\end{align*}
\]
</div>
If $t \ne 0$, we can divide by $t$, which gives a matrix with three leading ones. Thus, the space $U_t$ which is spanned by these vectors has dimension 3 in this case. If $t = 0$, we continue simplifying the matrix into row echelon form:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left ( \begin{array}{cccc} 1 & 0 & -1 & 2 \\ 0 & t & 2 & -2 \\ 0 & 0 & 1 & -1 \\ 0 & 0 & 0 & 0 \end{array} \right ) & = 
\left ( \begin{array}{cccc} 1 & 0 & -1 & 2 \\ 0 & 0 & 2 & -2 \\ 0 & 0 & 1 & -1 \\ 0 & 0 & 0 & 0 \end{array} \right ) \\
& \leadsto \left ( \begin{array}{cccc} 1 & 0 & -1 & 2 \\ 0 & 0 & 1 & -1 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{array} \right ).
\end{align*}
\]
</div>
This has two leading ones, thus $\dim U_t = 2$ in this case.

We now consider $t = 1$. The subspace $U := U_1$ then has a basis consisting of the non-zero rows if the matrix above, i.e., it has a basis consisting of the vectors
<div class="arithmatex" markdown="1">
\[
(1,0,-1,2), (0,1,2,-2), (0,0,1,-1).
\]
</div>

In order to determine a basis of $W$, we form the matrix associated to these homogeneous equations, which is
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc} 1 & 1 & 1 & 0 \\ 1 & 0 & 0 & -3 \end{array} \right ) \leadsto \left ( \begin{array}{cccc} 1 & 1 & 1 & 0 \\ 0 & -1 & -1 & -3 \end{array} \right ).
\]
</div>
This has two columns not having a leading one, namely the last two. These are the free variables, say $x_3 = a$, $x_4 = b$ for $a , b \in {\bf R}$. To determine a basis of $W$, we therefore have to consider the system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x_1 + x_2 + a & = 0\\
x_2 + a + 3b & = 0
\end{align*}
\]
</div>
This gives $x_2 = -a-3b$, and $x_1 - 3b=0$ so that $x_1 = 3b$. Thus, a basis of $W$ is given by the two vectors
<div class="arithmatex" markdown="1">
\[
(0,-1,1,0) \text{ and }(3,-3,0,1).
\]
</div>

In order to determine $U \cap W$, consider a generic vector of $U$, i.e., one of the form
<div class="arithmatex" markdown="1">
\[
\begin{align*}
v & = a(1,0,-1,2) + b(0,1,2,-2) + c(0,0,1,-1) \\
&= (a,b,-a+2b+c,2a-2b-c).
\end{align*}
\]
</div>
We require it to satisfy the equations describing $W$:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
a+b+(-a+2b+c) & = 0\\
a-3(2a-2b-c) & = 0.
\end{align*}
\]
</div>
Simplifying these expressions gives the system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
3b+c & = 0\\
-5a+6b+3c & = 0.
\end{align*}
\]
</div>
Therefore $c = -3b$, plugging this into the second equation gives, after simplifying, $-5a-3b = 0$ or $a = -\frac35b$. Thus, our vector $v \in U$ belongs to $W$ precisely if it can be written as
<div class="arithmatex" markdown="1">
\[
\begin{align*}
-\frac 35 b(1,0,-1,2)+b(0,1,2,-2)+(-3b)(0,0,1,-1) & = (-\frac 3bb, b, \frac35b+2b-3b,-\frac 65b-2b+3b) \\
&= b(-\frac 35, 1, -\frac25, -\frac15),
\end{align*}
\]
</div>
where $b \in {\bf R}$ is arbitrary. Thus, a basis of $U \cap W$ is this vector
<div class="arithmatex" markdown="1">
\[
(-\frac 35, 1, -\frac 25, -\frac 15).
\]
</div>
In particular, $\dim U \cap W = 1$.

</div>
