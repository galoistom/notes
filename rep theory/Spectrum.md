Recall that $C$ a commutative ring, then the spectrum of $C$, denoted $Spec(C)$, is the set of prime ideals of $C$. 

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

**Propsition**: if $M=0$, $P_{0,c_1}=$