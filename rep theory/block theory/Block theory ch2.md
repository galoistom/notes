# Induction and restirction
**Definition**:
Let $G$ be a finite group and let $H$ be a subgroup of $G$. 
We denote by $Res_H^G:Mod(k[G]) \rightarrow Mod(k[H])$ the *restriction functor* sending a $k[G]$-homomorphism $\phi:U \rightarrow U'$ to $\phi$ viewed as a $k[H]$-homomorphism. 
We denote by $Ind_H^G:Mod(k[H]) \rightarrow Mod(k[G])$ the *induction functor* sending a $k[H]$-module $V$ to the $k[G]$-module $Ind_H^G(V)=k[G] \otimes_{k[H]}V$ and sending a $k[H]$-homomorphism $\phi:V \rightarrow V'$ to the $k[G]$-homomorphism $id_{k[G]} \otimes \psi:k[G] \otimes_{k[H]}V \rightarrow k[G] \otimes_{k[H]} V'$. 

**Proposition**:
Let $G$ be a finite group and let $H,L$ be subgroups of $G$ such that $L \leq H \leq G$. For ant $k[G]$-module or complex of $k[G]$-modules $V$ we have a natural isomorphism $Res_L^{G}(V) \simeq Res_{L}^{H}(Res_H^G(V))$ and it is also true for $Ind$.

**Theorem**:
Let $G$ be a group and let $H$ be a subgroup of $G$. The covariant functors $Ind_H^G:Mod(k[H]) \rightarrow Mod(k[G])$ and $Res_H^G:Mod(k[G]) \rightarrow Mod(k[H])$ are k-linear exact. Moreover, both functors sends projective moudules to projective modules.

*Proof*:
Take a exact sequence of $k[G]$: $U \stackrel{\phi}{\longrightarrow} V \stackrel{\psi}{\longrightarrow} W$ then we have that $Im(\phi)=ker(\psi)$ and $Res_H^G$ is clearly exact. On the other hand, note that $k[H] \otimes_{k[H]} -$ is clearly exact, so $k[G]=\bigoplus_{x \in G/H}xk[H]$ is also exact. 

**Remark**:The definition of $Ind$ and $Res$ can be extended to general algebra $B \leq A$ or even to homomorphism $B \stackrel{\alpha}{\longrightarrow} A$, denoted by $Res_\alpha:Mod(A) \rightarrow Mod(B)$ ( by acting as $\alpha(b)$ ) and $Ind_\alpha:Mod(B) \rightarrow Mod(A)$ ( by tensor $A_\alpha \otimes -$ ), this lead us thinking about the twisted group $\alpha \in Z^2(G;k^\times)$, and the above proprsition still holds.

**Definition**:
Let $G$ be a finite group, $H$ a subgroup anb $V$ a $k[H]$-module. We define a $k[G]$-module $Ten_H^G(V)$ as follows. Set $n=|G:H|$, and let $\{x_i|1\leq i \leq n\}$ be a set of representatives of $G/H$ in $G$. Set $Ten_H^G(V)=\bigotimes_{i=1}^n(x_i \otimes V)$, the tensor product over $k$ of the k-modules $x_i \otimes V$ of $k[G] \otimes_{k[H]}V$, endowed with the following action of $G$. Let $x \in G,\ \pi \in S_n$ and $y_i \in H$ such that $xx_i=x_{\pi^{-1}(i)}y_i$, and let $v_i \in V$, for $1 \leq i \leq n$. Set $x \cdot (\bigotimes_{i=1}^n(x_i \otimes v_i))=\otimes_{i=1}^n(x_i \otimes y_{\pi(i)}v_{\pi(i)})$. One checks that the above definition is well defined.