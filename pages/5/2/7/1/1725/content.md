
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
* automatic table of contents goes here
{:toc}

## Idea

An __$(\infty,2)$-category__ is the special case of $(\infty,n)$-[[(infinity,n)-category|category]] for $n=2$.

It is best known now through a [[geometric definition of higher category]].

Models include 
* the definition by [[Carlos Simpson]] and Tamsamani;
* the definition in terms of [[n-fold Segal space]]s;
* a definition in terms of scaled simplicial sets, following Verity's [[simplicial model for weak omega-categories]] by Jacob Lurie (see reference below)

See also the list of all definitions of higher categories at [[n-category]].

## Models for the $(\infty,1)$-category of $(\infty,2)$-categories {#TotMod}

In _[[(∞,2)-Categories and the Goodwillie Calculus]]_ [[Jacob Lurie]] discusses a variety of [[model category]] structures, all [[Quillen equivalence|Quillen equivalent]], that all model the [[(∞,1)-category]] of $(\infty,2)$-categories, in generalization of the standard model category models for [[(∞,1)-category|(∞,1)-categories]] themselves (see there for details).

Recall that 

* the standard [[model structure on simplicial sets]] models [[∞-groupoid]]s.

a [[simplicial model category|simplicially]] [[enriched model category]] with with respect to the standard model structure on simplicial sets hence models [[∞Grpd]]-enriched categories, hence [[(∞,1)-category|(∞,1)-categories]].

Along this pattern $(\infty,2)$-categories should be modeled by [[enriched category|categories enriched]] in the [[model structure on simplicial sets|Joyal model structure]] that models the [[(∞,1)-category of (∞,1)-categories]].

Write $SSet^J$ for [[SSet]] equipped with the Joyal model structure. Then, indeed, there is a diagram of [[Quillen equivalence]]s of [[model category]] structures

$$
  SSet^J Cat \to SSet SegSp \to [\Delta^{op}, SSet^J]
$$

between Joyal-$SSet$-enriched categories, Joyal-$SSet$-enriched [[complete Segal space]]s and simplicial Joyal-simplicial sets.

This is [remark 0.0.4, page 5](http://arxiv.org/PS_cache/arxiv/pdf/0905/0905.0462v2.pdf#page=5) of the article.
There are many more models. See there for more.


##References

* [[Jacob Lurie]], _[[(∞,2)-Categories and the Goodwillie Calculus]]_

[[!redirects (infinity,2)-categories]]
[[!redirects (∞,2)-category]]
[[!redirects (∞,2)-categories]]