
<div class="rightHandSide toc">
[[!include topos theory - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Recall that a [[Grothendieck topos]] $T$ is a [[category of sheaves]] $T = Sh(S)$ on some [[site]] $S$.

If $S = Op(X)$ is the [[category of open subsets]] of a [[topological space]] $X$ (or some [[manifold]] or the like) then one calls $T$ a **petit topos**. 

If $S$ on the other hand is a category of _all test [[space]]s_ in some sense, such as

* the category [[Top]] of all [[topological space]]s;

* the category [[Diff]] of all smooth [[manifold]]s

etc. one call $T$ a **gros topos** .

Objects in a gros topos may be thought of as [[space]]s _modeled on $S$_ in the sense described at [[motivation for sheaves, cohomology and higher stacks]].

Also the objects in a petit topos $Sh(Op(X))$ are a kind of generalized spaces, but generalized spaces _over $X$_ on which the rigid structure of morphisms in $Op(X)$ (only inclusions of subsets, no more general maps) induces a correspondingly rigid structure so that they are not all that general. In fact, $Sh(Op(X))$ is equivalent to [[etale space]]s over $X$.


## Examples

For $X$ a [[topological space]], the _petit topos_ that it defines is the [[category of sheaves]] $Sh(X) := Sh(Op(X))$ on the [[category of open subsets]] of $X$. A general object in this topos is an [[etale space]] over $X$. THe space $X$ itself is incarnated as the [[terminal object]] $X = * \in Sh(X)$.

A _gros topos_ in which $X$ is incarnated is a [[category of sheaves]] on a [[site]] of test spaces with which $X$ may be probed. For instance for $C =$ [[Top]], or [[Diff]] or [[CartSp]] with their standard [[coverage]]s, $Sh(C)$ is such a gros topos.

In good cases the intrinsic properties of $X$ do not depend on whether one regards it as an object of a petit or a gros topos. For instance at [[cohomology]] in the section <a href="http://ncatlab.org/nlab/show/cohomology#NonabelianSheafCohomology">Nonabelian sheaf cohomology with constant coefficients</a> it is discussed how the [[nonabelian cohomology]] of a [[paracompact space|paracompact]] [[manifold]] $X$ with constant coefficients gives the same answer in each case.

## References

Some aspects of an axiomatic characterization of petit vs. gros toposes is in 

* [[Bill Lawvere]], _Axiomatic cohesion_ Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))



[[!redirects gros topos]]