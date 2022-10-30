
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

## Existence

### Cofibrant operads

+-- {: .un_theorem}
###### Theorem
Let $C$ be a [[cofibrantly generated model category|cofibrantly generated]] [[symmetric monoidal model category]].
Let $O$ be a [[cofibrant object|cofibrant]] [[operad]].
If $C$ satisfies the [[monoid axiom in a monoidal model category]], then there is an induced [[model structure]] on the category $Alg_C(O)$ of [[algebras over an operad]].
=--

See ([Spitzweck 01](#Spitzweck01), Theorem 4).


### $G$-objects

+-- {: .num_defn}
###### Assumption

Let $\mathcal{E}$ be a [[category]] equipped with the structure of

* a [[closed monoidal category|closed]] [[symmetric monoidal category]];

* a [[monoidal model category]];

such that

* the model structure is [[cofibrantly generated model category|cofibrantly generated]];

* the tensor unit $I$ is cofibrant.

=--

+-- {: .num_prop}
###### Proposition

Under these conditions there is for each [[finite group]] $G$ the structure of a [[monoidal model category]] on the category $\mathcal{E}^{\mathbf{B}G}$ of objects in $\mathcal{E}$ equipped with a $G$-[[action]], for which the [[forgetful functor]]

$$
  \mathcal{E}^{\mathbf{B}G} \to \mathcal{E}
$$

preserves and reflects fibrations and weak equivalences.

=--

This is discussed in the examples at _[[monoidal model category]]_.

### Coloured operads

For $C \in $ [[Set]] a set of colours and $P$ a $C$-[[coloured operad]] in $\mathcal{E}$ we write $Alg_{\mathcal{E}}(P)$ for the category of $P$-[[algebras over an operad]]. There is a [[forgetful functor]]

$$
  U_P \;\colon\; Alg_{\mathcal{E}}(P) \to \mathcal{E}^C
$$

from the category of [[algebra over an operad|algebras over the operad]] in $\mathcal{E}$ to the underlying $C$-colored objects of $\mathcal{E}$.

+-- {: .num_defn #admissible}
###### Definition

A $C$-[[coloured operad]] $P$ is called **admissible** if the [[transferred model structure]] on $Alg_{\mathcal{E}}(P)$ along the [[forgetful functor]]

$$
  U_P : Alg_{\mathcal{E}}(P)
  \to \mathcal{E}^{C}
$$

exists.

=--


+-- {: .num_defn}
###### Remark

So if $P$ is admissible, then $Alg_{\mathcal{E}}(P)$ carries the model structure where a morphism of $P$ algebras $f : A \to B$ is a fibration or weak equivalence if the underlying morphism in $\mathcal{E}$ is, respectively.

Below we discuss general properties of $P$ under which this model structure indeed exists.

=--



## Properties


### Existence by coalgebra intervals

The above [[transferred model structure]] on [[algebras over an operad]] exists if there is a suitable [[interval object]] in $\mathcal{E}$.

+-- {: .num_defn}
###### Definition


A **cocommutative coalgebra [[interval object]]** $H\in \mathcal{E}$ is

* a cocommutative co-unital [[comonoid]] in $\mathcal{E}$

* equipped with a factorization

  $$
    \nabla : I \coprod I \hookrightarrow H \to I
  $$

  of the [[codiagonal]] on $I$ into two [[homomorphism]]s of comonoids with the first a cofibration and the second a weak equivalence in $\mathcal{E}$.


=--


+-- {: .num_example}
###### Examples

Such cocommutative coalgebra intervals exist in

* the [[model structure on topological spaces|model structure on compactly generated topological spaces]];

* the [[model structure on simplicial sets]];

* the [[model structure on symmetric spectra]].

In

* the [[model structure on chain complexes]] 

there is a coalgebra interval.

=--



+-- {: .num_theorem}
###### Theorem

If $\mathcal{E}$ has a [[symmetric monoidal functor|symmetric monoidal]] fibrant replacement functor and a coalgebra [[interval object]] $H$ then every non-symmetric [[coloured operad]] in $\mathcal{E}$ is admissible, def. \ref{admissible}:  the [[transferred model structure]] on algebras exists.

If the interval is moreover cocommutative, then the same is true for every symmetric coloured operad.

=--

This is ([BergerMoerdijk, theorem 2.1](#BergerMoerdiskAlgebras)), following ([BergerMoerdijk-Homotopy, theorem 3.2](#BergerMoerdijkHomotopy)). For more details see at _[[model structure on operads]]_.

+-- {: .num_remark}
###### Remark

Since the coalgebra interval in the [[category of chain complexes]] is not cocommutative, this case requires special discussion, as some of the statements below will not apply to it. For more on this case see _[[model structure on dg-algebras over an operad]]_.

=--

### Rectification of algebras
 {#RectificationOfAlgebras}

Recall the notion of resolutions of operads and of the _[[Boardman-Vogt resolution]]_ $W(H,P)$ from [[model structure on operads]].

We now discuss conditions under which model categories of algebras over a resolved operad is Quillen equivalent to that over the original operad. This yields general _[[rectification]]_ results for homotopy-algebras over an operad (see also the _[Examples](#Examples)_ below.)



+-- {: .num_theorem}
###### Theorem

Let $\mathcal{E}$ be in addition a [[left proper model category]]. 

Then for $\phi : P \to Q$ a weak equivalence between admissible $\Sigma$-cofibrant well-pointed $C$-coloured operads in $\mathcal{E}$, the [[adjunction]]

$$
  (\phi_! \dashv \phi^*) : 
  Alg_\mathcal{E}(P)
  \stackrel{\leftarrow}{\to}
  Alg_\mathcal{E}(Q)
$$

is a [[Quillen equivalence]].

=--

This is  ([BergerMoerdijk, theorem 4.1](#BergerMoerdijkAlgebras)).

+-- {: .num_theorem #RectificationTheorem}
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

## Examples 
 {#Examples}

### Monoids (associative algebras)

For $P = Assoc$ the [[associative operad]] it category of algebras $Alg_{\mathcal{E}} P $ is the [[category of monoids]] in $\mathcal{E}$. The above model structure on $Alg_{\mathcal{E}} P$ is the standard [[model structure on monoids in a monoidal model category]].

### $A_\infty$-Algebras {#AInfAlgebras}

Let $Assoc$ be the [[associative operad]] in [[Set]] regarded as an operad in [[Top]] under the [[discrete space]] embedding $Disc : Set \to Top$.

Let $I_*$ be the operad whose algebras are pointed objects. There is a canonical morphism $i : I_* \to Assoc$. 

+-- {: .num_lemma}
###### Claim

The [[relative Boardman-Vogt resolution]]

$$
  I_* \hookrightarrow I_*[i] \hookrightarrow W([0,1], I_* \to Assoc)  \stackrel{\simeq}{\to} Assoc
$$

produces precisely [[Jim Stasheff|Stasheff]]'s [[A-∞ operad]]. 

=--

This is ([BergerMoerdijk, page 13](#BergerMoerdijkAlgebras))

+-- {: .num_cor}
###### Corollary

Every [[A-∞ space]] is equivalent as an $A_\infty$-space to a topological [[monoid]].

=--

+-- {: .proof}
###### Proof

This follows from the [rectification theorem](#RectificationTheorem), using that by the above algebras over $W([0,1], I_* \to Assoc)$ are precisely [[A-∞ space]]s.

=--

+-- {: .num_remark}
###### Remark

This is a classical statement. See [[A-∞ algebra]] for background and references.

=--

### $L_\infty$-algebras and simplicial Lie algebras

Let $Lie$ be the [[Lie operad]]. 

A cofibrant resolution is $L_\infty$, the operad whose algebras in [[chain complex]]es are [[L-infinity algebras]].

Now (...)
  

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

The [[rectification]] theorem above now says that every homotopy coherent diagram is equivalent to an ordinary $\mathcal{E}$-diagram. For $\mathcal{E} = $ [[Top]] this is known as [[Vogt's theorem]].

### $(\infty,1)$-Categories of algebras and bimodules over an operad {#InfCatOfMods}

The constuction $Alg_{\mathcal{E}}(P)$ of a category of [[algebras over an operad]] is contravariantly functorial in $P$. Therefore if $P^\bullet$ is a [[cosimplicial object]] in the category of operads, we have that $Alg_{\mathcal{E}}(P^\bullet)$ is a (large) [[simplicial category]] of algebras. Moreover, the [[Boardman-Vogt resolution]] $W(P)$ is functorial in $P$. 

These two facts together allow us to construct simplicial categories of homotopy algebras.

Specifically, there is a cosimplicial operad $Assoc^\bullet$ which

* in degree 0 is the usual [[associative operad]] $Assoc^0  = Assoc$,

* in degree 1 is the operad whose algebras are triples consisting of two associative monoids and one [[bimodule]] between them;

* in degree 2 it is the operad whose algebras are tuples consisting of three associative algebras $A_0, A_1, A_2$ as well as  one $A_i$-$A_j$-bimodule $N_{ i j}$ for each $0 \leq i \lt j \leq 2$ and a homomorphism of bimodules 

  $$
    N_{0 1} \otimes_{A_1} N_{1 2} \to N_{0 2}
  $$

* and so on.

The simplicial category of algebras over $Assoc^\bullet$ is one incarnation of the [[2-category]] of algebras, bimodules and bimodules homomorphisms.

We can pass to the corresponding $\infty$-algebras by applying the [[Boardman-Vogt resolution]] to the entire cosimplicial diagram of operads, to obtain the cosimplicial [[A-∞ operad]]

$$
  A_\infty^\bullet := W(Assoc^\bullet)
  \,.
$$

The [[simplicial category]] of algebras over this has as objects [[A-∞ algebra]]s, as morphism bimodules between these, and so on.

This is discussed in ([BergerMoerdijkAlgebras, section 6](#BergerMoerdijkAlgebras)).

## Related concepts

* [[model structure on monoids in a monoidal model category]]

* [[algebra over a monad]]

  [[∞-algebra over an (∞,1)-monad]] 

  * [[model structure on algebras over a monad]]

* [[algebra over an algebraic theory]] 

  [[∞-algebra over an (∞,1)-algebraic theory]]

  * [[homotopy T-algebra]] / [[model structure on simplicial T-algebras]]

* [[(∞,1)-operad]], [[model structure on operads]]

  * [[algebra over an (∞,1)-operad]], **model structure on algebras over an operad**

    * [[module over an algebra over an (∞,1)-operad]], [[model structure on modules over an algebra over an operad]]





## References

A general discussion of the [[model structure on operads]] is in

* [[Clemens Berger]], [[Ieke Moerdijk]], _Axiomatic homotopy theory for operads_ Comment. Math. Helv. 78 (2003), 805&#8211;831. ([arXiv:math/0206094](http://arxiv.org/abs/math/0206094))
{#BergerMoerdijkHomotopy}

See also

* {#Spitzweck01} [[Markus Spitzweck]], _Operads, Algebras and Modules in General Model Categories_, [arXiv:math/0101102](http://arxiv.org/abs/math/0101102).

The concrete construction of the specific cofibrant resolutions in these structures going by the name [[Boardman-Vogt resolution]] is in 

* {#BergerMoerdijkResolution} [[Clemens Berger]], [[Ieke Moerdijk]], _The Boardman-Vogt resolution of operads in monoidal model categories_ , Topology 45 (2006), 807&#8211;849. ([pdf](http://math.unice.fr/~cberger/BV.pdf))


The discussion of the model structure on algebras over a suitable operad is in

* [[Clemens Berger]], [[Ieke Moerdijk]], _Resolution of coloured operads and rectification of homotopy algebras_ ([arXiv:math/0512576](http://arxiv.org/abs/math/0512576))
{#BergerMoerdijkAlgebras}

More discussion on the transport of operad algebra structures along [[Quillen adjunctions]]/[[Bousfield localization of model categories|Bousfield localizations]] between the underlying model categories is in 

* [[Carles Casacuberta]], [[Javier Gutiérrez]], [[Ieke Moerdijk]], [[Rainer Vogt]], _Localization of algebras over coloured operads_, Proceedings of the London Mathematical Society (3) 101 (2010), no. 1, 105-136 ([arXiv:0806.3983](http://arxiv.org/abs/0806.3983))

* [[Javier Gutiérrez]], _Transfer of algebras over operads along derived Quillen adjunctions_, Journal of the London Mathematical Society 86 (2012), 607-625 ([arXiv:1104.0584](http://arxiv.org/abs/1104.0584))

[[!redirects model structures on algebras over an operad]]

[[!redirects model category of algebras over an operad]]
[[!redirects model categories of algebras over an operad]]