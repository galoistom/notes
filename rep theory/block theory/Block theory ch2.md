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
Let $G$ be a finite group, $H$ a subgroup anb $V$ a $k[H]$-module. We define a $k[G]$-module $Ten_H^G(V)$ as follows. Set $n=|G:H|$, and let $\{x_i|1\leq i \leq n\}$ be a set of representatives of $G/H$ in $G$. Set $Ten_H^G(V)=\bigotimes_{i=1}^n(x_i \otimes V)$, the tensor product over $k$ of the k-modules $x_i \otimes V$ of $k[G] \otimes_{k[H]}V$, endowed with the following action of $G$. Let $x \in G,\ \pi \in S_n$ and $y_i \in H$ such that $xx_i=x_{\pi^{-1}(i)}y_i$, and let $v_i \in V$, for $1 \leq i \leq n$. Set $x \cdot (\bigotimes_{i=1}^n(x_i \otimes v_i))=\otimes_{i=1}^n(x_i \otimes y_{\pi(i)}v_{\pi(i)})$. One checks that the above definition is well defined. This is some how view $G$ as $H^n \rtimes S_n$. one check that $Ten_H^G(V)\simeq Res_G^{H^n \rtimes S_n}(V^{\otimes n})$. 

**Proposition**:
let $G$ be a finite group, and let $H,L$ be subgroups of $G$. Let $V,V'$ be $k[H]$-modules and let $W$ be a $k[L]$-module.
1. If $L \leq H$, then $Ten^G_L(W) \simeq Ten_H^G(Ten_L^H(W))$. 
2. We have $Ten_H^G(V \otimes_k V'\simeq Ten_H^G(V) \otimes_k Ten_H^G(V')$.

# Forbenius reciprocity
**Theorem**(Forbenius reciprocity)
Let $G$ be a finite group and $H$ a subgroup of $G$. Let $U$ be a $k[G]$-module and $V$ a $k[H]$-module.
- we have a natural k-linear isomorphism
$$
\begin{cases}Hom_{k[G]}(Ind_H^G(V), U) &\simeq Hom_{k[H]}(V,Res_H^G(N))\\
\phi &\mapsto (v \mapsto \phi(1_G \otimes v))\end{cases}
$$
- we have a natural k-linear isomorphism
$$
\begin{cases}
Hom_{k[H]}(Res_H^G(V),U) \simeq Hom_{k[H]}(V,Res_H^G(U))\\
\psi \mapsto (u \mapsto \sum_{x \in [G/H]}x \otimes \psi (x^{-1}u)).
\end{cases}
$$

*Proof*:
simple, one immediately check that the maps are all well defined, and that the map sending $\psi \in Hom_{k[H]}(V,Res_H^G(U))$ to be the unique linear map $\phi$ refinded by $\phi(x \otimes v) = x\psi (v)$ for $x \in G$ and $v \in V$ is its inverse. The other way is similiar.

**Theorem**:
Let $G$ be a finite group and $H$ a subgroup of $G$. Let $U$ be a $k[G]$-module and $V$ a $k[H]$-module. There is a natural isomorphism if $k[G]$-modules
$$
\begin{cases}U \otimes_k Ind_{H}^G(V) &\simeq Ind_H^G(Res_H^G(U) \otimes_kV)\\
u \otimes (x \otimes v) &\mapsto x \otimes (x^{-1}u \otimes v)
\end{cases}
$$
where $u \in U$ and $v \in V$.

*Proof*:easy.

**Theorem**:
Let $A$ be a k-algebra and $B$ a subalgebra of $A$. For any $A$-module $U$ and any $B$-module $V$ we have natural inverse isomorphism of k-modules
$$
\begin{cases}
Hom_A(A \otimes_BV,U) &\simeq Hom_B(V,Res_B^A(U))\\
\phi &\mapsto (v \mapsto \phi(1 \otimes v))\\
(a \otimes v \mapsto a \psi(v)) &\leftarrowtail \psi
\end{cases}
$$

This is easy to varify but there is a more general case.

Consider the following two functors: $M \otimes_B-:Mod(B) \rightarrow Mod(A)$ and $Hom_A(M,-):Mod(A) \rightarrow Mod(B)$. Now if $B$ is a subalgebra of $A$ and $M=A$, viewed as $A,B$-bimodule, then $M \otimes_B -$ is the induction functor $Ind_B^A$ and $Hom_A(M,-)$ is the functor $Res_B^A$. 

**Theorem**:
Let $A,B$ be k-algebra and let $M$ be an $A-B$-bimodule. For any $A$-module $U$ anf any $B$-module $V$ we have natural inverse isomorphism of $k$-modules
$$
\begin{cases}
Hom_A(M\otimes_BV,U) &\simeq Hom_B(V,Hom(M,U))\\
\phi &\mapsto (v\mapsto(m\mapsto \phi(m,\otimes v)))\\
(m \otimes v \mapsto \psi(v)(m) &\leftarrowtail \psi
\end{cases}
$$

*Proof*:
rutine