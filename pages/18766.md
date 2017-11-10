
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# Linear hyperdoctrines

* table of contents
{: toc}

## Idea

A *linear hyperdoctrine* is a [[hyperdoctrine]] that is adapted for modeling first-order [[linear logic]].

## Definitions

Since there are many variants of linear logic, there are correspondingly many variants of linear hyperdoctrines, but all of them are some kind of [[indexed monoidal category]], or more precisely indexed monoidal poset.  We mention only a few of the most important.

+-- {: .un_defn}
###### Definition
A **MILL hyperdoctrine** is a closed indexed monoidal poset with [[indexed products]] and indexed coproducts satisfying the [[Beck-Chevalley condition]] and the [[Frobenius reciprocity]] condition.
=--

A MILL hyperdoctrine models predicate intuitionistic linear logic, with $\otimes,\mathbf{1},\multimap,\exists,\forall$.

+-- {: .un_defn}
###### Definition
A **MALL hyperdoctrine** is a MILL hyperdoctrine whose fibers are [[star-autonomous categories|*-autonomous]] [[lattices]] and whose reindexing functors preserve all the $\ast$-autonomous and lattice structure.
=--

A MALL hyperdoctrine models predicate classical linear logic without exponentials, with $\otimes,\mathbf{1},\parr,\bot,\&,\top,\oplus,\mathbf{0},\exists,\forall$.

+-- {: .un_defn}
###### Definition
A **linear-nonlinear hyperdoctrine** is a MALL hyperdoctrine $L$ together with a [[first-order hyperdoctrine]] $M$ and a fiberwise [[monoidal adjunction]] $F : M \rightleftarrows L : G$.
=--

A linear-nonlinear hyperdoctrine models full predicate classical linear logic, with the [[!-modality]] modeled as the comonad $F G$ and $?$ as its de Morgan dual.

## References

*  [[R. A. G. Seely]],  _Linear logic, $\ast$-autonomous categories and cofree coalgebras_, _Contemporary Mathematics_ 92, 1989.  ([[SeelyLinearLogic.pdf:file]], [ps.gz](http://www.math.mcgill.ca/rags/nets/llsac.ps.gz))
 {#Seely89}

[[!redirects linear hyperdoctrines]]
