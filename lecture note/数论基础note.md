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
1. $n=5$, $p$ odd prime $\neq5$. Then $p=x^{2}+2y^{2}$ <\==> $p\equiv1\text{ or } 9\pmod{20}$, $2p=x^{2}+5y^{2}$ <\==> $p=2u^{2}+2uv+3v^{2}$ <\==> $p\equiv3\text{ or }7\pmod{20}$. In this case, $\left( \frac{-5}{p} \right)=1$ <\==> $p\equiv1,3,7,9\pmod{20}$. 
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

**Definition**: A primitive positive defintie form $ax^{2}+bxy +cy^{2}$ is said to be "reduced" if $\lvert b \rvert\leq a\leq c$ and $b\geq0$ if $\lvert b \rvert=a$ and $a=c$. 

**Theorem**: Every positive definte form is properly equivalent to a unique reduced form

*Proof*: 
1. Let $a=\min\{ a'x^{2}+b'xy+c'y^{2}:(x,y)\neq(0,0) \}$. Then $a'x^{2}+b'xy+c'y^{2}$ is properly equivalent to a form $ax^{2}+b''xy+c''y^{2}$. There exists $k\in \mathbb{Z}$ such that $\lvert 2ak+b'' \rvert\leq a$, let $b=2ak+b''$, $c=ak^{2}+b''k+c''$. Get $ax^{2}+bxy+cy^{2}$ with $\lvert b \rvert\leq a$ and $a\leq c$. 
2. Let $ax^{2}+bxy+cy^{2}$ and $a'x^{2}+b'xy+c'y^{2}$ are reduced forms. Suppose they are properly equivalent $\lvert b \rvert\leq a\leq c$. Then $ax^{2}+bxy+cy^{2}=a\left( x+\frac{b}{2a}y \right)^{2}+\left( c-\frac{b^{2}}{4a} \right)y^{2}$. If $\lvert y \rvert\geq2$, then $ax^{2}+bxy+cy^{2}> c\geq a$. If $\lvert y \rvert=1$, may assume that $y=1$, when $x\neq0$, $\left\lvert  x+\frac{b}{2a}  \right\rvert\geq \frac{\lvert b\rvert}{2a}$, so $ax^{2}+bxy+cy^{2}\geq a\left( \frac{\lvert b \rvert}{2a} \right)^{2}+\left( c-\frac{b^{2}}{2a} \right)=c$. Therefore $a=\min\{ ax^{2}+bxy+cy^{2} \}$, $ax^{2}+bxy+cy^{2}=a$ if and only if $(x,y)=(\pm1,0)$, (and $(0,\pm1)$ if $a=c$). Note that $c=\min\{ ax^{2}+bxy+cy^{2}:(x,y)\in \mathbb{Z}-\mathbb{Z}(0,1) \}$. 
3. With this, we are able to distinguish $a,c$, but can $ax^{2}+bxy+cy^{2}\sim ax^{2}-bxy+cy^{2}$? In fact, it cannot be true, if they can, consider $(x,y)=(\pm1,0)\&(0,\pm1)$, then we know that the matrix must be $I$ or $-I$. 

**Definition**: Say two forms in the same **class** if thay are properly equivalent. Let $h(D)$ to be the number of classes of primitive positive definite forms. 

**Theorem**:
1. $h(D)<+\infty$.
2. $h(D)=$ the number of reduced form of discriminant $D$. 

*Proof*: $-D=4ac-b^{2}\geq4ac-a^{2}\geq3ac$, so $c< -D$, hance $(a,b,c)$ can only take finite many values.

We consider some small cases:

| $D$  |                                                                 |
| ---- | --------------------------------------------------------------- |
| -3   | $x^{2}+xy+y^2$                                                  |
| -4   | $x^{2}+y^{2}$                                                   |
| -7   | $x^{2}+xy+2y^{2}$                                               |
| -8   | $x^{2}+2y^{2}$                                                  |
| -11  | $x^{2}+xy+3y^{2}$                                               |
| -12  | $x^{2}+3y^{2}$                                                  |
| -15  | $x^{2}+xy+4y^{2}$, $2x^{2}+xy+2y^{2}$                           |
| -16  | $x^{2}+4y^{2}$                                                  |
| -20  | $x^{2}+5y^{2}$, $2x^{2}+2xy+3y^{2}$                             |
| -28  | $x^{2}+7y^{2}$                                                  |
| -56  | $x^{2}+14y^{2}$, $2x^{2}+7y^{2}$, $3x^{2}\pm2xy+5y^{2}$         |
| -108 | $x+27y^{2}$, $4x^{2}\pm2xy+7y^{2}$                              |
| -256 | $x^{2}+64y^{2}$, $5x^{2}\pm2xy+13y^{2}$, "$4x^{2}+4xy+17y^{2}$" |

Back to $p=x^{2}+ny^{2}$:

**Proposition**: If $h(-4n)=1$, then $\exists x,y\in \mathbb{Z}$, $p=x^{2}+ny^{2}$ <==> $\left(\frac{-n}{p}\right)=1$. 

**Theorem**: let $n$ be a positive integer, then $h(-4m)=1$ <==> $n=1,2,3,4,7$.

*Proof*: 
" \==> " is simple. 
" \<== ", assume that $h(-4n)=-1$. 
1. $n$ must be a prime power. Otherwise, therer exists positive integers $1<a<b$. $gcd(a,b)=1$, $ax^{2}+by^{2}$ is a reduced form different from $x^{2}+ny^{2}$, discriminant=-4ab=-4n. Thus $h(-4n)\geq2$. 
2. Assume that $n=2^{r}$, $r\geq3$. When $r\geq4$, $4x^{2}\pm4xy+(2^{r-1}+1)y^{2}$, thus $h(-4n)\geq3$. In the case $r=3$, $3x^{2}\pm2xy+3y^{2}$ are reduced form, so $h(-4n)\geq3$. 
3. Assume that $n=p^{r}$, $r>1$, $p$ odd prime. Let $b=\pm2$, then $ac=p^{r}+1$, it is immediately clear that $p^{r}+1$ cannot be a power of 2 (if $r$ even, then $ac\equiv2\pmod{4}$; if not, $p+1|p^{r}+1$). So $p^{r}$ failed when $r>1$.
4. $n=p$ a odd prime. Similar argument tells us that $p$ must be of the form $2^{q}-1$. Take $b=6$, we know that $ac=2^{q}+8$, which cannot be a prime or a $2^{k}$, the only exception is that the factors are too small, i.e. $2^{q-3}+1<6$, $q=0,1,2,3,4,5$, so $p=3,7,31$. To rule out $p=31$, $5x^{2}\pm4xy+7y^{2}$ is reduced form, hance $h(-124)\geq3$.

# Elementry genus group
Two primitive prositive definite forms of discriminant $D$ are said to be in the same genus if they represent the same value in $(\mathbb{Z} / D\mathbb{Z})^{\times}$, $D\equiv0,1\pmod{4}$

**Definition**: Let **Principle form** be:
$$
\begin{cases}x^{2}-\frac{D}{4}y^{2} \qquad &\text{if } D\equiv0\pmod{4} \\
x^{2}+xy+\frac{1-D}{4}y^{2}\qquad &\text{if } D\equiv1\pmod{4}\end{cases}
$$

**Lemma**: Let $f(x,y)$ be a primitive form and $M\in \mathbb{Z}_{>0}$. Then $\exists x,y\in \mathbb{Z}$ such that $gcd(f(x,y),M)=1$. 

*Proof*: We can reduce it to the case of $M$ prime. Put $f(x,y)=ax^{2}+bxy+cy^{2}$, $a,b,c\in \mathbb{Z}$, $gcd(a,b,c)=1$, $f(1,0)=a$, $f(0,1)=c$, $f(1,1)=a+b+c$, as $gcd(a,b,c)=1$, one of them must be prime to $p$. 

**Lemma**: $D\in \mathbb{Z}_{<0}$, $D\equiv0,1\pmod{4}$, $\chi:(\mathbb{Z} / D\mathbb{Z})^{\times}\rightarrow \{ \pm1 \}$, $\chi([p])=\left( \frac{D}{p} \right)$, $ker(\chi)\subset \mathbb{Z}$, then:
1. The values in $(\mathbb{Z} / D\mathbb{Z})^{\times}$ represented by principle form a subgroup $H$ of $ker(\chi)$.
2. The values in $(\mathbb{Z} / D\mathbb{Z})^{\times}$ represented by $f(x,y)$ form a coset of $H$ in $ker(\chi)$. 

*Proof*:
1. If $m$ is represented by $f(x,y)$ of discriminant $D$, then $[m]\in ker(\chi)$. Assume $D\equiv0\pmod{4}$, there exists $x,y\in \mathbb{Z}$ $m=ax^{2}+bxy+cy^{2}=f(x,y)$. PUt $d=gcd(x,y)$l, $x'=\frac{x}{d}$, $y'=\frac{y}{d}$, $m'=\frac{m}{d^{2}}=ax'^{2}+bx'y'+cy'^{2}$, $gcd(x',y')=1$ , $\chi([m])=\chi([m'd^{2}])=\chi([m'])$, so we may assume that $gcd(x,y)=1$. Then $f(x,y)$ is properly equivalent to some $mx^{2}+Bxy+Cy^{2}$ $D=B^{2}-4mC$, as $2|B$, $m$ odd, $gcd(B,m)=1$. $\chi([m])=\left( \frac{D}{m} \right)=\left( \frac{B^{2}-4mC}{m} \right)=\left( \frac{B^{2}}{m} \right)=1$. 
2. $f_{0}(x,y)=x^{2}+ny^{2}$, $D=-4n$, let $(x,y)\in \mathbb{Z}-\{ (0,0) \}$, $(u,v)\in \mathbb{Z}-\{ (0,0) \}$, $gcd(f_{0}(x,y),D)=1$, then $(x^{2}+ny^{2})(u^{2}+nv^{2})=(xu-nyv)^{2}+n(xv+yu)^{2}$. So it is cloed under multiplication, hance a subgroup of $H$. 
3. Let $a>0$, be represented by $f(x,y)$ and $gcd(a,D)=1$. Then $f(x,y)$ is properly equivalent to some $ax^{2}+bxy+cy^{2}$, $x,y\in \mathbb{Z}$, and $gcd(ax^{2}+bxy+cy^{2},D)=1$, then $a(ax^{2}+bxy+cy^{2})=\left( a+\frac{b}{2}y \right)+ny^{2}$. Thus $[a]H_{f}\subset H$, let $u,v\in \mathbb{Z}$, $gcd(u^{2}+nv^{2},D)=1$, $a(u^{2}+nv^{2})=a\left( u-\frac{b}{2}v \right)^{2}+b\left( u-\frac{b}{2}v \right)(av)+c(av)^{2}$. Thus $[a]H\subset H_{f}$, now we have $[a]H\subset H_{f}\subset[a]^{-1}H$. Therefore $[a]^{2}\in H$ or $[a]H=[a]^{-1}H$. 

**Definition**: Since distinct cosets of $H$ are disjoint, we know that different genera represent disjoint values in $(\mathbb{Z} / D\mathbb{Z})^{*}$. This allows us to describe genera cosets $H'$ of $H$ in $ker(\chi)$. We define the **genus** of $H'$ to consist of all forms of discriminant $D$ which represent the values of $H'$ modulo $D$. Then we have the following therorem:

**Theorem**: Assume that $D\equiv0,1\pmod{4}$ is negative, and let $H\subset ker(\chi)$ be the values in $(\mathbb{Z} / D\mathbb{Z})^{*}$ represented by the principle form of discriminant $D$. If $H'$ is a coset of $H$ in $ker(\chi)$ and $p$ is an odd prime not dividing $D$, then $[p]\in H'$ if and only if $p$ is represented by a reduced form of discriminant $D$ in the genus of $H'$.

**Proposition**: $D\equiv0,1\pmod{4}$, $p$ prime, $gcd(p,D)=1$, $p \in Ker\chi$, then $[p]\in H'$ <==> $\exists f$ in the genus of $H'$ such that $f$ represents $p$. 

**Corollary**: $n$ positive integer $D=-4n$, $p$ odd prime, $gcd(p,n)=1$. Then $[p]\in H$ <==> $p\equiv\beta ^{2}$ or $\beta ^{2}+n\pmod{4n}$. 

# Gauss, composition and genera
**lemma**: let $p_{1},q_{2},\dots,p_{r},q_{r},m \in \mathbb{Z}$ with $gcd(p_{1},p_{2},\dots,p_{r},m)=1$. Then the congruences $p_{i}B\equiv q_{i}\pmod{m}$ have a unique solution modulo $m$ if and only if $\forall i,j$ $p_{i}q_{j}-p_{j}q_{i}\equiv0\pmod{m}$. (easy, suppose $\sum_{i}a_{i}p_{i}\equiv1\pmod{m}$, then $B\equiv \sum_{i}a_{i}q_{i}\pmod{m}$)

**Lemma**: $f(x,y)=ax^{2}+bxy+cy^{2}$, $g(x,y)=a'x^{2}+b'xy+c'y^{2}$ with discriminant $D$, $gcd\left( a,a', \frac{b+b'}{2} \right)=1$. Then there is a unique integerr $B\pmod{2aa'}$ such that 
$$
\begin{cases}B&\equiv b&\pmod{2a} \\
B&\equiv b'&\pmod{2a'} \\
B^{2}&\equiv D&\pmod{4aa'}\end{cases}
$$

*Proof*: Notice that $4aa'|(B-b)(B-b')$, so $\frac{1}{2} (b+b')B\equiv bb'+D\pmod{2aa'}$. One check the condition of above lemma, so $B$ exists. 

With the lemma, we are now able to transfer $f,g$ into $ax^{2}+Bxy+\frac{B^{2}-D}{4a}y^{2}$ and $a'x^{2}+Bxy+\frac{B^{2}-D}{4a'}y^{2}$, and a new quadraic form $F(x,y)=aa'x^{2}+Bxy+\frac{B^{2}-D}{2aa'}y^{2}$ whose discriminant is also $D$. 

Written formaly, let $f,g,F$ be quadraic form with discriminant $D$, then we call $F$ a **composition** of $f$ and $g$ if there are bilinear form $u=B_{1}(x,t,z,w)=a_{1}xz+b_{1}xw+c_{1}yz+d_{1}yw$ and $v=B_{2}(x,y,z,w)=a_{2}xz+b_{2}xw+c_{2}yz+d_{2}yw$, such that $f(x,y)g(z,w)=F(u,v)$. 

**Lemma**: If $F$ is a composition of $f$ and $g$, then $a_{1}b_{2}-a_{2}b_{1}=\pm f(1,0)=\pm a$, $a_{1}c_{2}-a_{2}c_{1}=\pm g(1,0)=\pm a'$. (taking in turns $(x,y)=(1,0)$ and $(z,w)=(1,0)$)

We hope that the composition is unique (up to equivalence?). Unfortunately, this is not true in general. But if we ask $a_{1}b_{2}-a_{2}b_{1}=f(1,0)$ and $a_{1}c_{2}-a_{2}c_{1}=g(1,0)$, then we call $F$ is a **direct composition**, and its properly equivalent class is unique. 

In fact, the direct composition defines a multiplication of the class of quadraic forms $[f]*[g]=[F]$, this meas that the choice of representatives does note matter, and in fact, this multiplication is transitive and abelian. So this forms a group $C(D)=ker(\chi) / H$. 

**Definition**: Let **Principle form** be $x^{2}-\frac{D}{4}y^{2}$ for $4|D$, or $x^{2}+xy+\frac{1-D}{4}y^{2}$ for $D\equiv1\pmod{4}$. One notice that the dirichlet composition of  $ax^{2}+bxy+cy^{2}$ and $cx^{2}+bxy+ay^{2}$ are $acx^{2}+bxy+y^{2}$, which is properly equivalent too $x^{2}-bxt+acy^{2}$, hence properly equivalent to the principle form, so they are invers of each other in $C(D)$. 

**lemma**: A reduced form $f(x,y)=ax^{2}+bxy+cy^{2}$ of discriminant $D$ has order $\leq2$ in $C(D)$ if and only if $b=0,a=b\text{ or } a=c$. 

**Proposition**: Let $D<0$, $D\equiv0,1\pmod{4}$, let $r=$ the numer of odd prime factors of $D$. Define $\mu\geq0$: If $D\equiv1\pmod{4}$, $\mu=r$; if $D\equiv0\pmod{4}$, write $D=-4n$. 

| n                    | $\mu$ |
| -------------------- | ----- |
| $n\equiv3\pmod{4}$   | r     |
| $n\equiv1,2\pmod{4}$ | $r+1$ |
| $n\equiv4\pmod{8}$   | $r+1$ |
| $n\equiv0\pmod{8}$   | $r+2$ |
then $C(D)$ has $2^{\mu-1}$ elements of order $\leq2$. 

*Proof*: 
1. $b=0$, then $ac=n$, $a\leq c$, if $n=1$, $\#\{ (a,c) \}=1$, $n>1$ odd then $\#\{ (a,c) \}=2^{r-1}$, and if $n$ even then $\#\{ (a,c) \}=2$. 
2. $a=b$, then $b(4-b)=-D$. 
3. $a=c$, then $-D=(2c-b)(2c+b)$. Together with 2, we can write it as $-D=b'(4c-b')$, $0<b'\leq2c$, $gcd(b',c)=1$. 

# Genus theory
$D<0$, $D\equiv0,1\pmod{4}$, $\chi:(\mathbb{Z} / D\mathbb{Z})^{\times}\rightarrow \{ \pm1 \}$ $H\subset Ker\chi \subset(\mathbb{Z} / D\mathbb{Z})^{\times}$. "Principle form" $\phi :C(D)\rightarrow Ker\chi / H$. then $ker\phi$ is principle genus.

**Theorem**: 
1. $\#genera=2^{\mu-1}$
2. principle genus = $C(D)^{2}$ = $\{ x^{2}: x \in C(D) \}$

*proof*: 
take $p_{1}<p_{2}<\dots<p_{r}$, all odd prime factors of $D$. and $\chi_{i}(a)=\left( \frac{a}{p_{i}} \right)$, $1\leq i\leq r$, $a \in (\mathbb{Z} / p \mathbb{Z})^{\times}$; $\delta(a)=(-1)^{\frac{a-1}{2}}$, $a \in (\mathbb{Z} / 4 \mathbb{Z})^{\times}$; $\epsilon(a)=(-1)^{\frac{a^{2}-1}{8}}$, $a \in(\mathbb{Z} / 8\mathbb{Z})^{\times}$. 

consider the exact sequence:
$$
1\longrightarrow\{ x:x^{2}=1\} \longrightarrow C(D) \longrightarrow C(D) \longrightarrow C(D) / C(D)^{2} \longrightarrow1
$$
with $C(D)\rightarrow C(D)$ is $x \mapsto x^{2}$. 

# cubic and biquadratic reaprocity
We extend the ring $\mathbb{Z}$ to $\mathbb{Z}[\omega]$ where $\omega=-\frac{1}{2}+\frac{\sqrt{ 3 }}{2}i$. As one immediately know that $R=\mathbb{Z}[\omega]$ is **Euclidean ring**. 

- Call $0\neq\alpha \in R$ a **unit** if $\lvert \alpha \rvert=1$. i.e. $(\alpha)=R$
- Call $\alpha,\beta \in R$ **associates** if $\alpha=\beta r$ for some unit $r$. i.e. $(\alpha)=(\beta)$. 
- Call $\alpha\neq0$ irreducible if $\alpha=\beta r$ . i.e. $(\alpha)$ is a prime ideal. 