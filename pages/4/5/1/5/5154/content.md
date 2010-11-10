
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

=--

+-- {: .un_prop}
###### Proposition

Under these conditions there is for each [[finite group]] $G$ the structure of a [[monoidal model category]] on the category $\mathcal{E}^{\mathbf{B}G}$ of objects in $\mathcal{E}$ equipped with a $G$-[[action]], for which the [[forgetful functor]]

$$
  \mathcal{E}^{\mathbf{B}G} \to \mathcal{E}
$$

preserves and reflects fibrations and weak equivalences.

=--

This is discussed in the examples at [[monoidal model category]].

For $C \in $ [[Set]] a set of colours and $P$ a $C$-[[coloured operad]] in $\mathcal{E}$ we write $Alg_{\mathcal{E}}(P)$ for the category of $P$-[[algebras over an operad]]. There is a [[forgetful functor]]

$$
  U_P : Alg_{\mathcal{E}}(P) \to \mathcal{E}^C
  \,.
$$

+-- {: .un_def #admissible}
###### Definition

A $C$ coloured operad $P$ is called **admissible** if the [[transferred model structure]] on $Alg_{\mathcal{E}}(P)$ along the [[forgetful functor]]

$$
  U_P : Alg_{\mathcal{E}}(P)
  \to \mathcal{E}^{C}
$$

exists.

=--






## Properties


### Existence by coalgebra intervals

The above model transferred model structure on algebras over an operad exists if there is a suitable [[interval object]] in $\mathcal{E}$.

+-- {: .un_def}
###### Definition


A **cocommutative coalgebra [[interval object]]** $H\in \mathcal{E}$ is

* a cocommutative counittal [[comonoid]] in $\mathcal{E}$

* equipped with a factorization

  $$
    \nabla : I \coprod I \hookrightarrow H \to I
  $$

  of the [[codiagonal]] on $I$ into two [[homomorphism]]s of comonoids with the first a cofibration and the second a weak equivalence in $\mathcal{E}$.


=--


+-- {: .un_example}
###### Examples

Such cocommutative coalgebra inrvals exist in

* the [[model structure on topological spaces|model structure on compactly generated topological spaces]];

* the [[model structure on simplicial sets]];

* the [[model structure on symmetric spectra]].

In

* the [[model structure on chain complexes]] 

there is a coalgebra interval.

=--



+-- {: .un_theorem}
###### Theorem

If $\mathcal{E}$ has a [[symmetric monoidal functor|symmetric monoidal]] fibrant replacement functor and a coalgebra [[interval object]] $H$ then every non-symmetric [[coloured operad]] in $\mathcal{E}$ is [admissible](#admissible) -- the transfered model structure on algebras exists.

If the interval is moreover cocommutative, then the same is true for every symmetric colured operad.

=--

This is [BergerMoerdijk, theorem 2.1](#BergerMoerdisk), following ([BergerMoerdijk-Homotopy, theorem 3.2](#BergerMoerdijkHomotopy)). For more details see [[model structure on operads]].


### Resolutions

We now discuss the construction and properties of cofibrant [[resolution]]s of operads and their algebras.

+-- {: .un_remark}
###### Remark

The category of $C$-coloured operads is itself the category of algebras over a non-symmetric operad. See [[coloured operad]] for more. Thus the above theorem procides conditions under which $C$-coloured operads carry a model structure in which fibrations and weak equivalences are those morphisms of operads $P \to Q$ that are  degreewise fibrations and weak equivalences in $\mathcal{E}$.

=--

+-- {: .un_def}
###### Terminology

We shall from now on call an operad $P$ **cofibrant** if the morphism $I_C \to P$ from the initial $C$-[[coloured operad]] has the [[left lifting property]] against degreewise acyclic fibrations of operads (irrespective of whether the above conditions for the existence of the model structure hold).

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

### Rectificaction of algebras

We now discuss conditions under which model categories of algebras over a resolved operad is Quillen equivalent to that over the original operad.

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

* [[Clemens Berger]], [[Ieke Moerdijk]], _Axiomatic homotopy theory for operads_ Comment. Math. Helv. 78 (2003), 805&#8211;831.
{#BergerMoerdijkHomotopy}

* [[Clemens Berger]], [[Ieke Moerdijk]], _The Boardman-Vogt resolution of operads in monoidal model categories_ , Topology 45 (2006), 807&#8211;849.
{#BergerMoerdijkResolution}