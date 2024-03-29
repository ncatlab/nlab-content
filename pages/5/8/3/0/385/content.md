
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea 

The _Crans-Gray tensor product_ is a [[tensor product]] on the category of [[strict omega-category|strict omega-categories]] which is analogous to (the lax version of) the [[Gray tensor product]] for 2-categories.

This tensor product makes the category $Str\omega Cat$ of [[strict omega-category|strict omega-categories]] into a (non-symmetric) [[closed monoidal category|biclosed monoidal structure]]; thus in particular it has two internal-homs $Hom_r$ and $Hom_l$.  Both contain strict $\omega$-functors as their objects, and their $k$-cells for $k\gt 0$ are [[k-transfors]] which are lax or oplax in all dimensions (one internal-hom contains lax transfors and the other the oplax ones).


## Construction from cubical sets 

One abstract way to construct the Crans-Gray tensor product is as follows.

There is an obvious [[monoidal category|monoidal structure]] on the [[cube category]] obtained from the obvious product of cellular [[geometric shapes for higher structures|cubes]] which is analogous to the cartesian product of the topological cubes $[0,1]^n$.  By [[Day convolution]] this naturally induces a [[monoidal category|monoidal structure]] on [[cubical set|cubical sets]].

Now strict $\omega$-categories, although usually defined as [[globular set|globular sets]] with extra structure, can also be regarded as [[cubical set|cubical sets]] with extra structure.  More precisely, there is a forgetful functor from $Str\omega Cat$ to $CubSet$ which is [[monadic functor|monadic]], and the monad is a [[monoidal monad]].  It follows by further general results of Day that the tensor product on $CubSet$ lifts to $Str\omega Cat$.

It is also possible to give a direct construction of this tensor product; see Crans' thesis below.


## Relation to the Gray tensor product 

Strict $n$-categories for $n\lt\omega$ can of course be regarded as strict $\omega$-categories with all $k$-cells identities for $k\gt n$.   In general, the Crans-Gray tensor product of an $n$-category with an $m$-category will be an $(n+m)$-category, since the tensor product of the $n$-cube and the $m$-cube is the $(n+m)$-cube.  (Compare, for example, the fact that the [[Gray tensor product]] of two 1-categories is no longer, in general, a 1-category.)

However, we can obtain a tensor product on strict $n$-categories for any $n$ by applying the [[reflector]] (or "cotruncation") functor for the inclusion of strict $n$-categories into strict $\omega$-categories.  When $n=1$, this produces the cartesian product of categories, while when $n=2$ it reproduces the lax version of the [[Gray tensor product]].

Sjoerd Crans has also defined a tensor product *of* [[Gray-categories]], but the relationship between it and the tensor product of strict $\omega$-categories is not entirely clear, since neither $Str\omega Cat$ nor $GrayCat$ contains the other (their "intersection" is $Str3Cat$).


## Properties 

The Crans-Gray tensor product makes $Str\omega Cat$ into a bi[[closed monoidal category]].  So in particular for $X, Y \in Str\omega Cat$ two strict $\omega$-categories, there is an $\omega$-[[functor category]] between them defined by

$$
   [X,Y] = Str\omega Cat( X \otimes G^\bullet, Y)
  \,,
$$

where $\otimes$ is the CG-tensor product and $G^\bullet : G \to \omega Cat$ is the  [[globular set|globular]] object of standard [[globe]]s.  The objects in $[X,Y]$ are the (strict) $\omega$-functors, while the [[k-morphism]]s are a [[lax natural transformation|lax]] sort of $k$-[[transfor]]s between these.  A dual $\omega$-functor category can be defined by $\langle X,Y\rangle = Str\omega Cat(G^{\bullet}\otimes X, Y)$; this has the same objects but its k-morphisms are oplax $k$-transfors.

+--{: .query}
Or maybe lax and oplax should be switched here?  Can someone verify?
=--

## Further Remarks 

* The Crans-Gray tensor product extends the tensor product  on strict $\omega$-groupoids given by R. Brown and P.J. Higgins (see below); they construct a symmetric monoidal closed structure on these $\omega$-groupoids. It is used there to construct a monoidal closed structure on the category of [[crossed complex]]es. 

* The article [Al-Agl/Brown/Steiner](#Al-Agl/Brown/Steiner) sets up an equivalence between strict globular $\omega$-categories and certain cubical $\omega$-categories with [[connection]]s, to which the monoidal closed structure in the previous paper is easily extended. 

* The article [Steiner](#Steiner) gives a new construction of this tensor product in terms of augmented directed chain complexes, where he shows that it can be defined explicitly and computed efficiently on all strict &#969;-categories admitting a certain kind of loop-freeness assumption on their bases.  In particular, it generalizes the approaches in all earlier papers.   

* There is the [[Verity-Gray tensor product]] on [[stratified simplicial set]]s (as described there). Via the [[oriental|omega-nerve]] [[strict omega-category|strict omega-categories]] form the [[complicial set]]s within all [[stratified simplicial set]]s. According to observation 60 of [Verity06](http://arxiv.org/abs/math/0604414) section 11.4 of [Verity04](http://arxiv.org/abs/math/0410412) proves that the Crans-Gray tensor product is the reflection of the Verity-Gray tensor product under this inclusion.
 


## References

A detailed discussion is in

* [[Sjoerd Crans]], _Pasting schemes for the monoidal biclosed structure on $\omega$-Cat_ ([ftp, gzipped PostScript](ftp://ftp.math.mcgill.ca/pub/crans/thten.ps.gz))

* {#BrownHiggins} [[Ronnie Brown]] and Phil Higgins, _Tensor products and homotopies for $\omega$-groupoids and crossed complexes_ ,  J. Pure Appl. Alg. 47 (1987) 1--33. [PDF](http://www.sciencedirect.com/science/article/pii/0022404987900995)

* F.A. Al-Agl, R. Brown and R. Steiner,  Multiple categories: the equivalence between a globular and cubical approach, Advances in Mathematics, 170 (2002) 71--118. [ArXiv](http://arxiv.org/abs/math/0007009){#Al-Agl/Brown/Steiner}

* R. Brown, P.J.Higgins, R. Sivera, _Nonabelian algebraic topology: filtered spaces, crossed complexes, cubical homotopy groupoids_, EMS Tracts in Mathematics vol 15, 650 pages (autumn 2010 to appear). ([Nonabelian algebraic topology](http://www.groupoids.org.uk/nonab-a-t.html))

Some helpful remarks and diagrams are in 

* [[Sjoerd Crans]], _A tensor product for $Gray$-categories_ ([tac](http://www.tac.mta.ca/tac/volumes/1999/n2/5-02abs.html))

which is however mainly concerned with a slightly different topic. 

A collection of Crans's papers, including those on teisi, can be found here: 

* [Papers of Sjoerd Crans](http://home.tiscali.nl/secrans/papers/) (the website seems down at the moment, but there is [an archived version](https://web.archive.org/web/20130514042310/http://home.tiscali.nl/secrans/papers/))

The modern version, incorporating many new primitives is given in 

* [[Richard Steiner]], _Omega-categories and chain complexes_, Homology, Homotopy and Applications 6(1) (2004), 175-200 ([journal](http://www.intlpress.com/hha/v6/n1/a12/), [pdf](http://www.intlpress.com/hha/v6/n1/a12/pdf))
 {#Steiner}

A general theory of lax tensor products is in 

* [[Michael Batanin]], [[Denis-Charles Cisinski]], [[Mark Weber]], _Multitensor lifting and strictly unital higher category theory_ ([arXiv:1209.2776](http://arxiv.org/abs/1209.2776))

