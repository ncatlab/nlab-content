
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

The _model structure on reduced simplicial sets_ is a [[presentable (infinity,1)-category|presentation]] of the full [[sub-(∞,1)-category]] of [[∞Grpd]] $\simeq$ [[Top]] on those [[∞-groupoid]]s that are [[connected]].


## Definition


+-- {: .num_def }
###### Definition

A _reduced simplicial set_ is a [[simplicial set]] $S$ with a single vertex:

$$
  S_0 = *
  \,.
$$

Write $sSet_0 \subset $ [[sSet]] for the [[full subcategory]] of the category of [[simplicial sets]] on those that are reduced.

=--

+-- {: .num_prop }
###### Proposition



There is a [[model category]] structure on $sSet_0$ whose

* weak equivalences 

* and cofibrations

are those in the standard [[model structure on simplicial sets]].

=--

This appears as ([GoerssJardine, ch V, prop. 6.2](GoerssJardine)).


## Properties

+-- {: .num_prop }
###### Proposition

The simplicial loop space functor $G$ and the delooping functor $\bar W(-)$ (discussed at [[simplicial group]]) constitute a [[Quillen equivalence]]

$$
  (G \dashv \bar W) : sGr \stackrel{\overset{G}{\leftarrow}}{\underset{\bar W}{\to}}
  sSet_0
$$

with the [[model structure on simplicial groups]].

=--

This appears as ([GoerssJardine, ch. V prop. 6.3](#GoerssJardine)).


+-- {: .num_prop }
###### Proposition

Under the [[forgetful functor]] $U : sSet_0 \hookrightarrow sSet$ 

* a fibration $f : X \to Y$ maps to a fibration precisely if it has the [[right lifting property]] against $* \to S^1 := \Delta[1]/ \partial \Delta[1]$;

In particular

* every fibrant object maps to a fibrant object.

=--

The first statment appears as ([GoerssJardine, ch. V, lemma 6.6.](#GoerssJardine)). The second (an immediate consequence) appears as ([GoerssJardine, ch. V, corollary 6.8](#GoerssJardine)).

## Related concepts

* [[model structure on simplicial groups]]

* **model structure on reduced simplicial sets**

* [[groupoid object in an (∞,1)-category]]

## References

A standard textbook reference is chapter V of

* [[Paul Goerss]], Jardine, _Simplicial homotopy theory_ [chapter V](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-5.dvi). 
{#GoerssJardine}
