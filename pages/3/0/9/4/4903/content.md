
> This entry is about a certain way of formalizing [[higher geometry]]. For variants and more background, see there.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea and motivation

For $T$ a [[nLab:Lawvere theory]], the _geometry_ modeled on $T$ is encoded in the [[nLab:sheaf topos]] on formal duals of [[nLab:T-algebra]]s. For instance for $T = $ [[nLab:CartSp]] we have that $T$-algebras are [[nLab:smooth algebra]]s and the geometry modeled on them is [[nLab:synthetic differential geometry]].

This statement generalizes to [[nLab:(∞,1)-category theory]]: for $T$ an [[nLab:(∞,1)-algebraic theory]] and $C \subset T Alg^{op}$ a [[nLab:(∞,1)-site]] of formal duals of $\infty$-algebras over $T$, one says that the [[nLab:(∞,1)-topos]] $\mathbf{H} = \infty Sh(C)$ over $C$ encodes **[[nLab:derived geometry]]** modeled on $T$. The objects of $\mathbf{H}$ are also called _[[nLab:derived stack]]s_ on $C$.

The term "derived" here is meant to specifically contrast with [[nLab:∞-stack]]s on just a 1-categorical site. Even if $T$ happens to be just an ordinary Lawvere theory, regarded as a 1-[[nLab:truncated]] $(\infty,1)$-theory, the $\infty$-topos over $T Alg_\infty^{op}$ behaves considerably different from that over just $T Alg^{op}$.

An object $X$ in derived geometry has both, an [[nLab:∞-groupoid]] of internal symmetries as well as an $\infty$-[[nLab:function algebras on ∞-stacks|algebra of functions]]:

1. passing from a  sheaf topos over a site to the $\infty$-stacks over that site makes _[[nLab:colimit]]s_ behave well in [[nLab:cohomology]]. For instance a singular [[nLab:quotient]] becomes an [[nLab:orbifold]]. 

1. passing to derived geometry by making the site a genuine $(\infty,1)$-category makes _[[nLab:limit]]s_ behave well in cohomology. For instance the intersection pairing of non-[[nLab:transversal map|transversal]] [[nLab:smooth manifold]]s comes out correctly when regarding them as [[nLab:derived smooth manifold]]s.

A central class of examples for nontransveral [[nLab:pullback]]s in derived geometry are [[nLab:derived loop space]] objects. For $X \in T Alg^{op}$ an ordinary space, its [[nLab:free loop space object]] computed in the underived $\infty$-topos over $T Alg^{op}$ exists, but simply coincides with $X$, because $X$ is 0-[[nLab:truncated]] in there. But the free loop space object $\mathcal{L}X$ of $X$ computed in the $\infty$-topos over $T Alg_\infty^{op}$ may be very rich: its $\infty$-[[nLab:function algebras on infinity-stacks|function algebra]] is the [[nLab:Hochschild homology]] of $X$. Moreover, the functions on $\mathcal{L}X$ that are invariant under the canonical internal [[nLab:circle]]-[[nLab:action]] are the _closed_ [[nLab:Kähler differential]] forms on $X$.


Examples of derived spaces have appeared long ago as the configuration spaces in [[nLab:gauge theory]]. What is called the [[nLab:BV-BRST complex]] of a gauge theory is the function algebra on the [[nLab:infinitesimal object|infinitesimal]] approximation to a derived orbifold whose internal symmetries are the [[nLab:gauge transformation]]s and whose function complex provides a [[nLab:resolution]] of the locus of solutions to the physical equations of motion.

More recently, much of the motivation for derived geometry came from the observation that the [Goerss-Hopkins-Miller theorem](http://arxiv.org/abs/0910.5130) suggests that there is a [[nLab:A Survey of Elliptic Cohomology - the derived moduli stack of derived elliptic curves|derived moduli space of derived elliptic currves]], that it carries a [[nLab:structured (∞,1)-topos|structure ∞-sheaf]] of [[nLab:E-∞-rings]], and the the [[nLab:global section]]s of that yield the [[nLab:ring spectrum]] of the [[nLab:generalized cohomology theory]] called [[nLab:tmf]].


## An introduction

### $\infty$-Sites from $\infty$-algebraic theories {#Sites}

* _Oct 15, 2010_

  **[[nLab:algebraic theories]]** / **[[nLab:Lawvere theories]]**

  The theories of [[nLab:group]]s, [[nLab:ring]]s, $k$-[[nLab:algebra]]s,
  [[nLab:C-infinity-ring]]s and so forth are examples of 
  [[nLab:algebraic theories]]. [[nLab:Bill Lawvere]] famously 
  noticed that these theories are encoded by 
  categories $T$ with products, all whose objects are cartesian powers
  of a generating object $x$. One speaks of [[nLab:Lawvere theories]].
  An [[nLab:algebra over a Lawvere theory|algebra]] $A$ of a Lawvere theory is identified with a product-preserving co-presheaf

  $$
    A : T \to Set
    \,.
  $$
  
  Here the value $A(x)$ is identified with the underlying set of the algebra and for any morphism $f : x^n \to x$ in $T$ the morphism $A(f) : A(x^n) \simeq A(x)^n \to A(x)$ is an $n$-ary operation in the algebra. Functoriality of $A$ encodes the compatibilities of all these operations, such as associativity. 

  The identification of algebras with co-presheaves gives rise to [[nLab:Isbell duality]], which naturally identifies the opposite $T Alg^{op}$ of the category of all $T$-algebras with a category of test spaces: the [[nLab:sheaf topos]] $Sh(C)$ on a small full subcategory $C \hookrightarrow T Alg^{op}$ is the context in which geometry over $T$ takes place. For $T = $ [[nLab:CartSp]] the theory of [[nLab:smooth algebra]]s, this is [[nLab:synthetic differential geometry]].


* _Oct 22, 2010_

  **[[nLab:(∞,1)-algebraic theory]]**

  There is an $\infty$-categorical generalization of the notion of [[nLab:Lawvere theory]] and [[nLab:algebra over a Lawvere theory]]. The general abstract discussion of this is hidden in section 5.5.8 of _[[nLab:Higher Topos Theory]]_ .

  The idea is evident: we say 

  * an **$(\infty,1)$-algebraic theory** is an [[nLab:(∞,1)-category]] $T$ with [[nLab:(∞,1)-limit|(∞,1)-product]]s.

  * an **$(\infty,1)$-algebra** over $T$ is an [[nLab:(∞,1)-functor]] $A : T \to $ [[nLab:∞Grpd]] that preserves these products;

  * the $(\infty,1)$-category of all $T$-algebras is the full [[nLab:sub-(∞,1)-category]]  $\infty T Alg \hookrightarrow \infty Func(T, \infty Grpd)$ of the [[nLab:(∞,1)-category of (∞,1)-presheaves|(∞,1)-category of (∞,1)-copresheaves]] on those functors that preserve products.

Next, in order to handle $\infty T Alg$ and to compare it to other known structures it is useful to [[nLab:presentable (∞,1)-category|present]] it in terms of a [[nLab:model category]]. This is the topic of the next part.
  

### Models for $\infty$-algebras over ordinary algebraic theories {#Models}

* _Oct 29, 2010_

  **[[nLab:homotopy T-algebra]]s**

  We know from the [[nLab:model structure on simplicial presheaves]] that every [[nLab:(∞,1)-functor]] $A : T \to \infty Grpd$ is modeled by a strict functor $T \to $ [[nLab:sSet]]. A **homotopy $T$-algebra** is such a functor that preserves products up to weak equivalence in that for all $n \in \mathbb{N}$ the canonical morphism

  $$
     \prod_{i = 1}^n A(p_i) : A(x^n) \to (A(x))^n
  $$

  is a [[nLab:model structure on simplicial sets|weak equivalence]].

  There is a model structure for such homotopy $T$-algebras, given by left [[nLab:Bousfield localization of model categories|Bousfield localization]] of the projective [[nLab:model structure on simplicial presheaves]] at the morphisms $\coprod_n F_T(1) \to F_T(n)$, where $F_T(n)$ is the free $T$-algebra on $n$ generators.

  But it turns out that one can further strictify this: a [[nLab:simplicial algebra|simplicial T-algebra]] is a strict functor $T \to sSet$ that also preserves all products up to isomorphism. There is a [[nLab:model structure on simplicial T-algebras]], going back to Quillen, where the weak equivalences and the fibrations are objectwise those of simplicial sets.

  And there is a [[nLab:Quillen equivalence]] between these model structures for homotopy $T$-algebras and for simplicial $T$-algebras.

  This Quillen equivalence is described in

  * [[nLab:Bernard Badzioch]], _Algebraic theories in homotopy theory_ Annals of Mathematics, 155 (2002), 895-913 ([JSTOR](http://www.jstor.org/stable/3062135))

  The result that strict simplicial algebras model all $\infty$-$T$-algebras is also in

  * [[nLab:Julie Bergner]], _Rigidification of algebras over multi-sorted theories_ , Algebraic and Geometric Topoogy 7, 2007.


* _Nov 5, 2010_

  **[[nLab:monoidal Dold-Kan correspondence]]** and **[[nLab:model structure on dg-algebras]]**

  We have seen that the [[nLab:model structure on simplicial T-algebras]]
  models $\infty$-T-algebras. When $T$ is an _abelian_ Lawvere theory,
  so that every $T$-algebra has an underlying [[nLab:abelian group]],
  it is useful to consider the [[nLab:Moore complex|normalized chains complex]] of a simplicial $T$-algebra: equipped with the [[nLab:cup product]] this is a [[nLab:dg-algebra]] (in non-negative degree).

  There is a standard [[nLab:model structure on dg-algebra]]s that prevails
 much of the literature. For instance in its dual form this is the model structure 
 traditionally used in [[nLab:rational homotopy theory]]. 

  The [[nLab:monoidal Dold-Kan correspondence]] asserts that at least for
 $T$ a theory of ordinary commutative algebras, there is a [[nLab:Quillen equivalence]] 
 
  $$
    T Alg_{proj}^{\Delta^{op}} \simeq dgAlg^+_{proj}
  $$

  between the model structure on simplicial algebras and that on 
  chain dg-algebras in non-negative degree. This is a monoidal 
  refinement of the standard [[nLab:Dold-Kan correspondence]] that 
  identifies [[nLab:simplicial abelian group]]s with [[nLab:chain complex]]es.
  
  This means that dg-algebras are yet another equivalent model for (certain) $\infty$-algebras. In applications it is convenient to pass back and forth along this equivalence: the simplicial algebras connect more directly to the abstract theory, but the available toolset of theorems and techniqies for dg-algebras is much larger, and they are generally easier to handle.


### Derived geometry over $\infty-C^\infty$-rings {#Smooth}

* _Nov 12, 2010_

  **[[nLab:derived loop space]]s**

  Analogous to how a good deal of the phenomenology of [[nLab:stack]]s is exhibited already by the [[nLab:action groupoid|weak quotient]] $*//G$ we have that much of the phenomenology of derived geometriy is exhibited already by [[nLab:free loop space object]]s $\mathcal{L}X$ of a derived space $X$: the [[nLab:(∞,1)-pullback]] of the diagonal on $X$ along itself

  $$
    \mathcal{L}X := X \times_{X \times X} X
    \,.
  $$

  When $X$ is an ordinary object in the inclusion $(\infty,1)Sh(T Alg^{op}) \hookrightarrow (\infty,1)Sh(T Alg_\infty^{op})$ one calls $\mathcal{L}X$ for emphasis also the [[nLab:derived loop space]] of $X$.

  Since this pullback is maximally non-transversal, the derived free loop space is quite different from the ordinary free loop space object computed in $(\infty,1)Sh(T Alg^{op})$. Notably when $X$ is 0-[[nLab:truncated]] (just a plain space, no groupoidal morphisms, no derived resoluton) its underived loop space object is just $X$ itself and hence uninteresting, whereas its derived loop space is very rich:

  one finds that the [[nLab:function algebras on ∞-stacks|function algebra on]] $\mathcal{L}X$ is the complex that computes the [[nLab:Hochschild homology]] of the function algebra of $X$:

  $$
    C(\mathcal{L}X) \simeq \mathbf{HH}_\bullet(C(X))
    \,.
  $$

  To some extent this is just the tautological dual reformulation of Hochschild homology as the $(\infty,1)$-categorical ([[nLab:derived functor|derived]]) tensor product

  $$
    \mathbf{HH}_\bullet(A) := A \otimes_{A \otimes A} A
    \,.
  $$  

  But there are some noteworthy subtleties. For instance in the traditional literature the derived tensor product is taken in the context of modules, not of algebras.  But one can see that forming a fibrant replacement in the model structure on homotopy $T$-algebras puts an $\infty$-algebra structure back on the Hochschild complex.

  This relation between derived loop spaces and Hochschild homology is very fruitful. It gives a transparent conceptual interpretation to many constructions in Hochschild cohomology and makes all this standard theory applicable to the study of derived geometry. 
  
* _Nov 19, 2010_

  **[[nLab:derived smooth manifold]]s**

  The Lawvere theory that encodes standard models of smooth differential geometry ([[nLab:synthetic differential geometry]]) is the category [[nLab:CartSp]] of [[nLab:Cartesian space]]s and [[nLab:smooth function]]s between them. Its algebras are [[nLab:smooth algebra]]s / $C^\infty$-rings. Therefore its $\infty$-algebras are modeled by simplicial $C^\infty$-rings.

  Spaces locally ringed in such smooth $\infty$-algebras are called _derived smooth manifolds_ .


## References

A systematic description of derived geometry using [[nLab:model category]]-theoretic tools was first undertaken in 

* [[nLab:Bertrand Toën]], [[nLab:Gabriele Vezzosi]], 

  * _Homotopical Algebraic Geometry I: Topos theory_ ([arXiv](http://arxiv.org/abs/math/0207028))

  * _Homotopical Algebraic Geometry II: geometric stacks and applications _ ([arXiv](http://arxiv.org/abs/math/0404373))

This generalizes the Brown-Jardine-Joyal-[[nLab:model structure on simplicial presheaves]] to a [[nLab:model structure on sSet-enriched presheaves]] over an [[nLab:sSet-site]].

A proposal for the precise set of the scene of derived geometry in general abstract [[nLab:(∞,1)-category theory]]-terms is

* [[nLab:Jacob Lurie]], _[[nLab:Structured Spaces]]_

The main point of this is a formalization and identification of special tame objects inside the collection of all [[nLab:derived stack]]s, namely the [[nLab:derived scheme]]s and [[nLab:structured (∞,1)-topos]]es.

The relevance of [[nLab:derived loop space]]s in derived was notably amplified in a series of articles by [[nLab:David Ben-Zvi]] and [[nLab:David Nadler]],

* [[nLab:David Ben-Zvi]], [[nLab:David Nadler]],

  * _Loop Spaces and Langlands Parameters_ ([arXiv:0706.0322](http://arxiv.org/abs/0706.0322)) 

  * _Integral Transforms and Drinfeld Centers in Derived Algebraic Geometry _ ([arXiv:0805.0157](http://arxiv.org/abs/0805.0157))

  * _Loop Spaces and Connections_ ([arXiv:1002.3636](http://arxiv.org/abs/1002.3636))

    This article uses To&#235;n's theory of [[nLab:function algebras on ∞-stacks]] for showing that the function complex on a derived loop space $\mathcal{L}X$ is under mild conditions the [[nLab:Hochschild homology]] complex of $X$ hence by [[nLab:Hochschild-Kostant-Rosenberg theorem]] the collection of [[nLab:Kähler differential]] forms on $X$, and that the functions on $\mathcal{L}X$ that are invariant under the canonical $S^1$-[[nLab:action]] on $\mathcal{L}X$ are the _closed_ forms. This also gives a geometric interpretation of the old observation by [[nLab:Maxim Kontsevich]] and others, that the differential and grading on the de Rham complex may be understood as induced from automorphisms of the [[nLab:odd line]].

  * _Loop Spaces and Representations_ ([arXiv:1004.5120](http://arxiv.org/abs/1004.5120))


The application of derived geometry to the construction of [[nLab:tmf]] is described in

* [[nLab:Jacob Lurie]], _[[nLab:A Survey of Elliptic Cohomology]]_

The article

* [[nLab:David Spivak]], _Derived smooth manifolds_ ([arXiv:0810.5174](http://arxiv.org/abs/0810.5174))

discussed the $\infty$-version of [[nLab:smooth algebra|C-oo-rings]] -- the algebras over the Lawvere theory [[nLab:CartSp]] -- and the corresponding locally ringed spaces: [[nLab:derived smooth manifold]]s.
