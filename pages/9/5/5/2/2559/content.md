<div class="rightHandSide toc">
[[!include synthetic differential geometry - contents]]
***
[[!include compact object - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

#Definition#

[[Bill Lawvere]]'s definition of an _atomic_ [[infinitesimal space]] is as an [[object]] $\Delta$ in a [[topos]] $\mathcal{T}$ such that the [[inner hom]] [[functor]] $(-)^\Delta : \mathcal{T} \to \mathcal{T}$ has a [[right adjoint]].

Notice that by definition of [[inner hom]], $(-)^\Delta$ always has a [[left adjoint]]. A [[right adjoint]] can only exist for very particular objects. Therefore the term **amazing right adjoint**

# right adjoints to representable exponentials #

Assume $\mathcal{T} = Sh(C)$ is a [[Grothendieck topos]], that the [[Grothendieck topology]] on the [[site]] $C$ is [[subcanonical coverage|subcanonical]]. Let $\Delta \in C \hookrightarrow Sh(C)$ be a [[representable functor|representable object]]. 

Then $(-)^\Delta$ has a [[right adjoint]], hence $\Delta$ is an atomic [[infinitesimal space]],  precisely if it preserves [[colimit]]s.

For if $(-)^\Delta$ preserves colimits, its [[right adjoint]] is

$$
 (-)_\Delta : (Y \in Sh(C)) \mapsto (U \mapsto Sh_C(U^\Delta, Y))
  \,.
$$ 

The $Y_\Delta$ defined this way is indeed a sheaf, due to the assumption that $(-)^\Delta$ preserves colimits. So this is indeed a [[right adjoint]].



#References#

appendix 4 of

* [[Ieke Moerdijk]], [[Gonzalo Reyes]], [[Models for Smooth Infinitesimal Analysis]]