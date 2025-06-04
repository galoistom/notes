[[Basic Definitions of representation]]
# The  orthogonality relation

For two class function $f_1,f_2$ over $G$, define $<f_1,f_2>=\sum\limits_{s \in G} f_1(s) \overline{f_{2}(s)}$

>[!note] row relation 1
>Let $(V_1,\rho_1),(V_2,\rho_2)$ be two irreducible representation of a finite group $G$, then
>$$\frac{1}{Card(G)}\sum_{g \in G} \chi_1(g) \overline{\chi_2(g)}=\begin{cases} &0 \qquad V_1 \not\simeq V_2 \\ &1 \qquad V_1 \simeq V_2 \end{cases}$$

**Proof:**
	We will use the two following facts:
	$$\chi_{V_1} \cdot \chi_{V_2} = \chi_{V_1 \otimes V_2},\, \overline{\chi_{V}}=\chi_{V^*},V_1 \otimes V_2^* \simeq Hom(V_1,V_2)$$
	Thus, $\frac{1}{Card(G)}\sum\limits_{g \in G} \chi_1(g) \overline{\chi_2(g)}=\frac{1}{Card(G)}\sum\limits_{g \in G} \chi_{Hom(V_1,V_2)}(g)$, multiply it by $\chi_{Hom(V_1,V_2)}(t)$, we gathered that either  $\chi_{Hom(V_1,V_2)}=1$ or $\chi_{Hom(V_1,V_2)}=0$ . #
	Another proof is using the [[Schur's lemma]], it shows that $Hom(V_1,V_2)$ is either isomorphic to the trivial representation space or 0, and the former case occurs only when $V_1 \simeq V_2$.

**Remark:** Note that the vector space of class function on $G$ is obviously finite dimensional, and the above relation shows that all the irreducible characters are linearly independent, hence there are only finitely many irreducible representation.
 
>[!note] row relation 2
>Let $\chi_1,\dots,\chi_k$ be all the characters of irreducible representation of group $G$ , and let $c(s)$ denote the number of elements of the conjugacy classes consisting $s$, then:
>$$\sum_{i=1}^{k} \chi_i(s)\overline{\chi_i(t)}=\begin{cases}
>0 \qquad &t \not\in C(s)\\ 
>\frac{g}{c(s)} \qquad &t \in C(s)
>\end{cases}$$

**Proof:**
	 We will use the fact that every class function  can be written as a linear combination of $\chi_1, \dots, \chi_k$ (we will proof it later). Let $f_s(t)=\begin{cases}&0 \qquad t \not\in C(s)\\&1 \qquad t\in C(s)\end{cases}$ , and let $f_s=\sum\limits_{i=1}^{k} \lambda_i\chi_i$ ,then compute $<f_s,\chi_i>$, then we have $\lambda_i=\frac{g}{c(G)} \overline{\chi_i(s)}$ , now consider $f_s(t)$ , then we are done. #

# They form a basis of the vector of the class functions over $G$

>[!note] Forming basis
>For every $f$ a class function over $G$, there exists $\lambda_1,\dots,\lambda_k$ such that $f=\sum\limits_{i=1}^{k} \lambda_i\chi_i$.

**Proof:**
	Assume the contrary, there exists a $f \neq 0$ such that $\langle f,\chi_i \rangle=0$ for all $i = 1,\dots,k$ .
	Define $\rho_f = \sum\limits_{s \in G} f(s)\rho_s$ for all linear representation $(V,\rho)$ , then $$\rho_t\rho_f\rho_t^{-1}=\sum_{s \in G} f(s)\rho_t\rho_s\rho_t^{-1}=\sum_{s \in G} f(tst^{-1})\rho_{tst^{-1}}=\rho_f$$
	letting $(V,\rho)$ be irreducible, from [[Schur's lemma]] we know that $\rho_f=\lambda \cdot id$ , with $\lambda=<f,\chi_i>=0$ , thus $\rho_f=0$  for all $\rho$ irreducible. Hence $f=0$ , contracting the assumption.# 
