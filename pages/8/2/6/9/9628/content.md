+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

Hopf algebroids have a base and a total algebra (and some other data).
There are 3 levels of generality: commutative Hopf algebras (classical case, both base and the total space are commutative), Hopf algebras with commutative base (studied from late 1980s: Maltsionitis, later Connes' school etc) and genuinely noncommutative case for which see [[Hopf algebroid]] and [[bialgebroid]].

## Idea

Just as for [[groups]] and their [[Hopf algebras]], there are _two_ ways to assign a __Hopf algebroid over a commutative base algebra__ to a [[groupoid]] $\mathcal{G}_\bullet$: 

1. ([[commutative Hopf algebroids]]) with **commutative but non-co-commutative total algebra**: Form the [[commutative algebra|commutative]] [[algebras of functions]] $C(\mathcal{G}_1)$ and $C(\mathcal{G}_0)$ and regard the operation induced by the partially defined [[composition]] in $\mathcal{G}_\bullet$ as an in general non-co-commutative [[coalgebra]] structure on $C(\mathcal{G}_1)$ over $C(\mathcal{G}_0)$; the graded 
commutative case appears in algebraic topology and is classical 
(Steenrod algebra and other examples);

1. with **non-commutative but co-commutative total algebra**: Form the in general non-commutative [[groupoid convolution algebra]] $C_{conv}(\mathcal{G})$ and regard it as a co-commutative [[coalgebra]] over $C(\mathcal{G}_0)$.

Given an internal [[groupoid]] in the category $Aff_k$ of affine algebraic $k$-[[schemes]], where $k$ is a field, the $k$-algebras of [[global sections]] over the scheme of objects and the scheme of morphisms have an additional structure of a commutative Hopf algebroid. In fact this is an [[dual equivalence|antiequivalence of categories]]. Commutative Hopf algebroids are useful also in a version in [[brave new algebra]] (the work of John Rognes).

## Higher groupoid convolution algebras and n-vector spaces/n-modules

> under construction

We discuss here a natural generalization of the notion of [[groupoid convolution algebras]] to [[higher algebra|higher algebras]] for [[n-groupoid|higher groupoids]]. 

There may be several sensible such generalizations. The one discussed now follows the principle of iterated [[internalization]] and naturally matches to the concept of [[n-modules]] ([[n-vector spaces]]) as they appear in [[extended prequantum field theory]].

In order to disentangle conceptual from technical aspects, we first discuss [[discrete ∞-groupoid|geometrically discrete higher groupoids]]. The results of this discussion then in particular help to suggest what the right definition of "higher Lie groupoid" in the ontext of higher convolution algebras should be in the first place.

The consideration are based on the following

+-- {: .num_remark}
###### Remark

By the discussion at _[[2-module]]_ we may think of the [[2-category]] $k Alg_b$ of $k$-[[associative algebras]] and [[bimodules]] between them as a model for the 2-category [[2Mod]] of $k$-[[2-modules]] that admit a 2-[[basis]] ([[2-vector spaces]]). Hence the groupoid convolution algebra constructiuon is a 2-functor 

$$
  C \;\colon\; Grpd \to 2 Mod
  \,.
$$


There is then the following systematic refinement of this to higher groupoids and higher algebra: by the discussion at _[[n-module]]_, 3-modules are algebra objects in [[2Mod]] and maps between them are [[bimodule]] objects in there. An algebra object in  $k Alg_b$ is equivalently a [[sesquialgebra]], an algebra equipped with a second algebra structure up to coherent homotopy, that is exhibited by structure bimodules. 

Special cases of this are [[bialgebras]], for which these structure bimodules come from actual algebra homomorphisms. Examples of these in turn are [[Hopf algebras]]. These we naturally re-discover as special higher groupoid convolution higher algebras in example \ref{DoubleGroupoid2AlgebraOfDeloopingOfFiniteGroup} below. 

=--


This iterated internalization on the codomain of the groupoid convolution algebra functor has a natural analog on its domain: a 2-groupoid we may present by a [[double groupoid]], namely a [[groupoid object in an (∞,1)-category]] in [[Grpd]] which is 3-[[coskeleton|coskeletal]] as a [[simplicial object]] in [[Grpd]].

+-- {: .num_remark}
###### Remark

Given a [[groupoid object in an (∞,1)-category|groupoid object]] $\mathcal{G}_\bullet$ in the [[(2,1)-topos]] [[Grpd]] hence a [[double groupoid]], applying the groupoid convolution algebra $(2,1)$-functor $C$ to the corresponding [[simplicial object]] $\mathcal{G}_\bullet \in Grpd^{\Delta^{op}}$ yields:

* groupoid convolution algebras $C(\mathcal{G}_0)$ and $C(\mathcal{G}_1)$,

* a $C(\mathcal{G}_1) \otimes_{C(\mathcal{G}_{0,1})} C(\mathcal{G}_1)-C(\mathcal{G}_{0})$-bimodule, assigned to the [[composition]] functor $\partial_1 \colon \mathcal{G}_1 \underset{\mathcal{G}_0}{\times} \mathcal{G}_1 \to \mathcal{G}_1$.

Under the 2-functoriality of $C$, the [[Segal conditions]] satisfied by $\mathcal{G}_\bullet$ make this bimodule exhibi a [[sesquialgebra]] structure over $C(\mathcal{G}_{0,1})$.

This sesquialgebra we call the the **double groupoid convolution 2-algebra** of $\mathcal{G}_\bullet$.

(Here we make invariant sense of the [[tensor product]] by evaluating on a [[Reedy model structure|Reedy fibrant]] representative.)

=--

+-- {: .num_example #DoubleGroupoid2AlgebraOfDeloopingOfFiniteGroup}
###### Example

Let $G$ be a [[finite group]]. Write $\mathbf{B}G$ for its [[delooping]] [[groupoid]] (the connected groupoid with $\pi_1 = G$). There are two natural ways to present $\mathbf{B}G$ as a [[double groupoid]]:

1. $\underset{\longrightarrow}{\lim}(\cdots \mathbf{B}G \stackrel{\overset{id}{\to}}{\underset{id}{\to}} \mathbf{B}G) \simeq \mathbf{B}G$;

1. $\underset{\longrightarrow}{\lim}(\cdots G \times G \stackrel{\to}{\stackrel{\to}{\to}} G \stackrel{\to}{\to} *) \simeq \mathbf{B}G$.

Applying the [[groupoid convolution algebra]] functor to the first presentation yields the groupoid convolution algebra $C(\mathbf{B}G)$ equipped with a trivial multiplication bimodule, hence just the group convolution algebra $C(\mathbf{B}G) \simeq C_{conv}(G)$.

Applying however the [[groupoid convolution algebra]] functor to the second presentation yields the _commutative_ algebra of functions $C(G)$ equipped with the multiplication bimodule which is $C(G \times G)$ regarded as a $(C(G\times G), C(G))$-bimdodule, where the right action is induced by pullback along the group product map $G \times G \to G$.

This bimodule is in the image of the functor $Alg \to Alg_b$ that sends algebra homomorphisms to their induced bimodules, by sending $f \colon A \to B$ to $A$ regarded as an $(A,B)$-bimodule with the canonical left action on itself and the right action induced by $f$. Namely this bimdoule correspondonds to the map

$$
  \Delta \colon C(G) \to C(G \times G) \simeq C(G) \otimes C(G)
$$

given on $\phi \in C(G)$ and $g_1, g_2 \in G$ by

$$
  \Delta \phi \colon (g_1, g_2) \mapsto \phi
  \,.
$$

In summary this means that (for $G$ a finite group)

1. if we regard $\mathbf{B}G$ as presented as a  double groupoid constant on $\mathbf{B}G$, then the corresponding groupoid convolution [[sesquialgebra]] (basis for a [[n-module|3-module]]) is the convolution algebra of $G$;

1. if instead we regard $\mathbf{B}G$ as presented as the double groupoid which is degreewise constant as a groupoid, then the corresponding groupoid convolution sesquialgebra is the standard ("dual") [[Hopf algebra]] structure on the commutative pointwise product algebra of functions on $G$.

=--
## Properties

### Steenrod operations on coTor groups

For $\Gamma$ a suitable commutative Hopf algebroid and $N_1, N_2$
two $\Gamma$-[[comodules]], then the co[[Tor]] groups $CoTor_\Gamma(N_1, N_2)$
form a _[[Steenrod algebra]]_. See there for details and citations.

For [[MU]] this is the content of the [[Landweber-Novikov theorem]].


### Generalized dual Steenrod algebra
 {#GeneralizedDualSteenrodAlgebra}

For $E$ a suitable [[E-infinity ring]] [[spectrum]], its [[homotopy groups]]
$\pi_\bullet(E)$ and [[generalized homology]] $E_\bullet(E)$
form a Hopf algebroid of [[spectra]], the dual $E$-[[Steenrod algebra]].
(These examples have also been called [[brave new Hopf algebroids]].)
See at _[Steenrod algebra -- Hopf algebroid structure](Steenrod+algebra#HopfAlgebraStructure)_.

The general statement is this:

+-- {: .num_lemma #SelfHomologyIsModuleOverCohomologyRing}
###### Lemma

Let $R$ be an [[E-∞ ring]] and let $A$ an [[E-∞ algebra]] over $R$.
The self-[[generalized homology]] $A^R_\bullet(A)$ 
is naturally a [[module]] over the [[cohomology ring]] $A_\bullet$
via applying the [[homotopy groups]] $\infty$-functor $\pi_\bullet$ 
to the canonical inclusion

$$
  A \stackrel{\simeq}{\rightarrow}
  A \underset{R}{\wedge} R
  \stackrel{}{\rightarrow}
  A \underset{R}{\wedge} A
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

Let $R$ be an [[E-∞ ring]] and let $A$ an [[E-∞ algebra]] over $R$.
If the the $A_\bullet$-[[module]] $A^R_\bullet(A)$ of 
lemma \ref{SelfHomologyIsModuleOverCohomologyRing} is a [[flat module]],
then 

1. $(A_\bullet, A_\bullet(A))$ is a [[Hopf algebroid]] over $R_\bulllet$;

1. $A^R_\bullet(X)$ is a left $A^R_\bullet(A)$-module for every $R$-[[∞-module]] $X$.

=--

This is due to ([Baker-Lazarev 01](#BakerLazarev01)), further discussed  in ([Baker-Jeanneret 02](#BakerJeanneret02)) (there expressed in terms of the presentation by [[commutative monoids]] in [[symmetric spectra]]). 
A review is also in ([Ravenel, chapter 2, prop. 2.2.8](#Ravenel)).

## References


The generalization of [[commutative Hopf algebroids]] where the base is kept tcommutative while having the total algebra noncommutative, and the image of source and target maps are required to commute mutually is due Maltsiniotis; he also generalized this to [[quasi-Hopf algebra|quasi-Hopf]] version:

* [[Georges Maltsiniotis]], _Groupo&#239;des quantiques_, Comptes R
Rendus Acad. Sci. Paris __314__, pp. 249-252 (1992) [ps](http://people.math.jussieu.fr/~maltsin/ps/GRN-1.PS)
* G. Maltsiniotis, _Quasi-groupo&#239;des quantiques_ (travail en commun avec A. Brugui&#232;res), C.R. Acad. Sci. Paris __319__, pp. 933-936 (1994) [ps](http://people.math.jussieu.fr/~maltsin/ps/N-QSBIG.PS)

A [[Tannaka duality]]-type theorem relating certain subcategory of
commutative Hopf algebroids to discrete groupoids is in

* [[Laiachi El Kaoutit]], _Representative functions on discrete groupoids and duality with Hopf algebroids_, [arxiv/1311.3109](http://arxiv.org/abs/1311.3109)

For the relation to [[groupoid convolution algebras]] see also at _[groupoid convolution algebra -- References -- Convolution Hopf algebroids](category%20algebra#ReferencesConvolutionHopfAlgebroids)_.

* [[Mark Hovey]], _Morita theory for Hopf algebroids and presheaves of groupoids_ ([arXiv:math/0105137](http://arxiv.org/abs/math/0105137))




category: algebra

[[!redirects Hopf algebroids over a commutative base]]

