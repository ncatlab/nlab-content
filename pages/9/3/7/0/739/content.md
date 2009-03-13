#Definition#

The most elementary definition of a **profinite group** is a Hausdorff, compact, totally disconnected [[topological group]].  However, there is more to it than that.

The slickest definition of a **profinite group** is a [[pro-object]] in the category of [[finite group|finite groups]], what one might call a pro-(finite group).  In other words, it is a [[filtered category|cofiltered]] diagram of finite groups, which is thought of as a "formal limit" but the limit is not actually computed.  In most cases, the limit would not actually exist in the category of finite groups, and while it would exist in the category of all groups, it would be "wrong" category-theoretically: maps between profinite groups are not the same as maps between their honest limits in [[Grp]].

However, because of [[Stone duality]], it turns out that maps between profinite groups _are_ the same as maps between their honest limits in the category of [[topological group|topological groups]], where the finite groups are given the discrete topology.  Thus, the category of profinite groups can alternately be defined as the category of topological groups that are filtered inverse limits of finite groups.  Moreover, the topological groups that arise in this way can be characterized as those which are Hausdorff, compact, and totally disconnected, giving the more elementary definition above.


#Examples#

* A motivating example is the absolute [[Galois group]] of a number field.

* In SGA1, Grothendieck definied the fundamental group of a scheme to be a profinite group.  (This is linked with his work on [[pro-representable functor|pro-representable functors]].)

#Developments from the concept#

* The category of profinite groups has nice 'exactness' properties. The projective limit of a system of profinite groups is an exact functor, unlike its behaviour on groups themselves. To extend this behaviour beyond (pro)finite groups sometimes pro-localic groups have been used.

+--{: .query}
[[Mike Shulman|Mike]]: The three remarks below don't really seem to belong here; maybe they should go on something like [[profinite homotopy type]].

[[Tim Porter|Tim]]:  That was my eventual intention when others had had a chance to react to my rewrite of this entry.  (By the way I like your rewrite of my rewrite!)
I suspect some entry on &#233;tale homotopy type will also be needed.  (I have a feeling that there may be some useful 'synergy' between this and Andrew's generalsied space stuff, but I may be wrong.)

_Toby_:  (I rewrote the rewrite or the rewrite a bit to make it more a 'narrative', as John says.)

_Mike_: I actually think that the definition as pro-objects in finite-groups should be presented first and emphasized.  I see it as the "real" definition, whereas the fact that you can go ahead and take the inverse limit in topological groups is a nontrivial theorem, which is false for, say, pro-nonfinite-groups.
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
