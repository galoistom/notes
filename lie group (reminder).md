lie group is a manifold with a group structure (one need the operation $g$ has to be differential, of course). 
Some easy examples would be $GL(V)$, $SL(V)$ the group of element with $\det=1$, $SO(V)$ the goup of element keeps orthognality as well, etc. 

Unfortunately, general lie group is vary hard to study. People then notice that the neiberhood of $1_{G}$ genertate $G$ (if $G$ is connected of course), so we can know many information of $G$ by studying the tangent space of $G$ at $1_{G}$ which we call *lie algebra* (though it is wrong to say that lie algebra determines lie group). 

>[!note] First Principle
> Let $G$ and $H$ be lie groups, $G$ connected. A map $\rho :G\rightarrow H$ is uniquely determined by its differential $d\rho_{e}:T_{e}G \rightarrow T_{e}H$.  

As we know, the key of group is the morphism $m_{g}:G \rightarrow G$ sending $x \mapsto gx$. The problem is, $m_{g}$ does not fix any point, so it is hard to assoicate it to the tangent space. To solve this problem, people consider the inner automorphism $\Psi_{g} \in Aut(G)$ with $x \mapsto gxg^{-1}$. Thus by taking differential, we get $Ad(g):=(d\Psi_{g})_{e}$, but this still need the information of lie group to compute, so we go another step further the compute the differential of $Ad$, getting $ad(g):=(d(Ad(g)))_{e}:T_{e}G \rightarrow End(T_{e}(G))$.

Now let $X,Y$ be two vectors tangent to $G$ at $e$. Define the lie bracket $[X,Y]:=ad(X)(Y)$. Easy computation shows that in words of linear transformation (embeding it into a $GL(V)$), $[X,Y]=XY-YX$. The reason why not define the lie bracket in the first place is clear now, as we do not have a multiplication for $X$ and $Y$. 

One might notice that $[X,[Y,Z]]+[Y,[Z,X]]+[Z,[X,Y]]=0$, together with the skew-symmetric property, we now have all the property a lie bracket need to have.

Now a lie algebra is a vector space with a skew-symmetric bileaner map $[\ ,\ ]:\mathfrak{g} \times \mathfrak{g} \rightarrow \mathfrak{g}$ satisfying $[X,[Y,Z]]+[Y,[Z,X]]+[Z,[X,Y]]=0$. 

>[!note] Second Principle
> Let $G$ and $H$ be lie groups, with $G$ connected and simply connected. A linear map $T_{e}G \rightarrow T_{e}H$ is the differential of a homorphism $\rho:G \rightarrow H$ if and only if it preserves the bracket operation.

The *reprentation* of a lie algebra $\mathfrak{g}$ on a vector space $V$ is simply a map $\rho: \mathfrak{g}\rightarrow \mathfrak{gl}(V)=End(V)$. In order to satisfy the differential form, we define the tensor product to be $X(v \otimes w) = X(v) \otimes w + v \otimes X(w)$. 

For further classification. The *ideal* of a lie algebra $\mathfrak{h} \subseteq \mathfrak{g}$ is a subalgebra with $[\mathfrak{h},\mathfrak{g}] \subseteq \mathfrak{h}$ (one can proof that $H \triangleleft G$ if and only if the corresponding $\mathfrak{h}$ is an ideal of $\mathfrak{g}$). And say $\mathfrak{g}$ is *simple* if it has no nontrivial ideals and $dim\mathfrak{g}>1$

we also define the *lower central series* $\mathfrak{D}_{1}\mathfrak{g} = [\mathfrak{g},\mathfrak{g}]$, $\mathfrak{D}_{k}=[\mathfrak{g},\mathfrak{D}_{k-1}\mathfrak{g}]$. As well as the *drived series* $\mathfrak{D}^{1}\mathfrak{g}=[\mathfrak{g},\mathfrak{g}]$, $\mathfrak{D}^{k}=[\mathfrak{D}^{k-1} \mathfrak{g}, \mathfrak{D}^{k-1} \mathfrak{g}]$.  
1. We then say $\mathfrak{g}$ is *nilpotent* if $\mathfrak{D}_{k} \mathfrak{g} =0$ for some $k$ 
2. And is *solvable* if $\mathfrak{D}^{k} \mathfrak{g}=0$ for some $k$. 
3. It is *perfact* if $\mathfrak{D} \mathfrak{g} = \mathfrak{g}$.
4. It is *semisimple*l if $\mathfrak{g}$ has no nonzero solvable ideals.

One can check the definition of solvable coinside with the usual definition of having a sequence $\mathfrak{g} = \mathfrak{g}_{0} \supset \mathfrak{g}_{1} \supset \cdots \supset \mathfrak{g}=0$ such that $\mathfrak{g}_{i}$ is ideal and $\mathfrak{g}_{i} / \mathfrak{g}_{i+1}$ is abelian. Similar to regular algerbas, we can define the radical of $\mathfrak{g}$, simply by letting it denote the maximal solvable ideal of $\mathfrak{g}$. 