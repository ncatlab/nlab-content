# Profinite groups
* table of contents
{: toc}


## Definition

A **profinite group** is a [[pro-object]] in the category of [[finite group|finite groups]] (thus it might more precisely be called a pro-(finite group)).  

This means that it is a [[filtered category|cofiltered]] diagram of finite groups, which is thought of as a "formal limit" but the limit is not actually computed.  In most cases, the limit would not actually exist in the category of finite groups, and while it would exist in the category of all groups, it would be "wrong" category-theoretically: maps between profinite groups are not the same as maps between their honest limits in [[Grp]].

However, because of [[Stone duality]], it turns out that maps between profinite groups _are_ the same as maps between their honest limits in the category of [[topological group|topological groups]], where the finite groups are given the discrete topology.  Thus, the category of profinite groups can alternately be defined as the category of topological groups that are filtered inverse limits of finite groups.  Moreover, the topological groups that arise in this way can be characterized as those which are [[Hausdorff space|Hausdorff]], [[compact space|compact]], and [[totally disconnected space|totally disconnected]], giving a more elementary definition. In other words, their underlying topological spaces are [[profinite space|profinite]].


## Examples

* A motivating example is the absolute [[Galois group]] of a number field.

* In SGA1, Grothendieck defined the [[algebraic fundamental group]] of a scheme to be a profinite group.  (This is linked with his work on [[pro-representable functor|pro-representable functors]].)

*  Any finite group is profinite!

*  Any group has a [[profinite completion of a group|profinite completion]]. 

*  A profinite group is an [[internalization|internal]] [[group]] object in the category of [[profinite space|profinite spaces]], and conversely.


## Developments from the concept

* The category of profinite groups has nice 'exactness' properties. The projective limit of a system of profinite groups is an exact functor, unlike its behaviour on groups themselves. To extend this behaviour beyond (pro)finite groups sometimes pro-[[localic groups]] have been used; see [[progroup]].

* [[profinite completion of a group|Profinite completions]] have been extended from groups to homotopy types for the analysis of finitary properties of the homotopy type. Various constructions in algebraic geometry lead  naturally to [[profinite homotopy type|profinite homotopy types]].

* Subclasses of profinite groups are extensively studied.  For instance, if $p$ is a prime number, a pro-$p$ group is a pro-object in the category of $p$-groups.

* Pro-p analytic groups have been introduced as an analogue of Lie groups, with certain rings of formal power series replacing differentiable functions.


## References

 A recent textbook is

* L. Ribes and P. Zalesskii, 2000, _Profinite groups_, volume 40 of Ergebnisse der Mathematik und ihrer Grenzgebiete. 3. Folge, Springer-Verlag, 
Berlin. 

For the connections with, amongst other things, Galois theory from a categorical viewpoint:

* [[Francis Borceux]], [[George Janelidze]], _[[Galois Theories]]_, Cambridge Studies in Advanced Mathematics __72__, Cambridge University Press, 2001.

For the corresponding 'analytic theory' see:

* J. Dixon, M. du Sautoy, A. Mann and D. Segal, _Analytic pro-p groups_, volume 61 of Cambridge Studies in Advanced Mathematics, 
Cambridge Univ. Press 1999. 


[[!redirects profinite group]]
[[!redirects profinite groups]]
[[!redirects pro-finite group]]
[[!redirects pro-finite groups]]
