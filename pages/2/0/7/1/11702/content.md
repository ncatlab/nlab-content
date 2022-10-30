[[!redirects cohesive ∞-presheaf on E-∞ rings]]

> This entry is about a weak representability condition on [[(∞,1)-presheaves]] in [[E-∞ geometry]]. Intuitively this expresses similar behaviour as discussed at _[[cohesion]]_ and _[[infinitesimal cohesion]]_, but the definitions themselves are independent and unrelated and apply in somewhat disjoint contexts.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Write $CRing_\infty^{cn}$ for the [[(∞,1)-category]] of [[connective]] [[E-∞ rings]]. 

+-- {: .num_defn #CohesiveFunctor}
###### Definition

An [[(∞,1)-functor]]

$$
  X \;\colon\; CRing_\infty^{cn}\longrightarrow \infty Grpd
$$

([[(∞,1)-presheaf]] on $(CRing_\infty^{cn})^{op}$) is called _cohesive_ ([Lurie Rep, def. 2.1.1](#LurieRep)) if it sends [[(∞,1)-fiber products]] of [[morphisms]] which are [[surjection|surjective]] on $\pi_0$ to [[(∞,1)-fiber products]].

If at least those fiber products whose [[kernels]] are [[nilpotent ideals]] are preserved, then $X$ is called _infinitesimally cohesive_. 

=--

([Lurie Rep, def. 2.1.9](#LurieRep)).

+-- {: .num_remark}
###### Remark

Infinitesimal cohesion, def. \ref{CohesiveFunctor}, is (together with the property that the base ring is sent to a contractible space) the defining property that makes such a functor a _[[formal moduli problem]]_, hence equivalently an [[L-∞ algebra]]. It is also one of the characteristics of a [[Deligne-Mumford stack]], due to the [[Artin-Lurie representability theorem]], hence it is satisfied by those functors which are infinitesimal approximations to [[geometric infinity-stacks]].

=--

## References

* {#LurieRep} [[Jacob Lurie]], section 2.1 of _[[Representability theorems]]_

[[!redirects cohesive (∞,1)-presheaves on E-∞ rings]]

[[!redirects cohesive (infinity,1)-presheaf on E-infinity rings]]
[[!redirects cohesive (infinity,1)-presheaves on E-infinity rings]]

[[!redirects infinitesimally cohesive (∞,1)-presheaf on E-∞ rings]]
[[!redirects infinitesimally cohesive (∞,1)-presheaves on E-∞ rings]]
[[!redirects infinitesimally cohesive (infinity,1)-presheaf on E-infinity rings]]
[[!redirects infinitesimally cohesive (infinity,1)-presheaves on E-infinity rings]]

