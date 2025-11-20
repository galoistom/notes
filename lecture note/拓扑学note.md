---
updated_at: 2025-10-23T09:51:56.095+08:00
---
#topology #lectureNote 
>[!note] 拓扑的定义
>$(X,\tau)$ 是一个二元对, $X$ 是一个集合, $\tau \subseteq 2^{X}$, 满足:
>1. $X,\varnothing \in \tau$
>2. $\bigcap A \in \tau$, $\forall A \in \tau$. 
>3. $\bigcup_{i=1}^{n}A_{i} \in \tau$, $\forall A_{i} \in \tau$. 

一个比拓扑更强的概念是度量 $d:X\times X\rightarrow \mathbb{R}$, 满足: 
1. $d(x,y)\geq0$
2. $d(x,x)=0$, $d(x,y)=d(y,x)$
3. $d(x,y)+d(y,z)\geq d(z,x)$

特别的$\tau=\{ X ,\varnothing\}$ 为平凡拓扑, $\tau=2^{Z}$ 为离散拓扑 (对应度量为$d(x,y)=\begin{cases}1\text{ if } x=y\\ 0 \text{ if } x\neq y\end{cases}$) 但并非所有拓扑都有对应的度量.

我们称所有$\tau$中的集合为开集, $A\subseteq X$ 是闭集若$A^{c} \in \tau$. 特别的, $x \in X$ 的邻域是一个包含$x$的开集. 

**Proposition**: $U \subseteq X$, then $U \in \tau$ if and only if for all $x \in U$ there is a neighbor $x \in O \subseteq U$. 

我们定义内点$A^{\circ}:=\{ x \in A \subseteq X : \exists O \in \tau,\  x \in O \subseteq A \}$. Then we have $A$ open if and only if $A=A^{\circ}$ (Use the proposition above). 

我们会有$(A^{\circ})^{\circ} = A^{\circ}$, $(A \cup B)^{\circ} = A^{\circ}\cup B^{\circ}$, $(A\cap B)^{\circ}=A^{\circ}\cap B^{\circ}$. 

称 $x_{0}$ 为集合 $A$ 的极限点或聚点若 $x_{0}$ 的每个邻域都包含至少一个 $A$ 中的不同于 $x_{0}$ 的点. $\overline{A}:=\{ x: x \text{ a limit in } A \}$, 称为 $A$ 的闭包. 

**Proposition**: $A$ is closed if and only if $A=\overline{A}$. 

对于 $X$ 的子集 $A$, 若 $X=\overline{A}$, 则称 $A$ 在 $X$ 中稠密. 若 $X$ 存在可数的稠密集, 则称其为可分空间. 对于这样的一个$X$, 若有一族开集 $\beta$ s.t. $X$ 中任一开集都是 $\beta$ 中一些开集的并, 则称 $\beta$ 生成 $\tau$. 

**Theorem**: Let $\beta \subseteq \tau$, if $\forall U,V \in \beta$, and $x \in U\cap V$, there is a $W \in \beta$ such that $x \in W \subset U\cap V$. 

*Proof*: let $T=\left\{  \bigcup_{V\in B}V:B\in\beta  \right\}$, then $T$ is a topology on $X$. Taking $B$ to be $\varnothing$ and $X$, we know $X$ and $\varnothing$ is in $T$. Let $\beta_{\alpha} \in \beta$, $\alpha \in A$, and $U_{\alpha}=\bigcup_{v \in \beta_{\alpha}}V$. Let $\beta'=\bigcup_{\alpha \in A}\beta_{\alpha}$. then $U=\bigcup_{V\in\beta'}v=\bigcup_{\alpha \in A}\bigcup_{V\in\beta_{\alpha}}V=\bigcup_{\alpha \in A}U_{\alpha}\in T$. Similarly, we can check that if $\beta_{\alpha},\beta_{\theta}\in\beta$, then $\beta_{\alpha}\cap\beta_{\theta}\in T$. 

# 连续映射
**Definition**: $X,Y$ topological space, $f:X\rightarrow Y$ be morphism. 
1. $f$ is **continuous(连续的)** at $x$ if 所有 $f(x)$ 的邻域 $V$ 有 $f^{-1}(V)$ is open.
2. $f$ is continuous, if $f$ is continuous at all $x \in X$. 
3. $f$ is 同胚, if $f$ is a bijection and $f,f^{-1}$ both continuous. 此时, 我们也称 $X,Y$ 同胚. 

**Proposition**: $f:X\rightarrow Y$ continuous <==> for all $V$ open in $Y$, $U:=f^{-1}(V)$ is open in $X$. (proof is simple)

**Proposition**: suppose $f:X\rightarrow Y$ be a morphism, $A\subseteq X$ be a subspace, $f|_{A}:A\rightarrow Y$, then 
1. If $f$ is continuous on $A$ at $x \in A$, then $f|_{A}$ is continuous at $x$.
2. If $A$ is a neighbor for $x_{0} \in A$, $f|_{A}$ is continuous at $x_{0}$, then $f$ is continuous at $x_{0}$.

**Proposition**: the composition of continuous morphism is also a continuous. 

**Proposition**: TFAE
1. $f:X\rightarrow Y$ continuous.
2. suppose $B$ is a topological bases, then $f^{-1}(V)$ is open for all $V \in B$.
3. for all $A\subseteq X$, we have $f(\overline{A})\subset\overline{f(A)}$. 
4. for all $B\subset Y$, we have $\overline{f^{-1}(B)}\subset f^{-1}(\overline{B})$. 
5. $f^{-1}(V)$ is closed for all $V\subset Y$ closed. 

*Proof*:left as exercise.

**Definition**: Let $C\subset 2^{X}$, we call $C$ a **cover** if $X=\bigcup_{c\in C}c$. In particular, if $C$ is finite and consists of only open sets, we say it is 有限开覆盖. 

**Theorem**: let $\{ A_{1},\dots, A_{n} \}$ be a finite closed covering. If $f:X\rightarrow Y$, is continuous on all restrictions to $A_{i}$, then $f$ is continuous. 

*Proof*: we only need to check $f^{-1}(V)$ is cloed for all $V\subset Y$ closed. Suppose $B\subset Y$ closed, then $f^{-1}(B)=\bigcup_{i=1}^{n}f_{A_{i}}^{-1}(B)$, note that $f^{-1}_{A_{i}}(B)=f^{-1}(B)\cap A_{i}$, we know that $f^{-1}(B)$ is closed. 

# 乘积空间
$X,Y$ be two topology, then $X\times Y=\{ (x,y):x \in X,\,y \in Y \}$ with open set spanned by $B=\tau_{X}\times \tau_{Y}$ (one can varify this using $(U_{1}\times U_{2})\cap(V_{1}\times V_{2})=(U_{1}\cap U_{2})\times(V_{1}\cap V_{2})$). The finite case is fine, but in infinite case, there will be box topology $B_{1}=\left\{  \prod_{i\in \Lambda} U_{i}: U_{i}\in \tau_{i},\,\forall i\in\Lambda \right\}$ and $B_{2}=\left\{  \prod_{\in \Lambda}U_{i}: U_{i}\in \tau_{i},\,\forall i \in A \text{ with only finitly many} U_{i}\neq X_{i} \right\}$. 

**Proposition**: Let $X,Y,Z$ be topological space, $f:Z\rightarrow X\times Y$ then $f$ continuous <==> $f|_{X}$ and $f|_{Y}$ are both continuous. 

*Proof*: 
==> is straight forward, we will focous on <== . In fact, we only need to consider the open set $U\times V$, then $f^{-1}(U\times V)=f^{-1}(U\times Y)\cap f^{-1}(X\times V)$ is open. 

**Peano曲线**: $\mathbb{R}\simeq \mathbb{R}^{2}$, **Hilbrt曲线** 

# Some kinds of topological space
**Definition**: Let $X$ be a topological space
1. $X$ is $T_{1}$if $\forall x\neq y \in X$, there is neighbor $O_{x},O_{y}$ such that $x\not\in O_{y}$ and $y\not\in O_{x}$. 
2. $X$ is **Hausdoff** if $\forall x\neq y\in X$, there is neighbor $O_{x},O_{y}$ such that $O_{x}\cap O_{y}=\varnothing$. 
3. $X$ is $T_{3}$ or **regular** if for all $x$ and a closed set $A$ not containing $x$, there is a $O_{x}$ such that $O_{x}\cap A=\varnothing$.
4. $X$ is $T_{4}$ or **normal** if for all nonintersected closed set $A_{1},A_{2}$, there are two open set $B_{1},B_{2}$ containing then and $B_{1}\cap B_{2}=\varnothing$. 

**Proposition**: $X$ is $T_{1}$ <==> $\{ x \}$ is closed for all $x \in X$. 

*Proof*: For all $y\neq x$, and $y \in X$, there is a neighbor $O_{y}\subset X$ such that $x\not\in O_{y}$, then consider $\bigcup_{y\neq x}O_{y}$ contains every element of $X$ except $x$, and it is in fact open, so $\{ x \}$ is closed. 

**Proposition**: In a Hausdoff space $X$, a sequence will not converge to two point. (if not, all $x_{n}$ will be in neighbor of both $x$ and $y$) 

反例: $X=(\mathbb{R} / \{ 0 \})\cup \{ z_{1},z_{2} \}$, $p_{i}=\begin{cases}x\ &\text{ if } x\neq0\\ z_{i}\ &\text{ if }x=0\end{cases}$, choose topology making $p_{1},p_{2}$ continuous, then $X$ is neither $T_{1}$ nor $T_{2}$. 

**Proposition**: $X$ is $T_{3}$ if and only if $\forall x \in X$ and open neighbor $W$, there is another open neighbor $U$ s.t. $x \in U\subset \overline{U}\subset W$. $X$ is $T_{4}$ if and only if for all closed set $A$ and a open neighbor $W$, there is a open set $U$, s.t. $A\subset U\subset \overline{U}\subset W$. 

*Proof*: \==>, take $A$ a point or a set, we have $A\subset U\subset \overline{U}\subset W$, take $W=B^{c}$ for $B$ closed and disjoint with $A$, so $B$ is contained in $V=(\overline{U})^{c}$, so $X$ is $T_{3}$ or $T_{4}$. As to <== , take $B=W^{c}$, then $B$ range over all closed set disjoint $A$, and take $U,V$ be neighbor of $A,B$, then $U\subset V^{c}$, so $A\subset U\subset \overline{U}\subset V^{c}\subset B^{c}=W$. 

In fact, for all nonnormal space, we are able to "normalize" it by adding a point to the space. 

**Proposition**: the product of Hausdoff space is again hausdoff.

**Definition**: $(X,T)$ is $C_{1}$ if $\forall x \in X$, there is countable 邻域基, i.e. $\forall x \in X$, therer is a countable many open neighbor $U_{i}$ s.t. for all open neighbor $V$ of $x$, there is a $i\in \mathbb{N}$ s.t. $x \in U_{i}\subset V$. 

**Definition**: $X$ is $C_{2}$ if it has countable topological basis; and $X$ is **serperable** if it has a 可数稠密子集. 

We have $C_{2}$ \==> $C_{1}$ + serperable. 

**Theorem**:(lindelof) $T_{3}+C_{2} \implies T_{4}$. 

We focous on 度量空间, in fact, $(X,d)$ satisfies $T_{i}$, i=1,2,3,4, and a serperable measurable space is $C_{2}$. 
	
**Urysohn's lemma**: If $X$ is normal, $A,B\subset X$ closed, $A\cap B=\varnothing$ then there is a $f:X\rightarrow[0,1]$ s.t. $f(A)=0$ and $f(B)=1$. 

*Proof*: If $X$ is measurable space, $f(x):=\frac{d(x,A)}{d(x,A)+d(x,B)}$ then $f$ is continuous, so $f$ satisfies the condition. Now take $\mathbb{Q}_{0}=[0,1]\cap \mathbb{Q}$. $\mathbb{Q}_{0}$ countable, let it be $\{ r_{1}=1,r_{2}=0,\dots,r_{n},\dots \}$. For each $i$, we construct open set $U_{i}$ such that if $r_{n}<r_{m}$ then $\overline{U_{n}}\subset \overline{U_{m}}$, and $A\subset U_{n}\subset B^{c}$. We construct using induction, $U_{1}=B^{c}$, then suppose $U_{1},\dots ,U_{n}$ is ready, take $r_{m}=\max\{ r_{l}:l\leq n,\,r_{l}<r_{n+1} \}$ and $r_{k}=\min\{ r_{l}:l\leq n,\,r_{l}>r_{n+1} \}$, both are nonempty, and are disjoint, so by $X$ normal, there is a openset $\overline{U_{m}}\subset U_{n+1}\subset \overline{U_{n+1}}\subset U_{n+1}^{c}\subset U_{k}$. Now define $f:X\rightarrow \mathbb{E}^{1}$ as $f(x)=\sup\{ 0,r_{n}\in \mathbb{Q}_{0}:x \not\in U_{n} \}=\inf\{ 1,r_{n}\in \mathbb{Q}_{0}: x \in U_{n} \}$. To check $f$ continuous, we randomly choose $(a,b)\in \mathbb{E}^{1}$, and a $x \in f^{-1}(a,b)$, we need to check that there is a $U_{x}\subset f^{-1}(a,b)$. 
1. If $f(x)\in(0,1)$, then there is a $\mathbb{Q}_{0}$ such that $a<r_{m}<f(x)<r_{k}$, for all $y \in x \backslash \overline{r_{m}}$, as there is a rational number in $(r_{m},f(x))$, then there is a $x \in X \backslash \overline{U_{m}}$, $x \in U_{k}$. Now let $U=(X \backslash \overline{U_{m}})\cap U_{k}$, then $U\subset f^{-1}(a,b)$. 
2. If $f(x)=0$, take $r_{k}\in \mathbb{Q}_{0}$, $0<r_{k}<b$, then $x \in U_{k}\subset f^{-1}(a,b)$.
3. $f(x)=1$, take $r_{m}\in \mathbb{Q}_{0}$ s.t. $a<r_{k}<1$, then $x \in(\overline{U_{k}})^{c}\subset f^{-1}(a,b)$. Hence $f$ satisfies.

**Tietze's extension theorem**: Continuous function on a closed set of a normal space can be extended continuously to the whole space.

*Proof*: suppose $E\subset X$ closed, $f:E\rightarrow \mathbb{E}^{1}$, continuous.
Suppose $f(E)\subset[-1,1]$. Let $A_{1}=f^{-1}\left( \left[ -1,-\frac{1}{3} \right] \right)$, $B_{1}=f^{-1}\left( \left[ \frac{1}{3}, 1 \right] \right)$ then $A_{1}$ $B_{1}$ are closed and disjoint, use the Urysohn's lemma above, there is a $\phi_{1}:X\rightarrow \left[ -\frac{1}{3}, \frac{1}{3} \right]$ s.t. $\phi_{1}(A_{1})=-\frac{1}{3}$ $\phi(B_{1})=\frac{1}{3}$ take $f_{1}=f-\phi_{1}$, then $f_{1}(E)\subset\left[ -\frac{2}{3}, \frac{2}{3} \right]$, then construct $\phi_{2}:X\rightarrow\left[ -\frac{2}{9}, \frac{2}{9} \right]$, and $f_{2}=f_{1}-\phi_{2}$, $f_2(E)\subset\left[ -\frac{4}{9}, \frac{4}{9} \right]$ and using induction, we get a sequence of $\{ \phi_{n}:X\rightarrow \mathbb{E}^{1} \}$, we have $\phi_{n}\in\left[ -\frac{2^{n-1}}{3^{n}}, \frac{2^{n-1}}{3^{n}} \right]$, and $|f(x)-\sum_{i}\phi_{i}|\leq\left( \frac{2}{3} \right)^{n}$. On know immediately that $\sum \phi_{n}$ converges, then $\tilde{f}=\sum \phi_{n}\in[-1,1]$. We know that $f$ and $\tilde{f}$ coinside on $E$. Moreover, with $g=\frac{2}{\pi}\arctan(f)$, we are able to change all $f$ into the form we discussed. 

**Urysohn's measure theorem**: $C_{2}+T_{4}+T_{2}\implies measurable$. 

# compactness
**Heine-Borel theorem**: On space $[0,1]$, all open cover is finite covered. 

*Proof*: suppose $\mathcal{C}$ is an open cover of $[0,1]$, let $F=\{ a\in[0,1]:[0,a] \text{ have a finite subcover} \}$. One immediately know that $F$ is nonempty, and if $a\in F$, then $\forall b\in [0,a]$, $b\in F$. 从而 $F$ 是区间, 设右端点为 $A$, consider the open set that cover $A$, as it is open, we may assume that $\left( A-\frac{\epsilon}{2} , A+\frac{\epsilon}{2}\right) \in U$, so if $A\neq1$, we are able to construct a larger element in $F$, a contradicition, hence $1 \in F$. 

**Definition**: A topological space is called **compact** if all open cover of $X$ have a finite subcover. for example, $E \in \mathbb{E}^{1}$ is compact if and only if $E$ is closed and finite.

In fact, compact space is not necessarily closed, and its closure is not necessarily compact. But if $X$ is hausdoff and compact, then $X$ is closed. 

**Proposition**: $A$ compact, $B$ hausdoff, and $f:A\rightarrow B$ bijective, then $f$ 同胚. (just check $f$ send closed set to closed set)

**Proposition**: In hausdoff space, two compact set have disjoint neighbor.

**Bolzano-Weierstrass property**: 紧致空间的无穷子集必有聚点. 

**Definition**: $X$ is called **limit point compact** (聚点紧致) if all infinite subset have a limit point. $X$ is **sequentially compact** if all sequence of $X$ have a converges subsequence. 

**Proposition**: $C_{1}$ + compact ==> sequentially comapct.

**Theorem**: measure space is comapct if and only if it is sequentially comapct.

*Proof*: 
"==>", simple, just use Bolzano-Weierstrass property, we know that there is a point $x_{0}$, and take $x_{k}=A\cap B\left( \frac{x_{0},1}{k} \right)$. 
On the other hand, we claim that $\exists \delta>0$, s.t. $\forall x \in X$, $\exists U\in A$, where $A$ is an open cover of $X$. If not, then there is a $x_{n}$ such that $B\left( x_{n}, \frac{1}{n} \right)\backslash U\neq \varnothing$ for all $U$, then there is a converges subsequence, suppose the limit is $x_{*}$, then consider $x \in U$, so $B(x_{*},\delta)\subset U$ for some $\delta$, a contradicition. With this claim, we are able to restrict $A$ to the case of $B(x,\delta)$, in this case, it is vary straight forward, as all sequence all have a converges subsequence, so there will be a contradicition. 

**Proposition**: $X\times Y$ comapct if and only if $X,Y$ both comapct. 

*Proof*: one direction is easy, on the other hand, we need the following lemma:

**Lemma**: If $A\subset X$ compact, $W\subset X\times Y$ a neighbor of $A\times \{ y_{0} \}$, then there is a $A\subset U\subset X$ and $y_{0} \in V\subset Y$, s.t. $U\times V\subset W$. 
(Just consider covering $A$ with finite many neighbors $U_{x}$, and each choose a $U_{x}\times V_{x}\subset W$ and combine.)

**Tychonoff Theorem**: let $x_{i}$, $i \in I$, is a set of nonempty comapct space, then $X=\prod_{i \in I}x_{i}$ is also comapct. This theorem is infact equivalent to 选择公理.

# 仿紧空间
**Definition**: topological space $X$ is called **locally comapct** if all $x \in X$ has a compact neighbor. An opencover of $X$ is called locally finite if it is a finite cover when restrict to a neighbor of any $x \in X$. 

**Definition**: $X$ is **paracompact** (仿紧的) if all opencover of $X$ is locally finite. In fact, paracompact + hausdoff ==> regular

# Connectivity
**Definition**: $X$ is called connected if foall $X=A\cup B$, $A\cap \overline{B}$ or $A\cap \overline{B}$ $\neq \varnothing$. 

**Proposition**: The image of connected space is also connected.

*Proof*: In fact, connectivity is equivalent to there is no nontrival set that is open and closed. So if $f(X)$ is not connected, then there is a set $A\subset f(X)$ that is both open and closed. So $f^{-1}(A)$ is both open and closed, a contradicition. 

**Lemma**: $X_{0}$ is a subset of $X$ that is both open and closed, and $A$ is a connected subset of $X$, then $A\subset X_{0}$ or $A\cap X_{0}=\varnothing$. 

**Proposition**: If $X$ has a 稠密 connected subset $A$, then $X$ is connected. 

*Proof*: If $X_{0}$ is a subset of $X$ that is both open and closed, then the above lemma tells us that $X_{0}\cap A=\varnothing$ or $A\subset X_{0}$, so $X_{0}$ is either $\varnothing$ or $X$. 

**Corollary**: $Z$ a connected subset, $Z\subset Y\subset \overline{Z}$, then $Y$ is connected.

**Proposition**: Let $C$ be a covering of $X$ whose components are all connected, $A$ is a connected subspace of $X$ that has nonempty intersection with all parts of $C$, then $X$ is connected. 

*Proof*: Take $X_{0}$ to be a both open and closed subset of $X$. If $X_{0}\neq \varnothing$, then there is a $U \in C$ that have intersection with $X_{0}$, as $X_{0}$ is both open and closed, so $U\subset X_{0}$, hence $A\cap X_{0}\neq \varnothing$, so $A\subset X_{0}$. Now with for all $V \in C$, $V\subset X_{0}$, therefore $X=X_{0}$. 

**Proposition**: $X,Y$ connected $\Longleftrightarrow$ $X\times Y$ connected. 

*Proof*: Just take $A=X\times \{ y_{0} \}$, and $C=\{ \{ x \}\times Y:x \in X \}$. And the other direction is easy. 

**Definition**: A subspace of $X$ is a called 联通分支 of $X$ if it is a maximal connected subset of $X$. 

**Proposition**: In a topological space $X$, every connected subset $A$ is contained in a 联通分支.

*Proof*: Let $\mathcal{F}:=\{ F\subset X:F \text{ connected and have intersection with } A\}$. $X_{0}=\bigcup_{F \in \mathcal{F}}F$, then $A \in \mathcal{F}$, so $A\subset X_{0}$. With proposition above, one know that $X_{0}$ is connected. One immediately check that $X_{0}$ is maximal.

**Definition**: $X$ is called **path connected (道路连通)** if forall $x_{0},x_{1}\in X$, there is a path $x_{0}\rightarrow x_{1}$, i.e. there is a continuous map $f:[0,1]\rightarrow X$ with $f(0)=x_{0}$, $f(1)=x_{1}$. One immediately notice that path connected implies connected.

**Proposition**: In Euclidian space, all connected space is path connected. 

**Definition**: $X$ is called **locally connected** if $\forall x \in X$ and a neighbor $U$ there is a connected neighbor of $V$ contained in $U$. 

**Proposition**: the 联通分支 of locally connected space is open. 

**Definition**: $X$ is called **locally path connected** if $X$ is path connected locally i.e. for all $x \in X$ and neighbor $U$, there is a neighbor $V\subset U$ that is path connected. 

# quotient
**Definition**: Let $X$ be a topological space, $P\subset2^{X}$, nonempty, then $P$ is a **Partition** iff:
1. $A\cap B=\varnothing$ for $A,B\in P$.
2. $X=\bigcup_{A \in P}A$. 

Now we give $P$ a topology. Consider $\pi :X\rightarrow P$, let the topology be "biggest", i.e. $Q \in2^{P}$ is open iff $\bigcup_{p \in Q}p$ is open in $X$. This will be the quotient of topology. This can also be written as a universal property:

**Definition**: Let $X$ be a topological space, then the quotient is a space $Y$ with map $\pi :X\rightarrow Y$, such that forall $Z$ and $f:Y\rightarrow Z$, $f$ continuous $\Longleftrightarrow$ $f\circ\pi$ is continuous. 

On the other hand, a partition also gives a equivalent relation: $x\sim y$ iff $\exists U \in P$ s.t. $x,y\in U$. An the quotient can also be seen as $X / \sim$. 

**Proposition**: the composition of quotient is another quotient. 

*Proof*: Clear, just use the universal property of quotient.

a map $X\rightarrow Y$ is **open(closed)** if it send open(closed) set to open(closed) set.

**Proposition**: If continuous surjective morphism $f$ is open(closed) morphism, then $f$ is a quotient map. 

**Theorem**: (Whitehead)
let $P:X\rightarrow Y$ be a quotient morphism, $Z$ locally compact hausdoff space, then $P\times id:X\times Z\rightarrow Y\times Z$ is a quotient map. 

*Proof*: $f:P\times id$ is obviously surjective and continuous. We ten proof that forall $W \subset Y\times Z$ if $f^{-1}(W)\subset X\times Z$ is open then $W$ is open. take $(y_{0},z)\in W$, we proof that it is 内点. In fact, take $x_{0}\in f^{-1}(y_{0})$, then there is a compact subset $B\subset Z$ containing $z$. 

## Ther product of quotient map:
**Whitehead**: $p:X\rightarrow Y$, $Z$ locally comapct, then $p\times\mathbb{1}:X\times Z\rightarrow Y\times Z$ is quotient map as well.

# The classification of 曲面
**Definition**: Hausdorff space is called a $n$ dimensional manifold (流形) if $\forall x \in X$, there is a neighbor that is homeomorphic to $\mathbb{E}^{n}$ or $\mathbb{E}_{+}^{n}=\{ (x_{1}, \cdots, x_{n}):x_{n}\geq0 \}$. We say $X$ is a $n$-manifold in short.

$x \in X$ is called 内点 iff $x$ has a neighbor homeomorphic to $\mathbb{E}^{n}$. otherwise $x$ is 边界点 ($x$ should also have $\phi(x)=0$). 

- we need to show $n\neq m$ then $\mathbb{E}^{n} \not\simeq E^{m}$. 
- **We usually just consider comapct manifold or the inside of it**
- **If $X$ is a $n$-manifold, then $\partial X\neq \varnothing$ and is $n-1$-manifold**

二维流形称为曲面. $S^{2},\ \mathbb{D}^{2},\ \mathbb{E},\ T^{2}$, Mobius 带, klein瓶. 事实上, 正6边形对边同向粘合也是一个环面, 而正八边形,正10边形的对边粘合会形成一个双环面. 

**Theorem**: 任何闭曲面(紧致. 无边界) 都同胚于$S^{2}$, $nT^{2}$, or $mP^{2}$ 这些曲面中任何两个都不同胚. 

**Rado**: 任何闭曲面都从某个多边形两两配对来粘合边界得到.

---
拓扑学: 拓扑空间的分类
1. 无重复的列出所有情形.
2. 任何满足条件的空间, 要有办法确定是哪一个.

判断空间是否同胚: 不变量
1. 强大: 一定能判断出来
2. 好算

**Theorem**: 不存在算法, 判断任何两个有限表现群是否同构.

**Definition**: 同伦等价意义不变, $f,g:X\rightarrow Y$ 称为同伦(homotopic)的, 若存在 $H:X\times[0,1]\rightarrow Y$ s.t. $H(x,0)=f(x),\ H(x,1)=g(x)$. 记为 $f\simeq g$, $H$ 为 $f,g$ 的同伦.

**Proposition**: homotopic is a equivalent relation in $\mathfrak{C}(X,Y)=\{ f:X\rightarrow Y|f\ continuous \}$. 

若 $f$ 同伦于常值映射, 则称 $f$ 是零伦的. 若 $Y \subseteq \mathbb{E}^{n}$ 凸, 则 $\forall f:X\rightarrow Y$ 零伦. 

Let $A\subseteq X$, $f,g:X\rightarrow Y$ s.t. $f|_{A}=g|_{A}$, if there is $f$ to $g$ a homotopic $H$ s.t. $H(a,t)=f(a)=g(a)$, $\forall a \in A$, and $t \in[0,1]$, then we say that $f,g$ are relative homotopic to $A$, or $f\simeq_{H}g$ rel $A$. 

Now take $x_{o}\in X$, consider $\mathcal{L}=\{ \alpha:[0,1]\rightarrow X: \alpha(0)=\alpha(1)=x_{0} \}$, and $\pi(X)=\mathcal{L} / \sim$, one easily check that $\pi$ is well defined. We claime that there is a natural group structure on $\pi(X)$, the addition is obviously the composition of rutine. And the $1_{\pi}$ is the constant map, and inverse is obvious. Now consider $\pi(X,x_{0})$ as a functor $Top\rightarrow Group$. 

**Theorem**: let $f:X\rightarrow Y$ be a 同胚, then the induced map $\pi(X,x_{0})\rightarrow \pi(Y,f(x_{0}))$ is isomorphism.

When $X$ is path connected, $\pi(X,x)$ does not depend on $x$, so we will write $\pi(X)$ in short. 

How to compute $\pi$? **van-kampen** theorem

**Theorem**: $\omega_{n}:[0,1]\rightarrow S^{1}$, $\omega_{n}(t)=e^{2\pi nti}$, then $\Phi:\mathbb{Z}\rightarrow \pi_{1}(S^{1},1)$ $\Phi(n)=\langle \omega_{n} \rangle$ is an isomorphism. 

*Proof*: Consider $Y \stackrel{p}{\longrightarrow}X$, $A \stackrel{f}{\longrightarrow}X$ continuous, if there is a $\tilde{f}:A\rightarrow Y$, s.t. $f=p\circ \tilde{f}$, then we call $\tilde{f}$ be the **lift** of $f$. 
1. Given an $\alpha:[0,1]\rightarrow S^{1}$, suppose $\alpha(0)=x_{0} \in S^{1}$, then forall $\tilde{x_{0}} \in p^{-1}(x_{0})$, there is a unique lift $\tilde{\alpha}: [0,1]\rightarrow \mathbb{E}^{1}$, s.t. $\tilde{\alpha}(0)=\tilde{x_{0}}$. 
2. forall path based on $x_{0}$ homotopic $f_{t}:[0,1]\rightarrow S^{1}$ and $\tilde{x_{0}} \in p^{-1}(x_{0})$, then there is a unique homotopic based on $\tilde{x_{0}}$ $\tilde{f_{t}}:[0,1]\rightarrow \mathbb{E}^{1}$, s.t. $f_{t}=p\circ f_{t}$. 
3. Consider the lift $\tilde{\omega_{n}}:[0,1]\rightarrow \mathbb{E}^{1}$, sending $\tilde{\omega_{n}}(t)=nt$ coinside with $\tilde{f}:[0,1]\rightarrow \mathbb{E}^{1}$. So we are able to check $\Phi$ is a bijective homomorphism.

**Lemma**: Given $F:X\times[0,1]\rightarrow S^{1}$ and $\tilde{F_{0}}:X\rightarrow \mathbb{E}^{1}$ if $F(X,0)=p\circ\tilde{F_{0}}(X)$, then for all $x \in X$, there exists a unique morphism $\tilde{F}:X\times[0,1]\rightarrow \mathbb{E}^{1}$ s.t. $F=p\circ \tilde{F}$, whose restriction to $X\times \{ 0 \}$ is $\tilde{F_{0}}$. 

**Proposition**: Let $X=U\cup V$, $U,V$ open and connected, if $U\cap V$ is path connected, then $\pi(X)\simeq \{ 1 \}$. 

**Theorem**: $X,Y$ path connected topological space, then $\pi_{1}(X\times Y)\simeq \pi_{1}(X)\times \pi_{1}(Y)$. 

*Proof*: Consider the natural maping $\langle r \rangle\mapsto(\langle p_{1}\circ r \rangle, \langle p_{2}\circ r \rangle)$, its obviously a surjective homomorphism. Now we check that it is injective: For two $\langle r_{1} \rangle$ and $\langle r_{2} \rangle$ s.t. they all map to $(1,1)$, then there is $F(s,t)$ and $G(s,t)$ sending $p_{1}\circ r_{1}\rightarrow p_{1}\circ r_{2}$ and $p_{2}\circ r_{1}\rightarrow p_{2}\circ r_{2}$, and combine it to be $H(s,t)=(F(s,t),G(s,t))$, is a homotopic of $r_{1}\rightarrow r_{2}$. 

In fact, for $f:X\rightarrow Y$ and $g:X\rightarrow Y$, if $f\simeq g$, then it induced homomorphism $f_{*}:\pi_{1}(X,x_{0})\rightarrow \pi_{2}(Y,y_{0})$, and $g_{*}:\pi_{1}(X,x_{0})\rightarrow \pi_{1}(Y,y_{0})$, and $\omega_{\#}:\pi_{1}(Y,y_{0})\rightarrow \pi_{1}(Y,y_{1})$, sending $\langle \alpha \rangle\mapsto \langle \omega\alpha \overline{\omega} \rangle$, there $\omega=H(x_{0},\cdot)$. Then we have $g_{*}=\omega_{\#}\circ f_{*}$. 

**Definition**: $X,Y$ topological space, $f:X\rightarrow Y$, $g:Y\rightarrow X$, s.t. $f\circ g\simeq \mathbb{1}_{Y}$, $g\circ f\simeq \mathbb{1}_{X}$, then we say that $X,Y$ are **homotopy equivalent**. This is in fact an equivalence relation. It is a weaker equivalence relation to homeomorphic.

**Definition**: If $X$ is homotopy equivalent to a single point, we say that $X$ is 可缩的.