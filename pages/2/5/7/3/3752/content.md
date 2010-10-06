
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

* A semicategory is morally a [[category]] without the identity morphisms.  

* Semicategories, like categories, appear as [[semipresheaf|semipresheaves]] on the category with two objects and two morphisms.  

## Definition

A _category_ $C$ consists of 

* a [[collection]] $C_0$ of _objects_;

* a collection $C_1$ of _morphisms_ (or _arrows_);

* two maps $s, t : C_1 \to C_0$ called _source_ (or _domain_) and _target_ (or _codomain_);

  * one writes $f : x \to y$ if $s(f) = x$ and $t(f) = y$;

* a rule which assigns to any pair of morphisms $f$, $g$ such that $t(f) = s(g)$ their _composite_ morphism $g \circ f \in C_1$ (also  written $g f$ or sometimes $f;g$&#8212; see [[diagrammatic order]]);

* such that the following properties are satisfied:

  * source and target are respected by composition: $s(g \circ f) = s(f)$ and $t(g\circ f) = t(g)$;

  * composition is _associative_: $(h \circ g)\circ f = h\circ (g \circ f)$ whenever $t(f) = s(g)$ and $t(g) = s(h)$;

People often write $hom(x,y)$, $hom_C(x,y)$, or $C(x,y)$ for the collection of morphisms $f : x \to y$; the latter two have the advantage of making clear which category is being discussed.  People also often write $x \in C$ instead of $x \in C_0$ as a short way to indicate that $x$ is an object of $C$.  Also, some people write $Ob(C)$ and $Mor(C)$ instead of $C_0$ and $C_1$.

[[!redirects semicategories]]