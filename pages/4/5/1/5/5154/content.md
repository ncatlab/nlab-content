
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A [[model category]] structure on a [[category]] of [[algebras over an operad]] enriched in some suitable [[homotopical category]] $\mathcal{E}$ is a [[presentable (infinity,1)-category|presentation]] of the [[(∞,1)-category]] of [[∞-algebras over an (∞,1)-operad]].


## Definition

+-- {: .un_def}
###### Assumption

Let $\mathcal{E}$ be a [[category]] equipped with the structure of

* a [[closed monoidal category|closed]] [[symmetric monoidal category]];

* a [[monoidal model category]];

such that

* the model structure is [[cofibrantly generated model category|cofibrantly generated]];

* the tensor unit $I$ is cofibrant.

(...)

A cocommutative coalgebra [[interval object]] $H\in \mathcal{E}$ is

$$
  \nabla : I \coprod I \hookrightarrow H \to I
$$


(...)

=--

We need the following standard definitions from ordinary [[operad]] theory.

+-- {: .un_def}
###### Definition

Let $C$ be a [[set]]. A **$C$-[[coloured operad]]** $P$ in $\mathcal{E}$ is

(...).


=--

+-- {: .un_def}
###### Definition

For $P$ a $C$-colored operad, a **$P$-algebra** is (...)

We write $Alg_{\mathcal{E}}(P)$ for the category of $P$-algebras.

=--

+-- {: .un_def}
###### Definition

A $C$ coloured operad $P$ is called **admissible** if the [[transferred model structure]] along the [[forgetful functor]]

$$
  U_P : Alg_{\mathcal{E}}(P)
  \to \mathcal{E}^{C}
$$

exists.

=--

## Properties


+-- {: .un_theorem}
###### Theorem

If $\mathcal{E}$ has a [[symmetric monoidal functor|symmetric monoidal]] fibrant replacement functor and a coalgebra [[interval object]] $H$ then every non-symmetric coloured operad in $\mathcal{E}$ is admissible.

If the interval is moreover commutative, then the same is true for every symmetric colured operad.

=--


+-- {: .un_theorem}
###### Theorem


The [[forgetful functor]] from $C$-colored operads to pointed $C$-colored collections has a [[left adjoint]]

$$
  (F^*_C \dashv U_C)
  :
  Oper_C(\mathcal{E})
  \stackrel{\leftarrow}{\to}
  Coll_C^*(\mathcal{E})  
  \,.
$$

=--

This is  ([BergerMoerdijk, theorem 3.2](#BergerMoerdijk)).


+-- {: .un_theorem}
###### Theorem

For each well-pointed  $\Sigma$-cofibrant $C$-coloured operad $P$, the $(F^*_C \ashv U_C)$-counit factors as a cofibration followed by a weak equivalence

$$
  F_C^*(P) \hookrightarrow W(H,P) \stackrel{\simeq}{\to} P
$$

of $C$-coloured operads, [[natural transformation|naturally]] in $P$ and $H$.

If $P \to Q$ is a $\Sigma$-cofibration between well-pointed $\Sigma$-cofibrant $C$-coloured operads, then the induced map $W(H,P) \to W(H,Q)$ is a cofibration of cofibrant $C$-coloured operads.

=--

This is  ([BergerMoerdijk, theorem 3.5](#BergerMoerdijk)).

Here $W(H,P)$ is also called the **coloured Boardman-Vogt resolution** of $P$.

An [[algebra over an operad]] over $W(H,P)$ is called a **$P$-algebra up to homotopy**.

+-- {: .un_theorem}
###### Theorem

Let $\mathcal{E}$ be in addition a [[left proper model category]]. 

Then for $\phi : P \to Q$ a weak equivalence between asdmissible $\Sigma$-cofibrant well-pointed $C$-colourred operads in $\mathcal{E}$, the [[adjunction]]

$$
  (\phi_! \dashv \phi^*) : 
  Alg_\mathcal{E}(P)
  \stackrel{\leftarrow}{\to}
  Alg_\mathcal{E}(P)
$$

is a [[Quillen equivalence]].

=--

This is  ([BergerMoerdijk, theorem 4.1](#BergerMoerdijk)).

+-- {: .un_theorem}
###### Theorem
**(rectification of homotopy $T$-algebras)**

Let still $\mathcal{E}$ be left proper.

Let $P$ be an admissible $\Sigma$-cofibrant operad in $\mathcal{E}$ such that also $W(H,P)$ is admissible. 

Then 

$$
  (\epsilon_! \dashv \epsilon^*) : 
  Alg_\mathcal{E}(P)
  \stackrel{\leftarrow}{\to}
  Alg_\mathcal{E}(W(H,P))
$$

is a [[Quillen equivalence]].


=--


## Related concepts


* [[algebra over a monad]]

  [[∞-algebra over an (∞,1)-monad]] 

* [[algebra over an algebraic theory]] 

  [[∞-algebra over an (∞,1)-algebraic theory]]

  * [[homotopy T-algebra]] / [[model structure on simplicial T-algebras]]

* [[algebra over an operad]] 

   [[∞-algebra over an (∞,1)-operad]]

   * **model structure on algebras over an operad**





## References

* [[Clemens Berger]], [[Ieke Moerdijk]], _Resolution of coloured operads and rectification of homotopy algebras_ ([arXiv:math/0512576](http://arxiv.org/abs/math/0512576))
{#BergerMoerdijk}
