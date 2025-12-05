#algebra #nt
[[Valuations]]
Let $v$ be an arbitrary exponential valuation of the field $K$ and let $f(x)=a_{0}+a_{1}x+\cdots+a_{n}x^{n} \in K[x]$ be a polynomial satisfying $a_{0}a_{n}\neq0$. To each term $a_{i}x^{i}$ we associate a point $(i,v(a_{i}))\in \mathbb{R}^{2}$, ignoring however the point $(i,\infty)$ if $a_{i}=0$. We now take the lower convex envelpoe of the set of points $\{ (0,v(a_{0})), (1,v(a_{1})), \cdots, (n,v(a_{n})) \}$. This produces a polygonal chain which is called the **Newton polygon** of $f(x)$. 

The importance can be seen in the follow proposition: 

**Proposition**: Let $f(x)=\sum_{i} a_{i}x^{i}$, $a_{0}a_{n}\neq0$, be a polynomial over the field $K$, $v$ an exponential valustion of $K$, and $w$ an extension to the splittin field $L$ of $f$. If $(r,v(a_{r})) \leftrightarrow (s,v(a_{s}))$ is a line segment of slope $-m$ occurring in the Newton polygon of $f$, then $f(x)$ has percisely $s-r$ roots $\alpha_{1}, \cdots, \alpha_{s-r}$ of value $w(\alpha_{1})=w(\alpha_{2})=\cdots=w(\alpha_{s-r})=m$. 

*Proof*: WOLG, we may assume $a_{n}=1$. We number the roots $\alpha_{1}, \cdots, \alpha_{n} \in L$ of $f$ in such a way that $$
\begin{align}
w(\alpha_{1}) = \cdots = w(\alpha_{s_{1}}) = m_{1},\\
w(\alpha_{s_{1}+1}) = \cdots = w(\alpha_{s_{2}}) = m_{2}, \\
\cdots \qquad \cdots \qquad \cdots \qquad \cdots \\
w(\alpha_{s_{t}+1}) = \cdots = w(\alpha_{n}) = m_{t+1}
\end{align}
$$
where $m_{1}<m_{2}< \cdots <m_{t+1}$. Viewing the coefficents $a_{i}$ as elementary symetic functions of the roots $\alpha_{j}$, we immediately have $v(a_{n-t})\geq tm_{1}$, ($0< t<s_{1}$), and $v(a_{n})=0$, $v(a_{n-s_{1}})=s_{1}m_{1}$, similar result for $t$ greater than $s_{1}$. In pact, $v(a_{n-s_{i}}) = s_{1}m_{1} + \sum(s_{k}-s_{k-1})m_{k}$, the $(i,a_{i})$ must be above the line segment of $(n,0),\,(n-s_{1}, s_{1}m_{1}), (n-s_{2}, s_{1}m_{1}+(s_{2}-s_{1})m_{2}), \dots$. And the slope is percisely $-m_{i}$.

Moreover, if the valuation $v$ admits a unique extension $w$ to the splitting field $L$ of $f$, then the factorization $f(x) = a_{n}\prod ^{r}_{j=1}f_{j}(x)$, where $f_{j}= \prod_{w(\alpha_{i})=m}(x-\alpha_{i}) \in K[x]$. 