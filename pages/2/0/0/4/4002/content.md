# Connected topos
* table of contents
{: toc}

## Idea

If we view a (Grothendieck) [[topos]] as a generalized [[topological space]], then a *connected topos* is a generalization of a [[connected topological space]].

More generally, a *connected geometric morphism* $p\colon E\to F$ is a "relativized" notion of this, saying that $E$ is "connected as a topos over $F$."

## Definition

A [[geometric morphism]] $p\colon E\to F$ is **connected** if its inverse image part $p^*$ is [[fully faithful functor|full and faithful]].

A [[Grothendieck topos]] $E$ is **connected** if the unique geometric morphism $E \to Set = Sh(*)$ is connected.  If $E$ is the [[topos of sheaves]] on a [[topological space]] $X$ (or more generally a [[locale]]), then this is equivalent to the usual definition of connectedness for $X$ (see C1.5.7 in the [[Elephant]]).

## Connected locally connected morphisms

For geometric morphisms which are also [[locally connected geometric morphism|locally connected]], connectedness can be phrased in an especially nice form.

+-- {: .un_prop}
###### Proposition
If $p\colon E\to F$ is locally connected, then it is connected if and only if the left adjoint $p_!$ of the inverse image functor (which exists, since $p$ is locally connected) preserves the terminal object.
=--
+-- {: .proof}
###### Proof
This is C3.3.3 in the [[Elephant]].
=--

[[!redirects connected topoi]]
[[!redirects connected toposes]]
[[!redirects connected locally connected topos]]
[[!redirects connected locally connected topoi]]
[[!redirects connected locally connected toposes]]
[[!redirects connected geometric morphism]]
[[!redirects connected geometric morphisms]]
[[!redirects connected locally connected geometric morphism]]
[[!redirects connected locally connected geometric morphisms]]
