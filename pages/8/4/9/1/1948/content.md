<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}


# Idea #

For $C$ a [[combinatorial model category]] and $D$ any [[small category]] there are two natural [[model category]] structures on the [[functor category]] $[D,C]$ called the _projective_ and the _injective_ model structure.

A variant of this is the [[Reedy model structure]] on functor categories, which assumes less structure on $C$, but more on $D$. See there for furhter background.

In the special case that $C = $ [[SSet]] is the standard [[model structure on simplicial sets|model category of simplicial sets]] the projective and injective model structure on the functor categories $[D,SSet]$ are described in more detail at [[global model structure on simplicial presheaves]].

#Definition#

For $C$ a [[combinatorial model category]] and $D$ a [[small category]] there exists the following two [[combinatorial model category]] structures on the [[functor category]] $[D,C]$:

* the **projective** structure $[D,C]_{proj}$: weak equivalences and fibrations are the [[natural transformation]]s that are objectwise such morphisms in $C$. (The cofibrations are then defined by their [[weak factorization system|left lifting property]].)

* the **injective** structure $[D,C]_{inj}$: weak equivalences and cofibrations are the [[natural transformation]]s that are objectwise such morphisms in $C$. (The fibrations are then defined by their [[weak factorization system|right lifting property]].)


+-- {: .un_prop}
###### Proposition

For $C$ a [[combinatorial model category]] and $D$ a [[small category]] the projective and injective structures $[D,C]_{proj}$ and $[D,C]_{inj}$ are themselves [[combinatorial model category|combinatorial model categories]].

=--

+-- {: .proof}
###### Proof

This is for instance [[Higher Topos Theory|HTT]], prop A.2.8.2

=--





#References#

For instance proposition A.2.8.2 of

* [[Jacob Lurie]], [[Higher Topos Theory]]

[[!redirects injective model structure]]
[[!redirects projective model structure]]
[[!redirects global model structures on functor categories]]
