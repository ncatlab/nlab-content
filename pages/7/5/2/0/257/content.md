

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
* automatic table of contents goes here
{:toc}


## Idea

A __model category__ (sometimes called a _Quillen model category_ or a _closed model category_) is a context for doing [[homotopy theory]].    Quillen developed the definition of a model category to formalize the similarities between [[homotopy theory]] and [[homological algebra]]: the key examples which motivated his definition were the category of [[topological space|topological spaces]], the category of [[simplicial set|simplicial sets]], and the category of [[chain complex|chain complexes]].

So, what is a model category?  For starters, it is a category equipped with three classes of morphisms, each closed under composition: [[weak equivalences]], [[fibrations]] and [[cofibration|cofibrations]]:

* The weak equivalences play the role of 'homotopy equivalences' or something a bit more general.  Already in the case of [[topological space|topological spaces]], it is useful to say that two spaces have the same [[homotopy type]] if there is a map from one to the other that induces isomorphisms on homotopy groups for any choice of basepoint in the first space.  These maps are more general than homotopy equivalences, so they are called 'weak equivalences'.

* The [[fibrations]] play the role of 'nice surjections'.  For example, in the category [[Top]] of [[topological spaces]] with its usual [[model structure on topological spaces]], a locally trivial [[fiber bundle]] is typically a fibration.

* The [[cofibrations]] play the role of 'nice inclusions'.  For example, in the category [[Top]] of [[topological spaces]] with its usual [[model structure on topological spaces]], an [[NDR pair]] is typically a cofibration.  

A bit more technically: we can define an [[(∞,1)-category]] starting from any [[category with weak equivalences]].  The idea is that this (∞,1)-category keeps track of objects in our original category, morphisms between objects, homotopies between maps, homotopies between homotopies, and so on, _ad infinitum_.  However, the extra structure of a model category makes it easier to work with this (∞,1)-category.  We can obtain this (∞,1)-category in various ways, including [[simplicial localization]] if we want to obtain a simplicially enriched category as a variant of (∞,1)-category. Alternatively, to obtain a [[quasicategory]], given a model category $M$, the simplicial nerve $N_\Delta(M_{cf})$ of the subcategory $M_{cf}\subset M$ of cofibrant-fibrant objects is a quasicategory. We say this [[(∞,1)-category]] is _presented_ (or modeled) by the model category, and that the objects of the model category are _models_ for the objects of this $(\infty,1)$-category. Not every (∞,1)-category is obtained in this way (otherways it would necessarily have homotopy limits and colimits).

In this sense model categories are 'models for [[homotopy theory]]' or 'categories of models for homotopy theory'.  (The latter sense was the one intended by Quillen, but the former is also a useful way to think.)

Recall that the idea of [[category with weak equivalences|categories with weak equivalences]] is to work just with 1-morphisms instead of with $n$-morphisms for all $n$, but to carry around extra information to remember which 1-morphisms are really [[equivalence|equivalences]] in the full [[(∞,1)-category]], i.e. [[isomorphism]]s in the corresponding [[homotopy category]].

In a model category the data of weak equivalences is accompanied by further auxiliary data that helps to compute the [[(∞,1)-categorical hom-space]], the [[homotopy category]] and [[derived functor|derived functors]]. See [[homotopy theory]] for more on that.

If the model category happens to be a [[combinatorial simplicial model category]] $\mathbf{A}$ it [[presentable (infinity,1)-category|presents]] the [[(infinity,1)-category|category]] $\mathbf{A}^\circ$ in the form of a [[simplicially enriched category]] given by the full [[SSet]]-[[enriched category|enriched subcategory]] on objects that are both fibrant and cofibrant.


## Definition

A **model structure** on a [[category]] $C$ consists of three distinguished [[class]]es of [[morphism]]s - the **cofibrations** $Cof \subset Mor(C)$, the **fibrations** $Fib$, and the **weak equivalences** $W$ - satisfying the following two properties.

* (i) $W$ makes $C$ into a [[category with weak equivalences]], meaning that it is closed under **2-out-of-3**: given a composable pair of morphisms $f,g$, if two out of the three morphisms $f, g, g f$ are in $W$, so is the third.

* (ii) $(Cof, Fib \cap W)$ and $(Cof \cap W, Fib)$ are two [[weak factorization system|weak factorization systems]] on $C$.

A **model category** is a [[complete category|complete]] and [[cocomplete category]] $K$ with a model structure $(Cof,Fib,W)$.  


**Terminology**

* The morphisms in $W \cap Fib$ (the fibrations that are also weak equivalences) are called **trivial fibrations** or **[[acyclic fibrations]]** 

* The morphisms in $W \cap Cof$ (the cofibrations that are also weak equivalences) are called **trivial cofibrations** or **[[acyclic cofibrations]]**. 

* An object is called **[[cofibrant]]** if the unique morphism $\emptyset \to X$ from the [[initial object]] is a cofibration

* An object is called **[[fibrant]]** if the unique morphism $X\to *$ to the [[terminal object]] is a fibration.  

Often, the fibrant and cofibrant objects are the ones one is "really" interested in, but the category consisting only of these is not well-behaved (as a 1-category).  The factorizations supply fibrant and cofibrant replacement functors which allow us to treat any object of the model category as a 'model' for its fibrant-cofibrant replacement.


## Variants 

### Slight variations on the axioms

Quillen's original definition required only finite limits and colimits, which are enough for the basic constructions.  Colimits of larger cardinality are sometimes required for the [[small object argument]], however.

Some authors, notably [[Mark Hovey]], require that the factorizations given by (ii) are actually _functorial_. In practice, Quillen's [[small object argument]] means that many model categories can be made to have functorial factorizations.

### Enhancements of the axioms

There are several extra conditions that strengthen the notion of a model category:

* A [[monoidal model category]] is [[monoidal category]] that is also a model category in a compatible way.

* An [[enriched model category]] is an [[enriched category]] over a monoidal category, that is also a model category in a compatible way.

* An [[algebraic model category]] is one where the two defining [[weak factorization systems]] are refined to [[algebraic weak factorization systems]].

* A [[cofibrantly generated model category]] is one with a good compatible notion of [[cell complexes]].

* A [[combinatorial model category]] is one that in addition is a [[locally presentable category]].

* A left/right [[proper model category]] is one where the weak equivalences are stable under pushforward along cofibrations / pullback along fibrations

### Weaker axiom systems

There are several notions of [[category with weak equivalences]] with similar but less structure than a full model category.

* A [[category of fibrant objects]] has a notion of just weak equivalences and fibrations, none of cofibrations.  As the name implies, all of its objects are fibrant; the canonical example is the subcategory of fibrant objects in a model category.

* A [[Waldhausen category]] dually has a notion of weak equivalences and cofibrations, and all of its objects are cofibrant.

There is also a slight variant of the full notion of model category by Thomason that is designed to make the [[global model structure on functors]] more naturally accessible: this is the notion of [[Thomason model category]].




## Properties

### Closure of morphism classes under retracts

As a consequence of the definition, the classes $Cof, Fib$, and $W$ are all closed under [[retract]]s in the [[arrow category]] $Arr C$ and under composition and contain the [[isomorphism]]s of $C$. 

This is least obvious in the case of $W$. In the presence of functorial factorizations, it is easy to show that closure under retracts follows from axioms (i) and (ii); with a bit of cleverness, this can also be done without functoriality.

### Redundancy in the defining factorization systems
 {#RedundancyInTheAxioms}

It is clear that given a model category structure, any two of the three classes of special morphisms (cofibrations, fibrations, weak equivalences) determine the third:

* given $W$ and $C$, we have $F = RLP(W \cap C)$;

* given $W$ and $F$, we have $C = LLP(W \cap F)$;

* given $C$ and $F$, we find $W$ as the class of morphisms which factor into a morphism in $C \cap W$ followed by a morphism in $F \cap W$.

But, in fact, already the cofibrations and the fibrant objects determine the model structure.

+-- {: .num_prop}
###### Proposition

A model structure $(C,W,F)$ on a category $\mathcal{C}$ is determined by its class of cofibrations and its class of fibrant objects.

=--

This statement appears as ([Joyal, prop. E.1.10](#Joyal))


### Opposite model structure

+-- {: .num_prop}
###### Proposition

If a category $C$ carries a model category structure, then the [[opposite category]] $C^{op}$ carries the opposite model structure: 

its weak equivalences are those morphisms whose dual was a weak equivalence in $C$, its fibrations are those morphisms that were cofibrations in $C$ and similarly for its cofibrations.

=--

## Examples

Every category with limits and colimits carries the [[trivial model structure]] whose weak equivalences are the [[isomorphism]]s and all morphisms are cofibrations and fibrations.

### Classical model structures

The archetypical model structures are the

* [[model structure on topological spaces|Quillen model structure on topological spaces]] and the
* Quillen [[model structure on simplicial sets]].

These model categories are [[Quillen equivalence|Quillen equivalent]] and encapsulate much of "classical" homotopy theory.  From a higher-categorical viewpoint, they can be regarded as models for [[∞-groupoid]]s (in terms of [[CW complexes]] or [[Kan complex]]es, respectively).

Other classical topological objects of study, such as [[spectra]], [[equivariant homotopy theory|equivariant spaces]], and [[parametrized homotopy theory|parametrized spaces]], also form model categories.

In addition, there are also

* [[model structures on chain complexes]] and similarly
* [[model structures on dg-algebras]],

which encapsulate classical homological algebra, and are related to the [[model structure on simplicial sets]] by the [[Dold-Kan correspondence]].  In fact, Quillen's original definition of model categories was motivated by the analogy between homotopy theory and homological algebra.

### Categorical model structures

Of interest to category theorists is that many notions of [[higher category theory|higher categories]] come equipped with model structures, witnessing the fact that when retaining only invertible [[transfors]] between $n$-categories they should form an $(\infty,1)$-[[(infinity,1)-category|category]].  Many of these are called

* [[canonical model structure]]s, including "categorical" model structures for
  * categories
  * (strict or weak) [[2-categories]]
  * [[strict ∞-categories]], and
  * [[strict ∞-groupoids]].

Model categories have successfully been used to compare many different notions of [[(∞,1)-category]].  The following definitions of $(\infty,1)$-category all form Quillen equivalent model categories:

* [[simplicially enriched categories]]
* [[quasi-categories]] (via the Joyal [[model structure on simplicial sets]])
* [[Segal categories]]
* [[complete Segal spaces]]

Other "higher categorical structures" can also  be expected to form model categories, such as the 

* [[model structure on dendroidal sets]]

which generalizes the Joyal model structure from [[(∞,1)-categories]] to [[(∞,1)-operads]].

There is also another class of model structures on categorical structures, often called [[Thomason model structure]]s (not to be confused with the notion of "Thomason model category").  In the "categorical" or "canonical" model structures, the weak equivalences are the categorical [[equivalences]], but in the Thomason model structures, the weak equivalences are those that induce weak homotopy equivalences of [[nerves]].  Thomason model structures are known to exist on 1-categories and 2-categories, at least, and are generally Quillen equivalent to the Quillen model structures on topological spaces and simplicial sets (via the nerve construction).

### Parametrized model structures

The _parameterized_ version of the model structure on simplicial sets is a

* [[model structure on simplicial presheaves]] or
* [[model structure on simplicial sheaves]] or

which serves as a [[models for infinity-stack (infinity,1)-toposes|model for ∞-stack (∞,1)-toposes]] (for [[hypercomplete (∞,1)-topos]]es, more precisely).

### Functor and localized model structures

Many model structures, including those for complete Segal spaces, simplicial presheaves, and diagram spectra, are constructed by starting with a model structure on a functor category, such as a

* [[projective model structure]],
* [[injective model structure]], or 
* [[Reedy model structure]],

and applying a general technique called [[Bousfield localization]] which forces a certain class of morphisms to become weak equivalences.  It can also be thought of as forcing a certain class of objects to become fibrant.


## References

An account is in

* [[joyalscatlab:HomePage|Joyal's CatLab]], _[[joyalscatlab:Model categories]]_

and appendix E of 

* [[André Joyal]], _The theory of quasi-categories and its applications_ ([pdf](http://www.crm.cat/HigherCategories/hc2.pdf))
 {#Joyal}

An introductory survey of some key concepts is in the set of slides

* [[Peter May]], [[ModelCatPrimer.pdf:file]]

There is an unpublished manuscript of [[Chris Reedy]] from around 1974 that's been circulating as an increasingly faded photocopy. It's been typed into LaTeX, and the author has given  [permission](http://www-math.mit.edu/~psh/#Other%20mathematics) for it to be posted on the net:

* [[Chris Reedy]], _Homotopy theory of model categories_ ([pdf](http://www-math.mit.edu/~psh/reedy.pdf))

Recent review:

* [[Paul Goerss]], [[Kristen Schemmerhorn]], _Model Categories and Simplicial Methods_ ([arXiv](http://arxiv.org/abs/math.AT/0609537))

A nice first introduction:

* Dwyer, Spalinski, _Homotopy theories and model categories_ ([pdf](http://hopf.math.purdue.edu/Dwyer-Spalinski/theories.pdf))

Monographs: 

* Philip S. Hirschhorn, _Model Categories and Their Localizations_ ([AMS](http://www.ams.org/bookstore?fn=20&arg1=whatsnew&item=SURV-99))

* [[Mark Hovey]], _Model Categories_ Mathematical Surveys and Monographs, Volume 63, AMS (1999) ([Google books](http://books.google.co.uk/books?id=Kfs4uuiTXN0C&printsec=frontcover))

See 

* P. Hirschhorn, personal website: [Mathematics](http://www-math.mit.edu/~psh/#Mathematics)

for errata and more. 

* [[William Dwyer]], [[Philip Hirschhorn]], [[Daniel Kan]], 
  [[Jeff Smith]], _[[Homotopy Limit Functors on Model Categories
and Homotopical Categories]]_ , volume 113 of Mathematical Surveys and Monographs


For yet another introduction to model categories, with an eye towards their use as [[presentable (infinity,1)-category|presentations]] of $(\infty,1)$-[[(infinity,1)-category|categories]] see Appendix A.2 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_


[[!redirects model categories]]
[[!redirects model structure]]
[[!redirects model structures]]
[[!redirects Quillen model category]]
[[!redirects closed model category]]
[[!redirects closed Quillen model category]]
[[!redirects Quillen model categories]]
[[!redirects closed model categories]]
[[!redirects closed Quillen model categories]]
