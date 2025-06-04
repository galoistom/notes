# Definition

We say that two [[Short exact sequence]] are equivalent if there exists isomorphisms $\phi_x,\phi_y,\phi_z$ making the following diagram commute:

```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
&0 \arrow[r] & X \arrow[r, "f_1"] \arrow[d, "\phi_x"] & Y \arrow[r, "g_1"] \arrow[d, "\phi_y"] & Z \arrow[r] \arrow[d, "\phi_z"] & 0\\
& 0 \arrow[r] & X \arrow[r, "f_2"] & Y' \arrow[r, "g_2"] & Z \arrow[r] & 0
\end{tikzcd}
\end{document}
```
It is easily checked that this equivalent relation is indeed an equivalent relation. Now we are going to varify the addition and zero object in the equivalent classes of $Y$ and obtain the definition of $Ext^1(Z,X)$.

1. **Zero object**
	It is easy, we define the zero object to be the equivalent class of $\overline{X \oplus Z}$ as it is some how the simplest example we can construct.

2. **The Addition**
	A trivial idea is simply using the direct sum to add things up. Unfortunately, direct sum only provide the short exact sequence $$0 \longrightarrow X \oplus X \longrightarrow Y_1 \oplus Y_2 \longrightarrow Z \oplus Z \longrightarrow 0\tag{1}$$
	So we hope to use it to construct a $0 \longrightarrow X \longrightarrow Q \longrightarrow Z \longrightarrow 0$ from $(1)$.
	We will use the following two ways of constructing modules:

>[!note] Pullback(fibre product)
>Given $X,Y,Z$ and morphism $s:X\rightarrow Z$ and $t:Y\rightarrow Z$ then the pullback $P$ have two morphism $p_1:P\rightarrow X$, $p_2:P\rightarrow Y$ such that the square commute, and if there are another $P'$ making the square commute, then there exists a unique $\phi:P' \rightarrow P$ making the folloing diagram commute.

```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
P' \arrow[ddr,bend right=10,swap,"p'_2"] \arrow[drr,bend left=10,"p'_1"] \arrow[dr, "\exists \phi"]\\
&P \arrow[d,"p_2"] \arrow[r,swap,"p_1"] &X \arrow[d,"s"]\\
&Y \arrow[r,"t"] &Z
\end{tikzcd}
\end{document}
```
By reversing all arrows we got the definition of "Pushout", or cofiber product.An elementary argument shows that the product exists and is unique up to isomorphism. 

Now we are ready to construct the process of addition.

```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd} & 0 \arrow[r] & X \oplus X \arrow[r, "{(f_1,f_2)}"] \arrow[d] & Y_1 \oplus Y_2 \arrow[r, "{(g_1,g_2)}"] \arrow[d] & Z \oplus Z \arrow[r] \arrow[d, equal] & 0 \\
& 0 \arrow[r] & X \arrow[r, "f_0"] \arrow[d, equal] & P \arrow[r, "g_0"] & Z \oplus Z \arrow[r] & 0 \\ 
& 0 \arrow[r] & X \arrow[r, "f"] & Q \arrow[r, "g"] \arrow[u] & Z \arrow[r] \arrow[u] & 0 \end{tikzcd}
\end{document}
```

We say that $\overline{Q}=\overline{Y_1}+\overline{Y_2}$, it is the mix of a pullup and a pushout. It is easy to check that $Ext^1(X,Z)$ is well-defined abilian group.

## Key interpretation

Here is an important theorem discribs the structure of $Ext^1(M,X)$:

>[!note] Theorem
>Let $M$ be a module, and $P$, and there is a short exact sequence $0 \longrightarrow E \stackrel{f}{\longrightarrow} P \stackrel{g}{\longrightarrow} M \longrightarrow 0$, then $Ext^1(M,X) \simeq Coker(f^*)$(it is isomorphic even as $End(X)^{op}-module$ )

Here is some necessary definition:
1. It is obvious that  $Hom_{R}(_R\!X_S, _R\!Y)$ has the structure of $S-left-module$. And a $X \stackrel{f}{\longrightarrow} Y$ induce a map $Hom(X,Y) \stackrel{f^*}{\longrightarrow} Hom(X,Y')$ by 
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
X \arrow[r,"f"] \arrow[rr,bend right=20,swap,"f \circ \alpha"] &Y \arrow[r,"\alpha"] &Y'
\end{tikzcd}
\end{document}
```
2. By applying the above functor, we induce another exact sequence:$$0 \longrightarrow Hom(M,X) \stackrel{g^*}{\longrightarrow} Hom(P,X) \stackrel{f^*}{\longrightarrow} Hom(E,X) \longrightarrow Coker(f^*) \longrightarrow 0$$

We define the maps $Ext^1(M,X) \leftrightarrows Coker(f^*)$:

1. Let $0 \longrightarrow X \stackrel{\alpha}{\longrightarrow} I \stackrel{\beta}{\longrightarrow} M \longrightarrow 0$ be a short exact sequence, using the definition of [[Projective module and injective module]], there exists $\psi,\phi$ making the following diagram commute. Then we define the image of $I$ in $Coker(f^*)$ as the image of $\psi$ in $Coker(f^*)$.
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
&0 \arrow[r] & X \arrow[r, "\alpha"] & I \arrow[r, "\beta"] & M \arrow[r] & 0\\
& 0 \arrow[r] & K \arrow[r, "f"] \arrow[u, "\exists \psi"] & P \arrow[r, "g"] \arrow[u,"\exists \phi"] & M \arrow[r] \arrow[u,equal] & 0 

\end{tikzcd}
\end{document}
```
2. Given a $\overline{\psi} \in Coker(f^*)$, we use pushout to get the $I$ we want, i.e.
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
&0 \arrow[r] & K \arrow[r, "f"] \arrow[d,"\psi"] & P \arrow[r, "g"] \arrow[d,"\exists \phi"] & M \arrow[r] & 0\\
& 0 \arrow[r] & X \arrow[r, "\alpha"] & I \arrow[r, "\beta"] & M \arrow[r] \arrow[u,equal] & 0
\end{tikzcd}
\end{document}
```

Now we check that the two morphism is indeed a pair of well-defined isomorphisms.

>[!note] useful lemma
>In the following commutative diagram with exact rows, then the right square is a pullback square

```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
&K \arrow[r,"l"] \arrow[d,equal] &P \arrow[r,"p_1"] \arrow[d,"p_2"] &X \arrow[r] \arrow[d,"s"] &0\\
&K \arrow[r,"p_2 \circ l"] &Y \arrow[r,"t"] &Z \arrow[r] &0
\end{tikzcd}
\end{document}
```
 To proof the lemma, we assume (WOLG) that $l$ is injective, and Let $\tilde{P}$ denote the actual pullback of the square. Consider the following diagram:
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
&0 \arrow[r] &Ker(\alpha) \arrow[r,"k"] \arrow[d,"\overline{\beta}"] &\tilde{P} \arrow[r,"\alpha"] \arrow[d,"\beta"] &X \arrow[r] \arrow[d,"s"] &0\\
&0 \arrow[r] &Ker(t) \arrow[r,"p_2 \circ l"] &Y \arrow[r,"t"] &Z \arrow[r]&0
\end{tikzcd}
\end{document}
```
And by the definition of pullback square, we have a morphism $xi: P \rightarrow \tilde{P}$, which lead us to consider the diagram:
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
&0 \arrow[r] &K \arrow[r,"l"] \arrow[d] &P \arrow[r,"p_1"] \arrow[d,"\xi"] &X \arrow[r] \arrow[d,equal] &0\\
&0 \arrow[r] &K \arrow[r,"k \circ \beta^{-1}"] &\tilde{P} \arrow[r,"\alpha"] &X \arrow[r] &0
\end{tikzcd}
\end{document}
```
The right square is obviously commutative, note that $p_2$ restricts to tha identity map $K \rightarrow K$, and so does $\beta$, and $p_2=\beta \xi$, hence $\xi$ restricts to an isomorphism $K \rightarrow K$, appling the short five lemma, we have $\xi$ is an isomorphism $P \rightarrow \tilde{P}$, which completes the proof of the lemma.

The lemma above implies that the two morphisms are indees well-defined. It is left to check that they are mutually inversed isomorphisms.

We first check that $Coker(f^*)$ does not depend on the choice of $P$:

>[!note] Independency
>Let $0 \longrightarrow K \stackrel{f}{\longrightarrow} P \stackrel{g}{\longrightarrow} M \longrightarrow 0$ and $0 \longrightarrow K' \stackrel{f'}{\longrightarrow} P' \stackrel{g'}{\longrightarrow} M \longrightarrow 0$ be two short exact sequence with projective modules $P,P'$, then $Coker(f^*) \simeq Coker((f')^*)$

*Proof:*
From the definition of projective modules, we get $\alpha:P\rightarrow P'$ and $\alpha':P' \rightarrow P$ such that $g=\alpha g'$ and $g'=\alpha'g$, and restrict them to $\beta,\beta'$. Eventhough they are not acutally ajoints, we still tries to put them together to from the folling diagram:
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
&0 \arrow[r] &K \arrow[r,"f"] \arrow[d,"\beta'"] &P \arrow[r,"g"] \arrow[d,"\alpha'"] &M \arrow[r] \arrow[d,equal] &0\\
&0 \arrow[r] &K' \arrow[r,"f'"] \arrow[d,"\beta"] &P' \arrow[r,"g'"] \arrow[d,"\alpha"] &M \arrow[r] \arrow[d,equal] &0\\
&0 \arrow[r] &K \arrow[r,"f"] &P \arrow[r,"g"] &M \arrow[r] &0
\end{tikzcd}
\end{document}
```
Consider $\alpha\alpha'-id_p$, obviously we have $g(\alpha\alpha'-id_p)=0$, hence there exists $\tau:P\rightarrow P$ such that $\alpha \alpha' - id_p=\tau f$, similarly, $\tau':P' \rightarrow P'$ exists. Now we go to the follwoing diagram:
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
&0 \arrow[r] &Hom_A(M,X) \arrow[r,"g^*"] \arrow[d,equal] &Hom_A(P,X) \arrow[r,"f^*"] \arrow[d,"\alpha^*"] &Hom_A(K,X) \arrow[r] \arrow[d,"\beta^*"] &Coker(f^*) \arrow[r] \arrow[d,"\mu"] &0\\
&0 \arrow[r] &Hom_A(M,X) \arrow[r,"(g')^*"] \arrow[d,equal] &Hom_A(P',X) \arrow[r,"(f')^*"] \arrow[d,"(\alpha')^*"] &Hom_A(K',X) \arrow[r] \arrow[d,"(\beta')^*"] &Coker(f^*) \arrow[r] \arrow[d,"\mu'"] &0\\
&0 \arrow[r] &Hom_A(M,X) \arrow[r,"g^*"] &Hom_A(P,X) \arrow[r,"f^*"] &Hon_A(K,X) \arrow[r] &Coker(f^*) \arrow[r] &0
\end{tikzcd}
\end{document}
```
Here $\mu,\mu'$ is the induced map making the diagram commute.Note that for $\overline{h} \in Coker(f^*)$, $\mu' \mu \overline{h}=\overline{h \beta \beta'}$, and $\overline{h(\beta \beta'-id_p)}=\overline{h \tau f}=\overline{0}$
Hence $\mu' \mu=id$, hence $Coker(f^*) \simeq Coker((f')^*)$.

We check that the morphism $Ext^1(M,X) \rightarrow Coker(f^*)$ is well-defined:
	For $\phi,\phi'$ satifying the condition, we have $\beta(\phi-\phi')=0$, hence there exists $\tau:P \rightarrow X$ such that $\phi-\phi'=\alpha \tau$, thus $\psi=\tau f$, which is obviously in $Im(f^*)$.

To check the the morphism $Coker(f^*) \rightarrow Ext^(M,X)$ is well-defined:
	Suppose that $\overline{\psi}=\overline{\psi'} \in Coker(f^*)$, then there is a $\tau:P \rightarrow X$ such that $\psi-\psi'=\tau f$, note that $\beta \psi'=\beta \psi =g,\alpha \psi'=\phi' f$, hence $\psi',\phi'$ also form a pushout, and by the uniqueness, it is the same element in $Ext^1(M,X)$.

Thus the proof is completed #

# General definition

The more general version of the concept is defined using the prejective resolution:

>[!note] projective resolution
>a projective resolution is a chain of projective modules $(P_i)$ making the complex ecact:
>$$\cdots \longrightarrow P_3 \stackrel{\delta_3}\longrightarrow P_2 \stackrel{\delta_2}\longrightarrow P_1 \stackrel{\delta_1}\longrightarrow M \longrightarrow 0$$

then $Ext^{i}(M,N):=Ext^1(ker(\delta_n),N)=ker(Hom_A(\delta_i,N))/im(Hom_A(\delta_{i-1},N))$ 

## Some useful propositions

1. Let $R$ be a commutative ring, and two $R-algebra$ $A,B$ with a morphism $B \longrightarrow A$, such that $A$ is a $B$ module. Then for all $A-modules$ $M$ and $B-modules$ $N$ we have 
$$
Ext_{A}^{i}(A \otimes_{B} N,M) \simeq Ext_{B}^{i}(N,M)
$$
2. Let $R$ be a commutative ring, $G$ a group with subgroup $H$. Then for all $R[G]-modules$ $M$ and $R[H]-modules$ N we have
$$
Ext_{R[G]}^{i}(M,Ind_{H}^{G}N) \simeq Ext_{R[H]}^{i}(M,N)
$$
3. $Ext$ is additive under direct sum
4. Let $K$ be a commutative ring and $A$ be a $K-algebra$. Suppose $0 \longrightarrow M \longrightarrow N \longrightarrow L \longrightarrow 0$ is a exact sequence of $A-modules$, and let $T$ be an $A-module$. Then the following sequence is exact
$$
Ext_{A}^1(T,M) \longrightarrow Ext_{A}^1(T,N) \longrightarrow Ext_{A}^1(T,L)
$$
