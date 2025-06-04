# Definition

>[!note] Definition
>let $G$ be a group, and $R$ a commutative ring, $M$ a $R[G]-module$ then let $H_{R}^{n}(G,M):=Ext_{R[G]}^{n}(R,M)$ for $n \in \mathbb{N}$ be the n-th group homology.

($Ext$ is defined in [[First extension group]])

# Degree Zero Group Cohomology

By definition $H^0(G,M)=Hom_{R[G]}(R,M)=M^{G}$ is the largest submodule of $M$ with trivial $G-action$, the fixed points of $M$.

# Degree One Group Cohomology

We use the exact sequence $0 \longrightarrow I(R[G]) \longrightarrow R[G] \longrightarrow R \longrightarrow 0$, where $I(R[G])$ is the kernel of the trivial morphism $R[G] \rightarrow R$, $\sum\limits_{g \in G} c_{g} g \mapsto \sum\limits_{g \in G} c_{g}$ i.e. the ideal genereated by $\{g-1 | g \in G\}$. Take a projective resolution of $R$:
$$
\cdots \longrightarrow P_2 \stackrel{\delta_1}\longrightarrow P_1 \stackrel{\delta_0}\longrightarrow R[G] \stackrel{l}\longrightarrow R
$$
note that $I(R[G])=ker(R[G] \rightarrow R)$ so by the universial property, every $\phi:P_1 \rightarrow M$ with $\delta_1 \circ \phi=0$ factors through $I(R[G])$, hence we have: $ker(Hom_{R[G]}(\delta_1,M))=Hom_{R[G]}(I(R[G]),M)=\{f:G \rightarrow M|g \cdot f(h)= f(gh)-f(h)\}$. 
Similiarly, $im(Hom_{R[G]}(\delta_0,M))=\{f \in Hom_{R[G]}(I(R[G]),M) | \exists \phi \in Hom_{R[G]}(R[G],M):f=\phi \circ l\}$, which can be written as $\{f:G \rightarrow M| \exists m \in M, \forall g \in G : f(g)=gm-m\}$, we let the two sets be $Der(G,M),InnDer(G,M)$ thus we get $H^1(G,M)=Der(G,M)/InnDer(G,M)$.

# Degree Two group cohomology

We can construct the begining of the projective resolution of $R$ as follow:
$$
R[G] \otimes_{R} R[G] \otimes_{R} \otimes_{R} R[G] \otimes_{R} R[G] \stackrel{\delta_2}\longrightarrow R[G] \otimes_{R} \otimes_{R} R[G] \otimes_{R} R[G] \stackrel{\delta_1}\longrightarrow R[G] \otimes_{R} R[G] \stackrel{\delta_0}\longrightarrow R[G] \rightarrow R
$$
where 
$$
\begin{aligned}
\delta_0:R[G] \otimes_R R[G] &\longrightarrow R[G]\\
g_1 \otimes g_2 & \longmapsto g_1(g_2-1)\\
\delta_1:R[G] \otimes_R R[G] \otimes_R R[G] &\longrightarrow R[G] \otimes_R R[G]\\
g_1 \otimes g_2 \otimes g_3 & \longmapsto g_1g_2 \otimes g_3 - g_1 \otimes g_2g_3 + g_1 \otimes g_2\\
\delta_2:R[G] \otimes_R R[G] \otimes_R R[G] \otimes_R R[G] & \longrightarrow R[G] \otimes_R R[G] \otimes_R R[G]\\
g_1 \otimes g_2 \otimes g_3 \otimes g_4 &\longmapsto g_1g_2 \otimes g_3 \otimes g_4 -g_1 \otimes g_2g_3 \otimes g_4 + g_1 \otimes g_2 \otimes g_3g_4 - g_1 \otimes g_2 \otimes_3
\end{aligned}
$$

One can check that this indeed is a exact sequence, and each is projective, using the similiar argument in the chase of degree 1, we are able to compute $H^2(G,M)$. 

Here is another interpretation of $H^2(G,M)$ using the idea of group extention, i.e. $H^2(G,M)$ parameterises equivalence classes of [[Short exact sequence]] $1 \longrightarrow M \longrightarrow E \stackrel{\pi}\longrightarrow G \longrightarrow 1$, where $E$ corresbond to 0 in $H^2(G,M)$ if there exists a $G \stackrel{l}\longrightarrow E$ with $l \circ \pi=id_G$. 

Note that $H^2(G,M) \simeq Ext^2_{\mathbb{Z}[G]}(\mathbb{Z},M) \simeq Ext^1_{\mathbb{Z}}(I(\mathbb{Z}[G]),M)$, and every element the last one corresbond to a short exact sequence $0 \longrightarrow M \longrightarrow X \longrightarrow I(\mathbb{Z}[G]) \longrightarrow 0$, we hope that we can relate it to a short exact sequence of groups $1 \longrightarrow M \longrightarrow E \longrightarrow G \longrightarrow 1$, we do it as follow:
1. First we observe that: if $M$ is an abilian normal subgroup of $E$, with $E/M \simeq G$, then $M \simeq I(\mathbb{Z}[M])E/(I(\mathbb{Z}[E]) \cdot I(\mathbb{Z}[M]))$ as $\mathbb{Z}[G]-module$, by mapping $m \mapsto m-1$.
2. For every exact sequence $1 \longrightarrow M \longrightarrow E \longrightarrow G \longrightarrow 1$, we get $0 \longrightarrow I(\mathbb{Z}[M])E \longrightarrow \mathbb{Z}[E] \longrightarrow \mathbb{Z}[G] \longrightarrow 0$,  which is equivalent to $0 \longrightarrow I(\mathbb{Z}[M])E \longrightarrow I(\mathbb{Z}[E]) \longrightarrow I(\mathbb{Z}[G]) \longrightarrow 0$,  the quotient by $I(\mathbb{Z}[E]) \cdot I(\mathbb{Z}[M])$, we have $0 \longrightarrow M \longrightarrow I(\mathbb{Z}[E])/(I(\mathbb{Z}[E]) \cdot I(\mathbb{Z}[M])) \longrightarrow I(\mathbb{Z}[G]) \longrightarrow 0$, and its inverse is defined by pullbacks of groups (c.f.[[First extension group]]).