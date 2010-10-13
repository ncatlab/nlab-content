
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

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

Objects in a gros topos may be thought of as [[space]]s _modeled on $S$_ in the sense described at [[motivation for sheaves, cohomology and higher stacks]] and at [[space]].

Also the objects in a petit topos $Sh(Op(X))$ -- a [[category of sheaves]] on the [[category of open subsets]] of a [[topological space]] $X$ -- are a kind of generalized spaces, but generalized spaces _over $X$_ on which the rigid structure of morphisms in $Op(X)$ (only inclusions of subsets, no more general maps) induces a correspondingly rigid structure so that they are not all that general. In fact, $Sh(Op(X))$ is equivalent to [[etale space]]s over $X$.

There is another notion of 'large' topos associated to a space $X$ (or more generally an object in a site), namely the topos of sheaves on the [[slice category]] $Top/X$, with the obvious notion of covering family; a family is covering if it is so under the functor $Top/X \to Top$. This site is often referred to as the [[large site of an object in a site|large site]] of $X$, as compared to the [[small site]], which is $Op(X)$ as above. The topos $Sh(Top/X)$ can be viewed as spaces modelled [[Top]] (or more generally some site), but parameterised by the representable sheaf $X$.

## Definition

* The **petit topos of an object $a$ in a site $(C,J)$** is the category of sheaves on the [[small site]] of $a$.

* A proposed axiomatization of the notion of gros topos is that of a [[cohesive topos]].


## Examples

For $X$ a [[topological space]], the _petit topos_ that it defines is the [[category of sheaves]] $Sh(X) := Sh(Op(X))$ on the [[category of open subsets]] of $X$. A general object in this topos is an [[etale space]] over $X$. The space $X$ itself is incarnated as the [[terminal object]] $X = * \in Sh(X)$.

A _gros topos_ in which $X$ is incarnated is a [[category of sheaves]] on a [[site]] of test spaces with which $X$ may be probed. For instance for $C =$ [[Top]], or [[Diff]] or [[CartSp]] with their standard [[coverage]]s, $Sh(C)$ is such a gros topos.

In good cases the intrinsic properties of $X$ do not depend on whether one regards it as an object of a petit or a gros topos. For instance at [[cohomology]] in the section <a href="http://ncatlab.org/nlab/show/cohomology#NonabelianSheafCohomology">Nonabelian sheaf cohomology with constant coefficients</a> it is discussed how the [[nonabelian cohomology]] of a [[paracompact space|paracompact]] [[manifold]] $X$ with constant coefficients gives the same answer in each case.

## References

Some aspects of an axiomatic characterization of petit vs. gros toposes is in 

* [[Bill Lawvere]], _Axiomatic cohesion_ Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))

There is also something relevant in this article:

* [[Mathieu Anel]], _Grothendieck topologies from unique factorization systems_ ([arXiv:0902.1130](http://arxiv.org/abs/0902.1130))

* [[Mamuka Jibladze]], _Homotopy types for "gros" toposes_, thesis, [pdf](http://www.rmi.acnet.ge/~jib/thesis.pdf)

[[!redirects gros topos]]