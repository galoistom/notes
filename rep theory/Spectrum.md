Recall that $C$ a commutative ring, then the spectrum of $C$, denoted $Spec(C)$, is the set of prime ideals of $C$. We can define the topology by defining all closed set to be $V_{I}=\{ \mathfrak{p}: I \subseteq \mathfrak{p} \}$. 

Now let $Cl(G)$ be the set of conjugacy classes of $G$. Then one can identify $A^{Cl(G)}$ as the ring of class function. Then there are natural injection map $A\rightarrow A\otimes R(G)\rightarrow A^{Cl(G)}$, then we get 
$$
Spec(A^{Cl(G)}) \rightarrow Spec(A\otimes R(G))\rightarrow Spec(A)
$$
surjective. 

On the other hand, we know that $Spec(A)$ consists of the ideal 0 and the maximal ideals of $A$. Moreover, if $M$ is maximal in $A$, the field $A / M$ is finite; its characteristic is called the  **residur characteristic** of $M$. In fact, the spectrum of $A^{Cl(G)}$ can be identified with $Cl(G)\times Spec(A)$: with each $c\in Cl(G)$ and each $M\in Spec(A)$  we asscoiate the prime ideal $M_{c}$ consisting of those $f\in A^{Cl(A)}$ such that such that $f(c)\in M$. The image of $M_{c}$ in $Spec(A\otimes R(G))$ is the prime ideal $P_{M,c}=M_{c}\cap A\otimes(R(G))$. 

**Propsition**: We obtain once and only once each prime ideal of $A\otimes R(G)$ if: 
1. with each class $c \in Cl(G)$ we asscoiate $P_{0,c}$,
2. with each $p$-regular class $c$ and each maximal  ideal $M$ of $A$ with residual characteristic $p$ we asscoiate $P_{M,c}$, 

We can rephrase it as 

**Propsition**:
1. if $M=0$, $P_{0,c_1}=P_{0,c_{2}}$ is equivalent to $c_{1}=c_{2}$. 
2. Suppose that $M\neq0$ with residue characteristic $p$. Let $c'$ be the class consisting of the $p$ prime-components of the elements of $c_{1}$. Then $P_{M,c_{1}'}=P_{M,c_{2}'}$ if and only if $c_{1}'=c_{2}'$. 

**Remark**:
1. Let $I$ be an ideal of $A\otimes R(G)$. To show that $I$ is equal to $A\otimes R(G)$, it suffice to show that $I$ is not contained in any of the prime ideals $P_{M,c}$; this is the approach tatken in the proof of [[Brauer's Theorem]]. 
2. We can represent $Spec(A\otimes R(G))$ graphically as a union of "lines" $D_{c}$ corresponding to the various classes $c$, each of these lines representing $Spec(A)$. These lines "intersect" if a maximal ideal $M$ of $A$ with residue characteristic $p$ and the $p'$-component of $c_{1}$ and $c_{2}$ are equal. 

**Propsition**: $Spec(A\otimes R(G))$ is contained in the Zariski topology