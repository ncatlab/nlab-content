
> This page is growing incrementally as a lecture series proceeds.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

**Table of chapters**

* [About this page](#AboutThisPage)

1. [Coordinate systems](#CoordinateSystems)

1. [Smooth spaces](#SmoothSpaces)

1. [Differential forms](#DifferentialForms)

1. [Differentiation](#Differentiation)

1. [Smooth homotopy types](#SmoothnGroupoids)

1. [Groups](#NGroups)

1. [Principal bundles](#PrincipalBundles)

1. [Reduction of structure groups](#ReductionOfStructureGroups)

1. [Representations and Associated bundles](#AssociatedNBundle)

1. [Flat connections](#FlatConnections)

1. [de Rham coefficients](#deRhamCoefficients)

1. [Maurer-Cartan forms](#MaurerCartanForms)

1. [Principal connections](#PrincipalConnections)

1. [Characteristic classes](#CharacteristicClasses)

1. [Integration](#Integration)

1. [Gauge theories](#ActionFunctionalsForChernSimonsTypeGaugeTheories)

1. [Geometric quantization](#GeometricQuantization)

1. [Super-geometry](#SupergeometricCoordinateSystems)

1. [Quantum mechanics](#QuantumMechanics)


#Contents#
* table of contents
{:toc}


## About this page
 {#AboutThisPage}

This page is going to contain an introduction to aspects of [[differential geometry]] and their application in fundamental [[physics]]: the [[gauge theory]] appearing in the [[standard model of particle physics]] and the [[Riemannian geometry]] appearing in the [[standard model of cosmology]], as well as the [[symplectic geometry]] appearing in the [[quantization]] of both.

### Scope and perspective

The intended topic scope and readership of the first layer of this page -- the _[Model Layer](#LayerMod)_ --  is much like that of the book ([Frankel](#Frankel)), only that here we make use of a more modern and more transparent conceptual toolbox. We also discuss in two other layers, the _[Semantic Layer](#LayerSem)_ and the _[Syntactic Layer](#LayerSyn)_ deeper mechanisms at work in the background.

Notably, where traditional expositions of [[differential geometry]] proceed by generalizing the [[geometry]] of abstract [[coordinate|coordinate systems]] $\mathbb{R}^n$ to _[[smooth manifolds]]_, here we instead begin by generalizing, in _[Smooth spaces -- Model Layer](SmoothSpacesLayerMod)_, coordinate systems right away to _[[smooth spaces]]_, which happens to be both more expressive as well as actually much easier. In parallel (and to be read independently or not at all) we discuss in _[Smooth spaces -- Semantic Layer](#SmoothSpacesLayerSem)_ how this means that we are working in the _[[sheaf topos]]_ over abstract coordinate systems.  Smooth manifolds are then introduced later as an intermediate notion, together with that of _[[diffeological spaces]]_. (Many of the constructions in [[differential geometry]] applied in [[physics]] do not actually need the notion of a smooth manifold, and, more importantly, for many notions in modern theoretical physics smooth manifolds are not actually sufficiently general.) 

In fact we introduce smooth manifolds only after we introduce _[[smooth groupoids]]_ (below in _[Smooth homotopy type - Model Layer - Smooth groupoids](#SmoothGroupoids))_, which are differential geometric structures that are _still_ simpler than smooth manifolds, and of course even more expressive than smooth spaces. Moreover, smooth groupoids are at the very heart of the geometry of physics: modern fundamental physics is all based on the "[[gauge symmetry|gauge principle]]" and in  _[Model Layer -- Gauge transformations in electromagnetism](#GaugeTransformationsInElectromagnetism)_ we explain how, mathematically, this is essentially nothing but the theory of smooth groupoids. As further background information we discuss in _[Smooth homotopy types - Semantic Layer](#SmoothHomotopyTypesSemanticLayer)_ how this means that we are working in a [[(infinity,1)-topos|higher topos]] over abstract coordinate systems, and in _[Smooth homotopy type - Syntactic Layer](#SmoothHomotopyTypesSyntacticLayer)_ how this means that we are reasoning about physics using the _[[natural deduction]]_ rules of _[[homotopy type theory]]_.

From this setup then naturally flow all the many structures and phenomena seen in the geometry of physics:




### Layers of exposition
 {#Layers}

We discuss each topic below in three stages, in three _layers_. 

1. The first layer, called the **Model Layer **, deals with concrete explicit  constructions as familiar from traditional textbooks on differential geometry and physics. This layer is supposed to be readable and useful all in itself and the reader who feels that this is all he or she wants to see can stick to this and ignore the other layers. In particular, while the _Model Layer_ does invoke the basic notion of a _[[category]]_ and of a _[[functor]]_ -- which are as simple as the notions of [[group]] or [[associative algebra|algebra]] --, it does not use any actual _[[category theory]]_. 
 {#LayerMod}

1. The second layer, called the **Semantic Layer**, makes explicit the ([[(infinity,1)-category theory|higher]]) [[category theory]] and ([[(infinity,1)-topos theory|higher]]) [[topos theory]] at work in the background. This puts the concrete constructions of the _Model Layer_ into a more general context and helps to see certain organizational patterns that underlie the seemingly different phenomena. It provides some powerful theorems which the _Model Layer_ is secretly benefitting from. For instance this layer gives a systematic rule for generalizing everything at the beginning Model Layers from ordinary [[differential geometry]] to what is called  _[[supergeometry]]_, which is the context in which [[fermion|fermionic]] [[particles]] are formalized: the [[matter]] constituents of the [[observable universe]].
 {#LayerSem}

1. The third layer, called the **Syntactic Layer**, makes explicit the expression of these phenomena in the [[logical framework|formal]] [[internal language]] of the [[topos]] of [[smooth spaces]] -- which is _[[dependent type theory|dependent]] [[type theory]]_ -- and of the [[(infinity,1)-topos|higher topos]] of [[smooth infinity-groupoid|smooth higher groupoids]] -- which is _[[homotopy type theory]]_. This makes more transparent various constructions in ([[(infinity,1)-topos theory|higher]]) [[topos theory]] used in _Semantic Layer_, and in fact it provides 
a [[categorical semantics|natural construction principle]] for objects in a (higher) topos that model some intended _meaning_ -- which is precisely what [[mathematical physics]] is all about.
This is meant for readers who enjoy seeing fundamental physics _naturally_ rooted in genuinely fundamental mathematics, in _[[natural deduction]]_ from _[[practical foundations]]_, as it were. Everybody else should ignore this.
 {#LayerSyn}
 
**The three layers**

* **Model Layer** -- [[concrete particular]]: [[models]]

* **Semantic Layer** -- [[concrete general]]: [[categorical semantics]] in [[(infinity,1)-topos theory|higher]] [[topos theory]]

* **Syntactic Layer** -- [[abstract general]]: [[syntax]] in [[homotopy type theory|homotopy]]-[[type theory]]

This [[topos theory|topos-theoretic]] perspective on fundamental [[physics]] which is discussed here is mostly original in the identifications it makes ([Schreiber](#SchreiberCohesiveInfinityTopos)), but it draws insights and inspiration from (and maybe realizes) a vision already expressed since the 1960s by [[William Lawvere]], one of the central figures in the development of [[topos theory]] and [[categorical logic]]. Lawvere links the very inception of topos theory to the motivation to axiomatize physics:

> My own motivation $[$ for developing [[topos theory]] $]$ came from my earlier study of [[physics]]. The foundation of the [[continuum physics]] of general materials, $[...]$ involves powerful and clear physical ideas which unfortunately have been submerged under a mathematical apparatus including not only [[Cauchy sequences]] and countably additive [[measures]], but also ad hoc choices of [[charts]] for [[manifolds]] and of [[inverse limits]] of [[Sobolev space|Sobolev]] [[Hilbert spaces]], to get at the simple [[nuclear spaces]] of intensively and extensively variable quantities. But, as Fichera lamented, all this apparatus may well be helpful in the solution of certain problems, but can the problems themselves and the needed [[axioms]] be stated in a direct and clear manner? And might this not lead to a simpler, equally rigorous account? ([Lawvere, 2000](#Lawvere2000))

More historical pointers along these lines and further related material can also be found at _[[higher category theory and physics]]_.

To give a survey of how the exposition below proceeds in the fashion of these three layers, the following section _[The full story in a few formal words](#TabulatedIndex)_ provides what may be read as  commented _index_ to the central themes of the following text. Whereas the exposition below is organized to start each topic with the discussion of its concrete [[models]] in a [Model layer](#LayerMod), then pass to a general abstract semantics in a [Semantic Layer](#LayerSem) and then finally to the abstract formal syntax in a [Syntactic Layer](#LayerMod), these tables indicates how this passage to abstract syntax usefully reflects back onto the concrete theory: 

The leftmost columns of the following tables formulate concepts in terms of ordinary language. The second columns translate that ordinary language fairly directly to the formal language of ([[homotopy type theory|homotopy]]) [[type theory]]. The third columns then interprets these formal syntactical expressions as [[universal constructions]] in a ([[(infinity,1)-topos|higher]], [[cohesive (infinity,1)-topos|cohesive]]) [[topos]] by the rules of [[categorical semantics]].
Finally, the fourth columns indicate what this universal construction amounts to when concretely realized in the [[model]] given by [[smooth spaces]] and [[smooth ∞-groupoids]]. Finally the rightmost columns point to the chapters in the text below that deal with the given construction.

These tables show that fairly evident and na&#239;ve sounding statements in ordinary language turn under this translation into what is generally regarded as fairly sophisticated constructions. In fact some of these constructions have only been found by translating along the categorical semantics dictionary this way. So the following tables also serves to show how the general abstract discussion here is a means to facilitate reasoning about seemingly complicated concepts underlying fundamental physics:


### The full story in a few formal words
 {#TabulatedIndex}

The fundamental [[physics]] of the [[observable universe|observed world]]  is governed by what is called _[[quantum theory]]_. (This is explicitly so for the [[standard model of particle physics]] and induced from this all fundamental physics ever tested in laboratories; but by all that is known also the remaining ingredient of [[gravity]] is fundamentally a quantum theory, see at [[quantum gravity]] for comments).

Two major axiomatizations of [[quantum theory]] are known, namely 


1. _[[FQFT]]_ where one axiomatizes the assignment of [[spaces of states]] to pieces of [[worldvolume]] (the "[[Schrödinger picture]]" of quantum theory) 

   fragments of which involve:

   * [[finite quantum mechanics in terms of dagger-compact categories]]

   * [[spectral triples]] and [[graph field theory]] [[quantum mechanics]]

   * [[2-spectral triples]] and [[string]] [[sigma-models]]

   * [[Reshetikhin-Turaev construction]] for 3d [[TQFT]]

   * [[FFRS-formalism|FRS-construction]] of 2d [[CFT]] from this via [[holography]]

   * [[extended topological quantum field theories]]
  

1. _[[AQFT]]_ where one axiomatizes the assignment of [[algebras of observables]] to pieces of [[worldvolume]] (the "[[Heisenberg picture]]" of quantum theory)

   fragments of which involve:

   * [[Wightman axioms]], [[Haag-Kastler axioms]]

   * [[Bohr toposes]], [[schreiber:bachelor thesis Nuiten|Bohrification of local nets of observables]]

   * [[factorization algebras]], [[factorization homology]], [[topological chiral homology]], 

(For an attempt at a survey of the state of the art as of 2011 see the collection ([Sati-Schreiber](#SatiSchreiber))).

But all fundamental [[quantum field theories]] observed in (or conjectured to underlie) nature arise by a process called _[[quantization]]_ from structures in [[differential geometry]] (or are induced via a mechanism called the [[holographic principle]] from such that do). 

This differential geometric data involves 

* [[smooth function|smooth]] [[functionals]] -- called _[[action functionals]]_ 

* on [[smooth infinity-groupoid|smooth "spaces"]] -- called _[[moduli stacks]]_ 

* of [[differential geometry|differential geometric]] structures such as [[fiber bundles]] and [[connection on a bundle|connections]] -- called _[[gauge fields|gauge]] [[force|force fields]]_ 

* as well as [[sections]] of [[associated bundles]] -- called _[[matter fields]]_.

Similar differential geometric structures are involved in the _[[geometric quantization]]_ of such an [[action functional]] to an actual [[quantum field theory]].

Hence there is a sequence:

| [[differential geometry]] | $\to$ | [[geometric quantization]] | $\to$ | [[quantum field theory]] |
|--|--|--|--|--|

We discuss a formalization of central aspects of this entire sequence.
Our development proceeds -- as befits a theory of physics and hence of nature -- via _[[natural deduction]]_ from _[[practical foundation of mathematics|practical foundations]]_.

$\,$



Fundamentally, a [[metalanguage|language]] for [[physics]] is to be a language about _existence_; a language in which we can express [[judgements]] of the form:

> There is a thing $x$ of type $X$.

For instance:

> There is a [[gauge field]] $\nabla$ in the [[standard model of particle physics|standard model]] $[X,\mathbf{B}\left(U\left(1\right)\times SU\left(2\right)\times SU\left(3\right)\right)_{conn}]$ of gauge fields on [[spacetime]] $X$.

(Here the square bracket expression for a _[[moduli stack]]_ of gauge fields will be incrementally explained in the following.)

To be predictive, a [[metalanguage|language]] for physics is moreover to be a language in which we can make [[natural deduction|natural deductions]] to [[deductive reasoning|deduce]] further such [[judgements]] from given ones. For instance:

> Given a gauge field $\nabla$ as above, there is an underlying _[[Yang-Mills instanton|instanton]] sector_, $UnderlyingBundle(\nabla)$, in the collection $\left[X,\mathbf{B}\left(U\left(1\right)\times SU\left(2\right)\times SU\left(3\right)\right)\right]$ of instanton configurations in the standard model.

Quantum [[superpositions]] of such [[Yang-Mills instantons]] are the very substrate out of which the [[vacuum]] of the [[observable universe|observed world]] is build: the _[[instanton liquid in quantum chromodynamics]]_. (For more see at _[Yang-Mills theory](#Yang-MillsTheory)_ below.) We consider here a language to reason about such phenomena formally.

The [[metalanguage|formal language]] for such _[[natural deduction]]_ of _[[judgements]]_ about there being [[terms]] of some [[type]] is called _[[type theory]]_. 

**Expressions in ([[dependent type theory|dependent]]) [[type theory]]**:

(read columns 1+2 first, then 3+4)

| ordinary language | [[syntax]] | [[semantics]] | [[model]] | chapter |
|--|--|--|--|--|
|  | [[general abstract]] | [[general concrete]] | [[concrete particular]] | |
| There is... | $\vdash \ldots$ | We speak in the context of a ([[(∞,1)-topos|higher]]) [[topos]] $\mathbf{H}$, a _place where things may be_. (For the time being a ([[locally cartesian closed (infinity,1)-category|higher]]) [[locally cartesian closed category]] is sufficient.) | A [[topos]] for [[synthetic differential geometry|synthetic]] [[differential geometry]], such as $\mathbf{H} = $ [[sheaf topos|Sh]]$($[[SmthMfd]]$)$. Eventually a [[(∞,1)-topos|higher]] such topos: $\mathbf{H} = $ [[Smooth∞Grpd]] or [[SynthDiff∞Grpd]] or [[SmoothSuper∞Grpd]] or ... | _[Smooth spaces](#SmoothSpaces)_ and _[Smooth homotopy types](#SmoothnGroupoids)_  |
| There is a thing $x$ of type $X$. | $\vdash\; x \colon X$ | An [[element]] $\left(* \stackrel{x}{\to} X\right) \in Mor(\mathbf{H})$ of an [[object]] $X$ of $\mathbf{H}$. | A point $x$ in a [[smooth infinity-groupoid|smooth moduli stack]] $X$. | _[Judgements about types and terms](#Judgments)_ |
| There is a type $X$ of things $x$. | $\vdash\; X \colon Type$ | An [[element]] $(* \stackrel{\vdash X}{\to} Obj) \in Mor(\mathbf{H})$ of the [[small object|small]]-[[object classifier]] $Obj$ of $\mathbf{H}$. | A point in the _[[moduli stack]] of all [[small object|small]] moduli stacks_. | _[Judgements about types and terms](#Judgments)_  |
| Given a thing $x$ of type $X$ there is a thing $a(x)$ of type $A(x).$ | $x \colon X\;\vdash\; a(x) \colon A(x)$ | An [[element]] of a morphism $(A \to X)$ $\left(\array{ X &&\stackrel{a}{\to}&& A \\ & {}_{\mathllap{id}}\searrow &\swArrow& \swarrow_{} \\ && X }\right)$ in the [[slice (infinity,1)-topos|slice topos]] $\mathbf{H}_{/X}$. | An $X$-family  in a moduli stack [[bundle]] $A$ over $X$. | _[Slice categories](#SliceCategories)_ and _[Slice toposes](#SliceToposes)_ and _[Slice ∞-Toposes](#SlicedInfinityToposes)_ |
|  There is the collection of all things $a(x)$ for all $x$. | $\vdash\; \left(\sum_{x \colon X} A\left(x\right)\right) \colon Type$ | The [[dependent sum]]/[[left adjoint]] to the [[product]]: $\array{ \mathbf{H}_{/X} &\stackrel{X_!}{\to} & \mathbf{H} \\ (A \to X) &\mapsto& A \in \mathbf{H}} $ | The total space of a [[bundle]]. | _[Natural deduction rules for dependent sum types](#DependentSumTypes)_ |
| There is a thing $t$ in the collection of all things $a(x)$ for all $x$. | $\vdash\; t \colon \sum_{x \colon X} A(x)$ |  An element $*\stackrel{t}{\to} A$ of the total space object. | A point in the [[moduli stack]] $A$ over $X$. | |  
| There is an assignment $f$ of an $a(x)$ to each $x$. | $\vdash \; f \colon \prod_{x \colon X} A(x)$. | An [[element]] in the [[internal hom|internal]] [[object]] of [[sections]] $* \stackrel{f}{\to} [X,A]_X$  | A [[point]] in the smooth relative [[mapping space]] of smooth [[sections]].  | _[Natural deduction rules for dependent product types](#NaturalDeductionForDependentProduct)_ |   
| There is the collection of assignments of an $a(x)$ to each $x$. | $\vdash\; \left( \prod_{x \colon X} A\left(x\right) \right) \colon Type$ | [[internal hom|internal]] space of [[sections]] $[X,A]_X \in \mathbf{H}$ | A smooth relative [[mapping space]] of smooth [[sections]]. |  |
| In particular, there is the collection of such assignments when $A$ does not depend on $x$, the collection of _functions_ from $X$ to $A$. |  $\vdash \; \left(X \to A\right) \coloneqq \left(\prod_{x \colon X} A\right) \colon Type$ | The [[internal hom]] [[object]] $[X,A] \in \mathbf{H}$.  | A smooth [[mapping space]]. |  _[Smooth mapping spaces and smooth moduli spaces](#SmoothMappingSpaces)_ |
| There is a proof $p$ that it is true that there is $x$ of type $X$. | $ \vdash \;  p \colon [X] $ | An [[element]]  $* \stackrel{p}{\to}\tau_{-1}(X)$ of the [[truncated object of an (infinity,1)-topos|(-1)-truncation]] of the object $X$. | A point in the [[smooth space]] of [[equivalence classes]] of points in $X$. | _[Subobjects](#Subobjects)_ |
| There is a proof $p$ that it is true that there is an $a(x)$ for some $x$. | $\vdash\; p \colon \left(\exists_{x \colon X} A\left(x\right) \right) \coloneqq \left[ \sum_{x \colon X} A\left(x\right)\right]$ | | |  |

In order to describe a structured reality, our language needs to be able to speak about _comparison_ of things. 

Fundamental physics rests on the _[[gauge theory|gauge principle]]_: it is meaningless to say that two  things -- such as two [[gauge fields]] $\nabla$ as above -- are  _[[equality|equal]]_; instead they are _gauge [[equivalence|equivalent]]_ if there is a _[[gauge transformation]]_ between them. 

So our language needs to express [[judgements]] of the form:

> There is a [[gauge transformation|gauge]] [[equivalence]] between [[gauge fields]] $\nabla_1$ and $\nabla_2$.

And the language needs to be able to make [[natural deduction|natural deductions]] from such judgements to arrive at:

> Given an [[equivalence]] $\lambda \colon \nabla_1 \simeq \nabla_2 $  there is an equivalence $UnderlyingBundle(\lambda) \colon UnderlyingBundle(\nabla_1) \simeq UnderlyingBundle(\nabla_2)$ between the underlying [[Yang-Mills instanton|instanton sectors]].

The [[metalanguage|formal language]] based of the [[dependent type theory|dependent]] [[type theory]] which we have so far that contains these statements is _type theory with [[propositional equality]]_. In this language we have [[judgements]] such as the following.

**Expressions in [[dependent type theory|dependent]] [[type theory]] with [[propositional equality]]**:

| ordinary language | [[syntax]] | [[semantics]] | [[model]] | chapter |
|--|--|--|--|--|
|  | [[general abstract]] | [[general concrete]] | [[concrete particular]] | |
| Given $x,x'$, there is the collection of equivalences between $x$ and $x'$ equivalent. | $x,x' \colon X \;\vdash \; \left(x \simeq x'\right) \colon Type$. | The [[mapping cocone]] [[object]] $\array{ P_{x,x'} X &\to& * \\ \downarrow &\swArrow_{e}& \downarrow^{\mathrlap{x}} \\ * &\stackrel{x'}{\to} & X }$ | The [[smooth infinity-groupoid|moduli stack]] of [[gauge transformations]] between $x$ and $x'$. | _[Identity types](#IdentityTypes)_ |
| There is an equivalence $e$ between $x$ and $x'$. | $\array{\vdash \; e \colon (x \simeq x') \\ or \\ \vdash \; e \colon (x \rightsquigarrow x') }$ | An [[element]] of  the [[mapping cocone]] object. | A [[gauge transformation]] between $x$ and $x'$. |  |
| Given $x,x'$, there is the collection of proofs that it is true that $x$ and $x'$ are equivalent. | $x,x' \colon X \;\vdash \; [x \simeq x'] \colon Type$. | The [[truncated object of an (infinity,1)-topos|(-1)-truncation]] fo the [[mapping cocone]]. | The [[smooth space]] of [[equivalence classes]] of [[gauge transformations]] from $x$ to $x'$. | |

But the _[[gauge theory|gauge principle]]_ reaches deeper: [[gauge transformations]] themselves are subject to the gauge principle. 

In general it is meaningless to ask if two gauge transformations are equal, but we may ask if there is a _[[higher gauge theory|higher gauge transformation]]_ that transforms one gauge transformation into the other. In the physics literature such _[[gauge-of-gauge transformations]]_ are best known in their incarnation as _[[ghost-of-ghost fields]]_ in what is called the _[[BRST complex]]_ of the given [[gauge theory]]. 

Careful analysis for instance of the _[[Dirac charge quantization]]_ of _[[magnetic charge]]_ shows that already quite mundane physical phenomena exhibit such [[higher gauge transformations]]. But more famously they are known to arise in various guises in _[[string theory]]_, which is a hypothetical refinement of the [[standard model of particle physics]] and [[gravity]].

In either case, our [[metalanguage|formal language]] should not allow the [[natural deduction|deduction]] that gauge [[equivalences]] are themselves either [[equality|equal]] or not, but only allow [[judgements]] of the following form:

> There is a [[higher gauge transformation|gauge-of-gauge equivalence]] $\rho \colon (\lambda_1 \simeq \lambda_2)$ between two given [[gauge equivalences]] $\lambda_1, \lambda_2 \colon (\nabla_1 \simeq \nabla_2)$ between two given [[gauge fields]] $\nabla_1, \nabla_2$.

The flavor of [[type theory]] with [[propositional equality]] for which this is the case is called _[[intensional type theory]]_.

Since therefore a [[type]] $X$ in intensional type theory may contain [[homotopies]] between its [[terms]] of arbitrary order, we call it a _[[homotopy type]]_. 

The homotopy-type nature of the type of gauge connections $[X,\mathbf{B}G_{conn}]$ is most familiar in the physics literature in its [[infinity-Lie theory|infinitesimal approximation]], which is the (off-shell) _[[BRST complex]]_ of the gauge theory: the $n$-fold [[ghost-of-ghost fields]] in the BRST complex correspond to the $n$-fold [[homotopies]] in $[X, \mathbf{B}G_{conn}]$.

In particular, in [[intensional type theory]] we find the [[gauge group]] of a homotopy type, as indicated in the following table.

**Expressions in [[intensional type theory]]**:

| ordinary language | [[syntax]] | [[semantics]] | [[model]] | chapter |
|--|--|--|--|--|
|  | [[general abstract]] | [[general concrete]] | [[concrete particular]] | |
| Given a type $X$, there is (the underlying space) of a group $G$ of ways that $X$ is equivalent to itself. | $X \colon Type \;\vdash \; (X \stackrel{\simeq}{\to} X ) \colon Type $ | A [[loop space object]] $ \array{ G &\to& * \\ \downarrow &\swArrow& \downarrow^{\mathrlap{X}} \\ * &\stackrel{X}{\to} & Type }  $ | A [[∞-group|smooth ∞-group]]. | _[n-groups](#NGroups)_ |
| Given a function between collections of things $X$ and $Y$, and given a thing $y$, there is its preimage-up-to-equivalence. | $\left( f \colon \left(X\to Y\right)\right), \left(y \colon Y\right) \;\vdash\; \sum_{x \colon X} \left(f\left(x\right) \simeq y\right) $ | A  [[(infinity,1)-pullback|homotopy pullback]] $\array{ X \times_{Y} \{y \} &\to& X \\ \downarrow &\swArrow& \downarrow^{\mathrlap{f}} \\ {*} &\underset{y}{\to}&  Y } $  | The [[homotopy fiber]] of a [[homomorphism]] of [[smooth infinity-stack|smooth moduli stacks]]. | |

Suppose then that we have such a map between collections of gauge fields 

$$
  f \colon [X, \mathbf{B}G_{conn}] \to [Y, \mathbf{B}H_{conn}]
$$ 

on two possibly different [[spacetimes]] with two possibly different [[gauge groups]]. 

(For instance we might be looking at _[[Montonen-Olive duality]]_/_[[S-duality]]_ or _[[Seiberg duality]]_ of [[super Yang-Mills theory]].) 

Then we should call $f$ an [[equivalence]] - in the physics literature often: a _[[duality in physics|duality]]_ -- if, while not necessarily being a "[[bijection]]", it is such that the preimage $\phi^{-1}(\nabla) \in [X,\mathbf{B}G_{conn}]$ of a gauge field $\nabla \in [Y, \mathbf{B}H_{conn}]$ consists of gauge fields that are all gauge equivalent to each other, with the gauge equivalences exhibiting this equivalence themselves all being gauge equivalent to each other, etc. 

If this is the case one says that all [[homotopy fibers]] -- _all gauge pre-images_ -- of $\phi$ are [[contractible]] -- are _gauge equivalent to a single gauge field_ -- and that $\phi$ is a _[[weak homotopy equivalence]]_.

For consistency we should demand that the notion of equivalence is such that the space of direct equivalences 
$[X, \mathbf{B}G_{conn}] \simeq [Y, \mathbf{B}H_{conn}]$ is itself equivalent to the space of such  weak homotopy equivalences ("[[duality in physics|dualities]]") $[X, \mathbf{B}G_{conn}] \stackrel{\simeq}{\to} [Y, \mathbf{B}H_{conn}]$. 

This requirement is called the _[[univalence]] [[axiom]]_. 
The [[intensional type theory]]-language considered so far equipped with this axiom is called _[[homotopy type theory]]_.

We indicate now some central judgements that are expressible in homotopy type theory. This involves fundamental judgements in _[[group theory]]_ and in _[[representation theory]]_, two of the pillars of modern [[quantum theory]]/[[quantum field theory]].

**Structures expressible in [[homotopy type theory]]**:

| ordinary language | [[syntax]] | [[semantics]] | [[model]] | chapter |
|--|--|--|--|--|
|  | [[general abstract]] | [[general concrete]] | [[concrete particular]] | |
| Given a type $X$, there is a group $G$ of ways that $X$ is equivalent to itself. | $X \colon Type \;\vdash \; (X \stackrel{\simeq}{\to} X ) \colon Type $ | A [[loop space object]] $ \array{ G &\to& * \\ \downarrow &\swArrow& \downarrow^{\mathrlap{X}} \\ * &\stackrel{X}{\to} & Type }  $ | A [[smooth infinity-groupoid|smooth]] [[automorphism ∞-group]]. | _[n-groups](#NGroups)_ |
| Given a type $X$, there is the _delooping_ $\mathbf{B}G$ of $G$, which is the collection of things equipped with equivalences to $X$. | $X \colon Type \; \vdash \; \mathbf{B}G \coloneqq  \sum_{Y \colon Type} \left[X \simeq Y\right] $ | The [[looping and delooping]] relation $\array{G \simeq &\Omega \mathbf{B}G &\to& * \\ & \downarrow &\swArrow& \downarrow^{\mathrlap{}} \\ & * &\underset{}{\to}& \mathbf{B}G}$ | The [[smooth infinity-groupoid|smooth]] [[moduli stack]] of smooth $G$-[[principal ∞-bundles]]. | _[Principal n-bundles](#PrincipalNBundles)_ |
| Given a thing in $\mathbf{B}G$, there is a thing $V$. | $\array{* \colon \mathbf{B}G \;\vdash\; V(*) \colon Type \\  or\;with\;more\;emphasis: \\  (*,*',g) \colon \sum_{*,*' \colon \mathbf{B}G} (*\rightsquigarrow *') \;\vdash\; V(* \stackrel{g}{\rightsquigarrow} *') \colon Type }$  | A [[homotopy fiber sequence]] $\array{V &\to& V\sslash G \\&& \downarrow^{\overline{\rho}} \\ && \mathbf{B}G }$ with [[homotopy fiber]] $V$ over $\mathbf{B}G$.  | An [[∞-action]]/[[∞-representation]] of $G$ on some $V$, together with its universal $\rho$-[[associated ∞-bundle|associated]] $V$-[[fiber ∞-bundle]] over the [[moduli stack]] $\mathbf{B}G$ for $G$-[[principal ∞-bundles]]. | [Higher actions](#HigherActions) |
| Given a function $g$ classifying a $G$-principal bundle and given a point in the delooping, there is the $G$-principal bundle $P$ itself, being the collection of identifications of the fiber $g(x)$ with $X$| $\left(g \colon X \to \mathbf{B}G\right), \left(* \colon \mathbf{B}G\right) \;\vdash\; P \coloneqq  \sum_{x \colon X} (g(x) \simeq *) $ |  $\array{P &\to& * & \simeq \mathbf{E}G \\ \downarrow &\swArrow& \downarrow \\ X &\stackrel{g}{\to} & \mathbf{B}G }$ | The [[principal ∞-bundle]] given as the [[homotopy pullback]] of the [[universal principal ∞-bundle]]. | _[Principal ∞-bundles](#PrincipalNBundles)_ |
| There is a $G$-equivariant map from the principal bundle to the representation space. | $\vdash\; \sigma \colon \prod_{* \colon \mathbf{B}G} \left(P \to V\right)  $ | An [[element]] $\array{ X &&\stackrel{\sigma}{\to}&& V \\ & \searrow &\swArrow& \swarrow \\ && \mathbf{B}G}$ of $V$ in the [[slice (infinity,1)-topos|slice topos]] $\mathbf{H}_{/\mathbf{B}G}$ | A [[section]] of the $\rho$-[[associated infinity-bundle|associated]] $V$-[[fiber ∞-bundle]]. | | 

In [[gauge theory]] physics, a [[representation]] $\rho$ of the [[gauge group]] $G$ encodes the [[particle]]-content of the [[model (in theoretical physics)]]: a [[section]] of the $\rho$-[[associated bundle]] to the gauge bundle is a _[[matter field]]_ in the [[model (in theoretical physics)|model]]. 

Therefore all the ingredients so far encode the _[[kinematics]]_ of gauge theory, its setup before an actual _[[dynamics]]_ is specified.

Dynamics in physics says how things _move_, hence how they trace out [[trajectories]] in a given [[spacetime]] or more generally in some [[phase space]].

Our [[metalanguage|language]] for reasoning about physics should be able to express this. For $X$ a homotopy type that models [[spacetime]] (the collection of all points of spacetime) there should be a homotopy type $\Pi(X)$ whose [[homotopies]] and higher homotopies are the _smooth trajectories_, the _[[path groupoid|smooth paths]]_ and higher paths in $X$. 

In order to analyse the notion of _smoothness_ here -- we will say: the way that points hold together by _[[cohesion]]_ -- there should also be 

* an expression $\flat X$ for the [[discrete space|discrete]] collection of points underlying $X$ -- **detaching** all points;

*  an expression $\sharp X$ which **dissolves** the cohesion and produces the [[codiscrete object|codiscrete]] smooth structure on $X$.

There are some natural simple [[axioms]] on these constructions. For instance every smooth path in a discrete space $\flat X$ should be constant:  $\Pi (\flat X) \simeq \flat X$.

With such natural axioms understood, these three constructions constitute an [[adjoint triple]] of _[[modal logic|modalities]]_ $(\Pi \dashv \flat \dashv \sharp)$ in our language. 
In particular $\Pi$ and $\flat$ are a _[[monad]]_ and _[[comonad]]_ on the type system, _[[monad (in computer science)|in the sense of computer science]]_ and $\sharp$ is even an internal monad.

Equipping the above _[[homotopy type theory]]_ with these [[modal logic|modalities]] turns it into what we call _[[cohesive homotopy type theory]]_. 

**Structures expressible in [[cohesive homotopy type theory]]**:

| ordinary language | [[syntax]] | [[semantics]] | [[model]] | chapter |
|--|--|--|--|--|
|  | [[general abstract]] | [[general concrete]] | [[concrete particular]] | |
| Given a cohesive homotopy type $X$, there is the _dissolved_ homotopy type $\sharp X$ in which all separate points are collected to one cohesive blob. | $X \colon Type \;\vdash\; \sharp X \colon Type$ | The [[codiscrete object]]-[[monad]] on a ([[local (infinity,1)-topos|higher]]) [[local topos]]. | The [[codiscrete object|codiscrete]] smooth structure on the points of $X$.  | _[Locality of the topos of smooth spaces](##LocalSmooth0Type)_ |
| Given a cohesive homotopy type, there is the map that dissolves the cohesion of the points. | $X \colon Type \;\vdash\;  DeCoh_X \colon X \to \sharp X$ | The [[unit of an adjunction|unit]] of the [[codiscrete object]] [[monad]]. | The function that sends smooth families in a smooth [[moduli stack]] to families of points. | |
| Given $X$ there is the collection $\Pi(X)$ of points in $X$ and smooth trajectories between points in $X$. | $\left(X \colon \sharp Type\right) \;\vdash\; \Pi(X) \colon \sharp Type$ | The construction of the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]]. | The smooth [[fundamental ∞-groupoid|path ∞-groupoid]] of $X$. | _[The local ∞-connectedness of the (∞,1)-topos of smooth ∞-groupoids](#InfinityConnectednessOfSmoothInfinityGrpd)_ |
| Given $X$, there is a canonical map to $\Pi(X)$. | $\left(X \colon \sharp Type\right) \;\vdash\; ConstantPathInclusion_X \colon X \to \Pi(X)$. | The [[unit of an adjunction|unit]] of the $\Pi$-[[monad]] on a [[locally ∞-connected (∞,1)-topos]]. | The inclusion of $X$ into its smooth [[fundamental ∞-groupoid|path ∞-groupoid]] as the constant paths. | |
| Given $X$, there is the result of detaching the points in $X$. |  $\left(A \colon \sharp Type\right) \;\vdash\; \flat A \colon \sharp Type$ | The operation of the [[discrete object]] [[comonad]] on a ([[local (infinity,1)-topos|higher]]) [[local topos]].  | The [[moduli stack]] for [[connection on an infinity-bundle|flat ∞-connections]]. | |
| Given $A$, there is a map from flat $A$-connections to the underlying $A$-bundles  | $\left(A \colon \sharp Type\right) \;\vdash\; UnderlyingBundle_A \colon \flat A \to A $  | The [[counit of an adjunction|counit]] of the [[discrete object]]-[[comonad]] on a ([[local (infinity,1)-topos|higher]]) [[local topos]]. | The function that sends a flat [[connection on an ∞-bundle|∞-connection]] to its underlying [[principal ∞-bundle]]. | _[Flat connections](#FlatConnections)_  |

Adding the [[modal logic|modalities]] $(\Pi \dashv \flat \dashv \sharp)$ to the above language of [[homotopy type theory]] yields a language that we call _[[cohesive homotopy type theory]]_ (following a term introduced by [[Bill Lawvere|Lawvere]]).

Fundamental [[judgements]] in [[cohesive homotopy type theory]] include those indicated in the following table, which capture central concepts of [[gauge theory]] and its ([[higher geometric quantization|higher]]) [[geometric quantization]].

**Structures expressible in [[cohesive homotopy type theory]]**:

[[gauge field|Gauge fields]], [[matter fields]], and smooth [[action functionals]] on their [[moduli stacks]]...

| ordinary language | [[syntax]] | [[semantics]] | [[model]] | chapter |
|--|--|--|--|--|
|  | [[general abstract]] | [[general concrete]] | [[concrete particular]] | |
| A flat connection $\nabla$ on $X$ is a rule for sending paths $(x \stackrel{\gamma}{\to} y) \in \Pi X$ to group elements, respecting composition. 
| $transport(\nabla) \colon \underset{x,y \colon \Pi X}{\sum} \left( x \rightsquigarrow y \right) \to \underset{*,*' \colon \mathbf{B}G}{\sum} (* \rightsquigarrow *')  $  |  $\frac{\Pi(X) \stackrel{transport(\nabla)}{\to} \mathbf{B}G}{X \stackrel{\nabla}{\to} \flat \mathbf{B}G}$.| The [[higher parallel transport]] $trans(\nabla)$ of a [[flat connection]] $\nabla$: a ([[higher gauge theory|higher]]) [[gauge field]] with vanishing [[field strength]]. | _[Flat connections](#FlatConnections)_ | 
| A closed differential form $\omega$ is a flat connection $\nabla$ and a trivialization of the underlying bundle. |  $\begin{aligned} & \flat_{dR} \mathbf{B} G  \coloneqq  \\ & \sum_{\nabla \colon \flat \mathbf{B}G} (UnderlyingBundle(\nabla) \simeq *) \end{aligned}$ | $\begin{matrix} \flat_{dR}\mathbf{B}G  & \stackrel{UnderlyingConnection}{\begin{svg} [[!include SVG rightarrow]]\end{svg}}& \flat \mathbf{B}G \\ \begin{svg}[[!include SVG downarrow]]\end{svg} & \mathclap{\array{\arrayopts{\align{bottom}}\;\begin{svg}[[!include SVG pullback]]\end{svg} & \space{10}{0}{30} \\ \space{10}{30}{1} & \swArrow}} & \begin{svg}[[!include SVG downarrow]]\end{svg}{}^{\mathrlap{Underlying \atop Bundle}} \\ * &\stackrel{}{\begin{svg}[[!include SVG rightarrow]]\end{svg}}& \mathbf{B}G \end{matrix}$  | The [[coefficients]] for [[de Rham cohomology|de Rham]] [[hypercohomology]] -- flat [[∞-Lie algebra valued differential forms]]. | _[de Rham coefficients](#deRhamCoefficients)_ |
| A general connection $\nabla$ is the equivalence between the curvature $curv(\mathbf{c})$ of a bundle $\mathbf{c}$ and a closed differential form $\omega$. | $\nabla \colon \underset{{\mathbf{c} \colon \mathbf{B}^n \mathbb{G}} \atop { \omega \colon \Omega^{n+1}_{cl} }}\sum \left( curv\left(\mathbf{c}\right) = \omega\right) $ | $ \begin{matrix} \mathbf{B}^n \mathbb{G}_{conn}  & \stackrel{F_{(-)}}{\begin{svg} [[!include SVG rightarrow]]\end{svg}}& \Omega^{n+1}_{cl} \\ \begin{svg}[[!include SVG downarrow]]\end{svg} & \mathclap{\array{\arrayopts{\align{bottom}}\;\begin{svg}[[!include SVG pullback]]\end{svg} & \space{10}{0}{30} \\ \space{10}{30}{1} & \swArrow}} & \begin{svg}[[!include SVG downarrow]]\end{svg} \\ \mathbf{B}^n \mathbb{G} &\stackrel{curv}{\begin{svg}[[!include SVG rightarrow]]\end{svg}}& \flat_{dR} \mathbf{B}^{n+1}\mathbb{G} \end{matrix} $  | The [[coefficients]] for smooth [[differential cohomology]]: abelian ([[higher gauge theory|higher]]) [[gauge fields]]. | _[Circle principal n-connections](CirclePrincipalConnections)_ |
| There is a cohesive function from $G$-gauge fields to higher $\mathbb{G}$-gauge fields. | $\vdash \; \exp(i S) \colon \mathbf{B}G_{conn} \to \mathbf{B}^n \mathbb{G}_{conn}$ | A [[differential cohomology|differential]] [[universal characteristic class]]. | An extended [[action functional]]/[[prequantum circle n-bundle|prequantum n-bundle]] for extended [[schreiber:infinity-Chern-Simons theory|higher Chern-Simons-type]] [[gauge theory]].   |  |

... and their _[[schreiber:∞-geometric prequantization]]_ (see there for a more comprehensive disctionary):

| ordinary language | [[syntax]] | [[semantics]] | [[model]] | chapter |
|--|--|--|--|--|
|  | [[general abstract]] | [[general concrete]] | [[concrete particular]] | |
| There is a $\mathbb{G}$-equivariant map $\psi$ from the prequantum bundle to the representation space. | $\vdash \; \psi \colon \underset{\nabla \colon \mathbf{B}\mathbb{G}_{conn}}{\prod} \left( P\left(\nabla\right) \to V\left(\nabla\right) \right)$  |  $\array{ X &&\stackrel{\psi}{\to}&&  V\sslash \mathbb{G}_{conn} \\ & {}_{\mathllap{\nabla}}\searrow &\swArrow& \swarrow_{\overline{\rho}} \\ && \mathbf{B} \mathbb{G}_{conn}}$ | A [[space of states (in geometric quantization)|prequantum state]]. | _[Geometric quantization](#GeometricQuantization)_ | 
| There is a differentially $\mathbb{G}$-equivariant equivalence $\exp(\hat O)$ from the prequantum bundle to itself.  | $\vdash \; \exp(\hat O)  \colon \underset{\nabla \colon \mathbf{B}\mathbb{G}_{conn}}{\prod} \left( P\left(\nabla\right) \stackrel{\simeq}{\to} P\left(\nabla\right) \right)$  |  $\array{ X &&\stackrel{\exp(\hat O)}{\to}&&  X \\ & {}_{\mathllap{\nabla}}\searrow &\swArrow& \swarrow_{\nabla} \\ && \mathbf{B} \mathbb{G}_{conn}}$ | A [[quantum operator (in geometric quantization)|prequantum operator]]: an element of the [[quantomorphism group]]/[[Heisenberg group]] of the [[quantum mechanical system|quantum system]]. | _[Geometric quantization](#GeometricQuantization)_ | 

Finally, in order to be able to concretely speak about not just about any gauge field, but the [[concrete particular]] gauge fields in the [[observable universe]], our language should be able to express the existence of the _[[continuum]] [[real line]]_. 

| ordinary language | [[syntax]] | [[semantics]] | [[model]] | chapter |
|--|--|--|--|--|
|  | [[general abstract]] | [[general concrete]] | [[concrete particular]] | |
| There is the continuum line. | $\begin{aligned}\vdash\; &  \mathbb{R} \colon Type \\ &  i \colon \mathbb{Z} \to \mathbb{R} \\ &  GeometricallyContract_{\mathbb{R}} \colon (\Pi(\mathbb{R}) \simeq Point) \end{aligned} $ | [[line object]] | [[real line]]  | _[The continuum real worldline](#TheContinuumRealWorldLine)_ |

This then induces the existence of the [[circle group]] $U(1) = \mathbb{R}/\mathbb{Z}$. The [[electromagnetic field]] is a [[gauge field]] for [[gauge group]] $U(1)$. Therefore in the language of cohesive homotopy type theory we can say

> Let there be light.

| ordinary language | [[syntax]] | [[semantics]] | [[model]] | chapter |
|--|--|--|--|--|
|  | [[general abstract]] | [[general concrete]] | [[concrete particular]] | |
| There is the collection of higher $U(1)$-principal connections. | $n\colon \mathbb{N} \; \vdash \; \mathbf{B}^n U(1)_{conn} \colon Type$ | The [[coefficients]] for [[ordinary differential cohomology]] (with coefficients in an [[Eilenberg-MacLane object]].) |  The  [[smooth infinity-groupoid|smooth higher moduli stack]] of smooth [[circle n-bundles with connection]]. | _[Circle-principal n-connections](#CirclePrincipalNConnections)_. | 
| There is light. | $ \vdash \; \nabla_{em} \colon [X,\mathbf{B}U(1)_{conn}]$ |  A [[cocycle]] in [[ordinary differential cohomology]] in degree-2. | A configuration of the [[electromagnetic field]] on [[spacetime]] $X$. | _[Circle principal connection](#CirclePrincipalConnections)_ |


$\,$

There are of many more constructions in fundamental ([[quantum theory|quantum]]) [[physics]] that are naturally expressible in [[cohesive homotopy type theory]], but the above should already give an idea and highlight the cornerstones of the following discussion. 

$\,$

We now end this introduction and overview and turn to the in-depth account of _geometry of physics_.

## **Coordinate systems**
 {#CoordinateSystems}

Every kind of _[[geometry]]_ is modeled on a collection of [[generator|archetypical]] basic [[spaces]] and geometric [[homomorphisms]] between them. In [[differential geometry]] the archetypical spaces are the abstract standard [[Cartesian space|Cartesian coordinate systems]], denoted $\mathbb{R}^n$, in every [[dimension]] $n \in \mathbb{N}$, and the geometric homomorphism between them are [[smooth functions]] $\mathbb{R}^{n_1} \to \mathbb{R}^{n_1}$, hence smooth (and possibly degenerate) [[coordinate transformations]].

Here we discuss the central aspects of the nature of such abstract coordinate systems in themselves. At this point these are not yet coordinate systems _on_ some other space. That is instead the topic of the next section _[Smooth spaces](#SmoothSpaces)_.

### Model Layer
 {#CoordinateSystemsLayerMod}

In this [Mod Layer ](#LayerMod) we discuss the [[concrete particulars]] of _[[coordinate systems]]_: the [[continuum]] [[real line]] $\mathbb{R}$, the [[Cartesian spaces]] $\mathbb{R}^n$ formed from it and the [[smooth functions]] between these.

#### The continuum real (world-)line
 {#TheContinuumRealWorldLine}

The fundamental premise of [[differential geometry]] as a model of [[geometry]] in [[physics]] is the following.

**Premise.** _The abstract [[worldline]] of any [[particle]] is modeled by the [[continuum]] [[real line]] $\mathbb{R}$._

This comes down to the following sequence of premises.

1. There is a [[linear ordering]] of the [[points]] on a [[worldline]]: in particular if we pick points at some intervals on the worldline we may label these in an order-preserving way by [[integers]]

   $\mathbb{Z}$.

1. These intervals may each be subdivided into $n$ smaller intervals, for each natural number $n$. Hence we may label points on the [[worldline]] in an order-preserving way by the [[rational numbers]]

   $\mathbb{Q}$.

1. This labeling is dense: every point on the worldline is the [[supremum]] of an [[inhabited set|inhabited]] [[bounded subset]] of such labels. This means that a [[worldline]] [[equivalence|is]] the _[[real line]]_, the [[continuum]] of [[real numbers]]

   $\mathbb{R}$.
  
The adjective "real" in "[[real number]]" is a historical shadow of the old idea that real numbers are related to _observed reality_, hence to [[physics]] in this way. The experimental success of this assumption shows that it is valid at least to very good approximation. 

Speculations are common that in a fully exact theory of [[quantum gravity]], currently unavailable, this assumption needs to be refined. 
For instance in _[[p-adic physics]]_ one explores the hypothesis that the relevant [[complete field|completion]] of the rational numbers as above is not the reals, but [[p-adic numbers]] $\mathbb{Q}_p$ for some [[prime number]] $p \in \mathbb{N}$. Or for example in the study of [[QFT on non-commutative spacetime]] one explore the idea that at small scales the smooth [[continuum]] is to be replaced by an object in [[noncommutative geometry]]. Combining these two ideas leads to the notion of [[non-commutative analytic space]] as a potential model for _[[space]]_ in [[physics]]. And so forth.

For the time being all this remains speculation and differential geometry based on the [[continuum]] [[real line]] remains the context of all fundamental [[model (in theoretical physics)|model building]] in physics related to observed [[phenomenology]]. Often it is argued that these speculations are necessitated by the very nature of [[quantum theory]] applied to [[gravity]]. But, at least so far, such statements are not actually supported by the standard theory of [[quantization]]:
we discuss below in _[Geometric quantization](GeometricQuantization)_ how not just [[classical physics]] but also [[quantum theory]], in the best modern version available, is entirely rooted in differential geometry based on the [[continuum]] [[real line]].

This is the motivation for studying models of physics in geometry modeled on the [[continuum]] [[real line]]. On the other hand, in all of what follows our discussion is set up such as to be _maximally independent_ of this specific choice (this is what _[[topos theory]]_ accomplishes for us, discussed below _[Smooth spaces -- Semantic Layer](#SmoothSpacesLayerSem)_). If we do desire to consider another choice of archetypical spaces for the geometry of physics we can simply "change the [[site]]", as discussed [below](#SmoothSpacesLayerSem) and many of the constructions, propositions and theorems in the following will continue to hold. This is notably what we do below in _[Supergeometric coordinate systems](#SupergeometricCoordinateSystems)_ when we generalize the present discussion to a flavor of differential geometry that also formalizes the notion of [[fermion]] [[particles]]: "differential [[supergeometry]]."


#### Cartesian spaces and smooth functions
 {#CartesianSpaces}



+-- {: .num_defn}
###### Definition

A [[function]] of [[sets]] $f : \mathbb{R} \to \mathbb{R}$ is called 
a **[[smooth function]]** if, [[coinduction|coinductively]]:

1. the [[derivative]] $\frac{d f}{d x} : \mathbb{R} \to \mathbb{R}$ exists;

1. and is itself a smooth function.

=--

+-- {: .num_defn #CartesianSpaceAndHomomorphism}
###### Definition

For $n \in \mathbb{N}$, the **[[Cartesian space]]** $\mathbb{R}^n$ is the set

$$
  \mathbb{R}^n = \{ (x^1 , \cdots, x^{n}) | x^i \in \mathbb{R} \}
$$

of $n$-[[tuples]] of [[real numbers]]. For $1 \leq k \leq n$ write

$$
  i^k : \mathbb{R} \to \mathbb{R}^n
$$

for the [[function]] such that $i^k(x) = (0, \cdots, 0,x,0,\cdots,0)$ is the [[tuple]] whose $k$th entry is $x$ and all whose other entries are $0 \in \mathbb{R}$; and write

$$
  \mathbb{p}^k : \mathbb{R}^n \to \mathbb{R}
$$

for the function such that $p^k(x^1, \cdots, x^n) = x^k$.

A **[[homomorphism]]** of Cartesian spaces is a [[smooth function]]

$$
  f : \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}
  \,,
$$

hence a [[function]] $f : \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ such that all [[partial derivatives]] exist and are [[continuous map|continuous]] (...).

=--

+-- {: .num_example}
###### Example

Regarding $\mathbb{R}^n$ as an $\mathbb{R}$-[[vector space]], 
every [[linear function]] $\mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$
is in particular a [[smooth function]].

=--

+-- {: .num_remark}
###### Remark

But a homomorphism of Cartesian spaces in def. \ref{CartesianSpaceAndHomomorphism} is *not* required to be a [[linear map]]. We do *not* regard the Cartesian spaces here as [[vector spaces]]. 

=--

+-- {: .num_defn}
###### Definition

A [[smooth function]] $f : \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ is called a **[[diffeomorphism]]** if there exists another smooth function 
$\mathbb{R}^{n_2} \to \mathbb{R}^{n_1}$ such that the underlying functions of sets are [[inverse]] to each other

$$
  f \circ g = id
$$

and

$$
  g \circ f = id
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

There exists a [[diffeomorphism]] $\mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ precisely if $n_1 = n_2$.

=--

+-- {: .num_defn #CartesianSpacesAndSmoothFunctions}
###### Definition

We will also say equivalently that

1. a [[Cartesian space]] $\mathbb{R}^n$ is an **[[coordinate system|abstract coordinate system]]**;

1. a [[smooth function]] $\mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ is an **[[coordinate transformation|abstract coordinate transformation]]**;

1. the [[function]] $p^k : \mathbb{R}^{n} \to \mathbb{R}$ is the $k$th **[[coordinate]]** of the coordinate system $\mathbb{R}^n$. We will also write this function as $x^k : \mathbb{R}^{n} \to \mathbb{R}$.

1. for $f : \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ a [[smooth function]], and $1 \leq k \leq n_2$ we write

   1. $f^k \coloneqq p^k\circ f$

   1. $(f^1, \cdots, f^n) \coloneqq f$.

=--

+-- {: .num_remark }
###### Remark

It follows with this notation that

$$
  id_{\mathbb{R}^n} = (x^1, \cdots, x^n) : \mathbb{R}^n \to \mathbb{R}^n
  \,.
$$

Hence an abstract coordinate transformation 

$$ 
  f : \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}
$$

may equivalently be written as the tuple

$$
  \left(
    f^1 \left( x^1, \cdots, x^{n_1} \right)
    ,
    \cdots,
    f^{n_2}\left( x^1, \cdots, x^{n_1} \right)
  \right)
  \,.
$$

=--

+-- {: .num_prop #CartSpCategory}
###### Propositions

Abstract coordinate systems according to prop. \ref{CartesianSpacesAndSmoothFunctions} form a _[[category]]_ 
-- to be denoted _[[CartSp]]_ -- whose

* [[objects]] are the abstract coordinate systems $\mathbb{R}^{n}$ (the [[class]] of objects is the [[set]] $\mathbb{N}$ of [[natural numbers]] $n$);

* [[morphisms]] $f : \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ are the abstract [[coordinate transformations]] = [[smooth functions]].

Composition of morphisms is given by [[composition]] of [[functions]].

We have that

1. The [[identity]] morphisms are precisely the identity functions.

1. The [[isomorphisms]] are precisely the [[diffeomorphisms]].

=--

+-- {: .num_defn}
###### Definition

Write [[CartSp]]${}^{op}$ for the [[opposite category]] of [[CartSp]].

This is the category with the same objects as $CartSp$, but where a morphism $\mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ in $CartSp^{op}$ is given by a morphism $\mathbb{R}^{n_1} \leftarrow \mathbb{R}^{n_2}$ in $CartSp$.

=--

We will be discussing below the idea of exploring smooth spaces by laying out abstract coordinate systems in them in all possible ways. The reader should begin to think of the sets that appear in the following definition as the _set of ways_ of laying out a given abstract coordinate systems in a given space. This is discussed in more detail below in _[Smooth spaces](#SmoothSpaces)_.

+-- {: .num_defn}
###### Definition

A [[functor]]  $X : CartSp^{op} \to Set$ (a "[[presheaf]]") is

1. for each abstract coordinate system $U$ a [[set]] $X(U)$

1. for each [[coordinate transformation]] $f : \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ a [[function]] $X(f) : X(\mathbb{R}^{n_1}) \to X(\mathbb{R}^{n_2})$

such that 

1. [[identity]] is respected $X(id_{\mathbb{R}^n}) = id_{X(\mathbb{R}^n)}$;

1. [[composition]] is respected $X(f_2)\circ X(f_1) = X(f_2 \circ f_1)$

=--


#### The fundamental theorems about smooth functions
 {#PropertiesOfSmoothFunctions}

The special properties [[smooth functions]] that make them play an important role different from other classes of functions are the following.

1. existence of [[bump functions]] and [[partitions of unity]]

1. the [[Hadamard lemma]] and [[Borel's theorem]]

Or maybe better put: what makes smooth functions special is that the first of these properties holds, while the second is still retained.

(...)


### Semantic Layer
 {#CoordinateSystemsLayerSem}

In this [Sem Layer](#LayerSem) we discuss the [[concrete general]] aspects of _abstract [[coordinate systems]]_, def. \ref{CartesianSpacesAndSmoothFunctions}: the fact that they naturally form: 

1. an _[[algebraic theory]]_, 

1. a _[[site]]_.


#### The algebraic theory of smooth algebras
 {#TheAlgebraicTheoryOfSmoothAlgebras}

+-- {: .num_prop}
###### Propositions

* The [[category]] [[CartSp]] has all [[finite limit|finite]]
[[products]]. 

* Every object is a finite [[product]] of the object $\mathbb{R}$ (the [[real line]] itself).

* The [[terminal object]] is $\mathbb{R}^0$, the [[point]].

=--

Hence [[CartSp]] is (the [[syntactic category]]) of an [[algebraic theory]] (a [[Lawvere theory]]). 

This is called the [[theory]] of _[[smooth algebras]]_.

+-- {: .num_defn}
###### Definition

A [[product]]-preserving [[functor]] 

$$
  A : CartSp \to Set
$$

is a _[[smooth algebra]]_. A [[homomorphism]] of smooth algebras is a [[natural transformation]] between the corresponding functors.

=--

The basic example is:

+-- {: .num_example #TheSmoothgAlgebraOfFunctionsOnACartesianSpace}
###### Example

For $n \in \mathb{N}$, the [[smooth algebra]] $C^\infty(\mathbb{R}^n)$ 
is the functor $CartSp \to Set$ which is [[representable functor|functor corepresented]] by $\mathbb{R}^n \in $ [[CartSp]]. This means that to $\mathbb{R}^k \in CartSp$ it assigns the set

$$
  Hom_{CartSp}(\mathbb{R}^n , \mathbb{R}^k)
  = 
  C^\infty(\mathbb{R}^n, \mathbb{R}^k)
$$

of [[smooth functions]] from $\mathbb{R}^n$ to $\mathbb{R}^k$, and to a [[smooth function]] $f \colon \mathbb{R}^{k_1} \to \mathbb{R}^{k_2}$ it assigns the function

$$
  f\circ (-)
  \colon
  C^\infty(\mathbb{R}^n, \mathbb{R}^{k_1})
  \to
  C^\infty(\mathbb{R}^n, \mathbb{R}^{k_2})
$$

given by postcomposition with $f$.

=--

+-- {: .num_remark}
###### Remark

Example \ref{TheSmoothgAlgebraOfFunctionsOnACartesianSpace} shows how we are to think of a functor $A \colon CartSp \to Set$ as encoding an algebra: such a functor assigns to $\mathbb{R}^n$ a set to be interpreted as a set of "smooth functions on something with values in $\mathbb{R}^n$", only that the "something" here is not pre-defined, but is instead indirectly characterized by this assignment.

Due to this we will often denote smooth algebras as "$C^\infty(X)$", even if "$X$" is not a pre-defined object, and write their value on $\mathbb{R}^n$ as $C^\infty(X,\mathbb{R}^n)$. 

=--

This is illustrated by the next example.

+-- {: .num_example #DualNumbers}
###### Example

The **[[ring of dual numbers|smooth algebra of dual numbers]]** $C^\infty(\mathbf{D})$ is the smooth algebra which assigns to $\mathbb{R}^n$ the [[Cartesian product]]

$$
  C^\infty(D,\mathbb{R}^n)
  \coloneqq
  \mathbb{R}^n \times \mathbb{R}^n
$$

of two copies of $\mathbb{R}^n$, which we will write as

$$
  \left\{
    (\epsilon \mapsto (\vec x + \epsilon \vec v))
    |
    \vec x , \vec v \in \mathbb{R}^n
  \right\}
  \,.
$$

Moreover, a [[smooth function]] $f \colon \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ is sent to the function

$$
  C^\infty(D, f)
  \colon
  C^\infty(D, \mathbb{R}^{n_1})
  \to 
  C^\infty(D, \mathbb{R}^{n_2})
$$

given by

$$
  \begin{aligned}
  \left(\epsilon \mapsto \left(\vec x + \epsilon \vec v\right)\right)
  \\
  \left(
    \epsilon \mapsto f(\vec x) + (\mathbf{d}f)(\vec v)
  \right)
  &\mapsto 
  \left(
    \epsilon
    \mapsto 
    \left(
       f\left(\vec x\right) 
        +  
       \sum_{j = 1}^{n_2}
       \left(\sum_{i = 1}^{n_1}\frac{\partial f^j}{\partial x^i} v^i\right)
       \vec e_i  
    \right)
    \right)
  \end{aligned}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

As the notation suggests, we may think of $C^\infty(D)$ as the functions on a first order [[infinitesimal object|infinitesimal neighbourhood]] of the origin in $\mathbb{R}^n$. 

=--




#### The coverage of differentially good open covers
 {#CoverageOfDifferentiallyGoodOpenCovers}

We discuss a standard structure of a _[[site]]_ on the category [[CartSp]]. Following _[[Sketches of an Elephant|Johnstone -- Sketches of an Elephant]]_, it will be useful and convenient to regard a site as a ([[small site|small]]) category equipped with a _[[coverage]]_. This generates a genuine [[Grothendieck topology]], but need not itself already be one.

+-- {: .num_defn}
###### Definition

For $n \in \mathbb{N}$ the standard [[open ball|open n-ball]] is the subset

$$
  D^n = \{ (x_i)_{i =1}^n \in \mathbb{R}^n | \sum_{i = 1}^n (x_i)^2 \lt 1 \}  \hookrightarrow \mathbb{R}^n
  \,.
$$


=--

+-- {: .num_prop}
###### Proposition

There is a [[diffeomorphism]]

$$
  \mathbb{R}^n \stackrel{\simeq}{\to} D^n
  \,.
$$

=--


+-- {: .num_defn #DifferentiallyGoodOpenCover}
###### Definition

A **differentially [[good open cover]]** of a [[Cartesian space]] $\mathbb{R}^n$ is a set $\{U_i \hookrightarrow \mathbb{R}^n\}$ of [[open subset]] inclusions of Cartesian spaces such that these [[open cover|cover]] $\mathbb{R}^n$
and such for each non-empty finite [[intersection]] there exists a [[diffeomorphism]] 

$$
  \mathbb{R}^n \stackrel{\simeq}{\to} U_{i_1} \cap \cdots \cap U_{i_k}
$$

that identifies the $k$-fold intersection with a Cartesian space itself.

=--

+-- {: .num_remark}
###### Remark

Differentiably good covers are useful for computations. Their full impact is however on the [[homotopy theory]] of [[simplicial presheaves]] over [[CartSp]]. This we discuss further below, around 
prop. \ref{DifferentiablyGoodCoverGivesSPlitHyperCoverOverCartSp}.

=--



+-- {: .num_prop #DiffGoodOpenCoversRefineOpenCovers}
###### Proposition

Every [[open cover]] refines to a differentially good open cover, def. \ref{DifferentiallyGoodOpenCover}. 

=--

A proof is at _[[good open cover]]_. 

+-- {: .num_remark}
###### Remark

Despite its appearance, this is not quite a classical statement. The classical statement is only that every open cover is refined by a _topologically_ [[good open cover]]. See the comments _[here in the references-section](http://ncatlab.org/nlab/show/ball#References)_ at _[[open ball]]_ for the situation concerning this statement in the literature.

=--

+-- {: .num_remark}
###### Remark

The _good_ open covers do not yet form a [[Grothendieck topology]] on [[CartSp]]. One of the axioms of a Grothendieck topology is that for every [[covering]] family also its [[pullback]] along any morphism in the category is a covering family. But while the pullback of every [[open cover]] is again an open cover, and hence open covers form a Grothendieck topology on [[CartSp]], not every pullback of a _[[good open cover|good]]_ open cover is again _good_.

=--

+-- {: .num_example #ExampleThatGoodOpenCoversAreNotPullbackStable}
###### Example

Let $\{\mathbb{R}^2\stackrel{\phi_{i}}{\hookrightarrow}\mathbb{R}^2\}_{i \in \{1,2\}}$ be the [[open cover]] of the [[plane]] by an open left half space

$$
   \mathbb{R}^2 \simeq \{ (x_1,x_2) \in \mathbb{R}^2 | x_1 \lt 1 \} \stackrel{\phi_1}{\hookrightarrow} \mathbb{R}^2
$$

and a right open half space

$$
   \mathbb{R}^2 \simeq \{ (x_1,x_2) \in \mathbb{R}^2 | x_1 \gt -1 \} \stackrel{\phi_2}{\hookrightarrow} \mathbb{R}^2
  \,.
$$

The intersection of the two is the open strip

$$
  \mathbb{R}^2 \simeq \{ (x_1, x_2) \in \mathbb{R}^2 | -1 \lt x_1 \lt 1 \}
  \hookrightarrow 
  \mathbb{R}^2
  \,.
$$

So this is a [[good open cover]] of $\mathbb{R}^2$. 

But consider then the smooth function 

$$
  2(\cos(2 \pi (-)), \sin(2 \pi (-))) \colon \mathbb{R}^1 \to \mathbb{R}^2 
$$

which sends the line to a curve in the plane that periodically goes around the [[circle]] of radius 2 in the plane. 

Then the pullback of the above good open cover on $\mathbb{R}^2$ to $\mathbb{R}^1$ along this function is an [[open cover]] of $\mathbb{R}$ by two open subsets, each being a disjoint union of countably many open [[intervals]] in $\mathbb{R}$. 
Each of these open intervals is an open 1-ball hence diffeomorphic to $\mathbb{R}^1$, but their _[[disjoint union]]_ is not [[contractible topological space|contractible]] (it does not contract to the point, but to many points!). 

So the pullback of the good open cover that we started with is an open cover which is not _good_ anymore. But it has an evident _refinement_ by a good open cover. 

=--

This is a special case of what the following statement says in generality.

+-- {: .num_prop #TheDifferentiallyGoodOpenCoverCoverage}
###### Proposition

The differentially good open covers, def. \ref{DifferentiallyGoodOpenCover}, constitute a [[coverage]] on [[CartSp]]. 

Hence [[CartSp]] equipped with that coverage is a [[site]].

=--

+-- {: .proof}
###### Proof

By definition of [[coverage]] we need to check that for $\{U_i \hookrightarrow \mathbb{R}^n\}_{i \in I}$ any [[good open cover]] and $f \colon \mathbb{R}^k \to \mathbb{R}^n$ any smooth function, we can find a good open cover $\{K_j \to \mathbb{R}^k\}_{j \in J}$ and a [[function]] $J \to I$ such that for each $j \in J$ there is a smooth function $\phi \colon K_j \to U_{\rho(j)}$ that makes this [[diagram]] 
[[commuting diagram|commute]]:

$$
  \array{
    K_j &\stackrel{\phi}{\to}& U_{i(j)}
    \\
    \downarrow && \downarrow
    \\
    \mathbb{R}^k &\stackrel{f}{\to}& \mathbb{R}^n
  }
  \,.
$$

To obtain this, let $\{f^* U_i \to \mathbb{R}^k\}$ be the pullback of the original covering family, in that 

$$
  f^* U_i \coloneqq \{ x \in \mathbb{R}^k | f(x) \in U_i \}
  \hookrightarrow \mathbb{R}^k
  \,.
$$

This is evidently an [[open cover]], albeit not necessarily a _[[good open cover]]_. But by prop. \ref{DiffGoodOpenCoversRefineOpenCovers} there does exist a good open cover $\{\tilde K_{\tilde j} \hookrightarrow \mathbb{R}^k\}_{\tilde j \in \tilde J}$ _refining_ it, which in turn means that for all $\tilde j$ there is  

$$
  \array{
    \tilde K_{\tilde j} &\to& K_{j(\tilde j)}
    \\
    \downarrow && \downarrow 
    \\
    \mathbb{R}^k &\stackrel{=}{\to}& \mathbb{R}^k
  }
  \,.
$$

Therefore then the [[pasting]] composite of these commuting squares 

$$
  \array{
    \tilde K_{\tilde j} &\to& K_{j(\tilde j)} &\to& U_{i(j(\tilde j))}
    \\
    \downarrow && \downarrow && \downarrow
    \\
    \mathbb{R}^k &\stackrel{=}{\to}& \mathbb{R}^k
   &\stackrel{f}{\to}& \mathbb{R}^n
  }
$$

solves the condition required in the definition of [[coverage]].

=--

By example \ref{ExampleThatGoodOpenCoversAreNotPullbackStable} this [[good open cover]] [[coverage]] is not a [[Grothendieck topology]]. But as any coverage, it uniquely completes to one which has the same [[sheaves]].

+-- {: .num_prop}
###### Proposition

The [[Grothendieck topology]] induced on [[CartSp]] by the differentially good open cover coverage of def. \ref{TheDifferentiallyGoodOpenCoverCoverage} has as covering families the ordinary [[open covers]]. 

=--

+-- {: .num_remark}
###### Remark

This means that for every sheaf-theoretic construction to follow we can just as well consider the Grothendieck topology of open covers on $CartSp$. The sheaves of the open cover topology are the same as those of the good open cover coverage. But the latter is (more) useful for several computational purposes in the following. It is the _good_ open cover coverage that makes manifest, below, that sheaves on $CartSp$ form a [[locally connected topos]] and in consequence then a [[cohesive topos]]. This kind of argument becomes all the more pronounced as we pass [further below](#SmoothnGroupoids) to [[(∞,1)-sheaves]] on [[CartSp]]. This will be discussed in _[Smooth n-groupoids -- Semantic Layer -- Local Infinity-Connectedness](#InfinityConnectednessOfSmoothInfinityGrpd) below.

=--

#### The slice category 
 {#SliceCategories}

(...)

* [[slice category]] $CartSp_{\mathbb{R}^n}$

* [[subterminal object]], [[open cover]]

(...)


### Syntactic Layer
 {#CoordinateSystemsLayerSyn}

In this [Syn Layer](#LayerSyn) we discuss the [[abstract generals]] of _abstract [[coordinate systems]]_, def. \ref{CartesianSpacesAndSmoothFunctions}: the [[internal language]] of a category with [[products]], which is _[[type theory]]_ with _[[product types]]_.

#### Judgments about types and terms
 {#Judgments}

We now introduce a different _notation_ for [[objects]] and [[morphisms]] in a [[category]] (such as the category [[CartSp]] of def. \ref{CartSpCategory}). This notation is designed to, eventually, make more transparent what exactly it is that happens when we [[deductive reasoning|reason deductively]] about [[objects]] and [[morphisms]] of a [[category]]. 

But before we begin to make any actual [[deductions]] about [[objects]] and [[morphisms]] in a category [below](#NaturalDeductionRulesForProductTypes), in this section here we express the given objects and morphisms at hand in the first place. Such basic statements of the form "There is an object called $A$" are to be called _[[judgments]]_, in order not to confuse these with genuine _[[propositions]]_ that we eventually formalize _within_ this [[metalanguage]].

To express that there is an [[object]] 

$$
  X \in \mathcal{C}
$$ 

in a [[category]] $\mathcal{C}$, we write now equivalently the string of symbols (called a _[[sequent]]_)

$$
  \vdash \; X \colon Type
  \,.
$$

We say that these symbols express the _[[judgment]]_ that $X$ is a _[[type]]_. We also say that $\vdash \; X \colon Type$ is the _[[syntax]]_ of which $X \in \mathcal{C}$ is the _[[categorical semantics]]_.

For instance the [[terminal object]] $* \in \mathcal{C}$ we call the [[categorical semantics]] of the _[[unit type]]_ and write [[syntax|syntactically]] as

$$
  \vdash \; Unit \colon Type
  \,.
$$

If we want to express that we do assume that a terminal object indeed exists, hence that we want to be able to _[[deduction|deduce]]_ the existence of a terminal object from no hypothesis, then we write this [[judgment]] below a horizontal line

$$
  \frac{}{\vdash \; Unit \colon Type}
  \,.
$$

We will see more interesting such horizontal-line statements [below](#NaturalDeductionRulesForProductTypes).

Next, to express an [[element]] of the object $X$ in $\mathcal{C}$, hence a [[morphism]] 

$$
  * \stackrel{x}{\to} X
$$ 

in $\mathcal{C}$ we write equivalently the [[sequent]]

$$
  \vdash \; x \colon X
$$

and call this the [[judgment]] that $x$ is a _[[term]]_ of [[type]] $X$.

Notice that every object $X \in \mathcal{C}$ becomes the [[terminal object]] in the _[[slice category]]_ $\mathcal{C}_{/X}$.
Let $A \to X$ be any morphism in $\mathcal{C}$, regarded as an object in the [[slice category]]

$$
  A \in \mathcal{C}_{/X}
  \,.
$$

We declare that the [[syntax]] of which this is the [[categorical semantics]] is given by the [[sequent]]

$$
  x \colon X \;\vdash \;  A(x) \colon Type
  \,.
$$

We say that this expresses the [[judgement]] that $A$ is an  _$X$-[[dependent type]]_; or a type in the _[[context]] of a [[free variable]]_ $x$ of [[type]] $X$.

Notice that an [[element]] of $A \in \mathcal{C}_{/X}$ is a [[generalized element]] of $A$ in $\mathcal{C}$, namely a morphism $X \to A$ which fits into a [[commuting diagram]]

$$
  \array{
    X &&\stackrel{a}{\to}&& A
    \\
    & {}_{\mathllap{id_X}}\searrow && \swarrow_{}
    \\
    && X
  }
$$

in $\mathcal{C}$.

We declare that the [[syntax]] of which such

$$
  a \in A  \;\;\;\; (in \mathcal{C}_{/X})
$$

is this the [[categorical semantics]] is the [[sequent]]

$$
  x\colon X \;\vdash\; a(x) : A(x)
  \,.
$$

We say that this expresses the [[judgment]] that $a(x)$ is a [[term in context|term depending on]] the [[free variable]] $x$ of [[type]] $X$.

This completes the list of _[[judgment]]_ [[syntax]] to be considered. Notice that if the category $\mathcal{C}$ has [[products]] then, even though it does not explicitly appear above, this is sufficient to express any morphism $X \stackrel{f}{\to} Y$ in $\mathcal{C}$ as the [[semantics]] of a [[term]]: we regard this morphism naturally as being the corresponding morphism in the [[slice category]] $\mathcal{C}_{/X}$ which as a [[commuting diagram]] in $\mathcal{C}$ itself is

$$
  \array{
     X && \stackrel{(f,id_X)}{\to} &&  Y\times X
     \\
     & {}_{\mathllap{id_X}}\searrow && \swarrow_{\mathrlap{p_2}}
     \\
     && X
  }
  \,.
$$ 

This is the [[categorical semantics]] for which the [[syntax]] is simply

$$
  x \colon X \;\vdash\; y(x) \colon Y
  \,,
$$

being the [[judgment]] which expresses that $y(x)$ is a [[term in context]] of an $X$-[[dependent type]] $Y$ in the special degenerate case that $Y$ does not actually vary with $x \colon X$.



#### Natural deduction rules for product types
 {#NaturalDeductionRulesForProductTypes}

With the [above symbolic notation](#Judgments) for making [[judgments]] about the presence of [[objects]] and [[morphisms]] in a [[category]] $\mathcal{C}$, we now consider a system of rule of [[deduction]]  that tells us how we may _process_ these symbols (how to do _[[computations]]_) such that the new symbols we obtain in turn express new objects and new morphisms in $\mathcal{C}$ that we can build out of the given ones by _[[universal constructions]]_ in the sense of [[category theory]]. 

This way of _deducing_ new expressions from given ones is very basic as well as very natural and hence goes by the technical term _[[natural deduction]]_. For every kind of [[type]] (every [[universal construction]] in [[category theory]]) there is, in [[natural deduction]], one set of rules for how to [[deductive reasoning|deductively reason]] about it. This set of rules, in turn, always consists of four kinds of rules, called the

1. [[type formation rule]]

1. [[term introduction rule]]

1. [[term elimination rule]]

1. [[computation rule]].

These are going to be the [[syntax]] in _[[type theory]]_ of which [[universal constructions]] in [[category theory]] is the [[categorical semantics]].

In our running example where $\mathcal{C} = $ [[CartSp]], the only [[universal construction]] available is that of forming [[products]]. We therefore introduce now the [[natural deduction]] rules by way of example of the special case of [[product types]].

**1. [[type formation rule]]** Let 

$$
  A , B \in \mathcal{C}
$$ 

be two [[objects]] in a [[category]] with [[products]]. Then there exists [[generalized the|the]] [[product]] [[object]]

$$
  A \times B \in \mathcal{C}
  \,.
$$

We now declare that the [[syntax]] of which this state of affairs is the [[categorical semantics]] is the collection of symbols of the form

$$
  \frac{A \colon Type \;\;\;\;\; B \colon Type}{ A \times B \colon Type}
  \,.
$$

Here on top of the horizontal line we have the two [[judgments]] which express that, [[syntax|syntactically]], $A$ is a [[type]] and $B$ is a [[type]], and [[semantics|semantically]]  that $A \in \mathcal{C}$ and $B \in \mathcal{C}$. Below the horizontal line is, in turn, the [[judgment]] which expresses that there is, syntactically,  a [[product type]], which semantically is the [[product]] $A \times B \in \mathcal{C}$. The horizontal line itself is to indicate that if we are given the (symbols of) the collection of judgments on top, then we are entitled to also obtain the judgment on the bottom.

**Remark (Computation)** All this may seem, on first sight, like being a lot of fuss about something of grandiose banality. To see what is gradually being accomplished here despite of this appearance, as we proceed in this discussion, the reader can and should think of this as the first steps in the definition of a [[programming language]]: the notion of judgment is a syntactic rule for strings of symbols that a computer is to read in, and a [[natural deduction]]-step as the [[type formation rule]] above is an operation that this computer validates as being an allowed step of transforming a memory state with a given collection of such strings into a new memory state to which the string below the horizontal line is added. As we add the remaining rules below, what looks like a grandiose banality so far will remain grandiose, but no longer be a banality. The reader feeling in need of more motivational remarks along these lines might want to take a break here and have a look at the entry _[[computational trinitarianism]]_ first, that provides more pointers to the grandiose picture which we are approaching here.

Next, the second [[natural deduction]] rule for [[product types]] is the

**2. [[term elimination rule]]**. The fact that $A \times B \in \mathcal{C}$ is equipped with two [[projection]] [[morphisms]] 

$$
  \array{
    A \stackrel{p_1}{\leftarrow} A \times B \stackrel{p_2}{\to} B
  }
$$ 

means that from every [[element]] $t$ of $A \times B$ we may deduce the existence of [[elements]] $p_1(t)$ and $p_2(t)$ of $A$ and $B$, respectively. We declare now that this is the [[categorical semantics]] of which the [[natural deduction]] [[syntax]] is:

$$
  \frac{\vdash \; t \colon A \times B}{\vdash \; p_1(t) \colon A}
  \;\;\;\;\;\;\;\;\;
  \frac{\vdash \; t \colon A \times B}{\vdash \; p_2(t) \colon B}
  \,.
$$

As before, this is to say that if syntactically we are given strings of symbols expressing [[judgments]] as on the top of these horizontal lines, then we may "[[natural deduction|naturally deduce]]" also the judgment of the string of symbols on the bottom of this line.

**3. [[term introduction rule]]**. The first part of the [[universal property]] of the [[product]] in [[category theory]] is that for  $Q \in \mathcal{C}$ any other [[object]] equipped with morphisms 

$$
  \array{
    && Q
    \\
    & {}^{\mathllap{a}}\swarrow && \searrow^{\mathrlap{b}}
    \\
    A  && &&  B
  }
$$ 

in $\mathcal{C}$, we obtain a canonical morphism 

$$
  Q \to A \times B
$$ 

in $\mathcal{C}$. This is now declared to be the [[categorical semantics]] of which the [[natural deduction]] [[syntax]] is

$$
  \frac{
    \vdash\; a \colon A \;\;\;\;\;\; \vdash\; b \colon B
  }{
   \vdash (a,b) \colon A \times B
  }
  \,.
$$

With the [[elements]] that are the [[semantics]] of the terms appearing here made explicit, this is the syntax for a [[diagram]]

$$
  \array{
     && Q
     \\
     & {}^{\mathllap{a}}\swarrow &\downarrow^{\mathrlap{(a,b)}}& \searrow^{\mathrlap{b}}
     \\
     A && A \times B && B
  }
  \,.
$$


**4. [[computation rule]]**. The next part of the [[universal property]] of the [[product]] in [[category theory]] is that the resulting [[diagram]]

$$
  \array{
    && Q
    \\ 
    & {}^{\mathllap{a}}\swarrow &\downarrow& \searrow^{\mathrlap{b}}
    \\
    A &\stackrel{p_1}{\leftarrow}& A \times B & \stackrel{p_2}{\to} & B
  }
$$

is in fact a _[[commuting diagram]]_. Syntactically this is, clearly, the rule that the following identifications of strings of symbols are to be enforced

$$
  p_1(a,b) = a \;\;\;\;\;\; p_2(a,b) = b
  \,. 
$$

This concluces the description of the [[natural deduction]] about [[objects]], [[morphisms]] and [[products]] in a [[category]] using its [[type theory]] [[syntax]]. We summarize the dictionary between [[category theory]] and [[type theory]] discussed so far [below](#DictionaryTypeTheoryCategoryTheory).


In the [next section](#SmoothSpaces) we promote our running example category $\mathcal{C}$, which admits only very few [[universal constructions]] (just [[products]]), to a richer category, the [[sheaf topos]] over it. That richer category then accordingly comes with a richer [[syntax]] of [[natural deduction]] inside it, namely with full [[dependent type theory]]. This we discuss in the [Syn Layer below](#SmoothSpacesLayerSyn).


#### Natural deduction rules for dependent sum types
 {#DependentSumTypes}

(...) [[dependent sum type]] (...)


#### Dictionary: type theory / category theory
 {#DictionaryTypeTheoryCategoryTheory}


The dictionary between [[dependent type theory|dependent]] [[type theory]] with [[product types]] and [[category theory]] of categories with [[products]].

[[!include judgements for types and terms - table]]

$\,$

[[!include substitution natural deduction - table]]

$\,$

[[!include product natural deduction - table]]

$\,$


[[!include dependent sum natural deduction - table]]


Below in [Smooth spaces - Syntactic Layer](#SmoothSpacesLayerSyn) we complete this dictionary to one between [[dependent type theory]] with [[dependent products]] and [[toposes]].


## **Smooth spaces**
 {#SmoothSpaces}

In the section _[Coordinate systems](#CoordinateSystems)_ we have set up the archetypical [[spaces]] of [[differential geometry]]. Here we now define in terms of these the most general _[[smooth spaces]]_ that differential geometry can deal with. We also discuss basic properties of these smooth spaces, all in the [Mod Layer](#SmoothSpacesLayerMod).

In the [Sem Layer](SmoothSpacesLayerSem) we discuss smooth spaces as a _[[topos]]_ and in fact as a _[[cohesive topos]]_. This is essentially the stage on which all of the fellowing developments take place. Or rather, the refinement of this to a _[[(infinity,1)-topos|higher topos]]_ is, which we discuss further below in the chapter _[Smooth ∞-Groupoids](#SmoothnGroupoids)_.


### Model Layer
 {#SmoothSpacesLayerMod}

In this [Model Layer](#LayerMod) we discuss concretely the definition of [[smooth spaces]] and of  [[homomorphisms]] between them,  together with basic examples and properties.

#### Plots of smooth spaces and their gluing
 {#PlotsOfSmoothSpacesAndTheirGluing}

The general kind of "[[smooth space]]" that we want to consider is a [[type|something]] that can be _probed_ by laying out coordinate systems as in def. \ref{CartesianSpacesAndSmoothFunctions} inside it, and that can be obtained by _gluing_ all the possible coordinate systems in it together. 

At this point we want to impose no further conditions on a "space" than this. In particular we do not assume that we know beforehand a [[set]] of [[points]] underlying $X$. Instead, we define smooth spaces $X$ entirely _operationally_ as something about which we can ask "Which ways are there to lay out $\mathbb{R}^n$ inside $X$?" and such that there is a self-consistent answer to this question. The following definitions make precise what we mean by this. The reader wishing to see more motivational discussion first might look at _[[motivation for sheaves, cohomology and higher stacks|conceptual exposition]]_.

For brevity we will refer "a way to lay out a coordinate system in $X$" as a _plot_ of $X$. The first set of consistency conditions on plots of a space is that they respect _coordinate transformations_. This is what the following definition formalizes.

+-- {: .num_defn #SmoothPreSpace}
###### Definition

A **smooth pre-space $X$ is 

1. a collection of sets: for each [[Cartesian space]] $\mathbb{R}^n$ (hence for each [[natural number]] $n$) a [[set]] 

   $$
     X(\mathbb{R}^n) \in Set
   $$  

   -- to be thought of as the _set of ways of laying out $\mathbb{R}^n$ inside $X$_;

1. for each abstract coordinate transformation, hence for each [[smooth function]] $f : \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ a [[function]] between the corresponding sets

   $$
     X(f) : X(\mathbb{R}^{n_2}) \to X(\mathbb{R}^{n_1})
   $$

   -- to be thought of as the function that sends a _plot_ of $X$ by $\mathbb{R}^{n_2}$ to the correspondingly transformed plot by $\mathbb{R}^{n_1}$ induced by laying out $\mathbb{R}^{n_1}$ inside $\mathbb{R}^{n_2}$.

such that this is compatible with coordinate transformations:

1. the [[identity]] coordinate transformation does not change the plots:

   $$
     X(id_{\mathbb{R}^n}) = id_{X(\mathbb{R}^n)}
     \,,
   $$

1. changing plots along two consecutive coordinate transformations $f_1 \colon \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ and $f_2 \colon \mathbb{R}^{n_2} \to \mathbb{R}^{n_3}$ is the same as changing them along the [[composition|composite]] coordinate transformation $f_2 \circ f_1$:

   $$
     X(f_1) \circ X(f_2)  = X(f_2 \circ f_1)
     \,.
   $$
   
=--

But there is one more consistency condition for a collection of plots to really be probes of some space: it must be true that if we glue small coordinate systems to larger ones, then the plots by the larger ones are the same as the plots by the collection of smaller ones that agree where they overlap. We first formalize this idea of "plots that agree where their coordinate systems overlap."

+-- {: .num_defn #MatchingFamiliesOfPlots}
###### Definition

Let $X$ be a smooth pre-space, def. \ref{SmoothPreSpace}.
For $\{U_i \to \mathbb{R}^n\}_{i \in I}$ a differentially [[good open cover]], def. \ref{DifferentiallyGoodOpenCover}, let 

$$
  GluedPlots(\{U_i \to \mathbb{R}^n\}, X) \in Set
$$

be the set of $I$-[[tuples]] of $U_i$-plots of $X$ which coincide on all double [[intersections]] 

$$  
  \array{
    && U_i \cap U_j
    \\
    & {}^{\mathllap{\iota_i}}\swarrow && \searrow^{\mathrlap{\iota_j}}
    \\
    U_i &&&& U_j
    \\
    & \searrow && \swarrow
    \\
    && \mathbb{R}^n
  }
$$ 

(also called the _[[matching families]]_ of $X$ over the given cover):

$$
  GluedPlots(\{U_i \to \mathbb{R}^n\}, X)
  \;\;\coloneqq\;\;
  \left\{
    \;
    \left(p_i \in X(U_i)\right)_{i \in I}
    \;|\;\;
    \forall_{i,j \in I} \;:\; X(\iota_i)(p_i) = X(\iota_j)(p_j)
    \;
  \right\}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

In def. \ref{MatchingFamiliesOfPlots} the [[equation]]

$$ 
  X(\iota_i)(p_i) = X(\iota_j)(p_j)
$$

says in words:

> The plot $p_i$ of $X$ by the coordinate system $U_i$ inside the bigger coordinate system $\mathbb{R}^n$ coincides with the plot $p_j$ of $X$ by the other coordinate system $U_j$ inside $X$ when both are restricted to the [[intersection]] $U_i \cap U_j$ of $U_i$ with $U_j$ inside $\mathbb{R}^n$.

=--

+-- {: .num_remark #NaiveDescentMorphism}
###### Remark

For each differentially good open cover $\{U_i \to X\}_{i \in I}$ and each smooth pre-space $X$, def. \ref{SmoothPreSpace}, there is a canonical [[function]]

$$
  X(\mathbb{R}^n) \to GluedPlots(\{U_i \to \mathbb{R}^n\}, X)
$$

from the set of $\mathbb{R}^n$-plots of $X$ to the set of tuples of glued plots, which sends a plot $p \in X(\mathbb{R}^n)$ to its restriction to all the $\phi_i \colon U_i \hookrightarrow \mathbb{R}^n$:

$$
  p \mapsto (X(\phi_i)(p))_{i \in I}
  \,.
$$

=--

If $X$ is supposed to be consistently probable by coordinate systems, then it must be true that the set of ways of laying out a coordinate system $\mathbb{R}^n$ inside it coincides with the set of ways of laying out tuples of glued coordinate systems inside it, for each good cover $\{U_i \to \mathbb{R}^n\}$ as above. Therefore:

+-- {: .num_defn #SmoothSpace}
###### Definition

A smooth pre-space $X$, def. \ref{SmoothPreSpace} is a **[[smooth space]]** if for all differentially good open covers $\{U_i \to \mathbb{R}^n\}$, def. \ref{DifferentiallyGoodOpenCover}, the canonical function of remark \ref{NaiveDescentMorphism} from plots to glued plots is a [[bijection]]

$$
  X(\mathbb{R}^n) \stackrel{\simeq}{\to} GluedPlots(\{U_i \to \mathbb{R}^n\}, X)
  \,.
$$

=--

+-- {: .num_remark #OnTheNotionOfSmoothSpaces}
###### Remark

We may think of a [[smooth space]] as being a kind of [[space]] whose _local models_ (in the general sense discussed at _[[geometry]]_) are [[Cartesian spaces]]: 

while definition \ref{SmoothSpace} explicitly says that a smooth space is something that is _consistently probeable_ by such local models; by a [[category theory|general abstract]] fact -- which we discuss in more detail below in _[Smooth Spaces - Semantic Layer](#SmoothSpacesLayerSem)_  -- that is sometimes called the [[co-Yoneda lemma]] it follows in fact that smooth spaces are precisely the objects that are obtained by 
_gluing coordinate systems_ together.

For instance we will see that two open 2-balls $\mathbb{R}^2 \simeq D^2$ along a common rim yields the smooth space version of the [[sphere]] $S^2$, a basic example of a [[smooth manifold]]. But before we examine such explicit constructions, we discuss here for the moment more general properties of smooth spaces. The reader instead wishing to see more of these concrete examples at this point should jump ahead to _[Smooth Spaces - Outlook](#SmoothSpacesOutlook)_.

=--

But the following most basic example we consider right now:

+-- {: .num_example #CartesianSpaceAsSmoothSpace}
###### Example

For $n \in \mathbb{R}^n$, there is a [[smooth space]], def. \ref{SmoothSpace}, whose set of plots over the abstract coordinate systems $\mathbb{R}^k$ is the set

$$
  CartSp(\mathbb{R}^k, \mathbb{R}^n) \in Set
$$ 

of [[smooth functions]] from $\mathbb{R}^k$ to $\mathbb{R}^n$.

Clearly this is the rule for plots that characterize $\mathbb{R}^n$ itself as a smooth space, and so we will just denote this smooth space by the same symbols "$\mathbb{R}^n$":

$$
  \mathbb{R}^n \colon \mathbb{R}^k \mapsto CartSp(\mathbb{R}^k, \mathbb{R}^n)
  \,.
$$

In particular the [[real line]] $\mathbb{R}$ is this way itself a [[smooth space]].

=--


In a moment we find a formal justification for this slight abuse of notation.

Another basic class of examples of smooth spaces are the [[discrete space|discrete]] smooth spaces:

+-- {: .num_defn #DiscreteSmoothSpace}
###### Definition

For $S \in $ [[Set]] a set, write

$$
  Disc S \in Smooth0Type
$$

for the smooth space whose set of $U$-plots for every $U \in CartSp$ is always $S$.

$$
  Disc S \colon U \mapsto S
$$

and which sends every coordinate transformation $f \colon \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ to the identity function on $S$.

A smooth space of this form we call a **[[discrete object|discrete smooth space]]**.

=--



More examples of smooth spaces can be built notably by [[intersection|intersecting]] [[images]] of two smooth spaces inside a bigger one. In order to say this we first need a formalization of [[homomorphism]] of smooth spaces. This we turn to now.


#### Homomorphisms of smooth spaces
 {#HomomorphismsOfSmoothSpaces}

We discuss "functions" or "maps" between [[smooth spaces]], def. \ref{SmoothSpace}, which preserve the smooth space [[structure]] in a suitable sense. As with any notion of function that preserves structure, we refer to them as _[[homomorphisms]]_.

The idea of the following definition is to say that whatever a [[homomorphism]] $f : X \to Y$ between two smooth spaces is, it has to take the plots of $X$ by $\mathbb{R}^n$ to a corresponding plot of $Y$, such that this respects coordinate transformations.

+-- {: .num_defn #HomomorphismOfSmoothSpaces}
###### Definition

Let $X$ and $Y$ be two smooth spaces, def. \ref{SmoothSpace}. Then a [[homomorphism]] $f \colon X \to Y$ is

* for each abstract coordinate system $\mathbb{R}^n$ (hence for each $n \in \mathbb{N}$) a [[function]]

  $f_{\mathbb{R}^n} : X(\mathbb{R}^n) \to Y(\mathbb{R}^n)$

  that sends $\mathbb{R}^n$-plots of $X$ to $\mathbb{R}^n$-plots of $Y$ 

such that 

* for each [[smooth function]] $\phi : \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ we have

  $$
    Y(\phi) \circ f_{\mathbb{R}^{n_1}} = f_{\mathbb{R}^{n_2}} \circ X(\phi)
  $$   

  hence a [[commuting diagram]]

  $$
    \array{
      X(\mathbb{R}^{n_1}) &\stackrel{f_{\mathbb{R}^{n_1}}}{\to}& Y(\mathbb{R}^{n_1})
      \\
      \downarrow^{\mathrlap{X(\phi)}} && \downarrow^{\mathrlap{Y(\phi)}}
      \\
      X(\mathbb{R}^{n_2}) &\stackrel{f_{\mathbb{R}^{n_2}}}{\to}& Y(\mathbb{R}^{n_1})
    }
    \,.
  $$

For $f_1 : X \to Y$ and $f_2 : X \to Y$ two homomorphisms of smooth spaces, their [[composition]] $f_2 \circ f_1 \colon X \to Y$ is defined to be the homomorphism whose component over $\mathbb{R}^n$ is the composite of functions of the components of $f_1$ and $f_2$:

$$
  (f_2\circ f_1)_{\mathbb{R}^n} \coloneqq {f_2}_{\mathbb{R}^n} \circ {f_1}_{\mathbb{R}^n}
  \,.
$$

=--

+-- {: .num_defn}
###### Definition

Write $Smooth0Type$ for the [[category]] whose [[objects]] are [[smooth spaces]], def. \ref{SmoothSpace}, and whose [[morphisms]] are homomorphisms of smooth spaces, def. \ref{HomomorphismOfSmoothSpaces}.

=--

At this point it may seem that we have now _two different_ notions for how to lay out a coordinate system in a smooth space $X$: on the hand, $X$ comes by definition with a rule for what the set $X(\mathbb{R}^n)$ of its $\mathbb{R}^n$-plots is. On the other hand, we can now regard the abstract coordinate system $\mathbb{R}^n$ itself as a smooth space, by example \ref{CartesianSpaceAsSmoothSpace}, and then say that an  $\mathbb{R}^n$-plot of $X$ should be a homomorphism of smooth spaces of the form $\mathbb{R}^n \to X$.

The following proposition says that these two superficially different notions actually naturally coincide. 

+-- {: .num_prop #YonedaForSmoothSpaces}
###### Proposition

Let $X$ be any [[smooth space]], def. \ref{SmoothSpace}, and regard the abstract coordinate system $\mathbb{R}^n$ as a smooth space, by example \ref{CartesianSpaceAsSmoothSpace}. There is a [[natural bijection]]

$$
  X(\mathbb{R}^n) \simeq Hom_{Smooth0Type}(\mathbb{R}^n, X)
$$

between the _postulated_ $\mathbb{R}^n$-plots of $X$ and the _actual_ $\mathbb{R}^n$-plots given by homomorphism of smooth spaces $\mathbb{R}^n \to X$.

=--

+-- {: .proof}
###### Proof

This is a special case of the _[[Yoneda lemma]]_, as will be made more explicit below in _[The topos of smooth spaces](#ToposOfSmoothSpaces)_. 
The reader unfamiliar with this should write out the simple proof explicitly: use the defining [[commuting diagrams]] in def. \ref{HomomorphismOfSmoothSpaces} to deduce that a homomorphism $f : \mathbb{R}^n \to X$ is uniquely fixed by the image of the [[identity]] element in  $\mathbb{R}^n(\mathbb{R}^n) \coloneqq CartSp(\mathbb{R}^n, \mathbb{R}^n)$ under the component function $f_{\mathbb{R}^n} : \mathbb{R}^n(\mathbb{R}^n) \to X(\mathbb{R}^n)$.

=--

+-- {: .num_example #SmoothFunctionOnSmoothSpace}
###### Example

Let $\mathbb{R} \in Smooth0Type$ denote the [[real line]], regarded as a [[smooth space]] by def. \ref{CartesianSpaceAsSmoothSpace}. Then for $X \in Smooth0Type$ any smooth space, a homomorphism of smooth spaces

$$
  f \colon X \to \mathbb{R}
$$

is a _[[smooth function]] on $X$_. Prop. \ref{YonedaForSmoothSpaces} says here that when $X$ happens to be an abstract coordinate system regarded as a smooth space by def. \ref{CartesianSpaceAsSmoothSpace}, then this general notion of smooth functions between smooth spaces reproduces the basic notion of def, \ref{CartesianSpaceAndHomomorphism}.

=--

+-- {: .num_defn #PointsOfASmoothSpace}
###### Definition

The 0-[[dimension|dimensional]] abstract coordinate system $\mathbb{R}^0$ we also call the **[[point]]** and regarded as a smooth space we will often write it as

$$
  * \in Smooth0Type
  \,.
$$

For any $X \in Smooth0Type$, we say that a homomorphism

$$
  x \colon * \to X
$$ 

is a **point of $X$**.

=--

+-- {: .num_remark}
###### Remark

By prop. \ref{YonedaForSmoothSpaces} the points of a smooth space $X$ are naturally identified with its 0-dimensional plots, hence with the "ways of laying out a 0-dimensional coordinate system" in $X$:

$$
  Hom(*, X) \simeq X(\mathbb{R}^0)
  \,.
$$

=--


#### Products and fiber products of smooth spaces
 {#ProductsAndFiberProductsOfSmoothSpaces}

+-- {: .num_defn #ProductOfSmoothSpaces}
###### Definition

Let $X, Y \in Smooth0Type$ by two smooth spaces. Their **[[product]]** is the smooth space $X \times Y \in Smooth0Type$ whose plots are pairs of plots of $X$ and $Y$:

$$
  X\times Y (\mathbb{R}^n) \coloneqq X(\mathbb{R}^n) \times Y(\mathbb{R}^n)
  \;\;
  \in Set
  \,.
$$

The **projection on the first factor** is the homomorphism

$$
   p_1 \colon X \times Y \to X
$$

which sends $\mathbb{R}^n$-plots of $X \times Y$ to those of $X$ by forming the projection of the [[cartesian product]] of sets:

$$
  {p_1}_{\mathbb{R}^n} \colon X(\mathbb{R}^n) \times Y(\mathbb{R}^n) \stackrel{p_1}{\to} X(\mathbb{R}^n)
  \,.
$$

Analogously for the **projection to the second factor**

$$
  p_2 \colon X \times Y \to Y
  \,.
$$

=--

+-- {: .num_prop #ProductOfSmoothSpaceWithThePoint}
###### Proposition

Let $* = \mathbb{R}^0$ be the [[point]], regarded as a smooth space, def. \ref{PointsOfASmoothSpace}. Then for $X \in Smooth0Type$ any smooth space the canonical projection homomorphism

$$
  X \times * \to X
$$

is an [[isomorphism]].

=--

+-- {: .num_defn}
###### Definition

Let $f \colon X \to Z$ and $g \colon Y \to Z$ be two [[homomorphisms]] of smooth spaces, def. \ref{HomomorphismOfSmoothSpaces}. There is then a new smooth space to be denoted 

$$
  X \times_Z Y \in Smooth0Type
$$ 

(with $f$ and $g$ understood), called the [[fiber product]] of $X$ and $Y$ along $f$ and $g$, and defined as follows:

the set of $\mathbb{R}^n$-plots of $X \times_Z Y$ is the set of pairs of plots of $X$ and $Y$ which become the same plot of $Z$ under $f$ and $g$, respectively:

$$
  (X \times_Z Y)(\mathbb{R}^n)
  =
  \left\{
    (p_X \in X(\mathbb{R}^n), p_Y \in Y(\mathbb{R}^n))
    \; |\;
    X(f)(p_X) = Y(g)(p_Y)
  \right\}
  \,.
$$

=--



#### Smooth mapping spaces and smooth moduli spaces
 {#SmoothMappingSpaces}


+-- {: .num_defn #SmoothFunctionSpace}
###### Definition

Let $\Sigma, X \in Smooth0Type$ be two [[smooth spaces]], def. \ref{#SmoothSpace}. Then the **smooth [[mapping space]]** 

$$
  [\Sigma,X] \in Smooth0Type
$$ 

is the [[smooth space]] defined by saying that its set of $\mathbb{R}^n$-plots is

$$
  [\Sigma, X](\mathbb{R}^n)
   \coloneqq
  Hom(\Sigma \times \mathbb{R}^n, X)
  \,.
$$

=--

Here in $\Sigma \times \mathbb{R}^n$ we first regard the abstract coordinate system $\mathbb{R}^n$ as a smooth space by example \ref{CartesianSpaceAsSmoothSpace} and then we form the [[product]] smooth space by def. \ref{ProductOfSmoothSpaces}.

+-- {: .num_remark #NatureOfPlotsOfMappingSpace}
###### Remark

This means in words that a $\mathbb{R}^n$-plot of the [[mapping space]] $[\Sigma,X]$ is a smooth $\mathbb{R}^n$-parameterized _family_ of homomorphisms $\Sigma \to X$.

=--


+-- {: .num_prop #UniversalPropertyOfMappingSpace}
###### Proposition

There is a [[natural bijection]]

$$
  Hom(K, [\Sigma, X])
  \simeq
  Hom(K \times \Sigma, X)  
$$

for every smooth space $K$.

=--

+-- {: .proof}
###### Proof

With a bit of work this is straightforward to check explicitly by unwinding the definitions. It follows however from [[category theory|general abstract]] results once we realize that $[-,-]$ is of course the _[[internal hom]]_ of smooth spaces. This we come to below in _[Smooth spaces - Semantic Layer](#SmoothSpacesLayerSem)_.

=--


+-- {: .num_remark #MappingSpaceAsModuliSpace}
###### Remark

This says in words that a smooth function from any $K$ into the mapping space $[\Sigma,X]$ is equivalently a smooth function from $K \times \Sigma$ to $X$. The latter we may regard as a _$K$-parameterized smooth family_ of smooth functions $\Sigma \to X$. Therefore in view of the previous remark \ref{NatureOfPlotsOfMappingSpace} this says that smooth mapping spaces have a [[universal property]] not just over abstract coordinate systems, but over all smooth spaces.

We will therefore also say that $[\Sigma,X]$ is the **smooth [[moduli space]]** of smooth functions from $\Sigma \to X$, because it is such that smooth maps $K \to [\Sigma,X]$ into it _modulate_, as we move around on $K$, a family of smooth functions $\Sigma\to X$, depending on $K$.

=--

First interesting examples of such smooth moduli spaces are discussed in _[Differential forms -- Model Layer](#DifferentialFormsLayerMod)_ below. Many more interesting examples follow once we pass from smooth 0-types to smooth $n$-types below in _[Smooth n-groupoids](#SmoothnGroupoids)_. 

We will see many more examples of smooth moduli spaces, starting below in _[Differential forms - Model Layer](#DifferentialFormsLayerMod)_.

+-- {: .num_prop #UnderlyingSetOfSmoothMappingSpace}
###### Proposition

The set of points, def. \ref{PointsOfASmoothSpace}, of a smooth mapping space $[\Sigma,X]$ is the bare set of homomorphism $\Sigma \to X$: there is a [[natural isomorphism]]

$$
  Hom(*, [\Sigma, X]) \simeq Hom(\Sigma, X)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Combine prop. \ref{UniversalPropertyOfMappingSpace} with prop. \ref{ProductOfSmoothSpaceWithThePoint}.

=--


+-- {: .num_example #SmoothPathSpace}
###### Example

Given a [[smooth space]] $X \in Smooth0Type$, its smooth **[[path space]]** is the smooth mapping space

$$
  \mathbf{P}X \coloneqq [\mathbb{R}^1, X]
  \,.
$$ 

By prop. \ref{UnderlyingSetOfSmoothMappingSpace} the points of $P X$ are indeed precisely the smooth trajectories $\mathbb{R}^1 \to X$. But $P X$ also knows how to _smoothly vary_ such smooth trajectories. 

This is central for [[variational calculus]] which determines [[equations of motion]] in [[physics]]. This we turn to below in _[Variational calculus](#VariationalCalculus)_.

=--

+-- {: .num_remark}
###### Remark

In [[physics]], if $X$ is a model for [[spacetime]], then $P X$ may notably be interpreted as the smooth space of [[worldlines]] _in_ $X$, hence the smooth space of paths or _trajectories_ of a [[particle]] in $X$. 

=-- 

#### The smooth moduli space of smooth functions
 {#SmoothModuliSpaceOfSmoothFunctions}


In example \ref{SmoothFunctionOnSmoothSpace} we saw that a smooth function on a general [[smooth space]] $X$ is a homomorphism of smooth spaces, def. \ref{HomomorphismOfSmoothSpaces}

$$
  f \colon X \to \mathbb{R}
  \,.
$$

The collection of these forms the [[hom-set]] $Hom_{Smooth0Type}(X, \mathbb{R})$. But by the discussion in _[Smooth mapping spaces](#SmoothMappingSpaces)_ such hom-sets are naturally refined to smooth spaces themselves.

+-- {: .num_defn}
###### Definition

For $X \in Smooth0Type$ a [[smooth space]], we say that the **moduli space of smooth functions** on $X$ is the smooth mapping space (def. \ref{SmoothFunctionSpace})

$$
  [X, \mathbb{R}] \in Smooth0Type
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

We call this a _[[moduli space]]_ because by prop. \ref{UniversalPropertyOfMappingSpace} above and in the sense of remark \ref{MappingSpaceAsModuliSpace} it is such that smooth functions into it _modulate_ smooth functions $X \to \mathbb{R}$.

By prop. \ref{UnderlyingSetOfSmoothMappingSpace} a point $* \to [X,\mathbb{R}^1]$ of the moduli space is equivalently a smooth function $X \to \mathbb{R}^1$.

=--



#### Outlook
 {#SmoothSpacesOutlook}

(...)

+-- {: .num_remark}
###### Remark

Later we define/see the following:

* A _[[smooth manifold]]_  is a [[smooth space]] that is [[covering|locally]] _[[equivalence|equivalent]]_ to a [[coordinate system]];

* A _[[diffeological space]]_ is a [[smooth space]] such that every coordinate labels a [[point]] in the space. In other words, a diffeological space is a smooth space that has an underlying set $X_s \in Set$ of points such that the set of $\mathbb{R}^n$-plots is a subset of the set of all functions:

  $$
    X(\mathbb{R}^n) \hookrightarrow Functions(\mathbb{R}^n, S_s)
    \,.
  $$

  (This need not be the case in a general smooth space, important counterexamples are the _universal smooth moduli spaces of differential forms_ in [Smooth moduli space of differential forms](#SmoothUniversalModuliSpaceOfDifferentialForms)).

  

We will establish a long sequence of [[faithful functor|faithful]] inclusions 

$\{$[[coordinate systems]]$\}$ 
 $\hookrightarrow$
$\{$[[smooth manifolds]]$\}$ 
 $\hookrightarrow$
$\{$[[diffeological spaces]]$\}$ 
 $\hookrightarrow$
$\{$[[smooth spaces]]$\}$ 
 $\hookrightarrow$
$\{$[[smooth groupoids]]$\}$ 
 $\hookrightarrow \cdots $


=--



### Semantic Layer
 {#SmoothSpacesLayerSem}

In this [Semantic Layer]{#LayerSem} we mention some basic definitions of [[topos theory]] and discuss the [[topos]] formed by the [[smooth spaces]] defined in [Smooth Spaces - Mayer Mod](#SmoothSpacesLayerMod).

#### Toposes
 {#Toposes}


+-- {: .num_defn #SheafToposAsSubtopos}
###### Definition

A [[sheaf topos]] is [[subtopos]] of [[presheaf topos]]

$$
  Sh(C) 
    \stackrel{\overset{\overline{(-)}}{\leftarrow}}{\hookrightarrow}
  PSh(C)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Here the [[left adjoint]] $\overline{(-)}$, which is equivalently

* the [[inverse image]] of the [[geometric embedding]] [[geometric morphism]]

* the [[sheafification]] functor

is precisely such that for every [[covering]] $\{U_i \to U\}_{i \in I}$ in the [[site]] $C$ the [[sieve]] inclusion 

$$
  S(\{U_i\}) \hookrightarrow U \;\;\;\; \in PSh(C)
$$

(a [[dense monomorphism]]) is sent to an [[isomorphism]].

Hence the sheaf topos is the left exact [[localization]] at the covering sieve inclusions.

=--

+-- {: .num_remark}
###### Remark

The [[presheaf topos]] $PSh(C)$ is the [[free cocompletion]] of the [[category]] $C$, hence the category obtained from $C$ by [[free construction|freely]] forming [[colimits]] of its objects.

In contrast, the [[localization]] $Sh(C) \hookrightarrow PSh(C)$ enforces _relations_ between these free colimits.

Therefore in total we may think of $Sh(C)$ as obtained by [[generators and relations]] from the [[site]] $C$: 

* the objects of $C$ are the generators;

* the [[coverings]] of $C$ are the relations.

=--

Def. \ref{SheafToposAsSubtopos} is the "external" characterization of sheaf toposes. 

More intrinsically we have _[[Giraud's theorem]]_:

+-- {: .num_theorem}
###### Theorem

A [[sheaf topos]] is equivalently a [[presentable category]] with

1. [[universal colimits]]

1. [[effective quotients]]

1. [[disjoint coproducts]]

=--

This characterization, or rather its refinement to [[(infinity,1)-categories of (infinity,1)-sheaves]], is crucial, below, for the discussion of [[principal bundles]] and their [[associated bundle|associated]] [[fiber bundles]]. 

For other general considerations we need rather that every [[sheaf topos]] is in particular an _[[elementary topos]]_

+-- {: .num_defn}
###### Definition

An [[elementary topos]] is 

* a [[locally cartesian closed category]] 

* with a [[subobject classifier]].

=--

The first of these says that the [[internal language]] is [[dependent type theory]] with [[dependent sum types]] and [[dependent product types]], the second says that its has a [[type of propositions]]. This we turn to in [Smooth Spaces - Syntactic Layer](#SmoothSpacesLayerSyn) below.

#### Subobjects
 {#Subobjects}

* [[subobject]], [[subobject classifier]]

* [[truncated object in an (infinity,1)-topos|(-1)-truncation]]

#### Slice toposes
 {#SliceToposes}

* [[slice topos]]

* [[etale geometric morphism]]

#### Local, connected and cohesive toposes

* [[local topos]]

  * [[concrete object]]

* [[locally connected topos]], [[connected topos]]

  * [[connected object]]

* [[cohesive topos]]


#### The topos of smooth spaces
 {#ToposOfSmoothSpaces}

+-- {: .num_remark}
###### Remark

* A _smooth pre-space_, def. \ref{SmoothPreSpace} is equivalently a [[presheaf]] on [[CartSp]], hence a [[functor]] $X : CartSp^{op} \to Set$;

* a _[[smooth space]]_, def. \ref{SmoothSpace}, is equivalently a presheaf on [[CartSp]] which is a [[sheaf]] with respect to the differentially [[good open cover]]-[[coverage]]:

  * the set of "glued plots", def. \ref{MatchingFamiliesOfPlots} is the [[descent object]];

  * the canonical morphism of remark \ref{NaiveDescentMorphism} is the [[descent morphism]];

  * the condition that it be an isomorphism (for each differentially good open cover) is the [[descent]]- or [[sheaf]] condition.

=--


The [[sheaf topos]], def. \ref{SheafToposAsSubtopos}, of [[smooth spaces]] enjoys a few crucial properties: it is

* a [[locally connected topos|locally connected]] and [[connected topos]]

* a [[local topos]]

* a [[cohesive topos]]. This we discuss in the remainder of this [Semantic Layer](#LayerSem).


##### Connectedness 
 {#ConnectedSmooth0Type}

The full [[sheaf topos]] $Sh(CartSp)$ on [[CartSp]] is a [[locally connected topos]] in that the terminal [[global section]] [[geometric morphism]] to [[Set]] is an [[essential geometric morphism]]:

$$
  Sh(CartSp)
  \stackrel{\overset{\Pi_0}{\to}}{\stackrel{\overset{L Const}{\leftarrow}}{\underset{\Gamma}{\to}}}
  Set
$$

The extra [[left adjoint]] $\Pi_0 : Sh(CartSp) \to Set$ sends diffeological spaces to the set of path-[[connected]] components of their underlying [[topological space]]s.


+-- {: .num_prop}
###### Proposition

The [[sheaf topos]] $Sh(CartSp)$ on [[CartSp]] is a [[locally connected topos]].

=--

+-- {: .proof}
###### Proof

The following argument works for every [[site]] $C$ which is such that constant presheaves on $C$ are already sheaves.

Notice that this is the case for $C = CartSp$ because every Cartesian space is connected: for $S \in Set$ a compatible family of elements of $Const S$ on a cover $\{U_i \to \mathbb{R}^n\}$ of some $\mathbb{R}^n$ is an element of $S$ on each patch, such that their restriction maps to intersections of patches coincide. But the restriction maps are all identities, so this says that all these elements coincide. Therefore the set of compatible families is just the set $S$ itself, hence the presheaf $Const S$ is a sheaf.

So with $L : PSh(C) \to Sh(C)$ the [[sheafification]] functor we have that $L Const S \simeq Const S$.

Whenever this is the case the [[left adjoint]] to the constant presheaf functor, which always exists for presheaves and is given by the [[colimit]] functor, is also left adjoint on the level of sheaves, because for each $X \in Sh(C)$ and $S \in Set$ we have natural bijections

$$
  \begin{aligned}
    Hom_{Sh(C)}(X, L Const S)
    & =
    Hom_{PSh(C)}(X, L Const S)
    \\
    & \simeq
    Hom_{PSh(C)}(X, Const S)
    \\
    & \simeq
    Hom_{Set}(\lim_\to X, S)
  \end{aligned}
  \,.
$$

=--

+-- {: .num_defn}
###### Definition

Write $\Pi_0 := \lim_\to : Sh(CartSp) \to Set$
for the [[left adjoint]] to $LConst : Set \stackrel{Const}{\to} PSh(C) \stackrel{L}{\to} Sh(C)$.

=--

+-- {: .num_prop}
###### Proposition

For $X \in Sh(C)$ a diffeological space, $\Pi_0(X)$ is the set of path-connected components of the topological space underlying $X$.

=--

+-- {: .proof}
###### Proof

By the [[co-Yoneda lemma]] we may write 

$$
  X = {\lim_\to}_{(U \to X) \in y/X} U
$$

and since $\Pi_0$ commutes with colimits we have

$$
  \Pi_0(X) \simeq 
  \Pi_0 {\lim_\to}_{(U \to X)} U
  \simeq
  {\lim_\to}_{(U \to X)} \Pi_0(U)
  \,.
$$

But also by the co-Yoneda lemma we have that the [[colimit]] over any [[representable functor|representable]] is the singleton set, hence our expression

$$
  \cdots \simeq 
  {\lim_\to}_{(U \to X)} *
$$

is the colimit over the category of plots of $X$ of the functor that is constant on the point. This colimit is the [[coproduct]] of points over the connected components of the [[diagram]] category.

The connected components of the category of plots $y/X$ are the path-connected (or "plot-connected") components of the underlying topological space of $X$.



=--


+-- {: .num_prop}
###### Proposition

The [[sheaf topos]] $Sh(CartSp)$ on [[CartSp]] is actually a [[connected topos]].

=--

+-- {: .proof}
###### Proof

Since $CartSp$ is a [[connected category]] it is immediate that $Const \colon Set \to PSh(CartSp)$ is a [[full and faithful functor]]. By the above this equals $L Const$, which is hence also full and faithful.

By the discussion at [[connected topos]] we could equivalently convince ourselves that $\Pi_0$ preserves the terminal object. The terminal object of $Sh(CartSp)$ is $y(\mathbb{R}^0)$, hence representable. By the above, $\Pi_0$ sends all representable objects to the singleton set, which is the terminal object of $Set$. 

=--

##### Locality 
 {#LocalSmooth0Type}


+-- {: .num_prop}
###### Proposition


The [[sheaf topos]] $Sh(CartSp)$ is also a [[local topos]]

$$
  (L Const \dashv \Gamma \dashv CoDisc)
  :
  Sh(CartSp) \stackrel{\overset{L Const}{\leftarrow}}{\stackrel{\overset{\Gamma}{\to}}{\underset{CoDisc}{\leftarrow}}} 
  Set
$$

=--

+-- {: .proof}
###### Proof


The [[site]] [[CartSp]] is a [[local site]]: it has a [[terminal object]] and the only [[covering]] [[sieve]] of this object is the trivial one. This implies the claim, by the discussion at [[local site]].

Concretely, the extra [[right adjoint]] $CoDisc$ takes a [[set]] $S$ to the presheaf given by the assigmnent

$$
  CoDisc(S) : U \mapsto Hom_{Set}(CartSp(*,U), S)
  \,,
$$

that takes a Cartesian space $U$ to the set of [[function]]s from its underlying set of points to $S$. This is clearly a sheaf (a function of sets from $U$ to $S$ is clearly fixed by all its restrictions to a collections of  subsets of $U$ whose unition is $U$.)

=--

Geometrically, the object $CoDisc S \in Sh(CartSp)$ is the diffeological space [[codiscrete space|codiscrete]] (indiscrte) smooth structure.

+-- {: .num_prop}
###### Proposition

Every [[local topos]] comes with its notion of [[concrete sheaves]] that form a sub-[[quasitopos]]. For the local topos $Sh(CartSp)$ these are precisely the diffeological spaces.

$$
  Set \stackrel{\leftarrow}{\underset{CoDisc}{\hookrightarrow}}
  DiffologicalSp \stackrel{\leftarrow}{\hookrightarrow}
  Sh(CartSp)
$$


=--



+-- {: .proof}
###### Proof


The [[concrete sheaves]] for the [[local topos]] $Sh(CartSp)$ are by definition those objects $X$ for which the 
$(\Gamma \dashv CoDisc)$-[[unit of an adjunction|unit]]

$$
  X \to CoDisc \Gamma X
$$

is a [[monomorphism]]. Monomorphisms of sheaves are tested objectwise, so that means equivalently that for every $U \in CartSp$ we have that 

$$
  X(U) \simeq Hom_{Sh}(U,X) \to Hom_{Sh}(U, Codisc \Gamma X)
  \simeq Hom_{Set}(\Gamma U, \Gamma X)
$$

is a monomorphism. This is precisely the condition on a sheaf to be a diffeological space.

=--



##### Cohesion
 {#CohesionOfTheToposOfSmoothSpaces}


+-- {: .num_prop}
###### Proposition

The [[sheaf topos]] $Sh(CartSp)$ is even a [[cohesive topos]] in which the axiom _[pieces have points](/nlab/show/cohesive+topos#PiecesHavePoints)_ holds.

=--

+-- {: .proof}
###### Proof

The [[site]] [[CartSp]] is a [[cohesive site]] (see there for detail). This implies the statement.

=--

This implies that $Sh(CartSp)$ is a [[locally connected topos]], [[connected topos]], [[local topos]]. It means in addition that it is also a [[strongly connected topos]].

This means that there is a _homotopy category_ or _concordance category_ of [[smooth spaces]], with the same objects as $Sh(CartSp)$, but with hom-sets given by

$$
  Conc(X,Y) := \Pi_0 [X,Y]_{Sh(CartSp)}
 \,,
$$

where $[X,Y]_{Sh(CartSp)}$ is the [[internal hom]] in the [[cartesian closed category]] $Sh(CartSp)$.




### Syntactic Layer
 {#SmoothSpacesLayerSyn}

In this [Syntactic Layer](#LayerSyn) we discuss the two further aspects that the [[internal language]] of a [[topos]] adds to the internal language of a just a category with [[finite products]] (which is the [[dependent type theory|dependent]] [[type theory]] with [[unit type]] and [[product type]] discussed in _[Coordinate systems - Syntactic Layer](#CoordinateSystemsLayerSyn)): [[dependent product types]] and a [[type of propositions]].

[[dependent type theory]] $\leftrightarrow$ [[locally cartesian closed category]]

[[type of propositions]] $\leftrightarrow$ [[subobject classifier]]

(...)


#### Type theory of a topos

##### Natural deduction rules for dependent product types
 {#NaturalDeductionForDependentProduct}

[[!include dependent product natural deduction - table]]

In the special case that $A$ does not actually deopend on $X$:

[[!include function type natural deduction - table]]

##### Internal logic of a topos

What is called _[[logic]]_ is the [[syntax]] for [[n-truncated object in an (infinity,1)-category|(-1)-truncated objects]] in [[slice categories]], hence of [[monomorphisms]] regarded as objects of slice categories.

(...)

* [[propositions as types]], [[programs as proofs]]

* [[computational trinitarianism]]

* [[type of propositions]]

#### Modal type theory

##### Modalities

* [[modal logic]], [[modal type theory]]

* [[monad (in computer science)]]

##### Sharp modality and Codiscrete types

+-- {: .num_defn #SharpModalityOfLocalTopos}
###### Definition

Let $\mathbf{H}$ be a [[local topos]]

$$
  \mathbf{H}
   \stackrel{\stackrel{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\to}}{\underset{CoDisc}{\leftarrow}}}
  \,.
$$

Write

$$
  (\flat \dashv \sharp)
  \;
  \colon
  \;
  \mathbf{H}
  \stackrel{\overset{Disc}{\leftarrow}}{\underset{\Gamma}{\to}}
  \, .
  \stackrel{\overset{\Gamma}{\leftarrow}}{\underset{coDisc}{\to}}
  \, .
$$

for the induced [[adjoint functor|adjoint]] [[monad]] $\sharp$ and [[comonad]] $\flat$. We 

* call $\sharp$ the **sharp modality**;

* call $\flat$ the **flat modality**.

=--

The term _modality_ refers to _[[modal logic]]_. (...)

+-- {: .num_remark}
###### Remark

We refer to $\sharp A$ as the **sharp type** of $A$. 
This may be thought of as referring to the fact that by [[adjunction]] a homomorphism
$X \to \sharp A$ is equivalently a function
$\Gamma X \to \Gamma A$ of the underlying sets. This means that smooth maps $X \to \sharp A$ are like maps into $A$ that do _not_ have to respect the cohesive structure on $A$, but instead 
can be arbitrarily "kinky" ("sharp").

=--

This motivates the following terminology.

+-- {: .num_defn #Decohese}
###### Definition

We write

$$
  DeCoh_X \colon X \to \sharp X
$$

For the [[unit of an adjunction|unit]] of the $(\Gamma \vdash coDisc)$-[[adjunction]].

=--


(...)



## **Differential forms**
 {#DifferentialForms}


We introduce the standard concept of _[[nLab:differential forms]]_ in _[Model Layer](#DifferentialFormsLayerMod)_, adding to the traditional discussion a precise version of the statement that differential forms are equivalently "incremental smooth $n$-dimensional measures", which accurately captures the role that they play in [[physics]], notably in [[local action functionals]].

We define differential forms on general smooth spaces seamlessly in terms of the smooth [[moduli space]] $\Omega^\in \in Smooth0Type$ of differential forms. This has the special property that it is, for $n \geq 1$, a _non-[[concrete object|concrete]]_ smooth space. In _[Semantic Layer](#DifferentialFormsLayerSem)_ below we take this as occasion to discuss the notion of [[concrete objects]] in a [[local topos]], such as the topos of smooth spaces. We show how the _concretification_ of the smooth mapping space $[X,\Omega^n]$ for any smooth space $X$ is the _smooth (moduli) space of differential forms on $X$_. Below in _[Action functionals for Chern-Simons type gauge theories](#ActionFunctionalsForChernSimonsTypeGaugeTheories)_ the theory of _concretification_ in a local topos is a central ingredient in the _canonical existence_ of certain [[nLab:action functionals]].

The process of concretification involves the general abstract notion of _[[image|images]]_. The type-theory of this notion we discuss in [Syntactic Layer](#DifferentialFormsLayerSyn) here.


### Model Layer
 {#DifferentialFormsLayerMod}

We have seen above in _[The continuum real (world-)line](TheContinuumRealWorldLine)_ that that [[real line]] $\mathbb{R}$ is the basic [[kinematics|kinematical structure]] in the [[differential geometry]] of [[physics]]. Notably the smooth [[path spaces]] $[\mathbb{R}, X]$ from example \ref{SmoothPathSpace} are to be thought of as the smooth spaces of _trajectories_ (for instance of some [[particle]]) in a [[smooth space]] $X$, hence of smooth maps $\mathbb{R} \to X$.

But moreover, _[[dynamics]]_ in [[physics]]  is encoded by _[[functionals]] on such trajectories_: by "[[action functionals]]". In the simplest case these are for instance homomorphisms of smooth spaces

$$
  S \colon \left[I, X\right] \to \mathbb{R}
  \,,
$$

where $I \hookrightarrow \mathbb{R}$ is the standard unit [[interval]].

Such [[action functionals]] we discuss in their own right in _[Variational calculus](#VariationalCalculus)_ below. Here we first examine in detail a fundamental property they all have: they are supposed to be _[[local action functional|local]]_.

Foremost this means that the value associated to a trajectory is _built up incrementally_ from small contributions associated to small sub-trajectories: if a rajectory $\gamma$ is decomposed as a trajectory $\gamma_1$ followed by a trajectory $\gamma_2$, then the action functional is additive

$$
  S(\gamma) = S(\gamma_1) + S(\gamma_2)
  \,.
$$

As one takes this property to the limit of iterative subdivision, one finds that action functionals are entirely determined by their value on _[[infinitesimal space|infinitesimal]] displacements_ along the worldline. If $\gamma \colon \mathbb{R} \to X$ denotes a path and "$\dot \gamma(x)$" denotes the corresponding "infinitesimal path" at worldline parameter $x$, then the value of the action functional on such an infinitesimal path is traditionally written as

$$
  \mathbf{d}S(\dot \gamma)_x  \in \mathbb{R}
  \,,
$$

to be read as "the small change $\mathbf{d}S$ of $S$ along the infinitesimal path $\dot \gamma_x$". 

This function $\mathbf{d}S$ that assigns numbers to infinitesimal paths is called a _[[differential form]]_. Etymologically this originates in the use of "form" as in _[[bilinear form]]_: something that is evaluated. Here it is evaluated on _infinitesimal differences_, referred to as _differentials_.



We define smooth differential forms on [[Cartesian spaces]] in 

* _[Differential forms on abstract coordinate sysetms](#DifferentialFormsOnAbstractCoordinateSystem)_

Then we discuss how this induces a notion of smooth differential forms on general [[smooth spaces]] in 

* _[Smooth universal moduli space of differential forms](#SmoothUniversalModuliSpaceOfDifferentialForms)_.

Further below we provide a precise version of the statement that "Differential 1-forms are differential measures along paths." in 

* _[Differential 1-forms are smooth incremental path measures](#1FormsAsSmoothFunctors)_.


#### Differential forms on abstract coordinate systems
 {#DifferentialFormsOnAbstractCoordinateSystem}

We introduce the basic concept of a smooth [[differential form]] on a [[Cartesian space]] $\mathbb{R}^n$. Below in _[Differential forms on smooth spaces](#SmoothUniversalModuliSpaceOfDifferentialForms)_ we use this to define differential forms on any [[smooth space]].

+-- {: .num_defn #Differential1FormsOnCartesianSpaces}
###### Definition

For $n \in \mathbb{N}$ a **[[smooth differential 1-form]]** $\omega$ on a [[Cartesian space]] $\mathbb{R}^n$ is an $n$-[[tuple]] 

$$
  \left(\omega_i \in CartSp\left(\mathbb{R}^n,\mathbb{R}\right)\right)_{i = 1}^n
$$

of [[smooth functions]], which we think of equivalently as the [[coefficients]] of a [[formal linear combination]]

$$
  \omega = \sum_{i = 1}^n f_i \mathbf{d}x^i
$$

on a [[set]] $\{\mathbf{d}x^1, \mathbf{d}x^2, \cdots, \mathbf{d}x^n\}$ of [[cardinality]] $n$.

Write 

$$
  \Omega^1(\mathbb{R}^k) \simeq CartSp(\mathbb{R}^k, \mathbb{R})^{\times k}\in Set
$$

for the set of smooth [[differential 1-forms]] on $\mathbb{R}^k$.

=--

+-- {: .num_remark}
###### Remark

We think of $\mathbf{d} x^i$ as a measure for [[infinitesimal space|infinitesimal]] displacements along the $x^i$-[[coordinate]] of a [[Cartesian space]]. This idea is made precise below in _[Differential 1-forms are smooth increnemental path measures](#1FormsAsSmoothFunctors)_.

=--

If we have a measure of infintesimal displacement on some $\mathbb{R}^n$ and a smooth function $f \colon \mathbb{R}^{\tilde n} \to \mathbb{R}^n$, then this induces a measure for infinitesimal displacement on $\mathbb{R}^{\tilde n}$ by sending whatever happens there first with  $f$ to $\mathbb{R}^n$ and then applying the given measure there. This is captured by the following definition.

+-- {: .num_defn #PullbackOfDifferential1FormsOnCartesianSpaces}
###### Definition

For $\phi \colon \mathbb{R}^{\tilde n} \to \mathbb{R}^n$ a [[smooth function]], the **[[pullback of differential forms|pullback of differential 1-forms]]** along $\phi$ is the [[function]]

$$
  \phi^* \colon \Omega^1(\mathbb{R}^{k}) \to \Omega^1(\mathbb{R}^{\tilde k})
$$

between sets of differential 1-forms, def. \ref{Differential1FormsOnCartesianSpaces}, which is defined on [[basis]]-elements by

$$
  \phi^* \mathbf{d} x^i \coloneqq \sum_{j = 1}^{\tilde k} \frac{\partial f^i}{\partial \tilde x^j} \mathbf{d}\tilde x^j
$$

and then extended linearly by

$$
  \begin{aligned}
    \phi^* \omega & = \phi^* \left( \sum_{i} \omega_i \mathbf{d}x^i \right)
    \\
    & \coloneqq
     \sum_{i = 1}^k \left(\phi^* \omega\right)_i \sum_{j = 1}^{\tilde k} \frac{\partial f^i }{\partial \tilde x^j}  \mathbf{d} \tilde x^j 
    \\
    & = 
     \sum_{i = 1}^k  \sum_{j = 1}^{\tilde k} (\omega_i \circ \phi) \cdot \frac{\partial f^i }{\partial \tilde x^j}  \mathbf{d} \tilde x^j 
  \end{aligned}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

The term "pullback" in _[[pullback of differential forms]]_ is not really related, certainly not historically, to the term _[[pullback]]_ in [[category theory]]. One can relate the pullback of differential forms to categorical pullbacks, but this is not really essential here. The most immediate property that both concepts share is that they take a [[morphism]] going in one direction to a map between structures over domain and codomain of that morphism which goes in the other direction, and in this sense one is "pulling back structure along a morphism" in both cases.

=--

Even if in the above definition we speak only about the [[set]] $\Omega^1(\mathbb{R}^k)$ of differential 1-forms, this set naturally carries further [[structure]].

+-- {: .num_defn #ModuleStructureOn1FormsOnRk}
###### Definition

1. The set $\Omega^1(\mathbb{R}^k)$ is naturally an [[abelian group]] with addition given by componentwise addition

   $$
      \begin{aligned}
         \omega + \lambda & =
          \sum_{i = 1}^k \omega_i \mathbf{d}x^i + \sum_{j = 1}^k \lambda_j \mathbf{d}x^j
         \\
         & = \sum_{i = 1}^k(\omega_i + \lambda_i) \mathbf{d}x^j
      \end{aligned}
      \,,
   $$

1. The abelian group $\Omega^1(\mathbb{R}^k)$ is naturally equipped with the structure of a [[module]] over the [[ring]] $C^\infty(\mathbb{R}^k,\mathbb{R}) = CartSp(\mathbb{R}^k, \mathbb{R})$ of [[smooth functions]], where the [[action]] $C^\infty(\mathbb{R}^k,\mathbb{R}) \times\Omega^1(\mathbb{R}^k) \to \Omega^1(\mathbb{R}^k)$ is given by componentwise multiplication

   $$
     f \cdot \omega = \sum_{i = 1}^k( f \cdot \omega_i) \mathbf{d}x^i
     \,.
   $$

=--

+-- {: .num_defn }
###### Remark

More abstractly, this just says that $\Omega^1(\mathbb{R}^k)$ is the [[free module]] over $C^\infty(\mathbb{R}^k)$ on the set $\{\mathbf{d}x^i\}_{i = 1}^k$.

=--

The following definition captures the idea that if $\mathbf{d} x^i$ is a measure for displacement along the $x^i$-[[coordinate]], and $\mathbf{d}x^j$ a measure for displacement along the $x^j$ coordinate, then there should be a way te get a measure, to be called $\mathbf{d}x^i \wedge \mathbf{d} x^j$, for infinitesimal _surfaces_ (squares) in the $x^i$-$x^j$-plane. And this should keep track of the [[orientation]] of these squares, whith 

$$
  \mathbf{d}x^j \wedge \mathbf{d}x^i = - \mathbf{d}x^i \wedge \mathbf{d} x^j
$$

being the same infinitesimal measure with orientation reversed.

+-- {: .num_defn #DifferentialnForms}
###### Definition

For $k,n \in \mathbb{N}$, the **smooth [[differential forms]]** on $\mathbb{R}^k$ is the [[exterior algebra]]

$$
  \Omega^\bullet(\mathbb{R}^k) 
   \coloneqq
  \wedge^\bullet_{C^\infty(\mathbb{R}^k)} \Omega^1(\mathbb{R}^k)
$$

over the [[ring]] $C^\infty(\mathbb{R}^k)$ of [[smooth functions]] of the [[module]] $\Omega^1(\mathbb{R}^k)$ of smooth 1-forms, prop. \ref{ModuleStructureOn1FormsOnRk}.

We write $\Omega^n(\mathbb{R}^k)$ for the sub-module of degree $n$ and call its elements the **smooth [[differential n-forms]]**.

=--

+-- {: .num_remark}
###### Remark

Explicitly this means that a [[differential n-form]] $\omega \in \Omega^n(\mathbb{R}^k)$ on $\mathbb{R}^k$ is a [[formal linear combination]] over $C^\infty(\mathbb{R}^k)$ of [[basis]] elements of the form $\mathbf{d} x^{i_1} \wedge \cdots \wedge \mathbf{d}x^{i_n}$ for $i_1 \lt i_2 \lt \cdots \lt i_n$:

$$
  \omega = \sum_{1 \leq i_1 \lt i_2 \lt \cdots \lt i_n \lt n} \omega_{i_1, \cdots, i_n} \mathbf{d}x^{i_1} \wedge \cdots \wedge \mathbf{d}x^{i_n}
  \,.
$$


=--

+-- {: .num_defn #PullbackOfDifferentialForms}
###### Definition

The [[pullback of differential forms|pullback of differential 1-forms]] of def. \ref{Differential1FormsOnCartesianSpaces} extends as an $C^\infty(\mathbb{R}^k)$-[[associative algebra|algebra]] [[homomorphism]] to $\Omega^n(-)$, given for a smooth function $f \colon \mathbb{R}^{\tilde k} \to \mathbb{R}^k$ on basis elements by

$$
  f^* \left(  \mathbf{d}x^{i_1} \wedge \cdots \wedge \mathbf{d}x^{i_n} \right)
  = 
  \left(f^* \mathbf{d}x^{i_1} \wedge \cdots \wedge \mathbf{d}x^{i_n} \right)
  \,. 
$$ 

=--


#### Differential forms on smooth spaces
 {#SmoothUniversalModuliSpaceOfDifferentialForms}

Above we have defined differential $n$-form on abstract coordinate systems. Here we extend this definition to one of differential $n$-forms on arbitrary [[smooth spaces]]. We start by observing that the space of _all_ differential $n$-forms on cordinate systems themselves naturally is a smooth space.

+-- {: .num_prop}
###### Proposition

The assignment of differential $n$-forms

$$
  \Omega^n(-) \colon \mathbb{R}^k \mapsto \Omega^n(\mathbb{R}^k)
$$

of def. \ref{DifferentialnForms} together with the [[pullback of differential forms]]-functions of def. \ref{PullbackOfDifferentialForms}

$$
  \array{
    \mathbb{R}^{k_1} &\mapsto & \Omega^1(\mathbb{R}^{k_1})
    \\
    \uparrow^{\mathrlap{f}} && \downarrow^{\mathrlap{f^*}}
    \\
    \mathbb{R}^{k_2} &\mapsto& \Omega^1(\mathbb{R}^{k_2})
  }
$$

defines a [[smooth space]] in the sense of def. \ref{SmoothSpace}:

$$
  \Omega^n(-) \in Smooth0Type
  \,.
$$

=--

+-- {: .num_defn #SmoothModuliSpaceOfnForms}
###### Definition


We call this 

$$
  \Omega^n \colon Smooth0Type
$$

the **universal smooth [[moduli space]]** of differential $n$-forms. 

=--

The reason for this terminology is that homomorphisms of smooth spaces into $\Omega^1$ _modulate_ differential $n$-forms on their [[domain]], by prop. \ref{YonedaForSmoothSpaces} (and hence by the [[Yoneda lemma]]):

+-- {: .num_example}
###### Example

For the [[Cartesian space]] $\mathbb{R}^k$ regarded as a smooth space by example \ref{CartesianSpaceAsSmoothSpace}, there is a [[natural bijection]]

$$
  \Omega^n(\mathbb{R}^k) \simeq Hom(\mathbb{R}^k, \Omega^1)
$$

between the set of smooth $n$-forms on $\mathbb{R}^n$ according to def. \ref{Differential1FormsOnCartesianSpaces} and the set of homomorphism of smooth spaces, $\mathbb{R}^k \to \Omega^1$, according to def. \ref{HomomorphismOfSmoothSpaces}.

=--

In view of this we have the following elegant definition of smooth $n$-forms on an arbitrary smooth space.

+-- {: .num_defn #DifferentialnFormOnSmoothSpace}
###### Definition

For $X \in Smooth0Type$ a [[smooth space]], def. \ref{SmoothSpace}, a **[[differential n-form]]** on $X$ is a [[homomorphism]] of [[smooth spaces]] of the form

$$
  \omega \colon X \to \Omega^n(-)
  \,.
$$

Accordingly we write

$$
  \Omega^n(X) \coloneqq Smooth0Type(X,\Omega^n)
$$

for the set of smooth $n$-forms on $X$.

=--

We may unwind this definition to a very explicit description of differential forms on smooth spaces. This we do in a moment in remark \ref{DifferentialFormOnSmoothSpaceAsSystemOfDiffFormsOnCoordinates}.

Notice that differential 0-forms are equivalently smooth $\mathbb{R}$-valued functions.

+-- {: .num_prop #SpaceOf0FormsIsRealLine}
###### Proposition

$\Omega^0 = \mathbb{R}$

=--


+-- {: .num_defn #PullbackOfDifferentialFormsOnSmoothSpaces}
###### Definition

For $f \colon X \to Y$ a [[homomorphism]] of [[smooth spaces]], def. \ref{HomomorphismOfSmoothSpaces}, the **[[pullback of differential forms]]** along $f$ is the [[function]]

$$
  f^* \colon \Omega^n(Y) \to \Omega^n(X)
$$

given by the [[hom-functor]] into the smooth space $\Omega^n$ of def. \ref{SmoothModuliSpaceOfnForms}:

$$
 f^* \coloneqq Hom(-, \Omega^n)
 \,.
$$

This means that it sends an $n$-form $\omega \in \Omega^n(Y)$ which is modulated by a homomorphism $Y \to \Omega^n$ to the $n$-form $f^* \omega \in \Omega^n(X)$ which is modulated by the [[composition|composite]] $X \stackrel{f}{\to} X \to \Omega^n$.

=--

+-- {: .num_defn}
###### Proposition

For $X = \mathbb{R}^{\tilde k}$ and $Y = \mathbb{R}^{k}$ definition \ref{PullbackOfDifferentialFormsOnSmoothSpaces} reproduces def. \ref{PullbackOfDifferentialForms}.

=--

+-- {: .proof}
###### Proof

Again by the [[Yoneda lemma]].

=--

+-- {: .num_remark #DifferentialFormOnSmoothSpaceAsSystemOfDiffFormsOnCoordinates}
###### Remark

Using def. \ref{PullbackOfDifferentialFormsOnSmoothSpaces}

Unwinding def. \ref{DifferentialnFormOnSmoothSpace} yields the following explicit description:

a differential $n$-form $\omega \in \Omega^n(X)$ on a smooth space $X$ is

1. for each way $\phi \colon \mathbb{R}^k \to X$ of laying out a coordinate system $\mathbb{R}^k$ in $X$ a differential $n$-form

   $$
     \phi^* \omega \in \Omega^n(\mathbb{R}^k)
   $$

   on the abstract coordinate system, as given by def. \ref{DifferentialnForms};

1. for each abstract [[coordinate transformation]] $f \colon \mathbb{R}^{k_2} \to \mathbb{R}^{k_1}$ a corresponding compatibility condition between local differential forms $\phi_1 \colon \mathbb{R}^{k_1} \to X$ and $\phi_2 \colon \mathbb{R}^{k_2} \to X$ of the form

   $$
     f^* \phi_1^* \omega = \phi_2^* \omega
     \,.
   $$

Hence a differential form on a smooth space is simply a collection of differential forms on all its coordinate systems such that these glue along all possible coordinate transformations.

=--


The following adds further explanation to the role of $\Omega^n \in Smooth0Tye$ as a _[[moduli space]]_. Notice that since $\Omega^n$ is itself a [[smooth space]], we may speak about differential $n$-forms on $\Omega^n$ itsefl.

+-- {: .num_defn #UniversalDifferentialnForm}
###### Definition

The **universal differential $n$-forms** is the differential $n$-form

$$
  \omega^n_{univ} \in \Omega^n(\Omega^n)
$$

which is modulated by the [[identity]] [[homomorphism]] $id \colon \Omega^n \to \Omega^n$.

=--

With this definition we have:

+-- {: .num_prop}
###### Proposition

For $X \in Smooth0Type$ any [[smooth space]], every differential $n$-form on $X$, $\omega \in \Omega^n(X)$ is the pullback of differential forms, def. \ref{PullbackOfDifferentialFormsOnSmoothSpaces}, of the universal differential $n$-form, def. \ref{UniversalDifferentialnForm}, along a homomorphism $f$ from $X$ into the moduli space $\Omega^n$ of differential $n$-forms:

$$
  \omega = f^* \omega^n_{univ}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This statement is of course in a way a big tautology. Nevertheless it is a very useful tautology to make explicit. The whole concept of differential forms on smooth spaces here may be thought of as simply a variation of the theme of the [[Yoneda lemma]].

=--




### Semantic Layer
 {#DifferentialFormsLayerSem}

#### Concrete smooth spaces
 {#ConcreteObjects}

The smooth universal moduli space of differential forms $\Omega^n(-)$
from def. \ref{SmoothModuliSpaceOfnForms}
is noteworthy in that it has a property not shared by 
many smooth spaces that one might think of more naively: while evidently being "large" (the space of all differential forms!) it has "very few points" and "very few $k$-dimensional subspaces" for low $k$.  In fact 

+-- {: .num_prop}
###### Proposition

For $k \lt n$ the smooth space $\Omega^n$ admits only a unique probe by $\mathbb{R}^k$:

$$
  Hom(\mathbb{R}^k, \Omega^n(-))
  \simeq
  \Omega^n(\mathbb{R}^k)
  = 
  \{0\}
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the [[Yoneda lemma]] a smooth morphism $\mathbb{R}^k \to \Omega^n$ is a [[differential n-form]] $\omega \in \Omega^n(\mathbb{R}^k)$. But for $n \gt k$ there is only the 0 element.

=--

So while $\Omega^n()$ is a large smooth space, it is "not supported on probes" in low dimensions in as much as one might expect, from more naive notions of smooth spaces.

We now formalize this. The formal notion of an smooth space which _is_ supported on its probes is that of a _[[concrete object]]_. There is a univeral map that sends any smooth space to its _concretification_. The universal moduli spaces of differential forms turn out to be _non-concrete_ in that their concetrification is the point.

+-- {: .num_defn #ConcreteObjectsAndConcretification}
###### Definition

Let $\mathbf{H}$ be a [[local topos]]. Write $\sharp \colon \mathbf{H} \to \mathbf{H}$ for the corresponding sharp modality, def. \ref{SharpModalityOfLocalTopos}. Then. 

1. An object $X \in \mathbf{H}$ is called a **[[concrete object]]** if

   $$
     DeCoh_X \colon X \to \sharp X
   $$

   is a [[monomorphism]].

1. For $X \in \mathbf{H}$ any object, its  **concretification** $Conc(X) \in \mathbf{H}$ is the [[image]] factorization of $DeCoh_X$, hence the factorization into an [[epimorphism]] followed by a [[monomorphism]]

   $$
     DeCoh_X : X \to Conc(X) \hookrightarrow \sharp X
     \,.
   $$

=--

+-- {: .num_remark}
###### Remark

Hence the concretification $Conc(X)$ of an object $X$ is itself a [[concrete object]] and it is [[universal property|universal]] with this property. (...)

=--

+-- {: .num_prop #DecohesOverASiteWithTerminalObject}
###### Proposition

Let $C$ be a [[site]] of definition for the [[local topos]]
$\mathbf{H}$, with [[terminal object]] $*$. Then for 
$X \colon C^{op} \to Set$ a sheaf, $DeCoh_X$
is given over $U \in C$ by

$$
  X(U)
  \underoverset{Yoneda}{\simeq}{\to}
  \mathbf{H}(U, X)
  \stackrel{\Gamma_{U,X}}{\to}
  Set(\Gamma(U),\Gamma(X))
  \,.
$$

=--


+-- {: .num_prop}
###### Proposition

For $n \geq 1$ we have 

$$
  Conc(\Omega^n) \simeq *
  \,.
$$

=--

In this sense the smooth moduli space of differential $n$-forms is _maximally non-concrete_.

#### Smooth space of differential forms on a smooth space

We discuss the smooth space of differential forms _on a fixed smooth space_ $X$. 

+-- {: .num_remark}
###### Remark

For $X$ a [[smooth space]], the smooth mapping space $[X, \Omega^n] \in Smooth0Type$ is the smooth space whose $\mathbb{R}^k$-plots are differential $n$-forms on the [[product]] $X \times \mathbb{R}^k$

$$
  [X, \Omega^n] \colon \mathbb{R}^k \mapsto \Omega^n(X \times \mathbb{R}^k)
  \,.
$$

This is not _quite_ what one usually wants to regard as an $\mathbb{R}^k$-parameterized of differential forms on $X$. That is instead usually meant to be a differential form $\omega$ on $X \times \mathbb{R}^k$ which has "no leg along $\mathbb{R}^k$". Another way to say this is that the family of forms on $X$ that is represented by some $\omega$ on $X \times \mathbb{R}^k$ is that which over a point $v \colon * \to \mathbb{RR}^k$ has the value $(id_X,v)^* \omega$. Under this [[pullback of differential forms]] any components of $\omega$ with "legs along $\mathbb{R}^k$" are identified with the 0 differential form 

=--

This is captured by the following definition.

+-- {: .num_defn #SmoothSpaceOfFormsOnSmoothSpace}
###### Definition

For $X \in Smooth0Type$ and $n \in \mathbb{N}$, the **smooth space of differential $n$-forms** $\mathbf{\Omega}^n(X)$ on $X$ is the concretification, def. \ref{ConcreteObjectsAndConcretification}, of the smooth mapping space $[X, \Omega^n]$, def. \ref{SmoothFunctionSpace}, into the smooth moduli space of differential $n$-forms, def. \ref{SmoothModuliSpaceOfnForms}:

$$
  \mathbf{\Omega}^n(X) \coloneqq Conc([X, \Omega^n])
$$

=--

+-- {: .num_prop}
###### Proposition

The $\mathbb{R}^k$-plots of $\mathbf{\Omega}^n(\mathbb{R}^k)$
are indeed smooth differential $n$-forms on $X \times \mathbb{R}^k$ which are such that their evaluation on vector fields tangent to $\mathbb{R}^k$ vanish.

=--

+-- {: .proof}
###### Proof (sketch)

By def. \ref{Decohese}, def. \ref{ConcreteObjectsAndConcretification} and 
prop. \ref{DecohesOverASiteWithTerminalObject} the set of plots of $\mathbf{\Omega}^n(X)$ over $\mathbb{R}^k$ is the [[image]] of the [[function]]

$$
  \Omega^n(X \times \mathbb{R}^k)
  \simeq
   Hom_{Smooth0Type}(\mathbb{R}^k, [X,\Omega^n])
   \stackrel{\Gamma_{ \mathbb{R}^k, [X,\Omega^n] }}{\to}
   Hom_{Set}(\Gamma(\mathbb{R}^k), \Gamma [X, \Omega^n])
   \simeq
   Hom_{Set}(\mathbb{R}^k_s, \Omega^n(X))
  \,,
$$

where on the right $\mathbb{R}^k_s$ denotes, just for emphasis, the underlying set of $\mathbb{R}^k_s$. This function manifestly sends a smooth differential form $\omega \in \Omega^n(X \times \mathbb{R}^k)$ to the function from points $v$ of $\mathbb{R}^k$ to differential forms on $X$ given by

$$
  \omega \mapsto \left(v \mapsto  (id_X, v)^* \omega \right)
  \,.
$$

Under this function all components of differential forms with a "leg along" $\mathbb{R}^k$ are sent to the 0-form. Hence the image of this function is the collection of smooth forms on $X \times \mathbb{R}^k$ with "no leg along $\mathbb{R}^k$".

=--

### Syntactic Layer
 {#DifferentialFormsLayerSyn}

#### Images

+-- {: .num_prop}
###### Proposition

Let a morphism $f \colon X \to Y$ in $\mathbf{H}$ be the [[categorical semantics]] of the [[syntax]]

$$
  x \colon X \; \vdash \; f(x) \colon Y
  \,.
$$

Then the syntax for the [[infinity-image|image]] $i_f \colon im(f) \hookrightarrow Y$ is

$$
  \vdash\;
   \left(
     \sum_{y \colon Y} \exists_{x \colon X} \left(f\left(x\right) = y\right)
   \right)
   \colon
   Type
  \,.
$$

=--

Here $\exists_{\cdots} \cdots =_{def} \left[ \sum_{\cdots} \cdot\right]$ is the [[bracket type]] of the [[dependent sum type]].

Accordingly the syntax for the smooth moduli space of differential $n$-forms, def. \ref{SmoothSpaceOfFormsOnSmoothSpace},
on a smooth space $X$, 


$$
  \sum_{\omega \colon \sharp [X, \Omega^n]}
  \exists_{\lambda \colon [X,\Omega^n]}
  (\omega = DeCoh_X(\lambda)) 
  \,.
$$

(...)

## **Differentiation**
 {#Differentiation}

So far we have dealt with _cohesive_ structures for which there is a notion of _smooth variation_, say of the position of a [[particle]] along a [[trajectory]] in [[spacetime]]. The idea of _differentiation_ is to measure the _[[difference]]_ between the position of two points on a cohesive trajectory in space as the difference between their [[worldline]] coordinates "tends to 0" without actually becoming 0. One also says that differentiation is forming "[[infinitesimal space|infinitesimal]] differences" of a cohesive process -- and we will make precise here what this means.

There are two stages to the theory of differentiation:

1. We may think of differentiation as just a means to analyze more in detail the [[cohesive topos|cohesive structure]] already given, without adding new [[structure]], hence without a priori refining our notion of what a "[[cohesion|cohesive]] [[trajectory]]" is. Indeed, given any [[line object]] $\mathbb{R}$ in a [[cohesive ∞-topos]], there is a canonically a homomorphism of cohesive spaces

   $$
      \mathbf{d} \colon \mathbb{R} \to \Omega^1_{cl}(-,\mathbb{R})
   $$

   from the line to the cohesive moduli space of closed [[differential 1-forms]], which is such that it sends a cohesive curve on the line to the differential form on this curve whose value at each point is the _differential_ of the curve, its rate of infinitesimal change at that point.

   Below in _[Differentiation of smooth functions and differetial forms](#DifferentiationOfSmoothFunctionsAndDifferentialForms)_ we discuss this construction in the standard model of [[smooth infinity-groupoid|smooth cohesion]] for [[smooth spaces]], where it reproduces what traditionally is called the _[[de Rham differential]]_ $\mathbf{d}$. 

   Further below in _[Maurer-Cartan forms -- Cohesive differentiation](#CohesiveDifferentiation)_ we show how $\mathbf{d}$ comes out from just the abstract axioms of cohesionn.

1. We may think of differentiation as reflecting a refinement of smooth cohesion such that [[infinitesimal space|infinitesimal]] cohesive trajectories actually exist. Here, on top of having a _measure_ for how a cohesive trajectory changes infinitesimally at a given point, it makes sense to ask concretely if two points on a trajectory are infinitesimally close to each other. In this approach the very notion of cohesion is refined to include _explicitly_ a way to speak not just about a "cohesive blob of points", but to decide whether it is in fact just an "infinitesimal cohesive blob of points" -- an _[[infinitesimally thickened point]]_.

   [[differential geometry|Differential geometry]] with such an explicit notion of [[infinitesimal space|infinitesimals]] is known as _[[synthetic differential geometry]]_: the [[axioms]] here allow one to _synthesize_ an [[infinitesimally thickened point]] and not just to reason about it _as if_ it existed. 

   In such a synthetic differential context then the differential $\mathbf{d}$ from above not just exists as a whole, but we can "take it apart and re-synthesize it" by realizing its value at each point literally as the ordinary [[difference]] between two _infinitesimally close_ points. Similarly, various other fundamental constructions in [[differential geometry]], such as that of [[tangent bundles]] and [[jet bundles]] have a usefully transparent axiomatic characterization in the presence of synthetic infinitesimals. ([[Sophus Lie]], one of the founding fathers of [[differential geometry]] [famously said](synthetic+differential+geometry#SophusLieQuote) that he indeed found his theorems using such synthetic reasoning intuitively, and just did not publish them this way due to a lack of formalization of this language -- at his time. ) This we discuss in the Mod Layer in _[D-geometry](#DGeometry)_ below.

In the [Differentiation semantic layer](#DifferentiationLayerSem) below we formalize differentiation, and these two aspects of it, by adding to the notion of _[[cohesive topos]]_ that of an _[[infinitesimal cohesion|infinitesimal cohesive neighbourhood]]_.

Recalling that a [[cohesive topos]] is an abstract _cohesive blob_, an infinitesimal cohesive neighbourhood is accordingly an infinitesimally thicked cohesive blob (which is itself again a cohesive blob):


$$
  \array{
    CohesiveBlob &&\hookrightarrow&& InfinitesimallyThickenedCohesiveBlob
    \\
    & \searrow && \swarrow
    \\
    && Point
  }
  \;\;\;\;\;\;\;\;
  \array{
    \mathbf{H} &&\stackrel{}{\hookrightarrow}&& \mathbf{H}_{th}
    \\
    & \searrow && \swarrow
    \\
    && DiscSpaces
  }
  \,.
$$

### Model Layer
 {#DifferentiationLayerMod}

We discuss 

* [Differentiation of smooth functions and differential forms](#DifferentiationOfSmoothFunctionsAndDifferentialForms)

  * first just _[on coordinate patches](#DifferentiationOnCoordinatePatches)_

  * and then _[on general smooth spaces](#DifferentiationOnSmoothSpaces)_.

By considering [[fiber products]] of smooth [[mapping spaces]] with [[discrete spaces]] of boundary configurations, we obtain from this the differentiation theory called 

* _[Variational calculus](#VariationalCalculus)_

  * with the notion of _[Smooth functional](#SmoothFunctionals)_

  * and _[Variational derivative](#FunctionalDerivative)_ of smooth functionals.

  * The central class of examples of this of interest in physics is the variation of [[action functionals]] that yields the [[Euler-Lagrange equations|Euler-Lagrange]] [[equations of motion]] in [[classical field theory]]. This we discuss in _[Euler-Lagrange equations](#EulerLagrangeEquations)_.

#### Differentiation of smooth functions and differential forms
 {#DifferentiationOfSmoothFunctionsAndDifferentialForms}

##### Differentiation on coordinate patches
 {#DifferentiationOnCoordinatePatches}

By definition to [[smooth function]] $f \colon \mathbb{R} \to \mathbb{R}$ is associated its [[derivative]], a smooth function $f' \colon \mathbb{R} \to \mathbb{R}$. And more generally to a smooth function $f \colon \mathbb{R}^n \to \mathbb{R}$ are associated its [[partial derivatives]], smooth functions

$$
  \frac{\partial f}{\partial x^i} \colon \mathbb{R}^n \to \mathbb{R}
$$

for $1 \leq i \leq n $.

The [[de Rham differential]] collects all partial derivatives of a function into a single [[differential 1-form]]

+-- {: .num_defn #DeRhamDifferentialOn1Forms}
###### Definition

For $n \in \mathbb{N}$,  The **[[de Rham differential]]** on [[smooth functions]] in $C^\infty(\mathbb{R}^n)$ is the [[function]]

$$
  \mathbf{d} \colon C^\infty(\mathbb{R}^n) \to \Omega^1(\mathbb{R}^n)
$$

which takes $f \in C^\infty(\mathbb{R}^n)$ to

$$
  \mathbf{d}f \coloneqq \sum_{i = 1}^n \frac{\partial f}{\partial x^i} \mathbf{d} x^i
  \,.
$$

=--

+-- {: .num_example}
###### Example

For $x^i \colon \mathbb{R}^n \to \mathbb{R}$ one of the [[coordinate]] functions, the de Rham differential $\mathbf{d} x^i$ indeed coincides with the basis element of the same name according to def. \ref{Differential1FormsOnCartesianSpaces}, using that 

$$
  \frac{\partial x^i}{\partial x^{j}} = 
  \left\{
    \array{
      1 & | i = j
      \\
      0 & | otherwise
    }
  \right.
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

The de Rham differentials $\mathbf{d} \colon C^\infty(\mathbb{R}^n) \to \Omega^1(\mathbb{R}^n)$ for all $n \in \mathbb{N}$ are compatible with [[pullback of differential forms|pullback of differential 1-forms]], def. \ref{PullbackOfDifferential1FormsOnCartesianSpaces}, in that for each coordinate transformation $\phi \colon \mathbb{R}^{\tilde k} \to \mathbb{R}^{k}$ the [[diagram]]

$$
  \array{
     C^\infty(\mathbb{R}^k) 
      &\stackrel{\mathbf{d}}{\to}& 
    \Omega^1(\mathbb{R}^k)
     \\
     \downarrow^{\mathrlap{\phi^\ast}} && \downarrow^{\mathrlap{\phi^\ast}}
     \\
     C^\infty(\mathbb{R}^{\tilde k}) 
       &\stackrel{\mathbf{d}}{\to}&   
     \Omega^1(\mathbb{R}^{\tilde k})    
  }
$$

[[commuting diagram|commutes]].

=--

+-- {: .proof}
###### Proof

This is equivalently the statement of the _[[chain rule]]_ of [[differentiation]]: For any $f \in C^\infty(\mathbb{R}^k)$ we have on the one hand, by def. \ref{PullbackOfDifferential1FormsOnCartesianSpaces} and def. \ref{DeRhamDifferentialOn1Forms}

$$
  \begin{aligned}
    \mathbf{d} \phi^\ast f
    & = 
    \mathbf{d} (f \circ \phi)
    \\
    & =
    \sum_{j = 1}^{\tilde k} \frac{f \circ \phi}{\partial x^j}
  \end{aligned}
$$

and on the other hand, applying the definition in the other order,

$$
  \begin{aligned}
    \phi^* \mathbf{d}f
    & = 
    \phi^* \sum_{i = 1}^k \frac{\partial f}{\partial x^i} \mathbf{d}x^i
    \\
    & = \sum_{i = 1}^k \sum_{j = 1}^{\tilde k} 
     \left(\frac{\partial f}{\partial x^i}\circ \phi \right)
    \cdot 
    \left(\frac{\partial \phi^i}{\partial x^j}\right) \mathbf{d}x^j
  \end{aligned}
  \,.
$$

Both expressions agree precisely if for all $j$ we have

$$
  \frac{\partial (f \circ \phi)}{\partial x^j}
   =
  \sum_{i = 1}^k \left(\frac{\partial f}{\partial x^i}\circ \phi\right) \cdot \left(\frac{\partial \phi^i}{\partial x^j}\right)
  \;\;\;
  \in 
  C^\infty(\mathbb{R}^{\tilde k})
  \,.
$$

This is precisely the statement of the _[[chain rule]]_ for [[differentiation]].

=--

Notice that as smooth spaces $\mathbb{R} = \Omega^0 = C^\infty(-)$, by prop.  \ref{SpaceOf0FormsIsRealLine}. Therefore the above says that

+-- {: .num_prop}
###### Proposition

The [[de Rham differential]], def. \ref{DeRhamDifferentialOn1Forms}, constitutes a homomorphism of smooth spaces, def. \ref{HomomorphismOfSmoothSpaces}

$$
  \mathbf{d} \colon \mathbb{R} \to \Omega^1
$$

from the [[real line]] to the universal smooth moduli space of differential 1-forms, def. \ref{SmoothModuliSpaceOfnForms}.

=--

+-- {: .num_remark}
###### Remark

Below in _[Maurer-Cartan form on a Lie group](#MaurerCartanFormOnLieGroup)_ we discuss a more general abstract origin of $\mathbf{d} \colon \mathbb{R} \to \Omega^1_{cl}$.

=--

We now extend the de Rham differential to differential forms of higher degree.

+-- {: .num_defn #DeRhamDifferentialInGeneralDegreeOverCartesianSpaces}
###### Definition

For all $n \in \mathbb{N}$ let 

$$
  \mathbf{d} 
    \colon 
  \Omega^\bullet(\mathbb{R}^n)
   \to 
  \Omega^\bullet(\mathbb{R}^n)
$$

be the unique extension of $\mathbf{d} \colon C^\infty(-) \to \Omega^1(-)$ to a degree-1 [[derivation]] with 

$$
  \mathbf{d}\mathbf{d}x^i = 0
  \,.
$$


=--

(...)

+-- {: .num_prop #DeRhamDifferentialAsMorphismOfSmoothSpacesInEachDegree}
###### Proposition

For each $n \in \mathbb{N}$ the de Rham differential of def. \ref{DeRhamDifferentialInGeneralDegreeOverCartesianSpaces} constitutes a homomorphism of smooth spaces

$$
  \mathbf{d} \colon \Omega^n \to \Omega^{n+1}
$$

form the universal smooth moduli space of differental $n$-forms to that of differential $n+1$-forms.

=--

##### Differentiation on smooth spaces
 {#DifferentiationOnSmoothSpaces}

We now extend the notion of [[derivatives]] and [[de Rham differentials]] from [[smooth functions]] on [[Cartesian spaces]] to smooth functions on general [[smooth spaces]].

Recall from def. \ref{DifferentialnFormOnSmoothSpace} that the set of differential $n$-forms on a [[smooth space]] $X$ is $\Omega^n(X) \coloneqq Hom(X, \Omega^n)$. 

+-- {: .num_defn #DeRhamDifferentialOverSmoothSpaces}
###### Definition

For $X \in Smooth0Type$ a smooth space and $n \in \mathbb{N}$, the **[[de Rham differential]]** on $n$-forms over $X$ is the [[function]]

$$
  \mathbf{d} \colon \Omega^n(X) \to \Omega^{n+1}(X)
$$

which is the postcomposition with the homomorphism of smooth spaces of prop. \ref{DeRhamDifferentialAsMorphismOfSmoothSpacesInEachDegree}:
 
$$
  Hom(X,\mathbf{d}) \colon Hom(X,\Omega^n) \to Hom(X,\Omega^{n+1})
  \,.
$$

=--

In particular the [[derivative]] of a smooth function $f \colon X \to \mathbb{R}$ is the [[composition|composite]]

$$
  \mathbf{d}f \colon X \stackrel{f}{\to} \mathbb{R} \stackrel{\mathbf{d}}{\to} \Omega^1_{cl} \hookrightarrow \Omega^1
  \,.
$$

Below in _[Variation is differentiation on smooth spaces](#VariationIsDifferentiationOnSmoothSpaces)_ we find that this notion of differentiation of smooth functions on smooth spaces subsumes what traditionally is called _[[variational calculus]]_ of [[functionals]] on [[mapping spaces]].

##### Example: The electromagnetic field strength
 {#ElectromagneticFieldStrength}

for instance [[electromagnetic potential]]

$$
  A = \phi \mathbf{d}t + A_1 \mathbf{d}x^1 + A_2 \mathbf{d}x^2 + A_3 \mathbf{d}x^3
$$

then [[field strength]] is

$$
  F 
    \coloneqq
  \mathbf{d}A 
    = 
   E_1 \mathbf{d}t \wedge \mathbf{d}x^1 
    + 
   E_2 \mathbf{d}t \wedge \mathbf{d}x^2 
    + 
   E_3 \mathbf{d}t \wedge \mathbf{d}x^3
    + 
    B_1 \mathbf{d}x^2 \wedge \mathbf{d}x^3 
    + 
    B_2 \mathbf{d}x^3 \wedge \mathbf{d}x^1 
    + 
    B_3 \mathbf{d}x^1 \wedge \mathbf{d}x^2 
$$

with 

$$
  E_i = \frac{\partial \phi}{\partial x^i}
$$

and

$$
  B_1 = \frac{\partial A_2}{\partial x^3} - \frac{\partial A_3}{\partial x^2}
$$

etc


This are the first 2 of 4 [[Maxwell equations]]: $\mathbf{d} F = 0$

(the other 2 are discussed below in [Riemannian geometry](#RiemannianGeometry))

for

$$
  A,A' : X \to \Omega^1(-)
$$

a [[gauge transformation]] $A \to A'$
is $\lambda : X \to \mathbb{R}$ with

$$
  A' = A + \mathbf{d} \lambda
$$



#### Variational calculus
 {#VariationalCalculus}

Traditionally a _[[functional]]_ is a [[function]] which is sufficiently like a [[smooth function]], but defined not on a [[manifold]], but on a [[mapping space]] between manifolds. Also traditionally, a _[[variational derivative]]_ of such a functional is something aking to a [[derivative]], generalized to this context, and subject to the condition that all variations _preserve some boundary conditions_. 

We formulate this classical theory in the context of [[smooth spaces]]. Here a functional is simply a homomorphism of smooth spaces out of a smooth [[mapping space]], as in def. \ref{SmoothFunctionSpace}. We may impose _respect for boundary conditions_ by forming the [[fiber product]] of this mapping space with a _discrete smooth space inclusion_, given in def. \ref{MapFromDiscretizationOfSmooth0Type} below. Then the _variational derivative_ is simply the ordinary derivative of def. \ref{DeRhamDifferentialOverSmoothSpaces}.


##### Discrete points of a smooth space

+-- {: .num_defn #DiscretizationOfSmooth0Type}
###### Definition

For $X \in Smooth0Type$ a [[smooth space]], write

$$
  \Gamma X
  \coloneqq
  Hom(*,X)
  \in Set
$$

for its _set of points_, the set of homomorphisms, def. \ref{HomomorphismOfSmoothSpaces}, from the point to $X$. 

Write

$$
  \flat X \coloneqq Disc (\Gamma(X))
$$

for the discrete smooth space, def. \ref{DiscreteSmoothSpace}, on this set of points. 

=--

+-- {: .num_defn #MapFromDiscretizationOfSmooth0Type}
###### Definition

For every smooth space $X$ there is a canonical homomorphism of smooth spaces

$$
  \flat X \to X
  \,.
$$

This sends a plot $U \to \flat X$, which by definition of $Disc(-)$ is a point in $\Gamma X$, hence a homomorphism $x \colon * \to X$, to the plot $I \to * \stackrel{x}{\to} X$ of $X$.

=--


##### Smooth functionals
 {#SmoothFunctionals}

Let $X$ be a [[smooth manifold]].
Let $\Sigma$ be a [[smooth manifold|smooth]] [[manifold with boundary]] $\partial \Sigma \hookrightarrow \Sigma$. 

Write 

$$
  [\Sigma, X] \in Smooth0Type
$$

for the [[smooth space]] (a [[diffeological space]]) which is the [[mapping space]] from $\Sigma$ to $X$, hence such that for each $U \in $ [[CartSp]] we have

$$
  [\Sigma, X](U) = C^\infty(U \times \Sigma, X)
  \,.
$$


+-- {: .num_defn #MappingSpaceWithNonVaryingBoundary}
###### Definition

Write

$$
  [\Sigma, X]_{\partial \Sigma}
  \coloneqq
  [\Sigma, X] \times_{[\partial \Sigma,X]} \flat [\partial \Sigma,X]
$$

for the [[pullback]] in smooth spaces

$$
  \array{
    [\Sigma,X]_{\partial \Sigma}
    &\to&
    \flat [\partial \Sigma, X]
    \\
    \downarrow && \downarrow
    \\
    [\Sigma,X] &\stackrel{(-)|_{\partial \Sigma}}{\to}& [\partial \Sigma,X]
  }
  \,,
$$

where

* the bottom morphism is the restriction $[\partial \Sigma \hookrightarrow \Sigma, X]$ of configurations to the boundary;

* the right vertical morphism is the homomorphism from def. \ref{MapFromDiscretizationOfSmooth0Type}.
=--

+-- {: .num_prop #PlotsOfMappingSpaceWithNonVaryingBoundary}
###### Proposition

The [[smooth space]] $[\Sigma, X]_{\partial \Sigma}$ is a [[diffeological space]] whose underlying set is $C^\infty(\Sigma,X)$ and whose $U$-plots for $U \in $ [[CartSp]] are smooth functions
$\phi \colon U \times \Sigma \to X$ such that $\phi(-,s) \colon U \to X$ is the constant function for all $s \in \partial \Sigma \hookrightarrow \Sigma$.

=--


+-- {: .num_defn #SmoothFunctional}
###### Definition

A **[[functional]]** on the mapping space $[\Sigma, X]$ is a [[homomorphism]] of smooth spaces

$$
  S \colon [\Sigma, X]_{\partial \Sigma} \to \mathbb{R}
  \,.
$$

=--

##### Functional derivative / variational derivative
 {#FunctionalDerivative}

Write

$$
  \mathbf{d} \colon \mathbb{R} \to \Omega^1
$$

for the [[de Rham differential]] incarnated as a [[homomorphism]] of [[smooth spaces]] from the [[real line]] to the smooth [[moduli space]] of [[differential 1-forms]].


+-- {: .num_defn}
###### Definition

The **functional derivative** 

$$
  \mathbf{d}S
  \in 
  \Omega^1([\Sigma,X]_{\partial \Sigma})
$$ 

of a functional $S$, def. \ref{SmoothFunctional}, is simply its [[de Rham differential]] as a homomorphism of smooth spaces, hence the composite

$$
  \mathbf{d} S \colon [
  \Sigma, X]_{\partial \Sigma} 
     \stackrel{S}{\to} 
  \mathbb{R}   
    \stackrel{\mathbf{d}}{\to}
  \Omega^1
  \,.
$$

=--

+-- {: .num_defn}
###### Definition

This means that for each smooth parameter space $U \in $ [[CartSp]] and for each smooth $U$-parameterized collection 

$$
  \phi \colon U \times \Sigma \to X
$$

of smooth functions $\Sigma \to X$, constant in the parameter $U$ in some neighbourhood of the boundary of $\Sigma$, 

$$
  S_\phi \colon [\Sigma,X]_{\partial \Sigma}(U) \to C^\infty(U,\mathbb{R})
$$

is the function that sends each such $U$-collection of configurations to the $U$-collection of their values under $S$. Then

$$
  (\mathbf{d}S)_\phi \in \Omega^1(U)
$$

is the smooth [[differential 1-form]]

$$
  (\mathbf{d}S)_\phi = \mathbf{d}(S(\phi))
  \,.
$$

=--

+-- {: .num_example}
###### Example

Let $\Sigma = [0,1] \hookrightarrow \mathbb{R}$ be the standard [[interval]]. Let 

$$
  L(-,-) \mathbf{d}t \in \Omega^1([0,1], C^\infty(\mathbb{R}^2))
$$ 

and consider the functional

$$
  S
  \colon
  ([0,1] \stackrel{\gamma}{\to} X)
  \mapsto
  \int_{0}^1 L(\gamma(t), \dot \gamma(t)) d t
  \,.
$$

Then for $U = \mathbb{R}$ and any smooth $U$-parameterized collection $\{\gamma_{u} \colon \Sigma \to X\}_{u \in I}$ the functional derivative takes the value

$$
  \begin{aligned}
   \mathbf{d}S_{\gamma_{(-)}}
   & =
   \left(
     \frac{d}{d u} \int_0^1 L(\gamma_u(t), \dot \gamma_u(t)) dt
   \right)
   \mathbf{d}u
   \\
    & = 
     \int_{0}^1 
     \left(
       \frac{\partial L}{\partial \gamma}(\gamma_u(t), \dot \gamma_u(t))
       \frac{d \gamma_u(t)}{d u}
      + 
       \frac{\partial L}{\partial \dot \gamma}(\gamma_u(t), \dot \gamma_u(t))
       \frac{\partial \dot \gamma_u(t)}{\partial u}
     \right)
     \mathbf{d} u
     \\
     & =
     \int_{0}^1 
     \left(
       \frac{\partial L}{\partial \gamma}(\gamma_u(t), \dot \gamma_u(t))
       \frac{d \gamma_u(t)}{d u}
      + 
       \frac{\partial L}{\partial \dot \gamma}(\gamma_u(t), \dot \gamma_u(t))
       \frac{\partial }{\partial t}\frac{\partial \gamma_u(t)}{\partial u}
     \right)
     \mathbf{d} u
     \\
     & =
     \int_{0}^1
     \left(
       \frac{\partial L}{\partial \gamma}(\gamma_u(t), \dot \gamma_u(t))
      - 
       \frac{\partial}{\partial t}\frac{\partial L}{\partial \dot \gamma}(\gamma_u(t), \dot \gamma_u(t))
     \right)
     \frac{\partial \gamma_u(s)}{\partial u}
     \mathbf{d}u
  \end{aligned}
  \,.
$$

Here we used [[integration by parts]] and used that the boundary term vanishes

$$
  \begin{aligned}
    \int_{0}^1 \frac{\partial}{\partial t} 
    \left(
      \frac{\partial}{\partial \dot\gamma} L(\gamma_u(s), \dot \gamma_u(s))
      \frac{\partial \gamma_u(s)}{\partial u}
    \right)
    d s
    & = 
    \left(
      \frac{\partial}{\partial \dot\gamma} L(\gamma_u(1), \dot \gamma_u(1))
      \frac{\partial \gamma_u(1)}{\partial u}
    \right)
    - 
    \left(
      \frac{\partial}{\partial \dot\gamma} L(\gamma_u(0), \dot \gamma_u(0))
      \frac{\partial \gamma_u(0)}{\partial u}
    \right)
    \\
    & = 0
  \end{aligned}
$$

since by prop. \ref{PlotsOfMappingSpaceWithNonVaryingBoundary} $\gamma_{(-)}(1)$ and $\gamma_{(-)}(0)$ are constant.

=--

##### Euler-Lagrange equations
 {#EulerLagrangeEquations}

* [[critical locus]]

* [[Euler-Lagrange equation]]

* [[equations of motion]]

#### $\mathcal{D}$-geometry
 {#DGeometry}

* [[D-geometry]]

##### Infinitesimal smooth loci

+-- {: .num_defn #SmoothL}
###### Definition

Write

$$
  SmoothLoci \coloneqq SmoothAlgebras^{op} \coloneqq Func^\times(CartSp,Set)
$$

for the category of [[spaces]] which are [[Isbell duality|formally dual]] to [[smooth algebras]]: the [[opposite category]] of that of [[smooth algebras]]. This is called the category of **[[smooth loci]]**.

=--

+-- {: .num_defn #InfinitesimalAlgebra}
###### Definition

A **[[Artin ring|smooth Artin algebra]]** (also called a "Weil algebra" in the [[synthetic differential geometry]]-literature) is a [[smooth algebra]] $A$ whose underlying $\mathbb{R}$-[[vector space]] is a [[direct sum]] of the form

$$
  A = \mathbb{R} \oplus V
  \,,
$$

where $V$ is of finite [[dimension]] and such that every element $v \in V \subset A$ is nilpotent, in that there is $n \in \mathbb{N}$ such that the $n$-fold product of $v$ with itself in $A$ vanishes: $v^n = 0$.

=--

+-- {: .num_example }
###### Example

The smallest smooth Artin algebra is the [[ring of dual numbers]], 
def. \ref{DualNumbers}, for which $V = \mathb{R}$. 

=--

+-- {: .num_defn #InfinitesimallyThickenedPoints}
###### Definition

Write 

$$
  InfPoint \hookrightarrow SmoothLoci
$$

for the [[full subcategory]] of $SmoothLoci$, def. \ref{SmoothL}, of those that are duals of Artin algebras, def. \ref{InfinitesimalAlgebra}.

We call this the category of **[[infinitesimally thickened points]]**.

=--

##### de Rham space

* [[de Rham space]]

##### Jet bundles

* [[jet bundle]]


### Semantic Layer
 {#DifferentiationLayerSem}

#### Synthetic differential geometry

* [[synthetic differential geometry]]



We have two [[full and faithful functors]]

$$
  CartSp \hookrightarrow SmoothLoci
$$

$$
 InfPoint \hookrightarrow SmoothLoci
 \,.
$$

+-- {: .num_defn #InfinitesimallyThickenedCartesianSpaces}
###### Definition

Write [[CartSp]]${}_{th} \hookrightarrow SmoothLocus$ for the [[full subcategory]] of that of [[smooth loci]], def. \ref{SmoothL}, on those of the form 

$$
  \mathbf{U} = U \times D
$$ 

with $U \in CartSp \hookrightarrow SmoothLoci$ and $D \in InfPoint \hookrightarrow SmoothLoci$.

We may call this the category of **infinitesimally thickened Cartesian spaces** or or **[[formal smooth manifold|formal smooth Cartesian spaces]]**.

=--

The category $CartSp_{th}$ carries several [[coverages]] of interest. One is this:

+-- {: .num_defn #CahiersTopos}
###### Definition

For $\mathbf{U} = U \times D \in CartSp_{th}$ say that a [[covering family]] is a set of morphisms in $CartSp_{th}$ of the form $\{ U_i \times D \stackrel{(\phi_i, id_D)}{\to} U \times D\}_i$ such that 
$\{ U_i \stackrel{\phi_i}{\to} U\}_i$ is a [[covering]] family in [[CartSp]]. 

The corresponding [[sheaf topos]] $Sh(CartSp_{th})$ is known as the **[[Cahiers topos]]**.

=--

+-- {: .num_prop }
###### Proposition

The [[Cahiers topos]] $Sh(CartSp_{th})$, def. \ref{CahiersTopos},  
is a [[cohesive topos]].

=--

+-- {: .num_defn }
###### Definition

We write

$$
  SynthDiff0Type \coloneqq Sh(CartSp_{th})
  \,.
$$

=--

* [[synthetic differential infinity-groupoid]]

##### Tangent bundle

Write $D \in Sh(CartSp_{th})$ for the [[smooth locus]]
formally dual to the [[ring of dual numbers]], def. \ref{}.
Write

$$
  i \colon * \to D
$$

for the unique point inclusion.

+-- {: .num_defn }
###### Definition

For $X \in SynthDiff0Type$, the [[internal hom]]

$$
  T X \coloneqq [D,X] \in SynthDiff0Type
$$ 

equipped with the morphism

$$
  [i,X] \colon [D,X] \to [*,X] \simeq X
$$

is the **[[tangent bundle]]** of $X$.

=--

+-- {: .num_defn }
###### Definition

For $X \in SynthDiff0Type$, a **[[vector field]]** $v$ on $X$ is a [[section]] 

$$
  \array{
     X &&\stackrel{v}{\to}&& T X
     \\
     & {}_{\mathllap{id}}\searrow && \swarrow_{\mathrlap{[i,D]}}
     \\
     && X
  }
  \,.
$$

The **smooth space of vector fields** is the [[internal hom]] in the [[slice topos]] over $X$

$$
  \mathbf{\Gamma}_X(T X ) \coloneqq [X,T X]_X
  \,.
$$

=--

##### Differential equations

* [[equation]]

* [[differential equation]]


#### Differential cohesion of the topos of smooth spaces
 {#DifferentialCohesionOfToposOfSmoothSpaces}

Recall the sites 

* [[CartSp]], def. \ref{TheDifferentiallyGoodOpenCoverCoverage};

* [[infinitesimally thickened point|InfPoint]], def. \ref{InfinitesimallyThickenedPoints};

* [[formal smooth manifold|CartSp]]${}_{th}$, def. \ref{InfinitesimallyThickenedCartesianSpaces}.



+-- {: .num_defn #TheMorphismsOfSitesForCartSpInfinitesimalNeighbourhood}
###### Definition

Define [[functors]]

$$
  CartSp
   \stackrel{\overset{i}{\hookrightarrow}}{\underset{p}{\leftarrow}}
  CartSp_{th}
   \stackrel{\iota}{\leftarrow}
  InfPoint
$$

by

* $i \colon U \mapsto U \times *$;

* $p \colon U \times D \mapsto U$

* $\iota \colon D \mapsto * \times D$

=--

+-- {: .num_prop #DifferentialCohesiveStructureOfSmoothSpaces}
###### Proposition

All three functors in def. \ref{TheMorphismsOfSitesForCartSpInfinitesimalNeighbourhood} are [[morphisms of sites]]. The induced [[geometric morphism]] of [[sheaf toposes]] is of the form


$$
  Sh(CartSp)
   \stackrel{}{\stackrel{\overset{Lan_i}{\hookrightarrow}}{\stackrel{\overset{(-)\circ i}{\leftarrow}}{\stackrel{\overset{(-)\circ p}{\hookrightarrow}}{\underset{Ran_p}{\leftarrow}}}}}
  Sh(CartSp_{th})
   \stackrel{\overset{Lan_\iota}{\leftarrow}}{\underset{(-)\circ \iota}{\to}}
  Sh(InfPoint)
$$

where hence the morphism on the left is in particular an [[essential geometric morphism|essential]] [[geometric embedding]]. 

=--

+-- {: .num_prop }
###### Proposition

The sequence of [[geometric morphisms]]

$$
  Sh(CartSp) \stackrel{p^*}{\to} Sh(CartSp_{th}) \stackrel{\iota^*}{\to} Sh(InfPoint)
$$

exhibit a [[homotopy cofiber sequence]] in the [[(2,1)-category]] [[Topos]].

=--

+-- {: .proof}
###### Proof

By the discussion at _[(∞,1)Topos -- Existence of limits and colimits](%28infinity%2C1%29Topos#ExistenceOfLimitsAndColimits)_ the statement is equivalently that the [[inverse image]] functors

$$
  Sh(CartSp) 
    \stackrel{Lan_p}{\leftarrow}
  Sh(CartSp_{th})
    \stackrel{Lan_\iota}{\leftarrow}
  Sh(InfPoint)
$$

form a [[homotopy fiber sequence]] in [[(∞,1)Cat]]. Computing this in the [[model structure for quasi-categories]] after passing to [[nerves]], the morphism $N(Lan_p)$ is clearly an [[inner Kan fibration]] because of the [[subcategory]] inclusion $Sh(CartSp) \hookrightarrow Sh(CartSp_{th})$. So by the general discussion at [[homotopy pullback]] the homotopy fiber is given by the 1-categorical fiber of $N(Lan_p)$ in [[sSet]]. By the discussion at _[Left Kan extension - on representables](http://ncatlab.org/nlab/show/Kan+extension#LeftKanOnRepresentables)_ $Lan_p$ acts as $p$ on [[representable functor|representables]]. The 1-categorical fiber of $N(p) \colon N(CartSp_{th}) \to N(CartSp)$ is evidently $N(InfPoint)$. Since $Lan_\iota$ is a [[left adjoint]] it preserves colimits and since ever sheaf is a colimit of representables, this is sufficient to imply the claim.

=--

#### Differential cohesion
 {#DifferentialCohesion}


We axiomatize the existence of infinitesimals by further [[modal logic|modalities]] on a [[cohesive topos]].


+-- {: .num_defn #DifferentialCohesiveTopos}
###### Definition

Given a [[cohesive topos]] $\mathbf{H} = Cohesive0Type$ over a [[base topos]] [[Disc∞Grpd|Discrete0Type]], a structure of **[[differential cohesion]]** on $\mathbf{H}$ is an [[geometric embedding]] into a [[cohesive topos]] $\mathbf{H}_{th} = InfThickenedCohesive0Type$ with an extra [[left eadjoint]] that preserves the terminal object:

$$
  \array{
  Cohesive0Type
   &&\stackrel{\overset{i_!}{\hookrightarrow}}{\stackrel{\overset{i^*}{\leftarrow}}{\underset{i_*}{\hookrightarrow}}}&&
   InfThickenedCohesive0Type
   \\
   & {}_{\mathllap{\Gamma}}\searrow \nwarrow^{\mathrlap{Disc}} && {}^{\mathllap{\Gamma_{th}}}\swarrow \nearrow_{\mathrlap{Disc_{th}}}
   \\
   && Discrete0Type
  }
$$

=--

+-- {: .num_defn }
###### Definition

Given [[differential cohesion]], def. \ref{DifferentialCohesiveTopos}, define the [[monad]]/[[comonad]] [[adjunction]]

$$
  (Red \dashv \Pi_{inf})
  \colon
  \mathbf{H}_{th}
  \stackrel{\overset{i_*}{\leftarrow}}{\underset{i^*}{\to}}
  \mathbf{H}
  \stackrel{\overset{i_!}{\leftarrow}}{\underset{i_*}{\to}}
  \mathbf{H}
  \,.
$$

We call $Red(X)$ the **[[reduced type]]** of $X$ and $\Pi_{inf}(X)$ the [[infinitesimal path ∞-groupoid]] of $X$.


For the $(i_* \dashv i^*)$-[[unit of an adjunction|unit]] we write

$$
  InfinitesimalPathInclusion_X \colon X \to \Pi_{inf}(X)
$$

and call it the **constant infinitesimal path inclusion** on $X$.

The $(i_* \dashv i^*)$-[[unit of an adjunction|counit]] 

$$
  Red X \to X
$$

we call the **inclusion of the reduced part** of $X$.

=--



+-- {: .num_defn }
###### Definition

Given a [[geometric embedding]] of [[(∞,1)-topos|∞-toposes]] 

$$
  CohesiveType \stackrel{i}{\hookrightarrow} InfThickenedCohesiveType
$$

exhibiting [[differential cohesion]], write 

$$
  CohesiveType 
    \stackrel{i}{\hookrightarrow} 
  InfThickenedCohesiveType
   \to 
  InfinitesimalType
$$

for the corresponding [[homotopy cofiber sequence]] in [[(∞,1)-topos]]. The [[full sub-(∞,1)-category]] that is the [[kernel]] of the [[global section geometric morphism]] of $InfininitesimalType$ we call the [[(∞,1)-category]] of **synthetic [[∞-Lie algebras]]**

$$
  L_\infty Algebra \coloneqq ker(\Gamma) \hookrightarrow InfinitesimalType \stackrerl{\Gamma}{\to} DiscreteType
  \,.
$$


=--

+-- {: .num_example }
###### Example

For the moment see at _[Synthetic differential infinity-groupoid -- Lie differentiation](synthetic%20differential%20infinity-groupoid#LieDifferentiation)_.

=--









+-- {: .num_prop }
###### Proposition

Setting

* $\mathbf{H}_{th} \coloneqq Sh(CartSp_{th})$

* $\mathbf{H} \coloneqq Sh(CartSp)$

* $\mathbf{H}_{inf} \coloneqq Sh(InfPoint)$

makes prop. \ref{DifferentialCohesiveStructureOfSmoothSpaces}
exhibit [[differential cohesion|differential cohesive structure]].

=--

##### de Rham space
 {#DifferentiationSemLayerDeRhamSpace}

+-- {: .num_defn }
###### Definition

For $X \in \mathbf{H}_{th}$ we call $\Pi_{inf}(X) \in \mathbf{H}$ the
**[[de Rham space]] object** of $X$.

=--


##### Jet bundle
 {#DifferentiationSemLayerJetBundle}

+-- {: .num_defn }
###### Definition

For $X \in \mathbf{H}$

$$
  Jet_X 
    \coloneqq 
  (InfinitesimalPathInclusion_X)_*
  \colon
  \mathbf{H}_{th}/X \to \mathbf{H}_{th}/\Pi_{inf}(X)
  \,.
$$

=--

For $(E \to X) \in \mathb{H}_{th}/X$, $Jet_X(E)$ is the **[[jet bundle]]** of $E$.


##### Formally &#233;tale / formally unramified / formally smooth

+-- {: .num_defn }
###### Definition

For $f \colon X \to Y$ a morphism in $\mathbf{H}_{th}$ consider the morphism

$$
  q_f \colon \Pi_{inf}(X) \to Red(X) \times_{Red(Y)} \Pi_{inf}(Y)
  \,.
$$

We say that 

1. $f$ is a **[[formally étale morphism]]** if $q_f$ is an [[epimorphism]];

1. $f$ is a **[[formally unramified morphism]]** if $q_f$ is a [[monomorphism]];

1. $f$ is a **[[formally smooth morphism]]** if $q_f$ is an [[isomorphism]].


=--

+-- {: .num_prop }
###### Proposition

If $X, Y \in $ [[SmoothMfd]] $\hookrightarrow$ $\mathbf{H} \stackrel{i_!}{\to} \mathbf{H}_{th}$ then for $f \colon X \to Y$ any morphism

1. $f$ is [[formally étale morphism]] precisely if $f$ is a [[submersion]] of smooth manifolds;

1. $f$ is a [[formally unramified morphism]] precisely if it is an [[immersion]] of smooth manifolds;

1. $f$ is a [[formally smooth morphism]] precisely if it is a [[diffeomorphism]].

=--



### Syntactic Layer

#### Differential homotopy type theory

(...)

## **Smooth homotopy types**
 {#SmoothnGroupoids}
 {#SmoothGroupoids}


### Model Layer


#### Gauge transformations in electromagnetism
 {#GaugeTransformationsInElectromagnetism}

The mathematical notion of _[[groupoid]]_ is well familiar, in slight disguise, in basic _[[gauge theory]]_. Here we make this explicit for basic [[electromagnetism]].

We have seen in _[The electromagnetic field strength](#ElectromagneticFieldStrength)_ that a configuration of the electromagnetic field on $\mathbb{R}^4$ is given by a [[differential 1-form]] $A \in \Omega^1(\mathbb{R}^4)$, the "[[electromagnetic potential]]". It describes a field configuration with [[field strength]] Lorentz tensor

$$
  \begin{aligned}
    F & = 
       E_1 \mathbf{d}x^1 \wedge \mathbf{d}t
       + 
       E_1 \mathbf{d}x^1 \wedge \mathbf{d}t
       + 
       E_1 \mathbf{d}x^1 \wedge \mathbf{d}t
       + 
      \\
      & 
       + B_1 \mathbf{d}x^2 \wedge \mathbf{d}x^3
       + B_2 \mathbf{d}x^3 \wedge \mathbf{d}x^1
       + B_3 \mathbf{d}x^1 \wedge \mathbf{d}x^2
  \end{aligned}     
$$

with electric [[field strength]] $(E_i \in C^\infty(\mathbb{R}^4))_{i = 1}^3$ and magnetic [[field strength]] $(B_i \in C^\infty(\mathbb{R}^4))_{i = 1}^3$ given (with respect to the canonical [[coordinates]] $(t, x^1, x^2, x^3) \coloneqq (x^i)_{i = 1}^4 = $ on $\mathbb{R}^4$) that is given by the [[de Rham differential]] of $A$:

$$
  \begin{aligned}
    F = \mathbf{d}A
  \end{aligned}
  \,.
$$

After Maxwell it was thought that $F \in \Omega^2(\mathbb{R}^4)$ alone genuinely reflects the configuration of the electromagnetic field. But with the discovery of [[quantum mechanics]] it became clear that it is indeed the potential $A$ itself that reflects the configuration of the electromagnetic field: in the presence of [[magnetic flux]] or other topoligical constraints, there can be different $A, A' $ with the _same_ $F = \mathbf{d}A = \mathbf{d}A'$ which nevertheless describe experimentally distinguishable electromagnetic field configurations.

However, not _all_ different gauge potentials describe different physics. The actual configuration space of electromagnetism on a [[spacetime]] $X$ is finer than $\mathbf{\Omega}^2_{cl}(X)$ but coarser than $\mathbf{\Omega}^1(X)$. And it is not quite a smooth space itself, but a _[[smooth groupoid]]_:

one finds that two electromagnetic potentials $A, A' \in \Omega^1(\mathbb{R}^4)$ for which there is a function $\lambda \in C^\infty(\mathbb{R}^4)$ such that 

$$
  A' = A + \mathbf{d}\lambda
$$

represent _different but [[equivalence|equivalent]]_ field configurations. One says that 

* $\lambda$ induces a [[gauge transformation]] from $A$ to $A'$.

(...)

So the configuration space of electromagnetism does not just have points and coordinate systems. But it is also equipped with the information of a space of gauge transformation between any two coordinate systems laid out in it (which may be empty). 

(...)

So we have an [[action]] of the group $C^\infty(X)$ on $\Omega^1(X)$

$$
  \rho \colon \Omega^1(X)\times C^\infty(X) \to \Omega^1(X)
$$

$$
  \rho(A, \lambda) = A + \mathbf{d}\lambda
$$

We say that the configuration space is the [[action groupoid]]

$$
  \Omega^1(X) \sslash C^\infty(C)
$$

(...)


#### Groupoids

$$
  X_1 \stackrel{\overset{d_1}{\to}}{\stackrel{\overset{s_0}{\leftarrow}}{\underset{d_0}{\to}}}
  X_0
$$


$$
  \array{
    && X^{\Delta^2}
    \\
    &{}^{\mathllap{\exists}}\nearrow & \downarrow
    \\
    * &\stackrel{}{\to}& X^{\Lambda^2_i}
  }
$$


(...)

#### Smooth groupoids
 {#SmoothGroupoids}

* [[Lie groupoid]]

* [[smooth groupoid]]

$$
  \array{
    && X^{\Delta^2}
    \\
    &{}^{\mathllap{\exists}}\nearrow & \downarrow
    \\
    U &\stackrel{}{\to}& X^{\Lambda^2_i}
  }
$$

Example: $X$ a [[smooth space]] and $G$ a [[smooth group]] and 

$\rho : X \times G \to X$ an [[action]] then

[[action groupoid]]

$$
  X \sslash G = 
  \left(
    X \times G \stackrel{\overset{\rho}{\to}}{\underset{p_1}{\to}}
    X
  \right)
$$

##### Smooth path groupoid

* [[smooth path groupoid]]

##### Differential 1-forms are smooth incremental path measures
 {#1FormsAsSmoothFunctors}

We give a more intrinsic characterization of [[differential 1-forms]].

+-- {: .num_defn #SmoothPath}
###### Definition

A **smooth path with sitting instants** in $\mathbb{R}^k$ is a [[smooth function]] $\gamma \colon \mathbb{R} \to \mathbb{R}^k$ such 

1. the value of $\gamma$ converges to two points $x = \underset{t \to -\infty}{\lim} \gamma \in \mathbb{R}^k$ and $y = \underset{t \to \infty}{\lim} \gamma \in \mathbb{R}^k$;

1. the value of all [[derivatives]] of $\gamma$ converges to 0 at $t \to \pm \infty$.

A **localized diffeomorphism** $\phi \colon \mathbb{R} \to \mathbb{R}$ is a [[diffeomorphism]] such that there is an an open ball in $\mathbb{R}$ outside of which $\phi$ restricts to the identity.

Write

$$
  [\mathbb{R}, \mathbb{R}^k]\sslash Diff(\mathbb{R}) 
  \in 
  Smooth0Type
$$

for the smooth quotient space of smooth paths modulo localized diffeomorphism.

=--

+-- {: .num_defn #SmoothFunctorOnPathsInRkWithValuesInBR}
###### Definition

Say that a **smooth functor** $\mathbf{P}_1(\mathbb{R}^k) \to \mathbf{B}\mathbb{R}$ from the [[smooth path groupoid]] of $\mathbb{R}^k$ is

* a [[homomorphism]] of smooth space 

  $$
    S \colon [\mathbb{R}, \mathbb{R}^k] \to \mathbb{R}
  $$

* such that 

  1. composition of paths $\gamma_1, \gamma_2$ is sent to addition in $\mathbb{R}$

     $$
       S(\gamma_2\circ \gamma_1) = S(\gamma_1) + S(\gamma_2)
       \,.
     $$
  
  1. the constant path is sent to 0.

=--

+-- {: .num_prop }
###### Proposition

There is an [[equivalence]]

$$
  [\mathbf{P}_1(-), \mathbf{B}\mathbb{R}]
  \stackrel{\overset{\int_{(-)}(-)}{\leftarrow}}{\underset{}{\to}}
  DK(C^\infty(-) \stackrel{\mathbf{d}}{\to} \Omega^1(-)
  \,.
$$

=--

([SchreiberWaldorf](#SchreiberWaldorf)).

#### Simplicial sets

* [[simplicial set]]

* [[model structure on simplical sets]]

#### Simplicial presheaves

* [[simplicial presheaf]]

* [[model structure on simplicial presheaves]]

##### Good covers and split hypercovers

* [[Cech nerve]]

* [[good open cover]]

* [[split hypercover]]

+-- {: .num_prop #DifferentiablyGoodCoverGivesSPlitHyperCoverOverCartSp}
###### Proposition

For $X$ a [[smooth manifold]] let $\{U_i \hookrightarrow X\}_i$ be an [[open cover]]. This is a _differentiably good open cover_, def. \ref{DifferentiallyGoodOpenCover}, precisely if the corresponding  [[Cech nerve]] $C(\{U_i\}) \to X$ in $sPh(CartSp)_{proj,loc}$ is a [[split hypercover]].

=--



### Semantic Layer
 {#SmoothHomotopyTypesSemanticLayer}

#### $\infty$-Toposes

* [[(∞,1)-topos]]

##### Slice $\infty$-toposes
 {#SlicedInfinityToposes}

* [[slice (∞,1)-topos]]


##### Local, $\infty$-connected and cohesive $\infty$-toposes

* [[local (∞,1)-topos]]

* [[locally ∞-connected (∞,1)-topos]]

* [[cohesive (∞,1)-topos]]

#### The $\infty$-topos of smooth $\infty$-groupoids

* [[Lie groupoid]], [[differentiable stack]]

* [[smooth ∞-groupoid]]

##### Local $\infty$-Connectedness   {#InfinityConnectednessOfSmoothInfinityGrpd}

(...)

##### Locality 

(...)

##### Cohesion 

(...)

### Syntactic Layer
 {#SmoothHomotopyTypesSyntacticLayer}

#### Identity types
 {#IdentityTypes}

* [[identity type]]



#### Homotopy type theory

* [[h-level]]


* [[homotopy type theory]]


#### Cohesive modality II: flat types

**flat type** $\flat A$

maps $X \to \flat \mathbf{B}G$ are flat $G$-connections


$$
  \mathbf{B}G \colon Type
  \;\vdash\;
  UnderlyingBundle_{\mathbf{B}G} \colon \flat \mathbf{B}G \to \mathbf{B}G
$$

## **Groups**
 {#NGroups}

### Model Layer

#### 1-Groups

##### Discrete

* [[group]]

* [[delooping]] [[homotopy 1-type]]

##### Topological and Lie groups

* [[topological group]]

* [[Lie group]]

#### Simplicial groups

##### Discrete

* [[simplicial group]]

##### Abelian

* [[abelian group]]

##### Topological and Lie simplicial groups

* [[simplicial topological space]]

* [[geometric realization of simplicial topological spaces]]

#### 2-Groups

##### Discrete

* [[2-group]]

* [[crossed module]]

##### Braided and abelian

* [[braided 2-group]]

* [[symmetric 2-group]]

#### Abelian $\infty$-groups

##### Chain complex

* [[chain complex]]

##### Spectrum

* [[spectrum]], [[infinite loop space]]

##### Dold-Kan correspondence

* [[simplicial group]], [[Dold-Kan correspondence]], [[chain complex]]

* [[stable Dold-Kan correspondence]]

#### Cohomology

* [[cohomology]]

##### Nonabelian cohomology

* [[nonabelian cohomology]]

##### Abelian sheaf cohomology
 {#AbelianSheafCohomology}

* [[abelian sheaf cohomology]]

* [[Cech cohomology]]


### Semantic Layer

#### $A_\infty$-types

* [[A-infinity space]]

#### $\infty$-Groups

* [[infinity-group]]

* [[looping and delooping]]



### Syntactic Layer


#### Pointed connected types

* [[connected type]]

#### Identity types of connected types

(...)


## **Principal bundles**
 {#PrincipalBundles}
 {#PrincipalNBundles}

### Model Layer

#### Connected groupoids

any [[Lie group]] $G$ induces its [[delooping]] [[Lie groupoid]] 
  
$$
  \mathbf{B}G
  =
  * \sslash G
  = 
  \left(
     G \stackrel{\to}{\to} * 
  \right)
  \,.
$$

#### Universal principal bundle

* [[groupal model for universal principal infinity-bundles]]

#### Principal bundles

also

$$
  \mathbf{E}G
  =
  G \sslash G
  = 
  \left(
     G\times G \stackrel{\overset{\cdot}{\to}}{\underset{p_1}{\to}} G 
  \right)
  \,.
$$

canonical map

$$
  \array{
    \mathbf{E}G
    \\
    \downarrow
    \\
    \mathbf{B}G
  }
$$

[[universal principal bundle]]

for $X$ a [[smooth space]] a $G$-[[principal bundle]] over $X$ is a smooth space $P$ with map $P \to X$ such that there is a diagram 

$$
  \array{ 
     P &\stackrel{\simeq}{\leftarrow}& \tilde P &\to& \mathbf{E}G
     \\
     \downarrow && \downarrow &pb& \downarrow
     \\
     X &\stackrel{\simeq}{\leftarrow}& \tilde X &\underset{g}{\to}& \mathbf{B}G
  }
$$

where the left horizontal morphisms are [[weak equivalences]]
and the right square is a [[pullback]]


#### Weakly principal simplicial bundles

* [[simplicial principal bundle]]



### Semantic Layer

#### Principal $\infty$-bundles

* [[homotopy fiber]]

* [[homotopy colimit]]

* [[principal infinity-bundle]]

### Syntactic Layer

* [[connected type]]



## **Reduction of structure groups**
 {#ReductionOfStructureGroups}

### Model Layer

#### $G$-Structure

$$
  \mathbf{B}G \to \mathbf{B}K
$$

given a $K$-[[principal bundle]]

$$
  \array{
    \tilde X &\to &\mathbf{B}K
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
$$

a [[reduction of the structure group]] along $G \to K$ is

$$
  \array{
    \tilde X &&\to&& \mathbf{B}G
    \\
    & \searrow &\swArrow_{e}& \swarrow
    \\
    && \mathbf{B}K
  }
$$

#### Examples

##### Vielbein, orthogonal structure, Riemannian geometry
 {#RiemannianGeometry}

* [[vielbein]], [[orthogonal structure]]

[[reduction of the structure group]] along

$\mathbf{B}O(n) \to \mathbf{B}GL(n)$

$$
  \array{
    \tilde X &&\to&& \mathbf{B}O(n)
    \\
    & {}_{\mathllap{\vdash T \Sigma}}\searrow &\swArrow_{e}& \swarrow
    \\
    && \mathbf{B}GL(n)
  }
$$

$e$ is [[vielbein]]: definition of an [[orthonormal frame]]
at each point

###### Electromagnetism in gravitational background

example: the other 2 [[Maxwell equations]]: $\mathbf{d} \star F = j_{el}$.

[[Einstein-Maxwell theory]]

##### Almost complex structure

* [[almost complex structure]]

##### Almost Hermitean structure

* [[almost Hermitean structure]]

##### Almost symplectic structure

* [[almost symplectic structure]]

##### Metaplectic structure

* [[metaplectic structure]]

##### Metalinear structure

* [[metalinear structure]]

##### Generalized complex geometry

* [[generalized complex geometry]]

##### Type II geometry

* [[type II geometry]]

##### Generalized Calabi-Yau structure

* [[generalized Calabi-Yau manifold]]

##### Exceptional generalized geometry

* [[exceptional generalized geometry]]

##### Spin structure, String structure, Fivebrane structure

* [[spin structure]]

* [[string structure]]

* [[fivebrane structure]]



#### Smooth manifolds
  {#Manifolds}
  {#SmoothManifold}

A [[smooth manifold]] of [[dimension]] $n$ 

a [[smooth space]] with an [[atlas]] 

$$
  \{ \mathbb{R}^n \underoverset{\simeq}{\phi_i^{-1}}{\to} U_i \hookrightarrow X\}
$$ 

of [[coordinate charts]]. On each overlap $U_i \cap U_j$ of two charts, the [[partial derivatives]] of the corresponding [[coordinate transformations]]

$$
  \phi_j\circ \phi_i^{-1}
  : 
  U_i \cap U_j \subset \mathbb{R}^n \to \mathbb{R}^n
$$

form the [[Jacobian matrix]] of [[smooth functions]]

$$
  ((\lambda_{i j})^{\mu}{}_{\mu})
  \coloneqq
  \left[\frac{d}{d x^\nu} \phi_j \circ \phi_i^{-1} (x^\mu)
  \right]
  :
  U_i \cap U_j 
  \to 
  GL_n
$$

with values in invertible [[matrices]], hence in the
[[general linear group]] $GL(n)$. By construction (by the [[chain rule]]), these functions satisfy on triple overlaps of coordinate charts the [[matrix product]] equations

$$
  (\lambda_{i j})^\mu{}_\lambda (\lambda_{j k})^\lambda{}_{\nu} 
  = 
  (\lambda_{i k})^\mu{}_{\nu}
  \,,
$$

(here and in the following sums over an index appearing upstairs and downstairs are explicit)

hence the equation

$$
  \lambda_{i j} \cdot \lambda_{j k} = \lambda_{i k}
$$

in the [[group]] $C^\infty(U_i \cap U_j \cap U_k, GL(n))$ of smooth $GL(n)$-valued functions on the chart overlaps.

This is the _[[cocycle]] condition_ for a smooth [[Cech cohomology|Cech cocycle]] in degree 1 with coefficients in $GL(n)$ (precisely: with coefficients in the [[sheaf]] of [[smooth functions]] with values in $GL(n)$ ). We write

$$
  [(\lambda_{i j})] \in H^1_{smooth}(X, GL_n)
  \,.
$$

Formulated as [[smooth groupoids]]

* $X$ itself is a [[Lie groupoid]] $(X \stackrel{\to}{\to} X)$ with trivial morphism structure;

* from the atlas $\{U_i \to X\}$ we get the corresponding [[Cech groupoid]] 
  $$
    C(\{U_i\}) = 
    (\coprod_{i, j} U_i \cap U_j \stackrel{\to}{\to} \coprod_i U_i)
    = 
    \left\{
      \array{
         && (x,j)
         \\
         & \nearrow &=& \searrow
         \\
        (x,i) &&\to&& (x,k)
      }
      \;\;\;
      for\, x \in U_i \cap U_j \cap U_k
    \right\}
    \,,
  $$

  whose objects are the points in the atlas, with morphisms identifying lifts of a point in $X$ to different charts of the atlas;

#### Tangent bundle


The above situation is neatly encoded in the existence of a [[diagram]] of Lie groupoids of the form

$$
  \array{
     C(\{U_i\}) &\stackrel{\lambda}{\to}& \mathbf{B} GL(n).
     \\
     {}^{\mathllap{\simeq}}\downarrow
     \\
     X
  }
  \,,
$$

where

* the left morphism is [[stalk]]-wise (around small enough [[neighbourhoods]] of each point) an [[equivalence of groupoids]] (we make this more precise in a moment);

* the horizontal functor has as components the functions $\lambda_{i j}$ and its functoriality is the cocycle condition $\lambda_{i j} \cdot \lambda_{j k} = \lambda_{i k}$.


A [[natural transformation|transformation]] of smooth functors $\lambda_1 \Rightarrow \lambda_2 : C(\{U_i\}) \to \mathbf{B} GL(n)$ is precisely a [[coboundary]] between two such cocycles.

### Semantics Layer

#### Manifolds modeled on an object $V$

+-- {: .num_defn }
###### Definition

Let $V \in \mathbf{H}$. We say that a **$V$-[[atlas]]** for an object $X \in \mathbf{H}$ is an [[effective epimorphism]]

$$
  a \colon \coprod_{i \in I} V \to X
$$

out of a [[coproduct]] of copies of $V$, such the [[fiber product]] of $a$ with itself is again a coproduct of $V$s and such that all the components of the two [[projections]] out of it are [[monomorphism in an (∞,1)-category|monomorphisms]].

An object $X$ that admits a $V$-atlas we call a **$V$-[[manifold]]**.

=--


### Syntax Layer

(...)



## **Representations and Associated bundles**
 {#AssociatedNBundle}

### Model Layer

#### Actions

* [[action]]


#### Spin geometry

* [[spin group]]

* [[spin representation]]



$$
  \array{
    V &\to& V \sslash Spin
    \\
    && \downarrow
    \\
    && \mathbf{B}Spin
  }
$$

* [[spinor bundle]]

* [[spinor]]

$$
  \array{
    X &&\stackrel{\psi}{\to}&& V \sslash Spin
    \\
    & \searrow &\swArrow& \swarrow
    \\
    && \mathbf{B}Spin
  }
$$

#### Associated bundle

* [[associated bundle]]

#### Representations up to coherent homotopy

* [[infinity-representation]]



### Semantic Layer


#### $\infty$-Actions

[[∞-action]]

  $$
    \array{
      V &\to& V\sslash G
      \\
      && \downarrow
      \\
      && \mathbf{B}G
    }
  $$

#### Associated $\infty$-bundles

* [[associated infinity-bundle]]

$$
  \array{
    E &\to& V\sslash G
    \\
    \downarrow &pb& \downarrow
    \\
    \tilde X &\to& \mathbf{B}G
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
$$

* [[section]]

$$
  \array{
    X &&\stackrel{\sigma}{\to}&& V \sslash G
    \\
    & \searrow &\swArrow_{\simeq}& \swarrow
    \\
    && \mathbf{B}G
  }
$$


### Syntactic Layer


#### The context of a pointed connected type: representation theory

(...)

#### Dependent product over a pointed connected type: invariants

(...)

#### Dependent sum over a pointed connected type: quotients 

(...)




## **Flat connections**
 {#FlatConnections}

### Model Layer

#### Flat 1-connections

* [[flat connection]]

$X$ [[connected topological space|connected]], $\pi_1(X) \in $[[Grp]] its [[fundamental group]] for any choice of basepoint, then the [[holonomy]] pairing

$$
  hol \colon [S^1,X]\times H^1_{conn}(X,G) \to G
$$

descends to homotopy classes of (based) loops

$$
  hol
  \colon
  H^1_{conn,flat}(X,G)
  \stackrel{\simeq}{\to}
  Hom_{Grp}(\pi_1(X), G)/G
$$

to a _[[bijection]]_ from equivalence classes of [[flat conenction|flat]] $G$-[[principal connections]] to the [[quotient]] set of [[group]] [[homomorphisms]] $\pi_1(X) \to G$ modulo the [[adjoint action]] of $G$ on itself.

### Semantic Layer

+-- {: .num_defn #FlatCohesiveConnection}
###### Definition

For $G \in Grp(\mathbf{H})$ and $X \in \mathbf{H}$ a **flat $G$-connection** $\nabla$ on $X$ is a morphism

$$
  \nabla \colon X \to \flat \mathbf{B}G
  \,.
$$

We write

$$
  \mathbf{H}_{flat}(X, \mathbf{B}G)
  \coloneqq 
  \mathbf{H}(X, \flat \mathbf{B}G)
$$

and accordingly

$$
  H^1_{flat}{X, G} \coloneqq \pi_0 \mathbf{H}_{flat}(X,G)
$$

for the [[cohomology]] of $X \in \mathbf{H}$ **with flat coefficients**.

=--

+-- {: .num_remark}
###### Remark

By adjunction,

$$
  \frac{X \stackrel{\nabla}{\to} \flat \mathbf{B}G}{\Pi(X) \stackrel{transport(\nabla)}{\to} \mathbf{B}G}
$$

a flat $G$-connection is equivalently a morphism 

$$
  transport(\nabla) \colon \Pi(X) \to \mathbf{B}G
  \,.
$$

Since $\Pi(X)$ is the [[fundamtal infinity-groupoid]] of $X$, this manifestly encodes the [[higher parallel transport]] of the flat connection.

=--

+-- {: .num_defn}
###### Definition

Write

$$
  UnderlyingBundle_{\mathbf{B}G} \colon \flat \mathbf{B}G \to \mathbf{B}G
$$

for the $(Disc \vdash \Gamma)$-[[unit of an adjunction|counit]]-

=--


+-- {: .num_defn #UnderlyingBundleOfFlatConnection}
###### Definition

For $\nabla \colon X \to \flat \mathbf{B}G$ the [[composition|composite]]

$$
  UnderlyingBundle(\nabla) 
   \colon 
  X 
    \stackrel{\nabla}{\to} 
  \flat\mathbf{B}G
    \stackrel{UnderlyingBundle_{\mathbf{B}G}}{\to}
  \mathbf{B}G
$$

modulates a $G$-[[principal ∞-bundle]] on $X$, by def. \ref{spring}. This we call the **underlying $G$-principal bundle** of $\nabla$.

=--




$$
  ConstantPaths_{X} \colon X \to \Pi(X)
$$

### Syntactic Layer

$$
  \mathbf{B}G \colon Type
  \;\vdash \;
  UnderlyingBundle \colon \flat \mathbf{B}G \to \mathbf{B}G
$$

## **de Rham Coefficients**
 {#deRhamCoefficients}

### Model Layer

#### Lie-algebra valued differential 1-forms

+-- {: .num_defn #SheafOfLieAlgebraValuedForms}
###### Definition

Let $G$ be a [[Lie group]], and write $\mathfrak{g}$ for its [[Lie algebra]]. The set of [[Lie algebra valued differential 1-forms]] is the [[tensor product]]

$$
  \Omega^1(U,\mathfrak{g}) = \Omega^1(U) \otimes_{\mathbb{R}} \mathfrak{g}
  \,.
$$

flat forms:

$$
  \Omega^1_{flat}(U, \mathfrak{g}) = 
  \left\{
    \omega \in \Omega^1(U,\mathfrak{g}) |
    F_\omega = \mathbf{d} \omega + [\omega, \omega] = 0
  \right\}
  \,.
$$

=--

(...)

This is a [[smooth space]]

$$
  \Omega^1_{flat}(-,\mathfrak{g}) \in Smooth 0 Type
$$

For $\mathfrak{g} = Lie(\mathbb{R})$ we have

$$
  \Omega^1(-,Lie(\mathbb{R})) = \Omega^1
$$

and we write

$$
  \Omega^1_{flat}(-,Lie(\mathbb{R})) = \Omega^1_{cl}
$$


Below we see

$$
  \flat_{dR}\mathbf{B}G \simeq \Omega^1_{flat}(-,\mathfrak{g})
$$

#### The de Rham complex

* [[de Rham complex]]

* [[de Rham cohomology]]

* [[de Rham theorem]]

Below we see that 

$$
  \flat_{dR}\mathbf{B}^n \mathbb{R} 
    \simeq
  \flat_{dR}\mathbf{B}^n U(1)
   \simeq
  DK[ \Omega^1(-) \stackrel{\mathbf{d}}{\to} \Omega^2(-) \stackrel{\mathbf{d}}{\to}\cdots \stackrel{\mathbf{d}}{\to} \Omega^n_{cl}(-)]
 \,.
$$

### Semantic Layer

#### De Rham coefficient objects

+-- {: .num_defn #deRhamCoefficientObject}
###### Definition


For $G \in Gpr(\mathbf{H})$, its **de Rham coefficient object**
is the [[homotopy pullback]]

$$
  \flat_{dR} \mathbf{B}G \coloneqq \flat \mathbf{B}G \times_{\mathbf{B}G} * 
$$

in

$$
  \array{
     \flat_{dR} \mathbf{B}G &\stackrel{UnderlyingConnection}{\to}& \flat \mathbf{B}G
     \\
     \downarrow &pb& \downarrow^{\mathrlap{UnderlyingBundle}}
     \\
     * &\to& \mathbf{B}G
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This pullback diagram expresses that [[generalized element|elements]] of $\flat_{dR}\mathbf{B}G$ are flat $G$-connections $\nabla \colon X \to \flat \mathbf{B}G$, def. \ref{FlatCohesiveConnection} equipped with a trivialization of their underlying $G$-principal bundle, def. \ref{UnderlyingBundleOfFlatConnection}.

=--


#### Recovering smooth differential forms from cohesive de Rham coefficients
 {#OrdinaryDifferentialFormsFromSmoothCohesion}

Let $\mathbf{H} = $ [[Smooth∞Grpd]]. All [[smooth manifolds]] and sheaves on smooth manifolds etc. in the following are canonically regarded as objects in this $\mathbf{H} = Sh_\infty(CartSp)$.

+-- {: .num_prop #DeRhamCoefficientsOfLieGroup}
###### Proposition

For $G$ a [[Lie group]], the de Rham coefficient object $\flat_{dR}\mathbf{B}G$, def. \ref{deRhamCoefficientObject} of its [[delooping]] is given by the [[sheaf]] of flat [[Lie algebra valued differential 1-forms]] $\Omega^1_{flat}(-,\mathfrak{g})$, def. \ref{SheafOfLieAlgebraValuedForms}, for $\mathfrak{g}$ the [[Lie algebra]] of $G$:

$$
  \flat_{dR}\mathbf{B}G \simeq \Omega^1_{flat}(-,\mathfrak{g})
  \,.
$$

=--

This is disucssed at _[smooth ∞-groupoid - structures - de Rham coefficients for BG with G a Lie group](smooth+infinity-groupoid+--+structures#deRhamWithCoefficientsInBOfLieGroup)_.

Write $U(1)$ for the [[circle group]] regared as a [[Lie group]] in the standard way.

+-- {: .num_prop}
###### Proposition

For $n \in \mathbb{N}$, the de Rham coefficient object $\flat_{dR}\mathbf{B}^n U(1)$, def. \ref{deRhamCoefficientObject}, of the $n$-fold [[delooping]] of $U(1)$ is given by the image under the [[Dold-Kan correspondence]] 

$$
  DK \colon : Sh(CartSp, Ch_\bullet) \to Sh(CartSp, sSet)
  \to L_{lwhe} Sh(CartSp, sSet) \simeq \mathbf{H}
$$ 

of the truncated [[de Rham complex]] of sheaves of differential forms, 

$$
  \begin{aligned}
   \flat_{dR}\mathbf{B}^n U(1)
   &\simeq
   \flat_{dR} \mathbf{B}^n \mathbb{R}
   \\
   & \simeq
   DK[\Omega^1(-) \stackrel{\mathbf{d}}{\to} \cdots \stackrel{\mathbf{d}}{\to} \Omega^n_{cl}(-)]
    \\ 
   & \simeq DK[\Omega^1_{cl}(-) \to 0 \to  \cdots \to 0]
  \end{aligned}
  \,.
$$

=--

This is discussed at _[smooth ∞-groupoid - structures - de Rham coefficients for the circle n-groups](smooth+infinity-groupoid+--+structures#deRhamCoefficientsInBnU1)_.

### Syntactic Layer

$$
  \begin{aligned}
    \flat_{dR}(\mathbf{B}G \colon Type)\; \colon & Type
    \\
    \coloneqq & 
     \;\;
    \sum_{\nabla \colon \flat \mathbf{B}G}
    (  UnderlyingBundle(\nabla) = * )
  \end{aligned}
$$

## **Maurer-Cartan forms**
 {#MaurerCartanForms}


### Model Layer
 {#MaurerCartanLayerMod}

#### Maurer-Cartan form on a Lie group
 {#MaurerCartanFormOnLieGroup}

* [[Maurer-Cartan form]]

$$
  \theta_G \colon G \to \Omega^1_{flat}(-,\mathfrak{g})
$$


Consider

$$
  \flat_{dR} \mathbf{B}\mathbb{R}  = \Omega^1_{cl}
$$

the Maurer-Cartan form on $\mathbb{R}$ is the [[de Rham differential]]

$$
  \theta_{\mathbb{R}} = \mathbf{d} \colon \mathbb{R} \to \Omega^1_{cl} \hookrightarrow \Omega^1
  \,.
$$





### Semantic Layer

#### Maurer-Cartan form on a cohesive $\infty$-group

Let $G \in Grp(\mathbf{H})$. 

Use the [[pasting law]] together with the fact that $\flat$ is
[[right adjoint]] and hence preserves [[limits]] to get $\theta$ in

$$
  \array{
    G &\to& *
    \\
    \downarrow^{\mathrlap{\theta}} & pb & \downarrow
    \\
    \flat_{dR} \mathbf{B}G &\to& \flat \mathbf{B}G
    \\
    \downarrow &pb& \downarrow
    \\
    * &\to& \mathbf{B}G
  }
$$

+-- {: .num_defn #GeneralAbstractMaurerCartanForm}
###### Definition

This is the **[[Maurer-Cartan form]]** on $G$

$$
  \theta \colon G \to \flat_{dR} \mathbf{B}G
  \,.
$$

=--

#### Maurer-Cartan forms on smooth $\infty$-groups

+-- {: .num_prop}
###### Proposition

For $G$ a [[Lie group]] canonically regarded  in $\mathbf{H} = $[[Smooth∞Grpd]] the general abstract morphism

$$
  \theta_G \colon G \to \flat_{dR}\mathbf{B}G
$$

is identified, via the identification $\flat_{dR}\mathbf{B}G \simeq \Omega^1_{flat}(-,\mathfrak{g})$  of prop. \ref{DeRhamCoefficientsOfLieGroup} and the [[Yoneda lemma]], with the traditional [[Maurer-Cartan form]] 

$$
  \theta_G \in \Omega^1_{flat}(G, \mathfrak{g})
  \,.
$$

=--

#### Cohesive differentiation 
 {#CohesiveDifferentiation}

The Maurer-Cartan form on the [[line object]]

$$
  \theta_{\mathbb{R}} \colon \mathbb{R} \to \Omega^1_{cl}(-,\mathbb{R})
$$

is the [[de Rham differential]], 

$$
  \mathbf{d} = \theta_{\mathbb{R}}
  \,.
$$

#### Universal curvature characteristic forms

For $G = \mathbf{B}^n U(1)$

$$
  curv \colon \mathbf{B}^n U(1) \to \flat_{dR} \mathbf{B}^{n+1}U(1)
$$

sends a circle $n$-bundle to the curvature of a pseudo-connection on it.

### Syntactic Layer

(...)

## **Principal connections**
 {#PrincipalConnections}

### Model Layer

#### Circle-principal connections
 {#CirclePrincipalConnections}

[[Dirac charge quantization]] says that the
[[electromagnetic field]] is only locally in general a map

$$
  \array{
    && \Omega^1(-)
    \\
    & {}^{\mathllap{A}}\nearrow & \downarrow^{\mathrlap{\mathbf{d}}}
    \\
    X &\stackrel{\omega}{\to}& \Omega^2_{cl}
  }
$$

globally it is instead a map

$$
  \array{
    && \mathbf{B}U(1)_{conn}
    \\
    & {}^{\nabla}\nearrow & \downarrow^{F_{(-)}}
    \\
    X &\stackrel{\omega}{\to}& \Omega^2_{cl}
  }
$$

where

$$
  \array{  
    \mathbf{B}U(1)_{conn} &\stackrel{F_{(-)}}{\to}& \Omega^2_{cl}
    \\
    \downarrow &pb& \downarrow
    \\
    \mathbf{B}U(1)_{diff} &\to& \Omega^{1 \leq \bullet \leq 2}_{cl}
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}U(1)
  }
$$

[[circle bundle with connection]]

the [[smooth groupoid]] is

$$
  \mathbf{B}U(1)_{conn}
  =
  \Omega^1(-) \sslash U(1)
$$

quotient of $\Omega^1(-)$ by $U(1)$-[[gauge transformations]]

for

$$
  A,A' : X \to \Omega^1(-)
$$

a [[gauge transformation]] $A \to A'$
is $\lambda : X \to U(1)$ with

$$
  A' = A + \mathbf{d} log \lambda
$$

#### Dirac charge quantization and the electromagnetic field
 {#DiracChargeQuantizationAndElectromagneticField}

* [[Dirac charge quantization]]

* [[electromagnetic field]]

#### Principal 1-connection

* [[principal connection]]

#### Covariant derivatives

* [[covariant derivative]]

$$
  \array{
     (V\sslash G)_{conn}
     \\
     \downarrow
     \\
     \mathbf{B}G_{conn}
  }
$$

$$
  \array{
    \tilde X &&\stackrel{(\sigma, \nabla \sigma)}{\to}&& (V \sslash G)_{conn}
    \\
    & \searrow &\swArrow& \swarrow
    \\
    && \mathbf{B}G_{conn}
  }
$$




#### Deligne cohomology and Cheeger-Simons differential characters

* [[Deligne cohomology]]

* [[Cheeger-Simons differential character]]

* [[Beilinson-Deligne cup product]]

* [[fiber integration in ordinary differential cohomology]]

#### Circle-principal 2-connection

* [[circle n-group|circle 2-group]] [[principal 2-bundle]]

* [[circle n-bundle with connection|circle 2-bundle with connection]]

#### Magnetic charge and the B-field

* [[magnetic charge]], [[B-field]]

#### Circle-principal 3-connection

* [[circle n-group|circle 3-group]] [[principal 3-bundle]]

* [[circle n-bundle with connection|circle 3-bundle with connection]]

#### The 3d Chern-Simons action functional and the C-field

* [[supergravity C-field]]

#### Circle-principal $n$-connection
  {#CirclePrincipalNConnections}

* [[ordinary differential cohomology]]

* [[circle n-bundle with connection]]

### Semantic Layer

#### Differential cohomology
 {#SmoothDifferentialCohomology}

Let $G \in Grp(\mathbf{H})$ be a [[braided ∞-group]]. Equivalently, let its [[delooping]] $\mathbf{B}G \in \mathbf{H}$ be itself equipped with the structure of an [[∞-group]]. Write

$$
  \mathbf{B}^2 G \in \mathbf{H}
$$

for the corresponding double [[delooping]].

+-- {: .num_defn #UniversalCurvatureCharacteristic}
###### Definition

Write 

$$
  curv_{G} 
   \coloneqq 
  \theta_{\mathbf{B}\mathbb{G}}
  \colon
  \mathbf{B}G
  \to
  \flat_{dR} \mathbf{B}^2 G
$$

for the [[Maurer-Cartan form]] on the [[∞-group]] $\mathbf{B}G$, def. \ref{GeneralAbstractMaurerCartanForm}. We call this the **universal curvature characteristic** of $G$.

=--

+-- {: .num_defn #GeneralConcreteDifferentialCohomology}
###### Definition

The **[[differential cohomology]]** with [[coefficients]] in $\mathbf{B}G$ is [[cohomology]] in the [[slice (∞,1)-topos]] $\mathbf{H}_{/\flat_{dR} \mathbf{B}^2 G}$ with [[coefficients]] in $curv_G$

$$
  \mathbf{H}_{/\flat_{dR}\mathbf{B}^2 G}(-, curv_G)
  \,.
$$

=--

#### Differential-form curvatures


$$
  \array{
     \mathbf{B}^n \mathbb{G} &\to& \Omega^{n+1}_{cl}(-)
     \\
     \downarrow &pb& \downarrow^{\mathrlap{}}
     \\
     \mathbf{B}\mathbb{G} 
       &\stackrel{curv}{\to}&
     \flat_{dR} \mathbf{B}^2 \mathbb{G}
  }
$$

presented by [[ordinary differential cohomology]]


#### Higher holonomy
 {#Holonomy}

* [[higher holonomy]]

$$
  \exp(2 \pi i \int_{\Sigma}(-))
  \colon
  [\Sigma,\mathbf{B}^n U(1)_{conn}]
  \stackrel{conc \circ \tau_0}{\to}
  U(1)
$$

### Syntactic Layer

#### The dependent curvature type


The universal curvature characteristic, def. \ref{UniversalCurvatureCharacteristic}, has the [[syntax]]

$$
  \vdash curv_{G} \colon \mathbf{B}G \to \flat_{dR} \mathbf{B}^2 G
  \,.
$$

Regarded as a [[dependent type]] in the de Rham coefficient [[context]] this is

$$
    \omega \colon \flat_{dR}\mathbf{B}^2 G
    \;
    \vdash 
    \;
    \underset{\mathbf{c} \colon \mathbf{B}G}{\sum} 
    \left(
      curv_G\left(\mathbf{c}\right)
      \simeq \omega
    \right)
  \colon
  Type
$$

Therefore the [[syntax]] for a domain object $F \colon X \to \flat_{dR} \mathbf{B}^2 G$ in this [[context]] is

$$
  \omega \colon \flat_{dR} \mathbf{B}^2 G
  \;\vdash\;
  \underset{x \colon X}{\sum} 
  \left(
    F_x \simeq \omega
  \right)
  \colon Type
$$

and the [[syntax]] for a [[cocycle]] 

$$
  \array{
    X &&\stackrel{\bar P}{\to}&& \mathbf{B}G
    \\
    & {}_{\mathllap{F}}\searrow &\swArrow_{\nabla}& \swarrow_{\mathrlap{curv_G}}
    \\
    && \flat_{dR} \mathbf{B}^2 G
  }
$$

in [[differential cohomology]], def. \ref{GeneralConcreteDifferentialCohomology}, on $(X,F)$ is hence

$$
  \vdash \;
  (\bar P,\nabla)
  \colon
  \underset{\omega \colon \flat_{dR} \mathbf{B}^2 G}{\prod}
  \left(
    \left(
    \underset{x \colon X}{\sum}
    \left(
      F_x \simeq \omega
    \right)
    \right)
    \to 
    \left(
    \underset{\mathbf{c} \colon \mathbf{B}G}{\sum}
    \left(
      curv_G(\mathbf{c}) \simeq \omega
    \right)
    \right)
  \right)
$$

#### Fixed curvature twists

$$
  \begin{aligned}
    (\mathbf{B}^n \mathbb{G} \colon Type)_{conn} \colon & Type
    \\
     \coloneqq &  
     \sum_{\mathbf{c} \colon \mathbf{B}\mathbb{G}}
     \sum_{\omega \colon \Omega^{n+1}_{cl}}
     \left(
       curv(\mathbf{c}) = \omega
     \right)
  \end{aligned}
$$





## **Characteristic classes**
 {#CharacteristicClasses}


### Model Layer

#### Magnetic charge and first Chern class

* [[magnetic charge]], [[first Chern class]]

$$
  \array{
    && && \mathbf{B}(\mathbb{R}\sslash \mathbb{Z})
    &\to& \mathbf{B}^2 \mathbb{Z}
    \\
    && && \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}\mathbb{Z} 
      &\to&  
    \mathbf{B}\mathbb{R} 
      &\to&  
    \mathbf{B}U(1)
  }
$$

$$
  \mathbf{c}_1
   :
  \pi_0\mathbf{H}(X,\mathbf{B}U(1))
  \to 
  \pi_0 \mathbf{H}(X, \mathbf{B}^2 \mathbb{Z})
  \simeq
  H^2(X, \mathbb{Z})
$$

#### Yang-Mills instanton number and second Chern class

* [[QCD instanton]]


### Semantic Layer

#### Gauge theory Lagrangeans

a differential characteristic class

$$
  \mathbf{L}
  \colon
  \mathbf{B}G_{conn}
  \to
  \mathbf{B}^n U(1)_{conn}
$$

is an (extended) [[Lagrangean]] for [[schreiber:infinity-Chern-Simons theory]]. 

The corresponding [[action functional]] is discussed in [Semantic Layer - Action functionals from Lagrangeans](#SemLayerActionFunctionalsFromLagrangeans).


### Syntactic Layer

(...)



## **Integration**
 {#Integration}

By the discussion in _[Differential forms](#DifferentialForms)_ and _[Principal connections](#PrincipalConnections)_, [[differential forms]] and more generally [[connection on a bundle|connections]] may be regarded as [[infinitesimal space|infinitesimal]] [[measures]] of _change_, of _displacement_. The discussion in _[Differentiation](#Differentiation)_ showed how to extract from a _finite_ but [[cohesion|cohesive]] (e.g. smoothly continuous) displacement all its infinitesimal measures of displacements by [[differentiation]]. 

Here we discuss the reverse operation: _[[integration]]_ is a construction from a [[differential form]] of the corresponding finite cohesive displacement. More generally this applies to any [[connection on a bundle|connection]] and is then called the _[[nLab:parallel transport]]_ of the connection, a term again referring to the idea that a finite displacement proceeds pointwise in parallel to a given infinitesimal displacement.

Under good conditions this construction can proceed literally by "adding up all the infinitesimal contributions" and therefore [[integration]] is traditionally thought of as a generalization of forming [[sums]]. Therefore one has the notation "$\int_{\Sigma} \omega$"
for the [[integral]] of a [[differential form]] $\omega$ over a space $\Sigma$, as a variant of the notation "$\sum_{S} f$" for the [[sum]] of values of a [[function]] on a [[set]] $S$. For the case of integrals of connections the corresponding parallel transport expression is often denoted by an exponentiated integral sign "$\mathcal{P} \exp(\int_\Sigma \omega)$", referring to the fact that the passage from infinitesimal to finite quantities involves also the passage from [[Lie algebra]] data to [[Lie group]] data ("[[Lie integration|exponentiated Lie algebra data]]"). 

However, both from the point of view of [[gauge theory]] [[physics]] as well as from the [[general abstract]] perspective of [[cohesive homotopy type theory]] another characterization of integration is more fundamental: the [[integral]] $\int_\Sigma \omega$ of a [[differential form]] $\omega$ (or more generally of a [[circle n-bundle with connection|connection]]) is an [[invariant]] under those [[gauge transformations]] of $\omega$ that are trivial on the [[boundary]] of $\Sigma$, and it is the _[[universal construction|universal]]_ such invariant, hence is uniquely characterized by this property.

In traditional accounts this fact is referred to via the _[[Stokes theorem]]_ and its generalizations (such as the [[nonabelian Stokes theorem]]), which says that the [[integral]]/[[parallel transport]] is indeed _[[invariant]]_ under gauge transformations of differential forms/connections. That this invariance actually characterizes the integral and the parallel transport is rarely highlighted in traditional texts, but it is implicit for instance in the old "path method" of [[Lie integration]] (discussed below in _[Lie integration](#LieIntegration)_) as well as in the famous characterization of [[flat connections]], discussed above in _[Flat 1-connections](#Flat1Connections)_: 

for $X$ a [[connected topological space|connected]] [[manifold]] and for $G$ a [[Lie group]], the operation of sending a [[flat connection|flat]] $G$-[[principal connection]] $\nabla$ to its [[parallel transport]] $\gamma \mapsto hol_{\gamma}(\nabla)$ around [[loops]] $\gamma\colon S^1 \to X$, hence to the [[integral]] of the connection around all possible loops (its [[holonomy]]),  for any fixed basepoint

$$
  hol \coloneqq \mathcal{P} \exp(\int_{(-)} (-)) 
  \;\colon\; 
  H^1_{conn, flat}(X,G) 
   \stackrel{\simeq}{\to} 
  Hom_{Grp}(\pi_1(X) , G)/G
$$

exhibits a [[bijection]] between gauge  [[equivalence classes]] of connections and [[group]] homomorphisms from the [[fundamental group]] $\pi_1(X)$ of $X$ to the [[gauge group]] $G$ (modulo [[adjoint action|adjoint]] $G$-action from gauge transformations at the base point, hence at the integration boundary). This is traditionally regarded as a property of the definition of the [[parallel transport]] $\mathcal{P} \exp(\int_{(-)}(-))$ by [[integration]]. But being a [[bijection]], we may read this fact the other way round: it says that forming equivalence classes of flat $G$-connections is a way of computing their [[integral]]/[[parallel transport]]. 

We saw a generalization of this fact to non-closed forms and non-flat connections already in the discussion at _[Differential 1-forms as smooth incremental path measures](##1FormsAsSmoothFunctors)_, where gauge equivalence classes of differential forms are shown to be equivalently assignments of [[parallel transport]] to [[path groupoid|smooth paths]].

This is also implied by the above discussion: for $\nabla \in H^1_{conn}(X,G) $ any non-flat connection and $\gamma \colon S^1 \to X$ a trajectory in $X$, we may form the [[pullback of differential forms|pullback]] of $\nabla$ to $S^1$. There it becomes a necessarily flat connection $\gamma^* \nabla \in H^1_{conn, flat}(S^1,G)$, since the [[curvature]] [[differential 2-form]] necessarily vanishes on the 1-[[dimension|dimensional]] [[manifold]] $S^1$. Accordingly, by the above bijection, forming the gauge [[equivalence class]] of $\gamma^* \nabla$ means to find a group homomorphism

$$
  \mathbb{Z} \simeq \pi_1(S^1) \to G
$$  

modulo conjugation (modulo nothing if $G$ is [[abelian group|abelian]], such as $G = U(1)$) and since $\mathbb{Z}$ is the [[free group]] on a single generator this is the same as finding an element 

$$
  hol_\gamma(\nabla)
  = 
  \mathcal{P} \exp(\int_\gamma \gamma^*\nabla)
  \in 
  G
  \,.
$$

This total operation of first pulling back the connection and then forming its [[integration]] (by taking gauge equivalence classes) is called the _[[transgression]]_ of the original 1-form connection on $X$ to a 0-form connection on the [[loop space]] $[S^1,X]$.

Below in the [Model Layer](#IntegrationModelLayer) we discuss the classical examples of [[integration]]/[[parallel transport]] and their various generalizations in detail. Then in the [Semantic Layer](#IntegrationSemanticLayer) we show how indeed all these constructions are obtained forming [[equivalence classes]] in the [[(∞,1)-topos]] of [[smooth ∞-groupoids|smooth homotopy types]], hence by _[[truncated object in an (∞,1)-category|truncation]]_ (followed, to obtain the correct cohesive structure, by _concretification_, def. \ref{ConcreteObjectsAndConcretification}). 





 
### Model Layer
 {#IntegrationModelLayer}

#### Integration

##### Integration over a coordinate patch

For $n \in \mathbb{N}$ let

$$
  C^n 
  \coloneqq
  \{
    \vec x \in \mathbb{R}^n
    |
    \forall_i (0 \leq x_i \leq 1)
  \}
  \hookrightarrow
  \mathbb{R}^n
$$

be the standard unit [[cube]]. 

Let 

$$
  \omega \in \Omega^n(\mathbb{R}^n)
$$

be a [[differential n-form]]. 

$$
  \omega = f \mathbf{d} x^1 \wedge \mathbf{d} x^2 \wedge \cdots \wedge \mathbf{d} x^n
  \,.
$$

Let $Partitions(C^k)$ be the [[poset]] whose elements are partitions of the unit $n$cube $C^n$ into $N^n$ subcubes, for $N \in \mathbb{N}$, ordered by inclusion. 

Let 

$$
  \sum_{(-)} \omega
  \colon
  Partitions(C^k)
  \to 
  \mathbb{R}
$$

be the function that sends

$$
  \frac{1}{N^n}
  \sum_{x^1 = 0}^N
  \sum_{x^2 = 0}^N
  \cdots
  \sum_{k^n = 0}^N
  f( x^1, \cdots, x^n )
  \,.
$$

Then 

$$
  \int_{C^k} \omega \colon \lim_{N} \sum_N \omega
  \,. 
$$

##### Integration of differential forms over a manifold
 {#IntegrationOfDifferentialFormsOverASmoothManifold}

Let $\Sigma$ be a [[closed manifold|closed]] [[orientation|oriented]] [[smooth manifold]] of [[dimension]] $k$

+-- {: .num_defn #IntegrationOfDifferentialFormsInTermsOfSmoothModuli}
###### Definition

For $n \in \mathbb{N}$, $n \geq k$, define the 
morphism of [[smooth spaces]]

$$
  \int_{\Sigma} \colon [\Sigma, \Omega^n] \to \Omega^{n-k}
$$

by declaring that over a [[coordinate chart]] $U \in$ [[CartSp]] 
it is the ordinary [[integration of differential forms]] over smooth manifolds

$$
  \int_{\Sigma, U} : \Omega^n(\Sigma\times U) \to \Omega^{n-k}(U)
  \,.
$$

=--

##### Integration in ordinary differential cohomology

* [[fiber integration in ordinary differential cohomology]]


#### Holonomy

##### Parallel transport

given $A \in \Omega^1(\Delta^1, \mathfrak{g})$

we say $f \in C^\infty(\Delta^1, G)$ is the [[parallel transport]] of $A$ if 

1. $f(0) = 1$

1. $f$ satisfies the [[differential equation]]

   $$
     \mathbf{d}f = A f
   $$

where on the right we have the differential of the left action of the group on itself.

In this case one writes

$$
  \mathcal{P} \exp\left(\int_{\Delta^1} A \right)
  \coloneqq
  f(1) 
$$

and calls it the _[[path ordered integral]]_ of $A$. Here the enire left hand side is primitive notation.

In the case that $G = U(1)$ this reproduces the ordinary [[integral]]

$$
  \left(G = \mathbb{R}\right)
  \Righarrow
  \mathcal{P} \exp(\int_{\Delta^1} A)
  = 
  \exp(i \int_{\Delta^1} A)
  \in 
  U(1)
$$

There is another way to express this [[parallel transport]],
related to [[Lie integration]]:

Define an [[equivalence relation]] on $\Omega^1(\Delta^1, \mathfrak{g})$ as follows: two 1-forms $A,A'$ are taken to be equivalent if there is a flat 1-form $\hat A \in \Omega^1_{flat}(D^2, \mathfrak{g})$ on the 2-[[disk]] such that its restriction to the upper semicircle is $A$ and the restriction to the lower semicircle is $\tilde A$.

If $G$ is [[simply connected topological space|simply connected]], then the [[equivalence classes]] of this relation form

$$
  \Omega^1(\Delta^1,\mathfrak{g})_{/\sim} \simeq
  G
$$

and the [[quotient]] map coincides with the [[parallel transport]]

$$
  \mathcal{P} \exp\left(\int_{\Delta^1} \left(-\right)\right)
  \colon
  \Omega^1(\Delta^1, \mathfrak{g})
  \to 
  \Omega^1(\Delta^1, \mathfrak{g})_{/\sim}
  \simeq
  G  
$$

Finally yet another perspective is this: consider the [[equivalence relation]] on $\Omega^1(\Delta^1, \mathfrak{g})$ where two 1-forms are regarded as equivalent if there is a [[gauge transformation]] $\lambda \in C^\infty(\Delta^1, G)$ with $\lambda(0) = e$ and $\lambda(1) = e$, then again 

$$
  \mathcal{P} \exp\left(\int_{\Delta^1} \left(-\right)\right)
  \colon
  \Omega^1(\Delta^1, \mathfrak{g})
  \to 
  \Omega^1(\Delta^1, \mathfrak{g})_{/\sim}
  \simeq
  G  
$$

is the parallel transport


##### Holonomy of a flat principal connection

if $X$ is connected then forming the [[holonomy]] of flat $G$-connections

$$ 
  hol
  \colon
  G Bund_{\nabla, flat}(X)
  \stackrel{\simeq}{\to}
  Hom_{Grp}(\pi_1(X), G)
$$

is an [[equivalence]], $\pi_1(X)$ the [[fundamental group]]. If $X$ is not connected then 

$$ 
  hol
  \colon
  G Bund_{\nabla, flat}(X)
  \stackrel{\simeq}{\to}
  Hom_{Grpd}(\Pi_1(X), \mathbf{B}G)
$$

is an equivalence.


#### Transgression
 {#Transgression}

What is called _[[transgression]]_ is the combination of 

1. passing a [[cocycle]] on some space $X$ with [[coefficients]] in some $A$ to a [[cocycle]] on a [[mapping space]] $[\Sigma,X]$ with coefficients in $[\Sigma,A]$ and 

1. [[integration|integrating]] the resulting coefficient over $\Sigma$ to obtain a $B$-valued cocycle on the mapping space, where $B$ is some recipient of an integration map of $A$-cocycles over $\Sigma$.

##### Transgression of differential forms
 {#TransgressionOfDifferentialForms}

Let $\Sigma_k$ be a [[closed manifold|closed]] [[smooth manifold]] of [[dimension]] $k$.

+-- {: .num_defn}
###### Definition

For $X \in \mathbf{H}$, the **[[transgression]] of [[differential forms]]** on $X$ to the [[mapping space]] $[\Sigma,X]$ is the morphism

$$
  \int_\Sigma [\Sigma,-]
  : 
  \Omega^n(X) \to \Omega^{n-k}([\Sigma,X])
$$

given on a differential form

$$
  (X \stackrel{\omega}{\to} \Omega^n) \in \Omega^n(X)
$$

as the [[composition]] of the [[mapping space]] operation with the [[integration of differential forms]], def. \ref{IntegrationOfDifferentialFormsInTermsOfSmoothModuli}:

$$
  \int_{\Sigma} [\Sigma,\omega]
   \;\colon\;
  [\Sigma, X] 
    \stackrel{[\Sigma, \omega]}{\to}  
  [\Sigma, \Omega^n]
    \stackrel{\int_{\Sigma}}{\to}
  \Omega^{n-k}
  \,.
$$

=--

We discuss some examples and applications:

* [Gauge coupling action functional of charged particle](#GaugeCouplingActionFunctionalOfChargedParticle)

* [Transgression of Killing form to symplectic form of Chern-Simons theory](#TransgressionOfKillingFormToSymplecticFormOfChernSimons)

###### Gauge coupling action functional of charged particle
 {#GaugeCouplingActionFunctionalOfChargedParticle}

Let $X \in \mathbf{H}$ and consider a [[circle group]]-[[principal connection]] $\nabla \colon X \to \mathbf{B}U(1)_{conn}$ over $X$. By the discussion in _[Dirac charge quantization and the electromagnetic field](#DiracChargeQuantizationAndElectromagneticField)_ above this encodes an [[elecrtromagnetic field]] on $X$. Assume for simplicity here that the underlying [[circle principal bundle]] is trivialized, so that then the connection is equivalently given by a differential 1-form

$$
  \nabla = A \colon X \to \Omega^1
  \,,
$$

the [[electromagnetic potential]].

Let then $\Sigma = S^1$ be the [[circle]].  The [[transgression]] of the electromagnetic potential to the [[loop space]] of $X$ 

$$
  \int_{S^1} [S^1, A]
   \;\colon\;
  [S^1, X]
    \stackrel{[S^1, A]}{\to}
  [S^1 , \Omega^1]
    \stackrel{\int_{S^1}}{\to}
  \Omega^0
  \simeq
  \mathbb{R}
$$

is the [[action functional]] for an [[electron]] or other electrically charged [[particle]] in the [[background gauge field]] $A$ is $S_{em} = \int_{S^1} [S^1, A]$.

The [[variational calculus|variation]] of this contribution in addition to that of the [[kinetic action]]  of the electron gives the _[[Lorentz force]]_ law describing the [[force]] exerted by the [[background gauge field]] on the electron.

###### Transgression of Killing form to symplectic form of Chern-Simons theory
 {#TransgressionOfKillingFormToSymplecticFormOfChernSimons}

Let $\mathfrak{g}$ be a [[Lie algebra]] with 
binary [[invariant polynomial]] 
$\langle -,-\rangle \colon \mathfrak{g} \otimes \mathfrak{g} \to \mathbb{R}$.

For instance $\mathfrak{g}$ could be a [[semisimple Lie algebra]] and $\langle -,-\rangle$ its [[Killing form]]. In particular if $\mathfrak{g} = \mathfrak{su}(n)$ is a [[matrix Lie algebra]] such as the [[special unitary Lie algebra]], then the Killing form is given by the [[trace]] of the product of two matrices.

This pairing $\langle -,-\rangle$ defines a differential 4-form on the [[smooth space]] of [[Lie algebra valued 1-forms]]

$$
  \langle F_{(-)} \wedge F_{(-)} \rangle
  \colon
  \Omega^1(-,\mathfrak{g})
   \stackrel{F_{(-)}}{\to}
  \Omega^2(-, \mathfrak{g})
   \stackrel{(-)\wedge (-)}{\to}
  \Omega^4(-, \mathfrak{g}\otimes \mathfrak{g})
   \stackrel{\langle-,-\rangle}{\to}
  \Omega^4
$$

Over a [[coordinate patch]] $U \in $ [[CartSp]] this sends a differential 1-form $A \in \Omega^1(U)$ to the differential 4-form

$$
  \langle F_A \wedge F_A \rangle \in \Omega^4(U)
  \,.
$$

The fact that $\langle -, - \rangle$ is indeed an _[[invariant polynomial]]_ means that this indeed extends to a 4-form on the smooth [[groupoid of Lie algebra valued forms]]

$$
  \langle F_{(-)} \wedge F_{(-)}\rangle
  \colon
  \mathbf{B}G_{conn}
  \to 
  \Omega^4
  \,.
$$

Now let $\Sigma$ be an [[orientation|oriented]] [[closed manifold|closed]] [[smooth manifold]].  The [[transgression]] of the above 4-form to the [[mapping space]] out of $\Sigma$ yields the 2-form

$$
  \omega
    \coloneqq
  \int_{\Sigma} \langle F_{(-)}\wedge F_{(-)}\rangle
   \colon
  \mathbf{\Omega}^1(\Sigma,\mathfrak{g})
   \hookrightarrow
  [\Sigma, \mathbf{B}G_{conn}]
    \stackrel{[\Sigma, \langle F_{(-)}\wedge F_{(-)}\rangle]}{\to}
  [\Sigma, \Omega^4]
    \stackrel{\int_{\Sigma}}{\to}
  \Omega^2
$$

to the [[moduli stack]] of [[Lie algebra valued 1-forms]] on $\Sigma$.

Over a [[coordinate chart]] $U = \mathbb{R}^n \in $ [[CartSp]] an element $A \in \mathbf{\Omega}^1(\Sigma,\mathfrak{g})(\mathbb{R}^n)$ is a $\mathfrak{g}$-valued 1-form $A$ on $\Sigma \times U$ with no leg along $U$. Its [[curvature]] 2-form therefore decomposes as

$$
  F_A = F_A^{\Sigma} + \delta A
  \,,
$$

where $F_A^{\Sigma} $ is the curvature component with all legs along $\Sigma$ and where

$$
  \delta A
  \coloneqq 
  - \sum_{i = 1}^n \frac{\partial}{\partial x^i} A \wedge \mathbf{d}x^i
$$

is the [[variational calculus|variational]] derivative of $A$.

This means that in the 4-form

$$
  \langle F_A \wedge F_A\rangle
  = 
  \langle F_A^\Sigma \wedge F_A^\Sigma \rangle
  + 
  2 \langle F_A^\Sigma \wedge \delta A\rangle 
  + 
  \langle \delta A \wedge \delta A\rangle 
  \in
  \Omega^4(\Sigma \times U)
$$

only the last term gives a 2-form contribution on $U$. Hence we find that the transgressed 2-form is

$$
  \omega = \int_\Sigma \langle \delta A \wedge \delta A\rangle
   \colon
  \mathbf{\Omega}^1(\Sigma, \mathfrak{g})
   \to
  \Omega^2
  \,.
$$

When restricted further to flat forms

$$
  \mathbf{\Omega^1}_{flat}(\Sigma,\mathfrak{g})
  \hookrightarrow
  \mathbf{\Omega^1}(\Sigma,\mathfrak{g})  
$$

which is the [[phase space]] of $\mathfrak{g}$-[[Chern-Simons theory]], then this is the corresponding [[symplectic form]] (by the discussion at _[Chern-Simons theory -- covariant phase space](Chern-Simons theory#CovariantPhaseSpace)_).




##### Transgression of circle $n$-bundles with connection


* [[fiber integration in ordinary differential cohomology]]

##### Action functionals from transgression

(...)

#### Lie integration
 {#LieIntegration}

* [[Lie integration]]


### Semantic Layer
 {#IntegrationSemanticLayer}

#### Integration and higher holonomy

[[integration]]/[[higher holonomy]] is

$$
  \exp(2 \pi i \int_{\Sigma}(-))
  \colon
  [\Sigma_n, \mathbf{B}^n U(1)_{conn}]
  \to
  Conc \tau_0 [\Sigma, \mathbf{B}^n U(1)]
  \simeq
  U(1)
$$

#### Transgression

[[transgression]] is 

$$
  [\Sigma_k, \mathbf{B}^n U(1)_{conn}]
  \stackrel{\exp(2 \pi i \int_{\Sigma_k}) (-) }{\to}
  \mathbf{B}^{n-k} U(1)_{conn}
$$

#### Action functionals from Lagrangeans
 {#SemLayerActionFunctionalsFromLagrangeans}

and [[schreiber:infinity-Chern-Simons theory|higher Chern-Simons]] [[action functionals]] induced from

$$
  \mathbf{L} \colon \mathbf{B}G_{conn} \to \mathbf{B}^n U(1)_{conn}
$$

are

$$
  \exp\left(i S\left(-\right)\right)
  \coloneqq
  \exp(2 \pi \in \int_{\Sigma_k} [\Sigma_k, \mathbf{L}] )
  \colon
  [\Sigma_k, \mathbf{B}G]
  \stackrle{[\Sigma_k, \mathbf{L}]}{\to}
  [\Sigma_k, \mathbf{B}^n U(1)]
  \stackrel{\exp(2 \pi i\left(-\right))}{\to}
  \mathbf{B}^{n-k} U(1)_{conn}
$$


here $\mathbf{L}$ is the [[Lagrangean]].

### Syntactic Layer

(...)





## **Gauge theories**
 {#ActionFunctionalsForChernSimonsTypeGaugeTheories}



* [[cohesion]] 

* $\stackrel{differential\;refinement\;of\;universal\;char\;classes}{\Rightarrow}$ [[schreiber:infinity-Chern-Simons theory]]

  * [[closed bosonic string field theory|closed string field theory]]

    * via level-truncation and [[Kaluza-Klein mechanism]] $\Rightarrow$ 

      [[Einstein-Yang-Mills theory]]

      * [[standard model of particle physics]]

      * [[standard model of cosmology]]

    


### Model Layer

#### 3d Chern-Simons theory for compact simple gauge group

* [[Chern-Simons theory]]

#### Higher dimensional abelian Chern-Simons theory
 {#AbelianChernSimonsTheory}

* [[higher dimensional Chern-Simons theory]]

* [[cup-product in ordinary differential cohomology]]

$$
  \cup_{conn}
  :
  \mathbf{B}U(1)_{conn}
  \to 
  \mathbf{B}^3 U(1)_{conn}
$$

$$
  \exp(2 \pi i \int_{\Sigma}[\Sigma, \cup_\conn])
   : 
  [\Sigma, \mathbf{B}U(1)_{conn}]
   \stackrel{[\Sigma, \cup_{conn}]}{\to}
  [\Sigma, \mathbf{B}^3 U(1)_{conn}]
   \stackrel{\exp(2 \pi i \int_\Sigma (-))}{\to}
  U(1)
$$

#### Self-dual higher gauge theory

* [[self-dual higher gauge theory]]


#### Closed string field theory

* [[closed string field theory]]

##### Einstein gravity

* [[gravity]]

##### Kaluza-Klein mechanism

* [[Kaluza-Klein mechanism]]

##### Einstein-Yang-Mills theory

* [[Einstein-Yang-Mills theory]]

###### Yang-Mills theory
 {#Yang-MillsTheory}

* [[Yang-Mills theory]]

* [[Yang-Mills instanton]] number = [[second Chern class]]

###### Einstein gravity

* [[gravity]]

###### Phenomenological Standard model of particle physics and cosmology

* [[model (in theoretical physics)]]

* [[standard model of particle physics]]

* [[standard model of cosmology]]


### Semantic Layer

(...)

### Syntactic Layer

(...)




## **Geometric quantization**
 {#GeometricQuantization}

### Model Layer

#### 1-Geometric quantization

* [[geometric quantization]]

#### Quantum 3d Chern-Simons theory for compact simple gauge group

* [[Reshetikhin-Turaev construction]], [[Turaev-Viro construction]]

* [[conformal blocks]]

#### Higher geometric quantization

* [[higher geometric quantization]]


### Semantics Layer

* [[n-plectic smooth infinity-groupoid]]


### Syntactic Layer

(...)


## **Super-geometry**
 {#SupergeometricCoordinateSystems}

### Model Layer

The premise in [The continuum real world line](#TheContinuumRealWorldLine) is now refined to

**Premise.** The abstract worldline of a [[fermionic particle]] is a $\mathbb{Z}_2$-[[odd line|graded]] [[formal manifold|formal neighbourhood]] $\mathbb{R}^{1|n}$ of the [[real line]], for some $n \in \mathbb{N}$.

For $n = 0$ this is again the real line $\mathbb{R}^{1|0} = \mathbb{R}$.


* [[supermanifold]]

#### Fermion

* [[fermion]]


### Semantic Layer

#### Super cohesion

* [[super infinity-groupoid]]

* [[smooth super infinity-groupoid]]

### Syntactic Layer

(...)

## **Quantum mechanics**
 {#QuantumMechanics}

### Model Layer

#### Worldvolumes and cobordisms

* [[cobordism]], [[FQFT]]

#### Spectral triple

* [[spectral triple]]

### Semantic Layer

#### Internal categories in an $\infty$-topos

##### Simplicial objects in an $\infty$-topos

* [[simplicial object in an (∞,1)-category]]

##### Category objects in an $\infty$-topos

* [[Segal condition]]

* [[internal category in an (∞,1)-category]] 

### Syntactic Layer

#### Directed homotopy type theory

* [[directed homotopy type theory]]


## **References**

### General

A textbook with basic introductions to [[differential geometry]] and [[physics]] is

* [[Theodore Frankel]], _[[The Geometry of Physics - An Introduction]]_
 {#Frankel}

A discussion with emphasis on the kind of tools that we are using here is in 

* [[Frédéric Paugam]], _Towards the mathematics of quantum field theory_ ([pdf](http://people.math.jussieu.fr/~fpaugam/documents/enseignement/master-mathematical-physics.pdf))

An introductory discussion with much overlap with the above discussion is in section "1.3 Introduction -- Models and applications" of

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_
 {#SchreiberCohesiveInfinityTopos}

Another introductory discussion along the above lines of aspects in [[gravity]] and [[higher gauge theory]] motivated from [[string theory]] is in 

* [[Urs Schreiber]], _[[twisted smooth cohomology in string theory]]_, ESI (2012)

### Differential forms and parallel transport

The relation between differential 1-forms and smooth incremental path measures as used above is discussed in 

* [[Urs Schreiber]], [[Konrad Waldorf]], _Parallel transport and functors_, J. Homotopy Relat. Struct. 4, 187-244 ([arXiv:0705.0452](http://arxiv.org/abs/0705.0452))
 {#SchreiberWaldorf}

For a commented list of related literature see [here](http://ncatlab.org/schreiber/show/differential+cohomology+in+a+cohesive+topos+--+references#HistConnAsParTrans).

### Mathematical quantum field theory

A textbook (really a collection of lecture notes) on [[quantum field theory]] and [[string theory]] that tries to present material as conceptually precise as possible is

* [[Pierre Deligne]], [[Pavel Etingof]], [[Dan Freed]], L. Jeffrey, 
[[David Kazhdan]], [[John Morgan]], D.R. Morrison and [[Edward Witten]], eds.   _[[Quantum Fields and Strings, A course for mathematicians]]_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))

A collection trying to summarize the state of the art of the formalization of [[QFT]] by [[FQFT]] and [[AQFT]] is 

* [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_, Proceedings of Symposia in Pure Mathematics, volume 83 AMS (2011)
 {#SatiSchreiber}

### Topos theory in differential geometry and physics

One of the central figures of [[topos theory]] and [[categorical logic]], [[William Lawvere]], has motivated his interest in these subject always with intended application to the formalization of [[physics]] (of [[classical mechanics|classical]] [[continuum mechanics]] in his case). See for instance

* [[William Lawvere]], _Comments on the Development of Topos Theory_, Development of Mathematics 1950-2000, 715-734 (2000) Birkh&#228;user Basel
 {#Lawvere2000}

For more pointers see also at _[[higher category theory and physics]]_.

### Further

(...)


