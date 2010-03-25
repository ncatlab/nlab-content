
<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


## Definition

+-- {: .un_defn}
###### Definition

Let $C$ be a [[cofibrantly generated model category]] such that 
all acyclic cofibrations are [[monomorphism]]s. 

Choose a set $\{A_j \to B_j\}_{j \in J}$ of acyclic cofibrations such that an object $X \in C$ is fibrant precisely if it has the [[right lifting property]] against these morphisms.

An **algebraic fibrant object** in $C$ is a fibrant object of $C$ together with a choice of lifts ("fillers") $\sigma_j : B_j \to X$ in

$$
  \array{
    A_j &\to& X
    \\
    \downarrow & \nearrow_{\mathrlap{\sigma_j}}
    \\
    B_j
  }
$$

for each morphism $A_j \to X$, $j \in J$. 

Write $ALg C$ for the category whose objects are algebraic fibrant objects in $C$ and whose morphisms are morphisms in $C$ that respect the chosen lifts.

=--

+-- {: .un_theorem}
###### Theorem

The [[forgetful functor]] [[adjunction]]

$$
  F : C \stackrel{\to}{\leftarrow} Alg C : U
$$

induces the [[transferred model structure]] on $Alg C$: the fibrations
and weak equivalences in $Alg C$ are those of the underlying morphisms in $C$.

In particular, every object in $Alg C$ is fibrant.

The [[Quillen adjunction]] $(F \dashv U)$ is a [[Quillen equivalence]].


=--

+-- {: .proof}
###### Proof

This is theorem 2.18

* [[Thomas Nikolaus]], _Algebraic models for higher categories_ ([arXiv](http://arxiv.org/abs/1003.1342))


=--


## Refereces

* [[Thomas Nikolaus]], _Algebraic models for higher categories_ ([arXiv](http://arxiv.org/abs/1003.1342))

