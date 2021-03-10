
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
* table of contents
{:toc}


## Idea

A __model category__ (sometimes called a _Quillen model category_ or a _closed model category_, but **not** related to "[[closed category]]") is a context for doing [[homotopy theory]].    Quillen developed the definition of a model category to formalize the similarities between [[homotopy theory]] and [[homological algebra]]: the key examples which motivated his definition were the category of [[topological space|topological spaces]], the category of [[simplicial set|simplicial sets]], and the category of [[chain complex|chain complexes]].

So, what is a model category?  For starters, it is a [[category]] equipped with three [[classes]] of [[morphisms]], each closed under [[composition]] and  called _[[weak equivalences]]_, _[[fibrations]]_ and _[[cofibrations]]_:

* The weak equivalences play the role of '[[homotopy equivalences]]' or something a bit more general (such as [[weak homotopy equivalences]]).  Already in the case of [[topological spaces]], it is useful to say that two spaces have the same [[homotopy type]] if there is a map from one to the other that induces [[isomorphisms]] on [[homotopy groups]] for any choice of basepoint in the first space.  These maps are more general than homotopy equivalences, so they are called 'weak equivalences'.

* The [[fibrations]] play the role of 'nice surjections'.  For example, in the category [[Top]] of [[topological spaces]] with its usual [[Quillen model structure on topological spaces]], a locally trivial [[fiber bundle]] is a fibration. More generally the fibrations here are the [[Serre fibrations]].

* The [[cofibrations]] play the role of 'nice inclusions'.  For example, in the category [[Top]] of [[topological spaces]] with its usual [[model structure on topological spaces]], an [[NDR pair]] is typically a cofibration.  

A bit more technically: we can define an [[(∞,1)-category]] starting from any [[category with weak equivalences]].  The idea is that this (∞,1)-category keeps track of [[objects]] in our original category, [[morphisms]] between objects, [[homotopies]] between morphisms, homotopies between homotopies, and so on, _ad infinitum_.  However, the extra structure of a model category makes it easier to work with this (∞,1)-category.  We can obtain this (∞,1)-category in various ways, such as [[simplicial localization]] of the underlying [[category with weak equivalences]], or (if the model category is simplical) the [[homotopy coherent nerve]] of the [[simplicially enriched category|simplicial subcategory]] $M_{cf}\subset M$ of cofibrant-fibrant objects. We say this [[(∞,1)-category]] is _presented_ (or modeled) by the model category, and that the objects of the model category are _models_ for the objects of this $(\infty,1)$-category. Not every (∞,1)-category is obtained in this way (otherways it would necessarily have all small [[homotopy limits]] and [[homotopy colimits]]).

In this sense model categories are 'models for [[homotopy theory]]' or 'categories of models for homotopy theory'.  (The latter sense was the one intended by Quillen, but the former is also a useful way to think.)

Recall that the idea of [[category with weak equivalences|categories with weak equivalences]] is to work just with 1-morphisms instead of with [[n-morphisms]] for all $n$, but to carry around extra information to remember which 1-morphisms are really [[equivalence|equivalences]] in the full [[(∞,1)-category]], i.e. [[isomorphisms]] in the corresponding [[homotopy category]].

In a model category the data of weak equivalences is accompanied by further auxiliary data that helps to compute the [[(∞,1)-categorical hom-space]], the [[homotopy category]] and [[derived functor|derived functors]]. See [[homotopy category of a model category]] for more on that.

If the model category happens to be a [[combinatorial simplicial model category]] $\mathbf{A}$ it [[presentable (infinity,1)-category|presents]] the [[(infinity,1)-category|category]] $\mathbf{A}^\circ$ in the form of a [[simplicially enriched category]] given by the full [[SSet]]-[[enriched category|enriched subcategory]] on objects that are both fibrant and cofibrant.



## Definition

The following is a somewhat terse account. For a more detailed exposition see  at _[[Introduction to Homotopy Theory]]_ the section _[Abstract homotopy theory](Introduction+to+Homotopy+Theory#ModelCategoryTheory)_.

<br>


+-- {: .num_defn #ModelStructure}
###### Definition

A **model structure** on a [[category]] $\mathcal{C}$ is a choice of three distinguished [[classes]] of [[morphisms]]

* _cofibrations_ $Cof \subset Mor(\mathcal{C})$, 

* _fibrations_ $Fib \subset Mor(\mathcal{C})$, 

* _weak equivalences_ $W \subset Mor(\mathcal{C})$ 

satisfying the following conditions:

1.  $W$ makes $\mathcal{C}$ into a [[category with weak equivalences]], 

    (meaning that it contains all [[isomorphisms]] and is closed under **[[two-out-of-three]]**: given a composable pair of morphisms $f,g$, if two out of the three morphisms $f, g, g f$ are in $W$, so is the third);

1. $(Cof, Fib \cap W)$ and $(Cof \cap W, Fib)$ are two [[weak factorization systems]] on $\mathcal{C}$.

=--

+-- {: .num_defn #ModelCategory}
###### Definition

A **model category** is a [[complete category|complete]] and [[cocomplete category]] $\mathcal{C}$ equipped with a model structure according to def. \ref{ModelStructure}.

=--

This equivalent version of the definition was observed in ([Joyal, def. E.1.2](#Joyal)), highlighted in ([Riehl 09](#Riehl09)). This definition already implies all the closure conditions on classes of morphisms which other definitions in the literature explicitly ask for, see [below](#ClosureOfMorphisms).

+-- {: .num_defn }
###### Definition
**(terminology)**

* The morphisms in $W \cap Fib$ (the fibrations that are also weak equivalences) are called **trivial fibrations** or **[[acyclic fibrations]]** 

* The morphisms in $W \cap Cof$ (the cofibrations that are also weak equivalences) are called **trivial cofibrations** or **[[acyclic cofibrations]]**. 

* An object is called **[[cofibrant]]** if the unique morphism $\emptyset \to X$ from the [[initial object]] is a cofibration

* An object is called **[[fibrant]]** if the unique morphism $X\to *$ to the [[terminal object]] is a fibration.  

=--

+-- {: .num_remark }
###### Remark

Often, the fibrant and cofibrant objects are the ones one is "really" interested in, but the category consisting only of these is not well-behaved (as a 1-category).  The factorizations supply fibrant and cofibrant replacement functors which allow us to treat any object of the model category as a 'model' for its fibrant-cofibrant replacement.

=--

## Variants 

### Slight variations on the axioms

Quillen's original definition required only [[finite limits]] and [[finite colimits]], which are enough for the basic constructions.  Colimits of larger cardinality are sometimes required for the [[small object argument]], however.
This change was popularized by [[Dwyer]], [[Hirschhorn]], [[Kan]], and [[Jeff Smith|Smith]]
in their book [[Homotopy Limit Functors on Model Categories and Homotopical Categories]]

[[Robert W. Thomason]] proposed to require that the factorizations given by (ii) are actually _[[functorial factorization systems]]_,
resulting in the notion of a [[Thomason model category]].
[[Mark Hovey]] later included the data of such a functorial factorization
(and not just its existence) into his definition of a model category.
In practice, Quillen's [[small object argument]] means that many model categories can be made to have functorial factorizations.  (But not all: an example of a model category with non-functorial factorizations can be found in [Isaksen 2001](https://arxiv.org/abs/math/0106152).)

### Enhancements of the axioms

There are several extra conditions that strengthen the notion of a model category:

* A [[monoidal model category]] is [[monoidal category]] that is also a model category in a compatible way.

* An [[enriched model category]] is an [[enriched category]] over a monoidal category, that is also a model category in a compatible way.

* An [[algebraic model category]] is one where the two defining [[weak factorization systems]] are refined to [[algebraic weak factorization systems]].

* A [[cofibrantly generated model category]] is one with a good compatible notion of [[cell complexes]].

* A [[combinatorial model category]] is a cofibrantly generated one that in addition is a [[locally presentable category]].

* An [[accessible model category]] is one on a locally presentable category that admits [[accessible functor|accessible]] factorizations, which can therefore be enhanced to [[algebraic weak factorization systems]].

* A left/right [[proper model category]] is one where the weak equivalences are stable under pushforward along cofibrations / pullback along fibrations

### Weaker axiom systems

There are several notions of [[category with weak equivalences]] with similar but less structure than a full model category.

* A [[category of fibrant objects]] has a notion of just weak equivalences and fibrations, none of cofibrations.  As the name implies, all of its objects are fibrant; the canonical example is the subcategory of fibrant objects in a model category.

* A [[Waldhausen category]] dually has a notion of weak equivalences and cofibrations, and all of its objects are cofibrant.

* There is also a slight variant of the full notion of model category by Thomason that is designed to make the [[global model structure on functors]] more naturally accessible: this is the notion of [[Thomason model category]].

* [[Semimodel categories]] relax some of the conditions on lifting properties.

* [[Weak model categories]] relax these conditions even further.

* [[Premodel categories]] are an even weaker notion that allows
for a nice [[2-categorical]] treatment.


## Properties

### Closure of morphism classes under retracts
 {#ClosureOfMorphisms}

As a consequence of the definition, the classes $Cof, Fib$,  and $W$ are all closed under [[retracts]] in the [[arrow category]] $Arr C$ and under composition and contain the [[isomorphisms]] of $C$. 

For $Cof$ and $Fib$ and $W \cap Cof$ and $W \cap Fib$ this and further closure properties are discussed in detail at _[[weak factorization system]]_ in the section _[Closure properties](https://ncatlab.org/nlab/show/weak+factorization+system#ClosureProperties)_.

In the presence of [[functorial factorizations]], it follows immediately that also $W$ is closed under retracts: for any retract diagram may then be funtorially factored with the middle morphism factored through $W \cap Cof$ followed by $W \cap Fib$, and so the statement follows from the above closure of these classes under retracts.

Without assuming functorial factorization the statement still holds:

+-- {: .num_prop #WeakEquivalencesAreClosedUnderRetracts}
###### Proposition

Given a model category in the sense of def. \ref{ModelCategory}, then its class of weak equivalences is closed under forming [[retracts]] (in the [[arrow category]]). 

=--

([Joyal, prop. E.1.3](#Joyal)), highlighted in ([Riehl 09](#Riehl09))


+-- {: .proof}
###### Proof

Let

$$
  \array{
    id \colon & A &\longrightarrow& X &\longrightarrow& A
    \\
    & 
    {}^{\mathllap{f}}
    \downarrow
      &&
    \downarrow^{\mathrlap{w}}
      &&
    \downarrow^{\mathrlap{f}}
    \\
    id \colon & B &\longrightarrow& Y &\longrightarrow& B
  }
$$

be a [[commuting diagram]] with $w \in W$ a weak equivalence. We need to show that then also $f \in W$.

First consider the case that $f \in Fib$. 

In this case, factor $w$ as a cofibration followed by an acyclic fibration. Since $w \in W$ and by [[two-out-of-three]] this is even a factorization through an acyclic cofibration followed by an acyclic fibration. Hence we obtain the commuting diagram

$$
  \array{
    id \colon 
    & 
    A 
      &\longrightarrow& 
    X 
      &\overset{\phantom{AAAA}}{\longrightarrow}& A
    \\
    & 
    {}^{\mathllap{id}}\downarrow
      &&
    \downarrow^{\mathrlap{\in W \cap Cof}}
      &&
    \downarrow^{\mathrlap{id}}
    \\
    id \colon
    & A' &\overset{s}{\longrightarrow}& 
     X' 
     &\overset{\phantom{AA}t\phantom{AA}}{\longrightarrow}& A'
    \\
    &
    {}^{\mathllap{f}}_{\mathllap{\in Fib}}
    \downarrow
      &&
    \downarrow^{\mathrlap{\in W \cap Fib}}
      &&
    \downarrow^{\mathrlap{f}}_{\mathrlap{\in Fib}}
    \\
    id \colon & B &\longrightarrow& Y &\underset{\phantom{AAAA}}{\longrightarrow}& B
  }
  \,,
$$

where $s$ is uniquely defined and where $t$ is any lift of the top middle vertical acyclic cofibration against $f$. This now exhibits $f$ as a retract of an acyclic fibration. These are closed under retract by [this prop.](weak+factorization+system#ClosuredPropertiesOfWeakFactorizationSystem).

Now consider the general case. Factor $f$ as an acyclic cofibration followed by a fibration and form the pushout in the top left square of the following diagram

$$
  \array{
    id \colon 
    & 
    A 
      &\longrightarrow& 
    X 
      &\overset{\phantom{AAAA}}{\longrightarrow}& A
    \\
    & 
    {}^{\mathllap{\in W \cap Cof}}\downarrow
      &(po)&
    \downarrow^{\mathrlap{\in W \cap Cof}}
      &&
    \downarrow^{\mathrlap{\in W \cap Cof}}
    \\
    id \colon
    & A' &\overset{}{\longrightarrow}& 
     X' 
     &\overset{\phantom{AA}\phantom{AA}}{\longrightarrow}& A'
    \\
    &
    {}^{\mathllap{\in Fib}}
    \downarrow
      &&
    \downarrow^{\mathrlap{\in W }}
      &&
    \downarrow^{\mathrlap{\in Fib}}
    \\
    id \colon & B &\longrightarrow& Y &\underset{\phantom{AAAA}}{\longrightarrow}& B
  }
  \,,
$$

where the other three squares are induced by the [[universal property]] of the pushout, as is the identification of the middle horizontal composite as the identity on $A'$. Since acyclic cofibrations are closed under forming pushouts by [this prop.](weak+factorization+system#ClosuredPropertiesOfWeakFactorizationSystem), the top middle vertical morphism is now an acyclic fibration, and hence by assumption and by [[two-out-of-three]] so is the middle bottom vertical morphism.

Thus the previous case now gives that the bottom left vertical morphism is a weak equivalence, and hence the total left vertical composite is.



=--

### Redundancy in the defining factorization systems
 {#RedundancyInTheAxioms}

It is clear that:

+-- {: .num_remark #AnyTwooClassesDetermineTheThird}
###### Remark

Given a model category structure, any two of the three classes of special morphisms (cofibrations, fibrations, weak equivalences) determine the third:

* given $W$ and $C$, we have $F = RLP(W \cap C)$;

* given $W$ and $F$, we have $C = LLP(W \cap F)$;

* given $C$ and $F$, we find $W$ as the class of morphisms which factor into a morphism in $LLP(F)$ followed by a morphism in $RLP(C)$.

(Here $RLP(S)$ denotes the class of morphisms with the [[right lifting property]] against $S$ and $LLP(S)$ denotes the class of morphisms with the [[left lifting property]] against $S$.)

=--

But, in fact, already the cofibrations and the fibrant objects determine the model structure.

+-- {: .num_prop}
###### Proposition

A model structure $(C,W,F)$ on a category $\mathcal{C}$ is determined by its class of cofibrations and its class of fibrant objects.

=--

This statement appears for instance as ([Joyal, prop. E.1.10](#Joyal))

+-- {: .proof}
###### Proof

Let $\mathcal{E}$ with $C,F,W \subset Mor(\mathcal{E})$ be a model category.

By remark \ref{AnyTwooClassesDetermineTheThird} it is sufficient to show that the cofibrations and the fibrant objects determine the class of weak equivalences. Moreover, these are already determined by the weak equivalences between cofibrant objects, because for $u : A \to B$ any morphism, [[functorial factorization|functorial]] cofibrant replacement $\emptyset \hookrightarrow \hat A \stackrel{\simeq}{\to} A$ and $\emptyset \hookrightarrow \hat B \stackrel{\simeq}{\to} B$ with 2-out-of-3 implies that $u$ is a weak equivalence precisely if $\hat u : \hat A \to \hat B $ is.

By the nature of the [[homotopy category]] $Ho$ of $\mathcal{E}$ and by the [[Yoneda lemma]], a morphism $\hat u : \hat A \to \hat B$ between cofibrant objects is a weak equivalence precisely if for every fibrant object $X$ the map

$$
  Ho(\hat u, X) : Ho(\hat B, X) \to Ho(\hat A, X)
$$

is an [[isomorphism]], namely a [[bijection]] of sets. The [[equivalence relation]] that defines $Ho(\hat A,X)$ may be taken to be given by [[left homotopy]] induced by [[cylinder objects]], which in turn are obtained by factoring [[codiagonals]] into cofibrations followed by acyclic fibrations. So all this is determined already by the class of cofibrations, and hence weak equivalences are determined by the cofibrations and the fibrant objects.

=--

### Opposite model structure

+-- {: .num_prop}
###### Proposition

If a category $C$ carries a model category structure, then the [[opposite category]] $C^{op}$ carries the [[opposite model structure]]: 

its weak equivalences are those morphisms whose dual was a weak equivalence in $C$, its fibrations are those morphisms that were cofibrations in $C$ and similarly for its cofibrations.

=--

### Homotopy and Homotopy category

See at 

* [[homotopy in a model category]]

* [[homotopy category of a model category]]

## Examples

Every category with limits and colimits carries the [[trivial model structure]] whose weak equivalences are the [[isomorphism]]s and all morphisms are cofibrations and fibrations.

### Classical model structures

The archetypical model structures are the

* [[classical model structure on topological spaces]] 

and the

*  [[classical model structure on simplicial sets]].

These model categories are [[Quillen equivalence|Quillen equivalent]] and encapsulate much of "classical" [[homotopy theory]].  From a higher-categorical viewpoint, they can be regarded as models for [[∞-groupoids]] (in terms of [[CW complexes]] or [[Kan complexes]], respectively).

The passage to [[stable homotopy theory]] is given by [[model structures on spectra]] built out of either of these two classical model structures. See at _[[Model categories of diagram spectra]]_ for a unified treatment.

Accordingly [[homological algebra]] with its [[derived categories]] and [[derived functors]] (which may be thought of as a sub-topic of [[stable homotopy theory]] via the [[stable Dold-Kan correspondence]]) is reflected by 

* [[model structures on chain complexes]] 

* [[model structures on dg-algebras]]

In fact, the original definition of model categories in \cite{Quillen1967} was motivated by the [[analogy]] between constructions in [[homotopy theory]] and [[homological algebra]].

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

There are related model structures for enriched higher categories:

* [[model structure on enriched categories]]
* [[model structure on dg-categories]]

Other "higher categorical structures" can also  be expected to form model categories, such as the 

* [[model structure on dendroidal sets]]

which generalizes the Joyal model structure from [[(∞,1)-categories]] to [[(∞,1)-operads]].

There is also another class of model structures on categorical structures, often called [[Thomason model structure]]s (not to be confused with the notion of "Thomason model category").  In the "categorical" or "canonical" model structures, the weak equivalences are the categorical [[equivalences]], but in the Thomason model structures, the weak equivalences are those that induce weak homotopy equivalences of [[nerves]].  Thomason model structures are known to exist on 1-categories and 2-categories, at least, and are generally [[Quillen equivalence|Quillen equivalent]] to the [[Quillen model structure on topological spaces]] and thus (via the [[singular simplicial complex]] and [[geometric realization]] [[adjunction]]) to the and [[Quillen model structure on simplicial sets]].

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

### Limit and colimit model structures

Model structures can be induced on certain (usually [[lax limit|lax]]) limits and colimits of diagrams of model categories.

* [[Grothendieck construction for model categories]] (lax colimits)
* [[model structure on sections]] (lax limit)

## Related concepts

* [[simplicial homotopy theory]]

* [[synthetic homotopy theory]]

* [[homotopy category of a model category]]

* [[localization of model categories]]

* [[double category of model categories]]

* [[Ho(CombModCat)]]

* [[premodel category]]

[[!include algebraic model structures - table]]

## References

The concept of a model category originates in Chapter I, _Axiomatic homotopy theory_, of

\bibitem{Quillen1967}


#### Monographs and textbooks

* [[Mark Hovey]], _[[Model Categories]]_, Mathematical Surveys and Monographs, Volume 63, AMS (1999) ([ISBN:978-0-8218-4361-1](https://bookstore.ams.org/surv-63-s),   [doi:10.1090/surv/063](https://doi.org/http://dx.doi.org/10.1090/surv/063), [pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/hovey-model-cats.pdf), [Google books](http://books.google.co.uk/books?id=Kfs4uuiTXN0C&printsec=frontcover))

* {#Hirschhorn02} [[Philip Hirschhorn]], _Model Categories and Their Localizations_, AMS Math. Survey and Monographs Vol 99 (2002) ([ISBN:978-0-8218-4917-0](https://bookstore.ams.org/surv-99-s/), [pdf toc](http://www.gbv.de/dms/goettingen/360115845.pdf), [pdf](http://www.maths.ed.ac.uk/~aar/papers/hirschhornloc.pdf))

* [[William G. Dwyer]], [[Philip S. Hirschhorn]], [[Daniel M. Kan]], [[Jeffrey H. Smith]], _Homotopy Limits Functors on Model Categories and Homotopical Categories_, [AMS](https://bookstore.ams.org/surv-113-s/), Mathematical Surveys and Monographs 113 (2004).

* [[J. Peter May]], [[Kate Ponto]], _[[More Concise Algebraic Topology]]_, The University of Chicago Press, 2012.  Part 4.

* [[Emily Riehl]], _[[Categorical Homotopy Theory]]_, Cambridge University Press, 2014.

#### Coverage table for major sources

|Topic                                      |Quillen|Hovey|Hirschhorn|DHKS|May-Ponto|Riehl|Lurie|
|-------------------------------------------|-------|-----|----------|----|---------|-----|-----|
|[[combinatorial model categories]]         |no     |no   |no        |no  |no*      |yes  |yes  |
|[[monoidal model categories]]              |no     |yes  |no        |no  |yes      |yes  |yes  |
|[[enriched model categories]]              |no     |no   |no        |no  |yes      |yes  |yes  |
|[[homotopy colimits]]                      |no     |no   |yes       |yes |no*      |yes  |yes  |
|[[Bousfield localizations]]                |no     |no   |yes       |no  |yes      |no   |yes  |
|[[transferred model structures]]           |yes    |no   |yes       |no  |no       |yes  |yes  |
|[[Reedy model structures]]                 |no     |yes  |yes       |yes |no       |yes  |yes  |

#### Book chapters

* {#GoerssJardine99} [[Paul Goerss]], [[Rick Jardine]], Chapters 1 and 2 of _[[Simplicial homotopy theory]]_, Birkhäuser, 1999, 2009.

For yet another introduction to model categories, with an eye towards their use as [[presentable (infinity,1)-category|presentations]] of $(\infty,1)$-[[(infinity,1)-category|categories]] see 

* [[Jacob Lurie]], Appendix A.2 and A.3 of _[[Higher Topos Theory]]_

#### Survey articles

* {#DwyerSpalinski95} [[William Dwyer]], J. Spalinski, _[[Homotopy theories and model categories]]_ ([pdf](http://folk.uio.no/paularne/SUPh05/DS.pdf)) in [[Ioan Mackenzie James]] (ed.), _[[Handbook of Algebraic Topology]]_ 1995

* [[Paul Goerss]], [[Kirsten Schemmerhorn]], _Model categories and simplicial methods_, Notes from lectures given at the University of Chicago, August 2004, in: _Interactions between Homotopy Theory and Algebra_, Contemporary Mathematics 436, AMS 2007([arXiv:math.AT/0609537](http://arxiv.org/abs/math.AT/0609537), [doi:10.1090/conm/436](http://dx.doi.org/10.1090/conm/436))



#### Other sources

An account is in

* [[joyalscatlab:HomePage|Joyal's CatLab]], _[[joyalscatlab:Model categories]]_

and appendix E of 

* {#Joyal} [[André Joyal]], _The theory of quasi-categories and its applications_ ([pdf](http://mat.uab.cat/~kock/crm/hocat/advanced-course/Quadern45-2.pdf), [[JoyalTheoryOfQuasicategories.pdf:file]])
 
The version of the definition in ([Joyal](#Joyal)) is also highlighted in

* {#Riehl09} [[Emily Riehl]], _A concise definition of model category_, 2009 ([pdf](http://www.math.jhu.edu/~eriehl/modelcat.pdf), [[RiehlConciseDefinitionOfModelCategory.pdf:file]])

An introductory survey of some key concepts is in the set of slides

* [[Peter May]], _[[ModelCatPrimer.pdf:file]]_

There is an unpublished manuscript of [[Chris Reedy]] from around 1974 that's been circulating as an increasingly faded photocopy. It's been typed into LaTeX, and the author has given  [permission](http://www-math.mit.edu/~psh/#Other%20mathematics) for it to be posted on the net:

* [[Chris Reedy]], _Homotopy theory of model categories_ ([pdf](http://www-math.mit.edu/~psh/reedy.pdf))


See 

* [[Philip Hirschhorn]], personal website: _[Mathematics](http://www-math.mit.edu/~psh/#Mathematics)_

for errata and more. 


[[!redirects model categories]]
[[!redirects model structure]]
[[!redirects model structures]]
[[!redirects model category structure]]
[[!redirects Quillen model structure]]
[[!redirects Quillen model structures]]
[[!redirects Quillen model category]]
[[!redirects closed model category]]
[[!redirects closed Quillen model category]]
[[!redirects Quillen model categories]]
[[!redirects closed model categories]]
[[!redirects closed Quillen model categories]]
