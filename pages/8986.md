
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

An [[endofunctor]] on a [[category]] $\mathcal{A}$ is _pointed_ if it is equipped with a morphism from the [[identity]] functor.


+-- {: .num_defn}
###### Definition

An [[endofunctor]] $S:\mathcal{A}\to \mathcal{A}$ is called **pointed** if it is equipped with a [[natural transformation]] $\sigma:Id_\mathcal{A} \to S$.  It is called **well-pointed** if $S\sigma = \sigma S$ (as natural transformations $S\to S^2$).

=--

The definition of a pointed endofunctor naturally extends to any [[2-category]], where we can define a **pointed endomorphism** as an endomorphism $s : a \to a$ equipped with a 2-cell $\sigma : 1_a \Rightarrow s$ from the identity.

## Properties

### Relation to free algebras

The pointed [[algebras over an endofunctor]] on a pointed endofunctor induce a theory of _[[transfinite construction of free algebras]]_ [[algebra over an endofunctor|over]] general endofunctors.

## Examples

A [[monad]] can be regarded as a pointed endofunctor where $\sigma$ is its unit.  Such an endofunctor is well-pointed precisely when the monad is [[idempotent monad|idempotent]].

## For pointed object in the endofunctor category

Notice that the statement which one might expect, that a pointed endofunctor is a [[pointed object]] in the [[endofunctor category]] is not quite right in general.

The [[terminal object]] of the category of endofunctors on $\mathcal{A}$ is the functor $T$ which sends all objects to $\ast$ and all morphisms to the unique morphism $\ast \to \ast$, where $\ast$ is the terminal object of the category $\mathcal{A}$. So a pointed object in the endofunctor category should be an endofunctor $S:\mathcal{A} \to \mathcal{A}$ equipped with a natural transformation $\sigma:T \to S$.

Rather, a pointed endofunctor is equipped with a map from the [[unit object]] for the monoidal structure on the endofunctor category.


## Related concepts

* [[pointed object]]

[[!redirects pointed endofunctors]]
[[!redirects pointed endomorphism]]
[[!redirects pointed endomorphisms]]