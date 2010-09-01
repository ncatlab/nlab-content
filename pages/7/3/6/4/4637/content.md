
#Contents#
* tabel of contents
{:toc}

## Idea

A general abstract [[adjunction]] $(\mathcal{O} \dashv Spec)$ relates [[presheaves]] with [[copresheaves]]: [[Isbell conjugation]].

Objects preserved by the [[monad]] of this adjunction are called **Isbell self-dual**.

## Definition

Let $\mathcal{V}$ be a [[cosmos]] and $C$ a small $\mathcal{V}$-[[enriched category]].


The _Isbell dual_ of an object $X \in [C^{op}, \mathcal{V}]$ is its image $\mathcal{O}$ under [[Isbell conjugation]]

$$
  [C,\mathcal{V}]^{op} 
  \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\underset{Spec}{\to}}
  [C^{op}, \mathcal{V}]
$$

Similarly for $A \in [C, \mathcal{V}]$ its image $Spec A$ is its Isbell-dual.

An object $X$ or $A$ is **Isbell-self-dual** if 

* $A \stackrel{}{\to} \mathcal{O} Spec(A)$ is an isomorphism in $[C,\mathcal{V}]$;

* $X \to Spec \mathcal{O} X$ is an isomorphism in $[C^{op}, \mathcal{V}]$ is an isomorphism, respectively.

## Properties

+-- {: .un_prop}
###### Proposition

All [[representable functor|representables]] are Isbell self-dual.

=--

+-- {: .proof}
###### Proof

By [Proof B , lemma 1](http://ncatlab.org/nlab/show/Isbell+conjugation#ProofB) we have a [[natural isomorphism]]s in $c \in C$

$$
  Spec(\mathcal{V}(c,-)) \simeq \mathcal{V}(-,c)
  \,.
$$

Therefore we have also the natural isomorphism

$$
  \begin{aligned}
     \mathcal{O} Spec \mathcal{V}(c,-) 
     & \simeq
     \mathcal{O} \mathcal{V}(-,c) (d)
     \\
     & :=
      [C^{op}, \mathcal{V}](\mathcal{V}(-,c), \mathcal{V}(-,d))
     \\
     & \simeq
     \mathcal{V}(c,d)
  \end{aligned}
  \,,
$$

where the second step is the [[Yoneda lemma]]. Similarly the other way round.

=--


## Examples



## References

In

* [[nLab:Bertrand Toën]], _Champs affine_ ([arXiv:math/0012219](http://arxiv.org/abs/math/0012219))
{#Toen}

Isbell self-dual [[∞-stack]]s over duals of commutative associative [[algebra]]s are called _affine stacks_ . They are characterized as those objects that are _small_ in a sense and local with respect to the [[cohomology]] with coefficients in the canonical [[line object]].