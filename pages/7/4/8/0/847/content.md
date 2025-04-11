
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
#### Directed homotopy type theory
+-- {: .hide}
[[!include directed homotopy type theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Contents#
* tic
{: toc}


## Idea

In a [[(infinity,1)-category]], the notion of [[terminal object]] known from ordinary [[category theory]] is relaxed in the [[homotopy theory|homotopy theoretic]] sense to the suitable notion in [[(∞,1)-category theory]]:

instead of demanding that from any other object there is a _unique_ morphism into the terminal object, in a quasi-category there is a _[[contractible]] [[infinity-groupoid]]_ of such morphisms, i.e. the morphism to the terminal object is unique _up to [[homotopy]]_.

## Incarnations

### In quasi-categoires

Let $C$ be a [[quasi-category]] and $c \in C$ one of its [[object]]s (a vertex in the corresponding [[simplicial set]]). The object $c$ is a **terminal object** in $C$ if the following equivalent conditions hold:

* The projection from the [[over quasi-category]] $C_{/c} \to C$ is a [[model structure on simplicial sets|trivial fibration of simplicial sets]].

* For every object $d$ of $C$ the right hom Kan-complex into $c$ is contractible:

$$
  Hom_C^R(d,c) \simeq {*}
  \,.
$$

### In simplicial type theory

Let $A$ be a type in [[simplicial type theory]]. An element $y:A$ is a **terminal object** if for all elements $x:A$, the [[hom-type]] $\mathrm{hom}_A(x, y)$ is a [[contractible type]]. 

If $A$ is a [[Segal type]] then this notion coincides with the usual notion of terminal object in an (infinity,1)-category. However, the fact that this definition works for any type $A$ implies that terminal objects should be definable in any [[simplicial infinity-groupoid]] or [[simplicial object in an (infinity,1)-category]], not just the $(\infty,1)$-categories or [[category objects in an (infinity,1)-category]]. 

## Related concepts

* [[initial object]], [[terminal object]]

* [[h-terminal object]]

* [[terminal object in a 2-category]]

* [[initial object in an (infinity,1)-category]]

## References 

A quick survey of terminal objects in quasicategories is on page 159 of

* [[André Joyal]], _The theory of quasicategories and its applications_, lectures at [Simplicial Methods in Higher Categories](http://www.crm.es/HigherCategories/), ([pdf](https://mat.uab.cat/~kock/crm/hocat/advanced-course/Quadern45-2.pdf))

For more details see [definition 1.2.12.3, p. 46](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=46) in 

*  [[Jacob Lurie]], _[[Higher Topos Theory]]_

Terminal objects in $(\infty,1)$-categories are also defined in

* [[Denis-Charles Cisinski]], [[Bastiaan Cnossen]], [[Hoang Kim Nguyen]], [[Tashi Walde]], section 5.5 of: *Formalization of Higher Categories*, work in progress ([pdf](https://drive.google.com/file/d/1lKaq7watGGl3xvjqw9qHjm6SDPFJ2-0o/view))

[[!redirects terminal object in a quasi-category]]
[[!redirects terminal objects in a quasi-category]]
[[!redirects terminal objects in quasi-categories]]

[[!redirects terminal object in a quasicategory]]
[[!redirects terminal objects in a quasicategory]]
[[!redirects terminal objects in quasicategories]]

[[!redirects terminal object in an (∞,1)-category]]
[[!redirects terminal objects in an (∞,1)-category]]
[[!redirects terminal objects in (∞,1)-categories]]

[[!redirects terminal object in an (infinity,1)-category]]
[[!redirects terminal objects in an (infinity,1)-category]]
[[!redirects terminal objects in (infinity,1)-categories]]

[[!redirects final object in a quasi-category]]
[[!redirects final objects in a quasi-category]]
[[!redirects final objects in quasi-categories]]

[[!redirects final object in a quasicategory]]
[[!redirects final objects in a quasicategory]]
[[!redirects final objects in quasicategories]]

[[!redirects final object in an (∞,1)-category]]
[[!redirects final objects in an (∞,1)-category]]
[[!redirects final objects in (∞,1)-categories]]

[[!redirects final object in an (infinity,1)-category]]
[[!redirects final objects in an (infinity,1)-category]]
[[!redirects final objects in (infinity,1)-categories]]

[[!redirects terminal object in simplicial type theory]]
[[!redirects terminal objects in simplicial type theory]]

[[!redirects terminal object in a type]]
[[!redirects terminal objects in a type]]

[[!redirects terminal object in a Segal type]]
[[!redirects terminal objects in a Segal type]]

[[!redirects terminal object in a complete Segal type]]
[[!redirects terminal objects in a complete Segal type]]

[[!redirects terminal object in a Rezk type]]
[[!redirects terminal objects in a Rezk type]]

[[!redirects final object in simplicial type theory]]
[[!redirects final objects in simplicial type theory]]

[[!redirects final object in a type]]
[[!redirects final objects in a type]]

[[!redirects final object in a Segal type]]
[[!redirects final objects in a Segal type]]

[[!redirects final object in a complete Segal type]]
[[!redirects final objects in a complete Segal type]]

[[!redirects final object in a Rezk type]]
[[!redirects final objects in a Rezk type]]
