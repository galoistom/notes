# The theorem

>[!note] Burnside's theorem
>Let $G$ be a finite group with order $p^m q^n$, $p,q$ prime, then $G$ is a sovlvable.

Note that there is only one element in the conjugarcy class containing ${e}$, henece there must be another conjugarcy class have $q^k$ elements, so we have the stronger version of the theorem.

>[!note] Burnside's theorem (stronger version)
>Let $G$ be a finite simple group with a conjugarcy class $C$ that have $q^K$ elements, where $q$ is prime, then $G$ is cyslic.

# So, how do we get started?

1. It is normal to see a group as a set of symmetric action on a abgebric structrue, so we want to find the structure we need.
2. From the theorem, we know that it is important for the structure to have something to do with the conjugarcy classes, which lead us to consider $K[G]$, because conjugarcy classes forms a basis of the center of the group ring. And an algebric structure is acted upon by a ring is more or less related with modules of $K[G]$. Now we have a bold assumption: simply let $K$ be a field (or even better $\mathbb{C}$), and $K[G]$ acts on some $K-$ vector space, and getting our proof using representation theory (cf.[[Basic Definitions of representation]])

# Proof:

1. We want to show that there are some property hiding behind the requirements, but we know little more than nothing about the structure of the representations of $G$ themselves, but we do know alot about the characters of the representations (cf.[[Property of the character table]]), what's more, the characters preserves the structure of conjugarcy classes, so the characters might be a breaking point of the proof.
2. First take an irreducible representation $(V,\rho)$ with character $\chi$, then consider the homomorphism $\overline{\rho}:cent.\mathbb{Z}[G] \rightarrow \mathbb{C}$ induced from $\rho:\mathbb{C} \rightarrow V$, as the center of the group ring act as scalar pructduct. As $cent.\mathbb{C}$ is finitly generated $\mathbb{Z}-module$, the image of $\sum\limits_{c \in C} c$ is an algebric integer, hence $\frac{|C|\chi(c)}{\chi(1)}$ is an algebric integer. Let $\chi(1)$ be relativily prime to $q$, then we have $s|C|+t\chi(1)=1$, with $s,t \in \mathbb{Z}$, which leads to the fact that $\frac{\chi(c)}{\chi(1)}=s\cdot \frac{|C|\chi(c)}{\chi(1)}+t\chi(c)$, is an algebric integer. Meanwhile, $\chi(c)$ is the sum of $\chi(1)$ roots of unity, hence all the eigenvalue of $\rho_c$ is the same, i.e.$\rho_c=\lambda \cdot id$, with the fact that $G$ is simple, $\rho$ is thus injective, whence $c\in Z(G)$, which is equivalent to saying that $G$ is cyclic.#