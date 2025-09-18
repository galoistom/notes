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

# Isomorphism Theorem, composition series, hölder theorem
**Theorem** 1: $\phi :G\rightarrow H$ homomorphism. Then $ker(\phi)\triangleleft G$, and $G / ker(\phi)\simeq \phi(G)$. 

*Proof*: Define a map $\psi:G /ker(\psi)\rightarrow \phi(G)$, $g\cdot ker(\phi)\mapsto \phi(g)$. We first check $\psi$ is well defined: In fact, if $g,g'$ are in the same coset, suppose $g'=gk$, $k\in ker(\phi)$, then $\phi(g')=\phi(g)\cdot \phi(k)=\phi(g)$. It is also clear that it is indeed a homomorphism.
One immediately note that $\psi$ is surjective, so we only have to check that it is injective. In fact, $\psi(g\cdot ker(\phi))=1_{H}$ if and only if $g\in ker(\phi)$, i.e. $g\cdot ker(\phi)=ker(\phi)$. 

**Theorem** 2: $A<G$, $B\triangleleft G$. Then $AB<G$, $B\triangleleft AB$, $A\cap B\triangleleft A$, and $(AB) / B\simeq A/(A\cap B)$. 

*Proof*: Normal is easy to check. Consider $A\rightarrow AB\rightarrow(AB) / B$, $a\in A$ is in the kernel is when $a \in B$ is in $B$ as well, i.e. $a\in A\cap B$, and use the theorem 1.

**Theorem** 3: $H\triangleleft K\triangleleft G$. Then $K / H \triangleleft G /H$, and $(G / H)/(K / H)\simeq G / K$. 

*Proof*: Consider $G / H\rightarrow G / K$, $gH\mapsto gK$, we need to check it has kernel $K / H$. As if $gH$ s.t. $gK=K$, then $g\in K$, so $ker=\{ gH:g\in K \}=K / H$. 

**Theorem** 4: $N\triangleleft G$ normal, then there is a bijection {subgroups of $G$ containing $N$} <--> {subgroups of $G / N$}, with $A\mapsto A / N$ and $\overline{A}\mapsto \pi ^{-1}(\overline{A})$, where $\pi:G\rightarrow G / N$ is the quotient map. In fact, the bijection preserves intersection, index, normal, quotient.
