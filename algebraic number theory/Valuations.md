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
Two valuations $|\ |_{1}$ and $|\ |_{2}$ on $K$ are equivalent (the topology are the same) if and only if there is a real number $s>0$ such that one has $|x|_{1} = |x|_{2}^{s}$ for all $x \in K$. 

*Proof*:
<== is simple, so we have to proof ==>. Note that for $x \in K$ if $\{x^{n}\}$ converges into $0$ if and only if $|x|<0$, so we have $|x|_{1}<1 \Longleftrightarrow |x|_{2}<1$. Now fix a $y \in K$ with $|y|_{1}>1$ and $s:=\frac{\log|y|_{1}}{\log|y|_{2}}$. We proof that this $s$ is what we want. For any $x \in K$, suppose $|x|_{1}=|y|_{1}^{\alpha}$, then we use $\frac{m_{i}}{n_{i}}$ to approach to $\alpha$ from above, then $|\frac{x^{n_{i}}}{y^{m_{i}}}|_{1}<1$, so we have $| \frac{x^{n_{i}}}{y^{m_{i}}} |_{2}<1$, hence $|x|_{2} \leq |y|_{2}^{\alpha}$, and let $\frac{m_{i}}{n_{i}}$ converge from below, then $|x|_{2} \geq |y|_{2}^{\alpha}$. Thus $|x|_{1} = |x|_{2}^{s}$. 

**Appoximation Theorem**:
Let $|\ |_{1},\cdots, |\ |_{n}$ be pairwise inequivalent valuations of the field $K$ and let $a_{1},\cdots, a_{n}\in K$ be given elements. Then for every $\epsilon>0$ there exists an $x \in K$ such that $|x-a_{i}|_{i}<\epsilon$ for all $i$.

*Proof*:
WOLG, we assume $a_{1}=1$ and $a_{i}=0$ $i=2,\cdots,n$, and using the fact the the measures are pairwise inequivalent, we are able to find a $z \in K$ such that $|z|_{1}>1$ and $|z|_{i}<1$ (using induction to find $\frac{z^{m}}{1+z^{m}}y$ where $z$ is for the case $n-1$, and $y$ such that $|y|_{1}>1$ and $|y|_{n}<1$). Then we are able to find $\frac{z^{m}}{1+z^{m}}$ that satisfied the properties we want.

**Definition**:
The valuation $|\ |$ is called *nonarchimedean* is $|n|$ stays bounded, for all $n \in \mathbb{N}$. Otherwise it is called *archimedean*. In fact, the valuation is nonarchimedean if and only if $|x+y|\leq \max\{|x|,|y|\}|$ (the *strong triangle inequality*) holds. 

The proof is not so difficult, suppose $|n|\leq N<1$, then $$|x+y|^{n} \leq \sum_{v=0}^{n}\left\lvert\begin{pmatrix}n\\v\end{pmatrix}\right\rvert|x|^{v}|y|^{n-v} \leq N(n+1)|x|^{n}$$. So $|x+y| \leq N^{1/n}(1+n)^{1/n}\max\{|x|,|y|\}$, hence $|x+y|\leq \max\{|x|,|y|\}$. One might also notice that this inequality implies that if $|x| \neq |y|$, then $|x+y| = \max\{|x|,|y|\}$. 

**Proposition**:
Every valuation of $\mathbb{Q}$ is equivalent to one of $|\ |_{p}$ or $|\ |_{\infty}$. 

*Proof*:
If $|\ |$ is nonarchimedean, then take $\mathfrak{a}:=\{a \in \mathbb{Z} : \Vert a \Vert <1 \}$, because it is an nonzero ideal, so we are able to find $p\mathbb{Z}=\mathfrak{a}$. Then it is easy to check that $\Vert a \Vert = |a|_{p}^{s}$ for some $s$. 
If $|\ |$ is archimedean, take two $m,n \in \mathbb{Z}$ and write $m=a_{0}+a_{1}n+\cdots+a_{r}n^{r}$. Hence $\|m\| \leq \sum \|a_{i}\| \cdot \|n\|^{r} \leq \left( 1+ \frac{\log m}{\log n} \right)n \cdot \|n\|^{\log m/\log n}$ and perform the same trick above, we have $\|m\|^{1/\log m} \leq \|n\|^{1/\log n}$ and $\|n\|^{1/\log n} \leq \|m\|^{1/\log m}$. So we have $\|m\|^{1/\log m}= \|n\|^{1/\log n}$. Suppose $c=\|n\|^{1/\log n}$, then $\|n\|=c^{\log n}=n^{s}$ for some fixed $s$. 

Moreover, we will have the folllowing notion:
1. $\mathcal{O}=\{x \in K:v(x)\geq 0\} = \{x \in K : |x|\leq 1\}$,
2. $\mathcal{O}^{*} = \{x \in K : v(x)=0\} = \{x \in K : |x|=1\}$,
3. $\mathfrak{p}= \{x \in K : v(x)>0\} = \{x \in K : |x|<1\}$.
4. $U=1+\mathfrak{p}=\left\{  x \in K : |1-x| < \frac{1}{q^{n-1}} \right\}$.
With $v(x) = -\log|x|$. 

So we are now able to change our view, let $\mathcal{O}$ is an integral domain with field of fraction $K$ and has property that for all $x \in K$, either $x \in \mathcal{O}$ or $x^{-1} \in \mathcal{O}$. Such a ring is called a *valuation ring* as it can be seen as a valuation if a field. We are also able to define the maximal ideal $\mathfrak{p}$ in the sence of $\{ x \in \mathcal{O} : x^{-1} \not\in \mathcal{O} \}$. In particular, an exponential valuation $v$ is called *descrete* if and only if $v(K^{*}) \simeq s\mathbb{Z}$ for some $s$, in other words, it admits a smallest prositive value $s$. One can easily normalize it (which is lettin $s=1$) then we are able to find a $\pi \in \mathcal{O}$ such that $v(\pi)=1$, and $(\pi)$ is then the ideal $\mathfrak{p}$ and $\pi$ is the *prime element*, and we are able to write all $x \in K$  in the form of $u\pi ^{m}$ where $u \in \mathcal{O}^{*}$. Moreover, we define $U^{(n)}=1+\mathfrak{p}^{n}=\left\{  x \in K^{*} : |1-x|< \frac{1}{q^{n-1}}  \right\}$

A simple fact is that $\mathfrak{p}^{n} / \mathfrak{p}^{n+1} \simeq \mathcal{O} / \mathfrak{p}$. 

# Completions
Next, we will focous on completions. The definition is simple, just making all cauchy sequence converge. We denote the completion of $K$ as $\widehat{K}$. 

**Theorem**:(Ostrowski) Let $K$ be a field which is complete with respect toe an archimedean valuation $|\ |$. Then there is a isomorphism $\sigma$ from $K$ to $\mathbb{R}$ or $\mathbb{C}$ satisfying $|a|=|\sigma a|^{s}$ for all $a \in K$ for some fixed $s$. 

*Proof*: We may assume with out loss that $\mathbb{R} \subseteq K$ and that $|\ |$ is an extension of the usual absolute value of $\mathbb{R}$. We then consider the completion $\widehat{\mathbb{Q}}$ of $\mathbb{Q}$, which extend the valuation. In order to proof that $K=\mathbb{R}$ or $\mathbb{C}$, we show that each $\xi \in K$ satisfies a quadratic equation over $\mathbb{R}$. So we consider $f:\mathbb{C} \rightarrow \mathbb{R}$ defined by $f(z)=|\epsilon^{2} - (z+\bar{z})\epsilon + z \bar{z}|$. It is clear that $f$ has a minimun $m$, and we take $S=\{ z \in \mathbb{C}: f(z) =m \} \neq \varnothing$. Moreover, $S$ is bounded and closed, so we can take $z_{0} \in S$ such that $|z_{0}|>|z|$ for all $z \in S$. We hope to proof that $m=0$. If not, it is natural for us to consider shifting the equation a little so as to give ourselves space to work with. Consider the equations $g(x)=x^{2}-(z_{0}+\overline{z_{0}})x+z_{0}\overline{z_{0}}$, we randomly choose some $z \not\in S$, then by building a polynomial $P(x) \in \mathbb{R}[x]$ with degree $n$, consider $P(g(x)) = \prod_{i}(x-\alpha_{i}) = \prod_{i}(x-\overline{\alpha_{i}})$, taking square and let $x=\xi$, we have $|P(g(\xi))|$ is no less than $m^{n}$, and we know that $P(g(\xi))$ is just about the size of $m^{n}$, so if we are now pretty shure that there must be something wrong. In fact, we fix a root $\epsilon$ as a root of monic polynomial $P$, then we are pretty sure that $|P(g(\xi))|$ will be bigger that $m^{n}$, and $|P(g(\xi))|$ will have limit $m^{n}$ if we take $P$ as $x^{n}-\epsilon^{n}$. The rest is to make sure that the $g(z_{0})-\epsilon$ is bigger than $m$, which is simple, just by letting $\epsilon<0$, then the root $z_{1}$ will be bigger than $z_{0}$ in the sense of $|\ |$. 

So the proof is this: take $g'(x)=g(x)-\epsilon$, with root $z_{1}$, so we have $f(z_{1})>m$. Consider $P_{n}=x^{n}-\epsilon ^{n}$, and we know that $|P(g(\xi))|^{2}=f(z_{1})m^{2n-1}$. But $|P(g(\xi))|\leq g(\xi)^{n}+|\epsilon|^{n} = m^{n}+|\epsilon|^{n}$, letting $n$ goes to $\infty$, we know that $f(z_{1})$ cannot be greater than $m$, thus a contradiction.

Now with the help of the theorem, we can focous on the cases of nonarchimedean valuations. We first have a simple proposition $\widehat{\mathcal{O}} / \widehat{\mathfrak{p}} \simeq \mathcal{O} / \mathfrak{p}$. Moreover, we can see the completion as adding elements that is of the form of infinite power series $x=\pi ^{m}(a_{0}+a_{1}\pi+a_{2}\pi ^{2}+\cdots)$. As in the case of p-adic numbers, we are now able to acquire similiar result in general valuation theory. The construction is similiar, we first have $$
\mathcal{O} / \mathfrak{p} \stackrel{\lambda_{1}}{\longleftarrow} \mathcal{O} / \mathfrak{p}^{2} \stackrel{\lambda_{2}}{\longleftarrow} \cdots 
$$
and this gives  us a homomorphism $\mathcal{O} \rightarrow \lim\limits_{\longleftarrow} \mathcal{O} / \mathfrak{p}^{n}$, in fact, the mapping is a isomorphism and a homeomorphism. The same is true for $\mathcal{O}^{*} \rightarrow \lim\limits_{\longleftarrow} \mathcal{O}^{*} / U^{(n)}$. The proof is clear, and notice that $\mathcal{O}^{*}\simeq(\lim\limits_{\longleftarrow} \mathcal{O} / \mathfrak{p}^{n})^{*}$, then the rest is simple. 

Now we introduce the important hensel's lemma:

**hensel's lemma**: If a primitive polynomial $f(x) \in \mathcal{O}[x]$ admits modulo $\mathfrak{p}$ a factorization $f(x)\equiv \overline{g}(x)\overline{h}(x)\pmod{\mathfrak{p}}$ into relatively prime polynomials $\overline{g},\overline{h} \in k[x]$, then $f(x)$ admits a factorization $f(x)=g(x)h(x)$ into polynomial $g,h \in \mathcal{O}[x]$ such that $deg(g)=deg(\overline{g})$ ad $g(x)\equiv \overline{g}(x)\pmod{\mathfrak{p}}$ and $h(x)\equiv \overline{h}(x)\pmod{\mathfrak{p}}$. Here $k= \mathcal{O} / \mathfrak{p}$. 

*proof*: using induction, adding a bit of $\pi ^{n}$ each time, amounting to $g=g_{0}+p_{1}\pi+p_{2}p^{2}+\cdots$ and $h=h_{0}+q_{1}\pi+q_{2}\pi ^{2}+\cdots$. First take $g_{0}$ with dimension $m=deg(\overline{g})$, and $h_{0}$ dimension small such that $g_{0}\equiv g\pmod{\mathfrak{p}}$ and $h\equiv h_{0}\pmod{\mathfrak{p}}$. Then using induction, we have $f-g_{n-1}h_{n-1}\equiv(g_{n-1}q_{n}+h_{n-1}p_{n})\pi ^{n}\pmod{\pi ^{n+1}}$, so we need $g_{n-1}q_{n}+h_{n-1}p_{n}\equiv g_{0}q_{n}+h_{0}p_{n}\equiv f_{n}\pmod{\pi}$, where $f_{n}=\pi ^{-n}(f-g_{n-1}h_{n-1}) \in \mathcal{O}[x]$. Choosing $g_{0}a+h_{0}b\equiv{1}\pmod{\pi}$, we can easily construct the desired $p_{n},q_{n}$. 