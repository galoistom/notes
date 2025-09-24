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