
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory#
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--



# Commutative diagrams
* table of contents
{: toc}

## Idea

In [[category theory]], a _commutative diagram_ is a [[free diagram]] in which all [[parallel morphisms]] obtained by [[composition|composing]] morphisms in the diagram agree.

For example that a square diagram of the form

$$
  \array{& X & \overset{f}\rightarrow & Z & \\
          g & \downarrow &&\downarrow & g'\\
          &Y & \underset{f'}\rightarrow& W & \\
}$$

commutes is to say that $g' \circ f = f' \circ g$ (see also at _[[commuting square]]_).


## Definitions

### Slick definition

For our purposes, a __[[free diagram]]__ $D$ in a [[category]] $C$ consists of a [[graph]] $J$ and a [[functor]] to $C$ from the [[free category]] on $J$:
$$ F(J) \overset{D}\to C $$
Then this diagram $D$ __commutes__ if this functor $D$ factors (up to [[natural isomorphism]]) through a [[poset]] $P$:
$$ F(J) \to P \to C \;\cong\; F(J) \to C ,\; P\;\text{a poset} ;$$
or equivalently (treating $C$ as a [[strict category]]) if the functor factors up to [[equality]] through a [[preorder]] $Q$:
$$ J \to Q \to C \;\cong\; J \to C ,\; Q\;\text{a preorder} .$$
In the above, we are identifying [[posets]], and [[preorder]] with certain categories in the usual ways.


### Elementary definition

Recall that a __[[graph]]__ $J$ consists of a [[set]] $V$ of _vertices_, a set $E$ of _edges_, and two [[functions]] $s,t\colon E \to V$.  Given a category $C$, a __free diagram__ $D$ of shape $J$ in a category $C$ comprises a map from $V$ to the [[objects]] of $C$ and a map from $E$ to the [[morphisms]] of $C$, both denoted $D$, such that $D(s(e)) = s(D(e))$ and $D(t(e)) = t(D(e))$ for each edge $e$, where $s,t$ also denote the [[source]] and [[target]] maps in $C$.

Recall that a __[[path]]__ $p$ in $J$ comprises a [[list]] $(v_0,v_1,\ldots,v_n)$ of vertices and a list $(e_1,\ldots,e_n)$ of edges such that $s(e_i) = v_{i-1}$ and $t(e_i) = v_{i}$ for each $i$, where $n$ is any [[natural number]] (possibly zero).  We say that $v_0$ is the __source__ of the path and that $v_n$ is its __target__.  Given a path $p$ and a diagram $D$, the __composite__ of $p$ under $D$ is the [[composite]] $F(e_1);\ldots;D(e_n)\colon D(v_0) \to D(v_n)$ in $C$. (Note that the paths of length zero are composed to the identity $\id_{D(v_0)}\colon D(v_0) \to D(v_0)$.)

A diagram $D$ __commutes__ if, given any two vertices $x,y$ in $J$ and any two paths $p,p'$ with source $x$ and target $y$, the composites of $p$ and $p'$ under $D$ are equal in $C$.

## Edges cases

### Cycles and loops 

Cycles (including loops) are generally avoided in commutative diagrams in [[category theory]] texts. However, they make sense under the definition above. For instance, commutativity of the following diagram implies that $h g f = 1$, $g f h = 1$, and $f h g = 1$.
\begin{tikzcd}
	& B \\
	A && C
	\arrow["g", from=1-2, to=2-3]
	\arrow["f", from=2-1, to=1-2]
	\arrow["h", from=2-3, to=2-1]
\end{tikzcd}
Similarly, every loop in a commutative diagram is required to be an [[identity morphism]].

### Forks

Diagrams like the following are often used to denote [[forks]] in category theory.
\begin{tikzcd}
	A & B & C
	\arrow["f", from=1-1, to=1-2]
	\arrow["g", shift left=2, from=1-2, to=1-3]
	\arrow["h"', shift right=2, from=1-2, to=1-3]
\end{tikzcd}
However, note that for this diagram to commute, we require the stronger condition that $g = h$, not just that $g f = h f$.

If this is undesirable, a weaker notion of commutativity may be asked for, in which we only ask for commutativity of parallel paths where the source is a **source** in the sense that it only has outgoing edges, and the target is a **sink** in that it only has incoming edges. This convention may sometimes be implicitly encountered in category theory texts.

## Related entries

* [[diagram]]

* [[internal diagram]]

* [[free diagram]]

## References

* [Wikipedia](http://en.wikipedia.org/wiki/Commutative_diagram)
* [Mathworld](http://mathworld.wolfram.com/CommutativeDiagram.html)


[[!redirects commutative diagram]]
[[!redirects commutative diagrams]]
[[!redirects commuting diagram]]
[[!redirects commuting diagrams]]
