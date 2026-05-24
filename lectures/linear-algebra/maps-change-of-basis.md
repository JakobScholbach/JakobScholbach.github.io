---
title: Change of Basis
---

# Change of basis

Let $V$ be a vector space with a basis $v_1, \dots, v_n$. For brevity we write $\underline v$ for this basis. Recall from <a href="../spaces-bases/#prop-basis-coordinate-system" data-reference-type="ref+Label" data-reference="prop:basis-coordinate-system">Proposition 3.64</a> that then any vector $x \in V$ can be written *uniquely* as
<div class="arithmatex" markdown="1">
\[
x = \alpha_1 v_1 + \dots + \alpha_n v_n
\]
</div>
and we regard the coefficients $\alpha_1, \dots, \alpha_n$ as the coordinates of $x$ with respect to the basis $\underline v$. We indicate this notationally by writing $(\alpha_1, \dots, \alpha_n)_{\underline v}$.

If we take, instead, another basis $\underline w$ consisting of vectors $w_1, \dots, w_n \in V$ then
<div class="arithmatex" markdown="1">
\[
x = \beta_1 w_1 + \dots + \beta_n w_n,
\]
</div>
giving *different* coordinates of $x$ with respect to the basis $\underline w$. Our goal in this section is to answer the natural question how to pass from the coordinates $(\alpha_1, \dots, \alpha_n)_{\underline v}$ to $(\beta_1, \dots, \beta_n)_{\underline w}$.

<div class="example" markdown="1">


<p class="env-number"><strong>Example 4.84</strong></p>

<span id="ex-maps-example-026" label="ex:maps-example-026"></span> Consider the identity map ${\mathrm {id}}_V : V \to V$ (<a href="../maps-definition-and-first-examples/#ex-example-linear-maps" data-reference-type="ref+Label" data-reference="ex:example-linear-maps">Example 4.7</a>). We fix a basis $\underline v = \{v_1, \dots, v_n\}$ of $V$ and determine the matrix of ${\mathrm {id}}_V$ with respect to this basis both in the domain and in the codomain. We have
<div class="arithmatex" markdown="1">
\[
\begin{align*}
{\mathrm {id}}_V(v_1) & = v_1 = 1 \cdot v_1 + 0 v_2 + \dots + 0 v_n \\
\vdots \\
{\mathrm {id}}_V(v_n)  & = v_1 =  0 \cdot v_1 + \dots + 0 v_{n-1} + 1 v_n.
\end{align*}
\]
</div>
These coefficients in ${\mathrm {id}}_V(v_i)$ form the $i$-th column of the matrix, which therefore is equal to
<div class="arithmatex" markdown="1">
\[
{\mathrm M}_{ {\mathrm {id}}_V, \underline v, \underline v} = \left ( \begin{array}{cccc} 1 & 0 & \dots & 0 \\ 0 & 1 & \dots & 0 \\ \vdots & & \ddots & \vdots \\ 0 & \dots & 0 & 1 \end{array} \right ) = {\mathrm {id}}_n.
\]
</div>

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 4.85</strong> (Related exercises: <a href="../exercises-spaces/#base-change-matrix">Exercise 3.12</a>)</p>

<span id="ex-base-change-matrix" label="ex:base-change-matrix"></span> We now consider still the identity map ${\mathrm {id}}_V$, but with a basis $\underline v = \{v_1, \dots, v_n\}$ on the domain and another basis $\underline w = \{w_1, \dots, w_n\}$ on the codomain. The matrix of ${\mathrm {id}}_V$ with respect to these bases is found by expressing
<div class="arithmatex" markdown="1">
\[
{\mathrm {id}}_V(v_1) = v_1 = a_{11} w_1 + \dots + a_{n1} w_n
\]
</div>
i.e., we express $v_1$ in coordinates with respect to the basis $\underline w$. More generally, for all $i \le n$:
<div class="arithmatex" markdown="1">
\[
{\mathrm {id}}_V(v_i) = v_1 = a_{1i} w_1 + \dots + a_{ni} w_n.
\]
</div>
The matrix of ${\mathrm {id}}_V$ with respect to the bases $\underline v$ (domain) and $\underline w$ (codomain) is then
<div class="arithmatex" markdown="1">
\[
{\mathrm M}_{ {\mathrm {id}}_V, \underline v, \underline w} = \left ( \begin{array}{cccc} a_{11} & a_{12} & \dots & a_{1n} \\ a_{21} & a_{22} & \dots & a_{2n} \\ \vdots & \vdots & \ddots & \vdots \\ a_{n1} & a_{n2} & \dots & a_{nn} \end{array} \right ).
\]
</div>
We refer to this matrix as the *base change matrix* from $\underline v$ to $\underline w$.

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 4.86</strong></p>

<span id="ex-maps-example-028" label="ex:maps-example-028"></span> Here is a concrete example of the above situation. Let $V = {\bf R}^2$, $\underline v = \{e_1, e_2\} = \{(1,0), (0,1)\}$ be the standard basis and $\underline w = \{w_1, w_2\} = \{(1,1), (1,3)\}$ be another basis. We compute the matrix following the above lines:
<div class="arithmatex" markdown="1">
\[
{\mathrm {id}}_{ {\bf R}^2}(1,0) = (1,0) = a_{11} (1,1) + a_{21} (1,3)
\]
</div>
has the solution $a_{11}=\frac 32$ and $a_{21} = -\frac 12$.
<div class="arithmatex" markdown="1">
\[
{\mathrm {id}}_{ {\bf R}^2}(0,1) = (0,1) = a_{12} (1,1) + a_{22}(1,3)
\]
</div>
has the solution $a_{12} = -\frac 12$, $a_{22}=\frac 12$, so the matrix reads
<div class="arithmatex" markdown="1">
\[
{\mathrm M}_{ {\mathrm {id}}_{ {\bf R}^2}, \underline v, \underline w} = \left ( \begin{array}{cc} \frac 32 & -\frac 12 \\ -\frac 12 & \frac 12 \end{array} \right ).
\]
</div>
Thus, for example, the vector $(3,2) = 3e_1 + 2e_2$ can be expressed as
<div class="arithmatex" markdown="1">
\[
{\mathrm M}_{ {\mathrm {id}}_{ {\bf R}^2}, \underline v, \underline w} {\left ( \begin{array}{c} 3 \\ 2 \end{array} \right )}_{\underline v} = \left ( \begin{array}{cc} \frac 32 & -\frac 12 \\ -\frac 12 & \frac 12 \end{array} \right ) 
{\left ( \begin{array}{c} 3 \\ 2 \end{array} \right )}_{\underline v} = 
{\left ( \begin{array}{c} \frac 72 \\ -\frac 12 \end{array} \right )}_{\underline w},
\]
</div>
i.e.,
<div class="arithmatex" markdown="1">
\[
(3, 2) = \frac 72 w_1 - \frac 12 w_2.
\]
</div>

</div>

By <a href="../maps-composing/#prop-composition-matrices" data-reference-type="ref+Label" data-reference="prop:composition-matrices">Proposition 4.52</a>, the composition of linear maps corresponds to the product of matrices. We apply this to the composition
<div class="arithmatex" markdown="1">
\[
{\mathrm {id}}_V \circ {\mathrm {id}}_V = {\mathrm {id}}_V.
\]
</div>
We choose the following bases on $V$, indicated by a subscript:
<div class="arithmatex" markdown="1">
\[
V_{\underline v} \xrightarrow{ {\mathrm {id}}_V} V_{\underline w} \xrightarrow{ {\mathrm {id}}_V} V_{\underline v}.
\]
</div>
We consider the associated matrices ${\mathrm M}_{ {\mathrm {id}}_V, \underline v, \underline w}$ for the first map, and ${\mathrm M}_{ {\mathrm {id}}_V, \underline w, \underline v}$ for the second one. We have
<div class="arithmatex" markdown="1">
\[
{\mathrm M}_{ {\mathrm {id}}_V, \underline w, \underline v} \cdot {\mathrm M}_{ {\mathrm {id}}_V, \underline v, \underline w} = {\mathrm M}_{ {\mathrm {id}}, \underline v, \underline v} = {\mathrm {id}}_n.
\]
</div>
In other words,
<div class="arithmatex" markdown="1">
\[
{\mathrm M}_{ {\mathrm {id}}_V, \underline w, \underline v} = ({\mathrm M}_{ {\mathrm {id}}_V, \underline v, \underline w})^{-1}.
\]
</div>

The above observations lead to the following.

<div class="method" markdown="1">


<p class="env-number"><strong>Method 4.87</strong></p>

<span id="met-maps-method-001" label="met:maps-method-001"></span> Let $f : V \to V$ be a linear map represented by a matrix $E \in {\mathrm {Mat}}_{n \times n}$ with respect to a fixed basis $\underline v$ on the domain and codomain. The matrix of $f$ with respect to another basis $\underline w$ (again on the domain and the codomain) is
<div class="arithmatex" markdown="1">
\[
{\mathrm M}_{f, \underline w, \underline w} = A E A^{-1},
\]
</div>
where $A$ is the matrix describing the change of basis from $\underline v$ to $\underline w$, i.e., $A = {\mathrm M}_{ {\mathrm {id}}_V, \underline v, \underline w}$ (cf. <a href="#ex-base-change-matrix" data-reference-type="ref+Label" data-reference="ex:base-change-matrix">Example 4.85</a>).

</div>

<div class="proof" markdown="1">

*Proof.* Indeed, $E$ is the matrix for $V_{\underline v} \xrightarrow{f} V_{\underline v}$, which we indicate by writing
<div class="arithmatex" markdown="1">
\[
V_{\underline v} \xrightarrow[E]{f} V_{\underline v}.
\]
</div>
The composition
<div class="arithmatex" markdown="1">
\[
V \xrightarrow{ {\mathrm {id}}_V} V \xrightarrow{f} V \xrightarrow{ {\mathrm {id}}_V} V
\]
</div>
is again $f$, but as above we now put a different basis on $V$:
<div class="arithmatex" markdown="1">
\[
V_{\underline w} \xrightarrow[{\mathrm M}_{ {\mathrm {id}}_V, \underline w, \underline v}]{ {\mathrm {id}}_V} V_{\underline v} \xrightarrow[E]{f} V_{\underline v} \xrightarrow[{\mathrm M}_{ {\mathrm {id}}_V, \underline v, \underline w}] { {\mathrm {id}}_V} V_{\underline w}.
\]
</div>
According to the above, this simplifies to
<div class="arithmatex" markdown="1">
\[
V_{\underline w} \xrightarrow[A^{-1}]{ {\mathrm {id}}_V} V_{\underline v} \xrightarrow[E]{f} V_{\underline v} \xrightarrow[A] { {\mathrm {id}}_V} V_{\underline w}.
\]
</div>
 ◻

</div>

<div class="example" markdown="1">


<p class="env-number"><strong>Example 4.88</strong></p>

<span id="ex-maps-example-029" label="ex:maps-example-029"></span> Consider the linear map $f : {\bf R}^2 \to {\bf R}^2$ given in the standard basis $\underline e = \{e_1, e_2\}$ by multiplication with the matrix $E = \left ( \begin{array}{cc} 2 & 0 \\ -1 & 3 \end{array} \right )$. We compute the matrix associated to $f$ with respect to the basis $\underline w = \{w_1, w_2\} = \{(1,1), (1,-2)\}$ (on the domain and codomain). According to the above, we need to compute the base change matrix $A = {\mathrm M}_{ {\mathrm {id}}, \underline e, \underline w}$ and its inverse $A^{-1} = {\mathrm M}_{ {\mathrm {id}}, \underline w, \underline e}$. The matrix $A^{-1}$ can be computed *more easily* than $A$, because its entries are given by coefficients in the following linear combinations:
<div class="arithmatex" markdown="1">
\[
{\mathrm {id}}(w_1) = w_1 = (1,1) = 1 \cdot e_1 + 1 \cdot e_2,
\]
</div>
<div class="arithmatex" markdown="1">
\[
{\mathrm {id}}(w_2) = w_2 = (1,-2) = 1 \cdot e_1 - 2 \cdot e_2.
\]
</div>
Thus $A^{-1} = \left ( \begin{array}{cc} 1 & 1 \\ 1 & -2 \end{array} \right )$. We compute $A = (A^{-1})^{-1}$ using the method described in <a href="../maps-inverses/#thm-invertible-elimination" data-reference-type="ref+Label" data-reference="thm:invertible-elimination">Theorem 4.81</a>:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
(A^{-1} | {\mathrm {id}}) & = \left ( \begin{array}{cc|cc} 1 & 1 & 1 & 0 \\ 1 & -2 & 0 & 1 \end{array} \right )
\leadsto
\left ( \begin{array}{cc|cc} 1 & 1 & 1 & 0 \\ 0 & -3 & -1 & 1 \end{array} \right )
\\
& \leadsto
\left ( \begin{array}{cc|cc} 1 & 1 & 1 & 0 \\ 0 & 1 & \frac 13 & -\frac 13 \end{array} \right )
\leadsto
\left ( \begin{array}{cc|cc} 1 & 0 & \frac 23 & \frac 13 \\ 0 & 1 & \frac 13 & -\frac 13 \end{array} \right ) \\
& = ({\mathrm {id}} | (A^{-1})^{-1}) = ({\mathrm {id}} | A).
\end{align*}
\]
</div>
This leads to
<div class="arithmatex" markdown="1">
\[
{\mathrm M}_{f, \underline w, \underline w } = A E A^{-1} = 
\left ( \begin{array}{cc} \frac 23 & \frac 13 \\ \frac 13 & -\frac 13 \end{array} \right )
\cdot
\left ( \begin{array}{cc} 2 & 0 \\ -1 & 3 \end{array} \right )
\cdot 
\left ( \begin{array}{cc} 1 & 1 \\ 1 & -2 \end{array} \right ) =
\left ( \begin{array}{cc} 2 & -1 \\ 0 & 3 \end{array} \right ).
\]
</div>

</div>
