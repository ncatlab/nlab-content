
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
* automatic toc
{:toc}

## Idea

The _Dold--Kan correspondence_ asserts there is an [[equivalence of categories]] between [[abelian group|abelian]] [[simplicial group]]s and [[connective]] [[chain complex]]es of [[abelian groups]].

Since every [[simplicial group]] is in particular a [[Kan complex]] with [[group object|group structure]], hence an [[∞-groupoid]] with group structurem, hence an [[∞-group]], the Dold-Kan correspondence says that connective chain complexes are a model for abelian [[∞-group]]s. (This is part of the [[cosmic cube]] of [[higher category theory]]). The relevance of this is that chain complexes are typically easier to handle: all the tools of [[homological algebra]] apply. In fact, the [[functor]] that identifies simplicial abelian groups with their corresponding chain complexes -- the [[Moore complex|normalized chains functor]] -- does precisely this: it _normalizes_ an abelian group by discarding irrelevant information and constructing a smaller and less redundant model for it.

There are various variants and generalizations of the Dold-Kan correspondence. These are discussed further [below](#Variants).



## Statement (abelian case)

Let $A$ be an [[abelian category]].

We say a [[chain complex]] in $A$ is _connective_ if it is concentrated in non-negative degree. The [[full subcategory]]

$$
  Ch^+_\bullet(A) \hookrightarrow Ch_\bullet(A)
$$

of connective chain complexes is naturally identified with the category of $\mathbb{N}$-graded chain complexes.

### Equivalence of categories {#EquivalenceOfCategories}

+-- {: .un_theorem }
###### Theorem (Dold--Puppe)

For $A$ an [[abelian category]] 
there is an [[equivalence of categories]]

$$
  N : A^{\Delta^{op}}
      \stackrel{\leftarrow}{\to} Ch_\bullet^+(A) : \Gamma
$$

between 

* the [[category of simplicial objects]] in $A$;

* the [[category of chain complexes|category of connective chain complexes]] in $A$;

where

* $N$ is the normalized chains/normalized [[Moore complex]] functor;


This is an [[adjoint equivalence]] in both ways: $(\Gamma \dashv N)$ and $(N \dashv \Gamma)$.

=--

+-- {: .un_theorem }
###### Theorem (Kan)

For the case that $A$ is the category [[Ab]] of [[abelian group]]s, the functors $N$ and $\Gamma$ are [[nerve and realization]] with respect to the cosimplicial chain complex

$$
  \mathbb{Z}[-]: \Delta \to Ch_+(Ab)
$$

that sends the standard $n$-[[simplex]] to the normalized [[Moore complex]] of the free simplicial abelian group $F_{\mathbb{Z}}(\Delta^n)$ on the [[simplicial set]] $\Delta^n$, i.e.

$$
    \Gamma(V : [k]  \mapsto 
    Hom_{Ch_\bullet^+(Ab)}(N(\mathbb{Z}(\Delta[k])), V)
    \,.
$$

=--

More explicitly we have the following

+-- {: .un_prop }
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

This is spelled out around prop. 2.2 in section III.2 of ([GoerssJardine](#Goerssjardine)).




### Quillen equivalence of model categories {#ModelCatVersion}

Both $Ch_\bullet^+(A)$ and $A^{\Delta^{op}}$ are [[categories with weak equivalences]] in an standard way: 

* the weak equivalences of simplicial abelian groups are the [[weak homotopy equivalence]]s of the underlying [[Kan complex]]es, hence morphisms that induces [[isomorphism]]s on all [[simplicial homotopy group]];

* the weak equivalences of chain complexes are the [[quasi-isomorphisms]]: the morphisms that induces isomorphisms on all [[chain homology]] groups.

+-- {: .num_prop }
###### Proposition

These functors $N$ and $\Gamma$ both respect all weak equivalences.

standard weak equivalences with respect to the standard [[model structure on simplicial sets]] [[model structure on chain complexes|and on chain complexes]] in that they induce isomorphisms between [[simplicial homotopy groups]] and [[homology group]]s.

=--


The structures of categories with weak equivalences have standard refinements to [[model category]] structures:

* the _projective_ [[model structure on chain complexes]] $Ch_\bullet$ has as weak equivalences the [[quasi-isomorphism]]s and as fibrations the chain maps that are surjections in each positive degree;

* the _[[model structure on simplicial T-algebras|model structure on simplicial abelian groups]]_ has as weak equivalences and fibrations those of the underlying morphisms in [[sSet]] with respect to the standard [[model structure on simplicial sets]].

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

This is discussed for instance in [section 4.1](http://www.math.uic.edu/~bshipley/monoidalequi.final.pdf#page=17) of [SchwedeShipley](#SchwedeShipley)


+-- {: .num_remark }
###### Remark

The category $Ab^{\Delta^{op}}$ is -- being a [[category of simplicial objects]] of a category with colimits -- naturally an [[sSet]]-[[enriched category]] and with the model structure this makes it a [[simplicial model category]].

Since the DK-correspondence is even an [[equivalence of categories]], this induces accordingly the structure of a simplicial model category also on $Ch_\bullet^+$. Therefore the above Quillen equivalence is even an [[sSet]]-Quillen equivalence of simplicial model categories.

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

* [[Ronnie Brown]], _[[Nonabelian Algebraic Topology]]_

see <a href="http://ncatlab.org/nlab/show/Nonabelian+Algebraic+Topology#DoldKanMap">Dold-Kan map and omega-nerve</a>.

+-- {: .un_defn}
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

+-- {: .un_prop}
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

+-- {: .un_cor}
###### Corollary


The simplicial Dold-Kan map

$$
  Hom(C_\bullet \Delta[n], -) : Ch_\bullet + \to sSet 
$$

factors as the identification of chain complexes with strictly abelian strict $\infty$-groupoids, followed by the functor that forgets the abelian structue and then followed by the [[omega-nerve]] operation that embeds strict $\infty$-groupoids into all $\infty$-groupoids.

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



**Remark**
Perhaps the 'ultimate' form of a 'classical' Dold--Kan result is by Pilar Carrasco, who identified the extra structure on chain complexes of groups in order that they be [[Moore complex|Moore complexes]] of simplicial groups.  Dominique Bourn has a general form of this result for his [[semi-abelian category|semi-abelian categories]]. His results provide a neat categorical gloss on the theorem.

Dominique Bourn's formulation is very pretty. The Moore complex functor is [[monad|monadic]] when the basic category is semi-Abelian (Th. 1.4. p.113 in _Bourn2007_ below). Of course for simplicial _groups_, the  monad on chain complexes of groups gives the [[hypercrossed complex]]es of Carrasco and Cegarra, but here they fall out from the theory.  On the down side there is apparently no 
full analysis as yet of the actual form of this monad.







## Generalizations and variants {#Variants}

There are various variants, generalizations and enhancements of the
Dold--Kan correspondence.


### Monoidal version 

See [[monoidal Dold-Kan correspondence]].

### Dual Dold--Kan correspondence 

There is a version relating [[cochain complexes]] in non-negative degree to cosimplicial abelian groups.  Indeed,
replacing the abelian category $A$ by its [[opposite category]] $A^{op}$ in the Dold--Puppe theorem above, we instantly see:

+-- {: .num_theorem }
###### Theorem (dual Dold--Puppe)

For $A$ an [[abelian category]] 
there is an [[adjoint equivalence]] between 

* the category $[\Delta,A]$ of [[cosimplicial object|cosimplicial objects]] in $A$;

and 

* the [[category of cochain complexes]] in $A$ that are 0 in negative degree.
=--

More concretely, let us take the case where $A$ is the category of abelian groups, and construct an explicit equivalence.

If $G$ is a cosimplicial abelian group, the dual Moore complex $C^\bullet$ is formally defined just as the ordinary [[Moore complex]] with

$$
  C^k := G^k
$$

by taking the the alternating sum of the [[simplicial identities|face maps]] $\partial_i$. 

$$
  d : \sum_{i = 0}^{k} (-1) \partial_i : C^k \to C^{k+1}
  \,.
$$

Notice that since we have now a cosimplicial object this differential indeed increases degree, as befits a [[cochain complex]].

It is in the definition of the _normalized_ dual Moore complex $N^\bullet G$ that the role of face maps $d_i$ and boundary maps $s_i$ is interchanged as compared to the ordinary normalized complex. We have

$$
  N^k G := G^n/\sum{i=0}^n d_i G^n
  \simeq
  \cap_{i=0}^{n-1} ker(s_i)
  \,.
$$

This statement is reviewed and various further references are given in [section 4](http://arxiv.org/PS_cache/math/pdf/0306/0306289v3.pdf#page=5) of 

* J.L. Castiglioni, G. Corti&#241;as, 
Cosimplicial versus DG-rings: a version of the Dold-Kan correspondence, J. Pure Appl. Algebra  191  (2004),  no. 1-2, 119--142, [arXiv:math.KT/0306289](http://arxiv.org/abs/math/0306289).



### Version for Lie algebras 

In rational homotopy theory, Quillen proved and used an analogous statement for Lie algebras: Quillen equivalence between the reduced rational dg Lie algebras and reduced rational simplicial Lie algebras:

* D. G. Quillen, Rational homotopy theory, Ann. Math. 90 (1969), 204--265.



### Parameterized version 

The statement of the Dold--Kan correspondence generalizes to
[[sheaf|sheaves]] with values in the respective categories and this way from [[? Grpd]] to more general $(\infty,1)$-[[(infinity,1)-topos|topoi]]:

For $X$ be a [[site]], let $Sh(X, sAb)$ be the category of 
_simplicial abelian sheaves_ -- i.e. [[simplicial presheaf|simplicial sheaves]] which take values
in simplicial abelian groups -- and let $Sh(X, Ch_+(Ab))$
be the category of [[sheaf|sheaves]] on $S$ with values in
non-negatively graded [[chain complexes]] of abelian groups.
The normalized chain complex extends objectwise to a functor
$$
  Sh(X,sAb) \stackrel{\simeq}{\to} Sh(X, Ch_+(Ab))
$$
which is an [[equivalence]] of categories. Moreover, 
both these categories are naturally 
[[category with weak equivalences|categories with weak equivalences]]:
the weak equivalences in $Sh(X, sAb)$ are the stalkwise
[[model structure on simplicial sets|weak equivalences of simplicial sets]]
and the weak equivalences in $Sh(X, Ch_+(Ab))$ are the
[[quasi-isomorphisms]]. The normalized chain complex functor
preserves these weak equivalences.
This sheaf version of the Dold--Kan correspondence 
allows to understand [[abelian sheaf cohomology]]
as a special case of [[nonabelian cohomology]].

See page 9,10 of 

* K. Brown, [[BrownAHT|Abstract Homotopy Theory and Generalized Sheaf Cohomology]]

### $(\infinity,1)$-Version 

There is a version of the Dold--Kan correspondence in the context of $(\infty,1)$-[[(infinity,1)-category|categories]]:

let $C$ be a [[stable (∞,1)-category]]. Then the $(\infty,1)$-categories of [[complexes]] in $C$ is equivalent to the $(\infty,1)$-category of [[simplicial objects]] in $C$

$$
  Fun(N(\mathbb{Z}_{\geq 0}), C)
  \simeq
  Fun(N(\Delta)^{op}, C)  
  \,.
$$

This is [theorem 12.8, p. 50](http://www.math.harvard.edu/~lurie/topoibook/DAGI.pdf) of 

* [[Jacob Lurie]], [[Stable ∞-Categories]] 

### Dendroidal version 

There is a version of the Dold--Kan correspondence with [[simplicial sets]] generalized to [[dendroidal sets]]. This is described in

* [[Javier Gutierrez|Javier Gutiérrez]], [[Andor Lukacs]], [[Ittay Weiss]], _Dold-Kan correspondence for dendroidal abelian groups_ ([arXiv](http://arxiv.org/abs/0909.3995))

### Related nerve constructions 

This gives a pattern for constructing simplicial structures, often called the _simplicial [[nerve]]_,  from algebraic structures. 

For example the nerve of a groupoid $G$ may be defined as the simplicial set which is $Ob(G)$ in dimension 0 and is given in dimension $n\gt 0$ by 

$$Nerve(G)_n= Gpd(\pi_1(\Delta^n,\Delta^n_0) , G).$$

where $\Delta^n_0$ denotes the set of vertices of $\Delta^n$. 

A [[filtered space]] $X_*$ has a fundamental crossed complex $\Pi X_*$, and a geometric simplex $\Delta^n$ has a filtration $\Delta^n_*$ by skeleta. The nerve of a [[crossed complex]] $C$ is then the simplicial set given in dimension $n$ by 

$$Nerve(C)_n= Crs(\Pi(\Delta^n_*, C).$$

This includes the case when $C$ is a [[crossed module]] (of groupoids) regarded as a crossed complex of length 2. The geometric realisation of this simplicial set gives the [[classifying space]] $BC$ of the crossed complex $C$. This space is filtered by the length of truncations of $C$ to give a filtered space $(BC)_*$ and it is a theorem that $\Pi(BC)_* \cong C$. 


An obvious analogue gives cubical or globular nerves. 



## References

Historical references for the Dold--Kan correspondence are

* A. Dold, _Homology of symmetric products and other functors of complexes_ 
([jstor](http://www.jstor.org/stable/1970043))

which considers the correspondence for categories of [[modules]], and

* A. Dold, D. Puppe, _Homologie nicht-additiver Funktoren. Anwendugen_ ([numdam](http://www.numdam.org/item?id=aif_1961__11__201_0))

that generalizes the result to arbitrary [[abelian category|abelian categories]].

The expression of the correspondence in terms of [[nerve and realization]] is due to

* [[Daniel Kan]], _Functors involving c.s.s complexes_, Transactions of the American Mathematical Society, Vol. 87, No. 2 (Mar., 1958), pp. 330--346 ([jstor](http://www.jstor.org/stable/1993103)).

This remarkable article, which appeared shortly after the work by Dold and Puppe but was apparently not influenced by that, introduces not just the abstract [[nerve and realization]] form of the Dold-Kan correspondence, but introduces the general notion of nerve and realization and in fact the general notion of what is now called [[Kan extension]].

A standard modern textbook reference for the ordinary Dold--Kan correspondence is [chapter III.2](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-3.dvi) of 

* Goerss, Jardine, _Simplicial Homotopy Theory_ ([web](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html))

Remarks about the interpretation in terms of model categories are in

* [[Stefan Schwede]], [[Brooke Shipley]], _Equivalences of monoidal model categories_ , Algebr. Geom. Topol. 3 (2003), 287--334 ([arXiv](http://arxiv.org/abs/math.AT/0209342))
{#SchwedeShipley}

The relation between [[strict ∞-groupoids]] and [[crossed complexes]] is in

* [[Ronnie Brown]], Peter Higgins, _The equivalence of $\infty$-groupoids and crossed complexes_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 22 no. 4 (1981), p. 371--386  ([pdf](http://archive.numdam.org/article/CTGDC_1981__22_4_371_0.pdf))

The discussion of Dold--Kan in the general context of [[semi-abelian category|semi-abelian categories]] is in

* [[Dominique Bourn]], _Moore normalisation and Dold--Kan theorem for semi-Abelian categories_, in 
Categories in algebra, geometry and mathematical physics , volume 431 of Contemp. Math., 
105--124, Amer. Math. Soc., Providence, RI. (2007)



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
