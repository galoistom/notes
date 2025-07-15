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

**Theorem**:
Let $A,B,C$ be k-algebras, ket $M$ be an $A-B$-bimodule, $U$ an $A-C$-bimodule and $V$ a $B-C$-bimodule. We have a natural isomorphism of $k$-modules $$Hom_{A \otimes_k C^{op}}(M \otimes_B V, U) \simeq Hom_{B \otimes_k C^{op}}(V,Hom_A(M,U))$$
*Proof*:
just the same as above. 

# Adjoint functors
**Definition**:
Let $\mathcal{C},\mathcal{D}$ be categories and let $\mathcal{F}: \mathcal{C} \rightarrow \mathcal{D}$, $\mathcal{G}: \mathcal{D} \rightarrow \mathcal{C}$ be covariant functors. We say that $\mathcal{G}$ is *left adjoint* to $\mathcal{F}$ and that $\mathcal{F}$ is *right adjoint* to $\mathcal{G}$, if there is an isomorphism of bifuntors $Hom_\mathcal{C}(\mathcal{G}(-),-) \simeq Hom_{\mathcal{D}}(-,\mathcal{F}(-))$. If $\mathcal{G}$ if left and right adjoint to $\mathcal{F}$ we say that $\mathcal{F}$ and $\mathcal{G}$ are *biadjoint*.

**Theorem**:
Let $\mathcal{C},\mathcal{D}$ be categories and let $\mathcal{F} :\mathcal{C} \rightarrow \mathcal{D}$, $\mathcal{G}: \mathcal{D} \rightarrow \mathcal{C}$ be covariant functors.
1) Suppose there is an adjunction isomorphism $\Phi: Hom_{\mathcal{C}}(\mathcal{G}(-),-) \simeq Hom_{\mathcal{D}}(-,\mathcal{F}(-))$. The unit $f$ and counit $g$ of $\Phi$ satisfy $(\mathcal{F}g)\circ (f\mathcal{F})= id_{\mathcal{F}}$ and $(g \mathcal{G})\circ (\mathcal{G} f)=id_{\mathcal{G}}$.
2) Let $f:id_{\mathcal{D}} \rightarrow \mathcal{F} \circ \mathcal{G}$ and $g:id_{\mathcal{C}}:\mathcal{G}\circ \mathcal{F} \rightarrow id_{\mathcal{C}}$ be two natural transformation satisfying $(\mathcal{F}g)\circ (f\mathcal{F})= id_{\mathcal{F}}$ and $(g \mathcal{G})\circ (\mathcal{G} f)=id_{\mathcal{G}}$. There is a unique adjunction isomorphism $\Phi: Hom_{\mathcal{C}}(\mathcal{G}(-),-) \simeq Hom_{\mathcal{D}}(-,\mathcal{F}(-))$ such that $f$ is the unit of $\Phi$ and $g$ is the counit of $\Phi$.
3) Let $\Phi: Hom_{\mathcal{C}}(\mathcal{G}(-),-) \simeq Hom_{\mathcal{D}}(-,\mathcal{F}(-))$ be an adjunction isomorphism with unit $f$ and counit $g$. Then $\Phi(V,U)(\phi) = \mathcal{F}(\phi) \circ f(V)$ for any object $U$ in $\mathcal{C}$, any object $V$ in $\mathcal{D}$ and any morphism $\psi:\mathcal{G}(V) \rightarrow U$ in $\mathcal{C}$ and $\Phi(V,U)^{-1}(\psi)=g(U)\circ \mathcal{G}(\psi)$ for any morphism $\psi:V \rightarrow \mathcal{F}(U)$ in $\mathcal{D}$. In particular, we have $\phi=g(U)\circ \mathcal{G}(\mathcal{F}(\phi)\circ f(V))$ and $\psi=\mathcal{F}(g(U) \circ \mathcal{G}) \circ f(V)$. 


**Theorem**:
Let $\mathcal{C}$, $\mathcal{D}$ be abelian categories. Let $\mathcal{F}:\mathcal{C} \rightarrow \mathcal{D}$ and $\mathcal{G}:\mathcal{D} \rightarrow \mathcal{C}$ be additive covariant functors. Suppose that $\mathcal{G}$ is left adjoint to $\mathcal{F}$. 
1) $\mathcal{G}$ is right exact and $\mathcal{F}$ is left adjoint.
2) If $\mathcal{F}$ is exact then $\mathcal{G}$ preserve projectivity.
3) If $\mathcal{G}$ is exact then $\mathcal{F}$ preserve injectivity.

# Mackley's formula
Mackley's formula discribes the ecomposition of the induction functor $Ind_L^G$ from a subgroup $L$ of a finte group $G$ followed by restriction functor $Res_H^G$ to some possibly different subgroup $H$ of $G$. 

**Theorem**(Mackley's formula):
Let $G$ be a finite group and let $H,L$ be subgroups of $G$.
1) We have $k[G]=\bigoplus_{x\in [H\backslash G / L]} k[HxL]$ as $k[HxL]$ as $k[H]-k[L]$-bimodules.
2) For any $x \in G$ we have an isomorphism of $k[H]-k[L]$-bimodules $k[HxL] \simeq k[H]\otimes_{k[H \,\cap \,^xL]}k[xL]$ mapping $yxz$ to $y \otimes xz$ where $y \in H$ and $z \in L$.
3) Let $B$ be a k-algebra, and let $W$ be a $k[L]-B$-bimidule or a complex of $k[L]-B$-bimidules. There is a natural isomorphism of $k[H]-B$-bimidules $$Res_H^G Ind_L^G(W) \simeq \bigoplus_{x \in [H\backslash G / L]} Ind_{H\,\cap\,^xL}^H Res_{H\, \cap \,^xL}^{^xL}(^xW)$$
*Proof*:
The statement 1 follows from the partition of $G$ into $H-L$-double coset. For the second statement, we first check that the assignment sending $yxz$ to $y \otimes xz$ is well defined. Let $y,y' \in H$ and $z,z' \in L$ such that $yxz=y'xz'$. We need to show that $y \otimes xz= y' \otimes xz'$ are equal. Multiplying by $y^{-1}$ on the left and by $(xz')^{-1}$ then we have $y^{-1}y'=xz(z')^{-1}x^{-1} \in H\, \cap \,^x L$. Thus setting $w=y^{-1}y'$, and using the tensor product on the right side in 2 is taken over $k(H\, \cap \,^xL)$, we can easily check $y \otimes xz= y' \otimes xz'$. Statement 3 follows from tensoring the formulae in 1,2 with $- \otimes_{k[L]} W$. 

This tells us that $V$ is a direct summand of $Res_{H}^G(Ind_H^G(V))$ as $RHS = (k[H] \otimes_{k[H]} V) \oplus (k[G\backslash H] \otimes_{k[H]} V)$, in fact, $Res_{N}^G(Ind_H^G(V)) = \bigoplus_{x \in [G/N]} \,^xV$ if $N \triangleleft G$. 

**Proprsition**:
Let $G$ be a finte group and $G$ and $H$ a subgroup of $G$. For any $k[G]$-module $U$ and any $k[H]$-module $V$ we have a natural isomorphism of $k[G]$-modules $$Ind_H^G(V) \otimes_k U \simeq Ind_H^G(V \otimes_k Res_H^G(U))$$sending $(x \otimes v) \otimes u$ to $x \otimes (v \otimes(x^{-1}u))$, where $x \in G, u \in U, v \in V$. 

**Theorem**
Let $G$ be a finite group, $N$ a normal subgroup of $G$. Suppose that $k$ is a splitting field for both $G$ and $N$, and that $|G:N|$ is invertible in $k$. Let $S$ be a simple $k[N]$-module. Then $Ind_N^G(S)$ is simple if and only if $S\, \not\simeq \,^xS$ for all $x\in G\backslash N$. 

*Proof*:
Note that $^xS$ is a simple $k[N]$-module for any $x \in G$. It follows that $Res_N^GInd_N^G(S) = \bigoplus_{x \in [G/N]}\,^xS$ is semisimple. Since $|G:N|$ is assumed to be invertible in $k$, we know that $Ind_N^G(S)$ is semisimple. Since $k$ is a splitting field for $G$, the module $Ind_N^G(S)$ is semisimple if ant only if $End_{k[G]}(Ind_N^G(S))$ has $k$-dimension 1. Using the forbenius reciprocity, we have $$End_{k[G]}(Ind_N^G(S)) = Hom_{k[G]}(Ind_N^G(S),Ind_N^G(S)) \simeq Hom_{k[N]}(S, Res_N^GInd_N^G(S)) = \bigoplus_{x \in [G/N]}Hom_{k[N]}(S,\,^xS)$$. Then by [[Schur's lemma]], the right side is 1-dimensional if and only if $S\, \not\simeq \,^xS$ for all $x \in G \backslash N$. 

# Relative traces
As seen in the earlier course in [[representation note]], the character of representations are very useful. We hope the extend it to the more general case of module representations. 

**Definition**: 
Let $G$ be a group and $U$ a $k[G]$-module. Let $H$ be a su