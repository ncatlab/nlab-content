
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea 
 {#Idea}

In generality, _homotopy theory_ is the study of mathematical contexts in which [[function|functions]] or rather ([[homomorphism|homo]]-)[[morphism|morphisms]] are equipped with a concept of _[[homotopy]]_ between them, hence with a concept of "equivalent [[deformations]]" of morphisms, and then iteratively with [[homotopies of homotopies]] between those, and so forth. 

For exposition see _[[Introduction to Topology -- 2|Introduction to Basic Homotopy Theory]]_, _[[Introduction to Homotopy Theory]]_, and _[[geometry of physics -- homotopy types]]_.

A key aspect is that in such homotopy theoretic contexts the concept of _[[isomorphism]]_ is relaxed to that of _[[homotopy equivalence]]_: Where a [[morphism]] is regarded as [[inverse morphism|invertible]] if there is a reverse function such that both [[composition|composites]] are _[[equality|equal]]_ to the [[identity morphism]], for a [[homotopy equivalence]] one only requires the composites to be [[homotopy|homotopic]] to the identity. Regarding objects in a homotopical context up to [[homotopy equivalence]] this way is to regard them as _[[homotopy types]]_. 

The classical example is the [[classical model structure on topological spaces|classical homotopy theory of topological spaces]], where one considers [[topological spaces]] with [[continuous functions]] between them, and with the original concept of [topological homotopies](Introduction+to+Topology#LeftHomotopy) between these continuous functions. The [[category]] whose [[objects]] are [[topological spaces]] and whose [[morphisms]] are [[homotopy equivalence]]-[[equivalence classes|class]] of [[continuous functions]] is also called the _[[classical homotopy category]]_. 
 
The [[classical model structure on topological spaces|classical homotopy theory of topological spaces]] has many applications, for example to _[[covering space]] theory_, to _[[classifying space]] theory_, to _[[generalized (Eilenberg-Steenrod) cohomology theory]]_ and many more. (See also at _[[shape theory]]_.) Accordingly, homotopy theory has a large overlap with _[[algebraic topology]]_.

The [[classical model structure on topological spaces|classical homotopy theory of topological spaces]] may be abstracted to yield an "abstract homotopy theory" that applies to a large variety of contexts. There are several more or less equivalent formalizations of the concept of "abstract homotopy theory", including

* _[[model categories]]_ 

* _[[(∞,1)-categories]]_

* _[[homotopy type theory|homotopy type theories]]_.

The terminology _[[model category]]_ is short for "category of models of homotopy types". The idea here is to consider [[categories]] equipped with suitable [[stuff, structure, property|extra structure and properties]] that encodes the existence of [[homotopies]] between all [[morphisms]] and convenient means to handle and control these, in particular a means to construct the corresonding [[homotopy category]].

For a detailed introduction to homotopy theory from this perspective see at _[[Introduction to Homotopy Theory]]_. 

The approach of [[(∞,1)-categories]] to homotopy theory is meant to be more truthful to the intrinsic nature of homotopy theory. Instead of equipping an ordinary category with a extra concept of homotopy between its morphisms, here one regards the resulting structure as a [[higher category]] where the [[homotopies]] themselves appear as a kind of higher order morphisms, called _[[2-morphisms]]_ and where higher [[homotopies of homotopies]] are regarded as _[[k-morphisms]]_ for all $k$.

The terminology "[[(∞,1)-category]]" signifies that homotopy theory is but one special case of general [[higher category theory]], namely [[(∞,1)-categories]] (hence homotopy theories) are those [[infinity-categories]] in which all [[k-morphisms]] for $k \gt 1$ are [[invertible morphisms|invertible]] up to [[homotopy]]. If one drops this constraint, so that homotopies become "directed" then one might still speak of "[[directed homotopy theory]]".


The archetypical example of an [[(∞,1)-category]] is the $(\infty,1)$-category _[[∞Grpd]]_ of [[∞-groupoids]], just as [[Set]] is the archetypical 1-[[category]].

This turns out to be equivalent, as homotopy theories, to the [[classical model structure on topological spaces|classical homotopy theory of topological spaces]] if restricted to those that admit the structure of [[CW-complexes]]. Another homotopy theory equivalent to this archetypical one is the [[classical model structure on simplicial sets|classical homotopy theory of simplicial sets]], see also at _[[simplicial homotopy theory]]_.

But there are many other homotopy theories besides (the various incarnations of) this classical one. Important sub-classes of homotopy theories include 

* _[[stable homotopy theory]]_ modeled by [[stable model categories]] and [[stable (∞,1)-categories]], where the operations of [[looping and delooping]] are an [[equivalence of (∞,1)-categories|equivalence]]. This includes the [[stable (∞,1)-category of spectra]] as well as those of [[sheaves of spectra]].

* _[[geometric homotopy theory]]_ modeld by [[model toposes]] and [[(∞,1)-toposes]], which are the homotopy theoretic analogs of ordinary [[toposes]]. This includes the  homotopy theoretic analog of [[categories of sheaves]], called _[[(∞,1)-categories of (∞,1)-sheaves]]_ or _of [[∞-stacks]]_, but it potentially also contains "[[elementary (∞,1)-toposes]]".
 
The [[geometric homotopy theory]] of [[(∞,1)-toposes]] in particular serves as the foundation for [[higher geometry]]/[[derived geometry]]. This is relevant notably in the [[physics]] of [[gauge theory]], where [[gauge transformations]] are identified with [[homotopies]] in [[geometric homotopy theory]]. For more on this see at _[[geometry of physics -- homotopy types]]_.

On the other hand, the incarnation of homotopy theory as _[[homotopy type theory]]_ exhibits the remarkably [[foundation|foundational]] nature of homotopy theory. Contrary to its original appearance as a fairly complicated-looking theory built on top of classical [[set theory]] and classcal [[topology]], homotopy theory turns out to be intrinsically simple: it arises from plain [[dependent type theory]] just by adopting a fully [[constructive mathematics|constructive]] attitude towards the concept of [[identity]]/[[equality]], see at _[[identity type]]_ for more on this. For exposition of this perspective see ([Shulman 17](#Shulman17)).



## Presentations ##

A convenient, powerful, and traditional way to deal with [[(∞,1)-categories]] is to "present" them by 1-categories with specified classes of morphisms called _[[weak equivalence|weak equivalences]]_ : a [[category with weak equivalences]] or [[homotopical category]].  The idea is as follows.  Given a category $C$ with a class $W$ of weak equivalences, we can form its **[[homotopy category]]** or **[[calculus of fractions|category of fractions]]** $C[W^{-1}]$ by adjoining formal inverses to all the morphisms in $W$.  The [[simplicial localization|(∞,1)-category presented by]] $(C,W)$" can be thought of as the result of regarding $C$ as an $\infty$-category with only identity $k$-cells for $k\gt 1$, then adjoining formal inverses to morphisms in $W$ in the $\infty$-categorical sense; that is, making them into [[equivalence|equivalences]] rather than isomorphisms.  It is remarkable that most $(\infty,1)$-categories that arise in mathematics can be presented in this way.

As with presentations of [[group]]s and other algebraic structures, very different presentations can give rise to equivalent $(\infty,1)$-categories.  For example, several different presentations of the $(\infty,1)$-category of $\infty$-groupoids are:

 * $C=$ [[CW-complex]]es, $W=$ [[homotopy equivalence]]s - see _[[Quillen model structure on topological spaces]]_
 * $C=$ [[topological space]]s, $W=$ [[weak homotopy equivalences]]
 * $C=$ [[Kan complex]]es, $W=$ simplicial homotopy equivalences
 * $C=$ [[simplicial set]]s, $W=$ weak homotopy equivalences - see _[[Quillen model structure on simplicial sets]]_
 * $C=$ [[small category|small categories]], $W=$ functors whose nerves are weak homotopy equivalences -- see _[[Thomason model structure]]_.


The latter three can hence be regarded as providing "combinatorial models" for the homotopy theory of topological spaces.

### Model Categories 

The value of working with presentations of $(\infty,1)$-categories rather than the $(\infty,1)$-categories themselves is that the presentations are ordinary 1-categories, and thus much simpler to work with.  For instance, ordinary limits and colimits are easy to construct in the category of topological spaces, or of simplicial sets, and we can then use these to get a handle on $(\infty,1)$-categorical limits and colimits in the $(\infty,1)$-category of $\infty$-groupoids.  However, we always have to make sure that we use only 1-categorical constructions that are _homotopically meaningful_, which essentially means that they induce $(\infty,1)$-categorical meaningful constructions in the presented $(\infty,1)$-category.  In particular, they must be invariant under weak equivalence.

Most presentations of $(\infty,1)$-categories come with additional classes of morphisms, called _fibrations_ and _cofibrations_, that are very useful in performing constructions in a homotopically meaningful way.  Quillen defined a [[model category]] to be a 1-category together with classes of morphisms called weak equivalences, cofibrations, and fibrations that fit together in a very precise way (the term is meant to suggest "a category of models for a homotopy theory").  Many, perhaps most, presentations of $(\infty,1)$-categories are model categories.  Moreover, even when we do not have a model category, we often have classes of cofibrations and fibrations with many of the properties possessed by cofibrations and fibrations in a model category, and even when we do have a model category, there may be classes of cofibrations and fibrations, different from those in the model structure, that are useful for some purposes.

Unlike the weak equivalences, which determine the "homotopy theory" and the $(\infty,1)$-category that it presents, fibrations and cofibrations should be regarded as _technical tools_ which make working directly with the presentation easier (or possible).  Whether a morphism is a fibration or cofibration has no meaning after we pass to the presented $(\infty,1)$-category.  In fact, _every_ morphism is weakly equivalent to a fibration and to a cofibration.  In particular, despite the common use of double-headed arrows for fibrations and hooked arrows for cofibrations, they do not correspond to $(\infty,1)$-categorical epimorphisms and monomorphisms.

In a model category, a morphism which is both a fibration and a weak equivalence is called an **acyclic fibration** or a **trivial fibration**.  Dually we have **acyclic** or **trivial cofibrations**. An object $X$ is called **cofibrant** if the map $0\to X$ from the initial object to $X$ is a cofibration, and **fibrant** if the map $X\to 1$ to the terminal# object is a fibration.  The axioms of a model category ensure that for every object $X$ there is an acyclic fibration $Q X \to X$ where $Q X$ is cofibrant and an acyclic cofibration $X\to R X$ where $R X$ is fibrant.

### Examples 


* [[topological homotopy theory]], [[classical model structure on topological spaces]],

* [[simplicial homotopy theory]], [[classical model structure on simplicial sets]]


* [[localic homotopy theory]]

For a (higher) category theorist, the following examples of model categories are perhaps the most useful to keep in mind:

 * $C=$ sets, $W=$ isomorphisms.  _All_ morphisms are both fibrations and cofibrations.  The $(\infty,1)$-category presented is again the 1-category $Set$.
 * $C=$ categories, $W=$ equivalences of categories.  The cofibrations are the functors which are injective on objects, and the fibrations are the [[isofibration|isofibrations]].  The acyclic fibrations are the equivalences of categories which are literally surjective on objects.  Every object is both fibrant and cofibrant.  The $(\infty,1)$-category presented is the 2-category $Cat$.  This is often called the _folk model structure_.
 * $C=$ (strict) 2-categories and (strict) 2-functors, $W=$ 2-functors which are [[equivalence of categories|equivalences of bicategories]].  The fibrations are the 2-functors which are isofibrations on hom-categories and have an equivalence-lifting property.  Every object is fibrant; the cofibrant 2-categories are those whose underlying 1-category is freely generated by some directed graph.  The $(\infty,1)$-category presented is the (weak) 3-category $2Cat$.  This model structure is due to Steve Lack.

### Generalized Morphisms 

The morphisms from $A$ to $B$ in the $(\infty,1)$-category presented by $(C,W)$ are zigzags
$
  \stackrel{\simeq}{\leftarrow}
  \to
  \stackrel{\simeq}{\leftarrow}
  \to
  \cdots
$; these are sometimes called **generalized morphisms**.  Many presentations (including every model category) have the property that any such morphism is equivalent to one with a single zag, as in $\stackrel{\simeq}{\leftarrow} \to \stackrel{\simeq}{\leftarrow}$.  In a model category,  a canonical form for such a zigzag is
$X \stackrel{\simeq}{\leftarrow} Q X \to  R Y \stackrel{\simeq}{\leftarrow} Y$
where $Q X$ is cofibrant and $R Y$ is fibrant.  In this case we can moreover take $Q X\to X$ to be an acyclic fibration and $Y\to R Y$ to be an acyclic cofibration.

Often it suffices to consider even shorter zigzags of the form $\stackrel{\simeq}{\leftarrow} \to$ or $\to \stackrel{\simeq}{\leftarrow}$.  In particular, this is the case if every object is fibrant or every object is cofibrant.  For example:

 * If $X$ and $Y$ are strict 2-categories, then pseudofunctors $X\to Y$ are equivalent to strict 2-functors $Q X \to Y$, where $Q X$ is a cofibrant replacement for $X$.
 * [[anafunctor|anafunctors]] are zigzags $\stackrel{\simeq}{\leftarrow} \to$ in the [[folk model structure]] on 1-categories whose first factor is an acyclic (i.e. surjective) fibration.  
 * [[Morita equivalence|Morita morphisms]] in the theory of [[Lie groupoid|Lie groupoids]] are generalized morphisms of length one where both maps are acyclic fibrations.

If $X$ is cofibrant and $Y$ is fibrant, then every generalized morphism from $X$ to $Y$ is equivalent to an ordinary morphism.  For example, if $X$ is a cofibrant 2-category, then every pseudofunctor $X\to Y$ is equivalent to a strict 2-functor $X\to Y$

### Quillen Equivalences 

Quillen also introduced a highly structured notion of equivalence between model categories, now called a [[Quillen equivalence]], which among other things ensures that they present the same $(\infty,1)$-category.  Quillen equivalences are now being used to compare different definitions of higher categories.

## Related concepts 

* [[synthetic homotopy theory]]

* [[simplicial homotopy theory]]

* [[stable homotopy theory]]

* [[parameterized homotopy theory]]

* [[equivariant homotopy theory]], [[global equivariant homotopy theory]]

* [[chromatic homotopy theory]]

* [[p-adic homotopy theory]]

* [[algebraic homotopy]]: In his talk at the 1950 ICM in Harvard, [[Henry Whitehead]] introduced the idea of [[algebraic homotopy]] theory and said

_"The ultimate aim of algebraic homotopy is to construct a purely
  algebraic theory, which is equivalent to homotopy theory in the same sort of 
  way that 'analytic' is equivalent to 'pure' projective geometry."_

This theme was taken up  by Baues, (1988), using a type of abstract homotopy theory closely related to Ken Brown's [[category of fibrant objects|categories of fibrant objects]].  Whitehead's own work was extended by Ronnie Brown and Phil Higgins, see [[nonabelian algebraic topology]].

*  [[homotopy type theory]]: A formalization of homotopy theory in terms of [[Martin-Löf dependent type theory]] is _[[homotopy type theory]]_.

* [[higher structures]]

## Related entries ##

* [[homotopy theory FAQ]]

* [[algebraic homotopy]]

* [[proper homotopy theory]]

* [[category of fibrant objects]]
* [[category with weak equivalences]]
* [[closed monoidal deformation retract]]
* [[closed monoidal homotopical category]]
* [[cylinder functor]], [[cocylinder]]
* [[derived functor]]
* [[deformation retract of a homotopical category]], [[neighborhood retract]]
* [[Dold fibration]]
* [[equivalence]]
* [[folk model structure]]
* [[fundamental groupoid]]
* [[homological resolution]]
* [[homotopical category]]
* [[homotopical cohomology theory]]
* [[homotopy]], [[homotopy group]]
* [[homotopy category]]
* [[homotopy limit]], [[homotopy colimit]]
* [[homotopy coherent category theory]]
* [[Hurewicz fibration]], [[Hurewicz connection]], [[Hurewicz cofibration]]
* [[interval object]]
* [[model category]]
* [[model structure on crossed complexes]]
* [[model structure on simplicial sets]], [[model structure on dendroidal sets]]
* [[path object]], [[path groupoid]], [[path n-groupoid]]

* [[rational homotopy theory]], [[p-adic homotopy theory]]

* [[test category]]
* [[topology]]
* [[weak equivalence]]

## References 
 {#References}

An exposition with an eye towards [[homotopy type theory]] is in 

* {#Shulman17} [[Mike Shulman]], _The logic of space_, chapter in [[Gabriel Catren]], [[Mathieu Anel]] (eds.), _[[New Spaces for Mathematics and Physics]]_ ([arXiv:1703.03007](https://arxiv.org/abs/1703.03007))

Lecture notes:

* [[Urs Schreiber]], _[[Introduction to Homotopy Theory]]_ (2016)

* {#Martins20} [[Yuri Ximenes Martins]], _Introduction to Abstract Homotopy Theory_ ([arXiv:2008.05302](https://arxiv.org/abs/2008.05302))


Survey

* [[Klaus Heiner Kamps]], [[Tim Porter]], _Abstract Homotopy and Simple Homotopy Theory_, World Scientific 1997 ([doi:10.1142/2215](https://doi.org/10.1142/2215), [GoogleBooks](http://books.google.de/books?id=7JYKxInRMdAC&dq=Porter+Kamps&printsec=frontcover&source=bl&ots=uuyl_tIjs4&sig=Lt8I92xQBZ4DNKVXD0x76WkcxCE&hl=de&sa=X&oi=book_result&resnum=3&ct=result#PPP1,M1))


* {#MunsonVolic15} [[Brian Munson]], [[Ismar Volic]], _Cubical homotopy theory_, Cambridge University Press, 2015  ([pdf](http://palmer.wellesley.edu/~ivolic/pdf/Papers/CubicalHomotopyTheory.pdf), [doi:10.1017/CBO9781139343329](https://doi.org/10.1017/CBO9781139343329))

  (with emphasis on [[cubical objects]] such as in [[n-excisive functors]] and [[Goodwillie calculus]])


* [[Haynes Miller]] (ed.), _[[Handbook of Homotopy Theory]]_, 2019

The original axiomatization of homotopy theory by [[model categories]] is due to

* {#Quillen67} [[Daniel Quillen]], _Homotopical algebra_, Lecture Notes in Mathematics 43, Berlin, New York, 1967

The similar axiomatization involving the weaker structure of a [[calculus of fractions]] is due to

* [[Pierre Gabriel]], [[Michel Zisman]], _[[Calculus of fractions and homotopy theory]]_, _Ergebnisse der Mathematik und ihrer Grenzgebiete_, Band 35. Springer, New York (1967) 

A standard account of the modern form of [[simplicial homotopy theory]] is in

* [[Paul Goerss]], [[Rick Jardine]], _[[Simplicial homotopy theory]]_, Progress in Mathematics, Birkh&#228;user (1996)

Formulation of abstract homotopy theory as the theory of [[(∞,1)-toposes]] is due to 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

and the formalization of this in the [[internal logic|internal language]] of [[homotopy type theory]] is due to

* Univalent Foundations Project, _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_ (2013)

A foundational set of lecture notes is developing in 

* [[Denis-Charles Cisinski]], _Higher category theory and homotopical algebra_ ([pdf](http://www.mathematik.uni-regensburg.de/cisinski/CatLR.pdf))


See also:

* H. J. Baues, _Homotopy types_, in  _Handbook of Algebraic Topology_, (edited by I.M. James), North Holland, 1995.

* Jasper Moller, _Homotopy theory for beginners_ ([pdf](http://www.math.ku.dk/~moller/e01/algtopI/comments.pdf))

* [[Zhen Lin Low]], _[[Notes on homotopical algebra]]_

* {#Riehl14} [[Emily Riehl]], _[[Categorical Homotopy Theory]]_, Cambridge University Press, 2014 ([pdf](http://www.math.jhu.edu/~eriehl/cathtpy.pdf), [doi:10.1017/CBO9781107261457](https://doi.org/10.1017/CBO9781107261457))

* [[William Dwyer]], _Homotopy theory and classifying spaces_, Copenhagen, June 2008 ([pdf](http://www.math.ku.dk/~jg/homotopical2008/Dwyer.CopenhagenNotes.pdf))

* [[William Dwyer]], [[Philip Hirschhorn]], [[Daniel Kan]], [[Jeff Smith]], _Homotopy Limit Functors on Model Categories and Homotopical Categories_, volume 113 of _Mathematical Surveys and Monographs_, American Mathematical Society (2004) (there exists [this](http://dodo.pdmi.ras.ru/~topology/books/dhks.pdf) pdf copy of what seems to be a preliminary version of this book)

From [[category theory]] to [[homotopy theory]]:

* [[Emily Riehl]], _[[Categorical Homotopy Theory]]_, Cambridge University Press, 2014 ([pdf](http://www.math.jhu.edu/~eriehl/cathtpy.pdf), [doi:10.1017/CBO9781107261457](https://doi.org/10.1017/CBO9781107261457))

* {#Richter19} [[Birgit Richter]], _From categories to homotopy theory_, Cambridge Studies in Advanced Mathematics 188, Cambridge University Press 2020 ([doi:10.1017/9781108855891](https://doi.org/10.1017/9781108855891), [book webpage](https://www.math.uni-hamburg.de/home/richter/catbook.html), [pdf](https://www.math.uni-hamburg.de/home/richter/bookdraft.pdf))

* [[Urs Schreiber]], _[[geometry of physics -- categories and toposes]]_


Brief indications of open questions and future directions (as of 2013) of [[algebraic topology]] and [[stable homotopy theory]] are in 

* [[Tyler Lawson]], _The future_, Talbot lectures 2013 ([pdf](http://math.mit.edu/conferences/talbot/2013/19-Lawson-thefuture.pdf))

and in

* {#ProblemsInHomotopyTheoryWiki} _Problems in homotopy theory_ ([wiki](http://topology-octopus.herokuapp.com/problemsinhomotopytheory/show/HomePage))
 
More regarding the sociology of the field (such as its [[folklore]] results):

* {#Barwick17} [[Clark Barwick]], _The future of homotopy theory_, 2017 ([pdf](http://www.maths.ed.ac.uk/~cbarwick/papers/future.pdf), [[BarwickFutureOfHomotopyTheory.pdf:file]])


[[!redirects Homotopy Theory]]
[[!redirects homotopy theories]]
