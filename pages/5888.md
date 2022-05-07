
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn}
###### Definition

A [[geometric morphism]] $f : \mathcal{E} \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}} \mathcal{F}$ is called **atomic** if its [[inverse image]] $f^*$ is a [[logical functor]].

=--

+-- {: .num_defn}
###### Definition

A [[sheaf topos]] $\mathcal{E}$ is called **atomic** if its [[global section]] geometric morphism is atomic, or in other words, if the [[constant sheaf|constant sheaf functor]] $\Delta\colon Set\to\mathcal{E}$ is logical.

Generally, a topos over a [[base topos]] $\Gamma : \mathcal{E} \to \mathcal{S}$ is called an [[atomic topos]] if $\Gamma$ is atomic.

=--

+-- {: .num_note}
###### Note

As shown in prop. \ref{AtomicMeansLocallyConnected} below, every atomic morphism $f : \mathcal{E} \to \mathcal{S}$ is also a [[locally connected geometric morphism]]. The connected objects $A \in \mathcal{E}$, $f_! A \simeq *$ are called the **atoms** of $\mathcal{E}$.

=--

See ([Johnstone, p. 689](#Johnstone)).

## Properties

### General

+-- {: .num_prop}
###### Proposition

Atomic morphisms are closed under composition.

=--

+-- {: .num_prop #AtomicMeansLocallyConnected}
###### Proposition

An atomic geometric morphism is also a [[locally connected geometric morphism]].

=--

+-- {: .proof}
###### Proof

By <a href="https://ncatlab.org/nlab/show/logical+functor#LeftRightAdjoint">this proposition</a> a logical morphism with a [[right adjoint]] has also a [[left adjoint]].

=--

+-- {: .num_prop #ConnectedAtomicImpliesHyperconnected}
###### Proposition

If an atomic morphism is also a [[connected geometric morphism|connected]], then it is even [[hyperconnected geometric morphism|hyperconnected]].
 
=--

This appears as ([Johnstone, lemma 3.5.4](#Johnstone)).



+-- {: .num_prop}
###### Proposition

A [[localic geometric morphism]] is atomic precisely if it is an [[etale geometric morphism]].

=--

This appears as ([Johnstone, lemma 3.5.4 (iii)](#Johnstone)).

+-- {: .num_prop}
###### Proposition

Every [[étale geometric morphism]] is atomic.

=--

## Related concepts

 * [[atomic topos]]

 * [[atomic site]]

## References

* {#Johnstone}[[Peter Johnstone]], _[[Sketches of an Elephant]] vol. 2_ , Oxford UP 2002. (section C3.5, pp.684-695)
 

[[!redirects atomic geometric morphisms]]
