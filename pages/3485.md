

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

For $G$ a [[group]] (tyically a [[finite group]]), consider a [[G-set]] $(S, \rho)$, hence a [[set]] $S$ (typically a [[finite set]]), equipped with an [[action]] of $G$

$$
  \rho \;\colon\; G \times S \longrightarrow S
  \,.
$$

Equivalently this is a [[group homomorphism]]

$$
  \rho \;\colon\; G \longrightarrow Aut_{Set}(S)
$$

from $G$ to the group of [[permutations]] of elements of $S$. As such it is a representation of $G$ "by permutations".

Specifically, if $S$ is a [[finite set]] and an [[isomorphism]] $S \simeq \{1, 2, 3, \cdots, n\}$ is understood, it is equivalently a [[group homomorphism]]

$$
  \rho \;\colon\; G \longrightarrow S_n
$$

to the [[symmetric group]] $S_n$ on $n$ elements.


For $k$ any [[field]] (or, more generally, any [[commutative ring]], but one mostly considers fields) this $G$-[[action]] may be _linearized_ to a $k$-[[linear representation]] of $G$ in an evident way: 

+-- {: .num_defn #LinearPermutationRepresentation}
###### Definition
**(linear permutation representation)**

The _linear permutation representation_ of a [[G-set]] $(S,\rho)$ is the following $k$-[[linear representation]] of $G$:

1. The underlying $k$-[[vector space]] is the [[free module|freely]] [[linear span|spanned]] vector space $k[S]$, whose elements ([[vectors]]) are the [[formal linear combinations]] 

   $$
     k[S]
     \;=\;
     \left\{
       v =\underset{ s \in S_{fin} \subset S }{\sum} v_s \, s
       \;\vert\;
       S_{fin} \, \text{finite subset}
       ,\;
       v_s \in k
     \right\}
   $$

   of elements of $S$ with [[coefficients]] in $k$, hence is the $k$-vector space for which $S$ is a canonical [[linear basis]].

1. The linear $G$-[[action]]

   $$
     k[\rho] \;\colon\; G \times k[\mathbb{C}] \longrightarrow k[\mathbb{C}]
   $$

   is given on [[linear basis]]-elements $s \in S \hookrightarrow k[S]$ by $\rho$, which uniquely defines it by linearity to act on a general vector as

   $$
     k[\rho]\left(g\right)
     \;\colon\;
     v 
     \;\mapsto\;
     \underset{ s \in S_{fin} \subset S }{\sum} v_s \, \rho(g)(s)
     \,.
   $$

=--

This concept immediately generalized to [[groupoid representations]] and so forth, see also at _[[infinity-action]]_ the section _[Examples -- Discrete group actions on sets](infinity-action#ExamplesPermutationRepresentations)_.



## Properties

### Functoriality

+-- {: .num_prop #FunctorialityOfLinearPermutationRepresentations}
###### Proposition
**(functoriality of linear permutation representations)**

The construction of linear permutation representations (Def. \ref{LinearPermutationRepresentation}) evidently extends to a [[functor]] from the [[category of G-sets]] $G Set$ to the [[category of representations|category of linear representations]] $G Rep$

$$
  G Set
    \overset{ k[-] }{\longrightarrow}
  G Rep
  \,.
$$

Both of these categories are [[rig categories]] with respect to [[disjoint union]] and [[Cartesian product]] on the left, and [[direct sum]] and [[tensor product of representations]] on the right.

The functor $k[-]$ is canonically a homomorphism of rig-categories in that it preserves the [[direct sums]] and is canonically a [[strong monoidal functor]]

$$
  \big(G Set, \sqcup, \times\big)
    \overset{ k[-] }{\longrightarrow}
  \big(G Rep, \oplus, \otimes \big)
  \,.
$$



=--

### Comparison from Burnside- to representation ring
 {#ComparisonMapFromBurnsideRingToRepresentationRing}


Let $G$ be a [[finite group]] and let all [[G-sets]] in the following be on [[finite set]] and all [[linear representations]] on [[finite-dimensional vector spaces]].

Consider

1. the [[Burnside ring]] $A(G)$, which is the [[Grothendieck ring]] of the [[rig-category]] $(G Set, \sqcup, \times)$ [[category of G-sets|of finite G-sets]];

1. the [[representation ring]] $R(G)$, which is the [[Grothendieck ring]] of the [[rig category]] $(G Rep, \oplus, \otimees)$ [[representation category|of finite-dimensional linear G-representations]].

+-- {: .num_defn #ComparisonMapBurnsideRingRepresentationRing}
###### Definition
**([[permutation representations]] make [[ring homomorphism]] from [[Burnside ring]] to [[representation ring]])**

Since forming $k$-linear permutation representations (Def. \ref{LinearPermutationRepresentation}) is a rig-functor $G Set\overset{k[-]}{\longrightarrow} G Rep$ (Prop. \ref{FunctorialityOfLinearPermutationRepresentations}), under passing to [[Grothendieck rings]] it induces a [[ring homomorphism]]

$$
  K(k[-])
  \;\colon\;
    K( G Set, \sqcup, \times )
    =
    \;
    A(G)
    \longrightarrow
    R(R)
    \;
    =
    K( G Rep, \oplus, \otimes)
$$

from the [[Burnside ring]] of $G$ to its [[representation ring]].

The [[image]] of $K(k[-])$ may be called the _virtual_ linear permutation representations.

=--

+-- {: .num_remark}
###### Remark
**(virtual permutation representations from [[equivariant stable cohomotopy]] into [[equivariant K-theory]])**

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

the [[ring homomorphism]] of Def. \ref{ComparisonMapBurnsideRingRepresentationRing} should be image under forming [[equivariant cohomology]] of the [[point]] of the [[initial object in an (infinity,1)-category|initial]] morphism of [[E-infinity ring spectra]]

$$
  \mathbb{S} \longrightarrow KU
$$

from the [[sphere spectrum]] to [[KU]].

=--

## Examples

### Permutation representations

+-- {: .num_example #RegularRepresentation}
###### Example
**([[regular representation]])

For $G$ a [[group]], write, for emphasis, $G_s$ for its underlying [[set]]. Let 

$$
  \array{
    G \times G_s
     &\overset{ \rho_\ell }{\longrightarrow}&
    G_s
    \\
    (g,s) &\mapsto& g \cdot s
  }
$$

be the canonical [[action]] of $G$ on itself, by left multiplication in the group. The corresponding linear permutation representation $(k[G_s], k(\rho_\ell))$ (Def. \ref{LinearPermutationRepresentation}) is called the _[[regular representation]]_ of $G$.

=--

### Virtual permutation representations

For the example that $G = S_n$ is a [[symmetric group]], this construction is analyzed in detail at _[Categorified Gram-Schmidt process](Gram-Schmidt+process#CategorifiedGramSchmidtProcess)_.

(...)

## Related entries

* [[representation theory]], [[linear representation]],
  [[category of representations]]

* [[covering space]]

* [[Burnside ring]]

* [[groupoidification]]

## Related concepts

* [[regular representation]]

* [[∞-permutation representation]]

[[!redirects permutation representation]]
[[!redirects permutation representations]]
[[!redirects linear permutation representation]]
[[!redirects linear permutation representations]]

[[!redirects permutation action]]
[[!redirects permutation actions]]
