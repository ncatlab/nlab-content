
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Hopf monoids

* table of contents
{: toc}

## Idea

A Hopf monoid is the generalization of a [[Hopf algebra]] to an arbitrary [[symmetric monoidal category]].

## Definition

We work in an arbitrary symmetric monoidal category $\mathcal{C}$ (although one can generalize to a [[braided monoidal category]] or even a [[duoidal category]]).  Recall that a [[bimonoid]] in $\mathcal{C}$ is an object $H$ which is both a [[monoid]] object and a [[comonoid]] object in a compatible way, i.e. the comultiplication and the counit are morphisms of monoids, or equivalently the multiplication and the unit are morphisms of comonoids. (To make sense of this description, one requires the symmetry in order to define the appropriate monoid/comonoid structure on $H \otimes H$; e.g., if $\sigma$ is the symmetry and $\mu$ the monoid multiplication on $H$, the multiplication on $H \otimes H$ is 

$$H \otimes H \otimes H \otimes H \stackrel{1 \otimes \sigma \otimes 1}{\to} H \otimes H \otimes H \otimes H \stackrel{\mu \otimes \mu}{\to} H \otimes H$$ 

where we are writing as if the monoidal product is [[coherence theorem for monoidal categories|strict]]. One can get away with an ambient context of a monoidal category provided that the monoid/comonoid structures in question can be viewed as living in the [[Drinfeld center|center]] of the monoidal category.) 

+-- {: .un_defn}
###### Definition
A **Hopf monoid** is a bimonoid $H$ such that there exists a map $s:H\to H$, called the **antipode**, such that the following diagram commutes
$$
\array{
  H & \xrightarrow{\epsilon} & I & \xrightarrow{\eta} & H\\
  ^{\Delta}\downarrow &&&& \uparrow^{m}\\
  H\otimes H & & \xrightarrow{1\otimes s} & & H\otimes H.
  }
$$
as does the analogous diagram with $1\otimes s$ replaced by $s\otimes 1$.
=--

## Examples

* A Hopf monoid in $Vect$ is precisely a [[Hopf algebra]].

* In a [[cartesian monoidal category]], every [[monoid]] object is a bimonoid in a unique way.  Such a bimonoid is a Hopf monoid exactly when the monoid object is a [[group object]]. More generally, see the corresponding remark [there](https://ncatlab.org/nlab/show/group+object#GroupObjectsInGeneralMonoidalCategories).

## Properties

### Closed monoidal structure on modules
{#ClosedStructureOnModules}

For any bimonoid $H$ in $\mathcal{C}$, the category $Mod_H$ of $H$-[[modules]] inherits a monoidal structure such that the [[forgetful functor]] ("[[fiber functor]]") $Mod_H \to \mathcal{C}$ is [[strong monoidal functor|strong monoidal]]; see _[[bimonoid]]_.  If $H$ is moreover a Hopf monoid and $\mathcal{C}$ is a [[closed monoidal category]], then $Mod_H$ is also closed, and the forgetful functor is strong closed (preserves [[internal homs]]).

This is a special case of [[Tannaka duality]] [for monoids/algebras](Tannaka+duality#ForAlgebraModules), see at _[[structure on algebras and their module categories - table]]_.


Specifically, given $H$-modules $M$ and $N$, we define an $H$-module structure on the internal-hom $Hom(M,N)$ in $\mathcal{C}$ to be the [[adjunct]] of the following composite:
$$
\begin{aligned}
  H \otimes Hom(M,N) \otimes M
  &\xrightarrow{\Delta} H\otimes H \otimes Hom(M,N) \otimes M\\
  &\xrightarrow{\cong} H \otimes Hom(M,N)\otimes H \otimes M\\
  &\xrightarrow{1\otimes 1\otimes s\otimes 1} H \otimes Hom(M,N)\otimes H \otimes M\\
  &\xrightarrow{act} H \otimes Hom(M,N)\otimes M\\
  &\xrightarrow{eval} H \otimes N\\
  &\xrightarrow{act} N.
\end{aligned}
$$
If $\mathcal{C}$ is cartesian and $H$ is a group object, then this is the "conjugation" action, with $g\in H$ sending $f:M\to N$ to $m\mapsto g\cdot f(g^{-1}\cdot m)$.  Diagram chases show that this makes $Hom(M,N)$ an $H$-module and $Mod_H$ a closed monoidal category.

This result can be generalized to algebras over any [[Hopf monad]] (in the sense of Brugui&#232;res-Lack-Virelizier).

## References

A few references emphasizing applications to combinatorics:

* [[Marcelo Aguiar]] and [[Swapneel Mahajan]]. [[Monoidal Functors, Species and Hopf Algebras]], 2010. ([author pdf](http://www.math.cornell.edu/~maguiar/a.pdf))

* [[Marcelo Aguiar]] and [[Swapneel Mahajan]]. Hopf monoids in the category of species. _Contemporary Mathematics_ 585 (2013), 17–124. ([author pdf](http://www.math.cornell.edu/~maguiar/hmonoid.pdf))

* [[Marcelo Aguiar]] and [[Federico Ardila]]. Hopf monoids and generalized permutahedra. [arXiv:1709.07504](https://arxiv.org/abs/1709.07504)

## Related concepts

* [[bimonoid]], [[Frobenius monoid]]

* [[Hopf algebra]]

* [[Hopf monoidal category]]

* [[Hopf monad]]



[[!redirects Hopf monoids]]
