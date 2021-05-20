
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The _free abelian group_ $\mathbb{Z}[S]$ on a [[set]] $S$ is the [[abelian group]] whose elements are _formal $\mathbb{Z}$-[[linear combinations]]_ of elements of $S$.


## Definition
 {#Definition}


+-- {: .num_defn #FreeAbelianGroup}
###### Definition

Let 

$$
  U \colon Ab \longrightarrow Set
$$

be the [[forgetful functor]] from the category [[Ab]] of abelian groups, to the category [[Set]] of sets. This has a [[left adjoint]] [[free construction]]:

$$
  \mathbb{Z}[-] \colon Set \longrightarrow Ab
  \,.
$$

This is the _free abelian group functor_. For $S \in $ [[Set]], the **free abelian group** $\mathbb{Z}[S] \in $ [[Ab]] is the [[free object]] on $S$ with respect to this [[free-forgetful adjunction]].

=--

Of course, this notion is meant to be invariant under isomorphism: it doesn't depend on the left adjoint chosen. Thus, if a functor of the form $\hom_{Set}(S, U-): Ab \to Set$ is [[representable functor|representable]] by 
an abelian group $A$, then we may say $A$ is a free abelian group on $S$. A specific choice of isomorphism 

$$\hom_{Ab}(A, -) \cong \hom_{Set}(S, U-)$$ 

corresponds, via the [[Yoneda lemma]], to a function $S \to U A$ which exhibits $S$, or rather its image under this function, as a specific [[basis]] of $A$. If $A$ is so equipped with such a universal arrow $S \to U A$, then it is harmless to call $A$ "the" free abelian group on $S$. 

Explicit descriptions of free abelian groups are discussed [below](#Properties).


## Properties
 {#Properties}

### In terms of formal linear combinations

+-- {: .num_defn #FormalLinearCombination}
###### Definition

A **formal linear combination** of elements of a set $S$ is 
a [[function]] 

$$
  a : S \to \mathbb{Z}
$$
such that only finitely many of the values $a_s \in \mathbb{Z}$ are non-zero.

Identifying an element $s \in S$ with the function
$S \to \mathbb{Z}$ which sends $s$ to $1 \in \mathbb{Z}$ and all other elements to 0, this is written as

$$
  a = \sum_{s \in S} a_s \cdot s
  \,.
$$

In this expression one calls $a_s \in \mathbb{Z}$ the [[coefficient]] of $s$ in the formal linear combination.

=--

+-- {: .num_remark}
###### Remark

Definition \ref{FormalLinearCombination} of formal linear combinations makes sense with  [[coefficients]] in any [[abelian group]] $A$, not necessarily the
integers.

$$
  A[S] \coloneqq \mathbb{Z}[S] \otimes A
  \,.
$$

=--


+-- {: .num_defn #GroupOfFormalLinearCombinations}
###### Definition

For $S \in $ [[Set]], the __group of formal linear combinations__ $\mathbb{Z}[S]$ is the 
[[group]] whose underlying [[set]] is that of formal linear combinations, 
def. \ref{FormalLinearCombination}, and whose group operation is 
the pointwise addition in $\mathbb{Z}$:

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

The free abelian group on $S \in Set$ is, up to [[isomorphism]], the 
group of formal linear combinations, def. \ref{GroupOfFormalLinearCombinations}, on $S$.

=--


+-- {: .num_defn}
###### Proposition

For $S$ a set, the free abelian group $\mathbb{Z}[S]$ is the [[direct sum]] in [[Ab]] of ${|S|}$-copies of $\mathbb{Z}$ with itself:

$$
  \mathbb{Z}[S] \simeq \oplus_{s \in S} \mathbb{Z}
  \,.
$$

=--

### Subgroups
 {#Subgroups}

+-- {: .num_prop #SubgroupsOfFreeAbelianGroupsAreFree}
###### Proposition

Assuming the [[axiom of choice]], then every [[subgroup]] of a free abelian group (def. \ref{FreeAbelianGroup}) is itself a free abelian group.

=--

(e.g. [Lang 02, Appendix 2 &#167;2, page 880](#Lang02)) For a full **proof** see at _[[principal ideal domain]]_ [this theorem](principal+ideal+domain#free).

+-- {: .num_remrk}
###### Remark

Prop. \ref{SubgroupsOfFreeAbelianGroupsAreFree} implies that (assuming AC) every abelian group admits a [[free resolution]] of length 2, hence with trivial [[syzygies]]. See [there](free+resolution#AbelianGroupHasFreeResolutionOfLength2).

=--



## Examples

* The free abelian group on the [[singular simplicial complex]] of a [[topological space]] $X$ consists of the [[singular chains]] on $X$.

* For $R$ a ring and $S$ a set, the [[tensor product of abelian groups]]
  $\mathbb{Z}[S] \otimes R$ is the [[free module]] over $R$ on the [[basis]] $S$. If $R = k$ is a [[field]], then this is the [[vector space]] over $k$ with basis $S$.

* For $R$ a ring, the [[tensor product of abelian groups]]  $\mathbb{Z}[\mathbb{N}]\otimes R$ is the abelian group underlying the [[ring]] of [[polynomials]] over $R$.
 

## Related concepts

* [[free group]]

* [[free commutative monoid]]

## References

* {#Lang02} [[Serge Lang]], _Algebra_, Graduate Texts in Mathematics 211 (Revised third ed.), Springer. 2002


[[!redirects free abelian group]]
[[!redirects free abelian groups]]

[[!redirects free abelian group functor]]
[[!redirects free abelian group functors]]
