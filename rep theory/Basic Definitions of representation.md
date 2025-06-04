
>[!note] representation
>A representation $(V,\rho)$ of an algebra $A$ contains a vector space $V$ and a homomorphism $\rho: A \rightarrow GL(V)$ , and the character of the representation $\chi(a)=tr(\rho(a))$ 
>Moreover, the definition can be extended to the modules over a ring.

Further definition: $(V,\rho)$ is said to be irreducible if $V$ do not have a non-trivial subspace(resp. submodule) that is stable under $\rho$.  We will see that the character $\chi$ of the representation $\rho$ more of less determined the whole representation. A group homomorphism $f:G \rightarrow k$ ($k$ a field) is called a class function if $f(tst^{-1})=f(s)$ for all $s,t \in G$, it is easy to see that $\chi$ is a class function over $G$.

>[!note] induced representation and restriction(especially over finite group)
>The definition of restriction is straightforward
>As to the induced representation $$Ind_{H}^{G}W=\mathbb{C}[G] \otimes_{\mathbb{C}[H]} W$$, where $W$ is a linear representation of $H<G$

It is easy to see that if we let $\phi$ denote the character of $(W,\theta)$ then then the character $\chi$ of $Ind_{H}^{G} W$ satisfies: $$\chi(s) = \frac{1}{Card(H)} \sum\limits_{t \in G,tst^{-1} \in H} \phi(tst^{-1})$$

Remark: The definition comes from a simple idea: can we extend the representation of a smaller group $H$ to a larger group $G$ (this can be somehow generalized by extending the inclusion map  to an injective map $H \rightarrow G$ ). In fact, there are two ways to do the extension, first is $\mathbb{C}[G] \otimes_{\mathbb{C}[H]} W$, another way is $Hom_{\mathbb{C}[H]}(W,\mathbb{C}[G])$, which is more or less the same(in the case of finite group, of course) 

>[!note] $R_{K}(G)$ and $P_{K}(G)$
>Let $K$ be a ring, and $G$ a finite group, then $R_{K}(G)$ denotes the [[Grothendieck group]] of the category of $K[G]$ modules, and $P_{K}(G)$ be the sub group of $R_{K}(G)$ consists of the classes of projective $K[G]$ modules(cf.[[Projective module and injective module]]).

The above notion will be used to consider the general case when the field $K$ has character $p>0$. More precisely, in order to study the case of $p>0$, we use the concept of $p-adic$ integer, which leads us to considering the system of $(K,A,k)$ where $A$ is a discrete valustion ring and $K$ be its field of fraction, and have a quotient field $k$.

>[!note] quiver algebra and its representation
>Let $Q=(Q_0,Q_1,s,t)$ be a quiver where $Q_0$ denotes the vertices and $Q_1$ be all the edges and $s,t:Q_1 \rightarrow Q_0$ records the source and target of the edges. We define multiplication of edges by composing then together if it is possible, otherwise it will be 0, thus we get the quiver algebra $K[Q]$.
>A representation of the algebra $K[Q]$ is giving each of the vertices a vector space, and the edges denote the linear transformation between them.

The above notion might also ontribute to the study of representation of finite group, by seeing $G$ as a 1-category, and giving the point a vector space and vertices linear transformation(i.e. each elements in $G$ are seen as an elements in $GL(V)$) which is precisely the definition of the representation of a group. 

Morover, some group might also have topological structure, and the representation preserving the structure(vector spaces have std.topolpgical structure) is called the representation of topological group. The concept will be used often in the representation of lie group and lie algebra.