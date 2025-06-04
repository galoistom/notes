[[Basic Definitions of representation]]

>[!note] Schur's lemma
>Let  $A$ be an algebra and $(V_1,\rho_1),(V_2,\rho_2)$ be two representations, $\phi:V_1 \rightarrow V_2$ are none zero homomorphism of representation, then:
>1. if $V_1$ is irreducible, then $\phi$ is injective.
>2. if $V_2$ is irreducible, then $\phi$ is surjective.
>In particular, if both are irreducible, then $\phi$ is isomorphism.

**Proof**:
	1. Note that the kernel of $\phi$ is a subrepresentation of $V_1$,  and the fact that $\phi \neq 0$ , thus the kernel is $0$, which implies that $\phi$ is injective.
	2. The proof is quiet the same, the image of $\phi$ is a subrepersentation of $V_2$, the same argument implies that the image is $V_2$, hence $\phi$ is surjective.#


>[!note] Schur's lemma (the case of finite group)
>Let $G$ be a finite group, $(V_1,\rho^1),(V_2,\rho^2)$ be two irreducible representation of $G$, assume that $f$ is a linear mapping $V_2 \rightarrow V_1$ satisfying: $\rho^1_s \circ f=f \circ \rho^2_s$, for all $s \in G$, then:
>1. If $\rho^1_s \not\simeq \rho^2$, then $f=0$.
>2. If $V_1 = V_2,\rho^1 \simeq \rho^2$, then $f=\lambda \cdot id$

**Proof:**
	1. By the previous version of the lemma, we know that $f$ must either be an isomorphism or 0, thus the first case is solved.
	2. Take $\lambda$ an eigenvalue of $f$, take $f'=f-\lambda \cdot id$ , then $Ker(f') \neq 0$ ,  whence $f'$ is not an isomorphism, the same argument in 1. shows that $f'=0$ . #

There is alse a module version of the lemma:

>[!note] Schur's Lemma (module version)
>Let $A$ be a k-algebra. For any simple A-module $S$ the k-algebra $End_A(S)$ is a division algebra. For any two nonisomorphic simple A-module S,T we have $Hom_A(S,T)=\{0\}$.

**Proof**:
	Let $S,T$ be simple A-modules, and suppose there is a nonzero A-homomorphism $\phi:S \rightarrow T$. Then $ker(\phi) \neq S$, hence $ker(\phi)=\{0\}$ because $S$ is simple. Thus $\phi$ is injective. In particular, $im(\phi) \neq \{0\}$. Since $T$ is simple this implies $im(\phi)=T$. Thus $\phi$ is an isomorphism. The result follows.