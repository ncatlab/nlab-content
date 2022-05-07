
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

A [[category]] is __subtractive__
if it is [[pointed]], admits [[finite limits]],
and left punctual [[reflexive relations]] are right punctual.

Here a [[relation]] $r\colon R\to X\times Y$ is left (respectively right)
__punctual__ if $(id_X,0)\colon X\to X\times Y$ (respectively $(0,id_Y)\colon Y\to X\times Y$) factors through $r$.

## Example

A [[variety of algebras]] is a subtractive category
if and only it is a __subtractive variety__ in the sense of Ursini,
meaning its theory contains a binary operation $s$ and constant $0$
such that $s(x,x)=0$ and $s(x,0)=x$.

## Relation to Malcev categories

A [[category]] $C$ with [[finite limits]] is a [[Malcev category]]
if and only if for any object $B$ of $C$
the category $Pt(B)$ is subtractive.

Here $Pt(B)$ is the [[pointed category]]
whose objects are triples $(A\in C,\alpha\colon A\to B,\beta\colon B\to A)$
such that $\alpha\circ\beta=id_B$.
Morphisms $(A,\alpha,\beta)\to(A',\alpha',\beta')$
are morphisms $f\colon A\to A'$ such that $\alpha'\circ f=\alpha$ and $f\circ\beta=\beta'$.

## References

\bibitem{Janelidze2005}

* [[Zurab Janelidze]], _Closedness properties of internal relations_.  A series of papers.

  * I. A unified approach to Malʹtsev, unital and subtractive categories.

  * II. Bourn localization.

  * III. Pointed protomodular categories.

  * IV. Expressing additivity of a category via subtractivity.

  * V. Linear Malʹtsev conditions.

  * VI. Approximate operations.