
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include algebra - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[classical mathematics]], every [[Heyting field]] is a [[discrete field]], which means that the [[residue field]] of a [[local ring]] is automatically a discrete field. However, in [[constructive mathematics]], there are Heyting fields which are not discrete fields, which means that there are local rings whose residue fields are not discrete fields. Hence, the concept of a *residually discrete local ring* in constructive mathematics, where the residue field of the local ring is a discrete field. 

+-- {: .standout}
Warning: residually discrete locally rings are not the same as *discrete local rings*, which are local rings which are also [[discrete rings]]. In [[constructive mathematics]], there exist residually discrete local rings which are not discrete, such as [[power series rings]] of [[discrete fields]], which are residually discrete [[local integral domain|local]] [[Heyting integral domains]] that are not provably [[discrete integral domains]]. 
=--

## Definition

A [[local ring]] is a **residually discrete local ring** if any of the following equivalent conditions hold:

* The [[residue field]] of the local ring is a [[discrete field]]

* The [[apartness relation]] of the local ring is a [[decidable relation]]

* Every element of the local ring is either invertible or noninvertible

## Examples

* Every [[discrete field]] is a residually discrete local ring. 

* Given any [[discrete field]] $K$, any [[local Artinian algebra|local Artinian $K$-algebra]] is a residually discrete local ring whose residue field is $K$.

  * Given a [[prime number]] $p$ and a positive natural number $n$, the [[prime power local ring]] $\mathbb{Z}/p^n\mathbb{Z}$ is a residually discrete local ring whose residue field is the finite field $\mathbb{Z}/p\mathbb{Z}$. 

  * Given a [[prime number]] $p$, the ring of [[p-adic integers]] $\mathbb{Z}_p$ is a residually discrete local ring whose residue field is the finite field $\mathbb{Z}/p\mathbb{Z}$. 

  * Given a [[discrete field]] $K$, the [[power series ring]] $K[[x]]$ is a residually discrete local ring whose residue field is $K$ itself. 

* In the presence of [[excluded middle]], every [[local ring]] is a residually discrete local ring. 

## Related concepts

* [[discrete field]]

* [[residue field]]

* [[local ring]]

* [[weak local ring]]

## References

* {#LombardiQuitté2010} [[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) ([doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf))

[[!redirects residually discrete local ring]]
[[!redirects residually discrete local rings]]