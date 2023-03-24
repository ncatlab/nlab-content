
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Combinatorial category
* table of contents
{: toc}

## Definition

A **combinatorial category** &lbrack;[Pultr (1973, Def. 1.7)](#Pultr73)&rbrack; $C$ is a [[locally finite category]] satisfying the _unnatural isomorphism property_:

For all objects $A, B \in C$, if there is an [[unnatural isomorphism]] $C(-, A) \cong C(-, B)$, then $A \cong B$. Equivalently if $\left|C(X, A)\right| = \left|C(X, B)\right|$ for all objects $X \in C$.

## Properties

\begin{proposition}
Let $C$ be a combinatorial category and let $A, B, X \in \C$. If $A \times X \cong B \times X$ and $X$ is [[weakly terminal]], then $A \cong B$.
\end{proposition}

\begin{proof}
For all $Y \in C$, we have
\begin{equation}
\left|C(Y, A)\right| \times \left|\C(Y, X)\right| = \left|C(Y, A \times X)\right| = \left|C(Y, B \times X)\right| = \left|C(Y, B)\right| \times \left|C(Y, X)\right|
\end{equation}
Hence we may divide both sides by $\left|C(Y, X)\right|$ (which is nonzero since $X$ is weakly terminal) and so $\left|C(Y, A)\right| = \left|C(Y, B)\right|$ for all $Y \in \C$, from which we have $A \cong B$.
\end{proof}

## Related concepts

* [[finite category]]

* *not* related is the notion of *[[combinatorial model category]]*

## References

* {#Pultr73} A. Pultr, *Isomorphism types of objects in categories determined by numbers of morphisms*, Acta Scientiarum Mathematicarum **35** (1973) 155-160 &lbrack;[pdf](http://acta.bibl.u-szeged.hu/14440/1/math_035_155-160.pdf)&rbrack;

[[!redirects combinatorial categories]]
