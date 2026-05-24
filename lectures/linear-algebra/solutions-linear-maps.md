<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.1</strong></p>

<span id="sol-al" label="sol--al"></span> (See <a href="../exercises-maps/#al" data-reference-type="ref+Label" data-reference="al">Exercise 4.1</a>.) By <a href="../maps-multiplication-of-a-matrix/#def-product-matrix-vector">Definition 4.9</a>, <a href="../maps-multiplication-of-a-matrix/#sect-2-x-2-matrices">Subsection 4.2.1</a>, for $A = \left ( \begin{array}{cc} a_{11} & a_{12} \\ a_{21} & a_{22} \end{array} \right )$ and $v = \left ( \begin{array}{c} x \\ y \end{array} \right )$, we have
<div class="arithmatex" markdown="1">
\[
Av = \left ( \begin{array}{c} a_{11}x+a_{12}y \\ a_{21}x+a_{22}y \end{array} \right ).
\]
</div>
So we determine $A$ by matching the target coordinates.

1.  Reflection along the $y$-axis sends $(x,y) \mapsto (-x,y)$, hence
<div class="arithmatex" markdown="1">
\[
    A = \left ( \begin{array}{cc} -1 & 0 \\ 0 & 1 \end{array} \right ).
\]
</div>

2.  “Same point” means $(x,y) \mapsto (x,y)$, so
<div class="arithmatex" markdown="1">
\[
    A = {\mathrm{id}}_2 = \left ( \begin{array}{cc} 1 & 0 \\ 0 & 1 \end{array} \right ).
\]
</div>

3.  “Always the origin” means $(x,y) \mapsto (0,0)$, so
<div class="arithmatex" markdown="1">
\[
    A = \left ( \begin{array}{cc} 0 & 0 \\ 0 & 0 \end{array} \right ).
\]
</div>

4.  Reflection along the line $\{(x,x)\}$ swaps coordinates: $(x,y) \mapsto (y,x)$, hence
<div class="arithmatex" markdown="1">
\[
    A = \left ( \begin{array}{cc} 0 & 1 \\ 1 & 0 \end{array} \right ).
\]
</div>

5.  By <a href="../maps-multiplication-of-a-matrix/#ex-rotation-matrix-general" data-reference-type="ref+Label" data-reference="ex:rotation-matrix-general">Example 4.18</a>, a counterclockwise rotation by angle $r$ is given by
<div class="arithmatex" markdown="1">
\[
    \left ( \begin{array}{cc} \cos r & -\sin r \\ \sin r & \cos r \end{array} \right ).
\]
</div>
For $r=60^\circ=\pi/3$ this gives
<div class="arithmatex" markdown="1">
\[
    A_{\mathrm{ccw}} = \left ( \begin{array}{cc} \frac12 & -\frac{\sqrt 3}{2} \\ \frac{\sqrt 3}{2} & \frac12 \end{array} \right ).
\]
</div>
Clockwise by $60^\circ$ means $r=-\pi/3$, so
<div class="arithmatex" markdown="1">
\[
    A_{\mathrm{cw}} = \left ( \begin{array}{cc} \frac12 & \frac{\sqrt 3}{2} \\ -\frac{\sqrt 3}{2} & \frac12 \end{array} \right ).
\]
</div>

For comparison with the $90^\circ$ case, see also <a href="../maps-multiplication-of-a-matrix/#ex-rotation-matrix" data-reference-type="ref+Label" data-reference="ex:rotation-matrix">Example 4.17</a>.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.2</strong></p>

<span id="sol-ex-maps-exercise-002" label="sol--ex:maps-exercise-002"></span> (See <a href="../exercises-maps/#ex-maps-exercise-002" data-reference-type="ref+Label" data-reference="ex:maps-exercise-002">Exercise 4.2</a>.) Using <a href="../maps-multiplication-of-a-matrix/#def-product-matrix-vector">Definition 4.9</a>, <a href="../maps-multiplication-of-a-matrix/#sect-2-x-2-matrices">Subsection 4.2.1</a>, for
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{cc} a_{11} & a_{12} \\ a_{21} & a_{22} \end{array} \right )
\]
</div>
and $v=\left ( \begin{array}{c} x \\ y \end{array} \right )$ we have
<div class="arithmatex" markdown="1">
\[
Av = \left ( \begin{array}{c} a_{11}x+a_{12}y \\ a_{21}x+a_{22}y \end{array} \right ).
\]
</div>
We want
<div class="arithmatex" markdown="1">
\[
Av = \left ( \begin{array}{c} -y \\ x \end{array} \right ),
\]
</div>
so comparing coefficients gives $a_{11}=0$, $a_{12}=-1$, $a_{21}=1$, and $a_{22}=0.$ Hence
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{cc} 0 & -1 \\ 1 & 0 \end{array} \right ).
\]
</div>

Geometrically, this is a counterclockwise rotation by $90^\circ$ (equivalently, clockwise by $270^\circ$), compare <a href="../maps-multiplication-of-a-matrix/#ex-rotation-matrix" data-reference-type="ref+Label" data-reference="ex:rotation-matrix">Example 4.17</a>.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.3</strong></p>

<span id="sol-ex-maps-exercise-003" label="sol--ex:maps-exercise-003"></span> (See <a href="../exercises-maps/#ex-maps-exercise-003" data-reference-type="ref+Label" data-reference="ex:maps-exercise-003">Exercise 4.3</a>.) By <a href="../maps-matrices-associated-to-linear-maps/#prop-matrix-to-linear-map" data-reference-type="ref+Label" data-reference="prop:matrix-to-linear-map">Proposition 4.44</a> (applied to the standard basis, cf. <a href="../spaces-bases/#ex-standard-basis" data-reference-type="ref+Label" data-reference="ex:standard-basis">Example 3.62</a>), the columns of the matrix $A$ are exactly the vectors $f(e_1),\dots,f(e_4)$. Hence
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{cccc} 1 & 0 & 0 & 13 \\ 2 & 0 & 0 & 0 \\ 3 & 7 & 0 & -1 \end{array} \right ).
\]
</div>

By <a href="../maps-kernel-and-image-1/#def-kernel" data-reference-type="ref+Label" data-reference="def:kernel">Definition 4.22</a>, to determine $\ker f$, we need to solve $Ax=0$. Since there are so many zeros in the matrix, we do this by hand; alternatively one could also use Gaussian elimination (cf. <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>). With $x=(x_1,x_2,x_3,x_4)^T$, this system reads
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x_1 + 13x_4 & = 0 \\
2x_1 & = 0 \\
3x_1 + 7x_2 - x_4 & = 0.
\end{align*}
\]
</div>
From $2x_1=0$ we get $x_1=0$, then $x_4=0$, then $x_2=0$; $x_3$ is free. So
<div class="arithmatex" markdown="1">
\[
\ker f = L\left(\left ( \begin{array}{c} 0 \\ 0 \\ 1 \\ 0 \end{array} \right )\right), \qquad \dim \ker f = 1.
\]
</div>

To compute the image, we use <a href="../maps-kernel-and-image-2/#prop-basis-row-column-space" data-reference-type="ref+Label" data-reference="prop:basis-row-column-space">Proposition 4.32</a>:
<div class="arithmatex" markdown="1">
\[
\operatorname{im} f = L\left(\left ( \begin{array}{c} 1 \\ 2 \\ 3 \end{array} \right ),
\left ( \begin{array}{c} 0 \\ 0 \\ 7 \end{array} \right ),
\left ( \begin{array}{c} 0 \\ 0 \\ 0 \end{array} \right ),
\left ( \begin{array}{c} 13 \\ 0 \\ -1 \end{array} \right )\right).
\]
</div>
Removing the zero vector, consider
<div class="arithmatex" markdown="1">
\[
u_1=\left ( \begin{array}{c} 1 \\ 2 \\ 3 \end{array} \right ),\quad
u_2=\left ( \begin{array}{c} 0 \\ 0 \\ 7 \end{array} \right ),\quad
u_3=\left ( \begin{array}{c} 13 \\ 0 \\ -1 \end{array} \right ).
\]
</div>
If $a_1u_1+a_2u_2+a_3u_3=0$, then from the second coordinate $2a_1=0$, hence $a_1=0$; from the first coordinate $13a_3=0$, hence $a_3=0$; from the third coordinate $7a_2=0$, hence $a_2=0$. So $u_1,u_2,u_3$ are linearly independent and therefore form a basis of $\operatorname{im} f$. Instead of the above approach, one may also bring $A$ to row-echelon form and observe that the resulting matrix has leading ones in the first, second, and fourth columns, so we again obtain that these three columns of $A$ form a basis of $\operatorname{im} f$ (<a href="../maps-kernel-and-image-2/#prop-basis-row-column-space" data-reference-type="ref+Label" data-reference="prop:basis-row-column-space">Proposition 4.32</a>). In particular,
<div class="arithmatex" markdown="1">
\[
\dim \operatorname{im} f = 3.
\]
</div>
As a check, <a href="../maps-kernel-and-image-1/#thm-rank-nullity-theorem" data-reference-type="ref+Label" data-reference="thm:rank-nullity-theorem">Theorem 4.26</a> gives
<div class="arithmatex" markdown="1">
\[
4 = \dim {\bf R}^4 = \dim \ker f + \dim \operatorname{im} f = 1+3.
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.4</strong></p>

<span id="sol-ex-maps-exercise-004" label="sol--ex:maps-exercise-004"></span> (See <a href="../exercises-maps/#ex-maps-exercise-004" data-reference-type="ref+Label" data-reference="ex:maps-exercise-004">Exercise 4.4</a>.) To compute the rank, we apply <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>, which requires us to bring the matrix into row-echelon form using Gaussian elimination (<a href="../systems-gaussian-elimination/#met-gaussian-algorithm" data-reference-type="ref+Label" data-reference="met:gaussian-algorithm">Method 2.29</a>). We perform the following elementary row operations (<a href="../systems-gaussian-elimination/#def-elementary-row-operations" data-reference-type="ref+Label" data-reference="def:elementary-row-operations">Definition 2.28</a>).

<div class="arithmatex" markdown="1">
\[
\begin{align*}
A = \left ( \begin{array}{cccc} 0 & 1 & 2 & 1 \\ 1 & 1 & 1 & 0 \\ 0 & -1 & 1 & 1 \\ 1 & 1 & 4 & 2 \end{array} \right )
&\leadsto
\left ( \begin{array}{cccc} 1 & 1 & 1 & 0 \\ 0 & 1 & 2 & 1 \\ 0 & -1 & 1 & 1 \\ 1 & 1 & 4 & 2 \end{array} \right ) 
\leadsto
\left ( \begin{array}{cccc} 1 & 1 & 1 & 0 \\ 0 & 1 & 2 & 1 \\ 0 & 0 & 3 & 2 \\ 0 & 0 & 3 & 2 \end{array} \right ) \\
&\leadsto
\left ( \begin{array}{cccc} 1 & 1 & 1 & 0 \\ 0 & 1 & 2 & 1 \\ 0 & 0 & 3 & 2 \\ 0 & 0 & 0 & 0 \end{array} \right ).
\end{align*}
\]
</div>
This row-echelon matrix has exactly 3 leading ones, so by <a href="../maps-kernel-and-image-2/#prop-basis-row-column-space" data-reference-type="ref+Label" data-reference="prop:basis-row-column-space">Proposition 4.32</a> we get $\operatorname{rk}(A) = 3.$

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.5</strong></p>

<span id="sol-ex-maps-exercise-005" label="sol--ex:maps-exercise-005"></span> (See <a href="../exercises-maps/#ex-maps-exercise-005" data-reference-type="ref+Label" data-reference="ex:maps-exercise-005">Exercise 4.5</a>.) From <a href="../maps-linear-maps-defined-on-basis-vectors/#ex-example-map-basis" data-reference-type="ref+Label" data-reference="ex:example-map-basis">Example 4.43</a> we have
<div class="arithmatex" markdown="1">
\[
f(e_1)=f(v_1)=(2,-1,0), \qquad f(e_2)=f(v_2)=(1,-1,1),
\]
</div>
and, since $e_3=v_2-v_3$ there,
<div class="arithmatex" markdown="1">
\[
f(e_3)=f(v_2-v_3)=f(v_2)-f(v_3)=(1,-3,-1).
\]
</div>

By <a href="../maps-multiplication-of-a-matrix/#prop-matrix-linear-map" data-reference-type="ref+Label" data-reference="prop:matrix-linear-map">Proposition 4.19</a>, the matrix of $f$ with respect to the standard basis in source and target has columns $f(e_1),f(e_2),f(e_3)$. Hence
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{ccc} 2 & 1 & 1 \\ -1 & -1 & -3 \\ 0 & 1 & -1 \end{array} \right ).
\]
</div>
This is exactly the matrix already identified in <a href="../maps-linear-maps-defined-on-basis-vectors/#ex-example-map-basis" data-reference-type="ref+Label" data-reference="ex:example-map-basis">Example 4.43</a>.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.6</strong></p>

<span id="sol-ex-maps-exercise-006" label="sol--ex:maps-exercise-006"></span> (See <a href="../exercises-maps/#ex-maps-exercise-006" data-reference-type="ref+Label" data-reference="ex:maps-exercise-006">Exercise 4.6</a>.) Let $v_1=(1,1+\lambda,-1)$, $v_2=(2,\lambda-2,\lambda+2)$. By definition, $W_\lambda=L(v_1,v_2).$ So a basis of $W_\lambda$ is either $\{v_1,v_2\}$ (if they are linearly independent) or a single nonzero vector among them (if they are dependent), cf. <a href="../spaces-linear-independence/#def-linearly-independent">Definition 3.49</a>, <a href="../spaces-bases/#def-basis">Definition 3.61</a>.

To find when they are dependent, check whether $v_2=t v_1$ for some $t\in{\bf R}$. From the first coordinate we get $2=t\cdot 1$, hence $t=2$. Then the second coordinate gives $\lambda-2=2(1+\lambda)$ which holds precisely if $\lambda=-4$. For $\lambda=-4$ the third coordinates also agree. Therefore:

- If $\lambda\neq -4$, the vectors $v_1,v_2$ are linearly independent and therefore a basis of $W_\lambda$. Thus $\dim W_\lambda=2$ by <a href="../spaces-dimension/#def-dimension" data-reference-type="ref+Label" data-reference="def:dimension">Definition 3.66</a>.

- If $\lambda=-4$, then $v_2=2v_1$, so $v_1=(1,-3,-1)$ is a basis vector of $W_{-4}$ (or any other non-zero multiple of it, such as $v_2)$. We have $\dim W_{-4}=1$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.7</strong></p>

<span id="sol-ex-maps-exercise-007" label="sol--ex:maps-exercise-007"></span> (See <a href="../exercises-maps/#ex-maps-exercise-007" data-reference-type="ref+Label" data-reference="ex:maps-exercise-007">Exercise 4.7</a>.) Let $A = \begin{pmatrix} \alpha & 0 & 0 \\ 0 & \alpha & 1+\alpha \\ \alpha & 1 & 2 \end{pmatrix}$ with $\alpha \in \mathbf{R}$. We determine $\operatorname{rank}(A)$ (for all $\alpha$) by bringing $A$ to row-echelon form and applying <a href="../maps-kernel-and-image-2/#prop-basis-row-column-space" data-reference-type="ref+Label" data-reference="prop:basis-row-column-space">Proposition 4.32</a>.

<div class="arithmatex" markdown="1">
\[
A \leadsto \begin{pmatrix}
\alpha & 0 & 0 \\
0 & \alpha & 1+\alpha \\
0 & 1 & 2
\end{pmatrix}
\]
</div>
In order to proceed we need to distinguish whether or not $\alpha = 0$. If $\alpha \neq 0$, we can divide the first row by $\alpha$ (<a href="../systems-gaussian-elimination/#def-elementary-row-operations" data-reference-type="ref+Label" data-reference="def:elementary-row-operations">Definition 2.28</a>)
<div class="arithmatex" markdown="1">
\[
\begin{pmatrix}
1 & 0 & 0 \\
0 & \alpha & 1+\alpha \\
0 & 1 & 2
\end{pmatrix}
\]
</div>
Now, subtract $\frac{1}{\alpha}$ times the second row from the third row (still for $\alpha \neq 0$):
<div class="arithmatex" markdown="1">
\[
\begin{pmatrix}
1 & 0 & 0 \\
0 & \alpha & 1+\alpha \\
0 & 0 & 2 - \frac{1+\alpha}{\alpha}
\end{pmatrix}
\]
</div>
Given that $\alpha \ne 0$, the rank of this matrix is 2 if $2-\frac{1+\alpha}\alpha = 0$, i.e., if $\alpha = 1$, and it is 3 otherwise. This finishes the analysis of the case $\alpha \ne 0$.

If $\alpha = 0$, the matrix reads
<div class="arithmatex" markdown="1">
\[
\begin{pmatrix}
                1 & 0 & 0 \\
                0 & 1 & 2 \\
                0 & 1 & 2
                \end{pmatrix}
\]
</div>
Since the 3rd row equals the 2nd one, one reads off $\operatorname{rank}(A) = 2$ in this case.

In total we get the following result:

- If $\alpha = 1$ or $\alpha = 0$, $\operatorname{rank}(A) = 2$.

- For all other $\alpha \neq 0,1$, $\operatorname{rank}(A) = 3$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.8</strong></p>

<span id="sol-ex-maps-exercise-010" label="sol--ex:maps-exercise-010"></span> (See <a href="../exercises-maps/#ex-maps-exercise-010" data-reference-type="ref+Label" data-reference="ex:maps-exercise-010">Exercise 4.9</a>.) Let $f : \mathbf{R}^4 \to \mathbf{R}^3$ be defined by
<div class="arithmatex" markdown="1">
\[
f\left(\begin{pmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{pmatrix}\right) = \begin{pmatrix} 2 & -1 & 1 & 1 \\ 0 & 5 & -3 & -5 \\ 3 & -4 & 3 & 4 \end{pmatrix} \begin{pmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{pmatrix} = \begin{pmatrix} 2x_1 - x_2 + x_3 + x_4 \\ 5x_2 - 3x_3 - 5x_4 \\ 3x_1 - 4x_2 + 3x_3 + 4x_4 \end{pmatrix}.
\]
</div>

1.  According to <a href="../maps-kernel-and-image-1/#def-kernel" data-reference-type="ref+Label" data-reference="def:kernel">Definition 4.22</a>, we need to compute the solution set of the system
<div class="arithmatex" markdown="1">
\[
    \begin{align*}
            2x_1 - x_2 + x_3 + x_4 &= 0 \\
            5x_2 - 3x_3 - 5x_4 &= 0 \\
            3x_1 - 4x_2 + 3x_3 + 4x_4 &= 0.
    \end{align*}
\]
</div>
We do this using Gaussian elimination (<a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>): we bring the coefficient matrix to row echelon form:
<div class="arithmatex" markdown="1">
\[
    \begin{pmatrix}
            2 & -1 & 1 & 1 \\
            0 & 5 & -3 & -5 \\
            3 & -4 & 3 & 4
        \end{pmatrix}
        \xrightarrow{R_3\leftarrow 2R_3-3R_1}
        \begin{pmatrix}
            2 & -1 & 1 & 1 \\
            0 & 5 & -3 & -5 \\
            0 & -5 & 3 & 5
        \end{pmatrix}
        \xrightarrow{R_3\leftarrow R_3+R_2}
        \begin{pmatrix}
            2 & -1 & 1 & 1 \\
            0 & 5 & -3 & -5 \\
            0 & 0 & 0 & 0
        \end{pmatrix}
\]
</div>
Divide row 2 by $5$, then eliminate the $-1$ in row 1, column 2:
<div class="arithmatex" markdown="1">
\[
    \begin{pmatrix}
            2 & -1 & 1 & 1 \\
            0 & 1 & -\frac35 & -1 \\
            0 & 0 & 0 & 0
        \end{pmatrix}
        \xrightarrow{R_1\leftarrow R_1+R_2}
        \begin{pmatrix}
            2 & 0 & \frac25 & 0 \\
            0 & 1 & -\frac35 & -1 \\
            0 & 0 & 0 & 0
        \end{pmatrix}
        \xrightarrow{R_1\leftarrow \frac12R_1}
        \begin{pmatrix}
            1 & 0 & \frac15 & 0 \\
            0 & 1 & -\frac35 & -1 \\
            0 & 0 & 0 & 0
        \end{pmatrix}.
\]
</div>
Hence $x_3,x_4$ are free, and
<div class="arithmatex" markdown="1">
\[
    x_1=-\frac15x_3,\qquad x_2=\frac35x_3+x_4.
\]
</div>
Writing $x_3=s$, $x_4=t$, we get
<div class="arithmatex" markdown="1">
\[
    \ker f=
        \left\{
        \begin{pmatrix}
        -\frac15 s\\[2pt]
        \frac35 s+t\\[2pt]
        s\\[2pt]
        t
        \end{pmatrix}
        : s,t\in\mathbf R
        \right\}
        =
        L\!\left(
        \begin{pmatrix}-1\\3\\5\\0\end{pmatrix},
        \begin{pmatrix}0\\1\\0\\1\end{pmatrix}
        \right).
\]
</div>

2.  In order to solve $f(v) = \begin{pmatrix} 1 \\ -3 \\ -3 \end{pmatrix}$, we again use Gaussian elimination:
<div class="arithmatex" markdown="1">
\[
    \begin{align*}
            2x_1 - x_2 + x_3 + x_4 &= 1 \\
            5x_2 - 3x_3 - 5x_4 &= -3 \\
            3x_1 - 4x_2 + 3x_3 + 4x_4 &= -3
    \end{align*}
\]
</div>
The augmented matrix is
<div class="arithmatex" markdown="1">
\[
    \begin{align*}
        \left ( \begin{array}{cccc|c} 2 & -1 & 1 & 1 & 1 \\ 0 & 5 & -3 & -5 & -3 \\ 3 & -4 & 3 & 4 & -3 \end{array} \right )
        & \xrightarrow{R_3\leftarrow 2R_3-3R_1}
        \left ( \begin{array}{cccc|c} 2 & -1 & 1 & 1 & 1 \\ 0 & 5 & -3 & -5 & -3 \\ 0 & -5 & 3 & 5 & -9 \end{array} \right ) \\
        & \xrightarrow{R_3\leftarrow R_3+R_2}
        \left ( \begin{array}{cccc|c} 2 & -1 & 1 & 1 & 1 \\ 0 & 5 & -3 & -5 & -3 \\ 0 & 0 & 0 & 0 & -12 \end{array} \right ).
    \end{align*}
\]
</div>
By <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>, the last row implies that there is no solution: this last row would imply $0=-12$, which is false. Therefore the system has no solution, so the preimage is the empty set:
<div class="arithmatex" markdown="1">
\[
    f^{-1}\!\left(\begin{pmatrix}1\\-3\\-3\end{pmatrix}\right)=\emptyset.
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.9</strong></p>

<span id="sol-ex-maps-3-1" label="sol--ex:maps-3-1"></span> (See <a href="../exercises-maps/#ex-maps-3-1" data-reference-type="ref+Label" data-reference="ex:maps-3-1">Exercise 4.8</a>.) By <a href="../maps-kernel-and-image-1/#def-kernel" data-reference-type="ref+Label" data-reference="def:kernel">Definition 4.22</a> $\ker f = \{ \left ( \begin{array}{c} x_1 \\ x_2 \end{array} \right ) \in {\bf R}^2 \ | \ f(\left ( \begin{array}{c} x_1 \\ x_2 \end{array} \right )) = \left ( \begin{array}{c} 0 \\ 0 \\ 0 \end{array} \right ) \}$. I.e., the kernel consists of the solutions of the homongeneous system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x_1+2x_2 & = 0\\
x_2 & = 0 \\
3x_1+5x_2 & = 0.
\end{align*}
\]
</div>
Solving this system gives $x_2 = 0$, then $x_1 = 0$. Thus, $\ker f = \{ \left ( \begin{array}{c} 0 \\ 0 \end{array} \right ) \}$.

For the second part note that by <a href="../maps-kernel-and-image-1/#def-image" data-reference-type="ref+Label" data-reference="def:image">Definition 4.20</a>, ${\operatorname{im}\ } f$ consists precisely of those vectors $\left ( \begin{array}{c} a \\ b \\ c \end{array} \right )$ that are of the form $\left ( \begin{array}{c} a \\ b \\ c \end{array} \right ) = f (\left ( \begin{array}{c} x_1 \\ x_2 \end{array} \right ))$ for some $x_1, x_2 \in {\bf R}$. Thus, the question amounts to this: do there exist $x_1, x_2 \in {\bf R}$ with
<div class="arithmatex" markdown="1">
\[
f (\left ( \begin{array}{c} x_1 \\ x_2 \end{array} \right )) = \left ( \begin{array}{c} x_1+2x_2 \\ x_2 \\ 3x_1+5x_2 \end{array} \right ) = \left ( \begin{array}{c} 1 \\ 0 \\ 3 \end{array} \right )?
\]
</div>
Equivalently, this is a (inhomogeneous) linear system:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x_1+2x_2 & = 1\\
x_2 & = 0 \\
3x_1+5x_2 & = 3.
\end{align*}
\]
</div>
One finds the solution $x_1 = 1$, $x_2 = 0$, i.e., $\left ( \begin{array}{c} 1 \\ 0 \\ 3 \end{array} \right ) = f (\left ( \begin{array}{c} 1 \\ 0 \end{array} \right ))$. So the vector lies in the image.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.10</strong></p>

<span id="sol-ex-maps-3-2" label="sol--ex:maps-3-2"></span> (See <a href="../exercises-maps/#ex-maps-3-2" data-reference-type="ref+Label" data-reference="ex:maps-3-2">Exercise 4.9</a>.) By <a href="../maps-kernel-and-image-1/#def-kernel">Definition 4.22</a>, <a href="../maps-kernel-and-image-1/#def-preimage">Definition 4.20</a>, both questions are about solving linear systems. We use Gaussian elimination as in <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>.

1.  To compute $\ker f$, solve the homogeneous system
<div class="arithmatex" markdown="1">
\[
    \begin{align*}
    2x_1-x_2+x_3+x_4 & = 0 \\
    5x_2-3x_3-5x_4 & = 0\\
    3x_1-4x_2+3x_3+4x_4 & = 0.
    \end{align*}
\]
</div>
Its augmented matrix is
<div class="arithmatex" markdown="1">
\[
    \begin{align*}
    \left ( \begin{array}{cccc|c} 2 & -1 & 1 & 1 & 0\\ 0 & 5 & -3 & -5 & 0\\ 3 & -4 & 3 & 4 & 0 \end{array} \right )
    & \xrightarrow{R_3\leftarrow 2R_3-3R_1}
    \left ( \begin{array}{cccc|c} 2 & -1 & 1 & 1 & 0\\ 0 & 5 & -3 & -5 & 0\\ 0 & -5 & 3 & 5 & 0 \end{array} \right ) \\
    & \xrightarrow{R_3\leftarrow R_3+R_2}
    \left ( \begin{array}{cccc|c} 2 & -1 & 1 & 1 & 0\\ 0 & 5 & -3 & -5 & 0\\ 0 & 0 & 0 & 0 & 0 \end{array} \right ) \\
    & \xrightarrow{R_2\leftarrow \frac15R_2,
    \;R_1\leftarrow R_1+R_2,
    \;R_1\leftarrow \frac12R_1}
    \left ( \begin{array}{cccc|c} 1 & 0 & \frac15 & 0 & 0\\ 0 & 1 & -\frac35 & -1 & 0\\ 0 & 0 & 0 & 0 & 0 \end{array} \right ).
    \end{align*}
\]
</div>
Hence $x_3,x_4$ are free variables and $x_1=-\frac15x_3$, $x_2=\frac35x_3+x_4.$ Putting $x_3=s$, $x_4=t$, this leads to the following basis of the kernel:
<div class="arithmatex" markdown="1">
\[
    \ker f=
    \left\{
    \begin{pmatrix}
    -\frac15 s\\[2pt]
    \frac35 s+t\\[2pt]
    s\\[2pt]
    t
    \end{pmatrix}
    : s,t\in\mathbf R
    \right\}
    =
    L\!\left(
    \begin{pmatrix}-1\\3\\5\\0\end{pmatrix},
    \begin{pmatrix}0\\1\\0\\1\end{pmatrix}
    \right).
\]
</div>

2.  We compute the preimage of $\left(\begin{smallmatrix}1\\-3\\3\end{smallmatrix}\right)$ again using Gaussian elimination, applied to the augmented matrix describing the inhomogeneous system:
<div class="arithmatex" markdown="1">
\[
    \begin{align*}
    \left ( \begin{array}{cccc|c} 2 & -1 & 1 & 1 & 1\\ 0 & 5 & -3 & -5 & -3\\ 3 & -4 & 3 & 4 & 3 \end{array} \right )
    & \xrightarrow{R_3\leftarrow 2R_3-3R_1}
    \left ( \begin{array}{cccc|c} 2 & -1 & 1 & 1 & 1\\ 0 & 5 & -3 & -5 & -3\\ 0 & -5 & 3 & 5 & 3 \end{array} \right ) \\
    &
    \xrightarrow{R_3\leftarrow R_3+R_2}
    \left ( \begin{array}{cccc|c} 2 & -1 & 1 & 1 & 1\\ 0 & 5 & -3 & -5 & -3\\ 0 & 0 & 0 & 0 & 0 \end{array} \right )
    \\
    &
    \xrightarrow{R_2\leftarrow \frac15R_2,
    \;R_1\leftarrow R_1+R_2,
    \;R_1\leftarrow \frac12R_1}
    \left ( \begin{array}{cccc|c} 1 & 0 & \frac15 & 0 & \frac15\\ 0 & 1 & -\frac35 & -1 & -\frac35\\ 0 & 0 & 0 & 0 & 0 \end{array} \right ).
    \end{align*}
\]
</div>
As before, $x_3,x_4$ are free variables
<div class="arithmatex" markdown="1">
\[
    x_1=\frac15-\frac15x_3,\qquad x_2=-\frac35+\frac35x_3+x_4.
\]
</div>
With $x_3=s$, $x_4=t$:
<div class="arithmatex" markdown="1">
\[
    f^{-1}\!\left(\begin{pmatrix}1\\-3\\3\end{pmatrix}\right)
    =
    \begin{pmatrix}\frac15\\-\frac35\\0\\0\end{pmatrix}
    +s\begin{pmatrix}-1\\3\\5\\0\end{pmatrix}
    +t\begin{pmatrix}0\\1\\0\\1\end{pmatrix},\qquad s,t\in\mathbf R.
\]
</div>
Hence this is an affine plane (solution set of an inhomogeneous system), so it is not a subspace (compare <a href="../maps-revisiting-linear-systems/#rem-never-subspace">Remark 4.38</a>, <a href="../maps-revisiting-linear-systems/#thm-solutions-inhomogeneous-system">Theorem 4.37</a>). Alternatively, one may compute this preimage by just finding *one* solution of the inhomogeneous system, such as $(\frac15,-\frac35,0,0)$. Then the preimage is the translate of the kernel by this solution, cf. <a href="../maps-revisiting-linear-systems/#thm-solutions-inhomogeneous-system" data-reference-type="ref+Label" data-reference="thm:solutions-inhomogeneous-system">Theorem 4.37</a>.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.11</strong></p>

<span id="sol-ex-maps-3-3" label="sol--ex:maps-3-3"></span> (See <a href="../exercises-maps/#ex-maps-3-3" data-reference-type="ref+Label" data-reference="ex:maps-3-3">Exercise 4.10</a>.) The rank of $A_t$ is the dimension of its row space, which we compute by bringing $A_t$ to row echelon form (<a href="../maps-kernel-and-image-2/#prop-basis-row-column-space" data-reference-type="ref+Label" data-reference="prop:basis-row-column-space">Proposition 4.32</a>):
<div class="arithmatex" markdown="1">
\[
\begin{align*}
A_t = \left ( \begin{array}{cccc} 1 & 3 & -1 & 2 \\ 1 & 5 & 1 & 1 \\ 2 & 4 & t & 5 \end{array} \right ) & \leadsto \left ( \begin{array}{cccc} 1 & 3 & -1 & 2 \\ 0 & 2 & 2 & -1 \\ 0 & -2 & t+2 & 1 \end{array} \right ) \\
& \leadsto \left ( \begin{array}{cccc} 1 & 3 & -1 & 2 \\ 0 & 2 & 2 & -1 \\ 0 & 0 & t+4 & 0 \end{array} \right ) \\
& \leadsto \left ( \begin{array}{cccc} 1 & 3 & -1 & 2 \\ 0 & 1 & 1 & -\frac12 \\ 0 & 0 & t+4 & 0 \end{array} \right )
\end{align*}
\]
</div>
If $t\ne-4$, then we can further divide the last row by $t+4 (\ne 0)$, and the rank is then 3. For $t = -4$, the rank is 2.

For the last task: the rank of $A_t$ is at most 3. Thus, $\dim {\operatorname{im}\ } f \le 3$, and therefore by the rank-nullity theorem (<a href="../maps-kernel-and-image-1/#thm-rank-nullity-theorem" data-reference-type="ref+Label" data-reference="thm:rank-nullity-theorem">Theorem 4.26</a>)
<div class="arithmatex" markdown="1">
\[
\dim \ker = \dim {\bf R}^4 - \dim {\operatorname{im}\ } f \ge 4 - 3 = 1.
\]
</div>
This means that, for all $t$, the kernel of $f$ does not just consist of the zero vector, hence the answer to the question is no.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.12</strong></p>

<span id="sol-ex-maps-exercise-011" label="sol--ex:maps-exercise-011"></span> (See <a href="../exercises-maps/#ex-maps-exercise-011" data-reference-type="ref+Label" data-reference="ex:maps-exercise-011">Exercise 4.11</a>.) Let $f:V\to W$ be linear and let $U\subset V$ be a subspace.

1.  We verify that $f(U)$ is a subspace of $W$. By definition,
<div class="arithmatex" markdown="1">
\[
    f(U)=\{f(u)\mid u\in U\}\subset W.
\]
</div>
We verify the subspace conditions (<a href="../spaces-definition-solution-of-homogeneous/#def-subspace" data-reference-type="ref+Label" data-reference="def:subspace">Definition 3.17</a>), similarly as in <a href="../maps-kernel-and-image-1/#prop-ker-im-subspace" data-reference-type="ref+Label" data-reference="prop:ker-im-subspace">Proposition 4.23</a>:

    - $0_W\in f(U)$: since $U$ is a subspace, $0_V\in U$, and linearity gives $f(0_V)=0_W$ (<a href="../maps-definition-and-first-examples/#rem-linear-map-basic" data-reference-type="ref+Label" data-reference="rem:linear-map-basic">Remark 4.4</a>).

    - *Closure under addition:* if $y_1,y_2\in f(U)$, then $y_1=f(u_1),y_2=f(u_2)$ for some $u_1,u_2\in U$. Since $U$ is a subspace, $u_1+u_2\in U$, and using the linearity of $f$ (<a href="../maps-definition-and-first-examples/#def-linear-map" data-reference-type="ref+Label" data-reference="def:linear-map">Definition 4.1</a>) we obtain
<div class="arithmatex" markdown="1">
\[
      y_1+y_2=f(u_1)+f(u_2)=f(u_1+u_2)\in f(U).
\]
</div>

- *Closure under scalar multiplication:* if $y=f(u)\in f(U)$ and $\lambda\in\mathbf R$, then $\lambda u\in U$ and again using linearity of $f$:
<div class="arithmatex" markdown="1">
\[
      \lambda y=\lambda f(u)=f(\lambda u)\in f(U).
\]
</div>

Hence $f(U)$ is a subspace of $W$.

2.  We prove $\dim f(U)\le \dim U$. Suppose $(u_1,\dots,u_n)$ is a basis of $U$. (Here we assume for simplicity that $\dim U < \infty$; in general the proof is essentially the same, though.) Then the vectors $f(u_1), \dots, f(u_n) \in W$ span $f(U)$. (Indeed, any $u \in U$ is of the form $u = \sum_{i=1}^n a_i u_i$ for certain (unique) $a_i \in \mathbf R$ (<a href="../spaces-bases/#prop-basis-coordinate-system" data-reference-type="ref+Label" data-reference="prop:basis-coordinate-system">Proposition 3.64</a>). Linearity of $f$ implies $f(u) = \sum_{i=1}^n a_i f(u_i)$, so $f(u)$ is a linear combination of the $f(u_1)$ etc.) Therefore, by the characterization of dimension via spanning sets (<a href="../spaces-dimension/#thm-basis-theorem" data-reference-type="ref+Label" data-reference="thm:basis-theorem">Theorem 3.71</a>),
<div class="arithmatex" markdown="1">
\[
    \dim f(U)\le n=\dim U.
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.13</strong></p>

<span id="sol-ex-maps-exercise-012" label="sol--ex:maps-exercise-012"></span> (See <a href="../exercises-maps/#ex-maps-exercise-012" data-reference-type="ref+Label" data-reference="ex:maps-exercise-012">Exercise 4.12</a>.) Let $f:V\to W$ be linear and let $U\subset W$ be a subspace. By <a href="../maps-kernel-and-image-1/#def-preimage" data-reference-type="ref+Label" data-reference="def:preimage">Definition 4.20</a>, $f^{-1}(U)=\{v\in V\mid f(v)\in U\}$.

We verify the subspace conditions for $f^{-1}(U)$ (<a href="../spaces-definition-solution-of-homogeneous/#def-subspace" data-reference-type="ref+Label" data-reference="def:subspace">Definition 3.17</a>), in the same spirit as <a href="../maps-kernel-and-image-1/#prop-ker-im-subspace" data-reference-type="ref+Label" data-reference="prop:ker-im-subspace">Proposition 4.23</a>.

- *Zero vector:* Since $f$ is linear, $f(0_V)=0_W$ (<a href="../maps-definition-and-first-examples/#rem-linear-map-basic" data-reference-type="ref+Label" data-reference="rem:linear-map-basic">Remark 4.4</a>). Because $U$ is a subspace, $0_W\in U$. Hence $0_V\in f^{-1}(U)$.

- *Closure under addition:* If $v_1,v_2\in f^{-1}(U)$, then $f(v_1),f(v_2)\in U$. Since $U$ is a subspace, $f(v_1)+f(v_2)\in U$. By linearity of $f$ (<a href="../maps-definition-and-first-examples/#def-linear-map" data-reference-type="ref+Label" data-reference="def:linear-map">Definition 4.1</a>), we have
<div class="arithmatex" markdown="1">
\[
  f(v_1+v_2)=f(v_1)+f(v_2)\in U,
\]
</div>
  so $v_1+v_2\in f^{-1}(U)$.

- *Closure under scalar multiplication:* If $v\in f^{-1}(U)$ and $\lambda\in\mathbf R$, then $f(v)\in U$. Since $U$ is a subspace, $\lambda f(v)\in U$. Again using linearity of $f$,
<div class="arithmatex" markdown="1">
\[
  f(\lambda v)=\lambda f(v)\in U,
\]
</div>
  so $\lambda v\in f^{-1}(U)$.

Therefore $f^{-1}(U)$ is a subspace of $V$.

As an aside, we note that the statement of this exercise, applied to $U=\{0_W\}$ this shows again that $f^{-1}(\{0_W\})=\ker f$ is a subspace, which is consistent with <a href="../maps-kernel-and-image-1/#prop-ker-im-subspace" data-reference-type="ref+Label" data-reference="prop:ker-im-subspace">Proposition 4.23</a>.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.14</strong></p>

<span id="sol-ex-maps-3-4" label="sol--ex:maps-3-4"></span> (See <a href="../exercises-maps/#ex-maps-3-4" data-reference-type="ref+Label" data-reference="ex:maps-3-4">Exercise 4.13</a>.) Let
<div class="arithmatex" markdown="1">
\[
A=\begin{pmatrix}
2 & -1 & -\frac52 & 1\\
-1 & 0 & 1 & -\frac12\\
1 & 1 & -\frac12 & \frac12\\
0 & 2 & 1 & 0
\end{pmatrix}.
\]
</div>

We directly bring $A$ to row-echelon form by Gaussian elimination:
<div class="arithmatex" markdown="1">
\[
\begin{pmatrix}
2 & -1 & -\frac52 & 1\\
-1 & 0 & 1 & -\frac12\\
1 & 1 & -\frac12 & \frac12\\
0 & 2 & 1 & 0
\end{pmatrix}
%\xrightarrow{R_1\leftrightarrow R_2,
%\;R_2\leftarrow R_2+2R_1,
%\;R_3\leftarrow R_3+R_1,
%\;R_3\leftarrow R_3+R_2,
%\;R_4\leftarrow R_4+2R_2}
\leadsto
\begin{pmatrix}
-1 & 0 & 1 & -\frac12\\
0 & -1 & -\frac12 & 0\\
0 & 0 & 0 & 0\\
0 & 0 & 0 & 0
\end{pmatrix}
%\xrightarrow{R_1\leftarrow -R_1,\;R_2\leftarrow -R_2}
\leadsto
\begin{pmatrix}
1 & 0 & -1 & \frac12\\
0 & 1 & \frac12 & 0\\
0 & 0 & 0 & 0\\
0 & 0 & 0 & 0
\end{pmatrix}.
\]
</div>
Hence $\operatorname{rk}(A)=2$ and $\dim\ker f=4-2=2$ (by <a href="../maps-kernel-and-image-2/#prop-basis-row-column-space" data-reference-type="ref+Label" data-reference="prop:basis-row-column-space">Proposition 4.32</a> and <a href="../maps-kernel-and-image-1/#thm-rank-nullity-theorem" data-reference-type="ref+Label" data-reference="thm:rank-nullity-theorem">Theorem 4.26</a>).

For $x=(x_1,x_2,x_3,x_4)^T$, the reduced system is
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x_1-x_3+\frac12x_4&=0,\\
x_2+\frac12x_3&=0.
\end{align*}
\]
</div>
With free variables $x_3=s$, $x_4=t$:
<div class="arithmatex" markdown="1">
\[
x=s\begin{pmatrix}1\\-\frac12\\1\\0\end{pmatrix}+t\begin{pmatrix}-\frac12\\0\\0\\1\end{pmatrix}.
\]
</div>
So one convenient basis is
<div class="arithmatex" markdown="1">
\[
\ker f=L\left(\begin{pmatrix}2\\-1\\2\\0\end{pmatrix},\begin{pmatrix}-1\\0\\0\\2\end{pmatrix}\right).
\]
</div>

For the image, use pivot columns (<a href="../maps-kernel-and-image-2/#prop-basis-row-column-space" data-reference-type="ref+Label" data-reference="prop:basis-row-column-space">Proposition 4.32</a>). Pivot columns are 1 and 2, so
<div class="arithmatex" markdown="1">
\[
\operatorname{im} f=L(c_1,c_2),\quad c_1=\begin{pmatrix}2\\-1\\1\\0\end{pmatrix},\ c_2=\begin{pmatrix}-1\\0\\1\\2\end{pmatrix}.
\]
</div>

Now compute $\ker f\cap\operatorname{im} f$, the intersection of these two subspaces (cf. <a href="../spaces-intersection/#sect-intersection-of-subspaces" data-reference-type="ref+Label" data-reference="sect:intersection-of-subspaces">Section 3.3</a>). A general vector in the image has the form
<div class="arithmatex" markdown="1">
\[
y=ac_1+bc_2=\begin{pmatrix}2a-b\\-a\\a+b\\2b\end{pmatrix}.
\]
</div>
In order to determine when this lies in the intersection, we also impose the kernel equations on $y$:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
y_1-y_3+\frac12y_4=(2a-b)-(a+b)+b=a-b & =0,\\
y_2+\frac12y_3=-a+\frac12(a+b)=\frac{-a+b}{2} & =0.
\end{align*}
\]
</div>
Thus $a=b$, and therefore
<div class="arithmatex" markdown="1">
\[
y=a(c_1+c_2)=a\begin{pmatrix}1\\-1\\2\\2\end{pmatrix}.
\]
</div>
Hence
<div class="arithmatex" markdown="1">
\[
\ker f\cap\operatorname{im} f=L\left(\begin{pmatrix}1\\-1\\2\\2\end{pmatrix}\right).
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.15</strong></p>

<span id="sol-ex-maps-exercise-013" label="sol--ex:maps-exercise-013"></span> (See <a href="../exercises-maps/#ex-maps-exercise-013" data-reference-type="ref+Label" data-reference="ex:maps-exercise-013">Exercise 4.14</a>.) Let
<div class="arithmatex" markdown="1">
\[
f:{\bf R}^3\to{\bf R}^2,\qquad f(x,y,z)=(2x-z,\,x+y+z).
\]
</div>

1.  With respect to the standard bases, the matrix is obtained from the coefficients of $x,y,z$ in each component (<a href="../maps-matrices-associated-to-linear-maps/#prop-matrix-to-linear-map" data-reference-type="ref+Label" data-reference="prop:matrix-to-linear-map">Proposition 4.44</a>):
<div class="arithmatex" markdown="1">
\[
    A=\begin{pmatrix}
    2&0&-1\\
    1&1&1
    \end{pmatrix}.
\]
</div>

2.  We bring $A$ to row-echelon form and read off both kernel and image:
<div class="arithmatex" markdown="1">
\[
    \begin{pmatrix}
    2&0&-1\\
    1&1&1
    \end{pmatrix}
    \xrightarrow{R_1\leftrightarrow R_2}
    \begin{pmatrix}
    1&1&1\\
    2&0&-1
    \end{pmatrix}
    \xrightarrow{R_2-2R_1}
    \begin{pmatrix}
    1&1&1\\
    0&-2&-3
    \end{pmatrix}
    \xrightarrow{R_2\leftarrow-\frac12R_2}
    \begin{pmatrix}
    1&1&1\\
    0&1&\frac32
    \end{pmatrix}
    \xrightarrow{R_1-R_2}
    \begin{pmatrix}
    1&0&-\frac12\\
    0&1&\frac32
    \end{pmatrix}.
\]
</div>
Hence, solving $A\begin{pmatrix}x\\y\\z\end{pmatrix}=0$, we get
<div class="arithmatex" markdown="1">
\[
    x-\frac12z=0,\qquad y+\frac32z=0.
\]
</div>
With free parameter $z=2t$, this gives $x=t$, $y=-3t$, so
<div class="arithmatex" markdown="1">
\[
    \ker f=L\left(\begin{pmatrix}1\\-3\\2\end{pmatrix}\right),\qquad \dim\ker f=1.
\]
</div>

For the image, the pivot columns are the first and second. Therefore, by <a href="../maps-kernel-and-image-2/#prop-basis-row-column-space" data-reference-type="ref+Label" data-reference="prop:basis-row-column-space">Proposition 4.32</a>, a basis of ${\operatorname{im}\,}f$ is given by the corresponding columns of the original matrix:
<div class="arithmatex" markdown="1">
\[
    c_1=\begin{pmatrix}2\\1\end{pmatrix},\qquad c_2=\begin{pmatrix}0\\1\end{pmatrix}.
\]
</div>
Hence
<div class="arithmatex" markdown="1">
\[
    \operatorname{im} f=L(c_1,c_2)={\bf R}^2,\qquad \dim\operatorname{im}f=2.
\]
</div>

3.  By <a href="../maps-kernel-and-image-1/#def-preimage" data-reference-type="ref+Label" data-reference="def:preimage">Definition 4.20</a>, $f^{-1}((0,1))$ is the solution set of the linear system
<div class="arithmatex" markdown="1">
\[
    \begin{align*}
    2x-z&=0,\\
    x+y+z&=1.
    \end{align*}
\]
</div>
One may again solve this by Gaussian elimination, or by inspection: $z=2x$, and then $y=1-3x$. With parameter $t:=x$:
<div class="arithmatex" markdown="1">
\[
    f^{-1}((0,1))=\left\{\begin{pmatrix}t\\1-3t\\2t\end{pmatrix}:t\in{\bf R}\right\}
    =\begin{pmatrix}0\\1\\0\end{pmatrix}+t\begin{pmatrix}1\\-3\\2\end{pmatrix}.
\]
</div>
This is an affine line (solution set of an inhomogeneous system), not a subspace of ${\bf R}^3$ because it does not contain $0$ (compare <a href="../maps-revisiting-linear-systems/#rem-never-subspace">Remark 4.38</a>, <a href="../maps-revisiting-linear-systems/#thm-solutions-inhomogeneous-system">Theorem 4.37</a>).

4.  Let
<div class="arithmatex" markdown="1">
\[
    v_1=(0,1,2),\quad v_2=(0,-1,1),\quad v_3=(1,1,1).
\]
</div>
To check they form a basis of ${\bf R}^3$, put them as rows and bring to row-echelon form:
<div class="arithmatex" markdown="1">
\[
    M=\begin{pmatrix}
    0&1&2\\
    0&-1&1\\
    1&1&1
    \end{pmatrix}
    \xrightarrow{R_1\leftrightarrow R_3}
    \begin{pmatrix}
    1&1&1\\
    0&-1&1\\
    0&1&2
    \end{pmatrix}
    \xrightarrow{R_3+R_2}
    \begin{pmatrix}
    1&1&1\\
    0&-1&1\\
    0&0&3
    \end{pmatrix}.
\]
</div>
This echelon matrix has three nonzero rows, hence $\operatorname{rk}(M)=3$, for example by <a href="../maps-transpose/#cor-rows-columns-independent" data-reference-type="ref+Label" data-reference="cor:rows-columns-independent">Corollary 4.94</a>. Therefore $v_1,v_2,v_3$ are linearly independent and form a basis of ${\bf R}^3$.

    The matrix of $f$ with respect to this domain basis and the standard basis in ${\bf R}^2$ has columns $f(v_1),f(v_2),f(v_3)$:
<div class="arithmatex" markdown="1">
\[
    \begin{align*}
    f(v_1)&=f(0,1,2)=(-2,3),\\
    f(v_2)&=f(0,-1,1)=(-1,0),\\
    f(v_3)&=f(1,1,1)=(1,3).
    \end{align*}
\]
</div>
So the wanted matrix is
<div class="arithmatex" markdown="1">
\[
    \mathrm M_{\{v_1, v_2, v_3\},\{e_1, e_2\}}=
    \begin{pmatrix}
    -2&-1&1\\
    3&0&3
    \end{pmatrix}.
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.16</strong></p>

<span id="sol-ex-maps-3-5" label="sol--ex:maps-3-5"></span> (See <a href="../exercises-maps/#ex-maps-3-5" data-reference-type="ref+Label" data-reference="ex:maps-3-5">Exercise 4.15</a>.) We have $v_1 = (1,1,0)$, and compute
<div class="arithmatex" markdown="1">
\[
v_2 = \left ( \begin{array}{ccc} 2 & -1 & 0 \\ 1 & 0 & 2 \\ 0 & 2 & -1 \end{array} \right ) \left ( \begin{array}{c} 1 \\ 1 \\ 0 \end{array} \right ) = \left ( \begin{array}{c} 1 \\ 1 \\ 2 \end{array} \right ),
\]
</div>
<div class="arithmatex" markdown="1">
\[
v_3 = \left ( \begin{array}{ccc} 2 & -1 & 0 \\ 1 & 0 & 2 \\ 0 & 2 & -1 \end{array} \right ) \left ( \begin{array}{c} 1 \\ 1 \\ 2 \end{array} \right ) = \left ( \begin{array}{c} 1 \\ 5 \\ 0 \end{array} \right ).
\]
</div>
In order to confirm that they form a basis, we apply <a href="../spaces-linear-combinations/#met-check-generating-system" data-reference-type="ref+Label" data-reference="met:check-generating-system">Method 3.46</a> and <a href="../spaces-linear-independence/#met-check-linear-independence" data-reference-type="ref+Label" data-reference="met:check-linear-independence">Method 3.56</a> by forming the associated matrix and bringing it into row echelon form:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left ( \begin{array}{ccc} 1 & 1 & 0 \\ 1 & 1 & 2 \\ 1 & 5 & 0 \end{array} \right ) & \leadsto
\left ( \begin{array}{ccc} 1 & 1 & 0 \\ 0 & 1 & 2 \\ -4 & 0 & 0 \end{array} \right ) \\
& \leadsto \left ( \begin{array}{ccc} 1 & 1 & 0 \\ 0 & 1 & 2 \\ 0 & 4 & 0 \end{array} \right ) \\
& \leadsto \left ( \begin{array}{ccc} 1 & 1 & 0 \\ 0 & 1 & 2 \\ 0 & 0 & -8 \end{array} \right ) \\
& \leadsto \left ( \begin{array}{ccc} 1 & 1 & 0 \\ 0 & 1 & 2 \\ 0 & 0 & 1 \end{array} \right ). \\
\end{align*}
\]
</div>
This matrix has three leading ones, so that the vectors do form a basis.

We compute $v_4 = f(v_3) = \left ( \begin{array}{ccc} 2 & -1 & 0 \\ 1 & 0 & 2 \\ 0 & 2 & -1 \end{array} \right ) \left ( \begin{array}{c} 1 \\ 5 \\ 0 \end{array} \right ) = \left ( \begin{array}{c} -3 \\ 1 \\ 10 \end{array} \right )$. The equation $v_4 = a_1 v_1 + a_2 v_2 + a_3 v_3$ is the linear system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
a_1 + a_2 + a_3 & = {-3} \\
a_1 + a_2 + 5a_3 &= 1 \\
2a_2 & = 10.
\end{align*}
\]
</div>
We solve this: the last equation gives $a_2 = 5$, which leads to
<div class="arithmatex" markdown="1">
\[
\begin{align*}
a_1 + 5 + a_3 & = -3 \\
a_1 + 5 + 5a_3 & = 1.
\end{align*}
\]
</div>
Therefore
<div class="arithmatex" markdown="1">
\[
\begin{align*}
a_1 + a_3 & = -8 \\
a_1 + 5a_3 & = -4.
\end{align*}
\]
</div>
This can be solved to $a_3 = 1$ and $a_1 = -9$. Thus, $(a_1, a_2, a_3) = (1,5,-9)$ are the coordinates of $v_4$ in the basis $v_1, v_2, v_3$.

We now determine the matrix of $f$ with respect to the basis $v_1, v_2, v_3$ (both in the domain and the codomain of $f$). We therefore write each $f(v_i)$ as a linear combination of these three vectors:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
f(v_1) = v_2 &= 0v_1 + 1 v_2 + 0 v_3 \\
f(v_2) = v_3 & =0v_1 + 0v_2+1v_3 \\
f(v_3) = v_4 & = -9v_1 + 5v_2 + v_3.
\end{align*}
\]
</div>
According to <a href="../maps-matrices-associated-to-linear-maps/#prop-matrix-to-linear-map" data-reference-type="ref+Label" data-reference="prop:matrix-to-linear-map">Proposition 4.44</a>, the matrix of $f$ with respect to $v_1, v_2, v_3$ is
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc} 0 & 0 & -9 \\ 1 & 0 & 5 \\ 0 & 1 & 1 \end{array} \right ).
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.17</strong></p>

<span id="sol-ex-maps-3-6" label="sol--ex:maps-3-6"></span> (See <a href="../exercises-maps/#ex-maps-3-6" data-reference-type="ref+Label" data-reference="ex:maps-3-6">Exercise 4.16</a>.) The map is $f(x,y,z,t)=(-x+z,\,-y+t,\,x-y)$. Applying $f$ to the standard basis vectors $e_1,e_2,e_3,e_4$ of $\mathbf{R}^4$ gives the columns of the matrix (<a href="../maps-matrices-associated-to-linear-maps/#prop-matrix-to-linear-map" data-reference-type="ref+Label" data-reference="prop:matrix-to-linear-map">Proposition 4.44</a>):
<div class="arithmatex" markdown="1">
\[
A = \begin{pmatrix} -1 & 0 & 1 & 0 \\ 0 & -1 & 0 & 1 \\ 1 & -1 & 0 & 0 \end{pmatrix}.
\]
</div>

We compute the kernel by solving $Av=0$ by row reduction (<a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>):
<div class="arithmatex" markdown="1">
\[
\begin{pmatrix} -1 & 0 & 1 & 0 \\ 0 & -1 & 0 & 1 \\ 1 & -1 & 0 & 0 \end{pmatrix}
  \longrightarrow
  \begin{pmatrix} 1 & 0 & -1 & 0 \\ 0 & 1 & 0 & -1 \\ 0 & -1 & 1 & 0 \end{pmatrix}
  \longrightarrow
  \begin{pmatrix} 1 & 0 & -1 & 0 \\ 0 & 1 & 0 & -1 \\ 0 & 0 & 1 & -1 \end{pmatrix}
  \longrightarrow
  \begin{pmatrix} 1 & 0 & 0 & -1 \\ 0 & 1 & 0 & -1 \\ 0 & 0 & 1 & -1 \end{pmatrix}.
\]
</div>
The free variable is $t$; setting $t=\lambda$ gives $x=\lambda$, $y=\lambda$, $z=\lambda$, so
<div class="arithmatex" markdown="1">
\[
\ker f = \operatorname{span}\!\left\{\begin{pmatrix}1\\1\\1\\1\end{pmatrix}\right\}, \qquad \dim\ker f = 1.
\]
</div>

*Image.* By the rank–nullity theorem (<a href="../maps-kernel-and-image-1/#thm-rank-nullity-theorem" data-reference-type="ref+Label" data-reference="thm:rank-nullity-theorem">Theorem 4.26</a>), we have $\dim\operatorname{im} f = \dim\mathbf{R}^4 - \dim\ker f = 4 - 1 = 3.$ Since $\operatorname{im} f \subseteq \mathbf{R}^3$ and has dimension $3$, we conclude from <a href="../spaces-dimension/#thm-basis-theorem" data-reference-type="ref+Label" data-reference="thm:basis-theorem">Theorem 3.71</a> that $\operatorname{im} f = \mathbf{R}^3$. Alternatively, using <a href="../maps-kernel-and-image-2/#prop-basis-row-column-space" data-reference-type="ref+Label" data-reference="prop:basis-row-column-space">Proposition 4.32</a>, the first three columns of $A$ above are another basis of $\operatorname{im} f$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.18</strong></p>

<span id="sol-ex-maps-3-7" label="sol--ex:maps-3-7"></span> (See <a href="../exercises-maps/#ex-maps-3-7" data-reference-type="ref+Label" data-reference="ex:maps-3-7">Exercise 4.17</a>.)

1.  We check the linearity of the functions.

    $f_1$ is linear: $f_1(x)=(x_1+x_2,\,3x_1,\,2x_2)$ is given by multiplying with the matrix $\begin{pmatrix}1&1\\3&0\\0&2\end{pmatrix}$, so it is linear by <a href="../maps-multiplication-of-a-matrix/#prop-matrix-linear-map" data-reference-type="ref+Label" data-reference="prop:matrix-linear-map">Proposition 4.19</a>. Alternatively, one may also check the linearity directly by applying <a href="../maps-definition-and-first-examples/#def-linear-map" data-reference-type="ref+Label" data-reference="def:linear-map">Definition 4.1</a>.

    $f_2$ is *not* linear: $f_2(0)=(0,1)\neq(0,0)$, violating $f(0)=0$ (<a href="../maps-definition-and-first-examples/#rem-linear-map-basic" data-reference-type="ref+Label" data-reference="rem:linear-map-basic">Remark 4.4</a>).

    $f_3$ is *not* linear: the first component $x_3^2$ is not a linear function of $(x_1,x_2,x_3)$ (e.g. $f_3(2e_3)=(4,0)\neq 2f_3(e_3)=(2,0)$).

    The identity map $f_4$ is linear (cf. <a href="../maps-definition-and-first-examples/#ex-example-linear-maps" data-reference-type="ref+Label" data-reference="ex:example-linear-maps">Example 4.7</a>).

    $f_5$ is linear: $f_5(x)=(x_1+x_2,\,x_2+x_3,\,x_3+x_1)$ is given by multiplication with the matrix $\begin{pmatrix}1&1&0\\0&1&1\\1&0&1\end{pmatrix}$.

2.  We describe the images of these functions.

    For the linear map $f_1$, we can use <a href="../maps-kernel-and-image-2/#prop-image-column-space" data-reference-type="ref+Label" data-reference="prop:image-column-space">Proposition 4.30</a>, according to which $\operatorname{im} f_1 = \operatorname{span}\!\left\{\begin{pmatrix}1\\3\\0\end{pmatrix},\begin{pmatrix}1\\0\\2\end{pmatrix}\right\}$, a $2$-dimensional subspace of $\mathbf{R}^3$ (the two columns are linearly independent).

    $f_2$ is not linear, but its image is $\{(x_3+x_1,\,3x_2+4x_1+1)\mid x\in\mathbf{R}^3\}=\mathbf{R}^2$ (e.g. vary $x_1,x_2,x_3$ freely).

    We have $\operatorname{im} (f_3) = \{(x_3^2,\,x_2+x_1)\mid x\in\mathbf{R}^3\} = [0,\infty)\times\mathbf{R}$ (its first component is a square, the second one is arbitrary).

    We clearly have $\operatorname{im} f_4 = \mathbf{R}^3$.

    For $f_5$, let $\left ( \begin{array}{c} a \\ b \\ c \end{array} \right ) \in \mathbf{R}^3$. To decide whether it lies in the image, we solve
<div class="arithmatex" markdown="1">
\[
    \begin{align*}
    x_1+x_2 & = a \\
    x_2+x_3 & = b \\
    x_3+x_1 & = c.
    \end{align*}
\]
</div>
Solving this, for example using Gaussian elimination, one finds the following solutions:
<div class="arithmatex" markdown="1">
\[
    x_1=\frac{a-b+c}{2}, \qquad x_2=\frac{a+b-c}{2}, \qquad x_3=\frac{-a+b+c}{2}.
\]
</div>
Thus for every $\left ( \begin{array}{c} a \\ b \\ c \end{array} \right ) \in \mathbf{R}^3$ there is a solution, so $\operatorname{im} f_5=\mathbf{R}^3$.

3.  *Injectivity and surjectivity (for the linear maps $f_1,f_4,f_5$).* For the linear maps we can use the rank-nullity theorem (<a href="../maps-kernel-and-image-1/#thm-rank-nullity-theorem" data-reference-type="ref+Label" data-reference="thm:rank-nullity-theorem">Theorem 4.26</a>) and our knowledge about the image to determine injectivity. Recall from <a href="../maps-kernel-and-image-1/#lem-injective-ker" data-reference-type="ref+Label" data-reference="lem:injective-ker">Lemma 4.25</a> that a linear map $f$ is injective precisely if its kernel $\ker f$ consists only of the zero vector, or equivalently if $\dim \ker f = 0$.

    For $f_1$: the domain is $\mathbf{R}^2$, we have seen $\dim\operatorname{im} f_1=\dim\mathbf{R}^2=2$, so $\ker f_1=\{0\}$ by rank–nullity (<a href="../maps-kernel-and-image-1/#thm-rank-nullity-theorem" data-reference-type="ref+Label" data-reference="thm:rank-nullity-theorem">Theorem 4.26</a>), so $f_1$ is injective. It is not surjective since $\dim \operatorname{im} f_1 = 2 < 3 = \dim \mathbf{R}^3$.

    The identity map $f_4$ is bijective (i.e., injective and surjective).

    The map $f_5$ is also bijective. To see this, we again use rank-nullity, which implies $\dim \ker f_5 = 3 - \dim \operatorname{im} (f_5) = 3 - 3 = 0$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.19</strong></p>

<span id="sol-ex-maps-exercise-014" label="sol--ex:maps-exercise-014"></span> (See <a href="../exercises-maps/#ex-maps-exercise-014" data-reference-type="ref+Label" data-reference="ex:maps-exercise-014">Exercise 4.18</a>.)

1.  Put the vectors as rows of a matrix and row-reduce:
<div class="arithmatex" markdown="1">
\[
    M=\begin{pmatrix}
    v_1\\
    v_2\\
    v_3
    \end{pmatrix} = \begin{pmatrix}
    1&2&-3&-1\\
    3&4&4&1\\
    1&0&10&3
    \end{pmatrix}
    \xrightarrow{R_2-3R_1,\;R_3-R_1}
    \begin{pmatrix}
    1&2&-3&-1\\
    0&-2&13&4\\
    0&-2&13&4
    \end{pmatrix}
    \xrightarrow{R_3-R_2}
    \begin{pmatrix}
    1&2&-3&-1\\
    0&-2&13&4\\
    0&0&0&0
    \end{pmatrix}.
\]
</div>
This row-echelon matrix has two nonzero rows, so by <a href="../maps-kernel-and-image-2/#prop-basis-row-column-space" data-reference-type="ref+Label" data-reference="prop:basis-row-column-space">Proposition 4.32</a> we read off
<div class="arithmatex" markdown="1">
\[
    \dim U=2,
\]
</div>
where $U=L(v_1,v_2,v_3)$. A basis of $U$ is given by the nonzero rows of the echelon form:
<div class="arithmatex" markdown="1">
\[
    \left\{(1,2,-3,-1),\,(0,-2,13,4)\right\}.
\]
</div>
(From the row operation $R_3-R_1=R_2-3R_1$ we get
<div class="arithmatex" markdown="1">
\[
    v_2=2v_1+v_3,
\]
</div>
so equivalently $U=L(v_1,v_3)$, i.e., $v_1$ and $v_3$ also form a basis of $U$.)

2.  We extend two independent vectors to a basis of ${\bf R}^4$. For example, take
<div class="arithmatex" markdown="1">
\[
    e_1=(1,0,0,0),\qquad e_2=(0,1,0,0).
\]
</div>
Then the vectors $v_1,v_3,e_1,e_2$ form a basis of ${\bf R}^4$. To check their linear independence, we again form the matrix comprised of these vectors
<div class="arithmatex" markdown="1">
\[
    \begin{pmatrix}
    1&2&-3&-1\\
    1&0&10&3\\
    1&0&0&0\\
    0&1&0&0
    \end{pmatrix},
\]
</div>
One checks that the rank of this matrix is 4. Thus the rows are linearly independent, hence form a basis of ${\bf R}^4$.

3.  Yes, such an $f:{\bf R}^4\to{\bf R}^2$ exists. Define it on the basis $v_1,v_3,e_1,e_2$ by
<div class="arithmatex" markdown="1">
\[
    f(v_1)=(1,0),\qquad f(v_3)=(0,1),\qquad f(e_1)=(0,0),\qquad f(e_2)=(0,0)
\]
</div>
(or any other choices for $f(e_1)$, $f(e_2)$ would also do). By <a href="../maps-linear-maps-defined-on-basis-vectors/#prop-linear-map-defined-on-basis" data-reference-type="ref+Label" data-reference="prop:linear-map-defined-on-basis">Proposition 4.40</a>, this determines a unique linear map $f:{\bf R}^4\to{\bf R}^2$. Since $U=L(v_1,v_3)$, we get
<div class="arithmatex" markdown="1">
\[
    f(U)=L(f(v_1),f(v_3))=L((1,0),(0,1))={\bf R}^2.
\]
</div>

For $g:{\bf R}^4\to{\bf R}^3$, the answer is no. Indeed, the restriction
<div class="arithmatex" markdown="1">
\[
    g_{|U}:U\to {\bf R}^3
\]
</div>
is a linear map with image $g(U)$. By <a href="../maps-kernel-and-image-2/#cor-maps-dim" data-reference-type="ref+Label" data-reference="cor:maps-dim">Corollary 4.28</a>,
<div class="arithmatex" markdown="1">
\[
    \dim g(U)\le \dim U=2.
\]
</div>
Therefore $g(U)$ cannot be all of ${\bf R}^3$, since ${\bf R}^3$ has dimension $3$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.20</strong></p>

<span id="sol-ex-maps-example-031" label="sol--ex:maps-example-031"></span> (See <a href="../exercises-maps/#ex-maps-example-031" data-reference-type="ref+Label" data-reference="ex:maps-example-031">Exercise 4.19</a>.) We attempt to invert $A$ by row-reducing the augmented matrix $[A\mid I]$:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
  \left ( \begin{array}{ccc|ccc} 1 & 3 & -1 & 1 & 0 & 0 \\ 2 & 1 & 5 & 0 & 1 & 0 \\ 1 & -7 & 13 & 0 & 0 & 1 \end{array} \right )
&  \xrightarrow{R_2-2R_1,\;R_3-R_1}
  \left ( \begin{array}{ccc|ccc} 1 & 3 & -1 & 1 & 0 & 0 \\ 0 & -5 & 7 & -2 & 1 & 0 \\ 0 & -10 & 14 & -1 & 0 & 1 \end{array} \right ) \\
 & \xrightarrow{R_3-2R_2}
  \left ( \begin{array}{ccc|ccc} 1 & 3 & -1 & 1 & 0 & 0 \\ 0 & -5 & 7 & -2 & 1 & 0 \\ 0 & 0 & 0 & 3 & -2 & 1 \end{array} \right ).
\end{align*}
\]
</div>
The third row of the left block is all zeros, so $A$ does not row-reduce to the identity. Therefore $A$ is *not* invertible, according to <a href="../maps-inverses/#thm-invertible-elimination" data-reference-type="ref+Label" data-reference="thm:invertible-elimination">Theorem 4.81</a>.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.21</strong></p>

<span id="sol-matrices-commute" label="sol--matrices.commute"></span> (See <a href="../exercises-maps/#matrices-commute" data-reference-type="ref+Label" data-reference="matrices.commute">Exercise 4.20</a>.) We compute $AB$ and $BA$ in each case, by applying <a href="../maps-composing/#def-product-matrices" data-reference-type="ref+Label" data-reference="def:product-matrices">Definition 4.49</a>:

1.  For $A=\begin{pmatrix}1&2\\2&1\end{pmatrix}$, $B=\begin{pmatrix}0&1\\-1&1\end{pmatrix}$ we obtain $AB=\begin{pmatrix}-2&3\\-1&3\end{pmatrix}$, as opposed to $BA=\begin{pmatrix}2&1\\1&-1\end{pmatrix}$. Hence $AB\neq BA$, confirming that matrix multiplication is in general not commutative, cf. <a href="../maps-composing/#war-not-commutative" data-reference-type="ref+Label" data-reference="war:not-commutative">Warning 4.55</a>.

2.  For $A=\begin{pmatrix}3&0\\0&4\end{pmatrix}$, $B=\begin{pmatrix}-1&0\\0&2\end{pmatrix}$ we compute $AB=\begin{pmatrix}-3&0\\0&8\end{pmatrix}$, which happens to be equal to $BA=\begin{pmatrix}-3&0\\0&8\end{pmatrix}$.

3.  For $A=\begin{pmatrix}1&x\\0&1\end{pmatrix}$ and $B=\begin{pmatrix}y&1\\0&y\end{pmatrix}$ we get
<div class="arithmatex" markdown="1">
\[
    AB=BA=\begin{pmatrix}-3&0\\0&8\end{pmatrix}.
\]
</div>

4.  For $A=\begin{pmatrix}1&x\\0&1\end{pmatrix}$ and $B=\begin{pmatrix}y&1\\0&y\end{pmatrix}$ we obtain
<div class="arithmatex" markdown="1">
\[
    AB=\begin{pmatrix}y&1+xy\\0&y\end{pmatrix},\qquad
     BA=\begin{pmatrix}y&xy+1\\0&y\end{pmatrix}.
\]
</div>
Since $1+xy=xy+1$, we get $AB=BA$ for all $x,y\in\mathbf{R}$. The matrices $A$ and $B$ are examples of *elementary matrices*, cf. <a href="../maps-composing/#def-elementary-matrices" data-reference-type="ref+Label" data-reference="def:elementary-matrices">Definition 4.62</a>.

5.  For $A=\begin{pmatrix}3&0\\0&3\end{pmatrix}=3I_2$ and arbitrary $B \in \mathrm{Mat}_{2 \times 2}$, we get
<div class="arithmatex" markdown="1">
\[
    AB=(3I_2)B=3B=B(3I_2)=BA.
\]
</div>
So $AB=BA$ for every such $B$.

6.  Let $A$ be arbitrary and $B=A^2$. Then, by associativity of matrix multiplication (cf. <a href="../maps-composing/#lem-matrix-multiplication-properties" data-reference-type="ref+Label" data-reference="lem:matrix-multiplication-properties">Lemma 4.60</a>),
<div class="arithmatex" markdown="1">
\[
    AB=A\,A^2=A^3=A^2\,A=BA.
\]
</div>
So $AB=BA$ always.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.22</strong></p>

<span id="sol-ex-maps-exercise-015" label="sol--ex:maps-exercise-015"></span> (See <a href="../exercises-maps/#ex-maps-exercise-015" data-reference-type="ref+Label" data-reference="ex:maps-exercise-015">Exercise 4.21</a>.) We use that a matrix $A\in \mathrm{Mat}_{2\times 2}$ determines a linear map
<div class="arithmatex" markdown="1">
\[
f_A:\mathbf R^2\to \mathbf R^2,\qquad x\mapsto Ax,
\]
</div>
by <a href="../maps-multiplication-of-a-matrix/#prop-matrix-linear-map" data-reference-type="ref+Label" data-reference="prop:matrix-linear-map">Proposition 4.19</a>, and conversely that a linear map is determined by the images of a basis, by <a href="../maps-matrices-associated-to-linear-maps/#prop-matrix-to-linear-map" data-reference-type="ref+Label" data-reference="prop:matrix-to-linear-map">Proposition 4.44</a>.

1.  The vectors $e_1=(1,0)$ and $e_2=(0,1)$ form the standard basis of $\mathbf R^2$ (cf. <a href="../spaces-bases/#ex-standard-basis" data-reference-type="ref+Label" data-reference="ex:standard-basis">Example 3.62</a>). Hence prescribing
<div class="arithmatex" markdown="1">
\[
    Ae_1=\begin{pmatrix}3\\4\end{pmatrix},\qquad
    Ae_2=\begin{pmatrix}4\\5\end{pmatrix}
\]
</div>
determines the linear map uniquely. By <a href="../maps-matrices-associated-to-linear-maps/#prop-matrix-to-linear-map" data-reference-type="ref+Label" data-reference="prop:matrix-to-linear-map">Proposition 4.44</a>, the corresponding matrix has these vectors as its columns:
<div class="arithmatex" markdown="1">
\[
    A=\begin{pmatrix}3&4\\4&5\end{pmatrix}.
\]
</div>

2.  Again $e_1=(1,0)$ is prescribed, and the second condition is compatible with linearity because
<div class="arithmatex" markdown="1">
\[
    2e_1=\begin{pmatrix}2\\0\end{pmatrix}
    \quad\text{and therefore}\quad
    A(2e_1)=2A(e_1)=2\begin{pmatrix}3\\4\end{pmatrix}=\begin{pmatrix}6\\8\end{pmatrix},
\]
</div>
using <a href="../maps-definition-and-first-examples/#def-linear-map" data-reference-type="ref+Label" data-reference="def:linear-map">Definition 4.1</a>. So such matrices do exist.

    However, the matrix is not unique, because we only prescribe the image of the line $L(e_1)$, not of a full basis. The vector $e_2=(0,1)$ may be sent to any vector of $\mathbf R^2$. Thus all solutions are of the form
<div class="arithmatex" markdown="1">
\[
    A=\begin{pmatrix}3&a\\4&b\end{pmatrix},\qquad a,b\in \mathbf R.
\]
</div>
Indeed, for such a matrix,
<div class="arithmatex" markdown="1">
\[
    A\begin{pmatrix}1\\0\end{pmatrix}=\begin{pmatrix}3\\4\end{pmatrix},
    \qquad
    A\begin{pmatrix}2\\0\end{pmatrix}=2A\begin{pmatrix}1\\0\end{pmatrix}=\begin{pmatrix}6\\8\end{pmatrix}.
\]
</div>

3.  Here the conditions are incompatible with linearity. As above,
<div class="arithmatex" markdown="1">
\[
    A\begin{pmatrix}2\\0\end{pmatrix}=A(2e_1)=2A(e_1)=2\begin{pmatrix}3\\4\end{pmatrix}=\begin{pmatrix}6\\8\end{pmatrix},
\]
</div>
again by <a href="../maps-definition-and-first-examples/#def-linear-map" data-reference-type="ref+Label" data-reference="def:linear-map">Definition 4.1</a>. But the exercise requires instead
<div class="arithmatex" markdown="1">
\[
    A\begin{pmatrix}2\\0\end{pmatrix}=\begin{pmatrix}3\\4\end{pmatrix},
\]
</div>
which is different. Therefore no such matrix exists.

    Geometrically, the vector $(2,0)$ lies on the same line as $(1,0)$, and a linear map must preserve scalar multiplication along that line. So once the image of $(1,0)$ is fixed, the image of $(2,0)$ is forced to be twice as large.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.23</strong></p>

<span id="sol-ex-maps-exercise-016" label="sol--ex:maps-exercise-016"></span> (See <a href="../exercises-maps/#ex-maps-exercise-016" data-reference-type="ref+Label" data-reference="ex:maps-exercise-016">Exercise 4.22</a>.) One possible choice is
<div class="arithmatex" markdown="1">
\[
A=\begin{pmatrix}1&0\\0&0\end{pmatrix},
\qquad
B=\begin{pmatrix}0&0\\1&0\end{pmatrix}.
\]
</div>
Both matrices are nonzero. Using the definition of matrix multiplication (<a href="../maps-composing/#def-product-matrices" data-reference-type="ref+Label" data-reference="def:product-matrices">Definition 4.49</a>), we compute
<div class="arithmatex" markdown="1">
\[
AB=
\begin{pmatrix}1&0\\0&0\end{pmatrix}
\begin{pmatrix}0&0\\1&0\end{pmatrix}
=
\begin{pmatrix}0&0\\0&0\end{pmatrix}.
\]
</div>
Hence $AB=0$, although $A\neq 0$ and $B\neq 0$.

Using that matrices give rise to linear maps (<a href="../maps-multiplication-of-a-matrix/#prop-matrix-linear-map" data-reference-type="ref+Label" data-reference="prop:matrix-linear-map">Proposition 4.19</a>), this exercise may also be understood in terms of linear maps. Consider the linear maps $f_A,f_B:\mathbf R^2\to\mathbf R^2$. In light of <a href="../maps-composing/#prop-composition-matrices" data-reference-type="ref+Label" data-reference="prop:composition-matrices">Proposition 4.52</a>, the relation $AB=0$ means that
<div class="arithmatex" markdown="1">
\[
f_A\circ f_B=0,
\]
</div>
so every vector in the image of $f_B$ lies in the kernel of $f_A$ (cf. <a href="../maps-kernel-and-image-1/#def-image">Definition 4.20</a>, <a href="../maps-kernel-and-image-1/#def-kernel">Definition 4.22</a>). In our example,
<div class="arithmatex" markdown="1">
\[
\operatorname{im}(f_B)=L\left(\begin{pmatrix}0\\1\end{pmatrix}\right)
\subseteq
L\left(\begin{pmatrix}0\\1\end{pmatrix}\right)=\ker(f_A).
\]
</div>
That is why the composition is the zero map even though neither of the two maps is zero.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.24</strong></p>

<span id="sol-ex-maps-exercise-017" label="sol--ex:maps-exercise-017"></span> (See <a href="../exercises-maps/#ex-maps-exercise-017" data-reference-type="ref+Label" data-reference="ex:maps-exercise-017">Exercise 4.23</a>.)

1.  By <a href="../maps-transpose/#def-transpose" data-reference-type="ref+Label" data-reference="def:transpose">Definition 4.89</a>,
<div class="arithmatex" markdown="1">
\[
    \left ( \begin{array}{cc} 1 & s \\ -2 & t \end{array} \right )^T
    =
    \left ( \begin{array}{cc} 1 & -2 \\ s & t \end{array} \right ).
\]
</div>
The matrix is symmetric if and only if it is equal to its transpose, so the off-diagonal entries must agree. Hence $s=-2$. The entry $t$ already agrees with itself on the diagonal, so $t$ is arbitrary.

2.  Let $A=(a_{ij})$ be any square matrix. By <a href="../maps-transpose/#lem-properties-transposition" data-reference-type="ref+Label" data-reference="lem:properties-transposition">Lemma 4.91</a>, transposition is compatible with addition, so
<div class="arithmatex" markdown="1">
\[
    (A+A^T)^T = A^T + (A^T)^T.
\]
</div>
Applying again <a href="../maps-transpose/#lem-properties-transposition" data-reference-type="ref+Label" data-reference="lem:properties-transposition">Lemma 4.91</a>, we have $(A^T)^T=A$. Thus
<div class="arithmatex" markdown="1">
\[
    (A+A^T)^T = A^T + A = A + A^T.
\]
</div>
Hence $A+A^T$ is symmetric by definition.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.25</strong></p>

<span id="sol-trace" label="sol--trace"></span> (See <a href="../exercises-maps/#trace" data-reference-type="ref+Label" data-reference="trace">Exercise 4.24</a>.) Let $A=(a_{ij})$ and $B=(b_{ij})$ be square matrices of the same size.

1.  By <a href="../maps-transpose/#def-transpose" data-reference-type="ref+Label" data-reference="def:transpose">Definition 4.89</a>, the diagonal entries of $A^T$ are $(A^T)_{ii}=a_{ii}$ for all $i$. By definition of the trace (<a href="../exercises-maps/#trace" data-reference-type="ref+Label" data-reference="trace">Exercise 4.24</a>), we have
<div class="arithmatex" markdown="1">
\[
    \operatorname{tr}(A^T)=(A^T)_{11}+\dots+(A^T)_{nn}=a_{11}+\dots+a_{nn}=\operatorname{tr}(A).
\]
</div>

2.  Using the definition of matrix multiplication (<a href="../maps-composing/#def-product-matrices" data-reference-type="ref+Label" data-reference="def:product-matrices">Definition 4.49</a>), the $(i,i)$-entry of $AB$ is
<div class="arithmatex" markdown="1">
\[
    (AB)_{ii}=\sum_{k=1}^n a_{ik}b_{ki}.
\]
</div>
Hence
<div class="arithmatex" markdown="1">
\[
    \operatorname{tr}(AB)=\sum_{i=1}^n (AB)_{ii}=\sum_{i=1}^n \sum_{k=1}^n a_{ik}b_{ki}.
\]
</div>
Similarly,
<div class="arithmatex" markdown="1">
\[
    \operatorname{tr}(BA)=\sum_{k=1}^n (BA)_{kk}=\sum_{k=1}^n \sum_{i=1}^n b_{ki}a_{ik}.
\]
</div>
These are the same double sum, just with the order of summation reversed. Therefore
<div class="arithmatex" markdown="1">
\[
    \operatorname{tr}(AB)=\operatorname{tr}(BA).
\]
</div>
This is noteworthy because one generally has $AB\ne BA$, cf. <a href="../maps-composing/#war-not-commutative" data-reference-type="ref+Label" data-reference="war:not-commutative">Warning 4.55</a>.

3.  The trace is additive because diagonal entries add componentwise:
<div class="arithmatex" markdown="1">
\[
    \operatorname{tr}(A+B)=(a_{11}+b_{11})+\dots+(a_{nn}+b_{nn})=\operatorname{tr}(A)+\operatorname{tr}(B).
\]
</div>
Likewise, scalar multiplication acts componentwise on the diagonal, so
<div class="arithmatex" markdown="1">
\[
    \operatorname{tr}(rA)=ra_{11}+\dots+ra_{nn}=r\,\operatorname{tr}(A).
\]
</div>

4.  Suppose there were a matrix $B$ with
<div class="arithmatex" markdown="1">
\[
    AB-BA={\mathrm{id}}.
\]
</div>
Applying part (3) and then part (2), we obtain
<div class="arithmatex" markdown="1">
\[
    \operatorname{tr}(AB-BA)=\operatorname{tr}(AB)-\operatorname{tr}(BA)=0.
\]
</div>
But
<div class="arithmatex" markdown="1">
\[
    \operatorname{tr}({\mathrm{id}})=1+\dots+1=n,
\]
</div>
where $n$ is the size of the matrix. Hence $\operatorname{tr}(AB-BA)\ne \operatorname{tr}({\mathrm{id}})$, a contradiction. Therefore no such matrix $B$ exists.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.26</strong></p>

<span id="sol-ex-maps-exercise-018" label="sol--ex:maps-exercise-018"></span> (See <a href="../exercises-maps/#ex-maps-exercise-018" data-reference-type="ref+Label" data-reference="ex:maps-exercise-018">Exercise 4.25</a>.) Consider the fixed number $r \in \mathbf R$. If we look for a matrix $R$ such that for all $2 \times 2$-matrices $A$ we have $RA = rA$, then this equation applied to $A = \mathrm{id}_2$ (the identity matrix, cf. <a href="../maps-composing/#def-identity-matrix" data-reference-type="ref+Label" data-reference="def:identity-matrix">Definition 4.58</a>) gives
<div class="arithmatex" markdown="1">
\[
R \mathrm{id}_2 = r \mathrm{id}_2 = \begin{pmatrix} r & 0 \\ 0 & r \end{pmatrix}.
\]
</div>
By <a href="../maps-composing/#lem-matrix-multiplication-properties" data-reference-type="ref+Label" data-reference="lem:matrix-multiplication-properties">Lemma 4.60</a>, the left hand side equals $R$, so we see that we need to have $R = \begin{pmatrix} r & 0 \\ 0 & r \end{pmatrix}$. One then confirms that the equation $RA = rA$ holds for all $A$. This can be done by direct computation.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.27</strong></p>

<span id="sol-ex-maps-exercise-019" label="sol--ex:maps-exercise-019"></span> (See <a href="../exercises-maps/#ex-maps-exercise-019" data-reference-type="ref+Label" data-reference="ex:maps-exercise-019">Exercise 4.26</a>.)

1.  Using <a href="../maps-composing/#def-product-matrices" data-reference-type="ref+Label" data-reference="def:product-matrices">Definition 4.49</a>, we compute
<div class="arithmatex" markdown="1">
\[
    A^2=
    \begin{pmatrix}
    0&a&b\\
    0&0&c\\
    0&0&0
    \end{pmatrix}
    \begin{pmatrix}
    0&a&b\\
    0&0&c\\
    0&0&0
    \end{pmatrix}
    =
    \begin{pmatrix}
    0&0&ac\\
    0&0&0\\
    0&0&0
    \end{pmatrix}.
\]
</div>
Multiplying once more, we obtain
<div class="arithmatex" markdown="1">
\[
    A^3=A^2A=
    \begin{pmatrix}
    0&0&ac\\
    0&0&0\\
    0&0&0
    \end{pmatrix}
    \begin{pmatrix}
    0&a&b\\
    0&0&c\\
    0&0&0
    \end{pmatrix}
    =
    \begin{pmatrix}
    0&0&0\\
    0&0&0\\
    0&0&0
    \end{pmatrix}=0.
\]
</div>

2.  A generalization to arbitrary square matrices is the following: if $A$ is a strictly upper triangular $n\times n$-matrix, meaning that all entries on and below the diagonal are zero, then
<div class="arithmatex" markdown="1">
\[
    A^n=0.
\]
</div>
Indeed, when one multiplies strictly upper triangular matrices, the first superdiagonal can move only upward. More precisely, every entry of $A^k$ on or below the $(k-1)$-st superdiagonal is zero. After $n$ factors there is no possible nonzero position left, so all entries vanish.

    Equivalently, each multiplication shifts possible nonzero entries at least one step farther above the main diagonal; after $n$ steps they have all disappeared. Thus every strictly upper triangular $n\times n$-matrix is nilpotent. In terms of linear maps one can observe that such a matrix $A$ describes a linear map $f_A$ such that $f_A(e_1) = 0$, while $f_A(e_2)$ is a linear combination of $e_1$, $f_A(e_3)$ is a linear combination of $e_1$ and $e_2$, etc. Thus, the image of $f_A$ is contained in the span of $e_1, \dots, e_{n-1}$, and the image of $f_A^2$ is contained in the span of $e_1, \dots, e_{n-2}$ etc., so that $f_A^n = 0$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.28</strong></p>

<span id="sol-ex-maps-3-8" label="sol--ex:maps-3-8"></span> (See <a href="../exercises-maps/#ex-maps-3-8" data-reference-type="ref+Label" data-reference="ex:maps-3-8">Exercise 4.27</a>.) We write any vector $v = (a,b) = a(1,0) + b(0,1) = ae_1 + be_2$ in terms of $v_1, v_2$:
<div class="arithmatex" markdown="1">
\[
v = \alpha v_1 + \beta v_2 = \alpha(1,-3)+\beta(2,1).
\]
</div>
As an example, if $v=(0,6)$, then $(0,6)=\alpha(1,-3)+\beta(2,1)$ gives the linear system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
0 & = \alpha + 2\beta \\
6 & = -3\alpha + \beta.
\end{align*}
\]
</div>
This can be solved as $\beta = \frac 67$ and $\alpha = -\frac{12}7.$ Thus, we can write
<div class="arithmatex" markdown="1">
\[
v = (0,6)_{(e_1, e_2)} = (-\frac{12}7,\frac 67)_{(v_1, v_2)},
\]
</div>
where the subscripts indicate that the coordinates are with respect to the standard basis, resp. to the basis $v_1, v_2$.

We now determine the base change matrix. We have to write the matrix of the identity map in terms of the standard basis in the domain, and the basis $v_1, v_2$ in the codomain:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
e_1 = (1,0) \mapsto & {\mathrm {id}}(e_1) = (1,0) = \alpha_1 v_1 + \alpha_2 v_2 \\
e_2 = (0,1) \mapsto & {\mathrm {id}}(e_2) = (0,1) = \beta_1 v_1 + \beta_2 v_2.
\end{align*}
\]
</div>
The base change matrix is then the matrix
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cc} \alpha_1 & \beta_1 \\ \alpha_2 & \beta_2 \end{array} \right ).
\]
</div>
We can compute $\alpha_1$ etc. similarly as above:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
1 &= \alpha_1 + 2 \alpha_2 \\
0 &= -3\alpha_1+\alpha_2
\end{align*}
\]
</div>
We solve this as $\alpha_1 = \frac 17$, $\alpha_2 = \frac 37$. As for $\beta_1, \beta_2$, the relevant system is
<div class="arithmatex" markdown="1">
\[
\begin{align*}
0 &= \beta_1 + 2 \beta_2 \\
1 &= -3\beta_1+\beta_2
\end{align*}
\]
</div>
whose solution is $\beta_1 = -\frac 27$, $\beta_2 = \frac 17$. Therefore, the base change matrix is
<div class="arithmatex" markdown="1">
\[
H = \left ( \begin{array}{cc} \frac 17 & -\frac 27 \\ \frac 37 & \frac 17 \end{array} \right ).
\]
</div>

We compute the coordinates of $(2,-5)$ in terms of the basis $v_1, v_2$:
<div class="arithmatex" markdown="1">
\[
H \left ( \begin{array}{c} 2 \\ -5 \end{array} \right ) = \left ( \begin{array}{cc} \frac 17 & -\frac 27 \\ \frac 37 & \frac 17 \end{array} \right ) \left ( \begin{array}{c} 2 \\ -5 \end{array} \right ) = \left ( \begin{array}{c} \frac{12}7 \\ \frac 17 \end{array} \right ).
\]
</div>
Thus, the coordinates of $(2, -5)$ with respect to the basis $v_1, v_2$ is $(\frac {12}7, \frac 17)$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.29</strong></p>

<span id="sol-ex-maps-3-9" label="sol--ex:maps-3-9"></span> (See <a href="../exercises-maps/#ex-maps-3-9" data-reference-type="ref+Label" data-reference="ex:maps-3-9">Exercise 4.28</a>.) We have, for example,
<div class="arithmatex" markdown="1">
\[
{\mathrm {id}}(v_1) = v_1 = (1,0,-1) = 1 \cdot e_1 + 0 \cdot e_2 + (-1) \cdot e_3.
\]
</div>
Likewise for $v_2$ and $v_3$. Therefore, the base change matrix is
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc} 1 & 2 & -1 \\ 0 & 1 & -1 \\ -1 & 1 & 7 \end{array} \right ).
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.30</strong></p>

<span id="sol-ex-maps-3-10" label="sol--ex:maps-3-10"></span> (See <a href="../exercises-maps/#ex-maps-3-10" data-reference-type="ref+Label" data-reference="ex:maps-3-10">Exercise 4.30</a>.) We follow the given hint, and first compute $H$. We have
<div class="arithmatex" markdown="1">
\[
\begin{align*}
v_1 \mapsto & v_1 = (1,-1) = e_1 - e_2, \\
v_2 \mapsto & v_2 =(3,-1) = 3e_1 - e_2.
\end{align*}
\]
</div>
Thus $H = \left ( \begin{array}{cc} 1 & 3 \\ -1 & -1 \end{array} \right )$.

We now compute the base change matrix $K$ from the standard basis to the basis $\underline t = \{t_1, t_2, t_3\}$:
<div class="arithmatex" markdown="1">
\[
e_1 = (1,0,0) \mapsto (1,0,0) = \alpha_1 t_1 + \alpha_2 t_2 + \alpha_3 t_3.
\]
</div>
Plugging in the values of $t_1, t_2, t_3$, this gives the linear system
<div class="arithmatex" markdown="1">
\[
\begin{align*}
1 &= \alpha_1+2\alpha_2 - \alpha_3 \\
0 & = \alpha_2 - \alpha_3 \\
0 & = \alpha_1 + \alpha_2 - \alpha_3.
\end{align*}
\]
</div>
This has the solution
<div class="arithmatex" markdown="1">
\[
\alpha_1 = 0, \ \alpha_2 = 1, \ \alpha_3 = 1.
\]
</div>
Similarly, if instead of $e_1 = (1,0,0)$, we consider $e_2 = (0,1,0)$, the constants in the above system change accordingly to 0, resp. 1, resp. 0 in the three equations above. The solution is then
<div class="arithmatex" markdown="1">
\[
\alpha_1 = -1, \alpha_2 = 0, \alpha_3 = -1.
\]
</div>
Similarly, for $e_3$, we obtain the solution
<div class="arithmatex" markdown="1">
\[
\alpha_1 = 1, \alpha_2 = -1, \alpha_3 = -1.
\]
</div>
Hence
<div class="arithmatex" markdown="1">
\[
K = \left ( \begin{array}{ccc} 0 & -1 & 1 \\ 1 & 0 & -1 \\ 1 & -1 & -1 \end{array} \right ).
\]
</div>
(Alternatively, using methods of later chapters, one may also compute $K = T^{-1}$, the inverse of the matrix $T = \left ( \begin{array}{ccc} 1 & 2 & -1 \\ 0 & 1 & -1 \\ 1 & 1 & -1 \end{array} \right )$ which is the matrix whose columns are the basis vectors $t_1, t_2$ and $t_3$.) We compute
<div class="arithmatex" markdown="1">
\[
\begin{align*}
KAH & = \left ( \begin{array}{ccc} 0 & -1 & 1 \\ 1 & 0 & -1 \\ 1 & -1 & -1 \end{array} \right ) \cdot 
\left ( \begin{array}{cc} 2 & 1 \\ 0 & 1 \\ -3 & 1 \end{array} \right ) \cdot 
\left ( \begin{array}{cc} 1 & 3 \\ -1 & -1 \end{array} \right ) \\
& = \left ( \begin{array}{ccc} 0 & -1 & 1 \\ 1 & 0 & -1 \\ 1 & -1 & -1 \end{array} \right ) \cdot
\left ( \begin{array}{cc} 1 & 5 \\ -1 & -1 \\ -4 & -10 \end{array} \right ) \\
& = \left ( \begin{array}{cc} -3 & -9 \\ 5 & 15 \\ 6 & 16 \end{array} \right ).
\end{align*}
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.31</strong></p>

<span id="sol-ex-maps-3-11" label="sol--ex:maps-3-11"></span> (See <a href="../exercises-maps/#ex-maps-3-11" data-reference-type="ref+Label" data-reference="ex:maps-3-11">Exercise 4.32</a>.) We follow the solution of <a href="../exercises-maps/#ex-maps-3-10" data-reference-type="ref+Label" data-reference="ex:maps-3-10">Exercise 4.30</a>, see above:
<div class="arithmatex" markdown="1">
\[
{\bf R}^2_{\underline v} \xrightarrow[H]{\mathrm {id}} {\bf R}^2_{\underline e} \xrightarrow[A]{f} {\bf R}^2_{\underline e} \xrightarrow[K]{\mathrm {id}} {\bf R}^2_{\underline v}.
\]
</div>
We have $H=\left ( \begin{array}{cc} 1 & 1 \\ 1 & 2 \end{array} \right )$. One computes $K = \left ( \begin{array}{cc} 2 & -1 \\ -1 & 1 \end{array} \right )$ and then
<div class="arithmatex" markdown="1">
\[
\begin{align*}
KAH& = \left ( \begin{array}{cc} 2 & -1 \\ -1 & 1 \end{array} \right ) \left ( \begin{array}{cc} 6 & -1 \\ 2 & 3 \end{array} \right ) \left ( \begin{array}{cc} 1 & 1 \\ 1 & 2 \end{array} \right ) \\
& = \left ( \begin{array}{cc} 2 & -1 \\ -1 & 1 \end{array} \right ) \left ( \begin{array}{cc} 5 & 4 \\ 5 & 8 \end{array} \right ) \\
& = \left ( \begin{array}{cc} 5 & 0 \\ 0 & 4 \end{array} \right ).
\end{align*}
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.32</strong></p>

<span id="sol-ex-maps-3-12" label="sol--ex:maps-3-12"></span> (See <a href="../exercises-maps/#ex-maps-3-12" data-reference-type="ref+Label" data-reference="ex:maps-3-12">Exercise 4.33</a>.) For the given matrix $A$, the system $Ax =x$ is written out like so:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
x_3 & = x_1 \\
x_2 &= x_2 \\
x_1 &= x_3.
\end{align*}
\]
</div>
The second equation holds for all $x$, and the first is equivalent to the third. Therefore, the system is equivalent to the one consisting of the single equation
<div class="arithmatex" markdown="1">
\[
x_1 - x_3  = 0.
\]
</div>
This corresponds to the system
<div class="arithmatex" markdown="1">
\[
B x  = x,
\]
</div>
where $B= (1 \ 0 \ {-1})$ is the corresponding $1 \times 3$-matrix. This matrix has rank 1, so that the solution space is two-dimensional, given by
<div class="arithmatex" markdown="1">
\[
L((1,0,1), (0,1,0)).
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.33</strong></p>

<span id="sol-ex-maps-3-13" label="sol--ex:maps-3-13"></span> (See <a href="../exercises-maps/#ex-maps-3-13" data-reference-type="ref+Label" data-reference="ex:maps-3-13">Exercise 4.34</a>.) We write out the given system
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc} 1 & 0 & 0 \\ 0 & 4 & 2 \\ 0 & 2 & 1 \end{array} \right ) \left ( \begin{array}{c} x_1 \\ x_2 \\ x_3 \end{array} \right ) = 5 \left ( \begin{array}{c} x_1 \\ x_2 \\ x_3 \end{array} \right )
\]
</div>
as
<div class="arithmatex" markdown="1">
\[
\left [ \left ( \begin{array}{ccc} 1 & 0 & 0 \\ 0 & 4 & 2 \\ 0 & 2 & 1 \end{array} \right ) - \left ( \begin{array}{ccc} 5 & 0 & 0 \\ 0 & 5 & 0 \\ 0 & 0 & 5 \end{array} \right ) \right ] \left ( \begin{array}{c} x_1 \\ x_2 \\ x_3 \end{array} \right ) = \left ( \begin{array}{c} 0 \\ 0 \\ 0 \end{array} \right ).
\]
</div>
This simplifies to
<div class="arithmatex" markdown="1">
\[
\underbrace{\left ( \begin{array}{ccc} -4 & 0 & 0 \\ 0 & -1 & 2 \\ 0 & 2 & -4 \end{array} \right )}_{=:B} \left ( \begin{array}{c} x_1 \\ x_2 \\ x_3 \end{array} \right ) = \left ( \begin{array}{c} 0 \\ 0 \\ 0 \end{array} \right ),
\]
</div>
which can be solved by bringing $B$ into row-echelon form:
<div class="arithmatex" markdown="1">
\[
B \leadsto \left ( \begin{array}{ccc} 1 & 0 & 0 \\ 0 & 1 & -2 \\ 0 & 0 & 0 \end{array} \right ).
\]
</div>
Thus $x_1 = 0$, $x_2 = 2x_3$ and $x_3$ is a free variable. Thus the solution space of the given system is
<div class="arithmatex" markdown="1">
\[
L((0, 2, 1)).
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.34</strong></p>

<span id="sol-ex-maps-3-14" label="sol--ex:maps-3-14"></span> (See <a href="../exercises-maps/#ex-maps-3-14" data-reference-type="ref+Label" data-reference="ex:maps-3-14">Exercise 4.35</a>.) We proceed the same way as for <a href="../exercises-maps/#ex-maps-3-10" data-reference-type="ref+Label" data-reference="ex:maps-3-10">Exercise 4.30</a> (see its solution above):
<div class="arithmatex" markdown="1">
\[
{\bf R}^2_{\underline v} \xrightarrow[H]{\mathrm {id}} {\bf R}^2_{\underline e} \xrightarrow[A]{f}
{\bf R}^2_{\underline e} \xrightarrow[H^{-1}] {\mathrm {id}}
{\bf R}^2_{\underline v}.
\]
</div>
Here $H$ is the base change matrix from $\underline v$ to the standard basis $\underline e = \{e_1 = (1,0), e_2 = (0,1)\}$. The base change matrix from $\underline e$ to $\underline v$ is then $H^{-1}$. From the given vectors we have $H  = \left ( \begin{array}{cc} 2 & 0 \\ 1 & 1 \end{array} \right )$. We compute the inverse $H^{-1}$ using <a href="../maps-inverses/#thm-invertible-elimination" data-reference-type="ref+Label" data-reference="thm:invertible-elimination">Theorem 4.81</a>:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left ( \begin{array}{cc|cc} 2 & 0 & 1 & 0 \\ 1 & 1 & 0 & 1 \end{array} \right ) & \leadsto  
\left ( \begin{array}{cc|cc} 1 & 1 & 0 & 1 \\ 2 & 0 & 1 & 0 \end{array} \right ) \leadsto 
\left ( \begin{array}{cc|cc} 1 & 1 & 0 & 1 \\ 0 & -2 & 1 & -2 \end{array} \right ) \\
& \leadsto
\left ( \begin{array}{cc|cc} 1 & 1 & 0 & 1 \\ 0 & 1 & -\frac 12 & 1 \end{array} \right ) \leadsto
\left ( \begin{array}{cc|cc} 1 & 0 & \frac 12 & 0 \\ 0 & 1 & -\frac12 & 1 \end{array} \right ) \\
& = ( {\mathrm {id}} \ | \ H^{-1}).
\end{align*}
\]
</div>
Thus, $H^{-1} = \left ( \begin{array}{cc} \frac12 & 0 \\ -\frac12 & 1 \end{array} \right )$. Therefore the requested matrix of $f$ is
<div class="arithmatex" markdown="1">
\[
\begin{align*}
H^{-1}AH & = 
\left ( \begin{array}{cc} \frac12 & 0 \\ -\frac12 & 1 \end{array} \right ) \left ( \begin{array}{cc} 3 & 0 \\ 8 & -1 \end{array} \right )
\left ( \begin{array}{cc} 2 & 0 \\ 1 & 1 \end{array} \right ) =
\left ( \begin{array}{cc} \frac12 & 0 \\ -\frac12 & 1 \end{array} \right ) \left ( \begin{array}{cc} 6 & 0 \\ 15 & - \end{array} \right )1  \\ &
= \left ( \begin{array}{cc} 3 & 0 \\ 12 & -1 \end{array} \right ).
\end{align*}
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.35</strong></p>

<span id="sol-ex-maps-3-15" label="sol--ex:maps-3-15"></span> (See <a href="../exercises-maps/#ex-maps-3-15" data-reference-type="ref+Label" data-reference="ex:maps-3-15">Exercise 4.37</a>.) This can be done as for <a href="../exercises-maps/#ex-maps-3-14" data-reference-type="ref+Label" data-reference="ex:maps-3-14">Exercise 4.35</a> above. The final solution is
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc} -2 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & -1 \end{array} \right ).
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.36</strong></p>

<span id="sol-ex-maps-3-16" label="sol--ex:maps-3-16"></span> (See <a href="../exercises-maps/#ex-maps-3-16" data-reference-type="ref+Label" data-reference="ex:maps-3-16">Exercise 4.38</a>.) One computes this solution space as
<div class="arithmatex" markdown="1">
\[
L((-1,2,3)) = L((1,-2,-3)).
\]
</div>

According to <a href="../spaces-dimension/#thm-basis-theorem" data-reference-type="ref+Label" data-reference="thm:basis-theorem">Theorem 3.71</a><a href="../spaces-dimension/#item-independent-add" data-reference-type="ref" data-reference="item--independent.add">2.</a>, this vector $l_1 = (1,-2,-3)$ can be completed to a basis of ${\bf R}^3$ by picking *any* basis $v_1, v_2, v_3$ of ${\bf R}^3$. Then it is possible to find two of these three vectors which together with $l_1$ will form a basis of ${\bf R}^3$. We pick the standard basis, $v_1=e_2$, $v_2=e_2$ and $v_3=e_3$. We check that $l_1, e_2, e_3$ form a basis. Indeed, the matrix whose rows are these vectors,
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc} 1 & -2 & -3 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{array} \right ),
\]
</div>
is a row-echelon matrix with three leading ones, so its rank is 3.

We compute the matrix of $f$ with respect to this basis $\underline v = \{l_1, e_2, e_3\}$:
<div class="arithmatex" markdown="1">
\[
{\bf R}^3_{\underline v} \xrightarrow[H]{ {\mathrm {id}}}
{\bf R}^3_{\underline e} \xrightarrow[A]{f}
{\bf R}^3_{\underline e} \xrightarrow[H^{-1}]{ {\mathrm {id}}}
{\bf R}^3_{\underline v}.
\]
</div>
We have
<div class="arithmatex" markdown="1">
\[
H=\left ( \begin{array}{ccc} 1 & 0 & 0 \\ -2 & 1 & 0 \\ -3 & 0 & 1 \end{array} \right ).
\]
</div>
We compute the inverse using <a href="../maps-inverses/#thm-invertible-elimination" data-reference-type="ref+Label" data-reference="thm:invertible-elimination">Theorem 4.81</a>:
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc|ccc} 1 & 0 & 0 & 1 & 0 & 0 \\ -2 & 1 & 0 & 0 & 1 & 0 \\ -3 & 0 & 1 & 0 & 0 & 1 \end{array} \right ) 
\leadsto
\left ( \begin{array}{ccc|ccc} 1 & 0 & 0 & 1 & 0 & 0 \\ 0 & 1 & 0 & 2 & 1 & 0 \\ 0 & 0 & 1 & 3 & 0 & 1 \end{array} \right )
= ({\mathrm {id}} \ | \ H^{-1}).
\]
</div>
Hence the matrix for $f$ with respect to the basis $\underline v$ is
<div class="arithmatex" markdown="1">
\[
H^{-1}AH = \left ( \begin{array}{ccc} 3 & -1 & 0 \\ 0 & 0 & 1 \\ 0 & -2 & 3 \end{array} \right ).
\]
</div>

<div class="remark" markdown="1">


<p class="env-number"><strong>Remark 4.95</strong></p>

<span id="rem-solutions-remark-002" label="rem:solutions-remark-002"></span> The choice of the two vectors $e_2$ and $e_3$, in addition to $l_1$ above, is arbitrary. To begin with, one may choose a different basis (other than the standard basis) to complete $l_1$ to a basis. Even if one takes the standard basis, for this particular value of $l_1$, *any* two of the three vectors $e_1, e_2, e_3$ together with $l_1$ would form a basis. The resulting base change matrix $H$ will then be different, and also the result $H^{-1}AH$ will be different.

</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.37</strong></p>

<span id="sol-ex-maps-3-17" label="sol--ex:maps-3-17"></span> (See <a href="../exercises-maps/#ex-maps-3-17" data-reference-type="ref+Label" data-reference="ex:maps-3-17">Exercise 4.39</a>.) The vectors
<div class="arithmatex" markdown="1">
\[
\underline v = \{v_1 = (1,0,1), v_2 = (0,3,-1), v_3 = (0,0,1)\}
\]
</div>
form a basis of ${\bf R}^3$ since the corresponding matrix $\left ( \begin{array}{ccc} 1 & 0 & 1 \\ 0 & 3 & -1 \\ 0 & 0 & 1 \end{array} \right )$ has rank 3. Hence we can compute the matrix of $f$ with respect to that basis as follows:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
f(v_1) &= 0 & = 0 v_1 + 0v_2 + 0v_3 \\
f(v_2) & = v_2 & = 0v_1 + 1v_2 +0v_3 \\
f(v_3) & = (0,0,2) = 2v_3 & = 0v_1 + 0v_2 + 2 v_3.
\end{align*}
\]
</div>
Therefore the matrix of $f$ with respect to that basis is
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{ccc} 0 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 2 \end{array} \right ).
\]
</div>
As before, we compute that matrix of $f$ with respect to the standard basis using the method above:
<div class="arithmatex" markdown="1">
\[
{\bf R}^3_{\underline e} \xrightarrow[K]{ {\mathrm {id}}}
{\bf R}^3_{\underline v} \xrightarrow[A]{f}
{\bf R}^3_{\underline v} \xrightarrow[K^{-1}]{ {\mathrm {id}}}
{\bf R}^3_{\underline e}.
\]
</div>
The base change matrix $K$ is easily read off:
<div class="arithmatex" markdown="1">
\[
K = \left ( \begin{array}{ccc} 1 & 0 & 0 \\ 0 & 3 & 0 \\ 1 & -1 & 1 \end{array} \right ).
\]
</div>
We compute the inverse $K^{-1}$:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left ( \begin{array}{ccc|ccc} 1 & 0 & 0 & 1 & 0 & 0 \\ 0 & 3 & 0 & 0 & 1 & 0 \\ 1 & -1 & 1 & 0 & 0 & 1 \end{array} \right ) & \leadsto
\left ( \begin{array}{ccc|ccc} 1 & 0 & 0 & 1 & 0 & 0 \\ 0 & 3 & 0 & 0 & 1 & 0 \\ 0 & -1 & 1 & -1 & 0 & 1 \end{array} \right ) \\
& \leadsto
\left ( \begin{array}{ccc|ccc} 1 & 0 & 0 & 1 & 0 & 0 \\ 0 & 1 & 0 & 0 & \frac13 & 0 \\ 0 & -1 & 1 & -1 & 0 & 1 \end{array} \right ) \\
& \leadsto \left ( \begin{array}{ccc|ccc} 1 & 0 & 0 & 1 & 0 & 0 \\ 0 & 1 & 0 & 0 & \frac13 & 0 \\ 0 & 0 & 1 & -1 & \frac13 & 1 \end{array} \right ) \\
& = ({\mathrm {id}} \ | \ K^{-1}).
\end{align*}
\]
</div>
Therefore the requested matrix is the product
<div class="arithmatex" markdown="1">
\[
\begin{align*}
KAK^{-1} & = \left ( \begin{array}{ccc} 1 & 0 & 0 \\ 0 & 3 & 0 \\ 1 & -1 & 1 \end{array} \right ) 
\left ( \begin{array}{ccc} 0 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 2 \end{array} \right )
\left ( \begin{array}{ccc} 1 & 0 & 0 \\ 0 & \frac13 & 0 \\ -1 & \frac13 & 1 \end{array} \right ) \\
& = \left ( \begin{array}{ccc} 1 & 0 & 0 \\ 0 & 3 & 0 \\ 1 & -1 & 1 \end{array} \right ) 
\left ( \begin{array}{ccc} 0 & 0 & 0 \\ 0 & \frac13 & 0 \\ -2 & \frac 23 & 2 \end{array} \right ) \\
& = \left ( \begin{array}{ccc} 0 & 0 & 0 \\ 0 & 1 & 0 \\ -2 & \frac13 & 2 \end{array} \right ).
\end{align*}
\]
</div>

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.38</strong></p>

<span id="sol-ex-maps-3-18" label="sol--ex:maps-3-18"></span> (See <a href="../exercises-maps/#ex-maps-3-18" data-reference-type="ref+Label" data-reference="ex:maps-3-18">Exercise 4.41</a>.) It is convenient to observe
<div class="arithmatex" markdown="1">
\[
5 \left ( \begin{array}{c} x_1 \\ x_2 \\ x_3 \end{array} \right ) = \left ( \begin{array}{ccc} 5 & 0 & 0 \\ 0 & 5 & 0 \\ 0 & 0 & 5 \end{array} \right ) 5 \left ( \begin{array}{c} x_1 \\ x_2 \\ x_3 \end{array} \right ).
\]
</div>
Thus the given system can be rewritten as
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc} 1 & 0 & 0 \\ 0 & 4 & 2 \\ 0 & 2 & 1 \end{array} \right ) \left ( \begin{array}{c} x_1 \\ x_2 \\ x_3 \end{array} \right ) =  \left ( \begin{array}{ccc} 5 & 0 & 0 \\ 0 & 5 & 0 \\ 0 & 0 & 5 \end{array} \right ) \left ( \begin{array}{c} x_1 \\ x_2 \\ x_3 \end{array} \right ).
\]
</div>
By <a href="../maps-composing/#lem-matrix-multiplication-properties" data-reference-type="ref+Label" data-reference="lem:matrix-multiplication-properties">Lemma 4.60</a>, this is the same as the system
<div class="arithmatex" markdown="1">
\[
\left [ \left ( \begin{array}{ccc} 1 & 0 & 0 \\ 0 & 4 & 2 \\ 0 & 2 & 1 \end{array} \right ) - \left ( \begin{array}{ccc} 5 & 0 & 0 \\ 0 & 5 & 0 \\ 0 & 0 & 5 \end{array} \right )\right ] \left ( \begin{array}{c} x_1 \\ x_2 \\ x_3 \end{array} \right ) =  \left ( \begin{array}{c} 0 \\ 0 \\ 0 \end{array} \right ) .
\]
</div>
The left hand matrix equals $\left ( \begin{array}{ccc} -4 & 0 & 0 \\ 0 & -1 & 2 \\ 0 & 2 & -4 \end{array} \right )$. From here, one can use the standard method to solve the linear system. (As a forecast to §<a href="../determinants-determinants-of-2-x-2-matrices/#sect-determinants" data-reference-type="ref" data-reference="sect--determinants">Chapter 5</a>, one can note that the determinant of the latter matrix is 0, so that the matrix is not invertible. Hence the system above has non-zero solutions.)

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.39</strong></p>

<span id="sol-ex-maps-3-19" label="sol--ex:maps-3-19"></span> (See <a href="../exercises-maps/#ex-maps-3-19" data-reference-type="ref+Label" data-reference="ex:maps-3-19">Exercise 4.43</a>.) Consider the vectors $v_1 = (1,0,-1)$, $v_2 = (1,1,0)$, $v_3 = (1,0,-2) \in {\bf R}^3$.

We have $f(v_1) = (3,0,-5) = v_1 + 2v_3$, $f(v_2) = 2v_2$ and $f(v_3) = (5,2,-5) = v_1 + 2v_2 + 2v_3$. Therefore the matrix $A$ with respect to the basis $\underline v := (v_1, v_2, v_3)$ in the domain and the codomain is
<div class="arithmatex" markdown="1">
\[
A = \left ( \begin{array}{ccc} 1 & 0 & 1 \\ 0 & 2 & 1 \\ 2 & 0 & 2 \end{array} \right ).
\]
</div>

In order to to compute the matrix $B$ with respect to the standard basis of ${\bf R}^3$, we express the standard basis vectors $e_1, e_2, e_3$ as linear combinations of the $v_1, v_2, v_3$, then compute $f(e_k)$ using the linearity of $f$. We have
<div class="arithmatex" markdown="1">
\[
\begin{align*}
e_1 & = 2v_1 - v_3 \\
e_2 & = v_2 - e_1 = -2v_1 + v_2 + v_3 \\
e_3 & = v_1 - v_3.
\end{align*}
\]
</div>
This implies
<div class="arithmatex" markdown="1">
\[
\begin{align*}
f(e_1) & = 2f(v_1) - f(v_3) = (6,0,-10) - (5,2,-5) = (1, -2, -5) \\
f(e_2) & = -2f(v_1) + f(v_2) + f(v_3) = (-6,0,10) + (2,2,0) + (5,2,-5) = (1, 4, 5) \\
f(e_3) & = f(v_1) - f(v_3) = (3,0,-5) - (5,2,-5) = (-2, -2, 0).
\end{align*}
\]
</div>
Therefore
<div class="arithmatex" markdown="1">
\[
B = \left ( \begin{array}{ccc} 1 & 1 & -2 \\ -2 & 4 & -2 \\ -5 & 5 & 0 \end{array} \right ).
\]
</div>

A slightly different way to solve this is to observe that the matrix of $f$ with respect to the basis $\underline v$ in the source and the standard basis $\underline e$ in the target is $C = \left ( \begin{array}{ccc} 3 & 2 & 5 \\ 0 & 2 & 2 \\ -5 & 0 & -5 \end{array} \right )$. We consider the matrix $H = \left ( \begin{array}{ccc} 1 & 1 & 1 \\ 0 & 1 & 0 \\ -1 & 0 & -2 \end{array} \right )$ whose columns are the three vectors $v_i$, i.e., the base change matrix from the basis $\underline v$ to $\underline e$. Compute the inverse of this matrix, for example using <a href="../maps-inverses/#thm-invertible-elimination" data-reference-type="ref+Label" data-reference="thm:invertible-elimination">Theorem 4.81</a>. This gives $H^{-1} = \left ( \begin{array}{ccc} 2 & -2 & 1 \\ 0 & 1 & 0 \\ -1 & 1 & -1 \end{array} \right )$. This is the base change matrix from $\underline e$ to the basis $\underline v$. Then $B = C H^{-1}$: ${\bf R}^3_{\underline e} \xrightarrow[H^{-1}]{ {\mathrm {id}}} {\bf R}^3_{\underline v} \xrightarrow[C]{f} {\bf R}^3_{\underline e}$, which confirms the above computation. Likewise $A = H^{-1} C$, corresponding to ${\bf R}^3_{\underline v} \xrightarrow[C]{f} {\bf R}^3_{\underline e} \xrightarrow[H^{-1}]{ {\mathrm {id}}} {\bf R}^3_{\underline v}$, which confirms the above computation.

The kernel and image of $f$ can be computed by bringing $B$ into row echelon form. The result is $\ker f = \{(x,x,x) | x \in {\bf R}\}$, i.e., it is 1-dimensional and has as a basis vector $(1,1,1)$. We have ${\operatorname{im}\ } f = L((1,4,5),(1,-2,-5))$.

For the last part, we form the matrix
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc|c} 1 & 1 & -2 & 3 \\ -2 & 4 & -2 & t \\ -5 & 5 & 0 & -5 \end{array} \right )
\leadsto
\left ( \begin{array}{ccc|c} 1 & 1 & -2 & 3 \\ 0 & 6 & -6 & t+6 \\ 0 & 10 & -10 & 10 \end{array} \right )
\leadsto
\left ( \begin{array}{ccc|c} 1 & 1 & -2 & 3 \\ 0 & 0 & 0 & t \\ 0 & 1 & -1 & 1 \end{array} \right )
\]
</div>
and bring it into row echelon form as shown above. We find that it has rank 2 (the same as the rank of $B$), if and only if $t = 0$. and $f^{-1}((3,0,-5)) = \{(x, x-1, x-2) | x \in {\bf R}\}$.

These computations can also be performed with any computer algebra software, such as Wolfram Alpha:

- <https://www.wolframalpha.com/input?i=Inverse%28%28%281%2C1%2C1%29%2C%280%2C1%2C0%29%2C%28-1%2C0%2C-2%29%29%29> (compute the inverse of $H$)

- <https://www.wolframalpha.com/input?i=%28%283%2C2%2C5%29%2C%280%2C2%2C2%29%2C%28-5%2C0%2C-5%29%29*Inverse%28%28%281%2C1%2C1%29%2C%280%2C1%2C0%29%2C%28-1%2C0%2C-2%29%29%29> (compute $H^{-1}C$)

- <https://www.wolframalpha.com/input?i=kernel%28%281%2C1%2C-2%29%2C%28-2%2C4%2C-2%29%2C%28-5%2C5%2C0%29%29>, <https://www.wolframalpha.com/input?i=column+space%28%281%2C1%2C-2%29%2C%28-2%2C4%2C-2%29%2C%28-5%2C5%2C0%29%29> (computation of kernel and image of $f$)

- <https://www.wolframalpha.com/input?i=Solve%28%28%281%2C1%2C-2%29%2C%28-2%2C4%2C-2%29%2C%28-5%2C5%2C0%29%29*%28x%2Cy%2Cz%29%3D%283%2Ct%2C-5%29%29> (compute the preimage of a vector)

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.40</strong></p>

<span id="sol-ex-maps-3-20" label="sol--ex:maps-3-20"></span> (See <a href="../exercises-maps/#ex-maps-3-20" data-reference-type="ref+Label" data-reference="ex:maps-3-20">Exercise 4.44</a>.) We form the matrix of $f$ and bring it to row echelon form:
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc} 1 & -1 & 2 \\ -2 & 3 & -1 \\ 0 & 1 & 3 \\ -1 & 3 & t \end{array} \right )
\leadsto
\left ( \begin{array}{ccc} 1 & -1 & 2 \\ 0 & 1 & 3 \\ 0 & 1 & 3 \\ 0 & 2 & t+2 \end{array} \right )
\leadsto
\left ( \begin{array}{ccc} 1 & -1 & 2 \\ 0 & 1 & 3 \\ 0 & 0 & 0 \\ 0 & 0 & t-4 \end{array} \right )
\]
</div>
The $\dim {\operatorname{im}\ } f$ equals the rank of that matrix, which is 2 if $t=4$ and 3 otherwise.

For no $t \in {\bf R}$, $f$ is surjective, since $\dim {\operatorname{im}\ } f \le 3$, but it would need to be 4 for $f$ to be surjective. For $t\ne 4$ it is injective. Indeed, the rank-nullity theorem (<a href="../maps-kernel-and-image-1/#thm-rank-nullity-theorem" data-reference-type="ref+Label" data-reference="thm:rank-nullity-theorem">Theorem 4.26</a>) asserts that $\dim \ker f = 3 - \dim {\operatorname{im}\ } f$, which is 0 for $t \ne 4$.

For $t=4$, we have $\ker f = L(-5,-3,1)$ and ${\operatorname{im}\ } f = L((-1,3,1,3), (1,-2,0,-1))$.

We have $w \notin {\operatorname{im}\ } f$ for all $t \in {\bf R}$. This can be shown by forming the augmented matrix
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc|c} 1 & -1 & 2 & 1 \\ -2 & 3 & -1 & 1 \\ 0 & 1 & 3 & 0 \\ -1 & 3 & t & 1 \end{array} \right )
\leadsto
\left ( \begin{array}{ccc|c} 1 & -1 & 2 & 1 \\ 0 & 1 & 3 & 3 \\ 0 & 1 & 3 & 0 \\ -1 & 3 & t & 1 \end{array} \right )
\leadsto \left ( \begin{array}{ccc|c} 1 & -1 & 2 & 1 \\ 0 & 0 & 0 & \underline{3} \\ 0 & 1 & 3 & 0 \\ -1 & 3 & t & 1 \end{array} \right )
\]
</div>
and the underlined entry $3$ shows $w \notin {\operatorname{im}\ } f$.

For $t=0$ we have seen above that $\dim {\operatorname{im}\ } f = 3$. By <a href="../spaces-dimension/#thm-basis-theorem" data-reference-type="ref+Label" data-reference="thm:basis-theorem">Theorem 3.71</a>, a basis $v_1, v_2, v_3$ of ${\operatorname{im}\ } f (\subset {\bf R}^4)$ can be extended to a basis of ${\bf R}^4$, say $v_1, v_2, v_3, v_4$. By <a href="../maps-linear-maps-defined-on-basis-vectors/#prop-linear-map-defined-on-basis" data-reference-type="ref+Label" data-reference="prop:linear-map-defined-on-basis">Proposition 4.40</a>, there is a unique linear map $g : {\bf R}^4 \to {\bf R}^3$ such that $g(v_i) = e_i$ (for $i=1,2,3$, and $e_i$ denotes the $i$-th standard basis vector of ${\bf R}^3$, and $g(v_4) = 0$ (or any other vector in ${\bf R}^3$). Then $g(f(x))=x$ for any $x \in {\bf R}^3$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.41</strong></p>

<span id="sol-ex-maps-2-7" label="sol--ex:maps-2-7"></span> (See <a href="../exercises-maps/#ex-maps-2-7" data-reference-type="ref+Label" data-reference="ex:maps-2-7">Exercise 4.45</a>.) The map $f$ is given by multiplication with the matrix, which we bring to row echelon form by elementary row operations
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc} 0 & -1 & 2 & 2 \\ 1 & 0 & -1 & 2 \\ -5 & 1 & 2 & -3 \end{array} \right ) 
\leadsto
\left ( \begin{array}{cccc} 0 & -1 & 2 & 0 \\ -3 & 6 & 0 & 4 \\ -8 & 1 & 2 & -3 \end{array} \right )
\leadsto
\left ( \begin{array}{cccc} 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ -2 & 1 & 2 & -3 \end{array} \right )
\]
</div>
It has 2 leading ones in the first two columns, so ${\operatorname{im}\ } f = L((0,2,-1,1), (-1,1,2,2))$. The third variable $z$ is a free variable, and $\ker f =L(-1,2,1)$.

The space $W$ defined by the equation $x_2 - 3x_3 = 0$ is the kernel of the matrix $\left ( \begin{array}{c} 0 \\ 1 \\ -3 \\ 0 \end{array} \right )$, which gives (for example) three free variables $x_1, x_3, x_4$, and accordingly a basis consisting of $(1,0,0,0), (0, 3, 1, 0), (0,0,0,1)$. We have $\dim W = 3$.

An element in $U = {\operatorname{im}\ } f$ is a linear combination of the first two column vectors, so of the form $(-b, 2a+b, -a+2b, a+2b)$, for arbitrary $a, b \in {\bf R}$. This lies in $W$ precisely if $2a+b-3(-a+2b)=0$, i.e., if $5a-5b=0$ or if $a=b$. A basis of $U \cap W$ is then given by choosing, say, $a=1$, and $U \cap W = L(-1,3,1,3)$.

We know $\dim U+W = \dim U + \dim W - \dim (U \cap W) = 2 + 3 - 1 = 4$. So, for example, the three basis vectors of $W$, together with any $u \in U \setminus W$ will form a basis. Thus, $(1,0,0,0), (0, 3, 1, 0), (0,0,0,1), (0, 2, -1, 1)$ forms a basis of $U+W$. (Note the last vector is not in $W$ since its does not satisfy the equation $x_2 - 3x_3 = 0$.)

In order to check when $(a,4,3,b)$ is in the image, we form the matrix corresponding to the linear system:
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cc|c} 0 & -1 & a \\ 2 & 1 & 4 \\ -1 & 2 & 3 \\ 1 & 2 & b \end{array} \right ) 
\leadsto
\left ( \begin{array}{cc|c} 0 & -1 & a \\ 0 & -3 & 4-2b \\ 0 & 4 & b+3 \\ 1 & 2 & b \end{array} \right ).
\]
</div>
This shows that $4-2b=3a$ and $4(4-2b)+3(b+3)=0$, i.e., $25-5b=0$, so $b=5$ and $a=-2$.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.42</strong></p>

<span id="sol-ex-maps-partial-2026-1" label="sol--ex:maps-partial-2026-1"></span> (See <a href="../exercises-maps/#ex-maps-partial-2026-1" data-reference-type="ref+Label" data-reference="ex:maps-partial-2026-1">Exercise 4.46</a>.) Part (1): The subspace $W \subset \mathbf R^4$ is the solution set of a homogeneous linear system. By <a href="../systems-matrices/#def-matrix-to-system" data-reference-type="ref+Label" data-reference="def:matrix-to-system">Definition 2.23</a>, the coefficient matrix describing that linear system reads $\left ( \begin{array}{cccc} 2 & -1 & -1 & 0 \\ 0 & 1 & -1 & 0 \end{array} \right )$. Thus, (after dividing the first row by 2), the leading ones in this matrix are in the first and second column, so $x_3$ and $x_4$ are free variables. By <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>, a basis of $W$ is given by the vectors $w_1 = (1,1,1,0)$ and $w_2 = (0,0,0,1)$. Hence $\dim W = 2$.

*Typical mistakes:* It is important to note that $W$ was defined as a subspace of ${\bf R}^4$. One must therefore take into account $x_4$, even though it is not present in the linear system as written.

Another typical mistake is to assume one can read of the basis vectors of $W$ simply as $(2,-1,-1,0)$ and $(0,1,-1,0)$. This is *wrong*, and can already be seen to be wrong by observing that these vectors do not even lie in $W$!

Part (2): To compute the subspace $U \cap W$ we first apply <a href="../spaces-linear-combinations/#lem-span-subspace" data-reference-type="ref+Label" data-reference="lem:span-subspace">Lemma 3.34</a> to write a general vector of $U$ as
<div class="arithmatex" markdown="1">
\[
a_1 u_1 + a_2 u_2 + a_3 u_3 = (a_1-a_2, -2a_1+a_2+3 a_3, 2a_2+a_3,a_1-a_3).
\]
</div>
Recall that $U \cap W$ consists of those vectors in $U$ that also lie in $W$ (<a href="../spaces-intersection/#lem-spaces-lemma-003" data-reference-type="ref+Label" data-reference="lem:spaces-lemma-003">Lemma 3.19</a>), so we need to check when the above vector lies in $W$. This happens if and only if
<div class="arithmatex" markdown="1">
\[
\begin{align*}
 0 & = 2(a_1-a_2)-( -2a_1+a_2+3 a_3)-(2a_2+a_3) = 4a_1 -5a_2-4a_3\\
0 & = -2a_1+a_2+3 a_3 - (2a_2+a_3) = -2a_1-a_2+2a_3
\end{align*}
\]
</div>
The solution of this system is $a_2=0$ and $a_1=a_3$. Therefore, the space $U \cap W$ consists of the vectors
<div class="arithmatex" markdown="1">
\[
a_1 u_1 + 0 u_2 + a_1 u_3 = a_1 (u_1+u_3).
\]
</div>
Thus, a basis vector of $U \cap W$ is $u_1+u_3=(1,1,1,0)$. In particular $\dim U \cap W=1$.

The three vectors $u_1, u_2, u_3$ spanning $U$ are linearly independent, as one sees from bringing the matrix into row echelon form:
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{cccc} 1 & -2 & 0 & 1 \\ -1 & 1 & 2 & 0 \\ 0 & 3 & 1 & -1 \end{array} \right ) 
\leadsto 
\left ( \begin{array}{cccc} 1 & -2 & 0 & 1 \\ 0 & -1 & 2 & 1 \\ 0 & 3 & 1 & -1 \end{array} \right )
\leadsto \text{etc.}
\]
</div>
and seeing that there are three leading ones. Therefore, $\dim U = 3$. <a href="../spaces-dimension/#thm-dim-cap-sum" data-reference-type="ref+Label" data-reference="thm:dim-cap-sum">Theorem 3.77</a> now allows to quickly compute $\dim (U+W)=\dim U + \dim W - \dim (U \cap W) = 3+2-1=4$. By <a href="../spaces-dimension/#thm-basis-theorem" data-reference-type="ref+Label" data-reference="thm:basis-theorem">Theorem 3.71</a>, we therefore obtain $U+W = \mathbf R^4$. Thus the standard basis $e_1, \dots, e_4$ is a basis of $U+W = \mathbf R^4$.

*Typical mistake:* One should not mix up columns and rows. While it is in principle possible to consider a matrix whose *columns* are the vectors $u_1, ...$, one then needs to perform elementary column operations. These are not discussed in these lecture notes (and are not necessary). For consistency with the methods applied in these notes, it is advisable to only write down these vectors in rows as mentioned above.

Part (3) We know that $\dim W=2$, so if we want that $U' \oplus W = {\bf R}^4$, we must have $\dim U' = 2$ by <a href="../spaces-dimension/#rem-dimension-direct-sum" data-reference-type="ref+Label" data-reference="rem:dimension-direct-sum">Remark 3.68</a> Since we know that $U \cap W = {\bf R} (1,1,1,0)$, it therefore is enough to find two linearly independent vectors $u'_1, u'_2 \in U$ that are both independent of $r := (1,1,1,0)$. For example, $u'_1 = u_1$, $u'_2 = u_2$ satisfy these requirements, as one sees by bringing
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{c} u_1 \\ u_2 \\ r \end{array} \right ) = \left ( \begin{array}{cccc} 1 & -2 & 0 & 1 \\ -1 & 1 & 2 & 0 \\ 1 & 1 & 1 & 0 \end{array} \right )
\]
</div>
into row-echelon form.

</div>

<div class="solution" markdown="1">


<p class="env-number"><strong>Solution 4.13.43</strong></p>

<span id="sol-ex-maps-partial-2026-2" label="sol--ex:maps-partial-2026-2"></span> (See <a href="../exercises-maps/#ex-maps-partial-2026-2" data-reference-type="ref+Label" data-reference="ex:maps-partial-2026-2">Exercise 4.47</a>.) Part (1): Using Gaussian elimination (<a href="../systems-gaussian-elimination/#met-gaussian-algorithm" data-reference-type="ref+Label" data-reference="met:gaussian-algorithm">Method 2.29</a>) we bring the matrix $A$ into row echelon form (as far as possible):
<div class="arithmatex" markdown="1">
\[
A = \begin{pmatrix}
1 & 2 & 1 \\
2 & 4a^2 & -1 \\
-1 & -2 & a
\end{pmatrix}
\leadsto 
\left ( \begin{array}{ccc} 1 & 2 & 1 \\ 0 & 4a^2-4 & -3 \\ 0 & 0 & a+1 \end{array} \right )
\]
</div>
In order to proceed, we need to distinguish the case $a=-1$ and $a \ne -1$. In the former case the matrix reads $\left ( \begin{array}{ccc} 1 & 2 & 1 \\ 0 & 0 & -3 \\ 0 & 0 & 0 \end{array} \right )$ and has rank 2. In the case $a \ne -1$, we have $a+1 \ne 0$, so we can divide the third row by $a+1$ (cf. <a href="../systems-gaussian-elimination/#def-elementary-row-operations" data-reference-type="ref+Label" data-reference="def:elementary-row-operations">Definition 2.28</a>) and get
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc} 1 & 2 & 1 \\ 0 & 4a^2-4 & -3 \\ 0 & 0 & 1 \end{array} \right )
\leadsto 
\left ( \begin{array}{ccc} 1 & 2 & 1 \\ 0 & 4a^2-4 & 0 \\ 0 & 0 & 1 \end{array} \right )
\]
</div>
The rank of this matrix is 3 provided that $4a^2-4 \ne 0$ and 2 if $4a^2-4=0$, i.e., if $a=1$. In summary, the rank is 2 if $a = \pm 1$ and is 3 otherwise.

*Typical mistake:* one should not stop the analysis after the first step above.

Part (2): We apply <a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a> and bring the augmented matrix of the system into row echelon form:
<div class="arithmatex" markdown="1">
\[
\begin{align*}
\left ( \begin{array}{ccc|c} 1 & 2 & 1 & b_1 \\ 2 & 4 & -1 & b_2 \\ -1 & -2 & 1 & b_3 \end{array} \right )
& \leadsto
\left ( \begin{array}{ccc|c} 1 & 2 & 1 & b_1 \\ 0 & 0 & -3 & b_2-2b_1 \\ 0 & 0 & 2 & b_3+b_1 \end{array} \right )
\\
&\leadsto
\left ( \begin{array}{ccc|c} 1 & 2 & 1 & b_1 \\ 0 & 0 & -3 & b_2-2b_1 \\ 0 & 0 & 0 & 2(b_2-3b_1)+3(b_3+b_1) \end{array} \right )
\end{align*}
\]
</div>
There is a solution precisely if the last entry is zero, i.e., if $2(b_2-2b_1)+3(b_3+b_1) = 0$ or if $-b_1 +2b_2 + 3b_3=0$.

*Typical mistake:* It is not legitimate to use the row echelon form of the matrix $A$ computed in the Part (1) above, and then to append the vector $\left ( \begin{array}{c} b_1 \\ b_2 \\ b_3 \end{array} \right )$. The row operations performed on the matrix $A$ must be identically performed on this vector, otherwise one changes the linear system.

Part (3): We again use Gaussian elimination to solve the system (<a href="../systems-gaussian-elimination/#met-gaussian-elimination-solve" data-reference-type="ref+Label" data-reference="met:gaussian-elimination-solve">Method 2.31</a>). One forms the augmented matrix
<div class="arithmatex" markdown="1">
\[
\left ( \begin{array}{ccc|c} 1 & 2 & 1 & 2 \\ 2 & 4 & -1 & 7 \\ -1 & -2 & -1 & c \end{array} \right )
\leadsto 
\left ( \begin{array}{ccc|c} 1 & 2 & 1 & 2 \\ 0 & 0 & -3 & 3 \\ 0 & 0 & 0 & 2+c \end{array} \right )
\]
</div>
This shows that there is a solution if $c=-2$. One then computes $x_3=-1$, $x_1=2-2x_2-x_3=3-2x_2$.

*Typical mistake:* Again, the row operations performed on the matrix $A$ must also be performed on the vector $\left ( \begin{array}{c} 2 \\ 7 \\ c \end{array} \right )$.

</div>
