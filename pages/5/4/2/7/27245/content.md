
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A **lift** or **lifting** of a [[morphism]] $f \colon X \to Y$ (in some [[category]]) through an [[epimorphism]] (or more general [[map]]) $p \colon \widehat{Y} \to Y$, is a morphism $\tilde{f} \colon X\to \widehat{Y}$ such that $f = p\circ\tilde{f}$:

\begin{tikzcd}
  &
  \widehat{Y}
  \ar[
    d,
    "{ p }"
  ]
  \\
  X
  \ar[
    r,
    "{ f }"
  ]
  \ar[
    ur,
    dashed,
    "{ \widetilde f }"
  ]
  &
  Y
  \mathrlap{\,.}
\end{tikzcd}

This is the concept [[formal duality|formally dual]] to *[[extension]]*.

More generally, given a square [[commuting diagram]], then one says a *lift* in the diagram is a dashed morphism from the bottom left to the top right, making both resulting triangles [[commuting diagram|commute]]:

\begin{tikzcd}
  \widehat{X}
  \ar[r]
  \ar[d, "{ h }"]
  &
  \widehat{Y}
  \ar[d, "{p}"]
  \\
  X 
  \ar[r]
  \ar[
    ur,
    dashed
  ]
  &
  Y
  \mathrlap{\,.}
\end{tikzcd}

This reduces to the previous situation in the case that $\widehat{X}$ is an [[initial object]]. (Whereas, when $Y$ is a [[terminal object]] then it reduces to the situation of an *[[extension]]*).

If such a lift exists at all, one also says that $h$ has the *left [[lifting property]]* against $p$, and equivalently that $p$ has the *right [[lifting property]]* against $h$.


## Related concepts

* [[lifting property]]

* [[Kan lift]]

* [[lifts and extensions]]

* [[section]]

* [[projective object]]


[[!redirects lifts]]

[[!redirects lifting]]
[[!redirects liftings]]

[[!redirects lifting problem]]
[[!redirects lifting problems]]
