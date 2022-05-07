
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category Theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Just as a [[subobject classifier]] in a [[(1,1)-category]] classifies the [[monomorphisms]] or [[(-1)-truncated]] morphisms (and thus the [[subobjects]]) of the category, a _discrete object classifier_ in a [[(2,1)-category]] should classify the [[faithful functor|faithful]] or [[0-truncated]] morphisms (and thus the [[discrete morphism|discrete objects]]) in the (2,1)-category, see at _[n-truncated morphisms -- between groupoids](n-truncated+object+of+an+infinity-category#TruncatedMorphismsBetweenGroupoids)_. 

## Definition

In a (2,1)-category $C$ with [[terminal object]] $*$ and finite [[2-pullback|(2,1)-pullbacks]], a __discrete object classifier__ is a nonterminal object $Set$ such that for every [[inhabited]] morphism $A: * \rightarrow Set$ and every [[faithful morphism]] $B \colon U \rightarrow G$ in $C$, there is a unique morphism $F:G \rightarrow Set$ such that there is a (2,1)-pullback [[diagram]] of the form

$$\array{U & \to & * \\
  ^{B}\downarrow & \cong & \downarrow^{A}\\
  G & \underset{F}{\to} & Set}$$

If $Set$ exists, it is typically called the __[[universe]] of [[set]]s__, a global element $F:G \rightarrow Set$ is typically called an [[indexed family]] and an element $A:* \rightarrow Set$ is typically called a set, where all these terms refer to the [[internalization|internal]] [[structural set theory]] of the (2,1)-category $C$. 

## Examples

### In $Grpd$

In the (2,1)-category [[Grpd]] of groupoids and functors between groupoids, the discrete object classifier $Set$ is the groupoids of sets, or, as $Set$ is a groupoid with a category structure, more commonly known as the [[category of sets]].
 

## See also

* [[subobject classifier]]

* [[(sub)object classifier in an (infinity,1)-topos]]

* [[classifying morphism]]

* [[type of types]], [[universe in a topos]]