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

The *representation* of a lie algebra $\mathfrak{g}$ on a vector space $V$ is simply a map $\rho: \mathfrak{g}\rightarrow \mathfrak{gl}(V)=End(V)$. In order to satisfy the differential form, we define the tensor product to be $X(v \otimes w) = X(v) \otimes w + v \otimes X(w)$. 

For further classification. The *ideal* of a lie algebra $\mathfrak{h} \subseteq \mathfrak{g}$ is a subalgebra with $[\mathfrak{h},\mathfrak{g}] \subseteq \mathfrak{h}$ (one can proof that $H \triangleleft G$ if and only if the corresponding $\mathfrak{h}$ is an ideal of $\mathfrak{g}$). And say $\mathfrak{g}$ is *simple* if it has no nontrivial ideals and $dim\mathfrak{g}>1$

we also define the *lower central series* $\mathfrak{D}_{1}\mathfrak{g} = [\mathfrak{g},\mathfrak{g}]$, $\mathfrak{D}_{k}=[\mathfrak{g},\mathfrak{D}_{k-1}\mathfrak{g}]$. As well as the *drived series* $\mathfrak{D}^{1}\mathfrak{g}=[\mathfrak{g},\mathfrak{g}]$, $\mathfrak{D}^{k}=[\mathfrak{D}^{k-1} \mathfrak{g}, \mathfrak{D}^{k-1} \mathfrak{g}]$.  
1. We then say $\mathfrak{g}$ is *nilpotent* if $\mathfrak{D}_{k} \mathfrak{g} =0$ for some $k$ 
2. And is *solvable* if $\mathfrak{D}^{k} \mathfrak{g}=0$ for some $k$. 
3. It is *perfact* if $\mathfrak{D} \mathfrak{g} = \mathfrak{g}$.
4. It is *semisimple*l if $\mathfrak{g}$ has no nonzero solvable ideals.

One can check the definition of solvable coinside with the usual definition of having a sequence $\mathfrak{g} = \mathfrak{g}_{0} \supset \mathfrak{g}_{1} \supset \cdots \supset \mathfrak{g}=0$ such that $\mathfrak{g}_{i}$ is ideal and $\mathfrak{g}_{i} / \mathfrak{g}_{i+1}$ is abelian. Similar to regular algerbas, we can define the radical of $\mathfrak{g}$, simply by letting it denote the maximal solvable ideal of $\mathfrak{g}$. 

In classification of lie algebra, one first build the faithful representation of the center, and building it up setp by setp to the rardical. Then one ues a splitting to get from the faithful representation of the radical to some representation on all of $\mathfrak{g}$. 

**Engel's Theorem**: Let $\mathfrak{g} \subset \mathfrak{gl}(V)$ be a lie subalgebra, and every $X \in \mathfrak{g}$ is a nilpotent endomorphism of $V$. Then is a nonzero $v \in V$ such that $X(v)=0$ for all $X \in V$. 

*sketch of the proof*: We first find the maximal proper subalgebra $\mathfrak{h}$, split the problem into two part $\mathfrak{h}$ and $\mathfrak{g} / \mathfrak{h}$ (to see why $h$ is ideal, one consider the adjoint action $ad(\mathfrak{h})$ which preserver $\mathfrak{h}$ and hence act on $\mathfrak{g} / \mathfrak{h}$), unsing indeuction we can find a $\overline{Y} \in \mathfrak{g} / \mathfrak{h}$ such that killed by $ad(X)$ for all $X \in \mathfrak{h}$. Take $Y$ be an element in $\mathfrak{g}$ such that $[\mathfrak{h},Y] \in \mathfrak{h}$. Noticing that $\mathfrak{h}$ is maximal, the subalgebra $\langle \mathfrak{h},Y \rangle$ must be $\mathfrak{g}$ itself. Now, using indeuction, we are able to take a nonzero $v\in V$ with $X(v)=0$ for all $X \in \mathfrak{h}$. So $W:=\{ v \in V : X(v)=0, \forall X \in \mathfrak{h} \}$ is none empty, taking the $Y$ above, we only need to proof that there is a $v\in W$ with $Y(v)=0$. Note that $X(Y(w))= Y(X(w)) + [X,Y](w)$, the two terms on the left are clearly 0, so we have $Y(w) \in W$. Since $Y$ is nilpotent, we are able to find the desirable $v$. 

In fact, the theorem tells us that we can also write nilpotent lie algebra into the form of upper triangle matraces.

**lie's theorem**: Let $\mathfrak{g} \in \mathfrak{gl}(V)$ be a solvable lie algebra. Then there exists a nonzero vector $v \in V$ that is an eigenvector of all $X \in \mathfrak{g}$. (This implies we can always write it in the form of upper triangle matraces)

The persedure is similar, we still use the induction, hoping to find an ideal with codimension 1. Different from the privious theorem, this time we consider $\mathfrak{g} / \mathfrak{Dg}$, which by assumption, is a nonzero abelian lie algebra. So we are able to find a ideal for it with codimension 1, hence the ideal assoicate to it in $\mathfrak{g}$ has codimension 1 as well. Now assume $\mathfrak{h}$ and $Y \in \mathfrak{g}$ spanned $\mathfrak{g}$. Using the indeuction hypothies, we are able to find a eigenvector $v_{0}$, let $\lambda:\mathfrak{h}\rightarrow V$ be a linear map such that $\lambda(X)\cdot v = X(v)$ for $\mathfrak{h}$. Take $W:=\{ w \in V: \lambda(X)\cdot w = X(w), \forall X \in \mathfrak{h} \}$, we hope to proof that $Y(W) \in W$. Evidently, we use $X(Y(w)) = Y(X(w)) + [X,Y](w) = \lambda(X)Y(w)+\lambda([X,Y])(w)$, but the second term no always be 0, indeed, $Y(W)$ lies in $W$ if and only if $\lambda([X,Y])=0$ for all $X \in \mathfrak{h}$. To solve this problem, we introduce another vector space $U$ spanned by $w,Y(w),Y^{2}(w),\cdots$. Since $X(Y^{k}(w))=Y(X(Y^{k-1}(w)))+ [X,Y](Y^{k-1}(w))$, we have $X$ sending $U$ into $U$ (using induction over $k$). Consider the matrix of the action $[X,Y]$, on immediately notice that the values on the diagnal are all $\chi(w)$, taking the trace, we have $Tr([X,Y]|_{U})=k\cdot\chi([X,Y])$ where $k$ is the dimension of $U$. Note that the trace of the commutator is always 0, hence $\chi([X,Y])$ is 0. (This also tells us that the proof will fail if we are working on a field with character greater than 0).

Using lie's theorem, we get the following property for complex lie algebra: Take $\mathfrak{g}_{ss}=\mathfrak{g} / Rad(\mathfrak{g})$. Then every irreducible representation of $\mathfrak{g}$ is of the form $V=V_{0} \otimes L$, where $V$ is an irreducible representation of $\mathfrak{g}_{ss}$ and $L$ a one dimensional representation. 

One might already notice that may theorem and property in representation of finite group is no longer valid in lie groups (for example the complete reducibility) . Another important different is that the openator is not always diagnalizable for representations. It might also be diagnalizable for some and none diagnalizable for others. 

But if we restrict our attention to those semisimple lie algebras, then every thing is well behaved again. 

**Theorem**: Let $\mathfrak{g}$ be a semisimple lie algebra, and $V$ a representation. If $W \subset V$ be a invariant subspace, there is a compelition of $W'$ of $W$ that is invariant as well. (proof of this can be found in [[Block theory ch1]] for general groups). 

As the the diagnalizable problem. One may hope the Jordan decomposition (i.e. every endomorphism $X$ can be uniquely written in the form $X=X_{s}+X_{t}$ where $X_{s}$ diagnalizable and $X_{t}$ nilpotent). Sadly this is not true either. But in the case of semisimple lie algebra, it is true in some way:

**Theorem**: Let $\mathfrak{g}$ be semisimple complex lie algebra. For any element $X \in \mathfrak{g}$, there is $X_{s}$ and $X_{t} \in \mathfrak{g}$, such that $\rho(X_{s}) = \rho(X)_{s}$ and $\rho(X_{t})= \rho(X)_{t}$, where $\rho(X)_{s}$ and $\rho(X)_{t}$ is the corresponding parts in the jordan decomposition of $\rho(X)$.   

>[!note] The unitary trick
>By assoicating the lie algebra we want to study to a representation of a compact lie group and working with that. 

This is the two main rutine in proving problems of lie algebras. The other is algebarically, using the property of lie algebra only. Written is formal language, the case would be a complex lie algebra $\mathfrak{g}$ is more or less the same as $\mathfrak{g}_{0} \otimes \mathbb{C}$ for some real lie algbra, hence a complex lie algbra is assoicate to a compact real lie group.