#nt #algebra #lectureNote 
>[!note] Main problem
>Find all prime of the form $x^{2}+ny^{2}$, i.e. find all $p=x^{2}+ny^{2}$

# Fermat & Euler
$n=1$, $p=x^{2}+y^{2}$.

**Lemma**: Suppose $N$ is a sum $x^{2}+y^{2}$, let $q|N$, $q=a^{2}+b^{2}$ for some $a,b \in \mathbb{Z}$, then $\frac{N}{q}=c^{2}+d^{2}$. 

*Proof*: Note that $q|a^{2}N-x^{2}q$, so $ay-bx=dq$ for some $d$. Again, $q=a^{2}+b^{2}$, so $ay-bx=d(a^{2}+b^{2})$, hence $a|x+bd$, let $x=ac-bd$, then $y=ad+bc$, hence $\frac{N}{q}=c^{2}+d^{2}$. 

**Theorem**: And odd prime $p$ can be written in the form $x^{2}+y^{2}$ if and only if $p\equiv1\pmod{4}$. (regular problem)

Euler then deal with the problem $p=x^{2}+2y^{2}$ and $p=x^{2}+3y^{2}$. 

**Theorem**: 
1) If $p\equiv1\text{ or } 3\pmod{8}$, then $p=x^{2}+2y^{2}$ for some $x,y \in \mathbb{Z}$. 
2) If $p\equiv1\pmod{12}$, then $p=x^{2}+3y^{2}$ for some $x,y \in \mathbb{Z}$. 

>[!note] Quadraic reaprocity
>$m,q \in \mathbb{Z}$, then define $\left( \frac{m}{q} \right)=\begin{cases}0\qquad&\text{if } m=0 \\ 1 \qquad &\text{if } m\equiv a^{2}\pmod{q} \\ -1 \qquad &\text{otherwise}\end{cases}$ be the Jacobi sumbol for prime $q$. As to general $n=\prod_{i}p_{i}^{\alpha_{i}}$, $\left( \frac{m}{n} \right)=\prod_{i}\left( \frac{m}{p_{i}} \right)^{\alpha_{i}}$
>
>More over, let $p,q$ be distinct odd primes. Then $\left( \frac{p}{q} \right)\cdot \left( \frac{q}{p} \right) = (-1)^{\frac{p-1}{2}\cdot \frac{q-1}{2}}$

In fact, $p|x^{2}+ny^{2}$ for some $x,y$ if and only of $\left( \frac{-n}{p} \right)=1$. And one should note that the theorem completely(more or less) solve the problem of computing $\left( \frac{a}{n} \right)$. 

*Proof*: Let $p^{*}=(-1)^{\frac{p-1}{2}}p$, then it is suffice to show $\left( \frac{p^{*}}{q} \right)=1$ $\Longleftrightarrow$ $p\equiv\pm\beta ^{2}\pmod{4q}$ for some odd integer $\beta$. 
1. "$\impliedby$", simple, check the definition.
2. "$\implies$", both sides depend only on $p\pmod{4q}$. and $p\mapsto\beta^{2}$ depend only on $\beta\pmod{4q}$. Both is half of the hole set, and one is contained in the other, so they must be the same. 

**Lemma**: $D\equiv0\text{ or } 1\pmod{4}$, $D\neq0$. There is a unique $\chi:(\mathbb{Z} / D\mathbb{Z})^{\times}\rightarrow \{ \pm1 \}$, s.t. $\chi([p])=\left( \frac{D}{p} \right)$ for all odd prime $p$. Moreover, $\chi([-1])=\begin{cases}1\  \text{ if } D>0\\ -1\ \text{ if } D<0\end{cases}$ 

*Proof*: 
1. Existence. For positive integer $n$ prime to $D$, define $\chi([n])=\left( \frac{D}{n} \right)$. One has to check that $\chi$ is well defined. 
	1) $D>0$ and $D\equiv1\pmod{4}$. Then $\left( \frac{D}{m} \right)=\left( \frac{m}{D} \right)(-1)^{\frac{D-1}{2}\cdot \frac{m-1}{2}}$, and it is easy to check $\left( \frac{D}{m} \right)=\left( \frac{D}{n} \right)$. 
	2) $D<0$ and $D\equiv1\pmod{4}$. Then $\left( \frac{D}{m} \right)=\left( \frac{-1}{m} \right)\cdot\left( \frac{-D}{M} \right)$, and the rest is same as above. 
	3) $D>0$ and $D\equiv0\pmod{4}$. Let $D=2^{k}D'$, with $k\geq2$. Then $\left( \frac{D}{m} \right)=\left( \frac{2}{m} \right)^{k}\left( \frac{D'}{m} \right)=(-1)^{\frac{m^{2}-1}{8}}\cdot\left( \frac{D'}{m} \right)$, simple discussion show that $\left( \frac{D}{m} \right) =\left( \frac{D}{n} \right)$. 
	4) $D<0$ and $D\equiv0\pmod{4}$. Let $D=-2^{k}D'$, with $k\geq2$. Then $\left( \frac{D}{m} \right)=\left( \frac{-1}{m} \right)\cdot\left( \frac{2}{m} \right)^{k}\left( \frac{D'}{m} \right)= (-1)^{\frac{m-1}{2}}\cdot(-1)^{\frac{m^{2}-1}{8}}\cdot\left( \frac{D'}{m} \right)$, and it is easy to check that this case is correct too. 
2. Condider $\chi([-1])$. Choose positive integer $n\equiv-1\pmod{8D}$. Then we need to compute $\left( \frac{D}{n} \right)$. Condider all four cases as above, then we are done. 

For "$x^{2}+ny^{2}$", consider $D=-4n$ $\rightsquigarrow$ $\chi:(\mathbb{Z} / D\mathbb{Z})^{\times} \rightarrow \{ \pm1 \}$. Then if there is a $x,y \in \mathbb{Z}$, $gcd(x,y)=1$ such that $p|x^{2}+ny^{2}$, then we have $\chi([p])=1$. 

cases of $n=5,27,64$:
1. $n=5$, $p$ odd prime $\neq5$. Then $p=x^{2}+2y^{2}$ <==> $p\equiv1\text{ or } 9\pmod{20}$, $2p=x^{2}+5y^{2}$ <==> $p=2u^{2}+2uv+3v^{2}$ <==> $p\equiv3\text{ or }7\pmod{20}$. In this case, $\left( \frac{-5}{p} \right)=1$ <==> $p\equiv1,3,7,9\pmod{20}$. 
2. $n=27$, $p$ odd prime $\neq3$. Then $p=x^{2}+27y^{2}$ <==> $p\equiv1\pmod{(3)}$, and $2$ is a cubic residue module $p$. 
3. $n=64$, $p$ odd prime. Then $p=x^{2}+64y^{2}$ <==> $p\equiv1\pmod{4}$ and $2,5$ a biquadratic residue module $p$. 

# Lagrange & Legendre
$f(x,y)=ax^{2}+bxy+cy^{2}$, $x,y \in \mathbb{Z}$, $a,b,c \in \mathbb{Z}$, is the quadraic from we are interested in. Of course, the determinate $D=b^{2}-4ac$ is also important. Definition like *primitive*, will not be written out specificly. We say that $m \in \mathbb{Z}$ is **represented** by $f(x,y)$ if $\exists x,y \in \mathbb{Z}$ s.t. $f(x,y)=m$.. and is "prnperly represented" if $gcd(x,y)=1$. If seen $f$ as $\begin{pmatrix}x&y\end{pmatrix}\begin{pmatrix}a&b\\c&d\end{pmatrix}\begin{pmatrix}x\\y\end{pmatrix}$, then $f$ and $g$ are **equivalent** if $B=QAQ^{T}$ for some $Q$, (called properly equivalent if $\det(Q)=1$). 

**Lemma**: $f(x,y)$ a quadraic form, then $m$ can be properly represented by $f$ if and only if $f$ is properly equivalent to a form $mx^{2}+bxy+cy^{2}$. 

*Proof*: "if" is trivial, we only proof "only if". 
Suppose $s,r\in \mathbb{Z}$, with $gcd(s,r)=1$ and $f(s,r)=1$. Take $ps-qr=1$, and consider the matrix $\begin{pmatrix}p&-q\\r&s\end{pmatrix}$, then we have $g(1,0)=f(s,r)=m$. 

**Lemma**: $D\equiv0\text{ or 1}\pmod{4}$, $m$ odd integer, $gcd(m,D)=1$. Then $m$ is properly represented by a primitive form of discriminant $D$ if and only if $D$ is a quadraic residue module $m$. 

*Proof*:
1. $m$ is properly represented by $f$, then $f$ is properly equivalent to $mx^{2}+bxy+cy^{2}$, then $D=b^{2}-4mc$. With $gcd(m,D)=1$, we know $gcd(b,m)=1$, hence $D\equiv b^{2}\pmod{m}$. 
2. If there is a $b^{2}\equiv D\pmod{m}$, we may assume that $B\equiv D\pmod{2}$, hence $b^{2}-D\equiv0\pmod{4m}$. Take $4mc=b^{2}-D$, and let $f(x,y)=mx^{2}+bxy+cy^{2}$. Then $f(1,0)=m$ with discriminant $D$. 