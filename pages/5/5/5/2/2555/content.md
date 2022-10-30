+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homotopy Theory
+-- {: .hide}
[[ !include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The concept of a **cylinder object** in a [[category]] is an abstraction of the construction in [[Top]] which associates to any [[topological space]] $X$ the _cylinder_ $X \times [0,1]$ over $X$, where $[0,1]$ is the standard [[interval]]. It is notably used to define the concept of [[left homotopy]], say in a [[model category]].

The standard topological cylinder $X \times [0,1]$ naturally comes equipped with a continuous map

$$
  X \coprod X \to X \times [0,1]
$$

that identifies $X$ as the two ends $X \times \{0\}$ and $X \times \{1\}$ of the cylinder, and with a map

$$
  X \times [0,1] \to X
$$

that collapses the cylinder back onto $X$.

The composite of these two maps is the [[codiagonal]] $(Id,Id) :  X \coprod X \to X$. Moreover, the cylinder $X \times [0,1]$ is [[homotopy equivalence|homotopy equivalent]] to $X$. 

These properties are the characterizing properties of the cylinder that can be abstracted and realized in other categories.

The notion dual to _cylinder object_ is [[path space object]], which is thus sometimes alternatively called a cocylinder. Cylinder objects and path space objects are used to define [[left homotopies]] and [[right homotopies]], respectively.


There are several views on the role of cylinders /  cocylinders in homotopy theory. If there is a natural notion of weak equivalence or [[quasi-isomorphism]] then the cylinder is used to encode a notion of homotopy equivalence compatible with the weak equivalences. In some other situations, a 'cylinder' , often functorially given and well structured in some way, may be the _primitive_ notion that allows a notion of 'homotopy equivalence' to be put forward.  Below we give a definition optimised for the former situation. Some indication of the second context is given in the entry [[cylinder functor]].

## Definition

In a [[category with weak equivalences]] $C$ that has [[coproducts]] a **cylinder object** $Cyl(X)$ for an [[object]] $X$ is a factorization

$$
  X \coprod X \to Cyl(X) \stackrel{\simeq}{\to} X
$$

of the codiagonal $X \coprod X \to X$ out of the [[coproduct]] of $X$ with itself, such that $Cyl(X) \to X$ is a weak equivalence and such that the morphism $X \coprod X \to Cyl(X)$ is "nice" in some way.

In some situations the assignment of cylinder objects may exist functorially, in which case one speaks of a [[cylinder functor]].

If $C$ has the structure of a [[model category]] then "nice" means that $X \coprod X \hookrightarrow Cyl(X)$ is a [[cofibration]].  The factorization axiom of a model category ensures that for each object there is a cylinder object with this property; in fact, one with the additional property that $Cyl(X) \to X$ is an acyclic fibration.  Cylinder objects such that $X \coprod X \hookrightarrow Cyl(X)$ is a cofibration are sometimes called *good*, and those for which moreover $Cyl(X) \to X$ is an acyclic fibration are then called *very good*.

## Examples

* In [[sSet]] equipped with the standard [[model structure on simplicial sets]] the standard cylinder object for any $S \in sSet$ is $S \times \Delta[1]$.

* In [[Top]], the standard cylinder $X\times [0,1]$ is a cylinder object for both the [[classical model structure on topological spaces]] $Top_{Quillen}$ (the one with [[Serre fibrations]]) as well as for the [[Strøm model structure]] $Top_{Strom}$ (the one with [[Hurewicz fibrations]]).

  This standard cylinder is generally a "good cylinder" in the above sense only for $Top_{Stron}$  (in which case it is in fact a "very good cylinder").

  In $Top_{Quillen}$ a sufficient condition for the standard cylinder $X\times I$ to be good is that $X$ is a [[CW-complex]].

## Related concepts

* [[cylinder functor]]

* [[left homotopy]]

* [[mapping cylinder]]

* [[path space object]]

* [[reduced cylinder]]

* [[cylinder spectrum]]

## References

The precise argument that for $X$ a [[cell complex]] then also the standard cyclinder $X\times I$ is a cell complex is spelled out for instance as prop. 2.9 in 

* {#Ottina14} Ottina, _An A-based cofibrantly generated model category_ ([arXi:1405.2086](http://arxiv.org/abs/1405.2086))



[[!redirects cylinder objects]]
[[!redirects cylinder]]
[[!redirects cylinders]]
