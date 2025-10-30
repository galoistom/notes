>[!note] Zorn' lemma
>If $A$ is a set with a partial order, and every chain has a upper bound (i.e. there is a $x \in A$ s.t. $\forall y \in B$ $y\leq x$), then there is a maximal element in $A$ (i.e. there is a $x \in A$ s.t. $\forall y \in A$, $y\geq x$).

It is equivalent to:
>[!note] the axiom of choice
>For any set $X$ of nonempty sets, there exists a choice function $f$ that is defined on $X$ and maps each set of $X$ to an element of that set.

**Definition**: A partial order on a nonzero on a nonempty set $A$ is a relation $\leq$ on $A$ s.t.
1. (reflative) $x\leq x$.
2. (anti-symmetric) $y\leq x$ and $x\leq y$ $\implies$ $x=y$.
3. (transitive) $x\leq y$, $y\leq z$ $\implies$ $x\leq z$.

A chain is a subset $B\subseteq A$ s.t. $\forall x,y\in B$, $x\leq y$ or $y\leq x$.
