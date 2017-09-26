
> This entry is about resolutions in the sense of [[homotopy theory]]. For resolutions of [[singularities]] see at _[[resolution of singularities]]_.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea


In the context of [[homotopy theory]] modeled by [[homotopical categories]], where [[equality]] is relaxed to a weaker concept of ([[weak homotopy equivalence|weak]]) [[homotopy equivalence]] or generally to _[[weak equivalences]]_, a _resolution_ of any [[object]] $X$ is a choice of weak equivalence to or from another object $X_{res}$, such that $X_{res}$ has some prescribed good properties which $X$ itself may be lacking. 

This general concept may be formalized by [[homotopical categories]] that carry extra information on what counts as a "good property" of an object, called _[[fibrant objects]]_ or _[[cofibrant objects]]_. This includes [[fibration categories]]/[[cofibration categories]] and notably [[model categories]].

A common cause for need of resolutions occurs when in a [[category]] of nice objects certain [[universal constructions]] -- such as [[quotients]] or [[intersections]] -- fail to exist. Homotopical resolution may allow to embed the nice objects in categories of _systems_ of nice objects (such as [[simplicial objects]] or [[chain complexes]]) inside which homotopical resolutions may be found (such as [[simplicial resolutions]] or [[homological resolutions]], respectively).

For example the [[quotient]] of a [[scheme]] or a [[smooth manifold]] by the [[action]] of an [[algebraic group]] or [[Lie group]] may fail to be a scheme or smooth manifold again, respectively, but the corresponding _[[action groupoid]]_ ([[orbifold]]) serves as a resolution of the quotient in a suitable [[homotopical category]] of [[simplicial objects]] in schemes/manifolds (presenting the "[[quotient stack]]", see at _[[higher geometry]]_ for more). 

Dually the [[intersection]] of two subschemes/[[submanifolds]] may fail to be a scheme/manifold itself, but the corresponding [[derived intersection]] may provide a resolution in a homotopical category of [[cosimplicial objects]] in schemes/manifolds, respectively (see at _[[derived geometry]]_ for more).



## In a model category

If $C$ is a [[model category]] then the most important resolutions are _cofibrant resolutions_ and _fibrant resolutions_.

A **fibrant resolution** (or *fibrant approximation*) of $X$ is a [[fibrant object]] $\hat X$ equipped with a weak equivalence into it

$$
  X \stackrel{\simeq}{\to} \hat X \to *
  \,.
$$

If the weak equivalence is also a [[cofibration]], the fibrant resolution is a *good fibrant resolution.*

A **cofibrant resolution** (or *cofibrant approximation*) of $X$ is a [[cofibrant object]] $\hat X$ equipped with a weak equivalence out of it

$$
  \emptyset \hookrightarrow \hat X \stackrel{\simeq}{\to} X
  \,.
$$

If the weak equivalence is also a [[fibration]] the cofibrant resolution is a *good cofibrant resolution.* 

Notice that the factorization axioms of a [[model category]] ensure that such resolutions always exist. 

Of course for the notion of fibrant resolution to make sense, also the ambient structure of a [[category of fibrant objects]] works. For cofibrant resolutions a [[Waldhausen category]] does the job, etc.

In the context of [[cofibration categories]], the  term used is *fibrant model*. (One also finds the term *fibrant replacement* used.)

## Examples

### In chain complexes

We consider the case of _[[homological resolutions]]_ in one of the standard [[model structures on chain complexes]].

If $C$ is a category of [[chain complex]]es in a suitable (possibly structured) [[abelian category]] or [[semiabelian category]] $A$ then one can in particular consider resolutions of ordinary objects of $A$ -- regarded as a chain complex concentrated in degree 0 - by chain complexes of $A$.

A _resolution_ is an acyclic nonpositive complex $P_\cdot$ which coaugments $M$ or an acyclic nonnegative complex $I^\cdot$ which augments $M$, i.e. it is equipped with a map of complexes $P_\cdot \to M$ or a map of complexes $M\to I^\cdot$.
 
If each object $P_n$ is a [[projective object]] then  $P_\cdot \to M$ is a **[[projective resolution]]** , and if each $I^n$ is an [[injective object]] then $M\to I^\cdot$ is an **[[injective resolution]]** . These are fibrant and cofibrant resolutions in the suitable [[model structure on chain complexes]].

There are further generalizations like unbounded resolutions etc.

### In simplicial objects

See at _[[simplicial resolution]]_.


## Related concepts


* [[fibrant object]]

* [[canonical resolution]], [[bar construction]]

* [[homological resolution]]

* [[minimal fibration]]

[[!redirects resolutions]]

[[!redirects fibrant resolution]]
[[!redirects cofibrant resolution]]
[[!redirects fibrant resolutions]]
[[!redirects cofibrant resolutions]]


[[!redirects cofibrant replacement functor]]
[[!redirects fibrant replacement functor]]

[[!redirects cosimplicial resolution functor]]
[[!redirects simplicial resolution functor]]
