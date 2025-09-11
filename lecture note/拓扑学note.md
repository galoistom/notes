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

对于 $X$ 的子集 $A$, 若 $X=\overline{A}$, 则称 $A$ 在 $X$ 中稠密. 若 $X$ 存在可数的稠密集, 则称其为可分空间. 对于这样的一个$X$, 若有一族开集 $\beta$ s.t. $X$ 中任一开集都是 $\beta$ 中一些开集的并, 则称 $\beta$ 生成 $\tau$