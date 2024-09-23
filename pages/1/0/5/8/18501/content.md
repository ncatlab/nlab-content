
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

\tableofcontents

## Idea

A *final pullback complement* is a "universal completion of a pair of [[arrows]] to a [[pullback]]".  Intuitively, it is a way to "remove part of an [[object]] of a [[category]]" while retaining information about how that part is "connected" to other parts.  Final pullback complements play an important role in some kinds of [[span rewriting]].

## Definition

Given [[morphisms]] $m:C\to A$ and $g:A\to D$ in a [[category]], a **pullback complement** is a pair of arrows $f:C\to B$ and $n:B\to D$ such that the square
\begin{tikzcd}
	C & A \\
	B & D
	\arrow["m", from=1-1, to=1-2]
	\arrow["f"', from=1-1, to=2-1]
	\arrow["g", from=1-2, to=2-2]
	\arrow["n"', from=2-1, to=2-2]
\end{tikzcd}
[[commutative square|commutes]] and is a [[pullback]].  This is of course the dual of a [[pushout complement]].

A morphism of pullback complements is a map $B\to B'$ making the obvious diagrams commute.  A **final pullback complement** is a [[terminal object]] in the category of pullback complements.  Since they have a universal property, final pullback complements are unique up to unique isomorphism when they exist.

## Relation to exponentials

Recall from [[distributivity pullback]] that a **pullback around $(g,m)$** is a diagram
$$\array{ X & \xrightarrow{p} & C & \xrightarrow{m} & A\\
  ^q\downarrow &&&& \downarrow^g\\
  Y && \xrightarrow{r} && D}
$$
in which the outer rectangle is a pullback, and that a **distributivity pullback** around $(g,m)$ is a terminal object in the category of pullbacks aroung $(g,m)$.  This makes the following evident:

+--{: .un_prop}
###### Proposition
If a distributivity pullback around $(g,m)$ exists and has the property that $p$ is an [[isomorphism]], then it is also a final pullback complement.
=--

A distributivity pullback has precisely the universal property of an [[exponential object]] of $m$ along $g$.  Thus, whenever such an exponential $\Pi_g m$ exists and the [[counit]] $g^* \Pi_g m \to m$ is an isomorphism, a final pullback complement exists.  This is the case in particular in a [[locally cartesian closed category]] if $g$ and $m$ are both [[monomorphisms]].

## Relation to pushout complements

In an [[adhesive category]], any pushout complement of a monomorphism is also a final pullback complement.

## Related pages

* [[pushout complement]]
* [[span rewriting]]
* [[distributivity pullback]]

## References

* Andrea Corradini, Tobias Heindel, Frank Hermann, and Barbara K&#246;nig, *Sesqui-pushout rewriting*, 2006, [springerlink](https://link.springer.com/chapter/10.1007/11841883_4), [pdf](http://www.ti.inf.uni-due.de/publications/koenig/icgt06b.pdf).
 {#CHHK}


[[!redirects final pullback complements]]
