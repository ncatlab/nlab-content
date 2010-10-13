
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

A [[geometric morphism]] is *locally connected* if it behaves as though its fibers are locally connected spaces.  In particular, a [[Grothendieck topos]] $E$ is [[locally connected topos|locally connected]] iff the unique morphism to $Set$ (the terminal Grothendieck topos, i.e. the [[point]] in the category of topoi) is locally connected.

## Definition

A geometric morphism $F \underoverset{f_*}{f^*}{\leftrightarrows} E$ is **locally connected** if it satisfies the following equivalent conditions:

1. It is [[essential geometric morphism|essential]], i.e. $f^*$ has a left adjoint $f_!$, and moreover $f_!$ can be made into an $E$-[[indexed functor]].

1. For every $A\in E$, the functor $f^* \colon E/A \to F/f^*A$ is [[cartesian closed functor|cartesian closed]].

1. For any morphism $h\colon A\to B$ in $E$, the canonically defined transformation $f^* \circ \Pi_h \to \Pi_{f^*h} \circ f^*$ is an isomorphism.

## Properties

If $f$ is locally connected, then it makes sense to think of the left adjoint $f_!$ as assigning to an object of $F$ its "set of connected components" in $E$.  In particular, if $f$ is locally connected, then it is moreover [[connected geometric morphism|connected]] if and only if $f_!$ preserves the terminal object.  However, not every connected geometric morphism is locally connected.

## Examples

If the terminal [[global section]] geometric morphism is locally connected, one speaks of a [[locally connected topos]].

## References

* Section C3.3 of the [[Elephant]]

