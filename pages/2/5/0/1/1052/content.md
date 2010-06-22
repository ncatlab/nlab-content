
<div class="rightHandSide toc">
[[!include infinity-limits - contents]]
***
[[!include category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _cocone_ under a [[commuting diagram]] is an [[object]] equipped with [[morphism]]s from each vertex of the diagram into it, such that all new diagrams arising this way commute.

A cocone which is [[universal property|universal]] is a [[colimit]].

The dual notion is _[[cone]]_ .

## Definition

Let $C$ and $D$ be [[category|categories]]; we generally assume that $D$ is [[small category|small]].  Let $f:D\to C$ be a [[functor]] (called a _[[diagram]]_ in this situation). Then a __cocone__ (or _inductive cone_) over $f$ is a a pair $(e,u)$ of an object $e\in C$ and a [[natural transformation]] $u : f\to \Delta e$ (where $\Delta e$ is the [[constant functor|constant diagram]] $\Delta e:D\to C$, $x\mapsto e$, $x\in D$).  

Note that a cocone in $C$ is precisely a [[cone]] in the [[opposite category]] $C^op$.

Terminology for [[natural transformation]]s can also be applied to cocones.  For example, a _component_ of a cocone is a component of the natural transformation $u$; that is, the component for each object $x$ of $D$ is the morphism $u(x): f(x) \to e$.

A __morphism of cocones__ $(e,u)\to (e',u')$ is a morphism $\gamma:e\to e'$ in $C$ such that $\gamma\circ u_x=u'_x$ for all objects $x$ in $D$ (symbolically $(\Delta \gamma)\circ u = u'$); the composition being the composition of underlying morphisms in $C$. Thus cocones form a category whose [[initial object]] if it exists is a [[colimit]] of $f$. 

[[!redirects cocones]]
[[!redirects co-cone]]
[[!redirects co-cones]]