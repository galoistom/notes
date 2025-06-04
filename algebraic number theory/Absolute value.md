>[!note] Absolute value
>An absolute value of a field $K$ is a function $K \rightarrow \mathbb{R}$ such that:
>1. $|x|>0$ except for $|0|=0$.
>2. $|x| \cdot |y| = |xy|$.
>3. $|x+y| \leq |x|+|y|$.
>(If $|x+y| \leq \max\{|x|,|y|\}$, then the absolute value is called a *nonarchimedean absolute value*.)

Two absolute value is said to be equivalent if they have the same topology over $K$, where the opensets are $U(a,\epsilon)=\{x:|x-a|<\epsilon\}$. The ondition is equivalent to $|\cdot|_1=|\cdot|_2^a$ for some $a \in K$ or $|a|_1<1$ if and only if $|a|_2<1$. 

We now determin the equivalent classes of the absolute value on $\mathbb{Q}$. 
>[!note] Ostrowski's theorem
>Let $|\,|$ be a nontrivial absolute value on $\mathbb{Q}$. 
>1. If $|\,|$ is archimedean, then $||$ is equivalent to $|\,|_{\infty}$ 
>2. If $|\,|$ is nonarchimedean, then it is equivalent to $|\,|_p$ for some prime $p$.

Proof:(sketch)
	1. let $m,n$ be two integers greater than 1. We then write  $$m=a_0+a_1n+\cdots+a_rn^r$$ with $0 \leq a_i<n$ and $n^r<m$. Let $N=max\{1,|n|\}$, then $$|m|\leq \sum_{i=0}^{r} |a_i||n^i| \leq \sum_{i=0}^{r}|a_i|N^r \leq (1+r)nN^r$$ where $r\leq\frac{\ln m}{\ln n}$, thus $|m| \leq (1+\frac{\ln m}{\ln n})nN^{\frac{\ln m}{\ln n}}$, by replacing $m$ with $m^t$ and $t$ large enough, we get $|m|\leq N^{\frac{\ln m}{\ln n}}$.
	2. If for all $n>1$, we have $|n|>1$, then $N=|n|$, hence $|m|^{\frac{1}{\ln m}} \leq |n|^{\frac{1}{\ln n}}$. By symmetry, we get $|m|^{\frac{1}{\ln m}} = |n|^{\frac{1}{\ln n}}$ for all $m,n>1$, suppose $c=|m|^{\frac{1}{\ln m}} = |n|^{\frac{1}{\ln n}}$, then we get $|n|=n^{\ln c}$, which is equivalent to $|\,|_{\infty}$.
	3. If for some $n>1$, we have $|n|\leq1$, which implies that $|m|\leq1$ for all $m>1$. Consider the local ring $A:=\{a \in K:|a|\leq1\}$ and its maximum ideal $\mathfrak{m}:=\{a \in K:|a|<1\}$. Then $\mathbb{Z}\subset A$, then $\mathfrak{m} \cap \mathbb{Z}$ is a prime ideal $(p)$ for some prime $p$. This implies that $|m|=1$ if $p$ dose not divide $m$, hence $|np^r|=|p|^r$ if $gcd(n,p)=1$. Take $a$ such that $|p|=(\frac{1}{p})^a$, then $|\,|=|\,|_p^a$, hence equivalent to $|\,|_p$.

>[!note] Product fromula
>For $p=2,3,\cdots ,\infty$, let $|\,|_p$ be the corresponding normalized absolute value on $\mathbb{Q}$. For any $a \in \mathbb{Q}$, we have $$\prod |a|_p = 1 (\text{product over all } p \text{ inlcluding } \infty). $$

The proof is simple, note that there are only finitly many $p$ such that $|a|_p \neq 1$, thus the porduct converges, then if $p|a$, we have $|a|_p=p^{-V_p(a)}$, if $p=\infty$, then $|a|_p=|a|$.

We extend the definition of primes to a number field $K$ by letting a prime to be an equivalent class of value. Then there exists exactly one prime of $K$ for: 
1. Each prime ideal $\mathfrak{p}$ of $\mathcal{O}_K$, $|a|_{\mathfrak{p}}=(\frac{1}{\mathbb{N}\mathfrak{p}})^{ord_{\mathfrak{p}}}=(\mathcal{O}_K:(a))^{-1}$.(c.f.[[Finiteness of class number]])
2. Each real embedding $\sigma:K \hookrightarrow \mathbb{R}$, $|a|=|\sigma a|$.
3. Each nonreal complex embedding $\sigma:K \hookrightarrow \mathbb{C}$, $|a|=|\sigma a|^2$.
One might notice that the product formula exists for general number field as well.

>[!note] Weak approximation theorem
>Let $|\cdot|_1,|\cdot|_2, \cdots, |\cdot|_n$ be nontrivial inequivalent absolute values of a number field $K$, and let $a_1,a_2,\cdots,a_n$ be elements of $K$. For every $\epsilon>0$, there is an element $a \in K$ such that $|a-a_i|<\epsilon$ for all $i$.

Proof: 
	It is sufficent to proof case of $a_1=1$ and $a_i=0$ for all $i \neq 0$. We proof by induction on $n$. $n=2$ is trivial, now suppose $n-1$ has been proved, consider the case $n$. By induction hypothesis, we choose $|b|_1>1$ and $|b|_i<1$ for $i=2,3,\cdots,n-1$, and $|c|_1>1$, $|c|_n<1$. If $|b|_n<1$, then $a=b^r$ with $r$ sufficently large works. If $|b|_n=1$, then $a=(cb)^r$ works for sufficently large $r$. If $|b|_n>1$, then let $a'=\frac{cb^r}{1+b^r}$ and let $r$ sufficently large, we have $|a'|_1>1$ and $|a'|_i<1$ for $i \neq 1$, then let $a=a'^r$, we have $|a|_1$ converges to 1 and $|a|_i$ converges to 0.

>[!note] Hensel's lemma
>Let $A$ be a discrete valusation ring, and $\pi$ gengerates its maximal ideal, and $k$ be its residue field. For $f \in A[X]$, write $\bar{f}$ be its image in $k[X]$, suppose $\bar{f}=g_0h_0$ where $g_0,h_0 \in k[X]$ and are relatively prime. Then if $f$ is monic, $f$ can be factor as $f=gh$ such that $\bar{g}=g_0$ and $\bar{h}=h_0$. Moreover, $h,g$ are uniquely determined and $(g,h)=A[X]$.

Proof:
	1. We frist proof that $(g,h)=A[X]$. Let $\mathfrak{m}$ be the maximal ideal of $A$, and $M=A[X]/(g,h)$, note that we have $\bar{g},\bar{h}$ are coprime, then we have $(g,h)+\mathfrak{m}A[X]=A[X]$, quotient by $(g,h)$, we have $\mathfrak{m}M=M$, then by Nakayama's lemma, we have $M=0$. Furthermore, we can take $u,v\in A[X]$ such that $ug+vh=1$ and $deg(u)<def(g)$, $deg(v)<deg(h)$.
	2. We then proof the uniqueness of $g,h$, suppose not, then there exists $r,s \in A[X]$ such that $rg+sh'=1$, then $g'=g'rg+g'sh'=g'rg+ghs$, hence $g$ divides $g'$, thus $g=g', h=h'$. 
	3. We proof the existance of $g,h$. We are given that there exists $g_0,h_0$ such that $f-g_0h_0 \in \pi A[X]$. We proof the statement by induction. Suppose we have $g_n,h_n$ such that $f-g_nh_n \in \pi^{n+1} A[X]$, we want to find $u,v$ such that $f-(g_n+\pi^{n+1}u)(h_n+\pi^{n+1}v) \in \pi^{n+2} A[X]$ and $deg(u)<deg(g_0)$,$deg(v)<deg(h_0)$, i.e. $f-g_nh_n-\pi^{n+1}(h_nu+g_nv) \in \pi^{n+2}A[X]$, which is to say we need $h_nu+g_nv \equiv (f-g_nh_n)/\pi^{n+1} \pmod{\pi A[X]}$. Note that we have $g_0,h_0$ coprime, then we are done. 

>[!note] Extensions of nonarchimedean absolute values
>Let $K$ be complete with respect to a discrete absolute vallue $|\,|_K$,  and let $L$ be a finite separable extension of $K$ of degree $n$. Then $|\,|_K$ extends uniquely to a discrete absolute value $|\,|_L$ on $L$,  and $L$ is complete for the extended absolute value. For all $\beta \in L$, $|\beta|_L=|Nm_{L/K} \beta|_K^{1/n}$.

Proof:
	1. Let $A$ be a discrete valusation ring in $K$, and let $B$ be its integral closure in $L$. Let $\mathfrak{p}$ be the maximal ideal of $A$. We know that $B$ is a [[Dedekind domain]], and the absolute values of $L$ extending $|\,|_{\mathfrak{p}}$ correspond tp the ideals of $B$ lying over $\mathfrak{p}$.
	2. Suppose there are distinct prime ideals $\mathfrak{P}_1,\mathfrak{P}_2$ dividing $\mathfrak{p}$. There will be a $\beta \in B$ such that $\mathfrak{P}_1 \cap A[\beta] \neq \mathfrak{P}_2 \cap A[\beta]$. Note that $A[\beta] \simeq A[X]/(f(X))$, where $f$ is the minimal polynomial of $\beta$ over $K$, and the fact that $f$ is irriducible and $A$ complete, Hensel's lemma shows that $\bar{f}$ must be a power of irriducible polynomial in $k[X]$, where $k=A/\mathfrak{p}$. Then $A[\beta]/\mathfrak{p}A[\beta] \simeq k[X]/(\bar{f}(X))$ is a local ring, contradiction the fact that $A[\beta]$ has two prime ideals containing $\mathfrak{p}$.
	3. Extend $|\,|_{\mathfrak{p}}$ to a galois closure of $L$, then for $\sigma \in Gal(L'/K)$ we have $|\beta|_L=|\sigma \beta|_L$ using the uniqueness we proved above. Thus $|Nm(\beta)|_K=|\prod \sigma\beta|_{L'}=|\beta|_{L'}^n$.
	4. The completeness is trivial.

>[!note] Newton's polygon
>Let $K$ be complete with respect to a discrete absolute value. Let ord be the additive valuation $ord:K^{\times}  \twoheadrightarrow \mathbb{Z}$, and extend ord to a valuation $ord:K^{al\times} \rightarrow \mathbb{Q}$. For a polynomial $f(x)=a_0x^n+a_1x^{n-1}+ \cdots + a_n$ where $a_0=1,a_i \in K$. Let Newton's polygon be the part of the convex hull of $P_i=(i,ord(a_i))$ that starts at $P_0$ and ends at $P_n$.

The most important porposition related to the concept is that if $ch(K)=0$, and $f\in K[x]$ has segements of $x-length$ $m_i$ and slope $s_i$. Then $f(x)$ has exactly $n_i$ roots $\alpha \in K^{al}$ with $ord(\alpha)=s_i$.

Proof:
	1. We discuss the question in a sufficently large extension of $K$. then we need to prove that if $f=\prod(x-\alpha_j)$ and have exactly $n_i$ of the $\alpha_j$ that have order $s_i$, then the Newton's polygon of $f$ has a segment of slope $s_i$ and $x-length$ $n_i$. 
	2. We proof this by induction on $deg(f)$. the case $n=1$ is obvious. Suppose it for $n$, and put $g(x)=(x-\alpha)f(x)=x^{n+1}+b_1x^n+\cdots+b_{n+1}$. Note that $b_i=a_i-\alpha a_{i-1}$.
	3. If $ord(\alpha)<s_1$. Then the Newton polygon of $g$ is obtained by adding a segment of slope $ord(\alpha)$ and $x-length$ 1, and moving the Newton polygon of $f$ to start at $(1,ord(\alpha))$. This is what the proposition predicts.
	4. If $ord(\alpha)=s_1$. In this case, the initial segment of slpoe $s_1$ is lengthened by 1, ans the rest of the polygon is as before. This is what the proposition predicts. The rest cases is similar.

>[!note] Unramified extensions of a local field
>Let $K$ be a field complete with respect to a discrete absolute value $|\,|$. Let $A=\{\alpha\in K:|\alpha|\leq1\}$ and $\mathfrak{m}=\{\alpha\in A:|\alpha|<1\}$, then the field $k=A/\mathfrak{m}$ is called the residue field of $K$.

There is an equivalence between the category of finite unramified extensions of $K$ and the category of finite (separable) extensions of $k$.

Moreover, we have that $L/K$ is totally ramified if and only if $L=K[\alpha]$ with $\alpha$ a root of an Eisenstein polynomial.(The proof is easy)

>[!note] Ramification groups
>Let $L$ be a finite galois extension of $K$, and assume that the residue field is perfect. Let $G:=Gal(L/K)$, then it preserve $B:=\{\alpha\in L : |\alpha|\leq1\}$ and $\mathfrak{p}:=\{\alpha\in L:|\alpha|<1\}$. We then define $G \geq G_1 \geq G_2 \cdots$ where $\sigma\in G_i$ if and only if $|\sigma\alpha-\alpha|<|\Pi|^i$ for all $\alpha\in B$ and $\Pi$ a prime element of $L$.

>[!note] Krasner's lemma
>Let $\alpha,\beta\in K^{al}$, and assume that $\alpha$ is separable over $K[\beta]$. If $\alpha$ is closer to $\beta$ than any conjugate of $\alpha$, then $K[\alpha]\subset K[\beta]$.

Proof:
	Let $\sigma$ be an embedding of $K[\alpha,\beta]$ in to $K^{al}$ fixing $K[\beta]$, then we only need to proof that $\sigma\alpha=\alpha$. But we have $|\sigma\alpha-\beta|=|\alpha-\beta|$, hence $|\sigma\alpha-\alpha|=|\sigma\alpha-\beta+\beta-\alpha|\leq|\alpha-\beta|$. Contradicting the hypothesis.

From this we gather that if $f,g\in K[x]$ is close enough, we have that the feld gengerated by the root of $f$ and $g$ are the same.