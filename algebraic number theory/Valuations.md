# The p-adic Numbers
>[!note] Definition
>Fix a prime number $p$. A *p-adic number is a formal infinite series*: $a_{0} + a_{1}p + a_{2}p^{2} + \dots$, where $0 \leq a_{i} < p$ for all $i = 0,1,2,\dots$ The set of all p-adic integers is denoted by $\mathbb{Z}_{p}$.

In fact, we have $a\equiv a_{0}+a_{1}p+\dots+a_{n-1}p^{n-1} \pmod{p^{n}}$. The idea of p-adic numbers come from the Taylor expansion of $f = \frac{g}{h} \in \mathbb{C}(z)$. 

In analogy with the laurent series $f(z)=\sum_{v=-m}^{\infty}a_{v}(z-a)^{v}$, we now extend the domain of p-adic integers in to that of the formal series $$\sum_{v=-m}^{\infty}a_{v}p^{v} = a_{-m}p^{-m}+ \cdots + a_{-1}p^{-1} + a_{0} + a_{1}p + \cdots$$, where $m \in \mathbb{Z}$ and $0\leq a_{v}<p$. Such series we call simply *p-adic numbers* and we write $\mathbb{Q}_{p}$ for the set of all these p-adic numbers. If $f \in \mathbb{Q}$ is any rational number, then we write $f = \frac{g}{h} p^{-m}$ where $g,h \in \mathbb{Z}$ and $(gh,p)=1$, and move the series of $\frac{g}{h}$ backwards $m$ to $\sum_{v=-m}^{\infty}a_{v}p^{v}$. In this way we obtains a canonical map $\mathbb{Q} \rightarrow \mathbb{Q}_{p}$, which takes $\mathbb{Z}$ to $\mathbb{Z}_{p}$ and is injective. 

**Remarks**:
The p-adic numbers can be considered as $\lim\limits_{\longleftarrow}\mathbb{Z} /\mathbb{Z}_{p^{n}}$ with the canonical projections $$\mathbb{Z} / p\mathbb{Z} \stackrel{\lambda_{1}}{\longleftarrow} \mathbb{Z} / p^{2}\mathbb{Z} \stackrel{\lambda_{2}}{\longleftarrow} \mathbb{Z} / p^{3}\mathbb{Z} \stackrel{\lambda_{3}}{\longleftarrow} \cdots$$. 

Despite their origin in function-theoretic ideas, the p-adic live up to their destiny entirely within arithmetic, especially in the *Diophantine equations* as it is natural to check $F(x_{1},\cdots,x_{n})\equiv 0 \pmod{m}$ for all $m \in \mathbb{N}$, and using the chinese remainders theorem, we only need to check the case of $m = p^{v}$, and the p-adic number preserves these information pretty well