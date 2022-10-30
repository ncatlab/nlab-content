
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
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

## Idea

An ordinary [[group]] is either an [[abelian group]] or not. For an [[∞-group]] there is an infinite tower of notions ranging from completely non-abelian to completely abelian. An _abelian ∞-group_ is one which is maximally abelian. This is equivalently a [[connective spectrum object]].

## Proposition

### Relation to commutative $\infty$-rings

+-- {: .num_defn #GroupOfUnitsFunctor} 
###### Definition

Write

$$
  gl_1 \; \colon \;  CRing_\infty \to AbGrp_\infty
$$

for the [[(∞,1)-functor]] which sends a [[E-∞ ring|commutative ∞-ring]] to its [[∞-group of units]]. 

=--

+-- {: .num_defn}
###### Definition

The [[∞-group of units]] [[(∞,1)-functor]] of def. \ref{GroupOfUnitsFunctor} is a  right-[[adjoint (∞,1)-functor]] (or at least a [[right adjoint]] on [[homotopy category of an (∞,1)-category|homotopy categories]])

$$
  CRing_\infty 
  \stackrel{\overset{\mathbb{S}[-]}{\leftarrow}}{\underset{gl_1}{\to}}
  AbGrp_\infty
  \,.
$$

=--

This is ([ABGHR 08, theorem 2.1](#ABGHR08)).


## Examples

* A [[0-truncated]] abelian $\infty$-group is equivalently an [[abelian group]].

* A [[1-truncated]] abelian $\infty$-group is equivalently a [[symmetric 2-group]].

* A [[2-truncated]] abelian $\infty$-group is equivalently a [[symmetric 3-group]].

## Related concepts


[[!include k-monoidal table]]


* [[∞-group]], [[k-tuply groupal n-groupoid]]

* [[braided ∞-group]],

  * [[braided 2-group]]

  * [[braided 3-group]]

* [[sylleptic ∞-group]]

  * [[sylleptic 3-group]]

* **abelian ∞-group**

  * [[abelian group]]

  * [[abelian 2-group]]

  * [[abelian 3-group]]

## References

General discussion is in section 5 of 

* [[Jacob Lurie]], _[[Higher Algebra]]_

Discussion in the context of [[E-∞ rings]] and [[twisted cohomology]] is in 

* [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], [[Michael Hopkins]], [[Charles Rezk]], _Units of ring spectra and Thom spectra_ ([arXiv:0810.4535](http://arxiv.org/abs/0810.4535))
 {#ABGHR08}

[[!redirects k-monoidal ∞-group]]

[[!redirects abelian ∞-group]]
[[!redirects abelian ∞-groups]]

