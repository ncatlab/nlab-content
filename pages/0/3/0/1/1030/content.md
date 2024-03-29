
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

+-- {: .num_defn}
###### Definition

In a [[category]] $C$ with [[zero object]] $0$ the **zero morphism ** $0_{c,d} : c \to d$ between two [[object]]s $c, d \in C$ is the unique [[morphism]] that factors through $0$:

$$
  0_{c,d} : c \to 0 \to d
  \,.
$$


More generally, in any category [[enriched category|enriched]] over the [[closed monoidal category|closed monoidal]] [[category of pointed sets]] (with [[tensor product]] the [[smash product]]), the **zero morphism** $0_{c,d} : c \to d$ is the basepoint of the [[hom-object]] $[c,d]$.

=--

+-- {: .num_remark}
###### Remark

In fact, an enrichment over pointed sets consists precisely of the choice of a 'zero' morphism $0_{c,d}:c\to d$ for each pair of objects, with the property that $0_{c,d} \circ f = 0_{b,d}$ and $f\circ 0_{a,b} = 0_{a,c}$ for any morphism $f:b\to c$.  Such an enrichment is unique if it exists, for if we are given a different collection of zero morphisms $0'_{c,d}$, we must have
$$0'_{c,d} = 0'_{c,d} \circ 0_{c,c} = 0_{c,d}$$
for any $c,d$.  Thus, the existence of zero morphisms can be regarded as a [[stuff, structure, property|property]] of a category, rather than structure on it.  (To be more precise, it is an instance of [[property-like structure]], since not every functor between categories with zero morphisms will necessarily preserve the zero morphisms, although an [[equivalence of categories]] will.)

=--


## Examples

See at _[[zero object]]_ for examples.


## Related concepts

* [[zero]]

* [[zero function]]

* [[null homotopy]]


[[!redirects zero morphism]]
[[!redirects zero morphisms]]
[[!redirects zero map]]
[[!redirects zero maps]]
