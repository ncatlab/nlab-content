#Definition#

A **profinite group** is a [[pro-object]] in the category of [[finite group|finite groups]] (thus it might more precisely be called a pro-(finite group)).  

This means that it is a [[filtered category|cofiltered]] diagram of finite groups, which is thought of as a "formal limit" but the limit is not actually computed.  In most cases, the limit would not actually exist in the category of finite groups, and while it would exist in the category of all groups, it would be "wrong" category-theoretically: maps between profinite groups are not the same as maps between their honest limits in [[Grp]].

However, because of [[Stone duality]], it turns out that maps between profinite groups _are_ the same as maps between their honest limits in the category of [[topological group|topological groups]], where the finite groups are given the discrete topology.  Thus, the category of profinite groups can alternately be defined as the category of topological groups that are filtered inverse limits of finite groups.  Moreover, the topological groups that arise in this way can be characterized as those which are [[Hausdorff space|Hausdorff]], [[compact space|compact]], and [[totally disconnected space|totally disconnected]], giving a more elementary definition.


#Examples#

* A motivating example is the absolute [[Galois group]] of a number field.

* In SGA1, Grothendieck defined the [[algebraic fundamental group]] of a scheme to be a profinite group.  (This is linked with his work on [[pro-representable functor|pro-representable functors]].)

*  Any finite group is profinite!

*  Any group has a [[profinite completion of a group|profinite completion]]. 

*  A profinite group is an [[internalization|internal]] [[group]] object in the category of [[profinite space|profinite spaces]], and conversely.

#Developments from the concept#

* The category of profinite groups has nice 'exactness' properties. The projective limit of a system of profinite groups is an exact functor, unlike its behaviour on groups themselves. To extend this behaviour beyond (pro)finite groups sometimes pro-[[localic groups]] have been used.

* [[profinite completion of a group|Profinite completions]] have been extended from groups to homotopy types for the analysis of finitary properties of the homotopy type. Various constructions in algebraic geometry lead  naturally to [[profinite homotopy type|profinite homotopy types]].

* Subclasses of profinite groups are extensively studied.  For instance, if $p$ is a prime number, a pro-$p$ group is a pro-object in the category of $p$-groups.

* Pro-p analytic groups have been introduced as an analogue of Lie groups, with certain rings of formal power series replacing differentiable functions.

#References#

 A recent textbook is

* L. Ribes and P. Zalesskii, 2000, _Profinite groups_, volume 40 of Ergebnisse der Mathematik und ihrer Grenzgebiete. 3. Folge, Springer-Verlag, 
Berlin. 

For the connections with, amongst other things, Galois theory from a categorical viewpoint:

*  F. Borceux and G. Janelidze, 2001, _Galois theories_, volume 72 of Cambridge Studies in Advanced Mathematics, Cambridge University Press.

For the corresponding 'analytic theory' see:

* J. Dixon, M. du Sautoy, A. Mann and D. Segal, 1999, _Analytic pro-p groups_, volume 61 of Cambridge Studies in Advanced Mathematics, 
Cambridge Univ. Press. 

# To be moved elsewhere soon!# 
+--{: .query}
[[Mike Shulman|Mike]]: The three remarks below don't really seem to belong here; maybe they should go on something like [[profinite homotopy type]].

[[Tim Porter|Tim]]:  That was my eventual intention when others had had a chance to react to my rewrite of this entry.  (By the way I like your rewrite of my rewrite!)
I suspect some entry on &#233;tale homotopy type will also be needed.  (I have a feeling that there may be some useful 'synergy' between this and Andrew's generalsied space stuff, but I may be wrong.)

_Toby_:  (I rewrote the rewrite or the rewrite a bit to make it more a 'narrative', as John says.)

_Mike_: I actually think that the definition as pro-objects in finite-groups should be presented first and emphasized.  I see it as the "real" definition, whereas the fact that you can go ahead and take the inverse limit in topological groups is a nontrivial theorem, which is false for, say, pro-nonfinite-groups.

_Toby_:  Ah, and I thought that it sounded exciting.  'However, there is more to it than that ...' (cue ominous music).  Change it back if you like, I won\'t argue.
=--

* In Algebraic Topology, profinite homotopy types are frequently encountered. This is often because of the use of profinite completions of homotopy types in an attempt to get more information out of the invariants. 

* In the 1960s Artin and Mazur constructed a functor which associates to
each locally noetherian scheme $X$ its &#233;tale homotopy type $X_{et}$ , an object of
$pro\Ho(SSets)$, the [[pro-object|pro-category]] of the homotopy category $Ho(SSets)$ of simplicial sets. They observed that this did not correspond to a homotopy category of a [[model category]] on a category of pro simplicial sets.



* In the 1990s, Morel and Voevodsky, defined a neat framework
for the use of topological methods in algebraic geometry. They embedded the
category of smooth schemes of 'finite type over a field k into a larger category
of 'k-spaces', which carries the structure of a closed model category. The study of these k-spaces is linked to &#233;tale homotopy theory, see Schmidt, _On the &#233;tale homotopy type of
Morel-Voevodsky spaces_, and Isaksen, _Etale realization on the $A^1$-homotopy theory of schemes_. Adv. in Math. 184, 37--63 (2004).
