# Definition

>[!note] Projective module and injective module
>If P is a projective, then for any $N \stackrel{f}{\longrightarrow} M$ surjective and a morphism $P \stackrel{g}{\longrightarrow} M$, then there exists a morphism $P \stackrel{h}{\longrightarrow} N$ such that $fh=g$. Reversing all the arrows, we get the definition of injective module.

Another expression of the definition is that there exists a $h$ such that the following diagram commute:
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
&N \arrow[r,"f"] &M \arrow[r] &0\\
&p \arrow[u,"\exists h"] \arrow[ur,"g"]
\end{tikzcd}
\end{document}
```

The point of defining this object is that if $P$ is projective(resp. injective), then $Ext^1(P,\cdot)=0$ (resp.$Ext^1(\cdot,P)=0$) cf.[[First extension group]]

Here is another property of the projective module: it is a direct summand of a free moudule of the ring $R$, i.e. there exists a set $I$ and a module $Q$ such that $\bigoplus\limits_{i \in I} R = P \oplus Q$. In particualr, if $R$ is PID, then every projective moudule of $R$ is a free module.

>[!note] Undecidable problem
>We know that $P$ is projective leads to $Ext^1(P,\cdot)=0$, so dose that mean all $P$ with $Ext^1(P,\cdot)=0$ is projective? In the special case of $R=\mathbb{Z}$, the answer is yes when $P$ is countable, but in general case, it is undecidable.
# Some simple properties:

1. Let $R$ be a ring and $P$ an $R-module$. Then if every Left ideal $I$ the following diagram commute, then $P$ is injective.
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
0 \arrow[r] &I \arrow[r] \arrow[d,swap,"\forall f"] &R \arrow[dl,dashed,"\exists g"]\\
&P
\end{tikzcd}
\end{document}
```
2. $R$ a PID, $I$ a $R-module$, if $rI=I$ for all $r \in R$, then $I$ is injective.
3. $Hom(P,\cdot)$ is an exact functoe(i.e. it keeps the short exact sequence) $\Leftrightarrow$ $P$ is projective 
4. Let $A$ be an artinian algebra, then for every $A-module$ $S$, there exists a indicomposible porjective $A-module$ $P_S$ up to isomorphism such that $S \simeq P_S/rad(P_S)$, which is called the projective envelope of $S$.
5. Let $K$ be a field, and $A$ a finite dimensional $K-algebra$, then every finite dimensional $A-modules$ M has a projective envelope.
6. Let $A$ ba an artinian algebra, then $P$ is a indicomposible $A-module$ if and only if it is isomorphic to $A \cdot e$ for an idempotent element $e \in A$, i.e. $e^2=e$.