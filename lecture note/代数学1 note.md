why group/ring/fields?
- Describe symmetry uniformly
- Compose subsymmetry in different context (e.g. 正二十面体 vs symmetry group of roots of 五次方程) and extract the key(fundmantal) property of the objects we are studying. 

**Example**: 
- the equation $x^{2}-Dy^{2}=1$, $D$ square free >1. The solution is of the form $\pm(x_{0}+y_{0}\sqrt{ D })^{N}$. 
- Elliphc curve $F:=\{ (x,y) : y^{2} = x^{3} - Dx \} \cup \{ \infty \}$. Define $A,B,C \in F$ have the property $A+B+C=0$ if $A,B,C$ share a line (the group is indeed abelian). 

---

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