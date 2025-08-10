
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .un_defn}
###### Definition

A [[site]] is called a **local site** if

* it has a [[terminal object]] $*$;

* the only [[covering]] family of $*$ is the trivial cover.

=--

This appears as ([Johnstone example C.3.6.3 (d) ](#Johnstone)).

## Properties

+-- {: .un_prop}
###### Proposition

The [[category of sheaves]] $Sh(C)$ on a local site $C$ is a [[local topos]].

=--

+-- {: .proof}
###### Proof


Since $C$ has a terminal object, the [[global section]] functor $Sh(C) \to Set$ is given by evaluation on that object, hence is precomposition of sheaves with the inclusion $* \to C$. At the level of presheaves this has a right [[Kan extension]] functor, given by sending a set $S$ to the presheaf

$$
  \nabla S : U \mapsto S^{C(*,U)}
  \,.
$$

This is indeed a sheaf if $*$ is covered only by the trivial cover.


=--

See ([Johnstone example C.3.6.3 (d) ](#Johnstone)).


## Examples

* [[CartSp]]

## Related concepts

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

  * [[connected topos]] / [[∞-connected (∞,1)-topos]]

  * [[strongly connected topos]] / [[strongly ∞-connected (∞,1)-topos]]

  * [[totally connected topos]] / [[totally ∞-connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* [[cohesive topos]] / [[cohesive (∞,1)-topos]]

and

* [[locally connected site]] / [[locally ∞-connected site]]

  * [[connected site]] / [[∞-connected site]]

  * [[strongly connected site]] / [[strongly ∞-connected site]]

  * [[totally connected site]] / [[totally ∞-connected site]]

* **local site** / [[∞-local site]]

* [[cohesive site]], [[(∞,1)-cohesive site]]

## References

The definition appears as example C.3.6.3 (d) in 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_
{#Johnstone}

[[!redirects local sites]]