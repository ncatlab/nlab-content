
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

An __endomorphism__ of an [[object]] $x$ in a [[category]] $C$ is a [[morphism]] $f : x \to x$.  

An endomorphism that is also an [[isomorphism]] is called an [[automorphism]].

## Properties

Given an object $x$, the endomorphisms of $x$ form a [[monoid]] under [[composition]], the __[[endomorphism monoid]]__ of $x$:
$$
  End_C(x) = Hom_C(x,x)
,$$
which may be written $End(x)$ if the category $C$ is understood.  Up to equivalence, every monoid is an endomorphism monoid; see [[delooping]].

An endomorphism monoid is a special case of a monoid structure on an [[end]] construction. Let $d:D\to C$ be a diagram in $C$, where $C$ is a [[monoidal category]] (in the case above the monoidal structure is the [[cartesian product]] and $d$ is a constant diagram from the initial category). One defines $End(d)$ as an object in $C$, equipped with a natural transformation $a: End(d) \otimes d \to d$ which is universal in the sense that for all objects $Z \in C$, and any natural transformation $f: Z \otimes d \to d$ there exists a unique morphism $g: Z \to End(d)$ such $a \circ (g \otimes d) = f: Z \otimes d \to d$.

+--{: .un_prop}
###### Proposition

If the universal object $(End(d),a)$ exists then there is a unique structure of a monoid $\mu: End(d) \otimes End(d) \to End(d)$, such that the map $a: End(d) \otimes d \to d$ is an [[action]].
=--

## Related entries


* **endomorphism**, [[automorphism]]

* [[endomorphism monoid]], [[endomorphism ring]]

* [[endomorphism operad]]



[[!redirects endomorphisms]]
[[!redirects endomorphism monoid]]
[[!redirects endomorphism monoids]]