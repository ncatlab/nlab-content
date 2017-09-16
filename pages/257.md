See also: [[homotopy theory]].

#Idea#

A __model category__ (sometimes called a _Quillen model category_ or a _closed model category_) is a [[category]] equipped with extra structure which allows one to treat it as a presentation for an $(\infty,1)$-[[(infinity,1)-category|category]], i.e. as a model for [[homotopy theory]].

The idea of model categories is to work just with 1-morphisms instead of with $n$-morphisms for all $n$, but to carry around extra information to remember which 1-morphisms should become [[equivalence|equivalences]] in the full $(\infty,1)$-category, along with additional data which allows us to perform many $(\infty,1)$-categorical constructions at the level of the model category.

Most importantly, a model category is a [[category with weak equivalences]]. The collection of weak equivalences already determines the corresponding $(\infty,1)$-[[(infinity,1)-category|category]]. The rest of the structure carried by a model category -- the choice of [[fibration]]s and [[cofibration]]s -- is auxiliary data whose purpose is to _facilitate computations_, in particular to facilitate the computation of the [[homotopy category]] and of [[derived functor]]s.  See [[homotopy theory]] for more details.

#Definition#

A **model structure** on a category $K$ consists of three distinguished classes of morphisms - the **cofibrations** $C$, the **fibrations** $F$, and the **weak equivalences** $W$ - satisfying the following two properties.

(i) $W$ has the **2 of 3** property: given a composable pair of morphisms $f,g$ if two of three of $f, g, g f$ are in $W$, so is the third. 

(ii) $(C, F \cap W)$ and $(C \cap W, F)$ are two [[weak factorization system|weak factorization systems]] on $K$.

A **model category** is a complete and cocomplete category $K$ with a model structure $(C,F,W)$.

#Notes#

* Some authors, notably Mark Hovey, require that the factorizations given by (ii) are actually _functorial_. In practice, Quillen's [[small object argument]] means that many model categories can be made to have functorial factorizations.

* As a consequence of the above definition, the classes $C, F,$ and $W$ are all closed under retracts and composition and contain the isomorphisms of $K$. This is least obvious in the case of $W$. In the presence of functorial factorizations, it is easy to show that closure under retracts follows from (i) and (ii); with a bit of cleverness, this can also be done without functoriality.

#Examples#

Historically, the most important examples have been the following.

* [[model structure on simplicial sets]]
* [[model structure on topological spaces]]
* [[model structure on chain complexes]]

Other model structures which at the moment we have entries for are

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

For yet another introduction to model categories, with an eye towards their use as [[presentable (infinity,1)-category|presentations]] of [[(infinity,1)-category|(infinity,1)-categories]] see Appendix A.2 of

* [[Jacob Lurie]], [[Higher Topos Theory]]