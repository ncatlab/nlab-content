#Idea#

The _Dold--Kan correspondence_ asserts that certain [[infinity-category|infinity-categories]] are equivalently encoded as categories of [[chain complex]]es. 

This allows one

* on the one hand to understand the true conceptual home of many constructions with [[chain complex]]es in [[homological algebra]];

* on the other to efficiently compute with certain higher categorical structures.

Compare this to the role played by [[rational homotopy theory]].

The classical Dold--Kan correspondence states the equivalence of

: [[simplicial group|simplicial abelian groups]] $\;\simeq\;$ non-negatively graded [[chain complex]]es of abelian groups.

Since every [[simplicial group]] is a [[Kan complex]], one can equivalently read this more suggestively as 

: $\infty$-groupoids internal to abelian groups $\;\simeq\;$ chain complexes$_+$ internal to abelian groups.

The fact that this involves _[[abelian group|abelian]]_ groups is essential for the correspondence. However, a similar correspondence still holds in a slightly more nonabelian context:

There are various generalizations of this, described below.


#Details#

We now spell out technical details of the Dold-Kan correspondence.

+-- {: .num_theorem }
###### Theorem (Dold-Puppe)

For $A$ an [[abelian category]] 
there is an [[adjoint equivalence]]

$$
  N : [\Delta^{op},A] 
      \stackrel{\leftarrow}{\to} Ch_+(A) : \Xi
$$

between 

* the category $[\Delta^{op},A]$ of [[simplicial object]]s in $A;

* the [[category of chain complexes]] in $A$ that are 0 in negative degree,

where

* $N$ is the normalized [[Moore complex]] functor;

These functors respect the standard weak equivalences with respect to the standard [[model structure on simplicial sets]] [[model structure on chain complexes|and on chain complexes]] in that they induce isomorphisms between [[simplicial homotopy group]]s and [[homology]] groups.

=--




+-- {: .num_theorem }
###### Theorem (Kan)

For the case that $A$ is the category of abelian groups, the functor $\Xi$ is is the [[nerve]] functor on chain complexes that is induced from the [[simplicial object|cosimplicial chain complex]]

$$
  Ch_* := N F_\mathbb{Z}(-): \Delta \to Ch_+(Ab)
$$

that sends the standard $n$-[[simplex]] to the normalized [[Moore complex]] of the free simplicial abelian group $F_{\mathbb{Z}}(\Delta^n)$ on the [[simplicial set]] $\Delta^n$, i.e.

$$
    \Xi(C)_n= Hom_{Ch_*(Ab)}(C_*(\Delta^n), C)
    \,.
$$

=--




# Generalizations #

There are various generalizations of the standard
Dold-Kan correspondence.

## Nonabelian versions ##

In a series of articles by Brown and Higgins, based on old work by Whitehead, the above was generalized to

: strict $\infty$-groupoids $\;\simeq\;$ crossed complexes.

Here on the left we have [[strict omega-groupoid]]s and on the right [[crossed complex]]es, a non-abelian generalization of chain complexes of groups.

: crossed complexes $\supset$ chain complexes$_+$ internal of abelian groups

There is a discussion of some of these and extensions to them to the non-Abelian case, in the entry on [[Moore complex]].


Perhaps the 'ultimate' form of a 'classical' Dold--Kan result is by Pilar Carrasco, who identified the extra structure on chain complexes of groups in order that they be [[Moore complex|Moore complexes]] of simplicial groups.  Dominique Bourn has a general form of this result for his [[semi-abelian category|semi-abelian categories]]. His results provide a neat categorical gloss on the theorem.

Dominique Bourn's formulation is very pretty. The Moore complex functor is [[monad|monadic]] when the basic category is semi-Abelian (Th. 1.4. p.113 in _Bourn2007_ below). Of course for simplicial _groups_, the  monad on chain complexes of groups gives the [[hypercrossed complex]]es of Carrasco and Cegarra, but here they fall out from the theory.  On the down side there is apparently no 
full analysis as yet of the actual form of this monad.


## Versions for monoids in abelian categories ##

In **characteristic zero** there is also a Dold--Kan correspondence between simplicial algebras and [[dg-algebra]]s in nonnegative degrees, as well as between cosimplicial algebras and dg-algebras in nonpositive degrees, which is rather a [[Quillen equivalence]] (thus the two adjoint functors constructed in that case are inverses up to a [[quasi-isomorphism]] of dg-algebras):

* J.L. Castiglioni, G. Corti&#241;as, 
Cosimplicial versus DG-rings: a version of the Dold-Kan correspondence, J. Pure Appl. Algebra  191  (2004),  no. 1-2, 119--142, [arXiv:math.KT/0306289](http://arxiv.org/abs/math/0306289).

* Stefan Schwede, Brooke Shipley, Equivalences of monoidal model categories, Algebr. Geom. Topol. 3 (2003), 287--334 ([arXiv](http://arxiv.org/abs/math.AT/0209342))


## Version for Lie algebras ## 

In rational homotopy theory, Quillen proved and used an analogous statement for Lie algebras: Quillen equivalence between the reduced rational dg Lie algebras and reduced rational simplicial Lie algebras:

* D. G. Quillen, Rational homotopy theory, Ann. Math. 90 (1969), 204--265.



## Parameterized version ##

The statement of the Dold--Kan correspondence generalizes to
[[sheaf|sheaves]] with values in the respective categories and this way from [[Infinity-Grpd]] to more general [[(infinity,1)-topos|(infinity,1)-topoi]]:

For $X$ be a [[site]], let $Sh(X, sAb)$ be the category of 
_simplicial abelian sheaves_ -- i.e. [[simplicial presheaf|simplicial sheaves]] which take values
in simplicial abelian groups -- and let $Sh(X, Ch_+(Ab))$
be the category of [[sheaf|sheaves]] on $S$ with values in
non-negatively graded [[chain complex]]es of abelian groups.
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
[[quasi-isomorphism]]s. The normalized chain complex functor
preserves these weak equivalences.
This sheaf version of the Dold--Kan correspondence 
allows to understand [[abelian sheaf cohomology]]
as a special case of [[nonabelian cohomology]].

See page 9,10 of 

* K. Brown, [[BrownAHT|Abstract Homotopy Theory and Generalized Sheaf Cohomology]]

## $(\infinity,1)$-verson ##

There is a version of the Dold-Kan correspondence in the context of [[(infinity,1)-category|(infinity,1)-categories]]:

let $C$ be a [[stable (infinity,1)-category]]. Then the $(\infty,1)$-categories of [[complex]]es in $C$ is equivalent to the $(\infty,1)$-category of [[simplicial object]]s in $C$

$$
  Fun(N(\mathbb{Z}_{\geq 0}), C)
  \simeq
  Fun(N(\Delta)^{op}, C)  
  \,.
$$

This is [theorem 12.8, p. 50](http://math.mit.edu/~lurie/topoibook/DAGI.pdf) of 

* [[Jacob Lurie]], [[Stable Infinity-Categories]] 


## Related [[nerve]] constructions ## 

This gives a pattern for constructing simplicial structures, often called the _simplicial [[nerve]]_,  from algebraic structures. 

For example the nerve of a groupoid $G$ may be defined as the simplicial set which is $Ob(G)$ in dimension 0 and is given in dimension $n\gt 0$ by 

$$Nerve(G)_n= Gpd(\pi_1(\Delta^n,\Delta^n_0) , G).$$

where $\Delta^n_0$ denotes the set of vertices of $\Delta^n$. 

A [[filtered space]] $X_*$ has a fundamental crossed complex $\Pi X_*$, and a geometric simplex $\Delta^n$ has a filtration $\Delta^n_*$ by skeleta. The nerve of a [[crossed complex]] $C$ is then the simplicial set given in dimension $n$ by 

$$Nerve(C)_n= Crs(\Pi(\Delta^n_*, C).$$

This includes the case when $C$ is a [[crossed module]] (of groupoids) regarded as a crossed complex of length 2. The geometric realisation of this simplicial set gives the [[classifying space]] $BC$ of the crossed complex $C$. This space is filtered by the length of truncations of $C$ to give a filtered space $(BC)_*$ and it is a theorem that $\Pi(BC)_* \cong C$. 


An obvious analogue gives cubical or globular nerves. 



#References#

Historical references for the Dold-Kan correspondence are

* A. Dold, _Homology of symmetric products and other functors of complexes_ 
([jstor](http://www.jstor.org/stable/1970043))

which considers the correspondence for categories of [[module]]s, and

* A. Dold, D. Puppe, _Homologie nicht-additiver Funktoren. Anwendugen_ ([numdam](http://www.numdam.org/item?id=aif_1961__11__201_0))

that generalizes the result to arbitrary [[abelian category|abelian categories]].


A standard modern textbook reference for the ordinary Dold-Kan correspondence is [chapter III.2](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-3.dvi) of 

* Goerss, Jardine, _Simplicial Homotopy Theory_ ([web](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html))

The relation between [[strict omega-groupoid]]s and [[crossed complex]]es is in

* R. Brown, P. Higgins, _The equivalence of $\infty$-groupoids and crossed complexes_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 22 no. 4 (1981), p. 371-386  ([pdf](http://archive.numdam.org/article/CTGDC_1981__22_4_371_0.pdf))

The discussion of Dold--Kan in the generalized context of [[semi-abelian category|semi-abelian categories]] is in

* **Bourn2007** D. Bourn, _Moore normalisation and Dold--Kan theorem for semi-Abelian categories_, in 
Categories in algebra, geometry and mathematical physics , volume 431 of Contemp. Math., 
105--124, Amer. Math. Soc., Providence, RI. (2007)


[[!redirects Dold--Kan correspondence]]
[[!redirects Dold–Kan correspondence]]
[[!redirects Dold-Kan theorem]]
[[!redirects Dold--Kan theorem]]
[[!redirects Dold–Kan theorem]]