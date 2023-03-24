
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

A **combinatorial category** $C$ is a [[locally finite category]] satisfying the _unnatural isomorphism property_:

For all objects $A, B \in C$, if there is an [[unnatural isomorphism]] $C(-, A) \cong C(-, B)$, then $A \cong B$. Equivalently if $|C(X, A)| = |C(X, B)|$ for all objects $X \in C$.

## Properties

\begin{proposition}
Let $C$ be a combinatorial category and let $A, B, X \in \C$. If $A \times X \cong B \times X$ and $X$ is [[weakly terminal]], then $A \cong B$.
\end{proposition}

\begin{proof}
For all $Y \in C$, we have
\begin{equation}
|C(Y, A)| \times |\C(Y, X)| = |C(Y, A \times X)| = |C(Y, B \times X)| = |C(Y, B)| \times |C(Y, X)|
\end{equation}
Hence we may divide both sides by $|C(Y, X)|$ (which is nonzero since $X$ is weakly terminal) and so $|C(Y, A)| = |C(Y, B)|$ for all $Y \in \C$, from which we have $A \cong B$.
\end{proof}

## Related concepts

* [[finite category]]

## References

* A. Pultr. _Isomorphism types of objects in categories determined by numbers of morphisms_. Acta Scientiarum Mathematicarum 35 (1973): 155-160. [pdf](http://acta.bibl.u-szeged.hu/14440/1/math_035_155-160.pdf)

[[!redirects combinatorial categories]]
