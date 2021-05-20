
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The _free commutative monoid_ $\mathbb{N}[S]$ on a [[set]] $S$ is the [[commutative monoid]] whose elements are _formal $\mathbb{N}$-[[linear combinations]]_ of elements of $S$.

## Definition
 {#Definition}


+-- {: .num_defn #FreeCommutativeMonoid}
###### Definition

Let 

$$
  U \colon CMon \longrightarrow Set
$$

be the [[forgetful functor]] from the category [[CMon]] of commutative monoids, to the category [[Set]] of sets. This has a [[left adjoint]] [[free construction]]:

$$
  \mathbb{Z}[-] \colon Set \longrightarrow CMon
  \,.
$$

This is the _free commutative monoid functor_. For $S \in $ [[Set]], the **free commutative monoid** $\mathbb{N}[S] \in $ [[CMon]] is the [[free object]] on $S$ with respect to this [[free-forgetful adjunction]].

=--

Of course, this notion is meant to be invariant under isomorphism: it doesn't depend on the left adjoint chosen. Thus, if a functor of the form $\hom_{Set}(S, U-): CMon \to Set$ is [[representable functor|representable]] by 
a commutative monoid $M$, then we may say $M$ is a free commutative monoid on $S$. A specific choice of isomorphism 

$$\hom_{CMon}(M, -) \cong \hom_{Set}(S, U-)$$ 

corresponds, via the [[Yoneda lemma]], to a function $S \to U M$ which exhibits $S$, or rather its image under this function, as a specific [[basis]] of $M$. If $M$ is so equipped with such a universal arrow $S \to U M$, then it is harmless to call $M$ "the" free commutative monoid on $S$. 

Explicit descriptions of free commutative monoid are discussed [below](#Properties).

## Properties
 {#Properties}

### In terms of formal linear combinations

+-- {: .num_defn #FormalLinearCombination}
###### Definition

A **formal linear combination** of elements of a set $S$ is 
a [[function]] 

$$
  a : S \to \mathbb{N}
$$
such that only finitely many of the values $a_s \in \mathbb{N}$ are non-zero.

Identifying an element $s \in S$ with the function
$S \to \mathbb{N}$ which sends $s$ to $1 \in \mathbb{N}$ and all other elements to 0, this is written as

$$
  a = \sum_{s \in S} a_s \cdot s
  \,.
$$

In this expression one calls $a_s \in \mathbb{N}$ the [[coefficient]] of $s$ in the formal linear combination.

=--

+-- {: .num_remark}
###### Remark

Definition \ref{FormalLinearCombination} of formal linear combinations makes sense with  [[coefficients]] in any [[commutative monoid]] $M$, not necessarily the
natural numbers.

$$
  M[S] \coloneqq \mathbb{N}[S] \otimes M
  \,.
$$

=--

+-- {: .num_defn #MonoidOfFormalLinearCombinations}
###### Definition

For $S \in $ [[Set]], the __monoid of formal linear combinations__ $\mathbb{N}[S]$ is the 
[[monoid]] whose underlying [[set]] is that of formal linear combinations, 
def. \ref{FormalLinearCombination}, and whose group operation is 
the pointwise addition in $\mathbb{N}$:

$$
  (\sum_{s \in S} a_s \cdot s)
  + 
  (\sum_{s \in S} b_s \cdot s)
  =
  \sum_{s \in S} (a_s + b_s) \cdot s
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

The free commutative monoid on $S \in Set$ is, up to [[isomorphism]], the 
monoid of formal linear combinations, def. \ref{MonoidOfFormalLinearCombinations}, on $S$.

=--

+-- {: .num_defn}
###### Proposition

For $S$ a set, the free commutative monoid $\mathbb{N}[S]$ is the [[biproduct]] in [[CMon]] of ${|S|}$-copies of $\mathbb{N}$ with itself:

$$
  \mathbb{ZlN}[S] \simeq \oplus_{s \in S} \mathbb{N}
  \,.
$$

=--

## Examples

* For $R$ a [[rig]] and $S$ a set, the [[tensor product of commutative monoids]]
  $\mathbb{N}[S] \otimes R$ is the [[free module]] over $R$ on the [[basis]] $S$. 

* For $R$ a rig, the [[tensor product of commutative monoids]]  $\mathbb{N}[\mathbb{N}]\otimes R$ is the commutative monoid underlying the [[rig]] of [[polynomials]] over $R$.

## Related concepts

* [[free monoid]]

* [[free abelian group]]

[[!redirects free commutative monoid]]
[[!redirects free commutative monoids]]

[[!redirects free commutative monoid functor]]
[[!redirects free commutative monoid functors]]

[[!redirects formal linear combination]]
[[!redirects formal linear combinations]]

[[!redirects formal sum]]
[[!redirects formal sums]]
