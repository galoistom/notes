>in the following notes all ring will be assumed to be commutative with unit(unless stated otherwise)

**Definition 1.1**: Let $A$ be a ring, a abilian group $M$ is said to be an $A-module$ if $A$ acts on $M$ linearly (i.e. there is a ring homomorphism $A \rightarrow End(M)$)
**Example**:
1. every abilian group $G$ is naturally a $\mathbb{Z}-module$.
2. Let $A$ be a field, then an $A-module$ is actually an $A-v.s.$
3. Let $G$ be a finite group, and $A=k[G]$ be a group ring, then an $A-module$ is a linear representation of $G$ (c.f. [[Basic Definitions of representation]])
4. $A$ and the ideals of $A$ is also modules of $A$, with the multiplication as the action over it.

**Definition**: Let $Mod_A$ be a category whose elements is the modules of $A$, and morphism is the homomorphism between $M,N$ preserving the module structure.
We have a natural isomorphism $Hom(A,M) \simeq M$ by sending $f \mapsto f(1)$.

**Definition**: Let $N \leq M$ be a sub group of $M$, stable under $A$, then $N$ is called the submodule of $M$, one should note that $M/N$ also inherit the structure of $A-module$.
**Example**: Let $f: M \rightarrow N$ be an homomorphism, then $ker(f),Im(f),coker(f),coIm(f)$ are all $A-module$

Let $f: A \rightarrow B$ be a ring homomorphism, then $B$ is an $A-module$, and $ker(f)$ is an ideal, $Im(f)$ is a $B-submodule$ but not an ideal of $B$.

**Definition**: an $A-module$ M who can be represented by $\sum Ax_i$ with $x_i \in A$, then we say that $(x_i)$ is the set of generator of $M$. Let $N,P \subset M$, let $(N:P):=\{a \in A : aP \subset N\}$ is an ideal. Specifically, $(0,M)$ is called the annihilator $Ann(M)$ of $M$.

**Definition**: a ring is integral domain if it has no zero divsor (i.e. $\not\exists ab=0,a \neq0, b\neq0$), a ring is a field if $1 \neq 0$ and every element is a unit. Let $\mathfrak{p}$ be an ideal, consider $A/\mathfrak{p}$, we say $\mathfrak{p}$ is prime if $A/\mathfrak{p}$ is integral domain, and maximal if there is no bigger nontrivial ideal containing $\mathfrak{p}$, which can also be expressed as $A/\mathfrak{p}$ is a field.

Let A be a ring, we let $spec(A)$ be a topological space with elements $\mathfrak{p}$ and the close sets look like $V(E)=\{\mathfrak{p} \in spec(A):E \subset\mathfrak{p}\}$, for an element $f \in A$, let $V(f)=\{\mathfrak{p} \in spec(A):f \in \mathfrak{p}\}$.
Basic example: let k be an algebraicly closed field, $f \in k[x]$, then for any $\alpha \in k$, $(x-\alpha)$ is a maximum ideal of $k[x]$ and $(x-\alpha)$ is a closed point of $spec(k[x])$ then $f(\alpha)=0$ is equvalient to $(x-\alpha) \in V(f)$.

**Theorem(Hochster)**: let $X$ be a topological space then the TFAE:
1. there is a ring $A$ such that $X \simeq spec(A)$.
2. $X$ is an inverse limit of finite $T_0-spaces$.
3. $X$ is spectrial, i.e. $X$ is quasi compact, has a bisis of quasi-compact open sub sets stable under finite intersections, and every irr closed subsets has a unique generic point(sober)

**Construction 1.14** $f:A \rightarrow B$ is a ring homomorphism. then it defines a map $^af:Spec(B) \rightarrow Spec(A)$ which maps $\mathfrak{q} \mapsto f^{-1}(\mathfrak{q})=\mathfrak{q} \cap A$. It is eqsy to check that it is well defined. One should note that for a maximal $\mathfrak{m} \subset B$ its image $^af(\mathfrak{m})$ is not necessarily maximal.

**Theorem 1.16** Let $A \neq 0$ be a commutative ring, then $A$ has at least one maximal ideal (i.e. $Spec(A)$ is a closed point)
Proof:(applying zorn's lemma) Let $\Sigma:=\{I \subset A: I \neq (1)\}$, ordered by inclusion. since $(0) \in \Sigma$ we have $\Sigma\neq0$. We show: Every chain $(I_\alpha)$ in $\Sigma$ has an upper bound. Indeed, $I= \cup I_\alpha$ is an upper bound. Using zorn's lemma, $\Sigma$ has an maximal element.#
Cor1.18 if $I$ is an ideal of $A$, then there is a maximal ideal ideal $\mathfrak{m}$ s.t. $I \subset \mathfrak{m}$.

**Definition 1.20** If $A$ has exactly one maximal ideal $\mathfrak{m}$, then we call $A$ a local ring. We call $k:=A/\mathfrak{m}$ the residue field of $A$.
Localization $A_{\mathfrak{p}}$ is some how looking at the functions at the small area around the spot $\mathfrak{p}$.

**Prop 1.21** If $\mathfrak{m} \subset A$ is a maximal ideal, such that every $x\in A\backslash \mathfrak{m}$ is a unit, then A is a local ring.
Proof:every ideal $I \neq (1)$ consists only non-units have $I \subset \mathfrak{m}$, hence $\mathfrak{m}$ is the only maximal ideal.#
**Prop 1.22** If $\mathfrak{m} \subset A$ is a maximal ideal such that all elements in $1+\mathfrak{m}$  are units, then $A$ is a local ring
Proof:all we need to show is that elements in $A \backslash\mathfrak{m}$ are units. For $x \in A \backslash\mathfrak{m}$, we have $\mathfrak{m} \subset (x)+\mathfrak{m}$, so there is a $y \in A$ such that $y+tx=1$, thus $xy=1-m$ is a unit, hence $x$ is a unit.

**Ideal's geometrical motive**. let $k$ be a field, and $Y \subset k^n$, then $I(Y)=\{f \in k[x_1,\cdots,x_n]: \forall p\in Y,f(p)=0\}$ is a tipical ideal for $k^n$.
We consider when $I(Y)$ is prime?

**Definition 1.23** Let $n=\{a \in A:\exists n \in \mathbb{N},a^n=0\}$, is called the nilradical of $A$. It is an ideal, specifically the intersection of all prime ideals in $A$. And $R=\bigcap \mathfrak{m}$ the intersection of all maximal ideal, we have $R=\{x \in A: \forall y \in A, 1-xy \text{ is a unit in } A\}$.
Lemma Suppose $f \in A-\mathfrak{m}$ is not a nilpotet, then there is a prime ideal $\mathfrak{p}$ with $f \notin \mathfrak{p}$. Let $\Sigma:=\{\mathfrak{a}:\forall n \in \mathbb{N},f^n \notin \mathfrak{a}\}$. Using Zorn's lemma, take the masimal element $\mathfrak{p}$ of $\Sigma$, it is easy to see that $\mathfrak{p}$ is prime. 

**Definition 1.25** Let $S \subset A$ as a set, with $1\in S$ and $\forall x,y \in S$, we have $xy\in S$, the $S$ is called the multiplicative subset. Let $I$ be a ideal, then radical $\sqrt{I}:=\{a:\exists n\in\mathbb{N},a^n\in I\}$, similiar definition can be used on multiplicative subset.
Lemma: if $S$ is a radical multiplicative subset, and $0 \notin S$, then there is a prime ideal $\mathfrak{p} \cap S=0$.
Motive: We have that $V(I)=V(\sqrt{I})$, so $\sqrt{I}$ is the largest ideal with the close set $V(I)$.

**Definition**: Let $I,J$ be ideals of $A$, and they are relativly prime if $I+J=(1)$.

**Proposition**: 
1. Let $\mathfrak{p}_1,\cdots,\mathfrak{p}_n \in Sepc(A)$, and $I \subseteq \bigcup_i \mathfrak{p}_i$, the there is an $i$ such that $I \subseteq \mathfrak{p}_i$.
2. Let $I_1,\cdots,I_n$ be a set of ideals, and $\mathfrak{p}$ is prime ideal in $A$ with $\bigcap_i I_i \subseteq \mathfrak{p}$, then there is a $I_i \subseteq \mathfrak{p}$. if fact, if $\mathfrak{p}=\bigcap_i I_i$, then there is a $I_i=\mathfrak{p}$.
*Proof*:
We proof by induction on $n$. $n=1$ clear. if $n=2$, observe that there must be $x \in \mathfrak{p}_1-\mathfrak{p}_2,y \in \mathfrak{p}_2-\mathfrak{p}_1$ in $I$, but if we consider $x+y$, we found a contradiction. We extend this method, using the induction hypothesis, we may assume that for every $i$, there is a $x_i \in I \cap \mathfrak{p}_i,x_i \not\in \mathfrak{p}_j$, and now consider $y:=\sum_i\prod\widehat{x_i}$ is in $I$ but not in any of the $\mathfrak{p}_i$.
Similiarly, choosing $x_i \in I_i-\mathfrak{p}$, and let $y:=\prod_ix_i$, giving a contradiction.

**Definition**(extension and contraction): Let $f:A \rightarrow B$ be a ring homomorphism, and $I \subseteq A,J \subseteq B$ be two ideals, then $f(I)$ may not be an ideal, $f^{-1}(J)$ must be an ideal. Let $I^e:=f(I)B$ be de ideal generated by $f(I)$, and $J^c:=f^{-1}(J)$.
*question:* does $I^e$ preserve the property of prime?
In general it is not correct, consider $\mathbb{Z}[\sqrt{-1}]$ as an example: $(2)^e=(1-i)(1+i)$.

**Definition**: Free modules are modules that are isomorphic to $A^I:= \bigoplus_{i \in I} A$. 

**Theorem**(Nakayama Lemma):(c.f.[[Block theory ch1]]])
Let $M$ be a finiely generated A-module, assume $I \subseteq A$, is a ideal, and if $I$ is contained in the jacobradical of $A$, then if $IM=M$, we have $M=0$.

---
# A quick view of homological algebra
**Definition**:A sequence of A-module $\cdots\longrightarrow M_{i-1} \stackrel{f_i}{\longrightarrow} M_i \stackrel{f_{i+1}}{\longrightarrow} M_{i+1} \longrightarrow \cdots$ is called a *chain complex* if $f_{i+1} \circ f_{i}=0$ for all $i$, sepcifically, the complex is called *exact* if $ker(f_{i+1})=im(f_i)$ for all $i$. And define $H_i(M_\cdot)=ker(f_{i+!1})/im(f_i)$ the homology(cohomology) at $i$.

**Definition**:
A *functor* $F:Mod_A \rightarrow Mod_B$ is a function that preserve the multiplication of morphism and send $id$ to $id$. And $F$ is *additive* if $Hom(M,N) \rightarrow Hom(FM,FN)$ is a group homomorphism.
**Example**:
1. $Mod_A \rightarrow Mod_A$ sending $M \mapsto Hom(N,M)$ is covariant, and $M \mapsto Hom(M,N)$ is controvariant.

**Definition**:
$F:Mod_A \rightarrow Mod_B$ is a additive covariant functor.
1. We say that $F$ is *left-exact* if for [[Short exact sequence]] $0 \longrightarrow M \longrightarrow N \longrightarrow R \longrightarrow 0$ we have $0 \longrightarrow FM \longrightarrow FN \longrightarrow FR$ are exact.
2. We say that $F$ is *right-exact* if for [[Short exact sequence]] $0 \longrightarrow M \longrightarrow N \longrightarrow R \longrightarrow 0$ we have $FM \longrightarrow FN \longrightarrow FR \longrightarrow 0$ are exact.
3. We say that $F$ is *exact* if it preserve the exactness of short exat sequence.

**Proposition**(exact test):
In the category $Mod_A$, the comlex $M' \longrightarrow M \longrightarrow M'' \longrightarrow 0$ is exact if for all $N$ the complex $0 \longrightarrow Hom(M',N) \longrightarrow Hom(M,N) \longrightarrow Hom(M'',N)$ is exact.
*Proof*:
$\Rightarrow$: easy.
$\Leftarrow$: Take $N=M''/im(M \rightarrow M'')$, then one can check that this leads to $M'' \rightarrow 0$ is surjective. Taking $N=M/im(M' \rightarrow M)$, then one get $ker(M \rightarrow M'') \subseteq im(M' \rightarrow M)$, hence it is exact at $M$.

**Proposition**:
Let $F$ be left-exact, then there will be a *derived-functor* $R$ such that for any short exact sequence $0 \longrightarrow M \longrightarrow N \longrightarrow R \longrightarrow 0$ we have
$$
0 \longrightarrow FM \longrightarrow FN \longrightarrow FR \longrightarrow R^1FM \longrightarrow R^1FN \longrightarrow R^1FR \longrightarrow R^2FN \longrightarrow \cdots
$$
(Similiar thing is also true for controvariant functor)
**Example**:
Let $Hom(-,N):Mod^{op}_A \rightarrow Mod_A$ be left-exact, define $Ext^i(-,N)=R^iHom(-,N)$, and $Hom(M,-):Mod_A \rightarrow Mod_A$ be right-exact, define $Ext^i(M,-)=R^iHom(M,-)$. One can check that $Ext$ is well-defined, there are also another definition(c.f.[[First extension group]])

**Definition**:
1. If $Hom(P,-)$ is an exact functor then $P$ is projective.
2. If $Hom(-,I)$ is an exact functor then $I$ is injective.
(C.f.[[Projective module and injective module]])

**Theorem**(Snake lemma):
In the category $Mod_A$, the diagram below is exact and commutative,
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
&0 \arrow[r] &M' \arrow[r,"u"] \arrow[d,"f'"] &M \arrow[r,"v"] \arrow[d,"f"] &M'' \arrow[r] \arrow[d,"f''"] &0\\
&0 \arrow[r] &N' \arrow[r,"u'"] &N \arrow[r,"v'"] &N'' \arrow[r] &0
\end{tikzcd}
\end{document}
```
Then the following are exact:
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
&0 \arrow[r] &kerf' \arrow[r,"\overline{u}"] &kerf \arrow[r,"\overline{v}"] &kerf'' \arrow[r,"\delta"] &cokerf' \arrow[r,"\overline{u'}"] &cokerf \arrow[r,"\overline{v'}"] &cokerf'' \arrow[r] &0
\end{tikzcd}
\end{document}
```
*Proof*:
Simple, using the technique of diagram chasing. In fact, the only thing we need to check is those involves $\delta$. The definition of $\delta$ is clear, simply taking an element in $x \in ker(f)$, such that $vy=x$, $y \in M$, then we have $v'fy=f''x=0$, so $fy \in im(u')$, suppose $u'z =fy$. One set $\delta x=z$. It is clear that $\delta$ is well-defined. Using the similiar technique, one can proof the lemma.

**Theorem**(five lemma):
Cosider the following diagram with exact rows:
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
&A \arrow[r] \arrow[d,"f_A"] &B \arrow[r] \arrow[d,"f_B"] &C \arrow[r] \arrow[d,"f_C"] &D \arrow[r] \arrow[d,"f_D"] &E \arrow[d,"f_E"]\\
&A' \arrow[r] &B' \arrow[r] &C' \arrow[r] &D' \arrow[r] &E'
\end{tikzcd}
\end{document}
```
1. If $f_A,f_B,f_D,f_E$ are both isomorphism, then $f_C$ is also isomorphism.
2. If $f_B,f_D$ are injective, $f_A,f_E$ are surjective, then $f_C$ is injective.
3. If $f_B,f_D$ are surjective, $f_A,f_E$ are injective, then $f_C$ is surjective.
*Proof*:
classical exercise for diagram chasing.

---

**Definition**:
A set $S \subseteq A$ is a multiplicative closed subset if $S$ is closed under multiplication and $1 \in S$. And for a multiplicative closed subset $S$, there is a $S^{-1}A$ unique up to isomorphism, such that every element $\frac{a}{s} \in S^{-1}A$ can be chosen $a \in A,s \in S$, and a map $f:A \rightarrow S^{-1}A$ sending $a \mapsto \frac{a}{1}$, such that $\forall g:A \rightarrow B$ a ring homomorphism, there is a unique $h:S^{-1}A \rightarrow B$ such that $hf=g$. And the explicit construction is $A \times S$ quotient out by the equvalient relation:$\frac{a_1}{s_1}=\frac{a_2}{s_2}$, if there is a $s \in S$ such that $s(s_1a_2-s_2a_1)=0$.

Sepcifically, $A_{\mathfrak{p}}=(A-\mathfrak{p})^{-1}A$ is the localization of $\mathfrak{p}$, which is a locla ring, with residue field $A_{\mathfrak{p}}/\mathfrak{p}A_{\mathfrak{p}}$. And if $A$ is integral domain, then $(0) \in Spec(A)$, and $A_{(0)}=(A-(0))^{-1}A$ is the field of fraction of $A$. For $f \in A$, write $A_f=(f)^{-1}A=A[\frac{1}{f}]$ 

One should note that the action of localization is exact so it behave very nicely in most condition. It is also easy to extend the idea to modules of $A$.

**Proposition**:
the map $M \rightarrow \prod_\mathfrak{m} M_\mathfrak{m}$, where $\mathfrak{m}$ runs through the maximal ideals of $A$, is injective.
*Proof*:
Consider $I=Ann(x)$ is a nontrival ideal, then there must be a maximal ideal $\mathfrak{m}$ containing $I$, then consider $M_\mathfrak{m}$, one know that there must be some $y \in A-\mathfrak{m}$ such that $xy=0$, contradiction.

**Proposition**:
There is a bijection between the prime ideals of $S^{-1}A$ and the prime ideals $\mathfrak{p}$ of $A$ such that $\mathfrak{p} \cap S = \varnothing$. Then we know that $S^{-1}\sqrt{I}=\sqrt{S^{-1}I}$ for all ideal $I \subseteq A$.

**Definition**:
Let $M,N \in Mod_A$, a map $f:M \times N \rightarrow T$ is bilinear if $f(x,-):N \rightarrow T$ and $f(-,y):M \rightarrow T$ are all linear. The tensor product $M \otimes_A N$ is the pair $(T, \rho)$, where $\rho:M \times N \rightarrow T$ is bilinear, such that for all $f: M \times N \rightarrow T'$ is bilinear there is a unique $\bar{f}:T \rightarrow T'$ such that $\rho(\bar{f})=f$.
The uniqueness and existence is clear.

Note: Tensor product does note preserve exactness, but is right exact. example: $0 \longrightarrow \mathbb{Z} \longrightarrow \mathbb{Z} \longrightarrow \mathbb{Z}/2\mathbb{Z} \longrightarrow 0$, when tensored with $\mathbb{Z}/2\mathbb{Z}$, it is nolonger injective.

**Proposition**:
Let $A$ be a ring, and $S$ a multiplicative subset, then there is a canonical isomorphism $S^{-1}M \otimes_{S^{-1}A}S^{-1}N \simeq S^{-1}(M \otimes N)$, where $M,M \in Mod_A$.
And $Hom(M \otimes_A N,P) \simeq Hom(M,Hom(N,P))$. $S^{-1}A \otimes_A M \simeq S^{-1}M$.

**Definition**:
If $- \otimes N$ is exact, then we say that $N$ is flat. It is equvalient to $M' \longrightarrow M$ injective, with $M',M$ finitely gengerated $\Rightarrow$ $f \otimes 1$ is injective.

**Flatness is a local property**