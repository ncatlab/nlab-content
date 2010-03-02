
<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The standard [[model category]] structure on [[cosimplicial object]]s in unital, commutative algebras over $k$.

Under the [[monoidal Dold-Kan correspondence]] this is [[Quillen equivalence|Quillen equivalent]] to the [[model structure on dg-algebras|model structure on commutative non-negative cochain dg-algebras]].

## Definition

Write $Alg_k^\Delta$ for the category of [[cosimplicial object]]s in the category of unital, commutative $k$-algebras. Sending algebras to their underlying $k$-[[module]]s yields a [[forgetful functor]]

$$
  U : Alg_k^\Delta \to k Mod^\Delta
  \,.
$$

The [[Dold-Kan correspondence]] provides the normalized cochain complex ([[Moore complex]]) functor

$$
  N : k Mod_k^\Delta \to Ch^\bullet(k)_+
  \,.
$$

Define a morphism $f : A \to B$ of cosimplicial algebras is a morphism is a weak equivalence if 

$$
  N(U(f)) : N(U(A)) \to N(U(B))
$$

is a [[quasi-isomorphism]] in $Ch^\bullet_+(k)$.

Say a morphism of cosimplicial algebras is a fibration if it is a [[monomorphism]] (degreewise surjection).

This defines the **projective [[model category]] structure** on $Alg_k^\Delta$.

There is also the structure of an [[sSet]]-[[enriched category]] of $Alg_k^\Delta$.

For $X$ a [[simplicial set]] and $A \in Alg_k$ let $A^X  \in Alg_k^\Delta$ be the corresponding $A$-valued [[cochains on simplicial sets]]

$$
  A^X : [n] \mapsto \prod_{X_n} A
  \,.
$$

For $A,B \in Alg_k^\Delta$ define the [[sSet]]-[[hom-object]] $Alg_k^\Delta(A,B)$ by

$$
  Alg_k^\Delta(A,B) := Hom_{sSet}(A, B^{\Delta[\bullet]})
  \in sSet
  \,.
$$

This makes $Alg_k^\Delta$ into a [[simplicially enriched category]] which is [[copower|tensored]] and [[power|cotensored]] over $sSet$.

And this is compatible with the model category structure: 

+-- {: .un_theorem}
###### Theorem

With the definitions as above, $Alg_k^\Delta$ is a [[simplicial model category]].

=--

+-- {: .proof}
###### Proof

[To06, theorem 2.1.2](http://arxiv.org/abs/math/0012219)

=--

Under the [[monoidal Dold-Kan correspondence]] this is related to the [[model structure on dg-algebras|model structure on commutative non-negative cochain dg-algebras]].

## References


Details are in section 2.1 of

* [[Bertrand Toen]], _Affine stacks (Champs affines)_ ([arXiv:math/0012219](http://arxiv.org/abs/math/0012219)) .

See also

* Goerrs, Jardine, _Simplicial homotopy theory_

The generalization to arbitrary cosimplicial rings is proposition 9.2 of

* J.L. Castiglioni G. Corti&#241;as, _Cosimplicial versus DG-rings: a version of the Dold-Kan correspondence_ ([arXiv](http://arxiv1.library.cornell.edu/abs/math/0306289v2))

There also aspects of relation to the [[model structure on dg-algebras]] is discussed. (See [[monoidal Dold-Kan correspondence]] for more on this).

[[!redirects model structure on cosimplicial algebras]]