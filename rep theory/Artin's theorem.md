#algebra #rp 
[[Basic Definitions of representation]]

Let $G$ be a finite group and let $\chi_{1},\dots,\chi_{h}$ be its distinct irrducible characters (c.f. [[Property of the character table]]). Recall that a class function of $G$ is a character if and only if it is a linear combination of the $\chi_{i}$'s with non-negative integer coefficients, we will denote the set of these functions as $R^{+}(G)$ and $R(G)$ will refer to $\mathbb{Z}\chi_1\oplus\dots \oplus \mathbb{Z}\chi_{h}$, as a "generalization" of character, called *virtral character*. As one immediately notice, $R(G)$ is a subring of the ring $F_{\mathbb{C}}(G)$ of the complex class function on $G$, and $\chi_{i}$ form the basis of $F_{\mathbb{C}}(G)$, so $\mathbb{C}\otimes R(G)$ identifies with $F_{\mathbb{C}}(G)$. 

**Remark**: It can also be viewed as the [[Grothendieck group]] of the category of finite generated $\mathbb{C}[G]$-modules. 

In this case, if $H\leq G$, then the *restriction* operation of defins a $R(G)\rightarrow R(H)$, denoted by $Res_{H}^{G}$ or $Res$ in short. And the *induction* operation $R(H)\rightarrow R(G)$ denoted by  $Ind_{H}^{G}$ or $Ind$ in short. In particular, consider the bilinear form $\langle \phi,\psi \rangle_{H}$ and $\langle \phi,\psi \rangle_{G}$, especially with $Ind(\phi \cdot Res(\psi))=Ind(\phi)\cdot \psi$. 