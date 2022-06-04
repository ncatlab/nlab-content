+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

The notion of *cotopos* is [[abstract duality|dual]] to that of a [[topos]]. 

A co-elementary cotopos should be the 1-categorical version of a [[co-Heyting algebra]] (which model [[dual intuitionistic logic]]), and a co-Grothendieck cotopos should be the 1-categorical version of a [[coframe]] (which model [[closed sublocales]] in [[topology]]). 

## Definition 

### Co-elementary cotopos

A co-elementary cotopos is a [[finitely cocomplete category|finitely cocomplete]] [[cocartesian coclosed category|cocartesian coclosed]] [[category]] with a [[quotient object coclassifier]]. 

### Co-Grothendieck cotopos

A co-Grothendieck cotopos is a [[locally small category|locally small]] [[finitely cocomplete category]] with a small [[cogenerator]], with all small [[products]] which are codisjoint and pushout-stable, and where all internal [[bisimulations]] have effective [[subobjects]], which are also pushout-stable. 

## Properties

Every [[cotopos]] is a [[protomodular category]]. 

## Examples

A [[binary relation]] $R$ between sets $A$ and $B$ is *injective* if for all $a \in A$, $b \in A$, and $c \in B$, if $R(a, c)$ and $R(b, c)$ then $a = c$. A binary relation $R$ between sets $A$ and $B$ is *onto* if for all $b \in B$ there exists an element $a \in A$ such that $R(a, b)$. The category of sets and injective onto binary relations is a cotopos. 

## See also

* [[coclosed category]]

* [[coclosed monoidal category]]

* [[cocartesian monoidal category]]

* [[cocartesian coclosed category]]

* [[locally cocartesian coclosed category]]

* [[coslice category]]

* [[protomodular category]]

* [[M-cotopos]]

* [[co-well-pointed cotopos]]

* [[quotient object coclassifier]]

* [[co-Heyting algebra]]

* [[coframe]]

* [[topos]]

## References

* Mamuka Jibladze, "Cosheaves, coframes, cotoposes: some new facts, some old questions" ([web archive](https://web.archive.org/web/20130602214748/http://www.wra1th.plus.com/gcw/rants/math/PSSL/1997.html))

[[!redirects cotopoi]]
[[!redirects cotoposes]]