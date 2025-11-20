---
updated_at: 2025-10-23T15:15:43.233+08:00
edited_seconds: 140
---
#algebra #lectureNote 

why group/ring/fields?
- Describe symmetry uniformly
- Compose subsymmetry in different context (e.g. 正二十面体 vs symmetry group of roots of 五次方程) and extract the key(fundmantal) property of the objects we are studying. 

**Example**: 
- the equation $x^{2}-Dy^{2}=1$, $D$ square free >1. The solution is of the form $\pm(x_{0}+y_{0}\sqrt{ D })^{N}$. 
- Elliphc curve $F:=\{ (x,y) : y^{2} = x^{3} - Dx \} \cup \{ \infty \}$. Define $A,B,C \in F$ have the property $A+B+C=0$ if $A,B,C$ share a line (the group is indeed abelian). 

---
# Group,example and isomorphism
**Definition**: A group is a pair of $(G,*)$, where $G$ is a nonempty set and $*$ a binary operation $G\times G \rightarrow G$ such that $(a*b)*c=a*(b*c)$, and there is a $1_{G}$ (the identity) s.t. $1_{G}*a=a*1_{G}$, and there is always an $a^{-1} \in G$ s.t. $a*a^{-1}=a^{-1}*a=1_{G}$. (also see in [[高等代数2 note]]). A group is alled **abelian** if $a*b=b*a$ for all $a,b \in G$. 

Given a group $(G,*)$ and $(H,\circ)$ be two groups, define $\times:(G\times H)\times(G\times H)\rightarrow G\times H$ with $(g,h)\times(g',h')=(g*g',h\circ h')$ to be the **direct product** of groups. 

**Important application**: the Dihedral groups $D_{2n}$. The usual definition is the group of a regular $n$-gon. (In particular, $\langle s,t \rangle / \langle s^{2}=1, t^{n}=1, sts=t^{-1} \rangle$ or $\langle s,t | s^{2}=1, t^{n}=1, sts=t^{-1} \rangle$ in short). 

**Definition**: Let $S=\{ s_{1}, s_{2} , \cdots \}$ be a subset of $G$, such that $g \in G$ can always be written in the form of $\prod s$ where $s \in S \cup S^{-1}$. If elements in $S$ have some relations then we can write it in the from $G=\langle S|R_{1}, R_{2} \rangle$. 

**Definition**: Let $\Omega$ be a set, then $S_{\Omega}:=\{ bijection\ \sigma:\Omega\rightarrow\Omega \}$ forms a group with multiplication the composition of maps. For example, consider $S_{7}$, and 
$$
\sigma = \begin{pmatrix}
1&2&3&4&5&6&7 \\
7&5&1&3&2&6&4
\end{pmatrix}
$$
, can also be written as $\sigma=(1\,7\,4\,3)(2\,5)$, where $(1\,7\,4\,3)$ is a cycle. 

**Definition**: Group Isomorphism (see also in [[高等代数2 note]]). $G$ and $H$ be two groups, and $\phi:G\rightarrow H$ be a map sending $1_{G}\mapsto1_{H}$ and $\phi(ab)=\phi(a)\phi(b)$. In fact, we usually consider groups that are isomorphic is the same. 

**Definition**: Let $H$ be a subset of $G$, we say $H$ is a **subgroup** of $G$ (denoted by $H\leq G$) if $1_{G} \in H$, and $*$ is closed under with inverse $H$ (in fact one only need to check $ab^{-1} \in H$). 

**Definition**: Define the order of $x \in G$, denoted by $\lvert x \rvert = \lvert \langle x \rangle \rvert$. 

# 2 Cosets, Langurange theorem, quotient
**Definition**: $H<G$ be a subgroup, a **left coset** is a subset of $G$ of the form $gH:=\{ gh:h \in H \}$, $g \in G$. (similar for right coset), in particular, we say $g$ is the **representative** of the coset. In the future, we use coset to denote the right coset by the abuse of notion. 

**Proposition**: Two left cosets $g_{1}H$ and $g_{2}H$ are either the same or disjoint. (trivial)

**Definition**: $H<G$, subgroup, define **left quitient** $G/H:=\{ gH:g \in G \}$. Right quotient can also be defined similiarly.

**Theorem**(Langurange): If $H<G$, finite group, then $\lvert H \rvert$ divides $\lvert G \rvert$. 

*Proof*: $G=\bigsqcup_{g \in G / H}gH$. Note that $H$ and $gH$ has a natural bijction $g,\,g^{-1}$, so $\lvert H \rvert=\lvert gH \rvert$. In particular, $\lvert G \rvert=\lvert H \rvert\cdot \lvert G / H \rvert$. 

**Corollary**: 
1. If $G$ is finite, $g \in G$, then $\lvert g \rvert$ devides $\lvert G \rvert$.
2. $g^{\lvert G \rvert}=1_{G}$.

**Remark**: Let $n,a \in \mathbb{N}$. Eula function $\phi(n):=\lvert (\mathbb{Z} / n\mathbb{Z})^{\times} \rvert$, then if $gcd(a,n)=1$, we have $a^{\phi(n)}\equiv1\pmod{n}$. In particular, if $n$ is prime, then $\phi(n)=n-1$, and we get the Femart's little theorem. The proof is similar to the theorem above, in fact, if you see $G=(\mathbb{Z} / n \mathbb{Z})^{\times}$ as a group, then the order of $a \in G$ must be a divisor of $\phi(n)=\lvert G \rvert$. 

**Theorem**: If $G$ finite of order $p$, where $p$ prime, then $G$ is cyclic. 

*Proof*: Take $g \in G - \{ 1_{G} \}$, then $\lvert g \rvert\neq1$, hence $\lvert g \rvert=p$. Take $\langle g \rangle\leq G$, we have $G\simeq C_{p}$ cyclic. 

**Definition**: 
1. $a,g \in G$, call $gag^{-1}$ the **conjugate** of $a$ by $g$. 
2. $H<G$ subgroup, $gHg^{-1}=\{ ghg^{-1}:h \in H \}$ is the conjugate of $H$ by $g$. One immediately notice that $gHg^{-1}$ is a subgroup of $H$ too. 
3. $H<G$ is **normal** if $H=gHg^{-1}$ for all $g \in G$. In particular, if $G$ is abelian, then all subgroups are normal.

**Notion**: $H<G$ or $H\leq G$ denote $H$ is the subgroup of $G$. $H\triangleleft G$ or $H\trianglelefteq G$ is denote $H$ is the normal subgroup of $G$. 

**Definition**: Now we are ready to define the group structure of $G / H$. What we need is multiplication, we hope that $abH=aH\cdot bH = ab(b^{-1}Hb)\cdot H$, so we want $b^{-1}Hb=H$, which is percisly the property of normal subgroup $H \triangleleft G$. Written formally, the multiplication is as above, and the identity $1_{G /H}$ is $1_{G}H$, and $(gH)^{-1}=g^{-1}H$. 

**Lemma**: $H,K$ subgroups of $G$. 
1. If $K$ normal, then $HK=KH=\{ kh:k\in K,\,h\in H \}$, is as subgroup of $G$.
2. If $H,K$ both normal, then $HK=KH$ normal. 

# Group homomorphism(同态)
>[!note] Homomorphism 
>**Definition**: $G,H$ groups, a map $\phi:G\rightarrow H$ is a **homomorphism** if:
>1. $\phi(xy)=\phi(x)\phi(y)$, for all $x,y\in G$. ($\phi$ is multiplicative)
>2. $\phi(1_{G})=1_{H}$. Though not necessary

Isomorphism = bijection + homomorphism

**Example**: $H \triangleleft G$, then $G\rightarrow G/H$ is homomorphism (c.f. [[高等代数2 note]]). In particular, $\mathbb{Z}\rightarrow C_{n}$ is a surjective homomorphism, as $C_{n}\simeq \mathbb{Z} / n\mathbb{Z}$. 

**Lemma**: $\phi:G\rightarrow H$, $\psi:H\rightarrow K$, then $\psi \circ \psi:G\rightarrow K$ is also a homomorphism. 

**Lemma**: $\phi:G\rightarrow H$ a homomorphism, then $\phi(G)$ and $ker(\phi):=\phi ^{-1}(1_{H})=\{ g\in G:\phi(g)=1_{H} \}$ are subgroup of $H$ and $G$ (ni fact, these subgroups are all normal). Moreover, $\phi ^{-1}(h)$ is a coset of $ker$ on $G$. 

# Isomorphism Theorem, composition series, Hölder theorem
**Theorem** 1: $\phi :G\rightarrow H$ homomorphism. Then $ker(\phi)\triangleleft G$, and $G / ker(\phi)\simeq \phi(G)$. 

*Proof*: Define a map $\psi:G /ker(\psi)\rightarrow \phi(G)$, $g\cdot ker(\phi)\mapsto \phi(g)$. We first check $\psi$ is well defined: In fact, if $g,g'$ are in the same coset, suppose $g'=gk$, $k\in ker(\phi)$, then $\phi(g')=\phi(g)\cdot \phi(k)=\phi(g)$. It is also clear that it is indeed a homomorphism.
One immediately note that $\psi$ is surjective, so we only have to check that it is injective. In fact, $\psi(g\cdot ker(\phi))=1_{H}$ if and only if $g\in ker(\phi)$, i.e. $g\cdot ker(\phi)=ker(\phi)$. 

**Theorem** 2: $A<G$, $B\triangleleft G$. Then $AB<G$, $B\triangleleft AB$, $A\cap B\triangleleft A$, and $(AB) / B\simeq A/(A\cap B)$. 

*Proof*: Normal is easy to check. Consider $A\rightarrow AB\rightarrow(AB) / B$, $a\in A$ is in the kernel is when $a \in B$ is in $B$ as well, i.e. $a\in A\cap B$, and use the theorem 1.

**Theorem** 3: $H\triangleleft K\triangleleft G$. Then $K / H \triangleleft G /H$, and $(G / H)/(K / H)\simeq G / K$. 

*Proof*: Consider $G / H\rightarrow G / K$, $gH\mapsto gK$, we need to check it has kernel $K / H$. As if $gH$ s.t. $gK=K$, then $g\in K$, so $ker=\{ gH:g\in K \}=K / H$. 

**Theorem** 4: $N\triangleleft G$ normal, then there is a bijection {subgroups of $G$ containing $N$} <--> {subgroups of $G / N$}, with $A\mapsto A / N$ and $\overline{A}\mapsto \pi ^{-1}(\overline{A})$, where $\pi:G\rightarrow G / N$ is the quotient map. In fact, the bijection preserves intersection, index, normal, quotient.

**Definition**: A group $G$ is **simple** if it has no nontrivial normal subgroup. This definition is important because we can some how split the question into two part, first split $G$ intn parts of simple groups, and glue then together into $G$. 

>[!note] Hölder's program
>Classify all finite groups. (People have already solve the case of simple groups)

## composition series
**Definition**: In a group $G$, a sequence of subgroups
$$
\{ 1_{G} \} = N_{0} \triangleleft N_{1} \triangleleft \cdots \triangleleft N_{k}=G
$$
is a **composition series** if $N_{i} / N_{i-1}$ is simple. In fact, the $\{ N_{i} / N_{i-1} \}$ is called the **composition factors**. 

**Theorem**(Jordan-Hölder): $G$ a finite group, then:
1. $G$ has a composition series
2. The composition serires factors are unique up to permutation. 

*Proof*: 
1. IF $G$ simple, done; if $G$ not simple, then $G$ has a normal subgroup $H\neq \{ 1_{G} \},G$, consider $\{ 1_{G} \}\triangleleft H \triangleleft G$, and use induction, and consider finite group $H$ and $G /H$, then (with the help of the isomorphism theorem 4) we are able to fill up the space on both side. 
2. Induction on $\lvert G \rvert$. Consider 
$$
\begin{align} 
\{ 1_{G} \}\triangleleft A_{1} \triangleleft A_{2}\triangleleft \cdots \triangleleft A_{m-1} \triangleleft G  \\
\{ 1_{G} \}\triangleleft B_{1} \triangleleft B_{2}\triangleleft \cdots \triangleleft B_{n-1} \triangleleft G
\end{align}
$$ 
then if $A_{m-1}=B_{n-1}$, use induction; if $A_{m-1}\neq B_{n-1}$, then notice $A\triangleleft AB\triangleleft G$, so we must have $AB=G$. Now we change it to $1\triangleleft(A\cap B)\triangleleft A\triangleleft AB=G$ and $1\triangleleft(A\cap B)\triangleleft B\triangleleft AB=G$, and use induction to fill up $1\triangleleft(A\cap B)$, then we have $G / A=AB / A\simeq B / (A\cap B)$, $G / B = AB /B\simeq A /(A\cap B)$. 

**Definition**: A group $G$ is **solvable** if $\exists$ a chain of subgroups 
$$
\{ 1_{G} \}=G_{0}\triangleleft G_{1}\triangleleft \cdots \triangleleft G_{s} = G
$$
such that $G_{i} / G_{i-1}$ is **abelian**. In fact, $G$ is solvable if and only if all composition factors of $G$ are isomorphic to $\mathbb{Z} / p\mathbb{Z}$ for some prime $p$. (Take a chain above, then fill up $G_{i-1}\triangleleft G_{i}$ with their decomposition series, as they are abelian, so all its factors must be $\mathbb{Z} / p\mathbb{Z}$). 

# alternating group
$S_{n}$ symmctric group of $n$ elements $\{ 1,2,\cdots,n \}$. Our goal is to introduce a subgroup $A_{n}\triangleleft S_{n}$, normal of index 2. 

**Definition**: 
1. In $S_{n}$, for distinct $a_{1},\dots,a_{m}\in \{ 1,2,\dots,n \}$ the $m$-cycle $\sigma=(a_{1}a_{2}\cdots a_{m})$ sending $a_{i}\mapsto a_{i+1}$. In fact, all $\sigma \in S_{n}$ can be decomposed into disjoint union of cycles.
2. A 2-cycle $(ab)$ is called a **transposition**. One can easily decompose cycles into transposition. 
3. $\forall\sigma \in S_{n}$, $\sigma(a_{1}a_{2}\cdots a_{m})\sigma^{-1}=(\sigma(a_{1})\sigma(a_{2})\cdots\sigma(a_{m}))$. 

**Definition**: $\forall\sigma \in G$, define
$$
sgn(\sigma)=\frac{\prod_{1\leq i<j\leq n}(x_{i}-x_{j})}{\prod_{1\leq i<j\leq n}(x_{i}-x_{j})} \in \{ \pm1 \}
$$
where $x_{i}$ are indefinite, this defines a sign of $\sigma$. Now let $A_{n}=\ker(sgn)$. 

**Theorem**: if $n\geq 5$, then $A_{n}$ is simple.

**Idea**: 
1. $A_{n}$ is gen by all 3-cycles
2. If $N\triangleleft A_{n}$ contains a 3-cycles, then is contains all 3-cycles
3. Proof $N$ contians all 3-cycles.

# Direct product
**Definition**: Let $G_{i}$ ($i\in I$) be a set of groups, the direct product of $\{ G_{i} \}$ is $\prod_{i\in I}G_{i}$, with product $(g_{i})_{i\in I}\cdot(g'_{i})_{i\in I}=(g_{i}g'_{i})_{i\in I}$. 

**Theorem**: (a corollary of the one in [[高等代数2 note]])
Any finitly generated abelian group $G$ is of the form 
$$
G\simeq \mathbb{Z}^{r}\times(\mathbb{Z} / n_{1}\mathbb{Z}) \times \cdots \times (\mathbb{Z} / n_{s}\mathbb{Z})
$$
with $r\geq0$ and $2\leq n_{1}|n_{2}|\cdots|n_{s}$, moreover they are unique.

**Remark**: we can see the direct product as the unique (up to isomorphism) $G$ (together wit $G_{i}\rightarrow G$) such that if there is a $H$ with $G_{i}\rightarrow H$, then there is a unique map $G\rightarrow H$ making the diagram commute. 

**lemma**: If $m,n\in \mathbb{Z}$, $gcd(m,n)=1$, then $\mathbb{Z} / mn\mathbb{Z}\simeq \mathbb{Z} / m\mathbb{Z}\times \mathbb{Z} / n\mathbb{Z}$. 

*Proof*: Chinese Remainder theorem. 

**Theorem**: (criterion of direct product) $G$ group, $H,K$ subgroup of $G$ s.t. $H,K$ normal and $H\cap K=\{ 1_{G} \}$, then $HK\simeq H\times K$. 

*Proof*: We first check that $hk=kh$ for all $h\in H,k \in K$, in fact, $hkh^{-1}k^{-1}=(hkh^{-1})k^{-1}=h(kh^{-1}k^{-1})\in H\cap K=\{ 1_{G} \}$. Now set $f:H\times K\rightarrow HK\subset G$ to be $(h,k)\mapsto hk$, as $H,K$ commute, one immediately know that $f$ is a homomorphism. One may also check that $f$ is injective and surjective.

# Group action
see also in [[高等代数2 note]]

**Definition**: Let $G$ be a group, $X$ a set, A **left $G$ action** on $X$ is a homomorphism $\rho :G\rightarrow S_{X}$, where $S_{X}$ is the group of permutation of $X$. 

**Example**: 
1. $S_{n}$ acting on $\{ 1,\dots,n \}$.
2. $GL_{n}(\mathbb{C})$ acting on $\mathbb{C}^{n}$.
3. $G$ acting on $G$ by left multiplication $x\mapsto gx$, right reanslation $x\mapsto xg^{-1}$ and conjugation $x\mapsto gxg^{-1}$. 

**Definition**:
1. The action is called **faithful** if $ker(\rho)=\{ 1_{G} \}$.
2. The action is trivial if $Im(\rho)=\{ id \}$. 

**Theorem**: Every group is isomorphic to a subgroup of a permutation group. In particular, if $\lvert G \rvert=n<\infty$, then $G<S_{n}$. 

## Semidirect product
motive: take $N\triangleleft G$, and $H<G$, with $N\cap H=\{ e \}$, then $NH$ is a subgroup of $G$.

**Definition**: Let $H,N$ be groups, $\phi:H\rightarrow Aut(N)$ be homomorphism, then $N\rtimes_{\phi}H$ be the **semidirect product** related to $\phi$. In fact, as a set, it is just $N\times H$ as set, and the multiplication is $(n_{1},h_{1})\cdot(n_{2},h_{2})=(n_{1}\phi(h_{1})(n_{2}),h_{1}h_{2})$. (One check that this is indeed a group). One can see it as $G$ such that 
$$
1\longrightarrow H \longrightarrow G \longrightarrow N \longrightarrow1
$$

For example $D_{2m}=\mathbb{Z} / m\mathbb{Z} \rtimes \mathbb{Z} / 2\mathbb{Z}$. 

---
# Stabilizers, orbits, class equations
**Definition**:
1. $\forall x \in X$, the **stabilizer subgroup** of $x$ is $Stab_{G}(x):=\{ g \in G: gx=x \}$. 
2. $\forall x \in X$, the **orbit** of $x$ is $Orb_{G}(x):=\{ gx:g \in G \}$. In particular, we write $G \backslash X$ is the set of orbits, i.e. $\{ Gx:x \in X \}$. 

**Proposition**: 
1. $Stab_{G}(x)$ is a subgroup of $G$. 
2. $\forall x,y \in X$, either $Orb_{G}(x)=Orb_{G}(y)$, or $Orb_{G}(x)\cap Orb_{G}(y)=\varnothing$. As a consequence, $X=\bigsqcup Orb$. 
3. If $y=g\cdot x$, then $Stab_{G}(y)=g\cdot Stab_{G}(x)\cdot g^{-1}$. 

**Definition**: $G$ a group on itself by conjugation, $\forall g \in G$, $Ad_{g}:G\rightarrow G$ by $Ad_{g}(x)=gxg^{-1}$.
1. Two elements $a,b \in G$ are **conjugate** if they lie in the same orbit under the conjugation, i.e. $\exists g \in G$ s.t. $b=gag^{-1}$. 
2. An **orbit** is called a **conjugacy class** of $G$. (which will become very usefull in [[Basic Definitions of representation]]). 

**Example**: In $S_{n}$, we have that $\sigma_{1},\sigma_{2}$ are in the same conjugacy class if and only if they have the same Young diamgra (c.f. [[representation of symmetric group]])

**Definition**: $H<G$, subgroup, $S\subseteq G$.
1. The **Centralizer** of $S$ in $G$ $C_G(S)=\{ g\in G:gxg^{-1}=x,\forall x \in S$.
2. The **center** of $G$, $Z(G):=\{ g\in G:ghg^{-1},\forall h \in G \}$
3. The **normalizer** of $H$ in $G$ is $N_{G}(H)=\{ g \in G : gHg^{-1}=H\}$. 

**Definition**: $G$ acts on $X$ and $Y$. Say map $\phi:X\rightarrow Y$ is **equivariant** if $\phi \circ g=g\circ\phi$. 

**Definition**: The action on $X$ is called **transitive** if $\forall x,y \in X$, $\exists g \in G$ s.t. $y=gx$. 

**Theorem**: $G$ finite group (actin on itself by conjugation)
1. $\forall g\in G$, $\lvert G \rvert / \lvert C_{G}(g) \rvert=[G:C_{G}(g)]$. 
2. (classequation) If $g_{1},\dots,g_{r}$ are representation of conjugacy classes of $G$ not contained in $Z(G)$, then 
$$
\lvert G \rvert = \lvert Z(G) \rvert + \sum_{i=1}^{r}[G:C_{G}(g_{i})] 
$$

**Definition**: $p$ prime, say $G$ is a **$p$-group**  if $\lvert G \rvert=p^{n}$ for some $n\geq0$. 

**Proposition**: If $G$ is a nontrivial $p$-group, then the center $Z(G)$ is nontrivial. In fact if $\lvert G \rvert=p^{2}$, then $G$ is abelian.

# Automorphism
One notice that $G / Z(G) \simeq Ad(G) \hookrightarrow Aut(G)$. Then we define $Inn(G)=Ad(G)$, and $Out(G)=Aut(G) / Inn(G)$. 

# Sylow's Theorem
**Definition**: ($p$ prime)
1. A **$p$-group** is a finite group of order equal to a power of $p$. 
2. If $G$ finite group of order $|G|=p^{r}m$ then a subgroup $H$ of $G$ of order $p^{r}$ is called a **Sylow $p$-subgroup** of $G$. 
3. Denote $Syl_{p}(G)=\{ \text{Sylow p-subgroup of G} \}$, $n_{p}=\lvert Syl_{p} \rvert$. 

**Theorem**: $G$ finite group $\lvert G \rvert=p^{r}m$, $r>0$, then:
1. (First Sylow Theorem) Sylow $p$-subgroup exists.
2. (Second) If $P,Q$ $p$-subgroups of $G$, and $P$ is a $p$-sylow, then $\exists g \in G$ s.t. $Q\leq gPg^{-1}$. In other words, we have all Sylow $p$-subgroup are conjugate and any $p$-group is contained in a sylow $p$-subgroup. 
3. (Third) $n_{p}=\lvert Syl_{p}(G) \rvert$ satisfies $\begin{cases}n_{p}\equiv1\pmod{p}\\ n_{p}|m\end{cases}$ (We say that a sylow $p$-subgroup of $G$ is **normal** iff $n_{p}=1$). 

*Proof*:
1. Recall $Z(G)$ center of $G$. If $p| \,\lvert Z(G) \rvert$m then by ther structure of finite generated abelian group, $Z(G)$ has a unique sylow $p$-subgroup $W$, congider $G / W$ and use induction. In not, consider $G$ acting on $G$ by conjugation, we know that $\lvert G \rvert=\sum_{O}\lvert O \rvert=\lvert Z(G) \rvert+\sum_{i=1}^{s} \frac{\lvert G \rvert}{|Stab_{G}(x)|}$, as $p$ is not a dividsor of $\lvert Z(G) \rvert$, so there must be a $x$ such that $v_{p}(\lvert G \rvert)=v_{p}(\lvert Stab_{G}(x) \rvert)$ and use induction. 
2. Consider $Q$ acting on $G / P$ by left multiplication. Then we have $\lvert G / P \rvert=\sum_{g_{i}P}orb_{Q}(g_{i}P)=\sum_{g_{i}P} \frac{\lvert Q \rvert}{\lvert Stab_{Q}(g_{i},P) \rvert}$, as $Stab_{Q}(g_{i}P)=\{ q \in G:q \in g_{i}Pg_{i}^{-1} \}=Q\cap(g_{i}Pg_{i}^{-1})$. As left is not a multiple of $p$, so there must be a 1 on the right side, hance $Q=gPg^{-1}$ for some $g$. 
3. Consider action $G$ on $Syl_{p}(G)$ by $P\mapsto gPg^{-1}$, then $n_{p}= \frac{\lvert G \rvert}{Stab_{G}(P)}$, so $n_{p}|m$. Consider the conjugate $P$ acting on $Syl_{p}(G)$. Then $\lvert Syl_{p} \rvert=\sum_{P_{i}}\lvert Orb_{P}(P_{i}) \rvert = \sum_{P_{i}} \frac{\lvert P \rvert}{Stab_{P}(P_{i})}$, if there is a $P_i$ such that $Stab_{P}(P_{i})=P$. Then $P\leq N_{G}(P_{i})\leq G$, so $P_{i}=P$, hence $n_{p}\equiv1\pmod{p}$. 

# Commutator subgroups, nilpotent group, $p$-groups
**Definition**: $G$ groups
1. $x,y \in G$, define **commutator** $[xy]=x^{-1}y^{-1}xy \in G$. 
2. If $H_{1},\ H_{2} \in G$, define $[H_{1},H_{2}]$ be the subgroup generated by $[x_{1}x_{2}]$, $x_{1} \in H_{1},\ x_{2}\in H_{2}$. 
3. The **Drived subgroup (or commutator subgroup)** of $G$ is $G^{der}=G'=[G,G]$. 

**Fact**:
1. $xy=yx$ $\Longleftrightarrow$ $[xy]=1_{G}$.
2. $g[xy]g^{-1}=[gxg^{-1},gyg^{-1}]$ so $G^{der}$ is normal in $G$.
3. $G / G^{der}$ is **abelian**, denote it as $G^{ab}$.
4. In fact, for all $A$ abelian, $G\rightarrow A$, then there is a unique $G^{ab}\rightarrow A$ such that $G\rightarrow G^{ab}\rightarrow A$ commute. (this is the so called "universal property"). 

**Definition**: $G$ group, define $G^{(0)}=G$, $G^{(i+1)}=[G^{(i)},G^{(i)}]$. Then $G=G^{(0)}\geq G^{(1)}\geq G^{(2)}\geq\cdots$ is called the **derived seires** for $G$.

**Example**: 
$$
G=\begin{pmatrix}
\mathbb{C}^{\times}&\mathbb{C}& \mathbb{C} \\
0& \mathbb{C}^{\times} &\mathbb{C} \\
0 &0 &\mathbb{C}^{\times}
\end{pmatrix}\ <\  GL_{3}(\mathbb{C})
$$
then we have 
$$
G^{(3)} = \{ 1 \} \ <\ 
G^{(2)} = \begin{pmatrix}
1 & 0 & \mathbb{C} \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix} \ < \ 
G^{(1)}=\begin{pmatrix}
1 &\mathbb{C} &\mathbb{C} \\
0 & 1& \mathbb{C} \\
0 & 0 & 1
\end{pmatrix}\ <\ G
$$

**Proposition**: $G$ is solvable iff $G^{(n)}=\{ 1 \}$ for some finite $n\geq1$. 

*Proof*: 
1. "$\impliedby$", clear, as $G^{(i)}\triangleright G^{(i+1)}$ and $G^{(i)} / G^{(i+1)}$ is abelian.
2. "$\implies$", notice that $G / H_{1}$ is abelian, so $G^{(1)}\leq H_{1}$, similiarly, we have $H_{2}\geq [H_{1},H_{1}]\geq[G^{(1)},G^{(1)}]=G^{(2)}$. 

**Definition**: $G$ a group, $G^{0}=G$, $G^{1}=[G,G]$, $G^{i+1}=[G,G^{i}]$. One immediately notice that $G=G^{0}\geq G^{1}\geq G^{2}\geq\cdots$, is called the **Central series** of $G$. One say that $G$ is nilpotent if $G^{n}=\{ 1 \}$ for some $n$. 

**Definition**: $G$ group, $Z_{0}(G)=\{ 1 \}$, for $i\geq1$ , define $Z_{i+1}(G)$ to be the inverse image of $Z(G / Z_{i}(G))$ in $G$. The chain $\{ 1 \} = Z_{0}(G)\leq Z_{1}(G)\leq\cdots$ is called the **upper central series** of $G$.

## Structure theorem of nilpotent groups
**Proposition**: All $p$-groups are nilpotent

*Proof*:
$G$ a $p$-group $\implies$ $Z(G)\neq\{ 1 \}$.

**Proposition**: Let $P$ be a $p$-group
1. $Z(P)\neq \{ 1 \}$.
2. If $H\trianglelefteq P$ nontrivial normal, then $H\cap Z(P)\neq \{ 1 \}$.
3. If $H<P$, then $H<N_{P}(H)$. 

*Proof*: 
1. Clear.
2. Consider the conjugate action of $P$ on $H$. Count $\#H$ by orbits, repeat the proof of 1.
3. If $Z(G)\not\subseteq H$, done as $Z(P)\subseteq N_{G}(H)$. If $Z(P)\subseteq H$, take quotient $\overline{H}=H / Z(P)$, $\overline{P} = P / Z(P)$. By induction, the result holds for $(\overline{H},\overline{P})$ then it holds for $(H,P)$. 

In fact, if $H<P$ with index $p$, then $H\triangleleft P$. 

**Theorem**: $\lvert G \rvert=n=p_{1}^{\alpha_{1}}\cdots p_{r}^{\alpha_{r}}$, $P_{i}\in Syl_{p_{i}}(G)$. Then TFAF:
1. $G$ is nilpotent.
2. $\forall H<G$, $H<N_{G}(H)$. 
3. All Sylow subgroups $P_{i}$ are normal.
4. $G\simeq P_{1}\times\cdots\times P_{r}$. 

**Theorem**:(Schur-Zassenhaus)
$G$ a finite group, $N\triangleleft G$ normal s.t. $gcd(\lvert G \rvert,\lvert G / N \rvert)=1$. $\pi:G\rightarrow G / N$ a quotient map.
1. Then there exist a subgroup $H\leq G$ s.t. $\pi|_{H}:H\rightarrow G / N$ is isomorphism. Therefore, $G\simeq N \rtimes(G / N)$.
2. If $N$ or $G / N$ are solvable, then 

---
# Ring, ideals, quotient rings
**Definition**: A **ring** is a set with two binary operations: addition $+$ and multiplication $\cdot$ such that:
1. $(R,+)$ is an **abelian group,** with unit $0$ and inverse is $-$.
2. $\cdot$ is **asscoiative**, i.e. $a\cdot b\cdot c=a\cdot(b\cdot c)$. 
3. The operation is **asscoiative** $(a+b)\cdot c=a\cdot c+b\cdot c$ and $a\cdot(b+c)=a\cdot b+a\cdot c$. 
4. $R$ is **unital**, i.e. the multiplication has a unit $1 \in R$, s.t. $1\cdot a=a\cdot1=a$ forall $a \in R$. Generally, we suppose $1\neq0$. 

We say that $R$ is commutative iff $\cdot$ is commutative ($a\cdot b=b\cdot a$). 

**Definition**: 
1. A ring is called a division ring or a skew field (除环/体/斜域) if there is an inverse for all nonzero element in $R$. 
2. A **field** is a commutative dividsion ring.

**Example**: 
1. $\mathbb{Z}$ is clearly a ring.
2. $\mathbb{Q}$, $\mathbb{R}$, $\mathbb{C}$ are fields, $\mathbb{H}$ (c.f. [[高等代数2 note]]) is a dividsion ring.
3. $\mathbb{Z}\left[ \frac{1}{N} \right]:=\left\{  \frac{a}{N^{r}}: a \in Z\ r \in \mathbb{Z}_{\geq}  \right\}$ a subring of $\mathbb{Q}$, in fact, this is a localization of $\mathbb{Z}$. 
4. $R$ a ring, then $R[x]:=\left\{  \sum_{i=0}^{n}a_{i}x^{i}:n \in \mathbb{N}, a_{i}\in R  \right\}$ is also a ring. The polynomial ring can be extended to multiple variabels. 
5. $R$ a ring, then $M_{n}(R)$ is also a ring. 
6. Group ring (c.f.[[Basic Definitions of representation]]), let $R$ be a commutative ring, $G$ be a group, then $R[G]=\{ \sum_{g \in G}a_{g}g: \text{finite sum}, \ a_{g}\in R \}$, with regular addition and multiplication ($\left( \sum_{g}a_{g}g \right)\cdot\left( \sum_{g}b_{g}g \right)=\sum_{g,h}a_{g}b_{h}gh$). One immediately notice that $1_{R[G]}=1_{R}\cdot1_{G}$. 

**Definition**: $R,S$ rings
1. A map $R\rightarrow S$ is called **ring homomorphism** if it keep addition and multiplication as well as $1_{R}\mapsto1_{S}$. 
2. An **isomorphism** is a bijective homomorphism.
3. For a homomorphism $\phi:R\rightarrow S$ $ker\phi=\phi ^{-1}(0):=\{ a\in R:\phi(a)=0 \}$.

**Definition**: $R$ a ring.
1. A **zero dividsor** is a nonzero $a \in R$, s,t, $ab=0$ or $ba=0$ for some nonzero $b \in R$.
2. $A$ **unit** is an element $u \in R^{\times}$. 
3. $R$ is called an **integal domain** iff it has no zero dividsor. In fact, integal domain has cancellation law.

**lemma**: a finite integal domain is a field

*Proof*: Consider the map $a:R\rightarrow R$, $x\mapsto ax$, is bijective. 

**Definition**: $R$ a integal domain. The **field for fraction** is somehow "adding" inverse to $R$. Formally, it is $R\times R / \sim$, where $(a,b)\sim(c,d)$ iff $ad=bc$ (take it as $\frac{a}{b}=\frac{c}{d}$). Addition is then $(ad+bc,db)$, multiplication is $(ac,bd)$, and unit is $(1,1)$. We will denote it as $Frac(R)$. It is in fact a field which injective ring homomorphism $R \hookrightarrow Frac(R)$. 

**Definition**: $A$ subset $I\subset R$ is called a **left ideal** if
1. $I$ is a subgroup of $R$ under addition.
2. $RI\subseteq I$. 

An ideal is a two sided ideal, and $I$ is proper if $I\neq R$. 

**Definition**: $R$ commutative, $x_{1}, \cdots,x_{s}\in R$, the ideal generated by $x_{1}, \cdots,x_{s}$ is $(x_{1}, \cdots, x_{s}):=\left\{  \sum_{i=1}^{s}a_{i}x_{i}:a_{i}\in R  \right\}$. It is sort of a generalization of "gcd" and is first introduce by Kummer in his attempt on proof Fermat's Theorem. 

**Definition**: $R$ a ring, $I\subset R$, ideal, define the **quotient ring** $R / I:=\{ xI:x \in R \}$. 

**Theorem**: (comes from groups, and check the property of multiplication)
1. If $\phi:R\rightarrow S$ ring homomorphism, then $ker$ is an ideal of $R$, $\phi(R)$ is a subring of $S$. Moreover, $\phi$ induces a ring isomorphism $R / ker\phi\rightarrow \phi(R)$.
2. $I\subseteq J\subset R$ ideal then $J / I\subset R / I$, as ideals, and $(R / I) / (J / I)\simeq R / J$ is an isomorphism.
3. $I \subset R$ an ideal. Then there is a 1-1 map $\{ \text{ideals of } R  \text{ containing } I\}$ $\longleftrightarrow$ $\{ \text{ideals } \overline{J} \text{ of } R / I \}$. 

**Definition**: $I,J$ be 2-sides ideals of $R$.
1. Define **sum** $I+J=\{ i+j:i \in I,\ j \in J \}$.
2. Define the **product** $IJ=I\cdot J$ be the ideal generated by $\{ ij: i \in I,\ j \in J \}$. 
3. $I\cap J$ is also an ideal, $IJ\subset I\cap J$. 

**Remark**: $R / I$ <--> in computation, can replace any $x \in R$ by any $x' \in R$ s.t. $x-x' \in I$. 

## Chinese remainder theorem
**Classical result**: If $n_{1}, \cdots,n_{r}$ pairwise coprime integers, then we have a ring isomorphism:
$$
\mathbb{Z} / (n_{1}, \cdots, n_{r}) \simeq (\mathbb{Z} / n_{1}\mathbb{Z}) \times \cdots \times(\mathbb{Z} / n_{r}\mathbb{Z})
$$

**General case**: Let $R$ be commutative ring, $I_{1}, \cdots,I_{r}$ be pairwise coprime ideals (i.e. $I_{i}+I_{j}=R$) then we have a ring isomorphism:
$$
R / \prod_{i=1}^{r}I_{i} \simeq \prod_{i=1}^{r} R / I_{i}
$$

*Proof*: 
1. One immediately know that there is a natural map $\phi :R / \bigcap_{i}I_{i}\rightarrow\prod_{i}R / I_{i}$. So we have to check in the case of pairwise coprime, $\bigcap_{i}I_{i}=\prod_{i}I_{i}$ and $\phi$ is surjective. In fact, using induction, we only have to check the case of $r=2$.
2. Take $I,J$ coprime, then there is a $x \in I$ and $y \in J$, s.t. $x+y=1$, then consider the map $\phi$ that send $x\mapsto(0,1)$ and $y\mapsto(1,0)$. Then write $R=Rx+Ry$, so it is surjective. Now we only have to check $I\cap J=I\cdot J$, i.e. $I\cap J\subseteq I\cdot J$. Take $z \in I\cap J$, then $z=(x+y)z=xz+yz$, as $xz \in I\cdot J$ and $yz \in I\cdot J$, so we have $z \in I\cdot J$. 

**Definition**: $R$ a rings
1. A 2-sided ideal $I$ of $R$ is **maximal** if there is no ideal between $I$ and $R$. 
2. If $R$ is commutative, an ideal $I$ is **prime** if $ab \in I$ $\implies$ $a\in I || b \in I$. Or $R / I$ is integal domain. In fact, $R \backslash I$ is closed under multiplication so the localization is possible.

**Theorem**: $R$ ring, $I$ a nontrivial ideal, then it is contained in a maximal ideal (this depends on [[Zorn's lemma]]).

*Proof*: just take $S=\{ J\subset R:I\subseteq J \}$, with natural partial order, then $S$ every chain $A$ has a upper bound $\bigcup_{J \in A}J$, so the [[Zorn's lemma]] tells us that $S$ has a maximal element, hence $I$ is contained in a maximal ideal.

**Proposition**: $R$ commutative, $I$ an ideal
1. $I$ is maximal iff $R / I$ is a field.
2. $I$ is prime iff $R / I$ is integal domain.
3. Maximal ideal is prime.

**Facts**: 
1. $f:R\rightarrow S$ a ring homomorphism, let $J\subseteq S$, then $I=f^{-1}(J)$ is also an ideal. As a result, $f$ always induces $Spec(R)\rightarrow Spec(S)$, where $Spec$ is the [[Spectrum]] of the ring.
2. $f(I)$ is not necessarily an ideal, just as in topology.

**Definition**:
An ideal $I\subseteq R$ is called a **principle ideal** if $I=(a)$ for some $a \in R$. A ring $R$ is called a **principle ideal domain** (or PID in short) if all ideals of $R$ are principle.

**Proposition**: In PID, all prime ideals are maximal.

*proof*:
Consider $I=(p)$ be a prime ideal, if $I$ is not maximal, then there is a $I\subset J\subset R$, $J$ maximal, suppose $J=(m)$, then there is a $n \in R$ s.t. $p=mn$. Since $(p)$ prime, we know $m\in I$ or $n \in I$, hance $n \in I$. Let $n=kp$ for some $k \in R$, then $p=kmp$, so $km=1$, whence $J=(1)=R$ a contradiction.

**Definition**: A ring is a **Unique factorization domain** (or UFD in short), if all $a \in R$ can be uniquely written in the form of $a=u\cdot p_{1}p_{2}\cdots p_{n}$ for some $u$ a unit and $p_{i}$ prime (i.e. $(p_{i})$ is prime ideal, but when $R$ not PID, then irreducible is not necessarily prime).

**Definition**: A ring is a **Euclidian domain**, if there is a $N:R\rightarrow \mathbb{Z}_{\geq0}$ s.t. $N(0)=0$, and for all $a,b \in R$ $b\neq0$, there is a $q,r \in R$, with $a=bq+r$, and either $N(r)=0$ or $N(r)<N(b)$. (Not very useful). 

One immediately know that (maybe not so immediately :( ) $EUD\implies PID\implies UFD$

**Theorem**: $R$ an integal domain, then $R$ is UFD iff $R[x]$ is a UFD.

**Theorem**: $R$ a UFD, $K=Frac(R)$, assume $f(x)=A(x)B(x)$, with $A,B \in K[x]$, then there is a $r \in K^{\times}$ s.t. $rA,r^{-1}B\in R[x]$. 

**Theorem B**: $R$ commutative, $\mathfrak{p}\subset R$ prime ideal, assume $\mathfrak{p}|(f(x)g(x))$, $f,g \in R[x]$, then $\mathfrak{p}|f$ or $\mathfrak{p}|g$. 

*proof of B*: Just consider $R / \mathfrak{p}[x]$, which is an integal domain, so one of $\overline{f},\overline{g}$ must be 0.

*Proof of A*: take $A=\frac{1}{a}A'$, $B=\frac{1}{b}B'$, then for all $p|ab$, $p|A'$ or $p|B'$, so $\frac{ab}{p}f=A_{1}B_{1}$, and use induction on $ab$. 

**Proposition**: (Eisenstein's criterion)
$R$ integral domain, $\mathfrak{p}\subseteq R$ prime, $f(x)=x^{n}+a_{n-1}x^{n-1}+\cdots+a_{0} \in R[x]$, if $a_{0},\dots,a_{n-1}\in \mathfrak{p}$, $a_{0}\not\in \mathfrak{p}^{2}$, then $f$ is irreducible. 

**Proposition**: $K$ a field, $G\subseteq K^{\times}$ a finite group, then $G$ is cyclic.

# Modules, classification of finitely generated modules
**Analogue**: Modules of ring $\longleftrightarrow$ vector space of field.

**Definition**: $R$ a ring, let $M$ be an abelian group and $\phi:R\rightarrow End(M)$ as a ring homomorphism, then $(M,\phi)$ is a **left $R$-module**. (Or, $\phi$ is more or less a vector spece over $R$). The concept of submodule is clear. Right $R$-module is $R^{-1}\rightarrow End(M)$. 

We still have direct product and direct sum, $\prod_{i \in I}M_{i}$, and $\bigoplus_{i \in I}M_{i}$, the difference is that direct sum can only have finitely many spaces that is nonzero. As the definition show, if there is an $\phi:S\rightarrow R$, then a left $R$-module can also be viewed as $S$-module. In particular, $R$ is also an $R$-module, and all its submodules are ideals.  

**Definition**: $R$ a ring, $M,N \in Mod_{R}$. 
1. An **$R$-module homomorphism** is a homomorphism of group and kept the action of $R$ on it, i.e. $\phi:M\rightarrow N$ is a homomorphism of module iff $\phi(r\cdot m)=r\cdot \phi(m)$. But $Hom_{R}(M,N)$ is just an abelian group, and is still an $R$-module iff $R$ is abelian. 
2. An **$R$-module isomorphism** is a bijective homomorphism of $R$-module.
3. $\phi:M\rightarrow N$, $R$-module homomorphism, and $ker(\phi)=\{ m \in M:\phi(m)=0 \}$, and $\mathrm{Im}(\phi)=\phi(M)$. 
4. $N\subseteq M$, $R$-submodule, define **quotient module** as $M / N$, abelian group with $R$-action $r\cdot(m+N)=r\cdot m+N$. 
5. $M$ a module is called **irreducible** if $M$ havs no nontrivial submodule. 

**Theorem**: Jordan-Hölder theorem on $R$-module. $M$ a $R$-module, $0=M_{0}<M_{1}<\cdots<M_{r}=M$ s.t. $M_{i} / M_{i-1}$ is irreducible, and $\{ M_{i} / M_{i-1} \}$ is unique. 

**Definition**：$M$ a left $R$-module, $X\subseteq M$ subset $RX:=\left\{  \sum_{i}a_{i}x_{u}:a_{i} \in R, x_{i} \in X  \right\}$, is the submodule of $M$ generated by $X$. If $X=\{ x_{1}, \dots, x_{n} \}$, then get surjective $R$-module homomorphism $R^{n}\rightarrow RX$. 
1. A $R$-module $M$ is **finitely generated** if there is a $X \subseteq M$ finite s.t. $RX=M$. 
2. $M$ is called **cyclic** if it is generated by a single element $m \in M$. 

**Theorem**: $R$ a PID, $M$ finitely generated $R$-module. Then $M\simeq R^{\oplus r}\oplus R / (a_{1})\oplus \cdots\oplus R / (a_{m})$, with $r\geq 0$, $a_{i} \in R$, $a_{i}|a_{i+1}$. Moreover, $r$ is unique and $a_{i}$ is unique up to associates. 

*Proof of uniqueness*: Assmue $M\simeq R^{\oplus r}\oplus R / (a_{1})\oplus \cdots\oplus R /(a_{m})\simeq R^{\oplus r}\oplus R / (b_{1})\oplus \cdots\oplus R /(b_{m})$, need to proof $r=s,\ m=n,\ (a_{i})=(b_{i})$. Consider $dM=\{ dx:x \in M \}\subseteq M$, $R$-submodule. The first decompose gives $dM\simeq R^{\oplus r}\simeq R^{\oplus s}$. Then tensor with $F=Frac(R)$, we have $F^{\oplus r}\simeq F^{\oplus s}$, hence $r=s$. Now consider $M_{tor}$ as multiply it with $b_{i}$, so $(b_{i})\subseteq(a_{j})$ for some $j$. 

The idea is as follow: 
1. decompose $a_{i}$ into product of prime element of $R$. Apply chinese remainder theorem, $a=p_{1}^{e_{1}}\cdots p_{s}^{e_{s}}$, hence $R /(a)=\bigoplus_{j}R /(p_{i}^{e_{i}})$. So we reduce to the case of $a_{i}=p^{t}$, $t>0$, and $t_{i}<t_{i+1}$, $p$ prime. Then $M\simeq R^{\oplus r}\oplus R /(p^{t_{1}})\oplus\cdots\oplus R /(p^{t_{m}})\simeq R^{\oplus r'}\oplus R /(p^{t'_{1}})\oplus\cdots\oplus R /(p^{t'_{m}})$, and we have to proof that $r=r'$ and $t_{i}=t_{i}'$. 
2. $k=R /(p)$ a field, $dim_{k}(M /pM)=r+\#\{ t_{1}, \cdots,t_{m} \}$. (Note that $M / pM$ is $R$-module, and if $b \in(p)$, then $bx=0$ forall $x \in M /pM$, so is also an $R /(p)$-module). Moreover, $dim_{k}(p^{t}M / p^{t+1}M)=r+\#\{ t_{i}:|t_{i}\geq t \}$. Thus we know that $r=r'$ and $t_{i}=t_{i}'$. 
3. As to the existence. We will proof another theorem

**Theorem**: $R$ a PID, $N$ a free $R$-module of rank $n$, $M\subseteq N$, then 
1. $M$ is free of rank $l\leq n$.
2. there is a set of basis $\{ f_{1},f_{2}, \cdots,f_{n} \}$ of $N$, and there is $a_{1}|a_{2}|\cdots|a_{n} \in R-\{ 0 \}$, s.t. $a_{i}f_{i}$ form a basis of $M$. 

*Proof*: 
Consider all $\lambda(M)$ for all $\lambda \in Hom(N,R)$, then there must be a maximal element. Suppose it is $(d_{1}) \subseteq R$. If $d_{1}=0$, then $M=0$. Take $\lambda(x_{1})=d_{1}$, then forall $\lambda' \in Hom(N,R)$ $d_{1}|\lambda'(x_{1})$, thus $x_{1}=f_{1}d_{1}$ for some $f_{1} \in E$. Now we have $Rf_{1}\oplus ker(\lambda)=N$, and $Rx_{1}\oplus ker(\lambda)\cap M=M$. And as we choose $(d_{1})$ to be biggest, we know that when we keep doing the same action and the following $(d_{i})$ must have $d_{1}|d_{i}$. 

Now with this theorem, we know that $M$ is finitely generated, so $R^{n}\rightarrow M$ is injective, hence $M\simeq R^{n} /N$, and use the above theorem.

# Field Extension
**Recall**: A **field** is a commutative ring in which every nonzero element is invertible.

**Definition**: The **characteristic** of a field $K$, denoted by $char(K)$ is either the smallest positive integer $p$ s.t. $1+1+\cdots+1=0$ ($p$ copies) or $0$ if $p$ does not exist. 

**Definition**: The **prime** field of a field $K$ is the smallest subfield of $F$, i.e. 
1. $\mathbb{F}_{p}=\mathbb{Z} /p\mathbb{Z}$ if $char(K)=p\neq0$.
2. $\mathbb{Q}$, if $char(K)=0$. 

**Notation**: If $F\subseteq K$ a subfield, then also say $K$ is a field extension of $F$. Say $F$ is the a base field. Any field $E$ with $F\subseteq E\subseteq K$ is called an intermediate field