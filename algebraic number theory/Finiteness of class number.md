>[!note] Main Theorem
>Let $K$ be an extension of degree $n$ of $\mathbb{Q}$, and let $\Delta_K$ be the discriminant of $K/\mathbb{Q}$. Let $2s$ be the number of nonreal complex embedings of $K$. Then there exists a set of representatives of the ideal calss group of $K$ consisting of integeral ideals $\mathfrak{a}$ with 
>$$\mathbb{N}(\mathfrak{a}) \leq \frac{n!}{n^n} (\frac{4}{\pi})^s |\Delta_K|^{\frac{1}{2}}$$

We called the number on the right the **Mikowski bound** which we sometime denote it by $B_K$.

There are something left to be explained. 
1. $\mathbb{N}(\mathfrak{a})=(\mathcal{O}_K:\mathfrak{a})$ is the norm of the fractional ideal $\mathfrak{a}$ (c.f.[[Dedekind domain]]) i.e. Let $A$ be a dedekind domain with field of fraction $K$, and $L$ be a finite extension of $K$ with $B$ the integeral closure of $A$, then the morphism $Nm:Id(B) \longrightarrow Id(A)$ should make the following diagram commute:
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
&L^{\times} \arrow[r] \arrow[d,"Nm"] &Id(B) \arrow[d,"Nm"]\\
&K^{\times} \arrow[r] &Id(A)
\end{tikzcd}
\end{document}
```
2. $\Delta_K=disc(K/\mathbb{Q})$ is the discriminant of $K/\mathbb{Q}$ i.e. the image of $det(Tr(\beta_i\beta_j))$ in $\mathbb{Q}/\mathbb{Q}^2$ where $\beta_1, \cdots, \beta_n$ is a basis of $K$ as a vector space of $\mathbb{Q}$.

Now we start to proof the theorem.
1. We first introduce the concept of Lattices.
>[!note] Lattices
>Let $V$ be a finite diensional $\mathbb{R}$ vector space. A lattice $\Lambda$ is a subgroup of th from $$\Lambda=\mathbb{Z}e_1 + \cdots +\mathbb{Z}e_r$$ with $e_1,\cdots e_r$ linearly independent in $V$.

It can also be defined as a discrete subgrup of $V$ with the natural topology of $\mathbb{R}^n$. Using this, we have a very useful theorem.

>[!note] [[Minkowski Lattice Therorem]]
>Let $T$ be a subsey of $V$ that is compact, convex, and symmetric in the origin. If $\mu(T) \geq 2^n \mu(D)$ then $T$ contains a point of the lattice other that the origin.

2. Let $V:=\mathbb{R}^r \times \mathbb{C}^s$ if $K$ has $r$ real embedings over $\mathbb{Q}$ and $s$ complex embedings. Using the basis $\{1,i\}$ for $\mathbb{C}$. Let $\mathfrak{a}$ be a nonzero ideal of $\mathcal{O}_K$ and we check that $\sigma(\mathfrak{a})$ forms a lattice and the volume of the fundamental parallelopiped is $2^{-s} \cdot \mathbb{N}(\mathfrak{a}) \cdot |\Delta|^{\frac{1}{2}}$ by taking a basis $a_1,\cdots ,a_n$ of $\mathfrak{a}$. Then we need to check $det(A) \neq 0$, where $A$ is a matrix whose i-th row is $(\sigma_1(a_i), \cdots, \sigma_r(a_i),\mathcal{R}(\sigma_{r+1}(a_i)),\mathcal{S}(\sigma_{r+1}(a_i)), \cdots , \mathcal{R}(\sigma_{r+s}(a_i)),\mathcal{S}(\sigma_{r+s}(a_i)))$, we know that $det(B)^2=D(a_1,\cdots,a_n)$ if the i-th row of $B$ is $(\sigma_1(a_i), \cdots, \sigma_r(a_i),\sigma_{r+1}(a_i),\overline{\sigma_{r+1}(a_i)}, \cdots , \sigma_{r+s}(a_i),\overline{\sigma_{r+s}(a_i)})$, thus $det(A)=(-2i)^s det(B)\neq 0$. Moreover, $D(a_1,\cdots,a_n)=(\mathcal{O}_K:\mathfrak{a})^2 \Delta_K$, whence $\mu(D)=2^{-s} \cdot \mathbb{N}(\mathfrak{a}) \cdot |\Delta|^{\frac{1}{2}}$. 
3. Note that if we let $X(t)=\{x \in V | \lVert x \rVert \leq t\}$ where $\lVert x \rVert = \sum\limits_{i=1}^{r} |x_i| + 2\sum\limits_{i=r+1}^{r+s} |z_i|$, then $\mu(X(t))=2^r \cdot (\frac{\pi}{2})^s \cdot \frac{t^n}{n!}$. Now let $t^n=n! \cdot \frac{2^{n-r}}{\pi^{s}} \cdot \mathbb{N}(\mathfrak{a}) \cdot |\Delta_K|^{\frac{1}{}2}$. Then by the theorem above, we get taht there exists an $\alpha \in \mathfrak{a}-\{0\}$ such that $|Nm(\alpha)| \leq \frac{n!}{n^n} \cdot \frac{2^{n-r}}{\pi^{s}} \cdot \mathbb{N}(\mathfrak{a}) \cdot |\Delta_K|^{\frac{1}{2}}$. 
4. With this we proof the main theorem. Let $\mathfrak{c}$ is a fractional ideal of $K$, and fro some $d \in K^{\times},d\mathfrak{c}^{-1}$ is an integeral ideal, say $(d)\mathfrak{c}^{-1}=\mathfrak{b}$, then we have $|Nm(\beta)| \leq B_K \cdot \mathbb{N}(\mathfrak{b})$ for some $\beta \in \mathfrak{b}$, then we get a $\mathfrak{a} \mathfrak{b}=\beta \mathcal{O}_K$ and $\mathfrak{a}$ integeral, thus $\mathfrak{a}$ is equivalent to $\mathfrak{c}$ up to a principle ideal. Then by the property of $\beta$, we have $\mathbb{N}(\mathfrak{a}) \leq B_K$.  

The main theorem immediately lead to the finiteness of the class number of [[Dedekind domain]].  