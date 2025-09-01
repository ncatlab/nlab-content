
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


\tableofcontents


## Idea 

The **Gray tensor product** is a "better" replacement for the cartesian product of [[strict 2-categories]] with respect to [[pseudonatural transformations]].  To get the idea it suffices to consider the 2-category $\mathbf{2}$ which has two objects, 0 and 1, one non-identity morphism $0\to 1$, and no nonidentity 2-cells. Then the cartesian product $\mathbf{2}\times\mathbf{2}$ is a commuting square, while the Gray tensor product $\mathbf{2}\otimes\mathbf{2}$ is a square which commutes up to isomorphism.

More generally, given [[2-categories]] $C$ and $D$, a [[2-functor]] $C\times\mathbf{2} \to D$ consists of two 2-functors $C\to D$ and a strict 2-natural transformation between them, while a 2-functor $C\otimes\mathbf{2} \to D$ consists of two 2-functors $C\to D$ and a *[[pseudonatural transformation]]* between them.

## Preliminaries
 {#Preliminaries}

Throughout, write

\[
  \label{2Cat}
  2Cat \in CAT
\]

for the [[very large category|very large]] [[category]] whose 

* [[objects]] are [[strict 2-categories]]

* [[morphisms]] are [[strict 2-functors]].

For $X, Y \in 2Cat$, we write

$$
  Hom_{2Cat}(X,Y) \in Set
$$

for the [[hom set]] of this 2-category, hence for the [[set]] of [[strict 2-functors]] $X \to Y$.

Of course, there is not just a set but a [[strict 2-category]] of such functors. Specifically, we write

\[
  \label{Ps}
  Ps(Y,Z)
  \in
  2Cat
\] 

for the [[strict 2-category|strict]] [[2-functor 2-category]] whose

* [[objects]] are [[strict 2-functors]] $Y \to Z$,

* [[1-morphisms]] are [[pseudonatural transformations]] between these, 

* [[2-morphisms]] are [[modifications]] between those,

with [[composition]] operations the canonical [[horizontal composition]] and [[vertical composition]] of this data.

(cf. [Johnson & Yau 2020, Ntn. 12.2.24](#JohnsonYau20))

The point of the Gray tensor product may be regarded as bringing out the [[enriched category|enrichment]] of $2Cat$ by these hom 2-categories $Ps(-,-)$ (eq:Ps):


## Definition
 {#Definition}

\begin{definition}
The *Gray tensor product* is the [[functor]]

\[
  \label{GrayTensorAsFunctor}
  \otimes_{Gray} 
    \;\colon\; 
  2Cat \times 2Cat \longrightarrow 2Cat
\]

given by (...).

\end{definition}

(cf. [Johnson & Yau 2020, Def. 12.2.5](#JohnsonYau20))


## Properties
 {#Properties}

### Hom-adjunction and closure

First of all: 

\begin{proposition}
The Gray tensor product (eq:GrayTensorAsFunctor) makes $2Cat$ (eq:2Cat) into a [[symmetric monoidal category|symmetric]] [[monoidal category]]

\[
  \label{2CatAsAMonoidalCategory}
  \big(
    2Cat, \otimes_{Gray}, \ast
  \big)
  \in MonCAT
  \,.
\]

\end{proposition}

(cf. [Johnson & Yau 2020, Thm. 12.2.23](#JohnsonYau20))

As such, the characteristic property of the Gray tensor product is that: 

\begin{proposition}
\label{HomIsomorphism}
There are [[natural bijections]] 

\[
  \label{TheHomIsomorphism}
  Hom_{2Cat}(X \otimes_{Gray} Y, Z)   
   \simeq 
  Hom_{2Cat}\big(X, Ps(Y,Z)\big) 
  \,,
\]

natural in $X, Y, Z \in 2 Cat$.

\end{proposition}

(cf. [Johnson & Yau 2020, Prop. 12.2.27 with Thm. 12.2.20](#JohnsonYau20))

Since (eq:TheHomIsomorphism) are the [hom isomorphism](adjoint+functor#InTermsOfHomIsomorphism) for an [[internal hom]]-[[adjoint functor|adjunction]]

$$
  \big(
  (-) \otimes_{Gray} Y
  \big)
  \;\dashv\;
  Ps(Y,-)
  \,,
$$

Prop. \ref{HomIsomorphism} says that the [[symmetric monoidal category]] $(2Cat, \otimes_{Gray}, \ast)$ (eq:2CatAsAMonoidalCategory) is in a fact [[closed monoidal category|closed]], hence is a [[symmetric closed monoidal category]] (with tensor product being the Gray tensor and) with [[internal hom]] given by $Ps(-,-)$ (eq:Ps).

### Further properties

\begin{proposition}
  \label{BiequivalenceToCartesianProduct}
  For $X, Y \in 2Cat$, the canonical comparison 2-functor from their Gray tensor product to their [[Cartesian product]] is an [[equivalence of 2-categories]]:
\[
  \label{ComparisonMapGrayToCartesian}
  X \otimes_Gray Y 
    \xrightarrow{\phantom{--} 
      \sim 
    \phantom{--}} 
  X \times Y
  \,.
\]
\end{proposition}
(cf. [Lack 2002, top of p. 7](#Lack2002))

\begin{proposition}
  \label{UnderSimplicialNerve}
  Under passage to [[simplicial set|simplicial]] [[geometric nerve of a bicategory|nerves]] of [[strict 2-groupoids]]
\[
  \label{SimplicialNerveOf2Groupoids}
  N 
    \;\colon\;
  2Grpd \longrightarrow sSet
  \mathrlap{\,,}
\]


1. the nerve of a Gray tensor product of 2-groupoids,

1. the [[Cartesian product]] (cf. *[[product of simplices]]*) of the nerves of the separate 2groupoids 

are related by a [[simplicial weak equivalence]], in fact by an [[acyclic Kan fibration]]:

$$
  \mathllap{
  X, Y \in 2Grpd
  \;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;
  }
  N\big(
   X \otimes_{Gray} Y
  \big)
  \xrightarrow{ \in Fib \cap W }
  N(X) \times N(Y)
  \mathrlap{\,.}
$$
\end{proposition}
\begin{proof}
  The comparison map (eq:ComparisonMapGrayToCartesian) is indeed an [[acyclic fibration]] ([Lack 2002, top of p. 7](#Lack2002)) in the [[canonical model structure on 2-categories|canonical model structure on 2-groupoids]], and on that the nerve (eq:SimplicialNerveOf2Groupoids) is a [[right Quillen functor]] to the [[classical model structure on simplicial sets]] ([Lack 2002, end of p. 29](#Lack2002), following [Moerdijk & Svensson 1993](canonical+model+structure+on+2-categories#MoerdijkSvensson93)).
\end{proof}

## Remarks 

* When considered with this monoidal structure, $2Cat$ is often called $Gray$.  [[Gray-category|Gray-categories]], or categories [[enriched category|enriched]] over $Gray$, are a model for [[semi-strict infinity-category|semi-strict]] [[3-categories]].  Categories enriched over $2Cat$ with its cartesian product are _strict_ 3-categories, which are not as useful.  This is one precise sense in which the Gray tensor product is "more correct" than the cartesian product.

* $Gray$ is an example of a [[semicartesian monoidal category]], i.e. a non-[[cartesian monoidal category|cartesian]] monoidal category whose unit object is nevertheless the terminal object.

* There are also versions of the Gray tensor product in which pseudonatural transformations are replaced by lax or oplax ones.  (In fact, these were the ones originally defined by Gray.)

* $Gray$ is actually a monoidal [[model category]] (that is, a model category with a monoidal structure that interacts well with the model structure), which $2Cat$ with the cartesian product is not.  In particular, the cartesian product of two cofibrant 2-categories need not be cofibrant.  This is another precise sense in which the Gray tensor product is "more correct" than the cartesian product.

* The cartesian monoidal structure is sometimes called the "black"  product, since the square $2\times 2$ is "completely filled in" (i.e. it commutes).  There is another "white" tensor product in which the square $2\Box 2$ is "not filled in at all" (doesn't commute at all), and the "gray" tensor product is in between the two (the square commutes up to an isomorphism).  This is a pun on the name of John Gray, for whom the Gray tensor product is named.  The "white" tensor product is also called the [[funny tensor product]].

* There are generalizations to [[higher category theory|higher categories]] of the Gray tensor product. In particular there is a tensor product on [[strict omega-category|strict omega-categories]] -- the [[Crans-Gray tensor product]] -- which is such that restricted to strict 2-categories it reproduces the Gray tensor product.

* A  [[closed monoidal category|closed monoidal structure]] on [[strict omega-category|strict omega-categories]] is introduced by Al-Agl, Brown and Steiner. This uses an equivalence between the categories of strict (globular) omega categories and of strict  cubical omega categories with connections; the construction of the closed  monoidal  structure on the latter category is direct and generalises that for strict cubical omega groupoids with connections established by Brown and Higgins.

* The Gray tensor product cannot be extended to a [[2-functor]] (or 3-functor) on the [[2-category]] of 2-categories, 2-functors, [[2-natural transformations]], and [[modifications]]. See [this MathOverflow answer](https://mathoverflow.net/a/459360).

## Related entries

* [[Crans-Gray tensor product]]

* [[generalized Gray tensor product]]

* [[Verity-Gray tensor product]]


## References

### In 2-category theory

Original discussion of the Gray tensor product in [[2-category theory]]:

* [[John W. Gray]], Theorem 1, 4.14 of: _[[Adjointness for 2-Categories|Formal category theory: Adjointness for 2-categories]]_, Lecture Notes in Mathematics **391**, Springer (1974) &lbrack;[doi:10.1007/BFb0061280](https://doi.org/10.1007/BFb0061280)&rbrack; 

* [[John W. Gray]], _Coherence for the Tensor Product of 2-Categories, and Braid Groups_, in: _Algebra, Topology, and Category Theory_, Academic Press (1976) 62-76

In the context of the [[canonical model structure on 2-categories]]:

* {#Lack2002} [[Stephen Lack]]: *A Quillen model structure for 2-categories*, K-Theory **26** 2 (2002) 171-205 &lbrack;[doi:10.1023/A:1020305604826](http://dx.doi.org/10.1023/A:1020305604826), [[Lack-ModelOn2Cat.pdf:file]], [zbmath](https://zbmath.org/?q=an%3A1017.18005)&rbrack;


Further discussion:

* [[Ronnie Brown]], [[Philip Higgins]]: *Tensor products and homotopies for $\omega$-groupoids and crossed complexes*,J. Pure Appl. Alg. **47** (1987) 1-33 *lbrack;doi:[10.1016/0022-4049(87)90099-5](https://doi.org/10.1016/0022-4049(87%2990099-5), ([pdf](https://pdfs.semanticscholar.org/3323/d82ed1effb1953a6af573aab2e3fb0b02394.pdf)&rbrack;

* [[Robert Gordon]], [[John Power]], [[Ross Street]]:  _Coherence for tricategories_, Mem. Amer. Math. Soc. **117** 558 (1995) &lbrack;[doi:10.1090/memo/0558](http://dx.doi.org/10.1090/memo/0558), [ams:memo-117-558](https://bookstore.ams.org/memo-117-558/)&rbrack;

* F.A. Al-Agl, R. Brown and   R. Steiner, _Multiple categories: the equivalence between a globular and cubical approach_, Advances in Mathematics, 170 (2002) 71-118. doi:[10.1006/aima.2001.2069](https://doi.org/10.1006/aima.2001.2069), arXiv:[math/0007009](https://arxiv.org/abs/math/0007009)

Comprehensive review:

* {#JohnsonYau20} [[Niles Johnson]], [[Donald Yau]], section 12.2 of: *2-Dimensional Categories*, Oxford University Press (2021) &lbrack;[arXiv:2002.06055](http://arxiv.org/abs/2002.06055), [doi:10.1093/oso/9780198871378.001.0001](https://oxford.universitypressscholarship.com/view/10.1093/oso/9780198871378.001.0001/oso-9780198871378)&rbrack;


On the Gray tensor product as the [[left Kan extension]] of a tensor product on the full subcategory $Cu$ of $2Cat$:

* [[Ross Street]], p. 16 of: _Gray's tensor product of 2-categories_, 22-page handwritten note, (1988) &lbrack;[pdf](http://maths.mq.edu.au/~street/GrayTensor.pdf)&rbrack;

A general theory of lax tensor products, unifying Gray tensor products with the [[Crans-Gray tensor product]] is in 

* [[Michael Batanin]], [[Denis-Charles Cisinski]], [[Mark Weber]], _Multitensor lifting and strictly unital higher category theory_ ([arXiv:1209.2776](http://arxiv.org/abs/1209.2776))

A proof that the Gray tensor product does form a monoidal structure, based only on its universal property, is in

* [[John Bourke]], [[Nick Gurski]], _The Gray tensor product via factorisation_, Appl Categor Struct **25** (2017) p603-624, doi:[10.1007/s10485-016-9467-6](https://doi.org/10.1007/s10485-016-9467-6), arXiv:[1508.07789](http://arxiv.org/abs/1508.07789)

On its generalization to [[Gray-category|Gray-categories]]

* [[Sjoerd Crans]]. "A tensor product for $Gray$-categories". *Theory and applications of categories*, 5(2), 12-69. ([tac](http://www.tac.mta.ca/tac/volumes/1999/n2/5-02abs.html)) ([pdf](http://www.tac.mta.ca/tac/volumes/1999/n2/n2.pdf))

### In enhanced 2-category theory

For [[enhanced 2-categories]]:

* [[Nathanael Arkor]], [[John Bourke]], Joanna Ko: _Enhanced 2-categorical structures, two-dimensional limit sketches and the symmetry of internalisation_ &lbrack;[arXiv:2412.07475](https://arxiv.org/abs/2412.07475)&rbrack;

### In $(\infty,2)$-category theory
 {#ReferencesInInfinity2CategoryTheory}

Discussion of the Gray tensor product in [[(infinity,2)-category|$(\infty,2)$-category]] theory:

* {#GaitsgoryRozenblyum17} [[Dennis Gaitsgory]], [[Nick Rozenblyum]]: *Lax functors and the Gray product*, Chapter 10.3 in the Appendix of: *[[A study in derived algebraic geometry]]*, Mathematical Surveys and Monographs **221**, Americal Mathematical Society (2017) &lbrack;[ams:SURV/221](https://bookstore.ams.org/view?ProductCode=SURV/221), [book webpage](https://people.mpim-bonn.mpg.de/gaitsgde/Book/)&rbrack;

* [[Félix Loubaton]], [[Jaco Ruit]]: *On the squares functor and the Gaitsgory-Rozenblyum conjectures* &lbrack;[arXiv:2507.07807](https://arxiv.org/abs/2507.07807)&rbrack;

* {#Loubaton25} [[Félix Loubaton]], answer to: *The missing proofs in Gaitsgory–Rozenblyum's derived algebraic geometry book* (Jul 2025) &lbrack;[MO:a/497541](https://mathoverflow.net/a/497541/)&rbrack;


[[!redirects Gray tensor products]]

[[!redirects Gray]]




