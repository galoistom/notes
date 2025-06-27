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
Take a exact sequence of $k[G]$ $U \stackrel{\phi}{\longrightarrow} V \stackrel{\}$ 