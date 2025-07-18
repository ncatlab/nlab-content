
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

An __$(\infty,2)$-category__ is the special case of $(\infty,n)$-[[(infinity,n)-category|category]] for $n=2$.

It is best known now through a [[geometric definition of higher category]].

Models include:
 
* the definition by [[Carlos Simpson]] and Tamsamani;

* the definition in terms of [[n-fold Segal spaces]];

* a definition in terms of scaled simplicial sets, following Verity's [[simplicial model for weak omega-categories]] by Jacob Lurie (see reference below)

See also the list of all definitions of higher categories at [[(∞,n)-category]].

## Properties

### Models for the $(\infty,1)$-category of $(\infty,2)$-categories {#TotMod}

In _[[(∞,2)-Categories and the Goodwillie Calculus]]_ [[Jacob Lurie]] discusses a variety of [[model category]] structures, all [[Quillen equivalence|Quillen equivalent]], that all model the [[(∞,2)-category]] of $(\infty,1)$-categories, in generalization of the standard model category models for [[(∞,1)-category|(∞,1)-categories]] themselves (see there for details).

Recall that 

* the standard [[model structure on simplicial sets]] models [[∞-groupoid]]s.

A [[simplicial model category|simplicially]] [[enriched model category]] with respect to the standard model structure on simplicial sets hence models [[∞Grpd]]-enriched categories, hence [[(∞,1)-category|(∞,1)-categories]].

Along this pattern $(\infty,2)$-categories should be modeled by [[enriched category|categories enriched]] in the [[model structure on simplicial sets|Joyal model structure]] that models the [[(∞,1)-category of (∞,1)-categories]].

Write $SSet^J$ for [[SSet]] equipped with the Joyal model structure. Then, indeed, there is a diagram of [[Quillen equivalence]]s of [[model category]] structures

$$
  SSet^J Cat \to SSet SegSp \to [\Delta^{op}, SSet^J]
$$

between Joyal-$SSet$-enriched categories, Joyal-$SSet$-enriched [[complete Segal space]]s and simplicial Joyal-simplicial sets.

This is [remark 0.0.4, page 5](http://arxiv.org/PS_cache/arxiv/pdf/0905/0905.0462v2.pdf#page=5) of the article.
There are many more models. See there for more.

## Examples

Classes of examples include

* [[(∞,2)-toposes]]

* For $\mathcal{C}$ a suitable [[monoidal (∞,1)-category]] there is the $(\infty,2)$-category $Mod(\mathcal{C})$ of $\infty$-algebras and $\infty$-bimodules in $\mathcal{C}$. See at _[bimodule - Properties - The (∞,2)-category of ∞-algebras and ∞-bimodules](bimodule#Infinity2CategoryOfInfinityAlgebrasAndBimodules)_.

## Related concepts

* [[0-category]], [[(0,1)-category]]

* [[category]]

* [[2-category]]

* [[3-category]]

* [[n-category]]

* [[(∞,0)-category]]

* [[(∞,1)-category]]

* **(∞,2)-category**

* [[(∞,n)-category]]

* [[(n,r)-category]]




## References

The original article:

* [[Jacob Lurie]]: *$(\infty,2)$-Categories and the Goodwillie Calculus I*  &lbrack;[arXiv:0905.0462](https://arxiv.org/abs/0905.0462)&rbrack;

Further discussion:

* {#GaitsgoryRozenblyum17} [[Dennis Gaitsgory]], [[Nick Rozenblyum]]: *$(\infty,2)$-Categories*, Appendix of (Vol 1 of): *[[A study in derived algebraic geometry]]*, Mathematical Surveys and Monographs **221**, Americal Mathematical Society (2017) &lbrack;[ams:SURV/221](https://bookstore.ams.org/view?ProductCode=SURV/221), [book webpage](https://people.mpim-bonn.mpg.de/gaitsgde/Book/)&rbrack;

Specifically on the [[Gray tensor product]] in the context of $(\infty,2)$-categories, following [Gaitsgory & Rozenblyum 2017 §10.3](#GaitsgoryRozenblyum17):

* Félix Loubaton, [[Jaco Ruit]]: *On the squares functor and the Gaitsgory-Rozenblyum conjectures* &lbrack;[arXiv:2507.07807](https://arxiv.org/abs/2507.07807)&rbrack;


[[!redirects (infinity,2)-categories]]
[[!redirects (∞,2)-category]]
[[!redirects (∞,2)-categories]]