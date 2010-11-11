
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A [[model category]] structure on a [[category]] of [[algebras over an operad]] enriched in some suitable [[homotopical category]] $\mathcal{E}$ is supposed to be a [[presentable (infinity,1)-category|presentation]] of the [[(∞,1)-category]] of [[∞-algebras over an (∞,1)-operad]].


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


+-- {: .un_def}
###### Remark

So if $P$ is admissible, then $Alg_{\mathcal{E}}(P)$ carries the model structure where a morphism of $P$ algebras $f : A \to B$ is a fibration or weak equivalence if the underlying morphism in $\mathcal{E}$ is, respectively.

Below we discuss general properties of $P$ under which this model structure indeed exists.

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

If the interval is moreover cocommutative, then the same is true for every symmetric coloured operad.

=--

This is [BergerMoerdijk, theorem 2.1](#BergerMoerdiskAlgebras), following ([BergerMoerdijk-Homotopy, theorem 3.2](#BergerMoerdijkHomotopy)). For more details see [[model structure on operads]].



### Rectification of algebras

Recall the notion of resolutions of operads and of the _[[Boardman-Vogt resolution]]_ $W(H,P)$ from [[model structure on operads]].

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

This is  ([BergerMoerdijk, theorem 4.1](#BergerMoerdijkAlgebras)).

+-- {: .un_theorem #RectificationTheorem}
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

## Examples {#Examples}

### $A_\infty$-Algebras {#AInfAlgebras}

Let $Assoc$ be the [[associative operad]] in [[Set]] regarded as an operad in [[Top]] under the [[discrete space]] embedding $Disc : Set \to Top$.

Let $I_*$ be the operad whose algebras are pointed objects. There is a canonical morphism $i : I_* \to Assoc$. 

+-- {: .un_lemma}
###### Claim

The [[relative Boardman-Vogt resolution]]

$$
  I_* \hookrightarrow I_*[i] \hookrightarrow W([0,1], I_* \to Assoc)  \stackrel{\simeq}{\to} Assoc
$$

produces precisely [[Jim Stasheff|Stasheff]]'s [[A-∞ operad]]. 

=--

This is ([BergerMoerdijk, page 13](#BergerMoerdijkAlgebras))

+-- {: .un_corollary}
###### Corollary

Every [[A-∞ space]] is equivalent as an $A_\infty$-space to a topological [[monoid]].

=--

+-- {: .proof}
###### Proof

This follows from the [rectification theorem](#RectificationTheorem), using that by the above algebras over $W([0,1], I_* \to Assoc)$ are precisely [[A-∞ space]]s.

=--

+-- {: .un_remark}
###### Remark

This is a classical statement. See [[A-∞ algebra]] for background and references.

=--

### Homotopy coherent diagrams {#HomotopyCoherentDiagrams}

Let $C$ be a small $\mathcal{E}$-[[enriched category]] with set of objects $Obj(C)$. There is an operad $Diag_{C}$


$$
  Diag_C(c_1, \cdots, c_n;c) = 
  \left\{
    \array{
      C(c_1, c) & if n = 1
      \\
      \emptyset & otherwise
    }
  \right.
$$

whose algebras are [[enriched functor]]s

$$
  F : C \to \mathcal{E}
  \,,
$$

hence [[diagram]]s in $\mathcal{E}$. Then the [[Boardman-Vogt resolution]]

$$
  HoCoDiag_C := W(H,Diag_C)
$$

is the operad for [[homotopy coherent diagram]]s over $C$ in $\mathcal{E}$.

The rectification theorem above now says that every homotopy coherent diagram is equivalent to an ordinary $\mathcal{E}$-diagram. For $\mathcal{E} = $ [[Top]] this is known as [[Vogt's theorem]].


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

A general discussion of the [[model structure on operads]] is in

* [[Clemens Berger]], [[Ieke Moerdijk]], _Axiomatic homotopy theory for operads_ Comment. Math. Helv. 78 (2003), 805&#8211;831. ([arXiv:math/0206094](http://arxiv.org/abs/math/0206094))
{#BergerMoerdijkHomotopy}

The concrete construction of the specific cofibrant resolutions in these structures going by the name [[Boardman-Vogt resolution]] is in 

* [[Clemens Berger]], [[Ieke Moerdijk]], _The Boardman-Vogt resolution of operads in monoidal model categories_ , Topology 45 (2006), 807&#8211;849. ([pdf](http://math.unice.fr/~cberger/BV.pdf))
{#BergerMoerdijkResolution}

The discussion of the model structure on algebras over a suitable operad is in

* [[Clemens Berger]], [[Ieke Moerdijk]], _Resolution of coloured operads and rectification of homotopy algebras_ ([arXiv:math/0512576](http://arxiv.org/abs/math/0512576))
{#BergerMoerdijkAlgebras}

