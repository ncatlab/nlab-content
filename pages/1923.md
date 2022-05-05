
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _symmetric monoidal functor_ is a [[functor]] $F : C \to D$ between [[symmetric monoidal category|symmetric monoidal categories]] that is a [[monoidal functor]] which respects the symmetry on both sides.

## Definition

A [[monoidal functor]] $F : (C,\otimes) \to (D, \otimes)$ between [[symmetric monoidal categories]] is **symmetric** if for all $A,B \in C$ the diagram

$$
  \array{
    F A \otimes F B &\stackrel{\sigma}{\to}& F B \otimes F A
    \\
    {}^{\mathllap{\nabla_{A,B}}}\downarrow 
    && 
    \downarrow^{\mathrlap{\nabla_{B,A}}}
    \\
    F(A\otimes B) &\stackrel{F(\sigma)}{\to}& F(B \otimes A)
  }
$$

commutes, where $\sigma$ denotes the symmetry isomorphism both of $C$ and $D$.

As long as it goes between symmetric monoidal categories a symmetric monoidal functor is the same as a [[braided monoidal functor]]. 

## Properties

+-- {: .num_prop #SymmetricMonoidalFunctorInducesFunctorOnCommutativeMonoids}
###### Proposition
**([[symmetric monoidal functor]] induces [[functor]] on [[commutative monoid in a symmetric monoidal category|commutative monoids]])**


A symmetric monoidal functor 

$$
  \left(\mathcal{C}_1, \otimes_1, \tau_1\right)
  \longrightarrow
  \left(\mathcal{C}_2, \otimes_2, \tau_2\right)
$$

between two symmetric monoidal categories canonically preserves [[commutative monoid in a symmetric monoidal category|commutative monoids]] and extends to a functor between categories of commutative monoids (see [here](geometry+of+physics+--+categories+and+toposes#MonoidsPreservedByLaxMonoidalFunctor) for more)

$$
  CMon\left(\mathcal{C}_1, \otimes_1, \tau_1\right)
  \longrightarrow
  CMon\left(\mathcal{C}_2, \otimes_2, \tau_2\right)
$$

=--

## Examples 

+-- {: .num_example #IdentityFunctorOnCategoryOfChainComplexesOfSuperVectorSpaces}
###### Example
**([[identity functor]] on [[category of chain complexes of super vector spaces]])**

The [[category of chain complexes of super vector spaces]] $Ch(Supervect)$ equipped with the [[tensor product of chain complexes]] carries two [[symmetric monoidal category|symmetric]] [[braidings]], $\tau_{Deligne}$ and $\tau_{Bernst}$ ([this Prop.](chain+complex+in+super+vector+spaces#SymmetricStructureOnCategoryOfChainComplexesOfSuperVectorSpaces)). The [[identity functor]] on $Ch(SuperVect)$ carries the structure of a [[strong monoidal functor|strong]] symmetric monoidal functor with respect to these two, making them equivalent. By Prop. \ref{SymmetricMonoidalFunctorInducesFunctorOnCommutativeMonoids} this in turn induces an [[equivalence of categories|equivalence]] on the catories of commutative monoids, which in this case are [[differential graded-commutative superalgebras]], with one of two equivalent grading conventions

$$
  dgcsAlg_{Deligne} \;\simeq\; dgcsAlg_{Bernstein}
$$

[[!include sign rules in homological superalgebra -- table]]



=--


## Related concepts

* [[monoidal functor]]

* [[strong monoidal functor]]

* [[lax monoidal functor]]

* [[oplax monoidal functor]]

* [[bilax monoidal functor]]

* [[Frobenius monoidal functor]]

* [[braided monoidal functor]]

* **symmetric monoidal functor**

## References

An exposition is in

* [[John Baez]], [Some definitions everyone should know](http://math.ucr.edu/home/baez/qg-fall2004/definitions.pdf).


[[!redirects symmetric monoidal functor]]
[[!redirects symmetric monoidal functors]]
