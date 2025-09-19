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

We then notice the two following proposition:
1. If $G$ is a finite group of order $g$, then $g=\sum_{A\subset G}Ind_{A}^{G}(\theta_{A})$, where $A$ runs through all the cyclic subgroups of $G$.
2. If $A$ is a cyclic group, then $\theta_{A}\in R(A)$. 

For the first, put $\theta_{A}'=Ind^{G}_{A}(\theta_{A})$. For $x \in G$ we have 
$$
\theta'_{A}(x)=\frac{1}{a}\sum_{y\in G,yxy^{-1}\in A}\theta_{A}(yxy^{-1})=\frac{1}{a}\sum_{y \in G,yxy^{-1}\,gen.A} a = \sum_{y\in G, yxy^{-1}\,gen.A}1
$$
, taking sum over $A\subset G$, then we notice that $yxy^{-1}$ generates a unique cyclic subgroup of $G$ for each $y\in G$, we have $LHS=g$. 

As to the second one, we proof it by induction. We know that $a=\sum_{b\subset A}Ind_{B}^{A}(\theta_{B})=\theta_{A}+\sum_{B\neq A}Ind_{B}^{A}(\theta_{B})$. The induction hypothesis gives $\theta_{B}\in R(B)$ for $B\neq A$, hence $Ind_{B}^{A}(\theta_{B})$ belongs to $R(A)$; on hte other hand. It is clear that $a\in R(A)$ and so it follows that $\theta_{A}$ belongs to $R(A)$. 

How those this helps us the proof the Artin's theorem? In fact, on note that If $A'$ is contained in $gAg^{-1}$ for some $g$, then $Ind_{A'}^{G}$ is contained in $Ind_{A}^{G}$, so we may assume without loss that $X$ is consists of only cyclic subgroups. Using the proposition above, we know that $g=\sum_{A\in X}Ind_{A}^{G}(\theta_{A})$ belongs to the image of $Ind$, which is in fact an ideal, so it proof the second sersion of 2.  

**Proposition**: If $A$ is cyclic of order $a$, put $\lambda_{A}=\phi(a)r_{A}-\theta_{A}$, where $\phi(a)$ is the number of generators of $A$ and $r_{A}$ is the character of regular representation of $A$ (c.f. [[Basic Definitions of representation]]). Then $\lambda_{A}$ is orthogonal to the unit character. Show that, if $A$ runs over the set of cyclic subgroups of a group $G$ of order $g$, we have $\sum_{A\subset G}Ind_{A}^{G}(\lambda_{A})=g(r_{G}-1)$, where $r_{G}$ is the character of the regular representation of $G$. 

*proof*: $\frac{1}{a}\sum_{g}\overline{T(g)}(\phi(a)\cdot r_{A}(g)-\theta_{A})=\frac{1}{a}\sum_{g}(\phi(a)r_{A}(g)-\theta_{A}(g))$, note that $\frac{1}{a}\sum_{g}\theta_{A}=\phi(a)$, and $\frac{1}{a}\sum_{g}r_{A}(g)=a$, so it is clear that is is orthogonal to the unit representation. Now use the proposition above, we have $\sum_{A\subset G}Ind_{A}^{G}(\theta_{A})=g$, so we only have to proof that $\sum_{A\subset G}Ind_{A}^{G}(\phi(a)r_{A})=gr_{G}$. In fact, $Ind_{A}^{G}r_{A}(x)=\frac{1}{a}\sum_{y\in G,\,yxy^{-1}\in A}r_{A}(yxy^{-1})$, one immediately notice that $Ind_{A}^{G}r_{A}(x)$ is nonzero if and only if $x=1_{G}$, as $yxy^{-1}=1_{A}$ <==> $x=1_{G}$. In this case $Ind_{A}^{G}r_{A}(1_{G})=g\phi(a)$, now  with $a|g$, we have $\sum_{A\subset G}Ind_{A}^{G}r_{A}(1_{G})=g\sum_{a|n}\phi(a)=g^{2}$, so $\sum_{A\subset}$ 