
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition 

 ... [[quasi-category]] ... Joyal's [[model structure for quasi-categories]] ...

## Properties 

+-- {: .un_lemma }
###### Lemma

An [[(∞,1)-functor]] $f : C \to D$ is an **equivalence** in [[(∞,1)Cat]] if  the following equivalent conditions hold

* On the underlying [[simplicial set]]s it is a weak categorical equivalence in Joyal's [[model structure for quasi-categories]].

* For every [[simplicial set]] $K$ the induced morphism $f_* : SSet(K,C) \to SSet(K,D)$ is a [[model structure for quasi-categories|weak categorical equivalence]].

* For every [[simplicial set]] $K$ the induced morphism $f_* : Core(SSet(K,C)) \to Core(SSet(K,D))$ on the maximal [[Kan complex]]es is a [[model structure on simplicial sets|equivalence of Kan complexes]] (a [[homotopy equivalence]]).


=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, lemma 3.1.3.2]].

=--

[[!redirects equivalence of (∞,1)-categories]]