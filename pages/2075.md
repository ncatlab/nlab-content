
# Idea #

...

# Definition #

 ... [[quasi-category]] ... Joyal's [[model structure on simplicial sets]] ...

# Properties #

+-- {: .un_lemma }
###### Lemma

An [[(∞,1)-functor]] $f : C \to D$ is an equivalence if  the following equivalent conditions hold

* On the underlying [[simplicial set]]s it is a weak categorical equivalence in Joyal's [[model structure on simplicial sets]].

* For every [[simplicial set]] $K$ the induced morphism $f_* : SSet(K,C) \to SSet(K,D)$ is a [[model structure on simplicial sets|weak categorical equivalence]].

* * For every [[simplicial set]] $K$ the induced morphism $f_* : Core(SSet(K,C)) \to Core(SSet(K,D))$ on the maximal [[Kan complex]]es is a [[model structure on simplicial sets|weak categorical equivalence]].


=--

+-- {: .proof}
###### Proof

This is lemma 3.1.3.2 in [[Higher Topos Theory|HTT]].

=--