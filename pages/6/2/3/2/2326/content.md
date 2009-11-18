
#localic topos#
* automatic table of contents goes here
{:toc}

##Definition##

In intrinsic terms, a [[topos]] is _localic_ if it is generated under [[colimit]]s by the [[subobject]]s of its [[terminal object]]. In equivalent but extrinsic terms, a [[Grothendieck topos]] is localic if it is equivalent to the [[category of sheaves]] on a [[locale]] with respect to the [[coverage|topology]] of jointly epimorphic families. The locale may indeed be taken as the [[poset]] of [[subobject]]s of 1. 

## Properties ##

Let $Topos$ be the non-full sub-[[2-category]] of [[Cat]] whose 

* objects are localic toposes;

* morphisms are [[functor]]s that are [[geometric morphism]]s, i.e. functors that preserve finite [[limit]]s and have a [[right adjoint]];

* 2-morphisms are [[natural transformation]]s between these functors.

Then this 2-category is equivalent to the category of [[locale]]s.

> Is that right this way?

##Examples##

Every [[Grothendieck topos]] that is a [[category of sheaves]] on (the [[category of open subsets]] of) a [[topological space]] is localic. 

Many familiar toposes $E$, even when they are not localic, can be covered by a localic slice $E/X$ ("covered" means the unique map $X \to 1$ is an epi). For example, if $G$ is a group, then $E = Set^G$ is not itself localic, but it has a localic slice $Set^G/G \simeq Set$ that covers it. Such toposes have been dubbed _etendu_ (see Lawvere's 1976 monograph Variable Sets, Etendu, and Variable Structure in Topoi). 

A significant result due to Joyal and Tierney is that for any Grothendieck topos $E$, there exists an open surjection $F \to E$ where $F$ is localic. This fact is reproduced in Mac Lane and Moerdijk's text _Sheaves in Geometry and Logic_ (section IX.9), where the localic cover taken is the _Diaconescu cover_ of $E$. 

* Then, using methods of descent theory, Joyal and Tierney deduce that every Grothendieck topos is equivalent to the category $B G$ of continuous discrete representations of a localic groupoid $G$. (Their result is relativized so as to hold internally over any Grothendieck topos $S$ as base.) This should be regarded as a major extrapolation of Grothendieck's Galois theory (as in SGA 1), where it is shown that the etale topos of a field $k$ is equivalent to the category of continuous discrete representations of the fundamental pro-group $Gal(\bar{k}/k)$, where $\bar{k}$ denotes the separable closure of $k$. It was a watershed event for the penetration of localic methods in topos theory. 

## Generalizations ##

In the context of [[(∞,1)-topos]] [[Higher Topos Theory|theory]] there is a notion of [[n-localic (∞,1)-topos]].

Notice that a [[locale]] is itself a (Grothendieck) [[(0,1)-topos]]. Hence a localic topos is a 1-[[topos]] that behaves essentially like a [[(0,1)-topos]]. In the wider context this would be called a [[n-localic (infinity,1)-topos|1-localic (1,1)-topos]].