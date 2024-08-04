
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

* For all objects $A, B \in C$, if there is an [[unnatural isomorphism]] $C(-, A) \cong C(-, B)$, then $A \cong B$.

Or equivalently

* For all objects $A, B \in C$, if $\left|C(X, A)\right| = \left|C(X, B)\right|$ for all objects $X \in C$ then $A \cong B$.

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

* [[Věra Trnková]], _Unnatural isomorphisms of products in a category_, Category Theory: Applications to Algebra, Logic and Topology Proceedings of the International Conference Held at Gummersbach, July 6–10, 1981. Berlin, Heidelberg: Springer Berlin Heidelberg.

* {#Pultr73} A. Pultr, *Isomorphism types of objects in categories determined by numbers of morphisms*, Acta Scientiarum Mathematicarum **35** (1973) 155-160 &lbrack;[pdf](http://acta.bibl.u-szeged.hu/14440/1/math_035_155-160.pdf)&rbrack;

* Ehsan Momtahan, Afshin Amini, and Babak Amini, _From $Hom (A, X) \cong Hom(B, X)$ to $A \cong B$_, Filomat 32.11 (2018): 4079-4087.

* [[Luca Reggio]], _Polyadic sets and homomorphism counting_, Advances in Mathematics 410 (2022): 108712.

* Shoma Fujino and Makoto Matsumoto, _Lov&aacute;sz's hom-counting theorem by inclusion-exclusion principle_, [arXiv:2206.01994](https://arxiv.org/abs/2206.01994) (2022).

[[!redirects combinatorial categories]]
