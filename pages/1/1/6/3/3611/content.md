
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

If $V$ is a [[symmetric monoidal category]] that is also a [[monoidal model category]], then under suitable conditions there is also the structure of a [[model category]] on the category of [[symmetric operad|symmetric]] $V$-[[operads]]. 

This is important for the notion of _homotopy_ [[algebra over an operad]], such as [[A-∞ algebras]] and [[E-∞ algebras]].


## Definition

Throughout, let $V$ be a [[symmetric monoidal category|symmetric]] [[closed monoidal category|closed]] [[monoidal model category]] with all small [[colimit]]s and finite [[limit]]s. 


### Symmetric collections

We first consider the _collections_ of operations underlying a [[symmetric operad]] (with no notion of composition of operations yet).

For $G$ a [[discrete group]] write $\mathbf{B}G$ for the [[delooping]] [[groupoid]]: the category with a single object and $G$ as its set of [[morphisms]]. Then for $V$ any other category, write $V^{\mathbf{B}G}$ for the [[functor category]], consisting of [[functors]] $\mathbf{B}G \to V$. This is the category of [[actions]] of $G$ on [[objects]] in $V$ (the [[category of representations]]). 

For $G$ a [[finite group]] also $V^{\mathbf{B}G}$ inherits the structure of a [[closed monoidal category|closed]] [[symmetric monoidal category]] with small [[colimits]] and [[finite limits]]. There is a [[forgetful functor]]/[[free functor]] [[adjunction]]

$$
  V^{\mathbf{B}G} \stackrel{(-)[G]}{\underset{U}{\to}}
  V
  \,.
$$

Write $\Sigma_n$ for the [[symmetric group]] on $n \in \mathbb{N}$ elements. Take $\Sigma_0$ and $\Sigma_1$ both to be the trivial group.


+-- {: .num_defn }
###### Definition

The category of **collections** (of potential operations) in $V$  is the [[product]]

$$
  Coll(V) := \prod_{n \geq 0} V^{\mathbf{B}\Sigma_n}
  \,.
$$

=--

A collection $P$ is a tuple of objects

$$
  P = (P(n))_{n \in \mathbb{N}}
$$

each equipped with an [[action]] by the respective $\Sigma_n$.

### Hopf interval object

+-- {: .num_defn }
###### Definition

An object $H \in V$ is a [[Hopf algebra]] object if it is equipped with the structure of a [[monoid]], that of a [[comonoid]] such that product and coproduct preserve each other.

If $V$ is equipped with a compatible structure of a [[monoidal model category]] we say that a a Hopf algebra object is an **Hopf [[interval object]]** if it is equipped with morphisms

$$
  I \coprod I \hookrightarrow H \stackrel{\simeq}{\to} I
$$

that factor the [[codiagonal]] on $I$ by a cofibration followed by a weak equivalence.
 
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


+-- {: .num_remark}
###### Remark

Since the coalgebra interval in the [[category of chain complexes]] is not cocommutative, this case requires special discussion, as some of the statements below will not apply to it. For more on this case see [[model structure on dg-operads]].

=--

### Model category structure

Assume now that $V$ is moreover equipped with a compatible structure of a [[monoidal model category]].

+-- {: .num_lemma }
###### Lemma

If $V$ is a [[cofibrantly generated model category]], then for each [[finite group]] $G$ the [[transferred model structure]] on $V^{\mathbf{B}G}$ along the [[forgetful functor]]

$$
 U :  V^{\mathbf{B}G} \to V
$$

exists.

It follows that in this case the category of collections $Coll(V)$ is a [[cofibrantly generated model category]] where a morphisms is a fibration or weak equivalence if it is so degreewise in $V$, respectively.

=--

+-- {: .num_lemma #SigmaCofibrant}
###### Lemma

A $V$-operad is called **$\Sigma$-cofibrant** if its underlying collection is cofibrant in the above model stucture

=--

A $V$-operad $P$ is called _reduced_ if $P(0)$ is the tensor unit, $P(0) = I$.  A morphism of reduced operads is one that is the identity on the 0-component. 

+-- {: .num_theorem #ModelStrucOnOperads}
###### Theorem

If 

* $V$ is [[cofibrantly generated model category|cofibrantly generated]] 

* $I$ is cofibrant;

* the [[model structure on an over category|model structure on the overcategory]] $V/I$ has a [[symmetric monoidal functor|symmetric monoidal]] fibrant [[resolution|replacement]] functor;

* $V$ admits a commutative Hopf interval object.

Then there exists a [[cofibrantly generated model category]] structure on the category of reduced $V$-[[operad]]s, in which 

* a morphism $P \to Q$ is a weak equivalence (resp. fibration) precisely if for all $n \gt 0$ the morphisms $P(n) \to Q(n)$ are weak equivalences (resp. fibrations) in $V$.

=--

+-- {: .proof}
###### Proof

This is [BergerMoerdijk, theorem 3.1](#BergerMoerdijkHomotopy).

=--

If $V$ is even a [[cartesian closed category]], a stronger statement is possible:

+-- {: .num_theorem }
###### Theorem

Let $V$ be a [[cartesian closed category]], such that

* $V$ is [[cofibrantly generated model category|cofibrantly generated]] and the [[terminal object]] is cofibrant;

* $V$ has a symmetric monoidal fibrant replacement functor.

Then there exists a cofibrantly generated model structure on the category of $V$-operads, in which a morphism $P \to Q$ is a weak equivalence (resp. fibration) precisely if for all $n \geq 0$ the morphisms $P(n) \to Q(n)$ are weak equivalences (resp. fibrations) in $V$.



=--




## Examples

The conditions of the above theorems are satisfied for

* $V = $ [[sSet]] with the standard [[model structure on simplicial sets]].

  The induced model structure on $sSet$-operads is [[Quillen equivalence|Quillen equivalent]] to the [[model structure on dendroidal sets]].

* $V = $ [[Top]] the equivalence model structure on compactly generated topological spaces;

  The _homotopy algebras_ over a simplicial/topological operad as defined by Boardman and Vogt (see references below), are algebras for cofibrant replacements of these operads in this moel structure. This is essentially the statement of theorem 4.1 in ([Vogt](#Vogt))


* $V = Ch_\bullet$, the [[model structure on chain complexes]];

* $V = sSh(C)$ the [[model structure on simplicial sheaves]] on some [[site]] $C$.

In these contexts, 

* the [[associative operad]] is admissible $\Sigma$-cofibrant

  ([BergerMoerdijk, page 15](#BergerMoerdijkHomotopy))

* the [[commutative operad]] is far from being $\Sigma$-cofibrant.

This means we have rectification theorems for [[A-∞ algebras]] but not for [[E-∞ algebras]]. See [[model structure on algebras over an operad]] for more.

## Properties

### Cofibrancy

+-- {: .num_prop }
###### Proposition

Every cofibrant operad is also $\Sigma$-[cofibrant](#SigmaCofibrancy).

=--

This is ([BergerMoerdijk, prop. 4.3](#BergerMoerdijkHomotopy)).


+-- {: .num_remark }
###### Remark

The relebance of this is in section [Homotopy algebras](#HomotopyAlgebras): this property enters the proof of the statement that the [[model structure on algebras over an operad]] over a $\Sigma$-cofibrant resolution is already Quillen equivalent to that of a full cofibrant resolution.

Many resolutions of operads that appear in the literature are in fact just $\Sigma$-cofibrant.

=--



### Resolutions {#Resolutions}


We now discuss the construction and properties of cofibrant [[resolution]]s of operads and their algebras.

> (assumptions now as at [[model structure on algebras over an operad]])

First we describe _free_ operads, and then _[[Boardman-Vogt resolution]]s_ of operads, obtained from the construction of the free ones by adding labels for _lengths_ in an [[interval object]]
 
+-- {: .num_remark}
###### Remark

The category of $C$-coloured operads is itself the category of [[algebra over an operad|algebras over]] a [[non-symmetric operad]]. See [[coloured operad]] for more. Thus the above theorem provides conditions under which $C$-coloured operads carry a model structure in which fibrations and weak equivalences are those morphisms of operads $P \to Q$ that are  degreewise fibrations and weak equivalences in $\mathcal{E}$.

=--

+-- {: .num_defn}
###### Terminology

We shall from now on call an operad $P$ **cofibrant** if the morphism $I_C \to P$ from the initial $C$-[[coloured operad]] has the [[left lifting property]] against degreewise acyclic fibrations of operads (irrespective of whether the above conditions for the existence of the model structure hold).

=--



+-- {: .num_theorem}
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

This is  ([BergerMoerdijk, theorem 3.2](#BergerMoerdijkAlgebras)).


+-- {: .num_theorem}
###### Theorem

For each well-pointed  $\Sigma$-[cofibrant](#SigmaCofibrancy) $C$-coloured operad $P$, the $(F^*_C \dashv U_C)$-counit factors as a cofibration followed by a weak equivalence

$$
  F_C^*(P) \hookrightarrow W(H,P) \stackrel{\simeq}{\to} P
$$

of $C$-coloured operads, [[natural transformation|naturally]] in $P$ and $H$.

If $P \to Q$ is a $\Sigma$-cofibration between well-pointed $\Sigma$-cofibrant $C$-coloured operads, then the induced map $W(H,P) \to W(H,Q)$ is a cofibration of cofibrant $C$-coloured operads.

=--

This is  ([BergerMoerdijk, theorem 3.5](#BergerMoerdijkAlgebras)).

Here $W(H,P)$ is also called the **coloured [[Boardman-Vogt resolution]]** of $P$.

An [[algebra over an operad]] over $W(H,P)$ is called a **$P$-algebra up to homotopy**.


### Homotopy algebras over an operad {#HomotopyAlgebras}

We discuss model structures on algebras over resolutions of operads. A more  detailed treatment is at [[model structure on algebras over an operad]].


With $V$ as above, say 


+-- {: .num_defn}
###### Definition

A $V$-operad $P$ is _admissible_ if the category of $P$-[[algebra over an operad|algebras]] carries a [[transferred model structure]] from the [[free functor]]/[[forgetful functor]] [[adjunction]]

$$
  F_P : V \stackrel{\leftarrow}{\to} Alg_P : U_P
  \,.
$$

=--

Under mild assumptions on $V$, cofibrant operads are admissible.

+-- {: .num_defn }
###### Definition

For an arbirtrary $V$-operad $P$, [[generalized the|the]] category of **homotopy $P$-algebras** is the category of $\hat P$-algebras for some cofibrant replacement $\hat P$ of $P$.

=--

Indeed, this is well defined up to [[Quillen equivalence]]:

[BerMor03, corollary 4.5](http://arxiv.org/PS_cache/math/pdf/0206/0206094v3.pdf#page=15).

Moreover, for this it is sufficient that $\hat P$ be _$\Sigma$-[cofibrant](#SigmaCofibrancy)_ . 

+-- {: .num_prop }
###### Proposition

If $V$ is a [[left proper model category]] with cofibrant unit, then for $\hat P$ a $\Sigma$-[cofibrant](#SigmaCofibrancy) [[resolution]] of $P$ (not necessarily fully cofibrant!) the category of $\hat P$ algebras is [[Quillen equivalence|Quillen equivalent]] to that of homotopy $P$-algebras.

=--

For instance the [[associative operad]] is $\Sigma$-cofibrant, so that by the above every $A-\infty$-algebra may be rectified to an ordinary monoid.

See around [BerMor03, remark 4.6](http://arxiv.org/PS_cache/math/pdf/0206/0206094v3.pdf#page=15).

For more see [[model structure on algebras over an operad]].


## Related concepts

* [[(∞,1)-operad]], **model structure on operads**

  * [[canonical model structure on Operad]], [[model structure on dendroidal sets]]

  * [[algebra over an (∞,1)-operad]], [[model structure on algebras over an operad]]

    * [[module over an algebra over an (∞,1)-operad]], [[model structure on modules over an algebra over an operad]]


* [[A-∞ operad]]

* [[E-∞ operad]]

## References

An influential article in which many of the homotopical and $(\infty,1)$-categorical aspects of operad theory originate is

* [[Michael Boardman]] and [[Rainer Vogt]], _Homotopy invariant algebraic structures on topological spaces_ , Lect. Notes Math. 347 (1973).

An early notion of [[resolution]] of operads in [[chain complex]]es is given in section 3 of 

* [[Martin Markl]], _Models for Operads_ ([arXiv](http://arxiv.org/abs/hep-th/9411208))

Cofibrant [[Boardman-Vogt resolution]]s of operads are discussed in

* [[Rainer Vogt]], _Cofibrant operads and universal $E_\infty$-operads_ , 
Bielefeld SB 343 (1999), to appear in Topology Appl.

A systematic study of [[model category]] structures on operads and their algebras is in

* [[Clemens Berger]], [[Ieke Moerdijk]], _Axiomatic homotopy theory for operads_ Comment. Math. Helv. 78 (2003), 805&#8211;831. ([arXiv:math/0206094](http://arxiv.org/abs/math/0206094))
{#BergerMoerdijkHomotopy}

An explicit construction of cofibrant resolution in this model structure and its relation to the original constructon of the [[Boardman-Vogt resolution]] is in

* [[Clemens Berger]], [[Ieke Moerdijk]], _The Boardman-Vogt resolution of operads in monoidal model categories_ , Topology 45 (2006), 807&#8211;849. ([pdf](http://math.unice.fr/~cberger/BV.pdf))
{#BergerMoerdijkResolution}

The induced model structures and their properties on [[algebras over operads]] are discussed in

* [[Clemens Berger]], [[Ieke Moerdijk]], _Resolution of coloured operads and rectification of homotopy algebras_ ([arXiv:math/0512576](http://arxiv.org/abs/math/0512576))
{#BergerMoerdijkAlgebras}

The [[model structure on dg-operads]] is discussed in

* [[Vladimir Hinich]],  _Homological algebra of homotopy algebras_ Communications in algebra, 25(10). 3291-3323 (1997)([arXiv:q-alg/9702015](http://arxiv.org/abs/q-alg/9702015), _Erratum_ ([arXiv:math/0309453](http://arxiv.org/abs/math/0309453)))
{#Hinich}

