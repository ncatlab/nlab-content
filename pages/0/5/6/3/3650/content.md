
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
+ automatic table of contents goes here
{:toc}

## Idea

A [[geometric morphism]] is *locally connected* if it behaves as though its [[fiber]]s are [[locally connected space]]s.  In particular, a [[Grothendieck topos]] $E$ is [[locally connected topos|locally connected]] iff the unique [[geometric morphism]] to [[Set]] (the terminal Grothendieck topos, i.e. the [[point]] in the [[category]] [[Toposes]] of toposes) is locally connected.

## Definition

A [[geometric morphism]] $ (f^* \dashv f_*) : F \underoverset{f_*}{f^*}{\leftrightarrows} E$ is **locally connected** if it satisfies the following equivalent conditions:

1. It is [[essential geometric morphism|essential]], i.e. $f^*$ has a [[left adjoint]] $f_!$, and moreover $f_!$ can be made into an $E$-[[indexed functor]].

1. For every $A\in E$, the functor $f^* \colon E/A \to F/f^*A$ is [[cartesian closed functor|cartesian closed]].

1. For any morphism $h\colon A\to B$ in $E$, the canonically defined transformation $f^* \circ \Pi_h \to \Pi_{f^*h} \circ f^*$ is an [[isomorphism]].

## Properties

If $f$ is locally connected, then it makes sense to think of the left adjoint $f_!$ as assigning to an object of $F$ its "set of connected components" in $E$.  In particular, if $f$ is locally connected, then it is moreover [[connected geometric morphism|connected]] if and only if $f_!$ preserves the terminal object.  However, not every connected geometric morphism is locally connected.

## Examples

* If the terminal [[global section]] geometric morphism $E \to Set$ is locally connected, one calls $E$ a [[locally connected topos]].  More generally, if $E\to S$ is locally connected, we may call $E$ a *locally connected $S$-topos*.

* Let $X$ be a [[topological space]] (or a [[locale]]) and $U\subseteq X$ an [[open subset]], with corresponding [[geometric embedding]] $j\colon Sh(U)\to Sh(X)$.  Then any $A\in Sh(X)$ can be identified with a space (or locale) $A$ equipped with a [[local homeomorphism]] $A\to X$, in such a way that $Sh(X)/A \simeq Sh(A)$.  Moreever, $j^*A \in Sh(U)$ can be identified with the pullback of $A\to X$ along $U$, and so $Sh(U)/j^*A \simeq Sh(j^*A)$ similarly.  Noting that $j^*A \to A$ is again the inclusion of an open subset, and using the fact that the inverse image part of any open [[geometric embedding]] is cartesian closed, we see that $(j/A)^*\colon Sh(X)/A \to Sh(U)/j^*A$ is cartesian closed for any $A$.  Hence $j$ is locally connected.

## References

Section C3.3 of

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_


[[!redirects locally connected geometric morphisms]]
