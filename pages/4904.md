
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
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

For $T$ a [[Lawvere theory]] and $T Alg$ the [[category]] of [[algebra over a Lawvere theory]], there is a [[model category]] structure on the category $T Alg^{\Delta^{op}}$ of [[simplicial object|simplicial]] $T$-algebras which models the $\infty$-algebras for $T$ regarded as an [[(∞,1)-algebraic theory]].

## Details

First we consider the case of [[simplicial objects]] in algebras over an ordinary Lawvere theory:

* _[For algebras over ordinary Lawvere theories](#OverOrdinaryLawvereTheories)_

Then we generalize to the case that the Lawvere theory itself is simplicial: 

* _[For algebras over simplicial Lawvere theories](#ForAlgebrasOverSimplicialLawvereTheories)_


### For algebras over ordinary Lawvere theories
  {#OverOrdinaryLawvereTheories}

Recall that the [[(∞,1)-category of (∞,1)-presheaves]] $PSh_{(\infty,1)}(C^{op})$ itself is modeled by the [[model structure on simplicial presheaves]]

$$
  PSh_{(\infty,1)}(C^{op})
  \simeq
  [C, sSet]^\circ
  \,,
$$

where we regard $C$ as a [[Kan complex]]-[[enriched category]] and have on the right the [[sSet]]-[[enriched functor category]] with the projective or injective model structure, and $(-)^\circ$ denoting the full enriched subcategory on fibrant-cofibrant objects.

This says in particular that every weak $(\infty,1)$-functor $f : C \to \infty \mathrm{Grp}$ is equivalent to a _rectified_ one $F : C \to KanCplx$. And $f \in PSh_{(\infty,1)}(C^{op})$ belongs to $Alg_{(\infty,1)}(C)$ if $F$ preserves finite products _weakly_  in that for $\{c_i \in C\}$ a finite collection of objects, the canonical natural morphism

$$
  F(c_1 \times \cdots, \c_n)
  \to
  F(c_1) \times \cdots \times F(c_n)
$$ 

is a [[homotopy equivalence]] of [[Kan complexes]].

We now look at model category structure on _strictly_ product preserving functors $C \to sSet$, which gives an equivalent model for $Alg_{(\infty,1)}(C)$. See [[model structure on homotopy T-algebras]].

+-- {: .num_prop #ModelStructureOnSimplicialAlgebrasOverOrdinaryLawveretheory}
###### Proposition

Let $T$ be the [[syntactic category]] of a [[Lawvere theory]], and let $T Alg^{\Delta^{op}} \subset Func(T,sSet)$ be the [[full subcategory]] of the [[functor category]] from $T$ to [[sSet]] on those functors that preserve these [[finite products]].  

Then $T Alg^{\Delta^{op}}$ carries the structure of a [[model category]] $(T Alg^{\Delta^{op}})_{proj}$ where the weak equivalences and the fibrations are those maps underlying which are weak equivalences or fibrations, respectively, in the [[classical model structure on simplicial sets]]. 

=--

This is due to ([Quillen 67, II.4 theorem 4](#Quillen67)).

The inclusion $i : sAlg(C) \hookrightarrow sPSh(C^{op})_{proj}$ into the projective [[model structure on simplicial presheaves]] evidently preserves fibrations and acyclic fibrations and gives a [[Quillen adjunction]]

$$
  sAlg(C)_{proj}
  \stackrel{\leftarrow}{\underset{i}{\hookrightarrow}}
  sPSh(C^{op})
  \,.
$$


+-- {: .num_prop}
###### Proposition

The total right [[derived functor]] 

$$
  \mathbb{R}i \;\colon\; Ho(sAlg(C)_{proj}) \to Ho(sPSh(C^{op})_{proj})
$$ 

is a [[full and faithful functor]] and an object $F \in sPSh(C^{op})$ belongs to the [[essential image]] of $\mathbb{R}i$ precisely if it preserves products up to [[weak homotopy equivalence]].

=--

This is due to ([Badzioch 02, def. 5.2, prop. 5.4, cor. 5.7](#Badzioch02)).

It follows that the natural $(\infty,1)$-functor

$$
  (sAlg(C)_{proj})^\circ 
    \stackrel{}{\longrightarrow}
  PSh_{(\infty,1)}(C^{op})
$$

is an [[equivalence of quasi-categories|equivalence]].



### For algebras over simplicial Lawvere theories
 {#ForAlgebrasOverSimplicialLawvereTheories}

+-- {: .num_defn #SimplicialLawvereTheory}
###### Definition

Let $\Gamma = (Skel(FinSet^{\ast/}))$ be [[Segal's category]], the [[opposite category]] of a [[skeleton]] of [[finite set|finite]] [[pointed sets]].

A _[[simplicial Lawvere theory]]_ is a a pointed [[simplicial category]] $T$ equipped with a [[functor]] $i \;\colon\;\Gamma \to T$ such that 

1. $T$ has the same [[set]] of [[objects]] as $\Gamma$;

1. $i$ is the identity on objects

1.  $i$ preserves [[finite products]]

Given a simplicial theory $T$, then a _simplicial $T$-algebra_ is a product preserving [[simplicial functor]] $X$ to the [[simplicial category]] of [[pointed simplicial sets]]. The simplicial set

$$
  X(1_+) \in sSet
$$

(the value on the pointed 2-element set) is called the _underlying simplicial set_ of the $T$-algebra.

A [[homomorphism]] of $T$-algebras is a simplicial [[natural transformation]] between such functors. Write

$$
  T Alg \in sSet Cat
$$

for the resulting [[simplicial category]].

A homomorphism is called a _weak equivalence_ or a _fibration_ if on underlying simplicial sets it is a weak equivalence or fibration, respectively, in the [[classical model structure on simplicial sets]].
Write

$$
  (T Alg)_{proj}
$$

for the category equipped with these [[classes]] of morphisms.

=--

([Schwede 01, def. 2.1 and def. 2.2 and beginning of section 3](#Schwede01))

+-- {: .num_remark}
###### Remark

In the case that the [[simplicial Lawvere theory]] $T$ happens to be simplicially discrete, i.e. an ordinary [[category]], then the category $(T Alg)_{proj}$ of simplicial $T$-algebras from def. \ref{SimplicialLawvereTheory} with that from prop. \ref{ModelStructureOnSimplicialAlgebrasOverOrdinaryLawveretheory}.

=--

+-- {: .num_prop}
###### Proposition

For $T$ a [[simplicial Lawvere theory]] (def. \ref{SimplicialLawvereTheory}) the category $(T Alg)_{poj}$ from def. \ref{SimplicialLawvereTheory} is a [[simplicial model category]].

=--

This is due to ([Reedy 74, theorem I](#Reedy74)), reviewed in ([Schwede 01](#Schwede01)).

The analogous statement with the [[classical model structure on simplicial sets]] replaced by the [[classical model structure on topological spaces]] is due to ([Schw&#228;nzl-Vogt 91](#Schw&#228;nzlVogt91)9




A comprehensive statement of these facts is in [[Higher Topos Theory|HTT, section 5.5.9]].

### Other cases
 {#OtherCases}

+-- {: .num_prop #QuillenCriterion}
###### Proposition

Let $\mathcal{C}$ be a [[category]] with [[enough projectives]]. Say that a morphism $f$ in the category $\mathcal{C}^{\Delta^{\mathrm{op}}}$ of [[simplicial objects]] in $\mathcal{C}$ is a _weak equivalence_ or _fibration_ if for every [[projective object]] $P \in \mathcal{C}$ then $Hom(P,f)$ is a weak equivalence or fibration, respectively, in the [[classical model structure on simplicial sets]] (i.e. a [[Kan fibration]] or [[weak homotopy equivalence]], respectively). If now at least one of the following conditions is satisfied, 

* every object of $\mathcal{C}^{\Delta^{op}}$ is fibrant;

* $\mathcal{C}$ is closed under [[colimits]] and has a [[small set]] of [[projective object|projective]] [[generators]];

then this makes $\mathcal{C}^{\Delta^{op}}$ a [[simplicial model category]].



=--

([Quillen 67, II.4, theorem 4](#Quillen67))


## Properties

### Relation to homotopy $T$-algebras

+-- {: .num_theorem}
###### Theorem

There is a [[Quillen equivalence]] between the model structure on simplicial $T$-algebras and the model structure for [[homotopy T-algebra]]s. (See there).

=--

This is ([Badzioch 02, theorem 1.3](#Badzioch02)).

### Homotopy groups

Let $T$ be an _abelian Lawvere theory_,  a theory that contains the theory of [[abelian group]], $Ab \to T$. Then every simplicial $T$-algebra has an underlying [[simplicial abelian group]] and is necessarily a [[Kan complex]].

+-- {: .num_prop}
###### Observation

The [[homotopy groups]] $\pi_*$ of a simplicial abelian $T$-agebra form an $\mathbb{N}$-graded $T$-algebra $\pi_*(A)$

=--

+-- {: .num_prop}
###### Observation

The inclusion of the full [[subcategory]] $i : T Alg \hookrightarrow T Alg^{\Delta^{op}}$ of ordinary $T$-algebra as the simplicially constant ones constitutes a [[Quillen adjunction]]

$$
  (\pi_0  \dashv i) : T Alg \stackrel{\overset{\pi_0}{\leftarrow}}{\underset{i}{\hookrightarrow}}
  T Alg^{\Delta^{op}}
$$

from the [[trivial model structure]] on $T Alg$.

The [[derived functor]] $\mathbb{R} i : T Alg \to Ho(T Alg^{\Delta^{op}})$ is a  [[full and faithful functor]].

=--

This allows us to think of ordinary $T$-algebras a sitting inside $\infty$-$T$-algebras.


> all this is certainly true for ordinary $k$-algebras. Need to spell out general proof.
> I believe this is the Badzioch paper cited above - JB


## Examples

### Simplicial associative $k$-algebras

A [[simplicial ring]]s is a simplicial $T$-algebras for $T$ the Lawvere theory of rings. 

Let $k$ be an ordinary commutative ring and $T$ the theory of commutative [[associative algebras]] over $k$. We write $T Alg$ as $sCAlg_k$ or $CAlg_k^{op}$.

Such simplicial $k$-algebras are discussed for instance in ([To&#235;n-Vezzosi, section 2.2.1](#ToenVezzosi)).
According to ([Schwede 97](#Schwede97), Lemma 3.1.3), this model structure is [[proper model category|proper]].

### Simplicial commutative $k$-algebras

The following is a variant of the model structure on simplicial commutative algebras that is implied by the above general theorem.

+-- {: .num_prop}
###### Proposition
**(second model structure)**

Let $T$ be the [[Lawvere theory]] for  ([[associative algebra|associative]] and) [[commutative algebras]] over a [[ring]] $k$. Then $(cAlg_k)^{\Delta^{op}}$ becomes a [[simplicial model category]] with

* weak equivalences the morphisms whose underlying morphism of simplicial sets are weak equivalences in the [[classical model structure on simplicial sets]];

* fibrations the morphisms $X \to Y$ such that $X \to \pi_0 X \times_{\pi_0 Y} Y$ is a degreewise surjection.

=--

This appears as ([Goerss-Schemmerhorn, theorem 4.17](#GoerssSchemmerhorn)).


### Simplicial Lie algebras

See at _[[model structure on simplicial Lie algebras]]_.

### Simplicial complete Hopf algebras
 {#SimplicialCommutativeHopfAlgebras}

Complete rational [[Hopf algebras]] are not the models of a [[Lawvere theory]], even though in some sense they are close ([Quillen 67, bottom of p. 265 (61 of 92)](#Quillen67)).

But they do satisfy the assumptions of proposition \ref{QuillenCriterion} ([Quillen 69, appendix B, prop. 2.24](#Quillen69)). Hence simplicial rational complete Hopf algebras form a [[simplicial model category]]. 

## Related concepts

* [[model structure on simplicial abelian groups]]

* [[model structure on cosimplicial algebras]]

* [[model structure on monoids]]

* [[algebra over a monad]]

  [[∞-algebra over an (∞,1)-monad]] 

  * [[model structure on algebras over a monad]]

* [[algebra over an algebraic theory]] 

  [[∞-algebra over an (∞,1)-algebraic theory]]

  * [[homotopy T-algebra]]

* [[algebra over an operad]] 

   [[∞-algebra over an (∞,1)-operad]]

   * [[model structure on algebras over an operad]]




## References

The classical reference for the [[transferred model structure]] on simplicial $T$-algebras is

* {#Quillen67} [[Daniel Quillen]], Section II.4 item 5 in: _[[Homotopical Algebra]]_, Lecture Notes in Mathematics 43, Springer 1967([doi:10.1007/BFb0097438](https://doi.org/10.1007/BFb0097438))

with some further remarks in

* {#Quillen69} [[Dan Quillen]], Section II.3 of: _Rational homotopy theory_, The Annals of Mathematics, Second Series, Vol. 90, No. 2 (Sep., 1969), pp. 205-295 ([JSTOR](http://www.jstor.org/stable/1970725), [pdf](http://www.math.northwestern.edu/~konter/gtrs/rational.pdf))


The generalization to the case that the theory $T$ itself is allowed to be simplicial is due to 

* {#Reedy74} [[Christopher Reedy]], _Homology of algebraic theories_, Ph.D. Thesis, University of California, San Diego, 1974

and the topological version is due to

* {#Schw&#228;nzlVogt91} [[Roland Schwänzl]], [[Rainer Vogt]], _The categories of $A_\infty$- and $E_\infty$-monoids and ring spaces as closed simplicial and topological model categories_, Archives of Mathematics 56 (1991) 405-411



More is in

* {#Schwede01} [[Stefan Schwede]], _Stable homotopy of algebraic theories_, Topology 40 (2001) 1-41 ([pdf](http://www.math.uni-bonn.de/people/schwede/stable.pdf))


In 

* {#Rezk} [[Charles Rezk]], _Every homotopy theory of simplicial algebras admits a proper model_ ([math/0003065](http://arxiv.org/abs/math/0003065)) ,


it is discussed that every model category of simplicial $T$-algebras is [[Quillen equivalence|Quillen equivalent]] to a left [[proper model category]].

The fact that the model structure on simplicial $T$-algebras serves to model $\infty$-algebras is in

* {#Badzioch02} [[Bernard Badzioch]], _Algebraic theories in homotopy theory_, Annals of Mathematics, 155 (2002), 895-913 ([JSTOR](http://www.jstor.org/stable/3062135))

and the multi-sorted version is in 

* {#Bergner07} [[Julie Bergner]], _Rigidification of algebras over multi-sorted theories_, Algebraic and Geometric Topoogy 7 (2007) ([arXiv:0508152](https://arxiv.org/abs/math/0508152))


The simplicial model structure on ordinary simplicial algebras (i.e. simplicial [[associative algebras]]) is discussed in

* [[Paul Goerss]], [[Kirsten Schemmerhorn]], _Model categories and simplicial methods_ ([pdf](http://www.math.northwestern.edu/~pgoerss/papers/ucnotes.pdf))


* {#Schwede97} [[Stefan Schwede]], _Spectra in model categories and applications to the algebraic cotangent complex_, Journal of Pure and Applied Algebra 120 (1997), pp. 77-104, [pdf](http://www.math.uni-bonn.de/people/schwede/modelspec.pdf).


Discussion of simplicial commutative associative algbras over a ring in the context of [[derived geometry]] is in

* {#ToenVezzosi} [[Bertrand Toën]], [[Gabriele Vezzosi]], _Homotopical Algebraic Geometry II: geometric stacks and applications _ ([arXiv](http://arxiv.org/abs/math/0404373))

Discussion of divided [[power operations]] on simplicial algebras is in

* [[Benoit Fresse]], _On the homotopy of simplicial algebras over an operad_, Transactions of the AMS, volume 352, number 9 ([jstor](http://www.jstor.org/stable/118177))



[[!redirects model structure on simplicial T-algebras]]

[[!redirects simplicial T-algebra]]

[[!redirects simplicial algebra]]
[[!redirects simplicial algebras]]


