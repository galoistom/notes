j adjoint function
Let $T:V \rightarrow W$ be a linear transformation and $V$ has a symmetric bilinear measures, then $T^*:W \rightarrow V$ is called the adjoint function if and only if $(Tv_1|v_2)=(v_1|T^*v_2)$ for all $v_1,v_2 \in V$.
Recall that $ker(T)=ker(T^*T:V \rightarrow V)$, and that $T^*T \in End(V),TT^* \in End(W)$, both are self-adjoint and positive semidefinite.

# SVD
Let $T:V \rightarrow W$ be linear transformation and $n=dim(V),m=dim(W)$, then there is a ONB(单位正交基) $v_1,v_2, \cdots,v_n$ and $w_1,w_2,\cdots,w_m$ and $\sigma_1\geq\sigma_2\geq\cdots\geq\sigma_q$, $q=\min\{m,n\}$, such that $Tv_i=\sigma_i w_i$ if $1 \leq i \leq p$ and $Tv_i=0$ if not. The $(\sigma_i)$ are uniquely determined by $T$ which is called the singular value of $T$. Using the language of matrix, then it is that for any $A \in M_{n \times m}(\mathbb{R})$, then there is $P \in SO(m),Q\in SO(n)$ such that $Q^{-1}AP$ is sort of "diagonal".
**We proof the uniqueness**: We claim that $T^*w_j=\sigma_jv_j$ if $j \leq p$. We let $S$ to satisfy the condition, then $(v_i|Sv_j)=\sigma_j \delta_{ij}$, note that $(Tv_i|v_j)=\sigma_i\delta_{ij}$, then we have $(T|\cdot)=(\cdot|S)$, hence $S=T^*$. After that, we note that $\sigma_i^3$ is the eigenvalue of $T^*T$, so the $\sigma_i$ are uniquely determined.(Using the above result, we can easily construct the $P,Q$, so existence is clear)
In fact, one only need to compute the eigenvalue of $T^*T$, take $\lambda_1,\cdots,\lambda_p$ for example, then $\sigma_i=\sqrt{\lambda_i}$.
# MP inverse
Let $T:V \rightarrow W$ and $S:W \rightarrow V$, we say $S$ is the MP inverse of $T$ if and only if:1.$STS=S$ 2.$TST=T$ 3.$(ST)^*=ST$ 4.$(TS)^*=TS$. We will proof that this inverse is unique.
**The existence:** Let $v \in V, w \in W, v' \in ker(T), v'' \in ker(T)^{\perp}, w' \in im(T), W'' \in im(T)^\perp$ with $v=v'+v'',w=w'+w''$ and $Tv=w'$ we set $Sw:=v''$. It is easy to check that $S$ is well defined. As to the uniqueness, suppose $S,R$ are both MP inverse of $T$, then we have 
$$
S=STS=S(TS)^*=SS^*T^*=SS^*(TRT)^*=SS^*T^*R^*T^*=S(TS)^*(TR)*=STSTR=STR
$$
Hence $S=STR=R$.

# proposition 1:
Let $T:V \rightarrow W$ be a linear transformation, $r:=rank(T)$
Using SVD, we have ONBs: $v_1,v_2, \cdots, v_m$ of V, and $w_1,w_2, \cdots, w_n$ of W, and singular values $\sigma_1\geq\sigma_2\geq\cdots$.
Define $S:W \rightarrow V$, with $Sw_j=\frac{1}{\sigma_J}v_i$ if $1 \leq j \leq r$ and 0 if not.
then $S$ is the MP inverse of $T$.

we proof this using the explicit construction of MP inverse. for any $w \in W$, $w=\sum\limits_{j=1}^{n}a_jw_j$, and $imT=<w_1,w_2, \cdots, w_r>$, hence $w'=\sum\limits_{j=1}^{r}a_jw_j$, and $v=\sum\limits_{i=1}^{r}\frac{a_j}{\sigma_J}v_j \in V$, then $v \in ker(T)^{\perp}$, hence the projection of $v''$ to $ker(T)^{\perp}$ is v. hence $Sw=v''$ agrees with the construction above.

# Min-Max principle:
Let V be a vector space with natural inner product and $B:V\times V \rightarrow \mathbb{R}$ be a symmetric bilinear form. then there is a unique $S \in End(V)$ such that $B(v_1,v_2)=(v_1|Sv_2)$. giving it a corodinates, then we get there is a unique $A \in M_{n \times n}(\mathbb{R})$ such that $B(v_1,v_2)=v_1^{T}Av_2$, moreover, if B is symmetric, we have $A^T=A$,i.e. $S=S^*$. Take $v_1,v_2,\cdots,v_n$ of V, s.t. $Sv_i=\lambda_iv_i$ for all i, $\lambda_1\geq\cdots\geq\lambda_n$.
Simple observation:$\lambda_1=\max\limits_{\lVert v \rVert=1} B(v,v), \lambda_n=\min\limits_{\lVert v \rVert=1} B(v,v)$.
Using this fact, we can give another proof of 正交对角化定理: note that $S^n$ is compact, hence $\max\limits_{\lVert v \rVert=1} (v,Sv)$ exists, and using the fact that $S=S^*$, then we get the max point $v$ is an eigenvector of S (Langrange multiples).

**Theorem(Coueant-fischer)**
Given B, for a $k<1<n=dim(V)$, we have $\lambda_k=\min\limits_{dim(U)=n-k+1}(\max\limits_{\lVert v \rVert=1 \in U}B(v,v))$, and $\lambda_k=\max\limits_{dim(U)=k}(\min\limits_{\lVert v \rVert=1 \in U}B(v,v))$.

*Proof*: we only need to proof the first one. Assume $U \subset V, dim(U)=n-k+1$, then $dim(U \cap \langle v_1,\cdots,v_k \rangle)=dimU+k-dim(U+<v_1,\cdots,v_k>)\geq 1$. We can then take $v=\sum\limits_{i=1}^{k}a_iv_i, \lVert v \rVert=1$, then $B(v,v)=\sum\limits_{i=1}^{k}\lambda_ia_i^2 \geq\lambda_k$, we now check that the maximum exists: Take $U=\langle v_k,\cdots,v_n \rangle$, then for any v, we have $B(v,v) \leq \lambda_l$, hence the inf is attained.

*This is also related to SVD:* 
proposition 2: Let V,W be finite dimensional vector space with inner product. and $T:V\rightarrow W$ be linear transformation and $\sigma_1\geq\sigma_2\cdots$ be its singular values of T. Let $\sigma_i=0$ if i>min(dimV,dimW). Then $\sigma_1=\max\limits_{v \neq 0} \frac{\lVert Tv \rVert}{\lVert v \rVert}$, $\sigma_i=\min\max\frac{\lVert Tv \rVert}{\lVert v \rVert}$, and $\sigma_{dimV}=\min\limits_{V\neq0}\frac{\lVert Tv \rVert}{\lVert v \rVert}$. We proof this by taking $S=T^*T$, and $B(v_1,v_2)=(v_1|T^*Tv_2)=(Tv_1|Tv_2)$, hence $B(v,v)=\frac{\lVert Tv \rVert^2}{\lVert v \rVert^2}$, recall that $\sigma_i^2$ is the eigenvalue of $S$, using the theorem above and take square root, then we are done.

# Positive matrix:
We define $A \geq B$ if $a_{ij}\geq b_{i,j}$. Then $A>0,A\geq0$ make sense. Then we have the following lemma: if $A \in M_{m \times n}(\mathbb{R})>0, x \in \mathbb{R}^n\geq0$, then $Ax>0$. To study eigenvalues and eigenvector of $A>0$. Define the spectral radius $S(A)=\max\limits_{\lambda}|\lambda|$, where $\lambda$ runs through A's eigenvalues.
Theorem: Let $A>0$
1. if S(A)>0, then there is a $v>0$ such that $Av=S(A)v$.
2. if $\mu$ is a eigenvalue of A $\neq S(A)$, then $|\mu|<S(A)$. 
3. the S(A)-eigenspace has dim 1.
4. S(A) is a simple root of A 的特征多项式.
(More general version for $A\geq0$(+conditions) "Perron-Frobenius Theorem")

**we proof the frist statement**: Let $S:=\{x\in \mathbb{R}^n:\lVert x \rVert=1,x\geq0\}$, which is compact. Consider the continuous map $\mathcal{L}:S \rightarrow \mathbb{R}_{\geq0}$, $x \mapsto \min\{\frac{(Ax)_i}{x_i}:1 \leq i \leq n, x_i \neq 0\}$. So there is a $v \in S$ that attains the maximum $S>0$ at v. We claim that $Av=S(A)v$. $\mathcal{L}(v)=S$ hence $Av \geq Sv$ if $Av\neq Sv$, then $Av-Sv>0$, so we get $A(Av-Sv)>0$. For a small $\epsilon>0$ $A(Av-Sv)>\epsilon Av$, thus $Aw>(S+\epsilon)w$, where $w=t\cdot Av$, which is to say $\mathcal{L} \geq S+\epsilon$. the contradiction shows that $Av=Sv$. We also have $S \leq S(A)$, to show $S=S(A)$, we take $\mu\in\mathbb{C}, w\in \mathbb{C}^n-{0}, Aw=\mu w$,then for any i, $|(\mu w)_i|=|\mu||W_i|$, so $|\sum a_{ij}w_j| \leq \sum a_{ij}|w_j|$, we now take $w'\in\mathbb{C}^n$ whose i-th value is $|w_i|$, scaling it to have absoluate value 1. Hence $S(A) \geq S \geq \mathcal{L}(w') \geq |\mu|$ for all eigenvalue $\mu$, thus we have $S=S(A)$.

**We now proof (2)**: what we need is to show is that $|\mu|=S(A)$ leads to $\mu=S(A)$. The consiquence is that $|\mu|=S(A)$ shows that $\mathcal{L}(w')=\max \mathcal{L}$, hence $\sum\limits_{j}a_{ij}|w_j|=|\sum\limits_j a_{ij}w_j|$, so $w_i$ are all on the same ray in $\mathbb{C}$. Take a $c \in \mathbb{C}$ such that $c^{-1}w_i \in \mathbb{R}_{\geq0}$, then we have $A(c^{-1}w)=\mu(c^{-1}w)$, hence $\mu \in \mathbb{R}_{\geq 0}$, so we have $\mu=S(A)$.

**Proof of (3)**: Suppose $v,v' \in \mathbb{R}^n$, $Av=S(A)v,Av'=S(A)v'$, and $v>0$, we want to show that $v' \in \mathbb{R}v$. If not, we may choose $\epsilon>0$ s.t. $v-\epsilon v'>0$, but $\exists i,(v-\epsilon v')_i=0$. Then $(v-\epsilon v')=S(A)^{-1}A(v-\epsilon v')>0$, a contradictiom.

**Proof of (4)**: May assume $n \geq 2$. Fix $v>0$, $Av=S(A)v$, $S(A)=S(A^T)$. Then $\exists u\in\mathbb{R}^n,u>0,s.t.A^Tu=S(A)u$, let $\langle u \rangle:=\mathbb{R}u, \langle u \rangle^{\perp}:=\{x\in\mathbb{R}:u^{\perp}x=0\}$ is A-invariant. Note that $\langle u \rangle^{\perp}$ has dimension n-1 and $u^Tv=0$, we have $\mathbb{R}^n=\langle v\rangle \oplus \langle u \rangle^{\perp}$, so $Char_A=Char_{A|_{\langle v \rangle}} \cdot Char_{A|_{\langle u \rangle^{\perp}}}$. If $(x-S(A))^2|Char_A$, then $Char_{A|_{\langle u \rangle^{\perp}}}(S(A))=0$, so we get a $S(A)-eigenvector$ $v'$ in $\langle u \rangle^{\perp}$, contradicting (3).#
**More general version**: Forbenius-perron Theorem for $A \geq 0$.
**Application**: Page rank algorithm.

# Complex inner product
**Recall**: real IRS=$\mathbb{R}$-v.s V + symmetric bilinear form which is positive definite.
Idea: complex $\times$ IPS=$\mathbb{C}$-v.s. V form $(\cdot|\cdot):V\times V \rightarrow \mathbb{C}$ with pisitive definite.

**Definition**: 
Let $T:V\rightarrow W$ be a map between $\mathbb{C}-v.s.$ If $T(v_1+v_2)=Tv_1+Tv_2$ and $T(zv_1)=\bar{z}\,Tv_1$, we say that it is a semi-linear(半线性)
A cplx IPS:=$\mathbb{C} -v.s.$ V + map $(\cdot|\cdot):V\times V \rightarrow \mathbb{C}$, linear in $v_2$ and semi-linear in $v_1$, then $(v_1|v_2)=(v_2|v_1),(v|v)+0$. 

**Construction**: 
given a $\mathbb{C}-v.s.$ V, consider the same set V ans the same $+:V\times V\rightarrow V$, but with $\odot:\mathbb{C}\times V\rightarrow V$ that $(z,v) \mapsto \bar{z} v$. Then $(V,+,\odot)$ forms a $\mathbb{C}-v.s.$, we denote it as $\overline{V}$. Then we have $\overline{\overline{V}}=V$, and are additive under direct sum, mean while, by sending $z\mapsto \bar{z}$, we get an isomorphism between $\mathbb{C}$ and $\overline{\mathbb{C}}$. Moreover, semi-linear map $T:V\rightarrow W$ is the linear map $\overline{V} \rightarrow W$ or $V \rightarrow \overline{W}$, thus $Hom(\overline{V},W)=Hom(V,\overline{W})$. We also notice that $\overline{Hom(V_1,V_2)}=Hom(\overline{V_1},\overline{V_2})$. Recall that $V^*=Hom(V,\mathbb{C})$, then we have $\overline{V}^*=\overline{Hom(V,\overline{\mathbb{C}})}$ and is isomorphic to $\overline{Hom(V,\mathbb{C})}=\overline{V^*}$. 

**Definition**: 
Let $V,W,X$ be $\mathbb{C}-v.s.$ We asy a map $B:V\times W\rightarrow X$  is a sesquilinear(半双线性) if $B$ is semi-linear in $V$ and linear in $W$. All sesquilinear $V\times W \rightarrow X$ form a $\mathbb{C}-v.s$ by $(B_1+zB_2)(v,w)=B_1(v,w)+zB_2(v,w)$, where $B_i$ sesquilinear and $z \in \mathbb{C},v\in V,w\in W$. Specially, let $X=\mathbb{C}$, then we get the definition of sesquilinear form.

**Definition**: 
Let $B:V\times W \rightarrow \mathbb{C}$ be sesquilinear, then the left radical is $ker(B(\cdot,W))$, similiarly, right radical is $ker(B(V,\cdot))$. When $dimV,dimW<\infty$, if let and right radical are both $\{0\}$, then we say $B$ is nondegenerated. Similiar to real bilinear form, we have that when $dimV=dimW$ then $B$ is nondegenerated $\Longleftrightarrow$ Left rad = $\{0\}$ $\Longleftrightarrow$ Right rad = $\{0\}$. We can also get that if $B$ is nondegenerated, we induces $W\simeq \overline{V}^*,\overline{V}\simeq W^*$.
Sesquilinear forms and maxraices: Let $V=\mathbb{C}^n,W=\mathbb{C}^m$, the $B$ takes the form of $A\in M_{m\times n}(\mathbb{C})$. 

**Definition**:
Let $V:\mathbb{C}-v.s.$ $\epsilon\in \{1,-1\}$, $B:V\times V\rightarrow \mathbb{C}$ is a sesquilinear, we say that $B$ is $\epsilon-Hermitian$ if $\overline{B(v,w)}=\epsilon B(v,w)$ 

# Adjoint linear maps
**Def-prop** 
Let $B_1:V_1\times V_1' \rightarrow \mathbb{C}$ and $B_2:V_2\times V_2' \rightarrow \mathbb{C}$ be nondegenerated sesquilinear forms, then there is a semi-linear map $Hom(V_1,V_2) \rightarrow Hom(V_1',V_2'),T\mapsto T^*$, characterized by $B_2(T(v_1),v_2')=B_1(v_2,T^*(v_1'))$, there is also a $Hom(V_1',V_2')\rightarrow Hom(V_1,V_2)$ such that $B_2(v_2, T(v_1'))=B_1(^*T(v_1),v_1')$. There are three ways to proof this:
1. Repeat the proof in the bilinear case
2. Reduce to the bilinear case by passing $\overline{V_1},\overline{V_2}$.
3. Look at the matrices: $V_i,V_i'$ can be written in the form of $\mathbb{C}^{m_i},\mathbb{C}^{m_i'}$ up tp isomorphism, which maps $B_i$ to invertible matrix $A_i \in M_{m_i\times m_i'}(\mathbb{C})$, then $$B_2(Tv_1,v_2')=(Tv_1)^tA_2v_2=v_1^tT^tA_2v_2=v_1^tA_1A_1^{-1}T^tA_2v_2=v_1^tA_1T^*v_2$$the other one is similiear
**Observation**: 1.$(ST)^*=T^*S^*,^*(ST)=^*T^*S$ 2. $^*(T^*)=T=(^*T)^*$ 3. If $\epsilon=\pm 1$ both $B_1,B_2$ are $\epsilon-Hermitian$, then $^*T=T^*$.

**Definition**: Given a nondegenerated $\epsilon-Hermitian$ form ($\epsilon=\pm1$) $B:V\times V\rightarrow \mathbb{C}$, and $T\in End(V)$, then $T=T^*$ is self-adjoint, $T^*=-T$ is anti-adjoint.
**Remark**: Let $c\in i\mathbb{R}-{0}$, then $B:V\times V \rightarrow \mathbb{C}$ is Hermitian $\Longleftrightarrow$ $cB$ is anti-Hermitian, $T \in End(V)$ is self-adjoint $\Longleftrightarrow$ $cT$ is anti-adjoint.

**Definition**: $dimV<\infty, B:V\times V\rightarrow \mathbb{C}$ be $\epsilon-Hermitian$, Then $T\in End(V)$ is normal if and only if $T^*T=TT^*$.

# Hermitian forms
Recall the quadratic forms say over $\mathbb{R}$. Then a $\sum\limits_{1\leq i,j\leq n}a_{ij}x_ix_j$, where $a_{ij}=a_{ji}$, is equvalient to a $A\in M_{n\times n}(\mathbb{R})$ where $A^T=A$, and a bilinear form $B:\mathbb{R}^n\times\mathbb{R}^n\rightarrow\mathbb{R}$.
We usie the similiar notions. Let $\sum\limits_{1\leq i,j\leq n}a_{ij}\overline{x_i}x_j$ be hermitian form, then it is equvalient to $A\in M_{n\times n}(\mathbb{C}): \epsilon-hermintian$ and $B:\mathbb{C}^n\times\mathbb{C}^n\rightarrow\mathbb{C}$ a $\epsilon-hermintian\}$.
To classify them, we can reduce to the quadratic forms over $\mathbb{C}$, or using "spectral theorem" for self-adjoint matrices, or copy the arguments for quadratic forms.

Using the third way: 
1. 对角化, we state that for any $f=\sum\limits_{1\leq i,j\leq n}a_{ij}\overline{x_i}x_j$ is $\simeq$ to a "diagonal" $f'=\sum a_i |x_i|^2,a_i\in \mathbb{R}$. 配方即可
2. 伸缩, let $x_i'=|a_i|^{\frac{1}{2}}x_i$, then we reduce to the case where $a_i\in\{1,0,-1\}$, so it can be expressed as $|x_1|^2+\cdots+|x_p|^2-|x_{p+1}|^2-\cdots-|x_{p+q}|^2$, where $p,q\in \mathbb{Z}_{\geq 0},\,p+q\leq n$.
Thus we get the following proposition: Given $n\in \mathbb{Z}_{\geq 1}$, then the hermitian form $\{f:\mathbb{C}^n \rightarrow \mathbb{R}\}$ has a one-to-one morphism to $\{(p,q)\in\mathbb{Z}_{\geq0}:p+q\leq n\}$.

**Definition:** Given $V:\mathbb{C}-v.s.$ and $B:V\times V\rightarrow \mathbb{C}$ be hermitian form, we say that $B$ is positive semi-definite if an only if $B(v,v)\in \mathbb{R}$, and positive definite if $B(v,v)\geq 0$ for all $v$. Those notion is only related to the isomorphism class of $(v,B)$, hance is determined by the pair $(p,q)$, and the first case is that $q=0$, the second is $p=n$, for other notion similiar to quadratic forms, we won't write that down specifically.

**Definition:** If an Hermitian form $(|):V \times V \rightarrow \mathbb{C}$ which has positive definite, then it is called a Hermitian IPS. Then for all $v\in V$, we define $\Vert v \Vert := \sqrt{(v \vert v)}$. If $\Vert v \Vert =1$, then we sety that $v$ is a unit vector. Let $S \subset V$, we say that $S$ is orthogonal if $\forall v\neq w \in S, (v \vert w)=0$, and $S$ is orthonormal if $S$ is orthogonal and $\forall v\in S, \Vert v \Vert =1$. It is easy to see that if $S$ is orthogonal, then it is linearly independent.

**Definition:** $V:IPS/\mathbb{C}$, let $V_0,V_1 \subset V$ be subspaces, then $V_0 \perp V_1$ means that $\forall v_0 \in V_0, v_1 \in V_1, (v_0 \vert v_1)=0$. Given a family of $(V_i)_{i \in I} \in V$, if $V = \bigoplus V_i$, and $V_i \perp V_j$ then we say that $V$ is orthogonal direCT sum of $(V_i)_{i \in I}$.
**Fact**: If $V:IPS/\mathbb{C}$, and $V_0 \subset V$,be a subspaces, $dimV_0<\infty$, then $V_0^\perp :=\{v \in V: (v_0 \vert v)=0, \forall v_0 \in V_0 \}$ has the property of $V=V_0 \oplus V_0^\perp$.

**Theorem**(Caushy-Bunyakousky-Schwary): In a $V:IPS/\mathbb{C}$, we have 
$$\vert (v | w) \vert^2  \leq (v | v) \cdot (w|w),\forall v,w \in V$$
Proof: For all $t \in \mathbb{C}$, we have $0 \leq \Vert v+tw \Vert^2 = \Vert v \Vert^2 + 2Re(v|tw) + \Vert tw \Vert^2$, put $t=\frac{-(w|v)}{(w,w)}$, to get $0 \leq \Vert v \Vert^2 - \frac{|(v|w)|^2}{(w|w)}$, the equality holds if and only if there is a $t \in \mathbb{C}$ such that $v+tw=0$. This theorem leads to the triangle inequality $\Vert v+w \Vert \leq \Vert v \Vert + \Vert w \Vert$. #

**Theorem**(Gram-Schmidt):  Let $V:IPS/\mathbb{C}$ and $v_1,v_2, \cdots$ be linearly independent in $V$, define inductively, let $w_1=v_1$ and $w_k=v_k-\sum\limits_{i=1}^{k-1} \frac{(w_i|v_k)}{(w_i|w_i)}w_i$, then $(w_i)$ are orthogonal and $\langle v_1, \cdots, v_k \rangle=\langle w_1, \cdots, w_k \rangle$.

Proof: trivial.#

Using this theorem, we can extend a set of orthogonal elements to a orthogonal basis of a finite dimensional $IPS/\mathbb{C}$. Moreover, there will always be an orthonormal basis for finite dimensional $V:IPS/\mathbb{C}$.

Examples: 
1. standard inner product on $\mathbb{C}^n$, the standard basis is an ONB.
2. Function space: Let $a<b \mathbb{R}$ and $C[a,b]:=\{f:[a,b] \rightarrow \mathbb{C},\, continuous\}$ be a $\mathbb{C}-v.s.$ by $(f+cg)(x)=f(x)+cg(x)$, and $(f|g):= \int_a^b \bar{f}g dx$. Then $\mathbb{C}[x]$ restric to $[a,b]$ forms an ONB in $C[a,b]$.

Notions of isomorphism: Let $V,W:IPS/\mathbb{C}$ If $T\in Hom(V,W)$, $\Vert Tv \Vert_W= \Vert v \Vert_V$, then we say that $T$ is isometry. Notice that $T$ is isometry $\Longleftrightarrow$ $T$ preserve the inner product. Moreover $T$ is an isomorphism between $IPS/\mathbb{C}$. Suppose $dimV=n \in \mathbb{Z}_{\geq1}$, then the isomorphism $\mathbb{C} \rightarrow V$ has a bijection with the ordered ONB of $V$.

**Definition**: the unitary operator on an $IPS/\mathbb{C}$ is the isomorphism $T:(V,(|)) \rightarrow (V,(|))$,  such that $T^*=-T$, a matrix is unitary if and only if $^\dagger A=-A$. We can see that $P$ unitary $\Longleftrightarrow$ $^\dagger PP=I_n$. On the other hand, it is also equvalient to $P \cdot (^ \dagger P)=I_n$. 

# Spectral theorem for normal operators
Recall: $T \in End(V)$, is said to be normal if $TT^*=T^*T$.

**Theorem**: The following are equvalient for $T \in End(V)$:
1. there is an $ONB$ $v_1, \cdots v_n$ of $V$ and $\lambda_1 \cdots \lambda_n \in \mathbb{C}$ s.t. $Tv_i=\lambda_iv_i$ for all $i$.
2. $T$ is normal.
Taking $V=\mathbb{C} + std.IP$, then 1 says: $T$ unitary such that $P^{-1}AP$ is diagonal matrix when $A \leftrightarrow T$. 

Proof: 
1. ($1 \rightarrow 2$) Choosing $ONB$ of $V$, one may assume $V=\mathbb{C}^n,\,T \leftrightarrow A\in M_{n\times n}(\mathbb{C})$, then $P^{-1}AP=\begin{pmatrix}\lambda_1&&\\&\ddots&\\&&\lambda_n\end{pmatrix}$, so we have $T^* \leftrightarrow \,^\dagger P^{-1}\begin{pmatrix}\overline{\lambda_1}&&\\&\ddots&\\&&\overline{\lambda_n}\end{pmatrix}\,^\dagger P=P\begin{pmatrix}\overline{\lambda_1}&&\\&\ddots&\\&&\overline{\lambda_n}\end{pmatrix}P^{-1}$ hence $T$ is normal.
2. ($2 \rightarrow 1$) Any $T \in End(V)$, decomposes uniquely as $T'+T''$, with $(T')^*=T',\,(T'')^*=-T''$. If $T$ is normal, then $T'T''=T''T'$.  One should also noteice that if $V_0 \subset T$ is a $T-invariant$ subspace, then $V_0^{\perp}$ is $T^*-invariant$. 
3. The first case is when $T^*=T$, we proof that there is a $v_1 \in V,\lVert v_1 \rVert =1$ and $\lambda_1 \in \mathbb{R}\, s.t.\, Tv_1=\lambda_1v_1$.  Just consider any eigenvalue $\lambda$ we have $(Tv_1|v_1)=\lambda(v_1|v_1)$ hence $\overline{\lambda}=\lambda$. Using the facts mentioned above, we now that we can split $V=\langle v_1 \rangle \oplus \langle v_1 \rangle^{\perp}$ and use induction. Thus we proof the case.
4. The second case s when $T^*=-T$, one might notice that multiplying $\sqrt{-1}$, one get the case of 3.
5. Third case is the general case. Let $T=T'+T''$, then $T'T''=T''T'$,  同步正交对角化 $V=V_{\mu_1} \oplus \cdots \oplus V_{\mu_m}$ where $\mu_1, \cdots, \mu_n$ are the distinct eigenvalue of $T'$ and $V_{\mu_i} \perp V_{\mu_j}$ if $i \neq j$, where $V_{\mu_i}$ is the eigenspace of $\mu_i$. Notice that $T'T''=T''T'$, so $V_{\mu_i}$ is stable under $T''$, and $(T''|_{V_{\mu_i}})^*=-(T''|_{V_{\mu_i}})$, so $V_{\mu_i}$ has an $ONB$ consisting of eigenvectors of $T''$, so we get an $ONB$ of $V$. Both $T',T''$ acts on it as a scalers and so does $T=T'+T''$.

# Facts for $IPS/\mathbb{R}$ carry over to $\mathbb{C}$
**Theorem**: Let $f:\mathbb{C}^n \rightarrow \mathbb{R}$ be an hermitian form corresponding $A \in M_{n \times n}(\mathbb{C})$ then $f$ is positive definite if and only if all the eigenvalues of $A$ are positive. 

Proof: Using the spectral theorem, there is a unitary $C$ s.t. $^\dagger CAC=\begin{pmatrix}\lambda_1&&\\&\ddots&\\&&\lambda_n\end{pmatrix}$, where $\lambda_i \in \mathbb{R}$, hence $f \simeq \sum\limits_{i=1}^n \lambda_i|x_i|^2$ as hermitian form on $\mathbb{C}^n$, so every $\lambda_i \geq 0$.

Let $T \in End(V),\,^*T=T$, then $(v_1,v_2) \mapsto (Tv_1|v_2)=(v_1|Tv_2)$ is Hermitian. We say $T$ is positive definite if this Hermitian form is. Let $V,W$ be $IPS/\mathbb{C}$ ans $Hom(V,W)$ $\Rightarrow$ $T^*T \in End(V),\,TT^* \in End(W)$ are both simi-definite as $(T^*Tv|v)=(Tv|Tv) \geq 0$, in fact $kerT^*=(imT)^\perp$, noticing that $(T^*w|v)_W=(w|Tv)_V$.

**Def-prop**: If $T\in End(V)$  is positive definite, then there is a unique $S \in End(V)$ such that $T$ is positive definite and $S^2=T$, we denote $S$ as $\sqrt{T}$. (The proof is the same as the case in $\mathbb{R}$ using spectral therorem.)

**Theorem**(极分解/polar decomposition): Let $T \in End(V)$ be invertable, then there is a unique pair of $R,U \in End(V)$ s.t. $T=RU$ and $R$ is opsitive definite $R^*=R$ and $U$ unitary. (Special case is when $V=\mathbb{C}$, the theorem is simply $z=r \cdot e^{i\pi\theta}$)

**Theorem**(SVD/$\mathbb{C}$):Let $V,W$ be $IPS/\mathbb{C}$ with $dim(V)=m,dim(W)=n$ finite dimensional, and $T \in Hom(V,W)$, then there is a $ONB$ $v_1,\cdots,v_m$ of $V$ and $w_1,\cdots,w_n$ of $W$, and $\sigma_1 \geq \cdots \geq \sigma_p \geq 0,p:=\min\{m,n\}$, such that $Tv_i=w_i$ if $1 \leq i \leq p$. Then $\sigma_i$ are unique for $T$, we call it the singular values of $T$.

Proof: $T^*T \in End(V)$, which is self adjoint and positive semidefinite. Using spectral theorem, one get that ites eigenvalue $\lambda_1 \geq \cdots \geq \lambda_p \geq \cdots \geq 0$, and eigenvalue $v_1,\cdots,v_m$ are ONB, taking $\sigma_i=\sqrt{\lambda_i}$, the rest is the same as the real version. #
SVD says: $\exists$ unitary matrices $P:m \times m,Q:n \times n$, and $\sigma_1 \geq \cdots \geq \sigma_p \geq 0$ such that $^\dagger QAP=P^{-1}AP=\begin{pmatrix}\sigma_1&&\\&\ddots&\\&&\sigma_p\end{pmatrix}_{n \times m}$.

**Def-Thm**(Moore-Perose inverse): for any $T \in Hom(V,W),\exists!S \in Hom(W,V)$ s.t. $TST=T,STS=S,(TS)^*=TS,(ST)^*=ST$.

Proof: same as the $\mathbb{R}$ version.

# Orthogonal transformation/operators on $IPS/\mathbb{R}$
Let $V:IPS\mathbb{R}$, $dimV<\infty$, recall that $T \in End(V)$ is orthogonal if $T^*=T^{-1}$, so we have that $detT = \pm 1$.

**Definition**: We say $T \in End(V)$ is normal if $^*TT=TT^*$.

Lemma: if $T$ normal, $\exists k \geq 0$ s.t. $T^k=0_V \in End(V)$, then $T=0_V$

Proof: Work with matrix, using sepctral theorem(for $\mathbb{C}$), then there is a unitary $P$ s.t. $P^{-1}AP=\begin{pmatrix}\lambda_1&&\\&\ddots&\\&&\lambda_p\end{pmatrix}$, then $P^{-1}A^kP=\begin{pmatrix}\lambda_1^k&&\\&\ddots&\\&&\lambda_p^k\end{pmatrix}$, hence $\lambda_i=0$, so $T=0$.
Next: classify orthogonal transformation on $V:IPS/\mathbb{R}$, $dimV=n$. Observe that $A \in M_{n \times n}(\mathbb{R})$ is orthogonal $\Longleftrightarrow$ $A=(v_1| \cdots | v_n)$ forms an $ONB$ of $\mathbb{R}^n$.

Examples:
1. if n=1, then the orthogonal transformations are $\{\pm id_V\}$.
2. assume $V=\mathbb{R}^2+std.IP$, then the orthogonal transformation must be sort of rotation: $R(\theta)=\begin{pmatrix}\cos\theta&-\sin\theta\\\sin\theta&\cos\theta\end{pmatrix}$. It is a two dimensional representation of topological group $\mathbb{R}$ (c.f. [[Basic Definitions of representation]]). 

**Theorem**:
$n:=dim(V)$. Let $T \in End(V)$ be orthogonal then there is a $ONB$ under which $T$ becames 
$$
\begin{pmatrix}I_a&&&&\\
&-I_b&&&\\
&&R(\theta)&\\
&&&\ddots&\\
&&&&R(\theta_m)\end{pmatrix}
$$
where $a+b+2m=n,\theta_1,\cdots,\theta_m \in \mathbb{R}-\mathbb{Z}\pi$.

Lemma: $T$ orthogonal, then $T+T^{-1}$ is self-adjoint and its eigenvalue $\in [-2,2]$.

Proof:Let $S=T+T^{-1}$ then $V= \oplus_{\lambda \in [-2,2]} V_\lambda$, where $V_\lambda:=\{v \in V: Sv=\lambda_v\}$, and $\lambda$ runs through the eigenvalue of $S$, $TS=T^2+1=ST$, so $V_\lambda$ is $T-invariant$, so we reduce to the cease $V=V_\lambda$, i.e. $T+T^{-1}=\lambda \cdot id_V$. If $\lambda = \pm 2$, then $(T \mp id_V)^2=0_V$, and that $T \mp id_V$ is normal, so $T=\pm id_V$. If $|\lambda|<2$, then $T$ has no real eigenvalues. Fix $v \in V$, $v \neq 0$ and $Tv,v$ are linearly independent. Let $W= \langle v,Tv \rangle$, then $dimW=2$, invariant under $T$, so $W^\perp$ is invariant under $T^*=T^{-1}$, so $W^\perp$ is also $T-invariant$, hence $V=W \oplus W^\perp$. Using induction, we reudce the case to $V=V_\lambda, |\lambda|<2, dimV=2$, in which $x^2-\lambda x+1$ is the characteristic polynomial of $T$, hence $T=R(\theta),\theta \in \mathbb{R}-\mathbb{Z}\pi$ under $ONB$.
*Remark*: the data $a,b,\theta_1,\cdots, \theta_m$ are uniquely determined by $T$ up to permutation by $\pi\mathbb{Z}$.

Next we will consider the special case of $dimV=3$. 
Definition: We say $T \in End(V)$ is a ratation if $T$ is orthogonal, $det(T)=1$.

**Definition**:
Let $V:IPS/\mathbb{R}$ dimV=3. A rotation in $V:=$ orthogonal $T \in End(V)$ with $det(T)=1$.

**Theorem**:
they are either $I_3,\begin{pmatrix}1&\\&-I_2\end{pmatrix},\begin{pmatrix}1&\\&R(\theta)\end{pmatrix}$ for some suitable $ONB$, i.e. they act as rotating $v_2$ with angle $\theta$ around $v_1$. We may assume that $V= \mathbb{R}^n$.

*Recall:* There is bijection $\{T \in GL(V)\} \leftrightarrow \{\text{ordered basis in } V\}$. We denote the ordered basis of $V$ by the frame basis of $V$. We say that two frames $v_1, \cdots, v_n$ have the same orientation if $detT>0$ and $T(e_1, \cdots, e_n)=(v_1, \cdots,v_n)$. Now asssume $V:IPS/\mathbb{R},dimV=n$, fix $e_1, \cdots, e_n$ a ordered $ONB$. Orthogonal frames := frames $v_1, \cdots,v_n$ that is an $ONB$ in $V$. We say a frame is positive orientated if the orthogonal frame has tha same orientation with $e_1, \cdots, e_n$. Hence: $\{\text{rotations in } \mathbb{R}^3\} \leftrightarrow \{\text{positive orientated frame in } \mathbb{R}\}$. $\forall u \in \mathbb{R}^3$ let $R_u(\theta):=$ the rotatate $\theta$ around $u$. Take the orthogonal frame $u=u_1,u_2,u_3$ then $R_u(\theta):=\begin{pmatrix}1&\\&R(\theta)\end{pmatrix}$ under the $ONB$ $u_1,u_2,u_3$. Easy to check that the definition does not depend on the choice of $u_2,u_3$.

**Euler's angle**:
Fix $T$. $u_1,u_2,u_3$ as above.
First set $f_2=e_3 \times u_3$ if $e_3,u_3$ are linearly independent, $f_2=e_2$ if $e_3 \parallel u_3$, then $f_2 \perp e_3,u_3$, then we may take $R_{e_3}(\psi)e_2=f_2$, and the map $R_{e_3}(\psi):(e_1,e_2,e_3) \mapsto (f_1,f_2,e_3)$ for some $f_1$ is a positive orientated orthogonal frame.
The second step is taking $\theta$ such that $R_{f_2}(\theta)e_3=u_3$, then tht map $R_{f_2}(\theta):(f_1,f_2,e_3) \mapsto (g_1,f_2,u_3)$ for some $g_1$ is a positive orientated orthogonal fram.
The third step is note that $g_1,u_1$ are both $\perp u_3$, the one may choose $\phi$ such that $R_{u_3}(\phi)g_1=u_1$, sending $R_{u_3}(\phi):(g_1,f_2,u_3) \mapsto (u_1, \cdot, u_3)$, then the $\cdot$ must be $u_2$. 

**Theorem**:
Let $T$ be a rotation in $\mathbb{R}^3$ corresponding to $(u_1,u_2,u_3)$ then $T=R_{u_3}(\phi)R_{f_2}(\theta)R_{e_3}(\psi)$ we say $T$ is  expressed by the *Euler angles* $(\phi,\theta,\psi)$.

# Quaternion's (四元数)
$\mathbb{R} \subset \mathbb{C} \subset \mathbb{H}$: where $\mathbb{H}$ is the quaternions (Hamilton) which is a division ring.

**Definition**:
$\mathbb{H}$ is a 4 dimensional $\mathbb{R}$ vector space, which basis $1,i,j,k$ and multiplication $i^2=j^2=k^2=-1$ and $ij=k,jk=i,ki=j$, and span linearly to the multiplication of the ring(one can check that it is indeed a ring). Moreover, it is noncommutaive.
One immediately know that we can embed $\mathbb{C} \hookrightarrow \mathbb{H}$ as a subring by $a+bi \mapsto a+bi$. Hence $\mathbb{H}$ became a $\mathbb{C}-v.s.$ by $(a+bi,q) \mapsto (a+bi)q$. One has $dim_{\mathbb{C}}\mathbb{H}=2$, with basis $\{1,j\}$.

Consider the center $Z(\mathbb{H})$, assume $z=a+bi+cj+dk$, and using $zi=iz$, one get $c=d=0$, similiar arguments show that $b=c=d=0$, hence $Z(\mathbb{H})=\mathbb{R}$. Now we want to proof that $\mathbb{H}$ is a *division ring*, i.e. every nonzero emelent $z \in \mathbb{H}$ has an inverse.

**Definition**:
For $q \in \mathbb{H}$, let $\overline{q}:=a-bi-cj-dk$ to be its conjugate if $q=a+bi+cj+dk$ with trace $Tr(q):=q+\overline{q}=2a$, and norm $N(q):=q \cdot \overline{q}=a^2+b^2+c^2+d^2$.
1. $q \mapsto \overline{q}$ is $\mathbb{R}$ linear, $\overline{\overline{q}}=q$.
2. $\overline{q_1q_2}=\overline{q_2} \cdot \overline{q_1}$.
3. $Tr:\mathbb{H} \rightarrow \mathbb{R}$ is $\mathbb{R}$-linear.
4. $N(1)=1;N(q) \in \mathbb{R}$, $N(q_1q_2)=N(q_1)N(q_2)$ since $N(q_1q_2)=q_1q_2\overline{q_1q_2}=q_1q_2\overline{q_2}\overline{q_1}=q_1\overline{q_1}q_2\overline{q_2}=N(q_1)N(q_2)$.

**Theorem**:
$\mathbb{H}$ is a division ring. In fact $q^{-1}=N(q)^{-1}\overline{q}$

*Proof*:
Let $q=a+bi+cj+dk$, then $N(q)=a^2+b^2+c^2+d^2$, $\overline{q}=a-bi-cj-dk$, then $q \cdot N(q)^{-1}\overline{q}=N(q)^{-1}q\overline{q}=N(q)^{-1}N(q)=1$, the other side is similiar.
**Remark**: Forbenius proved that: if $D$ a division $\mathbb{R}$-algebra, and $dim_\mathbb{R}D < \infty$, then $D \simeq \mathbb{R},\mathbb{C},\mathbb{H}$ as $\mathbb{R}$-algebra.

There is a embedding of rings:
$\Phi:\mathbb{H} \hookrightarrow M_{2 \times 2} (\mathbb{C})$ sending $z+jw \mapsto \begin{pmatrix}z&-\overline{w}\\ w&\overline{z}\end{pmatrix}$ where $z,w \in \mathbb{C}$. $\Phi(1)=id$ is clear, and using $jw=\overline{w}j$, one get $\Phi(p_1p_2)=\Phi(p_1)\Phi(p_2)$. Clearly $Tr$ of $\mathbb{H}$ $\leftrightarrow$ $Tr$ of $M_{2 \times 2}(\mathbb{C})$, and $N$ of $\mathbb{H}$ $\leftrightarrow$ $det$ of $M_{2 \times 2}(\mathbb{C})$.

# Quaternions vs. rotations in $\mathbb{R}^3$
$\mathbb{R}^3 \simeq \mathbb{H}_0:=\{q \in \mathbb{H}:\overline{q}=-q\}=\{q \in \mathbb{H}:Tr(q)=0\}=\{ai+bj+ck:a,b,c \in \mathbb{R}\}$ by sending $(a,b,c) \leftrightarrow ai+bj+ck=q$. If we transport this standard IP on $\mathbb{R}^3$, then $\Vert q \Vert^2=N(q)$.

*Lemma*:
1. $N(xqx^{-1})=N(q),\forall q \in \mathbb{H}$.
2. We have an orthogonal transformation $R_x:q \mapsto xqx^{-1}$ on $\mathbb{H}_0$.
3. $detR_x=1$.

*Proof*:
We proof the third one. Identify $\mathbb{H}$ with $\mathbb{R}^4$, then $\mathbb{H}_0$ corresponds to $\mathbb{R}^3$, so $R_x$ is identified with a $3 \times 3$ orthogonal matrix, hence $detR_x=\pm1$, and $R_x$ extries are continuous functions in $x \in \mathbb{H}^\times \simeq \mathbb{R}^4-\{0\}$. So $\mathbb{R}^4-\{0\} \rightarrow \{\pm 1\}$ is continuous, and $detR_1=1$, so we are done.

Thus we have $R_xR_y=R_{xy},R_1=id,R_{x^{-1}}=R_{x}^{-1},R_{tx}=R_x$. Now we ask that whether these $R_x$ are all rotations in $\mathbb{R}^3$ ?

**Theorem**:
Let $T$ be a rotation in $\mathbb{H}_0$, then $\exists x \in \mathbb{H},N(x)=1$ s.t. $T=R_x$.

*Proof*:
Existence: Identify $\mathbb{H}_0$ with $\mathbb{R}^3$. Using Euler angle, $\exists \phi,\theta,\psi \in \mathbb{R}$ with $T=R_{e_1}(\psi)R_{e_2}(\theta)R_{e_3}(\phi)$, so we reduce to the case of $T=R_{e_l}(\psi)$.
- l=1: Take $x=\cos \theta + \sin \theta \cdot i \in \mathbb{H}^{\times}$ with $N(x)=1$. Then $x^{-1}=\cos\theta-\sin\theta \cdot i$. Then $xix^{-1}=i,\ xjx^{-1}=\cos2\theta \cdot j+\sin2\theta \cdot k,\ xkx^{-1}=-\sin2\theta \cdot j+\cos2\theta \cdot k$, whence $R_x$ is in the form of $\begin{pmatrix}1&\\&R(2\theta)\end{pmatrix}$. The other two is similiar.
Uniqueness: $R_x=R_y$, then $R_{xy^{-1}}=R_xR_y^{-1}=id$, so we only need to proof that if $R_x=id,N(x)=1$, then $x=\pm 1$. In fact, $R_x=id$ $\Rightarrow$ $xqx^{-1}=q$ for all $q \in \mathbb{H}_0$, hence $xqx^{-1}=q$ for all $q \in \mathbb{H}$, so $x \in Z(\mathbb{H})$, thus $x=\pm 1$. 

**Corollary**:
Let $u \in \mathbb{H}_0$, $N(u)=1$, and $\theta \in \mathbb{R}$, then $R_u(\theta)$ a rotation around $u$ with degree $\theta$, is equal to $R_x$, where $x=\cos\frac{\theta}{2}+\sin\frac{\theta}{2}u$.

*Proof*:
One can check that $\overline{u}=-u$, then $N(x)=\cos^2\frac{\theta}{2}-\sin^2\frac{\theta}{2}u^2$, and note $1=u\overline{u}=-u^2$, hance $N(x)=1$. If $u=i$, then we know that $R_u(\theta)=R_x$. In general, there is a rotation $P$ in $\mathbb{H}_0 \simeq \mathbb{R}^3$, such that $P(i)=u$, know: $R_u(\theta)=PR_i(\theta)P^{-1}=R_yR_i(\theta)R_{y^{-1}}=R_x$, whence $x=y(\cos\frac{\theta}{2}+\sin\frac{\theta}{2}i)y^{-1}=\cos\frac{\theta}{2}+\sin\frac{\theta}{2}u$.
*Remark*:
1. there is a 2 to 1 mapping $\{1 \in \mathbb{H}^\times,\, N(x)=1\} \twoheadrightarrow \{\text{rotation in } \mathbb{H}_0 \simeq \mathbb{R}^3\}$.
2. $R_u(\theta)=R_x$ (let $\psi:=\frac{\theta}{2}$), then $x=e^{\psi u}=\sum_{n=0}^{\infty}\frac{\psi^nu^n}{n!}=\cos\psi+\sin\psi u$, which is to say $e^{i\psi}=\cos\psi+\sin\psi i$.

# 对称多项式
**Definition**:
1. Ring: is a set $R$ with commutative "+" and a multiplication "$\cdot$" with "1".
2. Division ring: A ring $\neq \{0\}$ such that $R^{\times}=R-\{0\}$.
3. field: A commutative division ring.

Now fix a field $F$, and $n \in \mathbb{Z}_{\geq 1}$. $S_n$ is the symmetric group. $\forall f \in F[x_1, \cdots,x_n], \forall \sigma \in S_n$, set $(\sigma f):=f(x_{\sigma(1)},\cdots,x_{\sigma(n)}) \in F[x_1,\cdots,x_n]$. Then $idF=F,(\sigma\tau) f=\sigma(\tau f)$.

**Definition**:
If $f \in F[x_1,\cdots,x_n]$ satisfies $\forall \sigma \in S_n$, $\sigma f=f$. We say that $f$ is a symmetric polynomial (in n variables)/$F$. $F[x_1, \cdots, x_n]^{S_n}:=\{symmetric \ f\}$. 
It is a subring of $F[x_1,\cdots,x_n]$.
elementary symmetric polynomials: $e_k:=\sum\limits_{1 \leq i_1 < \cdots < i_k \leq n}x_{i_1} \cdots x_{i_n},\forall 1 \leq k \leq n$. $e_1=\sum_i x_i$, $e_n=\prod_ix_i$, set $e_0=1$. then $(y+x_1) \cdots (y+x_n)=\sum_ie_iy^i$. 

**Theorem**(对称多项式基本定理--存在性):
$\forall f\in F[x_1,\cdots,x_n]^{S_n}, \exists g \in F[x_1,\cdots,x_n]$ s.t. $f=g(e_1,\cdots,e_n)$.

*Proof*:
For all $f \in F[x_1,\cdots,x_n]$, write $f=\sum_df_d$ where $f_d:=\sum\limits_{i_1+\cdots+i_n=d}x_1^{i_1}\cdots x_n^{i_n}$ are d-homogeneous part of $f$. If $f=\sum\limits_{i_1,\cdots,i_n\geq 0}C_{i_1,\cdots,i_n}x_1^{i_1}\cdots x_n^{i_n}$, when $f=f_d$, we say $f$ is homogeneous of set $degf:=\begin{cases}\max\{d \geq 0:f_d \neq 0\} &\text{ if }f \neq 0\\-\infty &\text{ if } f=0\end{cases}$. 
*Lemma*: Let $f \in F[x_1,\cdots,x_n]^{S_n}$. Then $f(x_1,\cdots,x_{n-1},0)=0 \Leftrightarrow e_n|f$. (easy)
Let $f \in F[x_1,\cdots,x_n]^{S_n}$, $\forall d \geq 0$, $f_d$ is symmetric, so we may assume $f=f_d$, for some $d$. $\forall g \in F[x_1,\cdots,x_n]$, define its weight $wt(g):=\begin{cases}\max{\sum_{k=1}^{n}ki_k:C_{i_1,\cdots,i_n} \neq 0},& g \neq 0\\-\infty &g=0\end{cases}$. To show: If $f=f_d$, then $\exists g$ s.t. $wt(g) \leq d$, and $f=g(e_1,\cdots,e_n)$. Induction on $n+d$. If $d=0$, then $f \in F$, and we can take $g=f$, and $wt(g) \leq 0$. Assume $d \geq 1$, $\forall h \in F[x_1, \cdots,x_n]$, set $h^{\mathfrak{b}}:=h(x_1,\cdots,x_{n-1},0)\in F[x_1,\cdots,x_n]$, $n=1 \Rightarrow$ element of $F$. $h^{\mathfrak{b}}$ is symmetric in $n-1$ variables, $f^\mathfrak{b}$ still homogeneous of degree $d$ that is symmetric. Using induction, there is a $g_1 \in F[x_1, \cdots,x_{n-1}]$ s.t. $f^\mathfrak{b}=g_1(e_1^{\mathfrak{b}},\cdots,e_n^{\mathfrak{b}})$, and $degg_1(e_1^{\mathfrak{b}},\cdots,e_n^{\mathfrak{b}}) \leq wt(g_1) \leq d$. Hence $f_1=f-g_1(e_1,\cdots,e_{n-1})$ has degree $\leq d$, is symmetric and $f_1^{\mathfrak{b}}=f^{\mathfrak{b}}-g_1(e_1^{\mathfrak{b}},\cdots,e_{n-1}^{\mathfrak{b}})=0$. using the lemma, one get $e_n|f_1$, let $f_2:=\frac{f_1}{e_n}$ is symmetric, and $degf_2 \leq d-n$. Using induction, then the theorem is proved.
(it is easier to understand if one just pick the elements in $f$ where $x_1$ has the highest degree, then extend them to symmetric, using induction).

**Theorem**(对称多项式基本定理--唯一性):
If $g_1(e_1,\cdots,e_n)=g_2(e_1,\cdots,e_n)$, then $g_1=g_2$.

*Proof*:
We only need to show $g \in F[x_1,\cdots,x_n]$, if $g(e_1,\cdots,e_n)=0$, then $g=0$.
1. May enlarge the field $F$. May assume $F$ is infinite (sending finite feld $F \hookrightarrow F(t)$).
2. $F$ infinite, $g \neq 0$, then there is a $(y_1, \cdots,y_n) \in F^{n}$ s.t. $g(y_1, \cdots,y_n)$.
3. Consider $p:=x^n-y_1x^{n-1}+ \cdots+(-1)^{n}y_n$, then there is a extension fields $F \hookrightarrow L$ s.t. $p$ split in $L[x]:p=\prod_i(x-x_i)$, hence $e_k(x_1, \cdots, x_n)=y_k$, so $g(e_1, \cdots,e_n) \neq 0$.

*Facts*: $F$ infinite field, $g \in F[x_1, \cdots,x_n],g \neq 0$ then there is a $(y_1, \cdots,y_n) \in F^n$, $g(y_1,\cdots,y_n) \neq 0$. Using induction, $n=1$ clear, if $n>1$, take $(g_1,\cdots,g_{n-1})$, such that $g_k(y_1,\cdots,y_k) \neq 0$, then see $g$ as a polynomial of $x_n$ .
*Remark*: If $F$ is a subfield of $\mathbb{C}$, then we may work as $\mathbb{C}$. An the theorem still holds if $F$ is an integal domain (R:integral $\Rightarrow$ $R \hookrightarrow F$, where $F$ is its field of fraction.)

**Example**:
- discriminant/判别式: $f=x^n-c_{1}x^{n-1} + \cdots+(-1)^nc_{n}=\prod_i(x-\alpha_i)$. Define $disc(f):=\prod_{i<j}(\alpha_i-\alpha_j)^2$ If we view $\alpha_1,\cdots,\alpha_n$ as variables, then $disc(f)$ is a symmetric polynomial in $\alpha_1, \cdots,\alpha_n$, so $disc(f)$ is a polynomial in $e_i(\alpha_1, \cdots,\alpha_n)=c_i$ and is unique.
- $disc(x^2-bx+c)=(\alpha_1+\alpha_2)^2-4\alpha_1\alpha_2=b^2-4c$.
- $disc(x^3+px+q)=((\alpha_1-\alpha_2)(\alpha_2-\alpha_3)(\alpha_3-\alpha_1))^2=-4p^3-27q^2$.
- Using PARI ant type *poldisc(X^3+aX^2+bX+c)* one can get the disc of the polynomial.

# Resultant/结式
**Motivation**:
$F$ a field, $f,g \in F[x]$ Determine whether $f,g$ are coprime. It is ok to use euclidean algorithm. But we also want an "equational" criterion.

**Definition**:
Fix $n,m \in \mathbb{Z}_{\geq 1}$, consider $f=v_0x^n+ \cdots+v_n$, $g=w_0x^m+\cdots+w_m$, then the resultant
$$
Res(f,g):=\begin{vmatrix}v_0&\cdots&\cdots&\cdots&v_n\\&v_0&\cdots&\cdots&\cdots&v_n\\&&\ddots&&&&\ddots\\&&&v_0&\cdots&\cdots&\cdots&v_n\\
w_0&\cdots&\cdots&\cdots&w_m\\&w_0&\cdots&\cdots&\cdots&w_m\\&&\ddots&&&&\ddots\\&&&w_0&\cdots&\cdots&\cdots&w_m\end{vmatrix}
$$
*Property*:
- View $v_i,w_j$ as variables, then $Res(f,g)$ is a polynomial in $v_0, \cdots,w_m$, independent of $F$.
- The coefficient of $v_0^mw_m^n$ is 1.
- $Res(f,g)=(-1)^{mn}Res(g,f)$.
- $\forall\, t \in F$, $Res(tf,g)=t^mRes(f,g)$ and $Res(f,tg)=t^nRes(f,g)$.

**Lemma**:
Given $n,m$ and $f,g$ then $Res(f,g)=0 \Longleftrightarrow$ $\exists\,f_1,g_1 \in F[x]-\{0\}$ such that $degf_1<n,\,degg_1<m,\ fg_1+gf_1=0$.

**Theorem**:
Given $n,m$ and $f,g$ as before. $Res(f,g)=0 \Longleftrightarrow$ wither $v_0=w_0=0$ or there is $h \in F[x],degh>0$ such that $h|f,h|g$. 

*Proof*:
($\Longleftarrow$) If $v_0=0=w_0$, then $Res(f,g)=0$. If there is $h|f,h|g$, then $f \cdot \frac{g}{h}-g \cdot \frac{f}{h}=0$.
($\Longrightarrow$) Assume $Res(f,g)=0$.
- Case 1. One of $f,g$ are 0. Suppose $f=0$, $degg>0$, then we take $h=g$ then one get $w_0=0$.
- Case 2. $f,g$ are nonzero. May assume $(v_0,w_0) \neq (0,0)$, then there is $f_1,g_1 \neq 0$, such that $f_1g+fg_1=0$. In $F(x):=Frac(F[x])$, $\frac{f}{g}=\frac{-f_1}{g_1}$. If $f$ is coprime to $g$, then we would get $g|g_1$, contradiction.

**Theorem**:
Fix $n,m \in \mathbb{Z}_{\geq 1}$. $f=a\prod_i(x-\alpha_i),\,g=b\prod_j(x-\beta_j)$, then $Res(f,g)=a^m\prod_ig(\alpha_i)=(-1)^{nm}b^n\prod_jf(\beta_j)=\alpha^m\beta^n\prod_{i,j}(\alpha_i-\beta_j)$.

*Proof*:
We only need to show $Res(f,g)=a^m\prod_ig(\alpha_i)$. 
1. Special case: $g(\alpha_1),\cdots,g(\alpha_n)$ are distinct, consider $Res(f,g-y) \in F[y]$ has degree $n$, note that $f$ and $g-g(\alpha_i)$ has a common root $\alpha_i$, then $\prod_i(g(\alpha_i)-y)|Res(f,g-y)$. Both side have $deg_y=n$, and leaing coefficient, so it muse be euqal.
2. General case "Perturbation". (the theorem is true for almost every $f,g$, so we know it must be true). Keep $g$, assume $b \neq 0$, and take $f=\prod_i(x-z_i)$, in the "special case" $Res(f,g)=\prod_ig(z_i)$. Since $g(z_1),\cdots,g(z_n)$ are distinct in $F[z_1,\cdots,z_n]$, let $z_i \rightarrow \alpha_i$ then we are done.

Back to discriminant.
Fiven $f=a \prod_i(x-\alpha)$ in $F[x]$, set $disc(f):=a^{2n-2}\prod_{i<j}(\alpha_i-\alpha_j)^2$, then $a \cdot disc(f)=(-1)^{\frac{n(n-1)}2}Res(f,f')$. 

**Newton's formula**
$\forall k \geq 0$, fix $x \in \mathbb{Z}_{\geq 1}$ and $p_k:=\sum_{i=1}^nx_i^k$, $e_1,\cdots,e_n$ are elementary symmetric polynomials, $e_0:=1$. Then
1. $1 \leq k \leq n$ then $e_0p_k-e_1p_{k-1}+ \cdots+(-1)^kke_k=0$.
2. $k \geq n$, then $p_k-e_1p_{k-1}+ \cdots+(-1)^ne_np_{k-n}=0$.
Using these, one can:
- express $p_k$ in terms of $e_1,\cdots,e_n$, with coefficients$/\mathbb{Z}$.
- express $e_k$ in terms of $p_1,\cdots,p_n$, with coefficients$/\mathbb{Q}$.

*Proof*:
Consider the formal power series in $Y:P(y):=\sum_{k \geq 1}y^{k-1}=\sum_{k \geq 1}\sum_{i=1}^nx_i^ky^{k-1}=\sum_{i=1}^n\frac{x_i}{1-x_iy_i}$ and $E(y)=\sum_{k=0}^{n}e_ky^k=\prod_{i=1}^n(1+x_iy)$, then $P(-y)=\sum_{i=1}^n\frac{x_i}{1+x_iy}=\frac{E'(y)}{E_y}$. So we have $E(y)P(-y)=E'(Y)=\sum_{k=1}^nke_ky^k$. Compute each coefficients, one proof the theorem.

# Irreducible polynomials
Recall: $R$ is an integral domain, and $x,y \in R$. If $\exists u \in R$, $xu=y$ we write x~y. Let $x \in R-R^\times$, if $x=ab$, then a~1 or b~1, we say $x$ is irreducible in $R$. 

Now let $F$ be a field. $R=F[x]$, $R^\times=F^\times$ $f \in F[x]-F$ is irreducible means: $f=g_1g_2 \Rightarrow g_1 \in F^\times || g_2 \in F^\times$. FOr $\mathbb{Z}$: more complicated. Example: $2x \in \mathbb{Z}[x]$ reducible yet all its divisor are of deg=0. Irreducible in $\mathbb{Q}[x]$ must cope with $\mathbb{Z}[x]$.

**Definition**:
Let $f=a_0+ \cdots+a_nx^n$, and $c(f):=gcd(a_0,\cdots,a_n)$, if $c(f)=1$, we say that $f$ is primitive. 

**Lemma**:
Let $g,h \in \mathbb{Z}[x]$ be both primitive, then so in $gh$.

*Proof*:
$\forall p$ prime. Write $g=a_0+\cdots+a_rx^r+\cdots$, where $r$ is biggest $p \nmid a_r$, and similiarly $h=b_0+\cdots+b_sx^s+\cdots$, then the coefficient of $x^{r+s}$ is not divided by $p$, hence $gh$ is primitive. 
*Remark*: This is just $\mathbb{F}_p[x]$ is an integral domain.

**Theorem**:
Let $f \in \mathbb{Z}[x]-\{0\}$ be primitive.
1. If $f=gh$ in $\mathbb{Q}[x]$, then there is an $\alpha \in \mathbb{Q}$ such that $g_1:=\alpha g,h_1=\alpha^{-1}h$ are both in $\mathbb{Z}[x]$ and primitive.
2. When $degf >0$, $f$ is irreducible in $\mathbb{Q}[x]$ $\Leftrightarrow$ there is no $g,h \in \mathbb{Z}[x]$ such that $degg,degh>0$ and $f=gh$.

*Proof*:
in (1), $degf=0 \Rightarrow$ take $\alpha:=g^{-1}$. Assume $degf>0,f=gh$ in $\mathbb{Q}[x]$. Take $u,v \in \mathbb{Z}_{\geq 1}$ s.t. $ug,vh \in \mathbb{Z}[x]$. Then $uv=c(uvf)=c(ugvh)=c(ug)c(vh)$, hence $f=\frac{ug}{c(ug)}\ \frac{vh}{c(vh)}$, so one may take $\alpha=\frac{u}{c(uv)}$. 
For (2), clear.

**Recall**:an integral domain is $UFD$ if $\forall r \in R-\{0\}$ has a decomposition $r=up_1\cdots p_m$ where $p_i$ are irreducible emelents in $R$ and $u$ a unit.

**Theorem**:
$\mathbb{Z}[x]$ is $UFD$ whose irreducibles are $\begin{cases}1. \text{irrducibles in } \mathbb{Z}\\2. \text{ primitive } f \in \mathbb{Z}[x] \text{satisfying the second condition in the above theorem}\end{cases}$ 

Now we want to show that $\mathbb{Z}[x]$ is a $UFD$, in fact $\mathbb{Z}[x]$ is a $ED$, which immediately lead to what we want.

**Eisenstein criterion**
Let $n \geq 1$, $f=a_0 + \cdots+a_nx^n \in \mathbb{Z}[x]$. If $\exists$ prime $p$, s.t. $p \nmid a_n$, $p|a_0,\cdots,a_{n-1}$ and $p^2 \nmid a_0$, then $f$ is irreducible in $\mathbb{Q}[x]$.

*Proof*:
$p \nmid a_n$ $\Rightarrow$ $p \nmid c(f)$, hence the same conditions hold for $f/c(f) \in \mathbb{Z}[x]$. So we may assume $f$ is primitive. If $f$ is reducible in $\mathbb{Q}[x]$, then we know $f=gh$, where $g=b_0+\cdots+b_mx^m$ and $h=c_0+\cdots+c_lx^l$, with $l,m>0$, then $a_n=b_mc_l$, $a_0=b_0c_0$, so $p \nmid b_m,c_l$, and we may assume $p|b_0$. Suppose $p|b_0,\cdots,b_{k-1}$, and $p \nmid b_k$. Using $a_k \equiv 0 \pmod{p}$, one know that $b_kc_0 \equiv 0 \pmod{p}$, hence $p|c_0$ $\Rightarrow$ $p^2|a_0$, contradiction.

**Remark**:
- It is an typical exercise to proof $\Phi_p$ is irreducible using Eisenstein criterion. General definition of $\Phi_n$ is product of $(x-\zeta)$ where $\zeta$ runs over all primitive n-th root of unity. 
- The general theory works if $\mathbb{Z} \rightarrow R:UFD$ and $\mathbb{Q} \rightarrow K:=Fra(R)$. One can define $c(f)$ over $R$, then one have all the theorem above.
- In particular $R:UFD$ $\Rightarrow$ $R[x]:UFD$. Moreover, $f \in R[x]$ is irreducible then eigher $f$ is irreducible in $R$, or $degf>0$ and $f$ irreducible in $K[x]$.
- $R:UFD$ $\Rightarrow$ $\forall n \geq 1,\ R[x_1,\cdots,x_n]$ is UFD (Using induction on n).
- $R:UFD$, $f=a_nx^n+\cdots+_0$, $f(\frac{u}{v})$, $\frac{u}{v} \in K$, then $v|a_n$ and $u|a_0$.
- Given $f \in \mathbb{Z}[x]-\mathbb{Z}$: primitive then there is a algorithm to test irreducibility. Choose $x_1,\cdots,x_n \in \mathbb{Z}$ distinct and $f(x_i) \neq 0$, then one have $g(x_i)|f(x_i)$, so there is only finitly many choice of $g(x_i)$, then one check whether $g$ generated by $(g(x_i))_i$ have $g|f$. 

---
# Groups
**motivation**:"Symmetries" in mathmatics.
These are certain bijection on sets+structures. 
Common featrues: "identtity" Multiplication/Composition.
$\exists$ other math objects sharing these featrues!

**Definition**:
Group:=$data(G,\cdot)$, where $G$ is a set $\neq \varnothing$ and $\cdot:G \times G \rightarrow G$ such that
- $xyz=x(yz)$ $\forall x,y,z \in G$.
- $\exists 1_G \in G$ s.t. $1_gx=x1_g=x$ $\forall x \in G$.
- $\forall x \in G$ $\exists x^{-1} \in G$ s.t. $xx^{-1}=x^{-1}x=1_G$.
We say $G$ is commutative/abelian if $xy=yx$ for all $x,y \in G$. And $G$ is trivial if $G=\{1_G\}$. The order of $G$:=$|G|$.

**Variants**:
If we remove the axiom of the existence of $x^{-1}$, then we get "monoid"(幺半群)
If we remove the third axiom as well, then we get "semigroup"(半群)
One can define $x^n$ on group $G$.

**Definition**:
$G$:group, $H$ a subset of $G$, if:
1. $1_G \in H$.
2. $x,y \in H$ $\Rightarrow$ $xy \in H$.
3. $x \in H$ $\Rightarrow$ $x^{-1} \in H$.
we say that $H$ is a subgroup of $G, in which case $(H,\cdot)$ is a group.
Boring examples: $\{1_G\}$ and $G$ are subgroup of $G$.
$\bigcap$ of subgroups are a subgroup.
another example: $G$ a group, let $Z(G):=\{a:ax=xa,\forall x \in G\}$, be the center of the group $G$. one can check that it id indeed a subgroup. If $G$ is abelian, then $Z(G)=G$.

**Example**:
- Permutation group $S_X$, which contains all one to one map $X \rightarrow X$, in particular, $S_n:=S_{\{1,\cdots,n\}}$. 
- Alternating group $A_n$, which is a subgroup of $S_n$ with $\sigma \in S_n$ such that $sign(\sigma)=1$.
- General linear group $GL(V)$, where $V$ is a vector space, is all invertable linear transformation $V \rightarrow V$.
- Special linear group $SL(V):=\{T \in End(V):det(T)=1\}$. It is necessary that $dimV<\infty$.
- Orthogonal group $SO(V)$. Let $dimV<\infty$ be an $IPS/\mathbb{R}$ then $O(V)$ contains invertable linear transformation that preserve $IPS/\mathbb{R}$, and $SO(V):=O(V) \cap SL(V)$.
- Unitary group $SU(V)$. Similiar to $SO(V)$ but over $\mathbb{C}$.
- $GL,SL,SO,SU$ all have matrix version.
- $(\mathbb{Z},+)$ is also a group.
- $R$ a ring, then $R^{\times}:=\{r \in R:r \text{ invertable}\}$ forms a group (actually, in algebra, on almost always assume $R^\times$ has a unit, which is not true in general).

**Notion**:
Let $G$ be a group $S \subseteq G$ be a set, then set $\langle S \rangle:=\{s_1^{a_1}\cdots s_n^{a_n}:s_i \in S,\ a_i \in \mathbb{Z}\} \subseteq G$ (i.e. every string consisting of elements in $S$) is the subgroup of $G$ generated by $S$. In particular, if $\langle S \rangle=G$, we say that $S$ generated $G$.

**Example**:
- $S_n$ is generated by $(i,i+1)$ 
- $\mathbb{Z}/n\mathbb{Z}$ ios generated by $\bar{1}$.

**Definition**:
Let $(G_i)_{i \in I}$ be a family of group. Endow $\prod_{i \in I}G_i$ with a group structure:$(g_i)_{i \in I} \cdot (g'_i)_{i \in I}=(g_ig'_i)_{i \in I}$. Clearly $(1_i)_{i \in I}$ is the unit and $(g_i^{-1})_{i \in I}=(g_i)_{i \in I}^{-1}$. One can also check that $G_1 \times G_2 \times G_3 \simeq G_1 \times (G_2 \times G_3)$.

# Homomorphism and Isomorphism
**Definition**:
$G,G'$ are groups, then map $f:G \rightarrow G'$ that preserves product $f(x)f(y)=f(xy)$ is called *homomorphism*.
It is clear that if $f$ is a homomorphism, then $f(1_G)=1_{G'}$ and $f(x^{-1})=f(x)^{-1}$.
*Remark*:This also works for semigroup and monoids.

**Example**:
- Let $H \leq G$ be subgroup, then the inclusion map $H \hookrightarrow G$ is a homomorphism.
- $sign:S_n \rightarrow \{\pm 1\}$ is a homomorphism.
- $det:GL(n,F) \rightarrow F^{\times}$ is a homomorphism.
- $P_j:\prod_{i \in I}G_i \rightarrow G_i$ sending $(g_i)_{i \in I} \mapsto g_j$is a homomorphism.
- $f:G \rightarrow G',g:G' \rightarrow G''$ are both homomorphism, then $gf:G \rightarrow G''$ is a group homomorphism.

**Definition**:
Let $G,G'$ be two groups, then $f:G \rightarrow G'$ is *isomorphism* if there is a $g:G' \rightarrow G$ (homomorphism) such that $gf=id_G$ and $fg=id_{G'}$. If there is an isomorphism $G \rightarrow G'$, we say that $G$ and $G'$ are isomorphic.

**Proposition**:
Let $f:G \rightarrow G'$ be a bijective homomorphism, then $f$ is an isomorphism

**Example**:
- $G$ a group, $g \in G$, then $Ad_g:G \rightarrow G$ sending $x \mapsto gxg^{-1}$ is an isomorphism, with $Ad_gAd_h=Ad_{gh}$.
- $Aut(G):=$ all automorphisms is a group. 

# Cyclic group
**Definition**:
A group $G$ is *cyclic* if and only if there is a generator $\langle \sigma \rangle=G$.

**Example**:
- $\mathbb{Z}$ is obviously a cyclic group.
- $\mathbb{Z}/n\mathbb{Z}$ is cyclic
In fact, these are all cyclic groups.

# Cosets in a group
**Definition**:
Let $G$ be a group and $H \leq G$, then we define the equvalience relation between elements in $G$: $x$ ~ $y$ if there is a $h \in H$ with $x=yh$. Then we can have quotient f the equvalient classes $G/H$ and $H \backslash G$. 

**Definition**:
Let $(G:H)$ be a common cardirality(基数) of $G/H$. Some time denoted also by $[G:H]$.

**Theorem**:(Langrange)
$|G|=|H|(G:H)$

*Proof*:
For all $C$ a coset, pick a $x_C \in C$, then $G/H \times H \rightarrow G$ sending $(C,h) \mapsto x_Ch$, then it is obviously injective and surjective.
**Corollary**:
- If $G$ is finite, then $|H|\,|\, |G|$.
- If $|H|$ and $|K|$ are coprime, then $H \cap K=\{1\}$.
- Let $g \in G$, then $ord(g)\,|\,|G|$.

# Group action
**Definition**:
a Group action is a homomorphism $\phi:G \rightarrow End(X)$, where $X$ is a set denoted by $\phi(g)(x)=gx$. Moreover, $G \simeq G^{op}$ by $g \mapsto g^{-1}$, so a $G$-rightaction on $X$= a $G^{op}$-action on $X$.
It is clear that similiar definition works on semigroup.

**Definition**:
Let $G$ act on $X$, then the $G$-orbit of $x \in X$ $Gx=:\{gx:g \in G\}$. And the stabilizer of $x$ is $Stab_G(x):=\{g \in G:gx=x\}$.
In fact, it forms an equvalience relation on $X$ by $x$ ~ $y$ if $Gx=Gy$.
One can decompose $X$ into orbit.

**Example**:
- $So(3)$ act on $\mathbb{R}^3-\{0\}$ naturally, and for $\vec{v} \in \mathbb{R}^3-\{0\}$, its orbit is all $\vec{w}$ with $\Vert \vec{w} \Vert=\Vert \vec v \Vert$, and its stabilizer $Stab(\vec{v}):=\{R_{\vec{v}}(\theta):\theta \in \mathbb{R}/2\pi\mathbb{Z}\}$.
- Let $H \leq G$, then orbit of $H$ acting on $G$ is $Hx$ and stabilizer is $\{1\}$.

**Definition**:
We say that $G$ acting on $X$ is 
- *faithful* if $\bigcap_{x \in X} Stab(x)=\{1\}$.
- *transitive* if $\forall x,y \in X$, there is a $g \in G$, $gx=y$.
- *free* if $Stab(x)=\{1\}$ for all $x \in X$.
and $X^G:=\{x \in X:\forall g \in G,gx=x\}$.

**Structure of orbits**
Let $G$ act on $X$, then $Gx$ is an orbit, and $G \twoheadrightarrow Gx$ by $g \mapsto gx$, take $H=Stab(x)$, then there is a one to one map $G/H \rightarrow Gx$.
Then we have *Orbit decomposition*: $X=\bigsqcup_{Gx}Gx$. So $|X|=\sum_{orbits}|Gx|=\sum_{orbits}(G:Stab(x))$.

**Theorem**:(Cayley)
Every group $G$ can be embedded into $S_G$.

# Case study:permutations and cycles
$a_1,\cdots,a_m \in X$ distinct say indexed by $\mathbb{Z}/m\mathbb{Z}$. Permutation $\sigma \in S_X$ of the form $\sigma(a_i)=a_{i+1}$ and $\sigma(x)=x$ are called $m$-cycles written by $\sigma=(a_1a_2\cdots a_m)$.

one immediately notice that $ord(a_1\cdots a_m)=m$ in $S_X$ and $\sigma=(a_1\cdots a_m),\,\tau=(b_1\cdots b_n)$ commutes if and only if they are disjoint.

**Proposition**:
Every $\sigma \in S_n$ decompose into pairwise disjoint cycles unique up to permutations. 

*Proof*:
take take $X=\{1,\cdots,n\}$ then $S_X=S_n$, and $\langle \sigma \rangle$ acting on $X$ decompose it into $\bigsqcup_iC_i$ and one immediately check that $\sigma$ restric to a $C_i$ is just the same as $(a_1\cdots a_m)$, then we are done.

Let $|C_i|=l_i$, then it is clear that $ord(\sigma)=lcm(l_1,\cdots,l_m)$, and $sgn(\sigma)=(-1)^{\sum_{i}l_i-1}$.

# application of orbit decomposition
**Idea**:Counting
**Definition**:
$G$ a finite group, and $p$ a prime number. If $|G|=p^n,n \in \mathbb{Z}_{\geq 0}$, then we say $G$ is a p-group.

**Proposition**:
$G$ a p-group, and $G$ act on $X$ a finite set, then $|X^G| \equiv |X| \pmod{p}$.

*Proof*:
$X=Gx_1 \sqcup \cdots \sqcup Gx_m$ and $H_i:=Stab(x_i)$, then $|X|=\sum_i(G:H_i)=\sum_{H_i=G}1+\sum_{H_i<G}(G:H_i)=|X^G|+\sum_{H_i<G}(G:H_i) \equiv |X^G| \pmod{p}$.

**Proposition**:
Let $G$ be a p-group, and $G \neq \{1\}$ then $Z_G \neq \{1\}$.

*Proof*:
$a:G \times G \rightarrow G$, define by action $(g,x) \mapsto gxg^{-1}$. Then $x \in G$ is a fixed point if and only if $x \in Z_G$. So $|Z_G| \equiv |G| \equiv 0 \pmod{p}$, and note that $1 \in Z_G$, so $|Z_G|>0$.

# Normal subgroup and quotient group
**Definition**:
A subgroup $H$ is *normal* if $\forall g \in G$, $gHg^{-1}=H$. Equvaliently $gH=Hg$ and $gHg^{-1} \subseteq H$. Denoted by $H \triangleleft G$.

**Example**:
- If $G$ is abelian, then for all $H \leq G$, $H \triangleleft G$. 
- $\{1\},G \triangleleft G$.
- $Z_G \triangleleft G$.
- If $N \triangleleft G$ and $H \leq G$, then $N \cap H \triangleleft H$.
- If $(G:H)=2$, then $H \triangleleft G$.

*Key observation*: $ker(f) \triangleleft G$.

**Examples**:
- Homomorphism: $sgn:S_n \rightarrow \{ \pm 1\}$, we usually denote the kernel by $A_n:=ker(sgn) \triangleleft S_n$ (the alternating group). In fact, by decomposing $\sigma \in S_n$ into cycles, one immediately know that the conjugacy classes are all elements that have some how the same decomposition into cycles (there is a one to one map from one cycle to the other with the same length). In particular, if $V \triangleleft S_4$, then $V$ must be of the form $\{id,all\ (ab)(cd)\}$.
- $W$: a vector space over field $F$ with $dimW<\infty$. Then the homomorphism $det:GL(W) \rightarrow F^\times$ gives a normal subgroup $SL(W):=ker(det) \triangleleft GL(W)$.

*Observation*:
$N:=ker(f:G \rightarrow G')$, then $\forall x,y \in G$, $f(x)=f(y) \Longleftrightarrow f(xy^{-1})=1_{G'} \Longleftrightarrow xy^{-1} \in N$, which is to say $x \in Ny$.

Now, given $N \triangleleft G$, we want to give $G/N$ a group structure, such that the natural map $q:G \rightarrow G/N$ is a homomorphism. In fact, we only need to map $g \mapsto gN$, one check that $g_1g_2N=g_1Ng_2N$, this is why we need to consider normal subgroup instead of arbitrary subgroups.

**Def-prop**: 
Let $N \triangleleft G$, on $G/N:=\{cosets\ gN:g \in G\}$, one can define a multiplication $xN \cdot yN=xyN$, then $G/N$ forms a group and $G \rightarrow G/N$ is a homomorphism, then we say that $G/N$ is the quotient group(商群) of $G$ by $N$.
*Remark*:
The group structure on $G/N$ is the unique one making $q$ into a homomorphism.

**simpliar extensions**:
- Quotient of vector space: $V/U$ where $U \subset V$ are vector sapces, then the quotient group $V/U$ also forms a vector space over $F$.
- Quotient of ring: $R$ a ring and $I$ an ideal, then $R/I$ also have a ring structure.

**Proposition**(universal property of quotient):
Let $f:G \rightarrow G'$ be a homomorphism and $N \triangleleft G$ such that $N \subseteq ker(q)$, then there is a unique $\bar{f}:G/N \rightarrow G'$ making the following diagram commute:
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
&G \arrow[d,"q"] \arrow[r,"f"] &G'\\
&G/N \arrow[ur,"\bar{f}"]
\end{tikzcd}
\end{document}
```
**Corollary**:
Let $f:G \rightarrow G'$ be a homomorphism, put $N:=ker(f)$, we get $\bar{f}:F/ker(f) \simeq im(f) \subseteq G'$. In particular, $(G:ker(f))=|im(f)|$

**Example**:
- $sgn:S_n \rightarrow \{\pm 1\}$ is surjective (when n>1), and $(S_n:A_n)=2$.
- $N:\mathbb{H}^\times \rightarrow \mathbb{R}^\times_{\geq 0}$ is a homomorphism and $\mathbb{H}^1:=ker(N) \triangleleft \mathbb{H}^\times$, and that $\mathbb{H}^1 \twoheadrightarrow So(3)$ by $q \mapsto qxq^{-1}$  where $x \in \mathbb{R}^3 \simeq \mathbb{H}_0$, is a homomorphism, and $ker(\mathbb{R})=\{\pm1\}$, hence $R$ induces isomorphism $\mathbb{H}^1/\{\pm1\} \simeq So(3)$. Recall that $\mathbb{H} \simeq \{\begin{pmatrix}z&-\bar{w}\\ w&\bar{z}\end{pmatrix}|z,w \in \mathbb{C}\}$ as ring, and the map $z+wj \mapsto (z,w)$ forms $N \leftrightarrow det$, hance $\mathbb{H}^1 \simeq \{\begin{pmatrix}z&-\bar{w}\\ w&\bar{z}\end{pmatrix}:|z|^2+|w|^2=1\}$, and $\{\pm1\} \simeq \{ \pm I_2\}$, so we have $Su(2)/\{\pm I_2\} \simeq \mathbb{H}^1/\{ \pm 1\} \simeq So(3)$. 

**Proposition**:
Let $f:G \rightarrow G'$ be a surjective homomorphism, let $N:=ker(f)$, then $\{H' \leq G'\} \leftrightarrow \{N \leq H \leq G\}$, and the normal ones maps to normal ones, and preserves inclusion.

*Proof*:
In fact, $G' \simeq G/N$, then we use $H' \mapsto H'N$, and the proof is straightforward.

**Supplemnets**:
We say that a group $G$ is *simple* if $G \neq \{1\}$ and $G$ has no nontrivial normal subgroup.
**Example**:
Cyclic group $\mathbb{Z}/n\mathbb{Z}$, one immediately check that it is simple if and only if $\pm n$ is a prime.

**Proposition**:
Let $H \leq G$ and $K \triangleleft G$ then $HK:=\{hk:k \in K,h \in H\} \subseteq G$ is a subgroup and $HK=KH$.

*Proof*:
It is clear that $1 \in HK$, and $hk=hkh^{-1}h \in KH$, so $HK=KH$. Moreover, $(hk)^{-1}=k^{-1}h^{-1} \in KH=HK$, and $(h_1k_1)(h_2k_2)=h_1h_2(h_2^{-1}k_1h_2k_2)$, so $HK$ is closed under multiplication.
**Generalization**:
$\forall$ subgroup $K \subset G$, Define $Z_G(K):=\{g \in G:gkg^{-1}=k\} \subseteq N_G(K):=\{g \in G:gKg^{-1}=K\} \triangleright K$. Then if $H,K \leq G$, such that $H \subseteq N_G(K)$, then $HK=KH$ is a subgroup.

**Proposition**:
$H,K \subseteq G$ be subgroups, $H \subseteq N_G(K)$. Then $H \cap K \triangleleft H$ and $H/H \cap K \rightarrow HK/K$ by sending $h(H \cap K) \mapsto hK$ is an isomorphism.

*Proof*:
Let $x \in H \cap K$, $h \in H$ $hxh{-1} \in H$, $H \subseteq N_G(K) \Rightarrow hxh^{-1} \in K \Rightarrow H \cap K \triangleleft H$. Consider $H \hookrightarrow HK \twoheadrightarrow HK/K$ use $f$ to denote the composition, then $f(h)=hK$, then $f$ is surjective since $hkK=hK=f(h)$, then $ker(f)=H \cap K$ as if $f(h)=K$ then $hK=K$ so $h \in H\cap K$, thus $H/H \cap K \simeq HK/K$.

# Semidirect prouct
Already show $G_1,G_2$ are groups, then $G_1 \times G_2$ are groups. Now we consider a "twist version".
Given $H,N$ groups and $Aut(N)$ be the group of automorphisms $N \rightarrow N$, and a homomorphism $H \rightarrow Aut(N)$. On the set $N \times H$, define the multiplication $(n,h)(n'h')=(n \phi_h(n),hh')$. Then the group will be denoted by $N \rtimes_\phi H$, and $N \rtimes H$ in short.
*Idea*: To find a group $G$ with $N \hookrightarrow G \hookleftarrow H$, $N \triangleleft G$ and all $g \in G$ can be uniquely written in the from $nh$. One can check that the above definition indeed works.

Internal case: Given a group $G$ and subgroup $N,H$ when can we identify $G$ with $N \rtimes H$ for suitable $\phi$ such that $N \rtimes H \simeq G$ ? In fact, If $N \cap H =\{1\}$ and $N \triangleleft G$ then $G=NH$.

**Proposition**:
Consider $Ad:H \rightarrow Aut(N)$ by $Ad_h(n)=hnh^{-1}$. Then $N \rtimes_{Ad} H \simeq G$ by $(n,h) \mapsto nh$. 

*Proof*:
$\Phi$ is an homomorphism: $\Phi((n,h)(n'h'))=\Phi(nAd(n'),hh')=nhn'h'=\Phi((n,h))\Phi((n',h'))$. And it is clearly surjective, and $\Phi((n,h))=1$ if and only if $nh=1$ hence $n=h^{-1} \in N \cap H =\{1\}$.

**Example**:
- $S_n=A_n \rtimes \langle \tau \rangle$ there $\langle \tau \rangle=\{id,\tau\}$. Note that when $n > 2$, $S_n \not\simeq A_n \times \mathbb{Z}/2\mathbb{Z}$.
- diledral groups 二面体群 $O(2):=\{\text{orthogonal transformation on } \mathbb{R}^2\} \triangleright so(2)$, and one have $D_n$ the dihedral group and it is well known that $D_{2n}=\langle \sigma \rangle \rtimes \langle \tau \rangle$. 

# Modules 模
**Ideas**: $F$ a field and an $F$-vector space is an additive group with $\cdot:F \times V \rightarrow V$ s.t. $t(v_1+v_2)=tv_1+tv_2,\, \forall t \in F$ and $(t_1+t_2)v=t_1v+t_2v$ and $(t_1t_2)v=t_1(t_2v)$, $1_Fv=v$. One notice that the definition still works for $F$ as a ring, this leads to the definition of *modules*.

**Definition**:
Let $R$ be a ring 
1. A (left) $R$-module is an additive group $(M,+)$ such that $R \times M \rightarrow M$ satisfying the above conditions. In fact it is just there is a ring homomorphism $R \rightarrow End(M)$.
2. A (right) $R$-module is almost the same but with homomorphism $R \rightarrow End(M)^{op}$.
**Remark**:
Left $R$-module is the same as right $R^{op}$-module (seeing the above definition).

**General properties**:
just the same as vector spaces.

**Examples**:
1. $F$ a field, then a $F$-module is just the same as $F$-vector field.
2. $R$ itself is an $R$ module.
3. Take $R=\mathbb{Z}$, then $\mathbb{Z}$-module is just abelian groups.

**Definition**:
Let $M_1,M_2$ be two $R$-modules, then the map preserving the module structure $f:M_1 \rightarrow M_2$ is said to be a homomorphism. Just like the case of vector space, $Hom(M_1,M_2)$ is an additive group and "0" is the trivial homomorphism $M_1 \rightarrow M_2$ by $m \mapsto 0$.
*Caution:* In general, there is no natural way to give a $R$-module structure for $Hom(M_1,M_2)$. However, if $R$ is commutative, then $Hom(M_1,M_2)$ is naturally an $R$-module.

Homomorphism are closed under composition and is "bi-additive".

**Definition**:
Isomorphism from $M$ to $M'$ means a homomorphism $f:M \rightarrow M'$ such that $\exists g:M' \rightarrow M$ with $fg=id_M,\,gf=id_{M'}$. And we say that $M \simeq M'$ ($M$ is isomorphic to $M'$) if there is an isomorphism $f: M \rightarrow M'$.

**Proposition**:
Let $f:M \rightarrow M'$ be  homomorphism if $f$ is bijective, then $f$ is $\simeq$.

*Proof*: Same as groups.

**Definition**:
Submodule $N \subseteq M$ is a submodule if $N \leq M$ as a group and have $R \rightarrow End(N)$ restriced from $R \rightarrow End(M)$.

**Examples**:
- $R$ a field then it is a vector subspace. If $R=\mathbb{Z}$, then it is just subgroups. If $R$ is commutative, and $M=R$, then submodules are ideals of $R$.
- Let $(M_i)_{i \in I}$ be a set of submodules of $M$, then $\cap_{i \in I}M_i$ are submodule of $M$ and $\sum_{i \in I} M_i$ are also submodule of $M$.
- S:any subset of $M$, set $\langle S \rangle:=\{\sum_{s \in S} r_s s:r_s \in R\}=\bigcap_{N \leq M,\ S \subseteq N} N=\sum_{s \in S}Rs$.

**Observation**:
Let $f:M \rightarrow M'$ be a homomorphism $ker(f):=f^{-1}(0_{M'}) \leq M$ and $im(f) \leq M'$.

# Quotient modules
Let $R$ a ring and $M:R$-module and $N$ a submodule. We want to copy the notion of quotient in modules, i.e. give $M/N$ a addition such that it is still a module and $q:M \rightarrow M/N$ is a homomorphism of module.

**Def-prop**:
On the quotient group $(M/N,+)$ define $R \times (M/N) \rightarrow M/N$ by $(r,x+N) \mapsto rx+N$: This makes $M/N$ a $R$-moduleand $q$ a homomorphism.

*Proof*:
same as group.

If $R$ is a field, then it is quotient space, and if $R=\mathbb{Z}$ then it is just quotient group.

**Definition**:
Leet $f:M \rightarrow M'$ be a homomorphism, define $coker(f):=M'/im(f)$ be the cokernel(余核) and $coim(f):=M/ker(f)$ be the coimage of $f$. 

**Proposition**:(universal property of quotient)
Let $f:M \rightarrow M'$ be a homomorphism, $N \leq M$:submodule $N \subseteq ker(f)$ then there is a unique homomorphism $\bar{f}:M/N \rightarrow M'$ making the diagram commute:
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
&M \arrow[d,"q"] \arrow[r,"f"] &N'\\
&M/N \arrow[ur,"\bar{f}"]
\end{tikzcd}
\end{document}
```

*Proof*:
OK at the cases of additive groups, remain to show : $\bar{f}$ is an $R$-module homomorphism, in fact $\bar{f}(rx+N)=f(rx)=rf(x)=r\bar{f}(x+N)$.

**Proposition**:
$f:M \rightarrow M'$ then $\bar{f}:M/ker(f) \simeq im(f) \subseteq M'$.

*Proof*:
Know that $M/ker(f) \simeq im(f)$ as group, and $\bar{f}$ is a module homomorphism, so it is an isomorphism as modules.

**Definition**:
Let $R$ be a ring, and $(M_i)_{i \in I}$ be a family of $R$-module, then $\prod_{i \in I} M_i$ can be defined as an additive goroup. We further makes it into an $R$-module by $R \times \prod_{i \in I}M_i \rightarrow \prod_{i \in I}M_i$ by $(r,(x_i)_{i \in I}) \mapsto (rx_i)_{i \in I}$. This product is called direct product. And $\oplus_{i \in I}M_i$:= the submodule $\{(x_i)_{i \in I} \in \prod_{i \in I}M_i| \exists I_0 \subset I, \text{ finite s.t. } i \in I \backslash I_0,\ x_i=0\}$. We have homomorphism $M_j \stackrel{l_j}{\longrightarrow} \bigoplus_{i \in I} M_i \subset \prod_{i \in I}M_i \stackrel{p_j}{\twoheadrightarrow}M_j$ 

There is a internal verion of the above definition:
**Def-prop**:
Let $M$ be a $R$-module, $(M_i)_{i \in I}$ be a family of submodules define $\sigma: \bigoplus_{i \in I}M_i \rightarrow M$ sending $(x_i) \mapsto \sum x_i$.
1. $\sum_i M_i=M$ and $M_i\cap\sum_{j \neq i}M_j=\{0\}$.
2. $\forall x \in M$ there is a unique $(x_i) \in \bigoplus_{i \in I}M_i$ such that $x=\sum_ix_i$.
3. $\sigma$ is an isomorphism.
If these hold, we say that $M$ is the direct sum of $(M_i)_{i \in I}$. 

**Definition**:
Let $X$ be a set, then $R^{\oplus X}$ is an $R$-module, with a natural injection $X \hookrightarrow R^{\oplus X}$ by $x \mapsto (\delta_{xy})_{y \in X}$. The modules above are called *free module*.
Observation: for all $R$-module $N$, there is a natural bijection between $Hom_R(R^{\oplus X},N) \leftrightarrow \{f:X \rightarrow N\}$ 

Question:Given $M$ a module, is there a $X \subseteq M$ such that $M \simeq R^{\oplus X}$?
**Def-prop**: TFAE
1. $X$ generates $M$ and $X$ is linearly independent.
2. $\forall\,y \in M$ there is a unique $(r_x)_{x \in R} \in R^{\oplus X}$ such that $y=\sum_{x \in X}r_x x$.
3. Let $\phi:R^{\oplus X} \rightarrow M$ be the homomorphism corresponding to $X \hookrightarrow M$. Then $\phi$ is isomorphism.

*Proof*:
(1)$\Longleftrightarrow$(2): clear, just the same as the case of vector space.
(2)$\Longleftrightarrow$(3): the existence tells that $\phi$ is surjective, and the uniqueness tells that $\phi$ is injective.

In this case we say $M$ is free with basis $X$. We say $M$ is free if there is a $X \in M$ such that $M$ is free with basis $X$.
**Remark**: If $R$ is a field, then all $R$-module is free (It is also true if $R$ is division ring). But it is not true in general, for example $R=\mathbb{Z}$ and $M=\mathbb{Z}/n\mathbb{Z}$ with $|n|>1$ then $M \not\simeq \mathbb{Z}^{\oplus X}$ for any set $X$.

**Def-prop**:
$R$ a commutative ring, $M$ free with basis $X,Y$, then $|X|=|Y|$ which we will define it as $rk(M)$. 

*Proof*:(the case $R$ is integal domain)
First, $\forall X$ a basis, $|X|< \infty$. Seconly, $|Y| \leq |X|=:n$ the we identify $M$ with $R^{\oplus n} \hookrightarrow K^{\oplus n}=K^n$ where $K:=Frac(R)$ be the field of fraction. then for all $y_1,\cdots,y_{n+1}$ in $M=R^{\oplus n}$ there is $a_1,\cdots,a_{n+1} \in K$ such that $\sum_ia_iy_i=0$ in $k^n$, one may further assume $a_i \in R$ for all $i$, so $y_i$ are linearly dependent in $M$ hence $|Y| \leq |X|$.
**Remark**: $\exists$ versions for right $R$-modul. Facts: $Hom_R(R^{\oplus n},R^{\oplus m}) \leftrightarrow M_{m \times n}(R)$.

**key example**:
$F$ field and $x$ variable, then $M:F[X]-module \rightarrow F-vector\ space$ via $F \hookrightarrow F[x]$ as ring.We fix a $T \in End(V)$ and give $V$ a $F[x]$-module structure by $f \cdot v=f(T)v$. 

*Proof*: simple, consider $\phi:F[x] \rightarrow End(V)$ take $T=\phi(x)$, then $\phi(f)=f(T)$, and the other direction is clear.

**Goal**: Classify all $F[x]$-modules $V$ up to isomorphism.
**Proposition**:
Define $\sim$ a equvalient relation between $(V,T)$ where $V \in Mod_{F[x]}$ and $T \in End(V)$ as follows: $(V,T) \sim (V',T')$ if there is an isomorphism $\phi:V \rightarrow V$ such that $\phi T=T'\phi$. Then there is a bijection between all $F[x]$-modules $V,dim_FV=n$ (up to isomorphism) and $\{(V,T):dim_FV=n,T \in End(V)\}/\sim$.

**Theorem**:
$R:PID$ and $M$:f.g. $R$-module. Then $M \simeq R/I_1 \oplus \cdots \oplus R/I_k \oplus E$ where $I_1 > \cdots > I_k$ ideals in $R$ and $E$ a finitly generated free $R$ module and the set $(I_1,\cdots,I_k,E)$ is unique up to isomorphism.
In other words: Fix $n \in \mathbb{Z}_{\geq 1}$. Let $A \in M_{n \times n}(F)$  then there is a unique sequence of monic $f_1|\cdots | f_k$, $k \geq 1$ such that $\sum_{i}dimf_i=n$ and $A \sim diag(C_{f_1},\cdots,C_{f_k})$ called the rational canonical form. And $f_1|\cdots|f_k$ are invariant under conjugates.

*Proof*:
Let $M$ be the $F[x]$-module$/\simeq$ corresponding to $A$/conj, then $M \simeq F[x]/(f_1) \oplus \cdots \oplus F[x]/(f_k) \oplus E$. Because $M$ is finitly generated, so $E=\{0\}$. We already know that $F[x]/(f_i) \leftrightarrow C_{f_i}$, so $M \leftrightarrow  diag(C_{f_1},\cdots,C_{f_k})$ and the uniqueness follows from the structure theorem.

In fact, the minimal polynomial $Min_A=f_k$ and the characteristic polynomial $Char_A=\prod_if_i$. In particular, $Min_A | Char_A$ which is another proof of Cayley-Hamilton theorem.

Another application of the theorem: take $R=\mathbb{Z}$, then any abelian group $A \simeq \mathbb{Z}/d_1\mathbb{Z}\oplus\cdots\oplus\mathbb{Z}/d_k\mathbb{Z}\oplus\mathbb{Z}^r$, for some unique $d_1|\cdots|d_k$.

**NEXT**:
- Variants of the structure theorem.
- applications to the rational canonical form.(Jordan canonical form)
- Proof of the structure theorem.

**Definition**:
$R$: commutative ring $I \subset R$ be ideal and $M:R$-module then $M[I]:=\{x \in M| \forall a \in I,ax=0\}$. When $I=(h)$ then write $M[I]=M[h]$. If $R$ is integal and $x \in M$ $x \in M[h]$ for some $h \in R-\{0\}$ then $x$ is a torsion element of $M$. Otherwise we say $x$ is torsion-free.
**Example** $R$:integal domain then there are No torsion emelents $\neq 0$ in free $R$-modules. For integal domain $R$ and $R$-module $M$ then $M_{tors}:=\{x \in M:\text{torsion element}\}$ is a submodule of $M$.

**Definition**:
Let $M_{tf}:=M/M_{tors}$ called the torsion-free quotient of $M$. Check that $M_{tf}$ has not torsion elements$\neq 0$.

**Observation**:$h|k$ in $R$ $\Longrightarrow$ $M[h] \subset M[k]$.
Now assume$t \in R-\{0\}$ and $R:PID$ then $t \sim p_1^{a_1}\cdots p_m^{a_m}$.

**Lemma**:$M[t]=\bigoplus_iM[p_i^{a_i}]$.

*Proof*:
Suffice to show $t=ab$, $a,b \in R$ coprime then $M[t]=M[a]\oplus M[b]$. In fact, there is $u,v \in R$ such that $au+bv=1$, hence $x=aux+bvx$, then $M[t]=M[a]+M[b]$, and if $x \in M[a]\cap M[b]$ then $x=uax+vbx=0$.

Let $p$ be a prime in $R$, and $M:R$-module, then $M[p] \subset M[p^2] \cdots$. Write $M[p^\infty]=\bigcup M[p^i]$. So if $M[t]=M$, then $M=\bigoplus_p M[p^\infty]$. 

**Second** form of structure theorem for $M:f.g$ $R$-module, $R:PID$. $M \simeq R/(f_1) \oplus \cdots \oplus R/(f_k) \oplus (free)$ where $f_1|\cdots|f_k$ and for all $p \in R$ prime $p|f_k$ take $b_i(p)=sup_j\{p^j|f_i\}$, then $R/(f_1) \simeq \bigoplus R/(p^{b_i(p)})$, then $M_{tors} \simeq \bigoplus_{p|f_k}\bigoplus R/(p^{b_i(p)})$. Now take $R=F[x]$, we obtain the second form of rational canonical forms: $A \in M_{n \times n}(F),n \in \mathbb{Z}_{\geq 1}$, $Min_A=p_1^{a_1} \cdots p_m^{a_m}$, where $p_i$ are monic irreducible in $F[x]$, then $A \sim diag(A_1,\cdots,A_m)$, where $A_j=diag(C_{P_j^{b_1j}},\cdots,C_{P_j^{b_{r_j}j}})$. These data are uniquely determined by $A/conj$, up to permutation of $p_1,\cdots,p_m$.

# part of structure theorem
R:PID, the key tool is:
**Lemma**:
$E$ a free $R$-module, rank $n \in \mathbb{Z}_{\geq 0}$ and $N$ a submodule, then there is $f_1,\cdots,f_n$ in $E$ and $d_1,\cdots,d_n \in R$ such that $d_1|\cdots|d_n$ and $d_1f_1, \cdots,d_rf_r$ form a basis of $N$ where $r:=max\{i|d_i \neq 0\}$.

*Proof of $\exists$ part in structure theorem*
$M:f.g.R$-module, say generated by $E:=R^{\oplus n} \twoheadrightarrow M$ its kenral =:$N$ then $(r_i)_i \mapsto \sum_{i}r_ix_i$, so $M \simeq E/N$. Take $f_1,\cdots,f_n$ and $d_1,\cdots,d_n,r$ from the lemma, the $M \simeq Rf_1 \oplus \cdots Rf_n/(Rd_1f_1 \oplus \cdots\oplus Rd_rf_r)$. 

*Proof* of the uniqueness part of the structure therorem
$M_{tors} \subset M$ and $M_{tf}=M/M_{tors}$. Then the formation is canonical if $M \simeq M'$ then $M_{tors} \simeq M'_{tors}$ and $M_{tf} \simeq M'_{tf}$. We now reduced to the case of $E=\{0\}$. Pass from invariant factor to elementary factors, so it is suffices to show that given a unique $p$ in $R$, if $R/(p^{b_1}) \oplus \cdots \oplus R/(p^{b_k}) \simeq R/(p^{b_1'}) \oplus \cdots \oplus R/(p^{b_{k'}'})$, with $1 \leq b_1 \leq \cdots$ and $1 \leq b_1' \leq \cdots$, then $k=k'$ and $b_i=b_i'$.
Note that $M[p]=\bigoplus_i(R/p^{b_i})[p]=\bigoplus_i p^{b_i-1}R/p^{b_i}R \simeq \bigoplus_iR/(p)$ is naturally a $R/(p)$-module (recall that $R/(p)$ is a field) so $k=k'=dim_{R/(p)}M[p]$. More generally, for all $j>0$, $p^jM \simeq \bigoplus_ip^jR/p^{b_i}R \simeq_{i:j<b_i}R/p^{b_i-j}R$ so $(p^jM)[p]$ had dimension = the number of i such that $j<b_i$, denoted as $v_i$ and $v_i'$ resp. using $M \simeq M'$ the $p^jM[p] \simeq p^{j}M'[p]$ so $v_i=v_i'$ for all $j$, thus we have $b_i=b_i'$ 

It remains to show the lemma:
**Lemma**:
$E$ a free $R$-module, rank $n \in \mathbb{Z}_{\geq 0}$ and $N$ a submodule, then there is $f_1,\cdots,f_n$ in $E$ and $d_1,\cdots,d_n \in R$ such that $d_1|\cdots|d_n$ and $d_1f_1, \cdots,d_rf_r$ form a basis of $N$ where $r:=max\{i|d_i \neq 0\}$.

# Smith normal form of matrix
$R$ commutative ring and $n,m \in \mathbb{Z}_{\geq 1}$ $M$ a $R$-module, for $e_1,\cdots,e_n,x_1,\cdots,x_m \in M$ and $A=(a_{ij}) \in M_{n \times m}(R)$, and $(x_1,\cdots,x_m)=(e_1,\cdots,e_n)A$.

Facts: 
- $(e_1,\cdots,e_n)(AB)=((e_1,\cdots,e_n)A)B$
- $(e_1,\cdots,e_n)I_n=(e_1,\cdots,e_n)$
- If $(e_i)$ are linearly independent, then $(e_i),(x_i)$ uniquely determined the matrix $A$.
$$GL(n,R):= \{A \in M_{n \times n}(R): \exists B \in M_{n \times n}(R)\ AB=BA=I_n\} =\{A \in M_{n \times n}(R):det(A) \in R^\times\}$$
- If $(y_1',\cdots,y_n')=(y_1,\cdots,y_n)P$ and $P \in GL(n,R)$, then $\sum_{i}Ry_i=\sum_iRy_i'$. 
- If $M$ is free, and $e_1,\cdots,e_n$ is a basis, then $(e_1',\cdots,e_n')=(e_1,\cdots,e_n)A$, A unique, then $e_1' ,\cdots,e_n'$ form a basis of $M$ if and only if $A \in GL(n,R)$.

Let $E$ free with basis $e_1,\cdots,e_n$ and $N$ a submodule generated by $x_1,\cdots,x_m$. Take the unique $A$ such that $(x_1,\cdots,x_m)=(e_1,\cdots,e_n)A$
Observe that $A \rightarrow AP$ with $P \in GL(m,R)$, is euqvalient to replacing $(x_1,\cdots,x_n)$ with $(x_1',\cdots,x_n')$. 
**Theorem**(H.I.S.Smith):
Let $R$ be $PID$, and $A \in M_{n \times m}(R)$, then there is $P \in GL(m,R)$ and $Q \in GL(n,R)$, such that $d_1|d_2|\cdots$ with $A=Q \begin{pmatrix}d_1\\&d_2\\&&\ddots\end{pmatrix} P$. 

*Proof* of the Lemma:
Given $E$:free say with $N \subset E$ be submodule, first $N$ is finitly generated(omitted)
Next, take generators $x_1,\cdots,x_m$ of $N$. Take $A$ such that $(x_1,\cdots,x_m)=(e_1,\cdots,e_n)A$ and using the above theorem, there is $P,Q$ such that $(x_1,\cdots,x_m)P^{-1}=(e_1,\cdots,e_n)Q \begin{pmatrix}d_1\\&d_2\\&&\ddots\end{pmatrix}$, and let $(f_i)=(e_i)Q$ is still a generator of $E$ and $(x_i')=(x_i)P^{-1}$ is still a generator of $N$, so $x_i'$ can be written in the form of $d_if_i$.

*Proof* of the theorem:
Assume that $R=\mathbb{Z}$ or $F[x]$ where $F$ is a field. We start with the case of $R=\mathbb{Z}$. Among all matrix entries of all $QAP$, the one with minimal $|\cdot|$. Can move it ro $(1,1)$. May assume it is $a_{11}$
Claim:$a_{11}|a_{1j}$ and $a_{11}|a_{ij}$
If not, say $a_{1j}=a_{11}d+r$ $0<r<|a_{11}|$ , using elementary column operation we get $r$ at $(1,j)$ a contradiction.
Now we may assume that $A=\begin{pmatrix}d_1\\&*\end{pmatrix}$, using inductiong, by multiplying $\begin{pmatrix}1&\\&GL\end{pmatrix}$ we may assume $d_2|d_3|\cdots$, it is left to be shown that $d_1|d_2$. If not, we still ues the elementary column operator, and form a contradiction of the choice of $d_1$.
(There is a proof of the general version in the text book)

**Definition**:
$R$ a commutative ring. We say $R$ is *noetherian* if all acending chain $I_1 \subset I_2 \subset \cdots$ of ideals are of finite length (c.f.[[noetherian and artinian ring]]) We say $M$ a module if *noetherian* if all acending chain of submodules $M_1 \subset M_2 \subset \cdots$ are of finite length.
*Recall*: $PID$ are noetherian.

**Proposition**:
Assume $R$ commutative ring $M:$ $R$-modules, $M' \subset M$ submodule, $M'':=M/M'$. Then $M$ is noetherian iff $M''$ and $M'$ are both noetherian.

# computing RCF
$V$ a F-vector space, $dim_FV=n \in \mathbb{Z}_{\geq 1}$. Let $T \in End(V) \rightarrow$ ungraded $V$ to $F[X]$-modules $\phi:F[X]^{\oplus n} \rightarrow V$ such that there is a $F[X]$-basis $f_1,\cdots,f_n$ of $F[X]^{\oplus n}$ and monic $d_1|\cdots|d_n$ in $F[X]-\{0\}$ such that $Ker \phi=\bigoplus_iF[X]d_if_i$. Fix an $F$-basis $v_1,\cdots,v_n$ of $V$ let $e_1,\cdots,e_n$ be the standard $F[X]$-basis of $F[X]^{\oplus n}$.
Define $\phi$ by $\phi(e_i)=v_i$, then $\phi(\sum_ir_ie_i)=\sum_ir_i(T)v_i$ => $\phi$ is surjective. In $F[X]^{\oplus n}$ define $_j=Xe_i-\sum_ia_{ij}e_i$, then $A \in M_{n \times n}(F) \leftrightarrow T \in End(V)$. $N:=\sum_jF[X]x_j \subset F[X]^{\oplus n}$.

**Lemma**:$ker(\phi)=n$.

*Proof*:
($\supset$) $\phi(x_j)=Tv_j-\sum_ia_{ij}v_i=0$.
($\subset$) $Xe_j=\sum_ia_{ij}e_i+x_j \in$ the coset $\sum_ia_{ij}e_i+N$, so $\forall x \in F[X]^{\oplus n}$ $x+N=\sum_ic_ie_i+N$. In general, $x=\sum_jg_je_j$, for $g_j \in F[X]$, so it is suffice to consider $x=X^ke_j$. Hence $\phi(x)=0 \Rightarrow \sum_ic_i \phi(e_i)=0 \Leftrightarrow c_1=\cdots=c_n=0$.

Thus $\phi$ induces $\overline{\phi}:F[X]^{\oplus n}/N \stackrel{\sim}{\longrightarrow} V$ as $F[X]$-module.

Observe that $(x_1|\cdots|x_n)=(e_1|\cdots|e_n)(XI_n-A)=(e_1|\cdots|e_n)Q \begin{pmatrix}d_1\\&\ddots\\&&d_n\end{pmatrix}P$, drop these $d_i=1$, the invariant factors in $RCF$.

# Jordan canonical form (JCF)
$F$:field $n \in \mathbb{Z}_{\geq 1}$.

**Definition**:
$R$:ring $r \in R$. If $\exists d \geq 1$ s.t. $r^d=0$, we say $r$ is a nilpotent elements of $R$. The minimal possible $b$ is called the nilpotent index of $r$. $R=M_{n \times n}(F)$ or $End(V)$ identify $\lambda \in F$ with $\lambda \cdot 1_{n \times n}$ or $\lambda \cdot id_V$.
**Recall**:$V_{[\lambda]}:=Ker(T-\lambda)^n=V[(X-\lambda)^\infty]$. 

**Proposition**:
TFAE for $T \in End(V)$.
1. $T$ is nilpotent.
2. $\exists k >1$, $Min_T=X^k$.
3. $Char_T=X^n$.
4. $V=V_{[0]}$.

*Proof*: easy

$\forall \lambda \in F, d \in \mathbb{Z}_{\geq 1}$, define $J_d(\lambda):=\begin{pmatrix}\lambda &1\\&\ddots&\ddots\\&&\ddots &1\\ &&& \lambda\end{pmatrix} \in M_{d \times d}(F)=\lambda+J(_d0)$, $J_1(\lambda)=\lambda$, $J_d^{下}(\lambda)=\,^tJ_d(\lambda)$. Then $J_d^{下}(0)=C_{X^d}$ => $Min_{J_d(0)}=X^d=char_{J_d(0)}$. In general $Min_{J_d(\lambda)}=(X-\lambda)^d=Char_{J_b(\lambda)}$.

**Lemabda**:
Let $A \in M_{n \times n}(F)$, nilpotent, there is a uniue $b_1 \leq \cdots \leq b_r \in \mathbb{Z}_{\geq 1}$ such that $A \sim \begin{pmatrix}J_{b_1}(0)\\&\ddots\\&&J_{b_r}(0) \end{pmatrix}$, morover $b_r$ is the nilpotent index of $A$.

*Proof*:
Start with the verion of $J_{d_i}^{下}(0)$. let $d:=$ the nilpotent index of $A$, and $X^d=Min_A$. Let $f_1|\cdots|f_r$ be the invariant factor , then $f_i=X^{b_i}$. Using $RCF$, then we are done. 

**Theorem**:
Suppose $A \in M_{n \times n}(F)$, with $Char_A$ split in $F[X]$ say with roots $\lambda_1,\cdots,\lambda_m$ then $A \sim \begin{pmatrix}A_1\\&\ddots\\&&A_m\end{pmatrix}$ where $A_j=\begin{pmatrix}J_{b_{1,j}}(\lambda_j)\\&\ddots\\&&J_{b_{r_jj}}(\lambda_j)\end{pmatrix}$. These data are unique up to permutation of index $j$.

*Proof*:
Consider $T \in End(V)$, $dim_FV=n$, $V=\bigoplus_{i=1}^mV_{[\lambda_i]}$, forall $j$ $T_j-\lambda_j$ is nilpotent => $T_j \leftrightarrow A_j$.
Uniqueness: Suoopse we hace the above expression, corresponding to $V=\bigoplus_jV_j:$ T-invariant subspaces => $T|_{V_j}$ is nilpotent for all $j$, i.e. $V_j \subset V[(X-\lambda_j)^\infty]=V_{[\lambda_j]}$ => $V_j=V[\lambda_j]$. So the uniqueness reduced to that of $RCF$.
**Note**: $J_1(\lambda)=\lambda$, so $A$ is diagonalizable <=> $Char_A$ split in $F[X]$ and all Jordan blocks are $1 \times 1$.

Application: Jordan-chevalley decomposition

**Theorem**:
$dimV=n \in \mathbb{Z}_{\geq 1}$, $T \in End(V)$, $Char_T$ splits in $F[x]$, then there is a unique $S,N \in End(V)$ such that $S$ is diagonalizable over $F$ and $N$ a nilpotent, and $T=S+N$, $SN=NS$.

*Proof*:
- Existence: Using $JCF$, we may assume $V=F^n$, T <-> $J_n(\lambda) \in M_{n \times n}(F)$ and $J_n(\lambda)=\lambda+J_n(0)$.
- Uniqueness: $T=S+N$, $SN=NS$. Let $\mu_1,\cdots,\mu_l$ be the distinct eigenvalues of $S$. $V=V_1 \oplus \cdots \oplus V_l$: eigenspace of $S$. Then $\forall 1 \leq j \leq l$, $T_j:=T|_{V_i}=\mu_j+(N|_{V_j})$, one know that $T_j-\mu_j$ is nilpotent so $V_j \subset$ the generalized $\mu_j-eigenspce$ of $T$. So $V=\bigoplus_{\mu \in F}V_{[\mu]}$, then we have $V_j=V_{[\mu_j]}$ and $\mu_1,\cdots,\mu_l$ are perscisely the eigenvalues of $T$ => $S$ is determined by $T$: $S|_{V_{[\lambda]}}=\lambda$, and then $N=FS$.
**Remark**:
there is $f,g \in F[x]$ suck that $F(T)=S$ and $g(T)=N$. Take $V=V_1 \oplus \cdots \oplus V_l$ as before and take $f \equiv \mu_i \pmod{(X-\mu_i)^n}$ if $F[X]$m then $f(T)|_{V_{j}}=\mu_i$ since $(T-\mu_j)^n|_{V_j}=0$, so $f(T)=S$, take $g=X-f$.

# Tenser products
**Idea**: Given a field $F$, $V,W$ a $F$-vector space. Want to form paired vectors $v \otimes w$ such that $V \times W \rightarrow$ some v.s. is bilinear.

The constructiong is somehow canonical.

**Def-prop**:
Given $V,W$ as before, consider pairs $(L,B)$ where $L$ is $F$-vector space and $B:V \times W \rightarrow L$ bilinear.
1. $\exists(L_{univ},B_{univ})$ such that for all $(L,B)$ there is a unique $\phi:L_{univ} \rightarrow L$ such that $B=\phi \circ B_{univ}$.
2. $(L_{univ},B_{univ})$ is unique up to isomorphism.

*Proof*:
1. Let $$L_{univ}=V \times W/ \langle (\lambda_1v_1+v_2) \otimes (\lambda_2w_1 +w_2)-\lambda_1\lambda_2(v_1 \otimes v_2)-\lambda_1(v_1 \otimes w_2)-\lambda_2(v_2 \otimes w_1)-v_2 \otimes w_2 \rangle$$ then one immediately check that it is what we want.
2. easy, taking $(L,B)=(L_{univ},B_{univ})$, then id is the unique morphism. Meanwhile, consider $(L'_{univ},B'_{univ})$, then there is $\phi,\phi'$ such that $\phi \circ\phi'=id$ and $\phi' \circ \phi=id'$.

**Def-prop**:
Given a linear maps $f_i:V_i \rightarrow W_i$ $1 \leq i \leq n$ then there is a unique map $f_1 \otimes \cdots \otimes f_n$ such that the diagran commutes.

- $id_{V_1} \otimes \cdots \otimes id_{V_n}=id_{V_1\otimes\cdots\otimes V_n}$ 
- $(f_1 \otimes \cdots \otimes f_n)(g_1\otimes\cdots\otimes g_n)=f_1g_1\otimes\cdots\otimes f_ng_n$ for $U_i \stackrel{g_i}{\longrightarrow} V_i \stackrel{f_i}{\longrightarrow} W_i$. 

**Observation**:If $V_i=\{0\}$ for some $i$, then $V_1 \otimes \cdots \otimes V_n =\{0\}$. 

**Lemma**:
$\phi,\psi \in Hom(V_1 \otimes \cdots \otimes V_n,M)$ if $\phi(v_1\otimes\cdots\otimes v_n)=\psi(v_1\otimes\cdots\otimes v_n)$ for all $v_1,\cdots,v_n$, then $\phi=\psi$.

*Proof1*:
$\{v_1\otimes\cdots\otimes v_n:v_i \in V_i\}$ generates $V_1\otimes\cdots\otimes V_n$ and use the construction of tensor product.

*Proof2*:
use the natural isomorphism $Mul(V_1 \times \cdots \times V_n,M) \rightarrow Hom(V_1\otimes\cdots\otimes V_n,M)$ where $Mul$ refers to the multilinear maps. Then the lemma is clear.

**Basic properties**
- $V_1 \otimes V_2 \otimes V_3=V_1 \otimes (V_2 \otimes V_3)$. 
- $F \otimes V \simeq V \otimes F \simeq V$.
- $V \otimes W \simeq W \otimes V$.
*Proof*: using the basic definitions and is easy.

**Next**:$\cdots \otimes \bigoplus_{i \in I}V_i \otimes \cdots \simeq \bigoplus_{i \in I} \cdots \otimes V_i \otimes \cdots$.
*Proof*:
Suffice to show $V \otimes W \simeq \bigoplus_{i \in I} (V_i \otimes W)$. 
idea: check the universal properties for "$V \otimes W$". 
Fix $L:F$-v.s. $Bil(V,W;L) \rightarrow \prod_{i \in I}Bil(V_i,W;L) \simeq Hom(V_i,W;L)$ by $B \mapsto (B|_{V_i \times W})_{i \in I}$, note that $Hom(\bigoplus_{i \in I}(V_i \otimes W),L) \rightarrow \prod_{i \in I}Hom(V_i \otimes W,L)$ by $\phi \rightarrow(\phi_i:=\phi|_{V_i \otimes W})_{i \in I} \rightarrow (\phi_iB_{i,univ})$. Hence there is  a unique map $V \otimes W \rightarrow \bigoplus_{i \in I}(V_i \otimes W)$ such that $V \times W \rightarrow V \otimes W \rightarrow \bigoplus_{i \in I}(V_i \times W)=V \times W \rightarrow \bigoplus_{i \in I}(V_i \otimes W)$.

Then $V \otimes W$ has basis $\{v_i \otimes w_j\}_{(i,j) \in I \times J}$ as $V = \bigoplus_{i \in I} Fv_i \simeq F$, $W=\bigoplus_{j \in J} Fw_j \simeq F$, and use the above proposition.

Fix a field $F$.

**Proposition**:
Let $f_i:V_i \rightarrow W_i$, be a family of linear map
1) If $\forall i$ $f_i$ is surjective, then so is $f_1 \otimes \cdots \otimes f_n$ in $V_1\otimes\cdots\otimes V_n \rightarrow W_1\otimes\cdots\otimes W_n$.
2) Same if "surjective" -> injective.
*Proof*:
- Elements of the form $w_1\otimes\cdots\otimes w_n$ generate $W_1\otimes\cdots\otimes W_n$ the image of $f_1\otimes\cdots\otimes f_n$.
- Special case $W_i=V_i \oplus V_i'$ for all $i$, and $f_i:V_i \hookrightarrow W_i$ be the natural inclusion. Then we have $W_1\otimes\cdots\otimes W_n=(V_1\otimes\cdots\otimes V_n) \oplus others$ ($\otimes$ commutes with $\oplus$). General case: $\forall i$, $\exists V_i' \subset W_i$ s.t. $W_i=f_i(V_i) \oplus V_i'$, and use the previous case.
**Remark**:
Almost all properties above is still correct over a general commutative ring, except the proposition above where we use $W=V \oplus V'$.

Recall $V$ a $F$-vector space, $V^*=Hom(V,F)$ the dual space of $V$.

Canonical paring $\langle,\rangle:V^* \times V \rightarrow F$ by $(\lambda,v)\mapsto \lambda v$. The map is clearly bilinear, so $V^* \otimes V \rightarrow F$ naturally.

**Proposition**:
$V,W$ F-vector space. There is a linear map $V^* \otimes W \rightarrow Hom(V,W)$ is injective ($\lambda \otimes w \mapsto (v \mapsto \lambda v w)$). In particular, if $V,W$ are finite dimensional, then it is an isomorphism.

*Proof*:
The map $V^* \otimes W \rightarrow Hom(V,W)$ $(\lambda,w) \mapsto \langle \lambda, \cdot \rangle w$. Consider $\sum_i\lambda_i \otimes w_i$, may assume $w_1,\cdots,w_k \in W$ are linearly independent. $\forall v \in V$ $\sum_i\langle \lambda_i,v\rangle=0$, so $\langle\lambda_i,v\rangle=0$, so $\lambda_i=0 \in V^*$. Then the map is comtained in $\langle w_1,\cdots,w_n \rangle$ so it is of rank <= k.

**Dual of $\otimes$-product**
There is a linear map $\Psi:V^*_1\otimes\cdots\otimes V^*_n \rightarrow (V_1\otimes\cdots\otimes V_n)^*$. $\Psi$ is an isomorphism if $dimV_i< \infty$.

*Proof*:
The existence of $\Psi$: Given $\lambda_1\cdots \lambda_n$. The map $V_1 \times \cdots \times V_n \rightarrow F$ by $(v_1,\cdots,v_n) \mapsto \prod_i \langle \lambda_i,v_i \rangle$ we get $V_1\otimes\cdots\otimes V_n \rightarrow F$ as it is multilinear. Assume $dimV_i<\infty$, we have the dimension of two side are the same. 
Show $\Psi$ is injective: just choose a basis of $V_i$, and it is rutine to check.

V:F-v.s. and $n \in \mathbb{Z}_{\geq 0}$, then $V^{\otimes n}:=V \otimes \cdots \otimes V$, $V^{\otimes 0}=F$. So the above propositions tells us that if $dimV < \infty$, we have that $()^*,\ Hom(,) \ \otimes$ are canonically isomorphic to $V^{\otimes p} \otimes (V^*)^{\otimes q}$ for some $p,q \geq 0$. Elements like this are called tensers of $(p,q)$-type.

# Tensor algebra
**Definition**:
$F$ a field, a $F$-algebra is a ring $A$ with $F$-vector structure. The notion of "subalgebra", "ideal", "quotient" can inherait from ring. 

**Def-prop**:
$V$ a F-v.s. set $T(V)=\bigoplus_{n \geq 0}V^{\otimes n}$, $(V^{\otimes a}) \otimes (V^{\otimes b}) \stackrel{\sim}{\longrightarrow} V^{\otimes a+b}$ assemble into $T(V) \otimes T(V) \rightarrow T(V)$. This makes $T(V)$ into an $F$-algebra with $1_{T(V)}=1_F \in V^{\otimes 0}=F$.

Note:$T(V)$ is note commutative ingeneral.

# Symmetric/ecterior algebra
$V$ a F-v.s. $m \in \mathbb{Z}_{\geq 1}$, $M$:F-v.s. $C:V \times \cdots \times V \rightarrow M$ be multilinear map.

**Definition**:
If $C(\cdots,x,y,\cdots)=C(\cdots,y,x,\cdots)$ then $C$ is cyclic. IF $C(\cdots,x,x,\cdots)=0$, then $C$ is alternating.

**Definition**:
Sym(V) is $T(V)$ quotient out by ideals generated by $x \otimes y-y \otimes x$. 

$\bigwedge(V)=\bigoplus_{n \geq 0} \wedge^n(V)$, and $Sym(V)=\bigoplus_{n \geq 0} sym^n(V)$. Then $Sym(V)=T(v)/id_{\bigwedge}$. 
- They satisfy $sym^0(V)=F=\wedge^0(V)$ and $sym^1(V)=V=\wedge^1(V)$. 
- These algebras are generated by $V$ over $F$ because the same holds for $T(V)=\bigoplus_{n \geq 0}V^{\otimes n}$, write the multiplication $Sym(V)$ as $\cdot$.
- forall $x,y \in V$, $xy=yx$ in $Sym^2(V)$ by construction => $sym^2(V)$ is commutative and $x \wedge y= -y \wedge x$ in $\wedge^2(V)$.
- Functoriality. Given a linear map $f:V \rightarrow W$ we get a homomorphism $T(f):T(V) \rightarrow T(W)$ of $F$-algebra $T(f)|_{V^{\otimes n}}=f \otimes \cdots \otimes f$. $T(f)$ induces homomorphisms of $F$-algebra $Sym(f):Sym(V) \rightarrow Sym(W)$, and $\wedge (f): \wedge(V) \rightarrow \wedge(W)$.

**Goal**: understand the structure of $Sym(V)$ and $\bigwedge(V)$.
*Facts*: $dim(V)=n \in \mathbb{Z}_{\geq 1}$ => $F[X_1,\cdots,X_n] \stackrel{\sim}{\longrightarrow} Sym(V)$ by $X_i \mapsto v_i$ as $F$-algebra.

**Theorem**:
Assume $dim(V)=n \in \mathbb{Z}_{\geq 0}$. Say with basis $v_1,\cdots,v_n$.
1) $m>n$ => $\wedge^m(V)=\{0\}$.
2) $0 \leq m \leq n$, => $dim(\wedge^m(V))=\begin{pmatrix}n\\ m\end{pmatrix}$
3) $dim(\bigwedge)=2^n$.

These concept is related to the minors of matrix $A$.

**Proposition**:
$char F \neq 2$:same as $^tA=-A$, in general, $R$ a ring, we write $n \in R^\times$ to mean $n \cdot 1_R \in R^\times$ i.e. $\div n$ make sanse in $R$. Then $R=F$ a field <==> $char F \not{\vert}$ $n$. 

# case of char = 0
$F$ a field and $V$ a f-v.s. and $n \in \mathbb{Z}_{\geq 1}$. Let $S_n$ acts on $V^{\otimes n}$ as follows $V \times\cdots\times V \rightarrow V^{\otimes n}$ by $(v_1,\cdots,v_n) \mapsto v_{\sigma^{-1}(1)} \otimes\cdots\otimes v_{\sigma^{-1}(n)}$ get $\sigma:V^{\otimes n} \rightarrow V^{\otimes n}$. One immediately check that it is indeed an homomorphism.

**Definition**:
$V^{\otimes n}_{sym}:=\{x\in V^{\otimes n}:\forall \sigma \in S_n,\ \sigma x=x\}$, and $V^{\otimes n}_{sym}:=\{x\in V^{\otimes n}:\forall \sigma \in S_n,\ \sigma x=x\}$. Take $\bigoplus_{n \geq 0}$, => get subspaces $T_{sym}(V),\ T_{\bigwedge}(V)$ of $T(V)$. When $char F=0$, they are often used to define $Sym(V)$ and $\bigwedge(V)$. 
Quotient map $q^n_{sym}:V^{\otimes n} \twoheadrightarrow sym^n(V)$ and $q^n_{\wedge}:V^{\otimes n} \twoheadrightarrow \wedge^n(V)$.

**Theorem**:
when $n! \in F^{\times}$ they restric to $V^{\otimes n}_{sym} \stackrel{\sim}{\longrightarrow} sym^n(V)$, the same is also true for $\wedge$.

*Proof*:
Consider only $sym^n$ and take $Avg:x \mapsto \sum_{\sigma}\frac{\sigma x}{n!}$ is a projection $V^{\otimes n} \twoheadrightarrow V^{\otimes n}_{sym}$, so we can split $V^{\otimes n}=V^{\otimes n}_{sym} \oplus ker(Avg)$. note that $ker(Avg) \subset ker(q^n_{sym})$, also the intersection of $V^{\otimes n}$ and $ker(q^{n}_{sym})$ are $\{0\}$, then we are done.

Symmetric algebra: $charF=0$ cases/exterior
The quotient maps $q^n_{sym}:V^{\otimes n} \twoheadrightarrow Sym^nV$ and $q^n_{\wedge}:V^{\otimes n} \twoheadrightarrow \wedge^n(V)$ restrict to isomorphism $V^{\otimes n}_{sym} \stackrel{\sim}{\longrightarrow} Sym^nV$ and $V^{\otimes n}_\wedge \stackrel{\sim}{\longrightarrow} \wedge^n(V)$. $p^n_{sym}$ and $p^{n}_{\wedge}$ be its inverse.

**Proposition**:
$\forall x \in V^{\otimes a}_{sym}\ y \in V^{\otimes b}_{sym}$, $char F \not{\vert} (a+b)!$ then $p^{a+b}_{sym}(q^a_{sym}(x)q^b_{sym}(y))=\frac{a!b!}{(a+b)!}\sum_{\sigma \in S_{a+b}/S_a \times S_b}\sigma(x \otimes y)$. $S_a \times S_b \hookrightarrow S_{a+b}$ i.e. multiplication in $T_{sym}(V)$ is $\otimes$ + symmetrication

*Proof*: Omit the idea of averaging.

**Corollary**:
$dim V< \infty$, $n \in \mathbb{Z}_{\geq 0}$, $n! \in F^{\times}$, => there are canonical $\simeq$ of vector spaces $Sym^n(V^v) \simeq Sym^n(V)^v$ where $V^v:=Hom(V,F)$.

*Proof*:
$(V^v)^{\otimes n} \stackrel{\Psi}{\longrightarrow} (V^{\otimes n})^v \stackrel{\Phi}{\longrightarrow} Mul(V, \cdots,V;F)$. and $S_n$ acts on $(V^v)^{\otimes n}$. $S_n$ acts on $Mul(V,\cdots,V;F)$ by $(\sigma C)(x_1,\cdots,x_n)=C(x_{\sigma(1)},\cdots,x_{\sigma(n)})$ and they match under $\Phi\Psi$! the rest is clear. 
# Another application:Change of field

**Idea**: $E$ a field and $F \subset E$ a subfield, given a $F$-v.s $V$ want to construct a $V_E$ as E-v.s.

Write $\otimes_F:= \otimes$ as $F$-v.s. One obviously can view $E$ as an $F$-v.s., then we define $V_E:=V \otimes_F E$, the one immediately check that it is what we want.

**observation**:
Let $f:V \rightarrow W$ be a linear map of $F$-vector space, then $id_E \otimes f:V_E \rightarrow W_E$ is an E-linear 

If $V$ has a basis $\{v_i\}_{i \in I}$, then $V_E=E \otimes_F(\bigoplus_{i \in I}Fv_i) \simeq \bigoplus_{i \in I}(E\otimes_FFv_i) \simeq \bigoplus_{i \in I} E$ => $V_E$ has basis $\{\tilde{v_i}:=1_E \otimes v_i\}$, in particular $dim_FV=dim_EV_E$.

Consider the $F$-linear mao $i:V \rightarrow V_E$ by $v \mapsto 1_E \otimes v$, the $i$ is injective as it is the composite of $V \simeq F \otimes_F V \hookrightarrow E \otimes_FV=V_E$. 

**Remark**:THis characterized up to a unique isomorphic when $V$ is given.

# Some words about categories
A category contains:
- $Ob(e)$: a class of "objects" in $\mathcal{C}$.
- morphism : $\forall x,y \in Ob(e)$, a set $Hom_{\mathcal{C}}(x,y)=Hom(x,y)$, in particular $id_x \in Hom(x,x)$.
- $\forall x,y,x$ $o:Hom(y,z) \times Hom(x,y) \rightarrow Hom(x,z)$ such that $o$ is associative.
Example:everything learned before in this class (morphism -> homomorphism)

In a generated category, we have:
- commutative diagram: $x \stackrel{h}{\longrightarrow}z$, $x \stackrel{f}{\longrightarrow} y$, $y \stackrel{g}{\longrightarrow} z$ such that $gf=h$, then we may draw a diagram 
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
&x \arrow[r,"f"] \arrow[d,"h"] &y \arrow[dl,"g"]\\
&z 
\end{tikzcd}
\end{document}
```
- isomorphism: we say $f \in Hom(X,Y)$ is an isomorphism if there is a $f^{-1} \in Hom(Y,X)$ such that $f \circ f^{-1}=id_Y$ and $f^{-1} \circ f=id_X$.