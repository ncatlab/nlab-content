
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
#### Higher Category Theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An *$H^*$-category* is a [[horizontal categorification]] of the notion of an [[H-star-algebra | $H^\ast$-algebra]]. 

## Definition

\begin{definition}\label{HStarCategory}
An **$H^*$-category** is a [[Hilb | $\mathrm{Hilb}$]]-category with a [[dagger category | $\dagger$-structure]] that defines an [[antinatural transformation]] from $\operatorname{hom}(x,y)$ to $\operatorname{hom}(y,x)^{\mathrm{conj}}$, where $\operatorname{hom}(y,x)^{\mathrm{conj}}$ is the conjugate [[enriched hom-functor | hom-Hilbert space]].
\end{definition}

([Baez 1997 Def. 2](#Baez97))

The data of such an [[antinatural transformation]] is equivalent to the existence of compatible [[involution | involutory]][[antilinear map | antilinear maps]] between the hom-Hilbert spaces.

\begin{proposition}\label{HStarCategoryEquivalent}
An **$H^*$-category** is equivalently a $\mathrm{Hilb}$-category with antilinear maps $\ast : \operatorname{hom}(x,y) \to \operatorname{hom}(y,x)$ for all objects $x$ and $y$, such that 

* $f^{**} = f$,

* $(g \circ f)^* = f^* \circ g^*$,

* $\langle g \circ f, h \rangle = \langle g, h \circ f^* \rangle$,

* and $\langle g \circ f , h \rangle = \langle f, g^* \circ h\rangle$

for all $f \in \operatorname{hom}(x,y)$, $g \in \operatorname{hom}(y,z)$, and $h \in \operatorname{hom}(x,z)$.
\end{proposition}

([Baez 1997 Prop. 3](#Baez97))

## Related concepts

* [[H-star-algebra]]

* [[2-Hilbert space]]

## References

Introduced in:

* {#Baez97} [[John Baez]], _Higher-dimensional algebra II: 2-Hilbert spaces_, Adv. Math. **127** (1997) 125-189 &lbrack;[arXiv:q-alg/9609018](http://arxiv.org/abs/q-alg/9609018)&rbrack;
