
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
* automatic table of contents goes here
{:toc}

## Idea

If $V$ is a [[symmetric monoidal category]] that is also a [[monoidal model category]], then under suitable conditions there is also the structure of a [[model category]] on the category of $V$-[[operad]]s. 

This is important for the notion of _homotopy_ [[algebra over an operad]], such as $A_\infty$- and $E_\infty$-algebras.


## Definition

Recall that a $V$-operad $P$ is called _reduced_ if $P(0)$ is the tensor unit, $P(0) = I$.  

+-- {: .un_theorem }
###### Theorem


Let $V$ be a [[symmetric monoidal model category|symmetric]] [[monoidal model category]] with unit $I$, such that

* $V$ is [[cofibrantly generated model category|cofibrantly generated]] and $I$ is cofibrant;

* the [[model structure on an over category|model structure on the overcategory]] $V/I$ has a symmetric monoidal fibrant replacement functor;

* $V$ admits a commutative Hopf [[interval object]].

Then there exists a cofibrantly generated model structure on the category of reduced $V$-operads, in which a morphism $P \to Q$ is a weak equivalence (resp. fibration) precisely if for all $n \gt 0$ the morphisms $P(n) \to Q(n)$ are weak equivalences (resp. fibrations) in $V$.

=--

+-- {: .proof}
###### Proof

This is [BerMor03, theorem 3.1](http://arxiv.org/PS_cache/math/pdf/0206/0206094v3.pdf#page=8).

=--

If $V$ is even a [[cartesian closed category]], a stronger statement is possible:

+-- {: .un_theorem }
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

  The _homotopy algebras_ over a simplicial/topological operad as defined by Boardman and Vogt (see references below), are algebras for cofibrant replacements of these operads in this moel structure. This is essentially the statement of theorem 4.1 in

  * [[Rainer Vogt]], 
    _Cofibrant operads and universal $E_\infty$-operads_ , 
    Bielefeld SB 343 (1999), to appear in Topology Appl.


* $V = Ch_\bullet$, the [[model structure on chain complexes]];

* $V = sSh(C)$ the [[model structure on simplicial sheaves]] on some [[site]] $C$.

## Properties

### Resolutions {#Resolutions}


We now discuss the construction and properties of cofibrant [[resolution]]s of operads and their algebras.

> (assumptions now as at [[model structure on algebras over an operad]])

First we describe _free_ operads, and then _Boardman-Vogt resolutions_ of operads, obtained from the construction of the free ones by adding labels for _lengths_ in an [[interval object]]
 
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

This is  ([BergerMoerdijk, theorem 3.2](#BergerMoerdijkAlgebras)).


+-- {: .un_theorem}
###### Theorem

For each well-pointed  $\Sigma$-cofibrant $C$-coloured operad $P$, the $(F^*_C \dashv U_C)$-counit factors as a cofibration followed by a weak equivalence

$$
  F_C^*(P) \hookrightarrow W(H,P) \stackrel{\simeq}{\to} P
$$

of $C$-coloured operads, [[natural transformation|naturally]] in $P$ and $H$.

If $P \to Q$ is a $\Sigma$-cofibration between well-pointed $\Sigma$-cofibrant $C$-coloured operads, then the induced map $W(H,P) \to W(H,Q)$ is a cofibration of cofibrant $C$-coloured operads.

=--

This is  ([BergerMoerdijk, theorem 3.5](#BergerMoerdijkAlgebras)).

Here $W(H,P)$ is also called the **coloured Boardman-Vogt resolution** of $P$.

An [[algebra over an operad]] over $W(H,P)$ is called a **$P$-algebra up to homotopy**.


### Homotopy algebras over an operad

With $V$ as above, say a $V$-operad $P$ is _admissible_ if the category of $P$ [[algebra over an operad|algebras]] carries a [[transferred model structure]] from the free-forgetful adjunction

$$
  F_P : V \stackrel{\leftarrow}{\to} Alg_P : U_P
  \,.
$$

Under mild assumptions on $V$, cofibrant operads are admissible.

+-- {: .un_theorem }
###### Theorem

For an arbirtrary $V$-operad $P$, [[generalized the|the]] category of **homotopy $P$-algebras** is the category of $\hat P$-algebras for some cofibrant replacement $\hat P$ of $P$.

=--

Indeed, this is well defined up to [[Quillen equivalence]]:

[BerMor03, corollary 4.5](http://arxiv.org/PS_cache/math/pdf/0206/0206094v3.pdf#page=15).

Moreover, for this it is sufficient that $\hat P$ be _$\Sigma$-cofibrant_ . 

For instance the [[associative operad]] is $\Sigma$-cofibrant, so that by the above every $A-\infty$-algebra may be rectified to an ordinary monoid.

See around [BerMor03, remark 4.6](http://arxiv.org/PS_cache/math/pdf/0206/0206094v3.pdf#page=15).

For more see [[model structure on algebras over an operad]].


## Related concepts

* **model structure on operads**

* [[model structure on algebras over an operad]]

## References

An influential article in which many of the homotopical and $(\infty,1)$-categorical aspects of operad theory originate is

* [[Michael Boardman]] and [[Rainer Vogt]], _Homotopy invariant algebraic structures on topological spaces_ , Lect. Notes Math. 347 (1973).

A systematic study of [[model category]] structures on operads and their algebras is in

* [[Clemens Berger]], [[Ieke Moerdijk]], _Axiomatic homotopy theory for operads_ Comment. Math. Helv. 78 (2003), 805&#8211;831.
{#BergerMoerdijkHomotopy}

An explicit construction of cofibrant resolution in this model structure and its relation to the original constructon by Boardman and Vogt is in

* [[Clemens Berger]], [[Ieke Moerdijk]], _The Boardman-Vogt resolution of operads in monoidal model categories_ , Topology 45 (2006), 807&#8211;849. ([pdf](http://math.unice.fr/~cberger/BV.pdf))
{#BergerMoerdijkResolution}

The induced model structures and their properties on [[algebras over operads]] are discussed in

* [[Clemens Berger]], [[Ieke Moerdijk]], _Resolution of coloured operads and rectification of homotopy algebras_ ([arXiv:math/0512576](http://arxiv.org/abs/math/0512576))
{#BergerMoerdijkAlgebras}
