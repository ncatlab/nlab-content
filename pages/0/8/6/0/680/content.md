
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _Dold--Kan correspondence_ asserts there is an [[equivalence of categories]] between [[abelian group|abelian]] [[simplicial groups]] and [[connective chain complex|connective]] [[chain complexes]] of [[abelian groups]].

Since every [[simplicial group]] is in particular a [[Kan complex]] with [[group object|group structure]], hence an [[∞-groupoid]] with group structure, hence an [[∞-group]], the Dold-Kan correspondence says that connective chain complexes are a model for certain [[abelian ∞-groups]], thus the correspondence interpolates between [[homological algebra]] and general [[simplicial homotopy theory]]. (This is part of the [[cosmic cube]] of [[higher category theory]]). The relevance of this is that chain complexes are typically easier to handle: all the tools of [[homological algebra]] apply. In fact, the [[functor]] that identifies simplicial abelian groups with their corresponding chain complexes -- the [[Moore complex|normalized chains functor]] -- does precisely this: it _normalizes_ an abelian group by discarding irrelevant information and constructing a smaller and less redundant model for it.

There are various variants and generalizations of the Dold-Kan correspondence. These are discussed further [below](#Variants).



## Statement (abelian case)

Let $A$ be an [[abelian category]].

We say a [[chain complex]] in $A$ is _connective_ if it is concentrated in non-negative degree. The [[full subcategory]]

$$
  Ch^+_\bullet(A) \hookrightarrow Ch_\bullet(A)
$$

of connective chain complexes is naturally identified with the category of $\mathbb{N}$-graded chain complexes.

### Equivalence of categories {#EquivalenceOfCategories}

+-- {: .num_theorem }
###### Theorem (Dold--Puppe)

For $A$ an [[abelian category]] 
there is an [[equivalence of categories]]

$$
  N \;\colon\; A^{\Delta^{op}}
      \stackrel{\leftarrow}{\to} Ch_\bullet^+(A) \;\colon\; \Gamma
$$

between 

* the [[category of simplicial objects]] in $A$;

* the [[category of chain complexes|category of connective chain complexes]] in $A$;

where

* $N$ is the [[normalized chains complex]]/normalized [[Moore complex]] functor.


=--

([Dold 58](#Dold58), [Kan 58](#Kan58), [Dold-Puppe 61](#DoldPuppe61)).

+-- {: .num_theorem }
###### Theorem (Kan)

For the case that $A$ is the category [[Ab]] of [[abelian group]]s, the functors $N$ and $\Gamma$ are [[nerve and realization]] with respect to the cosimplicial chain complex

$$
  \mathbb{Z}[-]: \Delta \to Ch_+(Ab)
$$

that sends the standard $n$-[[simplex]] to the normalized [[Moore complex]] of the free simplicial abelian group $F_{\mathbb{Z}}(\Delta^n)$ on the [[simplicial set]] $\Delta^n$, i.e.

$$
    \Gamma(V) : [k]  \mapsto 
    Hom_{Ch_\bullet^+(Ab)}(N(\mathbb{Z}(\Delta[k])), V)
    \,.
$$

=--

This is due to ([Kan 58](#Kan58)).

More explicitly we have the following

+-- {: .num_prop #ExplicitUnitAndCounit}
###### Proposition

* For $V \in Ch_\bullet^+$ the simplicial abelian group $\Gamma(V)$ is in degree $n$ given by

  $$
    \Gamma(V)_n = \bigoplus_{[n] \underset{surj}{\to} [k]} V_k
  $$

  and for $\theta : [m] \to [n]$ a morphism in $\Delta$ the corresponding map
  $\Gamma(V)_n \to \Gamma(V)_m$ 

  $$
    \theta^* : \bigoplus_{[n] \underset{surj}{\to} [k]} V_k
     \to 
     \bigoplus_{[m] \underset{surj}{\to} [r]} V_r
  $$
  
  is given on the summand indexed by some $\sigma : [n] \to [k]$ by the composite
  
  $$
    V_k  \stackrel{d^*}{\to} V_s \hookrightarrow \bigoplus_{[m] \underset{surj}{\to} [r]} V_r
  $$

  where

  $$
    [m] \stackrel{t}{\to} [s] \stackrel{d}{\to} [k]
  $$

  is the [[weak factorization system|epi-mono factorization]] of the composite $[m] \stackrel{\theta}{\to} [n] \stackrel{\sigma}{\to} [k]$.

* The [[natural isomorphism]] $\Gamma N \to Id$ is given on $A \in sAb^{\Delta^{op}}$ by the map

  $$
    \bigoplus_{[n] \underset{surj}{\to} [k]}
     (N A)_k
    \to
    A_n
  $$

  which on the [[direct sum]]mand indexed by $\sigma : [n] \to [k]$ is the composite 

  $$
    N A_k \hookrightarrow A_k \stackrel{\sigma^*}{\to} A_n
    \,.
  $$

* The [[natural isomorphism]] $Id \to N \Gamma$ is on  a chain complex $V$ given by the composite of the projection

  $$
    V \to C(\Gamma(V)) \to C(\Gamma(C))/D(\Gamma(V))
  $$

  with the inverse

  $$
    C(\Gamma(V))/D(\Gamma(V)) \to N \Gamma(V)  
  $$

  of 

  $$
    N \Gamma(V) \hookrightarrow C(\Gamma(V)) \to C(\Gamma(V))/D(\Gamma(V))
  $$

  (which is indeed an [[isomorphism]], as discussed at [[Moore complex]]).

=--

This is spelled out in  ([Goerss-Jardine, prop. 2.2 in section III.2](#Goerssjardine)).



+-- {: .num_prop }
###### Proposition

With the explicit choice for $\Gamma N \stackrel{\simeq}{\to} Id$ as [above](#ExplicitUnitAndCounit) we have that $\Gamma$ and $N$ form an [[adjoint equivalence]] $(\Gamma \dashv N)$ 

=--

This is for instance ([Weibel, exercise 8.4.2](#Weilbel)).


+-- {: .num_remark }
###### Remark

It follows that with the inverse structure maps, we also have an [[adjunction]] the other way round: $(N \dashv \Gamma)$.

=--


### Quillen equivalence of model categories {#ModelCatVersion}

Both $Ch_\bullet^+(A)$ and $A^{\Delta^{op}}$ are [[categories with weak equivalences]] in an standard way: 

* the weak equivalences of simplicial abelian groups are the [[weak homotopy equivalence]]s of the underlying [[Kan complex]]es, hence morphisms that induces [[isomorphism]]s on all [[simplicial homotopy group]];

* the weak equivalences of chain complexes are the [[quasi-isomorphisms]]: the morphisms that induces isomorphisms on all [[chain homology]] groups.

+-- {: .num_prop }
###### Proposition

These functors $N$ and $\Gamma$ both respect all weak equivalences 
with respect to the standard [[model structure on simplicial sets]] [[model structure on chain complexes|and on chain complexes]] in that they induce isomorphisms between [[simplicial homotopy groups]] and [[homology group]]s.

=--


The structures of categories with weak equivalences have standard refinements to [[model category]] structures:

* the _projective_ [[model structure on chain complexes]] $Ch_\bullet$ has as weak equivalences the [[quasi-isomorphism]]s and as fibrations the chain maps that are surjections in each positive degree;

* the _[[model structure on simplicial T-algebras|model structure on simplicial abelian groups]]_ has as weak equivalences and fibrations those whose underlying morphisms in [[sSet]] are fibrations ([[Kan fibrations]]) with respect to the standard [[model structure on simplicial sets]].

+-- {: .num_prop }
###### Proposition

Both 

$$
  (N \dashv \Gamma) : Ch_\bullet^+ \stackrel{\overset{N}{\leftarrow}}{\underset{\Gamma}{\to}}
  sAb
$$

as well as

$$
  (\Gamma \dashv N) : sAb \stackrel{\overset{\Gamma}{\leftarrow}}{\underset{N}{\to}}
  Ch_\bullet^+
$$

are [[Quillen equivalence]]s with respect to these model structures.

=--

This is discussed for instance in ([Schwede-Shipley, section 4.1](#SchwedeShipley), [p.17](http://www.math.uic.edu/~bshipley/monoidalequi.final.pdf#page=17)).


+-- {: .num_remark }
###### Remark

The category [[sAb]] $ = Ab^{\Delta^{op}}$ is -- being a [[category of simplicial objects]] of a category with [[colimits]] -- is naturally an [[sSet]]-[[enriched category]] and with the model structure this makes it a [[simplicial model category]].

Since the DK-correspondence is even an [[equivalence of categories]], this induces accordingly the structure of a simplicial model category also on $Ch_\bullet^+$. Therefore the above Quillen equivalence is even a [[simplicial Quillen adjunction]].

=--

+-- {: .num_remark }
###### Remark

The [[free functor|free]]/[[stuff, structure, property|forgetful]] [[adjunction]] $(F \dashv U) : Ab \stackrel{\leftarrow}{\to} Set$ prolongs to [[simplicial object]]s

$$
  (F\dashv U) : sAb \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}}
  sSet
$$

as an [[sSet]]-[[enriched functor|enriched]] adjunction. Moreover, by the above the right adjoint $U$ is a right Quillen functor to the standard [[model structure on simplicial sets]].

This means we have a [[simplicial Quillen adjunction]]

$$
  ( \Gamma F \dashv U N) : Ch_\bullet^+ \stackrel{\overset{}{\leftarrow}}{\underset{U N}{\to}}
  \,.
$$

This manifestly [[presentable (infinity,1)-category|presents]] connective chain complexes as models for certain [[∞-groupoid]]s.


=--


## Statement (general nonabelian case) {#StatementGeneral}


### Globular and cubical version {#GlobularAndCubical}

There are versions of the Dold-Kan correspondence for other [[geometric shapes for higher structures]] than the [[simplex]], also for the [[globe]] and the [[cube]].

+-- {: .num_theorem }
###### Theorem (globular Dold-Kan correspondence)

Write [[Ab]] for the category of [[abelian group]]s. (Could be any [[additive category]] with [[kernel]]s for the following to be true). Then the following categories of structures [[internalization|internal to]] $Ab$ are equivalent.

1. The category of [[chain complex]]es (in non-negative degree).

1. The category of [[crossed complex]]es.

1. The category of [[cubical set]]s with [[connection on a cubical set]].

1. The category of cubical [[strict ∞-groupoid]]s.

1. The category of [[globe|globular]] [[strict ∞-groupoid]]s.

=--

A proof with references to the rich literature can be found for instance in 

* [[Ronnie Brown]], [[Philip Higgins]], [[Rafael Sivera]], _[[Nonabelian Algebraic Topology]]_ 

see the section  [Cubical Dold-Kan theorem](http://ncatlab.org/nlab/show/Nonabelian+Algebraic+Topology#CubicalDoldKan).

This version of the Dold-Kan theorem reproduces the simplicial Dold-Kan theorem after application of the [[omega-nerve]], i.e. the simplicial Dold-Kan correspondence factors through the globular one via the $\omega$-nerve. 


### Presentation of strict groupal $\infty$-groupoids

It was mentioned above that the standard simplicial Dold-Kan correspondence $Ch_\bullet(Ab) \stackrel{\leftarrow}{\to} sAb$ may be understood as identifying strictly abelian  [[strict ∞-groupoid]]s among all [[∞-groupoid]]s. This statement is also surveyed and put into a larger context at [[cosmic cube of higher category theory]]. 

We now give a formal version of this statement, following an observation by [[Richard Garner]]. A different but closely analogous sequence of arguments to the same extent is also in the book

* [[Ronnie Brown]], [[Philip Higgins]], [[Rafael Sivera]],  _[[Nonabelian Algebraic Topology]]_, European Math. Soc. Tracts in Mathematics 15, 2011.

see <a href="http://ncatlab.org/nlab/show/Nonabelian+Algebraic+Topology#DoldKanMap">Dold-Kan map and omega-nerve</a>.

+-- {: .num_defn}
###### Definition

Write

$$
  (L \dashv R) : Ch_\bullet(Ab)^+ \stackrel{\leftarrow}{\to}
  Str \infty Cat(Ab) 
  \stackrel{\leftarrow}{\to}
  Str \infty Cat(Set)
$$

for the [[adjunction]] obtained by composing the [globular Dold-Kan correspondence](#GlobularAndCubical) with the forgetful functor which forgets the abelian group structure on a strict $\infty$-category in the image of the globular/cubical Dold-Kan map.

=--

+-- {: .num_prop}
###### Proposition

The functor

$$
  C_\bullet : \Delta \to Ch_\bullet^+
$$

which sends a [[simplex]] to its (normalized) chain complex factors as

$$
  C_\bullet : \Delta \stackrel{\mathcal{O}}{\to} Str \infty Cat
  \stackrel{L}{\to} Ch_\bullet^+
  \,,
$$

where the cosimplicial strict $\infty$-category $\mathcal{O}$ is the [[oriental]] functor.

=--

This is a remark by [[Richard Garner]] posted <a href="http://golem.ph.utexas.edu/category/2010/07/the_doldkan_theorem_two_questi.html#c034102">here</a>.

+-- {: .proof}
###### Proof

Use that $\mathcal{O}(n)$ is the [[free construction|free]] strict $\infty$-category on a [[computad]].

Observe that $L$ sends a strict $\omega$-category $X$ to the chain complex obtained from the abelian reflexive globular set $X \times \mathb{Z}$. In particular the value on the $n$-[[globe]] is the chain complex

$$
  \mathbb{Z} \to \mathbb{Z}\oplus\mathbb{Z} \to 
   \mathbb{Z}\oplus\mathbb{Z} \to \cdots \to
   \mathbb{Z}\oplus\mathbb{Z}
$$

with $(n+1)$ terms and differential given by $x \mapsto (x, -x)$ in each dimension. 

Moreover, the value of $L$ on the boundary of the $n$-globe is the chain complex obtained from this by removing the uppermost copy of $\mathbb{Z}$.

Given a [[computad]] $C$, the associated abelian chain complex $L C$ has for $(L C)_n$ the free abelian group on the set of generating $n$-cells of $C$, and differential given by $\partial x = \sum_j t_j - \sum_i s_i$, where $\{s_i\}$ and $\{t_i\}$ are the sets of source- and or target-cells, respectively. A glance at [[Ross Street]]'s presentation of the [[oriental]]s shows that $L(\mathcal{O}(n)) = C_\bullet(\Delta[n])$.

=--

+-- {: .num_cor}
###### Corollary


The simplicial Dold-Kan map

$$
  Hom(C_\bullet \Delta[n], -) : Ch_\bullet + \to sSet 
$$

factors as the identification of chain complexes with strictly abelian strict $\infty$-groupoids, followed by the functor that forgets the abelian structure and then followed by the [[omega-nerve]] operation that embeds strict $\infty$-groupoids into all $\infty$-groupoids.

=--


+-- {: .proof}
###### Proof

Use the above adjunction and proposition to write for $K_\bullet$ a chain complex

$$
  Hom_{Ch_\bullet}(C_\bullet \Delta[n], K)
  =
  Hom_{Ch_\bullet}(L \mathcal{O}(n), K)
  =
  Hom_{Str \infty Cat}(\mathcal{O}(n), R K)
  =
  N (R K)_n
  \,.
$$

=--



**Remark** The alternative construction in [[Nonabelian Algebraic Topology]] factors also versions of the nonabelian Dold-Kan correspondence through the $\omega$-nerve.

##Non-abelian forms of the Dold-Kan correspondence.

Perhaps the 'ultimate' form of a 'classical' Dold--Kan result is by Pilar Carrasco, who identified the extra structure on chain complexes of groups in order that they be [[Moore complex|Moore complexes]] of simplicial groups.  Dominique Bourn has a general form of this result for his [[semi-abelian category|semi-abelian categories]]. His results provide a neat categorical gloss on the theorem.

Dominique Bourn's formulation is very pretty. The Moore complex functor is [[monad|monadic]] when the basic category is semi-Abelian (Th. 1.4. p.113 in _Bourn2007_ below). Of course for simplicial _groups_, the  monad on chain complexes of groups gives the [[hypercrossed complex]]es of Carrasco and Cegarra, but here they fall out from the theory.  On the down side there is apparently no 
full analysis as yet of the actual form of this monad.


## Stable Dold-Kan correspondence
 {#StableDoldKanCorrespondence}

The Dold-Kan correspondence [[stabilization|stabilizes]]
to identify _unbounded_ [[chain complexes]]
with the category of stably simplicial abelian groups.
The latter are closely related to [[combinatorial spectrum|combinatorial spectra]] of [[Daniel Kan]] and can be defined as stably simplicial objects in
the category of abelian groups.
More precisely, we have the following definitions.

+-- {: .num_defn}
###### Definition
The category of _stable simplices_ has integer numbers as objects.
Given two objects $k$ and $l$, the set of morphisms
from $k$ to $l$ is the set of order-preserving maps $h$
from the set of natural numbers to itself
such that $h(n)=n+l-k$ for all but a finite number of $n$.
Morphisms are composed by composing the corresponding maps.
=--

+-- {: .num_defn}
###### Definition
A _stably simplicial abelian group_ is a presheaf $F$ of abelian groups
on the category of stable simplices
such that for any integer $k$ every element $x$ of $F(k)$
belongs to the kernels of all but a finite number of degeneracy maps.
Morphisms of stably simplicial abelian groups are morphisms
of presheaves.
=--

The following theorem was established in 1963 by [[Daniel Kan]]
in his paper "Semisimplicial spectra" (see Proposition 5.8):

+-- {: .num_theorem}
###### Theorem
The [[category of unbounded chain complexes]] is [[equivalence of categories|equivalent]] to the
category of stably simplicial abelian groups,
with equivalences being given by the same functors

as in the unstable Dold-Kan correspondence, but appropriately
extended to the above categories.
=--

Similarly to the unstable case,
the above categories, when interpreted as ∞-categories,
are also equivalent to the ∞-category of module spectra over
the Eilenberg-MacLane ring spectrum of the integers.
For more see at _[[stable Dold-Kan correspondence]]_.

## Generalizations and variants {#Variants}

There are various variants, generalizations and enhancements of the
Dold--Kan correspondence.


* The [[monoidal Dold-Kan correspondence]] relates [[simplicial algebra]]s with [[dg-algebra]]s.


* In [[rational homotopy theory]], Quillen proved and used an analogous statement for [[Lie algebra]]s: a Quillen equivalence between the reduced rational [[dg-Lie algebra]]s and reduced rational simplicial Lie algebras:

  D. Quillen, _Rational homotopy theory_ , Ann. Math. 90 (1969), 204--265.


* The statement of the Dold--Kan correspondence generalizes to [[sheaf|sheaves]] with values in the respective categories and this way from [[? Grpd]] to more general $(\infty,1)$-[[(infinity,1)-topos|topoi]]:

  For $X$ be a [[site]], let $Sh(X, sAb)$ be the category of  _simplicial abelian sheaves_ -- i.e. [[simplicial presheaf|simplicial sheaves]] which take values in simplicial abelian groups -- and let $Sh(X, Ch_+(Ab))$ be the category of [[sheaf|sheaves]] on $S$ with values in non-negatively graded [[chain complexes]] of abelian groups. The normalized chain complex extends objectwise to a functor 
  $$
   Sh(X,sAb) \stackrel{\simeq}{\to} Sh(X, Ch_+(Ab))
  $$
  which is an [[equivalence]] of categories. Moreover, both these categories are naturally  [[category with weak equivalences|categories with weak equivalences]]: the weak equivalences in $Sh(X, sAb)$ are the stalkwise [[model structure on simplicial sets|weak equivalences of simplicial sets]]
and the weak equivalences in $Sh(X, Ch_+(Ab))$ are the [[quasi-isomorphisms]]. The normalized chain complex functor preserves these weak equivalences.
This sheaf version of the Dold--Kan correspondence  allows to understand [[abelian sheaf cohomology]] as a special case of [[nonabelian cohomology]].

  See page 9,10 of 

  * K. Brown, [[BrownAHT|Abstract Homotopy Theory and Generalized Sheaf Cohomology]]


* There is a version of the Dold--Kan correspondence in the context of $(\infty,1)$-[[(infinity,1)-category|categories]]:

  let $C$ be a [[stable (∞,1)-category]]. Then the $(\infty,1)$-categories of non-negatively graded [[complexes]] in $C$ is equivalent to the $(\infty,1)$-category of [[simplicial objects]] in $C$

  $$
    Fun(N(\mathbb{Z}_{\geq 0}), C)
    \simeq
    Fun(N(\Delta)^{op}, C)  
    \,.
  $$

  This is [[infinity-Dold-Kan correspondence]] is [theorem 12.8, p. 50](http://www.math.harvard.edu/~lurie/topoibook/DAGI.pdf) of 

  * [[Jacob Lurie]], [[Stable ∞-Categories]] 


* There is a version of the Dold--Kan correspondence with [[simplicial sets]] generalized to [[dendroidal sets]]. This is described in

  * [[Javier Gutierrez|Javier Gutiérrez]], [[Andor Lukacs]], [[Ittay Weiss]], _Dold-Kan correspondence for dendroidal abelian groups_ ([arXiv](http://arxiv.org/abs/0909.3995))


## Applications 
  {#Applications}


### Eilenberg-MacLane objects
  {#EilenbergMacLaneObjects}

The Dold-Kan correspondence gives a convenient construction of [[Eilenberg-MacLane object]]s in [[simplicial group]]s.

+-- {: .num_prop #ExplicitUnitAndCounit}
###### Proposition

For $A$ an [[abelian group]] write $A[-n]$ for the [[chain complex]] concentrated on $A$ in degree $n$. 

The simplicial abelian group $\Gamma (A[-n])$ is an [[Eilenberg-MacLane object]] $K(A,n)$.

And conversely, every such Eilenberg-MacLane object in simplicial abelian groups is related by an [[∞-anafunctor]]-equivalence to a $\Gamma(A[-n])$.

=--

### Looping and delooping
 {#LoopingAndDelooping}

The Dold-Kan correspondence provides a convenient way to describe formation of [[loop space object]]s and [[delooping]] for anything in the image of $\Xi : Ch_\bullet \to sSet$:

by the basic fact that the homotopy groups of $\Xi(V_\bullet)$ are the homology groups of $V_\bullet$, looping and delooping simply corresponds to shifting chain complexes up or down in degree.

But the relation is also strongly coherent: it respects the standard delooping functor $\bar W : sGrp \to sSet$ for [[simplicial group]]s (see there and at [[looping and delooping]]) (notice that restricted to simplicial abelian groups this produces simplicial abelian groups $\bar W : sAbGrp \to sAbGrp$):

+-- {: .num_prop }
###### Proposition

There is a [[natural isomorphism]]

$$
  N \bar W G \simeq (N G)[-1]
$$

natural in $G \in sAbGrpd$.

=--

This appears for instance as 
([GoerssJardine, remark III.5.6](#GoerssJardine)) or around ([Jardine, theorem 4.57](#Jardine)).

### Abelian sheaf cohomology in nonabelian cohomology

Composed with the [[forgetful functor]] $sAb \to sSet$ the Dold-Kan correspondence presents certain [[simplicial set]]s by chain complexes. Since this is entirely functorial, it prolongs to a functor from chain complexes of (pre)[[sheaves]] on any [[site]] $S$, to [[simplicial presheaves]]

$$
  \Gamma : [S^{op}, Ch_\bullet^+(ab)] \to [S^{op}, sSet]

  \,.
$$

If $[S^{op}, sSet]$ is equipped with the projective [[model structure on simplicial presheaves]] it models the [[(∞,1)-sheaf (∞,1)-topos]] on $S$. The [[derived hom-space]]s compute general [[nonabelian cohomology]].

If the coefficient objects come from sheaves of chain complexes along $\Gamma$, this cohomology restricts to ordinary [[abelian sheaf cohomology]]. See there for more details.

### Computational aspects

One may view the (monoidal) Dold-Kan correspondence as a relation between a well-behaved theory (simplicial/higher methods) that work in any characteristic but is very abstract and mainly suited to the proof of abstract theorems, and a more computational theory (strict structures in dg-modules) that are particularly well adapted to computations. The relation between these two (symmetric monoidal) theories may only be properly used with characteristic 0 coefficients. This remark is very naive and basic, but certainly at the center of computational implementations of abstract homotopical methods.


## Related concepts

* **Dold-Kan correspondence**

* [[monoidal Dold-Kan correspondence]]

* [[operadic Dold-Kan correspondence]]

* [[infinity-Dold-Kan correspondence]]

* [[stable Dold-Kan correspondence]]

## References


Historical references for the Dold--Kan correspondence are

* {#Dold58} [[Albrecht Dold]], _Homology of symmetric products and other functors of complexes_, Annals of Mathematics Second Series, Vol. 68, No. 1 (Jul., 1958), pp. 54-80  ([jstor](http://www.jstor.org/stable/1970043))

which considers the correspondence for categories of [[modules]], and

* {#DoldPuppe61} [[Albrecht Dold]], [[Dieter Puppe]], _Homologie nicht-additiver Funktoren. Anwendungen_, Annales de l'institut Fourier, 11 (1961), p. 201-312  ([numdam](http://www.numdam.org/item?id=aif_1961__11__201_0))

that generalizes the result to arbitrary [[abelian category|abelian categories]].

The expression of the correspondence in terms of [[nerve and realization]] is due to

* {#Kan58} [[Daniel Kan]], _Functors involving c.s.s complexes_, Transactions of the American Mathematical Society, Vol. 87, No. 2 (Mar., 1958), pp. 330--346 ([jstor](http://www.jstor.org/stable/1993103)).

This remarkable article, which appeared shortly after the work by Dold and Puppe but was apparently not influenced by that, introduces not just the abstract [[nerve and realization]] form of the Dold-Kan correspondence, but introduces the general notion of nerve and realization and in fact the general notion of what is now called [[Kan extension]].

A standard modern textbook reference for the ordinary Dold-Kan correspondence is [chapter III.2](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-3.dvi) of 

* {#GoerssJardine} [[Paul Goerss]], [[Rick Jardine]], _[[Simplicial homotopy theory]]_ ([web](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html))
 

Similar material is in section 4.6 of 

* {#Jardine} [[Rick Jardine]], _Generalized etale cohomology theories_ Modern Birkh&#228;user Classics, (1991)
 

Remarks about the interpretation in terms of model categories are in

* [[Stefan Schwede]], [[Brooke Shipley]], _Equivalences of monoidal model categories_ , Algebr. Geom. Topol. 3 (2003), 287--334 ([arXiv](http://arxiv.org/abs/math.AT/0209342))
{#SchwedeShipley}

Discussion in the generality of [[idempotent complete category|idempotent complete]] [[additive categories]] is in 

* [[Jacob Lurie]], section 1.2.3 of _[[Higher Algebra]]_
 
The relation between [[strict ∞-groupoids]] and [[crossed complexes]] is in

* [[Ronnie Brown|R. Brown]] and P.J. Higgins, _The equivalence of $\infty$-groupoids and crossed complexes_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 22 no. 4 (1981), p. 371--386  ([pdf](http://archive.numdam.org/article/CTGDC_1981__22_4_371_0.pdf))


P. 59 of 

* R. Brown, _Groupoids and crossed objects in algebraic topology_, Homology, Homotopy and Applications, 1 (1999) 1-78.

gives seven equivalent categories with the equivalences all expressing  nonabelian versions of the Dold--Kan correspondence. One of these is given in 

* Ashley, N., _Simplicial T-complexes and crossed complexes: a  nonabelian version of a theorem of Dold and Kan_. University of Wales PhD Thesis, (1978);  Dissertationes Math. (Rozprawy Mat.) 265 (1988) 1--61. 

The relation of these with the abelian version is given in 

* Brown, R. and Higgins, P. J., _Cubical abelian groups with connections are equivalent to   chain complexes_. Homology Homotopy Appl. 5 (1) (2003) 49--52. 

The discussion of Dold--Kan in the general context of [[semi-abelian category|semi-abelian categories]] is in

* [[Dominique Bourn]], _Moore normalisation and Dold--Kan theorem for semi-Abelian categories_, in 
Categories in algebra, geometry and mathematical physics , volume 431 of Contemp. Math., 
105--124, Amer. Math. Soc., Providence, RI. (2007)

The classical Dold-Kan theorem occurs as a special case among others from [[combinatorics]] and [[representation theory]] here:

* [[Stephen Lack]], [[Ross Street]], _Combinatorial Categorical Equivalences_, arxiv:1402.7151 (2014).  ([pdf](http://arxiv.org/pdf/1402.7151v1))

[[!redirects Dold--Kan correspondence]]
[[!redirects Dold?Kan correspondence]]
[[!redirects Dold-Kan theorem]]
[[!redirects Dold--Kan theorem]]
[[!redirects Dold?Kan theorem]]
[[!redirects dual Dold--Kan correspondence]]
[[!redirects dual Dold?Kan correspondence]]
[[!redirects dual Dold-Kan theorem]]
[[!redirects dual Dold--Kan theorem]]
[[!redirects dual Dold?Kan theorem]]