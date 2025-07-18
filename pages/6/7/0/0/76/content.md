
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


### General idea
 {#GeneralIdea}

In generality, _homotopy theory_ is the study of mathematical contexts in which [[function|functions]] or rather ([[homomorphism|homo]]-)[[morphism|morphisms]] are equipped with a concept of _[[homotopy]]_ between them, hence with a concept of "equivalent [[deformations]]" of morphisms, 

\begin{imagefromfile}
    "file_name": "2Cell.jpg",
    "width": 200,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 10,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


and then iteratively with [[homotopies of homotopies]] between those:


\begin{imagefromfile}
    "file_name": "3Cell.jpg",
    "width": 215,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 0,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

and so forth.



A key aspect here is that in such homotopy theoretic contexts the concept of _[[isomorphism]]_ is relaxed to that of _[[homotopy equivalence]]_: Where a [[morphism]] is regarded as [[inverse morphism|invertible]] if there is a reverse function such that both [[composition|composites]] are _[[equality|equal]]_ to the [[identity morphism]], for a [[homotopy equivalence]] one only requires the composites to be [[homotopy|homotopic]] to the identity. Regarding objects in a homotopical context up to [[homotopy equivalence]] this way is to regard them as _[[homotopy types]]_. 

It is not wrong to summarize this by saying that: 

> *Homotopy theory embodies the [[gauge principle]] in mathematics*.

Namely, in [[physics]], the [[gauge principle]] says that it is wrong to ask for any two [[field history|things]] to be [[equal]], instead one always has to ask whether there is a [[gauge transformation]] relating them, and then a [[gauge-of-gauge transformation]] relating these, etc. Similarly in homotopy theory it is wrong to ask whether any two objects are equal, instead one has to ask whether there is a [[homotopy equivalence]] between them and then [[higher homotopies]] between these, etc.

\linebreak

For more exposition on the general idea of homotopy theory see:

* *[[schreiber:Higher Structures]]*

\linebreak


### Topological homotopy theory
 {#TopologicalHomotopyTheoryInIdeaSection}

\begin{imagefromfile}
    "file_name": "AHomotopy.jpg",
    "float": "right",
    "width": 380,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

The archetypical example of a homotopy theory is the [[classical model structure on topological spaces|classical homotopy theory of topological spaces]], where one considers [[topological spaces]] with [[continuous functions]] between them, and with the original concept of [topological homotopies](Introduction+to+Topology+--+2#LeftHomotopy) between these continuous functions. 


The [[category]] whose [[objects]] are [[topological spaces]] and whose [[morphisms]] are [[homotopy equivalence]]-[[equivalence class|classes]] of [[continuous functions]] is also called the _[[classical homotopy category]]_. 
 
Classical constructions in topological homotopy theory are *[[homotopy groups]]*, *[[Toda brackets]]*, *[[long exact sequences of homotopy groups]]*, ...

This [[classical model structure on topological spaces|classical homotopy theory of topological spaces]] has many applications, for example to _[[covering space]] theory_, to _[[classifying space]] theory_, to _[[Whitehead-generalized cohomology theory]]_ and many more. (See also at _[[shape theory]]_.) Accordingly, homotopy theory has a large overlap with _[[algebraic topology]]_.


\linebreak

For more exposition of topological homotopy theory see:

* _[[Introduction to Topology -- 2|Introduction to Basic Homotopy Theory]]_




\linebreak

### Abstract homotopy theory

The basic structures seen in  [[classical model structure on topological spaces|classical homotopy theory of topological spaces]] may be abstracted to yield an "abstract homotopy theory" that applies to a large variety of contexts. There are several more or less equivalent formalizations of the concept of "abstract homotopy theory", including

* _[[model categories]]_ 

* _[[(∞,1)-categories]]_

* _[[homotopy type theory|homotopy type theories]]_.

* _[[higher observational type theories]]_.

The terminology _[[model category]]_ is short for "category of models of homotopy types". The idea here is to consider [[categories]] equipped with suitable [[stuff, structure, property|extra structure and properties]] that encodes the existence of [[homotopies]] between all [[morphisms]] and convenient means to handle and control these, in particular a means to construct the corresponding [[homotopy category]].


\linebreak

For a detailed introduction to abstract homotopy theory via model cateories see:

* _[[Introduction to Homotopy Theory]]_, 

* _[[geometry of physics -- homotopy types]]_.

\linebreak


The approach of [[(∞,1)-categories]] to homotopy theory is meant to be more truthful to the intrinsic nature of homotopy theory. Instead of equipping an ordinary category with a extra concept of homotopy between its morphisms, here one regards the resulting structure as a [[higher category]] where the [[homotopies]] themselves appear as a kind of higher order morphisms, called _[[2-morphisms]]_ and where higher [[homotopies of homotopies]] are regarded as _[[k-morphisms]]_ for all $k$.

The terminology "[[(∞,1)-category]]" signifies that homotopy theory is but one special case of general [[higher category theory]], namely [[(∞,1)-categories]] (hence homotopy theories) are those [[infinity-categories]] in which all [[k-morphisms]] for $k \gt 1$ are [[invertible morphisms|invertible]] up to [[homotopy]]. If one drops this constraint, so that homotopies become "directed" then one might still speak of "[[directed homotopy theory]]".

The archetypical example of an [[(∞,1)-category]] is the $(\infty,1)$-category _[[∞Grpd]]_ of [[∞-groupoids]], just as [[Set]] is the archetypical 1-[[category]]. 

This turns out to be equivalent, as homotopy theories, to the [[classical model structure on topological spaces|classical homotopy theory of topological spaces]] if restricted to those that admit the structure of [[CW-complexes]].

\linebreak

### Relation between topological and abstract homotopy theory: Cohesion.
{#RelationBetweenTopologicalAndAbstractHomotopyTheoryInIdeaSection} 

The case of the homotopy theory of topological spaces ([above](#TopologicalHomotopyTheoryInIdeaSection))
is so classical that often the distinction between [[topology]] and homotopy theory has been (certainly so in the early literature) and still is often blurred (for instance in textbook titles or lecture notes). A transparent conceptual way to understand how [[topology]] and homotopy theory are closely related and yet different is provided by the notion of [[cohesion]]: 

A [[topological space]] $X$ *has* (or *presents*) a [[homotopy type]] through the data that is retained in its [[path ∞-groupoid]], conveniently modeled by its [[singular simplicial set]] $Sing(X)$ (which is a [[Kan complex]] and as such an [[∞-groupoid]]). 
But the topological space contains more information than that retained in its [[path ∞-groupoid]] -- the latter is just a shadow of it, called the *[[shape modality|shape]]* of the topological space.

The extra information in a topological space is the [[cohesion]] on its [[underlying]] [[set]] of points: The [[geometry|geometric]] information of how these [[points]] stick together within [[open subsets]]. This information is lost when one regards topological spaces as stand-ins for their [[shape modality|shapes]] ([[path ∞-groupoids]]) in plain homotopy theory.

More formally:

The [[Top|category of]] [[D-topological spaces]] is a [[full sub-(∞,1)-category|full subcategory]] of the [[cohesive (infinity,1)-topos|cohesive $(\infty,1)$-topos]] of [[D-topological infinity-groupoid|D-topological $\infty$-groupoids]] (also of [[smooth infinity-groupoids|smooth $\infty$-groupoids]]). These carry a [[modal homotopy type theory|qualitative aspect]] called their **[[shape modality|shape]]**, which is a [[shape via cohesive path ∞-groupoid|generalization]] of the [[fundamental ∞-groupoid]]-construction. Now, regarding a [[topological space]] as an object in (plain) [[homotopy theory]], as traditionally done, really means to first regard it as a [[topological groupoid]] in [[cohesive (∞,1)-topos|cohesive homotopy theory]] and then, as such, to retain only its [[shape modality|shape]]. The result is the *[[homotopy type]]* which is "presented" by the topological space:

\begin{imagefromfile}
    "file_name": "RelationTopologyHomotopyTheory_20210921.jpg",
    "width": 700,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 40,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

\linebreak

### Simplicial homotopy theory

The most immediate way to model an [[∞-groupoid]] is as a [[simplicial set]] which is a [[Kan complex]].  Accordingly, another homotopy theory equivalent to archetypical homotopy theory of [[∞-groupoids]] is the [[classical model structure on simplicial sets|classical homotopy theory of simplicial sets]], typically referred to as _[[simplicial homotopy theory]]_.

\linebreak

### Flavors of homotopy theory

But there are many other homotopy theories besides (the various incarnations of) this classical one. Important sub-classes of homotopy theories include:

* _[[stable homotopy theory]]_ modeled by [[stable model categories]] and [[stable (∞,1)-categories]], where the operations of [[looping and delooping]] are an [[equivalence of (∞,1)-categories|equivalence]]. This includes the [[stable (∞,1)-category of spectra]] as well as those of [[sheaves of spectra]].

* _[[geometric homotopy theory]]_ modeled by [[model toposes]] and [[(∞,1)-toposes]], which are the homotopy theoretic analogs of ordinary [[toposes]]. This includes the  homotopy theoretic analog of [[categories of sheaves]], called _[[(∞,1)-categories of (∞,1)-sheaves]]_ or _of [[∞-stacks]]_, but it potentially also contains "[[elementary (∞,1)-toposes]]".
 
The [[geometric homotopy theory]] of [[(∞,1)-toposes]] in particular serves as the foundation for [[higher geometry]]/[[derived geometry]]. This is relevant notably in the [[physics]] of [[gauge theory]], where [[gauge transformations]] are identified with [[homotopies]] in [[geometric homotopy theory]]. For more on this see at _[[geometry of physics -- homotopy types]]_.

On the other hand, the incarnation of homotopy theory as _[[homotopy type theory]]_ exhibits the remarkably [[foundation|foundational]] nature of homotopy theory. Contrary to its original appearance as a fairly complicated-looking theory built on top of classical [[set theory]] and classical [[topology]], homotopy theory turns out to be intrinsically simple: it arises from plain [[dependent type theory]] just by adopting a fully [[constructive mathematics|constructive]] attitude towards the concept of [[identity]]/[[equality]], see at _[[identity type]]_ for more on this. For exposition of this perspective see ([Shulman 17](#Shulman17)).

\linebreak

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



## Related entries
 {#RelatedConcepts}


### General 

* [[homotopy theory FAQ]]

* [[higher structures]]

* [[algebraic homotopy]]

* [[homotopy type theory]]


### Flavors of homotopy theory

* [[synthetic homotopy theory]]

* [[simplicial homotopy theory]]

* [[stable homotopy theory]]

* [[proper homotopy theory]]

* [[parameterized homotopy theory]]

* [[equivariant homotopy theory]], [[global equivariant homotopy theory]]

* [[equivariant stable homotopy theory]]

* [[rational homotopy theory]]

* [[rational parameterized stable homotopy theory]]

* [[p-adic homotopy theory]]

* [[chromatic homotopy theory]]

* [[persistent homotopy theory]]

* [[discrete homotopy theory]]



### Basic concepts in homotopy theory

* [[interval object]], 

  [[cylinder object]], [[path space object]]


* [[homotopy]], [[homotopy group]]

* [[deformation retract]], [[neighborhood retract]]


### Categorical homotopy theory


* [[category with weak equivalences]]

  [[homotopical category]], [[relative category]]

* [[category of fibrant objects]], [[cofibration category]]

* [[model category]]

(...)

* [[closed monoidal deformation retract]]

* [[closed monoidal homotopical category]]

* [[cylinder functor]], [[cocylinder]]

* [[derived functor]]

* [[deformation retract of a homotopical category]]

* [[Dold fibration]]

* [[equivalence]]

* [[folk model structure]]

* [[fundamental groupoid]]

* [[homological resolution]]

* [[homotopical category]]

* [[homotopical cohomology theory]]

* [[homotopy category]]

* [[homotopy limit]], [[homotopy colimit]]

* [[homotopy coherent category theory]]

* [[Hurewicz fibration]], [[Hurewicz connection]], [[Hurewicz cofibration]]



* [[model structure on crossed complexes]]

* [[model structure on simplicial sets]], [[model structure on dendroidal 
sets]]

* [[path object]], [[path groupoid]], [[path n-groupoid]]


* [[test category]]


* [[weak equivalence]]


## References 
 {#References}


[[!include homotopy theory and algebraic topology -- references]]





[[!redirects Homotopy Theory]]
[[!redirects homotopy theories]]
