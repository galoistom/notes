We extend the ideal of [[Basic Definitions of representation]] to the modules of group algebra $k[G]$.

# Definitions

> [!note] Definition
> Let $G$ be a group. A representation of $G$ over $k$ is a pair $(V,\rho)$ consisting of a $k-module$ $V$ and a group homomorphism $\rho:G \rightarrow GL(V)$, where $GL(V)=Aut_k(V)$ is the group of $k-linear$ automorphism.

Morphism between two representations are simple, just preserve the module structure and the $G$ action over it.

# Twisted group algebra

We want to construct different multiplication for $k[G]$. Let $\alpha:G \times G \rightarrow k^\times$ be a max, and multiplication be $x \cdot y=\alpha(x,y) xy$, then the multiplication is associative if and only if $\alpha(xy,z)\alpha(x,y)=\alpha(x,yz)\alpha(y,z)$. We extend this definition to general abilian group $Z$, thus we get the definition of the 2-cocycle $Z^2(G;Z)$, i.e. all $\alpha:G \times G \rightarrow Z$ such that, $\alpha(xy,z)\alpha(x,y)=\alpha(x,yz)(^x\alpha(y,z))$. But one might notice that when viewing $k_\alpha[G],k_\beta[G]$ with multiplication $\alpha,\beta$, if there is a scalar $\gamma:G \rightarrow k^\times$ s.t.$\alpha(x,y)=\beta(x,y)\gamma(x)\gamma(y)\gamma(xy)^{-1}$(i.e. there is an isomorphism between $k_\alpha[G] \simeq k_\beta[G]$ by sending $x \mapsto \gamma(x)x$), then there is no much different between the multiplications, and note that $\alpha(x,y)=\gamma(x)(^x\gamma(y))\gamma(xy)^{-1}$ where $\gamma(x)=(^xz)z^{-1}$ for some $z \in Z$ forms a subgroup of $Z^2(G;Z)$, we shall denote it by $B^2(G;Z)$. Now, by lowering the dimension one get $Z^1(G;Z)$, the set of $\gamma:G \rightarrow Z$ such that $\gamma(xy)=\gamma(x)(^x\gamma(y))$, and $B^1(G;Z)$, the set of $\gamma:G \rightarrow Z$ such that there is a $z \in Z$ s.t. $\gamma(x)=(^xz)z^{-1}$. Using quotient, we get the [[Cohomology on groups]] $H^1(G;Z)=Z^1(G;Z)/B^1(G;Z)$ and $H^2(G;Z)=Z^2(G;Z)/B^1(G;Z)$.
**Remark**: Using the above interpretation, one get a natural link between $H^i(G;Z)$ and $Ext_{\mathbb{Z}[G]}^i(\mathbb{Z},Z)$ through the extension of group $G$:

$$
1 \longrightarrow Z \stackrel{l}{\longrightarrow} \widehat{G} \stackrel{\pi}{\longrightarrow} G \longrightarrow 1
$$

where the multiplication $\widehat{x}\cdot\widehat{y}=\alpha(x,y)\widehat{xy}$.

# G-algebras

We already have $G-module$, so it is natural to consider the concept of $G-algebra$. The definition is straightforward: simply giving an algebra $A$ a $G-action$ over it, specifically, the homomorphism between $G \rightarrow A^\times$ is called the *structural homomorphism of the interior G-algebra A*. Moreover, the algebraic morphism $A \rightarrow B$ preserving the $G-action$ is called the homomorphism of $G-algebra$.

# Category algebra

One might now that a group $G$ is a special monoid category. So we extend the idea of group algebra to category algebra, where the morphism between objects take the place of group action. This lead to the quiver algebra, which is the quotient $A=k\mathcal{C}/I$, where $I$ is an ideal of the algebra.

# Center and commutator subspace

It is well known that the center $Z(k[G])$ of the group algebra $k[G]$ is spanned by the conjugacy classes of $G$, i.e. let $\mathcal{K}$ be the set of conjugacy classes of $G$, and for each conjugacy classes $C \subset G$, set $\overline{C}=\sum_{c\in C}c$, then every $z \in Z(k[G])$ can be uniquely expressed by $\sum_{C \in \mathcal{K}}\lambda_C\overline{C}$.

**Theorem**:
Let A,B be k-algebras. Suppose that $A$ and $Z(B)$ are free as k-modules, ans that $Z(B)$ us a direct summand of $B$ as k-module. Then the centralizer of the subalgebra $1 \otimes B$ of $A \otimes_k B$ is $A \otimes_k Z(B)$, and we have $Z(A \otimes_k B)= Z(A) \otimes_k Z(B)$.
*Proof*:
One side of the inclusion is clear, we shall proof the other side. Taking a k-basis $\{a_i\}_{i \in I}$ for $A$, and $\{z_j\}_{j \in J}$ for $Z(B)$. Then the set $\{a_i \otimes 1_B\}_{i \in I},\{1_A \otimes z_j\}_{j \in J}$ are basis for $A \otimes_k B,A \otimes_k Z(B)$ as a $B,A$ module. Thus $z \in A \otimes_k B$ can be written in the from $z=\sum_{i \in I}a_i \otimes b_i$ where $b_i$ are uniquely determined and almost all equal to 0. Now suppose $z$ centralise $1 \otimes_k B$, then we have $\sum_{i \in I}a_i \otimes bb_i=\sum_{i \in I}a_i \otimes b_ib$, using the uniqueness, one gets $b_i \in Z(B)$ for all $i \in I$, so $z \in A \otimes_k Z(B)$. Suppose now that $z \in Z(A \otimes_k B)$, then $z \in A \otimes_k Z(B)$, so $z=\sum_{j \in J}c_j \otimes z_j$ is unique up to $c_j$. Using the same argument above, one proof he theorem.

Using the above theorem, one easily know that $Z(k[G \times H])=Z(k[G]) \otimes Z(k[H])$ if $H \leq G$. But in general, the twisted group algebra does not have the similar properties. In fact, the center $Z(k_{\alpha}[G])$ may not be free as k-module since the multiplicative inverse of a group element $x$ is not necessarily $x^{-1}$. But there is another way to measure how far it is to be commutative is using the commutator space $[A,A]$ which is generated by $ab-ba$, $a,b \in A$. One might notice that $[A,A]$ is a $Z(A)$ module, so $A/[A,A]$ is also a $Z[A]$ module.

**Proposition**:

1. the commutator space $[k[G],k[G]]$ is spanned by $[x,y]=xy-yx,\  x,y \in G$.
2. If $x,x'$ are conjugate, then $x-x' \in [k[G],k[G]]$, in fact, those sets of $[x,x']$ span the space $[k[G],k[G]]$.
3. We have an isomorphism of k-module $k[G]/[k[G],k[G]] \simeq Z(k[G])^*$, sending $x+[k[G],k[G]] \mapsto \sigma$ where $\sigma \in Z(k[G])^*$ is the maps that sent the conjugacy class sum of $x^{-1}$ to 1, and other classes to 0.
4. We have an isomorphism of k-module $(k[G]/[k[G],k[G]])^* \simeq Z(k[G])$, sending $\phi \in (k[G]/[k[G],k[G]])^*$ to $\sum_{g \in G} \phi(g^{-1})g$.
5. Let $A,B$ be k-algebras. We have $[A \otimes_k B,A \otimes_k B]=A \otimes [B,B]+[A,A] \otimes B$.

We extend the commutator operator to modules: Let $A$ be a k-algebra, and $M$ an $A-A$ bimodule. We set $M^A=\{m \in M | am=ma, \forall a \in A\}$ and denote by $[A,M]$ be k-submodule of $M$ generated by $am-ma$.
*Remark*: note that $End_k(U)$ is also an $A-A$ bimodule for an A-module $U$, and $End_k(U)^A=End_A(U)$.

# The Hopf algebra structure of group algebra

The main idea here is that we want to generalize the group algebra, but close enough to preserve many properties.

**Definition**:
Let $G$ be a group. The argumentation homomorphism of $k[G]$ is the unique k-algebra homomorphism $\epsilon:k[G] \rightarrow k$ sending every element of $G$ to $1_K$. Set $I(k[G])=ker(\epsilon)= \{\sum_{g \in G} \lambda_g g: \sum_{g \in G} \lambda_g=0\}$.

**Proposition**:
LEt $G,H$ be finite groups. Let $\phi:G \rightarrow H$ be a group homomorphism an let $\alpha:k[G] \rightarrow k[H]$ be the induced algebra homomorphism. Set $N=ker(\alpha)$, then we have $ker(\alpha)=k[G] \cdot I(k[G])=I(k[N])k[G]$.

Recall that for any k-algebra $A$, there is a natural map $\mu:A \otimes_k A \rightarrow A$, such that $\mu(a \otimes b)=ab$. $\mu$ is naturaly a morphism as $A-A$ bimodule, but not as algebra in general. However, in the case of group algebra, there is always a *comultiplication* map $\Delta:k[G] \rightarrow k[G] \otimes_k k[G] \simeq k[G \times G]$ induced from $\Delta:G \rightarrow G \times G$, sending $g \mapsto (g,g)$.

Another property is that there is an *antipode* $l:k[G] \simeq k[G]^{op}$ sending $g \rightarrow g^{-1}$, and one also have $l \circ l =id_{k[G]}$. Moreover, a *unit* map $\eta:k \rightarrow k[G]$ sending $1_k \mapsto 1$.

Then we have the following **theorem**:

1. $\mu \circ (id \otimes eta)=id=\mu \circ (\eta \otimes id)$.
2. $\mu \circ (\mu \otimes id)=\mu \circ (if \otimes \mu):k[G] \otimes_k k[G] \otimes_k k[G] \rightarrow k[G]$.
3. $(id \otimes \epsilon) \circ \delta = id = (\epsilon \otimes id) \circ \Delta$.
4. $(\Delta \otimes id) \circ \Delta = (id \otimes \Delta) \circ \Delta: k[G] \rightarrow k[G] \otimes_k k[G] \otimes_k k[G]$.
5. $\mu \circ (id \otimes l) \circ \Delta=\eta \circ \epsilon=\mu \circ (l \otimes id) \circ \Delta:k[G] \rightarrow k[G]$.

The algebra satisfying the above theorem are called *Hopf algebra*. the second equation is the associativity of $\mu$, the third and the forth correspond to $A$ being a *coalgebra* with the last one being the *coassociativity*. The antipode ensures that the category of left and right modules are the equivalent. The comultiplication meusres that a tensor product over $k$ of two A-module is again a A-module.

We want some how extend these maps to the twisted group algebra, then we get that the map sending $g \mapsto \alpha(g,g^{-1})g^{-1}$ where $g \in G$ induced an isomorphism $(k_\alpha[G])^{op} \simeq k_{\alpha^{-1}}G$, and that if $\gamma=\alpha\beta$ then there is a natural injective k-algebra homomorphism $k_\gamma[G] \rightarrow k_\alpha[G] \otimes_k k_\beta[G]$, and $k_\gamma[G]$ is a direct summand of $k_\alpha[G] \otimes_k k_\beta[G]$ as a $k_\gamma[G]-k_\gamma[G]$ bimodule.

# Blocks and idempotent

Given two k-algebra $B,C$, set the carstesian product $B \times C$ with the componentwise sum ans multiplication, together with the canonical projections onto $B$ ans $C$, is the direct product of $B,C$ in the category of k-algebra. Let $A$ be an k-algebra, a subalgebra $B$ is a direct factor if there is a split surjective $A-A$ bimodule homomorphism $\tau:A \rightarrow B$.

Let $A$ be a k-algebra, and $b \in Z(A)$ be an idempotent, then $Ab:=\{ab:a \in A\}$ is a k-algebra with unit $b$. one  immediately know that $A(1-b)$ is also a k-algebra, and that $A=Ab \times A(1-b)$ as k-algebra. The following theorem bridge the connection between the two concept above.

**Theorem**:
Let $A$ be a k-algebra, $B$ a k-submodule of $A$, then the following are equivalent:

1. $B$ is a direct summand of $A$ as an $A-A$ bimodule.
2. B is a direct factor of A as a k-algebra.
3. B=Ab for sum idempotent b in Z(A).
   *Proof*:
   Suppose (1) holds, let $A=B \oplus N$ as an A-A-bimodule. Notice that $BN \subset B \cap N \{0\}$, and write $1_A=b+n$, then $b=b \cdot 1_A=b^2+bn=b^2$ so $b$ is an idempotent, the same argument shows that $n$ is idempotent, so they are orthogonal. Write $a=c+r$ for some $c \in B,r \in N$, and $a=ab+an=ba+na$, so $b,n \in Z(A)$, and $B=Ab,N=An$.
   Suppose (2) holds, let $A=B \times C$, then $1_A=(1_B,0)+(0,1_C)$ and $(1_B,0),(0,1_C)$ are orthogonal idempotent in $Z(A)$. Setting $b=(1_B,0)$, then $B=Ab$.
   Suppose (3) holds, let $B=Ab$, and $C=A(1-b)$, then $A=B \oplus C$ as A-A-bimodule, and $A=B \times C$ as k-algebra.

**Definition**:
Let $A$ be a k-algebra. A *block* of $A$ is a primitive idempotent $b$ in $Z(A)$; the algebra $Ab$ is called a *block algebra* of $A$.

**Theorem**:
Suppose that k is noetherian. Let $A$ be a k-algebra such that $Z(A)$ is finitly generated as a k-module. Then $Z(A)$ is noetherian, and the following hold.

1. The set of Blocks $\mathcal{B}$ of $A$ is the unique primitive decomposition of $1_A$ in $Z(A)$. In particular, $\mathcal{B}$ is finite, and they are pairwise orthogonal blocks of $A$.
2. $A=\prod_{b \in \mathcal{B}} Ab$ is the uniuqe decomposition of $A$ as a direct product of indecomposable k-algebras.
3. $A=\oplus_{b \in \mathcal{B}}Ab$ is the unique decomposition of $A$ as direct sum of indecomposable A-A-bimodule.
   *Proof*:
   Since $k$ is noetherian and $Z(A)$ is finitly generated as k-module, so $Z(A)$ is noetherian. Let $b \in \mathcal{B}$, and $c \in Z(A)$ is another primitive idempotent such that $bc \neq 0$. Then one have $b=bc+b(1-c)$, where $bc,b(1-c)$ are idempotent in $Z(A)$ but $b$ is primitive, so one must have $b(1-c)=0,b=bc$, the same agrument shows that $c=cb=bc=b$. The rest it then clear.

In view of abilian category, there is no much difference between direct product and direct sum, and coproduct coincides with tensor product. That's why the decomposition of $A$ to its block yealds a direct sum and a direct product.

**Definition**:
Let $A$ be a k-algebra and $b$ be a block. We say that an A-module $M$ belongs to the block $b$ if $M=bM$.

**Proposition**:
Suppose that k is noetherian. Let $A$ be a k-algebra such that $A$ is finitl generated as a k-module, let $\mathcal{B}$ be the set of blocks of $A$.

1. for any A-module $M$ we have $M=\oplus_{b \in \mathcal{B}}\,bM$.
2. for any indecomposable A-module $M$ there is a unique block $b$ if $A$ such that $M=bM$.
3. for any two A-module belonging to two different blocks $b,c$. We have $Hom_A(M,N)=\{0\}$.

Using this proposition, we can study the category $Mod(A)$ by studying the category $Mod(Ab)$ where $b$ runs through the set of blocks of $A$.

# Composition series and Grothendieck groups

c.f.[[Grothendieck group]]

**Definition**:Let $A$ be a k-algebra. A *composition series* of A-module $M$ is a finite chain $M= M_0 \supset_1 M_1 \supset \cdots \supset M_n=\{0\}$ of submodules $M_i$ in $M$ such that $M_{i+1}$ is a maximal submodules, the module $M_i/M_{i+1}$ be the composition factors, and $n$ is the length of the series. Two composition series of A-modules $M$ and $M'$ are called *equivalent* if they have the same length $n$ and if there is a bijection between the sets of composition factors of each of these series such that corresponding composition factors are isomorphic.

**Theorem**(Hordan-Holder):
Let $A$ be a k-algebra, and let $M$ be an A-module. Then $M$ has a comspostion series if and only if $M$ is both Artinian and noetherian. In the case, any composition series of $M$ are equivalent.
*Proof*:
Using induction, one get that $M$ is noetherian and artinian. Take two decomposition series $M=M_0 \supset M_1 \supset \cdots \supset M_n=\{0\}$ and $M=N_0 \supset N_1 \supset \cdots \supset N_k=\{0\}$, and suppose that $n >1$. Set $N=N_1$, consider

$$
M=M_0+N \supset M_1+N \supset \cdots \supset M_n+N=N=M_0 \cap N \supset M_1 \cap N \supset \cdots \supset M_n \cap N=\{0\}
$$

Since $N$ is maximal, we know that there is a $i$ such that $M=M_i+N \supset M_{i+1}+N=N$, then we have $M/N \simeq (M_i+N)/(M_{i+1}+N) \simeq M_i/M_{i+1}$, and using induction, one get that $N_j/N_{j+1} \simeq (M_k \cap N)/(M_{k+1} \cap N) \simeq M_k/M_{k+1}$.

**Proposition**:
Let $U$ be a submodule of $M$, then there is a composition series with $U=M_i$.

**Definition**:
Let $A$ be a k-algebra. The *Grothendieck group* of $A$ is the abelian group denoted $R(A)$ which is generated by the set pf isomorphism classes of finitly generated A-modules $U$, subject to the relation $[U]+[V]=[W]$ whenever there is a [[Short exact sequence]] for A-modules of the form $0 \longrightarrow U \longrightarrow V \longrightarrow W \longrightarrow 0$. We denote by $[U]$ the image of $U$ in $R(A)$.
For a finite-dimensional algebra over a field has a particular simple structure: $[U]=\sum_{S}d(U,S)[S]$ where $S$ runs over a set of representatives of isomorphism classes of simple A-module and $d(U,S)$ is the number of $S$ in the composition factors of $U$.

# Semisimple modules

**Definition**:
Let $A$ be a k-algebra. An A-module $M$ is called *semisimple* if $M$ is the sum of its simple submoduels.

**Theorem**([[Schur's lemma]]):
Let $A$ be a k-algebra. For any simple A-module $S$ the k-algebra $End_A(S)$ is a division algebra. For any two nonisomorphic simple A-module S,T we have $Hom_A(S,T)=\{0\}$.
*proof*:
Let $S,T$ be simple A-modules, and suppose there is a nonzero A-homomorphism $\phi:S \rightarrow T$. Then $ker(\phi) \neq S$, hence $ker(\phi)=\{0\}$ because $S$ is simple. Thus $\phi$ is injective. In particular, $im(\phi) \neq \{0\}$. Since $T$ is simple this implies $im(\phi)=T$. Thus $\phi$ is an isomorphism. The result follows.
*Remark*:
This lemma leads to the following corollary: If $k$ is algebraically closed, and $A$ a k-algebra, then for a simple A-module $S$ of finite dimension over k, one has that $End_A(S)= \{\lambda id_S:\lambda \in K\}$.

**Theorem**:
Let $A$ be a k-algebra and let $M$ be an A-module. If $M$ is semisimple, so every quotient and every submoduel of $M$. Moreover, the following are equivalent:

1. $M$ is semisimple.
2. $M$ is a direct sum of simple modules.
3. Every submoduel $U$ has a compliment.
   *Proof*: not difficult (will use zorn's lemma).

**Theorem**(Clifford):
Let $G$ be a finite group, let $N$ be a  normal subgroup of $G$ and suppose that k is a field. For any simple $k[G]$ module $S$, the restriction $Res_{N}^G(S)$ to $k[N]$ is a semisimple $k[N]$ module. Moreover, if $T,T'$ are simple $k[N]$-submodules of $Res_N^G(S)$ then there is an element $x \in G$ such that $T' \simeq xT$. In other words, the isomorphism classes of simple $k[N]$-submodules of $Res_N^G(S)$ are permuted transitively by the action of $G$.
*Proof*:
Let $T$ be a simple $k[N]$-submodules of $S$. Then using $nxT=x(x^{-1}nx)T \subseteq xT$, we know that $xT$ is also a submoduels of $S$ in $k[G]$. Then the sum of $xT$ is a $k[G]$-submodules of $S$, hence it is $S$ itself.
*Remark*:
This is just saying that every $S$ can be written in the from of $Ind_N^G(T)$ for some simple $k[N]$-module $T$.

# The Jacobson radical

**Definition**: The *Jacobson radical* $J(A)$ of a k-algebra $A$ is the intersection of the annihilators of all simple left A-modules. More explicitly, $J(A)$ is equal to the set of all $a \in A$ satisfying $aS=\{0\}$ for every simple A-module $S$.
*Remark*: This is more or less the elements that we cannot study if we only pay attention on modules of algebra.

**Theorem**(Nakayama's lemma):
Let $A$ be a k-algebra. Let $M$ be a finitly generated A-module. If $N$ is a submoduel of $M$ such that $M=N+J(A)M$, then $M=N$. In particular, if $J(A)M=M$, then $M=\{0\}$.
*Proof*:
Note that there is always a maximal submodule of $M$ containing $V$, and notice that $J(A)M/V=0$ so one have $J(A)M \subseteq V$ hence $M \subseteq V$, so $N=M$.

**Definition**:
an ideal $I$ of $A$ is called *nilpotent* if there is a positive integer $n$ such that $I^n:=\{\prod_{i=1}^na_i:a_i \in I\}$ is $\{0\}$.

**Theorem**:
Let $A$ be a k-algebra

1. the set $1+J(A)$ is subgroup of $A^\times$.
2. the radical $J(A)$ contains every nilpotent in $A$.
3. the radical $J(A)$ contains no idempotent.
4. for any ring automorphism $\alpha$ of $A$, we have $\alpha(J(A))=J(A)$. In particular, if a group $G$ acts on $A$ by a ring automorphism, then $J(A)$ is a $G$-set.
   *Proof*:
   Let $a \in J(A)$, then consider $A=Aa+A(1-a)=J(A)+A(1-a)$, using the nakayama's lemma, one get $A=A(1-a)$, so $1-a$ has a inverse $1-b$ where $b=ba-a \in J(A)$, so we have (1). To proof (2), consider $IS$ for some simple module $S$ of $A$, which must be either $\{0\}$ of $S$, but the letter is impossible, because $I^nS=\{0\}$. (3) is obvious. (4) is just consider the module $_\alpha S$ on which $a \in A$ acts as $\alpha(a)$, then one immediately know that the map sending $S\, \mapsto \,_\alpha S$ is a one to one map, so one get that $J(A)$ is invariant under $\alpha$.

**Theorem**
Let $A$ be a k-algebra. The *radical* $J(A)$ is equal to any of the following:

1. the intersection of the annihilators of all right simple A-modules;
2. the intersection of all maximal left ideals in $A$;
3. the intersection of all maximal right ideal in $A$.
   *Proof*:
   Clearly, $J(A) \subseteq \cap_M M$ where $M$ go throught the maximal ideal of $A$. Let $S$ be a simple A-module, then the map $A \rightarrow S$ sending $a \mapsto as$ for a fixed $s \in S$ is surjective with kernel $M_s$ the annihilator of $s$, then $I_S$ the intersection of $M_s$ is the annihilator of $S$ in $A$, in particular, $I_S$ is intersection of all maximal ideal of $A$ containing $S$. Thus $J(A)$, the intersection of all $I_S$ it the intersection of all maximal ideal.

**Theorem**:
Let $A$ be a k-algebra, and $I \subseteq J(A)$ is an ideal of $A$. Then we have the following [[Short exact sequence]]:

$$
1 \longrightarrow 1+I \longrightarrow A^{\times} \longrightarrow (A/I)^\times \longrightarrow 1.
$$

**Theorem**:
Suppose that $k$ is a field. Let $A$ be a finite-dimensional k-algebra. Then $J(A)$ is the unique maximal nilpotent ideal in $A$. For any subalgebra $B$ of $A$ we have $J(A) \cap B \subseteq J(B)$, and we have $J(Z(A))=J(A) \cap Z(A)$.
*Proof*:
We know that $J(A)$ contains every nilpotent in $A$, so all we have to check is that $J(A)$ is nilpotent itself, which is easy by considering $J(A) \supseteq J(A)^2 \supseteq \cdots$, and using the fact that $A$ is finite-dimensional, we know there is $J(A)^n=J(A)^{n+1}$ for some $n$, so $J(A)$ is nilpotent. Moreover, we have $J(A) \cap B$ is a nilpotent ideal of $B$, hance contained in $J(B)$. We also note that $AJ(Z(A))=J(Z(A))A$ is also a nilpotent ideal in $A$, so $J(Z(A)) = Z(A) \cap J(A)$.
(*Remark*: then inclusion $J(A) \cap B \subset J(B)$ holds in a more general case: if $A \otimes_B T$ is nonzero for all simple modules $T$ of $B$, then $J(A) \cap B \subseteq J(B)$.)

**Theorem**:
Let $A$ be a k-algebra and let $I$ be an ideal in $A$. We have $(J(A)+I)/I \subseteq J(A/I)$.
**Theorem**:
Let $A$ and $B$ be k-algebras. Suppose that $A$ and $B$ are finitly generated as k-modules. We have $J(A) \otimes B+A \otimes J(B) \subseteq J(A \otimes_k B)$.

**Theorem**:
Let $A$ be a k-algebra and let $e$ be an idempotent in $A$.

1. For any simple A-module $S$ either $eS=\{0\}$ or $eS$ is a simple $eAe$-module.
2. For any simple $eAe$-module $T$ there is a simple A-module $S$ such that $eS \simeq T$.
   *Proof:*
   Suppose that $eS \neq \{0\}$, then we take a nonzero $eAe$ submodule $V$ of $eS$. Then $S=AV=AeV$, so $eS=eAeV$ is a simple module of $eAe$.
   Let's consider $A \otimes_{eAe} T=Ae \otimes_{eAe} T$, which is a nonzero $eAe$ module, so there is a maximal submodule $M$. Let $S:=A \otimes_{eAe} T/M$ be a simple A-module, then we get  a surjective map $\pi:A \otimes_{eAe} T \rightarrow S$,  which leads to a map $T \rightarrow eS$, we need to check that the map is not 0, which is easy, noticing that $e \otimes T$ generated $A \otimes T$.
   *Remark*:
   the two proof is silimiar to the concept of $Res$ and $Ind$, the most important thing is that $A=Ae$ as $eAe$-module. And $M$ is chosen to help as get a simple A-module $S$ such that $\pi$ does not act as 0 when restriced to $T$. one may also proof that $M$ is unique, in fact, the is the biggest submodule with $eM=\{0\}$. As in the induced representation, we can get the same $S$ using $Hom_{eAe}(A,T)$.

**Theorem**:
Let $A$ be an artinian algebra, $M$ be a finitly generated A-module, and $J$ a proper ideal of $A$.

1. $M$ is semisimple if and only if $J(A)M=\{0\}$.
2. $J(A)M$ is the intersection of all maximal submodules of $M$.
   *Proof*:
   One direction is obvious, now assume that $J(A)M=\{0\}$,  recall that $J(A)$ is the intersection of all maximal of $A$, and note that $A$ is artinian, so $J(A)= \bigcap_iI_i$, then consider the surjective map $A \rightarrow \bigoplus_iA/I_i$, the kernel is $J(A)$ and the left hand side is semisimple,  so $A/J(A)$ is semisimple too. Using the fact that $M$ is finitly generated, it is the quotient of $A^n$, in fact, because $J(A)M=\{0\}$, one know that it is actually the quotient of $(A/J(A))^n$, whence it is semisimple.
   We first notice $J(A)M \subseteq N$ for all maximal submodule $N$, so we only need to consider the case of $J(A)M=\{0\}$, in which we only need to check that $\bigcap_iN_i=\{0\}$. This is simple, using the fact that $M$ is semisimple, then every $M/N_i\simeq S_i$ for some simple A-module $S_i$, and the intersection is obviously $\{0\}$.

**Definition**:
Let $A$ be a k-algebra and $M$ an A-module, then the *socle* of $M$ $soc(M):=\sum_{\text{simple }N \subseteq M}N$ and $rad(M):=\bigcap_{\text{max } N \subseteq M} N$ the radical of $M$. Moreover $rad^{n+1}(M)=rad(rad^n(M))$, $soc^{n+1}(M)=soc(soc^n(M))$.

**Theorem**:
Let $A$ be a finite-dimensional k-algebra and $M$ a finitly generated A-module.

1. $rad^n(M)=J^n(A)M$ for any $n \geq 0$.
2. $soc^n(M)=\{m \in M:J^n(A)M=0\}$ for any $n \geq 0$.
3. Let $s=inf_n\{rac^n(M)=0\}$ and $t=sup_n\{soc^n(M)=M\}$, then $s=t$ and for $0 \leq i \leq s$ we have $rad^i(M) \subseteq soc^{t-i}(M)$.
   *Proof*:
   Using the theorem above.

**Definition**:
Let $s$ mentioned above be a *Lovewy length* of $M$, denoted by $ll(M)$, and $rad^i(M)/rad^{i+1}(M)$ be the *Lovewy layers* of $M$.

# Jacobson radical of finite group algebra

**Theorem**:
Let $k$ be a field of character $p$, and $P$ a finite $p$-group, then we have $I(k[P])^{|P|}=\{0\}$, in particular $I(k[P])=J(k[P])$.
*Proof*:
Note that $k[P]/I(k[P]) \simeq k$ is one-dimensional, so $I(k[P])$ is maximal, and $P$ acts on it as identiy, so we only need to proof $I(k[P])^{|P|}=\{0\}$. Using induction, we may assume that $Z:=Z(P)$ is nontrivial, and that $I(k[P/Z])^{|P/Z|}=\{0\}$. So what we only need to proof that $(I(k[Z])k[P])^p=\{0\}$ as $I(k[Z])k[P]$ is the ker of $k[P] \rightarrow k[P/Z]$. Since $(z-1)^p=z^p-1=0$ for $z \in Z$, and $I(k[Z])k[P]=k[P]I(k[P])$, $I(k[Z])=(z-1)k[Z]$, the equation is obvious.

**Theorem**:
Let $k$ be a field and $H \leq G$ be two groups such that $[G:H]$ is invertable in $k$. Let $M$ be a $k[G]$-module whose restriction to $k[H]$ is semisimple, then $M$ is semisimple as $k[G]$-module.
*Proof*:
Let $U$ be a submodule of $M$, we want to show that there is a compliment of $U$ in $M$. Take $V$ be the compliment of $U$ in $M$ as a $k[H]$-module, and a map $M \rightarrow U$ with kernel $V$, then set $\tau:M \rightarrow M$ sending $\tau(m)=\frac{1}{[G:H]} \sum_{x \in G/H} x\pi(x^{-1}m)$, then we have $\tau(u)=u$ for $u \in U$ and $\tau(M) \subseteq U$. One immediately check that $\tau$ independent of the choice of $x$ and invariant under $G$.

**Theorem**(maschke's theorem):
Let $k$ be a field, $G$ be a finite field. If $|G|$ is invertable in $k$, then $J(k[G])=\{0\}$, hence every $k[G]$ module is semisimple. If not, then $z= \sum_{g \in G} g \in J(k[G])$.(c.f.[[representation note]])
*Proof*:
Recall that $J(k[N])k[G]=k[G]J(k[N]) \subseteq J(k[G])$ which takes equality when $[G:N]$ is invertable. So the first part is done(taking $N=\{1\}$). Taking $z:=\sum_{g \in G} J(k[G])$, one check that $z^2=|G|z=0$ and $zk[G]=k[G]z$, hence $z \in J(k[G])$.

# [[Projective module and injective module]]

**Definition**:
Let $A$ be a k-algebra, an A-module $P$ is projective if there is a module $P'$ such that $P \oplus P'$ is a free A-module.
**Examples**:
Let $A$ be a k-algebra and let $i$ be an idempotent in $A$. Then the left module $Ai$ is projective (note that $A=Ai \oplus A(1-i)$).

**Theorem**:
Let $A$ be a k-algebra, and let $P$ be an A-module. The following are equivalent:

1. The A-module $P$ is projective.
2. Any surjective A-homomorphism $\pi:U \rightarrow P$ for some A-module $U$ to $P$ splits, i.e. there is a $\sigma:P \rightarrow U$ s.t. $\pi \circ \sigma =id_P$.
3. For any surjective A-homomorphism $\pi:U \rightarrow V$ and any A-homomorphism $\psi:P \rightarrow V$ there is an A-homomorphism $\phi:P \rightarrow U$ such that $\pi \circ \phi=\psi$.
4. The fuctor $Hom_A(P,_): Mod_A \rightarrow Mod_k$ is exact.

**Theorem**:
Let $A$ be a k-algebra, let $M$ be an A-module and let

```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
&0 \arrow[r] &U \arrow[r] &P \arrow[r,"\pi"] &M \arrow[r] &0\\
&0 \arrow[r] &V \arrow[r] &Q \arrow[r,"\tau"] &M \arrow[r] &0
\end{tikzcd}
\end{document}
```

be two exact sequences of A-modules in which $P,Q$ are projective, then $U \oplus Q \simeq V \oplus P$.
*Proof*:
Note that taking the *pullback* $T=\{(p,q) \in P \oplus Q:\pi(p)=\tau(q)\}$, and the natural maping $\sigma:T \rightarrow P$, then one get that $ker(\sigma) \simeq V$ hence $P \oplus V \simeq T$.

**Theorem**:
Let $A$ be a k-algebra and $P$ an A-module. The following are equivalent:

1. $P$ is projective A-module.
2. For any A-module $U$ the canonical evaluation map $Hom(P,A) \otimes_A U \rightarrow Hom_A(P,U)$ is an isomorphism.(also true if $P$ is on the right side)
3. The canonical evaluation map $Hom_A(P,A) \otimes_A P \rightarrow Hom_A(P,P)$.
4. there is a finite subset $S$ in $P$ and for every $s \in S$, an A-homomorphism $\psi_s:P \rightarrow A$ such that $\sum_{s \in S}\psi_s(p)s=p$ for all $p \in P$.
   *Proof*:
   The map is naturally true for $M$ or $P$ is $A$, so this is ture for $P$ or $U$ are free of finite rank, and it is still isomorphism when multiply an idempotent, hence (1) implies (2), taking $U=P$, one get (3).
   Clearly (3) implies (4).
   Consider the free A-module $A_S$ generated by $\{e_s\}_{s \in S}$, then the map $A_S \rightarrow P$ splits by $p \mapsto \sum_{s \in S}\psi_s(p)e_s$, which implies (1).

**Remark**:
silimiar theorem is true for injective, c.f.[[Projective module and injective module]].

**Definition**:
A morphism $f:X \rightarrow Y$ in a category $\mathcal{C}$ is *split* if there is a morphism $s:Y \rightarrow X$ such that $f=f \circ s \circ f$.

# Wedderburn's theorem

**Definition**:
A k-algebra $A$ is called *simple* if $A \neq 0$ and has no ideals other than trivial ideals. A k-algebra is called *semisimple* if $A$ is semisimple as left A-module, or equivalently, if the regular left A-module is a direct sum of A-modules.

**Theorem**:
A k-algebra $A$ is simple artinian if and only if $A \simeq M_n(D)$ for some positive integer $n$ and some division algebra $D$ over $k$. In that case, $A$ has, up to isomorphism, a unique simple module $S$, and moreover the following holds:

1. We have an isomorphism of left A-modules $A \simeq S^n$; in particular, $A$ is semisimple.
2. We have $D \simeq End_A(S)^{op}$.
3. We have $A \simeq End_{D^{op}}(S)$.
   *Proof*:
   Let $D$ be a division algebra, take $I$ to be an ideal of $M_n(D)$, if $I$ is nontrivial, take $C=(c_{ij})$ be a nonzero element in $I$. Suppose $c_{ij} \neq 0$, then $E_{kj}CE_{il}=c_{ij}E_{kl}$, and $c_{ij}$ is invertable, so $E_{kl} \in I$, hence $I=D$, contradiction. Moreover, $D$ is a division algebra, so $D$ is artinian, hence $M_n(D)$ is artinian. Now suppose $A$ is simple artinian, then there must be a simple A-submodule $S$ (otherwise there would be an infinitly decreasing chain). Then $aS$ is either $\{0\}$ or $S$ for all $a \in A$, also a submodule of $A$. Now consider $\sum_a aS$, a two side ideal of $A$, hence it must be $A$, noting that $A$ is artinian, we know there are only finite $aS \neq 0$. Thus $A \simeq S^n$, taking $D=End_A(S)^{op}$, we get what we want.

**Theorem**:
Let $A$ be a semisimple k-algebra. Then $A$ has finitly many isomorphism classes of simple modules. Let $\{S_i:1 \leq i \leq m\}$ be a set of representatives of the isomorphism classes of simple A-modules. Set $D_i=End_A(S_i)$ and let $n_i$ be the unique positive integer that $A \simeq \bigoplus_{1 \leq i \leq m} (S_i)^{n_i}$ as left A-modules. Then we have an isomorphism of k-algebras $A \simeq \prod_{1 \leq i \leq m}M_{n_i}(D_i^{op})$. In proticular, $A$ is a finite direct product of simple k-algebras, and the simple algebra factors are parametrised by the isomorphism classes of simple A-modules.
*Proof*:
Let $A=\bigoplus_{j \in J}T_j$, where $J$ is a set and $T_j$ is simple left ideal of $A$. Write $1_A=\sum_{i \in I}t_i$, where $I$ is a finite set and $t_i \in T_i$. So we have $A=\bigoplus_{i \in I}T_i$, and using the above theorem, one know immediately $A \simeq \bigoplus_{i \in I}(S_i)^{n_i}$ as A-module, and $End_A(A) \simeq \prod_{i \in I}End_A((S_i)^{n_i}) \simeq \prod_{i \in I}M_{n_i}(D_i)$.

**Theorem**:
Let $A$ be a k-algebra, and $A/J(A)$ is artinian. Then the map sending simple A-module $S$ to its annihilators $M_S$ is a bijection between the isomorphism classes of simple A-modules to the maximal ideals of $A$. In particular, $A$ has only finitly many maximal ideal and their intersection are $J(A)$. Moreover, $A/J(A)$ is semisimple of finite length as $A \otimes_k A^{op}$-module.
*Proof*:
Using the above theorem, let $A/J(A) \simeq \prod_{i=1}^rE_i$, where $E_i$ are simple algebras. $E_i$ are all simple $A \otimes_k A^{op}$-modules, whence the last statment. Let $M_i=E_1 \times \cdots \times \widehat{E_i}\times\cdots\times E_r$, then $M_i$ is an ideal and $A/M_i$ is simple, hence $M_i$ is maximal in $A/J(A)$, one can check that all maximal ideals are of the form $M_i$, so we are done.

**Theorem**:
Let $A,B$ be k-algebras, and let $f:A \rightarrow B$ be a surjective algebra homomorphism, and $A/J(A)$ is artinian. Then $f(J(A))=J(B)$ and $f(A^\times)=B^\times$.
*Proof*:
First, one note that $f(J(A)) \subseteq J(B)$ as every B-module $S$ can be viewed as A-module by $(a,s) \mapsto f(a)s$, so $f(J(A))S=\{0\}$ for all simple modules $S$. Let $A/J(A) \simeq E_1 \times \cdots \times E_n$, let $1 \leq r \leq n$, restrict $f$ to $\bar{f}$ on $E_r$, then one know that $ker(\bar{f})$ is either $\{0\}$ or $E_r$. Hence $B/f(J(A))=\prod_i E_i$ for some $1 \leq i \leq n$, whence $J(B/f(J(A)))=\{0\}$, so $f(J(A))=J(B)$. It is also clear that $f(A^\times) \subseteq B^\times$.

**Theorem**:
Let $k$ be a field with more than three elements, then a finite-dimensional k-algebra $A$ must have a basis consisting of invertable elements.
*Proof*:
First proof that if it i true for $B,C$, then so does $A=B\times C$. Then using the theorem above to proof the semisimple case.

# Splitting field

**Definition**:
Let $A$ be a finite-dimensional k-algebra. We say that $A$ is *split* if $End_A(S) \simeq k$ for every simple A-module $S$, or equivalently, if $A/J(A)$ is a direct product of matrix algebra over $k$. An extension field $k'$ of $k$ is called a *splitting field* for $A$ if the k'-algebra $k' \otimes_k A$ is split. Furthermore, let $G$ be a finite group, we say that $k$ is a *splitting field* if the k-algebra $k[G]$ is split.
**Examples**: Using Wedderburn's theorem, one know that every finite-dimensional algebra over an algebraically closed field is split.

**Theorem**:
Let $A$ be a finite-dimensional k-algebra, and let $S$ be a A-module. The structural algebra homomorphism $A \rightarrow End_k(S)$ is surjective if and only if $S$ is a simple A-module and $End_A(S) \simeq k$.

**Theorem**:
Let $A$ be a split finite-dimensional k-algebra, and let $k'/k$ be a finite extension. Then $k' \otimes_kA$ is a split k'-algebra, we have $J(k' \otimes_k A)=k'\otimes_kJ(A)$, for every simple A-module $S$, then $k'\times_kA$-module $S'=k'\otimes_kS$ is simple, and the corresponding classes of simple A-modules and of simple $k'\otimes_kA$-modules.
*Proof*:
Obviously, $k' \otimes_k J(A) \subseteq J(k' \otimes_k A)$, so we only need to consider the case of $J(A)=\{0\}$, i.e. $A$ is semisimple. Using the wedderburn's theorem, we know that $k' \otimes_k A$ is the direct product of matrix algebra over k'. In particular, $k' \otimes_k A$ is semisimple, hence $J(k' \otimes_k A)=\{0\}$. The rest follows immediately.

**Proposition**:
Let $A$ be a finite-dimensional k-algebra. Let $S$ be a simple A-module, and let $b$ be the unique block idempotent in $Z(A)$ to which $S$ belongs. The block algebra $Ab$ is isomorphic to a matrix algebra over $k$ if and only if $S$ is projective and injective. In that case, we have $Ab \simeq End_k(S)$.
*Proof*:
Note that if $Ab$ is isomorphic to a matrix algebra, then $J(Ab)=\{0\}$. Then $S$ is projective and injective as an A-module. And that $A \rightarrow S$ is surjective, so there is a submodule isomorphic to $S$. Let $U=\bigoplus_ss$ where $s$ run through all submodule of $A$ isomorphic to $S$. Then $U \simeq S^n$, which is also injective, so there is a submodule $V$ such that $A=U \oplus V$. It follows that $Hom_A(U,V)=0$, so $A=End_A(A)^{op}=End_A(U)^{op} \times End_A(V)^{op}$, in fact the indecomposable algebra $End_A(U)^{op}=M_n(k)$ as $End_A(S)=k$. So $S$ is contained in that block. The result follows.

**Theorem**:
Let $k'/k$ be a field extension and let $A$ be a finite-dimensional k-algebra such that the k'-algebra $A'=k' \otimes_k A$ is split. Then the k-algebra $A$ is split if and only if for every simple A'-module $S'$ there is a (necessarily simple) A-module $S$ such that $k' \otimes_k S \simeq S'$. In that case, the map sending $S$ to $k' \otimes_k S$ induces a bijection between the sets of isomorphism classes of simple A-module and simple A'-modules, and we have $J(A')=k' \otimes_k J(A)$.
*Proof*:

1. We first proof that if $S' \rightarrow T'$ is a nonzero A'-homorphism of two simple A'-modules, then $S \simeq T$ as A-module. In fact, $S'=k' \otimes_kS,\,T'= k' \otimes_kT$ can been seen as A-module, and the map $\phi:S' \rightarrow T$ will be restriced to $\psi:S \rightarrow k'\otimes_kT \simeq T^n$ as A-modules. So $S \simeq T$.
2. Now one know that the map $S' \rightarrow S$ is injective. Consider $k' \otimes_k S$ for an arbitrary simple A-module, then because it is finite-dimensional, there must be a simple A'-submodule $W \simeq k' \otimes_k T$, so $S \simeq T$, hence the map is bijective.
3. The structural homomorphism $A \rightarrow \prod_S End(S)$ where $S$ run through all isomorphism classes of simple A-modules. The map above induced an injective map $A/J(A) \rightarrow \prod_S End(S)$. Using the fact that $S'$ is split and $S \rightarrow S'$ is bijective, one get $k' \otimes_k A/J(A) \rightarrow \prod_SEnd(k' \otimes_k S) \simeq (k' \otimes_k A)/k' \otimes_k J(A)$. Thus $J(A')=k' \otimes_k J(A)$.

**Theorem**:
Let $A$ be a finite-dimensional k-algebra, then there is a finite extension $k'/k$ such that $k' \otimes_k A$ is split as k'-algebra.
*Proof*:
Let $\bar{k}$ be the algebraic closure of $k$, then $\bar{k} \otimes_k A$ is split. Let $S$ be a simple $\bar{k} \otimes_k A$ which have a basis $\{s_1,\cdots,s_t\}$. Choose $X$ be a basis of $A$, then the action of $x \in X$ acts on $S$ as an $(\sigma_{i,j}) \in M_{t \times t}(\bar{k})$. Choose $k'$ such that all $\sigma_{i,j}$ are in $k'$, with $S$ runs over all representatives of isomorphism classes of simple modules, and $x$ runs over $X$. Now let $S'=\sum_ik's_i$ be the module generated by $\{s_1, \cdots,s_t\}$, one check immediately that it is a $A$ module. Moreover, $\bar{k} \otimes_{k'} S' \simeq S$, so unsing the theorem above, one proof the theorem.

**Definition**L:
Let $A$ be a k-algebra, and $k_0$ is a subfield of $k$. We say that $A$ is *defined over $k_0$* if there is a $k_0$-algebra $A_0$ such that $A \simeq k \otimes_{k_0}A_0$.

**Proposition**:
Suppose that $k$ is an algebraically closed field of primitive character $p$. Let $q$ be a power of $p$ and let $V$ be a k-vector space of finite-dimensional $n$. Let $\Phi$ be an additive automorphism of $V$ and denoted by $V^\Phi$ be the subgroup of fixed points in $V$ of $\Phi$. Suppose that $\Phi(\lambda v)=\lambda^q\Phi(v)$ for all $v \in V$ and all $\lambda \in k$. Then $V^\Phi$ is an $\mathbb{F}_q$-subspace of $V$ such that $V=k \otimes_{\mathbb{F}_q} V^\Phi$.
*Proof*:
It is clear that $V^\Phi$ is an $\mathbb{F}_q$-subspace of $V$, so we only need to check that $V=k\otimes_{\mathbb{F}_q} V^\Phi$. Set $I=\{1,\cdots,n\}$ and choose $(x_i)_{i \in I}$ be a basis for $V$. Take $S=(s_{ij}) \in M_{n \times n}(k)$ be the corresponding matirx of $\Phi$ under the basis $(x_i)$, clearly, $S$ is invertable. Set $F:k \rightarrow k$ by $F(\lambda)=\lambda^q$. Using the theorem of *Lang*, one know there is a $T=(t_{ij})$ such that $T\cdot F(T)^{-1}=S$. Set $y_i=\sum_{j}t_{ij}x_j$, then $\Phi(y_i)=\sum_jt_{ij}^q\Phi(x_j)=\sum_u\sum_j(s_{ju}t_{ij}^q)x_u$, using the fact that $S \cdot F(T)=T$, one know that $\Phi(y_i)=y_i$. Meanwhile, $S,T$ is invertable, so $y_i$ form a basis for $V$, so we proof the theorem.

# Modules for simple group algebra

**Theorem**:
Let $k$ be a splitting field for $G$ such that $|G|$ in invertable in $k$, then the number of isomorphism classes of simple $k[G]$-module is equal to the number of conjugacy classes of $G$.
*Proof*:
Using the Maschke's theorem, we know that $k[G]$ is semisimple, hence it is isomorphic to $\prod_iEnd_k(S_i)$ where $S_i$ is the representatives of isomorphism classes of simple $k[G]$-modules. Now consider $Z(k[G])$, one know that $dim_k(Z(k[G]))$ is equal to the number of conjugacy classes of $G$. Meanwhile, $Z(End_k(S_i))=k \cdot id_{S_i}$ ([[Schur's lemma]]), so the number of $S_i$ is equal to $dim_k(Z(k[G]))$ as well.

**Theorem**:
Let $A$ be a finite-dimensional split algebra over a field $k$, then the number of isomorphism classes of simple A-modules is equal to $dim_k(A/(J(A)+[A,A]))$.
*Proof*:
We may assume that $A$ is split semisimple since it won;t make any differece if we quotient out $J(A)$. In that case $A/(J(A)+[A,A])=A/[A,A]$. In particular, we may assume $A$ is a matrix algebra over $k$, but then $A$ has a unique isomorphism class of simple A-module, and that $dim_k(A/[A,A])=1$.

**Lemma**:
Let $G$ be a finite group and $k$ a field with prime character $p$. Then for all $x \in G$, there is a unique $u,v \in \langle x \rangle$ such that $u$ is a $p$-element and $q$ a $p'$-element with $x=uv=vu$, and if the order of $u$ is $p^a$, then $(x-v)^{p^a}=0$ in $k[G]$.

**Lemma**:
Let $A$ be a finite-dimensional algebra over a field $k$ with prime character $p$, then for all $a,b \in A$ and $n \in \mathbb{Z}_{\geq 0}$ there is a $c \in [A,A]$ such that $(a+b)^{p^n}=a^{p^n}+b^{p^n}+c$.
*Proof*:
Let $x_1x_2\cdots x_{p^n}$ be a string consists of $a,b$, set $\gamma(x_1\cdots x_{p^n})=x_{p^n}x_1\cdots x_{p^n-1}$, then $\gamma(x)-x$ is a commutator, hence $(a+b)^{p^n}=\sum_i \begin{pmatrix}p^n\\ i\end{pmatrix}a^ib^{n-i}+c=a^{p^n}+b^{p^n}+c$, where $c \in [A,A]$.

**Lemma**:
Let $A$ be a finite-dimensional algebra over a field $k$ with prime character $p$. For any $a \in [A,A]$ and any nonnegative integer $n$, we have $a^{p^n} \in [A,A]$. Meanwhile, $a \in J(A)+[A,A]$ if and only if $a^{p^n} \in [A,A]$ for some $n$.
*Proof*:
Let $\bar{a}$ be the image of $a$ in $A/J(A)$, a matrix space over $k$. So one have $\bar{a}^{p^n} \in [\bar{A},\bar{A}]$ has trace 0. Extending $k$ to its algebraic closure $\bar{k}$, $\bar{a}$ is conjugate to an upper triangle matrix, so the trace of $\bar{a}$ is 0 as well, hence $\bar{a} \in [\bar{A},\bar{A}]$, i.e. $a \in J(A)+[A,A]$. Conversely, choose $b \in J(A)$
such that $a+b \in [A,A]$, then let $n$ large enough, one have $a^{p^n}=(a+b)^{p^n}+c \in [A,A]$.

Now we are able to proof the following theorem.
**Theorem**(Brauer):
Let $G$ be a finite group and $k$ a splitting field of $k$ with character $p$, then the number of isomorphism classes of simple $k[G]$-modules is equal to the number of conjugacy classes of $p'$-elements in $G$.
*Proof*:
We now need to compute the dimension of $K[G]/(J(k[G])+[k[G],k[G]])$. Use the lemma above, $(x-v)^{p^n}=0$, so $x-v \in J(k[G])+[k[G],k[G]]$, so the image of $x$ and $s$ in $K[G]/(J(k[G])+[k[G],k[G]])$ is equal, hence $R'$ the set of representatives of all conjugacy classes for $p'$-elements spanned $K[G]/(J(k[G])+[k[G],k[G]])$. Suppose $\sum_{s \in R'} \lambda_ss \in J(k[G])+[k[G],k[G]]$, which is to say $\sum_{s \in R'} \lambda_s^{p^n}s^{p^n} \in [k[G],k[G]]$ for some $n$. One note that $s^{p^n}$ is just another set of representatives of these conjugacy classes, so they are linearly independent.

For any finite-dimensional algebra for any field $k$, $l(A)$ denote the number of isomorphism classes of simple A-modules.

**Theorem**:
Let $G$ be a finite group, $K$ a splitting field for $G$ of characteristic zero and $k$ an splitting field for all subgroups of $G$ of positive characteristic $p$. Denote by $\mathcal{U}$ a set of representatives of the conjugacy classes of p-elements in $G$. we have $l(K[G])=\sum_{u \in \mathcal{U}}l(k[C_G(u)])$.
*Proof*:
If $x,y \in G$ are conjugate then their p-parts are conjugate. If $x,y$ are the same p-parts $u$ then their p'-parts are conjugate in $C_G(u)$. Thus if $u$ runs over $\mathcal{U}$ and, for any such $u$ we let $s$ run over a set of representatives of the p'-conjugacy classes in $C_G(u)$, then $us$ runs over a set of representatives of the conjugacy classes of $G$. In particular, the number of conjugacy classes of $G$, which is in fact $l(K[G])$, is equal to the sum, taken over $u \in \mathcal{U}$, of the numbers of p'-conjugacy classes in $C_G(u)$.This sum is equal to the sum of the numbers $l(k[C_G(u)])$, with $u$ running over $\mathcal{U}$, as claimed.

> [!note] Alperin's Weight Conjecture for finite groups
> Let $G$ be a  finite group and $k$ an algebraically closed field of prime characteristic $p$. Then
>
> $$
> l(k[G])=\sum_Q\omega(k[N_G(Q)/Q])
> $$
>
> where $Q$ runs over a set of representatives of the G-conjugacy classes of p-subgroups of $G$, and where $\omega(k[N_G(Q)/Q])$ denotes the number of isomorphism classes of simple projective $k[N_G(Q)/Q]$.

**Definition**:
Let $G$ be a finite group and $k$ be a field of prime characteristic $p$. A projective simple $k[N_G(Q)/Q]$-module is called a *weight* of $G$, or a p-weight of $G$, if the ambient characteristic needs emphasising.

# Central simple and seperable algebras

**Definition**:
An algebra over a field $k$ is called *certral simple* if $A$ is a simple k-algebra such that $Z(A)=k$.

**Proposition**:
Let $A$ be a central simple algebra over a field $k$, and $B$ a simple k-algebra. Then $A \otimes_kB$ is simple, and if $B$ is central simple, then $A \otimes_kB$ is central simple.
*Proof*:
Let $I$ be a nonzero ideal in $A \otimes B$. Then any $x \in I$ can be written in the form $x=\sum_{i=1}^m a_i \otimes b_i$ for some $a_i \in A,b_i \in B$. Choose $x \neq 0$, and $m$ smallest possible. We show that $m=1$. If not, using the fact that $A$ is simple, we can find $\sum_jy_ja_1z_j=1$, then $\sum_j(y_j \otimes 1)x(z_j \otimes 1)=\sum_i(\sum_jy_ja_iz_j) \otimes b_i$ is in $I$, so one may assume $a_1=1$. Choose $a_2 \in I$, then $a_2 \not \in Z(A)$, so $(u \otimes 1)x-x(u \otimes 1) \in I-\{0\}$, which is now a sum of $m-1$ elements, a contradiction. The rest is clear.

**Proposition**:
Let $A$ be a finite-dimensional algebra over a field $k$. Then $A$ is a central-simple k-algebra if and only if the canonical algebra homomorphism $\Phi:A \otimes_k A^{op} \rightarrow End_k(A)$ defined by $\Phi(a \otimes b)(c)=acb$ for all $a,b,c \in A$ is an isomorphism.
*Proof*:
Suppose $\Phi$ is an isomorphism, then every ideal $J$ in $A$ yields an ideal $J \otimes A^{op}$. Since $End_k(A)$ is a simple algebra this imples $A$ is simple. Moreover, on one hand we hace $Z(End_k(A)) \simeq k$, and on the other hand we have $Z(A \otimes_k A^{op})=Z(A) \otimes_kA^{op}$. This forces $Z(A) \simeq k$, and hance $A$ is central simple. Suppose conversely that $A$ is central simple. Then, again we have $Z(A \otimes_k A^{op}) \simeq k$, and by the previous proposition, $A \otimes_k A^{op}$ is the map $\Phi$ is injective. But then $\Phi$ is an isomorphism as both sides hace the same dimension.

**Definition**:
Two finite dimensional central simple algebras $A,B$ over a field are called *equivalent* if there are positive integers $m,n$ such that $M_m(A) \simeq M_n(B)$. We denote by $[A]$ the equivalent class of $A$. The equivalence class of the trivial algebra $k$ consists of all amtrix algebra $M_n(k)$, with $n \in \mathbb{N}$. The above proposition tells us that $[A \otimes_k A^{op}]=[k]$. Using this observation, one get the *Brauer group* of a field $k$, with multiplication $[A] \cdot [B]=[A \otimes_k B]$, then it is clear that $[A]^{-1}=[A^{op}]$.

**Theorem**:(Skolem-Noether):
Let $A$ be a finite-dimensional central simple algebra over a field $k$. Any $k$-algebra automorphism of $A$ is an inner automorphism.
*Proof*:
Consider a simple $A$-module $V$, take $\alpha:A \rightarrow A$ be an automorphism, then $A$ acting on $V$ by $\alpha(a)v$ induces another $A$-module $\alpha V$, recall the wedderburn's theorem, $\alpha V \simeq V$, so there is a $\tau:V \rightarrow V$ such that $\alpha(a)v=\tau(av)$. Recall further that $A \simeq End_{D}(V)$ for some division algebra $D=End_A(V)$, so we hope that the above argument can be transfered to the case of $A$ being a $D$-module, the most easy way to do so is simply consider $A \otimes D$ as $V$ naturally have the structure of $D$-module and that $A \otimes D$ is still simple using the lemma above, thus we proof the theorem.
**Remark**:
In fact, one should note that the wedderburn's theorem tells us that $V$ more or less determined the structure of $A$, so it is natural for us to consider $V$ in this case.

The above theorem does not hold for ring automorphism that does note preserve the structure of algebra, clearly no nontrivial automorphism of a field can be inner. Given a subalgebra of an algebra $A$, define $C_A(B):=\{a \in A:ab=ba\ \forall b \in B\}$, i.e. the centraliser of $B$ in $A$.

**Theorem**:
Let $A$ be a finite-dimensional central simple algebra over a field $k$ and let $B$ be a simple subalgebra of $A$. THen $C_A(B)$ is a simple subalgebra of $A$, we have $dim_k(A)=dim_k(B)dim_k(C_A(B))$ and $C_A(C_A(B))=B$. Moreover, if $B$ is central, then multiplication in $A$ induces an isomorphism of $k$-algebras $B \otimes_k C_A(B) \simeq A$.
*Proof*:
Let $V$ be the simple module of $A$ and set $D=End_A(V)$, then we know that there is an positive integer $n$ such that $A\simeq M_n(D^{op})\simeq V^n$. So $dim_k(V)=n\cdot dim_k(D)$, then consider $V$ as $A \otimes_k D$-modules which is still central simple, hence $A \otimes D \rightarrow End_k(V)$ is injective but both sides have dimension $n^2$, so it is an isomorphism. Taking the centralizer of $B$, then we got $C_A(B) \simeq End_{B \otimes D}(V)$. Since $D$ is central simple, the algebra $B \otimes D$ is simple. Thus, if we denote by $W$ a simple $B \otimes_k D$ is simpl then $Res_{B \otimes_k D}^{A \otimes_k D} \simeq W^m$ for some positive integer $m$. We know that $B \otimes_kD \simeq End_E(W)$ where $E=End_{B \otimes D}(W)$. It follows that $C_A(B) \simeq End_{B \otimes D}(V) \simeq M_m(E)$, and this is a simple algebra as $E$ is a division algebra. We have $dim_k(B \otimes_k D)=dim_E(W)^2dim_k(E)$ and $dim_k(C_A(B))=m$2dim_k(E)$. Their product is euqal to $m^2dim_k(W)^2=dim_k(V)^2=m^2dim_k(E)$. This shows that $dim_k(A)=dim_k(B)dim_k(C_A(B))$. Since $B \subseteq C_A(C_A(B))$, comparing the dimension we know that $B=C_A(C_A(B))$. If $B$ is central simple, then $B \otimes_k C_A(B)$ is simple. Thus the map $B \otimes_k C_A(B) \rightarrow A$ induced by multiplication in $A$ is injective. But then this map is an isomorphism as both sides have the same dimension.

**Definition**:
A algebra $A$ over a commutative ring $k$ is called *seperable* if $A$ is projective as an $A \otimes_k A^{op}$-module, or equivalently, as an A-A-bimodule.
An easy example of this is $M_n(k)$ ,which is obviously seperable.

**Proposition**:
Let $A$ be a finite-dimensional seperable algebra over a field $k$. Then $J(A)={0}$, or equivalently, every left or right $A$-module is semisimple.
*Proof*:
Take $U$ an $A$-module then we know that $A \otimes_k A \rightarrow A$ splits, tensored with $- \otimes_A U$, one know that $A \otimes_k U \rightarrow U$ splits as well, thus $U$ is a direct summand of $A \otimes_k U$. Note that $U$ has a basis over $k$, so $A \otimes_k U$ free $A$-module, thus $U$ is projective. Hence all right $A$-module is projective, so $A$ is semisimple.
**Remark**: In the Maschke's theorem, we actually proof that $k[G]$ is not only semisimple, but seperable in the case of $|G|^{-1}$ exits in $k$.

**Propositon**:
Let $k$ be a field, $A$ a finite-dimensional seperable $k$-algebra, and $B$ a finite-dimensional $k$-algebra. Then $J(A \otimes_k B) =A \otimes_k(J(B))$.
*Proof*:
The key observation is $A \otimes_k B$ is a direct summand of $(A \otimes_k B) \otimes_B (A \otimes_k B)$ (where we WOLG assume that $B$ is semisimple), and then $A \otimes_k B$ is a projective $B$-module, so any $A \otimes_k B$-module is projective, hance $J(A \otimes_k B)=\{0\}=A \otimes_k J(B)$.

**Proposition**:
Let $k'/k$ be a field extension, and let $A$ be a k-algebra. Then $A$ is seperable if and only if the $k'$-algebra $k' \otimes_k A$ is seperable.
*Proof*:
One notice that $(k' \otimes_k A) \otimes_{k'} (k' \otimes_k A) \simeq k' \otimes_k (A \otimes_k A)$. It follows immediately that if $A$ is seperable, then so is $k' \otimes A$. If $k' \otimes A$ is seperable, then the canonical map $k' \otimes_k (A \otimes_k A) \rightarrow k' \otimes_k A$ splits. Writhe the image of $1_{k' \otimes A}$ under a section in the form $\sum_\lambda \lambda \otimes z_{\lambda}$
, with $\lambda \in k'$ running over a $k$-basis of $k'4 containing $1$, and where $z_\lambda \in A \otimes_k A$. One verifies that there is a unique section $A \rightarrow A \otimes_k A$ as bimodules that sends $1_A$ to $z_1$.

**Proposition**:
Let $k'/k$ be a finite extension, then $k'/k$ is a seperable extension if and only if $k'$ is a seperable $k$-algebra.
*Proof*:
One way of the equivalence is clear, note that take $\alpha \in k'$ and $f \in k[x]$ be its minimal polynomial over $k$, wirite it in the form of $f=\prod_i(x-\alpha_i)^{m_i}$ and $E$ the splitting field of $f$, then if $f$ is seperable i.e. $m_i=1$ for all $i$, hence $E \otimes_k k(\alpha) \simeq E[x]/fE[X] \simeq \prod_iE[X]/(x-\alpha_i)^{m_i}E[x] \simeq E^m$ for some $m$. In particular, the $E$-algebra $E \otimes_k k(\alpha)$ is seperable. On the other hand, if $m_i>1$ for some $i$, then $(x-\alpha_i)+(x-\alpha_i)^{m_i}E[x]$ is a nilpotent element in $E[x]/(x-\alpha_i)^{m_i}E[X]$, so it has a nonzero readical, hance $E \otimes_k k'$ has nonzero readicals. One know that if $k'/k$ is seperable, then there must be a $\alpha \in k'$ such that $k'=k(\alpha)$, using the proposition above, we know that $k'$ is seperable over $k$. On the other hand, if $k'/k$ is not a seperable extension, then there must be $m_i \geq 2$. By the above, there is a field extension $E$ of $k$ such that $E \otimes_k k'$ is not seperable, and hance neither is $k'$.

# Complexes and homology
(In almost all cases we consider the category of modules)

**Definition**:
A *graded object over a category* $\mathcal{C}$ is a family $X=(X_n)_{n \in \mathbb{Z}}$ of objects $X_n$ in $\mathcal{C}$. Given two graded objects $X=(X_n)_{n \in \mathbb{Z}}$ and $Y=(Y_n)_{n \in \mathbb{Z}}$ in $\mathcal{C}$, a *graded morphism of degree m* is a family $f=(f_n)_{n \in \mathbb{Z}}$ of morphisms $f_n: X_n \rightarrow Y_{n+m}$ in $\mathcal{C}$. The category of graded objects over $\mathcal{C}$ with graded morphisms of degree zero is denoted $Gr(\mathcal{C})$.

**Definition**:
A chain complexes over an additive category $\mathcal{C}$ is a pair $(X,\delta)$ consisting of a graded object $X$ in $\mathcal{C}$ and a graded endomorphism $\delta$ of degree $-1$, called the *differential of the complex*, satisfying $\delta \circ \delta=0$. Dually a cochain complex over a $\mathcal{C}$ is a pair $(X,\delta)$ consisting of a graded object $X=(X^n)_{n \in \mathbb{Z}}$ in $\mathcal{C}$ and a graded endomorphism $\delta=(\delta^n:X^n \rightarrow X^{n+1})_{n \in \mathbb{Z}}$, called differential of the cochain complex, of degree 1 satisfying $\delta \circ \delta=0$.
One can visualize it by thinking it as an infinitly long chain of morphisms with the composition of any neighbors are 0.
$$ \cdots \longrightarrow X_{n-1} \longrightarrow X_n \longrightarrow X_{n+1} \longrightarrow \cdots$$
Then a cochain is simply revering all the arrows and preserve all other features. We will use $X[i]_n=X_{n-i}$ to denote the action of shifting the complex forward, similarly $f[i]_n=f_{n-i}$.

**Definition**:
A *chain map* between two chain complexes $(X,\delta),(Y,\epsilon)$ oer an additive category $\mathcal{C}$ is a graded morphism of degreen zero $f=(f_n:X_n \rightarrow Y_n)_{n \in \mathbb{Z}}$ satisfying $f \circ \delta =\epsilon \circ f$, or equivalently, $f_{n-1} \circ \delta_n=\epsilon_n \circ f_n$ for $n \in \mathbb{Z}$. Cochain maps are defined similarly. The chain complexes, together with chain maps, form the category $Ch(\mathcal{C})$ of *chain complexes over* $\mathcal{C}$.

**Definition**:
Let $\mathcal{C}$ be an abelian category. The *homology* of a chain complex $(X,\delta)$ over $\mathcal{C}$ id the graded object $H_*(X,\delta)=ker(\delta)/Im(\delta)$; more explicitly, $H_n(X,\delta)=ker(\delta_n)/Im(\delta_{n+1})$ for $i \in \mathbb{Z}$. If $H_*(X)=\{0\}$ then $X$ is called *exact* or *acyclic*. Similarly, the *cohomology* of a cochain is just the same a homology.
In fact, if one consider $f:X \rightarrow Y$, then it induces a map $Im(\delta) \rightarrow Im(\epsilon)$ and $ker(\delta) \rightarrow ker(\epsilon)$ so there is a map $H_*(f):H_*(X) \rightarrow H_*(Y)$. One can easily verify that $H_*(g \circ f)=H_*(g) \circ H_*(f)$ for two chain maps $f,g$. The chain map $f$ is called *quasi-isomorphism* if the induced map $H_*(f)$ is an isomorphism $H_*(X) \simeq H_*(Y)$, and it actually forms an equivalent relation. 

**Theorem**:
Let $A$ be a k-algebra. Any [[Short exact sequence]] of chain complexes of $A$-modules 
$$0 \longrightarrow X \stackrel{f}{\longrightarrow} Y \stackrel{g}{\longrightarrow} Z \longrightarrow 0$$
induces a long exact sequence
$$ \cdots \longrightarrow H_n(X) \stackrel{H_n(f)}{\longrightarrow} H_n(Y) \stackrel{H_N(g)}{\longrightarrow} H_n(Z) \stackrel{d_n}{\longrightarrow} H_{n-1}(X) \longrightarrow \cdots$$
depending only on the [[Short exact sequence]].
*Proof*:
Denote by $\delta,\epsilon,\zeta$ the differentials of $X,Y,Z$, respectively. We defined $d_n:H_n(Z) \rightarrow H_{n-1}(X)$ as follows: any elements in $H_n(Z)$ is of the form $z+Im(\zeta_{n+1})$ for some $z \in ker(\zeta_n)$, then we notice that there must be a $y \in Y_n$ such that $g_n(y)=z$, then $g(\epsilon_n(y))=0$ so $\epsilon_n(y) \in ker(g_{n-1})=Im(f_{n-1})$, hence there must be a $x \in X_{n-1}$ such that $f_{n-1}(x)=y$, and we set $d_n:z+Im(\zeta_{n+1}) \mapsto x+Im(\delta_{n})$. We now check that $d_n$ is well defined: which is clear enough since if we choose $z+Im(\zeta_{n+1})=z'+Im(\zeta_{n+1})$ then there the difference can be represented by $\zeta_{n+1}(z_0)$ for some $z_0 \in Z_{n+1}$, take a $y_0 \in Y_{n+1}$ such that $g_{n+1}(y_0)=z_0$ using the fact that $Y$ is a complex, we know that this make no difference on the choice of $y$ in our definition. If we choose two different $y,y'$ such that $g_n(y)=g_n(y')=z$, then $y-y' \in ker(g_n)=Im(f_n)$, take $f_n(x_0)=y-y'$, so $\epsilon_n(y-y')=f_{n-1}(\delta_{n}(x_0))$, note that $f$ is injective, so the two different $x,x'$ construct from $y,y'$ only have the difference of $\delta_n(x_0) \in Im(\delta_n)$, so $d_n$ is indeed well defined.
**Remark**: The technique used in the proof is called *diagram chasing*, which is simple take an element and "chasing" it around the diagram, which will almost lead you to the satisfying result.

Here is a classical example:
**Lemma**(5-Lemma):
Let $A$ be a $k$-algebra and let
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
&X_1 \arrow[r,"f_1"] \arrow[d,"a_1"] &X_2 \arrow[r,"f_2"] \arrow[d,"a_2"] &X_3 \arrow[r,"f_3"] \arrow[d,"a_3"] &X_4 \arrow[r,"f_4"] \arrow[d,"a_4"]
&X_5 \arrow[d,"a_5"]\\
&Y_1 \arrow[r,"g_1"] &Y_2 \arrow[r,"g_2"] &Y_3 \arrow[r,"g_3"] &Y_4 \arrow[r,"g_4"] &Y_5
\end{tikzcd}
\end{document}
```
be a commutative diagram of $A$-modules with ecaxt rows. If $a_1,a_2,a_4,a_5$ are isomorphisms the $a_3$ is an isomorphism.

**Definition**:
Let $A$ be a k-algebra. Let $(X,\delta)$ be a complex of right $A$-modules, and let $(Y,\epsilon)$ be a complex of left $A$-modules. We define a complex of $k$-modules $X \otimes_k Y$ by setting $(X \otimes_A Y)_n=\oplus_{i+j=n}X_i \otimes_AY_j$, the direct sum taken over all pairs of integers $(i,j)$ satisfying $i+j=n$, with differential given by taking the direct sum of the maps $(-1)^iId_{X_i}\otimes \epsilon_j:X_i \otimes_A Y_j \rightarrow X_i \otimes_A Y_{j-1}$ and $\delta \otimes_A Y_j \rightarrow X_{i-1} \otimes_A Y_j$.
And the $Hom(X,Y)$ is just the "inverse" of $X \otimes Y$.

# Complexes and homotopy
**Definition**:
Let $\mathcal{C}$ be an additive category and let $(X,\delta),(Y,\epsilon)$ be complexes over $\mathcal{C}$. A *homotopy* from $X$ to $Y$ is a graded morphism $h:X \rightarrow Y$ of degree 1; that is $h$ is a family of morphisms $h_n:X_n \rightarrow Y_{n+1}$ in $\mathcal{C}$, for any $n \in \mathbb{Z}$. We do not require $h$ to commute with the differentials. Two chain morphisms $f,f':X \rightarrow Y$ are called *homotopic*, written $f \sim f'$, if there is a homotopy $h:X \rightarrow Y$ such that $f-f'=\epsilon \circ h+h \circ \delta$. In that case we say that $h$ is a *homotopy* from $f$ to $f'$. A chain map $f:X \rightarrow Y$ is a *homotopy equivalence* if there is a chain map $g:Y \rightarrow X$ such that $g \circ f \sim id_X$ and $f \circ g \sim id_Y$; in that case, $g$ is called a *homotopy inverse of $f$*, and the complexes $X,Y$ are said to be *homotopy equivalent*, written $X \simeq Y$. If $X \simeq 0$, we say that $X$ is *contradictable*. For cochain complexes, we define analogously a *cochain homotopy* to be a graded morphism of degree $-1$.

Further, let $\mathcal{C}$ be an additive category, then the *homotopy category* of complexes over $\mathcal{C}$ is the category $K(\mathcal{C})$ whose objects are complexes over $\mathcal{C}$ and morphism are graded morphism quotient out by homotopy equivalence. 

**Proposition**:
Let $\mathcal{C}$ bt a abelian category, and let $f,f':(X,\delta) \rightarrow (Y,\epsilon)$ be chain maps of complexes over $\mathcal{C}$.
1. For any homotopy $h:X \rightarrow Y$, the graded morphism $h \circ \delta + \epsilon \circ h: X \rightarrow Y$ is a chain map inducing the zero morphism from $H_*(X)$ to $H_*(Y)$.
2. If $f \sim f'$ then $H(f)=H(f'):H_*(X) \rightarrow H_*(Y)$.
3. If $f$ is a homotopy equivalence, then $f$ is a quasi-isomorphism.
4. If $X \simeq 0$ then $X$ is acyclic.
*Proof*:
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
&\cdots \arrow[r,"\delta_{n-1}"] &X_{n-1} \arrow[r,"\delta_{n}"] \arrow[rd,"h_{n-1}"] \arrow[d,"f_{n-1}"] &X_{n} \arrow[r,"\delta_{n+1}"] \arrow[rd,"h_{n}"] \arrow[d,"f_{n}"] &X_{n+1} \arrow[r,"\delta_{n+2}"] \arrow[rd,"h_{n+1}"] \arrow[d,"f_{n+1}"] &X_{n+2} \arrow[r,"\delta_{n+3}"] \arrow[d,"f_{n+2}"] &\cdots\\
&\cdots \arrow[r,"\epsilon_{n-1}"] &Y_{n-1} \arrow[r,"\epsilon_{n}"] &Y_{n} \arrow[r,"\epsilon_{n+1}"] &Y_{n+1} \arrow[r,"\epsilon_{n+2}"] &Y_{n+2} \arrow[r,"\epsilon_{n+2}"] &\cdots
\end{tikzcd}
\end{document}
```
1. note that $\epsilon \circ(h \circ \delta+\epsilon \circ h)=\epsilon \circ h \circ \delta=(h\circ \delta + \epsilon \circ h) \circ \delta$, so the morphism is well defined. In fact, if $x \in ker(\delta)$, then $(h \circ \delta + \epsilon \circ h)(x)=\epsilon \circ h(x) \in im(\epsilon)$, so all $H(X)$ are send to $0$ in $H(Y)$.
2. Note that if $f \sim f'$, then there is a $h$ such that $f-f'=h \circ \delta + \epsilon \circ h$, using the result of 1), one know that $f-f'$ is 0 morphism form $H(x) \rightarrow H(Y)$, hence $H(f)=H(f')$.
3. Using 2), one know that $id_{H_*(X)}=H(g)\circ H(f)$ and $id_{H_*(Y)}=H(f) \circ H(g)$.
4. Follow directly from 3).

**Proposition**:
Let $A$ be a k-algebra, $V$ an A-module, and $(X,\delta)$ a complex of A-modules. Let $n$ be an integer.
1. There is a natural isomorphism $H_n(Hom_A(V,X)) \simeq Hom_{K(Mod(A))}(V,X[n])$. In particular, there is a natural isomorphism $H_n(X) \simeq Hom_{K(Mod(A))}(A,X[n])$.
2. There is a natural isomorphism $H^n(Hom_A(X,Y)) \simeq Hom(X,V[n])$.

**Theorem**:
Let $\mathcal{C}$ be an abelian category, let $P$ be a complex of projective objects in $\mathcal{C}$, $I$ an porjective objects in $\mathcal{C}$ and let $0 \longrightarrow X \stackrel{f}{\longrightarrow} Y \stackrel{g}{\longrightarrow} Z \longrightarrow 0$ be a short ecaxt sequence of complexs over $\mathcal{C}$.
1. Suppose that $X$ is acyalic and that one of $P,Y$ is bounded below. The map $Hom_{Ch(\mathcal{C})}(P,Y) \rightarrow Hom_{Ch(\mathcal{C})}(P,Z)$ given by composition with $g$ is surjective and induces an isomorphism $Hom_{K(\mathcal{C})}(P,Y) \simeq Hom_{K(\mathcal{C})}(P,Z)$.
2. Suppose that $Z$ is acyclic and that one of $Y,I$ is bounded above. The map $Hom_{Ch(\mathcal{C})}(Y,I) \rightarrow Hom_{Ch(\mathcal{C})}(X,I)$ given by precomposition with $f$ is surjective and induces an isomorphism $Hom_{K(\mathcal{C})}(Y,I) \simeq Hom_{K(\mathcal{C})}(X,I)$.
*Proof*:
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
&&X_{n} \arrow[rr,"\delta_n"] \arrow[dd,"f_n"] 
&&X_{n-1} \arrow[rr,"\delta_{n-1}"] \arrow[dd,"f_{n-1}"] 
&&X_{n-2} \arrow[dd,"f_{n-2}"]\\

&P_{n} \arrow[rr,"\pi_n"] \arrow[rd,"p_n"] \arrow[rddd,"q_n"] 
&&P_{n-1} \arrow[rr,"\pi_{n-1}"] \arrow[rd,"p_{n-1}"] \arrow[rddd,"q_{n-1}"]
&&P_{n-2} \arrow[rd,"p_{n-2}"] \arrow[rddd,"q_{n-2}"]\\

&&Y_{n} \arrow[rr,"\epsilon_n"] \arrow[dd,"g_{n}"] 
&&Y_{n-1} \arrow[rr,"\epsilon_{n-1}"] \arrow[dd,"g_{n-1}"] 
&&Y_{n-2} \arrow[dd,"g_{n-2}"]\\
\\
&&Z_{n} \arrow[rr,"\zeta_{n}"] 
&&Z_{n-1} \arrow[rr,"\zeta_{n-1}"] 
&&Z_{n-2} 
\end{tikzcd}
\end{document}
```
Denote by $\delta,\epsilon,\zeta,\pi$ the differentials of $X,Y,Z,P$. Given any $q:P \rightarrow Z$, we construct a $p:P \rightarrow Y$ such that $q=g \circ p$. In fact, we have $P,Y$ is bounded below, so we can take $p_i=0$ for sufficently small $i$, and now we construct $p$ inductively. Since $P_n$ is projective and $g_n:Y_n \rightarrow Z_n$ is epimorphism, so there is a map $p'_n:P_n \rightarrow Y_n$ with $q_n=g_n \circ p'_n$. We hope to change $p'_n$ a little to fit the commutative condition. Note that $g_{n-1}(p_{n-1}\pi_{n}-\epsilon_{n}p_{n})=0$, so $Im(p_{n-1}\pi_n- \epsilon_np_n) \subset ker(g_{n-1})=Im(f_{n-1})$, so there is a $\sigma:P_n \rightarrow X_{n-1}$ such that $f_{n-1}\sigma=p_{n-1}\pi_n-\epsilon_{n}p_n$. Consider $\epsilon_{n-1}d_{n-1}\sigma=p_{n-2}\pi_{n-1}\pi_{n}-\epsilon_{n-1}\epsilon_{n}p_n=0$, we know that $f_{n-2}\delta_{n-1}\sigma=0$, hence $\delta_{n-1}\sigma=0$, so we can take a $\rho:P_n \rightarrow X_n$ such that $\delta_n\rho=\sigma$. Now we take $p_n=p'_n-f_n\rho$. It is easy to check that it satisfies the condition we need. 
We only need the check that $p \sim 0$ iff $q \sim 0$. In fact, the => is clear. Conversely, observe first that since $g_{n+1}$ is an epimorphism, any morphism $P_n \rightarrow Z_{n+1}$ lifts to a morphism $P_n \rightarrow Y_{n+1}$, and thus any homotopy $P \rightarrow Z$ lifts to $P \rightarrow Y$. This means that if $q \sim 0$, then there is some chain map homotopy $p':P \rightarrow Y$ such that $p' \sim 0$ and $g \circ p'=q$, but $p'$ need not to be $p$. It suffices to show that $p-p' \sim 0$. Since $g \circ(p-p')=0$, we mat there for assume $q=0$. Then $g \circ p=q=0$, hence we hace a canonical monomorphism $Im(p) \subset ker(g)=Im(f)$. This implies that there is a chain map $u:P \rightarrow X$ such that $fu=p$. It suffices to show that $u \sim 0$. This is again done inductively. We may assume that we hace $u_i=\delta_{i+1}h_i+h_{i-1}\pi_i$ for all $i<n$. Then we have $\delta_n(u_n-h_{n-1}\pi_n)=0$, as $u$ is a chain map. Again, we get a canonical monomorphism $Im(u_n-h_{n-1}\pi_n) \subset ker(\delta_n)=Im(\delta_{n+1})$. Therefore, as $P_n$ is projective, there is $h_n:P_n \rightarrow X_{n+1}$ such that $\delta_{n+1}h_n=u_n-h_{n-1}\pi_n$ as required. This completes the proof of (1). And the proof of (2) is similar.

**Remark**: This is more or less the fact that $Hom(-,I)$ and $Hom(P,-)$ preserve much of the infomation.

**Definition**:
Let $\mathcal{C}$ be an additive category. The *cone of all complex $(X,\delta)$ over $\mathcal{C}$* is the complex $(C(X),\Delta)$ ocer $\mathcal{C}$ by $C(X)_n=X_{n-1} \oplus X_n$ with differential 
$$\Delta_n= \begin{pmatrix}-\delta_{n-1} &0 \\ id_{X_{n-1}} & \delta_n\end{pmatrix}:X_{n-1} \oplus X_n \longrightarrow X_{n-2} \oplus X_{n-1}$$
for all integers $n$.
In fact, this gives a natural short exact sequence 
$$0 \longrightarrow X \stackrel{i_X}{\longrightarrow} C(X) \stackrel{p_X[1]}{\longrightarrow} X[1] \longrightarrow 0$$
**Definition**:
Let $\mathcal{C}$ be an additive category. A complex $(X,\delta)$ over $\mathcal{C}$ is called *split* if there is a graded endomorphism $s$ of degree 1 of $X$ such that $\delta \circ s \circ \delta=\delta$, or equivalently, if each $\delta_n$ is a split morphism in $\mathcal{C}$. ($s$ need not to be commute with the differentials)

**Proposition**:
Let $A$ be a k-algebra and $X$ a complex of $A$-modules.
1. The complex $X$ is split if $X \simeq Y \oplus H_*(X)$ for some contradictable $Y$, where $H_*(X)$ is considered as a complex with zero differential.
2. The complex $X$ is contradictable if and only if $X$ is split acyclic.
*Proof*:
Denote the differential of $X$ as $\delta$, then using the definition of split, we can find $\delta \circ s \circ \delta=\delta$ and $s \circ \delta \circ s=s$. Note that $ker(\delta) \subseteq ker(s \circ \delta) \subseteq ker(\delta \circ s \circ \delta) =ker(\delta)$ and $X=im(\delta \circ s) \oplus ker(\delta \circ s)=im(s \circ \delta) \oplus ker(s \circ \delta)$, so we have $X=im(s \circ \delta) \oplus ker(\delta)=im(s \circ \delta) \oplus im(\delta) \oplus H$, hance taking $Y=im(s \circ \delta) \oplus im(\delta)$, to proof the first statment, we still need to check that $Y$ is contradictable. In fact, take homotopy to be $s \circ \delta$, then we are done.
For the converse it suffices to note that a contradictable complex $(Y,\epsilon)$ is split acyclic. Indeed, $Y$ is acyclic and if $h$ is a homotopy on $Y$ such that $\epsilon \circ h+h \circ \epsilon =id_Y$, then composing by $\epsilon$ on the right yields $\epsilon \circ h \circ \epsilon=\epsilon$ hence $Y$ is split. 