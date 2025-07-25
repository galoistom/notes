# The p-adic Numbers
>[!note] Definition
>Fix a prime number $p$. A *p-adic number is a formal infinite series*: $a_{0} + a_{1}p + a_{2}p^{2} + \dots$, where $0 \leq a_{i} < p$ for all $i = 0,1,2,\dots$ The set of all p-adic integers is denoted by $\mathbb{Z}_{p}$.

In fact, we have $a\equiv a_{0}+a_{1}p+\dots+a_{n-1}p^{n-1} \pmod{p^{n}}$. The idea of p-adic numbers come from the Taylor expansion of $f = \frac{g}{h} \in \mathbb{C}(z)$. 

In analogy with the laurent series $f(z)=\sum_{v=-m}^{\infty}a_{v}(z-a)^{v}$, we now extend the domain of p-adic integers in to that of the formal series $$\sum_{v=-m}^{\infty}a_{v}p^{v} = a_{-m}p^{-m}+ \cdots + a_{-1}p^{-1} + a_{0} + a_{1}p + \cdots$$, where $m \in \mathbb{Z}$ and $0\leq a_{v}<p$. Such series we call simply *p-adic numbers* and we write $\mathbb{Q}_{p}$ for the set of all these p-adic numbers. If $f \in \mathbb{Q}$ is any rational number, then we write $f = \frac{g}{h} p^{-m}$ where $g,h \in \mathbb{Z}$ and $(gh,p)=1$, and move the series of $\frac{g}{h}$ backwards $m$ to $\sum_{v=-m}^{\infty}a_{v}p^{v}$. In this way we obtains a canonical map $\mathbb{Q} \rightarrow \mathbb{Q}_{p}$, which takes $\mathbb{Z}$ to $\mathbb{Z}_{p}$ and is injective. 

**Remarks**:
The p-adic numbers can be considered as $\lim\limits_{\longleftarrow}\mathbb{Z} / p^{n}\mathbb{Z}$ with the canonical projections $$\mathbb{Z} / p\mathbb{Z} \stackrel{\lambda_{1}}{\longleftarrow} \mathbb{Z} / p^{2}\mathbb{Z} \stackrel{\lambda_{2}}{\longleftarrow} \mathbb{Z} / p^{3}\mathbb{Z} \stackrel{\lambda_{3}}{\longleftarrow} \cdots$$. 

Despite their origin in function-theoretic ideas, the p-adic live up to their destiny entirely within arithmetic, especially in the *Diophantine equations* as it is natural to check $F(x_{1},\cdots,x_{n})\equiv 0 \pmod{m}$ for all $m \in \mathbb{N}$, and using the chinese remainders theorem, we only need to check the case of $m = p^{v}$, and the p-adic number preserves these information pretty well by the folllowing proposition.

**Proposition**:
Let $F(x_{1},\cdots,x_{n})$ be a polynomial with integer coefficents, and fix a prime number $p$. The congruence $F(x_{1},\cdots,x_{n})\equiv 0 \pmod{p^{v}}$ is solvable for arbitrary $v\geq 1$ if and only if the equation $F(x_{1},\cdots x_{n})=0$ is solvable in p-adic integers.

*Proof*:
We view $\mathbb{Z}_{p}$ as the projective limit $\lim\limits_{\longleftarrow}\mathbb{Z} /p^{n}\mathbb{Z}$, then it is obvious for the <== direction. On the other hand, if we are able to find a solution in $\lim\limits_{\longleftarrow}\mathbb{Z} /p^{n}\mathbb{Z}$ then we are done, but it is not always the case. 
We will now only proof the verison of $n=1$ as it is basicially the same. take $x_{v}:=\{x:x \in \mathbb{Z} / p^{v}\mathbb{Z}\}$ and view $(x_{v})$ as a sequence, choose a $x_{1}$ to be an element appeared infinite times, and creat a sub "sequence" $\{x_{v}^{(1)}\}$ such that all $x_{v}^{(1)}\equiv x_{1} \pmod{p}$ and $F(x^{(1)}_{v})\equiv 0 \pmod{p}$, like wise choose for 2,3,..., and we are able to find an element in $\lim\limits_{\longleftarrow}\mathbb{Z} / p^{n}\mathbb{Z}$. 

# The p-adic [[Absolute value]]
One immediately notice that the formal series $a_{0}+a_{1}p+\cdots$ does not converge in general. To solve this, we are now introducing another Valuation for p-adic numbers. In fact, the way of writing the p-adic numbers is vary similiar to $a_{0} + a_{1}\left( \frac{1}{10} \right)+a_{2}\left( \frac{1}{10} \right)^{2} + \cdots$ of real numbers $\leq 10$. 

Let $a=\frac{b}{c}$ with $b,c \in \mathbb{Z}$ be a nonzero rational number. We extract from $b$ and $c$ as high a power of the prime number $p$a as possible, $a=p^{m} \frac{b'}{c'}$ with $(b'c',p)=1$, and set $|a|_{p} = \frac{1}{p^{m}}$. Thus the measures nolonger represent how large the number is but rather how many $p$ is contains, and in this way, the formal series converges.

To be more specific, we define $v_{p}:\mathbb{Q} \rightarrow \mathbb{Z} \cup \{\infty\}$, with:
1. $v_{p}(a) = 0 \Longleftrightarrow a=0$,
2. $v_{p}(ab)=v_{p}(a)+ v_{p}(b)$,
3. $v_{p}(a+b)\geq \min\{v_{p}(a),v_{p}(b)\}$,

Then define $|a_{p}| = p^{-v_{p}(a)}$. Moreover, we define $|a|_{p}$ to be the natural absolute value.

**Proposition**:
For every rational number $a \neq 0$, one has $\prod_{p}|a|_{p}=1$, where $p$ varies over all prime numbers as well as the symbol $\infty$. 

*Proof*:
In the prime factorization $a = \pm \prod_{p \neq \infty} p^{v_{p}}$ of $a$, the exponent $v_{p}$ is precisely the exponential valuation $v_{p}(a)$ and the sign equals to $\frac{a}{|a|_{\infty}}$. The equation holds obviously.

**Remark**:
The notion of $|\ |_{\infty}$ is motivated by the analogy of the field of rational numbers $\mathbb{Q}$ with the rational function field $k(t)$ over a field $k$, with which we started our consideration. Take $\mathfrak{p}$ be a prime ideal (in this case $(p(x))$ where $p$ prime), and if $f$ contains $m$ $p$, we say $v_{\mathfrak{p}}(f)=m$, and $|f|_{\infty}$ is $-deg(f)$. And we are still able to get the same result $\prod_{\mathfrak{p}}|f|_{\mathfrak{p}}=1$. 

A sequence $\{x_{n}\}$ in $\mathbb{Q}$ is called *nullsequence* with respect to $|\ |_{\mathfrak{p}}$ if $|x_{n}|_{\mathfrak{p}}$ is a sequence converging to 0 in the usral sense.

**Definition**:
Let the Cauchy sequences form a ring $R$, the null sequences form a maximal ideal $\mathfrak{m}$, and we define afresh the field of p-adic numbers to be residue class field $\mathbb{Q}_{p}:R / \mathfrak{m}$. And $\mathbb{Q}$ is embed into $\mathbb{Q}_{p}$ by associating to every $a \in \mathbb{Q}$ with constant sequence $(a,a,a,\cdots)$. Taking $|x|_{p}:= \lim_{ n \to \infty }|x_{n}|_{p}$, we extend the p-adic valuation to $\mathbb{Q}_{p}$. In this case, the exponential valuation $v_{p}:\mathbb{Q}_{p} \longrightarrow \mathbb{Z} \cup \{\infty\}$ will be $v_{p}(x_{n}) = -\log_{p}|x_{n}|_{p}$, and $v_{p}(x)=v_{p}(x_{n})$ for large enough $n$. 

**Proposition**:
The set $\mathbb{Z}_{p}:=\{x \in \mathbb{Q}_{p} : |x|_{p} \leq 1\}$ is a subring of $\mathbb{Q}_{p}$. It is the closure with respect to $|\ |_{p}$ of the ring $\mathbb{Z}$ in the field $\mathbb{Q}_{p}$. 

*Proof*:
It is clear that $\mathbb{Z}_{p}$ is closed under addition and multiplication. If $\{x_{n}\}$ is a Cauchy sequence in $Z$ and $x=\lim_{ n \to \infty }x_{n}$, then $|x|_{p} \leq 1$. Conversly, if $x=\lim_{ n \to \infty }x_{n} \in \mathbb{Z}_{p}$, $|x_{n}|_{p}\leq 1$ for large enough $n$. Choosing $y_{n}\equiv x_{n}\pmod{p^{n}}$ and $y_{n} \in \mathbb{Z}$, we know that $x_{n}$ is in the closure of $\mathbb{Z}$. 

**Proposition**:
The homomorphism $\mathbb{Z}_{p} \longrightarrow \lim\limits_{\longleftarrow} \mathbb{Z} / p^{n}\mathbb{Z}$ is an isomorphism. Moreover, $\mathbb{Z}_{p} \simeq \mathbb{Z}[[X]] / (X-p)$. 

# Valuations
**Definition**:
A *Valuation* of a field $K$ is a function $|\ |:K \rightarrow R$ enjoying the properties:
1) $|x|>0$, and $|x|=0$ $\Longleftrightarrow$ $x=0$,
2) $|xy| = |x||y|$,
3) $|x+y| \leq |x|+|y|$.

We tacitly exclude the sequel the case where $|\ |$ is the trivial valuation of $K$ which satisfied $|x|=1$ for all $x \neq0$. Define the distance bewteen two points $x,y$ to be $d(x,y) = |x-y|$ makes $K$ into a metric space, hence a topological space.

**Proposition**:
Two valuations $|\ |_{1}$ and $|\ |_{2}$ on $L$