

#Definition#

In intrinsic terms, a [[topos]] is _localic_ if it is generated under [[colimit]]s by the [[subobject]]s of its [[terminal object]]. In equivalent but extrinsic terms, a Grothendieck topos is localic if it is equivalent to the category of sheaves on a [[locale]] with respect to the topology of jointly epimorphic families. The locale may indeed be taken as the poset of subobjects of 1. 

#Examples#

Every [[Grothendieck topos]] that is a [[category of sheaves]] on (the [[category of open subsets]] of) a [[topological space]] is localic. 

Many familiar toposes $E$, even when they are not localic, can be covered by a localic slice $E/X$ ("covered" means the unique map $X \to 1$ is an epi). For example, if $G$ is a group, then $E = Set^G$ is not itself localic, but it has a localic slice $Set^G/G \simeq Set$ that covers it. These toposes have been dubbed _etendu_ (see Lawvere's 1976 monograph Variable Sets, Etendu, and Variable Structure in Topoi). 

A significant result due to Joyal and Tierney is that for every Grothendieck topos $E$, there exists an open surjection $F \to E$ where $F$ is localic. Using methods of descent theory, they deduce that every Grothendieck topos is equivalent to the category $B G$ of continuous (internally discrete) representations of a localic groupoid $G$. 

This should be regarded as a major extrapolation of Grothendieck's Galois theory (as in SGA 1), where it is shown that the etale topos of a field $k$ is equivalent to the category of continuous discrete representations of the fundamental pro-group $Gal(\bar{k}/k)$, where $\bar{k}$ denotes the separable closure of $k$. It was a watershed event for the penetration of localic methods in topos theory. 

# Generalizations #

In the context of [[(∞,1)-topos]] [[Higher Topos Theory|theory]] there is a notion of [[n-localic (∞,1)-topos]].