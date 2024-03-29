
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

# Eso morphisms
* table of contents
{: toc}

## Definition

In any [[2-category]] $K$, a morphism $f:A\to B$ is called **eso**, or **strong 1-epic**, if for any [[fully faithful morphism]] $m:C\to D$, the following square is a ([[2-limit|2-categorical]]) [[pullback]] in [[Cat]]:
$$\array{K(B,C) & \to & K(B,D)\\
\downarrow & & \downarrow \\
K(A,C) & \to & K(A,D)}$$
This can be rephrased in elementary terms, without the need for a category $Cat$ in which the hom-categories of $K$ live.

One easily checks that when $K=$ [[Cat]], a functor $f$ is eso if and only if it is [[essentially surjective functor|essentially surjective on objects]] in the usual sense.  (This requires either the [[axiom of choice]] or the use of [[anafunctor]]s in defining $Cat$.)


## Remarks

* If $K$ has finite limits, then $f:A\to B$ is eso if and only if whenever $f\cong m g$ where $m$ is ff, then $m$ is an [[equivalence]].

* Any [[coinserter]], co-[[isoinserter]], [[coinverter]], [[coequifier]], or (lax or oplax) [[codescent object]] is eso.

* If $K$ has finite limits and $f:A\to B$ is eso, then for any $Z$ the functor $K(B,Z)\to K(A,Z)$ is [[faithful functor|faithful]] and [[conservative functor|conservative]].

* If $K$ is a 1-category with finite limits, regarded as a 2-category with only identity 2-cells, then a morphism in $K$ is eso if and only if it is an [[extremal epimorphism]] (equivalently, a [[strong epimorphism]]).


[[!redirects eso morphism]]
[[!redirects eso morphisms]]
[[!redirects strong 1-epimorphism]]
[[!redirects strong 1-epimorphisms]]
[[!redirects strong 1-epic morphism]]
[[!redirects strong 1-epic morphisms]]
[[!redirects strong 1-epic]]
[[!redirects strong 1-epics]]
[[!redirects strong 1-epi]]
[[!redirects strong 1-epis]]
