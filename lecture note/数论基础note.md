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

**Lemma**: $D\equiv0\text{ or } 1\pmod{4}$, $D\neq0$. There is a unique $\chi:(\mathbb{Z} / D\mathbb{Z})^{\times}\rightarrow \{ \pm1 \}$, s.t. $\chi([p])=\left( \frac{D}{p} \right)$ for all odd prime $p$. Moreover, $\chi([-1])=\begin{cases}1\  &\text{if } D>0\\ -1\ &\text{if } D<0\end{cases}$ 

*Proof*: 
1. Existence. For positive integer $n$ prime to $D$, define $\chi([n])=\left( \frac{D}{n} \right)$. One has to check that $\chi$ is well defined. 
	1) $D>0$ and $D\equiv1\pmod{4}$. Then $\left( \frac{D}{m} \right)=\left( \frac{m}{D} \right)(-1)^{\frac{D-1}{2}\cdot \frac{m-1}{2}}$, and it is easy to check $\left( \frac{D}{m} \right)=\left( \frac{D}{n} \right)$. 
	2) $D<0$ and $D\equiv1\pmod{4}$. Then $\left( \frac{D}{m} \right)=\left( \frac{-1}{m} \right)\cdot\left( \frac{-D}{M} \right)$, and the rest is same as above. 
	3) $D>0$ and $D\equiv0\pmod{4}$. Let $D=2^{k}D'$, with $k\geq2$. Then $\left( \frac{D}{m} \right)=\left( \frac{2}{m} \right)^{k}\left( \frac{D'}{m} \right)=(-1)^{\frac{m^{2}-1}{8}}\cdot\left( \frac{D'}{m} \right)$, simple discussion show that $\left( \frac{D}{m} \right) =\left( \frac{D}{n} \right)$. 
	4) $D<0$ and $D\equiv0\pmod{4}$. Let $D=-2^{k}D'$, with $k\geq2$. Then $\left( \frac{D}{m} \right)=\left( \frac{-1}{m} \right)\cdot\left( \frac{2}{m} \right)^{k}\left( \frac{D'}{m} \right)= (-1)^{\frac{m-1}{2}}\cdot(-1)^{\frac{m^{2}-1}{8}}\cdot\left( \frac{D'}{m} \right)$, and it is easy to check that this case is correct too. 
2. Condider $\chi([-1])$. Choose positive integer $n\equiv-1\pmod{8D}$. Then we need to compute $\left( \frac{D}{n} \right)$. Condider all four cases as above, then we are done. 

For "$x^{2}+ny^{2}$", consider $D=-4n$ $\rightsquigarrow$ $\chi:(\mathbb{Z} / D\mathbb{Z})^{\times} \rightarrow \{ \pm1 \}$. Then if there is a $x,y \in \mathbb{Z}$, $gcd(x,y)=1$ such that $p|x^{2}+ny^{2}$, then we have $\chi([p])=1$. 

cases of $n=5,27,64$:
1. $n=5$, $p$ odd prime $\neq5$. Then $p=x^{2}+2y^{2}$ $\Longleftrightarrow$ $p\equiv1\text{ or } 9\pmod{20}$, $2p=x^{2}+5y^{2}$ $\Longleftrightarrow$ $p=2u^{2}+2uv+3v^{2}$ <==> $p\equiv3\text{ or }7\pmod{20}$. In this case, $\left( \frac{-5}{p} \right)=1$ $\Longleftrightarrow$ $p\equiv1,3,7,9\pmod{20}$. 
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

| $D$   |                                                                 |
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
1. $n$ must be a prime power. Otherwise, there exists positive integers $1<a<b$. $gcd(a,b)=1$, $ax^{2}+by^{2}$ is a reduced form different from $x^{2}+ny^{2}$, discriminant=-4ab=-4n. Thus $h(-4n)\geq2$. 
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
\begin{cases}B &\equiv b \pmod{2a} \\
B &\equiv b' \pmod{2a'} \\
B^{2} &\equiv D \pmod{4aa'}\end{cases}
$$

*Proof*: Notice that $4aa'|(B-b)(B-b')$, so $\frac{1}{2} (b+b')B\equiv bb'+D\pmod{2aa'}$. One check the condition of above lemma, so $B$ exists. 

With the lemma, we are now able to transfer $f,g$ into $ax^{2}+Bxy+\frac{B^{2}-D}{4a}y^{2}$ and $a'x^{2}+Bxy+\frac{B^{2}-D}{4a'}y^{2}$, and a new quadraic form $F(x,y)=aa'x^{2}+Bxy+\frac{B^{2}-D}{2aa'}y^{2}$ whose discriminant is also $D$. 

Written formaly, let $f,g,F$ be quadraic form with discriminant $D$, then we call $F$ a **composition** of $f$ and $g$ if there are bilinear form $u=B_{1}(x,t,z,w)=a_{1}xz+b_{1}xw+c_{1}yz+d_{1}yw$ and $v=B_{2}(x,y,z,w)=a_{2}xz+b_{2}xw+c_{2}yz+d_{2}yw$, such that $f(x,y)g(z,w)=F(u,v)$. 

**Lemma**: If $F$ is a composition of $f$ and $g$, then $a_{1}b_{2}-a_{2}b_{1}=\pm f(1,0)=\pm a$, $a_{1}c_{2}-a_{2}c_{1}=\pm g(1,0)=\pm a'$. (taking in turns $(x,y)=(1,0)$ and $(z,w)=(1,0)$)

We hope that the composition is unique (up to equivalence?). Unfortunately, this is not true in general. But if we ask $a_{1}b_{2}-a_{2}b_{1}=f(1,0)$ and $a_{1}c_{2}-a_{2}c_{1}=g(1,0)$, then we call $F$ is a **direct composition**, and its properly equivalent class is unique. 

In fact, the direct composition defines a multiplication of the class of quadraic forms $[f]*[g]=[F]$, this means that the choice of representatives does note matter, and in fact, this multiplication is transitive and abelian. So this forms a group $C(D)=ker(\chi) / H$. 

**Definition**: Let **principle form** be $x^{2}-\frac{D}{4}y^{2}$ for $4|D$, or $x^{2}+xy+\frac{1-D}{4}y^{2}$ for $D\equiv1\pmod{4}$. One notice that the dirichlet composition of  $ax^{2}+bxy+cy^{2}$ and $cx^{2}+bxy+ay^{2}$ are $acx^{2}+bxy+y^{2}$, which is properly equivalent too $x^{2}-bxt+acy^{2}$, hence properly equivalent to the principle form, so they are invers of each other in $C(D)$. 

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
- Call $\alpha\neq0$ irreducible if $\alpha=\beta r$ for some $\beta,r \in R$ then one of $\beta,r$ must be a unit. i.e. $(\alpha)$ is a prime ideal. 

**Lemma**: If $N(\alpha)$ is prime for some $\alpha \in R$, then $\alpha$ is a prime

**Proposition**: Let $p$ be a prime in $\mathbb{Z}$. Then
1. if $p=3$, then $1-\omega$ is a prime in $\mathbb{Z}[\omega]$, then $3=-\omega ^{2}(1-\omega)^{2}$. 
2. If $p\equiv1\pmod{3}$, then there exists a prime $\pi \in \mathbb{Z}[\omega]$ such that $p=\pi \cdot \overline{\pi}$, and $\pi \& \overline{\pi}$ are not associates, $N(\pi)=N(\overline{\pi})=p$. 
3. If $p\equiv2\pmod{3}$, then $\pi=p$ is prime in $\mathbb{Z}[\omega]$, $N(\pi)=p^{2}$. 

Further more, every prime of $R$ is associate to one of the primes in 1,2,3. In any case, $\mathbb{Z}[\omega]$ is a finite field with $N(\pi)$ elements. 

*Proof*: 
1. Clear, as $N(1-\omega)=3$ prime, and one immediately check the other equation.
2. As $h(-3)=1$, we know that $p=x^{2}+xy+y^{2}$ for some $x,y$, hence $p=(x+\omega y)(x-\omega y)$, and it is clear that $x-\omega y$ are note associate to $x+\omega y$. 
3. Consider $(p)\subseteq \mathfrak{p}=(\alpha)$, for some $\alpha$, then $N(\alpha)|N(p)=p^{2}$. If $p$ is not a prime in $\mathbb{Z}[\omega]$, then $N(a)<N(p)$, so $N(\alpha)=p$, suppose $\alpha=a+b\omega$, then $p=a^{2}+ab+b^{2}$, a contradiction.

Now we define the biquadratic character. 

**Definition**: Let $\alpha \in \mathbb{Z}[\omega]$, that is not in $\pi \mathbb{Z}[\omega]$, where $\pi$ is a prime in $\mathbb{Z}[\omega]$ not dividing 3. Then we say 
$$
\alpha ^{(N(\pi)-1)/3} \equiv \left( \frac{a}{\pi} \right)_{3}\pmod{\pi}
$$

One immediately know that $\left( \frac{\alpha\beta}{\pi} \right)_{3}= \left( \frac{\alpha}{\pi} \right)_{3}\cdot\left( \frac{\beta}{\pi} \right)_{3}$.

**Theorem**: If $\pi$ and $\theta$ are primary primes in $\mathbb{Z}[\omega]$ of unequal norm, then 
$$
\left( \frac{\theta}{\pi} \right)_{3}= \left( \frac{\pi}{\theta} \right)_{3}
$$

**Remark**: 
1. $\left( \frac{-1}{\pi} \right)_{3}=1$.
2. $\pi=-1+3m+3n\omega$, $m,n \in \mathbb{Z}$, then $\left( \frac{\omega}{\pi} \right)_{3}=\omega ^{m+n}$, and $\left( \frac{1-\omega}{\pi} \right)_{3}=\omega ^{2m}$. 

**Theorem**: Let $p$ be a prime then there exists $x,y \in \mathbb{Z}$ such that $p=x^{2}+27y^{2}$ if and only if $p\equiv1\pmod{3}$ and 2 is a cubic residue module $p$. 

*Proof*: 
1. We first proof that it is necessary. In fact, one immediately notice that $p\equiv x^{2}\equiv1\pmod{3}$, thus $p=x^{2}+27y^{2}=\pi \cdot \overline{\pi}$, $\pi=(x+3y)+6y\omega$. Now 2 is a qubic residue is equivalent to $1=\left( \frac{2}{\pi} \right)_{3}=\left( \frac{\pi}{2} \right)_{3}$ <==> $\pi\equiv1\pmod{2}$. 
2. We then proof that the conditions are sufficicent. Since $p\equiv1\pmod{3}$, we are able to write it as $p=a+3b\omega$ for $p=\pi \cdot \overline{\pi}$. We may assume that $\pi\equiv-1\pmod{3}$, then $4p=4(a^{2}-3ab+9b^{2})=(2a-3b)^{2}+27b^{2}$, as 2 a cubic residue, we know that $a\equiv1\pmod{2}$ and $2|b$. 

# $\mathbb{Z}[i]$ and biquadraic reaprocity
Let $R:=\mathbb{Z}[i]$ with $i=\sqrt{ -1 }$. One immediately notice that $R$ is a Euclidean ring, hence a PID and UFD. 

**proposition**: Let $p$ be a prime. Then 
1. If $p=2$, then $1+i$ is a prime and $2=(-1)(1+i)^{2}$. 
2. If $p\equiv1\pmod{4}$, then there is a prime $\pi=x+yi \in \mathbb{Z}[i]$ such that $p=\pi \cdot \overline{\pi}$. 
3. If $p\equiv3\pmod{4}$, then $p$ is a prime in $\mathbb{Z}[i]$. 
4. In fact, any prime in $\mathbb{Z}[i]$ is associate to one in 1,2,3.

*Proof*: 
1. $\mathbb{Z}[i] / (1+i)\simeq \mathbb{Z} / \mathbb{Z}\cap(1+i)=\mathbb{Z} / 2\mathbb{Z}$. 
2. As $p=x^{2}+y^{2}$, with $gcd(x,y)=1$, so there is $u,v \in \mathbb{Z}$ such that $ux+vy=1$, then $a+bi-(x+yi)(u+vi)\in \mathbb{Z}$, hence $\mathbb{Z}[i] / (x+yi)\simeq \mathbb{Z} / p\mathbb{Z}$. Thus $\pi=x+yi$ is a prime in $\mathbb{Z}[i]$. 
3. One note that $x^{2}+1$ is irreducible in $\mathbb{F}_{p}[x]$, so $\mathbb{Z}[i] / (p)$ is a field. 

Now let $\pi$ be a prime in $\mathbb{Z}[i]$, and assume that $\pi$ is note associate to $1+i$. Then $4|N(\pi)-1$. Then one notice that $\alpha ^{\frac{N(\pi)-1}{4}}\equiv \eta \pmod{\pi}$ for some $\eta \in \{ \pm1,\pm i \}$, so $\left( \frac{\alpha}{\pi} \right)_{4} \in \{ \pm1,\ \pm i \}$. 

**Definition**: We call a prime $\pi$ of $\mathbb{Z}[i]$ **primary** if $\pi\equiv1\pmod{(1+i)^{3}}$. Assume that $\pi$ prime and $\pi \not\sim1+i$, then there is a unique associates that is primary.  

**Theorem**: (biquadratic reciporcity theorem)
If $\pi \&\theta$ are primary primes and $\pi \not\sim\theta$, then $\left( \frac{\theta}{\pi} \right)_{4}= \left( \frac{\pi}{\theta} \right)_{4} = (-1)^{\frac{(N(\pi)-1)(N(\theta)-1)}{16}}$

And $\left( \frac{i}{\pi} \right)_{4}=i^{- \frac{a-1}{2}}$, $\left( \frac{1+i}{\pi} \right)_{4}=i^{\frac{a-b-1+b^{2}}{4}}$ for $\pi=a+bi$ primary. 

**theorem**: 
1. If $\pi$ is primary prime in $\mathbb{Z}[i]$, $\pi=a+bi$, then $\left( \frac{2}{\pi} \right)_{4}=i^{\frac{ab}{2}}$.
2. let $p$ be a prime. There exists $x,y \in \mathbb{Z}$ $p=x^{2}+64y^{2}$ if and only if $p\equiv1\pmod{4}$ and $2$ is a biquadratic residue module $p$. 

*Proof*: 
1. Just check that $i^{ab/2}=i^{(a-b-1-b^{2})/2}\cdot i^{(a-1)/2}$, i.e. $8|2(a-1)-(b+b^{2})-ab$, which is easy using the fact that $\pi$ is primary ($a=1+2u,\ b=2v,\ 2|u+v$). 
2. if $p=x^{2}+64y^{2}$, iff $8|b$, hence $\left( \frac{2}{\pi} \right)_{4}=1$, which is equivalent to $t^{4}-2$ have a solution in $\mathbb{F}_{p}$. 

---

# Chapter 2: Class field theory
"The Hilbert clas field and $p=x^{2}+ny^{2}$"

>[!note] Main Theorem
>let $n>0$, be a square free positive integer, $n\not\equiv3\pmod{4}$. Then there exists a monic irreducible polynomial $f_{n}(x)\in \mathbb{Z}[x]$ of degree $h(-4n)$ s.t. if an odd prime $p$ divides neither $n$ nor the discriminant of $f_{n}(x)$, then $\exists x,y \in \mathbb{Z}$, $p=x^{2}+ny^{2}$ $\Longleftrightarrow$ $\left( \frac{-n}{p} \right)=1$ and $f_{n}(x)\equiv0\pmod{p}$ has a solution. 
>Further more, $f_{n}(x)$ may be chosen to be the minimal polynomial of a real algebraic integer $\alpha$ for which $L=K(\alpha)$ is the hilbert class field of $K=\mathbb{Q}(\sqrt{ -n })$. 

$K$ a number field, $\mathbb{Q}\subset K$ $[K:\mathbb{Q}]=dim_{\mathbb{Q}}K<+\infty$. $\mathcal{O}_{K}$ is the integer ring of $K$. 

Fact:
1. $\mathcal{O}_{K}$ is a free $\mathbb{Z}$-module of rank $dim_{\mathbb{Q}}K$.
2. $\mathcal{O}_{K}$ is a subring of $K$, in fact, $K$ is the field of fraction of $\mathcal{O}_{K}$. 
3. If $\mathfrak{a}\subset \mathcal{O}_{K}$, is a nonzero ideal, then $\mathcal{O}_{K} / \mathfrak{a}$ is finite
4. $\mathcal{O}_{K}$ is a [[Dedekind domain]]. 
5. Any nonzero ideal $\mathfrak{a}$ of $\mathcal{O}_{K}$ can be written as a product $\mathfrak{a}=\mathfrak{p}_{1}^{\alpha_{1}}\cdots\mathfrak{p}_{r}^{\alpha ^{r}}$ where $\mathfrak{p}_{i}$ are distinct prime ideals of $\mathcal{O}_{K}$. 

One notice that the residue field $\mathcal{O}_{K} / \mathfrak{p}$ is a finite field. 

**Definition**: $\mathfrak{a}\subset K$ is called **fraction ideal** if:
 1. $\mathfrak{a}$ is an additive subgroup.
 2. $O_{k}\cdot \mathfrak{a}\subseteq \mathfrak{a}$. 
 3. As an $O_{k}$-module, $\mathfrak{a}$ is finitely generated. 

**Proposition**: let $\mathfrak{a}$ be a fractional ideal,
1. $\mathfrak{a}$ is invertable, i.e. there exists a fractional ideal $\mathfrak{b}$ s.t. $\mathfrak{a}\cdot \mathfrak{b}=\mathcal{O}_{K}$. 
2. there are distinct nonzero prime ideals $\mathfrak{p}_{1}, \cdots,\mathfrak{p}_{r}$, and nonzero integers $\alpha_{1}, \cdots, \alpha_{r}$, s,t, $\mathfrak{a}=\mathfrak{p}_{1}^{\alpha_{1}}\cdots\mathfrak{p}_{r}^{d_{r}}$. 

**Definition**: Let $I_{k}$ be the group of fractional ideals and $P_{K}$ be the subgroup of nonzero principle fractional ideals, and $CL_{K}=I_{K} / P_{K}$. One know that $CL_{K}$ is finite (c.f.[[Finiteness of class number]]). 

Let $L|K$ be a finite extension. $\mathcal{O}_{K}\subseteq O_{L}$. then $P\subseteq \mathcal{O}_{K}$, nonzero prime ideal, $\mathfrak{p}\cdot O_{L}=\left\{  \sum_{k=1}^{m}x_{i}y_{i} :m\geq1, \ x_{i}\in \mathfrak{p}, y_{i}\in O_{L} \right\}$ be ideals of $O_{L}$, let it be $\mathfrak{q}_{1}^{e_{1}}\cdots \mathfrak{q}_{g}^{e_{g}}$. 

fact:
1. $\{ q_{i}:1\leq i\leq g \}=\{ \mathfrak{q} \subseteq O_{L}: prime,\ \mathfrak{q}\geq \mathfrak{p} \}$. 
2. $\mathcal{O}_{K} /\mathfrak{p} \hookrightarrow O_{L} /\mathfrak{q}_{j}$, finite extension, let it be $f_{\mathfrak{q}_{i} / \mathfrak{p}}=f_{j}$ 
3. $e_{\mathfrak{q}_{j} / \mathfrak{p}}=e_{j}$ be ramification index. 

**Theorem**: $\sum_{j=1}^{g}e_{j}f_{j}=[L:K]$.(use the fact that $\mathcal{O}_{L} / \mathfrak{p}\mathcal{O}_{L}\simeq \bigoplus_{i}\mathcal{O}_{L}/\mathfrak{q}_{i}^{e_{i}}$)

**Theorem**: $K\subseteq L$ finite Galois enxtension $\mathfrak{p}\subseteq \mathcal{O}_{K}$, nonzero prime ideal.
1. Galois group $Gal(L / K)$ acts transitively on the primes of $L$ containing $\mathfrak{p}$. 
2. $\forall j,j'$, $1\leq j,j'\leq g$, $e_{j}=e_{j'}$, $f_{j}=f_{j'}$, let it be $e,f$, then $efg=[L:K]$. 

*Proof*:
1. First show that $\mathfrak{q}'\subseteq\bigcup_{\sigma \in Gal(L / K)}\sigma \mathfrak{q}$. Let $x \in \mathfrak{q}'$, then $y:=\prod_{\sigma} \sigma x \in O_{L}\cap L=\mathcal{O}_{K}$. Then $y \in \mathcal{O}_{K}\cap \mathfrak{q}'=\mathfrak{p}\subseteq \mathfrak{q}$. Thus there is a $\sigma$ s.t. $\sigma ^{-1}x \in \mathfrak{q}$. Therefore $\mathfrak{q'}\subseteq \bigcup_{\sigma}\sigma \mathfrak{q}$. Second there is a $\sigma$ s.t. $\mathfrak{q'}\leq \sigma\mathfrak{q}$.

**Definition**: $\mathfrak{p}$ is **ramifies** in $L$ if $e>1$, and **unraminfied** if not.

Let $L / K$ be a Galois extension, $\mathfrak{p}\subset \mathcal{O}_{K}$ prime and $\mathfrak{q}\subset \mathcal{O}_{L}$, with $\mathfrak{p}=\mathfrak{q}\cap \mathcal{O}_{K}$. The decomposition group $D_{\mathfrak{q}}=\{ \sigma \in Gal(L / K): \sigma(\mathfrak{q})=\mathfrak{q} \}$, mertia group $I_{\mathfrak{q}}=\{ \sigma \in D_{\mathfrak{q}}: \sigma \cdot\alpha\equiv\alpha \pmod{\mathfrak{q}},\ \forall\alpha \in \mathcal{O}_{L} \}$, $\tilde{G}=Gal((\mathcal{O}_{L} / \mathfrak{q}) / (\mathcal{O}_{K} / \mathfrak{p}) )$. 

**proposition**: There is a homomorphism $\phi:\sigma\mapsto \tilde{\sigma}$
1. $ker\phi=I_{\mathfrak{q}}$.
2. "$\phi:D_{\mathfrak{q}}\rightarrow \tilde{G}$" is surjective.
3. $\#I_{\mathfrak{q}}=e_{\mathfrak{q}|\mathfrak{p}}$, $\#D_{\mathfrak{q}}=e_{\mathfrak{q}|\mathfrak{p}}\cdot f_{\mathfrak{q}|\mathfrak{p}}$. 

**Proposition**: $K\subset L$, galois extension, $L=K(\alpha)$ for some $\alpha \in \mathcal{O}_{L}$, $f(x)=min_{K}\alpha$, $f(x)\in\mathcal{O}_{K}[x]$, $deg\,f=[L:K]$. Let $\mathfrak{p}$ be a prime of $K$ and $f(x)$ be seperable module $\mathfrak{p}$. 
1. $\mathfrak{p}$ is unraminfied in $L$. 
2. Let $f\equiv f_{1}\cdots f_{n}\pmod{\mathfrak{p}}$. $f_{i}\not\equiv f_{j}$, and irreducible. Put $\mathfrak{q}_{i}=\mathfrak{p}\mathcal{O}_{L}+f_{i}(\alpha)\mathcal{O}_{L}$. Then each $\mathfrak{q}_{i}$ is a prime of $L$, $q_{i}\neq \mathfrak{q}_{j}$, and $\mathfrak{p}\cdot \mathcal{O}_{L}=\mathfrak{q}_{1}\cdots\mathfrak{q}_{n}$. with $deg\,f_{i}=deg\,f_{j}$, and is equal to the extension degree.
3. $\mathfrak{p}$ split completely in $L$ iff $f(x)\equiv0\pmod{\mathfrak{p}}$, has a solution in $\mathcal{O}_{K}$. 

*Proof*: In fact, 1 and 3 are direct consequence of 2. Consider $\mathcal{O}_{K}\subseteq \mathcal{O}_{K}[\alpha]\subseteq \mathcal{O}_{L}$, and put $\mathfrak{q}_{i}'=\mathfrak{p}\mathcal{O}_{K}[\alpha]+(f_{i}(x))$, then $\mathcal{O}_{K}[\alpha] / \mathfrak{q}_{i}'$ is a field and $\mathfrak{p}\cdot \mathcal{O}_{K}[\alpha]=\mathfrak{q}_{1}'\cdots\mathfrak{q}_{n}'$. $\prod_{i=1}^{n}\#(\mathcal{O}_{K}[\alpha] / \mathfrak{q}_{i}')=(\#\mathcal{O}_{K} / \mathfrak{p})^{deg\,f}$. Let $\mathfrak{q}_{i}'\mathcal{O}_{L}=\prod_{j}\mathfrak{q}_{i,j}$, then $\prod_{i}\prod_{j}\mathcal{O}_{L} / \mathfrak{q}_{i,j}=\#(\mathcal{O}_{K} / \mathfrak{p})^{[L:K]}=\#(\mathcal{O}_{K} / \mathfrak{p})^{deg\,f}$. and we get $\forall i,S_{i}=1$ and $\mathcal{O}_{L} / \mathfrak{q}_{i,1}\simeq \mathcal{O}_{K} / \mathfrak{q}_{i}'$. Hence $\mathfrak{q}_{i,1}=\mathfrak{q}_{i}'\cdot \mathcal{O}_{L}=\mathfrak{p}\cdot \mathcal{O}_{L}+(f_{i}(\alpha))$. 

For the special case of Quadraic fields, $N\neq0,1$ square free, put $K=\mathbb{Q}(\sqrt{ N })$, then the discriminant of $K=\begin{cases}N,\ &N\equiv1\pmod{4}\\4N,\ &N\equiv2,3\pmod{4}\end{cases}$. Then $d_{K}\equiv0,1\pmod{4}$, and $K=\mathbb{Q}(\sqrt{ d_{K} })$, $\mathcal{O}_{K}=\begin{cases}\mathbb{Z}\left[ \frac{1+\sqrt{ N }}{2} \right],\ &N\equiv1\pmod{4}\\\mathbb{Z}[\sqrt{ N }],\ &N\equiv2,3\pmod{4}\end{cases}=\mathbb{Z}\left[ \frac{d_{K}+\sqrt{ d_{K} }}{2} \right]$. 

**Definition**: the Kroneaker symbol $\left( \frac{D}{2} \right)$ by
$$
\left( \frac{D}{2} \right)=
\begin{cases}
0, &D\equiv0\pmod{4} \\
1, &D\equiv1\pmod{8} \\
-1, &D\equiv5\pmod{8}
\end{cases}
$$

**Proposition**: $K=\mathbb{Q}(\sqrt{ n })=\mathbb{Q}(\sqrt{ d_{K} })$
1. If $\left( \frac{d_{K}}{P} \right)=0$, then $p\mathcal{O}_{K}=\mathfrak{p}^{2}$ for some prime ideal $\mathfrak{p}$ of $\mathcal{O}_{K}$.
2. If $\left( \frac{d_{K}}{p} \right)=1$, then $p\mathcal{O}_{K}=\mathfrak{p}_{1}\mathfrak{p}_{2}$, for some prime ideal $\mathfrak{p}_{1}$, $\mathfrak{p}_{2}$ of $\mathcal{O}_{K}$, $\mathfrak{p}_{1}\neq \mathfrak{p}_{2}$. 
3. If $\left( \frac{d_{K}}{p} \right)=-1$, then $p\mathcal{O}_{K}$ is a prime ideal of $\mathcal{O}_{K}$. 

*Proof*: 
1. If $p$ is a odd prime, then $p|N$, put $\mathfrak{p}=p\mathcal{O}_{K}+\sqrt{ N }\mathcal{O}_{K}$. Then $\mathfrak{p}^{2}=p\mathcal{O}_{K}$. It $p=2$, $N\equiv2\pmod{4}$, put $\mathfrak{p}=2\mathcal{O}_{K}+\sqrt{ N }\mathcal{O}_{K}$. If $N\equiv3\pmod{4}$, then put $\mathfrak{p}=2\mathcal{O}_{K}+(1+\sqrt{ N })\mathcal{O}_{K}$.

## Hilbert class field
- **Finite prime**: A nonzero prime ideal of $\mathcal{O}_{K}$.
- **Real infinite prime**: $\sigma:K \hookrightarrow\mathbb{R}$.
- **Complex infinite prime**: $\sigma:K \hookrightarrow\mathbb{C}$, such that $\sigma(K)\not\subseteq \mathbb{R}$. 

An infinite prime $\sigma$ of $K$ is said to be ramified if $\sigma$ is real but it has an extension to $L$ which is complex. 

**Theorem**: Given a number field $K$, there exists a finite extension $L$ of $K$ such that 
1. $L$ is an unraminfied abelian extension of $K$.
2. Any unraminfied abelian extension of $K$ is contained in $L$. 

We call $L$ the hilbert class field of $K$. 

**Lemma**: Let $K\subset L$ be a galois extension, and let $\mathfrak{p}\subset \mathcal{O}_{K}$ be a nonzero ideal, let $\mathfrak{q}\subset \mathcal{O}_{L}$ be a nonzero prime ideal containing $\mathfrak{p}$. Then there exists a unique $\sigma \in Gal(L|K)$ such that $\sigma(\alpha)\equiv\alpha ^{N(\mathfrak{p})}\pmod{\mathfrak{q}}$, for all $\alpha \in \mathcal{O}_{L}$ where $N(\mathfrak{p})=\#\mathcal{O}_{K}|\mathfrak{p}$. 

*Proof*: $I_{\mathfrak{q}}\subset D_{\mathfrak{q}}\subset Gal(L / K)$ $\phi:D_{\mathfrak{q}} / I_{\mathfrak{q}}\simeq Gal\left((\mathcal{O}_{L} / \mathfrak{q}) / (\mathcal{O}_{K} / \mathfrak{p})\right)$, since $\mathfrak{p}$ is unraminfied in $L$, we have $I_{\mathfrak{q}}=1$. $N(\mathfrak{p})=\#\mathcal{O}_{K} / \mathfrak{p}$, $x\mapsto x^{N(\mathfrak{p})}(x \in \mathcal{O} / \mathfrak{q})$ is a generator of the galois group. There exists a unique $\sigma \in D_{\mathfrak{q}}$ such that $\tilde{\sigma}=\{ x\mapsto x^{N(\mathfrak{p})}:x \in \mathcal{O} / \mathfrak{q} \}$.

Write $\left( \frac{L / K}{\mathfrak{q}} \right)=\sigma$, and call the **Artin symbol of $\mathfrak{p}$**, $\left( \frac{L/K}{\mathfrak{q}} \right)\in Gal(L / K)$, and $\left( \frac{L / K}{\mathfrak{q}} \right)(\alpha)\equiv\alpha ^{N(\mathfrak{p})}\pmod{\mathfrak{q}}$ for all $\alpha$. 

Let $\mathfrak{p}$ be an unraminfied ideal of $\mathcal{O}_{K}$, $\mathfrak{q}\subseteq \mathcal{O}_{L}$ s.t. $\mathfrak{q}\cap \mathcal{O}_{K}=\mathfrak{p}$. 
1. $\left( \frac{L / K}{\sigma \mathfrak{q}} \right)=\sigma\left( \frac{L / K}{\mathfrak{q}} \right)\sigma ^{-1}$. 
2. the order of $\left( \frac{L / K }{\mathfrak{q}} \right)=[\mathcal{O}_{L} / \mathfrak{q} : \mathcal{O}_{K} / \mathfrak{p}]=f$. 
3. $\mathfrak{p}$ splite completely on $L$ iff $\left( \frac{L / K}{\mathfrak{q}} \right)=1$. 

When $L / K$ abelian, the artin symbol $\left( \frac{L / K}{\mathfrak{q}} \right)$ depend only on $\mathfrak{p}$, so we will also denote it as $\left( \frac{L /K}{\mathfrak{p}} \right)$ by abuse of notion. 

**Theorem**: $L / K$ hilbert class field, consider the artin map 
$$
\left( \frac{L / K}{\cdot} \right): I_{K} \longrightarrow Gal(L /K) 
$$
is surjective, and its kernel is exactly the subgroup $P_{K}$ of fractional ideals. Hence $C(\mathcal{O}_{K})\simeq Gal(L / K)$. 

As a result $\mathfrak{p}$ split completely in $L$ iff $\mathfrak{p}$ is a principle ideal. 

Let $K=\mathbb{Q}(\sqrt{ -n })$ be a imaginary quadraic field, and $\mathbb{Q}\subseteq K\subseteq L\subseteq \mathbb{C}$, where $L /K$ is hilbert class field. Consider $\tau:\mathbb{C}\rightarrow \mathbb{C}$ complex conjagutes $(z\mapsto \overline{z})$. Then $\tau(L)=L$ and $L / \mathbb{Q}$ is galois. In fact, $\tau\left( \frac{L / K}{\mathfrak{p}} \right)\tau ^{-1}=\left( \frac{L / K}{\tau(\mathfrak{p})} \right)$ for $\tau \in Gal(L / \mathbb{Q})$ (not just $Gal(L / K)$, but as it is the normal subgroup of $Gal(L / \mathbb{Q})$, so it is bascially the same). 

**Theorem**: Let $p$ be a prime, $n\not\equiv0\pmod{p}$, then there is a $x,y \in \mathbb{Z}$ s.t. $p=x^{2}+ny^{2}$ iff $p\mathbb{Z}$ split completely in $L$. 

*proof*: $\exists x,y \in \mathbb{Z}$ $p=x^{2}+ny^{2}$ $\Longleftrightarrow$ $p\cdot \mathcal{O}_{K}=\mathfrak{p}\overline{\mathfrak{p}}$ is a principle prime ideal, $\mathfrak{p}\neq \overline{\mathfrak{p}}$. The artin reciporcity theorem tells us that it is equivalent to $p\cdot \mathcal{O}_{L}=\mathfrak{p}\cdot \overline{\mathfrak{p}}$, where $\mathfrak{p}$ prime, hence $\mathfrak{p}$ split, so $p\mathbb{Z}$ splits completely in $L$. 

**Proposition**: $K$ imaginary quadraic field $L / K$ finite extension and $L / \mathbb{Q}$ Galoisa, $L$ is invariant under conjagutes of complex number, then:
1. $\exists\alpha \in \mathcal{O}_{L}\cap \mathbb{R}$ s.t. $L=K(\alpha)$. 
2. $f(x)=min_{K}(\alpha)$. If $p$ is a prime not dividing the discriminant of $f$, then $p$ splits completely in $L$ iff $\left( \frac{d_{K}}{p} \right)=1$ and $f(x)\equiv0\pmod{p}$ has an integer solution.

*Proof*: $o(\tau)=2$, $\tau(L)=L$, $[L:L^{\tau}]=2$, and $L^{\tau}=L\cap \mathbb{R}$, hence $[L\cap \mathbb{R}:\mathbb{Q}]=\frac{1}{2}[L:\mathbb{Q}]=[L:K]$. Choose a generator $\alpha \in \mathcal{O}_{L}\cap \mathbb{R}$ of $L\cap \mathbb{R}$ over $\mathbb{Q}$. Then $deg(f)=[L:K]$, so $L=K(\alpha)$. Let $p$ be a prime dividing the discriminant of $f(x)$. This tells us that $f(x)$ is seperable module $p$. So $p\mathcal{O}_{K}=\mathfrak{p}\overline{\mathfrak{p}}$ iff $\left( \frac{d_{K}}{p} \right)=1$. We may assume that $p$ splits completely in $K$, so that $\mathbb{Z} / p\mathbb{Z}\simeq \mathcal{O}_{K} / \mathfrak{p}$. Since $f(x)$ is seperable over $\mathbb{Z} / p\mathbb{Z}$, it is seperable over $\mathcal{O}_{K} / \mathfrak{p}$, and then we have that $\mathfrak{p}$ splits completely in $L$ iff $f(x)\equiv0\pmod{p}$ in $\mathbb{Z}$. 

**Theorem**: Let $K$ be a imaginary quadraic field of discriminant $d_{K}<0$, then:
1. If $f(x,y)=ax^{2}+bxy+cy^{2}$ is a primitive positive definte quadraic form of discriminant $d_{K}$, then $[a,(-b+\sqrt{ d_{K} }) / 2]=\{ ma+n(-b+\sqrt{ d_{K} }) / 2:m,n \in \mathbb{Z} \}$. Is an ideal of $\mathcal{O}_{K}$. 
2. The map sending $f(x,y)$ to $[a,(-b+\sqrt{ d_{K} }) / 2: m,n \in \mathbb{Z}]$ induces an isomorphism between the form class group $C(d_{K})$ and the ideal class group $C(\mathcal{O}_{K})$. Hence the order of $C(\mathcal{O}_{K})$ is the class number $h(\mathcal{O}_{K})$. 

**Example**: $n=-14$, $K=\mathbb{Q}(\sqrt{ -14 })$, $D=-56$, $f(x,y)=x^{2}+14y^{2}$, $\#C(d_{K})=h(-56)=4$, so $C(d_{K})=C_{4}$. And the hilbert class group is $L=K(\alpha)$, $\alpha=\sqrt{ 2\sqrt{ 2 }-1 }$, $f_{14}(x)=(x^{2}+1)^{2}-8$, with discriminant $f_{14}=\pm2^{a}7^{b}=-2^{14}7$.

**Theorem**: $p\neq2,7$, odd prime $\exists x,y \in \mathbb{Z},\ p=x^{2}+14y^{2}$ <==> $\left( \frac{-14}{p} \right)=1$ and $(x^{2}+1)^{2}-8\equiv0\pmod{p}$ has an integer solution.

**Lemma**: $K$ a quadraic field, with discriminant $d_{K}$, $K(\sqrt{ a })$ quadraic extension $a \in \mathbb{Z}$, square free. Then $K\subseteq K(\sqrt{ a })$ is unraminfied iff $a$ can be chosen as $a|d_{K}$ or $a\equiv1\pmod{4}$. 

$K\subseteq L$, $Gal(L / K)=C(d_{K})$, $K\subseteq E\subseteq L$, $Gal(L / E)=C(d_{K})^{2}$, $Gal(E / K)=C(d_{K}) / C(d_{K})^{2}$. 

**Theorem**: $K$ imaginary quadraic field, discriminant = $d_{K}$. $M$ be the number of prime factors of $d_{K}$, $p_{1}, \cdots,p_{r}$ be the prime factors of $d_{K}$. $M=\begin{cases}r,\ &d_{K}\equiv1\pmod{4}\\r+1,\ &d_{K}\equiv0\pmod{4}\end{cases}$.Set $p_{i}^{*}=(-1)^{\frac{p_{i}-1}{2}}p_{i}\equiv1\pmod{4}$. Then
1. genus field of $K$ = maximal unraminfied extension of $K$ which is an abelian extension of $\mathbb{Q}$.
2. genus field of $K$ = $K(\sqrt{ p_{1}^{*} }, \cdots, \sqrt{ p_{r}^{*} })$. 
3. number of genera of primitive positive definte forms of discriminant $d_{K}$ is $2^{\mu-1}$.
4. principle genus consists of square of classes.

# Orders in an imaginary quadraic field

**Definition**: A subring $\mathcal{O}\subseteq K$ is called an **order** if $1 \in \mathcal{O}$, $\mathcal{O}$ a subring of $K$, and $\mathcal{O}$ is a finitely generated $\mathbb{Z}$-module with a basis of $K / \mathbb{Q}$. So we know that $\mathbb{Z}\subseteq \mathcal{O}\subseteq \mathcal{O}_{K}$. 

**Lemma**: 
1. $[\mathcal{O}_{K}:\mathcal{O}]=\# \mathcal{O}_{K} / \mathbb{Q}<+\infty$. 
2. Write $f=\#\mathcal{O}_{K} / \mathbb{Q}$, then $\mathcal{O}=\mathbb{Z}+f\mathcal{O}_{K}=[1,fw_{K}]=\mathbb{Z}+w_{K}\cdot \mathbb{Z}$, where $w_{K}=\frac{d_{K}+\sqrt{ d_{K} }}{2}\in \mathcal{O}_{K}$. 

*Proof*: 
1. Choose a basis $\{ x_{1},x_{2} \}$ of $K /\mathbb{Q}$, may assume $x_{1},x_{2}\in \mathcal{O}$. $\mathcal{O}_{K}$ is a finitely generated $\mathbb{Z}$-module. Then $\exists n>1$, s.t. $\mathcal{O}_{K}\subseteq \frac{x_{1}}{n}\cdot\mathbb{Z}+\frac{x_{2}}{n}\cdot\mathbb{Z}$, so $\mathcal{O}_{K} / \mathcal{O}$ has at most $n^{2}$ element.
2. It is easy that $\mathbb{Z}\oplus fw_{K}\cdot\mathbb{Z}\subseteq \mathcal{O}$, with $[\mathcal{O}_{K}:\mathbb{Z}\oplus fw_{K}\cdot \mathbb{Z}]=f$ , so it must be equal. 

**Definition**: call $f=[\mathcal{O}_{K}:\mathcal{O}]$ be the conductor of $\mathcal{O}$, write $\mathcal{O}=\alpha \cdot\mathbb{Z}+\beta \cdot \mathbb{Z}$, and define the **discriminant** of $\mathcal{O}$ to be $D=\left(\det \begin{pmatrix}\alpha&\beta\\\alpha'&\beta'\end{pmatrix}\right)^{2}$, wherer $\alpha=1,\beta=f\cdot \frac{d_{K}+\sqrt{ d_{K} }}{2}$, so $D=f\cdot d_{K}^{2}$. 

**Lemma**: $K=\mathbb{Q}(\tau)$ imaginary quadraic field, "$ax^{2}+bxy+cy^{2}$" = minimal polynomial of $\tau$, then $[1,\tau]=\mathbb{Z}\oplus \mathbb{Z}\tau$ is the proper fractional ideal of the order $[1,a\tau]$ of $K$. 

*Proof*: 
1. We only have to show that $[1,a\tau]$ is a subring of $\mathcal{O}_{K}$. Minimal polynomial of $a\tau$ is $x^{2}+bxy+ac$, then $a\tau \in \mathcal{O}_{K}$. 
2. $a\tau \cdot 1=a\tau \in[1,\tau]$, $a\tau \cdot \tau=-b\tau+(-c) \in[1,\tau]$, thus $[1,\tau]$ is a fractional ideal of $[1,a\tau]$, hence $[1,a\tau]\cdot[1,\tau]\subseteq[1,\tau]$. It is suffices to show that $\{ x \in K:x[1,\tau]\subseteq[1,\tau] \}=[1,\tau]$.  In fact, we only have to check $\subseteq$. Suppose $x[1,\tau]\subseteq[1,\tau]$, then $x=m+n\tau$ as $x\cdot1 \in[1,\tau]$. Then $x\cdot \tau \in[1,\tau]$, hence $\frac{n}{a}b \in \mathbb{Z},\ \frac{n}{a}c \in \mathbb{Z}$ $\implies$ $\frac{n}{a} \in \mathbb{Z}$, so $x=m+\left( \frac{n}{a} \right)a\tau \in[1,\tau]$. 

$I(\mathcal{O})\ \sim$ set of proper fractional ideals of $\mathcal{O}$, $P(\mathcal{O}) \ \sim$ set of principle fractional ideals of $\mathcal{O}$. Let the **Ideal class group** of $\mathcal{O}$ := $I(\mathcal{O}) / P(\mathcal{O})$, with multiplication $a*b=a\cdot b$. 

$\mathcal{O}\subseteq \mathcal{O}_{K}$, $f=\#\mathcal{O}_{K} / \mathcal{O}$ conduction, then $f\mathcal{O}_{K}\subseteq \mathcal{O}\subseteq\mathcal{O}_{K}$. If $f>1$, then $f\mathcal{O}_{K}$ is an ideal of $\mathcal{O}$ not proper. 

**Theorem**: $K$ imaginary quadraic field $\mathcal{O}\subseteq \mathcal{O}_{K}$, order $f=\#(\mathcal{O}_{K} / \mathcal{O})$, $D=\text{discriminant of }\mathcal{O}=f^{2}d_{K}$. 

*Proof*:
1. If $f(x,y)=ax^{2}+bxy+cy^{2}$ is a primitive positive definte form of discriminant $D$, then $\left[ a, \frac{-b+\sqrt{ D }}{2} \right]$ is a proper ideal of $D$. $\mathcal{O}_{K}=\left[1, \frac{d_{K}+\sqrt{ d_{K} }}{2} \right]$, $\mathcal{O}=\left[ 1,f\cdot \frac{d_{K}+\sqrt{D}}{2} \right]$, so $2|b-f\cdot d_{K}$, $D=b^{2}-4ac=f^{2}d_{K}$. 
2. The map $ax^{2}+bxy+cy^{2}\mapsto\left[ a, \frac{-b+\sqrt{ D }}{2} \right]$ induces an isomorphism between "$C(D)$" and "$C(\mathcal{O})$". 
3. A positive integer $m$ is represented by a form $f(x,y)$ iff $m=N(\mathfrak{a})$ of some proper ideal $\mathfrak{a}$ of $\mathcal{O}$. Where $N(\mathfrak{a})=\#(\mathcal{O} /\mathfrak{a} )$. 

*Proof*: 
1. Notice that if we take $\tau=\frac{-b+\sqrt{ D }}{2a}$, then $[a,a\tau]=a[\tau]$ is a proper ideal of $[1,a\tau]$, in this case, it is percisly $\mathcal{O}$.
2. Just consider the roots of $f,g$, $\tau,\tau'$, we show that $f,g$ are properly equivalent iff $\tau'=\frac{p\tau+q}{r\tau+s}$, for some $\begin{pmatrix}p&q\\r&s\end{pmatrix} \in SL(2,\mathbb{Z})$, which is equivalent to $[1,\tau]=\lambda[1,\tau']$. The first part is easy, just consider the $0=f(\tau,1)=(r\tau+s)^{2}g\left( \frac{p\tau+q}{r\tau+s},1 \right)$, so it must be a root of $g$, hence must be $\tau'$. And two forms having the same root ust be properly equivalent. The second equivalence is clear for $\implies$, and the other way around is because that $\lambda \tau'=p\tau+q$ and $\lambda=r\tau+s$, hence $\tau'=\frac{p\tau+q}{r\tau+s}$. 
3. The injection part is obvious, and with some computation, one is able to check that this is true. Just notice that the multiplication happened in $C(D)$ maps ot $C(\mathcal{O})$ as $\left[ a, \frac{-b+f\sqrt{ d_{K} }}{2} \right]\cdot\left[ a', \frac{-b'+f\sqrt{ d_{K} }}{2} \right]\mapsto \left[ aa', \frac{-B+f\sqrt{ d_{K} }}{2} \right]$, or $[a,\Delta],[a',\Delta]\mapsto[aa',\Delta]$ in short. Which is obviously true and with the help of the lemma below, we are able to proof it.

**Remark**: $\mathcal{a}\subseteq \mathcal{O}$, proper ideal, $\mathfrak{a}^{-1}=\frac{1}{N(\mathfrak{a})}\overline{\mathfrak{a}}$. Write $\mathfrak{a}=\alpha[1,\tau]$, $\mathcal{O}=[1,a\tau]$, $\overline{\mathfrak{a}}=\alpha'[1,\tau']$. Then $\mathfrak{a}\cdot \overline{\mathfrak{a}}=N(\alpha)\left[ 1,\tau,-\frac{b}{a}\tau, \frac{c}{a}  \right]= \frac{N(\alpha)}{a}\mathcal{O}$. 

**Lemma**:
1. $N(\alpha \cdot \mathcal{O})=N(\alpha)$, $\alpha \in \mathcal{O}$, $\alpha \neq0$.
2. $N(\mathfrak{a}\cdot \mathfrak{b})=N(\mathfrak{a})\cdot N(\mathfrak{b})$. 
3. $\mathfrak{a}\cdot \overline{\mathfrak{a}}=N(\mathfrak{a})\cdot \mathcal{O}$. 

**Lemma**: let $\mathcal{O}$ be an order of conductor $f$.
1. An $\mathcal{O}$-ideal $\mathfrak{a}$ is prime to $f$ if and only if its norm $N(\mathfrak{a})$ is relatively prime to $f$. 
2. Every $\mathcal{O}$-ideal prime to $f$ is proper.

It follows that $\mathcal{O}$-ideals prime to $f$ lie naturally in $I(\mathcal{O})$ and are closed under multiplication. The subgroup of fractional ideals they generated are denoted as $I(\mathcal{O},f)\subset I(\mathcal{O})$. 

**Proposition**: The inclution $I(\mathcal{O},f)\subset I(\mathcal{O})$ incuced an isomorphism $I(\mathcal{O},f) /P(\mathcal{O},f)\simeq I(\mathcal{O}) /P(\mathcal{O})=C(\mathcal{O})$. 

*Proof*: We know that $I(\mathcal{O},f)\rightarrow C(\mathcal{O})$ is surjective, with kernel $I(\mathcal{O},f)\cap P(\mathcal{O})$, so we have to check that $P(\mathcal{O},f)=I(\mathcal{O},f)\cap P(\mathcal{O})$, infact, only $I(\mathcal{O},f)\cap P(\mathcal{O})\subseteq P(\mathcal{O},f)$ is nontrivial. In this case, take $\alpha \mathcal{O}=\mathfrak{a}\mathfrak{b}^{-1}\in I(\mathcal{O},f)\cap P(\mathcal{O})$, take $m=N(\mathfrak{b})$, then $m\mathcal{O}=\mathfrak{b}\overline{\mathfrak{b}}$, so $m\alpha \mathcal{O}=\mathfrak{a}\overline{\mathfrak{b}}\subset \mathcal{O}$, hence $\alpha \mathcal{O}=m\alpha \mathcal{O}(m\mathcal{O})^{-1}\subset \mathcal{O}$. 

**Proposition**: Let $\mathcal{O}$ be the order of conductor $f$ in an imaginary quadraic field $K$. Then:
1. If $\mathfrak{a}$ is an $\mathcal{O}_{K}$-ideal prime to $f$, then $\mathfrak{a}\cap \mathcal{O}$ is an $\mathcal{O}$-ideal prime to $f$ of the same norm. 
2. If $\mathfrak{a}$ is an $\mathcal{O}$-ideal prime to $f$, then $\mathfrak{a}\mathcal{O}_{K}$ is an $\mathcal{O}_{K}$-ideal prime to $f$ of the same norm.
3. The map $\mathfrak{a}\mapsto \mathfrak{a}\cap \mathcal{O}$ induces an isomorphism $I_{K}(f)\stackrel{\sim}{\longrightarrow}I(\mathcal{O},f)$, and the invers of this map is given by $\mathfrak{a}\mapsto \mathfrak{a}\mathcal{O}_{K}$. Where $I_{K}(f)$ is the group of fractional ideals of $\mathcal{O}_{K}$ prime to $f$. 

**Proposition**: Let $\mathcal{O}$ be an order of conductor $f$ in an imaginary quadraic firld $K$. Then there are natural isomorphism
$$
C(\mathcal{O}) \simeq I(\mathcal{O},f) / P(\mathcal{O}, f) \simeq I_{K}(f) / P_{K,\mathbb{Z}}(f)
$$
where $P_{K,\mathbb{Z}}(f)$ is the subgroup of $I_{K}(f)$ generated by principle ideals of the form $\alpha \mathcal{O}_{k}$,where $\alpha \in \mathcal{O}_{K}$ satisfied $\alpha\equiv a\pmod{f\mathcal{O}_{K}}$ for an integer $a$ relatively prime to $f$. 

*Proof*: As we know, the first isomorphism is already handled, and $I(\mathcal{O},f)\simeq I_{K}(f)$, so it remaind to proof the image $\tilde{P}\subset I_{K}(f)$ of $P(\mathcal{O},f)$ is $P_{K,\mathbb{Z}}(f)$. 

**Theorem**:
$K$ a imaginary quadraic number field, and $\mathcal{O}\subseteq \mathcal{O}_{K}$ be an order, and $f=\#\mathcal{O}_{K} /\mathcal{O}$, then
$$
h(\mathcal{O})=\frac{h(\mathcal{O}_{K})f}{[\mathcal{O}_{K}^{*}:\mathcal{O}^{*}]}\prod_{p|f}\left( 1-\left( \frac{d_{K}}{p} \right) \frac{1}{p} \right).
$$

Where $\left( \frac{d_{K}}{2} \right)=\begin{cases}0\ &2|d_{K}\\1 \ &d_{K}\equiv1\pmod{8}\\-1\ &d_{K}\equiv5\pmod{8}\end{cases}$. 

*Proof*: 
1. $h(\mathcal{O}_{K})=|I_{K} / P_{K}|$ and $h(\mathcal{O})=|I_{K}(f) / P_{K,\mathbb{Z}}(f)|$, with a [[Short exact sequence]] 
$$
0\longrightarrow I_{K}(f)\cap P_{K} / P_{K,\mathbb{Z}}(f) \longrightarrow I_{K}(f) / P_{K,\mathbb{Z}}(f) \longrightarrow I_{K} / P_{K} \longrightarrow 0
$$
   So $\frac{h(\mathcal{O})}{h(\mathcal{O}_{K})}=|I_{K}(f)\cap P_{K} / P_{K,\mathbb{Z}}(f)|$. So we now have to compute $I_{K}(f)\cap P_{K} / P_{K,\mathbb{Z}}(f)$. 
2. Consider $\phi:(\mathcal{O}_{K} / f\mathcal{O}_{K})^{\times}\longrightarrow I_{K}(f)\cap P_{K} / P_{K,\mathbb{Z}}(f)$. sending $[\alpha]=\alpha+f\mathcal{O}_{K}\mapsto\alpha \mathcal{O}_{K}$. As $\alpha+f\mathcal{O}_{k} \in(\mathcal{O}_{K} / f\mathcal{O}_{K})^{\times}$, we know that $\alpha \mathcal{O}_{K}+f\cdot \mathcal{O}_{K}=\mathcal{O}_{K}$, hence it is indeed in $I_{K}(f)\cap P_{K}$. If $[\alpha]=[\alpha']$, then there is a $u \in \mathcal{O}_{K}$ s.t. $u\alpha\equiv u\alpha'\equiv1\pmod{f\mathcal{O}_{K}}$. Thus $u\mathcal{O}_{k}\cdot\alpha \mathcal{O}_{K}=u\alpha \mathcal{O}_{K}=u\alpha'\mathcal{O}_{K}$, hence it is well defined. 
3. The check that $\phi$ is surjective any element in $I_{K}(f)\cap P_{K}$ is of the forme $\alpha \cdot \mathcal{O}_{K}=\mathfrak{a}\mathfrak{b}^{-1}$, for some $\mathfrak{a},\mathfrak{b}\subseteq \mathcal{O}_{K}$, let $m=N(\mathfrak{b})=\#(\mathcal{O}_{K} / \mathfrak{b})$. Now $\mathfrak{a}\overline{\mathfrak{b}}=(m\alpha)\mathcal{O}_{K}$ with $N(m\alpha)=N(\mathfrak{a})N(\mathfrak{b})$ prime to $f$, then $m\alpha+f\mathcal{O}_{K}\in(O_{K} / f\mathcal{O}_{K})^{\times}$, and $\phi(m\alpha)=m\alpha \mathcal{O}_{K}=\alpha \mathcal{O}_{K}\cdot m\mathcal{O}_{K}=\alpha \mathcal{O}_{K}$ in $I_{K}(f)\cap P_{K} / P_{K,\mathbb{Z}}(f)$. Hence $\phi$ is surjective. 
4. To determine $ker(\phi)$ when $\mathcal{O}_{K}^{\times}=\{ \pm1 \}$. We show that there is an exact sequence
$$
1\longrightarrow(\mathbb{Z} / f\mathbb{Z})^{\times} \stackrel{\psi}{\longrightarrow} (\mathcal{O}_{K} / f\mathcal{O}_{K})^{\times} \stackrel{\phi}{\longrightarrow} I_{K}(f)\cap P_{K} / P_{K,\mathbb{Z}}(f) \longrightarrow1
$$
   Therefore, $\#(I_{K} \cap P_{K} / P_{K,\mathbb{Z}}(f))=\frac{\#(\mathcal{O}_{K} / f\mathcal{O}_{K})^{\times}}{(\mathbb{Z} / f\mathbb{Z})^{\times}}=f\cdot \frac{\prod_{p|f}\left( 1- \frac{1}{p} \right)\left( 1-\left( \frac{d_{K}}{p} \right) \frac{1}{p}\right)}{\prod_{p|f} \left( 1-\frac{1}{p} \right)}$. 

# Class field theory and Cebotarev density theorem
Let $K$ be a number field. "modules" in $K$ formal product $\mathfrak{m}=\prod_{p}\mathfrak{p}^{n_{\mathfrak{p}}}$, over primes of $K$, where 
1. $n_{\mathfrak{p}}\geq0$ and $n_{\mathfrak{p}}\neq0$ for a most finitely many primes $p$. 
2. $n_{\mathfrak{p}}=0$ whenever $\mathfrak{p}$ is a complex infinite prime.
3. $n_{\mathfrak{p}}\leq1$ whenever $\mathfrak{p}$ is a real infinite prime.

Write $\mathfrak{m}=\mathfrak{m}_{0}\cdot \mathfrak{m}_{\infty}$, where $\mathfrak{m}_{0}=\prod_{\mathfrak{p}\ finite}\mathfrak{p}^{n_{\mathfrak{p}}}$ and $\mathfrak{m}_{\infty}=\prod_{\mathfrak{p}\ infinite}\mathfrak{p}^{n_{\mathfrak{p}}}$. When all $n_{\mathfrak{p}}$ are $0$, write $\mathfrak{m}=1$. Let $I_{K}(m)$ be the group of all fractional $\mathcal{O}_{K}$-ideals relatively prime to $m$ and let $P_{K,1}(\mathfrak{m})\subseteq I_{K}(\mathfrak{m})$ be generated by $\alpha \mathcal{O}_{K}$, $\alpha \in \mathcal{O}_{K}$ and $\alpha\equiv1\pmod{\mathfrak{m}_{0}}$ and $\sigma(\alpha)>0$ for real infinite prime $\sigma$ dividing $\mathfrak{m}$. In fact, $[I_{K}:P_{K,1}(\mathfrak{m})]<+\infty$. 

A subgroup $H\subseteq I_{K}(\mathfrak{m})$ is called a **conjaguence subgroup for $\mathfrak{m}$**, if $P_{K,1}(\mathfrak{m})\subseteq H\subseteq I_{K}(\mathfrak{m})$ and "$I_{K} / H$" is called the **genrealized ideal class group**. In fact, the class group and orders are just the special case of it. 

Abelian extension $K\subseteq L$, modules $\mathfrak{m}$, $\mathfrak{m}$ is divisable by all ramified primes of $K\subseteq L$. Given any finite porimes $\mathfrak{p}$, relatively prime to $\mathfrak{m}$, we have Artin symbol $\left( \frac{L / K}{\mathfrak{p}} \right)\in Gal(L / K)$. By multiplicativity, get a homomorphism $\phi_{m}=\phi_{L / K,m}:I_{K}(\mathfrak{m})\rightarrow Gal(L / K)$. Call the **Artin map** for $K\subseteq L$ and $m$. 

**Artin reaprocity theorem**: 
$K\subseteq L$, abelian extension, $\mathfrak{m}$ modules of $K$ divisable by all primes of $K$ that ramifies in $L$. 

**Theorem**: 
1. Then Artin map $\phi_{m}$ is surjective.
2. If that exponents of finite primes in $\mathfrak{m}$ are sufficicently large, then $ker(\phi_{\mathfrak{m}})$ is a congruence subgroup for $\mathfrak{m}$, i.e. $P_{K,1}(\mathfrak{m})\subseteq Ker(\phi_{m})\subseteq I_{K}(\mathfrak{m})$. 

Consiquently, there is an isomorphism $I_{K}(\mathfrak{m}) / P_{K,1}(\mathfrak{m}) \stackrel{\sim}{\longrightarrow}Gal(L / K)$.  

**Canductor theorem**: $K\subset L$ abelian extension. There exists a modulus $f=f(L / K)$ s.t.
1. A prime of $K$, ramifies in $L$ iff it divides $f$.
2. let $\mathfrak{m}$ be a modulus of $K$ divisable by all primes of $K$ that ramify in $L$. Then $ker(\phi)$ is a congruences subgroup if and only if $f|\mathfrak{m}$. 

**Existence theorem**: $\mathfrak{m}$ modulus of $K$, $H$ congruences subgroup , $P_{K,l}(\mathfrak{m})\subseteq H\subseteq I_{K}(\mathfrak{m})$. Then there is a unique abelian extension $L / K$, all ramified primes of $L / K$, divides $\mathfrak{m}$ s.t. Artin map $\phi_{\mathfrak{m}}:I_{K}(\mathfrak{m})\rightarrow Gal(L / K)$ satisfies $Ker(\phi_{\mathfrak{m}})=H$. 

**Kroeker-weber theorem**: 
$L / \mathbb{Q}$ an abelian extension, then there is a positive integer $n$ s.t. $L\subseteq \mathbb{Q}(\zeta_{m})$. where $\zeta_{m}=e^{\frac{2\pi\sqrt{ -1 }}{m}}$. 

Take $\mathfrak{m}=1$, by extension theorem, there is a unique abelian extension $L / K$, unraminfied s.t. $C(\mathcal{O}_{K})=I_{K} / P_{K}=I_{K}(\mathfrak{m}) / P_{K,1}(\mathfrak{m})\stackrel{\sim}{\longrightarrow}Gal(L / K)$.  

**Theorem**: $L$ is the maximal unraminfied extension of $K$. 

In fact, this gives a generalized verion of Hilbert class field. Given any modulus $\mathfrak{m}$, the existence theory tells us that there is a unique Abelian extension $K_{\mathfrak{m}}$ of $K$ s.t. $P_{K,1}(\mathfrak{m})=ker(\Phi_{K_{\mathfrak{m}} / K,\mathfrak{m}})$, then $K_{\mathfrak{m}}$ is called the ray class field for the modulus $\mathfrak{m}$, and when $\mathfrak{m}=1$, it reduce to the case of Hilbert class field. 

**Theorem**: $K$ number field, $\mu_{n}=\{ 1, \zeta, \cdots, \zeta ^{n-1} \}$, $0\neq\alpha \in \mathcal{O}_{K}$, $L=K(\sqrt[n]{\alpha})$, $\mathfrak{m}$ modulus of $K$, any prime ideal of $\mathcal{O}_{K}$ containing $n\alpha$ divides $\mathfrak{m}$, and assume that $ker(\Phi_{L / K, \mathfrak{m}})$ is a congruences subgroup for $\mathfrak{m}$. Then the map $I_{K}(\mathfrak{m})\stackrel{\Phi_{L / K, \mathfrak{m}}}{\longrightarrow} Gal(L / K)\hookrightarrow \mu_{n}$, is just the map $\left( \frac{\alpha}{\cdot} \right)_{n}$, where $Gal(L /K) \hookrightarrow \mu_{n}$ is the natural injection. (As $K\subseteq L=K(\sqrt[n]{ \alpha })$ is galois, and $\sigma \in Gal(L /K)$ send $\sqrt[n]{ \alpha }$ to $\zeta \sqrt[n]{ \alpha }$ for some $\zeta \in \mu_{n}$). 

*Proof*: It is sufficicent to show that 
$$
\left( \frac{L /K}{\mathfrak{p}} \right)(\sqrt[n]{ \alpha }) = \left( \frac{\alpha}{\mathfrak{p}} \right)_{n} \sqrt[n]{ \alpha } 
$$
In fact, the equation is correct module $\mathfrak{q}$ for all $\mathfrak{q} \subseteq \mathcal{L}$, $\mathfrak{q}\cap \mathcal{O}_{K}=\mathfrak{p}$. Since $\alpha \not\in \mathfrak{p}$, and $n \not\in \mathfrak{p}$, we have that they must be equal. 

**Theorem**: Let $K$ be a number field containing a primitive $n$th root of unity, and suppose that $\alpha,\beta \in \mathcal{O}_{K}$ are relatively prime to each other and to $n$. Then 
$$
\left( \frac{\alpha}{\beta} \right)_{n} \left( \frac{\beta}{\alpha} \right)_{n}^{-1} = \prod_{\mathfrak{p}|n_{\infty}} \left( \frac{\alpha,\beta}{\mathfrak{p}} \right)_{n}
$$
Where $\left( \frac{\alpha,\beta}{\mathfrak{p}} \right)_{n}$ is the $n$th power Hilbert symbol and $\infty$ is the product of the real infinite primes of $K$. 

**The Cebotarev Density Theorem**

$K$ number field, $\mathcal{P}_{K}$ the set of primes of $K$ Gien $\mathcal{S}\subseteq \mathcal{P}_{K}$, define the **Dirichlet density** of $\mathcal{S}$ to be 
$$
\delta(\mathcal{S})= \lim_{ s \to 1^{+} }  \frac{\sum_{\mathfrak{p} \in \mathcal{S}}N(\mathfrak{p})^{-s}}{-\log(s-1)}
$$

To learn more abot the density, we have to study the Dirichlet $\zeta$-function if $K$, which is defined by
$$
\zeta_{K}(s)=\sum_{\mathfrak{a}\subset \mathcal{O}_{K}}N(\mathfrak{a})^{-s} = \prod_{\mathfrak{p} \in \mathcal{P}_{K}}(1-N(\mathfrak{p})^{-s})^{-1}
$$

**Theorem**: Let $L$ be a Galois extension of $K$, and let $\langle \sigma \rangle$ be the conjugacy class of an element $\sigma \in Gal(L /K)$. Then the set $\mathcal{S}=\left\{  \mathfrak{p} \in \mathcal{P}_{K}: \mathfrak{p} \text{ is unraminfied in } L,\ \left( \frac{L /K}{\mathfrak{p}} \right)=\langle \sigma \rangle  \right\}$ has Dirichlet density $\delta(\mathcal{S})= \frac{\lvert \langle \sigma \rangle \rvert}{\lvert Gal(L /K) \rvert}= \frac{\lvert \langle \sigma \rangle \rvert}{[L:K]}$. 

$K\subseteq L$, $S_{L / K}=\{ \mathfrak{p}\subseteq \mathcal{O}_{K}: \text{prime, split completely in } L \}$. Then density of $S_{L /K}= \frac{1}{[L:K]}$. 

**Theorem**: $L\&M$ are galois extension of $K$. 
1. $L\subseteq M \Longleftrightarrow S_{M /K}\subset S_{L /K}$. 
2. $L=M \Longleftrightarrow S_{M /K}=S_{L /K}$. 

*Proof*: 
1. "=>" clear. On the other hand, Let $N$ be the minimal Galois extension containing both $L$ and $M$. Then $S_{N /K}=S_{M /K}\cap S_{L /K}=S_{M /K}$, hance $[M:K]=[N:K]$ so $M=N$. 
2. Comes immediately from 1.

**Proposition**: $L, M$ finite extension of $K$. 
1. If $M$ is Galois over $K$, then $L\subseteq M \Longleftrightarrow S_{M /K}\subset S_{L /K}$. 
2. If $L$ is Galois over $K$, then $L\subseteq M \Longleftrightarrow S_{M /K}\subset S_{L /K}$. 

Let $K=\mathbb{Q}(\sqrt{ -n })$. $\mathcal{O}\subseteq \mathcal{O}_{K}$ order, $f=[\mathcal{O}_{K}:\mathcal{O}]$, $-4n=f^{2}d_{K}$, $C(\mathcal{O})\simeq I_{K}(f) / P_{K,\mathbb{Z}}(f)$, $P_{K,1}(f)\subseteq P_{K,\mathbb{Z}}\subseteq I_{K}(f)$, generalized (ideal) class group. By existence theorem, there is a unique $L /K$ corresponding to this data. Call $L$ the **ring class field** of the order $\mathcal{O}$. 

1. $L /K$ is unraminfied for all primes of $K$ not dividing $f\mathcal{O}_{K}$.
2. Artin map $\phi :C(\mathcal{O})=I_{K}(f) /P_{K,\mathbb{Z}}(f)\stackrel{\sim}{\longrightarrow}Gal(L /K)$.
3. $[L:K]=\#Gal(L /K)=\#C(\mathcal{O})=h(\mathcal{O})=h(-4n)$. 

**Theorem**: there is a $f_{n} \in \mathbb{Z}[x]$ monic with degree $h(-4n)$, let $p$ be an odd prime, not dividing $n$ and the discriminant of $f_{n}$, then there is $x,y \in \mathbb{Z}$ , $p=x^{2}+ny^{2}$ iff $\left( \frac{-n}{p} \right)=1$ and $f_{n}(x)\equiv0\pmod{p}$. In fact, choose $\alpha \in \mathcal{O}_{L}\cap \mathbb{R}$ generating $L /K$, we can take $f_{n}(x)=min_{\mathbb{Q}}\alpha$. 

**Lemma**: $L /\mathbb{Q}$ galois, and $Gal(L /\mathbb{Q})=Gal(L /K) \rtimes\langle \tau \rangle$, where $\tau$ is the complex conjugation and $\tau\sigma \tau ^{-1}=\sigma ^{-1}$. 

$Gal(L /K)$ is generated by $\left( \frac{L /K}{\mathfrak{p}} \right)$, where $\mathfrak{p}=\left[ a, \frac{-b+\sqrt{ d_{k} }}{2} \right]$ is a prime ideal of $\mathcal{O}_{K}$. 

**Theorem**: $n>0$, $L$ the ring class field of $\mathbb{Z}[\sqrt{ -n }]\subset K=\mathbb{Q}(\sqrt{ -n })$ let $p$ be an odd prime not dividing $n$. Then there is a $x,y \in \mathbb{Z}$ s.t. $p=x^{2}+ny^{2}$ iff $p\mathbb{Z}$ splits completely in $L$. 

*Proof of main theorem*: $L /\mathbb{Q}$ Galois, then choose $\alpha \in \mathcal{O}_{L}\cap \mathbb{R}$ generating $L^{\tau}$ over $\mathbb{Q}$. Then $L=K(\alpha)$, $f_{n}=f_{\alpha}=min_{\mathbb{Q}}(\alpha)$. Then deg $f_{n}$ is $h(-4n)$. So $\left( \frac{-n}{p} \right)=1$ and $f_{n}(x)\equiv0\pmod{p} \Longleftrightarrow$ $p\mathbb{Z}$ splits completely in $L$ $\Longleftrightarrow$ $\exists x,y \in \mathbb{Z}$ s.t. $p=x^{2}+ny^{2}$. 
