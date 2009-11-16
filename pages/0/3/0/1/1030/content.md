In a [[category]] $C$ with [[zero object]] $0$ the **zero morphism ** $0_{c,d} : c \to d$ between two objects $c, d \in C$ is the unique [[morphism]] that factors through $0$:
$$
  0_{c,d} : c \to 0 \to d
  \,.
$$
See [[zero object]] for examples.

More generally, in any category [[enriched category|enriched]] over the [[closed monoidal category]] of [[pointed sets]] (with [[smash product]]), the **zero morphism** $0_{c,d} : c \to d$ is the basepoint of the [[hom-object]] $[c,d]$.

In fact, an enrichment over pointed sets consists precisely of the choice of a 'zero' morphism $0_{c,d}:c\to d$ for each pair of objects, with the property that $0_{c,d} \circ f = 0_{b,d}$ and $f\circ 0_{a,b} = 0_{a,c}$ for any morphism $f:b\to c$.  Such an enrichment is unique if it exists, for if we are given a different collection of zero morphisms $0'_{c,d}$, we must have
$$0'_{c,d} = 0'_{c,d} \circ 0_{c,c} = 0_{c,d}$$
for any $c,d$.  Thus, the existence of zero morphisms can be regarded as a [[stuff, structure, property|property]] of a category, rather than structure on it.  (Actually, it is more properly an instance of [[property-like structure]], since not ever functor between categories with zero morphisms will necessarily preserve the zero morphisms.)

[[!redirects zero morphisms]]
