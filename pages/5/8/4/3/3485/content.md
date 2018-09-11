

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

Let $C$ be a [[groupoid]].

A _permutation representation_ of $C$ is a [[representation]] of $C$ on [[Set]], i.e. a [[functor]] $C \to \Set$, also called a [[G-set]]. 

A _linear permutation representation_ is a functor $C \to $ [[Vect]] that factors through a permutation representation via the [[free functor]] $k^{|-|}\colon  Set \to Vect$ which sends a set to the vector space for which this set is a basis.

+-- {: .un_remark}
###### Warning
In the usual literature of [[representation theory]], "linear permutation representations" are just called "permutation representations".
=--


## Examples

Notably for $C = \mathbf{B}G$ the [[delooping]] [[groupoid]] of a [[group]] $G$, a permutation representation $\mathbf{B}G \to Set$ is a set equipped with a $G$-[[action]].

The category 

$$
  Rep(G, Set) \simeq PSh(\mathbf{B} G)
$$

is the [[classifying topos]] for the group $G$.

For other general perspectives on this see also at _[[infinity-action]]_ the section _[Examples -- Discrete group actions on sets](infinity-action#ExamplesPermutationRepresentations)_.

+-- {: .num_example #AutomorphismsOfGAsGTorsor}
###### Example

Let $G$ be a [[group]]. The [[automorphism group]] of $G$ regarded as a permutation representation of itself via left multiplication, is [[isomorphism|isomorphic]] to $G$:

$$
  G 
   \;\simeq\;
  Aut_{G Set}(G,G)
$$

=--

(See also at _[[torsor]]_.)

+-- {: .proof}
###### Proof

Consider an function

$$ 
  f \;\colon\; G \longrightarrow G
  \,.
$$

By $G$-equivariance, its value on any $g \in G$ is fixed by its value on the [[neutral element]] $1$

$$
  f(g) = f(g \cdot 1) = g \cdot f(1)
  \,.
$$

Moreover, if $f_1$ is a $G$-invariant function given by $f_1(1) = g_1$ and $f_2$ is given by $f_2(1) = g_2$, then their composite is given by

$$
  f_2 \circ f_1(1)
  = 
  f_2( g_1 ) = g_1 \cdot f_2(1) = g_1 \cdot g_2
  \,.
$$

=--

## Properties

### Comparison map from Burnside ring to representation ring
 {#ComparisonMapFromBurnsideRingToRepresentationRing}

Let $G$ be a [[finite group]]. Consider

1. the [[Burnside ring]] $A(G)$, which is the [[Grothendieck group]] of the [[monoidal category]] $G Set$ of [[finite set|finite]] [[G-sets]];

1. the [[representation ring]] $R(G)$, which is the [[Grothendieck group]] of the monoidal category $G Rep$ of [[finite dimensional vector space|finite dimensional]] $G$-[[linear representations]].

Then then map that sends a G-set to the corresponding linear permutation representation is a [[strong monoidal functor]]

$$
  G Set \longrightarrow G Rep
$$

and hence induces a [[ring homomorphism]]

$$
  A(G) \longrightarrow R(G)
$$

Under the identitification

1. of the [[Burnside ring]] with the [[equivariant stable cohomotopy]] of the point 

   $$
     A(G) \;\simeq\; \mathbb{S}_G(\ast)
   $$

   (see [there](Burnside+ring#AsTheEquivariantStableCohomotopyOfThePoint))

1. of the [[representation ring]] with the [[equivariant K-theory]] of the point

   $$
     R(G) \;\simeq\; K_G(\ast)
   $$

   (see [there](representation+ring#AsEquivariantKTheoryOfThePoint))

this should be image of the initial morphism of [[E-infinity ring spectra]]

$$
  \mathbb{S} \longrightarrow KU
$$

from the [[sphere spectrum]] to [[KU]].

## Related entries

* [[representation theory]], [[linear representation]],
  [[category of representations]]

* [[covering space]]

* [[Burnside ring]]

* [[groupoidification]]

## Related concepts

* [[∞-permutation representation]]

[[!redirects permutation representation]]
[[!redirects permutation representations]]
[[!redirects linear permutation representation]]
[[!redirects linear permutation representations]]

[[!redirects permutation action]]
[[!redirects permutation actions]]
