
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--




# Contents#
* tic
{: toc}


## Idea

In a [[quasi-category]] the notion of [[terminal object]] known from ordinary [[category theory]] is relaxed in the [[homotopy theory|homotopy theoretic]] sense to the suitable notion in [[(∞,1)-category theory]]:

instead of demanding that from any other object there is a _unique_ morphism into the terminal object, in a quasi-category there is a _[[contractible space]]_ of such morphisms, i.e. the morphism to the terminal object is unique _up to [[homotopy]]_.


##Definition

Let $C$ be a [[quasi-category]] and $c \in C$ one of its [[object]]s (a vertex in the corresponding [[simplicial set]]). The object $c$ is a **terminal object** in $C$ if the following equivalent conditions hold:

* The projection from the [[over quasi-category]] $C_{/c} \to C$ is a [[model structure on simplicial sets|trivial fibration of simplicial sets]].

* For every object $d$ of $C$ the right hom Kan-complex into $d$ is contractible:

$$
  Hom_C^R(d,c) \simeq {*}
  \,.
$$


##References#

A quick survey is on page 159 of

* [[André Joyal]], _The theory of quasicategories and its applications_ lectures at [Simplicial Methods in Higher Categories](http://www.crm.es/HigherCategories/), ([pdf](http://www.crm.cat/HigherCategories/hc2.pdf))

For more details see [definition 1.2.12.3, p. 46](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=46) in 

*  [[Jacob Lurie]], _[[Higher Topos Theory]]_


[[!redirects terminal objects in quasi-categories]]
[[!redirects terminal object in a quasicategory]]
[[!redirects terminal objects in quasicategories]]

[[!redirects terminal object in an (∞,1)-category]]
[[!redirects terminal objects in an (∞,1)-category]]
[[!redirects terminal objects in (∞,1)-categories]]