This is the same topic of [[lie group and their representation (reminder)]] but focous more on the algebra structure iteslf

Lie algebra is a vector space $\mathfrak{g}$ with a bilinear form which we will call **Lie bracket or commuator** $[\ ,\ ]:\mathfrak{g}\times \mathfrak{g}\rightarrow \mathfrak{g}$  such that: 
1. $[x,x]=0$ for all $x \in L$.
2. $[x,[y,z]]+[y,[z,x]]+[z,[x,y]]=0$ for all $x,y,z \in L$.

Then isomorphism and homomorphism are clear, just the map between vector that preserve the bracket. 

We use the terminology used in linear alebgra, by an **F-algebra** we mean a vector space $\mathfrak{U}$ over $F$ endowed with a bilinear operation $\mathfrak{U}\times \mathfrak{U}\rightarrow \mathfrak{U}$, usually denoted by juxtaposistion (unless it is lie algebra). And by derivation of $\mathfrak{U}$ we mean a map $\delta :\mathfrak{U}\rightarrow \mathfrak{U}$ satisfying the familiar $\delta(ab)=a\delta(b)+\delta(a)b$. In particular, we use $Der\,\mathfrak{g}$ to denote the set of all derivation of lie algebra $\mathfrak{g}$. As one might notice, the lie bracket is a derivation, and this kinds of derivation form are called **inner**, and all others **outer**. Moreover, for all $x \in \mathfrak{g}$ the linear map $ad(x)\in Der\,\mathfrak{g}$ defined by $y\mapsto[x,y]$ gives the **adjoint representation** of $\mathfrak{g}$, which plays an important role in this topic.

The most natural special case of lie algebra is the abelian lie algebra, i.e. the bracket $[x,y]=0$ for all $x,y \in \mathfrak{g}$. 

A subspace $I$ of $\mathfrak{g}$ is called an **ideal** of $\mathfrak{g}$ if $x \in \mathfrak{g}$, $y \in I$ together imply $[x,y] \in I$. The **center** $Z(\mathfrak{g})=\{ z \in \mathfrak{g}: [x,z]=0,\ \forall x \in \mathfrak{g} \}$ and the drieved 