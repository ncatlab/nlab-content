#derived group scheme#
* automatic table of contents goes here
{:toc}

## Idea ##

A **general group scheme** is a [[group object]] in [[generalized scheme]]s: it is a generalization to [[higher geometry]] of a [[group scheme]].

## Definition ##

Let $X$ be a $\mathcal{G}$-[[generalized scheme]] for $\mathcal{G}$ the [[geometry (for structured (∞,1)-toposes)]] that defines the desired notion of [[derived scheme]]s. 

A **commutative group $\mathcal{G}$-scheme over $X$ is an [[(∞,1)-functor]]

$$
  G : Sch(\mathcal{G})/X \to Ab \infty Grpd
$$

from $\mathcal{G}$-schemes over $X$ to topological abelian groups, such that composition with the forgetful functor $Ab \infty Grpd$ \to \infty Grpd$ is [[representable functor|representable]] by a [[derived scheme]] flat over $X$.


This is (adapted from) definition 3.1 of 

* [[Jacob Lurie]], [[A Survey of Elliptic Cohomology]]

> **warning** careful, this needs a bit more attention. The general idea is obvious, but the detaisl require care. One problem is that in the Elliptic Survey "derived scheme" really referes to [[Spectral Schemes]], which isn't available yet, and not to the derived schemes discussed in [[Structured Spaces]].


## special cases ##

An important special case is that of a [[derived elliptic curve]].
