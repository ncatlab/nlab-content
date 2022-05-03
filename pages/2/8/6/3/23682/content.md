[[!redirects W-topical dagger 2-posets]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

## Contents ##
* table of contents
{:toc}

## Idea ##

A W-topical dagger 2-poset is a dagger 2-poset whose [[category of maps]] is a [[W-topos]].

## Definition ##

A **W-topical dagger 2-poset** $C$ is an [[elementarily topical dagger 2-poset]] with an object $\mathbb{N} \in Ob(C)$ and [[map in a dagger 2-poset|maps]] $0 \in Map_C(\mathcal{P}(0),\mathcal{N})$ and $s \in Map_C(\mathbb{N},\mathbb{N})$, such that for every object $A$ with maps $0_A \in Map_C(\mathcal{P}(0),A)$ and $s_A \in Map_C(A,A)$, there is a map $f \in Map_C(\mathbb{N},A)$ such that $f \circ 0 = 0_A$ and $f \circ s = s_A \circ f$. 

## Examples ##

The dagger 2-poset [[Rel]] of [[sets]] and [[relations]] is a W-topical dagger 2-poset. 

## See also ##

* [[dagger 2-poset]]
* [[elementarily topical dagger 2-poset]]