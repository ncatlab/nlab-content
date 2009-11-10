
<div class="rightHandSide toc">
[[!include model category theory - contents]]
***
[[!include homotopy - contents]]
</div>




#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

A __model category__ (sometimes called a _Quillen model category_ or a _closed model category_) is a [[category with weak equivalences]] that is equipped with extra structure which  facilitates the computation and handling of its [[simplicial localization]] that yields the [[(∞,1)-category]] _modeled_ by the model category.

In this sense model categories are _models for [[homotopy theory]]_ .

Recall that the idea of [[category with weak equivalences|categories with weak equivalences]] is to work just with 1-morphisms instead of with $n$-morphisms for all $n$, but to carry around extra information to remember which 1-morphisms are really [[equivalence|equivalences]] in the full [[(∞,1)-category]], i.e. [[isomorphism]]s in the corresponding [[homotopy category]].

In a model category the data of weak equivalences is accompanied by further auxiliary data that helps to compute the [[(∞,1)-categorical hom-space]], the [[homotopy category]] and [[derived functor]]s. See [[homotopy theory]] for more on that.

If the model category happens to be a [[combinatorial simplicial model category]] $\mathbf{A}$ it [[presentable (infinity,1)-category|presents]] the [[(infinity,1)-category|category]] $\mathbf{A}^\circ$ in the form of a [[simplicially enriched category]] given by the full [[SSet]]-[[enriched category|enriched subcategory]] on objects that are both fibrant and cofibrant.


#Definition#

A **model structure** on a category $K$ consists of three distinguished classes of morphisms - the **cofibrations** $C$, the **fibrations** $F$, and the **weak equivalences** $W$ - satisfying the following two properties.

(i) $W$ is closed under retracts in the arrow category makes $K$ a [[category with weak equivalences]] in that it is closed under **2-out-of-3** : given a composable pair of morphisms $f,g$ if two of three of $f, g, g f$ are in $W$, so is the third. 

(ii) $(C, F \cap W)$ and $(C \cap W, F)$ are two [[weak factorization system|weak factorization systems]] on $K$.

A **model category** is a complete and cocomplete category $K$ with a model structure $(C,F,W)$.

# Variants #

There are several notions of [[category with weak equivalences]] with similar but less structure than a full model category.

* A [[category of fibrant objects]] has a notion of just weak equivalences and fibrations, none of cofibrations.

* A [[Waldhausen category]] dually has a notion of weak equivalences and cofibrations.

There is a slight variant of the full notion of model category by Thomason that is designed to make the [[global model structure on functors]] more naturally accessible: this is the notion of [[Thomason model category]].

#Notes#

* Some authors, notably Mark Hovey, require that the factorizations given by (ii) are actually _functorial_. In practice, Quillen's [[small object argument]] means that many model categories can be made to have functorial factorizations.

* As a consequence of the above definition, the classes $C, F,$ and $W$ are all closed under retracts and composition and contain the isomorphisms of $K$. This is least obvious in the case of $W$. In the presence of functorial factorizations, it is easy to show that closure under retracts follows from (i) and (ii); with a bit of cleverness, this can also be done without functoriality.

#Examples#

The archetypical model structures is 

* [[model structure on topological spaces]]

and its subcategory of nice topological spaces is [[Quillen equivalence|Quillen equivalent]] to the standard

* [[model structure on simplicial sets]]

that models [[∞-groupoid]]s  in terms of [[Kan complex]]es. 

More generally, the Joyal [[model structure on simplicial sets]] models [[(∞,1)-category|(∞,1)-categories]] in terms of [[quasi-category|quasi-categories]].

The [[operad]] version is given by the 

* [[model structure on dendroidal sets]]

and generalizes from the notion [[(∞,1)-category]] to that of [[(∞,1)-operad]].

Related by the [[Dold-Kan correspondence]] to the [[model structure on simplicial sets]] are structures like

* [[model structure on chain complexes]]
* [[model structure on dg-algebras]].


The _parameterized_ version of the model structure on simplicial sets is a

* [[model structure on simplicial presheaves]]

which serves as a [[models for infinity-stack (infinity,1)-toposes|model for ∞-stack (∞,1)-toposes]] (for [[hypercomplete (∞,1)-topos]]es, more precisely).

These are based on more generally available 

* [[projective model structure|global model structures on functor categories]]

such as

* [[Reedy model structure]]s .

A source of relevance in practice of new model structures from old ones is [[Bousfield localization]].

Many notions of [[higher category theory|higher categories]] come equipped with model structures, witnessing the fact that when retaining only invertible transformations between $n$-categories they should form an $(\infty,1)$-[[(infinity,1)-category|category]]. 

* [[model structure on simplicially enriched categories]]
* [[folk model structure|model structure on omega categories]]
* [[folk model structure|model structure on omega-groupoids]]


#References#

An introductory survey of some key concepts is in the set of slides

* Peter May, [[ModelCatPrimer.pdf:file]]

There is an unpublished manuscript of Chris Reedy from around 1974 that's been circulating as an increasingly faded photocopy. It's been typed into LaTeX, and the author has given  [permission](http://www-math.mit.edu/~psh/#Other%20mathematics) for it to be posted on the net:

* Chris Reedy, _Homotopy theory of model categories_ ([pdf](http://www-math.mit.edu/~psh/reedy.pdf))

Recent review:

* Paul G. Goerss, Kristen Schemmerhorn, _Model Categories and Simplicial Methods_ ([arXiv](http://arxiv.org/abs/math.AT/0609537))

A nice first introduction:

* Dwyer, Spalinski, _Homotopy theories and model categories_ [pdf](http://hopf.math.purdue.edu/Dwyer-Spalinski/theories.pdf)

Monographs: 

* Philip S. Hirschhorn, _Model Categories and Their Localizations_ ([AMS](http://www.ams.org/bookstore?fn=20&arg1=whatsnew&item=SURV-99))
* Mark Hovey, _Model Categories_ ([Google books](http://books.google.co.uk/books?id=Kfs4uuiTXN0C&printsec=frontcover))

See 

* P. Hirschhorn, personal website: [Mathematics](http://www-math.mit.edu/~psh/#Mathematics)

for errata and more. 

For yet another introduction to model categories, with an eye towards their use as [[presentable (infinity,1)-category|presentations]] of $(\infty,1)$-[[(infinity,1)-category|categories]] see Appendix A.2 of

* [[Jacob Lurie]], [[Higher Topos Theory]]

[[!redirects model categories]]
[[!redirects model structure]]
[[!redirects model structures]]
