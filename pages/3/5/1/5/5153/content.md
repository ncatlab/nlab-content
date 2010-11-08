+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An _$\infty$-algebra over an $(\infty,1)$-operad_ is an [[∞-groupoid]] equipped with higher algebraic operations as encoded by an [[(∞,1)-operad]].

This is the [[(∞,1)-category theory]]-analog of the notion of [[algebra over an operad]]. Notice that in the literature one frequently sees [[model category]] presentations of $(\infty,1)$-operads by ordinary [[operad]]s enriched in a suitable [[monoidal model category]]. In these models $\infty$-algebras are be presented by ordinary algebras over cofibrant [[resolution]]s of ordinary enriched operads. This is directly analogous to how [[(∞,1)-categories]] may be presented by [[simplicially enriched categories]].

Also notice that the enrichment used in these models is not necessarily over [[Top]] / [[sSet]] (the standard [[presentable (∞,1)-category|presentations]] of [[∞Grpd]]) but often notably over a [[category of chain complexes]]. But at least for connective chain complexes, the [[Dold-Kan correspondence]] says that these, too, are in turn models for certain [[∞-groupoid]]s. This, in turn, is in direct analogy to how a [[stable (∞,1)-category]] may be presented by a [[dg-category]].

## Model category presentations

We discuss [[presentable (∞,1)-category|presentations]] of [[(∞,1)-categories]] of $\infty$-algebras over [[(∞,1)-operad]]s by [[model category]] structures on categories of [[algebra over an operad|algebras over an operad]] enriched in some suitable [[monoidal model category]].

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

* [[algebra over an algebraic theory]] / [[homotopy T-algebra]]

* [[algebra over an operad]] / **$\infty$-algebra over an $(\infty,1)$-operad**

## References

Model category structures for $\infty$-algebras are discussed in

* [[Clemens Berger]], [[Ieke Moerdijk]], _Resolution of coloured operads and rectification of homotopy algebras_ ([arXiv:math/0512576](http://arxiv.org/abs/math/0512576))
{#BergerMoerdijk}

[[!redirects ∞-algebra over an (∞,1)-operad]]
