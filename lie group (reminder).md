lie group is a manifold with a group structure (one need the operation $g$ has to be differential, of course). 
Some easy examples would be $GL(V)$, $SL(V)$ the group of element with $\det=1$, $SO(V)$ the goup of element keeps orthognality as well, etc. 

Unfortunately, general lie group is vary hard to study. People then notice that the neiberhood of $1_{G}$ genertate $G$, so we can know many information of $G$ by studying the tangent space of $G$ at $1_{G}$ which we call *lie algebra* (though it is wrong to say that lie algebra determines lie group). 

As we know, the key of group is the morphism $m_{g}:G \rightarrow G$ sending $x \mapsto gx$. The problem is, $m_{g}$ does not fix any point, so it is hard to assoicate it to the tangent space. To solve this problem, people consider the inner automorphism $\Psi_{g} \in Aut(G)$ with $x \mapsto gxg^{-1}$. Thus by taking differential, we get $Ad(g):=(d\Psi_{g})_{e}$, but this still need the  