#algebra #rp 
[[Basic Definitions of representation]]

# Statement
Let $G$ be a finite group and let $\chi_{1},\dots,\chi_{h}$ be its distinct irrducible characters (c.f. [[Property of the character table]]). Recall that a class function of $G$ is a character if and only if it is a linear combination of the $\chi_{i}$'s with non-negative integer coefficients, we will denote the set of these functions as $R^{+}(G)$ and $R(G)$ will refer to $\mathbb{Z}\chi_1\oplus\dots \oplus \mathbb{Z}\chi_{h}$, as a "generalization" of character, called *virtral character*. As one immediately notice, $R(G)$ is a subring of the ring $F_{\mathbb{C}}(G)$ of the complex class function on $G$, and $\chi_{i}$ form the basis of $F_{\mathbb{C}}(G)$, so $\mathbb{C}\otimes R(G)$ identifies with $F_{\mathbb{C}}(G)$. 

**Remark**: It can also be viewed as the [[Grothendieck group]] of the category of finite generated $\mathbb{C}[G]$-modules. 

In this case, if $H\leq G$, then the *restriction* operation of defins a $R(G)\rightarrow R(H)$, denoted by $Res_{H}^{G}$ or $Res$ in short. And the *induction* operation $R(H)\rightarrow R(G)$ denoted by  $Ind_{H}^{G}$ or $Ind$ in short. In particular, consider the bilinear form $\langle \phi,\psi \rangle_{H}$ and $\langle \phi,\psi \rangle_{G}$, especially with $Ind(\phi \cdot Res(\psi))=Ind(\phi)\cdot \psi$. 

>[!throrem] Artin's Theorem
>Let $X$ be a family iof subgroups of a finite group $G$. Let $Ind:\bigoplus_{H \in X} R(H)\rightarrow R(G)$ be the homomorphism defined by the family of $Ind_{H}^{G}$, $H\in X$. Then the following propperties are equivalent:
>1. $G$ is the union of teh conjugates of the subgroups belonging  to $X$.
>2. The cokernel of $Ind:\bigoplus_{H\in X}R(H)\rightarrow R(G)$ is finite.

The second part can also be written as: For each character $\chi$ of $G$, there exist virtual characters  $\chi_{H}\in R(H)$, $H\in X$, and an integer $d\geq1$ such that $d_{\chi}=\sum Ind_{H}^{G}(\chi_{H})$. 

# First Proof
First show that 2 implies 1. Let $S=\bigcup_{H \in X,\,g\in G} gHg^{-1}$, then the function of the form $\sum Ind^{G}_{H}(f_{H})$ for $f_{H} \in R(H)$ vanishes off $S$. Now if 2 satisfied, we know that all class function on $G$ vanishes off $S$, hence $G=S$, so 1 holds.

Conversly, if 1 is satisfied. It is suffices to show that the $\mathbb{C}$-linear map 
$$
\mathbb{C}\otimes Ind:\bigoplus_{H\in X}\mathbb{C}\otimes R(H) \longrightarrow \mathbb{C}\otimes R(G)
$$
is surjective. By duality, it is equivalent to the injectivity of the adjoint map
$$
\mathbb{C}\otimes Res:\mathbb{C}\otimes R(G)\longrightarrow \bigoplus_{H\in X}\mathbb{C}\otimes R(H)
$$
which is obvious as it amounts to saying that if a class function on $G$ restricts to 0 on each cyclic subgroup, then it is zero. 

# Second proof
Let $A$ be a cyclic group with order $a$. Define a function $\theta_{A}$ on $A$ with:
$$
\theta_{A}(x)=\begin{cases}a\qquad \text{if } x \text{ generates } A \\
0 \qquad\text{otherwise}\end{cases}
$$

