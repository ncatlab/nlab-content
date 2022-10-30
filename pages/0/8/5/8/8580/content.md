
{:bluebox: .un_remark style="border:solid #000000;background: #E6DF13;border-width:2px 1px;padding:0 1em;margin:0 1em;"}



> This page is growing incrementally as a series of lecture series proceeds.

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

A set of lecture notes on [[differential geometry]] and theoretical fundamental [[physics]], combining an introduction to traditional notions with an exposition of their formulation and refinement by [[higher geometry]] and [[extended prequantum field theory]]. With an eye towards [[Hilbert's sixth problem]] ("[[schreiber:Synthetic Quantum Field Theory]]").

Divided into two parts:

* **Part I) [Geometry](#GEOMETRY)**

* **Part II) [Physics](#PHYSICS)**

***


+-- {: bluebox}
###### Table ######
**of chapters**

* [About this text](#AboutThisPage)

* [References](#References)

**Part I) [Geometry](#GEOMETRY)**

1. [Coordinate systems](#CoordinateSystems)

1. [Smooth spaces](#SmoothSpaces)

1. [Differential forms](#DifferentialForms)

1. [Differentiation](#Differentiation)

1. [Smooth homotopy types](#SmoothnGroupoids)

1. [Groups](#NGroups)

1. [Principal bundles](#PrincipalBundles)

1. [Structure sheaves](#StructureSheaves)

1. [Manifolds and Orbifolds](#Orbifolds)

1. [Reduction of structure groups](#ReductionOfStructureGroups)

1. [Representations and Associated bundles](#AssociatedNBundle)

1. [Modules](#Modules)

1. [Flat connections](#FlatConnections)

1. [de Rham coefficients](#deRhamCoefficients)

1. [Maurer-Cartan forms](#MaurerCartanForms)

1. [Principal connections](#PrincipalConnections)

1. [Characteristic classes](#CharacteristicClasses)

1. [Integration](#Integration)

1. [Super-geometry](#SupergeometricCoordinateSystems)

**Part II) [Physics](#PHYSICS)**

1. [Physics in Higher Geometry: Motivation and Survey](#PhysicsMotivationAndSurvey)

1. [Fields](#Fields)

1. [Lagrangians and Action functionals](#LagrangiansAndActionFunctionals)

1. [Equations of motion](#EquationsOfMotion)

1. [Classical mechanics via prequantized Lagrangian correspondences](#ClassicalMechanicsByPrequantizedLagrangianCorrespondences)

1. [Local (topological) prequantum field theory](#LocalTopologicalPrequantumFieldTheory)

1. [Prequantum Gauge theory and Gravity](#ActionFunctionalsForChernSimonsTypeGaugeTheories)

1. [Quantum mechanics](#QuantumMechanics)

1. [Geometric quantization](#GeometricQuantization)

=--



#Contents#
* table of contents
{:toc}


## About this text
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

We give an overview in the spirit of _[Synthetic Quantum Field Theory](#SyntheticQuantumFieldTheory)_.

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

> Let there be [[light]].

| ordinary language | [[syntax]] | [[semantics]] | [[model]] | chapter |
|--|--|--|--|--|
|  | [[general abstract]] | [[general concrete]] | [[concrete particular]] | |
| There is the collection of higher $U(1)$-principal connections. | $n\colon \mathbb{N} \; \vdash \; \mathbf{B}^n U(1)_{conn} \colon Type$ | The [[coefficients]] for [[ordinary differential cohomology]] (with coefficients in an [[Eilenberg-MacLane object]].) |  The  [[smooth infinity-groupoid|smooth higher moduli stack]] of smooth [[circle n-bundles with connection]]. | _[Circle-principal n-connections](#CirclePrincipalNConnections)_. | 
| There is light. | $ \vdash \; \nabla_{em} \colon [X,\mathbf{B}U(1)_{conn}]$ |  A [[cocycle]] in [[ordinary differential cohomology]] in degree-2. | A configuration of the [[electromagnetic field]] on [[spacetime]] $X$. | _[Circle principal connection](#CirclePrincipalConnections)_ |


$\,$

There are of many more constructions in fundamental ([[quantum theory|quantum]]) [[physics]] that are naturally expressible in [[cohesive homotopy type theory]], but the above should already give an idea and highlight the cornerstones of the following discussion. 

$\,$

We now end this introduction and overview and turn to the in-depth account of _geometry of physics_.


+-- {: bluebox #GEOMETRY}
###### Contents

**I) Geometry**

We begin by laying the foundations of [[differential geometry]]. Doing this in th natural abstract way seamlessly leads over to the foundations of [[higher differential geometry]] (see also _[[motivation for higher differential geometry]]_). Once this is set up, we discuss the fundamental constructions: [[groups]], [[actions]]/[[representations]], [[fiber bundles]], [[connection on a bundle|connections]], [[Chern-Weil theory]].



1. [Coordinate systems](#CoordinateSystems)

1. [Smooth spaces](#SmoothSpaces)

1. [Differential forms](#DifferentialForms)

1. [Differentiation](#Differentiation)

1. [Smooth homotopy types](#SmoothnGroupoids)

1. [Groups](#NGroups)

1. [Principal bundles](#PrincipalBundles)

1. [Manifolds and Orbifolds](#Orbifolds)

1. [Reduction of structure groups](#ReductionOfStructureGroups)

1. [Representations and Associated bundles](#AssociatedNBundle)

1. [Flat connections](#FlatConnections)

1. [de Rham coefficients](#deRhamCoefficients)

1. [Maurer-Cartan forms](#MaurerCartanForms)

1. [Principal connections](#PrincipalConnections)

1. [Characteristic classes](#CharacteristicClasses)

1. [Integration](#Integration)


1. [Super-geometry](#SupergeometricCoordinateSystems)

=--


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

This is the motivation for studying models of physics in geometry modeled on the [[continuum]] [[real line]]. On the other hand, in all of what follows our discussion is set up such as to be _maximally independent_ of this specific choice (this is what _[[topos theory]]_ accomplishes for us, discussed below _[Smooth spaces -- Semantic Layer](#SmoothSpacesLayerSem)_). If we do desire to consider another choice of archetypical spaces for the geometry of physics we can simply "change the [[site]]", as discussed [below](#SmoothSpacesLayerSem) and many of the constructions, propositions and theorems in the following will continue to hold. This is notably what we do below in _[Supergeometric coordinate systems](#SupergeometricCoordinateSystems)_ when we generalize the present discussion to a flavor of differential geometry that also formalizes the notion of [[fermion]] [[particles]]: "differential [[supergeometry]]".


#### Cartesian spaces and smooth functions
 {#CartesianSpaces}



+-- {: .num_defn #SmoothFunctions}
###### Definition

A [[function]] of [[sets]] $f : \mathbb{R} \to \mathbb{R}$ is called 
a **[[smooth function]]** if, [[coinduction|coinductively]]:

1. the [[derivative]] $\frac{d f}{d x} : \mathbb{R} \to \mathbb{R}$ exists;

1. and is itself a smooth function.

We write $C^\infty(\mathbb{R}) \in Set$ for the [[set]] of all smooth functions on $\mathbb{R}$.

=--

+-- {: .num_remark}
###### Remark

The superscript "${}^\infty$" in "$C^\infty(\mathbb{R})$" refers to the order of the [[derivatives]] that exist for smooth functions. More generally for $k \in \mathbb{N}$ one writes $C^k(\mathbb{R})$ for the set of $k$-fold [[differentiable functions]] on $\mathbb{R}$. These will however not play much of a role for our discussion here. 

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

+-- {: bluebox }
###### 

This ends the "Model layer"-part of the discussion of coordinate systems. In the [Semantics layer below](#CoordinateSystemsLayerSem) we continue with a more sophisticated perspective on this topic. The reader wishing to stick to more elementary discussion for the moment should skip ahead to the next "Model layer"-discussion [of Smooth spaces below](#SmoothSpaces).

=--

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

For $n \in \mathbb{N}$, the [[smooth algebra]] $C^\infty(\mathbb{R}^n)$ 
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
       \vec e_j  
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
    f_{\mathbb{R}^n}(p_X) = g_{\mathbb{R}^n}(p_Y)
  \right\}
  \,.
$$

=--



#### Smooth mapping spaces and smooth moduli spaces
 {#SmoothMappingSpaces}


+-- {: .num_defn #SmoothFunctionSpace}
###### Definition

Let $\Sigma, X \in Smooth0Type$ be two [[smooth spaces]], def. \ref{SmoothSpace}. Then the **smooth [[mapping space]]** 

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

+-- {: .num_example #SmoothLoopSpace}
###### Example

If in the above example \ref{SmoothPathSpace} the path is
constraind to be a [[loop]] in $X$, one obtains the _[[smooth loop space]]_

$$
  \mathbf{L}X \coloneqq [S^1, X]
  \,.
$$

=--


#### The smooth moduli space of smooth functions
 {#SmoothModuliSpaceOfSmoothFunctions}


In example \ref{SmoothFunctionOnSmoothSpace} we saw that a smooth function on a general [[smooth space]] $X$ is a homomorphism of smooth spaces, def. \ref{HomomorphismOfSmoothSpaces}

$$
  f \colon X \to \mathbb{R}
  \,.
$$

The collection of these forms the [[hom-set]] $Hom_{Smooth0Type}(X, \mathbb{R})$. But by the discussion in _[Smooth mapping spaces](#SmoothMappingSpaces)_ such hom-sets are naturally refined to smooth spaces themselves.

+-- {: .num_defn #SmoothSpaceOfSmoothFunctions}
###### Definition

For $X \in Smooth0Type$ a [[smooth space]], we say that the **moduli space of smooth functions** on $X$ is the smooth mapping space (def. \ref{SmoothFunctionSpace}), from $X$ into the standard [[real line]] $\mathbb{R}$

$$
  [X, \mathbb{R}] \in Smooth0Type
  \,.
$$

We will also denote this by 

$$
  \mathbf{C}^\infty(X) \coloneqq [X, \mathbb{R}]
  \,,

$$ 

since in the special case that $X$ is a [[Cartesian space]] this is the smooth refinement of the set $C^\infty(X)$ of [[smooth functions]], def. \ref{SmoothFunctions}, on $X$.

=--

+-- {: .num_remark}
###### Remark

We call this a _[[moduli space]]_ because by prop. \ref{UniversalPropertyOfMappingSpace} above and in the sense of remark \ref{MappingSpaceAsModuliSpace} it is such that smooth functions into it _modulate_ smooth functions $X \to \mathbb{R}$.

By prop. \ref{UnderlyingSetOfSmoothMappingSpace} a point $* \to [X,\mathbb{R}^1]$ of the moduli space is equivalently a smooth function $X \to \mathbb{R}^1$.

=--



#### Outlook
 {#SmoothSpacesOutlook}


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


+-- {: bluebox }
###### 

This ends the Model-layer discussion of smooth spaces. We now pass to a more advanced discussion of this topic in the [Semantics layer below](#SmoothSpacesLayerSem). The reader wishing to stick to more elementary discussion for the time being should skip ahead to the Model-layer discussion of [Differential forms below](#DifferentialForms). 

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
 {#SharpModalityAndCodiscreteTypes}

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

For $\phi \colon \mathbb{R}^{\tilde k} \to \mathbb{R}^k$ a [[smooth function]], the **[[pullback of differential forms|pullback of differential 1-forms]]** along $\phi$ is the [[function]]

$$
  \phi^* \colon \Omega^1(\mathbb{R}^{k}) \to \Omega^1(\mathbb{R}^{\tilde k})
$$

between sets of differential 1-forms, def. \ref{Differential1FormsOnCartesianSpaces}, which is defined on [[basis]]-elements by

$$
  \phi^* \mathbf{d} x^i \coloneqq \sum_{j = 1}^{\tilde k} \frac{\partial \phi^i}{\partial \tilde x^j} \mathbf{d}\tilde x^j
$$

and then extended linearly by

$$
  \begin{aligned}
    \phi^* \omega & = \phi^* \left( \sum_{i} \omega_i \mathbf{d}x^i \right)
    \\
    & \coloneqq
     \sum_{i = 1}^k \left(\phi^* \omega\right)_i \sum_{j = 1}^{\tilde k} \frac{\partial \phi^i }{\partial \tilde x^j}  \mathbf{d} \tilde x^j 
    \\
    & = 
     \sum_{i = 1}^k  \sum_{j = 1}^{\tilde k} (\omega_i \circ \phi) \cdot \frac{\partial \phi^i }{\partial \tilde x^j}  \mathbf{d} \tilde x^j 
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
  \omega = \sum_{1 \leq i_1 \lt i_2 \lt \cdots \lt i_n \lt k} \omega_{i_1, \cdots, i_n} \mathbf{d}x^{i_1} \wedge \cdots \wedge \mathbf{d}x^{i_n}
  \,.
$$


=--

+-- {: .num_defn #PullbackOfDifferentialForms}
###### Definition

The [[pullback of differential forms|pullback of differential 1-forms]] of def. \ref{Differential1FormsOnCartesianSpaces} extends as an $C^\infty(\mathbb{R}^k)$-[[associative algebra|algebra]] [[homomorphism]] to $\Omega^n(-)$, given for a smooth function $f \colon \mathbb{R}^{\tilde k} \to \mathbb{R}^k$ on basis elements by

$$
  f^* \left(  \mathbf{d}x^{i_1} \wedge \cdots \wedge \mathbf{d}x^{i_n} \right)
  = 
  \left(f^* \mathbf{d}x^{i_1} \wedge \cdots \wedge f^* \mathbf{d}x^{i_n} \right)
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

$\Omega^0 \simeq \mathbb{R}$

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

This means that it sends an $n$-form $\omega \in \Omega^n(Y)$ which is modulated by a homomorphism $Y \to \Omega^n$ to the $n$-form $f^* \omega \in \Omega^n(X)$ which is modulated by the [[composition|composite]] $X \stackrel{f}{\to} Y \to \Omega^n$.

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

+-- {: bluebox }
###### 

This ends the Model-layer discussion of differential forms. We now pass to a more advanced discussion of this topic in the [Semantics layer below](#DifferentialFormsLayerSem). The reader wishing to stick to more elementary discussion for the time being should skip ahead to the Model-layer discussion of [differentiation below](#Differentiation). 

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

#### Smooth moduli space of differential forms on a smooth space
 {#SmoothModuliSpaceOfDifferentialForms}

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
  \,.
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

+-- {: .num_remark }
###### Remark

For $n = 0$ we have (for any $X\in Smooth0Type$)

$$
  \begin{aligned}
    \mathbf{\Omega}^0(X) 
      & \coloneqq Conc [X, \Omega^1]
    \\
    & \simeq Conc [X, \mathbb{R}]
    \\
    & \simeq [X, \mathbb{R}]
  \end{aligned}
  \,,
$$

by prop. \ref{SpaceOf0FormsIsRealLine}.

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
    \sum_{j = 1}^{\tilde k} \frac{\partial (f \circ \phi)}{\partial x^j}\mathbf{d} x^j
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

then the [[electromagnetic field strength]] is

$$
  F 
    \coloneqq
  \mathbf{d}A 
    = 
   E_1 \mathbf{d}x^1 \wedge \mathbf{d}t 
    + 
   E_2 \mathbf{d}x^2 \wedge \mathbf{d}t 
    + 
   E_3 \mathbf{d}x^3 \wedge \mathbf{d}t
    + 
    B_1 \mathbf{d}x^2 \wedge \mathbf{d}x^3 
    + 
    B_2 \mathbf{d}x^3 \wedge \mathbf{d}x^1 
    + 
    B_3 \mathbf{d}x^1 \wedge \mathbf{d}x^2 
$$

with 

$$
  E_i = \frac{\partial \phi}{\partial x^i} - \frac{\partial A_i}{\partial t}
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

This sends a plot $U \to \flat X$, which by definition of $Disc(-)$ is a point in $\Gamma X$, hence a homomorphism $x \colon * \to X$, to the plot $U \to * \stackrel{x}{\to} X$ of $X$.

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

Then for $U = \mathbb{R}$ and any smooth $U$-parameterized collection $\{\gamma_{u} \colon \Sigma \to X\}_{u \in U}$ the functional derivative takes the value

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
     \right) dt
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
     \right) dt
     \mathbf{d} u
     \\
     & =
     \int_{0}^1
     \left(
       \frac{\partial L}{\partial \gamma}(\gamma_u(t), \dot \gamma_u(t))
      - 
       \frac{\partial}{\partial t}\frac{\partial L}{\partial \dot \gamma}(\gamma_u(t), \dot \gamma_u(t))
     \right)
     \frac{\partial \gamma_u(t)}{\partial u} dt
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
def. \ref{DualNumbers}, for which $V = \mathbb{R}$. 

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

For $(E \to X) \in \mathbf{H}_{th}/X$, $Jet_X(E)$ is the **[[jet bundle]]** of $E$.


##### Formally &#233;tale / formally unramified / formally smooth

+-- {: .num_defn #FormallyEtaleMap}
###### Definition

A morphism $f \;\colon\; X \to Y$ in $\mathbf{H}$ is called a **[[formally étale morphism]]** if the naturality square of the $\mathbf{\Pi}_{inf}$-[[unit of a monad|unit]] 

$$
  \array{
    X &\stackrel{}{\to}& \mathbf{\Pi}_{inf}(X)
    \\
    \downarrow^{\mathrlap{f}} && \downarrow^{\athrlap{\mathbf{\Pi}_{inf}(f)}}
  }
    \\
    Y &\to& \mathbf{\Pi}_{inf}(Y)
$$

is an [[(∞,1)-pullback]]. 

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

* [[differential homotopy type theory]]

(...)

## **Smooth homotopy types**
 {#SmoothnGroupoids}
 {#SmoothGroupoids}

Fundamental physics is all based on the _[[gauge principle]]_. This says in particular that it is wrong to think of two different _[[gauge field]] configurations_ (discussed in detail below in _[Fields](#Fields)_) as being [[equality|equal]] or not. Instead it makes sense to ask if there is (or not) a _[[gauge transformation]]_ from one to the other that exibits an gauge [[equivalence]] between the two fields. The simplest example of this is described in detail below in  _[Gauge transformations in electromagnetism](#GaugeTransformationsInElectromagnetism)_.

But this means that the collection of [[gauge fields]] on a [[spacetime]] $X$, which we will write as a [[mapping space]] $[X, \mathbf{B}G_{conn}]$, cannot be a [[smooth space]] as considered above, for if it were such a smooth space, then we could ask if two gauge fields $\nabla_1, \nabla_2 \colon * \to [X,\mathbf{B}G_{conn}]$ were equal or not. 

Notice that this already applies to a single gauge field: given any $\nabla \colon * \to [X,\mathbf{B}G_{conn}]$ it is certainly equal to itself, but is nevertheless also _gauge equivalent_ to itself, but the latter it may be in several non-equivalent ways: there may be non-trivial auto-gauge transformations $\nabla \to \nabla$. Since these can be composed, are, by definition, invertible, and contain the trivial gauge transformaiton, these form a _[[group]]_, the group of auto-gauge equivalences of $\nabla$. (Groups are discussed in detail below in _[Groups](#Groups)_) If that gauge field $\nabla$ is itself the trivial gauge field, $\nabla = \nabla_0$, then this group of auto-gauge equivalences is the _[[gauge group]]_ of the given [[gauge theory]]:

$$
  G \simeq Aut(\nabla_0) \simeq \{\nabla_0 \stackrel{\simeq}{\to} \nabla_0\}
  \,.
$$

For this reason, the collection of _all_ gauge fields and all gauge transformations between them form something that is a [[group]] over ever fixed element, but which generalizes the notion of a group in that there are not only auto-equivalences, but also equivalences going from one element to another. Such a structure is called a _[[groupoid]]_. Gauge fields form not a [[set]] with smooth structure, a [[smooth space]], but a [[groupoid]] with smooth structure: a _[[smooth groupoid]]_. 

At least ordinary gauge fields do. More generally, the gauge princple goes further: it is in general also a mistake to assume that given two gauge transformations $\lambda_1, \lambda_2 \colon \nabla_1 \to \nabla_2$ between two gauge fields, it makes good sense to ask whether they are equal or not. Again, the gauge prinicle says that we should instead ask if there is a _[[gauge-of-gauge transformation]]_ between them, that exhibits a gauge [[equivalence]] $\rho \colon \lambda_1 \simeq \lambda_2$. If these gauge-of-gauge equivalences are nontrivial it would seem that gauge fields form a generalization of the notion of a [[groupoid]] called a _[[2-groupoid]]_. But in general the gauge principle goes on: we can in general never decide if two $n$-fold gauge-of-gauge transformations are actually equal, all we have is, possibly, an $(n+1)$-fold gauge transformation going between them which exhibits their gauge equivalence, this being so for all $0 \lt n \lt \infty$. One therefore says that gauge fields in general form an _[[∞-groupoid]]_ whose _[[n-morphisms]]_ are $n$-fold [[gauge-of-gauge transformations]]. These $\infty$-groupoids are also called _[[homotopy types]]_. And since at the same time there is still a notion of gauge fields varying smoothly, these are _[[smooth ∞-groupoids]]_ or _[[smooth homotopy types]]_. This is what we discuss here. 

Remarkably, the same concept appears in [[constructive mathematics]]: there it is in general wrong to consider an [[equality]] between two [[terms]] $\nabla_1, \nabla_2 \colon [X, \mathbf{B}G_{conn}]$, instead one is to consider an explicit [[proof]] that they are equal, provide an explicit [[equivalence]] between them. Such a proof $\lambda$ is itself a [[term]], of [[identity type]], written just as before, $\lambda \colon (\nabla_1 \simeq \nabla_2)$. And, in turn, the same applies to these proofs of equivalence themselves: in [[constructive mathematics]] one demands a [[proof]] $\rho$ that two equivalences $\lambda_1, \lambda_2 \colon (\nabla_1 \simeq \nabla_2)$ are equivalent, and hence a term $\rho \colon (\lambda_1 \simeq \lambda_2)$ of a higher [[identity type]]. If this goes ever on, and one speak of _[[intensional type theory]]_ or _[[homotopy type theory]]_.

This remarkable matching of [[higher gauge theory]] and [[homotopy type theory]] is what drives the discussion here.  

+-- {: bluebox }
###### Contents:

1. [Model layer](#SmoothHomotopyTypesModelLayer)

   This introduces _[[groupoids]]_, then _[[smooth groupoids]]_ and eventually _[[∞-groupoids]]_ modeled as _[[Kan complexes]]_ and then _[[smooth ∞-groupoids]]_.

1. [Semantics layer](#SmoothHomotopyTypesSemanticLayer)

   This introduces the general abstract framework for [[smooth ∞-groupoids]] which is _[[cohesion]]_ of [[(∞,1)-toposes]].

1. [Syntactic layer](#SmoothHomotopyTypesSyntacticLayer)

   This introduces the [[internal language]] of [[cohesive (∞,1)-toposes]], called _[[cohesive homotopy type theory]]_.

**Remark** _The reader who is after elementary exposition may want to skip over this discussion of [[homotopy theory]] on first reading to the next chapter _[Groups](#Groups)_ and only come back here for reference as need arises.

=--



### Model Layer
 {#SmoothHomotopyTypesModelLayer}

#### Groupoids
 {#Groupoids}


> For the content of this section currently see at _[Essence of gauge theory: Groupoids and basic homotopy 1-type theory](#GroupoidsAndBasicHomotopy1TypeTheory)_ below.


#### Gauge transformations in electromagnetism
 {#GaugeTransformationsInElectromagnetism}

The mathematical notion of _[[groupoid]]_ is well familiar, in slight disguise, in basic _[[gauge theory]]_. Here we make this explicit for basic [[electromagnetism]].

We have seen in _[The electromagnetic field strength](#ElectromagneticFieldStrength)_ that a configuration of the electromagnetic field on $\mathbb{R}^4$ is given by a [[differential 1-form]] $A \in \Omega^1(\mathbb{R}^4)$, the "[[electromagnetic potential]]". It describes a field configuration with [[field strength]] Lorentz tensor (with respect to the canonical [[coordinates]] $(t, x^1, x^2, x^3) \coloneqq (x^i)_{i = 1}^4 = $ on $\mathbb{R}^4$)

$$
  \begin{aligned}
    F & = \mathbf{d}A 
      \\
      & =
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

with electric [[field strength]] $(E_i \in C^\infty(\mathbb{R}^4))_{i = 1}^3$ and magnetic [[field strength]] $(B_i \in C^\infty(\mathbb{R}^4))_{i = 1}^3$ given  that is given by the [[de Rham differential]] of $A$:

$$
  \begin{aligned}
    F = \mathbf{d}A
  \end{aligned}
  \,.
$$

After Maxwell it was thought that $F \in \Omega^2(\mathbb{R}^4)$ alone genuinely reflects the configuration of the electromagnetic field. But with the discovery of [[quantum mechanics]] it became clear that it is indeed the potential $A$ itself that reflects the configuration of the electromagnetic field: in the presence of [[magnetic flux]] or other topoligical constraints, there can be different $A, A' $ with the _same_ $F = \mathbf{d}A = \mathbf{d}A'$ which nevertheless describe experimentally distinguishable electromagnetic field configurations. (Distinguishable by the [[Aharonov-Bohm effect]] and also to some extent by [[Dirac charge quantization]]; this is discussed at _[Circle-principal connections](#CirclePrincipalConnections)_ below.)

However, not all different gauge potentials describe different physics. The actual configuration space of electromagnetism on a [[spacetime]] $X$ is finer than $\mathbf{\Omega}^2_{cl}(X)$ but coarser than $\mathbf{\Omega}^1(X)$. And it is not quite a smooth space itself, but a _[[smooth groupoid]]_:

one finds that two electromagnetic potentials $A, A' \in \Omega^1(\mathbb{R}^4)$ for which there is a function $\lambda \in C^\infty(\mathbb{R}^4)$ such that 

$$
  A' = A + \mathbf{d}\lambda
$$

represent _different but [[equivalence|equivalent]]_ field configurations. One says that _$\lambda$ induces a [[gauge transformation]] from $A$ to $A'$_. We write $\lambda \colon A \stackrel{\simeq}{\to} A'$ to reflect this.

So the configuration space of electromagnetism does not just have points and coordinate systems. But it is also equipped with the information of a space of gauge transformations between any two coordinate systems laid out in it (which may be empty). 

To see what the structure of such a _smooth gauge groupoid_ should be, notice that the above defines an [[action]] of smooth functions $\lambda$ on smooth $1$-forms $A$, 


+-- {: .num_defn #ActionOfFunctionsOnForms}
###### Definition

For any $U \in $ [[CartSp]], Write $\Omega^1_{vert}(X \times U)$ for the set of [[differential 1-forms]] on $X \times U$ with no components along $U$, and write $C^\infty(X \times U , U(1))$ for the [[group]] of [[circle group]] valued [[smooth functions]]. There is an [[action]] of this group on the 1-forms 

$$
  \rho_U 
   \colon 
  \Omega^1_{vert}(X \times U) \times C^\infty(X \times U, U(1))
    \to
  \Omega^1_{vert}(X \times U)
$$

given by

$$
  \rho_U \colon (A,\lambda) \mapsto A + \mathbf{d}_X \lambda
  \,.
$$

=--

Given such an action of a [[discrete group]] on a [[set]], we might be demoted to form the [[quotient]] set $\Omega^1_{vert}(X\times U)/C^\infty(X \times U, U(1))$. This set contains the gauge [[equivalence classes]] of $U$-parameterized collections of electromagnetic gauge fields on $X$. But it turns out that this is too little information to correctly capture physics. For that instead we need to remember not just that two gauge fields are equivalent, but how they are equivalent. That is, we for $\lambda$ a gauge transformation from $A_1$ to $A_2$, we should have an [[equivalence]] $\lambda \colon A_1 \stackrel{\simeq}{\to} A_2$.

+-- {: .num_defn #EMGaugeGroupoidOverU}
###### Definition

The [[action groupoid]]

$$
  \Omega^1_{vert}(X\times U)\sslash C^\infty(X \times U, U(1))
  \coloneqq
  (
    \Omega^1_{vert}(X\times U) \times C^\infty(X \times U, U(1))
    \stackrel{\overset{t = \rho}{\to}}{\underset{s = p_1}{\to}}
    \Omega^1_{vert}(X\times U)
  )
$$

is the [[groupoid]] whose 

* [[objects]] are $U$-parameterized collections of gauge potentials $A \in \Omega^1_{vert}(X \times U)$;

* [[morphisms]] are pairs $(A,\lambda)$ with $A$ an object and $\lambda \in C^\infty(X \times U, U(1))$, with [[domain]] $A$ and [[codomain]] $A + \mathbf{d}_X \lambda$;

* [[composition]] is given by multiplication of the $\lambda$-labels in the group $C^\infty(X \times U, U(1))$.

=--

This is the discrete _gauge groupoid_ for $U$-parameterized collections of fields. It refines the _[[gauge group]]_, which is recoverd as its [[fundamental group]]:

+-- {: .num_prop }
###### Proposition

Let $A_0 \coloneqq 0 \in \Omega^1_{vert}(X \times U)$ be the trivial gauge field. Then its [[automorphism group]] in the gauge groupoid of def. \ref{EMGaugeGroupoidOverU} is the group of [[circle]]-group valued functions on $U$:

$$
  \pi_1(\Omega^1_{vert}(X\times U)\sslash C^\infty(X \times U, U(1)), A_0)
  =
  Aut(A_0)
  \simeq
  C^\infty(U,U(1))
  \,.
$$

=--

+-- {: .proof}
###### Proof

By definition, an automorphism of $A_0$ is given by a function 
$\lambda \in C^\infty(X \times U, U(1))$ such that $A_0 = A_0 + \mathbf{d}_X \lambda$. This is the case precisely if $\mathbf{d}_X \lambda = 0$, hence if $\lambda$ is contant along $X$. But a function on $X \times U$ which is constant along $X$ is canonically identified with a function on just $U$.

=--

All this data in in fact [[natural transformation|natural]] in $U$. Recall that $\Omega^1_{vert}(X \times U) = \mathbf{\Omega}^1(X)(U)$ is the set of $U$-charts of the smooth moduli space $\mathbf{\Omega}^1(X)$ of smooth 1-forms on $X$. Similarly $C^\infty(X \times U) = \mathbf{C}^\infty(X)(U)$.

+-- {: .num_prop }
###### Proposition

There is a homomorphism of [[smooth spaces]] (def. \ref{HomomorphismOfSmoothSpaces})

$$
  \rho \colon \mathbf{\Omega}^1(X)\times \mathbf{C}^\infty(X) \to \mathbf{\Omega}^1(X)
$$

from the product smooth space, def. \ref{ProductOfSmoothSpaces}, of the smooth moduli spaces of 1-forms and 0-forms on $X$, def. \ref{SmoothSpaceOfFormsOnSmoothSpace}, to that of smooth functions, def. \ref{SmoothSpaceOfSmoothFunctions}, whose component over $U \in $ [[CartSp]] is the action 

$$
  \rho_U \colon (A,\lambda) \mapsto  A + \mathbf{d}\lambda
$$

of def. \ref{ActionOfFunctionsOnForms}.

=--

We then also want to consider a _smooth action groupoid_.

+-- {: .num_defn }
###### Definition

Write 

$$
  \mathbf{\Omega}^1(X) \sslash \mathbf{C}^\infty(X, U(1))
  : 
  CartSp^{op}
  \to 
  Grpd
$$

for the [[contravariant functor]] from coordinate systems to the [[category]] of [[groupoids]], which assigns to $U \in CartSp$ the discrete action groupoid of $U$-collections of gauge fields of def. \ref{EMGaugeGroupoidOverU}.

$$
  U \mapsto \Omega^1_{vert}(X \times U)\sslash C^\infty(X\times U, U(1))
  \,.
$$

=--

Such a structure _[[presheaf]]_ of [[groupoids]] is a common joint generalization of the notion of [[discrete groupoids]] and [[smooth spaces]]. We call them _[[smooth groupoids]]_. This is what we turn to in _[Smooth groupoids](#SmoothGroupoids)_

#### Smooth groupoids
 {#SmoothGroupoids}


+-- {: .num_defn }
###### Definition

Write [[Grpd]]${}_1$ for the [[category]] of [[groupoids]] and [[functors]] between them. Write then

$$
  gPsh(CartSp) \coloneqq Funct(CartSp^{op}, Grpd)
$$

for the [[category]] of [[groupoid]]-valued [[presheaves]].

=--

+-- {: .num_defn }
###### Definition

For $n \in \mathbb{N}$, and $0 \lt r \lt 1 \in \mathbb{R}$ let 

$$
  \mathbb{R}^n \simeq D^n_r \hookrightarrow \mathbb{R}^n
$$

Be the smooth function that regards $\mathbb{R}^n$ as the standard $n$-[[disk]] of radius $r$ around the origin in $\mathbb{R}^n$.

For $X \in gPSh(CartSp)$ we write

$$
  (D^n)^* X \coloneqq {\lim_\to}_r X(D^n_r) \in Grpd
$$

for the [[stalk]] of $X$ at the origin of $\mathbb{R}^n$. This is a [[functor]]

$$
  (D^n)^* \colon gPSh(CartSp) \to Grpd
  \,.
$$

=--

+-- {: .num_defn }
###### Definition

A morphism $f \colon X \to Y$ in $gPSh(CartSp)$ we call a 
_local [[weak equivalence]]_ if for every $n \in \mathbb{N}$
the stalk 

$$
  (D^n)^* f \colon (D^n)^* X \to (D^n)^* Y
$$

is an [[equivalence of groupoids]].

=--

+-- {: .num_defn }
###### Definition

Write 

$$
  Smooth1Type 
   \coloneqq
  L_{lwe} gPSh(CartSp)
$$

for the [[(2,1)-category]] which is the [[simplicial localization]] of groupoid-valued presheaves at the local weak equivalences.

An [[object]] $X \in Smooth1Type$ we call a **[[smooth groupoid]]** or
**[[smooth homotopy type|smooth homotopy 1-type]]**.

=--


+-- {: .num_example }
###### Example

Every [[smooth space]] is canonically a [[smooth groupoid]] with only identity morphisms.

=--

+-- {: .num_prop }
###### Proposition

The canonical identification yields a [[full subcategory]]

$$
  Smooth0Type \hookrightarrow Smooth1Type
  \,.
$$

=--

+-- {: .num_example }
###### Example

For $X$ a [[smooth space]] and $G$ a [[smooth group]] and 

$$\rho : X \times G \to X
$$ 

an [[action]] then  the [[action groupoid]]
 
$$
  X \sslash G \in Smooth1Type

$$

$$
  X \sslash G = 
  \left(
    X \times G \stackrel{\overset{\rho}{\to}}{\underset{p_1}{\to}}
    X
  \right)
$$

is a [[smooth groupoid]].

=--

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

#### $\infty$-Groupoids and Kan complexes

An [[∞-groupoid]] is first of all supposed to be a structure that has [[k-morphism]]s for all $k \in \mathbb{N}$, which for $k \geq 1$ go between $(k-1)$-morphisms. A useful tool for organizing such collections of morphisms is the notion of a [[simplicial set]]. This is a [[functor]] on the [[opposite category]] of the  [[simplex category]] $\Delta$, whose objects are the abstract cellular $k$-[[simplex|simplices]], denoted $[k]$ or $\Delta[k]$ for all $k \in \mathbb{N}$, and whose morphisms $\Delta[k_1] \to \Delta[k_2]$ are all ways of mapping these into each other. So we think of such a simplicial set given by a functor

$$
  K : \Delta^{op} \to Set
$$

as specifying

* a set $[0] \mapsto K_0$ of [[object]]s;

* a set $[1] \mapsto K_1$ of [[morphism]];

* a set $[2] \mapsto K_2$ of [[2-morphism]];

* a set $[3] \mapsto K_3$ of [[3-morphism]];

and generally

* a set $[k] \mapsto K_k$ of [[k-morphism]]s

as well as specifying

* functions $([n] \hookrightarrow [n+1]) \mapsto (K_{n+1} \to K_n)$
  that send $n+1$-morphisms to their boundary $n$-morphisms;

* functions $([n+1] \to [n]) \mapsto (K_{n} \to K_{n+1})$
  that send $n$-morphisms to [[identity]] $(n+1)$-morphisms
  on them.

The fact that $K$ is supposed to be a [[functor]] enforces that these assignments of sets and functions satisfy conditions that make consistent our interpretation of them as sets of $k$-morphisms and source and target maps between these. 
These are called the [[simplicial identities]].

But apart from this source-target matching, a generic simplicial set does not yet encode a notion of [[composition]] of these morphisms. 

For instance for $\Lambda^1[2]$ the simplicial set consisting of two attached 1-cells 

$$
  \Lambda^1[2] = \left\{
    \array{
       && 1
       \\
       & \nearrow && \searrow
       \\
       0 &&&& 2
    }
  \right\}
$$

and for $(f,g) : \Lambda^1[2] \to K$ an image of this situation in $K$, hence a pair $x_0 \stackrel{f}{\to} x_1 \stackrel{g}{\to} x_2$ of two _composable_ 1-morphisms in $K$, we want to demand that there exists a third 1-morphisms in $K$ that may be thought of as the [[composition]] $x_0 \stackrel{h}{\to} x_2$ of $f$ and $g$. But since we are working in [[higher category theory]] (and not to be [[evil]]), we want to identify this composite only up to a [[2-morphism]] equivalence

$$
    \array{
       && x_1
       \\
       & {}^{\mathllap{f}}\nearrow &\Downarrow^{\mathrlap{\simeq}}& 
       \searrow^{\mathrlap{g}}
       \\
       x_0 &&\stackrel{h}{\to}&& x_2
    }
  \,.
$$

From the picture it is clear that this is equivalent to demanding that for $\Lambda^1[2] \hookrightarrow \Delta[2]$ the obvious inclusion of the two abstract composable 1-morphisms into the 2-simplex we have a diagram of morphisms of simplicial sets

$$
  \array{
    \Lambda^1[2] &\stackrel{(f,g)}{\to}& K
    \\
    \downarrow & \nearrow_{\mathrlap{\exists h}}
    \\
    \Delta[2]
  }
  \,.
$$

A simplicial set where for all such $(f,g)$ a corresponding such $h$ exists may be thought of as a collection of higher morphisms that is equipped with a notion of composition of adjacent 1-morphisms. 

For the purpose of describing [[groupoid]]al composition, we now want that this composition operation has all [[inverse]]s. For that purpose, notice that for 

$$
  \Lambda^2[2] = \left\{
    \array{
       && 1
       \\
       & && \searrow
       \\
       0 &&\to&& 2
    }
  \right\}
$$

the simplicial set consisting of two 1-morphisms that touch at their end, hence for 

$$
  (g,h) : \Lambda^2[2] \to K
$$

two such 1-morphisms in $K$, then if $g$ had an inverse $g^{-1}$ we could use the above composition operation to compose that with $h$ and thereby find a morphism $f$ connecting the sources of $h$ and $g$. This being the case is evidently equivalent to the existence of diagrams of morphisms of simplicial sets of the form

$$
  \array{
    \Lambda^2[2] &\stackrel{(g,h)}{\to}& K
    \\
    \downarrow & \nearrow_{\mathrlap{\exists f}}
    \\
    \Delta[2]
  }
  \,.
$$

Demanding that all such diagrams exist is therefore demanding that we have on 1-morphisms a composition operation with inverses in $K$. 

In order for this to qualify as an $\infty$-groupoid, this composition operation needs to satisfy an [[associativity law]] up to [[coherent]] [[2-morphism]]s, which means that we can find the relevant [[tetrahedra]]s in $K$. These in turn need to be connected by _pentagonators_ and ever so on.  It is a nontrivial but true and powerful fact, that all these [[coherence]] conditions are captured by generalizing the above conditions to all dimensions in the evident way:

let $\Lambda^i[n] \hookrightarrow \Delta[n]$ be the simplicial set -- called the $i$th $n$-[[horn]] -- that consists of all cells of the $n$-[[simplex]] $\Delta[n]$ except the interior $n$-morphism and the $i$th $(n-1)$-morphism.

Then a simplicial set is called a [[Kan complex]], if for all images $f : \Lambda^i[n] \to K$ of such horns in $K$, the missing two cells can be found in $K$- in that we can always find a _horn filler_ $\sigma$ in the diagram

$$
  \array{
     \Lambda^i[n] &\stackrel{f}{\to}& K
     \\
     \downarrow & \nearrow_{\mathrlap{\sigma}}
     \\
     \Delta[n]
  }
  \,.
$$

The basic example is the [[nerve]] $N(C) \in sSet$ of an ordinary [[groupoid]] $C$, which is the [[simplicial set]] with $N(C)_k$ being the set of sequences of $k$ composable morphisms in $C$. The nerve operation is a [[full and faithful functor]]  from 1-groupoids into Kan complexes and hence may be thought of as embedding 1-groupoids in the context of general [[∞-groupoid]]s.

#### Model categories

* [[model structure on simplicial sets]]

* [[model structure on simplicial presheaves]]

#### Cohesive $\infty$-Groupoids and locally Kan simplicial presheaves

But we need a bit more than just bare [[∞-groupoid]]s. In generalization to [[Lie groupoid]]s, we need [[∞-Lie groupoid]]s. A useful way to encode that an $\infty$-groupoid has extra structure modeled on geometric test objects that themselves form a category $C$ is to remember the rule which for each test space $U$ in $C$ produces the $\infty$-groupoid of $U$-parameterized families of $k$-morphisms in $K$.  For instance for an [[∞-Lie groupoid]] we could test with each [[Cartesian space]] $U = \mathbb{R}^n$ and find the $\infty$-groupoids $K(U)$ of smooth $n$-parameter families of $k$-morphisms in $K$.

This data of $U$-families arranges itself into a [[presheaf]] with values in Kan complexes

$$
  K : C^{op} \to KanCplx \hookrightarrow sSet
$$

hence with values in simplicial sets. This is equivalently a [[simplicial presheaf]] of sets. The [[functor category]] $[C^{op}, sSet]$ on the [[opposite category]] of the category of test objects $C$ serves as a model for the [[(∞,1)-category]] of $\infty$-groupoids with $C$-structure.

While there are no [[higher morphism]]s in this functor 1-category that could for instance witness that two $\infty$-groupoids are not [[isomorphic]], but still [[equivalence of categories|equivalent]], it turns out that all one needs in order to reconstruct _all_ these higher morphisms (up to equivalence!) is just the information of which morphisms of simplicial presheaves would become invertible if we were keeping track of higher morphism. These would-be invertible morphisms are called _weak equivalences_ and denoted $K_1 \stackrel{\simeq}{\to} K_2$. 

For common choices of $C$ there is a well-understood way to define the weak equivalences $W \subset mor [C^{op}, sSet]$, and equipped with this information the category of simplicial presheaves becomes a _[[category with weak equivalences]]_ . There is a well-developed but somewhat intricate theory of how exactly this 1-cagtegorical data models the full higher category of structured groupoids that we are after, but for our purposes we essentially only need to work inside the [[category of fibrant objects]] of a [[model category]] structure [[model structure on simplicial presheaves|on simplicial presheaves]], which in practice amounts to the fact that we use the following three basic constructions:

1. **[[∞-anafunctor]]s** -- A morphisms $X \to Y$ between $\infty$-groupoids with $C$-structure is not just a morphism $X\to Y$ in $[C^{op}, sSet]$, but is a [[span]] of such ordinary morphisms

   $$
     \array{  
        \hat X &\to& Y
        \\
        \downarrow^{\mathrlap{\simeq}}
        \\
        X
     }
   $$

   where the left leg is a weak equivalence. This is sometimes called an _$\infty$-anafunctor_ from $X$ to $Y$.
 
1. **[[homotopy pullback]]** -- For $A \to B \stackrel{p}{\leftarrow} C$ a [[diagram]], the [[(∞,1)-pullback]] of it is the ordinary [[pullback]] in $[C^{op}, sSet]$ of a replacement diagram $A \to B \stackrel{\hat p}{\leftarrow} \hat C$, where $\hat p$ is a _good replacement_  of $p$ in the sense of the following factorization lemma.

1. **[[factorization lemma]]** -- For $p : C \to B$ a morphism in $[C^{op}, sSet]$, a _good replacement_ $\hat p : \hat C \to B$ is given by the composite vertical morphism in the ordinary [[pullback]] diagram

   $$
     \array{
       \hat C &\to& C
       \\
       \downarrow && \downarrow^{\mathrlap{p}}
       \\
       B^{\Delta[1]} &\to& B
       \\
       \downarrow
       \\
       B
     }
     \,,
   $$

  where $B^{\Delta[1]}$ is the [[path object]] of $B$: 
  the simplicial presheaf that is over each $U \in C$ the
  simplicial path space $B(U)^{\Delta[1]}$.

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

* [[local (∞,1)-topos]] $(\flat \dashv \sharp)$

* [[locally ∞-connected (∞,1)-topos]] $(\mathbf{\Pi} \dashv \flat)$

* [[cohesive (∞,1)-topos]] $(\mathbf{\Pi} \dashv \flat \dashv \sharp)$

[[!include cohesion - table]]

Some terminology:

+-- {: .num_defn #ShapeTerminology}
###### Definition

For $X \in \mathbf{H}$ locally $\infty$-connected, we say $\mathbf{\Pi}(X)$ is the **[[shape]] of $X$**. If $\mathbf{H}$ is in addition cohesive we also say that $\mathbf{\Pi}(X)$ is the **[[geometric realization]]** of $X$ or the **[[fundamental ∞-groupoid]]** of $X$.

If $\mathbf{\Pi}(X) \simeq *$ we say that $X$ is **geometrically contractible**.

=--


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
 {#Groups}

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

+-- {: .num_defn #DKMap}
###### Definition

Write 

$$
  DK 
  \colon
  Ch_\bullet(Ab(Smooth0Type))
  \stackrel{\Xi}{\to}
  sAb(Smooth0Type)
  \to
  Smooth0Type^{\Delta^{op}}
  \to
  L_{whe} Smooth0Type^{\Delta^{op}}
  \simeq
  Smooth \infty Grpd
$$

for the functor that sends a [[chain complex]] of [[abelian group|abelian]] [[group objects]] in [[smooth spaces]] first to the [[simplicial abelian group]] in [[smooth spaces]] given by the [[Dold-Kan correspondence]], then [[forgetful functor|forgets]] the abelian group structure and finally regards the resulting [[simplicial object|simplicial]] smooth space as a [[smooth ∞-groupoid]] under [[simplicial localization]].

=--

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

#### Principal 1-Bundles

Let $G$ be a [[Lie group]] and $X$ a [[smooth manifold]] (all our smooth manifolds are assumed to be finite dimensional and [[paracompact space|paracompact]]). 

We give a discussion of smooth $G$-[[principal bundle]]s on $X$ in a manner that paves the way to a straightforward generalization to a description of [[principal ∞-bundle]]s.

From the group $G$ we canonically obtain a [[groupoid]] that we write $\mathbf{B}G$ and call the [[delooping]] groupoid of $G$. Formally this groupoid is

$$
  \mathbf{B}G = (G \stackrel{\to}{\to} *)
$$

with composition induced from the product in $G$. A useful cartoon of this groupoid is

$$
  \mathbf{B}G = 
  \left\{
    \array{
      && \bullet
      \\
      & {}^{\mathllap{g_1}}\nearrow 
      &=& 
      \searrow^{\mathrlap{g_2}}
      \\
      \bullet &&\stackrel{g_2 \cdot g_1 }{\to}&& \bullet
    }
  \right\}
$$

where the $g_i \in G$ are elements in the group, and the bottom morphism is labeled by forming the product in the group. (The order of the factors here is a convention whose choice, once and for all, does not matter up to equivalence.)

But we get a bit more, even. Since $G$ is a [[Lie group]], there is smooth structure on $\mathbf{B}G$  that makes it a [[Lie groupoid]], an [[internal groupoid]] in the [[category]] [[Diff]] of [[smooth manifold]]s: its collections of objects (trivially) and of morphisms each form a smooth manifold, and all structure maps (source, target, identity, composition) are [[smooth function]]s. We shall write

$$
  \mathbf{B}G \in LieGrpd
$$

for $\mathbf{B}G$ regarded as equipped with this smooth structure. Here and in the following the boldface is to indicate that we have an object equipped with a bit more structure -- here: smooth structure -- than present on the object denoted by the same symbols, but without the boldface. Eventually we will make this precise by having the boldface symbols denote objects in the [[(∞,1)-topos]] [[Smooth∞Grpd]] which are taken by [[forgetful functor]]s to objects in [[∞Grpd]] denoted by the corresponding non-boldface symbols.[^TwoForgetful]

[^TwoForgetful]: There are actually two such forgetful functors, $\Gamma$ and $\Pi$. The first sends $\mathbf{B}G$ to $B G_{disc}$, which in [[topology]] is known as $K(G,1)$. The other sends $\mathbf{B}G$ to the [[classifying space]] $B G$. (see <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#GeometricRealization">∞-Lie groupoid -- geometric realization</a>). This distinction is effectively the origin of differential cohomology.

Also the smooth manifold $X$ may be regarded as a [[Lie groupoid]] -- a groupoid with only identity morphisms. Its cartoon description is simply

$$
  X = \{x \stackrel{id}{\to} x \}
  \,.
$$

But there are other groupoids associated with $X$:

Let $\{U_i \to X\}_{i \in I}$ be an [[open cover]] of $X$. To this is canonically associated the [[Cech groupoid]] $C(\{U_i\})$. Formally we may write this groupoid as

$$
  C(\{U_i\})
  =
  \left(
    \coprod_{i,j} U_i \cap U_j
    \stackrel{\overset{p_1}{\to}}{\underset{p_2}{\to}}
    \coprod_i U_i
  \right)
  \,.
$$

A useful cartoon description of this groupoid is

$$
  C(\{U_i\})
  = 
  \left\{
    \array{
       && (x,j)
       \\
       & \nearrow &=& \searrow
       \\
      (x,i) &&\to&& (x,k)
    }
  \right\}
  \,.
$$

This indicates that the objects of this groupoid are pairs $(x,i)$ consisting of a point $x \in X$ and a patch $U_i \subset X$ that contains $x$, and a morphism is a triple $(x,i,j)$ consisting of a point and _two_ patches, that both contain the point, in that $x \in U_i \cap U_j$. The triangle in the above cartoon symbolizes the evident way in which these morphisms compose. All this inherits a smooth structure from the fact that the $U_i$ are smooth manifolds and the inclusions $U_i \to X$ are [[smooth function]]s. 
hence also $C(U)$ becomes a [[Lie groupoid]].

There is a canonical [[functor]]

$$
  C(\{U_i\}) \to X \;\; :\;\; (x,i) \mapsto x
  \,.
$$

This functor is an [[internal functor]] in [[Diff]] and moreover it is evidently [[essentially surjective functor|essentially surjective]] and [[full and faithful functor|full and faithful]]. 

However, while 
essential surjectivity and full-and-faithfulness implies that the underlying bare functor has a homotopy-inverse, that homotopy-inverse never 
has itself smooth component maps, unless $X$ itself is a Cartesian space and the chosen cover is trivial.

We do however want to think of $C(\{U_i\})$ as being equivalent to $X$ even as a Lie groupoid. 
One says that a smooth functor whose underlying bare functor is an equivalence of groupoids is
a _weak equivalence_ of Lie groupoids, which we write as 
$C(\{U_i\}) \stackrel{\simeq}{\to} X$.
Moreover, we shall think of $C(U)$ as a _good_ equivalent replacement of $X$ if it comes from a cover that is in fact a [[good open cover]] in that all its non-empty finite intersections $U_{i_0 \cdots i_k} := U_{i_0} \cap \cdots \cap U_{i_k}$ are [[diffeomorphic]] to the [[Cartesian space]] $\mathbb{R}^{dim X}$. 

We shall discuss later in which precise sense this condition makes $C(U)$ _good_ in the sense that smooth functors out of $C(U)$ model the correct notion of morphism out of $X$ in the context of smooth groupoids (namely it will mean that $C(U)$ is cofibrant in a suitable [[model category]] structure on the category of Lie groupoids). The formalization of this statement is what [[(∞,1)-topos]] theory is all about, to which we will come. For the moment we shall be content with accepting this as an ad hoc statement.

Observe that a [[functor]]

$$
  g : C(U) \to \mathbf{B}G
$$

is given in components precisely by a collection of functions

$$
  \{g_{i j} : U_{i j} \to G \}_{i,j \in I}
$$

such that on each $U_i \cap U_k \cap U_j$ the equality $g_{j k} g_{i j}  = g_{i k}$ of [[smooth function]]s holds:

$$
  \left(
    \array{
       && (x,j)
       \\
       & \nearrow && \searrow
       \\
      (x,i) &&\to&& (x,k)
    }
  \right)
  \mapsto
  \left(
    \array{
       && \bullet
       \\
       & {}^{\mathllap{g_{i j}(x)}}\nearrow
       && \searrow^{\mathrlap{g_{j k}(x)}}
       \\
      \bullet &&\stackrel{g_{i k}(x)}{\to}&& \bullet
    }
  \right)
  \,.
$$

It is well known that such collections of functions characterize $G$-[[principal bundle]]s on $X$. While this is a classical fact, we shall now describe a way to derive it that is true to the Lie-groupoid-context and that will make clear how smooth principal $\infty$-bundles work.

First observe that in total we have discussed so far [[span]]s of smooth functors of the form

$$
  \array{
     C(U) &\stackrel{g}{\to}& \mathbf{B}G
     \\
     \downarrow^{\mathrlap{\simeq}}
     \\
     X
  }
  \,.
$$

Such spans of functors, whose left leg is a weak equivalence, are sometimes known, essentially equivalently, as [[Morita morphism]]s or _generalized morphisms_ of Lie groupoids, as [[Hilsum-Skandalis morphism]]s or groupoid [[bibundle]]s, or as [[anafunctor]]s. We are to think of these as concrete _models_ for more intrinsically defined direct morphisms $X\to \mathbf{B}G$ in the $(\infty,1)$-topos of $\infty$-Lie groupoids. 

Now consider yet another Lie groupoid canonically associated with $G$: we shall write $\mathbf{E}G$ for the groupoid whose formal description is

$$
  \mathbf{E}G  = 
  \left(
    G \times G \stackrel{\overset{\cdot}{\to}}{\underset{p_1}{\to}} G 
  \right)
$$

with the evident composition operation. The cartoon description of this groupoid is

$$
  \mathbf{E}G
  = 
  \left\{
     \array{
        && g_2
        \\
        & {}^{\mathllap{g_2 g_1^{-1}}}\nearrow &=& \searrow^{\mathrlap{g_3 g_2^{-1}}}
        \\
        g_1 &&\stackrel{ g_3 g_1^{-1}}{\to}&& g_3
     }
  \right\}
  \,,
$$

This again inherits an evident smooth structure from the smooth structure of $G$ and hence becomes a Lie groupoid.

There is an evident [[forgetful functor]]

$$
  \mathbf{E}G \to \mathbf{B}G
$$

which sends

$$
  (g_1 \to g_2) \mapsto (\bullet \stackrel{g_2 g_1^{-1}}{\to} \bullet)
  \,.
$$

Consider then the [[pullback]] diagram

$$
  \array{
     \tilde P &\to& \mathbf{E}G
     \\
     \downarrow && \downarrow
     \\
     C(U) &\stackrel{g}{\to}& \mathbf{B}G
     \\
     \downarrow^{\mathrlap{\simeq}}
     \\
     X
  }
$$

in the category $Grpd(Diff)$.
The object $\tilde P$ is the Lie groupoid whose cartoon description is


$$
  \array{
    \tilde P = 
    \left\{
       \array{
          (x,i,g_1) &&\stackrel{}{\to}&& (x,j,g_2 = g_{i j}(x) g_1 )
       }
   \right\}
  }
  \,,
$$

where there is a unique morphism as indicated, whenever the group labels match as indicated. Due to this uniqueness, this Lie groupoid is weakly equivalent to one that comes just from a manifold $P$ (it is 0-[[truncated]])

$$
  \tilde P \stackrel{\simeq}{\to} P
  \,.
$$

This $P$ is traditionally written as

$$
  P = \left( \coprod_{i} U_i \times G \right)/{\sim}
  \,,
$$

where the [[equivalence relation]] is precisely that exhibited by the morphisms in $\tilde P$. This is the traditional way to construct a $G$-[[principal bundle]] from cocycle functions $\{g_{i j}\}$. We may think of $\tilde P$ as _being_ $P$. It is a particular _representative_ of $P$ in the $(\infty,1)$-topos of Lie groupoids.

While it is easy to see in components that the $P$ obtained this way does indeed have a principal $G$-[[action]] on it, for later generalizations it is crucial that we can also recover this in a general abstract way. For notice that there is a canonical [[action]]

$$
  (\mathbf{E}G) \times G \to \mathbf{E}G
$$
given by the action of $G$ on the space of objects, which are themselves identified with $G$.

Then consider the [[pasting]] diagram of pullbacks

$$
  \array{
     \tilde P \times G &\to& \mathbf{E}G \times G
     \\
     \downarrow && \downarrow
     \\
     \tilde P &\to& \mathbf{E}G
     \\
     \downarrow && \downarrow
     \\
     C(U) &\stackrel{g}{\to}& \mathbf{B}G
     \\
     \downarrow^{\mathrlap{\simeq}}
     \\
     X
  }
  \,.
$$

The morphism $\tilde P \times G \to \tilde P$ exhibits the principal $G$-[[action]] of $G$ on $\tilde P$.


In summary we find

+-- {: .num_prop}
###### Observation

For $\{U_i \to X\}$ a [[good open cover]], there is an [[equivalence of categories]]

$$
  SmoothFunc(C(\{U_i\}), \mathbf{B}G)
  \simeq
  G Bund(X)
$$

between the [[functor category]] of smooth functors and smooth natural transformations, and the groupoid of smooth $G$-[[principal bundle]]s on $X$. 

=--

It is no coincidence that this statement looks akin to the maybe more familiar statement which says that _equivalence classes_ of $G$-principal bundles are classified by [[homotopy]]-classes of morphisms of [[topological space]]s 

$$
  \pi_0 Top(X, \mathbf{B}G)
  \simeq
  \pi_0 G Bund(X)
  \,,
$$

where $\mathbf{B}G \in $ [[Top]] is the topological [[classifying space]] of $G$. The category [[Top]] of topological spaces, regarded as an [[(∞,1)-category]], is the archetypical [[(∞,1)-topos]] the way that [[Set]] is the archetypical [[topos]]. And it is equivalent to [[∞Grpd]], the $(\infty,1)$-category of bare [[∞-groupoid]]s. What we are seeing above is a first indication of how [[cohomology]] of bare $\infty$-groupoids is lifted to a richer $(\infty,1)$-topos to cohomology of $\infty$-groupoids with extra structure.

In fact, all of the statements that we have considered so far become conceptually _simpler_ in the $(\infty,1)$-topos. We had already remarked that the [[anafunctor]] span $X \stackrel{\simeq}{\leftarrow} C(U) \stackrel{g}{\to} \mathbf{B}G$ is really a model for what is simply a direct morphism $X \to \mathbf{B}G$ in the $(\infty,1)$-topos. But more is true: that pullback of $\mathbf{E}G$ which we considered is just a model for the [[homotopy pullback]] of just the _point_ 


$$
  \array{
     \vdots && \vdots
     \\
     \tilde P \times G &\to& \mathbf{E}G \times G
     \\
     \downarrow && \downarrow
     \\
     \tilde P &\to& \mathbf{E}G
     \\
     \downarrow && \downarrow
     \\
     C(U) &\stackrel{g}{\to}& \mathbf{B}G
     \\
     \downarrow^{\mathrlap{\simeq}}
     \\
     X
     \\
     {}
     \\
     {}
     \\
     & in\;the\;model\;category &
  }
  \;\;\;\;\;\;\;
  \;\;\;\;\;\;\;
  \;\;\;\;\;\;\;
  \array{
     \vdots && \vdots
     \\
     P \times G &\to& G
     \\
     \downarrow &\swArrow_{\simeq}& \downarrow
     \\
     P &\to& * 
     \\
     \downarrow &\swArrow_{\simeq}& \downarrow 
     \\
     X &\stackrel{}{\to}& \mathbf{B}G
     \\
     .
     \\
     .
     \\
     \\
     \\
     & in\;the\;(\infty,1)-topos
  }
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

The [[principal ∞-bundle]]s that we wish to model are already the main and simplest example of the application of these three items: 

Consider an object $\mathbf{B}G \in [C^{op}, sSet]$ which is an $\infty$-groupoid with a single object, so that we may think of it as the [[delooping]] of an [[∞-group]] $G$, let $*$ be the point and $* \to \mathbf{B}G$ the unique inclusion map. The _good replacement_ of this inclusion morphism is the $G$-[[universal principal ∞-bundle]] $\mathbf{E}G \to \mathbf{B}G$ given by the pullback diagram
  
$$
  \array{ 
    \mathbf{E}G &\to& *
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}G^{\Delta[1]} &\to& \mathbf{B}G
    \\
    \downarrow
    \\
     \mathbf{B}G
   }
$$

An [[∞-anafunctor]] $X \stackrel{\simeq}{\leftarrow} \hat X \to \mathbf{B}G$ we call a [[cocycle]] on $X$ with coefficients in $G$, and the [[(∞,1)-pullback]] $P$ of the point along this cocycle, which by the above discussion is the ordinary [[limit]]


$$
  \array{ 
    P &\to& \mathbf{E}G &\to& *
    \\
    \downarrow && \downarrow && \downarrow
    \\
    && \mathbf{B}G^I &\to& \mathbf{B}G
    \\
    \downarrow && \downarrow
    \\
    \hat X &\stackrel{g}{\to}& \mathbf{B}G
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
$$

we call the [[principal ∞-bundle]] $P \to X$ classified by the cocycle.

It is now evident that our discussion of ordinary smooth principal bundles [above](#PrincipalBundles) is the special case of this for $\mathbf{B}G$ the [[nerve]] of the one-object groupoid associated with the ordinary [[Lie group]] $G$.

So we find the complete generalization of the situation that we already indicated there, which is summarized in the following diagram:

$$
  \array{
     \vdots && \vdots
     \\
     \tilde P \times G &\to& \mathbf{E}G \times G
     \\
     \downarrow && \downarrow
     \\
     \tilde P &\to& \mathbf{E}G
     \\
     \downarrow && \downarrow
     \\
     C(U) &\stackrel{g}{\to}& \mathbf{B}G
     \\
     \downarrow^{\mathrlap{\simeq}}
     \\
     X
     \\
     {}
     \\
     {}
     \\
     & in\;the\;model\;category &
  }
  \;\;\;\;\;\;\;
  \;\;\;\;\;\;\;
  \;\;\;\;\;\;\;
  \array{
     \vdots && \vdots
     \\
     P \times G &\to& G
     \\
     \downarrow && \downarrow
     \\
     P &\to& * 
     \\
     \downarrow &\swArrow_{\simeq}& \downarrow 
     \\
     X &\stackrel{}{\to}& \mathbf{B}G
     \\
     .
     \\
     .
     \\
     \\
     \\
     & in\;the\;(\infty,1)-topos
  }
  \,.
$$


* [[simplicial principal bundle]]



### Semantic Layer

#### Principal $\infty$-bundles

* [[homotopy fiber]]

* [[homotopy colimit]]

* [[principal infinity-bundle]]

### Syntactic Layer

* [[connected type]]


## **Structure sheaves**
 {#StructureSheaves}


### Model layer

* [[structure sheaf]]

### Semantics layer
 {#StructureSheavesSemanticsLayer}

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]] $(\mathbf{\Pi} \dashv \flat \dashv \sharp)$ equipped with [[differential cohesion]] $(Red \dashv \mathbf{\Pi}_{inf} \dashv \flat_{inf})$.

+-- {: .num_defn #PetitTopos}
###### Definition

For $X \in \mathbf{H}$, write

$$
  Sh_{\mathbf{H}}(X)
  \hookrightarrow
  \mathbf{H}_{/X}
$$

for the [[full sub-(∞,1)-category]] of the [[slice (∞,1)-topos]] over $X$ on the formally &#233;tale maps into $X$, def. \ref{FormallyEtaleMap}.

We call this the **[[petit (∞,1)-topos]] of $X$**.

=--

+-- {: .num_prop #PetitToposIsTopos}
###### Proposition

The petit topos $Sh_{\mathbf{H}}(X)$ of def. \ref{PetitTopos} is indeed an [[(∞,1)-topos]]. Moreover the defining inclusion into the [[slice (∞,1)-topos]] is both [[reflective (∞,1)-category|reflective]] as well as coreflective.

=--

This is proven at _[differential cohesion -- structure sheaves](cohesive+%28infinity%2C1%29-topos+--+infinitesimal+cohesion#StructureSheaves)_. 

+-- {: .num_defn #StructureSheafInPetitTopos}
###### Definition

For $X \in \mathbf{H}$ write

$$
  \mathcal{O}_{(-)}
  \;\colon\;
  \mathbf{H}
  \stackrel{X^*}{\to}
  \mathbf{H}_{/X}
  \stackrel{R}{\to}
  Sh_{\mathbf{H}}(X)
$$

for the [[(∞,1)-functor]] which is the composite of the [[base change]] to $X$ followed by the _co_-reflection of prop. \ref{PetitToposIsTopos}. We call this the **structure sheaf** of $X$.

=--

+-- {: .num_remark }
###### Remark

For $X, A \in \mathbf{H}_{th}$ and for $U \to X$ a [[formally étale morphism]] in $\mathbf{H}_{th}$, we have that 

$$
  \mathcal{O}_{X}(A)(U) 
  \coloneqq
  \Sh_{\mathbf{H}}(X)( U , \mathcal{O}_{X} )
  \simeq
  \mathbf{H}(U,A)
  =
  A(U)
  \,.
$$

This means that $\mathcal{O}_{X}(A)$ behaves as the _sheaf of $A$-valued functions over $X$_. 

=--


### Syntax layer

(...)

## **Manifolds and Orbifolds**
 {#Orbifolds}

For $n \in \mathbb{N}$ a _[[manifold]]_ of [[dimension]] $n$ is an object $X$ that _locally looks_ like a [[Cartesian space]] $\mathbb{R}^n$, hence that can be thought of as being _glued together_ from Cartesian spaces by gluing these along [[diffeomorphisms]]. 

A natural way to make this precisely is to say that a [[manifold]] of dimension $X$ is an object such that first of all there is a [[cover]], hence a [[1-epimorphism]] of the form

$$
  p \;\colon\; \left(\coprod_{i \in i} \mathbb{R}^n\right) \to X
  \,.
$$

This encodes that $X$ can surjectively covered by Cartesian spaces, but it does not yet ensure that $X$ is _locally equivalent_ to a Cartesian space in the intended sense. That intended sense is that $p$ is a [[local diffeomorphism]].

Hence a manifold is a [[smooth space]] which receives a map out of a [[coproduct]] of [[Cartesian spaces]] that is a [[1-epimorphism]] and a [[local diffeomorphism]].

By the discussion above at _[Structure sheaves](#StructureSheaves)_ the general way to say _[[local diffeomorphism]]_ is to say _[[formally étale morphism]]_. Hence more generally we can consider the notion of a [[smooth groupoid]] which received a map out of a coproduct of Cartesian spaces that is a [[1-epimorphism]] and a [[formally étale morphism]]. If here the souce-fibers of the groupoid are in addition compact, then this is what is called an _[[orbifold]]_.

### Model Layer

1. [Smooth manifolds](Manifolds)

1. [Tangent bundle and frame bundle](#TangentBundle)

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
 {#TangentBundle}

We discuss how the [[tangent bundle]] of a [[manifold]] $X$ naturally arises in the above perspecive in terms of the map 
$\tau_X \;\colon\; X \to \mathbf{B}GL(n)$ that modulates it.

The above situation is neatly encoded in the existence of a [[diagram]] of Lie groupoids of the form

$$
  \array{
     C(\{U_i\}) &\stackrel{\tau_X}{\to}& \mathbf{B} GL(n).
     \\
     {}^{\mathllap{\simeq}}\downarrow
     \\
     X
  }
  \,,
$$

where

* the left morphism is [[stalk]]-wise (around small enough [[neighbourhoods]] of each point) an [[equivalence of groupoids]] (we make this more precise in a moment);

* the horizontal functor $\tau_X$ has as components the functions $\lambda_{i j}$ and its functoriality is the cocycle condition $\lambda_{i j} \cdot \lambda_{j k} = \lambda_{i k}$.


A [[natural transformation|transformation]] of smooth functors $\lambda_1 \Rightarrow \lambda_2 : C(\{U_i\}) \to \mathbf{B} GL(n)$ is precisely a [[coboundary]] between two such cocycles.

This defines a morphism of [[smooth groupoids]]

$$
  \tau_X \;\colon\; X \to \mathbf{B}GL(n)
  \,.
$$

The [[homotopy fiber]] of this map is a $GL(n)$-[[principal bundle]] called the [[frame bundle]] of $X$, while  the canonically [[associated bundle]] via the canonical [[representation]] of $GL(n)$ on $\mathbb{R}^n$ is the [[tangent bundle]]

$$
  T X \to X
  \,.
$$


### Semantics Layer


Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]] $(\mathbf{\Pi} \dashv \flat \dashv \sharp)$ equipped with [[differential cohesion]] $(Red \dashv \mathbf{\Pi}_{inf} \dashv \flat_{inf})$. Let 

$$
  \mathbb{A}^1 \in \mathbf{H}
$$ 

be an [[line object]] that exhibits the cohesive structure. 


+-- {: .num_defn #ManifoldInSemLayer}
###### Definition


An **[[étale ∞-groupoid]]** of [[dimension]] $n$ is an object $X \in \mathbf{H}$ such that there exists a map $p \;\colon\;\left(\coprod_{i} \mathbb{A}^n\right) \to X$ such that

1. $p$ is a [[1-epimorphism]];

1. $p$ is a [[formally étale morphism]], def. \ref{FormallyEtaleMap}

If $X$ here is [[0-truncated]] then we call it it **[[manifold]]**. It $X$ is [[1-truncated]] we call it an **[[orbifold]]**.


=--

+-- {: .num_defn #ManifoldWithBoundaryInSemLayer}
###### Definition

(...)


=--


### Syntax Layer 

(...)


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




### Semantics Layer

(...)


### Syntax Layer

(...)



## **Representations and Associated bundles**
 {#AssociatedNBundle}

### Model Layer

#### Actions

* [[action]]


#### Spin geometry
 {#SpinGeometry}

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


## **Modules**
 {#Modules}

 for the moment see the sub-entry _[[geometry of physics - modules]]_


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

This is discussed at _[smooth ∞-groupoid - structures - de Rham coefficients for BG with G a Lie group](smooth+infinity-groupoid+--+structures#deRhamWithCoefficientsInBOfLieGroup)_.

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

Let $\mathbf{H}$ be a [[cohesive (infinity,1)-topos]] $(\mathbf{\Pi} \dashv \flat \dashv \sharp)$. We discuss a general formulation of [[Maurer-Cartan forms]] on cohesive [[infinity-groups]]


Let $G \in Grp(\mathbf{H})$ be a [[group object in an (infinity,1)-category|group object]]. 

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
  \theta \;\colon\; G \to \flat_{dR} \mathbf{B}G
  \,.
$$

=--

+-- {: .num_defn #DifferentiationOfInfinityGroupValuedFunction}
###### Definition

For $S \;\colon\; X \to G$ a morphism, write

$$
  S^{-1} \mathbf{d} S 
  \coloneqq S^* \theta_G
  \;\colon\;
  X \stackrel{S}{\to}
  G
  \stackrel{\theta_G}{\to}
  \flat_{dR}\mathbf{B}G
$$

for its composite with the map of def. \ref{GeneralAbstractMaurerCartanForm}, hence the **pullback of the Maurer-Cartan form along $S$**. We also call this the **[[de Rham differential]]** of $S$.

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

There are different equivalent definitions of the classical notion of a connection. One that is useful for our purposes is that a connection $\nabla$ on a $G$-principal bundle $P \to X$ is a rule $tra_\nabla$ for [[parallel transport]] along paths: a rule that assigns to each path $\gamma : [0,1] \to X$ a morphism $tra_\nabla(\gamma) : P_x \to P_y$ between the fibers of the bundle above the endpoints of these paths, in a compatible way:


$$
  \array{
    P_x &\stackrel{tra_\nabla(\gamma)}{\to}& P_y
    &\stackrel{tra_\nabla(\gamma')}{\to}& P_z &&& P
    \\
    && && &&& \downarrow
    \\
    x &\stackrel{\gamma}{\to}& y &\stackrel{\gamma'}{\to}& z
    &&&
    X
  }    
  \,.
$$

In order to formalize this, we introduce a ([[diffeological space|diffeological]]) [[Lie groupoid]] to be called the [[path groupoid]] of $X$. (Constructions and results in this section are from (<a href="http://nlab.mathforge.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SWI">[SWI]</a>).

+-- {: .num_defn}
###### Definition

For $X$ a [[smooth manifold]] let $[I,X]$ be the set of [[smooth function]]s $I = [0,1] \to X$. For $U$ a [[Cartesian space]], we say that _a $U$-parameterized smooth family of points in $[I,X]$_ is a smooth map $U \times I \to X$. (This makes $[I,X]$ a [[diffeological space]]).

Say a path $\gamma \in [I,X]$ has _[[sitting instant]]s_ if it is constant in a neighbourhood of the boundary $\partial I$. Let $[I,P]_{si} \subset [I,P]$ be the subset of paths with sitting instants. 

Let $[I,X]_{si} \to [I,X]_{si}^{th}$ be the projection to the set of [[equivalence class]]es where two paths are regarded as equivalent if they are cobounded by a smooth [[thin homotopy]].

Say a $U$-parameterized smooth family of points in $[I,X]_{si}^{th}$ is one that comes from a $U$-family of representatives in $[I,X]_{si}$ under this projection. (This makes also $[I,X]_{si}^{th}$ a [[diffeological space]].)

=--


+-- {: .num_remark}
###### Remark

The passage to the subset and quotient $[I,X]_{si}^{th}$ of the set of all smooth paths in the above definition is essentially the minimal adjustment to enforce that the concatenation of smooth paths at their endpoints defines the composition operation in a groupoid.

=--


+-- {: .num_prop}
###### Definition

The **path groupoid** $\mathbf{P}_1(X)$ is the groupoid

$$
  \mathbf{P}_1(X) = ([I,X]_{si}^{th} \stackrel{\to}{\to} X)
$$

with source and target maps given by endpoint evaluation and composition given by concatenation of classes $[\gamma]$ of paths along any orientation preserving [[diffeomorphism]] $[0,1] \to [0,2] \simeq [0,1] \coprod_{1,0} [0,1]$ of any of their representatives

$$
  [\gamma_2] \circ [\gamma_1] : [0,1]
  \stackrel{\simeq}{\to} [0,1] \coprod_{1,0} [0,1]
  \stackrel{(\gamma_2 , \gamma_1)}{\to}
  X
  \,.
$$

This becomes an [[internal groupoid]] in [[diffeological spaces]] with the above $U$-families of smooth paths. We regard it as a [[groupoid-valued presheaf]], an object in $[CartSp^{op}, Grpd]$:

$$
  \mathbf{P}_1(X) : U \mapsto (Diff(U \times I, X)_{si}^{th} \stackrel{\to}{\to} Diff(U,X) )
  \,.
$$

=--

Observe now that for $G$ a [[Lie group]] and $\mathbf{B}G$ its [[delooping]] [[Lie groupoid]] discussed [above](#PrincipalBundles), a smooth functor $tra : \mathbf{P}_1(X) \to \mathbf{B}G$ sends each (thin-homotopy class of a) path to an element of the group $G$ 

$$
  tra : (x \stackrel{[\gamma]}{\to} y)
  \mapsto
  (
  \bullet
  \stackrel{tra(\gamma) \in G}{\to}
  \bullet
  )
$$

such that composite paths map to products of group elements 

$$
  tra : 
  \left(
    \array{
      && y
      \\
      & {}^{\mathllap{[\gamma]}}\nearrow &=& \searrow^{\mathrlap{[\gamma']}}
      \\
      x &&\stackrel{[\gamma']\circ [\gamma]}{\to}&& z
    }
  \right)
  \mapsto
  \left(
    \array{
      && \bullet
      \\
      & {}^{\mathllap{tra(\gamma)}}\nearrow 
      &=& 
      \searrow^{\mathrlap{tra(\gamma')}}
      \\
      \bullet &&\stackrel{tra(\gamma)tra(\gamma')}{\to}&& \bullet
    }
  \right)
$$

and such that $U$-families of smooth paths induce smooth maps $U \to G$ of elements. 

There is a classical construction that yields such an assignment: the [[parallel transport]] of a [[Lie-algebra valued 1-form]].

+-- {: .num_prop}
###### Definition

Suppose $A \in \Omega^1(X, \mathfrak{g})$ is a degree-1 [[differential form]] on $X$ with values in the [[Lie algebra]] $\mathfrak{g}$ of $G$. Then its parallel transport is the smooth functor

$$
   tra_A : \mathbf{P}_1(X) \to \mathbf{B}G
$$

given by

$$
  [\gamma] \mapsto P \exp(\int_{[0,1]} \gamma^* A) \; \in G
  \,,
$$

where the group element on the right is defined to be the value at 1 of the unique solution $f :  [0,1] \to G$ of the [[differential equation]]

$$
  d_{dR} f + \gamma^*A \wedge f = 0
$$

for the boundary condition $f(0) = e$.

=--

+-- {: .num_prop}
###### Theorem 

This construction $A \mapsto tra_A$ induces an [[equivalence of categories]]

$$
  [CartSp^{op},Grpd](\mathbf{P}_1(X), \mathbf{B}G)
  \simeq
  \mathbf{B}G_{conn}(X)
  \,,
$$

where on the left we have the [[hom-groupoid]] of [[groupoid-valued presheaves]] and  where on the right we have the [[groupoid of Lie-algebra valued 1-forms]] whose 

* objects are 1-forms $A \in \Omega^1(X,\mathfrak{g})$, 

* morphisms $g : A_1 \to A_2$ are labeled by [[smooth function]]s $g \in C^\infty(X,G)$ such that $A_2 = g^{-1} A g + g^{-1}d g$.

=--

This equivalence is [[natural transformation|natural]] in $X$, so that we obtain another smooth groupoid.

+-- {: .num_def}
###### Definition

Define $\mathbf{B}G_{conn} : CartSp^{op} \to Grpd$ to be the (generalized) Lie groupoid

$$
  \mathbf{B}G_{conn} : U \mapsto [CartSp^{op}, Grpd](\mathbf{P}_1(-), \mathbf{B}G)
$$

whose $U$-parameterized smooth families of groupoids form the [[groupoid of Lie-algebra valued 1-forms]] on $U$.

=--

+-- {: .num_remark}
###### Remark

This equivalence in particular subsumes the classical facts that parallel transport $\gamma \mapsto P \exp(\int_{[0,1]} \gamma^* A)$ 

* is invariant under orientation preserving reparameterizations of paths;

* sends reversed paths to inverses of group elements.

=--

+-- {: .num_lemma}
###### Observation

There is an evident natural smooth functor $X \to \mathbf{P}_1(X)$ that includes points in $X$ as constant paths. This induces a natural morphism $\mathbf{B}G_{conn} \to \mathbf{B}G$ that forgets the 1-forms.

=--


+-- {: .num_def}
###### Defintion

Let $P \to X$ be a $G$-[[principal bundle]] that corresponds to a cocycle $g : C(U) \to \mathbf{B}G$ under the construction discussed [above](#PrincipalBundles).  Then a **[[connection on a bundle|connection]]** $\nabla$ on $P$ is  a lift $\nabla$ of the cocycle through $\mathbf{B}G_{conn} \to \mathbf{B}G$.

$$
  \array{
     && \mathbf{B}G_{conn}
     \\
     & {}^{\mathllap{\nabla}}\nearrow & \downarrow
     \\
     C(U) &\stackrel{g}{\to}& \mathbf{B}G
  }
  \,.
$$

=--

+-- {: .num_lemma}
###### Observation

This is equivalent to the [[connection on a bundle|traditional definitions]].

=--

A morphism $\nabla : C(U) \to \mathbf{B}G_{conn}$ is

* on each $U_i$ a 1-form $A_i \in \Omega^1(U_i, \mathfrak{g})$;

* on each $U_i \cap U_j$ a function $g_{i j} \in C^\infty(U_i \cap U_j , G)$;

such that

* on each $U_i \cap U_j$ we have $A_j = g_{i j}^{-1}( A + d_{dR} )g_{i j}$;

* on each $U_i \cap U_j \cap U_k$ we have $g_{i j} \cdot g_{j k} = g_{i k}$.


+-- {: .num_prop}
###### Definition

Let $[I,X]_{si}^{th} \to [I,X]^h$ the projection onto the full quotient by smooth [[homotopy]] classes of paths.

Write $\mathbf{\Pi}_1(X) = ([I,X]^h \stackrel{\to}{\to} X)$ for the smooth groupoid defined as $\mathbf{P}_1(X)$, but where instead of thin homotopies, all homotopies are divided out.

=--


+-- {: .num_prop}
###### Proposition

The above restricts to a natural equivalence

$$
  [CartSp^{op}, Grpd](\mathbf{\Pi}_1(X), \mathbf{B}G)
  \simeq
  \mathbf{\flat}\mathbf{B}G
  \,,
$$

where on the left we have the [[hom-groupoid]] of groupoid-valued presheaves, and on the right we have the [[full subcategory|full sub-groupoid]] $\mathbf{\flat}\mathbf{B}G \subset \mathbf{B}G_{conn}$ on those $\mathfrak{g}$-valued differential forms whose [[curvature]] 2-form $F_A = d_{dR} A + [A \wedge A]$ vanishes.

A connection $\nabla$ is _flat_ precisely if it factors through the inclusion $\flat \mathbf{B}G \to \mathbf{B}G_{conn}$.

=--

For the purposes of [[Chern-Weil theory]] we want a good way to extract the [[curvature]] 2-form in a general abstract way from a cocycle $\nabla : X \stackrel{\simeq}{\leftarrow }C(U) \to \mathbf{B}G_{conn}$. In order to do that, we first need to discuss [[connections on 2-bundles]].

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

+-- {: .num_defn }
###### Definition

Write $U(1) \in Smooth0Type$ for the [[smooth space]] of the [[circle group]]. Write

$$
  \mathbf{d}log \colon U(1) \to \Omega^1
$$

for the homomorphism of smooth spaces which over an abstract coordinate system $U \in$ [[CartSp]] is given by the function

$$
  \mathbf{d} log_u \colon C^\infty(U,U(1)) \to \Omega^1(U)
$$

which sends a $U(1)$-valued $f \colon U \to U(1)$ -- for which one can always find an $\mathbb{R}$-valued function $\hat f \colon U \to \mathbb{R}$ for whuch $f = \hat f \,mod\, \mathbb{Z}$ -- to the [[differential 1-form]] $\mathbf{d} \hat f$.

=--

+-- {: .num_defn }
###### Definition

For $n \in \mathbb{N}$, the [[chain complex]] of [[smooth spaces]] (of [[sheaves]] on [[CartSp]])

$$
  (U(1) \stackrel{\mathbf{d} log}{\to} \Omega^1 \stackrel{\mathbf{d}}{\to} \cdots \stackrel{\mathbf{d}}{\to} \Omega^n)
$$ 

(regarded as a chain complex of [[abelian groups]] and as sitting in degrees $n$ through 0) is called the (smooth) _[[Deligne complex]]_ in these degrees.

=--

+-- {: .num_defn #BnU1connFromDK}
###### Definition

For $n \in \mathbb{N}$, write

$$
  \mathbf{B}^n U(1)_{conn}
  =
  DK(U(1) \stackrel{\mathbf{d} log}{\to} \Omega^1 \stackrel{\mathbf{d}}{\to} \cdots \stackrel{\mathbf{d}}{\to} \Omega^n)
  \in
  Smooth\infty Grpd
$$

for the [[smooth ∞-groupoid]] presented by the [[Deligne complex]] under the [[Dold-Kan correspondence]] map, def. \ref{DKMap}.

=--

For $X \in $ [[Smooth∞Grpd]] we say that 

* a morphism $\nabla \colon X\to \mathbf{B}^n U(1)_{conn}$ modulates a [[circle n-bundle with connection]] on $X$.

We also call $\mathbf{B}^n U(1)_{conn}$ the **universal [[moduli ∞-stack]] of circle $n$-bundles with connection.

+-- {: .num_defn #UBnU1FromDK}
###### Definition

Write

$$
  \array{
    \mathbf{B}^n U(1)_{conn} & \coloneqq & DK( & U(1) &\stackrel{\mathbf{d} log}{\to}& \Omega^1 &\stackrel{\mathbf{d}}{\to}& \cdots & \stackrel{\mathbf{d}}{\to} & \Omega^n & )
   \\
   \downarrow^{\mathrlap{U_{\mathbf{B}^n U(1)_{conn}}}}
   & \coloneqq& DK( & \downarrow^{\mathrlap{id}} && \downarrow && && \downarrow )
   \\
    \mathbf{B}^n U(1) & \coloneqq & DK( & U(1) &\stackrel{}{\to}& 0 &\stackrel{}{\to}& \cdots & \stackrel{\mathbf{d}}{\to} & 0 & )    
  }
$$

for the canonical forgetful morphism from moduli of $n$-connections to those of the underlying principal bundles.

=--

+-- {: .num_defn #UBnU1connk}
###### Definition

More generally, we may consider the intermediate stages

$$
  \array{
    \mathbf{B}^n U(1)_{conn} & \coloneqq & DK( & U(1) &\stackrel{\mathbf{d} log}{\to}& \Omega^1 &\stackrel{\mathbf{d}}{\to}& \cdots & \stackrel{\mathbf{d}}{\to} & \Omega^k & \stackrel{\mathbf{d}}{\to} & \Omega^{k+1} &\to& \cdots &\stackrel{\mathbf{d}}{\to} & \Omega^n)
   \\
   \downarrow^{}
   & \coloneqq& DK( & \downarrow^{\mathrlap{id}} && \downarrow^{\mathrlap{id}} && && \downarrow^{\mathrlap{id}} & & \downarrow && \cdots & & \downarrow)
   \\
    \mathbf{B}^n U(1)_{conn^k} & \coloneqq & DK( & U(1) &\stackrel{\mathbf{d}}{\to}& \Omega^1 &\stackrel{\mathbf{d}}{\to}& \cdots & \stackrel{\mathbf{d}}{\to} & \Omega^k & \to & 0 &\to& \cdots &\to & 0 )    
  }
$$


=--


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

#### Differential moduli
 {#DifferentialModuli}

We discuss the _moduli stacks_ of higher principal connections, over a fixed $X \in Smooth\infty Grpd$.

For $n \in \mathbb{N}$ and with $\mathbf{B}^n U(1)_{conn} \in $ [[Smooth∞Grpd]] the universal [[moduli stack]] for [[circle n-bundles with connection]], def. \ref{BnU1connFromDK}, and for $X \in Smooth\infty Grpd$, one may be tempted to regard the [[internal hom]]/[[mapping space]] $[X, \mathbf{B}^n U(1)_{conn}]$ as the [[moduli stack]] of [[circle n-bundles with connection]] on $X$. However, for $U \in $ [[CartSp]] an abstract [[coordinate system]], $U$-plots and their [[n-morphism|k-morphisms]] in  $[X, \mathbf{B}^n U(1)_{\mathrm{conn}}]$ are circle principal $n$-connections and their $k$-fold [[gauge transformations]] on $U \times X$, and this is not generally what one would want the $U$-plots of the moduli stack of such connections on $X$ to be. Rather, that moduli stack should have

1. as $U$-plots smoothly $U$-parameterized collections $\{\nabla_u\}$ of $n$-connections on $X$;

1. as $k$-morphisms smoothly $U$-parameterized collections $\{\phi_u\}$ of [[gauge transformations]] between them.

The first item is equivalent to: a single $n$-connection on $U \times X$ such that its local connection $n$-forms have no legs along $U$. This is essentially the situation of moduli of differential forms which we have discussed above in _[Smooth moduli space of differential forms](#SmoothUniversalModuliSpaceOfDifferentialForms))_.

But the second item is different: a gauge transformation of a single $n$-connection $\nabla$ on $U \times X$ needs to respect the [[curvature]] of the connection along $U$, but a family $\{\phi_u\}$ of gauge tranformations between the restrictions $\nabla|_u$ of $\nabla$ to points of the coordinate patch $U$ need not.

In order to capture this correctly, the _concretification_-process, def. \ref{ConcreteObjectsAndConcretification}, that yielded the moduli spaces of differential forms in [above](#SmoothUniversalModuliSpaceOfDifferentialForms) is to be refined to a process that concretifies the higher stack $[X, \mathbf{B}^n U(1)_{conn}]$ degreewise in stages. 

1. [For circle-principal 1-connections](#DifferentialModuliCircle1Bundles)

1. [For circle-principal 2-connections](#DifferentialModuliCircle2Bundles)

##### For circle-principal 1-connections
 {#DifferentialModuliCircle1Bundles}

We discuss this first for $n = 1$, hence for moduli stacks of [[circle bundles]] [[connection on a bundle|with connection]].

+-- {: .num_defn }
###### Definition

For $X \in Smooth1Typpe \hookrightarrow$ [[Smooth∞Grpd]] a [[smooth groupoids]], we write 

$$
  X \to \sharp_2 X \to \sharp_1 X \to \sharp X 
$$

for the [[n-image]] factorization of the canonical morphism $X \to \sharp X$ to the sharp modality, def. \ref{SharpModalityOfLocalTopos}.

=--

+-- {: .num_remark }
###### Remark

If $X \in Smooth0Type$ is just a smooth space then $\sharp_2 X \simeq X$ and $\sharp_1 X = Conc X$ is the concretification of $X$, def. \ref{ConcreteObjectsAndConcretification}.

=--

One might call $\sharp_1 X$ the "1-concretification" and $\sharp_2 X$ the "2-concretification" of $X$. But generally what one might actually want to call a "concretification" of $X$ involves an interplay of both, as we will see now.

+-- {: .num_defn #U1ConnXByFiberProductOfSharpn}
###### Definition

For $X \in $ [[Smooth∞Grpd]], write 

$$
  U(1)\mathbf{Conn}(X) 
  \coloneqq
  \sharp_1[X, \mathbf{B}U(1)_{conn}]
  \underset{\sharp_1 [X,\mathbf{B}U(1)]}{\times}
  \sharp_2 [X, \mathbf{B}U(1)]
$$

for the [[smooth groupoid]] which is the [[homotopy pullback]] in 

$$
  \array{
    U(1)\mathbf{Conn}(X) &\to& \sharp_2 [X, \mathbf{B}U(1)]
    \\
    \downarrow && \downarrow
    \\
    \sharp_1[X, \mathbf{B}U(1)_{conn}]
    &\stackrel{\sharp_1 [X,U_{\mathbf{B}U(1)_{conn}}] }{\to}&
    \sharp_1 [X,\mathbf{B}U(1)]
  }
  \,.
$$

Here the bottom morphism is the $\sharp_1$-image of the forgetful morphism $U_{\mathbf{B}U(1)_{conn}} \colon \mathbf{B}U(1)_{conn} \to \mathbf{B}U(1)$ from def. \ref{UBnU1FromDK}; and the right morphism is the canonical projection from the [[2-image]] to the [[1-image]], as discussed there.

=--

+-- {: .num_prop #U1ConnXIsIndeedDifferentialModuli}
###### Proposition

The smooth groupoid $U(1)\mathbf{Conn}(X)$ of def. \ref{U1ConnXByFiberProductOfSharpn} is indeed the smooth moduli object/[[moduli stack]] of [[circle n-bundle with connection|circle-principal connections]] on $X$; in that its $U$-plots of  are smoothly $U$-parameterized collections of smooth circle-principal connections on $X$ and its morphisms of $U$-plots are smoothly $U$-parameterized collections of smooth gauge transformation between these, on $X$.

=--

+-- {: .proof}
###### Proof

By the discussion at [[n-image]] and using arguments as for the concretification of moduli of differential forms above, we have:

* $\sharp_1 [X, \mathbf{B}U(1)_{conn}]$ has as $U$-plots those connections $\nabla$ on $U \times X$ whose connection 1-forms have no leg along $U$, hence smooth $U$-parameterized families $\{\nabla_u\}$ of connections on $X$, and has as morphisms $\Gamma(U)$-parameterized (hence non-smooth) collections $\{\phi_u\}$ of gauge transformations of connections on $X$;

* $\sharp_1 [X, \mathbf{B}U(1)]$ looks similarly, just without the connection information;

* $\sharp_1 [X, U_{\mathbf{B}U(1)_{conn}}]$ simply forgets the connection data on the collections of bundles-with-connection; the point to notice is that oveach each chart $U$ it is a [[fibration]]([[isofibration]]): given a $\Gamma(U)$-parameterized collection of gauge transformations out of a smoothly $U$-parameterized collection of bundles and then a smooth choice of smooth connections on these bundles, the $\Gamma(U)$ collection of gauge transformations of course also acts on these connections;

* $\sharp_2 [X, \mathbf{B} U(1)] \simeq [X, \mathbf{B} U()1]$ (because if two gauge transformations of bundles on $U \times X$ coindide on each point of $U$ as gauge tranformations on $X$, then they were already equal).

From the third item it follows, by the discussion at [[homotopy pullback]], that we may compute equivalently simply the pullback in the 1-category of groupoid-valued presheaves on [[CartSp]]. This means that a $U$-plot of $U(1)\mathbf{Conn}(X)$ is a smoothly $U$-parameterized collection $\{\nabla_u\}$ of connections on $X$, and that a morphism between such as a $\Gamma(U)$-parameterized collection of gauge transformations $\{\phi_u\}$ of connections, such that their underlying collection of gauge transformations of bundles is a smoothly $U$-parameterized family. But gauge transformations of 1-connections are entirely determined by the underlying gauge transformation of the underlying bundle, and so this just means that also the morphism of $U$-plots of $U(1)\mathbf{Conn}(X)$ are smoothly $U$-paramezerized collections of gauge transformations. 


=--

##### For circle-principal 2-connections
 {#DifferentialModuliCircle2Bundles}

We now discuss moduli of [[circle n-bundle with connection|circle 2-bundles with connection]] over a given base $X$.

Recall that by def. \ref{UBnU1connk} we write

$$
  \mathbf{B}^2U(1)_{conn^1} \coloneqq DK(U(1) \stackrel{\mathbf{d}}{\to} \Omega^1 \to 0)
  \,.
$$


+-- {: .num_defn #BU1ConnXByFiberProductOfSharpn}
###### Definition

For $X \in Smooth \infty Grpd$ write

$$
  (\mathbf{B}U(1))\mathbf{Conn}(X)
  \coloneqq
  \sharp_1 [X, \mathbf{B}^2 U(1)_{conn}]
  \underset{\sharp_1 [X, \mathbf{B}^2 U(1)_{conn^1}]}{\times}
  \sharp_2 [X, \mathbf{B}^2 U(1)_{conn^1}] 
  \underset{\sharp_2 [X, \mathbf{B}^2 U(1)]}{\times}
  \sharp_3 [X, \mathbf{B}^2 U(1)]
$$

for the [[homotopy limit]] in the [[diagram]]

$$
  \array{
    (\mathbf{B}U(1))\mathbf{Conn}(X) &\to& &\to& 
    \sharp_3 [X, \mathbf{B}^2 U(1)]
    \\
    \downarrow && && \downarrow
    \\
    && \sharp_2 [X, \mathbf{B}^2 U(1)_{conn^1}] 
   &\to& 
    \sharp_2 [X, \mathbf{B}^2 U(1)]
    \\
    \downarrow && \downarrow
    \\
    \sharp_1 [X, \mathbf{B}^2 U(1)_{conn}]
    &\stackrel{}{\to}&
    \sharp_1 [X, \mathbf{B}^2 U(1)_{conn^1}]
  }
  \,.
$$

Here the horizontal morphisms are those induced under the [[n-image]] by those of def. \ref{UBnU1connk}  and where the vertical morphisms are the [[n-image]]-projections, as discussed there.

We call this the _moduli 2-stack of circle-principal 2-connections_ on $X$. 

=--

+-- {: .num_prop }
###### Proposition

The smooth 2-groupoid $(\mathbf{B}U(1))\mathbf{Conn}(X)$ of 
def. \ref{BU1ConnXByFiberProductOfSharpn} is indeed the smooth moduli object of [[circle n-bundle with connection|circle-principal 2-connections]] on $X$; in that its $U$-plots of  are smoothly $U$-parameterized collections of smooth circle-principal 2-connections on $X$ and its morphisms of $U$-plots are smoothly $U$-parameterized collections of smooth gauge transformation between these, on $X$, and
similarly for its 2-morphisms.

=--

+-- {: .proof}
###### Proof (sketch)

By a variant of the [[pasting law]] one sees that the defining 
[[homotopy limit]] may be computed as the pasting of [[homotopy pullbacks]]

$$
  \array{
    (\mathbf{B}U(1))\mathbf{Conn}(X) 
    &\to& 
    A
    &\to& 
    \sharp_3 [X, \mathbf{B}^2 U(1)]
    \\
    \downarrow && \downarrow && \downarrow
    \\
    B &\to & \sharp_2 [X, \mathbf{B}^2 U(1)_{conn^1}] 
   &\to& 
    \sharp_2 [X, \mathbf{B}^2 U(1)]
    \\
    \downarrow && \downarrow
    \\
    \sharp_1 [X, \mathbf{B}^2 U(1)_{conn}]
    &\stackrel{}{\to}&
    \sharp_1 [X, \mathbf{B}^2 U(1)_{conn^1}]
  }
  \,.
$$

For each of these smaller homotopy-pullback squares the reasoning is directly analogous to that in the proof of prop. \ref{U1ConnXIsIndeedDifferentialModuli}:

Starting in the bottom left, $\sharp_1 [X, \mathbf{B}^2 U(1)_{conn}]$ has over $U \in CartSp$ smoothly $U$-parameterized collections of 2-connections on $X$ as objects, but discretely $\Gamma(U)$-parameterized collections of morphisms and 2-morphisms between them. The morphism to the right forgets just the local differential 2-form part of a 2-connection (keeping the 1-form part). This has the effect that where in $\sharp_2 [X,\mathbf{B}^2 U(1)_{conn^1}]$ the 1-morphisms over $U$ are gauge transformations of such truncated 2-connections over $U \times X$, these are now not forced to strictly fix the curvature along $U$, hence these are smoothly $U$-parameterized collections of gauge transformation on $X$ (between truncated 2-connections). So the pullback object $B$ combines these two aspects and hence has as objects and as 1-morphisms now smoothly $U$-parameterized collections of connections and gauge transformations on $X$, respectively, and only the 2-morphisms of $B$ keep beeing discretely $\Gamma(U)$-parameterized collections of 2-gauge transformations.

Similarly then, $A$ is already the correct smooth moduli 2-stack, but of truncated connections, and so finally the fiber product of $A$ with $B$ forces the discrete families of 2-morphisms of untruncated gauge transformations to have underlying smooth families of 2-morphisms of truncated gauge transformations. But since these uniquely fix the untruncated ones, this makes $(\mathbf{B}U(1))\mathbf{Conn}(X)$ have the correct smooth collections of structures in each degree.

=--

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


+-- {: bluebox #PHYSICS}
###### Contents

**II) Physics**

1. [Physics in Higher Geometry: Motivation and Survey](#PhysicsMotivationAndSurvey)

1. [Fields](#Fields)

1. [Lagrangians and Action functionals](#LagrangiansAndActionFunctionals)

1. [Equations of motion](#EquationsOfMotion)

1. [Classical mechanics via prequantized Lagrangian correspondences](#ClassicalMechanicsByPrequantizedLagrangianCorrespondences)


1. [Local (topological) prequantum field theory](#LocalTopologicalPrequantumFieldTheory)

1. [Prequantum Gauge theory and Gravity](#ActionFunctionalsForChernSimonsTypeGaugeTheories)

1. [Geometric quantization](#GeometricQuantization)

1. [Quantum mechanics](#QuantumMechanics)


=--

## **Physics in Higher Geometry: Motivation and Survey**
 {#PhysicsMotivationAndSurvey}

Before we discuss technical details starting in the [next chapter](#Fields) here we survey general ideas of [[theory (physics)|theories]] in fundamental [[physics]] and motivate how these are naturally formulated in terms of the [[higher geometry]] that we developed in the [first part](#GEOMETRY).

+-- {: bluebox}
###### 

1. [Ingredients of fundamental physics](#IngredientsOfFundamentalPhysics)

1. [Topological local Lagrangian gauge field theory](#TopologicalLocalLagrangianGaugeFieldTheory)

1. [Chern-Simons field theory as a toy example](#ChernSimonsTheoryAsAToyExample)

1. [Topological local field theory in higher category theory](#TopologicalLocalFieldTheoryInHigherGeometry)

1. [Intermezzo: Elements of higher cohesive geometry](#IntermezzoElementsOfHigherCohesiveGeometry)

1. [Chern-Simons theory as the archetypical example](#CSAsArchetypicalExample)

1. [Topological local Lagrangian field theory in higher geometry](#TopologcalLocalLagrangianFieldTheoryInHigherGeometry)

1. [7-dimensional Chern-Simons theory as the next example](#7dCSTheoryAsExample)

1. [∞-Chern-Simons theory as the general example](#InfinityCSAsGeneralExample)

=--

### Ingredients of fundamental physics
 {#IngredientsOfFundamentalPhysics}

Ever since [[Issac Newton]], [[theories of physics]] are formulated in the language of [[mathematics]]. Modern physics is formulated in terms of modern mathematics in the most intimate way.
We aim to give here an account at least of central parts of modern physics naturally formulated in the mathematics of _[[higher geometry]]_ that we discussed in _[geometry of physics - Geometry](geometry+of+physics#GEOMETRY)_. 

The physics that we are concerned with is _fundamental_ physics,
that part of the large subject of physics which is concerned with elementary  processes and phenomena of physics from which all others are thought to _emerge_ as approximations to collective effects of complex configurations of the elementary 
entities.

The best [[theory (physics)|theory]] of fundamental physics as presently understood is known as _[[Einstein-Yang-Mills-Dirac-Higgs theory]]_. 
While fundamental, this theory has _free parameters_. These index different flavors of the same general mechanism. Notably the species and the masses of the fundamental [[fermion]] [[particles]] are such parameters, as 
is their coupling to the [[force fields]].

Specifying these parameters is called constructing a 
_[[model (in theoretical physics)|model]]_ in physics  and specifically a [[phenomenology|phenomenological model]] of fundamental physics, 
if aimed at making the observations that are predicted by the theory to closely match those that are being made in experiments. The global choice of these parameters that make the predictions  match all available data to the currently best possible degree is called the _standard model_, specifically the  _[[standard model of particle physics]]_ for the sector in which the large-scale description of the 
force of [[gravity]] is approximately negligible, and the 
_[[standard model of cosmology]]_
which focuses on that large scale structure.

The following table list some key ingredients of the standard theory of fundamental physics, all of which we discuss in detail further below.

[[!include standard model of fundamental physics - table]]

### Topological local Lagrangian gauge field theory
 {#TopologicalLocalLagrangianGaugeFieldTheory}

While the [[standard model of fundamental physics - table|standard model of fundamental physics]] is a specification of the general  framework of [[Einstein-Yang-Mills-Dirac-Higgs theory]], that theory itself is a particular realization of several deep general principles  of theoretical physics: it is 

1. a **[[field (physics)|field]]** theory;
1. a **[[gauge theory|gauge]]** theory;
1. a **[[Lagrangian]]** theory;
1. a **[[local quantum field theory|local]]** theory;
1. a **[[topological field theory|topological]]** theory.

We briefly indicate what this means, a formal discussion of these notions will be given in the  main part below.

* A **[[field (physics)|field]]** theory identifies the basic configurations of a physical system with generalized functions on spacetime, such as [[tensor fields]], and more generally with [[sections]] $\phi$ of some [[fiber bundle]] over spacetime

  $$
    \array{ 
      && E 
      \\
      & {}^{\mathllap{\phi}}{\nearrow} & \downarrow^{\mathrlap{field\;bundle}}   
      \\
      X &\stackrel{id}{\to}& X
     }
   $$

  (This is the traditional formulation. Below we discuss that the concept of _field [[fiber bundle]]_ needs to be refined to that of field _[[fiber ∞-bundle]]_ in order to accuratly capture all aspects of field theory:   _[The traditional idea of field bundles and its problems](#IdeaOfFieldBundlesAndItsProblems)_.)


* A **[[gauge theory|gauge]]** theory in the broad sense has not just a [[set]] or [[smooth space]] of field configurations but has a [[groupoid]] or [[stack]]/[[smooth groupoid]] of field configurations: there are equivalences between nominally different field configurations 

  $$
    \phi \stackrel{\simeq}{\to} \phi'
  $$

  called _[[gauge transformations]]_.

   A gauge theory in the original sense specifically has a groupoid of [[principal connections]] as its configurations. (Notice that gauge transformations are not in general just a redundancy of the description of the theory, but are genuine data: there are in general non-trivial gauge [[automorphisms]] of a field and the stack of gauge field configurations is not in general equivalent to a plain [[sheaf]].)

* A **[[Lagrangian]]** theory is one which is specified by a [[smooth function]] on the space of all its configurations, called the (exponentiated) _[[action functional]]_ $\exp(i S)$. This function is assumed to be the [[integration of differential forms|integral]] of a [[differential form]] $L$ on [[spacetime]] that itself is a function of the field configurations and called the [[Lagrangian]] of the theory. 

  $$
    \exp(i S(\phi)) = \exp\left(i \int_X L\left(\phi\right)\left(x\right) \right) 
  $$

  The [[critical locus]]

  $$
    \left\{
	 \phi \in \mathbf{Fields}(\Sigma)		|
		d_{\mathrm{var}} S_\phi \simeq 0
	  \right\}
  $$

  of the action functional is called the _[[phase space]]_ of the theory, a point of this is said to be a solution to the _[[equations of motion]]_ of the theory.

* A **[[local quantum field theory|local]]** theory has a Lagrangian form which at each point of spacetime only depends on the values of the fields at that point, and of finitely many derivatives of the fields at that point, hence a [[local action functional]]:

  $$
    \exp(i S(\phi)) = \exp\left(i \int_X L\left(\phi\left(x\right), \nabla \phi\left(x\right)\right)\right) 
  $$

  This means that a _[[local Lagrangian]]_ is a horizontal form on the [[jet bundle]] of the field bundle of which the fields are sections.

* A **[[topological field theory|topological]]** theory finally is one where a field bundle $E_X \to X$ is naturally associated to every [[smooth manifold]] $X$, typically of some fixed dimension and possibly equipped with  topological [[G-structure]] such as an [[orientation]], but not equipped with any further geometric structure: all geometric structure such as [[Riemannian metrics]] on spacetime are themselves regarded as parts of the field content in a topological theory.


### Chern-Simons field theory as a toy example
 {#ChernSimonsTheoryAsAToyExample}

Most of this was fairly well understood decades ago, by the 1960s. But even with all this conceptual understanding of the structure of fundamental physics available, there were and are a lot of implications of 
_[[topological field theory|topological]] [[local  Lagrangian]] [[gauge field theory]]_ which remained elusive.


In the 1980s attention turned to _other_ topological local Lagrangian gauge field theories than that governing the standard model: it turns out that there are many such  [[theories of physics]] that share crucial properties with the standard model but which  otherwise predict, if considered as phenomenological models, physics  radically different from that
which we actually observe experimentally. For instance there are respectable theories of fundamental 
physics which describe physics in dimensions other than the three spatial and one time dimension which we clearly observe, theories that contain no force of gravity, others that contain only the force of gravity, theories that contain mirror partners of every species of matter or contain no matter at all, etc.

In short, it was gradually realized, and realized to be important, that, in the platonic world of mathematics and of theoretical physics, there is a whole space of field theories, in which the one underlying the standard model of observed physics is only one single point, even if regarded with its free parameters.

A crucial step forward happened when around 1989 [[Edward Witten]], in this vein,  introduced the study of what is now called _[[Chern-Simons theory]]_ a topological local Lagrangian gauge field theory which, as such, shares
some crucial principles with Einstein-Maxwell-Yang-Mills theory, while at the  same time being  radically different and most importantly: 
much simpler to analyze. 

The dimension of Chern-Simons theory is 3 instead of 4, but 
Chern-Simons theory has a [[gauge field]] just as [[Yang-Mills theory]] does. For $G$ a [[connected topological space|connected]] [[simply connected topological space|simply connected]] [[gauge group]], this is mathematically represented by a 
[[infinity-Lie algebroid-valued differential form|Lie algebra-valued differential 1-form]] $A$.

The [[Lagrangian]] of [[Chern-Simons theory]] is the [[Chern-Simons 3-form]]

$$
  L(A)
  \coloneqq
  \mathrm{CS}_3(A)
  \coloneqq
  \langle A \wedge F_A\rangle
  + 
  c
  \langle A \wedge [A \wedge A]\rangle
  \,,
$$

whence the name of the theory, and hence the Chern-Simons [[action functional]] is

$$
  \exp(i S(A)) 
  =
   \exp\left(
     2 \pi i \int_{\Sigma_X} \mathrm{CS}_3(A)
	\right)
$$


At the same time Chern-Simons theory is still being rich in phenomena, 
in fact so rich in phenomena that for instance it helped illuminate deep mathematical problems that had not otherwise been understood as much before (properties called _[[knot invariants]]_).


### Topological local field theory in higher category theory
 {#TopologicalLocalFieldTheoryInHigherGeometry}

Another pleasant effect of the introduction of the Chern-Simons "toy model"  for topological field theory was that, 
due to its conceptual simplicity, its basic structure could be appreciated also by mathematicians not trained in theoretical physics, who would otherwise fail to see through all the  physics jargon involved in the available discussion of realistic models. Accordingly, immediately after the realization of Chern-Simons field theory,  the first mathematically precise axiomatizations of an $n$-dimensional _[[topological field theory]]_ was proposed, by [[Michael Atiyah]]: "[[functorial quantum field theory]]"

This axiomatization demands in particular that to each [[closed manifold]] of [[dimension]] $(n-1)$ is assigned a [[vector space]]

$$
  Z 
   \;\colon\; 
  \Sigma_{n-1} \mapsto Z(\Sigma_{n-1}) \in \mathrm{Vect}
$$

thought of as the _[[space of physical states]]_ of the theory on the
spatial slice $\Sigma_{n-1}$ of spacetime. 

However, This original axiomatization did not capture the full _[[local quantum field theory|locality]]_ property: the spaces of states are assigned globally to a space $\Sigma_{n-1}$ and are not required to be obtainable by "integrating up local data" over $\Sigma_{n-1}$. 

In order to refine this, one needs an axiomatization of field theory that assigns data also to manifolds $\Sigma_{k}$ of [[dimension]] $0 \leq k \leq n$. This should be such that the data assigned to a torus $\Sigma_{k} \times S^1$ is the [[trace]] in a suitable sense, of the data assigned to $\Sigma_{k}$ itself. It turns out that the way to capture this is to think of $Z(\Sigma_k)$ as being a vector space in [[higher category theory]]/[[directed homotopy type theory]]: an [[n-vector space|(n-k)-vector space]].

$$
  \Sigma_k \mapsto Z(\Sigma_k) \in (n-k)\mathrm{Vect}
$$

That something like this should work was hypothetized by [[Dan Freed]] (in _[[Higher Algebraic Structures and Quantization]]_), the precise formulation was later given by [[Jacob Lurie]] (in _[[On the Classification of Topological Field Theories]]_). In the literature the resulting axiomatization is called _[[extended topological field theory]]_ (with "extended" referring to extending the axioms from [[codimension]] 1 to higher codimension) or _[[multi-tiered field theory]]_ (thinking of the data in higher [[codimension]] as being higher "tiers" of the theory). 

But in the [[physics]]-community, at least in the [[algebraic quantum field theory]]-community, there is also the well-established term of _[[local quantum field theory]]_ which refers broadly to what the axioms of "extended TQFT" capture. Hence we should think of this as formalizing _topological local field theory_.


### Topological local *Lagrangian* field theory in higher geometry
 {#TopologcalLocalLagrangianFieldTheoryInHigherGeometry}

The formalization of [[extended topological field theory]] thus captures the _[[local quantum field theory|local]]_ aspect of [[field (physics)|field]] [[theory (physics)|theory]]. But we saw [above](#TopologicalLocalLagrangianGaugeFieldTheory) that the theories of fundamental physics have one more crucial property: they are _[[Lagrangian]]_. Here we indicate how to formulate Lagrangian theories that are also local in the sense of [[extended field theory]].

The step of passing from a [[Lagrangian]] to the corresponding 
[[quantum field theory]] is called _[[quantization]]_. There are two broad approaches to formalization of what this means, called _[[deformation quantization|algebraic deformation quantization]]_ and _[[geometric quantization]]_.  The first of these deals explicitly with producing [[algebras of quantum observables]], while the second describes explicitly how to construct the [[spaces of states]] that we considered above. Both are at least roughly dual to each other, in the spirit of [[Isbell duality|the general duality]] between [[algebra]] and [[geometry]]. 
For the following discussion we follow the ideas of [[geometric quantization]], which naturally fit a discussion of _[[geometry of physics]]_.
The following table surveys some keywords in this context which we will discuss in detail further below.

[[!include Isbell duality - table]]


In its traditional formulation, one considers the [[symplectic form]] $\omega$ which is naturally induced by a [[local Lagrangian]] on its (reduced) [[covariant phase space]] and says that a _[[geometric prequantization]]_ of this form is the choice of a $U(1)$-[[principal connection]] $\nabla$ on the phase space whose [[curvature]] $F_\nabla$ is $\omega$, hence a lift in

$$
  \array{
    &&& \mathbf{B}U(1)_{conn}
    \\
    {{prequantum} \atop {circle\;bundle}} && {}^{\mathllap{\nabla}}\nearrow & \downarrow^{\mathrlap{F_{(-)}}} & curvature
    \\
    &PhaseSpace
    &\stackrel{\omega}{\to}&
    \Omega^2_{cl}
    \\
    &&
    sympl.\;form
  }
  \,.
$$

A [[section]] of the [[associated bundle|associated]] [[complex line bundle]]

$$
  \array{
    && P \times_{U(1)}\mathbb{C}
    \\
    & {}^{\mathllap{\Psi}}\nearrow & \downarrow
    \\
    X &\stackrel{id}{\to}& X
  }
$$

is called a _[[wave function]]_ on phase space. One is to choose a [[polarization]] of phase space, equipping it locally with "[[canonical coordinates]]" and "[[canonical momenta]]". Then a _[[quantum state]]_ in geometric quantization is a [[wave function]] $\Psi$ which only depends on the [[canonical coordinates]].


$$
  Z(\Sigma_{n-1}) 
  \coloneqq
  \{wave\; functions\;of\;canonical\;coordinates\}
  \coloneqq
  \left\{
    polarized\;sections\;of\;prequantum\;line\;bundle
  \right\}
  \,.
$$

From this it is clear that in order to refine this to local (extended, multi-tiered)  [[prequantum field theory]] we are to assign _[[circle n-bundle with connection|higher line bundles]]_ in higher codimension, namely a [[prequantum n-bundle|prequantum (n-k)-bundle]] in [[codimension]] $k$.

As a first indication that this makes good sense, notice that the natural assignment to a field in codimension 0, hence to a field configuration on [[spacetime]], is its [[action functional]]. Being a $U(1)$-valued function, this is naturally thought of as a 0-bundle, the _[[prequantum 0-bundle]]_.

So we are after a picture as indicated in the following table. 

| | | [[extended prequantum field theory|local/extended Lagrangian field theory]] |  | [[extended quantum field theory|local/extended quantum field theory]]  |
|--|--|--|--|--|
| closed piece of [[spacetime]] of [[dimension]] $0 \leq k \leq n$ |  [[prequantum field theory]] | [[prequantum n-bundle|prequantum (n-k)-bundle]] | [[geometric quantization]] | [[space of states|space of]] $(n-k)$-[[wave functions]] |
| [[closed manifold]] of [[dimension]] $0 \leq k \leq n$ | $\stackrel{local\;prequantum\;field\;theory}{\mapsto}$ | [[circle n-bundle with connection|circle (n-k)-bundle with connection]] on [[moduli stack]] of [[field (physics)|field configurations]] | $\stackrel{polarized\; sections}{\mapsto}$ | [[n-vector space|(n-k)-vector space of states]] | 
| $\Sigma_k$ | $\mapsto$ | $\exp(2 \pi i \int_{\Sigma_k}[\Sigma_k,\mathbf{L}]) : [\Sigma_k, \mathbf{Fields}] \to \mathbf{B}^{n-k} U(1)_{conn}$ | $\mapsto$ | $Z(\Sigma_{n-k})$ |


### Intermezzo: Recalling elements of higher cohesive geometry  
 {#IntermezzoElementsOfHigherCohesiveGeometry}

The idea of _[[extended prequantum field theory]]_ indicated [above](#TopologcalLocalLagrangianFieldTheoryInHigherGeometry)  is best illustrated by the example of [[Chern-Simons field theory]]. We talk about this in a moment [below](#CSAsArchetypicalExample), but since in order to do so we need now at least some basic notions from [[cohesion|cohesive]] [[higher geometry]], we very briefly recall these first, just for reference. For more discussion see at _[geometry of physics - smooth homotopy types](geometry+of+physics#SmoothnGroupoids)_  and _[geometry of physics - Maurer-Cartan forms](geometry+of+physics#MaurerCartanForms)_ and _[geometry of physics  - principal connections](geometry+of+physics#PrincipalConnections)_

Fix some [[site]] $\mathcal{C}$ of test spaces which encode some notion of  [[geometry]]. The running example to keep in mind is the site [[SmthMfd]] of [[smooth manifolds]], or equivalently its full [[dense subsite]] of [[CartSp]] on manifolds of the form $\mathbb{R}^n$.  Assume for simplicity that the site has _[[point of a topos|enough points]]_ (which [[SmthMfd]] does).

Then the [[(2,1)-category]] of [[(2,1)-sheaves]] ([[stacks]]) on $\mathcal{C}$ is the [[simplicial localization]] 

$$
  Sh_{(2,1)}(\mathcal{C})
  \simeq
  L_{le} Func(\mathcal{C}^{op}, Grpd)
  \,.
$$

of that of [[groupoid]]-valued [[presheaves]] on $\mathbf{C}$ at the _local equivalences_. This means that $Sh_{(2,1)}(\mathcal{C})$ is the result of turning [[stalk]]-wise ("local") [[equivalence of groupoids|equivalence of groupoids]] into actual [[equivalences]].

For the running example of $\mathcal{C} \simeq $ [[SmthMfd]] we may think of an object in $Sh_{(2,1)}(\mathcal{C})$ as a _[[smooth groupoid]]_. Examples include [[smooth manifolds]], [[diffeological space]],  [[orbifolds]], [[Lie groupoids]]/[[differentiable stacks]], sheaves of smooth differential forms, etc.

The higher refinement of groupoids which we need are _[[∞-groupoids]]_. The collection of these is equivalently that of [[simplicial sets]] or (compactly generated weakly Hausdorff) [[topological spaces]] with the [[weak homotopy equivalences]] universally turned into actual [[homotopy equivalences]]:

$$
  \infty Grpd \simeq L_{whe} sSet \simeq L_{whe} Top
$$

The combination of these two aspects, the [[geometry]] and the [[homotopy theory]], is that of [[(∞,1)-sheaves]]/[[∞-stacks]], here we write $\mathbf{H}$ for the collection of [[presheaves]] of [[simplicial sets]] ([[simplicial presheaves]]) with the local ([[stalk]]-wise) [[weak homotopy equivalences]] universally turned into actual homotopy equivalences:

$$
  \array{
    \mathbf{H} \coloneqq
    & Sh_\infty(\mathcal{C})
    &
    \stackrel{
      \overset{\infty-stackif.}{\leftarrow}
    }{
      \hookrightarrow
    }
  &
  PSh_\infty(\mathcal{C})
  \\
  & \uparrow^{\mathrlap{\simeq}} && \uparrow^{\mathrlap{\simeq}}
  \\
  & L_{lwhe} Func(\mathcal{C}^{op}, sSet)
  &
  \stackrel{
    \overset{\mathbb{L} id}{\leftarrow}
   }{
     \underset{\mathbb{R} id}{\rightarrow}
  }&
  L_{whe} Func(\mathcal{C}^{op}, sSet)
  }
  \,.
$$

This $\mathbf{H}$ is the _[[(∞,1)-topos]]_ over $\mathcal{C}$. This is the kind of context for the [[higher geometry]] encoded by $\mathcal{C}$ in which all of our constructions take place.

In order to formulate not just [[kinematics]] but also [[dynamics]] in [[physics]], we need to require that $\mathbf{H}$ has an intrinsic notion of what it means to have a _path_ or _[[trajectory]]_ inside one of its objects. This is axiomatized by the notion of  _[[cohesion]]_: 

if $\mathcal{C}$ satisfies some properties that make it an an [[infinity-cohesive site]], the the [[global section geometric morphism]] of $\mathbf{H}$ extended to an [[adjoint quadruple]] of [[(∞,1)-functors]]:

$$
  \array{
   \mathbf{H}
    &
   \stackrel{\overset{\Pi}{\to}}{\stackrel{}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\to}}{\underset{coDisc}{\leftarrow}}}}} 
   &
  \infty Grpd
  \\
  \uparrow^{\mathrlap{\simeq}}
  &&
  \uparrow^{\mathrlap{\simeq}}
  \\
  L_{lwhe} Func(\mathcal{C}^{op}, sSet)
  &\stackrel{\overset{hocolim_{\mathcal{C}}}{\to}}{\stackrel{\overset{const}{\leftarrow}}{\stackrel{X \mapsto X(*)}{\stackrel{\overset{}{\to}}{\underset{}{\leftarrow}}}}}&
  L_{whe} sSet
  }
$$

with some mild extra condition on $\Pi$ and $coDisc$. This is the case in particular for $\mathcal{C} = $ [[SmthMfd]] in which case we say that $\mathbf{H}$ is the [[cohesive (∞,1)-topos]] of _[[smooth ∞-groupoids]]_.

The defining [[adjoint quadruple]] of [[(∞,1)-functors]] induces an [[adjoint triple]] of [[comonad|co]][[(∞,1)-monads]]:

| [[shape modality]] | $\dashv$ | [[flat modality]] | $\dashv$ |[[sharp modality]] |
|--|--|--|--|--|
| $\mathbf{\Pi} \coloneqq Disc \circ \Pi$ | | $flat \coloneqq Disc \circ \Gamma$ |   | $\sharp \coloneqq coDisc \circ \Gamma$  |

For $G \in Grp(\mathbf{H})$ a [[group object in an (∞,1)-category|group object]] in $\mathbf{H}$, hence a geometric [[∞-group]], we have by these axioms of [[cohesion]] a [[pasting diagram]] of [[(∞,1)-pullbacks]]

$$
  \array{
    G &\to& * 
    \\
    \downarrow^{\mathrlap{\theta_G}} && \downarrow
    \\
    \flat_{dR} \mathbf{B}G
    &\to&
    \flat \mathbf{B}G
    \\
    \downarrow && \downarrow
    \\
    * &\to& \mathbf{B}G
  }
  \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
  \array{
    \infty-group &\to& *
    \\
    {}^{\mathllap{MC\;form}}\downarrow && \downarrow
    \\
    deRham\, coefficients &\to& flat\;coefficients
    \\
    \downarrow && \downarrow
    \\
    * &\to& principal\,coefficients
  }
  \,.
$$

Here the [[delooping]] $\mathbf{B}G$ is the moduli of geometric $G$-[[principal ∞-bundles]],  $\flat_{dR} \mathbf{B}G$ is that of flat [[infinity-Lie algebroid-valued differential form
|L-∞ algebra valued differential forms]] and $\theta_G$ is the _[[Maurer-Cartan form]]_ on the [[smooth ∞-group]] $G$.

If $\mathbb{G}$ is "slightly abelian" in that it is equipped with the structure of a [[braided ∞-group]], then we write

$$
  curv_{\mathbb{G}}
  \;\colon\;
  \mathbf{B}\mathbb{G}
  \stackrel{\theta_{\mathbf{B}\mathbb{G}}}{\to}
  \flat_{dR}\mathbf{B}^2 \mathbb{G}
$$

for the [[Maurer-Cartan form]] of its [[delooping]] [[∞-group]] and call this the _universal [[curvature]] characteristic_.

Then _$\mathbb{G}$-[[differential cohomology]]_ is 
_$curv_{\mathbf{B}\mathbb{G}}$-[[twisted cohomology]]_.
In particular, if we consider globally defined curvature forms

$$
  \Omega_{cl}(-,\mathbb{G}) \to \flat_{dR}\mathbf{B}^2\mathbb{G}
$$

then the [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{B}\mathbb{G}_{conn}
    &\to&
    \Omega(-,\mathbb{G})
    \\
    \downarrow && \downarrow^{\mathrlap{F_{(-)}}}
    \\
    \mathbf{B}\mathbb{G}
    &\stackrel{curv_{\mathbf{B}\mathbb{G}}}{\to}&
    \flat_{dR}\mathbf{B}^2 \mathbb{G}
  }
$$

is the moduli for [[principal ∞-connections]].

Now for 

$$
  \mathbf{c}
  \;\colon\;
  \mathbf{B}G
  \to 
  \mathbf{B}\mathbb{G}
$$

a [[universal characteristic map]] we say that a _differential refinement_ is a choice of $\mathbf{B}G_{conn}$ and $\hat \mathbf{c}$ in

$$
  \array{
    \flat \mathbf{B}G 
    &\stackrel{\flat \mathbf{c}}{\to}&
    \mathbf{B}\mathbb{G}
    \\
    \downarrow && \downarrow^{}
    \\
    \mathbf{B}G_{conn} &\stackrel{\hat \mathbf{c}}{\to}&
    \mathbf{B}\mathbb{G}_{conn}
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}G
    &\stackrel{\mathbf{c}}{\to}&
    \mathbf{B}\mathbb{G}
  }
  \,.
$$

These are the [[extended Lagrangians]] in our discussion of [[extended prequantum field theory]].

In particular if, in the context of [[smooth ∞-groupoids]], we consider $\mathbb{G} = \mathbf{B}^{n-1}U(1)$ the [[circle n-group]] then 

$$
  \mathbf{B}\mathbb{G}_{conn}
  \simeq
  \mathbf{B}^n U(1)_{conn}
  \simeq
  DK(  U(1) \to \Omega^1 \to \cdots \to \Omega^n)
$$

is given as the [[∞-stackification]] of the image under the [[Dold-Kan correspondence]] of the _[[Deligne complex]]_ for [[ordinary differential cohomology]].

In this case there is [[fiber integration in ordinary differential cohomology]] refined to moduli $\infty$-stacks: for $\Sigma_k$ an oriented [[closed manifold]] of [[dimension]] $k$ we have a map of [[moduli ∞-stacks]]

$$
  \exp\left(
   2 \pi i \int_{\Sigma} (-)
  \right)
  \;\colon\;
  [\Sigma_k, \mathbf{B}^n U(1)_{conn}]
  \to 
  \mathbf{B}^{n-k} U(1)_{conn}
  \,.
$$

Composed with the [[internal hom]] this is _[[transgression]]_ of differential cocycles. The transgressions of an [[extended Lagrangian]] as above are (the moduli for) the higher [[prequantum n-bundles]] that we consider here.


### Chern-Simons theory as the archetypical example
 {#CSAsArchetypicalExample}

For illustration purposes, we survey how the [[Chern-Simons field theory]] considered as a toy model for topological local Lagrangian gauge field theory considered [above](#ChernSimonsTheoryAsAToyExample) has in [[higher geometry]] a [[prequantum n-bundle|prequantum (n-k)-bundle]] associated in [[codimension]] $k$.

First consider again $G$ to be a [[connected topological space|connected]] and [[simply connected topological space|simply connected]] [[simple Lie group]]. Then the [[integral cohomology]] of the [[classifying space]] of $G$ is

$$
  H^4(BG , \mathbb{Z}) \simeq \mathbb{Z}
  \,.
$$

An element in here is a [[universal characteristic class]] of $G$-[[principal bundles]]. In Chern-Simons theory this is going to be what traditionally is called the [[level (Chern-Simons theory)|level]] of the theory.

We write

$$
  c : B G \to  B^3 U(1) \simeq K(\mathbb{Z},4)
$$

for a representative [[universal characteristic map]] of the corresponding degree-4 [[universal characteristic class]]. 


Under [[geometric realization of cohesive ∞-groupoids|geometric realization]] as just [recalled](#IntermezzoElementsOfHigherCohesiveGeometry) this has an essentially unique lift to _smooth cohomology_, hence to a morphism of [[moduli ∞-stacks]]

$$
  \mathbf{c}
  \;\colon\;
  \mathbf{B}G
  \to 
  \mathbf{B}^3 U(1)
$$

which, in a precise sense, is the [[Lie integration]] of the canonical 3-[[cocycle]] 

$$
  \langle -, [-,-]\rangle \;\colon\; \mathfrak{g} \to \mathbf{B}^2 \mathbb{R}
$$

in the [[Lie algebra cohomology]] of the [[Lie algebra]] $\mathfrak{g}$ of $G$ in that

$$
  \mathbf{c} \simeq \tau_1 \exp(\mu)
  \,.
$$


Moreover, this smooth universal characteristic map  has a further lift to [[differential cohomology]]

$$
  \hat \mathbf{c}
  \;\colon\;
  \mathbf{B}G_{conn}
  \to 
  \mathbf{B}^3 U(1)_{conn}
  \,.
$$

This modulates a [[circle n-bundle with connection|circle 3-bundle with connection]] -- the "[[Chern-Simons circle 3-bundle with connection]]" -- on the [[smooth infinity-groupoid|smooth]] [[moduli stack]] of smooth $G$-[[principal connections]]. 

$$
  \array{
    \mathbf{B}G_{conn}
    &\stackrel{\hat \mathbf{c}}{\to}&
    \mathbf{B}^3 U(1)_{conn} 
    \\
    \downarrow && \downarrow &&&&& \in  \mathbf{H}
    \\
    \mathbf{B}G
    &\stackrel{\mathbf{c}}{\to}&
    \mathbf{B}^3 U(1)
    \\
    && &&& \downarrow^{\mathrlap{{\vert \Pi(-)\vert}}}
    \\
    B G &\stackrel{c}{\to}& B^3 U(1) &&&&& \in L_{whe} Top
  }
$$

One finds that the [[transgression]] of this to codimension 0 is the Chern-Simons action functional discussed above. The other transgressions are

| [[dimension]] |  | [[prequantum n-bundle|prequantum (3-k)-bundle]] |  |
|---------------|--|-------------------------------------------------|--|
| $k = 0$ | [[twisted differential string structure|differential fractional first Pontryagin class]] | $\hat \mathbf{c} \;\colon\; \mathbf{B}G_{conn} \to \mathbf{B}^3 U(1)_{conn}$ |  ([FSS](#FSS))  |
| $k = 1$ | [[WZW model]] [[background gauge field|background]] [[B-field]] | $G \to [S^1, \mathbf{B}G_{conn}] \stackrel{[S^1, \hat \mathbf{c}]}{\to} [S^1, \mathbf{B}^3 U(1)_{conn}] \stackrel{\exp(2 \pi i \int_{S^1} (-))}{\to} \mathbf{B}^2 U(1)_{conn}$ |  |
| $k = 2$ | off-sheff [[prequantum bundle]] | $[\Sigma_2, \mathbf{B}G_{conn}] \stackrel{[\Sigma_2, \hat \mathbf{c}]}{\to} [\Sigma_2, \mathbf{B}^3 U(1)_{conn}] \stackrel{\exp(2 \pi i \int_{\Sigma_2} (-))}{\to} \mathbf{B} U(1)_{conn}$ | | 
| $k = 3$ | [[action functional]] | $[\Sigma_3, \mathbf{B}G_{conn}] \stackrel{[\Sigma_3, \hat \mathbf{c}]}{\to} [\Sigma_3, \mathbf{B}^3 U(1)_{conn}] \stackrel{\exp(2 \pi i \int_{\Sigma_3} (-))}{\to} U(1)$

Here the [[WZW model|WZW]] [[B-field]] is the topological part of a 2-dimensional local Lagrangian field theory called the _[[Wess-Zumino-Witten model]]_. One says that the WZW model is related by the [[holographic principle]] with [[3d Chern-Simons theory]].

If the [[gauge group]] $G$ is not simple and simply connected, then there are other canonical [[universal characteristic classes]] in $H^4(B G, \mathbb{Z})$. If these have a differential refinement, they give rise to the corresponding Chern-Simons theory.

Notably in the case that $G = U(1)$ is the [[circle group]] (hence not [[simply connected topological space|simply connected]]) there is the [[cup product]] of the universal [[first Chern class]] with itself

$$
  c_1 \cup c_1 \;\colon\; B U(1) \to B^3 U(1)
  \,.
$$

The smooth and differential refinement of the [[first Chern class]] itself $c_1 \;\colon\; B U(1) \to B U(1) \simeq K(\mathbb{Z},2) $ is tautological: this is simply the identity 

$$
  \widehat \mathbf{c}_1 \coloneqq id 
  \;\colon\;
  \mathbf{B}U(1)_{conn}
  \to 
  \mathbf{B}U(1)_{conn}
  \,.
$$

The nontrivial part is that, as one can see, the  [[cup product]] on [[differential cohomology]] refines to [[moduli ∞-stacks]] of [[circle n-bundle with connection]] as the [[∞-stackification]] of what is called the [[Beilinson-Deligne cup product]], and so we have 

$$
  \widehat \mathbf{c}_1 \cup \widehat \mathbf{c}_1
  \;\colon\;
  \mathbf{B}U(1)_{conn}
  \to
  \mathbf{B}^3 U(1)_{conn}
  \,.
$$

This is the [[extended Lagrangian]] for abelian Chern-Simons theory. On field configuration which happens to be given by a globally defined 1-form $A$ its value is 

$$
  \exp\left(
    2\pi i \int_{\Sigma_3} A \wedge d A
  \right)
  \in 
  U(1)
  \,.
$$

But now not every field configuration is necessarily given by a globally defined 1-form anymore, and more generally the action functional has a more sophisticated expression.

### 7-dimensional Chern-Simons theory as the next example
 {#7dCSTheoryAsExample}


So far we have considered general motivation for [[extended prequantum field theory]], and indication how its application to the well-known case of [[3d Chern-Simons theory]] naturally captures the characteristics of the theory. Now we consider further examples whose higher geometry has not necessarily been considered traditionally.

An immediate class of further examples is obtained by abelian [[higher Chern-Simons theory]] induced by the [[cup product]] of the [[first Chern class]] with itself

$$
  [DD_{2k} \cup DD_{2k}] \in H^{4(k+1)}(B^{2k+1} U(1), \mathbb{Z})
  \,.
$$

This has a refinement ([FSS cup](#FSSCup)) to a [[differential characteristic class]] by the 
_[[Beilinson-Deligne cup product]]_ of the [[differential characteristic class|differential refinement]] of the higher [[Dixmier-Douady class]] with itself:

$$
  \widehat \mathbf{DD}_{2k}
  \cup
  \widehat \mathbf{DD}_{2k}
  \;\colon\;
  \mathbf{B}^{2k+1} U(1)_{conn}
  \to 
  \mathbf{B}^{4k+3} U(1)_{conn}
  \,.
$$

In particular there is the abelian [[7d Chern-Simons theory]]

$$
  \widehat \mathbf{DD}_2
  \cup
  \widehat \mathbf{DD}_2
  \;\colon\;
  \mathbf{B}^3 U(1)_{conn}
  \to 
  \mathbf{B}^7 U(1)_{conn}
  \,.
$$

An argument in ([Witten 98](#AdS-CFT#Witten98)) says that this abelian 
[[7d Chern-Simons theory]] (or more precisely a [[quadratic refinement]] of it) is related to the _[[self-dual higher gauge theory]]_ sector of the [[6d (2,0)-supersymmetric QFT]] on the [[worldvolume]] of a single [[M5-brane]]_  in analogy to how [[3d Chern-Simons theory]] is related to the [[WZW model]]:

| [[schreiber:∞-Chern-Simons theory]] | $\leftarrow$[[holographic principle]] $\rightarrow$| [[schreiber:∞-Wess-Zumino-Witten theory ]] | [[Kaluza-Klein reduction]] $\to$ |   |
|--|--|--|--|--|
| [[3d Chern-Simons theory]]  | [3dCS-2dCFT](holographic+principle#3dCS-2dCFT) | [[WZW model]] | | |
| [[7d Chern-Simons theory]]  | [AdS7/CFT6 duality](AdS-CFT#AdS7CFT6) | [[6d (2,0)-supersymmetric QFT]] | | [[N=4 D=4 super Yang-Mills theory]] | 

The argument in ([Witten 98](#AdS-CFT#Witten98)) also says that in view of [AdS7/CFT6 duality](AdS-CFT#AdS7CFT6) the [[field (physics)|field]] of the 7d theory here is to be identified withe the _[[supergravity C-field]]_ in [[11-dimensional supergravity]]/[[M-theory]]. 

But the [[supergravity C-field]] is known to have moduli that are in general more complicated than just $\mathbf{B}^3 U(1)_{conn}$ (due to a [[Green-Schwarz anomaly cancellation]] mechanism in [[11-dimensional supergravity]] and a "flux quantization" condition). In ([FSS 7dCD](#FSS7dCS)) the corrected moduli are dicussed and found to involve a coupling of the abelian 7d theory with a nonabelian 7d Chern-Simons theory whose [[field (physics)|fields]] are twisted higher spin connections: "[[twisted differential string structures]]".

To see what this is, recall that [above](#CSAsArchetypicalExample) we interpreted the [[extended Lagrangian]] of [[3d Chern-Simons theory]] for a simply connected compact simple gauge group $G$ as the smooth and moreover differential refinement of the canonical [[universal characteristic class]] in $H^4(B G, \mathbb{Z})$. Specifically for $G$ the [[spin group]] this is the [[first fractional Pontryagin class]], represented by a [[characteristic map]]  

$$
  \tfrac{1}{2}p_1 \;\colon\; B Spin \to B^3 U(1)
  \,.
$$ 

This can be understood as a higher analog of the [[second Stiefel-Whitney class]] $w_2 \;\colon\; B SO \to B^2 \mathbb{Z}$ which is the universal [[obstruction]] to [[spin structure]]. We say that $\tfrac{1}{2}p_1$ is the universal [[obstruction]] to a _[[higher spin structure]]_ called _[[string structure]]_ (this and the motivation for this terminology is discussed in detail in _[geometry of physics - Fields - Examples - Fields of gravity and G-structure](geometry+pf+physics##FieldsOfGravityAndGeneralizedGeometry)_). These higher obstructions are the (dual) [[k-invariants]] of the [[Whitehead tower]] of $B O$:

[[!include higher spin structure - table]]

From the point of view of [[extended prequantum field theory]] we are to regard each horizontal map in this tower as classifying the potential underlying [[instanton sector]] of an [[extended Lagrangian]]/[[prequantum n-bundle]], and we may ask if these lift to actual extended Lagrangian.

The next step up the ladder is the universal [[second fractional Pontryagin class]]. Its [[twisted differential string structure|differential refinement]] has been constructed in ([FSS diff coc](#FiorenzaSchreiberStasheff)).

$$
  \array{
    \mathbf{B}String_{conn}
    &\stackrel{\widehat {\tfrac{1}{6}\mathbf{p}_2}}{\to}&
    \mathbf{B}^7 U(1)_{conn} 
    \\
    \downarrow && \downarrow &&&&& \in \mathbf{H}
    \\
    \mathbf{B}G
    &\stackrel{ \tfrac{1}{6}\mathbf{p}_2 }{\to}&
    \mathbf{B}^7 U(1)
    \\
    && &&& \downarrow^{\mathrlap{{\vert \Pi(-)\vert}}}
    \\
    B String &\stackrel{\tfrac{1}{6}p_2}{\to}& B^7 U(1) &&&&& \in L_{whe} Top
  }
  \,.
$$

This now defines an [[extended Lagrangian]] for a  [[7d Chern-Simons theory]] on [[String 2-group]]-[[2-connections]].  

Coming back to the above arguments about the relation of the 7d theory to a 6d theory, these suggest that the 6d theory involves  [[prequantum n-bundle|prequantum 6-bundle]]-analog of the [[WZW model|WZW 2-bundle]]. 

Indeed, the assignment of a higher Wess-Zumino-Witten-type [[prequantum n-bundle|prequantum (n-1)-bundle]] to an extended prequantum Lagrangian works very generally: the _prequantum $(n-1)$-bundle_ is the WZW-type $(n-1)$-bundle of the theory.
Its underlying $(n-1)$-bundle is simply the [[looping]] of the $n$-bundle underlying the [[extended Lagrangian]]. Specifically, the [[string 2-group]]-[[7d Chern-Simons theory]] has a WZW- prequantum 6-bundle on the [[string 2-group]] which is modulated by the [[looping]] $\Omega(\tfrac{1}{6}\mathbf{p}_2)$ of the differential characteristic map $\tfrac{1}{2}\mathbf{p}_2$

$$
  \array{
    String
    && &\stackrel{\Omega \left( \tfrac{1}{6}\mathbf{p_2}\right)}{\to}& &&
    \mathbf{B}^6 U(1)
    \\
    \downarrow
    && && && \uparrow
    \\
    String //_{Ad} String
    &
    \stackrel{\simeq}{\to}
    &
    [\mathbf{\Pi}(S^1), \mathbf{B}String]
    &
    \stackrel{[\mathbf{\Pi}(S^1), \tfrac{1}{2}\mathbf{p}_2]}{\to}
    &
    [\mathbf{\Pi}(S^1), \mathbf{B}^7 U(1)]
    &\simeq&
    \mathbf{B}^6 U(1) // \mathbf{B}^6 U(1)
  }
  \,.
$$

Here the lower factorization of this map shows canonically that this 6-bundle is [[equivariant]] with respect to the [[adjoint action|adjoint]] [[∞-action]] of the [[string 2-group]] on itself, the analog of the ordinary adjoint equivariance of the ordinary WZW 2-bundle.

Therefore in summary we find the following identifications of [[extended prequantum field theory]] with (semi-)traditional notions:

[[!include extended prequantum field theory - table]]


### $\infty$-Chern-Simons theory as the general example
 {#InfinityCSAsGeneralExample}

In the examples of [[2d Chern-Simons theory]] and [[7d Chern-Simons theory]] that we have discussed above, the fully extended Lagrangian is equivalently the [[prequantum n-bundle]] on the universal [[moduli ∞-stack]] of [[field (physics)|fields]], for $n = 3$ and $n = 7$, respectively.

But in fact this is the general situation for fully extended Lagrangians: 

if $\mathbf{Fields} \in \mathbf{H}$ is the object that serves as the [[moduli ∞-stack]] of [[field (physics)|fields]] for some $n$-dimensional [[theory (physics)|theory]] in that for any [[spacetime]]/[[worldvolume]] $\Sigma_n$ of [[dimension]] $n$ the space of fields is the [[mapping stack]] $[\Sigma_n, \mathbf{Fields}]$, then the corresponding [[prequantum n-bundle]] has to be over this object $\mathbf{Fields}$ and hence to be modulated by a map of moduli $\infty$-stacks of the form

$$
  \mathbf{L} \;\colon\;
  \mathbf{Fields}
  \to 
  \mathbf{B}^n U(1)_{conn}
$$

hence by a fully extended Lagrangian. 

Above we considered the case that $\mathbf{Fields} \simeq \mathbf{B}G_{conn}$ for a [[Lie group]] $G$ or $\mathbf{Fields} \simeq \mathbf{B}String_{conn}$ for the [[string 2-group]]. In general for $G \in Grpd(\mathbf{H})$ a [[smooth ∞-group]] an extended Lagrangian as above
encodes an [[extended prequantum field theory|extended prequantum]] _[[higher gauge theory]] of Chern-Simons type_: 

the [[curvature]] $(n+1)$-form of $\mathbf{L}$ (i.e. the [[n-plectic geometry|pre n-plectic form]] of the [[n-plectic geometry|n-plectic]] [[∞-stack]] $\mathbf{Fields}$ )

$$
  F_{\mathbf{L}}
  \;\colon\;
  \mathbf{B}G_{conn}
  \stackrel{\mathbf{L}}{\to}
  \mathbf{B}^n U(1)_{conn}
  \stackrel{F_{(-)}}{\to}
  \Omega^{n+1}_{cl}
$$

is -- by [[∞-Chern-Weil theory]] -- an [[invariant polynomial]] of the [[∞-Lie algebra]] $\mathfrak{g}$ of $G$. Accordingly, the [[action functional]]

$$
  \exp\left( 
    2 \pi i \int_{\Sigma_n} [\Sigma_n, \mathbf{L}]
  \right)
  \;\colon\;
  [\Sigma_n, \mathbf{B}G_{conn}]
  \to 
  U(1)
$$

locally takes an [[infinity-Lie algebroid-valued differential form
|L-∞ algebra valued differential form]] $A$ (the [[higher gauge fields]]) to a [[Lagrangian]] $CS(A)$ which locally is a differential form with the property that $ d CS(A) = F_A$.
This means that 
$\exp\left( 2 \pi i \int_{\Sigma_n} [\Sigma_n, \mathbf{L}] \right)$ is a [[higher gauge theory]] _of Chern-Simons type_. We say that it is an _[[schreiber:∞-Chern-Simons theory]]_.

This remains true if $\mathbf{Fields}$ is of more general form, so that fields are [[infinity-Lie algebroid-valued differential form
|L-∞ algebroid valued differential form]].

This means that fully [[extended prequantum field theory]] is considerably more restrictive than the traditional notion of [[local Lagrangian]] field theory, just as [[extended topological quantum field theory]] is much more restrictive than non-extended [[TFT]]. 

1. **fewer choices in prequantization** Traditional [[geometric quantization]] involves making considerable choices. Notably the choice of [[prequantum bundle]] lifting the [[symplectic form]]. In [[extended prequantum field theory]] the prequantum bundles in codimension 1 are constrained to all arise by [[transgression]] from a [[prequantum n-bundle]] in codimension $n$. This is a strong coherence condition that drastically reduces the available choices. 

   For instance for $G$ a compact Lie group, there is an [[isomorphism]]

   $$
     H^n(B G, \mathbb{Z})
     \simeq
     \pi_0 \mathbf{H}(\mathbf{B}G, \mathbf{B}^n U(1))
     \,.
   $$

   This means that if $H^n(B G, \mathbb{Z})$ has no [[torsion subgroup|torsion]], then there is _at most one_ extended prequantization of a given invariant polynomial.


1. **selecting physically natural theories** While the traditional formalization of [[local Lagrangian]] field theory does capture crucial aspects of those [[theories (physics)|theories]] that one is interested in in [[physics]], it still admits many "unnatural theories". The _generic_ [[local Lagrangian]] (in the sense of a horizontal form on the [[jet bundle]] of the [[field bundle]]) contains many higher order derivatives of fields, non-polynomial interactions etc., properties that the typical [[theory (physics)|theories]] of relevance in theoretical physics do no share.

The remaining question then is how accurately [[extended prequantum field theory]] constrains the space of possible [[local Lagrangians]]. In other words: which theories of interest can not be thought of as [[schreiber:∞-Chern-Simons theories]] or [[schreiber:∞-Wess-Zumino-Witten theory ]]?

As a hint to the answer of this question, here is a list of names examples of [[schreiber:∞-Chern-Simons theories]]. We discuss the items of the list in detail in the following.


* [[higher dimensional Chern-Simons theory]]

  * [[1d Chern-Simons theory]]
 
    * [[Wilson loop]]

  * [[2d Chern-Simons theory]]

    * [[Poisson sigma-model]], 

    * [[A-model]], [[B-model]] [[topological string]]

  * [[3d Chern-Simons theory]]

    * [[Chern-Simons theory]]

    * [[Dijkgraaf-Witten theory]]

    * [[Courant sigma-model]]

    * [[3d quantum gravity]]

  * [[4d Chern-Simons theory]]

    * [[Yetter model]]

    * [[BF-theory]]

  * [[5d Chern-Simons theory]]

  * [[6d Chern-Simons theory]]

  * [[7d Chern-Simons theory]]

    * topological [AdS7/CFT6](http://ncatlab.org/nlab/show/AdS-CFT#AdS7CFT6)-sector

    * [[topological M-theory]]


* [[schreiber:∞-Chern-Simons theory]]

  * [[∞-Dijkgraaf-Witten theory]]

  * [[higher dimensional Chern-Simons gravity]]

  * [[AKSZ sigma-model]]

  * [[string field theory]]

The last example here brings us back full circle to where we started this motivation with [above](#IngredientsOfFundamentalPhysics): by the central property of [[string theory]], the action functional for [[string field theory]] (or some [[KK-reduction]] thereof) contains [[Einstein-Yang-Mills theory]].

## **Fields**
 {#Fields}

In fundamental [[physics]] the basic entities that are being described by a [[physical theory]] -- its _[[kinematics|kinematical]] content_ -- are called _[[field (physics)|fields]]_; such as the _[[electromagnetic field]]_ (which we already encountered 
[above](#ElectromagneticFieldStrength)) or the field of _[[gravity]]_ (which we also briefly encountered [before](#RiemannianGeometry)). Also all _[[matter]]_ is fundamentally described by fields (which we already mentioned [above](#SpinGeometry)).

We discuss here the general notion of _[[field (physics)|physics fields]]_ in _[[prequantum field theory]], [[classical field theory]] and [[quantum field theory]].

Apart from the [[kinematics]] encoded in the nature of the [[physical fields]], a [[physical theory]] consist of a specification of the _[[dynamics]]_. Formally this is encoded by what is called a  _[[Lagrangian]]_ and induced from that an _[[action functional]]_ on the space of all field configurations. This we turn to below in _[Lagrangians and Action functionals](#LagrangiansAndActionFunctionals)_

Surveys of some aspects discussed below are also in ([FSS 12, section 5.2](#FiorenzaSatiSchreiberCSIntroAndSurvey)) and in ([S 12](#TwistedCohomologyLecture))

+-- {: bluebox}
###### Content: ######
**Fields**

1. [Model layer](#FieldsModelLayer)

   The traditional [[differential geometry]] and [[differential cohomology]] of [[physical fields]].

1. [Semantics layer](#FieldsSemanticsLayer)

   The general abstract formulation of [[physical fields]] in [[slice (infinity,1)-topos|slices]] of a [[cohesive (∞,1)-topos]].

1. [Syntax layer](#FieldsSyntaxLayer)

   Some further remarks on the above general abstract formulation in terms of [[homotopy type theory]].

=--


### Model layer
 {#FieldsModelLayer}

(...)

### Semantics layer
 {#FieldsSemanticsLayer}


We discuss the notion of [[field (physics)|field]] in physics in the general abstract context of [[(∞,1)-topos theory]].

+-- {: bluebox}
###### 

1. [Idea](#FieldsModelLayerIdea)

1. [Definition](#FieldsModLayerDefinition)

1. [Properties](#FieldsModelLayerProperties)

1. [Examples](#FieldsModelLayerExamples)

=--

#### Idea
 {#FieldsModelLayerIdea}

+-- {: bluebox}
###### 

1. [General idea of physical fields](#GeneralIdeaOfPhysicalFields)

1. [The traditional idea of field bundles and its problems](#IdeaOfFieldBundlesAndItsProblems)

1. [The solution](#FieldsModelLayerIdeaSolution)

=--

##### General idea of physical fields
 {#GeneralIdeaOfPhysicalFields}

The basic example that probably gives the whole concept its name is the [[electric field]] and the [[magnetic field]] in the [[theory (physics)|theory]] of [[electromagnetism]]: if we fix a [[coordinate chart]] of [[spacetime]], then the [[electromagnetic field]] splits into the [[electric field]] and the [[magnetic field]] which are both modeled by a _[[vector field]]_, traditionally denoted $\vec E$ and $\vec B$, respectively, on this coordinate chart. The value $\vec E(x)$ of the vector field at a given point of spacetime is a [[vector]] that expresses the magnitude and direction of the electric [[force]] that is exerted on an [[electric charge|electrically charged]] [[particle]] at $x$. 

In fact more fundamentally, if we do not specify a [[coordinate chart]], then the [[electromagnetic field]] is not in fact represented by two vector fields. Rather, its [[field strength]] is represented by a [[differential 2-form]], hence a [[tensor field]] of rank $(0,2)$, but the whole field as such is not a tensor field, but is a [[cocycle]] of degree-2 in [[ordinary differential cohomology]]: a [[circle n-bundle with connection|circle bundle with connection]].

Or for instance the field of [[gravity]] if modeled as a [[pseudo-Riemannian metric]] is a [[tensor field]] of rank $(2,0)$ -- but subject to the constraint that this be pointwise non-degenerate. More fundamentally the field of gravity is instead a [[vielbein field]].

Similar statements hold for all [[forces]] of nature, such as the force of [[gravity]] and the [[weak nuclear force]] and [[strong nuclear force]]: a configuration of these is mathematically modeled by [[connection on a bundle|connections]]. Their [[field strengths]] are rank $(0,2)$-tensor fields.

The [[electromagnetic field]] and the field of [[gravity]] are the physical fields that historically gave rise to what is now called _[[classical field theory]]_. But it turns out that fundamentally, in [[quantum physics]], also all [[matter]] in physics is constituted by fields in a similar sense. Specifically, where [[force]] fields in physics are usually [[connection on a bundle|connections on a bundle]], matter fields are [[sections]] of [[associated bundles]]. 

Field theory was originally discovered as a [[theory (physics)|theory]] of fields on _[[spacetime]]_. But also the [[physical system]] consisting of a single [[particle]] propagating in a _fixed_ [[spacetime]] $X$ is described by a field theory. In this case the field is not defined on spacetime, but on the abstract _[[worldline]]_ of the particle, say the _[[real line]]_ $\mathbb{R}$. A consifiguration of the system, namely a [[trajectory]] of the particle, is then a [[smooth function]] $\phi \;\colon\; \mathbb{R}\to X$. This function may be regarded as a _field_ on the [[worldline]] and in then called a _[[sigma-model]]_ field. The [[quantum mechanics]] of a single particle may be equivalently thought of as a [[quantum field theory]] on the 1-dimensional [[worldline]] of the particle.

This perspective generalizes. Next one can consider fields on 2-dimensional [[surfaces]] $\Sigma_2$ which again are given by maps into some [[spacetime]] $X$. The corresponding 2-dimensional [[sigma-model]] [[quantum field theory]] is then said to describe not a particle but a _[[string]]_ propagating in spacetime, defined on the _[[worldsheet]]_ $\Sigma_2$, replacing the [[worldline]] of the particle. For $\Sigma$ of dimension 3 one accordingly speaks of the _[[worldvolume]]_ of a [[membrane]] and then for $\Sigma$ of general dimension here one speaks of the _[[worldvolume]]_ of a _[[brane]]_. 

But there is no fundamental distinction between physical fields on spaces that are interpreted as [[spacetimes]] and those that are interpreted as [[worldvolumes]] of objects propagating _in_ a fixed spacetime. In general these notions mix. For instance the full description of [[relativistic particles]] and [[relativistic strings]] involves a field that is really a field of [[gravity]] on the [[worldvolume]]. Conversely, [[theory (physics)|theories]] on [[spacetimes]] that arise by [[Kaluza-Klein compactification]] of higher dimensional theories typically have "[[scalar field|scalar moduli fields]]" that used to be components of the field of [[gravity]] in higher dimensions but now after compactifications become maps into some auxiliary [[target space]], hence again _[[sigma-model]]_ fields.


##### The traditional idea of field bundles and its problems
 {#IdeaOfFieldBundlesAndItsProblems}

A traditional approach to formalizing the notion of _physical field_ is to declare that the specification of a [[theory (physics)|theory in physics]]/[[physical system]] comes with a [[fiber bundle]] $E \to X$ over the [[spacetime]]/[[worldvolume]] $X$ (or better: naturally over all spacetimes, see at _[Locality](#IdeaLocality)_ below) called the ***[[field bundle]]*** and that a field configuration $\phi$ of the system is a [[section]] 

$$
  \array{
     && E
     \\
     & {}^{\mathllap{\phi}}\nearrow & \downarrow
    \\
    X &\stackrel{=}{\to}& X
  }
$$


of this field bundle. This is for instance the basis for the theory of the [[variational bicomplex]], hence of [[BV-BRST formalism]] for expressing [[covariant phase spaces]], for standard [[multisymplectic geometry]], etc.

While this goes in the right direction, it cannot be quite the final answer, as it misses crucial properties that are demanded of a general notion of field. We now discuss these problems:

1. [Large gauge transformations](#IdeaLargeGaugeTransformations)

1. [Locality](#IdeaLocality)

1. [Spin structures and other G-structures](#IdeaSpinStructures)

1. [Background fields](#BackgroundFields)

1. [Higher gauge fields](#HigherGaugeFields)

In the course of discussing the problems we also motivate and indicate their solution by a more natural notion of field moduli in [[higher geometry]]. This is then discussed in full detail in  
_[Physical fields in higher differential geometry](#FieldsModLayerDefinition)_ below.

###### Large gauge transformations 
 {#IdeaLargeGaugeTransformations}

In [[gauge theory]] specifically but in [[physics]] generally, physical fields come equipped with a notion of which fields configurations, while nominally different, are [[equivalence|equivalent]], called _[[gauge equivalence|gauge equivalent]]_ and it is crucial to retain the information of gauge equivalences and not pass to [[equivalence classes]] of gauge equivalent fields. This means that generically for any [[physical theory]], even if all field configurations would be represented by a section of some [[field bundle]], many such sections are in fact to be regarded as being equivalent. Or more precisely, there should be a _[[groupoid]]_ or _[[∞-groupoid]]_ of field configurations of which the sections of the field bundle only form the space of [[objects]], while the [[gauge transformations]] form the [[morphisms]] and the [[higher gauge transformations]] of order $n$ form the [[n-morphisms]].

   To some extent this is dealt with in traditional [[variational calculus]]: after a choice of [[action functional]] on the space of field configurations, [[BV-BRST formalism]] spits out a [[derived L-∞ algebroid]] whose objects are field configurations, and whose 1-cells are infinitesimal invariances of the given [[action functional]]. 

   This goes in the right direction-- it is the [[Lie differentiation]] of the more encompassing [[smooth ∞-groupoid]] of fields and gauge transformations -- but has several problems, the main one being that this does now know about the [[large gauge transformations]], those which are not connected to the identity (because it only sees infinitesimal data). 
These are important in the full quantum theory. 

Famous examples of the importance of [[large gauge transformations]] appear in

* [[2d CFT]], for which all standard theory would break down if the global [[conformal transformations]] were not considered as gauge transformations.


###### Locality 
 {#IdeaLocality}

Fields defined as sections of field bundles cannot capture gauge phenomena in a _loca_l way, as is necessary for a manifestly local formulation such in [[extended prequantum field theory]], [[extended quantum field theory]] (sometimes called the "multi-tiered" formulation).

   Spcefically, in [[Yang-Mills theory]] for [[gauge group]] $G$, a field configuration -- a _[[gauge field]] configuration_ -- is a combination of an [[instanton sector]] -- modeled by the [[equivalence class]] of a $G$-[[principal bundle]] $P$ -- and the "[[gauge potential]]", modeled by a [[connection on a bundle|connection on this bundle]] (see below at _[Gauge fields](#GaugeFields)_ for details).  There is a [[fiber bundle]] $E(P) \to X$ such that its [[sections]] are precisely the [[connection on a bundle|connections]] on $P \to X$, and so $\coprod_{c} E(P_c) \to X$, where $c$ ranges over the instanton sectors, is a field bundle for Yang-Mills fields on $X$. 

   But this construction is not local: if we consider this assignment of field bundles to all suitable manifolds $X$, and if $U \to X$ is a cover of $X$, then we cannot in general obtain the field bundle on $X$ by gluing the field bundle on the cover. This is because _locally_ every $G$-[[principal bundle]] has trivial class, so that locally there is always only a single (the trivial) instanton sector. 

This failure of locality is often not recognized in the literature, since many if not most descriptions of physics restrict to trivial spacetime topology and/or restrict to [[perturbation theory]] only. A formulation accurate and encompassing enough to see this issue is _[[AQFT on curved spacetimes]]_. A reference that explicitly runs into this non-locality issue of the field bundle in gauge theory in this context is ([Benini-Dappiaggi-Schenkel 13](field+bundle#BDS)): the authors define a [[functor]] from [[spacetimes]] equipped with a $G$-[[principal bundle]] that assigns the [[algebras of observables]] of the corresponding [[Yang-Mills fields]] built from the field bundle of connections on the given principal bundles; and they observe that the result fails to be a [[local net]] in that the inclusion of observables of a smaller spacetime into a larger patch may fail the isotony axiom ([BDS, remark 5.6](field+bundle#BDS)). The authors then try to circumvent this by restricting to trivial instanton sectors.

Notice that instanton sectors is a non-negligible phenomenon. For instance the very [[vacuum]] in the [[standard model of particle physics]] is a [[superposition]] of all possible instanton sectors (see at _[[instanton in QCD]]_ for more on this).  And there are field theories where the fields consist entirely of "[[instanton sectors]]" and where there is no infinitesimal information about the gauge group at all: these are theories whose gauge group is a [[discrete group]], which includes notably [[Dijkgraaf-Witten theory]] and its higher analogy such as the [[Yetter model]]. This means that for these [[theory (physics)|theories]] a local field bundle formalism can see nothing of the actual fields and also traditional tools applied to a global field bundle (such as traditional [[BV-BRST formalism]]) see nothing of the actual fields. All this is fixed by the formulation that we discuss [below](#Definition).


   But this example already points to the general nature of the problem with field bundles, and also to its solution: while the [[instanton]]-component of [[Yang-Mills fields]] are not section of a bundle, they famously are sections of a _[[stack]]_ -- the "[[moduli stack]] $\mathbf{B}G$ of $G$-principal bundles", an object in [[higher geometry]].

   The problem with the locality of the [[field bundle]] for [[Yang-Mills theory]] is solved by passing from [[fiber bundles]] to [[fiber ∞-bundles]]: in the [[smooth ∞-groupoid|higher differential geometry]] there is an object $\mathbf{B}G_{conn}$  -- the [[moduli stack]] of $G$-[[principal connections]] (being the [[stackification]] of the [[groupoid of Lie algebra-valued forms]]) such that maps $X \to \mathbf{B}G_{conn}$ are equivalent to Yang-Mills fields on $X$ (even including their [[gauge transformations]]). This means that if we allow field bundles in higher geometry -- [[fiber ∞-bundles]], then that for Yang-Mills theory over $X$ is even a trivial field bundle, namely the [[projection]]

   $$
     X \times \mathbf{B}G_{conn} \to X
   $$

out of the [[product]] of [[spacetime]] with the [[moduli stack]] of fields.

   This is a differential refinement of what is called the trivial _$G$-[[gerbe]]_ on $X$, which is 

   $$
     X \times \mathbf{B}G \to X
   $$

   and hence the "field bundle for instanton sectors" of Yang-Mills fields.

   In summary: there cannot be a [[fiber bundle]] such that its [[sheaf]] of [[local sections]] is the sheaf of configurations of the Yang-Mills field. But there is a [[fiber infinity-bundle|fiber 2-bundle]] whose [[stack]] of sections is the stack of configurations of the Yang-Mills field.


   Judging from these examples one might be tempted to guess that the notion of field [[fiber bundle]] should simply be replaced by that of field [[fiber ∞-bundle]]. But in fact what the example rather suggests is that what matters directly is the [[moduli stack]] $\mathbf{Fields}$ of fields, which for $G$-[[Yang-Mills theory]] is simply

   $$
     \mathbf{Fields} = \mathbf{B}G_{conn}
     \,.
   $$

   This perspective, which we describe in detail [below](#Definition) also has the pleasant effect that it drastically simplifies and unifies notions of quantum field theory, for this says equivalently that if only we allow spaces in [[higher geometry]], then [[Yang-Mills theory]] is a _[[sigma-model]]_ quantum field theory: one whose fields are simply maps to a given [[target space]], only that this target space here is a [[stack]].

   But there are more advantages, slightly less obvious. These we come to in the following points.


###### Spin-structures and other $G$-structures
 {#IdeaSpinStructures}

Some fields in physics are (or involve) choices of _[[G-structure]]_ in the sense of [[reduction and lift of structure groups]]. Well-known examples include the choice of _[[orientation]]_ and of _[[Spin structure]]_ in field theories with [[fermion]] fields (discussed in detail in _[Fermions](#Fermions)_ below). Often in the literature the choice of [[orientation]] and [[Spin structure]] is treated as an external parameter, but detailed analysis at least in low-dimensional examples shows that the in the full theory this is really a field configuration. For instance in [[path integral]] [[quantization]] for theories with fermions, part of the integral over all field configurations is a sum over Spin structures.

Now, a spin structure _is_ equivalently a section of something, but again not of a [[principal bundle]], but of an analog in [[higher geometry]], a [[principal 2-bundle]]. 

To see how this works, first recall the case of orientations, whose description as sections of the [[orientation bundle]] is familiar.

For a [[spacetime]] represented by a [[smooth manifold]] $X$ of [[dimension]] $n$, let 

$$
  \tau_X \;\colon\; X \to \mathbf{B}GL(n)
$$ 

be the map that modulates its [[tangent bundle]] (discussed at _[geometry of physics - tangent bundle](geometry of physics#TangentBundle)_). Consider then the following diagram, which shows lifts of this map to the  [[classifying spaces]]/[[moduli stacks]] for various other groups (this is the _[[Whitehead tower]]_ of $\mathbf{B}O(n)$):

$$
  \array{
    && \vdots
    \\
    && \downarrow
    \\
    && \mathbf{B}Spin(n) &\stackrel{\tfrac{1}{2}\mathbf{p}_1}{\to}& \mathbf{B}^3 U(1)
    \\
    &\mathllap{s_X}\nearrow& \downarrow
    \\
    && \mathbf{B}SO(n) &\stackrel{\mathbf{w}_2}{\to}& \mathbf{B}^2 \mathbb{Z}_2
    \\
    &{}^{\mathllap{o_X}}\nearrow& \downarrow
    \\
    X & \stackrel{e_X}{\to}& \mathbf{B}O(n) &\stackrel{\mathbf{w}_1}{\to}& \mathbf{B}\mathbb{Z}_2
    \\
    &{}_{\mathrlap{\tau_X}} \searrow& \downarrow
    \\
    && \mathbf{B}GL(n)
  }
$$

A lift of the tangent bundle map $\tau_X$ to a map $e_X \colon X \to \mathbf{B}O(n)$ as indicated is a choice of [[orthogonal structure]] (a [[vielbein field]], discussed in detail below in _[Ordinary gravity](#OrdinaryGravity)_). For the present discussion asssume that this is given.


The a further lift to $o_X : X \to \mathbf{B}SO(n)$ is a choice of [[orientation]], and finally a lift to $s_X : X \to \mathbf{B}Spin(n)$ is a choice of [[spin structure]].

Now, every hook-shaped sub-[[diagram]] in the above of the form

$$
  \array{
    \mathbf{B}\hat G
    \\
    \downarrow
    \\
    \mathbf{B}G &\stackrel{\mathbf{c}}{\to}& \mathbf{B}^n A
  }
$$

is a [[homotopy fiber sequence]]. By the [[universal property]] of the [[homotopy pullback]] this means that the "space" -- really: _[[homotopy type]]_ or just _[[type]]_, for short -- of lifts of a given map $X \to \mathbf{B}G$ to a map $X \to \mathbf{B}\hat G$ is equivalently the type of trivializations of the [[composition|composite]] $X \to \mathbf{B}G \stackrel{\mathbf{c}}{\to} \mathbf{B}^n A$. 

Now if we have an [[orthogonal structure]] $e_X : X \to \mathbf{B}O(n)$ given, then this composite map according to the above diagram is 

$$
  \mathbf{w}_1(e_X)
  \;\colon\;
  X \to \mathbf{B}\mathbb{Z}_2
  \,.
$$

This represents the [[first Stiefel-Whitney class]] $[w_1(\tau_X)] \in H^1(X, \mathbb{Z}_2)$ of $\tau_X$, and it classifies a $\mathbb{Z}_2$-[[principal bundle]], hence a [[double cover]] $\hat X \to X$ and this is precisely the [[orientation bundle]] of $X$. Sections of this bundle are choices of [[orientation]] on $X$, hence are "orientation-structure fields".

Assume then such orientation field $o_X$ is given.
Then in the next step the relevant composite map is

$$
  \mathbf{w}_2(o_X) \;\colon\; X \to \mathbf{B}^2 \mathbb{Z}_2
  \,.
$$

This now represents the [[second Stiefel-Whitney class]] $[w_2(\tau_X)] \in H^2(X, \mathbb{Z}_2)$ of $X$ and classifies a $(\mathbf{B}\mathbb{Z}_2)$-[[principal 2-bundle]] 

$$
  \array{
    \mathbf{B}\mathbb{Z}_2 &\to& P
    \\
    && \downarrow 
    \\
    && X
  }
  \,.
$$

This is sometimes called the _$Spin$-[[lifting bundle gerbe]]_ of $o_X$.
A choice of [[Spin structure]] is a choice of section of this 2-bundle.
Hence spin structures are parts of fields in physics which are not sections of a field 1-bundle. Again, this is faithfully captured only in [[higher geometry]].

This is only the most famous phenomenon in a large class of similar structures of fields in field theory. Notably in higher dimensional [[supergravity]] and in [[string theory]] there are fields which are ever higher lifts through this [[Whitehead tower]] -- [[higher spin structures]], such as [[String structures]] and [[Fivebrane structures]] in the next two steps. Accordingly, these are fields which are equivalently sections of [[principal 3-bundles]] (the "[[Chern-Simons circle 3-bundle]]") and [[principal infinity-bundle|principal 7-bundles]] (the "[[Chern-Simons circle 7-bundle]]").

###### Background fields
 {#BackgroundFields}

Comparison of the above discussions under _[Locality](#IdeaLocality)_ and _[Spin structures](#IdeaSpinStructures)_  shows that there we had a higher-geometric field bundle of [[Yang-Mills fields]] which was hower "trivial" in the sense that it was a projection out of the [[product]] of [[spacetime]] with a [[moduli stack]], so that a field configuration was equivalently of [[sigma-model]]-type, namely simply a map $\phi \colon : X \to \mathbf{B}G_{conn}$; whereas here the "spin-lifting 2-bundles" and its higher analogs are, in general, not of this product form, hence "Spin structure"-fields, at least superficially do not seem to be of [[sigma-model]]-type, even in [[higher geometry]].

But a closer inspection shows that in fact both situations are entirely analogous -- once we realize that here these Spin-structure fields are not really defined just on $X$, but on $X$ _equipped with its orientation_ $o_X$. Since, by the same logic as above, also the orientation is a "field", we may call it a ***[[background field]]***. It serves as "background" over which spin structure fields can be considered.

In [[higher geometry]] incarnated naturally as [[(∞,1)-topos theory|higher topos theory]], this state of affairs is naturally modeled and indeed yields again a _moduli stack of spin structure fields_ and makes spin-structures be [[sigma-model]]-type fields, as follows:

the natural way to regard both $X$ as well as its orientation structure $o_X$ as a single object is to regard the map $X \stackrel{o_X}{\to} \mathbf{B}SO(n)$ as an object in the [[slice (∞,1)-topos|slice (2,1)-topos]] $\mathbf{H}_{/\mathbf{B}SO(n)}$. In here an [[object]] is a map of [[stacks]] into $\mathbf{B}SO(n)$, and a morphism is map of the domains of these maps together with a [[homotopy]] filling the evident triangle [[diagram]]. Notably a lift of the orientation structure $o_X$ to a spin structure $s_X$ as above, hence a diagram of the form

$$
  \array{
    X &&\stackrel{s_X}{\to}&& \mathbf{B}Spin(n)
    \\
    & {}_{\mathllap{o_X}}\searrow &\swArrow_\simeq& \swarrow_{\mathrlap{\mathbf{SpinStruc}_n}}
    \\
    && \mathbf{B}O(n)
  }
$$ 

is equivalently a map 

$$
  o_X \to \mathbf{SpinStruc}_n
$$

in $\mathbf{H}_{/\mathbf{B}SO(n)}$. This is again of the same simple form of the Yang-Mills fields on $X$, which are maps

$$
  X \to \mathbf{B}G_{conn}
  \,,
$$

but in the collection of stacks $\mathbf{H}$ itself, not in a [[slice (infinity,1)-topos|slice]].

The slice here encodes the presence of [[background fields]] -- namely orientations in this case -- whose [[moduli stack]] in turn is, in this case, $\mathbf{B}SO(n)$. 

Notice that also the field of [[gravity]] has a background field in this precise sense: as metioned above, a gravitational field configuration is a lift of $\tau_X$ through $\mathbf{B}O(n) \stackrel{\mathbf{OrthStruc}_n}{\to} \mathbf{B}GL(n)$, hence a map

$$
  \tau_X \to \mathbf{OrthStruc}_n
$$

in the slice $\mathbf{H}_{/\mathbf{B}GL(n)}$. (Discussed in detail in _[Ordinary gravity](#OrdinaryGravity)_ below.) Hence also [[gravity]] becomes a [[sigma-model]]-type field theory in [[higher geometry]]. Notice that here it is [[smooth structure]] on $X$, as embodied in $\tau_X$, which is the background.

Now, at least for the field of gravity one can of course emulate the fields also by sections of a field bundle (while already for the second next step in the Whitehead tower, Spin structures, this is no longer the case, as we have seen). But even so, the field bundle formalism clearly misses then the relation between fields and background fields.

In particular for two reasons

1. Typically the presence of background fields indicates that in a more comprehensive discussion background fields are also fields that vary;

1. Often background fields on one space affect fields on _another_ space.

An archetypical example for both these effects combined is 3d [[Chern-Simons theory]] with a compact, simple and simply connected [[gauge group]] $G$ in the presence of [[Wilson lines]]. This is a [[theory (physics)|theory]] on 3-dimensional [[spacetime]]/[[worldvolume]] $\Sigma$ whose fields are $G$-[[gauge fields]] as for [[Yang-Mills theory]] above, hence given by maps $\Phi \colon \Sigma \to \mathbf{B}G_{conn}$. At the same time, this theory has a "coupling" to a 1-dimensional [[theory (physics)|theory]] which describes [[particles]] propagating around [[knots]] $C : S^1 \to \Sigma$ in $\Sigma$ for which the restriction $\Phi|_C$ serves as the [[background gauge field]]. Specifically, a field configuration of this 1-dimensional theory is equivalently a map in the slice $\mathbf{H}_{/\mathbf{B}G_{conn}}$ which in $\mathbf{H}$ is given by a diagram of the form

$$
  \array{
   S^1 &&\to&& \Omega^1(-,\mathfrak{g}//T)
   \\
   & {}_{\mathllap{C}}\searrow &\swArrow& \swarrow_{\mathrlap{\mathbf{OrbitStruct}}}
   \\
   && \mathbf{B}G_{conn} 
  }
$$ 

for some map on the right which we discuss in detail below in _[Chern-Simons fields with Wilson line fields](#ChernSimonsWithWilsonLines)_.

Here considering just these fields in the background of a fixed $\Phi|_C$ produced a 1-dimensional [[quantum field theory]] whose [[partition function]] is that "[[Wilson loop]]" observable of $\Phi|_C$. But this is not considered in isolation. The whole point of the relation of [[Chern-Simons theory]] to the [[Jones polynomial]] [[knot invariant]] of the [[knot]] $C$ is that one consider also $\Phi$ as a dynamical field, not as a fixed background. Indeed, in the full theory of Chern-Simons with Wilson loops that includes both the fields on $\Sigma$ as well as those on the knot, a field configuration is the diagram as above but regarded as the square 

$$
  \array{
    S^1 &\to& \Omega^1(-,\mathfrak{g})//T
    \\
    {}^{\mathllap{C}}\downarrow 
    &\swArrow& \downarrow^{\mathrlap{\mathbf{OrbitStruc}}}
    \\
    \Sigma &\stackrel{\Phi}{\to}& \mathbf{B}G_{conn}
  }
  \,,
$$

hence, again, a single map

$$
  C \to \mathbf{OrbiStruc}
$$

but now in the [[arrow (∞,1)-topos]] $\mathbf{H}^{(\Delta^1)}$.

This subtle interplay of "bulk fields" and "[[QFT with defects|defect fields]]" which is here captured most naturally in terms of [[higher geometry]] cannot really be expressed accurately just in terms of field bundles.


###### Higher gauge fields
 {#HigherGaugeFields}

Above we have seen the generalization of field bundles to [[higher geometry]] already for traditional notions such as Yang-Mills fields and Spin-structures. But many [[theory (physics)|theories]] considered in
in theoretical physics have fields that are more "explicitly" entities in [[higher geometry]].

For instance the higher analog of the [[electromagnetic field]] which is called the _[[B-field]]_ or _[[Kalb-Ramond field]]_ is a [[circle n-bundle with connection|2-connection]] on a [[principal 2-bundle]]. There is no way to faithfully encode this as a section of any ordinary [[fiber bundle]]. It follows that for instance also the [magnetic charge anomaly](magnetic+charge#MagneticChargeAnomaly) (as discussed there) has no accurate description in terms of field bundles. Next the [[supergravity C-field]] is a [[circle n-bundle with connection|3-connection]] on a [[principal 3-bundle]], and so on.

There is a wide variety of [[higher dimensional Chern-Simons theories]] whose fields are such [[higher gauge fields]]. In some traditional literature one sees parts of this theory be discussed by standard [[BV-BRST formalism]] applied to [[field bundles]], namely by ignoring the non-trivial [[instanton sectors]] and pretending that a field configuration for these [[connection on an ∞-bundle|∞-connections]] are given by globally dedined [[differential forms]]. In some special cases (for instance for [[spacetimes]]/[[worldvolumes]] of very special topology or low [[dimension]) this can be sufficient to capture everything, but in general (for instance for $U(1)$-[[higher dimensional Chern-Simons theory]] and its [[holographic principle|holographically dual]] [[self-dual higher gauge theory]]) it is not.

##### The solution: Field $\infty$-bundles and moduli $\infty$-stacks of fields
 {#FieldsModelLayerIdeaSolution}

By the [above](#IdeaOfFieldBundlesAndItsProblems), defining a physical field to be a section of some bundle goes in the right direction, but misses crucial aspects of physical fields. These problems are fixed by passing to [[higher geometry]].

Below in _[Definition](#Definition)_ we discuss a natural unified formulation of the notion of physical field in terms of [[higher geometry]] (the central definition being def. \ref{FieldsInAnActionFunctional} ) and then we spell out many [Examples](#Examples).

This definition turns out to be equivalent, at least under mild conditions, to a formulation where fields are sections of an [[associated ∞-bundle]], hence a "field $\infty$-bundle". This we discuss in _[Properties -- Relation of fields to sections of ∞-bundles](#RelationOfFieldsToSections)_. But this is just one of several equivalent perspectives on physical fields, and not always the most transparent one. In fact, sections of higher associated bundles are best known in the literature on [[twisted cohomology]] and indeed one equivalent characterization of fields is as [[cocycles]] in [[twisted cohomology]] in the general sense of [[cohomology]] in an [[(∞,1)-topos]]. This we discuss below in _[Relation to twisted cohomology](#RelationToTwistedCohomology)_.

In summary we find and discuss that

| fields | $\simeq$ |  [[twisted cohomology|twisted]] [[relative cohomology|relative]] [[cohesion|cohesive]] [[cocycles]] |
|--|--|--|



#### Definition: Physical fields in higher differential geometry
 {#FieldsModLayerDefinition}


We give a general abstract definition of physical fields in 

* _[Physical fields](#DefinitionPhysicalField)_

Then we consider some general abstract operations on fields in 

* _[Restriction and pullback of fields](#RestrictionAndPullback)_

Finally we discuss the generalization of the notion

* _[Boundary and defect fields](#BoundaryAndDefectFields).



##### Physical fields
 {#DefinitionPhysicalField}

A notion of _field_ in physics is part of a specification of _[[theory (physics)|physical theory]]_ or _[[model (physics)|physical model]]_. We consider specifically the framework of [[prequantum field theory]]. Here a [[theory (physics)|theory]]/[[model (physics)|model]] is specified by (or at least comes with) an _[[action functional]]_. The _field_ content of the theory is part of the specification of the [[domain]] of the action functional. Therefore in def. \ref{FieldsInAnActionFunctional} below we define _action functionals_ and the fields relative to this notion.

We work in the following context.

+-- {: .num_defn}
###### Context

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]]. For many of the examples below it is furthermore assumed that $\mathbf{H}$ is equipped with [[differential cohesion]]. This implies in particular that there is a notion of [[smooth manifold]] [[internalization|internal]] to $\mathbf{H}$.

Fix $\mathbb{G} \in Grp(\mathbf{H})$ a [[group object in an (∞,1)-category|group object]] in $\mathbf{H}$, hence a cohesive [[∞-group]].

=--



For the main definition below we need the following basic notation.

+-- {: .num_defn}
###### Definition

For $B \in \mathbf{H}$ any [[object]], and $X,A \in \mathbf{H}_{/B}$ two objects in the [[slice (∞,1)-topos]], write

$$
  [X,A]_{\mathbf{H}}
  \coloneqq
  \underset{B}{\prod} [X,A]
  \in \mathbf{H}
$$

for the $\mathbf{H}$-valued [[hom object]] between $X$ and $A$: the [[dependent product]] over $B \to *$ of the [[internal hom]] $[X, A] \in \mathbf{H}_{/B}$.

=--


The following defines the notion of _[[action functional]]_ and as part of the data it defines the notion of _physical field_.

+-- {: .num_defn #FieldsInAnActionFunctional}
###### Definition

Given an [[object]] $\mathbf{BgFields} \in \mathbf{H}$ and 
given two objects, to be denoted $\Phi_X, \mathbf{Fields}  \in \mathbf{H}_{/B}$, in the [[slice (∞,1)-topos|slice]] over $\mathbf{BgFields}$,
then an **[[action functional]]** in ($\mathbf{H}, \mathbb{G})$ "on fields on $X$" is a [[morphism]]

$$
  S \;\colon\; [\Phi_X, \mathbf{Fields}]_{\mathbf{H}} \to \mathbb{G}
  \,.
$$

In this context we say that

* the [[dependent sum]] $X \coloneqq \underset{\mathbf{BgField}}{\sum} \Phi_X$ is the **[[worldvolume]]** or **[[spacetime]]**;

* the morphism $\Phi_X \;\colon\; X \to \mathbf{BgFields}$ is the **[[background field]]**;

* the object $\mathbf{Fields}$ is the **[[moduli ∞-stack]] of fields**;

* the [[elements]] of $[\Phi_X,\mathbf{Fields}]_{\mathbf{H}}$, hence (see prop. \ref{GlobalPointsOfModuliOfFields} below) the morphisms

  $$
    \phi \;\colon\; \Phi_X \to \mathbf{Fields}
  $$

  in $\mathbf{H}_{/\mathbf{BgFields}}$, hence the [[diagrams]]

  $$
    \array{
       X &&\stackrel{\phi}{\to}&& \underset{\mathbf{BgFields}}{\sum} \mathbf{Fields}
       \\
       & {}_{\mathllap{\Phi_X}}\searrow 
       &\swArrow& 
       \swarrow_{\mathrlap{\mathbf{Fields}}}
       \\
       && \mathbf{BgFields}
    }
  $$

  in $\mathbf{H}$, are the **fields** on $X$;

* a **[[gauge transformation]]** is a [[homotopy]] in $[\Phi_X, \mathbf{Fields}]_{\mathbf{H}}$, hence a

  $$
    \phi \Rightarrow \phi'
  $$

* a **[[higher gauge transformation]]** is a [[higher homotopy]] in $[\Phi_X, \mathbf{Fields}]_{\mathbf{H}}$.


=--

+-- {: .num_remark}
###### Remark

Definition \ref{FieldsInAnActionFunctional} provides a unified perspective on fields from several perspectives. 

On the one hand, it almost explicitly says that in [[higher geometry]] all fields are "[[sigma-model]] fields" (see below at _[Examples -- Scalar and Sigma-model fields](#SclarModuliFields)_): if we regard the [[moduli ∞-stack]] $\mathbf{Fields}$ as the _[[target space]]_ then fields are simply maps from their domain (when regarded as [[spacetime]] _and_ [[background field]]) to this target space.

On the other hand, we see below in _[Relation to sections of ∞-bundles](#RelationOfFieldsToSections)_ that from another perspective def. \ref{FieldsInAnActionFunctional} says that all fields are [[sections]] of an [[associated ∞-bundle]] to an  $\infty$-bundle modulated by the background fields. This means that in [[higher geometry]] all fields are "[[matter]] fields" (see below at _[Matter fields](#MatterFields)_) [[charge (physics)|charged]] under the [[background gauge field]].

Finally, we see below in  _[Relation to twisted cohomology](#RelationToTwistedCohomology)_ that from yet another perspective def. \ref{FieldsInAnActionFunctional} says that fields are equivalently [[cocycles]] in general [[twisted cohomology]]. This perspective is traditionally known for certain examples (see _[Examples -- Chan-Paton gauge fields](#ChanPatonGaugeFields)_ below), but we see below that it is useful in its full generality. For instance the field of [[gravity]] is in a precise sense a 0-cocycle with coefficients in the [[coset space]] $GL(n)/O(n)$ that is twisted by the [[tangent bundle]] of spacetime (which exhibits the background gauge structure for [[gravity]]: the [[smooth structure]] of [[spacetime]]). An inkling of this perspective is certainly visible in the traditional literature, notably in the generalization to [[type II geometry]] and [[T-duality]], and here we see how this is a precise mechanism on the same conceptual footing with the twisted K-theory seen over D-branes.

=--


##### Restriction and pullback of physical fields
 {#RestrictionAndPullback}

It is familiar from basic examples that not every type of physical field on a [[spacetime]]/[[worldvolume]] $X$ can be pulled back (in the sense of pullback of functions) along any [[smooth function]] $f \;\colon\;Y \to X$. For instance the field of [[gravity]], a [[vielbein field]] or [[pseudo-Riemannian metric|pseudo]]-[[Riemannian metric]], discussed below in _[Ordinary graviry](#OrdinaryGravity)_ may be pulled back only along [[local diffeomorphisms]]. More generally, one needs other [[properties]] on $f$ to pull back a given field and in fact in general one needs [[extra structure]]. 

In view of def. \ref{FieldsInAnActionFunctional} above this is immediate: by that definition a field on $X$ in general does not just depend on $X$, but in fact also on the background field structure denoted $\Phi_X$. Accordingly, it can be pulled back only along maps that also carry this background field structure along.

+-- {: .num_remark #PullbackAlongGeneralizedLocalDiffeomorphisms}
###### Remark

Since by def. \ref{FieldsInAnActionFunctional} a physical field is a map $\phi \colon \Phi_X \to \mathbf{Fields}$ in 
$\mathbf{H}_{/\mathbf{BgFields}}$, it may be "pulled back" along maps  of [[spacetime]]/[[worldvolume]] $f \colon Y \to X$ when these are extended to maps $\Phi_Y \to \Phi_X$ in $\mathbf{H}_{/\mathbf{BgFields}}$ of the [[background fields]], hence to [[diagrams]] in $\mathbf{H}$ of the form

$$
  \array{
    Y &&\stackrel{f}{\to}&& X
    \\
    & {}_{\mathllap{\Phi_Y}}\searrow &\swArrow_{\kappa}& \swarrow_{\mathrlap{Phi_X}}
    \\
    && 
    \mathbf{BgFields}
  }
  \,,
$$

hence maps $f : X \to Y$ equipped with a choice of [[equivalence]] 

$$
  \kappa ;\colon\; f^*\Phi_X \simeq \Phi_Y 
$$

between the [[background fields]].

=--

In standard _[Examples](#Examples)_ discussed below we see that this is a familar fact. For instance applied to the field of gravity (see _[Gravity](#OrdinaryGravity)_ below) it says that the gravitational field can be pulled back precisely along [[local diffeomorphisms]], or that spin structures on oriented manifolds (see _[Spin structures](#SpinStructures)_ below) can be pulled back along orientation-preserving maps. Or : for [[Chan-Paton gauge fields]] on [[D-branes]] (see _[Chan-Paton gauge fields](#ChanPatonGaugeFields)_) it reproduces the familiar gauge relation for the [[B-field]] on D-branes known in [[string theory]], which is already less trivial. But the statement applies in full generality.

##### Boundary and defect fields
 {#BoundaryAndDefectFields}

In def. \ref{FieldsInAnActionFunctional} the [[background field]] $\Phi_X$ is a fixed datum of the domain ([[spacetime]]/[[worldvolume]]) on which the physical fields are defined. In some [[model (in theoretical physics)|models]] and for some of the fields this is precisely what one needs, but in other models one may need to be able to also regard the background fields as dynamical fields and to be able to switch between these perspectives, for instance to pass to a setup where what used to be a configuration of some field is now taken to be a fixed background field for the remaining fields. We now discuss how this more general setup is naturally formulated as a generalization of def. \ref{FieldsInAnActionFunctional}.


For $\mathbf{H}$ an [[(∞,1)-topos]] and $\mathbf{Fields} \colon \underset{\mathbf{BgFields}}{\sum} \mathbf{Fields} \to \mathbf{BgFields}$ a morphism in $\mathbf{H}$, we may consider this also as an object in the [[arrow (∞,1)-topos]] $\mathbf{H}^{(\Delta^1)}$ (the [[(∞,1)-functor (∞,1)-category]] from the [[interval category]]/1-[[simplex]] to $\mathbf{H}$).

A generic object in $\mathbf{H}^{(\Delta^1)}$ here is a morphism $\iota_X$ in $\mathbf{H}$. When we think of this as a domain on which to define fields we will write this

$$
  \iota_X 
    \;\colon\;
  X_{def}
  \to 
  X_{bulk}
$$

where the subscripts are for "bulk" and for "defect" (as in _[[QFT with defects]]_). A field in $\mathbf{H}^{(\Delta^1)}$ which is given by a map

$$
  \phi 
   \;\colon\;
  \iota_X \to \mathbf{Fields}
$$

in $\mathbf{H}^{(\Delta^1)}$ is equivalently a [[diagram]] of the form

$$
  \array{
    X_{def} &\stackrel{\phi_{def}}{\to}& \mathbf{Fields}_{def}
    \\
    {}^{\mathllap{\iota_X}}\downarrow 
    &\swArrow& 
    \downarrow^{\mathrlap{\mathbf{Fields}}}
    \\
    X_{bulk} &\stackrel{\phi_{bulk}}{\to}& \mathbf{Fields}_{bulk}
  }
$$

in $\mathbf{H}$.

This we interpret as a configuration consisting of 

1. a bulk field configuration $\phi_{bulk}$ 

1. a defect field configuration $\phi_{def}$, 

1. a [[gauge transformation]] that relates the restriction (or more generally: pullback to $X_{def}$) of the bulk field to the embedding (or more generally: push-forward) of the defect field into the bulk field configuration on the defect.

+-- {: .num_remark }
###### Remark

If $\phi_{bulk}$ is regarded as fixed, then this is equivalently a field configuration as in def. \ref{FieldsInAnActionFunctional} defined on $X_{def}$ and for background field the composite 

$$
  \Phi_{X_{def}}
  \coloneqq
  \iota_X^* \phi_{bulk}
  \;\colon\;
  X_{def} \stackrel{\iota_X}{\to}
  X \stackrel{\phi_{bulk}}{\to}
  \mathbf{Fields}_{bulk}
  \,.
$$ 

=--

This "fixing of bulk fields to background fields for defect fields" we discuss in more detail below in _[Properties -- Moduli stacks of fields](#ModuliStacksOfFields)_.


We formalize the moduli $\infty$-stack of all bulk and boundary fields as follows

+-- {: .num_defn }
###### Definition

Write

$$
  \mathbf{H}^{(\Delta^1)}
  \stackrel{\overset{Disc_{\mathbf{H}}}{\leftarrow}}{\underset{\Gamma_{\mathbf{H}}}{\to}}
  \mathbf{H}
$$

for the canonical [[geometric morphism]].

=--

+-- {: .num_defn #ModuliOfBulkAndBoundaryFields}
###### Definition

For $\iota_X ;\colon\; X_{def} \to X_{bulk}$ and $\mathbf{Fields} \;\colon\; \mathbf{Fields}_{def} \to \mathbf{Fields}_{bulk}$ morphisms in $\mathbf{H}$, we say that

$$
  [\iota_X, \mathbf{Fields}]_{\mathbf{H}}
  \coloneqq
  \Gamma_{\mathbf{H}}[\iota_X, \mathbf{Fields}]
  \;\;
  \in \mathbf{H}
$$

is the [[moduli ∞-stack]] of bulk and boundary fields on $\iota_X$.

=--


Several examples of this are discussed below.



#### Properties
 {#FieldsModelLayerProperties}


The definition of fields in def. \ref{FieldsInAnActionFunctional} is in fact the central part of a general theory of _[[cohomology]]_ and _[[principal ∞-bundles]]_ in [[higher geometry]]/[[(∞,1)-topos theory]] and various insights into [[prequantum field theory]] follow by making this perspective explicit.  This is what we do here.

1. [Moduli ∞-stacks of fields](#ModuliStacksOfFields)

1. [Relation of fields to sections of ∞-bundles](#RelationOfFieldsToSections)

1. [Relation of fields to twisted cohomology](#RelationToTwistedCohomology)

1. [Relation of fields to relative cohomology](#RelationToRelativeCohomology)

The central results that underly these identifications are in ([NSS](#NSS)), also [dcct, section 3.6.10, 3.6.11, 3.6.12, 3.6.15](#dcct).

##### Moduli $\infty$-stacks of fields
 {#ModuliStacksOfFields}

The object $[\Phi_X, \mathbf{Fields}]_{\mathbf{H}} \in \mathbf{H}$
of def. \ref{FieldsInAnActionFunctional} we may call the 
[[moduli ∞-stack]] of fields. Here we discuss various properties of this object. 

+-- {: .num_prop #GlobalPointsOfModuliOfFields}
###### Proposition

The [[∞-groupoid]] of global [[elements]] of $[X, \mathbf{Fields}]_{\mathbf{H}}$ is 

$$
  \mathbf{H}(*,[\Phi_X, \mathbf{Fields}_{\mathbf{H}}])
  \simeq
  \Gamma [\Phi_X, \mathbf{Fields}]_{\mathbf{H}}
  \simeq
  \mathbf{H}_{/\mathbf{BgFields}}(\Phi_X, \mathbf{Fields})
  \,.
$$

=--

+-- {: .proof}
###### Proof

Using the [[adjunction]] [[equivalences]] we have

$$
  \begin{aligned}
    \mathbf{H}(*, [\Phi_X, \mathbf{Fields}]_{\mathbf{H}})
    & \simeq
    \mathbf{H}(*, \underset{\mathbf{BgFields}}{\prod} [\Phi_X, \mathbf{Fields}])
    \\
    & \simeq \mathbf{H}_{/\mathbf{BgFields}}(\mathbf{BgFields}^*(*), [\Phi_X, \mathbf{Fields}])
    \\
    & \simeq \mathbf{H}_{/\mathbf{BgFields}}(*, [\Phi_X, \mathbf{Fields}])
    \\
    & \simeq \mathbf{H}_{/\mathbf{BgFields}}(\Phi_X, \mathbf{Fields})
  \end{aligned}
$$

where the first line is the definition, the second is the $(\mathbf{BgFields}^* \dashv \underset{\mathbf{BgFields}}{\prod})$ [[adjunction]]-[[equivalence]], the third is the $(\underset{\mathbf{BgFields}}{\sum} \dashv \mathbf{BgFields}^*)$-adjunction implying that $\mathbf{BgFields}^*$ preserves the [[terminal object]], and finally the last line is the defining [[internal hom]] [[adjunction]]-[[equivalence]]. 

=--

+-- {: .num_prop #ModuliStackOfFieldsAsHomotopyFiber}
###### Proposition

The [[moduli ∞-stack]] of fields $[\Phi_X, \mathbf{BgFields}]_{\mathbf{H}}$ sits in a [[homotopy pullback]] [[diagram]] of the form

$$
  \array{
    [\Phi_X, \mathbf{Fields}]_{\mathbf{H}}
    &\stackrel{}{\to}&
    [X, \underset{\mathbf{BgFields}}{\sum}\mathbf{Fields}]
    \\
    \downarrow &\swArrow_{\kappa}& \downarrow
    \\
    {*}
    &\stackrel{\vdash \Phi_X}{\to}&
    [X, \mathbf{BgFields}]
  }
  \,.
$$

=--

These relations are discussed at _[[slice (∞,1)-topos]]_, and ([dcct, section 3.6.1](#dcct)).


+-- {: .num_remark }
###### Remark

Proposition \ref{ModuliStackOfFieldsAsHomotopyFiber} makes precise the heuristic idea that a field $\phi \in [\Phi_X, \mathbf{Fields}]_{\mathbf{H}}$ is 

1. a configuration $\phi_X \;\colon\; X \to \underset{\mathbf{BgFields}}{\sum}\mathbf{Fields}$ on [[spacetime]]/[[worldvolume]] $X$;

1. together with a [[gauge transformation]] $\kappa_{\phi} \;\colon\;  \Phi_X \stackrel{\simeq}{\to} \mathbf{Fields}\circ \phi_X$ between the fixed [[background field]] and the background field induced by $\phi_X$.

=--

More generally, the moduli $\infty$-stacks of combined bulk/boundary-defect fields as in def. \ref{ModuliOfBulkAndBoundaryFields} is characterized as follows.

+-- {: .num_prop #ModuliOfBulkAndDefectFieldsAsPullback}
###### Proposition

The moduli stack $[\iota_X, \mathbf{Fields}]_{\mathbf{H}}$ of bulk and defect fields in def. \ref{ModuliOfBulkAndBoundaryFields} sits in an [[(∞,1)-pullback]] [[diagram]]

$$
  \array{
    [\iota_X, \mathbf{Fields}]_{\mathbf{H}}
    &\to&
    [X_{def}, \mathbf{Fields}_{def}]
    \\
    \downarrow && \downarrow^{\mathrlap{}}
    \\
    [X_{bulk}, \mathbf{Fields}_{bulk}]
    &\stackrel{}{\to}&
    [X_{def}, \mathbf{Fields}_{bulk}]
  }
  \,.
$$

=--

The following proposition expresses that fixing a bulk field gives rise to a background field for the remaining defect fields

+-- {: .num_prop }
###### Proposition

For $\phi_{bulk} \;\colon\; X_{bulk} \to \mathbf{Fields}_{bulk}$ a given bulk field, there is a [[natural equivalence|natural]] [[equivalence in an (∞,1)-category|equivalence]]

$$
  [\iota_X^* \phi_{bulk}, \mathbf{Fields}]_{\mathbf{H}}
  \simeq
  [\iota_X, \mathbf{Fields}]_{\mathbf{H}}
  \underset{[X_{bulk}, \mathbf{Fields}_{bulk}]}{\times} \{\phi_{bulk}\}
  \,.
$$

=--

##### Relation to sections of $\infty$-bundles
 {#RelationOfFieldsToSections}


We discuss here how def. \ref{FieldsInAnActionFunctional} equivalently says that fields are [[sections]] of a [[fiber ∞-bundle]] which is  which is [[associated ∞-bundle|associated]] to a ([[principal ∞-bundle|principal]])  $\infty$-bundle modulated by the [[background field]].

For simplicity of the discussion first consider the case that $\mathbf{BgFields} \simeq \mathbf{B}G$ is the [[delooping]] of an [[∞-group]] $G \in Grp(\mathbf{H})$. (In typical applications in [[physics]] we instead have the differential refinement $\mathbf{B}G_{conn}$ (see below at _[Examples -- Gauge fields](#GaugeFields)_) and the following discussion is directly generalized to that case. )

1. [Background fields as principal ∞-bundles](#BriefReviewOfPrincipalInfinityBundlesAsBackgroundFields)

1. [Fields as sections of associated fiber ∞-bundles](#FieldsAsSectionsOfAssociatedBundles)

###### Background fields as principal $\infty$-bundles
 {#BriefReviewOfPrincipalInfinityBundlesAsBackgroundFields}

We briefly recall the central aspects of [[principal ∞-bundles]] in the [[(∞,1)-topos]] $\mathbf{H}$.

For $X \in \mathbf{H}$ any [[object]] and $x \colon * \to \X$ a [[global element]], the [[homotopy pullback]] ([[(∞,1)-pullback]]) of the point along itse is the based [[loop space object]]

$$
  \Omega_x X  \coloneqq \{x\} \underset{X}{\times} \{x\}
  \,.
$$

Via composition of loops, this canonically has the structure of an [[A-∞ algebra]] object such that the [[truncated object in an (∞,1)-category|0-truncation]] $\tau_0 \Omega_x X$ is a [[monoid object]] which is a [[group object]]. Such _groupal $A_\infty$-algebra objects_ are _[[group objects in an (∞,1)-category|group objects]]_ in $\mathbf{H}$: [[∞-groups]].

In fact every [[∞-group]] is of this form. Moreover, restricted to [[pointed object|pointed]] and [[connected object in an (∞,1)-topos|connected objects]], the [[looping and delooping|looping]] [[(∞,1)-functor]] $\Omega$ is an [[equivalence of (∞,1)-categories]]

$$
  Grp(\mathbf{H})
  \stackrel{\overset{\Omega}{\leftarrow}}{\underoverset{\mathbf{B}}{\simeq}{\to}}
  \mathbf{H}^{*/}_{\geq 1}
  \,.
$$

Its inverse $\mathbf{B}$ we call the [[delooping]] operation. Notice that this means that we can conveniently discuss all aspects of [[∞-groups]] without ever explicitly considering [[A-∞ algebra]] structure by instead working with the pointed connected objects $\mathbf{B}G$.

Notably one finds that a $G$-[[principal ∞-bundle]] $P \to X$ in $\mathbf{H}$ is equivalently the [[homotopy fiber]] of a map $g \;\colon\; X \to \mathbf{B}G$

$$
  \array{
     fib(g) \simeq & P &\to& * & \simeq \mathbf{E}G
     \\
     & \downarrow && \downarrow
     \\
     & X &\stackrel{g}{\to}& \mathbf{B}G
  }
  \,.
$$

This construction yields an [[equivalence of ∞-groupoids]]

$$
  G Bund(X)
  \stackrel{\overset{fib}{\leftarrow}}{\underoverset{}{\simeq}{\to}}  
  \mathbf{H}(X, \mathbf{B}G)
$$

between $G$-[[principal ∞-bundles]] with [[gauge transformations]] between them and $G$-[[cocycles]] with [[coboundaries]]. In particular this means that $G$-[[principal ∞-bundles]] are classified by $G$-[[cohomology]] in $\mathbf{H}$

$$
  G Bund(X)_{/\sim}
  \simeq
  \pi_0 G Bund(X)
  \stackrel{\simeq}{\to}
  \pi_0 \mathbf{H}(X, \mathbf{B}G)
  \simeq
  H^1(X,G)
  \,.
$$

Hence if $\mathbf{BgFields} \simeq \mathbf{B}G$ then a [[background field]] on $X$ is equivalently a $G$-[[principal ∞-bundle]] on $X$. 


###### Fields as sections of associated fiber $\infty$-bundles
 {#FieldsAsSectionsOfAssociatedBundles}



+-- {: .num_prop #EquivalenceOfActionCategoryWithSlice}
###### Proposition

For $G \in Grp(\mathbf{H})$ a [[group object in an (∞,1)-category|group object]] in $\mathbf{H}$, the [[(∞,1)-functor]] that sends an [[∞-action]] $\rho$ of $G$ on some $V \in \mathbf{H}$ to the corresponding [[associated ∞-bundle]] of the $G$-[[universal principal ∞-bundle]] is an [[equivalence of (∞,1)-categories]]

$$
  (\mathbf{E}G)\times_G(-)
  \;\colon\;
  G Act(\mathbf{H})
  \stackrel{\simeq}{\to}
  \mathbf{H}_{/\mathbf{B}G}
  \,.
$$

Moreover there is a [[natural equivalence|natural]] [[equivalence in an (∞,1)-category|equivalence]]

$$
  (\mathbf{E}G)\times_G V
  \simeq
  {*} \times_G V
  \simeq
  V//G
$$

with the [[quotient]] of $V$ by the $G$-[[∞-action]] $\rho$ (this is the general abstract and version and geometric refinement of the traditional [[Borel construction]]). 

=--

+-- {: .num_defn }
###### Definition

For $\rho$ an [[∞-action]] of an [[∞-group]] $G \in Grp(\mathbf{H})$ on some $V \in \mathbf{H}$ we write

$$
  V//G \stackrel{\overline{\rho}}{\to} \mathbf{B}G
$$

for the image of $\rho$ under the equivalence of prop. \ref{EquivalenceOfActionCategoryWithSlice}.

=--

+-- {: .num_prop }
###### Proposition

The [[homotopy fiber]] of $\overline{\rho}$ is $V$, hence we have a [[homotopy fiber sequence]]

$$
  \array{
    V &\to& V//G
    \\
    && \downarrow^{\mathrlap{\overline{\rho}}}
    \\
    && \mathbf{B}G
  }
$$

identifying $\overline{\rho}$ with a $V$-[[fiber ∞-bundle]] over $\mathbf{B}G$. Moreover, this is the _[[universal associated ∞-bundle|universal rho-associated ∞-bundle]]_: for every $G$-[[principal ∞-bundle]] $P \to X$ with modulating map $g_X \;\colon\; X \to \mathbf{B}G$ there is a [[natural equivalence|natural]] [[equivalence in an (∞,1)-category]]

$$
  P \times_G V \simeq g_X^*(\overline{\rho})
$$

in $\mathbf{H}_{/X}$.

=--

+-- {: .num_remark }
###### Remark

In summary this means that an [[∞-action]] $\rho$ of an [[∞-group]] $G$ on any object $V \in \mathbf{H}$ is equivalently a [[homotopy fiber sequence]] of the form

$$
  \array{
    V &\to& V//G 
    \\
    && \downarrow^{\mathrlap{\overline{\rho}}}
    \\
    && \mathbf{B}G
  }
  \,.
$$

Moreover, for $P \to X$ any $G$-[[principal ∞-bundle]] modulated by a map $g ;\colon\; X \to \mathbf{B}G$ and for $\rho$ an [[∞-action]] of $G$ on some $V$, there is an [[(∞,1)-pullback]] diagram

$$  
  \array{
    P \times_G V
    &\to&
    V//G
    \\
    \downarrow && \downarrow^{\mathrlap{\overline{\rho}}}
    \\
    X &\stackrel{g}{\to}& \mathbf{B}G
  }
  \,.
$$

=--



Due to the [[universal property]] of the [[(∞,1)-pullback]] this has the following consequence which, basic as it is, is fundamental for the interpretation of fields in def. \ref{FieldsInAnActionFunctional}.

+-- {: .num_prop }
###### Proposition

There is a canonical [[equivalence in an (∞,1)-category]] between the [[sections]] of the $\rho$-[[associated ∞-bundle]] $P \times_X G$ and maps $g_X \to \overline{\rho}$ in the slice, hence fields in the sense of def. \ref{FieldsInAnActionFunctional} with background field $g_X$ and moduli stack $\overline{\rho}$:

$$
  \mathbf{\Gamma}_X(P \times_G V)
  \simeq
  [g_X, \overline{\rho}]_{\mathbf{H}}
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

This equivalence is constituted simply by forming the [[pasting diagram]] of the [[section]] with the above $(\infty,1)$-pullback

$$  
  \array{
    && P \times_G V
    &\to&
    V//G
    \\
    &{}^{\mathllap{\sigma}}\nearrow& \downarrow && \downarrow^{\mathrlap{\overline{\rho}}}
    \\
    X &\stackrel{id}{\to}& X &\stackrel{g}{\to}& \mathbf{B}G
  }
  \;\;\;\;\;\;
  \simeq
  \;\;\;\;\;\;
  \array{
    X &&\stackrel{\sigma}{\to}&& V//G
    \\
    & {}_{\mathllap{g}}\searrow && \swarrow_{\overline{\rho}}
    \\
    && \mathbf{B}G
  }
  \,.
$$

=--

The following further central property leads in the [following section](#RelationToTwistedCohomology) to an equivalent re-formulation of this in [[twisted cohomology]].

+-- {: .num_prop }
###### Proposition

Every $G$-[[principal ∞-bundle]] $P \to X$ in an [[(∞,1)-topos]] $\mathbf{H}$ is _locally trivizable_ in that there exists a [[1-epimorphism]] $p \;\colon\; U \to X$ and an [[(∞,1)-pullback]] [[diagram]] of the form

$$
  \array{
    U \times G &\to& P
    \\
    \downarrow && \downarrow
    \\
    U &\stackrel{p}{\to}& X
  }
$$

or equivalently a diagram

$$
  \array{
    U &\to& *
    \\   
    \downarrow^{\mathrlap{p}}
    &\swArrow_{\simeq}&
    \downarrow
    \\
    X & \stackrel{g}{\to} & \mathbf{B}G
  }
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

Together the above facts imply that for 

$$
  \array{
     && P \times_G V &\to& V//G
     \\
     & {}^{\mathllap{\sigma}}\nearrow & \downarrow
     && \downarrow^{\mathrlap{\overline{\rho}}}
     \\
     X &\stackrel{id}{\to}& X &\stackrel{g}{\to}& \mathbf{B}G
  }
$$

a [[section]] of the [[associated ∞-bundle]], the restriction $\sigma|_U$ of the section along the trivializing cover $p \;\colon\; U \to X$ factors through $V \to V//G$:

$$
  \array{
     && V &\to& V//G
     \\
     & {}^{\mathllap{\sigma|_U}}\nearrow &  && \downarrow^{\mathrlap{\overline{\rho}}}
     \\
     U &\stackrel{p}{\to}& X &\stackrel{g}{\to}& \mathbf{B}G
  }
  \,.
$$

This means that a section of an [[associated ∞-bundle|associated]] 
$V$-[[fiber ∞-bundle]] is locally a $V$-valued map, hence a [[cocycle]] in $\Omega V$-[[cohomology]].

=--

And so we say that _globally_ it is a "twisted" $\Omega V$-cocycle. This leads to the following equivalent description.



##### Relation to twisted cohomology
 {#RelationToTwistedCohomology}

We discuss here how def. \ref{FieldsInAnActionFunctional} of fields has an entirely equivalent expression in terms of _[[cocycles]]_ in general _[[cohomology]]_ and in fact, if the background field is nontrivial, in _[[twisted cohomology]]_.
This follows by direct comparison with the corresponding notions in _[[cohomology]]_ and _[[twisted cohomology]]_ as discussed there ([NSS](#NSS)). The unification of notions seen this way gives a natural home for instance to the familiar observations such as that [[Chan-Paton gauge fields]] on [[D-branes]] are identified with [[cocycles]] in  ([[differential K-theory|differential]]) [[twisted K-theory]] (see _[Chan-Paton gauge fields](#ChanPatonGaugeFields)_ below).

First observe the following

+-- {: .num_remark}
###### Remark

For $\phi \;\colon\; \Phi_X \to \mathbf{Fields}$ a field configuration as in def. \ref{FieldsInAnActionFunctional} in the corresponding [[diagram]] in $\mathbf{H}$

$$
  \array{
     X &&\stackrel{\phi}{\to}&& \underset{\mathbf{BgFields}}{\sum} \mathbf{Fields}
     \\
     & {}_{\mathllap{\Phi_X}}\searrow 
     &\swArrow& 
     \swarrow_{\mathrlap{\mathbf{Fields}}}
     \\
     && \mathbf{BgFields}
  }
$$

we have the following equivalently identifications when interpreting this as a [[cocycle]]:

* the object $\mathbf{Fields} \in \matbbf{H}_{/\mathbf{BgFields}}$ is the **[[local coefficient ∞-bundle]]**;

* the [[homotopy fiber]] $V$ of $\underset{\phi \in [X, \mathbf{Fields}]}{\sum}\mathbf{Fields} \to \mathbf{BgFields}$ is the **local [[coefficient]]** for a [[cohomology]] theory;

* the [[background field]] $\Phi_X$ is the **[[twisted cohomology|twist]]**

* the field $\phi \colon \Phi_X \to \mathbf{Fields}$ is 

  * a **[[cocycle]]** in $\Phi_X$-[[twisted cohomology]] on $X$ with local [[coefficients]] $V$

  * equivalently: a **$\Phi_X$-twisted [[G-structure|V-structure]]** on $X$;

* a [[gauge transformation]] is a **[[coboundary]]** in $\Phi_X$-twisted $V$-cohomology;

* the [[equivalence classes]] of fields are the $\Phi_X$-[[twisted cohomology|twisted]] $V$-[[cohomology]] of [[spacetime]] $X$

  $$
    H_{[\Phi_X]}(X,V) \simeq \tau_0\Gamma[X,\mathbf{Fields}]_{\mathbf{H}}
    \,.
  $$

=--

We see several illustrations of these identifications in the list of _[Examples](#Examples)_ below. More generally, there is a canonical identification of physical fields in the presence of background fields _and_ boundary/defect with twisted and _[[relative cohomology]]_. This we discuss below in _[Relation to relative cohomology](#RelationToRelativeCohomology)_.



##### Relation to relative cohomology
 {#RelationToRelativeCohomology}


When we refine background fields to dynamical fields as
discussed above in _[Boundary and defect fields](#BoundaryAndDefectFields)_ then the identification of fields with [[cocycles]] in [[twisted cohomology]] as discussed above in 
_[Relation to twisted cohomology](#RelationToTwistedCohomology)_ accordingly generalized a bit: it becomes a combination of twisted cohomology and _[[relative cohomology]]_.

For consider the special case that the moduli of defect fields are trivial, hence that 

$$
  \mathbf{Fields} \colon * \stackrel{pt_Q}{\to} \mathbf{Fields}_{bulk}
$$

is the global point inclusion into the bulk field moduli (the trivial bulk field).  By prop. \ref{ModuliOfBulkAndDefectFieldsAsPullback} it follows that

+-- {: .num_prop }
###### Proposition

There is a natural equivalence

$$
  [\iota_X, pt_A]
  \simeq
  [X_{bulk}, A] \underset{[X_{def}, A]}{\times} {*}
  \,,
$$

hence a [[homotopy fiber sequence]]

$$
  [\iota_X, pt_A]
   \to 
  [X_{bulk}, A]
   \to 
  [X_{def}, A]
$$

=--

+-- {: .num_remark }
###### Remark

This identifies the equivalence classes of global points in $[\iota_X, pt_A]$ as the 
$\iota_X$-[[relative cohomology|relative A-cohomology]] of $X$.

=--

In general, if the defect fields are not trivial, the fields $\iota_X \to \mathbf{Fields}$ (hence ordinary cocycles in $\mathbf{H}^{(\Delta^1)}$) are a kind of cocycles in $\mathbf{H}$ that are a combination of relative and twisted cocycles: instead with their pullback to $X_{def}$ being equipped with a trivialization, it is equipped with a "twisted trivialization" in the sense of [[twisted differential c-structure|twisted c-structures]], disucssed [below](#TwistedDifferentialcStructurs).



#### Examples
 {#FieldsModelLayerExamples}


We distinguish four broad classes of examples of [[physical fields]], according to def. \ref{FieldsInAnActionFunctional}:

1. [Scalar and moduli fields](#SclarModuliFields)

   The simplest type of field is a ([[smooth function|smooth]]) [[function]] on [[spacetime]] $X$ with values in the [[real numbers]] or [[complex numbers]], called a _[[scalar field]]_. Slightly more generally there are fields which are [[functions]] into some other [[vector space]] or more general [[manifold]], often called _linear/non-linear [[sigma-model]]_ fields. Often that manifold is a space of parameters of some [[geometry]], for instance of a compact space in [[Kaluza-Klein compactification]], in which case these fields are often called _moduli fields_. Scalar fields may be _charged_ under force fields, which we turn to next.

1. [Force fields](#ForceFields)

   1. [Fields of gravity, G-structure and generalized geometry](#FieldsOfGravityAndGeneralizedGeometry)

      In this case the [[background gauge field]] is a [[G-structure]], the [[moduli stack]] of fields is a [[delooping|delooped]] [[∞-group extension]] $\mathbf{B}\hat G \stackrel{\mathbf{Fields}}{\to} \mathbf{B}G$ and a field is a generalized [[vielbein]] exhibiting a [[reduction and lift of structure groups|reduction/lift of structure group]].

   1. [Gauge fields](#GaugeFields)

      In this case $\mathbf{Fields}$ is a [[moduli space]] $\mathbf{B}G_{conn}$ of [[connections on an ∞-bundle|∞-connections]] on $G$-[[principal ∞-bundles]] for some [[gauge group]] $G \in Grpd(\mathbf{H})$.

1. [Matter fields](#MatterFields)

   In this case the [[background gauge field]] is a $G$-[[principal ∞-bundle]] $P$ for some [[gauge group]] $G \in Grp(\mathbf{H})$ and $\mathbf{Fields}$ is the univeral $\rho$-[[associated ∞-bundle]] $V//G \stackrel{\mathbf{Fields}}{\to} \mathbf{B}G$ for $\rho$ an [[∞-action]] of $G$ on some $V \in \mathbf{H}$. A field is [[section]] of the [[associated ∞-bundle|associated]] $V$-[[fiber ∞-bundle]].

   
Not all examples fall squarely into one of these types, some are mixtures of these. Relevant examples we discuss in

* [Fields combining various of these properties](#FieldCombiningVariousProperties)

In particular the moduli stacks $\mathbf{B}G$ here are typically all differentially refined to moduli stacks $\mathbf{B}G_{conn}$ of [[connection on an ∞-bundle|∞-connections]] so that for instance every [[reduction and lift of structure groups]] goes along with a corresponding data of the reduction of an [[connection on an ∞-bundle|∞-connection]]. The archetypical example for this are [[spin connections]], see the example _[Ordinary gravity](#OrdinaryGravity)_ below.

+-- {: bluebox}
###### Examples ######

1. [Sigma-model fields](#SigmaModelFields)

   1. [Uncharged scalar particle](#UnchargedScalarField)

   1. [Particle trajectors](#ParticleTrajectory)

   1. [Brane trajectory](#BraneTrajectory)

1. [Force fields](#ForceFields)

   1. [Fields of gravity, G-structure and generalized geometry](#FieldsOfGravityAndGeneralizedGeometry)

   1. [General -- G-structure: twisted lift of structure group](##GStructure)

   1. [Gravity](#OrdinaryGravity)

   1. [Spin structures](#SpinStructures)

   1. [Spin-c structures](#SpinStructures)

   1. [Type II gravity, exceptional geometry](##TypeIIGravity)

   1. [Higher spin structures](#HigherSpinStructures)

   1. [Higher spin-c structures](#HigherSpincstructures)

1. [Gauge fields](#GaugeFields)

   1. [General -- Coefficients in differential cohomology: connections](#GaugeFieldsGeneral)

   1. [Electromagnetic field](#ElectromagneticField)

   1. [Yang-Mills field](#YangMillsField)

   1. [Kalb-Ramond B-field](#KalbRamondBField)

   1. [Supergeometric B-Field](#KalbRamondBField)

   1. [Supergravity C-field](#SupergravityCField)

1. [Matter fields](#MatterFields)

   1. [General -- Sections of associated bundles](#SectionsOfAssociatedBundles)

   1. [Fermions](#Fermions)

   1. [Tensor fields](#TensorFields)

1. [Fields combining these properties](##FieldCombiningVariousProperties)

   1. [General -- Twisted differential cocycles and c-structures](#TwistedDifferentialcStructurs)

   1. [Nonabelian charged particle trajectories -- Wilson lines](#NonabelianChargedParticle)

   1. [3d Chern-Simons field with Wilson line](#ChernSimonsWithWilsonLines)

   1. [Chan-Paton gauge bundles on D-branes: twisted differential K-cocycles](#ChanPatonGaugeFields)

   1. [Anomaly-free heterotic string background: differential String-c structures](#HeteroticStringBackgroundField)

=--


##### **0)** Sigma-model fields
 {#SigmaModelFields}

Traditionally a [[sigma-model]] field is a type of fields given simply by ([[smooth function|smooth]]) [[functions]] $\Sigma \to X$ from a [[worldvolume]] $\Sigma$ to a [[target space]] $X$. Now, by the general unified definition def. \ref{FieldsInAnActionFunctional} and as shown in the following sections, in [[higher geometry]] _every_ type of field is of this form if we allow [[target space]] $X$ to be a general [[∞-stack]] and functions to be maps in a suitable [[slice (∞,1)-topos]]. Nevertheless, here we start with briefly indicating those examples that are [[sigma-model]] fields also in the traditional restrictive sense of the term.

###### Uncharged scalar field
 {#UnchargedScalarField}

A _[[scalar field]]_ is given simply by a [[function]] on [[spacetime]]/[[worldvolume]], typically with values in the [[real numbers]] $\mathbb{R}$ ("real scalar fiedl") or the [[complex numbers]] $\mathbb{C}$ ("complex scalar field"). Hence this is the example of def. \ref{FieldsInAnActionFunctional} with trivial [[background fields]]

$$
  \mathbf{BgFields} \coloneqq *
$$

(the [[terminal object]]) and with the field moduli stack being the map

$$
  \mathbf{Fields} \;\colon\; \mathbb{R} \to *
$$

from (the [[smooth manifold]] underlying) the [[real numbers]] to the point, or else

$$
  \mathbf{Fields} \;\colon\; \mathbb{C} \to *
$$

regarded as an object in $\mathbf{H}_{/*} \simeq \mathbf{H}$.

[[scalar field|Scalar fields]] are, due to their simplicity, prominent in toy examples used to discuss general properties of [[quantum field theory]]. The only  fundamental scalar particle observed in nature to date is the [[Higgs particle]] (or presumeably so, in [[technicolor]] models it is not actually fundamental but a composite of [[fermion]] particles, discussed [below](#Fermions)), but the Higgs field is, crucially, charged under the [[electroweak field|electroweak]] [[special unitary group|SU(2)]]-[[gauge field]]. A [[model (in theoretical physics)|model]] of relevance in [[phenomenology]] which crucially features an uncharged scalar particle is [[cosmic inflation]]. But the fundamental nature of the [[inflaton field]] is hypothetical (if it exsists at all), it might well be the [[effective QFT|effective]] version of non-scalar fields.

###### Particle trajectory
 {#ParticleTrajectory}

The dynamics of a [[particle]] propagating in a [[spacetime]] $X$ is described by a field on the abstract [[worldline]] which is simply a [[smooth function]] $\mathbb{R} \to X$ to the [[target space]] $X$: a [[trajectory]] of the particle. The [[quantum mechanics]] that describes the [[dynamics]] of such a quantum particle is equivalently a 1-dimensional field theory on the [[worldline]], with these maps as its physical fields. 

Therefore such wordline [[sigma-model]] fields are given by the special case of def. \ref{FieldsInAnActionFunctional} with trivial [[background field]] $\mathbf{BgFields} \simeq *$ and with $\mathbf{Fields} \;\colon\; X \to * $ regarded as an object in $\mathbf{H}_{/*} \simeq \mathbf{H}$. 


###### Brane trajectory
 {#BraneTrajectory}

More generally, the [[worldvolume]] fields of any [[brane]] [[sigma-model]] with [[target space]] $X$ are given as [above](#ParticleTrajectory).


##### **I)** Force fields
 {#ForceFields}

We discuss examples for the two classes of [[force]] fields, which are:

* [Fields of gravity, G-structure and generalized geometry](#FieldsOfGravityAndGeneralizedGeometry);

* [Gauge fields](#GaugeFields).


###### **I a)** Fields of gravity, $G$-Structure and generalized geometry
 {#FieldsOfGravityAndGeneralizedGeometry}

We discuss the example of the field of [[gravity]], below in _[Gravity](#OrdinaryGravity)_, and various closely related types of fields that all encode [[geometry]] in some sense, in fact all encode geometry in the sense of _[[G-structure]]_. This most general case we discuss in _[G-structure -- (twisted lift of structure ∞-groups)](#GStructure)_.

####### **General** -- $G$-structure: (twisted) lift of structure $\infty$-group
 {#GStructure}

Let 

$$
  A \to \hat G \stackrel{\mathbf{p}}{\to} G
$$

be an [[∞-group extension]] in $\mathbf{H}$. Then for $g_X \colon X \to \mathbf{B}G$ a given $G$-[[principal ∞-bundle]], a [[lift of the structure group]] from $G$ to $\hat G$ is a field

$$
  \phi \; \colon\; g_X \to \mathbf{B p}
  \,.
$$

If the [[∞-group extension]] is central in that it extends to a [[homotopy fiber sequence]] of the form

$$
  \mathbf{B}A \to \mathbf{B}\hat G \stackrel{\mathbf{Bp}}{\to} \mathbf{B}G \stackrel{\mathbf{c}}{\to} \mathbf{B}^2 A
$$

then a [[twisted differential c-structure|twisted c-structure]] is a map

$$
  \phi 
   \;\colon\;
  g_X \to \mathbf{c}
$$

in $\mathbf{H}_{/\mathbf{B}G}$.
These kinds of fields are interpreted as fields of [[gravity]] and its variants, as shown by the following examples.

For recognizing traditional constructions in this formulation, the following basic fact is important.

+-- {: .num_prop #CosetIsHomotopyFiberOfDeloopedInclusion}
###### Proposition

For $\iota \colon H \hookrightarrow G$ an [[subgroup]] inclusion of [[Lie groups]], we have a [[homotopy fiber sequence]]

$$
  G/H \to \mathbf{B}H \stackrel{\mathbf{B}\iota}{\to} \mathbf{B}G
$$

with the [[coset space]] on the left.

=--



####### Gravity
 {#OrdinaryGravity}

We discuss the formulation of the field of [[gravity]] as a special case of def. \ref{FieldsInAnActionFunctional}.

+-- {: .num_defn}
###### Definition

For $n \in \mathbb{N}$, let 

$$
  \mathbf{Fields} 
  \;\colon\;
  \mathbf{B}O(n)
   \stackrel{\mathbf{OrthStruc}_n}{\to}
  \mathbf{B}GL(n)
$$

be the [[delooping]] of the [[Lie group|Lie]]-[[subgroup]] inclusion of the [[orthogonal group]] into the [[general linear group]] in [[dimension]] $n$ (the inclusion of the [[maximal compact subgroup]]).

For $X \in $ [[SmoothMfd]] $\hookrightarrow$ $\mathbf{H} \coloneqq$ [[Smooth∞Grpd]] a [[smooth manifold]] of [[dimension]] $n$, write

$$
  \Phi_X \coloneqq \tau_X \;\colon\; X \to \mathbf{B}GL(n)
$$

for the canonical map modulating the $GL(n)$-[[principal bundle]] to which the [[tangent bundle]] is canonically [[associated bundle|associated]].

=--

+-- {: .num_example #RiemannianVielbein}
###### Example

Morphisms

$$
  \phi \;\colon\; \tau_X \to \mathbf{OrthStruc}_n
$$

in $\mathbf{H}_{/\mathbf{B}GL(n)}$ hence [[diagrams]]

$$
  \array{
    X &&\stackrel{}{\to}&& \mathbf{B}O(n)
    \\
    & \searrow &\swArrow_{e}& \swarrow
    \\
    && \mathbf{B}GL(n)
  }
$$

in $\mathbf{H}$ are equivalently [[vielbein]] fields $e$ exhibiting the [[reduction of the structure group]] from $GL(n)$ to $O(n)$. A [[gauge transformation]] is a local frame transformation. Hence 

$$
  [\tau_X, \mathbf{OrthStruc}_n]_{\mathbf{H}}
  \in 
  \mathbf{H}
$$

is the [[moduli stack]] of [[Riemannian metrics]] on $X$. Every such is a field configuration of ordinary [[gravity]] on $X$. (But see example \ref{GenerallyCovariantFieldOfGravity} below.)

According to 
remark \ref{PullbackAlongGeneralizedLocalDiffeomorphisms} such fields pull back along map $f \colon Y \to X$ that fit into a diagram

$$
  \array{
    Y &&\stackrel{f}{\to}&& X
    \\
    & {}_{\mathllap{\tau_Y}}\searrow &\swArrow_{\simeq}& \swarrow_{\mathrlap{\tau_X}}
    \\
    && \mathbf{B}GL(n)
  }
  \,.
$$ 

These are precisely [[local diffeomorphisms]] and indeed these are precisely the maps along which [[vielbein]] fields / [[pseudo-Riemannian metric]] fiedls pull back. (Pullback along [[smooth functions]] may not preserve the non-degeneracy of a metric tensor, but precisely the local diffeomorphisms do.)

=--


+-- {: .num_remark}
###### Remark

The [[smooth structure]] on $X$ as embodied by $\tau_X$ is the [[background field]] in example \ref{RiemannianVielbein}.

=--

+-- {: .num_remark #OrthogonalStructureIsTrivialInPlainHomotopyTheory}
###### Remark

Under [[geometric realization of cohesive infinity-groupoids|geometric realization]] 

$$
  {\vert-\vert}
  \;\colon\;
  \mathbf{H} \to \infty Grpd \simeq L_{whe} Top
$$

the map of [[moduli stacks]] $\mathbf{B}O(n) \to \mathbf{B}GL(n)$ becomes an [[equivalence]] (a [[weak homotopy equivalence]]) of [[classifying space]] $B O(n) \stackrel{\simeq}{\to} B GL(n)$.

This means that in plain [[homotopy theory]], hence ignoring the [[geometry]], a lift in 

$$
  \array{
    && B O(n)
    \\
    & \nearrow & \downarrow
    \\
    X &\stackrel{\tau_X}{\to}& B GL(n)
  }
$$

is no information, up to equivalence: it always exists and exists uniquely up to a contractible space of choices. In order for such a lift really to be equivalently an [[orthogonal structure]] it needs to be taken with geometry included, hence for [[moduli stacks]] (_[[cohesive (infinity,1)-topos|cohesive]]_ [[homotopy type]]) as above.

The analog statement is true for every delooping $\mathbf{B}H \to \mathbf{B}G$ of the inclusion $H \hookrightarrow G$ of a [[maximal compact subgroup]] into a [[Lie group]]. More examples of this kind we discuss below in _[Type II Gravity and generalized geometry](#TypeIIGravity)_.

=--

+-- {: .num_remark}
###### Remark

The [[homotopy fiber]] of $\mathbf{OrthStruc}_n$ is the [[coset space]] $GL(n)//O(n)$, hence we have a [[homotopy fiber sequence]] of [[moduli stacks]] of the form

$$
  GL(n)//O(n)
  \to
  \mathbf{B}O(n)
  \stackrel{\mathbf{OrthStruc}_n}{\to}
  \mathbf{B}GL(n)
$$

in $\mathbf{H}$. This means that locally, over a [[cover]] ([[1-epimorphism]]) $p \colon U \to X$ over which the [[tangent bundle]] has a trivialization $\tau_X|_U \simeq *$, the space of fields is simply $[U, GL(n)//O(n)]$.

=--

The next example is the differential refinement of the previous one.

+-- {: .num_example}
###### Example

Let 

$$
  \widehat \mathbf{OrthStruc}_n
  \;\colon\;
  \mathbf{B}O(n)_{conn}
  \to 
  \mathbf{B}GL(n)_{conn}
$$

be the canonical differential refinement of $\mathbf{OrthStruc}_n$, where now the [[moduli stacks]] of [[principal connections]] appear. For $X$ a manifold as above, let then

$$
  \hat \tau_X 
  \;\colon\;
  X 
  \to
  \mathbf{B}GL(n)_{conn}
$$

modulate an [[affine connection]] on the [[tangent bundle]]. A field 

$$
  \phi \;\colon\; \hat \tau_X \to \widehat \mathbf{OrthStruc}_n
$$

is now still equivalently just a [[vielbein]], but its component

$$
  \underset{\mathbf{B}GL(n)_{conn}}{\sum} \hat \tau_X
  \;\colon\;
  X \to \mathbf{B}O(n)_{conn}
$$

now captures the orthognal connection which in the physics literature is often called (inaccurately) the _[[spin connection]]_, denoted $\omega$. The [[vielbein]] then exhibits the original [[affine connection]] as that whose components are the [[Christoffel symbols]] $\Gamma$ of the [[Riemannian metric]] defined as above, a relation that is familiar from the physics literature in the form of the [[equation]]

$$
  \omega = e^{-1}\Gamma e + e^{-1} d e
$$

between local connection 1-form components.

=--

But both these examples do not fully accurately reflect the field content of [[gravity]] yet. This is because the [[theory (physics)|theory]] of [[gravity]] is supposed to by [[general covariance|generally covariant]]. This means that for two [[vielbein]] field configurations as in example \ref{RiemannianVielbein} such that one goes into the other under a [[diffeomorphism]] of [[spacetime]] $X$, there is a [[gauge transformation]] between them.

+-- {: .num_example #GenerallyCovariantFieldOfGravity}
###### Example

Write $\mathbf{Diff}(X) \coloneqq \mathbf{Aut}(X) \in Grp(\mathbf{H})$ for the [[diffeomorphism group]] of the [[smooth manifold]] $X$. There is then the canonical [[∞-action]] of the [[automorphism ∞-group]] $\mathbf{Diff}(X)$ on $X$ itself, exhibited by the universal [[associated ∞-bundle]]

$$
  \left(X // \mathbf{Diff}\left(X\right) \to \mathbf{B}\mathbf{Diff}\left(X\right) \right)
  \in 
  \mathbf{H}_{/\mathbf{B}\mathbf{Diff}\left(X\right)}
  \,.
$$

This induces also an [[∞-action]] also on the [[tangent bundle]].

Moreover the trivial bundle

$$
  \mathbf{Fields}
  \coloneqq
  (\mathbf{Diff}(X)\times \mathbf{OrthStruc} \to \mathbf{B}\mathbf{Diff}(X) )
  \in 
  \mathbf{H}_{/\mathbf{B}\mathbf{Diff}(X)}
$$

corresponds to the trivial action.

Then

$$
  \underset{\mathbf{B}Diff(n)}{\sum}
  \underset{\mathbf{B}(GL(n))}{\prod} 
  [\tau_X, \mathbf{Fields}]
 \in \mathbf{H}
$$

is the accurate space of [[general covariance|generally covariant]] fields of [[gravity]]. 

=--


####### $Spin$-structures
 {#SpinStructures}

In theories with [[fermions]] (discussed [below](#Fermions)) the field of [[gravity]] is more refined than just a [[vielbein field]] as [above](#OrdinaryGravity), hence an [[orthogonal structure]] on [[spacetime]]: it also involves an [[orientation structure]] and a [[spin structure]].

To see that these structures are really all (fields) of the same kind, observe that they are the lifts through the first step of the [[Whitehead tower]] of $\mathbf{B}GL$, as shown in the following table

[[!include higher spin structure - table]]

Notice, as in remark \ref{OrthogonalStructureIsTrivialInPlainHomotopyTheory}, that for the interpretation of the first step here it is crucial to interpret this in [[moduli ∞-stacks]] and not in [[classifying spaces]].

Hence if a background field of [[gravity]] is assumed, $\mathbf{BgFields} \colon \mathbf{B}O(n)$, $\Phi_X = e_X$, then the moduli stack for [[orientation structure]]-fields is

$$
  \mathbf{Fields} \colon \mathbf{B} SO(n) \to \mathbf{B}O(n)
$$

in $\mathbf{H}_{/\mathbf{B}O(n)}$. And if an orientation background field is assumed, $\mathbf{BgFields} \colon \mathbf{B}SO(n)$, $\Phi_X = o_X$, then the moduli stack for [[spin structure]]-fields is

$$
  \mathbf{Fields} \colon \mathbf{B} Spin(n) \to \mathbf{B}SO(n)
  \,.
$$

Evidently there is then also a notion of [[higher spin structure]]-fields. These appear as backgrounds when one passes from [[spinning particles]] to  [[spinning strings]] and then to further "spinning" [[branes]]. This we discuss below in _[Higher spin structures](#HigherSpinStructures)_.

####### $Spin^c$-structures
 {#SpinStructures}

Some [[theory (physics)|theories]] involve not plain [[spin structures]] but [[spin-c structures]] on their [[spacetime]]/[[worldvolume]] (for instance in [[Seiberg-Witten theory]] or in the [[gauge theory]] over [[D-branes]] in [[type II string theory]], see the example _[Chan-Paton gauge fields on D-branes](#ChanPatonGaugeFields)_ below). By the discussion there, the [[moduli stack]] $\mathbf{B}Spin^c(n)$ for 
[[spin^c group]]-[[principal bundles]] sits in the [[homotopy pullback]] diagram

$$
  \array{
    \mathbf{B}Spin^c &\to& \mathbf{B}U(1)
    \\
    \downarrow && \downarrow^{\mathrlap{\mathbf{c}_1 \,mod\, 2}}
    \\
    \mathbf{B}SO(n) &\stackrel{\mathbf{w}_2}{\to}&
   \mathbf{B}^2\mathbb{Z}_2
  }
 \,,
$$

where the right vertical map represents the universal [[first Chern class]] modulo 2. In other words this says that a [[spin^c-structure]] on some $X$ is a [[twisted differential c-structure|twisted w2-structure]] with twist the first Chern-class of a [[circle bundle]].

So if that circle bundle is regarded as a [[background field]]

$$
  \phi_X \coloneqq g_X \;colon\; X \to \mathbf{B}U(1)
$$

then a $Spin^c$-structure for that underlying circle bundle is a field

$$
  \phi 
    \;\colon\;
  \Phi_X \to \mathbf{w}_2
$$

in $\mathbf{H}_{/\mathbf{B}^2 \mathbb{Z}_2}$.

Or rather, if $X$ is a [[manifold]] as before and the $SO(n)$-principal bundle involved in the above is required to be a [[reduction of the structure group|reduction]] of the [[tangent bundle]] $\tau_X : X \to \mathbf{B}GL(n)$ as before, then the [[background field]] for $Spin^c$-structure fields is

$$
  \Phi_X 
   \;\colon\;
   X 
   \stackrel{(\tau_X, g_X \,mod\, 2)}{\to}
   \mathbf{B}GL(n) \times \mathbf{B}^2 \mathbb{Z}_2
  \,,
$$

and the field moduli stack is 

$$
  \mathbf{Fields} \;\colon\; 
  \mathbf{B}SO(n)
   \stackrel{(p, \mathbf{w}_2)}{\to}
  \mathbf{B}GL(n) \times \mathbf{B}
  \,.
$$



####### Type II gravity, exceptional geometry
 {#TypeIIGravity}

By remark \ref{OrthogonalStructureIsTrivialInPlainHomotopyTheory} above the ordinary field of [[gravity]] on some [[manifold]] $X$ is equivalently a [[reduction of the structure group]] from the [[general linear group]] to its [[maximal compact subgroup]], regarded as a field whose [[background field]] is the [[tangent bundle]] itself.

If one instead considers a variant of the [[tangent bundle]] as a [[background field]] -- a _[[generalized tangent bundle]]_ $\tau_X^{gen} : X \to \mathbf{B}G$ -- with some other structure [[Lie group]] $G$, then a field with values in 

$$
  \mathbf{Fields} 
    \;\colon\;
  \mathbf{B}H \to \mathbf{B}G
$$

in $\mathbf{H}_{/\mathbf{B}G}$ and for $H \hookrightarrow$ the inclusion of the [[maximal compact subgroup]], may be thought of as an accordingly  _generized field of gravity_ defining a _generalized_ [[Riemannian geometry]].

Such fields naturally appear in [[theory (physics)|theories]] of higher-dimensional [[supergravity]], where related to the [[T-duality]] and more generally [[U-duality]] structure of these [[theory (physics)|theories]].

Notably in manifestly [[T-duality]]-equivariant [[type II supergravity]] the [[generalized tangent bundle]] on the $n$-dimensional [[spacetime]] is an $O(n,n)$-[[principal bundle]] $\tau^{gen}_X \;\colon\; X \to \mathbf{B}O(n,n)$. The corresponding [[maximal compact subgroup]] inclusion yields the moduli stack of fields

$$
  \mathbf{Fields}
  \;\colon\;
  \mathbf{B}(O(n)\times O(n))
  \to
  \mathbf{B}O(n,n)
$$

and a field $\phi \;\colon\; \tau_X^{gen} \to \mathbf{Fields}$ is equivalently the [[generalized vielbein]] for the generalized Riemannian geometry called  _[[type II geometry]]_ on $X$. 

In fact also the generalized tangent bundle itself should be regarded as a field: Notice that the canonical diagonal inclusion

$$
  GL(n) \hookrightarrow O(n,n)
$$

does not have a [[retraction]]. Write $GL(n) \hookrightarrow G_{geom} \hookrightarrow O(n,n)$ for the maximal subgroup for which a retrection to $GL(n)$ still exists, called the **geometric subgroup** in the context of [[type II geometry]]. Then a lift of the tangent bundle to $G_{geom}$

$$
  \array{
    X &&\stackrel{\tau_X^{gen}}{\to}&& \mathbf{B}G_{geom} & \hookrightarrow& \mathbf{B} O(n,n)
    \\
    & {}_{\athllap{\tau_X}}\searrow &\swArrow& \swarrow_{\mathrlap{\mathbf{p}}}
    \\
    && \mathbf{B}GL(n)
  }
  \,,
$$

hence a field 

$$
  e_X^{gen} \;\colon\; \tau_X \to \mathbf{p}
$$ 

is what is called a _geoemtric_ [[generalized tangent bundle]]. These are exactly the generalized tangent bundles primarily considered in the literature (see at _[[type II geometry]]_  for more).

In the [[Kaluza-Klein compactification]] of [[type II supergravity]] and of [[11-dimensional supergravity]] preserving some amount of global [[supersymmetry]] this generalized type II geometry is further enhanced to various flavors of what is called  [[exceptional generalized geometry]]. 

Here the [[generalized tangent bundle]] has as structure group an [[exceptional Lie group]] from the $E$-series $E_{n(n)}$ (for compactification on an $n$-dimensional compact space). The moduli stack of fields is then

$$
  \mathbf{Fields} 
  \;\colon\;
  \mathbf{B} K_{n}
  \to 
  \mathbf{B} E_{n(n)}
$$

and a field $ e_X^{gen} \;\colon\; \tau_X^{gen} \to \mathbf{Fields}$ is equivalently a [[generalized vielbein]]  for  [[exceptional generalized geometry]].



####### Higher spin structures
 {#HigherSpinStructures}

By the discussion of [Spin structure fields](#SpinStructures) above there are evident higher analogs, obtained by climbing through the [[Whitehead tower]] [[higher spin structure - table|of BO]].

In the next step we have _[[String structure]]_-fields which are maps to

$$
  \mathbf{Fields}
  \;\colon\;
  \mathbf{B}String \to \mathbf{B}Spin
  \,.
$$

These appear as fields in [[heterotic supergravity]] with [[quantum anomaly]]-cancellation by the [[Green-Schwarz mechanism]] and for trivial [[gauge field]]. In the presence of a non-trivial gauge field these are further refined to _[Higher spin-c structrures](#HigherSpincstructures)_ discussed below. This field content of [[heterotic supergravity]] is discussed in more detail below in _[Anomaly-free heterotic supergravity fields -- differential String-c structures](#HeteroticStringBackgroundField)_.

Further up the [[Whitehead tower]] _[[Fivebrane structure]]_-fields are maps to

$$
  \mathbf{Fields}
  \;\colon\;
  \mathbf{B}Fivebrane \to \mathbf{B}String
$$

in $\mathbf{H}_{/\mathbf{B}String}$. These, or their twisted variants, appear in [[dual heterotic string theory]]. 


####### Higher $Spin^c$-structures
 {#HigherSpincstructures}

As discussed above, an ordinary [[spin-c structure]] is really a [[spin structure]] which is _[[twisted differential c-structure|twisted]]_ by the class of a $U(1)$-[[principal bundle]]. 

Similarly the [[higher spin structure]]-fields just discussed have further twistes by background unitary bundles. For

$$
  \mathbf{c} \;\colon\; \mathbf{B}G \to \mathbf{B}^3 U(1)
$$

some [[universal characteristic map]] on [[moduli ∞-stacks]], for $\mathbf{B}^3 U(1)$ the moduli 3-stack of [[circle n-bundle with connection|circle 3-bundles]], hence [[circle 3-group]]-[[principal ∞-bundles]] we say that the [[smooth ∞-group]] $String^{\mathbf{c}}$ appearing in the [[homotopy pullback]] diagram

$$
  \array{
    \mathbf{B}String^{\mathbf{c}}
    &\to&
    \mathbf{B} G
    \\
    \downarrow && \downarrow^{\mathrlap{\mathbf{c}}}
    \\
    \mathbf{B}Spin &\stackrel{\tfrac{1}{2}\mathbf{p}}{\to}&
    \mathbf{B}^3 U(1)
  }
$$

is a higher [[string 2-group]]-analog of [[spin^c]]. 

In particular, if $G$ is a compact, connected and simply connected [[simple Lie group]] (such as the [[spin group]] or the [[special unitary group]]) then 

$$
  \pi_0\mathbf{H}(\mathbf{B}G, \mathbf{B}^3 U(1)) 
  \simeq
  H^4(BG, \mathbb{Z}) 
  \simeq 
  \mathbb{Z}
$$

(the first equivalence is discussed at _[[Lie group cohomology]]_ as a special case of a theorem discussed at _[[smooth infinity-groupoid]]_). This means that there is an essentially unique map of higher moduli stacks

$$
  \mathbf{c}
  \;\colon\;
  \mathbf{B}G
  \to \mathbf{B}^3 U(1)
$$

which maps to the generator of $H^4(BG, \mathbb{Z})$ under [[geometric realization of cohesive infinity-groupoids]]. For $G = Spin$ this is the smooth refinement of the [[first fractional Pontryagin class]] $\tfrac{1}{2}\mathbf{p}_1$, discussed further at _[[twisted differential string structure]]_. 

Of interest in [[heterotic supergravity]] here is the case that $G = E_8 \times E_8$ (the product of the  [[exceptional Lie group]] $E_8$ with itself) and $\mathbf{c}$ is twice the canonical string class.

If then $g_X \;\colon\; X \to \mathbf{B}(E_8 \times E_8)$ is the [[instanton sector]] of the gauge field in [[heterotic supergravity]] regarded as a [[background gauge field]] for the field of heterotic [[gravity]], then with  

$$
  \mathbf{Fields}
  \;\colon\;
  \mathbf{B}Spin \stackrel{\tfrac{1}{2}\mathbf{p}_1}{\to} \mathbf{B}^3 U(1)
$$

a map

$$
  g_X \to \mathbf{Fields}
$$

in $\mathbf{H}_{/\mathbf{B}^3 U(1)}$ is a $\mathbf{String}^{\mathbf{c}}$-structure on $X$ whose underlying gage bundle is the given $\Phi_X$. 

As before for $Spin^c$-structures, in applications one in addition demands that this $\mathbf{String}^{\mathbf{c}}$-structure is indeed a refinement of the field of [[gravity]] of the theory, which means that one takes the [[background field]] to be

$$
  \Phi_X
  \;\colon\;
  X
  \stackrel{(\tau_X, g_X)}{\to} \mathbf{B}GL(n) \times \mathbf{B}(E_8 \times E_8)
$$

and the moduli $\infty$-stack of fields to be

$$
  \mathbf{Fields}
  \;\colon\;
  \mathbf{B}Spin(n)
  \stackrel{(p, \tfrac{1}{2}\mathbf{p}_1)}{\to}
  \mathbf{B}GL(n) \times \mathbf{B}^3 U(1)
  \,.
$$

These are precisely the [[instanton sectors]] of the fields of [[Green-Schwarz mechanism|Green-Schwarz anomaly free]] [[heterotic supergravity]], discussed further below in _[Anomaly-free heterotic supergravity fields](#HeteroticStringBackgroundField)_. ([SSS](#SSS))


###### **I b)** Gauge fields
 {#GaugeFields}

####### **General** -- Coefficients in differential cohomology: $\infty$-connections
 {#GaugeFieldsGeneral}

The term _gauge field_ in _[[gauge theory]]_ with respect to a [[gauge group]] $G$ refers to fields which are modeled by [[connection on a bundle|connections]] either on $G$-[[principal bundles]] or on [[associated bundles]] for these. The notion of [[equivalence]] between two such fields (hence between [[connections on bundles]]) is the original meaning of the word _[[gauge transformation]]_, even though that term is also used for equivalences between fields which are not modeled by connections.

We discuss the general notion of gauge fields and then various special cases and variants. The following table gives an overview over the notions involved in the concept of gauge fields

[[!include gauge field - table]]

+-- {: bluebox}
###### Contents: ######

1. [Electromagnetic field](#ElectromagneticField)

1. [Yang-Mills field](#YangMillsField)

1. [Kalb-Ramond B-field](#KalbRamondBField)

1. [Supergeometric B-field](#SupergeometricBField)

1. [Supergravity C-field](#SupergravityCField)

=--

####### Electromagnetic field
 {#ElectromagneticField}

A field configuratiotion of the [[electromagnetic field]] is a [[circle n-bundle with connection|circle bundle with connection]] and a [[gauge transformation]] of the EM field is an equivalence of such connections.

Let therefore

$$
  \mathbf{B}U(1)_{conn}
  \coloneqq
  \Omega^1//U(1)
  \simeq
  DK(U(1) \stackrel{d log}{\to} \Omega^1)
$$

be the [[quotient stack]] of the [[action]] of $U(1)$ on the [[sheaf]] of [[differential 1-forms]], equivalently the image under the [[Dold-Kan correspondence]] of the sheaf of [[chain complexes]] given by the [[Deligne complex]] for degree-2 [[ordinary differential cohomology]], as indicated.

This is the [[moduli stack]] for $U(1)$-[[principal connections]]. Hence setting $\mathbf{BgFields} \simeq *$ and 

$$
  \mathbf{Fields} \coloneqq \mathbf{B}U(1)_{conn}
$$

in def. \ref{FieldsInAnActionFunctional} yields the type of the electromagnetic field.


####### Yang-Mills field
 {#YangMillsField}

More generally, let $G$ be a [[Lie group]], and $\mathfrak{g}$ its [[Lie algebra]]. Write $\Omega^1(-,\mathfrak{g})$ the sheaf of [[Lie algebra valued 1-forms]]

+-- {: .num_defn #ModuliStackOfGPrincipalConnection}
###### Definition

The **moduli stack of $G$-[[principal connections]]** is the [[quotient stack]]

$$
  \mathbf{B}G_{conn}
  \coloneqq
  \Omega^1(-,\mathfrak{g})//G
$$

of the [[action]] of $G$ on it [[Lie algebra valued differential forms]] by [[gauge transformations]] 

$$
  g \colon A^g \coloneqq \mapsto A^g Ad_g A + g^* \theta 
  \,.
$$ 

=--

This is the [[moduli stack]] of the $G$-[[Yang-Mills field]]. Hence setting $\mathbf{BgFields} \simeq *$ and

$$
  \mathbf{Fields} \coloneqq \mathbf{B}G_{conn}
$$

in def. \ref{FieldsInAnActionFunctional} yields [[Yang-Mills fields]].



####### Kalb-Ramond $B$-field
 {#KalbRamondBField}

Let 

$$
  \mathbf{B^2}U(1)_{conn}
  \coloneqq
  \Omega^{2 \leq \bullet \leq 1} // \mathbf{B}U(1)
  \simeq
  DK(U(1) \stackrel{d log}{\to} \Omega^1 \stackrel{d}{\to} \Omega^2)
$$

be the image under the [[Dold-Kan correspondence]] of the [[Deligne complex]] for degree-3 [[ordinary differential cohomology]]. This is the [[moduli infinity-stack|moduli 2-stack]] for [[circle n-bundle with connection|circle 2-bundle with connections]].

Setting $\mathbf{BgFields} \simeq *$ and

$$
  \mathbf{Fields} \coloneqq \mathbf{B}^2 U(1)_{conn}
$$

in def. \ref{FieldsInAnActionFunctional} yields the 2-form 
gauge field known as the _[[B-field]]_ or the _[[Kalb-Ramond field]]_.

####### Supergeometric $B$-field
 {#KalbRamondBField}

The [[B-field]] appears both in [[bosonic string theory]] as well as in [[type II superstring theory]]. In ([Distler-Freed-Moore](#Precis)) it was pointed out that for the [[superstring]] the plain formulation [above](#KalbRamondBField) needs to be refined. We discuss here the natural  formulation of this observation in [[smooth super infinity-groupoid|higher supergeometry]] as in ([FSS CSIntroAndSurvey, section 4.3](#FiorenzaSatiSchreiberCSIntroAndSurvey)).

Generally instead of the [[circle group]] $U(1)$ one can consider the [[multiplicative group]] $\mathbb{C}^\times$ of non-zero [[complex numbers]]. The canonical [[subgroup]] inclusion $U(1) \hookrightarrow \mathbb{C}^\times$ induces for each $n \in \mathbb{N}$ a canonical morphism of [[moduli ∞-stacks]]

$$
  \mathbf{B}^n U(1) \to \mathbf{B}^n \mathbb{C}^\times
  \,.
$$

This is not quite an [[equivalence]] of [[∞-stacks]] but it is a [[shape modality]]-equivalence in that [[geometric realization of cohesive ∞-groupoids]] sends it to an equivalence as

$$
  {\vert \mathbf{B}^n U(1)\vert}
  \simeq
  {\vert \mathbf{B}^n \mathbb{C}^\times\vert}
  \simeq
  K(\mathbb{Z}, n+1)
  \,.
$$

For instance smooth $U(1)$-[[principal bundles]] and $\mathbb{C}^\times$-[[principal bundles]] are both classified by the universal [[Chern class]] in $H^2(-, \mathbb{Z})$ but the [[gauge transformation|gauge]] [[automorphisms]] of the trivial $U(1)$-principal bundle form $C^\infty(-,U(1))$, while that of the trivial $\mathbb{C}^\times$-principal bundle form the larger $C^\infty(-,\mathbb{C}^\times)$.

Both versions of the moduli $n$-stack of $n$-bundles have their use. The version $\mathbf{B}^n \mathbb{C}^\times$ has the advantage that it is actually equivalent to the moduli $n$-stack of complex line $n$-bundles.

$$
  \mathbf{B}^n \mathbb{C}^\times \simeq n Line_\mathbb{C}
  \,.
$$

Specifically for $n = 2$ it is equivalent to the moduli 2-stack of [[line 2-bundles]]

$$
  \mathbf{B}^2 \mathbb{C}^\times \simeq 2 Line_\mathbb{C}
  \,.
$$

But now in [[supergeometry]] [complex super-line 2-bundle](http://ncatlab.org/nlab/show/line%202-bundle#SuperLine2BundlesAndTwistedK) have a richer classification that plain [[line 2-bundle]]. 
Explicitly, let now $\mathbf{H} \colon $ [[SmoothSuper∞Grpd]] be the ambient [[cohesive (∞,1)-topos]] for higher [[supergeometry]] and write

$$
  2\mathbf{sLine}_{\mathbb{C}}
  \in 
  \mathbf{H}
$$

for the 2-stack of [complex super-line 2-bundle](http://ncatlab.org/nlab/show/line%202-bundle#SuperLine2BundlesAndTwistedK). 

This has [[categorical homotopy groups in an (infinity,1)-topos|homotopy sheaves]] 

| $k$  | $\pi_k( 2 \mathbf{sLine})$ |
|--|--|
| 0 | $\mathbb{Z}_2$  |  
| 1 | $\mathbb{Z}_2$ |
| 3 | $\mathbb{C}^\times$ |

in the [[topos]] over [[supermanifolds]]. The $\pi_0(2 \mathbf{sLine}) \simeq \mathbb{Z}_2$ says that locally there is not just one super line 2-bundle, namely the standard line 2-bundle, but also its odd "superpartner". 

Under [[geometric realization of cohesive infinity-groupoids|geometric realization]] ${\vert-\vert} \;\colon\; \mathbf{H} \to \infty Grpd \simeq L_{whe} Top$ we have the [[homotopy type]] ${\vert 2 \mathbf{sLine}\vert}$ with [[homotopy groups]]

| $k$  | $\pi_k({\vert 2 \mathbf{sLine}\vert})$ |
|--|--|
| 0 | $\mathbb{Z}_2$  |  
| 1 | $\mathbb{Z}_2$ |
| 3 | $0$ |
| 4 | $\mathbb{Z}$ |

Since $2 \mathbf{sLine}$ is the [[Picard 3-group]] of the monoidal 2-stack $2 \mathbf{sVect}$ of super [[2-vector bundles]] it is a supergeometric [[3-group]]. Therefore there is the further [[delooping]] $\mathbf{B}2\mathbf{sLine}$ and hence the differential refinement $2\mathbf{sLine}_{conn}$ in the [[(∞,1)-pullback]] diagram

$$
  \array{
    2\mathbf{sLine}_{conn} &\to& \Omega^3_{cl}
    \\
    \downarrow && \downarrow
    \\
    2 \mathbf{sLine} &\stackrel{curv}{\to}& \flat_{dR} \mathbf{B}2 \mathbf{sLine}
  }
  \,.
$$

This is now the moduli 2-stack

$$
  \mathbf{Fields} \coloneqq 2\mathbf{2Line}_{conn}
  \;\;
  \in SmoothSuper\infty Grpd
$$

for the [[B-field]] in [[type II string theory]].


####### Supergravity $C$-field
 {#SupergravityCField}

Proceeding in this fashion, let 

$$
  \mathbf{B^3}U(1)_{conn}
  \coloneqq
  \Omega^{3 \leq \bullet \leq 1} // \mathbf{B}^2 U(1)
  \simeq
  DK(U(1) \stackrel{d log}{\to} \Omega^1 \stackrel{d}{\to} \Omega^2 \stackrel{d}{\to}\Omega^3)
$$

be the image under the [[Dold-Kan correspondence]] of the [[Deligne complex]] for degree-4 [[ordinary differential cohomology]]. This is the [[moduli infinity-stack|moduli 3-stack]] for [[circle n-bundle with connection|circle 3-bundle with connections]].

Fields whose moduli stack is

$$
  \mathbf{Fields} \;\colon\; \mathbf{B}^3 U(1)_{conn} \to *
$$ 

are one component of the [[supergravity C-field]].


##### **II)** Matter fields
 {#MatterFields}

Fundamental [[matter]]-fields as they appear in the [[standard model of particle physics]], hence fundamental [[fermions]] such as [[electrons]], [[quarks]] and [[neutrinos]], are [[sections]] of a $G$-[[associated bundle]] $E \to X$ on [[spacetime]], where $G$ is the [[gauge group]] of the [[force]] fields that interact with the matter fields and where $E \to X$ is [[associated bundle|associated]] to the [[principal bundle]] underlying such a force [[gauge field]], as discussed in _[Gauge fields](#GaugeFields)_ above, and, if we are talking indeed about fermions, to the [[spin bundle]] given by the gravity-spin structure field discussed in _[Gravity and generalized geometry](#MatterFields)_ above.

More precisely, fermioninc matter fields are sections of these bundles regarded in [[supergeometry]] with the fibers regarded as odd-graded. (...)


###### **General** -- sections of associated fiber $\infty$-bundles
 {#SectionsOfAssociatedBundles}

We start by discussing the general mechanism by which [[sections]] of $\rho$-[[associated ∞-bundles]] are an example of the general definition \ref{FieldsInAnActionFunctional}.

For $G \in \Grp(\mathbf{H})$ a geometric [[∞-group]], there is an [[equivalence of (∞,1)-categories]]

$$
  G Act \simeq \mathbf{H}_{/\mathbf{B}G}
$$

between that of [[∞-actions]] of $G$ and the [[slice (∞,1)-topos]] of $\mathbf{H}$ over the [[delooping]] $\mathbf{B}G$ of $G$. Under this equivalence an [[∞-action]]/[[∞-representation]] of $G$ on some $V \in \mathbf{H}$ is equivalently a [[homotopy fiber sequence]] of the form

$$
  \array{
    V &\to& V//G
    \\
    && \downarrow^{\overline \rho}
    \\
    && \mathbf{B}G
  }
$$ 

in $\mathbf{H}$. This is the [[universal associated ∞-bundle|universal rho-associated ∞-bundle]]: for $P \to X$ any $G$-[[principal ∞-bundle]] with modulating map $g_X \;\colon\; X \to \mathbf{B}G$ the corresponding [[associated ∞-bundle|associated]] $V$-[[fiber ∞-bundle]] is naturally equivalent to the [[(∞,1)-pullback]] of $\overline{\rho}$ along $g$:

$$
  P \times_G V \simeq g_X^*(\overline{\rho})
  \,.
$$

From this and the [[universal property]] of the [[(∞,1)-pullback]] one finds that a [[section]] of the [[associated ∞-bundle]] $P \times_G V \to X$ is equivalently a map

$$
  \phi : g_X \to \overline{\rho}
$$
  
in $\mathbf{H}_{/\mathbf{B}G}$.

This means that such sections are fields in the sense of def. \ref{FieldsInAnActionFunctional} where

* $\mathbf{BgFields} \simeq \mathbf{B}G$;

* the [[background field]] is the moduli $g_X$;

* the [[moduli ∞-stack]] of fields is $\overline{\rho} \in \mathbf{H}_{/\mathbf{B}G}$.



###### Fermions
 {#Fermions}

[[fermion]]:

$S$ a [[spin representation]]

$$
  \mathbf{Fields} 
  \;\colon\;
  S//Spin
  \to 
  \mathbf{B}Spin
$$

in [[supergeometry]] (...)

###### Tensor fields
 {#TensorFields}

While the term _physical field_ probably orignates from _[[tensor field]]_, few fields are fundamentally given by tensor fields. Nevertheless, tensor fields, being [[sections]] of a [[tensor product]] of copies of the [[tangent bundle]] and the [[cotangent bundle]] are certainly examples of the general notion of field as in def. \ref{FieldsInAnActionFunctional}. Gere we spell this out.

For $X$ a [[smooth manifold]], a [[tensor field]] of rank $(p,q)$ is a [[section]] of the [[tensor product]] bundle

$$
  \Gamma(T X)^{\otimes_{C^\infty(X)} p} \otimes_{C^\infty(X)} \Gamma(T^* X)^{\otimes q}
  \,. 
$$

This is canonically the [[associated bundle]] to the $GL(n)$-[[principal bundle]] which to which the [[tangent bundle]] is also canonically associated, by the given [[representation]] of $GL(n)$ on $\mathbb{R}^{n(p+q)}$.

The [[universal associated ∞-bundle]] of this representation is 

$\mathbf{Fields} 
\;\colon\; \mathbb{R}^{n (p+q)}//GL(n) \to \mathbf{B}GL(n) $.

Hence for $\tau_X \colon X \to \mathbf{B}GL(n)$ the canonical map, the space of $(p,q)$-tensor fields on $X$ is

$$
  [\tau_X, \mathbf{Fields}]_{\mathbf{H}}
  \in
  \mathbf{H}
  \,.
$$

By passing to [[irreducible representations]] in the above, we obtain specifically the corresponding subclasses of tensor fields, such as [[differential forms]].




##### Fields combining these properties
 {#FieldCombiningVariousProperties}

The above distinction of types of physical fields into into [Sigma-model fields](SigmaModelFields), [Force fields of gravity](#FieldsOfGravityAndGeneralizedGeometry), [Gauge force fields](#GaugeFields) and [Matter fields](#MatterFields) can be helpful for reasoning about fields and types of [[theories (physics)|theories in physics]], but is not fundamental. The general definition \ref{FieldsInAnActionFunctional} of which all these types are examples reflects that. In fact, one way to read that definition and the above list of examples is to say that it shows that in [[higher geometry]] _all_ types of fields are [[sigma-model]] fields: they are all given as maps $\Phi_X \to \mathbf{Fields}$ from a domain [[spacetime]]/[[worldvolume]]+[[background field]] $\Phi_X$ to a generalized [[target space]] $\mathbf{Fields}$ (the [[moduli ∞-stack]] of fields in the given [[slice (∞,1)-topos]] characterized by the nature of the [[background fields]]).

Accordingly, a general physical field in a general [[theory (physics)|theory]] does not fall squarely into one of the above categories, but combines aspects of all of these. Here we discuss such examples. 


###### **General** -- Twisted differential-cocycles and -$\mathbf{c}$-structures
 {#TwistedDifferentialcStructurs}

We have seen that the [[moduli ∞-stack]] of a field of plain [[gravity]] or general geometry is a map $\mathbf{c} \colon \mathbf{B}\hat G \to \mathbf{B}G$ of [[moduli ∞-stack]] of [[principal ∞-bundles]], regarded as an object in the [[slice (∞,1)-topos|slice]] $\mathbf{H}_{/\mathbf{B}G}$, and that the [[moduli ∞-stack]] of a plain $G$-[[gauge field]] is that of [[principal ∞-connections]] $\mathbf{B}G_{conn}$. These two concepts have an evident unification if $\mathbf{c}$ has a differential refinement $\at \mathbf{c}$ to a map of differential moduli stacks

$$  
  \array{
    \mathbf{B}\hat G_{conn} &\stackrel{\hat \mathbf{c}}{\to}&
   \mathbf{B}G_{conn}
     \\
     \downarrow && \downarrow
     \\
     \mathbf{B}\hat G &\stackrel{\mathbf{c}}{\to}&
     \mathbf{B}G
  }
  \,,
$$

regarded then as an object in the slice $\mathbf{H}_{/\mathbf{B}G_{conn}}$.

Since, as discussed [above](#GStructure), a field with coefficients in $\mathbf{c}$ is equivalently a _twisted $\mathbf{c}$-structure_, we may calla field with coefficients in $\hat \mathbf{c}$ a 
**[[twisted differential c-structure]]**.

Moreover, we have seen that [matter fields](#MatterFields) have 
[[moduli ∞-stacks]] coming not from a direct [[delooping]] $\mathbf{B}G \simeq *//G$ of an [[∞-group]] $G$, but from the [[homotopy quotient]] $V//G$ of an [[∞-action]] of $G$ on some object $V$. Combining this with differential refinement as above we consider fields whose [[moduli ∞-stacks]] are maps

$$
  (V//G)_{conn}
  \stackrel{\hat \mathbf{c}}{\to}
  (\mathbf{B}G)_{conn}
  \;\;\;\;
  \in \mathbf{H}_{/\mathbf{B}G_{conn}}
  \,.
$$

This is a differential refinement of fields which are [[cocycles]] in [[twisted cohomology]] with local [[coefficients]] $V$, hence **twisted differential cohomology**. The above case of [[twisted differential c-structures]] is a special case of this for $V \simeq \mathbf{B}A$ the [[delooping]] of the [[∞-group]] that [[∞-group extension|extended]] $G$ to $\hat G$.

Some further slight variants of these combinations appear in the examples below. 

###### Nonabelian charged particle trajectories -- Wilson line
 {#NonabelianChargedParticle}

We describe here a variant of the particle propagating on a spacetime $X$, where now the particle is charged under a [[background gauge field]] for a nonabelian [[gauge group]] $G$. 


Let $G$ be a [[simple Lie group]] which is connected, simply connected and [[compact Lie group|compact]].

Let $\rho$ be an [[irreducible representation|irreducible]] [[unitary representation]] of $G$ under which the particle is to be [[charge (physics)|charged]]. By the [[Borel-Weil-Bott theorem]] this corresponds equivalently to a [[weight (in representation theory)|weight]]

$$
  \langle \lambda, -\rangle
  \in
  \mathfrak{g}^*
  \,.
$$

Let $T \simeq G_\lambda \hookrightarrow G$ be the [[maximal torus]] which is the [[stabilizer subgroup]] that fixes this weight under the [[coadjoint action]] of $G$ on its dual [[Lie algebra]] $\mathfrak{g}^*$.

Set then in def. \ref{FieldsInAnActionFunctional} the [[moduli stack]] of [[background fields]] to be 

$$
  \mathbf{BgField} \colon \Omega^1(-,\mathfrak{g})//G \simeq \mathbf{B}G_{conn}
  \;\;\;
  \mathbf{H}
$$

as in def. \ref{ModuliStackOfGPrincipalConnection}. Moreover, let the moduli $\infty$-stack of fields in $\mathbf{H}_{/\mathbf{B}G_{conn}}$ be given by the canonical map

$$
  \mathbf{Fields} 
  \;\colon\;
  \Omega^1(-,\mathfrak{g})//T
  \to 
  \Omega^1(-,\mathfrak{g})//G
  \simeq
   \mathbf{B}G_{conn}
$$

which is induced by the defining inclusion of $T$.

+-- {: .num_remark}
###### Remark

For $U \in$ [[CartSp]] $\hookrightarrow \mathbf{H}$ a field $\phi \colon U \to \Omega^1(-,\mathfrak{g})//T$ is equivalently a [[Lie algebra valued form]] $A \in \Omega^1(U,\mathfrak{g})$, but a [[gauge transformation]] of such a field is constrained to be a smooth $T$-valued function $t \in C^\infty(U,T) \hookrightarrow C^\infty(U, G)$ instead of an arbitrary $G$-valued function.

=--

+-- {: .num_remark}
###### Remark

With these definitions we have for $X$ a [[manifold]] that

* a [[background gauge field]] $\Phi_X \;\colon\; X \to \mathbf{B}G_{conn}$ is equivalently a $G$-[[principal connection]] on $X$ (which if $G$ is assumed connected and simply connected and $\Sigma$ is of [[dimension]] at most 3 is equivalently just a [[Lie algebra valued form]]);

* a field configuration is a diagram in $\mathbf{H}$ of the form

  $$
    \array{  
      X &&\stackrel{\nabla^g}{\to}&& \Omega^1(-,\mathfrak{g})//T
      \\
      & {}_{\nabla}\searrow &\swArrow_{g}& \swarrow_{\mathrlap{\mathbf{Fields}}}
      \\
      && \mathbf{B}G_{conn}
    }
    \,,
  $$
  
  which is equivalently a differentially refined [[reduction of the structure group]] of the $G$-[[principal bundle]] underlying $\nabla$. If $\nabla$ is given by a globally defined connection form $A$ then this is equivalently just a smooth $G$-valued function $g$ on $X$ that takes $A$ to $A^g$ as indicated. 

=--

As a slight variant of prop. \ref{CosetIsHomotopyFiberOfDeloopedInclusion} we have

+-- {: .num_prop}
###### Proposition

We have a [[homotopy fiber sequence]]

$$
  \mathcal{O}_\lambda \simeq G/T \to \Omega^1(-,\mathfrak{g})//T
  \stackrel{\mathbf{Fields}}{\to} \mathbf{B}G_{conn}
  \,,
$$

where on the left we have the [[coadjoint orbit]] of $\langle \lambda , -\rangle$.

=--

+-- {: .num_remark}
###### Remark

This implies that if $\nabla = 0$ is the trivial background field, than fields $\phi : X \to \mathbf{Fields}$ are equivalently maps to the coadjoint orbit

$$
  [X, \mathbf{Fields}]_{\mathbf{H}}|_{\Phi_X = 0}
  \simeq
  C^\infty(X, \mathcal{O}_\lambda)
  \,.
$$

Hence in this sector we have simply a [[sigma-model]] field as in [Sigma-models](#SigmaModelFields) above. 

=--


+-- {: .num_remark}
###### Remark

There is a canonical [[extended Lagrangian]] on $[X, \mathbf{Fields}]_{\mathbf{H}}$ with the above definitions, whose [[action functional]], if $X = S^1$ is the closed connected 1-dimensional manifold,  is that of a [[1d Chern-Simons theory]]. The [[partition function]] of the corresponding [[quantum field theory]] is the [[holonomy]] map  -- the "[[Wilson line]]" -- on the background gauge field connection $\nabla$.

=--

This is discussed further at [geometry of physics -- Prequantum gauge theory and gravity](#ActionFunctionalsForChernSimonsTypeGaugeTheories).



###### 3d Chern-Simons field with Wilson line
 {#ChernSimonsWithWilsonLines}

We discuss the field content of 3d [[Chern-Simons theory]] for a simple, simply connected compact Lie group with [[Wilson loops]].
This is an example of _[Bulk fields with defect fields](#BoundaryAndDefectFields)_.

Let $\Sigma_3 \in SmthMfd \hookrightarrow \mathbf{H}$ be a [[smooth manifold]] of [[dimension]] 3, and let

$$
  C_X \;\colon\; S^1 \to \Sigma^3
$$

be the [[submanifold|embedding]] of a [[knot]]. Let the moduli of fields be

$$
  \mathbf{Fields}
  : 
  \Omega^1(-,\mathfrak{c})//T \to \mathbf{B}G_{conn}
$$

as defined in _[Nonabelian charged particle trajectories -- Wilson lines](#NonabelianChargedParticle)_ above. Regarding the not inclusion as a defect in the 3-dimnensional manifold, a bulk-defect fiedl configuration according to def. \ref{ModuliOfBulkAndBoundaryFields} is a map

$$
  \phi 
   \;\colon\;
   C_X \to \mathbf{Fields}
$$

in $\mathbf{H}^{(\Delta^1)}$. This is equivalently a diagram

$$
  \array{
    S^1 &\stackrel{A|_{S^1}^g}{\to}& \Omega^1(-,\mathfrak{g})//T
    \\
    \downarrow^{\mathrlap{C}} &\swArrow_{g}& \downarrow
    \\
    \Sigma_3 &\stackrel{A}{\to}& \mathbf{B}G_{conn}
  }
$$

in $\mathbf{H}$. This in turn is equivalently

1. a [[Lie algebra valued form]] $A \in \Omega^1(\Sigma_3, \mathfrak{g})$ (the bulk [[gauge field]] of $G$-[[Chern-Simons theory]])

1. a $g$-valued function on the circle $g \in C^\infty(S^1, G)$

which determine a background gauge field $A|_{S^1}^g$ on the knot.

Moreover a [[gauge transformation]] between two such field configurations $\kappa \;\colon\; \phi \Rightarrow \phi'$ is equivalently a gauge transformaiton of $A$ and of $A|_{S^1}$ such that together they intertwine $g$ and $g'$. In particular if the bulk field is held fixed, then such a gauge transformation is a function $t \colon S^1 \to T$ such that $g' = t g$. This means that the gauge equivalence classes of field confiurations for fixed background gauge field are labeled by maps to the [[coadjoint orbit]] $\mathcal{O}_\lambda \simeq G/T$ as above.

This are the field confugurations for 3d [[Chern-Simons theory]] (see the discussion there) with Wilson lines ([FSS](#FSS)).


###### Chan-Paton gauge fields on D-branes: twisted differential K-cocycles
 {#ChanPatonGaugeFields}

We discuss the [[Chan-Paton gauge fields]] over [[D-branes]]
in [[type II string theory]].

The [[extension of groups]] $U(1) \to U(n) \to PU(n)$ sits in a long [[homotopy fiber sequence]] of $\infty$-stacks

$$
  U(1) \to U(n) \to PU(n) \to \mathbf{B}U(1)
  \to \mathbf{B}U(n) \to \mathbf{B}PU(n) \stackrel{\mathbf{dd}_n}{\to}
  \mathbf{B}^2 U(1)
$$

Let

$$
  \mathbf{Fields}
  \colon
  (\mathbf{B}U(n)//\mathbf{B}U(1))_{conn}
  \to
  \mathbf{B}^2 U(1)_{conn}
$$

be the differential refinement of that universal [[Dixmier-Douady class]].

Let 

$$
  \iota_X   
    \;\colon\;
  Q \hookrightarrow X 
$$

be a [[submanifold]], to be thought of as a [[D-brane]] [[worldvolume]] in an ambient [[spacetime]] $X$.

 
Then a field configuration of the [[B-field]] on $X$ together with a compatible rank-$n$ gauge field on the [[D-brane]] is a map

$$
  \iota_X \to \mathbf{Fields}
$$

in $\mathbf{H}^{(\Delta^1)}$, hence a diagram in $\mathbf{H}$ of the form

$$
  \array{
    Q &\stackrel{}{\to}& (\mathbf{B}U(n)//\mathbf{B}U(1))
    \\
    {}^{\iota_X}\downarrow &\swArrow_{\simeq}& \downarrow^{\mathrlap{\hat \mathbf{dd}_n}}
    \\
    X &\stackrel{\nabla_B}{\to}& \mathbf{B}^2 U(1)_{conn}
  }
$$

This identifies a  [[twisted bundle]] with connection on the D-brane whose twist is the class in $H^3(X, \mathbb{Z})$ of the bulk [[B-field]]. 

This relation is the Kapustin-part of the [[Freed-Witten-Kapustin anomaly]] cancellation for the [[bosonic string]] or else for the [[type II string]] on $Spin^c$ D-branes. ([FSS](#FSS))


+-- {: .num_remark }
###### Remark

If we regard the [[B-field]] as a [[background field]] for the [[Chan-Paton gauge field]], then remark \ref{PullbackAlongGeneralizedLocalDiffeomorphisms} determines along which maps of the B-field the Chan-Paton gauge field may be transformed. 

$$
  \array{
    Y &\stackrel{}{\to}& X &\stackrel{}{\to}& (\mathbf{B}U(n)//\mathbf{B}U(1))_{conn}
    \\
    & \searrow & \downarrow & \swarrow
    \\
    &&\mathbf{B}^2 U(1)_{conn}
  }
  \,.
$$

On the local connection forms this acts as

$$
  A \mapsto A + \alpha
  \,.
$$

$$
  B \mapsto B + d \alpha
$$

This is the famous gauge transformation law known from the string theory literature.

=--


###### Anomaly-free heterotic string background: differential $String^c$-structure
 {#HeteroticStringBackgroundField}

Let

$$
  \mathbf{Fields}
  \;\colon\;
  \mathbf{B}Spin_{conn}
  \stackrel{\tfrac{1}{2}\hat \mathbf{p}_1}{\to}
  \mathbf{B}^3 U(1)_{conn}
$$

Let 

$$
  \Phi_X \;\colon\; X \stackrel{g_X}{\to} \mathbf{B}(E_8 \times E_8)_{conn}
  \stackrel{\hat \mathbf{c}_2}{\to}
  \mathbf{B}^3 U(1)
$$

then fields are [[twisted differential string structures]] or equivalently
differential $\mathbf{String}^{\mathbf{c}}$-structure with underlying gauge bundle give by $\Phi_X$, the differential refinement of the discussion in _[Higher spin structure](#HigherSpinStructures)_ above. 

As in the discussion there, we implement the constraint that the string structure is on the tangent bundle $\tau_X \;\colol\; X \to \mathbf{B}GL(n)$ of the manifold by settting

$$
  \mathbf{Fields}
  \;\colon\;
  \mathbf{B}Spin_{conn}
  \stackrel{(p,\tfrac{1}{2}\hat \mathbf{p}_1)}{\to}
  \mathbf{B}GL(n)_conn \mathbf{B}^3 U(1)_{conn}
$$

and

$$
  \Phi_X
  \;\colon\;
  X
  \stackrel{(\nabla_X, \hat \mathbf{c}_2(g_X))}{\to}
  \mathbf{B}GL(n)_{conn} \times \mathbf{B}^3 U(1)_{conn}
  \,.
$$

Then a field $\phi \;\colon\; \Phi_X \to \mathbf{Fields}$ 
is the higher spin-connection version as discussed in _[Gravity](#OrdinaryGravity)_ above of a twisted differential string structure.

The moduli stack of these fields is that of background fields that satisfy the [[Green-Schwarz anomaly cancellation]] in [[heterotic supergravity]]. ([SSS](#SSS)).


## **Lagrangians and Action functionals**
 {#LagrangiansAndActionFunctionals}

### Model layer

* [[Lagrangian]], [[action functional]]

### Semantics layer

* [[extended Lagrangian]], [[extended prequantum field theory]]

### Syntactic layer

(...)


## **Equations of motion**
 {#EquationsOfMotion}
 
Above in _[Lagrangians and Action functionals](#LagrangiansAndActionFunctionals)_ we discussed [[prequantum field theory]]. Given such there are two directions to go: to the corresponding _[[classical field theory]]_ and to a corresponding _[[quantum field theory]]_.

The classical field theory is the study of the _[[critical locus]]_ of the [[action functional]], whose points are the solutions to the _([[Euler-Lagrange equations|Euler-Lagrange]]-)[[equations of motion]]_ of the system, the conditions which characterize those [[field (physics)|field configurations]] that are "physically realized" as asserted by the [[physical theory]] that is encoded by the [[action functional]]. If the [[action functional]] comes from a [[local Lagrangian]] then this space carries a canonical [[presymplectic form]] and equipped with this form it is called the _[[covariant phase space]]_ of the system.

(The term "classical" originates from the time when [[quantum mechanics]] was discovered at the beginning of the 20th century. All of the physics that was known until the end of the 19th centure was then called "classical" to distinguish it from the new refinement to [[quantum theory]]. Nowadays the term has, strictly speaking, lost its original sense, since nowadays quantum theory is entirely "classical", but "classical physics" will forever refer to non-quantum physics. )

Here we first discuss the traditional theory of classical equations of motion. Maybe the archetypical example is the [[geodesic equation]] which describes the [[trajectories]] of [[particles]] and of [[light]]. Standard examples of [[equations of motion]] for [[spacetime]] [[force]] [[field (physics)|fields]] are _[[Maxwell equations]]_ and _[[Einstein equations]]_, describing the classical [[dynamics]] of the [[electromagnetic field]] and [[gravity]], respectively.

Then we reformulate this more abstractly in [[higher geometry]]. This yields a notion of _[[derived critical loci]]_ of action functionals for which the _[[BV-BRST formalism]]_ is a model, a traditional machinery for handling [[covariant phase spaces]] while taking care of [[gauge symmetry]] and resolving singularities in the critical locus. 

Moreover, we discuss how, when interpreted in _[[extended prequantum field theory]]_, the equations of motion are just the [[codimension]]-0 piece of a tower of notions which in codimension 1 is the notion of _[[Lagrangian submanifolds]]_ of [[phase space]].


+-- {: bluebox}
###### Contents: ######

1. [Model layer](#EquationsOfMotionModelLayer)

   Here we discuss the traditional theory of _[[covariant phase spaces]]_ and the traditional model of their resolution in higher geometry: _[[BV-BRST formalism]]_.

1. [Semantics layer](#EquationsOfMotionSemanticsLayer)

   Here we give a general abstract formulation of higher ("[[derived critical locus|derived]]") [[critical loci]] in a [[cohesive (∞,1)-topos]].

1. [Syntax layer](#EquationsOfMotionSyntaxLayer)

=--

### Model layer
 {#EquationsOfMotionModelLayer}

#### Traditional covariant phase space
 {#TradtionalCovariantPhaseSpace}

We had already discussed traditional [Variational calculus above](#VariationalCalculus). Using this we find:

* [[covariant phase space]]

#### Higher geometric covariant phase space: BV-BRST formalism

* [[BV-BRST formalism]]


### Semantics layer
 {#EquationsOfMotionSemanticsLayer}

+-- {: bluebox}
###### Contents: ######

1. [Critical loci](#0PlecticLagrangianSubspaces)


=--

#### Critical loci


We now discuss the general abstract formulation of [[critical loci]] of [[action functionals]] in the context of a [[cohesive (∞,1)-topos]]. This generalizes the traditional formulation to critical loci inside higher [[moduli ∞-stacks]] of field configuration. In particular, if the ambient [[(∞,1)-topos]] is not [[n-localic (infinity,1)-topos|1-localic]], then this gives a general abstract formulation of _[[derived critical loci]]_.

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]] $(\mathbf{\Pi} \dashv \flat \dashv \sharp) : \mathbf{H} \to \mathbf{H}$ equipped with [[differential cohesion]] $(Red \dashv \mathbf{\Pi}_{inf} \dashv \flat_{inf}) \;\colon\; \mathbf{H} \to \mathbf{H}$. 
We discuss the formalization of [[critical loci]] of [[action functionals]] and of [[equations of motion]] in this context.

Fix 

$$
  \mathbf{Fields} \in \mathbf{H}
$$ 

an object that serves as the [[moduli ∞-stack]] of [[physical fields]] for the [[theory (physics)|theory]] to be considered, as discussed in _[Fields](#Fields)_ above

+-- {: .num_defn #VariationFixedOnBoundary}
###### Definition

For $\Sigma \in Mfd_{bdr} \hookrightarrow \mathbf{H}$ a [[manifold with boundary]] in $\mathbf{H}$, def. \ref{ManifoldWithBoundaryInSemLayer}, write $[\Sigma,\mathbf{Fields}]_{\partial \Sigma} \in \mathbf{H}$ for the [[(∞,1)-pullback]]

$$
  \array{
    [X, \mathbf{Fields}]_{\partial \Sigma}
    &\to&
    \flat [\partial \Sigma, \mathbf{Fields}]
    \\
    \downarrow && \downarrow
    \\
    [\Sigma, \mathbf{Fields}]
    &\to&
    [\partial \Sigma, \mathbf{Fields}]
  }
  \,,
$$

where the right vertical morphism is the [[unit of a monad|counit]] of $\flat$ and where the bottom morphism is the image of the [[boundary]] inclusion $\partial \Sigma \to \Sigma$ under the [[internal hom]] $[-, \mathbf{Fields}]$.

=--

+-- {: .num_remark }
###### Rermark

This implies that for any geometrically contractible $U \in \mathbf{H}$, def. \ref{ShapeTerminology}, then we have

$$
  \mathbf{H}(U, [\Sigma, \mathbf{Fields}_{\partial \Sigma}])
  \simeq
  \mathbf{Fields}(\Sigma \times U)
  \underset{\mathbf{Fields}((\partial \Sigma) \times U)}{\times}
  \mathbf{Field}(\partial \Sigma)
  \,.
$$

This means that a variation in $[\Sigma, \mathbf{Fields}]_{\partial \Sigma}$ is a variation in $[\Sigma, \mathbf{Fields}]$ which remains constant over the boundary of $\Sigma$.

=--

Fix now 

$$
  \mathbb{G} \in Grp(\mathbf{H})
$$ 

a [[group object in an (∞,1)-category|group object]], hence a cohesive [[∞-group]], to be the object that the [[action functional]] is to take values in. In $\mathbf{H} = $ [[Smooth∞Grpd]] the standard choice is $\mathbb{G} = U(1)$, the [[circle group]], for "exponentiated action functionals" or $\mathbb{R} = \mathbb{R}$, the additive Lie group of [[real numbers]].



+-- {: .num_defn #VariationalDerivativeInCohesiveInfinityTopos}
###### Definition

For $S \;\colon\; [\Sigma, \mathbf{Fields}] \to \mathbb{G}$ a map, the **[[variational derivative]]** of $S$ is the restriction of the [[de Rham differential]] $S^{-1}\mathbf{d}S$ of def. \ref{DifferentiationOfInfinityGroupValuedFunction} to variations that keep the boundary data fixed as in def. \ref{VariationFixedOnBoundary}, hence the composite

$$
  S^{-1}\mathbf{d}_{var} S
  \;\colon\;
  [\Sigma, \mathbf{Fields}]_{\partial \Sigma}
  \to
  [\Sigma, \mathbf{Fields}]
  \stackrel{S}{\to}
  \mathbb{G}
  \stackrel{\theta_{\mathbb{G}}}{\to}
  \flat_{dR}\mathbf{B}\mathbb{G}
  \,.
$$

Since the variational context is clear from the domain of the map, we will often just write $S^{-1} \mathbf{d} S$ for $S^{-1} \mathbf{d}_{var} S$, for convenience.


=--

+-- {: .num_remark }
###### Remark

Under coreflection into [[structure sheaves]], def. \ref{StructureSheafInPetitTopos}, this induces a map

$$
  S^{-1}\mathbf{d}_{var} S
  \;\colon\;
  [\Sigma, \mathbf{Fields}]_{\partial \Sigma}
  \to 
  \mathcal{O}_{\Sigma}(\flat_{dR} \mathbf{B}G)
$$

in $Sh_{\mathbf{H}}(X)$,
which we will denote by the same symbol, as here, when the context is clear.
Since $\mathcal{O}_X(\flat_{dR} \mathbf{B}\mathbb{G})$ has the interpretation of the _sheaf of flat $Lie(\mathbb{G})$-valued forms_ on $X$, this may be thought of as realizing $\mathbf{d} S$ as a [[section]] of the [[tangent bundle]] over $X$.

=--

+-- {: .num_defn #CriticalLocusInCohesiveInfinityTopos}
###### Definition

For $S \;\colon\; [\Sigma, \mathbf{Fields}] \to \mathbb{G}$ a map in $\mathbf{H}$, its **[[critical locus]]** 

$$
  \underset{\phi \in [\Sigma, \mathbf{Fields}]_{\partial \Sigma}}{\sum}
  \left(S^{-1}\mathbf{d}_{var}S_{\phi} \simeq 0\right)
  \;\;\;\;
  \in 
  \mathbf{H}
$$

is the [[homotopy fiber]] of the [[variational derivative]] $S^{-1} \mathbf{d}S$ over the 0-section, hence the [[(∞,1)-pullback]]

$$
  \array{
    \underset{\phi \in [\Sigma, \mathbf{Fields}]_{\partial \Sigma}}{\sum}
    \left(S^{-1}\mathbf{d}_{var}S_{\phi} \simeq 0\right)
    &\to&
    0
    \\
    \downarrow && \downarrow
    \\
    [\Sigma, \mathbf{Fields}]_{\partial \Sigma}
    &\stackrel{S^{-1}\mathbf{d}_{var} S}{\to}&
    \mathcal{O}_X(\flat_{dR}\mathbf{B}\mathbb{G}) 
  }
$$

in the [[petit (∞,1)-topos]] $Sh_{\mathbf{H}}(X)$.

=--


+-- {: .num_remark }
###### Remark

In [[extended prequantum field theory]] we may, as discussed in _[Lagrangians and Action functionals](#LagrangiansAndActionFunctionals)_, think of the [[action functional]] $S$ as being the [[prequantum 0-bundle]]. In this perspective the variational derivative $S^{-1} \mathbf{d}_{var} S$ of def. \ref{VariationalDerivativeInCohesiveInfinityTopos} is the [[curvature]] of this 0-bundle. If $\mathbb{G}$ is a 1-group such as $U(1)$ then this is a [[differential 1-form]] which is the _[[n-plectic geometry|0-plectic]]_ form. This means that the [[critical locus]] in def. \ref{CriticalLocusInCohesiveInfinityTopos} the maximal subspace on which the 0-plectic 1-form vanishes.

=--



### Syntax layer
 {#EquationsOfMotionSyntaxLayer}



As the notation above suggests, the [[critical locus]] of 
the [[function]] $S\;\colon\; [X, \mathbf{Fields}] \to \mathbb{G}$ is syntactically
indeed the [[dependent sum]] over the type of fields
of the [[identity type]] of the variational derivative 
$S^{-1}\mathbf{d} S \in Sh_{\mathbf{H}}(X)$ and the 0-term in
$Sh_{\mathbf{H}}(X)$. This is indeed the standard expression in 
[[type theory]] which formalizes the variations equation of motion:

"The collection of fields for which the variational derivative equals zero." translates exactly into $\underset{\phi \in [X, \mathbf{Fields}]}{\sum} (S^{-1}\mathbf{d}S \simeq 0)$.

## **Classical mechanics via prequantized Lagrangian correspondences**
 {#ClassicalMechanicsByPrequantizedLagrangianCorrespondences}

The following is effectively a derivation of, and an introduction to, [[classical mechanics]] by studying [[correspondences]] in what is called (as we will explain) the _[[slice topos]] over the [[moduli stack]] of [[prequantum line bundles]]_. One such correspondence in this slice topos is precisely a _[[prequantized Lagrangian correspondence]]_ and the reader looking for just these should skip ahead to the section _[The classical action functional prequantizes Lagrangian correspondences](#TheClassicalActionFunctionalPrequantizesHamiltonianCorrespondences)_. But for completeness and to introduce the technology used here, we start with introducing also more basic concepts, such as [[phase space]] etc.

### Phase spaces and symplectic manifolds
 {#PhaseSpaceAndSymplecticManifolds}

Given a [[physical system]], one says that its _[[phase space]]_ is the
space of its possible ("classical") histories or _[[trajectories]]_. 
The first two of [[Newton's laws of motion]] say that [[trajectories]] of [[physical systems]] are (typically) determined by [[differential equations]] of  _second_ order, and therefore these spaces of trajectories are (typically) equivalent to initial value data of 0th and of 1st derivatives. In [[physics]] this data (or rather its linear dual) is referred to as the _[[canonical coordinates]]_ and the _[[canonical momenta]]_, respectively, traditionally denoted by the symbols "$q$" and "$p$". 
But being [[coordinates]], these are actually far from being canonical in the mathematical sense; all that has invariant meaning is, locally, the surface element $\mathbf{d}p \wedge \mathbf{d}q$ spanned by a change of coordinates and momenta.

So far this says that a physical phase space is mathematically formalized
by a sufficiently [[smooth manifold]] $X$ which is equipped with a closed
and non-degenerate [[differential 2-form]] $\omega  \in \Omega^2_{\mathrm{cl}}(X)$, hence by a [[symplectic manifold]] $(X,\omega)$.

But if the [[mechanical system]], and hence the [[differential equations]]
that describe it, is subject to [[constraints]], then the full [[phase space]] is [[foliation|foliated]] by unconstrained phase spaces in the above sense and so the  above surface element may be any closed 2-form, not necessarily non-degenerate. This is a _[[pre-symplectic manifold]]_ $(X,\omega)$ and this is the generality considered in the following discussion: a _[[phase space]]_ is a _[[pre-symplectic manifold|pre-symplectic]] [[smooth manifold]]_.



+-- {: .num_example #CanonicalR2PhaseSpace}
###### Example

The [[sigma-model]] describing the propagation of a [[particle]] on the [[real line]] $\mathbb{R}$ has as [[phase space]] the [[plane]] $\mathbb{R}^2 = T^\ast \mathbb{R}$ and as [[symplectic form]] its canonical [[volume form]]. Traditionally the two canonical [[coordinate functions]] on this phase space are denoted $q,p \;\colon\; \mathbb{R}^2 \longrightarrow \mathbb{R}$ (called the "[[canonical coordinate]]" and the "[[canonical momentum]]", respectively), and in terms of these the symplectic form in this example is $\omega = \mathbf{d} q \wedge \mathbf{d} p$.

=--

When dealing with spaces $X$ that are equipped with extra structure, such as  $\omega \in \Omega^2_{\mathrm{cl}}(X)$, then it is useful to have 
a _universal [[moduli space]]_ for these structures, and this will be central for our developments here. 
So we need a "[[smooth space]]" $\mathbf{\Omega}^2_{\mathrm{cl}}$ of sorts, characterized by the property that  there is a [[natural bijection]] between smooth closed differential  2-forms $\omega \in \Omega^2_{\mathrm{cl}}(X)$ and [[smooth maps]]
$
    X \longrightarrow \mathbf{\Omega}^2_{\mathrm{cl}}
$.
Of course such a universal moduli spaces of closed 2-forms does not exist in the  [[category]] of [[smooth manifolds]]. But it does exist canonically if we  slightly generalize the notion of "smooth space" suitably. 

+-- {: .num_defn}
###### Definition

A _[[smooth space]]_ or _smooth 0-type_ $X$ is 

1. an assignment to each $n \in \mathbb{N}$ of a  set, to be written $X(\mathbb{R}^n)$ and to be called the  _set of smooth maps from $\mathbb{R}^n$ into $X$_,

1. an assignment to each ordinary smooth function $f : \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ between Cartesian spaces of  a function of sets $X(f) : X(\mathbb{R}^{n_2}) \to X(\mathbb{R}^{n_1})$, to be called the _pullback of smooth functions into $X$ along $f$_;

such that

1. this assignment respects composition of smooth functions;

1. this assignment respects the [[covering]] of [[Cartesian spaces]] by [[open disks]]: for every [[good open cover]] $\{\mathbb{R}^n \simeq U_i \hookrightarrow \mathbb{R}^n\}_i$, the set $X(\mathbb{R}^n)$ of smooth functions out of $\mathbb{R}^n$ into $X$ is in natural bijection with the set $\left\{ (\phi_i)_i \in \prod_i X(U_i) \;|\;  \forall_{i,j}\; \phi_i|_{U_{i} \cap U_j}   = \phi_j|_{U_{i} \cap U_j} \right\}$ of tuples of smooth functions out of the patches of the cover which agree on all intersections of two patches.

=--

For more on this see at _[[geometry of physics]]_ in the section _[Smooth spaces](geometry%20of%20physics#SmoothSpaces)_.

While the formulation of this definition is designed to make transparent its geometric meaning, of course equivalently but more abstractly this says the following:

+-- {: .num_defn}
###### Definition

 Write [[CartSp]] for the [[category]] of [[Cartesian spaces]] with 
[[smooth functions]] between them, and consider it as a [[site]] by equipping it with the [[coverage]] of [[good open covers]]. 
A _[[smooth space]]_ or _smooth 0-type_ is a [[sheaf]] on this site. 
The _[[topos]] of smooth 0-types_ is the [[category of sheaves]]
  $$
    \mathrm{Smooth}0\mathrm{Type} \coloneqq \mathrm{Sh}(\mathrm{CartSp})
	\,.
  $$

=--

In the following we will abbreviate the notation to
$$
  \mathbf{H} \coloneqq \mathrm{Smooth}0\mathrm{Type}
  \,.
$$

For the discussion of presymplectic manifolds, we need the following two 
examples.

+-- {: .num_example}
###### Example

  Every smooth manifold $X \in \mathrm{SmoothManifold}$ becomes
  a smooth 0-type by the assignment 
  $$
    X : n \mapsto C^\infty(\mathbb{R}^n, X)
	\,.
  $$
  This construction extends to a [[full subcategory|full embedding]]
  of [[smooth manifolds]] into [[smooth spaces]]
  $$
    SmoothManifold
    \hookrightarrow
    \mathbf{H}
  $$

=--

+-- {: .num_example}
###### Example

  For $p \in \mathbb{N}$, write $\mathbf{\Omega}^p_{\mathrm{cl}}$
  for the smooth space given by the assignment
  $$
    \mathbf{\Omega}^p_{\mathrm{cl}} : n \mapsto \Omega^p_{\mathrm{cl}}(\mathbb{R}^n)
  $$
  and by the evident pullback maps of differential forms.

=--

For more see at _[[geometry of physics]]_ in the section _[Differential forms](geometry%20of%20physics#DifferentialForms)_.


This solves the [[moduli problem]] for closed smooth differential forms:


+-- {: .num_prop #PresymplecticFormsAsMapsIntoASmoothSpace}
###### Proposition

  For $p \in \mathbb{N}$
  and $X \in SmoothManifold \hookrightarrow Smooth0Type$, 
  there is a [[natural bijection]]
  $$
    \mathbf{H}(X,\mathbf{\Omega}^p_{\mathrm{cl}})
	\simeq
	\Omega^p_{\mathrm{cl}}(X)
	\,.
  $$

=--

So a presymplectic manifold $(X,\omega)$ is equivalently a map of smooth spaces of the form
$$
  \omega \;\colon\;
    X \longrightarrow \mathbf{\Omega}^2_{\mathrm{cl}}
  \,.
$$

### Canonical transformations and symplectomorphisms

An [[equivalence]] between two [[phase spaces]], hence a re-expression
of the "canonical" coordinates and momenta, is called a 
_[[canonical transformation]]_ in [[physics]]. Mathematically this is
a _[[symplectomorphism]]_.

+-- {: .num_defn}
###### Definition

Given two [[symplectic manifolds]] $(X_1, \omega_1)$ and $(X_2, \omega_2)$ (which might well be two copies of one single symplectic manifold), a _[[symplectomorphism]]_ between them

$$
  f \;\colon\; (X_1, \omega_1) \longrightarrow (X_2, \omega_2)
$$

is a [[diffeomorphism]]

$$
  f \;\colon\; X_1 \longrightarrow X_2
$$

of the underlying [[smooth manifolds]], such that the [[pullback of differential forms|pullback]] of the second [[symplectic form]] along $f$ equals the first, 

$$
  f^\ast \omega_2 = \omega_1
  \,.
$$

=--


The above formulation of pre-symplectic manifolds as maps into a [[moduli space]] of closed [[differential 2-forms]] yields the following formulation of symplectomorphisms,  which is very simple in itself, 
but contains in it the seed of an important phenomenon:


+-- {: .num_prop}
###### Proposition

A [[symplectomorphism]] $f \colon (X_1, \omega_2) \longrightarrow (X_2, \omega_2)$ as above is, under the identification of prop. \ref{PresymplecticFormsAsMapsIntoASmoothSpace}, equivalently a [[commuting diagram]] in $\mathbf{H}$ of the form

$$
  \array{
    X_1 && \stackrel{f}{\longrightarrow}&& X_2
    \\
    & {}_{\mathllap{\omega_1}}\searrow && \swarrow_{\mathrlap{\omega_2}}
    \\
    && \Omega^2_{cl}
  }
  \,.
$$

=--

Situations like this are naturally interpreted in a _[[slice topos]]_:

+-- {: .num_defn #TheSliceTopos}
###### Definition

For $A \in \mathbf{H}$ any [[smooth space]],
  the _[[slice topos]]_  $\mathbf{H}_{/A}$ is the [[category]] whose
  [[objects]] are objects $X \in \mathbf{H}$ equipped with [[maps]]
  $X \to A$, and whose [[morphisms]] are [[commuting diagrams]] in $\mathbf{H}$
  of the form
  $$
    \array{
      X &&\longrightarrow&& Y
      \\
      & \searrow && \swarrow
      \\
      && A
    }
  $$

=--

Hence if we write $\mathrm{SymplManifold}$ for the category of smooth pre-symplectic manifolds and symplectomorphisms betwen them, then we have the following.


+-- {: .num_prop #SymplecticManifoldsAsObjectsInSliceOverModuliOf2Forms}
###### Proposition


   The construction of
  prop. \ref{PresymplecticFormsAsMapsIntoASmoothSpace} constitutes a
  full embedding
  $$
     SymplManifold 
     \hookrightarrow 
     \mathbf{H}_{/\mathbf{\Omega}^2_{\mathrm{cl}}}
  $$
  of pre-symplectic manifolds with symplectomorphisms between them into 
  the slice topos of smooth spaces over the smooth moduli space of
  closed differential 2-forms.

=--

### Trajectories and Lagrangian correspondences
 {#TrajectoriesAndLagrangianCorrespondences}

A [[symplectomorphism]] clearly puts two [[symplectic manifolds]] "in _[[relation]]_" to each other. But it does so also in the formal sense of [[relations]] in mathematics. Recall:

+-- {: .num_defn}
###### Definition

For $X,Y \in $ [[Set]] two [[sets]], a [[relation]] $R$ between [[elements]] of $X$ and [[elements]] of $Y$ is a [[subset]] of the [[Cartesian product]] set 

$$
  R \hookrightarrow X \times Y
  \,.
$$

More generally, for $X, Y \in \mathbf{H}$ two [[objects]] of a [[topos]] (such as the topos of [[smooth spaces]]), then a [[relation]] $R$ between them is a [[subobject]] of their [[Cartesian product]]

$$
  R \hookrightarrow X \times Y
  \,.
$$

=--

In particular any [[function]] induces the [[relation]] "$y$ is the image of $x$":

+-- {: .num_example}
###### Example

For $f \;\colon\; X \longrightarrow Y$ a [[function]], its _induced relation_ is the [[relation]] which is exhibited by the [[graph of a function|graph]] of $f$

$$
  graph(f) 
    \coloneqq 
  \left\{
    (x,y) \in X \times Y \;|\; f(x) = y
  \right\}
$$

canonically regarded as a subobject 

$$
  graph(f) \hookrightarrow X \times Y
  \,.
$$

=--

Hence in the context of classical mechanics, in particular any [[symplectomorphism]] $f \;\colon\; (X_1, \omega_1) \longrightarrow (X_2, \omega_2)$ induces the relation 

$$
  graph(f) \hookrightarrow X_1 \times X_2
  \,.
$$

Since we are going to think of $f$ as a kind of "physical process", it is useful to think of the [[smooth space]] $graph(f)$ here as the _space of [[trajectories]]_ of that process. To make this clearer, notice that we may equivalently rewrite every [[relation]] $R \hookrightarrow X \times Y$ as a [[diagram]] of the following form:

$$
  \array{
     && R
      \\
     & {}^{\mathllap{i_X}}\swarrow && \searrow^{\mathrlap{i_Y}}
    \\
    X && && Y
  }
  \;\;
  = 
  \;\;
  \array{
     && R
     \\
     && \downarrow
     \\
     && X \times Y
      \\
     & {}^{\mathllap{p_X}}\swarrow && \searrow^{\mathrlap{p_Y}}
    \\
    X && && Y
  }
$$

reflecting the fact that every [[element]] $(x \sim y) \in R$ defines an element $x = i_X(x \sim y) \in X$ and an element $y = i_Y(x \sim y) \in Y$. 

Then if we think of $R = graph(f)$ we may read the relation as "there is a trajectory from an incoming configuration $x_1$ to an outgoing configuration $x_2$"

$$
  \array{
    && graph(f)
    \\
    & {}^{\mathllap{incoming}}\swarrow && \searrow^{\mathrlap{outgoing}}
    \\
    X_1 && && X_2
  }
  \,.
$$

Notice here that the defining property of a relation as a [[subset]]/[[subobject]] translates into the property of [[classical physics]] that there is _at most one trajectory_ from some incoming configuration $x_1$ to some outgoing trajectory $x_2$ (for a fixed parameter time interval at least, we will formulate this precisely in the next section when we genuinely consider Hamiltonian correspondences).

In a more general context one could consider there to be several such trajectories, and even a whole smooth space of such trajectories between given incoming and outgoing configurations. Each such trajectory would "relate" $x_1$ to $x_2$, but each in a possible different way. We can also say that each trajectory makes $x_1$ _correspond_ to $x_2$ in a different way, and that is the mathematical term usually used:

+-- {: .num_defn}
###### Defininition

For $X, Y \in \mathbf{H}$ two spaces, a [[correspondence]] between them is a [[diagram]] in $\mathbf{H}$ of the form

$$
  \array{
     && Z
     \\
     & \swarrow && \searrow
    \\
    X && && Y
  }
$$

with no further restrictions. 

=--

Here $Z$ is also called the _[[correspondence space]]_. 

Observe that the [[graph of a function]]  $f \colon X \to Y$ is, while defined differently, in fact [[equivalent]] to just the space $X$, the equivalence being induced by the map $x \mapsto (x,f(x))$

$$
  X \stackrel{\simeq}{\longrightarrow} graph(f)
  \,.
$$

In fact the [[relation]]/[[correspondence]] which expresses "$y$ is the image of $f$ under $x$" may just as well be exhibited by the diagram

$$
  \array{
    && X
    \\
    & {}^{\mathllap{id}}\swarrow && \searrow^{\mathrlap{f}}
    \\
    X && && Y
  }
  \,.
$$

It is clear that this correspondence with correspondence space $X$ should be regarded as being equivalent to the one with correspondence space $graph(f)$. We may formalize this equivalence by noting 

+-- {: .num_remark #EquivalenceOfCorrespndencesInducedByFunction}
###### Remark

Given an [[function]] $f \colon X \longrightarrow Y$
we have the [[commuting diagram]]

$$
  \array{
     && X
     \\
    & {}^{\mathllap{id}}\swarrow && \searrow^{\mathrlap{f}}
    \\
    X &&\downarrow^{\mathrlap{\simeq}} && Y
    \\
    & {}_{\mathllap{i_X}}\nwarrow && \nearrow_{\mathrlap{i_Y}}
    \\
    && graph(f)
  }
$$

exhibiting an [[equivalence]] of the [[correspondence]] at
the top with that at the bottom.

=--

A diagram like this we call an _[[equivalence]] or [[correspondences]]_. Correspondences between $X$ any $Y$ with such equivalences between them form a _[[groupoid]]_. (See at _[[geometry of physics]]_ the section _[Essence of gauge theory: Groupoids and basic homotopy 1-type theory](geometry%20of%20physics#GroupoidsAndBasicHomotopy1TypeTheory)_ for more on this.) Hence we write

$$
  Corr\left(\mathbf{H}\right)(X,Y) \in Grpd
  \,.
$$

Moreover, if we think of correspondences as modelling spaces of [[trajectories]], then it is clear that their should be a notion of [[composition]]:

$$
  \left(
  \array{    
    && Y_1 &&&& Y_2
    \\
    & \swarrow && \searrow && \swarrow && \searrow
    \\
    X_1 && && X_2 && && X_3 
  }
  \right)
  \;\;\;\;
  \mapsto 
  \;\;\;\;
  \left(
  \array{    
    && Y_1 \circ_{X_2} Y_2 
    \\
    & \swarrow && \searrow 
    \\
    X_1 && && X_3 
  }
  \right)
  \,.
$$

Heuristically, the composite space of trajectories $Y_1 \circ_{X_2} Y_2$ should consist precisely of those pairs of trajectories $( f, g ) \in Y_1  \times Y_2$ such that the endpoint of $f$ is the starting point of $g$. The space with this property is precisely the _[[fiber product]]_ of $Y_1$ with $Y_2$ over $X_2$, denoted $Y_1 \underset{X_2}{\times} Y_2$ (also called the [[pullback]] of $Y_2 \longrightarrow X_2$ along $Y_1 \longrightarrow X_2$ and then abbreviated $(pb)$):


$$
  \left(
  \array{    
    && Y_1 \circ_{X_2} Y_2 
    \\
    & \swarrow && \searrow 
    \\
    X_1 && && X_3 
  }
  \right)
  \;\;\;
  =
  \;\;\;
  \left(
  \array{  
     && && Z_1 \underset{Y}{\times} Z_2
     \\
      && & \swarrow && \searrow
      \\
      && Z_1 && (pb) && Z_2
      \\
     & \swarrow && \searrow && \swarrow && \searrow
    \\
    X && && Y && && Z
  }
  \right)
  \,.
$$ 

Hence given a [[topos]] $\mathbf{H}$, [[correspondences]] between its objects form a [[category]] which [[composition]] the [[fiber product]] operation, where however the collection of [[morphisms]] between any two objects is not just a [[set]], but is a [[groupoid]] (the groupoid of correspondences between two given objects and [[equivalences]] between them).

One says that correspondences form a _[[(2,1)-category]]_ 

$$
  Corr(\mathbf{H}) \in (2,1)Cat
  \,.
$$

But for most purposes here, the reader unwilling to enter [[higher category theory]] can, to good approximation, pretend that correspondences form an ordinary [[category]].

One reason for formalizing this notion of correspondences so much in the present context that it is useful now to apply it not just to the ambient [[topos]] $\mathbf{H}$ of [[smooth spaces]], but also to its [[slice topos]] $\mathbf{H}_{/\mathbf{\Omega}_{cl}^2}$ over the universal [[moduli space]] of closed [[differential 2-forms]].

To see how this is useful in the present context, notice the following basic observation:

+-- {: .num_defn}
###### Definition

Given a [[symplectic manifold]] $(X,\omgea)$, a [[submanifold]] $L \hookrightarrow$ is called a _[[Lagrangian submanifold]]_ of $\omega|_{L} = 0$ and if $L$ has [[dimension]] $dim(L) = dim(X)/2$.

=--

+-- {: .num_prop}
###### Proposition

Let $f \colon X_1 \to X_2$ be a [[smooth function]] between [[smooth manifolds]] and let

$$
  \array{
     && graph(f)
     \\
     && \downarrow
     \\
     && X_1 \times X_2
     \\
     & {}^{\mathllap{p_1}}\swarrow && \searrow^{\mathrlap{p_2}}
     \\
    X_1 && && X_2
  }
$$

be the induced [[correspondence]]. If $\omega_1$ and $\omega_2$ are [[symplectic forms]] on $X_1$ and $X_2$, respectively, then $p_1^\ast \omega_1 - p_2^\ast \omega_2$ is a pre-symplectic form on $X_1 \times X_2$, and $f$ is a [[symplectomorphism]] precisely if $graph(f) \hookrightarrow X_1 \times X_2$ is a [[Lagrangian submanifold]].

=--

To capture this phenomenon, one traditionally sets:

+-- {: .num_defn}
###### Definition

For $(X_1,\omega_1)$ and $(X_2,\omega_2)$ two [[symplectic manifolds]] (not necessarily of the same [[dimension]]), a [[Lagrangian correspondence]] between them is a [[correspondence]] of the underlying [[manifolds]]

$$
  \array{
     && R
     \\
     && \downarrow
     \\
     & {}^{\mathllap{p_1}}\swarrow && \searrow^{\mathrlap{p_2}}
     \\
    X_1 && && X_2
  }
$$

such that the [[correspondence space]] $R \hookrightarrow X_1 \times X_2$ is a [[Lagrangian submanifold]] of $(X_1 \times X_2 , p_1^\ast \omega_1 - p_2^\ast \omega_2)$.

=--


+-- {: .num_remark}
###### Remark

In the language of the [[topos]] $\mathbf{H}$ of [[smooth spaces]], this has a more evident formulation: that $graph(f)$ is an [[isotropic subspace]] equivalently means that there is a [[commuting diagram]] of [[smooth spaces]] of the following form

$$
  \array{
    && graph(f)
    \\
    & {}^{\mathllap{p_1}}\swarrow && \searrow^{\mathrlap{p_2}}
    \\
    X_1 && \swArrow_= && X_2
    \\
    & {}_{\mathllap{\omega_1}}\searrow && \swarrow_{\mathrlap{\omega_2}}
    \\
   && \Omega^2_{cl}
  }
  \,.
$$

Because the commutativity of this diagram says precisely that on $graph(f)$ we have

$$
  p_1^\ast \omega_1 = p_2^\ast \omega_2
$$

hence 

$$
  p_1^\ast \omega_1 - p_2^\ast \omega_2 = 0
  \,.
$$

This in turn is equivalent to being a [[correspondence]] in the [[slice topos]] $\mathbf{H}_{/\Omega^2_{cl}}$, def. \ref{TheSliceTopos}, under the identification of prop. \ref{SymplecticManifoldsAsObjectsInSliceOverModuliOf2Forms}.

=--

Therefore we have:

+-- {: .num_prop}
###### Proposition

For $(X_1, \omega_2)$ and $(X_2, \omega_2)$ two [[symplectic manifolds]], there is a [[full subcategory|full embedding]]

$$
  LagrangianCorrespondences\left(\left(X_1,\omega_1\right), \left(X_2, \omega_2\right)\right)
  \hookrightarrow
  Corr\left(\mathbf{H}_{/\mathbf{\Omega}^2_{cl}}\right)\left(\left(X_1,\omega_1\right), \left(X_2, \omega_2\right)\right)
$$

of the Lagrangian correspondences into the space of correspondences between the two manifolds as objects in the [[slice topos]] over the universal moduli space of closed differential 2-forms.

=--

(The co-image of this inclusion are those correspondences which are "isotropic" and not-necessarily even subspaces.)

### Hamiltonian (time evolution) trajectories and Hamiltonian correspondences

An important class of [[symplectomorphisms]] are the [[Hamiltonian symplectomorphisms]] from a [[symplectic manifold]] to itself, those which are the [[flow]] of a [[Hamiltonian vector field]] on $(X,\omega)$ induced by a [[Hamiltonian function]] 

$$
  H \;\colon\; X \longrightarrow \mathbb{R}
  \,.
$$

Using the [[Poisson bracket]] $\{-,-\}$ induced by the [[symplectic form]] $\omega$ and identifying the [[derivation]] $\{H,-\}$ with the corresponding [[Hamiltonian vector field]] and the exponent notation $\exp(t \{H,-\})$ with the corresponding [[flow]] for parameter "time" $t \in \mathbb{R}$, we may write these as 

$$
  \exp( t \{H,-\}) \;\colon\; (X,\omega) \longrightarrow (X,\omega)
  \,.
$$ 

Here we refer to [[Lagrangian correspondences]] induced from [[Hamiltonian symplectomorphisms]] as _Hamiltonian correspondences_.

+-- {: .num_remark #HamiltonianCorrespondencesAreSpacesOfTrajectories}
###### Remark

The [[smooth space|smooth]] [[correspondence space]] of a
Hamiltonian correspondence is naturally identified with the space of
_classical [[trajectories]]_ 

$$
  Fields_{traj}^{class}(t) = graph\left( \exp(t) \{H,-\}\right)
$$

in that 

1. every point in the space corresponds uniquely to a [[trajectory]] of parameter time length $t$ characterized as satisfying the [[equations of motion]] as given by [[Hamilton's equations]] for $H$;

1. the two projection maps to $X$ send a trajectory to its initial and to its final configuration, respectively.

=--

+-- {: .num_remark}
###### Remark

Forming Hamiltonian correspondences consitutes a [[functor]] from 1-dimensional [[cobordisms]] with [[Riemannian structure]] to the [[category of correspondences]] in the [[slice topos]]:

$$
  \exp((-)\{H,-\}) \;\colon\; Bord^{Riem}_1 \longrightarrow Corr_1(\mathbf{H}_{/\Omega^2})
$$

since for all ("time") parameter valued $t_1, t_2 \in \mathbb{R}$ 
we have a [[composition]] (by [[fiber product]]) of [[correspondences]] exhibited
by the following [[pasting diagram]]:

$$
  \array{
    &&&& graph\left(\exp\left(\left(t_1+t_2\right)\right) \left\{H,-\right\} \right)
    \\
    && & \swarrow && \searrow
    \\
    && graph\left(\exp\left(t_1\right)\left\{H,-\right\}\right) 
    && (pb) && graph\left(\exp\left(t_2 \left\{H,-\right\}\right)\right)
    \\
    & \swarrow && \searrow & & \swarrow && \searrow
    \\
    X && && X && && X
    \\
    & \searrow &&& \downarrow &&& \swarrow
    \\
    &&&& \Omega^2_{cl}
  }
  \,.
$$

=--

### The kinetic action, pre-quantization and differential cohomology

To naturally see why there would be any [[Hamiltonian]]
associated to a (to some) [[symplectomorphism]] in the first place, 
we step back and consider _local trivializations_ or _local potentials_
for [[symplectic forms]]. Doing so turns out to give rise to what
in physics is called the [[kinetic action]], what in 
the context of [[geometric quantization]] is called [[prequantization]]
and what in [[mathematics]] is called lifting to _[[differential cohomology]]_. All these concepts arise directly from the following simple consideration.

Given a [[pre-symplectic form]] $\omega \in \Omega^2_{\mathrm{cl}}(X) $, 
by the [[Poincaré lemma]] there is a [[good open cover]] $\{U_i \hookrightarrow X\}_i$
such that one can find smooth [[differential 1-forms]] $\theta_i \in \Omega^1(U_i)$ such that these are local trivializations/potentials
for the [[symplectic form]] on each patch $U_i$ of the cover:

$$
  \mathbf{d}\theta_i = \omega_{|U_i}
  \,.
$$

Physically such a 1-form is (up to a factor of 2) a choice 
of _[[kinetic energy]] [[density]]_ called a _[[kinetic Lagrangian]]_ 
$L_{\mathrm{kin}}$ (below in example \ref{StandardPrequantizationOfStandardR2PhaseSpace} we connect this statement to a maybe more familiar formla): 

$$
  \theta_i = 2 L_{\mathrm{kin}, i}
  \,.
$$

+-- {: .num_example #StandardPrequantizationOfStandardR2PhaseSpace}
###### Example

Consider the [[phase space]] $(\mathbb{R}^2, \; \omega = \mathbf{d} q \wedge \mathbf{d} p)$ 
of example \ref{CanonicalR2PhaseSpace}. Since $\mathbb{R}^2$ is a [[contractible topological space]] we consider the trivial [[covering]] ($\mathbb{R}^2$ covering itself) since this is already a [[good covering]] in this case. Then all the $\{g_{i j}\}$ are trivial and the data of a [[prequantization]] consists simply of a choise of 1-form $\theta \in \Omega^1(\mathbb{R}^2)$ such that 

$$
  \mathbf{d}\theta = \mathbf{d}q \wedge \mathbf{d}p
  \,.
$$

A standard such choice is 

$$
  \theta = - p \wedge \mathbf{d}q
  \,.
$$

Then given a [[trajectory]] $\gamma \colon [0,1] \longrightarrow X$ which satisfies [[Hamilton's equation]] for a standard [[kinetic energy]] term, then $p (\mathbf{d})q(\dot\gamma)$ is this [[kinetic energy]] of the [[particle]] which traces out this [[trajectory]].

=--

Given a path $\gamma : [0,1] \to X$ in phase space, its 
_[[kinetic action]]_ $S_{\mathrm{kin}}$ 
is supposed to be the integral of $L_{\mathrm{kin}}$
along this trajectory. In order to make sense of this in the generality where there is no globally defined $\theta$,
there need to be functions $g_{i j} \in C^\infty(U_i \cap U_j, \mathbb{R})$ for each double intersection of patches of the cover,
such that these the local $\theta$'s differ on these double
intersection only by the total [[derivative]] 
([[de Rham cohomology|de Rham]] [[differential]] $\mathbf{d}$ ) of these functions:

$$
  \theta_j|_{U_j} - \theta_i|_{U_i} = \mathbf{d}g_{i j}
  \,.
$$

One then finds (from the theory of [[Cech cohomology]]) that if on triple intersections these functions satisfy

$$
  g_{ij} + g_{j k} = g_{i k}
$$

then there is a well defined action functional

$$
  S_{\mathrm{kin}}(\gamma) \in \mathbb{R}
$$

obtained by dividing $\gamma$ into small pieces that each map to a single
patch $U_i$, integrating $\theta_i$ along this piece, and adding the 
contribution of $g_{i j}$ at the point where one switches from using
$\theta_i$ to using $\theta_j$. Technically this is called the [[holonomy]] or [[parallel transport]] of the $(\mathbb{R},+)$-[[principal connection]] which is defined by the data $(\{\theta_i\}, \{g_{i j}\} )$.

However, requiring this condition on triple overlaps as an equation between $\mathbb{R}$-valued functions makes the local patch structure trivial: if this is possible then one can in fact already find a single $\theta \in \Omega^1(X)$ and functions $h_i \in C^\infty(U_i, \mathbb{R})$ such that  $\theta_i = \theta|_{U_i} + \mathbf{d}h_i$. This has the superficially pleasant effect that the the action is 
simply the integral against this globally defined 1-form, 
$S_{\mathrm{kin}} = \int_{[0,1]} \gamma^\ast L_{\mathrm{kin}}$, but it also means that the pre-symplectic form $\omega$ is exact, which is 
not the case in many important examples.
(In more abstract terms what this is saying is that every 
$(\mathbb{R},+)$-[[principal bundle]] over a manifolds is trivializable.)

On the other hand, what really matters in [[prequantum field theory|prequantum]] [[physics]] is not the [[action functional]]
$S_{\mathrm{kin}} \in \mathbb{R}$ itself, 
but the _exponentiated_ action 

$$
  \exp\left( \tfrac{i}{\hbar} S \right) \in \mathbb{R}/(2\pi \hbar)\cdot\mathbb{Z}
  \,,
$$

which takes values in the [[quotient]] of the additive group of [[real numbers]] by [[integer|integral]] multiples of [[Planck's constant]] $2\pi \hbar$.


For this to be well defined, one only needs that the equation
$g_{i j} + g_{j k} = g_{i k}$ on triple intersection holds modulo addition of an integral multiple of [[Planck's constant]] $h = 2\pi \hbar$. 

If this is the case, then one says that the data 
$(\{\theta_i\}, \{g_{i j}\})$ defines 
equivalently

* a $U(1)$-principal connection;

* a degree-2 cocycle in ordinary differential cohomology 

on $X$, with _[[curvature]]_ the given symplectic 2-form $\omega$.

Such data is called a _[[pre-quantization]]_ of the symplectic manifold 
$(X,\omega)$. Since it is the exponentiated action functional
$\exp(\frac{i}{\hbar} S)$ that enters the quantization of the 
given mechanical system (for instance as the integrand of a 
[[path integral]]),
the [[prequantization]] of a symplectic manifold is indeed precisely
the data necessary before quantization.



Therefore, in the spirit of the above discussion of pre-symplectic structures,
we would like to refine the smooth moduli space of closed 
differential 2-forms to a moduli space of prequantized differential 
2-forms. 

Again this does naturally exist if only we allow for a good notion of
"space". An additional phenomenon to be taken care of now is that
while pre-symplectic forms are either equal or not, their
pre-quantizations can be different and yet be _[[equivalence|equivalent]]_:

because there is still a remaining freedom to change this data without
changing the exponentiated action along a _closed_ path:
we say that a choice of functions 
$h_i \in C^\infty(U_i, \mathbb{R}/(2\pi\hbar)\mathbb{Z})$
defines an equivalence between 
$(\{\theta_i\}, \{g_{i j}\})$ and $(\{\tilde \theta_i\}, \{\tilde g_{i j}\})$
if $\tilde \theta_i - \theta_i = \mathbf{d}h_i$
and $\tilde g_{i j} - g_{i j} = h_j - h_i$.

This means that the space of prequantizations of $(X,\omega)$
is similar to an _[[orbifold]]_: it has points which are connected by 
gauge equivalences: there is a _[[groupoid]]_ of pre-quantum structures
on a manifold $X$. 

In just the same way then that above we found a [[smooth space|smooth]] [[moduli space]] $\mathbf{\Omega}^2_{cl}$ of closed differential 2-forms, one can find a [[smooth groupoid]] (for more on this see at _[[geometry of physics]]_ the section _[Smooth homotopy types](geometry%20of%20physics#SmoothnGroupoids)_ ), which we denote 

$$
  \mathbf{B}U(1)_{\mathrm{conn}}
  \in 
  \mathbf{H}
$$

and which is _characterized_ as follows, and this is all that we here need to know about this object:

1. For $X$ a [[smooth manifold]], maps $X \longrightarrow \mathbf{B}U(1)_{conn}$ are equivalent to the above prequantum data $(\{\theta_i\}, \{g_{i j}\})$ on $X$;

1. for $\nabla_1, \nabla_2 \colon X \longrightarrow \mathbf{B}U(1)_{conn}$ two such maps, [[homotopies]] 

   $$
     \array{
       & \nearrow \searrow
       \\
       X & \Downarrow & \mathbf{B}U(1)_{conn}
       \\
       & \searrow \nearrow
     }
   $$

   between these are equivalent to the above [[gauge transformations]] $(\{h_i\})$ between this data.


The only other fact we need is that there is a universal [[curvature]] map

$$
  F
  \;\colon\;
   \mathbf{B}U(1)_{\mathrm{conn}}
     \longrightarrow
   \mathbf{\Omega}^2_{\mathrm{cl}}
$$

which is such that for $\nabla \colon X \longrightarrow \mathbf{B}U(1)_{conn}$ a $U(1)$-[[principal connection]], the composite

$$
  F_\nabla \;\colon\;
  X 
    \stackrel{\nabla}{\longrightarrow}
  \mathbf{B}U(1)_{conn}
    \stackrel{F_{(-)}}{\longrightarrow}
  \mathbf{\Omega}^2_{cl}
$$

is its [[curvature]] 2-form. Hence this is the map that sends $(\{\theta_i\}, \{g_{i j}\})$ to $\omega$ with $\omega|_{U_i} = \mathbf{d}\theta_i$.

Therefore:

+-- {: .num_defn }
###### Definition

Given a [[presymplectic manifold]] $(X,\omega)$, regarded equivalently as an object $(X \stackrel{\omega}{\longrightarrow} \mathbf{\Omega}^2_{cl}) \in \mathbf{H}_{/\mathbf{\Omega}^2_{cl}}$ by prop. \ref{SymplecticManifoldsAsObjectsInSliceOverModuliOf2Forms}, then a
**[[prequantization]]** of $(X,\omega)$ is a choice of lift $\nabla$ in

$$
  \array{
    X &\stackrel{\nabla}{\longrightarrow}& \mathbf{B}U(1)_{conn}
    \\
    & {}_{\mathllap{\omega}}\searrow & \downarrow^{\mathrlap{F_{(-)}}}
    \\
    && \mathbf{\Omega}^2_{cl}
  }
$$

hence a lift through the [[functor]] ([[base change]]/[[dependent sum]] along the universal [[curvature]] map)

$$
  \underset{F_{(-)}}{\sum}
   \;\colon\;
  \mathbf{H}_{/\mathbf{B}U(1)_{conn}}
   \longrightarrow
  \mathbf{H}_{/\mathbf{\Omega}^2_{cl}}
  \,.
$$

=--




### The classical action, the Legendre transform and Hamiltonian flows
 {#HamiltonianTrajectoriesAndPrequantizedLagrangianCorrespondences}

But the reason to consider [[Hamiltonian symplectomorphisms]] instead of general [[symplectomorphisms]] is really because these give [[homomorphisms]] not just between plain [[symplectic manifolds]], but between their _prequantizations_. To these we turn now.

+-- {: .num_defn}
###### Definition


A _[[prequantization]]_ of a [[symplectic manifold]] $(X,\omega)$ is -- if it exists -- a choice of [[circle group]]-[[principal connection]] $\nabla$ on $X$ whose [[curvature]] 2-form is the given [[symplectic form]]

$$
  F_\nabla = \omega
  \,.
$$

=--

+-- {: .num_remark #PrequantizationIsLiftThroughCurvatureBaseChange}
###### Remark

In the [[topos]] of [[smooth spaces]], or rather in the [[(2,1)-topos]] $\mathbf{H}$ of [[smooth groupoids]], this means that a [[prequantization]] is a lift $\nabla$ in the [[diagram]]

$$
  \array{
    X &\stackrel{\nabla}{\longrightarrow}& \mathbf{B}U(1)_{conn}
    \\
    & {}_{\mathllap{\omega}}\searrow & \downarrow^{\mathrlap{F}_{(-)}}
    \\
    && \Omega^2_{cl}
  }
  \,,
$$

where $\mathbf{B}U(1)_{conn}$ is the [[moduli stack]] of [[circle n-bundle with connection|circle bundle with connection]]. For details on this see at _[[geometry of physics]]_ the section _[Smooth homotopy types](geometry+of+physics#SmoothnGroupoids)_.

More abstractly we hence find that a [[prequantization]] is a lift of a symplectic manifold regard as an object of the [[slice topos]] $\mathbf{H}_{/\Omega^2_{cl}}$ through the [[base change]]/[[dependent sum]] map induced by the universal [[curvature]] map $F_{(-)} \;\colon\;\mathbf{B}U(1)_{conn} \longrightarrow \Omega^2_{cl}$ to the [[slice (infinity,1)-topos|slice (2,1)-topos]] $\mathbf{H}_{/\mathbf{B}U(1)_{conn}}$.

=--


Consider a morphism

$$
  \array{
    X_1 &&\stackrel{\phi}{\longrightarrow}&& X_2
    \\
    & {}_{\mathllap{\nabla_1}}\searrow &\swArrow& \swarrow_{\mathrlap{\nabla_2}}
    \\
    && \mathbf{B}U(1)_{conn}
  }
$$

hence a morphism in the slice $\mathbf{H}_{/\mathbf{B}U(1)_{conn}}$. This has been discussed in detail in ([hgp 13](#FiorenzaRogersSchreiber13a)).

One finds that [[infinitesimal object|infinitesimally]] such morphism are given by a [[Hamiltonian]] and its [[Legendre transform]]. 

+-- {: .num_prop #HamiltonianTransformationIsPrequantizedByTheExponentiatedAction}
###### Proposition

Consider the [[phase space]] $(\mathbb{R}^2, \; \omega = \mathbf{d} q \wedge \mathbf{d} p)$ 
of example \ref{CanonicalR2PhaseSpace} equipped with its canonical [[prequantization]] by $\theta = p \mathbf{d}q$ from example \ref{StandardPrequantizationOfStandardR2PhaseSpace}. 
Then for $H \colon \mathbb{R}^2 \longrightarrow \mathbb{R}$ a [[Hamiltonian]], and for $t \in \mathbb{R}$ a parameter ("time"), a lift of the [[Hamiltonian symplectomorphism]] 
$\exp(t \{H,-\})$ from $\mathbf{H}$ to the [[slice topos]] $\mathbf{H}_{/\mathbf{B}U(1)_{conn}}$ 
is given by

$$
  \array{       
    X && \stackrel{\exp(t \{H,-\})}{\longrightarrow} && X
    \\
    & {}_{\mathllap{\omega_1}} \searrow 
    & \swArrow_{\exp( i S_t  )} & \swarrow_{\mathrlap{\omega_2}}
    \\
    && \mathbf{B}U(1)_{conn}
  }
  \,,
$$

where 

* $S_t \;\colon\; \mathbb{R}^2 \longrightarrow \mathbb{R}$ is the [[action functional]] of the classical [[trajectories]] induced by $H$,

* which is the [[integral]] $S_t = \int_{0}^t L \, d t$ of the [[Lagrangian]] $L \,d t$ induced by $H$,

* which is the [[Legendre transform]]

  $$
    L \coloneqq p \frac{\partial H}{\partial p} - H \;\colon\; \mathbb{R}^2 \longrightarrow \mathbb{R}
    \,. 
  $$

In particular, this induces a [[functor]]

$$
  \exp(i S)
  \;\colon\;
  Bord_1^{Riem} 
    \longrightarrow 
  \mathbf{H}_{/\mathbf{B}U(1)_{conn}}
  \,.
$$

Conversely, a symplectomorphism, being a morphism in $\mathbf{H}_{/\mathbf{\Omega}^2_{cl}}$ is a [[Hamiltonian symplectomorphism]] precisely if it admits such a lift 
to $\mathbf{H}_{/\mathbf{B}U(1)_{conn}}$.

=--

This is a special case of the discussion in ([hgp 13](#FiorenzaRogersSchreiber13a)).

+-- {: .proof}
###### Proof

The canonical [[prequantization]] of $(\mathbb{R}^2, \mathbf{d} q \wedge \mathbf{d} p)$ is the globally defined [[connection on a bundle|connection]] 1-form

$$
  \theta \coloneqq p \, \mathbf{d} q
  \,.
$$

We have to check that on $graph(\exp(t\{H,-\}))$ we have the [[equation]]

$$
  p_2 \mathbf{d} q_2 = p_1 \mathbf{d} q_1 + \mathbf{d} S 
  \,.
$$

Or rather, given the setup, it is more natural to change notation to

$$
  p_t \mathbf{d} q_t = p \mathbf{d} q + \mathbf{d} S
  \,.
$$

Notice here that by the nature of $graph(\exp(t\{H,-\}))$ we can identify

$$
  graph(\exp(t\{H,-\}))
  \simeq
  \mathbb{R}^2
$$

and under this identification

$$
  q_t = \exp(t \{H,-\}) q
$$

and

$$
  p_t = \exp(t \{H,-\}) p
  \,.
$$

It is sufficient to check the claim [[infinitesimal object|infinitesimally]]. So let $t = \epsilon$ be an [[infinitesimal object|infinitesimal]], hence such that $\epsilon^2 = 0$. Then the above is [[Hamilton's equations]] and reads equivalently

$$
  q_\epsilon = q + \frac{\partial H}{\partial p} \epsilon
$$

and

$$
  p_\epsilon = p - \frac{\partial H}{\partial q} \epsilon
  \,.
$$

Using this we compute

$$
  \begin{aligned}
    \theta_\epsilon - \theta 
     & = 
    p_\epsilon \, \mathbf{d} q \epsilon - p \mathbf{d} q
     \\
      & =
    \left(p - \frac{\partial H}{\partial q} \epsilon \right)
    \mathbf{d}
    \left(
      q + \frac{\partial H}{\partial p} \epsilon
    \right)
    - p \mathbf{d}q
    \\
    & =
    \epsilon
    \left(
      p \mathbf{d}\frac{\partial H}{\partial p}
      - 
      \frac{\partial H}{\partial q} \mathbf{d}q
    \right)
    \\
    & = 
    \epsilon
    \left(
      \mathbf{d}\left( p \frac{\partial H}{\partial p}\right)
      -
      \frac{\partial H}{\partial p} \mathbf{d} p
      - 
      \frac{\partial H}{\partial q} \mathbf{d}q
    \right)
    \\
    & =
    \epsilon \mathbf{d}
    \left(
      p \frac{\partial H}{\partial p}
      -
      H
    \right)
  \end{aligned}
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

Proposition \ref{HamiltonianCorrespondenceIsPrequantizedByTheExponentiatedAction} 
says that the slice topos $\mathbf{H}_{/\mathbf{B}U(1)_{conn}}$
unifies [[classical mechanics]] in its two incarnations as
[[Hamiltonian mechanics]] and as [[Lagrangian mechanics]]. A morphism 
here is a diagram in $\mathbf{H}$ of the form

$$
  \array{
    X && \stackrel{}{\longrightarrow} && Y
    \\
    & \searrow &\swArrow& \swarrow
    \\
    && \mathbf{B}U(1)_{conn}
  }
$$

and which may be regarded as having two components: the top horizontal [[1-morphism]]
as well as the [[homotopy]]/[[2-morphism]] filling the slice. 
Given a smooth [[flow]] of these, the horizontal morphism is the [[flow]]
of a [[Hamiltonian vector field]] for some [[Hamiltonian]] function $H$, 
and the 2-morphism is a $U(1)$-[[gauge transformation]] given (locally) by 
a $U(1)$-valued function which is the exponentiated [[action functional]]
that is the integral of the [[Lagrangian]] $L$ which is the [[Legendre transform]]
of $H$.

So in a sense the [[prequantization]] lift through the [[base change]]/[[dependent sum]]
along the universal [[curvature]] map

$$
  underset{F_{(-)}}{\sum}
   \;\colon\;
  \mathbf{H}_{/\mathbf{B}U(1)_{conn}}
  \longrightarrow
  \mathbf{H}_{\mathbf{\Omega}^2_{cl}}
$$

is the [[Legendre transform]] which connects [[Hamiltonian mechanics]] with [[Lagrangian mechanics]].

[[!include Hamiltonian and Lagrangian -- table]]

=--


### The Heisenberg group and the Poisson bracket from prequantized Lagrangian equivalences

Above we have interpreted [[maps]] $f \colon X \to Y$ as [[correspondences]]
between $X$ and $Y$ by taking the [[correspondence space]] to be the 
[[graph of a function|graph]] of $f$. There is also another natural way
to regard maps as correspondences: we may simply take $X$ as the correspondence
space, take the left map out of it to be the identity and the right map 
to be $f$ itself:

$$
  \left(
    X \stackrel{f}{\longrightarrow} Y
  \right)
  \;\;  
    \mapsto
  \;\;
  \left(
    \array{
       && X
       \\
       & {}^{\mathllap{id}}\swarrow && \searrow^{\mathrlap{f}}
       \\
      X && && Y
    }
  \right)
  \,.
$$

Consider now those correspondences which are [[equivalences]] ([[isomorphisms]])
in the [[category of correspondences]] $Corr_1(\mathbf{H})$. If we forget
the [[smooth structure]] on everything and consider just correspondences
of the underlying [[sets]], hence $Corr_1(Set)$, then it is easy to see
that under the [[cardinality]] map correspondences are given by [[matrices]]
with [[cardinality]] entries and [[composition]] of correspondence 
by [[fiber product]] induces [[matrix multiplication]]. 

Therefore for a correspondence to be an equivalence-transformation it has
to be of the form above, induced by a direct [[map]], which in 
addition is an [[equivalence]] $f \colon X \stackrel{\simeq}{\longrightarrow} Y$.

+-- {: .num_prop}
###### Proposition

Let $(X,\omega)$ be a [[symplectic manifold]] and choose any 
[[prequantization]] $(L,\nabla)$, thought of, via remark \ref{PrequantizationIsLiftThroughCurvatureBaseChange}, as an object in the [[slice (infinity,1)-topos|slice (2,1)-topos]],
$\nabla \in \mathbf{H}_{/\mathbf{B}U(1)_{conn}}$. Then

* the [[automorphism group]] of $\nabla$ in the [[category of correspondences]] $Corr_1(\mathbf{H}_{/\mathbf{B}U(1)_{conn}})$ is what is called the _[[quantomorphism group]]_;

* its [[Lie algebra]] is the [[Poisson bracket]] Lie algebra of $(X,\omega)$.

=--

See ([hgp 13](#FiorenzaRogersSchreiber13a))

For some reason, the [[quantomorphism group]] which is the [[Lie integration]] of the [[Poisson bracket]] is less famous than the [[Heisenberg group]] that sits inside it:

+-- {: .num_remark}
###### Remark

Suppose that $(X,\omega)$ itself has the structure of a [[group]] (for instance if $(X,\omega)$ is a [[symplectic vector space]] such as $(\mathbb{R}^{2n}, \sum_i p_i \mathbf{d}q^i)$ ), then the [[subgroup]] of the [[quantomorphism group]] whose underlying [[diffeomorphisms]] are given by the action of $X$ is the _[[Heisenberg group]]_ of $X$.

=--

### Hamiltonian actions and moment maps are actions by prequantized Lagrangian equivalences

For $G$ a [[Lie group]], a [[Hamiltonian action]] of $G$ on $(X,\omega)$ is equivalently an action by prequantized Lagrangian correspondences, hence a group [[homomorphism]]

$$
  G \longrightarrow \mathbf{Aut}_\nabla(Corr_1(\mathbf{H}_{/\mathbf{B}U(1)_{conn}}))
  \,.
$$

The [[Lie differentiation]] of this is the corresponding [[moment map]].

See ([hgp 13](#FiorenzaRogersSchreiber13a))



### The classical action functional prequantizes Hamiltonian correspondences
 {#TheClassicalActionFunctionalPrequantizesHamiltonianCorrespondences}

Then for two prequantized symplectic manifolds, it is now clear what a _prequantized correspondence_ between them is: 

+-- {: .num_defn #PrequantizedLagrangianCorrespondence}
###### Definition


A _prequantization_ of a [[Lagrangian correspondence]] $Y \colon (X_1,\omega) \to (X_2,\omega_2)$
is a [[diagram]] in $\mathbf{H}$ of the form

$$
  \array{
    && Y
    \\
    & \swarrow &\swArrow& \searrow
    \\
    X_1 &\stackrel{\nabla_1}{\longrightarrow}& \mathbf{B}U(1)_{conn} &\stackrel{\nabla_2}{\longleftarrow}& X_2
    \\
    & {}_{\mathllap{\omega_1}}\searrow && \swarrow_{\mathrlap{\omega_2}}
    \\
   && \Omega^2_{cl}
  }
$$

hence a correspondence in the [[slice (infinity,1)-topos|slice (2,1)-topos]] $\mathbf{H}_{/\mathbf{B} U(1)_{conn}}$.

=--


For completing the general picture, it is useful to restate the 
discussion in _[The classical action functional, the Legendre transform and Hamiltonian flows](#HamiltonianTrajectoriesAndPrequantizedLagrangianCorrespondences)_, now in terms of [[correspondence]]:



The natural question is which Hamiltonian correspondences, remark \ref{HamiltonianCorrespondencesAreSpacesOfTrajectories}, may be prequantized, 
def. \ref{#PrequantizedLagrangianCorrespondence}, 
and what the corresponding prequantum data is. The following proposition shows that the prequantization of the Hamiltonian correspondence given by a [[Hamiltonian]] $H$ is given by the exponentiated [[action functional]] associated with $H$, namely the exponentiated integral over its [[Lagrangian]] $L$, which is its [[Legendre transform]] $L = p \frac{\partial H}{\partial p} - H$.


+-- {: .num_prop #HamiltonianCorrespondenceIsPrequantizedByTheExponentiatedAction}
###### Proposition

Consider the [[phase space]] $(\mathbb{R}^2, \; \omega = \mathbf{d} q \wedge \mathbf{d} p)$ equipped with its canonical [[prequantization]] by $\theta = p \mathbf{d}q$. Then for $H \colon \mathbb{R}^2 \to \mathbb{R}$ a [[Hamiltonian]], and for $t \in \mathbb{R}$ a parameter ("time"), a lift of the [[Lagrangian correspondence]] $\exp(t \{H,-\})$ to a prequantized Lagrangian correspondence is given by

$$
  \array{   
    && graph\left( \exp(t \{H,-\}) \right)
    \\
    & \swarrow && \searrow
    \\
    X && \swArrow_{\exp( i S_t  )} && X
    \\
    & {}_{\mathllap{\omega_1}} \searrow && \swarrow_{\mathrlap{\omega_2}}
    \\
    && \mathbf{B}U(1)_{conn}
  }
  \,,
$$

where 

* $S_t \;\colon\; \mathbb{R}^2 \longrightarrow \mathbb{R}$ is the [[action functional]] of the classical [[trajectories]] induced by $H$,

* which is the [[integral]] $S_t = \int_{0}^t L \, d t$ of the [[Lagrangian]] $L \,d t$ induced by $H$,

* which is the [[Legendre transform]]

  $$
    L \coloneqq p \frac{\partial H}{\partial p} - H \;\colon\; \mathbb{R}^2 \longrightarrow \mathbb{R}
    \,. 
  $$

In particular, this induces a [[functor]]

$$
  \exp(i S)
  \;\colon\;
  Bord_1^{Riem} 
    \longrightarrow 
  Corr_1(\mathbf{H}_{/\mathbf{B}U(1)_{conn}})
  \,.
$$

=--

+-- {: .proof}
###### Proof

Under the equivalence of correspondences of remark \ref{EquivalenceOfCorrespndencesInducedByFunction}
this is a re-statement of prop. \ref{HamiltonianTransformationIsPrequantizedByTheExponentiatedAction}.

=--



+-- {: .num_remark}
###### Remark

In summary,  prop. \ref{HamiltonianCorrespondenceIsPrequantizedByTheExponentiatedAction} 
and remark \ref{HamiltonianCorrespondencesAreSpacesOfTrajectories}
say that a prequantized Lagrangian correspondence is conceptually of the following form

$$
  \array{
    && {{space\,of} \atop {trajectories}}
    \\
    & {}^{\mathllap{{initial}\atop {values}}}\swarrow && \searrow^{\mathrlap{{Hamiltonian} \atop {evolution}}}
    \\
    phase\,space_{in} && \swArrow_{{action} \atop {functional}} && phase \,space_{out}
    \\
    & {}_{\mathllap{{prequantum}\atop {bundle}_{in}}}\searrow 
    && 
    \swarrow_{\mathrlap{{prequantum} \atop {bundle}_{out}}}
    \\
    && {{2-group} \atop {of\,phases}}
  }
  \,.
$$

=--



## **Local (topological) prequantum field theory**
 {#LocalTopologicalPrequantumFieldTheory}

We discuss local ("[[extended TQFT|extended]]") [[topological field theory|topological]] prequantum field theory. 

The following originates in the lecture notes ([Schreiber Pittsburgh13](#SchreiberPittLectures)) and draws on material that is discussed more fully in ([lpqft](#lpqft)).

After a technical preliminary to set the stage in 

* _[The ambient topos](#TheTopos)_,

the first section gives the the definitions and general properties of 

* _[Local prequantum field theory](#LocalPrequantumFieldTheory)_.

To digest this the reader may first or in parallel want to look at the simplest examples of these general considerations, which we discuss below in the first subsections of

* _[Higher Dijkgraaf-Witten prequantum field theory](#HigherDijkgraafWittenLocalPrequantumFieldTheory)_.

After that we turn to the general case of examples of 

* _[Higher Chern-Simons prequantum field theory](#HigherChern-SimonsLocalPrequantumFieldTheory)_.

Here the pattern of the discussion of examples is the following:

| | [[local prequantum field theory]] | [[homotopy theory]] |  | [[local action functional]] / [[prequantum n-bundle]] |  |
|--|--|--|--|--|--|
| **1)** | [[1-dimensional Dijkgraaf-Witten theory]] | [[1-groupoids]]/[[homotopy 1-types]] | $\mathbf{B}\flat G$ | $-$[[group character]]$\to$ | $\mathbf{B}\flat U(1)$ |
| | $\vdots$ |  |  |  |  |
| **2)** | [[n-dimensional Dijkgraaf-Witten theory]] | [[n-groupoids]]/[[homotopy n-types]] | $\mathbf{B}\flat G$ | $-$[[cocycle]] in [[group cohomology]]$\to$ | $\mathbf{B}^n\flat U(1)$ |
|  |  |  |  $\downarrow$ | embed [[flat ∞-connections]] in all [[principal ∞-connections]] |  $\downarrow$ |
| **3)** | [[schreiber:infinity-Chern-Simons theory|n-dimensional Chern-Simons theory]] | [[n-stacks]]/[[smooth homotopy n-types]] | $\mathbf{B}G_{conn}$ | $-$[[cocycle]] in [[differential cohomology]]$\to$ | $\mathbf{B}^n U(1)_{conn}$ |
| |  |  |  $\downarrow$  |   [[forgetful functor|forget]] connection, remember [[principal ∞-bundle]] |  $\downarrow$ |
| | (underlying [[instanton sectors]])  |  |  $\mathbf{B}G$ | $-$[[cocycle]] in [[smooth ∞-group]]-[[cohomology]]$\to$ | $\mathbf{B}^n U(1)$ |
| |  |  |  |  |  |
| | ([[transgression]]/[[fiber integration]]) |  |  $[\Sigma_k,\mathbf{B}G_{conn}]$ | $\stackrel{\exp(2 \pi in \int_{\Sigma_k} [\Sigma_k,\nabla])}{\to}$ | $\mathbf{B}^{n-k}U(1)$ |
| | |  |  | ([[Chern-Simons invariant]]) |

### The ambient topos
 {#TheTopos}

Prequantum field theory deals with "spaces of [[field (physics)|physical fields]]". These spaces of [[field (physics)|fields]] are, in general, richer than just plain [[sets]] in two ways

1. Spaces of [[field (physics)|fields]] carry [[geometry|geometric]] structure, notably they may be [[smooth spaces]], meaning that there is a way to determine which collections of [[field (physics)|fields]] form a smoothly parameterized collection. This is for instance the structure invoked (often implicitly) when performing [[variational calculus]] on spaces of [[field (physics)|fields]] in order to find their classical [[equations of motion]]. 

1. Spaces of fields have [[gauge transformations]] between their points and possibly [[higher gauge transformations]] between these, meaning that they are in fact [[groupoids]] and possibly [[infinity-groupoid|higher groupoids]]. In the physics literature this is best known in the [[infinitesimal object|infinitesimal]] approximation to these gauge transformations, in which case the spaces of fields are described by [[BRST complexes]]: the dg-algebras of functions on a [[Lie algebroid]] or [[L-∞ algebroid]] of fields.

Taken together this means that spaces of fields are _[[(∞,1)-sheaf|geometric higher groupoids]]_, such as [[orbifolds]] and more generally [[Lie groupoids]], [[differentiable stacks]], [[Lie 2-groupoids]], ... [[smooth ∞-groupoids]].

A collection of all such geometric higher groupoids for a chosen flavor of [[geometry]] -- for instance [[topology]] or [[differential geometry]] or  [[supergeometry]] (for the description of [[fermion]] fields) or [[synthetic differential geometry]] or [[synthetic differential supergeometry]], etc. -- is called an _[[∞-topos]]_. 

Not quite every [[∞-topos]] $\mathbf{H}$ serves as a decent context for collections (moduli stacks) of [[physical fields]] though. In the following we need at least that $\mathbf{H}$ has a reasonable notion of _[[discrete objects]]_ so that we can identify the geometrically discrete spaces in there. We here need this to mean the following

+-- {: .num_defn #ShapeAndFlatModality}
###### Definition

An [[∞-topos]] $\mathbf{H}$ is called _[[locally ∞-connected (∞,1)-topos|locally ∞-connected]]_ and _[[globally ∞-connected (∞,1)-topos|globally ∞-connetced]]_ if the [[locally constant ∞-stack]]-functor $LConst \colon $ [[∞Grpd]] $\to \mathbf{H}$ is a [[reflective sub-(∞,1)-category|reflective embedding]]. 

The corresponding reflector we write

$$
  \Pi \colon \mathbf{H} \to \infty Grpd \hookrightarrow \mathbf{H}
$$

and also call the _[[shape modality]]_ of $\mathbf{H}$. By the discussion at [[adjoint triple]] it follows that $LConst$ is also a [[coreflective subcategory|coreflective]] embedding; the corresponding coreflector we write 

$$
  \flat \colon \mathbf{H} \stackrel{\Gamma}{\to} \infty Grpd \hookrightarrow \mathbf{H}
$$

and call the _[[flat modality]]_.

=--

+-- {: .num_example}
###### Example

Every [[cohesive (∞,1)-topos]] is in particular globally and locally $\infty$-connected, by definition. Standard canonical examples to keep in mind are

* $\mathbf{H} = $ [[∞Grpd]] for [[∞-Dijkgraaf-Witten theories]];

* $\mathbf{H} = $ [[Smooth∞Grpd]] for [[schreiber:∞-Chern-Simons theories]];

* $\mathbf{H} = $ [[SuperSmooth∞Grpd]] for [[schreiber:∞-Chern-Simons theories]] with [[fermions]] and [[supersymmetry]];

* $\mathbf{H} = $ [[SynthDiff∞Grpd]] for [[AKSZ sigma-models]].

=--


### Local prequantum field theory
 {#LocalPrequantumFieldTheory}

After sketching out the general 

* _[Idea](#PrequantumFieldTheoryIdea)_

we formulate first 

* _[Bulk field theory](#BulkFieldTheory)_,

which concerns the case where the [[worldvolume]]/[[spacetime]] on which the [[field (physics)|physical fields]] propagate has no [[boundaries]] with [[boundary conditions]] imposed (no "[[branes]]" or "[[domain walls]]" or "[[QFT with defects|defects]]"). The point of this section is to see how the "space of fields" -- or rather: the [[moduli stack]] of fields -- on a point induces the corresponding spaces/moduli stacks of fields on an arbitrary [[closed manifold]], and, correspondingly, how the [[prequantum n-bundle]] on the space over fields over the point induces the [[action functional]] in [[codimension]] 0.

However, what makes local prequantum field theory rich is that it naturally incorporates extra structure on [[boundaries]] of [[worldvolume]]/[[spacetime]]. In fact, under suitable conditions there is another local prequantum field theory just over the boundary, which is related to the corresponding bulk field theory possibly by a kind of [[holographic principle]]. This general mechanism we discuss in 

* _[Boundary field theory](#BoundaryFieldTheory)_.

But plain boundaries are just the first example of a general phenomenon known as "[[QFT with defects|defects]]" or "phase dualities" or "singularities" in field theories. Notably the boundary field theory itself may have boundaries, in which case this means that the original theory had _[[manifold with corners|corners]]_ where different boundary pieces meet. This we discuss in 

* _[Corner field theory](#CornerFieldTheory)_.

Generally there are fields theories with general such singularties:

[[!include field theory with boundaries and defects - table]]


#### Idea
 {#PrequantumFieldTheoryIdea}

A _prequantum field theory_ is, at its heart, an assignment that sends a piece of [[worldvolume]]/[[spacetime]] $\Sigma$ -- technically a [[cobordism]] with [[boundary]] and [[corners]] -- to the 

1. [[space]] of [[physical field|field configurations]] over incoming and outgoing pieces of worldvolume/spacetime;

1. the space of field configurations over the bulk worldvolume/spacetime -- the [[trajectories]] of fields;

1. an [[action functional]] that assigns to all these field configurations [[phases]] in a compatible manner. 

These field configurations and spaces of [[trajectories]] between them are represented by [[spans]]/[[correspondences]] of ([[moduli space|moduli]]-)spaces of fields ([[moduli stacks]], really), hence [[diagrams]] of the form

$$
  \mathbf{Fields}_{in}
  \leftarrow
  \mathbf{Fields}
  \rightarrow
  \mathbf{Fields}_{out}
  \,.
$$

Here $\mathbf{Fields}_{in}$ is to be thought of as the space of incoming fields, $\mathbf{Fields}_{out}$ that of outgoing fields, and $\mathbf{Fields}$ the space of all fields on some [[cobordism]] connecting the incoming and the outgoing pieces of [[worldvolume]]/[[spacetime]]. The left map sends such a trajectory to its starting configuration, and the right one sends it to its end configuration.

Given two such spans/correspondences, that share a common field configuration as in 

$$
  \array{
    && \mathbf{Fields}_1 && && \mathbf{Fields}_2
    \\
    & \swarrow && \searrow && \swarrow && \searrow
    \\
    \mathbf{Fields}_{in_1}
    && &&
    \mathbf{Fields}_{out_1} = \mathbf{Fields}_{in_2}
    && &&
    \mathbf{Fields}_{out_2}
  }
$$ 

can be [[composition|composed]], by forming consecutive trajectories from all pairs of trajectories that match in the middle. The space of these composed trajectories is the [[fiber product]] 
$\mathbf{Fields}_1 \underset{{\mathbf{Fields}_{out_1}} \atop {=\mathbf{Fields}_{in_2}}}{\times} \mathbf{Fields}_2$ which sits in a new [[span]]/[[correspondence]]

$$
  \mathbf{Fields}_{in_1}
  \leftarrow
  \mathbf{Fields}_1 \underset{{\mathbf{Fields}_{out_1}} \atop {=\mathbf{Fields}_{in_2}}}{\times} \mathbf{Fields}_2
  \rightarrow
  \mathbf{Fields}_{out_2}
$$

exhibiting the composite of the previous two. This way, spaces of fields with spans/correspondences between them form a [[category]], which we denote $Span_1(\mathbf{H})$ if $\mathbf{H}$ denotes the ambient context (a [[topos]]) in which the spaces of fields live. 

If two cobordisms run in parallel, then the field configurations on their union are pairs of the original field configurations, which are elements in the [[cartesian product]] of spaces of fields. Hence the operations

$$
  \left(
  \mathbf{Fields}_{in}
  \leftarrow
  \mathbf{Fields}
  \rightarrow
  \mathbf{Fields}_{out}
  \right)
  \otimes
  \left(
  \tilde \mathbf{Fields}_{in}
  \leftarrow
  \tilde \mathbf{Fields}
  \rightarrow
  \tilde\mathbf{Fields}_{out}
  \right)  
  \;\;\coloneqq\;\;
  \left(
    \mathbf{Fields}_{in} \times \tilde\mathbf{Fields}_{in}
    \leftarrow
    \mathbf{Fields} \times \tilde\mathbf{Fields}
    \to
    \mathbf{Fields}_{out} \times \tilde\mathbf{Fields}_{out}    
  \right)
$$

make this category of fields and correspondence into a [[monoidal category]]. 

Then a choice of field configurations for a (not yet localized) field theory in dimension $n \in \mathbb{N}$ is a [[monoidal functor]] from a [[category of cobordisms]] of dimension $n$ to such a category of [[spans]]/[[correspondences]]

$$
  \mathbf{Fields} \colon Bord_n^\otimes \to Span_1(\mathbf{H})^\otimes
  \,,
$$

namely a consistent assignment that to each [[closed manifold]] $\Sigma_{n-1}$ of dimension $(n-1)$ assigns a space of field configurations $\mathbf{Fields}(\Sigma_{n-1})$ and that to each [[cobordism]]

$$
  \Sigma_{in} \to \Sigma \leftarrow \Sigma_{out}
$$

assigns a [[span]]/[[correspondence]] of spaces of field configurations and trajectories

$$
  \mathbf{Fields}(\Sigma_{in})
  \leftarrow
  \mathbf{Fields}(\Sigma)
  \rightarrow
  \mathbf{Fields}_{\Sigma_{out}}
  \,.
$$

Apart from the field configurations themselves, prequantum field theory assigns to each [[trajectory]] a "[[phase]]" -- an element in the [[circle group]] $U(1)$ -- by a map called the (exponentiated) [[action functional]]. In order to nicely relate that to the expression of spaces of trajectories as [[spans]]/[[correspondences]] as above, it is useful to think of the [[circle group]] here as being the [[automorphisms]] of something. This is universally accomplished by taking it to be the automorphisms of the unique point in the [[delooping]] [[groupoid]] $\mathbf{B}U(1) = \{\ast \stackrel{c \in U(1)}{\to} \ast\}$. (A lightning review of [[groupoid]]-[[homotopy theory]] is below in [Groupoids and basic homotopy 1-type theory](#GroupoidsAndBasicHomotopy1TypeTheory).) In other words, we think of the group of phases $U(1)$ as the space of [[homotopies]] from the point to itself in the [[Eilenberg-MacLane space]] $\mathbf{B}U(1)$, expressed by the [[diagram]] (a [[homotopy fiber product]] diagram)

$$
  \array{
    && U(1)
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow && \ast 
    \\
    & \searrow && \swarrow
    \\
    && \mathbf{B}U(1)
  }
  \,.
$$

Using this, if we assume for simplicity that the in- and outgoing field configurations are sent constantly to the point in $\mathbf{B}U(1)$, then an (exponentiated) [[action functional]] on the space of trajectories $\exp(i S) \colon \mathbf{Fields} \to U(1)$ is equivalently a [[homotopy]] as shown on the left of the following diagram

$$
  \array{
    && \mathbf{Fields}
    \\
    & \swarrow && \searrow
    \\
    \mathbf{Fields}_{in}
    && \swArrow &&
    \mathbf{Fields}_{out}
    \\
    & {}_{\mathllap{0}}\searrow && \swarrow_{\mathrlap{0}}
    \\
    && \mathbf{B}U(1)
  }
  \;\;\;\;
  \simeq
  \;\;\;\;
  \array{
    && \mathbf{Fields}
    \\
    && \downarrow^{\mathrlap{\exp(i S)}}
    \\
    && U(1)
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow && \ast
    \\
    & \searrow && \swarrow
    \\
    && \mathbf{B}U(1)
  }
  \,.
$$

Hence action functionals are naturally incorporated into [[spans]]/[[correspondences]] of [[moduli spaces]] of fields simply by regarding these to be formed not in the ambient [[topos]] $\mathbf{H}$ itself, but in its [[slice topos]] $\mathbf{H}_{/\mathbf{B}U(1)}$, where each object is equipped with a map to $\mathbf{B}U(1)$ and each morphism with a [[homotopy]] in $\mathbf{B}U(1)$ between the corresponding maps.

We write $\mathrm{Span}_1(\mathbf{H}, \mathbf{B}U(1))$ for the category of spans/correspondences as before, but now equipped with maps to, and transformations over, $\mathbf{B}U(1)$ as in the above diagram. 

Then an [[action functional]] for a choice of field configurations that itself is given as a [[monoidal functor]] $\mathbf{Fields} \colon Bord_n^\otimes \to Span_1(\mathbf{H})$ as above is a monoidal functor

$$
  S \colon Bord_n^\otimes \to Span_1(\mathbf{H}, \mathbf{B}U(1))
$$

such that the spans of spaces of fields are those specified before, hence such that it fits as a lift into the diagram

$$
  \array{
     && Span_1(\mathbf{H}, \mathbf{B}U(1))
     \\
     & {}^{\mathllap{S}}\nearrow & \downarrow 
     \\
     Bord_n &\underset{\mathbf{Fields}}{\to}& Span_1(\mathbf{H})
  }
  \,,
$$

where the right vertical functor [[forgetful functor|forgets]] the phase assignments and just remembers the correspondences of field trajectories.


So far this is a non-local (or: not-necessarily local) prequantum field theory, since it assigns data only to entire $n$-dimensional cobordisms and $(n-1)$-dimensional [[closed manifolds]], but is not guaranteed to be obtained by integrating up local data over little pieces of these manifolds. The latter possibility is however the characteristic property of [[local quantum field theory]], which in turn is the flavor of quantum field theory that seems to matter in nature, and fundamentally.

In order to formalize this localization, we allow the cobordisms to contain higher-[[codimension]] pieces that are [[manifolds with corners]]. These then form not just a [[category of cobordisms]], but an [[(∞,n)-category]] of cobordisms, which we will still denote $Bord_n^\otimes$. If we now have a cobordism with [[codimension]]-2 [[corners]], then the field configurations over it now form a span-of-spans

$$
  \array{
    \mathbf{Fields}_{ii} &\leftarrow& \mathbf{Fields}_{ic} &\to& \mathbf{Fields}_{io}
    \\
    \uparrow && \uparrow && \uparrow
    \\
    \mathbf{Fields}_{ci} &\leftarrow& \mathbf{Fields}_{cc} &\to& \mathbf{Fields}_{co}
    \\
    \downarrow && \downarrow && \downarrow
    \\
    \mathbf{Fields}_{oi} &\leftarrow& \mathbf{Fields}_{oc} &\to& \mathbf{Fields}_{oo}
  }
  \,.
$$

Generally, for $n$-dimensional cobordism that are "localized" all the way to [[corners]] in codimension $n$, their field configurations and trajectories-of-trajectories etc. form $n$-dimensional cubes of spans-of-spans this way. We write $Span_n(\mathbf{H})$ for the resulting [[(∞,n)-category of spans]].

In order to still have an [[action functional]] on trajectories is [[codimension]]-0 associated with this in the above fashion, we need to [[delooping|deloop]] $U(1)$ $n$-times to the [[n-groupoid]] $\mathbf{B}^n U(1)$ (the [[circle n-group|circle (n+1)-group]]). Accordingly a local prequantum field theory in dimension $n$ is given by a [[monoidal (∞,n)-functor]]

$$
  S \colon Bord_n^\otimes \to Span_n(\mathbf{H}, \mathbf{B}^n U(1))
  \,.
$$

The point of local topological (prequantum) field theory is that by the [[cobordism theorem]] the above story reverses: the assignment of fields and their action functional in higher dimension is necessarily given by [[higher traces]] of the data assigned in lower dimension. Hence the whole assignment $S$ above is fixed by its value on the point, hence by a choice of one single map

$$
  \left[
    \array{
      \mathbf{Fields}(\ast)
      \\
      \downarrow^\mathrlap{S}
      \\
      \mathbf{B}U(1)
    }
  \right]
  \,,
$$

the fully localized action functional. Or rather, this is the case for pure bulk field theory, with no [[branes]] or [[domain walls]]. If these are present, then each type of them in dimension $k$ is specified by a [[k-morphism]] in $Span_n(\mathbf{H}, \mathbf{B}^n U(1))$.

All this we now describe more formally.

#### Bulk field theory
 {#BulkFieldTheory}

We now first consider the formalization of prequantum field theory
in the absence of any data such as [[boundary conditions]], [[domain walls]], [[branes]], [[QFT with defects|defects]], etc. This describes either field theories in which no such phenomena are taken to be present, or else it describes that part of those field theories where such phenomena are present in principle, but restricted to the "[[bulk]]" of [[worldvolume]]/[[spacetime]] where they are not. Therefore it makes sense to speak of _bulk field theory_ in this case.

+-- {: .num_defn #nCategoryOfCobordisms}
###### Definition

For $n \in \mathbb{N}$, write

$$
  Bord_n^\otimes \in E_\infty Alg(Cat_{(\infty,n)})
$$

for the [[symmetric monoidal (∞,n)-category]] [[(∞,n)-category of cobordisms|of cobordisms]] with $n$-dimensional [[framed manifold|framing]]. For $S \to O(n)$ a homomorphism of [[∞-groups]] (may be modeled by a homomorphism of [[topological groups]]) to the [[general linear group]] (or homotopy-equivalently its [[maximal compact subgroup]], the [[orthogonal group]]), we write 

$$
  (Bord_n^S)^\otimes \in E_\infty Alg(Cat_{(\infty,n)})
$$

for the corresponding symmetric monoidal $(\infty,n)$-category of cobordisms equipped with [[G-structure|S-structure]] on their $n$-stabilized [[tangent bundle]]. 

=--

+-- {: .num_remark}
###### Remark

In this notation we have an identification

$$
  Bord_n \simeq Bord_n^{S \coloneqq \ast}
$$

because a [[framing]] of the $n$-stabilized tangent bundle is a trivialization of that bundle and hence equivalently a [[G-structure]] for $G$ the trivial group. In ([LurieTFT](#LurieTFT)) this is denoted by "$Bord_n^{fr}$".

=--

+-- {: .num_remark}
###### Remark

The [[cobordism theorem]] asserts, essentially, that $Bord_n$ is the [[symmetric monoidal (∞,n)-category]] with [[fully dualizable objects|full duals]] which is [[free construction|free]] on a single generator, the point. In itself this is a deep statement about the [[homotopy type]] of [[categories of cobordisms]]. But for the following discussion the reader may just take this as the _definition_ of $Bord_n$. This then makes $Bord_n$ a very simple object, as long as we are just mapping out of it, which we do.

What this means then is that a [[monoidal (∞,n)-functor]] 

$$
  Z \colon Bord_n^\otimes \to \mathcal{C}^\otimes
$$

sends the point to some [[fully dualizable object]] $Z(\ast) \in \mathcal{C}$ and sends

* the [[circle]] $S^1$ to the [[trace]] of the identity on $Z(\ast)$, 

* the [[sphere]] $S^2$ to the 2-dimensional [[higher trace]] of the identity,

and so on.


=--

+-- {: .num_defn #CorrespondencesInInfinityTopos}
###### Definition

For $\mathbf{H}$ an [[∞-topos]], and $n \in \mathbb{N}$, write 

$$
  Span_n(\mathbf{H}) \in Cat_{(\infty,n)}
$$

for the [[(∞,n)-category of spans]] in $\mathbf{H}$. From the [[cartesian monoidal category]] structure of $\mathbf{H}$ this inherits the structure of a [[symmetric monoidal (∞,n)-category]] which we write 

$$
  Span_n(\mathbf{H})^\otimes \in E_\infty Alg(Cat_{(\infty,n)})
  \,.
$$

=--

+-- {: .num_prop #FullSelfDualizabilityInSpan}
###### Proposition

Every object in $Span_n(\mathbf{H})$ is a self-[[fully dualizable object]]. The [[evaluation map]]/[[coevaluation map]] $k$-spans in dimension $k$ involve in top degree the spans

$$
  \ast \leftarrow X \stackrel{}{\to} [\Pi(S^k), X]
  \,.
$$

(...)

=--

+-- {: .num_defn #CorrespondencesOverB}
###### Definition

For $B \in Grp(\mathbf{H})$ an [[abelian ∞-group]] object in $\mathbf{H}$, spans in the [[slice (∞,1)-topos]]  $\mathbf{H}_{/B}$ inherits a monoidal structure given on objects by

$$  
  \otimes
    \;
    \colon
    \;
  \left[
    \array{
      X \\ \downarrow^{\mathrlap{f}} \\ B
    }
  \right]
  \times 
  \left[
    \array{
      Y \\ \downarrow^{\mathrlap{g}} \\ B
    }
  \right]
  \mapsto
  \left[
    \array{
      X \times Y \\ \downarrow^{\mathrlap{f \circ p_1 + g \circ p_2}}
     \\
     B
    }
    \;\;\;\;\;\;\;\;\;\;
  \right]
  \,.
$$

We write

$$
  Span_n(\mathbf{H}, B)^\otimes \in E_\infty Alg(Cat_{(\infty,n)})
$$

for the resulting [[symmetric monoidal (∞,n)-category]].

=--

+-- {: .num_remark}
###### Remark

In the case that $\mathbf{H} = $ [[∞Grpd]] this is a special case of ([LurieTFT, around prop. 3.2.8](#LurieTFT)), with the [[abelian ∞-group]] $B$ regarded as a special case of a [[symmetric monoidal (∞,1)-category]]. 

=--

+-- {: .num_remark}
###### Remark

Since the [[slice (∞,1)-category]] $\mathbf{H}_{/\flat \mathbf{B}^n U(1)}$ is itself an [[(∞,1)-topos]] -- the [[slice (∞,1)-topos]] -- we also have $Span_n(\mathbf{H}_{/\flat \mathbf{B}^n U(1)})$, according to def. \ref{CorrespondencesInInfinityTopos}. As an [[(∞,n)-category]] this is equivalent to $Span_n(\mathbf{H}, \flat \mathbf{B}^n U(1))$ from def. \ref{CorrespondencesOverB}, but the [[monoidal (∞,n)-category|monoidal structure]] is different. The [[cartesian product]] in the slice is given by [[homotopy fiber product]] in $\mathbf{H}$ over $\flat \mathbf{B}^n U(1)$, not by the addition in the [[∞-group]] structure on $\flat \mathbf{B}^n U(1)$, as in def. \ref{CorrespondencesOverB}.

=--

The central definition in the present context now is the following.

+-- {: .num_defn #LocalPrequantumFieldWithAction}
###### Definition

A **local prequantum bulk [[field (physics)|field]]** in [[dimension]] $n \in \mathbb{N}$ (in a given ambient [[cohesive (∞,1)-topos]] $\mathbf{H}$) is a [[monoidal (∞,n)-functor]]

$$
  \mathbf{Fields} \;\colon\; Bord^S_n \to Span_n(\mathbf{H})
$$

from the [[(∞,n)-category of cobordisms]] (with [[G-structure|S-structure]]), def. \ref{nCategoryOfCobordisms}, to the [[(∞,n)-category of n-fold correspondences]] in $\mathbf{H}$.

A **local action functional** on such a local prequantum bulk [[field (physics)|field]] is a monoidal lift $S$ of this in 

$$
  \array{
     && Span_n(\mathbf{H}, \flat \mathbf{B}^n U(1))
     \\
     & {}^{\mathllap{S}}\nearrow & \downarrow^{\mathrlap{Span_n\left(\underset{\flat \mathbf{B}^n U(1)}{\sum}\right)}}
     \\
     Bord_n^S 
     &\underset{\mathbf{Fields}}{\to}&
     Span_n(\mathbf{H})
  }
  \,.
$$

=--

For $\mathbf{H} = $ [[∞Grpd]] this is the perspective in ([FHLT, section 3](#FHLT)).

+-- {: .num_remark}
###### Remark

Since a monoidal $(\infty,n)$-functor $\mathbf{Fields} \colon Bord_n \to Span_n(\mathbf{H})$ is determined by its value on the point, we will often notationally identify it with this value and write

$$
  \mathbf{Fields} = \mathbf{Fields}(\ast) \in \mathbf{H} \hookrightarrow Span_n(\mathbf{H})
  \,.
$$



=--

As a corollary of prop. \ref{FullSelfDualizabilityInSpan} we have:

+-- {: .num_prop #ValueOfLocalPrequantumFieldTheoryOnCobordism}
###### Proposition

Given $\mathbf{Fields} \colon Bord_n^\otimes \to Span_n(\mathbf{H})^\otimes$, it assigns to a [[k-morphism]] represented by a [[closed manifold]] $\Sigma_k$ the [[internal hom]] ([[mapping stack]]) from  $\Pi(\Sigma_k)$ (the [[shape modality]] of $\Sigma_k$, def. \ref{ShapeAndFlatModality}) into the moduli stack of fields

$$
  \mathbf{Fields}
  \colon
  \Sigma_k
  \mapsto
  [\Pi(\Sigma_k), \mathbf{Fields}]
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

By the defining property of the [[mapping stack]] construction, this means that if $\mathcal{C}$ is an [[(∞,1)-site]] of definition of the [[(∞,1)-topos]] $\mathbf{H}$, then $[\Pi(\Sigma_k), \mathbf{Fields}]$ is the [[∞-stack]] which to $U \in \mathcal{C}$ assigns the [[(∞,1)-categorical hom space]]

$$
  [\Pi(\Sigma_k), \mathbf{Fields}](U) \simeq
  \mathbf{H}(\Pi(\Sigma_k)\times U , \mathbf{Fields})
  \,,
$$

hence the [[∞-groupoid]] of fields on $\Pi(\Sigma_k) \times U$. 

If $\mathbf{Fields}$ is a [[moduli ∞-stack]] of [[gauge fields]] for some [[smooth ∞-group]] $G$, hence of the form $\mathbf{B}G_{conn}$, then this an $\infty$-groupoid of a kind of smoothly (or else geometrically) $U$-parameterized collections of [[flat ∞-connections]] on $\Sigma_k$.

=--

(...)

#### Boundary field theory
 {#BoundaryFieldTheory}

(...)

#### Corner field theory
 {#CornerFieldTheory}

(...)


### Higher Dijkgraaf-Witten local prequantum field theory
 {#HigherDijkgraafWittenLocalPrequantumFieldTheory}

We discuss here aspects of higher [[Dijkgraaf-Witten theory]]-type 
prequantum field theories, which are those prequantum field theories 
whose moduli stack $\mathbf{Fields}$ is a [[discrete ∞-groupoid]] 
(and usually also required to be finite, especially if its [[quantization]] is considered).
This is a special case of the higher Chern-Simons theories discussed below in _[Higher Chern-Simons local prequantum field theory](#HigherChern-SimonsLocalPrequantumFieldTheory)_, and hence strictly speaking need not be discussed separately. We use it here as a means to review some of the relevant [[homotopy theory]] by way of pertinent examples.

The original [[Dijkgraaf-Witten theory]] is that in dimension 3 (reviewed in _[3d Local prequantum field theory](#3dDWLocalPrequantumFieldTheory)_ below), which was introduced in 
([Dijkgraaf-Witten 90](Dijkgraaf-Witten+theory#DijkgraafWitten90)) as a toy version of standard 3d [[Chern-Simons theory]] for [[simply connected topological space|simply connected]] [[gauge group]]. A comprehensive account with first indications of its role as a local (extended, multi-tiered) field theory
then appeared in 
([Freed-Quinn 93](Dijkgraaf-Witten+theory#FreedQuinn93)), and ever since this has served as a testing ground for understanding the general principles of local field theory, e.g. 
([Freed 94](Dijkgraaf-Witten+theory#Freed94)), 
independently of the subtleties of giving meaning to concepts such as the path integral when the space of fields is not finite.
In section 3 of ([FHLT 10](#FHLT)), the general prequantum formalization as in  def. \ref{LocalPrequantumFieldWithAction} is sketched for Dijkgraaf-Witten type theories, 
and in section 8 there the quantization of these
theories to genuine local quantum field theories is sketched.



#### 1d Dijkgraaf-Witten theory
 {#1dDWTheory}

[[Dijkgraaf-Witten theory]] in [[dimension]] 1 is what results when one regards a [[group character]] of a [[finite group]] $G$ as a local 
[[action functional]] in 
the sense of def. \ref{LocalPrequantumFieldWithAction}.
We give now an expository discussion of this simple but instructive example of a local prequantum field theory and in the course of it
introduce some of the relevant basics of the [[homotopy theory]] of [[groupoids]] ([[homotopy 1-types]]).

1. [Finite gauge groups](#FiniteGaugeGroups)

1. [Essence of gauge theory: Groupoids and basic homotopy 1-type theory](#GroupoidsAndBasicHomotopy1TypeTheory) 

1. [Trajectories of fields: Correspondences of groupoids](#CorrespondencesOfGroupoids)

1. [Action functionals on spaces of trajectories: Correspondences of groupoids over the space of phases](#1dDWLocalFieldTheory)

The punchline of this section is little theorem \ref{GroupCharacterPrequantumTheoryOnCircle} at the very end, which states that the 1d local prequantum field theory whose local action functional is the delooping of a [[group character]] assigns to the circle the [[action functional]] which is again that group character. The proof of this statement is an unwinding of the basic mechanisms of local prequantum field theories.


##### Finite gauge groups
 {#FiniteGaugeGroups} 

First some brief remarks, before we dive into the formalism.

A [[group character]] on a [[finite group]] $G$ is just a [[group]] [[homomorphism]] $G \to U(1)$ to the [[circle group]] (taken here as a [[discrete group]]).
In order to regard this as an [[action functional]], 
we are to take $G$ as the 
[[gauge group]] of a physical field theory. The simplest
such case is a field theory such that on the point there is 
just a single possible field configuration, to be denoted $\phi_0$.
The reader familiar with basics of traditional [[gauge theory]] may think of the fields as being 
[[gauge field]] [[connections]] ("[[vector potentials]]"), hence represented by  [[differential 1-forms]]. But on the point there is only the vanishing 1-form, hence just a single field configuration $\phi_0$.

Even though there is just a single such field, that $G$ is the [[gauge group]] means that for each [[element]] $g \in G$ there is a 
[[gauge transformation]] that takes
$\phi_0$ to itself, a state of affairs which we suggestively denote by the symbols
$$
  \phi_0 \stackrel{g}{\to}  \phi_0
  \,.
$$

Again, the reader familiar with 
traditional [[gauge theory]] may think of [[gauge transformations]] as in [[Yang-Mills theory]]. Over the point these form, indeed, just the [[gauge group]] itself, taking the trivial field configuration to itself.

That the [[gauge group]] is indeed a [[group]] means that gauge transformations can be  applied consecutively, which we express in symbols as

$$
  \array{
    && \phi_0
    \\
    & {}^{\mathllap{g_1}}\nearrow && \searrow^{\mathrlap{g_2}}
    \\
    \phi_0 && \underset{g_2 \cdot g_1}{\to} && \phi_0
  }
  \,.
$$

Regarded this way, we say the [[gauge group]] acting on the single field $\phi_0$ forms a _[[groupoid]]_, whose single _[[object]]_ is $\phi_0$ and whose set of _[[morphisms]]_ is $G$. 

Of course in richer field theories there may be more than one field configuration, clearly, with gauge transformations between them. If $\phi_0$ and $\phi_1$ are two field configurations and $g$ is a gauge transformation taking one to the other, we may usefully denote this by

$$
  \array{
    \phi_0 &\stackrel{g_1}{\to}& \phi_1
  }
   \,.
$$

Similarly then for yet another gauge configuration to another field configuration

$$
  \array{
    \phi_1 &\stackrel{g_2}{\to}& \phi_2
  }
$$


then composing them gives the picture

$$
  \array{
    && \phi_1
    \\
    & {}^{\mathllap{g_1}}\nearrow && \searrow^{\mathrlap{g_2}}
    \\
    \phi_0 && \underset{g_2 \cdot g_1}{\to} && \phi_2
  }
  \,.
$$

We now discuss this notion of [[groupoids]] more formally.

##### Essence of gauge theory: Groupoids and basic homotopy 1-type theory
 {#GroupoidsAndBasicHomotopy1TypeTheory}


The following is a quick review of basics of [[groupoids]] and their [[homotopy theory]] ([[homotopy 1-type]]-theory), geared towards the constructions and fact needed for 1-dimensional Dijkgraaf-Witten theory. 

+-- {: .num_defn #Groupoid}
###### Definition

A ([[small category|small]]) _[[groupoid]]_ $\mathcal{G}_\bullet$ is

* a pair of [[sets]] $\mathcal{G}_0 \in Set $ (the set of [[objects]]) and $\mathcal{G}_1 \in Set$ (the set of [[morphisms]])

* equipped with [[functions]]

  $$
    \array{
      \mathcal{G}_1 \times_{\mathcal{G}_0} \mathcal{G}_1
      &\stackrel{\circ}{\to}&
      \mathcal{G}_1
      & \stackrel{\overset{t}{\to}}{\stackrel{\overset{i}{\leftarrow}}{\underset{s}{\to}}}&
      \mathcal{G}_0
    }\,,
  $$

  where the [[fiber product]] on the left is that over $\mathcal{G}_1 \stackrel{t}{\to} \mathcal{G}_0 \stackrel{s}{\leftarrow} \mathcal{G}_1$, 

such that

* $i$ takes values in [[endomorphisms]];

  $$
    t \circ i = s \circ i =   id_{\mathcal{G}_0}, \;\;\; 
  $$

* $\circ$ defines a partial [[composition]] operation which is [[associativity|associative]] and [[unitality|unital]] for $i(\mathcal{G}_0)$ the [[identities]]; in particular

  $s (g \circ f) = s(f)$ and $t (g \circ f) = t(g)$;

* every morphism has an [[inverse]] under this composition.

=--

+-- {: .num_remark }
###### Remark

This data is visualized as follows. The set of morphisms is 

$$
  \mathcal{G}_1
  = 
  \left\{
    \phi_0 \stackrel{k}{\to} \phi_1
  \right\}
$$

and the set of pairs of composable morphisms is

$$
  \mathcal{G}_2 \coloneqq \mathcal{G}_1 \underset{\mathcal{G}_0}{\times} \mathcal{G}_1
  =
  \left\{
    \array{
      && \phi_1
      \\
      & {}^{\mathllap{k_1}}\nearrow && \searrow^{\mathrlap{k_2}}
      \\
      \phi_0 && \stackrel{k_2 \circ k_1}{\to} && \phi_2
    }
  \right\}
  \,.
$$

The functions $p_1, p_2, \circ \colon \mathcal{G}_2 \to \mathcal{G}_1$ are those which send, respectively, these triangular diagrams to the left morphism, or the right morphism, or the bottom morphism.

=--

+-- {: .num_example #SetAsGroupoid}
###### Example

For $X$ a [[set]], it becomes a groupoid by taking $X$ to be the set of objects and adding only precisely the [[identity]] morphism from each object to itself

$$
  \left(
    X 
    \stackrel
    {\overset{id}{\to}}
    {
      \stackrel{\overset{id}{\leftarrow}}{\underset{id}{\to}}
    }
   X
  \right)
  \,.
$$

=--


+-- {: .num_example #DeloopingGroupoid}
###### Example

For $G$ a [[group]], its [[delooping]] [[groupoid]] $(\mathbf{B}G)_\bullet$ has

* $(\mathbf{B}G)_0 = \ast$;

* $(\mathbf{B}G)_1 = G$.

For $G$ and $K$ two groups, group homomorphisms $f \colon G \to K$
are in [[natural bijection]] with groupoid homomorphisms
$$
  (\mathbf{B}f)_\bullet
  \;\colon\;
  (\mathbf{B}G)_\bullet \to (\mathbf{B}K)_\bullet
  \,.
$$

In 
particular a [[group character]] $c \colon G \to U(1)$ is equivalently a groupoid homomorphism

$$
  (\mathbf{B}c)_\bullet 
   \;\colon\;
   (\mathbf{B}G)_\bullet 
     \to
   (\mathbf{B}U(1))_\bullet
  \,.
$$

Here, for the time being, all groups are [[discrete groups]]. Since the [[circle group]] $U(1)$ also has a standard structure of a [[Lie group]], and since later for the discussion of Chern-Simons type theories this will be relevant, we will write from now on

$$
  \flat U(1) \in Grp
$$

to mean explicitly the [[discrete group]] underlying the circle group. (Here "$\flat$" denotes the "[[flat modality]]".)

=--

+-- {: .num_example #ActionGroupoid}
###### Example

For $X $ a [[set]], $G$ a [[discrete group]] and $\rho \colon X \times G \to X$ an [[action]] of $G$ on $X$ (a [[permutation representation]]), the **[[action groupoid]]** or **[[homotopy quotient]]** of $X$ by $G$ is the groupoid

$$
  X//_\rho G
  = 
  \left(
    X \times G
    \stackrel{\overset{\rho}{\to}}{\underset{p_1}{\to}}
    X
  \right)
$$

with composition induced by the product in $G$. Hence this is the groupoid whose objects are the elements of $X$, and where [[morphisms]] are of the form

$$
  x_1 \stackrel{g}{\to} x_2 = \rho(x_1)(g)
$$

for $x_1, x_2 \in X$, $g \in G$.

=--

As an important special case we have:

+-- {: .num_example #BGGroupoidAsActionGroupoid}
###### Example

For $G$ a [[discrete]] group and $\rho$ the trivial action of $G$ on the point $\ast$ (the singleton set), the coresponding [[action groupoid]] according to def. \ref{ActionGroupoid} is the [[delooping]] groupoid of $G$ according to def. \ref{DeloopingGroupoid}:

$$
  (\ast //G)_\bullet = (\mathbf{B}G)_\bullet
  \,.
$$

Another canonical action is the action of $G$ on itself by right multiplication. The corresponding action groupoid we write

$$
  (\mathbf{E}G)_\bullet \coloneqq G//G
  \,.
$$

The constant map $G \to \ast$ induces a canonical morphism

$$
  \array{
    G//G & \simeq & \mathbf{E}G
    \\
    \downarrow && \downarrow
    \\
    \ast //G & \simeq & \mathbf{B}G
  }
  \,.
$$

This is known as the $G$-[[universal principal bundle]]. See below in \ref{PullbackOfEGGroupoidAsHomotopyFiberProduct} for more on this.

=--

+-- {: .num_example }
###### Example

The [[interval]] $I$ is the groupoid with 

* $I_0 = \{a,b\}$;
* $I_1 = \{\mathrm{id}_a, \mathrm{id}_b, a \to  b \}$.

=--

+-- {: .num_example #FundamentalGroupoid}
###### Example

For $\Sigma$ a [[topological space]], its [[fundamental groupoid]]
  $\Pi_1(\Sigma)$ is

* $\Pi_1(\Sigma)_0 = $ points in $X$;
* $\Pi_1(\Sigma)_1 = $ [[continuous function|continuous]] paths in $X$ modulo [[homotopy]] that leaves the endpoints fixed.

=--

+-- {: .num_example #PathSpaceGroupoid}
###### Example

For $\mathcal{G}_\bullet$ any groupoid, there is the [[path space]] groupoid $\mathcal{G}^I_\bullet$ with

* $\mathcal{G}^I_0 = \mathcal{G}_1 = \left\{ \array{ \phi_0 \\ \downarrow^{\mathrlap{k}} \\ \phi_1  } \right\}$;

* $\mathcal{G}^I_1 = $ [[commuting diagram|commuting squares]] in $\mathcal{G}_\bullet$ = 
  $
    \left\{
       \array{
          \phi_0 &\stackrel{h_0}{\to}& \tilde \phi_0
          \\
          {}^{\mathllap{k}}\downarrow && \downarrow^{\mathrlap{\tilde k}}
          \\
          \phi_1 &\stackrel{h_1}{\to}& \tilde \phi_1
       }
    \right\}
    \,.
  $   

This comes with two canonical homomorphisms

  $$
    \mathcal{G}^I_\bullet
     \stackrel{\overset{ev_1}{\to}}{\underset{ev_0}{\to}}
	   \mathcal{G}_\bullet
  $$

  which are given by endpoint evaluation, hence which send such a commuting square to either its top or its bottom hirizontal component.


=--

+-- {: .num_defn }
###### Definition

For $f_\bullet, g_\bullet : \mathcal{G}_\bullet \to \mathcal{K}_\bullet$
two morphisms between groupoids,
  a _[[homotopy]]_ $f \Rightarrow g$ 
(a [[natural transformation]]) is
  a homomorphism of the form $\eta_\bullet : \mathcal{G}_\bullet \to \mathcal{K}^I_\bullet$
  (with [[codomain]] the [[path space object]] of $\mathcal{K}_\bullet$ as in example \ref{PathSpaceGroupoid})
  such that it fits into the diagram as depicted here on the right:
  $$
    \array{
      & \nearrow  \searrow^{\mathrlap{f_\bullet}}
      \\
      \mathcal{G} &\Downarrow^{\mathrlap{\eta}}& \mathcal{K}
     \\
     & \searrow \nearrow_{\mathrlap{g_\bullet}}
    }

	\;\;\;\;
	\coloneqq
	\;\;\;\;
    \array{
      && \mathcal{K}_\bullet
      \\
      & {}^{\mathllap{f_\bullet}}\nearrow & \uparrow^{\mathrlap{(ev_1)_\bullet}}
      \\
      \mathcal{G}_\bullet
      &\stackrel{\eta_\bullet}{\to}&
      \mathcal{K}^I_\bullet
      \\
      & {}_{\mathllap{g_\bullet}}\searrow & \downarrow^{\mathrlap{(ev_0)_\bullet}}
      \\
      && \mathcal{K}
    }
    \,.
  $$

=--

+-- {: .num_defn #GroupoidsAsHomotopy1Types}
###### Definition (Notation)

Here and in the following, the convention is that we write

* $\mathcal{G}_\bullet$ (with the subscript decoration) when we regard groupoids with just 
homomorphisms ([[functors]]) between them, 

* $\mathcal{G}$ (without the subscript decoration) when we regard groupoids
with homomorphisms ([[functors]]) between them and [[homotopies]] ([[natural transformations]]) between these

  $$
    \array{
      & \nearrow \searrow^{\mathrlap{f}}
      \\
      X &\Downarrow& Y
      \\
      & \searrow \nearrow_{g}
    }
    \,.
  $$

The unbulleted version of groupoids are also called _[[homotopy 1-types]]_ (or often just their [[homotopy]]-[[equivalence classes]] are called this way.) Below we generalize this to arbitrary homotopy types (def. \ref{KanComplexesAsHomotopyTypes}).

=--



+-- {: .num_example #MappingGroupoid}
###### Example

For $X,Y$ two groupoids, the [[internal hom|mapping groupoid]] $[X,Y]$ or $Y^X$ is

* $[X,Y]_0 = $ homomorphisms $X \to Y$;
* $[X,Y]_1 = $ homotopies between such. 

=--

+-- {: .num_defn #HomotopyEquivalenceOfGroupoids}
###### Definition

  A ([[homotopy equivalence|homotopy-]]) _[[equivalence of groupoids]]_ is a morphism
$\mathcal{G} \to \mathcal{K}$ which has a left and right [[inverse]] up to [[homotopy]].  

=--

+-- {: .num_example #BZIsPiSOne}
###### Example

The map

$$
  \mathbf{B}\mathbb{Z} \stackrel{}{\to} \Pi(S^1)
$$

which picks any point and sends $n \in \mathbb{Z}$ to the loop based at that point which winds around $n$ times, is an [[equivalence of groupoids]].

=--


+-- {: .num_prop #DiscreteGroupoidIsDijointUnioonOfDeloopings}
###### Proposition

  Assuming the [[axiom of choice]] in the ambient [[set theory]],
  every groupoid is equivalent to a disjoint union of 
  [[delooping]] groupoids,
  example \ref{DeloopingGroupoid} -- a _[[skeleton]]_.

=--

+-- {: .num_remark}
###### Remark

 The statement of prop. \ref{DiscreteGroupoidIsDijointUnioonOfDeloopings} 
 becomes false as when we pass to groupoids that are equipped with
 [[geometry|geometric]] structure. This is the reason why for discrete geometry all  [[Chern-Simons theory|Chern-Simons]]-type field theories (namely [[Dijkgraaf-Witten theory]]-type theories) fundamentally involve just groups (and higher groups),
 while for nontrivial geometry there are genuine groupoid theories, 
 for instance the [[AKSZ sigma-models]]. But even so, 
 [[Dijkgraaf-Witten theory]] is usefully discussed in terms of groupoid technology, in particular since the choice of equivalence in 
 prop. \ref{DiscreteGroupoidIsDijointUnioonOfDeloopings} is not canonical.

=--

+-- {: .num_defn #HomotopyFiberProductOfGroupoids}
###### Definition

Given two morphisms of groupoids 
$X \stackrel{f}{\leftarrow} B \stackrel{g}{\to} Y$
their _[[homotopy fiber product]]_

$$
  \array{
   X \underset{B}{\times} Y
   &\stackrel{}{\to}& X
   \\
   \downarrow &\swArrow& \downarrow^{\mathrlap{f}}
   \\
   Y &\underset{g}{\to}& B
  }
$$

is the [[limit]] [[cone]]

$$
  \array{
    X_\bullet \underset{B_\bullet}{\times} B^I_\bullet
    \underset{B_\bullet}{\times} Y_\bullet
    &\to& &\to& X_\bullet
    \\
    \downarrow && && \downarrow^{\mathrlap{f_\bullet}}
    \\
    && B^I_\bullet &\underset{(ev_0)_\bullet}{\to}& B_\bullet
    \\
    \downarrow && \downarrow^{\mathrlap{(ev_1)_\bullet}}
    \\
    Y_\bullet &\underset{g_\bullet}{\to}& B_\bullet
  }
  \,,
$$

hence the ordinary iterated [[fiber product]] over the [[path space]] groupoid, as indicated.

=--

+-- {: .num_remark #FiberProductsOfGroupoidsComponentwise}
###### Remark

An ordinary fiber product $X_\bullet \underset{B_\bullet}{\times}Y_\bullet$ of groupoids is given simply by the fiber product of the underlying sets of objects and morphisms:

$$
  (X_\bullet \underset{B_\bullet}{\times}Y_\bullet)_i 
  =
  X_i \underset{B_i}{\times} Y_i
  \,.
$$

=--


+-- {: .num_example #PullbackOfEGGroupoidAsHomotopyFiberProduct}
###### Example

For $X$ a [[groupoid]], $G$ a [[group]] and $X \to \mathbf{B}G$ a map into its [[delooping]], the [[pullback]] $P \to X$ of the $G$-[[universal principal bundle]] of example \ref{BGGroupoidAsActionGroupoid}
is equivalently the [[homotopy fiber product]] of $X$ with the point over $\matrhbf{B}G$:

$$
  P \simeq X \underset{\mathbf{B}G}{\times} \ast
  \,.
$$

Namely both squares in the following diagram are pullback squares

$$
  \array{
    P
    &\to& \mathbf{E}G &\to& \ast_\bullet
    \\
    \downarrow && && \downarrow^{\mathrlap{}}
    \\
    && (\mathbf{B}G)^I_\bullet &\underset{(ev_0)_\bullet}{\to}& (\mathbf{B}G)_\bullet
    \\
    \downarrow && \downarrow^{\mathrlap{(ev_1)_\bullet}}
    \\
    X_\bullet &\underset{}{\to}& (\mathbf{B}G)_\bullet
  }
  \,.
$$

(This is the first example of the more general phenomenon of [[universal principal infinity-bundles]].)

=--

+-- {: .num_example #LoopSpaceGroupoid}
###### Example

For $X$ a [[groupoid]] and $\ast \to X$ a point in it, we call

$$
  \Omega X
  \coloneqq
  \ast \underset{X}{\times} \ast
$$

the [[loop space object|loop space groupoid]] of $X$.

For $G$ a group and $\mathbf{B}G$ its  [[delooping]] groupoid from
  example \ref{DeloopingGroupoid}, we have
  $$
    G \simeq \Omega \mathbf{B}G = \ast \underset{\mathbf{B}G}{\times} \ast
    \,.
  $$

 Hence $G$ is the [[loop space object]] of its own [[delooping]], as it should be.

=--

+-- {: .proof}
###### Proof

We are to compute the ordinary limiting cone $\ast \underset{\mathbf{B}G_\bullet}{\times}  (\mathbf{B}G^I)_\bullet \underset{\mathbf{B}G_\bullet}{\times} \ast$ in

$$
  \array{
    &\to& &\to& \ast
    \\
    \downarrow && && \downarrow^{\mathrlap{}}
    \\
    && (\mathbf{B}G)^I_\bullet &\underset{(ev_0)_\bullet}{\to}& \mathbf{B}G_\bullet
    \\
    \downarrow && \downarrow^{\mathrlap{(ev_1)_\bullet}}
    \\
    \ast &\underset{}{\to}& \mathbf{B}G_\bullet
  }
  \,,
$$

In the middle we have the groupoid $(\mathbf{B}G)^I_\bullet$ whose objects are elements of $G$ and whose morphisms starting at some element are labeled by pairs of elements $h_1, h_2 \in G$ and end at $h_1 \cdot g \cdot h_2$. 
Using remark \ref{FiberProductsOfGroupoidsComponentwise} 
the limiting cone is seen to precisely pick those morphisms in $(\mathbf{B}G_\bullet)^I_\bullet$ such that these two elements are constant on the neutral element $h_1 = h_2 = e = id_{\ast}$, hence it produces just the elements of $G$ regarded as a groupoid with only identity morphisms, as in example \ref{SetAsGroupoid}.

=--

+-- {: .num_prop #FreeLoopSpaceOfGroupoid}
###### Proposition


The [[free loop space object]] is

  $$
    [\Pi(S^1), X]
	\simeq
	X \underset{[\Pi(S^0), X]}{\times}X
  $$

=--

+-- {: .proof}
###### Proof

Notice that $\Pi_1(S^0) \simeq \ast \coprod \ast$. Therefore
the [[path space object]] $[\Pi(S^0), X_\bullet]^I_\bullet$ has

* objects are pairs of morphisms in $X_\bullet$;

* morphisms are commuting squares of such.

Now the fiber product in def. \ref{HomotopyFiberProductOfGroupoids}
picks in there those pairs of morphisms for which both start at the same object, and both end at the same object. Therefore $X_\bullet \underset{[\Pi(S^0), X_\bullet]_\bullet}{\times} [\Pi(S^0), X_\bullet]^I_\bullet \underset{[\Pi(S^0), X_\bullet]_\bullet}{\times} X$ is the groupoid whose

* objects are diagrams in $X_\bullet$ of the form 

  $$
    \array{
       & \nearrow \searrow
       \\
       x_0 && x_1
       \\
       & \searrow \nearrow
    }
  $$

* morphism are cylinder-diagrams over these.

One finds along the lines of example 
\ref{BZIsPiSOne} that this is equivalent to maps from $\Pi_1(S^1)$ into $X_\bullet$ and homotopies between these.

=--

+-- {: .num_remark}
###### Remark

Even though all these models of the circle $\Pi_1(S^1)$ are equivalent,
below the special appearance of the circle in the proof of 
prop. \ref{FreeLoopSpaceOfGroupoid} as the combination of two semi-circles will be important for the following proofs. 
As we see in a moment, this is the natural way in which the circle
appears as the composition of an [[evaluation map]] with a [[coevaluation map]].

=--

+-- {: .num_example #AdjointActionGroupoidFromFreeLoopSpaceObject}
###### Example

For $G$ a [[discrete group]], the [[free loop space object]] of its [[delooping]] $\mathbf{B}G$ is $G//_{ad} G$, the [[action groupoid]], def. \ref{ActionGroupoid}, of the [[adjoint action]] of $G$ on itself:

$$
  [\Pi(S^1), \mathbf{B}G] \simeq G//_{ad} G
  \,.
$$

=--

+-- {: .num_example }
###### Example

For an [[abelian group]] such as $\flat U(1)$ we have

$$
  [\Pi(S^1), \mathbf{B}\flat U(1)]
  \simeq
  \flat U(1)//_{ad} \flat U(1)
  \simeq
  (\flat U(1)) \times (\mathbf{B}\flat U(1))
  \,.
$$

=--

+-- {: .num_example #GroupCharacterAsClassFunctionByFreeLoopSpace}
###### Example

Let $c \colon G \to \flat U(1)$ be a group homomorphism, hence a [[group character]]. By example \ref{DeloopingGroupoid} this has a [[delooping]] to a groupoid homomorphism 

$$
  \mathbf{B}c \;\colon\; \mathbf{B}G \to \mathbf{B}\flat U(1)
  \,.
$$

Unde the [[free loop space object]] construction this becomes

$$
  [\Pi(S^1), \mathbf{B}c]
  \;\colon\;
  [\Pi(S^1), \mathbf{B}G]
  \to 
  [\Pi(S^1), \mathbf{B}\flat U(1)]
$$

hence 

$$
  [\Pi(S^1), \mathbf{B}c]
  \;\colon\;
  G//_{ad}G
  \to 
  \flat U(1) \times \mathbf{B}U(1)
  \,.
$$

So by postcomposing with the [[projection]] on the first factor we recover from the general [[homotopy theory]] of groupoids the statement that a group character is a [[class function]] on [[conjugacy classes]]:

$$
  [\Pi(S^1), \mathbf{B}c]
  \;\colon\;
  G//_{ad}G
  \to 
  U(1)
  \,.
$$

=--


##### Trajectories of fields: Correspondences of groupoids 
 {#CorrespondencesOfGroupoids}

With some basic [[homotopy theory]] of [[groupoids]] in hand, we can now talk about [[trajectories]] in finite gauge theories, namely about [[spans]]/[[correspondences]] of groupoids and their composition. These correspondences of groupoids encode [[trajectories]]/histories of [[field (physics)|field configurations]].

Namely consider a groupoid to be called $\mathbf{Fields} \in$ [[Grpd]], to be thought of as the [[moduli space]] of [[field (physics)|fields]] in some field theory, or equivalently and specifically as the [[target space]] of a [[sigma-model]] field theory. This just means that for $\Sigma$ any [[manifold]] thought of as [[spacetime]] or [[worldvolume]], the space of fields $\mathbf{Fields}(\Sigma)$ of the field theory on $\Sigma$ is the [[mapping stack]] ([[internal hom]]) from $\Sigma$ into $\mathbf{Fields}$, which means here for DW theory that it is the mapping groupoid, def. \ref{MappingGroupoid}, out of the fundamental groupoid, def. \ref{FundamentalGroupoid}, of $\Sigma$:
$$
  \mathbf{Fields}(\Sigma) = [\Pi_1(\Sigma), \mathbf{Fields}]
  \,.
$$

We think of the [[objects]] of the groupoid $[\Pi_1(\Sigma), \mathbf{Fields}]$ as being the fields themselves, and of the [[morphisms]] as being the [[gauge transformations]] between them.

The example to be of interest in a moment is that where $\mathbf{Fields} = \mathbf{B}G$ is a [[delooping]] groupoid as in def. \ref{DeloopingGroupoid}, in which case the fields are equivalently [[flat connection|flat]] [[principal connections]]. In fact in the discrete and 1-dimensional case currently considered this is essentially the only example, due to prop. \ref{DiscreteGroupoidIsDijointUnioonOfDeloopings}, but for the general idea and for the more general cases considered further below, it is useful to have the notation allude to more general moduli spaces $\mathbf{Fields}$.

The simple but crucial observation that shows why [[spans]]/[[correspondences]] of groupoids show up in prequantum field theory is the following.

+-- {: .num_example }
###### Example

If $\Sigma$ is a [[cobordism]], hence a [[manifold with boundary]] with incoming [[boundary]] component $\Sigma_{in} \hookrightarrow \Sigma$ and outgoing boundary components $\Sigma_{out} \hookrightarrow \Sigma$, then the resulting [[cospan]] of manifolds

$$
  \array{
    && \Sigma
    \\
    & \nearrow && \nwarrow
    \\
    \Sigma_{in}
    && &&
    \Sigma_{out}
  }
$$

is sent under the operation of mapping into the moduli space of fields

$$
  [\Pi_1(-), \mathbf{Fields}]
  \;\colon\;
  Mfds^{op} \to Grpd
$$

to a [[span]] of groupoids

$$
  \array{
    && [\Pi_1(\Sigma), \mathbf{Fields}]
    \\
    & \swarrow && \searrow
    \\
    [\Pi_1(\Sigma_{in}), \mathbf{Fields}]
    && &&
    [\Pi_1(\Sigma_{out}), \mathbf{Fields}]
  }
  \,.
$$

Here the left and right homomorphisms are those which take a field configuration on $\Sigma$ and restrict it to the incoming and to the outgoing field configuration, respectively. (And this being a homomorphism of groupoids means that everything respects the [[gauge symmetry]] on the fields.) Hence if $[\Pi_1(\Sigma_{in,out}),\mathbf{Fields}]$ is thought of as the spaces of incoming and outgoing field configurations, respectively, then  $[\Pi_1(\Sigma), \mathbf{Fields}]$ is to be interpreted as the space of [[trajectories]] (sometimes: _histories_) of field cofigurations over [[spacetimes]]/[[worldvolumes]] of shape $\Sigma$.

=--

This should make it plausible that specifying the field content of a 1-dimensional discrete gauge field theory is a functorial assignsment

$$
  \mathbf{Fields}
  \;\colon\;
  Bord_1
  \to Span(Grpd)
$$

from a [[category of cobordisms]] of dimension one into a category of such [[spans]] of groupoids. It sends points to spaces of field configurations on the point and 1-dimensional manifolds such as the circle as spaces of trajectories of field configurations on them.

Moreover, for a _local_ field theory it should be true that the field configurations on the circle, says, are determined from gluing the field configurations on any decomposition of the circle, notably a decomposition into two semi-circles. But since we are dealing with a [[topological field theory]], its field configurations on a contractible interval such as the semicircle will be equivalent to the field configurations on the point itself. 

The way that the fields on higher spheres in a topological field theory are induced from the fields on the point is by an analog of _[[traces]]_ for spaces of fields, and higher traces of such correspondences (the "[[span trace]]"). This is because by the [[cobordism theorem]], the field configurations on, notably, the [[n-sphere]] are given by the $n$-fold [[span trace]] of the field configurations on the point, the trace of the traces of the ... of the 1-trace. This is because for instance the 1-sphere, hence the [[circle]] is, regarded as a 1-dimensional [[cobordism]] itself pretty much manifestly a [[trace]] on the point in the [[string diagram]] formulation of traces.

$$
  \array{
     &&  \ast^- 
     \\
     & \swarrow & & \nwarrow
     \\
     \downarrow && && \uparrow
     \\
     & \searrow && \nearrow
     \\
     && \ast^+
  }
  \,.
$$

Here $\ast^+$ is the point with its potitive orientation, and $\ast^-$ is its [[dual object]] in the [[category of cobordisms]], the point with the reverse orientation. Since, by this picture, the construction that produces the circle from the point is one that involves only the [[coevaluation map]] and [[evaluation]] map on the point regarded as a [[dualizable object]], a [[topological field theory]] $Z \colon Bord_n \to Span_n(\mathbf{H})$, since it respects all this structure, takes the circle to precisely the same kind of diagram, but now in $Span_n(\mathbf{H})^\otimes$, where it becomes instead the [[span trace]] on the space $\mathbf{Fields}(\ast)$ over the point. This we discuss now.

Before talking about correspondences of groupoids, we need to organize the groupoids themselves a bit more.

+-- {: .num_defn #TwoOneCategory}
###### Definition 

A  **[[(2,1)-category]]** $\mathcal{C}$ is 

1. a collection $\mathcal{C}_0$  -- the "collection of [[objects]]";

1. for each [[tuple]] $(X,Y) \in \mathcal{C}_0 \times \mathcal{C}_0$ a [[groupoid]] $\mathcal{C}(X,Y)$ -- the _[[hom-groupoid]]_ from $X$ to $Y$;

1. for each [[triple]] $(X,Y,Z) \in \mathcal{C}_0 \times \mathcal{C}_0 \times \mathcal{C}_0$ a groupoid homomorphism ([[functor]])

   $$
     \circ_{X,Y,Z} \colon \mathcal{C}(X,Y) \times \mathcal{C}(Y,Z) \to \mathcal{C}(X,Z)
   $$
  
   called _[[composition]]_ or _[[horizontal composition]]_ for emphasis;

1. for each [[quadruple]] $(W,X,Y,Z,)$ a [[homotopy]] -- the _[[associator]]_ --

   $$
     \array{
        \mathcal{C}(W,X) \times \mathcal{C}(X,Y) \times \mathcal{C}(Y,Z)
        &\stackrel{}{\to}&
        \mathcal{C}(W,Y) \times \mathcal{C}(Y,Z)
        \\
        \downarrow &\swArrow_{\alpha_{W,X,Y,Z}}& \downarrow
        \\
        \mathcal{C}(W,X) \times \mathcal{C}(X,Z)
        &\stackrel{}{\to}&
        \mathcal{C}(W,Z)
     }
   $$

   (...) and similarly a [[unitality]] homotopy (...)
   

such that for each [[quintuple]] $(V,W,X,Y,Z)$ the associators satisfy the [[pentagon identity]].

The [[objects]] of the [[hom-groupoid]] $\mathcal{C}(X,Y)$ we call the _[[1-morphisms]]_ from $X$ to $Y$, indicated by $X \stackrel{f}{\to} Y$, and the [[morphisms]] in $\mathcal{C}(X,Y)$ we call the [[2-morphisms]] of $\mathcal{C}$, indicated by

$$
  \array{
     \\
     & \nearrow \searrow^{\mathrlap{f}}
     \\
    X &\Downarrow&  Y
     \\
     & \searrow \nearrow_{\mathrlap{g}}
  }
  \,.
$$

If all associators $\alpha$ can and are chosen to be the [[identity]] then this is called a _[[strict 2-category|strict (2,1)-category]]_.

=--

+-- {: .num_defn}
###### Definition/Example

Write [[Grpd]] for the [[strict 2-category|strict]] [[(2,1)-category]], 
def. \ref{TwoOneCategory}, whose

* [[objects]] are [[groupoids]] $\mathcal{G}$;

* [[1-morphisms]] are [[functors]] $f \colon \mathcal{G} \to \mathcal{K}$;

* [[2-morphisms]] are [[homotopies]] between these.

=--


+-- {: .num_defn #OneSpansInOneGroupoids}
###### Definition/Example

Write $Span_1(Grpd)$ for the [[(2,1)-category]] whose

* [[objects]] are [[groupoids]];

* [[1-morphisms]] are [[spans]]/[[correspondences]] of [[functors]], hence 

  $$
    \array{
     A
      &\leftarrow&
      X
      &\rightarrow&
     B
     }
     \,;
  $$

* [[2-morphisms]] are [[diagrams]] in [[Grpd]] of the form

  $$
    \array{  
      && X_1
      \\
      & \swarrow &\downarrow& \searrow
      \\
      A &\seArrow& \downarrow^{\mathrlap{\simeq}} &\swArrow& B
      \\
      & \nwarrow &\downarrow& \nearrow
      \\
      && X_2
    }
  $$

* [[composition]] is given by forming the [[homotopy fiber product]], def. \ref{HomotopyFiberProductOfGroupoids}, of the two adjacent homomorphisms of two spans, hence for two spans

  $$
    X \stackrel{}{\leftarrow} K \rightarrow Y
  $$

  and

  $$
    Y \stackrel{}{\leftarrow} L \rightarrow Z
  $$
  
  their composite is the span which is the outer part of the diagram

  $$
    \array{
      && && K \underset{Y}{\times}L
      \\
      && & {}^{\mathllap{p_1}}\swarrow 
      && \searrow^{\mathrlap{p_2}}
      \\
      && K && \swArrow && L
      \\
      & \swarrow && \searrow && \swarrow && \searrow
      \\
      X && && Y && && Z
    }
    \,.
  $$

=--

+-- {: .num_defn }
###### Definition

There is the structure of a [[symmetric monoidal (2,1)-category]] on $Span_1(Grpd)$ by degreewise [[Cartesian product]] in [[Grpd]].

$$
  (X \leftarrow K \rightarrow Y)
  \otimes
  (\tilde X \leftarrow \tilde K \rightarrow \tilde Y)
  \;\coloneqq\;
  X \times \tilde X
  \leftarrow K \times \tilde K
  \rightarrow Y \times \tilde Y
  \,.
$$

=--

+-- {: .num_defn }
###### Definition

An [[object]] $X$ of a [[symmetric monoidal (2,1)-category]] $\mathcal{C}^\otimes$ is [[fully dualizable object|fully dualizable]] if there exists

1. another object $X^\ast$, to be called the _[[dual object]]_;

1. a [[1-morphism]] $ev_X \colon X^\ast \otimes X \to \mathbb{I}$, to be called the _[[evaluation map]]_;

1. a [[1-morphism]]  $coev_X \colon \mathbb{I} \to X \otimes X^\ast$, to be called the [[coevaluation map]];

1. [[2-morphisms]] 

   $$
     \array{
       && \rightarrow
       \\
       & \nearrow &\Downarrow^{coev_{tr(X)}}& \searrow^{\mathrlap{id}_{\mathbb{I}}}
       \\
       \mathbb{I} 
         &\underset{coev_X}{\to}& 
       X^\ast \otimes X
        &\underset{ev_X}{\to}&
       \mathbb{I}
     }
   $$

   and

   $$
     \array{
       && \rightarrow
       \\
       & \nearrow &\Uparrow^{ev_{tr(X)}}& \searrow^{\mathrlap{id}_{\mathbb{I}}}
       \\
       \mathbb{I} 
         &\underset{coev_X}{\to}& 
       X^\ast \otimes X
        &\underset{ev_X}{\to}&
       \mathbb{I}
     }
   $$

   and

   $$
     \array{
       && \rightarrow
       \\
       & \nearrow &\Downarrow^{sa(X)}& \searrow^{\mathrlap{id}_{\mathbb{I}}}
       \\
       X^\ast \otimes X 
         &\underset{ev_X}{\to}& 
       \mathbb{I}
        &\underset{coev_X}{\to}&
       X^\ast \otimes X
     }
   $$

   (the [[saddle]])

   and

   $$
     \array{
       && \rightarrow
       \\
       & \nearrow &\Uparrow^{cosa(X)}& \searrow^{\mathrlap{id}_{\mathbb{I}}}
       \\
       X^\ast \otimes X 
         &\underset{ev_X}{\to}& 
       \mathbb{I}
        &\underset{coev_X}{\to}&
       X^\ast \otimes X
     }
   $$

   (the co-saddle)

such that these exhibit an [[adjunction]] and are themselves adjoint (...).

=--

+-- {: .num_defn }
###### Definition

Given a [[symmetric monoidal (2,1)-category]] $\mathcal{C}$, and a [[fully dualizable object]] $X \in \mathcal{C}$ and a [[1-morphism]]  $f \colon X \to X$, the [[trace]] of $f$ is the [[composition]]

$$
  tr(f)
   \;\colon\;
  \mathbb{I}
    \stackrel{coev_X}{\to}
  X \otimes X^\ast
    \stackrel{f \otimes id_{X^\ast}}{\to}
  X \otimes X^\ast
    \stackrel{ev_x}{\to}
  \mathbb{I}
  \,.
$$

=--


+-- {: .num_prop #GroupoidInSpanOneIsSelfDual}
###### Proposition

Every [[groupoid]] $X \in Grpd \hookrightarrow Span_1(Grpd)$ 
is a [[dualizable object]] in 
$Span_1(Grpd)$, and in fact is self-dual.

The [[evaluation map]] $ev_X$, hence the possible image of a symmetric monoidal functor $Bord_1 \to Span_1(Grpd)$ of a cobordism of the form

$$
  \array{ 
    && \leftarrow & \ast^-
    \\
    & \swarrow 
    \\
    \downarrow
    \\
    & \searrow 
    \\
    && \rightarrow & \ast^+
  }
$$

is given by the [[span]]

$$
  \array{
    && X
    \\
    & \swarrow && \searrow
    \\
    \ast && && [\Pi_1(S^0),X] &\simeq& X \times X
  }
$$

and the [[coevaluation map]] $coev_X$ by the reverse span.

For $X \in Grpd \hookrightarrow Span_1(Grpd)$ any object,
the [[trace]] ("[[span trace]]") of the [[identity]] on it, hence the image of 

$$
  \array{
     &&  \ast^- 
     \\
     & \swarrow & & \nwarrow
     \\
     \downarrow && && \uparrow
     \\
     & \searrow && \nearrow
     \\
     && \ast^+
  }
$$

is its 
[[free loop space object]], prop. \ref{FreeLoopSpaceOfGroupoid}:

$$
  tr(id_X) \simeq 
  \left(
    \array{
      && [\Pi_1(S^1), X]
      \\
      & \swarrow && \searrow
      \\
      \ast && && \ast
    }
  \right)
  \,.
$$


The second order covaluation map on the [[span trace]] of the identity is 

$$
  \array{
    && && \ast
    \\
    && && \uparrow
    \\
    && && X
    \\
    && && \downarrow
    \\
    && && [\Pi(S^1), X]
    \\
    && & \swarrow & & \searrow
    \\
    \ast &\leftarrow& X &\rightarrow& [\Pi(S^0), X] &\leftarrow&
    X &\rightarrow& & \ast
  }
  \,.
$$

=--


+-- {: .proof}
###### Proof

By prop. \ref{GroupoidInSpanOneIsSelfDual}
the [[trace]] of the identity is given by the composite span

$$
  \array{
    && && X \underset{[\Pi_1(S^1), X]}{\times} X
    \\
    && & \swarrow && \searrow
    \\
    && X && \swArrow && X
    \\
    & \swarrow && \searrow && \swarrow && \searrow
    \\
    \ast
    &&
    &&
    [\Pi_1(S^0),X]
    &&
    &&
    \ast
  }
  \,.
$$

By prop. \ref{FreeLoopSpaceOfGroupoid} we have

$$
  X \underset{[\Pi_1(S^1), X]}{\times} X
  \simeq [\Pi_1(S^1), X]
  \,.
$$

Along these lines one checks the required [[zig-zag identities]].

=--

##### Action functionals on spaces of trajectories: correspondences of groupoids over the space of phases
 {#1dDWLocalFieldTheory}

We have now assembled all the ingredients need in order to formally regard a [[group character]] $c \colon G \to U(1)$ on a [[discrete group]] as a local action functional of a prequantum field theory, hence as a [[fully dualizable object]]

$$
  S
  \;\coloneqq\;
  \left[
    \array{
      \mathbf{B}G
      \\
      \downarrow^{\mathrlap{c}}
      \\
      \mathbf{B}\flat U(1)
    }
  \right]
  \;\in \;
  \mathrm{Span}_1(Grpd, \mathbf{B}\flat U(1))
$$

in a [[(2,1)-category]] of correspondences of groupoids as in def. \ref{OneSpansInOneGroupoids}, but equipped with maps and homotopies between maps to the [[coefficient]] over $\mathbf{B}\flat U(1)$. This is described in def. \ref{OneSpansInOneGroupoidsOverBU} below. Before stating this, we recall for the 1-dimensional case the general story of def. \ref{LocalPrequantumFieldWithAction}.



+-- {: .num_example #HomotopyAsActionFunctional}
###### Example

Given a [[discrete groupoid]] $X$, [[functions]] 

$$
  \exp(i S) \colon X \to \flat U(1)
$$ 

are in [[natural bijection]] with [[homotopies]] of the form

$$
  \array{
    && X
    \\
    & \swarrow &&  \searrow
    \\
    \ast && \swArrow_{\phi} && \ast
    \\
    & \searrow && \swarrow
    \\
    && \mathbf{B}\flat U(1)
  }
  \,,
$$

where the function corresponding to this homotopy is that given by the unique factorization through the [[homotopy fiber product] $\flat U(1) \simeq \ast \underset{\mathbf{B}\flat U(1)}{\times} \ast$ (example \ref{LoopSpaceGroupoid}) as shown on the right of 

$$
  \array{
    && X
    \\
    & \swarrow &&  \searrow
    \\
    \ast && \swArrow_{\phi} && \ast
    \\
    & \searrow && \swarrow
    \\
    && \mathbf{B}\flat U(1)
  }
  \;\;\;\;
  \simeq
  \;\;\;\;
  \array{
    && X
    \\
    &\swarrow& \downarrow^{\mathrlap{\exp(i S)}} & \searrow
    \\
    && \flat U(1)
    \\
    \downarrow & \swarrow &&  \searrow & \downarrow
    \\
    \ast && \swArrow && \ast
    \\
    & \searrow && \swarrow
    \\
    && \mathbf{B}\flat U(1)
  }  
  \,,
$$

=--

This means that if we have an [[action functional]] on a space of [[trajectories]], and if these trajectories are given by [[spans]]/[[correspondences]] of groupoids as discussed above, then the action functional is naturally expressed as the homotopy filling a completion of the span to a square diagram over $\mathbf{B}\flat U(1)$. Therefore we cosider the following.

+-- {: .num_defn #OneSpansInOneGroupoidsOverBU}
###### Definition

Write $Span_1(Grpd, \flat\mathbf{B}U(1))$
for the [[(2,1)-category]] whose

* [[objects]] are [[groupoids]] $X$ equipped with a morpism

  $$
    \left[
      \array{
         X
         \\
         \downarrow^{\mathrlap{f}}
         \\
         \mathbf{B}\flat U(1)
      }
    \right]
  $$

* [[morphisms]] are [[spans]] $X_1 \leftarrow Y \rightarrow X_2$ equipped with a [[homotopy]] $\phi$ in 

  $$
    \array{
       && Y
       \\
       & {}^{\mathllap{f_1}}\swarrow && \searrow^{\mathrlap{f_2}}
       \\
       X_1 && \swArrow_{\phi} && X_2
       \\
       & \searrow && \swarrow
       \\
       && \mathbf{B}\flat U(1)
    }
  $$

* [[2-morphisms]] are morphism of spans compatible with the maps to $\mathbf{B}\flat U(1)$ in the evident way.

The operation of [[composition]] is as in $Span_1(Grpd)$, def. \ref{OneSpansInOneGroupoids} on the upper part of these diagrams, naturally extended to the whole diagrams by composition of the [[homotopies]] filling the squares that appear. 

=--



+-- {: .num_prop}
###### Proposition

$Span_1(Grpd, \mathbf{B}\flat U(1))$ carries the structure of a
[[symmetric monoidal (infinity,n)-category|symmetric monoidal (2,1)-category]] where the [[tensor product]] is given by

$$
  \left[
    \array{  
       X_1
       \\
       \downarrow^{\mathrlap{f_1}}
       \\
       \mathbf{B}\flat U(1)
    }
  \right]
  \otimes
  \left[
    \array{  
       X_2
       \\
       \downarrow^{\mathrlap{f_2}}
       \\
       \mathbf{B}\flat U(1)
    }
  \right]
  \;\;
  \coloneqq
  \;\;
  \left[
    \array{  
       X_1 \times X_2
       \\
       \downarrow^{\mathrlap{f_1 \circ p_1 + f_2 \circ p_2}}
       \\
       \mathbf{B}\flat U(1)
    }
  \right]
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

There is an evident [[forgetful functor|forgetful]] [[(2,1)-functor]]

$$
  Span_1(Grpd, \mathbf{B}\flat U(1))
  \to 
  Span_1(Grpd)
$$ 

which forgets the maps to $\mathbf{B}\flat U(1)$ and the homotopies between them. This is a [[monoidal (infinity,1)-functor|monoidal (2,1)-functor]].

=--

As generalization of prop. \ref{GroupoidInSpanOneIsSelfDual} we now have the following:

+-- {: .num_prop}
###### Proposition

Every object 

$$
  \left[
    \array{  
       X
       \\
       \downarrow^{\mathrlap{f}}
       \\
       \mathbf{B}\flat U(1)
    }
  \right]
  \in Span_1(Grpd,\mathbf{B}\flat U(1))
$$

is a [[dualizable object]], with dual object 

$$
  \left[
    \array{  
       X
       \\
       \downarrow^{-\mathrlap{f}}
       \\
       \mathbf{B}\flat U(1)
    }
  \right]
$$

and with [[evaluation map]] given by

$$
  \array{
    && X
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow_{\mathrlap{\simeq}} && X \times X
    \\
    & {}_{\mathllap{0}}\searrow && \swarrow_{\mathrlap{f \circ p_1 - f \circ p_2}}
    \\
    && \mathbf{B}\flat U(1)
  }
  \,.
$$


=--

In conclusion we can now compute what the 1-dimensional prequantum field theory defined by a group character $c \colon G \to U(1)$ regarded as a local action functional assigns to the [[circle]].

+-- {: .num_theorem #GroupCharacterPrequantumTheoryOnCircle}
###### Theorem

The prequantum field theory defined by a [[group character]]

  $$
    \left[
      \array{
	    \mathbf{Field}
		\\
                \downarrow^{\mathrlap{\exp(i S)}}
		\\
		\flat \mathbf{B}U(1)
	  }
	\right]
	\;\;
	\coloneqq
	\;\;
    \left[
      \array{
	    \mathbf{B}G
		\\
                \downarrow^{\mathrlap{\mathbf{B}\mathrlap{c}}}
		\\
		\flat \mathbf{B}U(1)
	  }
	\right]	
      \in Span_1(Grpd,\mathbf{B}\flat U(1))
  $$

  assigns to the [[circle]] the [[trace]] of the identity on this object, which under the identifications of example \ref{LoopSpaceGroupoid}, example \ref{GroupCharacterAsClassFunctionByFreeLoopSpace}, and example \ref{HomotopyAsActionFunctional} is the group character itself:


$$
  \array{
    && && [\Pi_1(S^1), \mathbf{B}G]
    \\
    && & \swarrow && \searrow
    \\
    && \mathbf{B}G && \swArrow && \mathbf{B}G
    \\
    & \swarrow && \searrow && \swarrow && \searrow
    \\
    \ast && && \mathbf{B}G \times \mathbf{B}G && && \ast
    \\
    &{}_0\searrow & && \downarrow^{\mathrlap{\exp(i S \circ p_1 - i S \circ p_2)}}
    &&& \swarrow_{0}
    \\
    &&&& \mathbf{B}\flat U(1)
  }
  \;\;\;
   \simeq
  \;\;\;
  \array{
    && G//G
    \\
    && \simeq
    \\
    && [\Pi(S^1), \mathbf{B}G]
    \\
    && \downarrow^{\mathrlap{c}}
    \\
    && \flat U(1)
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow && \ast
    \\
    & \searrow && \swarrow
    \\
    && \mathbf{B}\flat U(1)
  }
  \;\;\;
$$

Here the [[action functional]] on the right  sends a [[field configuration]] $g \in G = [\Pi(S^1), \mathbf{B}G]_0$
to its value $c(g) \in U(1) = (\flat \mathbf{B}U(1))_1$ under the [[group character]].

=--

In conclusion, [[1-dimensional Dijkgraaf-Witten theory]] as a prequantum field theory comes down to be essentially a geometric interpretation of what [[group characters]] are and do. One may regard this as a simple example of [[geometric representation theory]]. Simple as this example is, it contains in it the seeds of many of the interesting aspects of richer prequantum field theories. 

#### 2d Dijkgraaf-Witten theory

The [[group character]] $c : G \to U(1)$ which defines 
1-dimensional prequantum Dijkgraaf-Witten theory
in [1d Dijkgraaf-Witten theory](#1dDWTheory) is equivalently a [[cocycle]] in degree-1 [[group cohomology]]

$$
  [c] \in H_{\mathrm{Grp}}(G,U(1))
  \,.
$$

More familiar are maybe cocycles in higher degree. 
In view of the above it is plausible that one may interpret a cocycle in degree-$n$ group cohomology, for 
all $n \in \mathbb{N}$ as a higher order [[action functional]]
$\mathbf{B}G \to \flat\mathbf{B}^n U(1)$ and induce an 
$n$-dimensional local prequantum Dijkgraaf-Witten-type theory
from it. 

Here we discuss the case of $n = 2$ where a group 2-cocycle is regarded as the local action functional of a 2-dimensional Digjkgraaf-Witten field theory. We use this as occasion to introduce a bit of the theory of [[2-groups]] and their [[homotopy theory]] ([[homotopy 2-type]]-theory). Below in _[3d DW theory](#3dDWLocalPrequantumFieldTheory)_ we then turn to the fully general case of [[∞-groupoid]]-theory.

##### 2-Groupoids and basic homotopy 2-type theory

(...)

#### $n$d Dijkgraaf-Witten theory
 {#3dDWLocalPrequantumFieldTheory}


In view of the above it is plausible that one may interpret a cocycle in degree-$n$ group cohomology, for 
all $n \in \mathbb{N}$ as a higher order [[action functional]]
$\mathbf{B}G \to \flat\mathbf{B}^n U(1)$ and induce an 
$n$-dimensional local prequantum Dijkgraaf-Witten-type theory
from it. 

Here we review how to formalize this and then consider the
example of DW theory in arbitrary dimension $n$.


##### Essence of higher gauge theory: $\infty$-Groupoids and basic homotopy theory
 {#EssenceOfHigherGaugeTheoryBasicHomotopyTheory}

We briefly recall here some basic definitions and facts of [[∞-groupoids]] and their [[homotopy theory]], geared towards their use in 3-dimensional [[Dijkgraaf-Witten theory]] and generally in [[∞-Dijkgraaf-Witten theory]].


###### Higher gauge transformations: Simplicial sets and Kan complexes
 {#HeuristicsOnCompositionAndInverses}

An [[∞-groupoid]] is first of all supposed to be a structure that consists of [[k-morphisms]] for all $k \in \mathbb{N}$, which for $k \geq 1$ go between $(k-1)$-morphisms. 

In the context of [[Kan complexes]], the tool for organizing such collections of [[k-morphisms]] is the notion of a _[[simplicial set]]_, which models $k$-morphisms as being of the [[geometric shape for higher structures|shape]] of $k$-[[simplices]] -- a [[vertex]] for $k = 0$, an [[edge]] for $k = 1$, a [[triangle]] for $k = 2$, a [[tetrahedron]] for $k = 3$, and so on. 

This means that a simplicial set $K_\bullet$ is a sequence of [[sets]] $\{K_n\}_{n \in \mathbb{N}}$ (sets of $k$-simplex shaped $k$-morphisms for all $k$) equipped with [[functions]] $d_i \colon K_{k+1} \to K_{k}$ that send a $(k+1)$-simplex to its $i$-th face, and functions $s_i \colon K_k \to K_{k+1}$ that over a $k$-simplex "erects a flat $(k+1)$-simplex" in all possible ways (hence which inserts "[[identities]]" called "degeneracies" in this context).

If we write $\Delta$ for the [[category]] whose [[objects]] are abstract cellular [[simplices]] and whose morphisms are all cellular maps between these, then such a simplicial set is equivalently a [[functor]] of the form

$$
  K \colon \Delta^{op} \to Set
$$

Hence we think of this as assigning

* a set $[0] \mapsto K_0$ of [[objects]];

* a set $[1] \mapsto K_1$ of [[morphism]];

* a set $[2] \mapsto K_2$ of [[2-morphism]];

* a set $[3] \mapsto K_3$ of [[3-morphism]];

and generally

* a set $[k] \mapsto K_k$ of [[k-morphism]]s

as well as specifying

* functions $([n] \hookrightarrow [n+1]) \mapsto (K_{n+1} \to K_n)$
  that send $n+1$-morphisms to their boundary $n$-morphisms;

* functions $([n+1] \to [n]) \mapsto (K_{n} \to K_{n+1})$
  that send $n$-morphisms to [[identity]] $(n+1)$-morphisms
  on them.

The fact that $K$ is supposed to be a [[functor]] enforces that these assignments of sets and functions satisfy conditions that make consistent our interpretation of them as sets of $k$-morphisms and source and target maps between these. 
These are called the _[[simplicial identities]]_.

But apart from this source-target matching, a generic simplicial set does not yet encode a notion of [[composition]] of these morphisms. 

For instance for $\Lambda^1[2]$ the simplicial set consisting of two attached 1-cells 

$$
  \Lambda^1[2] = \left\{
    \array{
       && 1
       \\
       & \nearrow && \searrow
       \\
       0 &&&& 2
    }
  \right\}
$$

and for $(f,g) : \Lambda^1[2] \to K$ an image of this situation in $K$, hence a pair $x_0 \stackrel{f}{\to} x_1 \stackrel{g}{\to} x_2$ of two _composable_ 1-morphisms in $K$, we want to demand that there exists a third 1-morphisms in $K$ that may be thought of as the [[composition]] $x_0 \stackrel{h}{\to} x_2$ of $f$ and $g$. But since we are working in [[higher category theory]] (and not to be [[evil]]), we want to identify this composite only up to a [[2-morphism]] equivalence

$$
    \array{
       && x_1
       \\
       & {}^{\mathllap{f}}\nearrow &\Downarrow^{\mathrlap{\simeq}}& 
       \searrow^{\mathrlap{g}}
       \\
       x_0 &&\stackrel{h}{\to}&& x_2
    }
  \,.
$$

From the picture it is clear that this is equivalent to demanding that for $\Lambda^1[2] \hookrightarrow \Delta[2]$ the obvious inclusion of the two abstract composable 1-morphisms into the 2-simplex we have a diagram of morphisms of simplicial sets

$$
  \array{
    \Lambda^1[2] &\stackrel{(f,g)}{\to}& K
    \\
    \downarrow & \nearrow_{\mathrlap{\exists h}}
    \\
    \Delta[2]
  }
  \,.
$$

A simplicial set where for all such $(f,g)$ a corresponding such $h$ exists may be thought of as a collection of higher morphisms that is equipped with a notion of composition of adjacent 1-morphisms. 

For the purpose of describing [[groupoid]]al composition, we now want that this composition operation has all [[inverse]]s. For that purpose, notice that for 

$$
  \Lambda^2[2] = \left\{
    \array{
       && 1
       \\
       & && \searrow
       \\
       0 &&\to&& 2
    }
  \right\}
$$

the simplicial set consisting of two 1-morphisms that touch at their end, hence for 

$$
  (g,h) : \Lambda^2[2] \to K
$$

two such 1-morphisms in $K$, then if $g$ had an inverse $g^{-1}$ we could use the above composition operation to compose that with $h$ and thereby find a morphism $f$ connecting the sources of $h$ and $g$. This being the case is evidently equivalent to the existence of diagrams of morphisms of simplicial sets of the form

$$
  \array{
    \Lambda^2[2] &\stackrel{(g,h)}{\to}& K
    \\
    \downarrow & \nearrow_{\mathrlap{\exists f}}
    \\
    \Delta[2]
  }
  \,.
$$

Demanding that all such diagrams exist is therefore demanding that we have on 1-morphisms a composition operation with inverses in $K$. 

In order for this to qualify as an $\infty$-groupoid, this composition operation needs to satisfy an [[associativity law]] up to [[coherent]] [[2-morphisms]], which means that we can find the relevant [[tetrahedron]]s in $K$. These in turn need to be connected by _pentagonators_ and ever so on.  It is a nontrivial but true and powerful fact, that all these [[coherence]] conditions are captured by generalizing the above conditions to all dimensions as in the definition of Kan complexes.

In order to conceive of the $k$-[[simplices]] for higher $k$ as "[[globular set|globular]] [[k-morphism]]" going from a source to a target one needs a bit of combinatorics. This provided by the _[[orientals]]_ (due to [[Ross Street]]).

The $k$-[[oriental]] $O(k)$ is precisely the prescription for how exactly to think of  a $k$-[[simplex]] as being a [[k-morphism]] in an [[omega-category]]. The first few look like this:

$$
\array{\arrayopts{\rowalign{center}}
O(\Delta^0) = & \{ 0\} \\
O(\Delta^1) = & \left\{ 0 \to 1\right\} \\
O(\Delta^2) = & \left\{
\array{\begin{svg}
[[!include oriental > Delta2]]
\end{svg}}
\right\}\\
O(\Delta^3) = & \left\{
\array{\begin{svg}
[[!include oriental > Delta3]]
\end{svg}}\right\}\\
O(\Delta^4) = & \left\{
\array{\begin{svg}
[[!include oriental > Delta4]]
\end{svg}}
\right\}
}
$$

In fact, the [[omega-nerve]] $N(K)$ of an [[omega-category]] $K$ is the [[simplicial set]] whose collection of $k$-cells $N(K)_k := Hom(O(k),K)$ is precisely the collection of images of the $k$th oriental $O(k)$ in $K$.

This is fully formally the prescription of how to think of a Kan complex as an $\infty$-groupoid: the Kan complex $C$ is the [[omega-nerve]] of an [[omega-category]] in which all morphism are invertible:

* the $k$-cells in  $C_k$ are precisely the collection of $k$-morphisms ihn the omega-category of shape the $k$th [[oriental]] $O(k)$;

* the [[horn]]-filler conditions satisfied by these cells is precisely a reflection of the fact that

  1. there exists a notion of composition of adjacent k-morphisms in the [[omega-category]];

  1. under this composition all $k$-morphisms have an inverse.

This is easy to see in low dimensions: 

* a 1-cell $\phi \in C_1$ in the [[simplicial set]] $C$ has a single source 0-cell $x := d_1 \phi$ and a single target 0-cell $y := d_0 \phi$ and hence may be pictured as a [[morphism]]

  $$
    x \stackrel{\phi}{\to} y
    \,.
  $$

* a 2-cell $\phi \in C_2$ in the [[simplicial set]] $C$ has two incoming 1-cells $d_2 \phi, d_0 \phi \in C_1$ and one outgoing 1-cell $d_1 \phi \in C_1$, and if we think of the two incoming 1-cells as representing the composite of the corresponding 1-morphisms, we may picture te 2-cell $\phi$ here as a globular 2-morphism

  $$
    \array{
      && x_1
      \\
      & {}^{\mathllap{d_2 \phi}}\nearrow &\Downarrow^\phi& \searrow^{\mathrlap{d_0 \phi}}
      \\
      x_0 &&\underset{d_1 \phi}{\to}&& x_2
    }
    \,.
  $$

More in detail, one may think of the incoming two adjacent $1$-cells here as _not_ being the composite of these two morphism, but just as a [[composable pair]], and should think of the existence of the 2-morphism $\phi$ here as being a **compositor** in a [[bicategory]] that shows how the composable pair is composed to the morphism $d_1 \phi$.

So if an $\infty$-groupoid is thought of as a [[geometric shapes for higher structures|globular]] [[Batanin ∞-category| ∞-category]] in which all [[k-morphism]]s are invertible, then the corresponding Kan complex is the [[nerve]] or rather the [[∞-nerve]] of this [[∞-category]].

Notably if $C$ is to be regarded as (the nerve of) an ordinary [[groupoid]], every composable pair of morphisms has a unique composite, and hence there should be a _unique_ 2-cell

  $$
    \array{
      && x_1
      \\
      & {}^{f}\nearrow &\Downarrow& \searrow^{g}
      \\
      x_0 &&\underset{h = g \circ f}{\to}&& x_2
    }
  $$

that is the unique **identity 2-morphism**

$$
  g \circ f \stackrel{=}{\Rightarrow} h
  \,.
$$

More generally, in a [[2-groupoid]] there may be non-identity 2-morphisms, and hence for any 1-morphism $k _ x_0 \to x_2$ 2-isomorphic to $h$, there may be many 2-morphisms $g \circ f \Rightarrow k$, hence many 2-cells

$$
  \array{
    && x_1
    \\
    & {}^{f}\nearrow &\Downarrow^{\simeq}& \searrow^{g}
    \\
    x_0 &&\underset{k }{\to}&& x_2
  }
  \,.
$$

All we can say for sure is that _at least_ one such 2-cell exists, and that the 2-cells themselves may be composed in some way. This is precisely what the horn-filler conditions in a Kan complex encode.

We have already seen in low dimension how the existence of composites in an $\omega$-category is reflected in the fact that in a Kan-complex certain 2-simplices exist, and how the non-uniqueness of these 2-simplices reflects the existence of nontrivial 2-morphisms.

To see in a similar fashion that the Kan condition ensures the existence of _inverses_ consider an _outer horn_ in $C$, a diagram of 1-cells of the form

$$
  \array{
    && x_1
    \\
    & {}^{\mathllap{f}}\nearrow
    \\
    x_0 &&\underset{h}{\to}&& x_2
  }
  \,.
$$

In general given such a diagram in a [[category]], there is no guarantee that the corresponding triangle as above will exist in its [[nerve]]. But if the category is a [[groupoid]], then it is guaranteed that the missing 1-face can be chose to be the [[inverse]] of $f$ composed with the morphism $h$, and there is at least one 2-morphism

$$
  \array{
    && x_1
    \\
    & {}^{\mathllap{f}}\nearrow
    &\Downarrow^{\simeq}& \searrow^{\mathrlap{h \circ f^{-1}}}
    \\
    x_0 &&\underset{h}{\to}&& x_2
  }
  \,.
$$

A similar analysis for higher dimensional cells shows that the fact that a Kan complex has all horn fillers encodes precisely the fact that it is the [[omega-nerve]] of an [[omega-category]] in which _all_ [[k-morphism]]s for all $k$ are composable if adjacent and have a weak inverse.


###### 1-Groupoids as Kan complexes
 {#1GroupoidsAsKanComplexes}

We review how [[1-groupoids]] are incarnated as Kan complexes via their [[nerve]].

+-- {: .num_defn #Groupoid}
###### Definition

A ([[small category|small]]) _[[groupoid]]_ $\mathcal{G}_\bullet$ is

* a pair of [[sets]] $\mathcal{G}_0 \in Set $ (the set of [[objects]]) and $\mathcal{G}_1 \in Set$ (the set of [[morphisms]])

* equipped with [[functions]]

  $$
    \array{
      \mathcal{G}_1 \times_{\mathcal{G}_0} \mathcal{G}_1
      &\stackrel{\circ}{\to}&
      \mathcal{G}_1
      & \stackrel{\overset{t}{\to}}{\stackrel{\overset{i}{\leftarrow}}{\underset{s}{\to}}}&
      \mathcal{G}_0
    }\,,
  $$

  where the [[fiber product]] on the left is that over $\mathcal{G}_1 \stackrel{t}{\to} \mathcal{G}_0 \stackrel{s}{\leftarrow} \mathcal{G}_1$, 

such that

* $i$ takes values in [[endomorphisms]];

  $$
    t \circ i = s \circ i =   id_{\mathcal{G}_0}, \;\;\; 
  $$

* $\circ$ defines a partial [[composition]] operation which is [[associativity|associative]] and [[unitality|unital]] for $i(\mathcal{G}_0)$ the [[identities]]; in particular

  $s (g \circ f) = s(f)$ and $t (g \circ f) = t(g)$;

* every morphism has an [[inverse]] under this composition.

=--


+-- {: .num_defn #NerveOfGroupoid}
###### Definition

For $\mathcal{G}_\bullet$ a [[groupoid]], def. \ref{Groupoid}, we write

$$
  \mathcal{G}_n \coloneqq \mathcal{G}_1^{\times_{\mathcal{G}_0}^n}
$$ 

for the set of sequences of composable morphisms of length $n$, for $n \in \mathbb{N}$; schematically:

$$
  \mathcal{G}_n = 
  \left\{
    x_0 
      \stackrel{f_1}{\to} 
    x_1
      \stackrel{f_2}{\to}
    x_2
      \stackrel{f_2}{\to}
    \cdots
      \stackrel{f_n}{\to}
    x_n
  \right\}
  \,.
$$

For each $n \geq 1$, the two maps $d_0$ and $d_n$ that forget the first and the last morphism in such a sequence and the $n-1$ maps $d_k$ that form the composition of the $k$th morphism in the sequence with the next one, constitute $(n+1)$ [[functions]] denoted

$$
  d_k \colon \mathcal{G}_n \to \mathcal{G}_{n-1}
  \,.
$$

Moreover, the assignments $s_i$ that insert an [[identity]] morphism in position $i$ constitute [[functions]] denoted

$$
  s_i \colon \mathcal{G}_{n-1} \to \mathcal{G}_n
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

These collections of maps in def. \ref{NerveOfGroupoid} satisfy the [[simplicial identities]], hence make the [[nerve]] $\mathcal{G}_\bullet$ into a [[simplicial set]]. Moreover, this simplicial set is a Kan complex, where each [[horn]] has a _unique_ filler (extension to a [[simplex]]).

=--

(A 2-[[simplicial coskeleton|coskeletal]] Kan complex.)


+-- {: .num_prop }
###### Proposition

The [[nerve]] operation constitutes a [[full and faithful functor]]

$$
  N \colon Grpd \to KanCplx \hookrightarrow sSet
  \,.
$$


=--


###### Homotopy theory of $\infty$-groupoids as Kan complexes
 {#HomotopyTheoryOfKanComplexes}


+-- {: .num_defn }
###### Definition

Write 

$$
  KanCplx \hookrightarrow sSet
$$

for the [[category]] of Kan complexes, which is the [[full subcategory]] of that of [[simplicial sets]] on the Kan complexes.

=--

+-- {: .num_remark }
###### Remark

This means that for $X_\bullet,Y_\bullet \in KanCplx$ two Kan complexes, an element $f_\bullet \colon X_\bullet \to Y_\bullet$ in the [[hom-set]] $Hom_{KanCplx}(X_\bullet,Y_\bullet)$ is 

* a sequences of [[functions]] $f_n \colon X_n \to Y_n$ for all $n \in \mathbb{N}$;

such that

* these respect all the face maps $d_k$ and the degeneracy maps $s_k$.

=--


+-- {: .num_defn #MappingObjectOfKanComplexes}
###### Definition

For $X_\bullet,Y_\bullet \in KanCplx$ two Kan complexes, their [[mapping space]]

$$
  Maps(X_\bullet,Y_\bullet)_\bullet \in KanCplx
$$

is the [[simplicial set]] given by 

$$
  Maps(X_\bullet,Y_\bullet) \colon [k] \mapsto Hom_{sSet}(X_\bullet \times \Delta^n_\bullet, Y_\bullet)
  \,.
$$

=--


+-- {: .num_prop }
###### Proposition

The construction in def. \ref{MappingObjectOfKanComplexes} defines an [[internal hom]] of Kan complexes. 

=--

+-- {: .num_remark }
###### Remark

As such it is also common to write $Y^X$ for $Maps(X,Y)$, as well as $[X,Y]$. Notice that the latter notation is sometimes used instead for just the set of [[connected components]] of $Maps(X,Y)$.

=--

It follows that the category $KanCplx$ is naturally [[enriched category|enriched]] over itself. 

We now have the following immediate generalizations of the corresponding constructions seen above for 1-groupoids.

+-- {: .num_example #PathSpaceObjectOfKanComplexes}
###### Example

Write 

$$
  I_\bullet \coloneqq \{0 \stackrel{\simeq}{\to} 1\}
$$

for the Kan complex which is [[1-groupoid]] with two objects and one nontrivial morphism and its inverse between them. This comes with two inclusions

$$
  i_0, i_1 \colon \ast \to I
$$

of its endpoints.

Then for $X_\bullet \in KanCplx$ any other Kan complex, the [[mapping space]] $[I,X]_\bullet$ from def. \ref{MappingObjectOfKanComplexes} is the [[path space object]] of $X_\bullet$. 

$$
  X_\bullet \stackrel{[i_0,X_\bullet]}{\leftarrow} [I_\bullet,X_\bullet]_\bullet \stackrel{[i_1,X]}{\to} X_\bullet
  \,.
$$

=--

A 1-cell in the mapping Kan complex $[X_\bullet, Y_\bullet]_\bullet$ is a [[homotopy]] between two morphisms of Kan complexes:

+-- {: .num_defn }
###### Definition

For $f_\bullet, g_\bullet \colon X_\bullet \to Y_\bullet$ two morphisms between two Kan complexes, hence $f_\bullet,g_\bullet \in Hom_{KanCplx}(X,Y)$, a (right-)[[homotopy]] $\eta \colon f \Rightarrow g$ is a morphism $\eta_\bullet \colon X_\bullet \to [I_\bullet,X_\bullet]_\bullet$ into the [[path space object]] of def. \ref{PathSpaceObjectOfKanComplexes} such that we have a [[commuting diagram]]

$$
  \array{
    && Y_\bullet
    \\
    & {}^{\mathllap{f_\bullet}}\nearrow & \uparrow^{\mathrlap{[i_0, X_\bullet]_\bullet}}
    \\
    X_\bullet &\stackrel{\eta_\bullet}{\to}& [I_\bullet, Y_\bullet]   
    \\
    & {}_{\mathllap{g_\bullet}}\searrow & \downarrow_{\mathrlap{[i_1, X_\bullet]_\bullet}}
    \\
    &&  Y \bullet
  }
  \,.
$$

=--


+-- {: .num_remark }
###### Remark

Hence a [[homotopy]] between two maps $X_\bullet \to Y_\bullet$ of Kan complexes is precisely a 1-cell in the [[mapping space]] $[X_\bullet, Y_\bullet]_\bullet$ of def. \ref{MappingObjectOfKanComplexes}.

=--

+-- {: .num_defn #HomotopyEquivalenceOfKanComplexes}
###### Definition

We say that a map $X_\bullet \to Y_\bullet$ of [[Kan complexes]] is a _[[homotopy equivalence]]_ if it has a left and right [[inverse]] up to [[homotopy]], hence an ordinary inverse in $\pi_0[X_\bullet, Y_\bullet]$.

=--

+-- {: .num_example }
###### Example

For Kan complexes which are [[1-groupoids]] hence which are [[nerves]] of [[groupoids]], homotopy equivalence of Kan complexes is equivalently homotopy equivalence of these groupoids according 
to def. \ref{HomotopyEquivalenceOfGroupoids}.

=--


+-- {: .num_defn #KanComplexesAsHomotopyTypes}
###### Definition


We may write [[∞Grpd]] for $KanCplx$ regarded as a $KanCplx$-[[enriched category]], hence as fibrant [[sSet-enriched category]]. 

We write $X$ (without the subscript) for a Kan complex $X_\bullet$ regarded as an object of $\infty Grpd$. As such, $X$ (or its [[equivalence class]]) is alse called a _[[homotopy type]]_.

The category [[∞Grpd]] itself "is" the canonical [[homotopy theory]]. (For more on this see also at _[[homotopy hypothesis]]_.)

=--

The following is the immediate generalization of def. \ref{HomotopyFiberProductOfGroupoids}.

+-- {: .num_defn #HomotopyFiberProductOfKanComplexes}
###### Definition

Given two morphisms of [[Kan complexes]]
$X \stackrel{f}{\leftarrow} B \stackrel{g}{\to} Y$
their _[[homotopy fiber product]]_

$$
  \array{
   X \underset{B}{\times} Y
   &\stackrel{}{\to}& X
   \\
   \downarrow &\swArrow& \downarrow^{\mathrlap{f}}
   \\
   Y &\underset{g}{\to}& B
  }
$$

is the [[limit]] [[cone]]

$$
  \array{
    X_\bullet \underset{B_\bullet}{\times} B^I_\bullet
    \underset{B_\bullet}{\times} Y_\bullet
    &\to& &\to& X_\bullet
    \\
    \downarrow && && \downarrow^{\mathrlap{f_\bullet}}
    \\
    && B^I_\bullet &\underset{(ev_0)_\bullet}{\to}& B_\bullet
    \\
    \downarrow && \downarrow^{\mathrlap{(ev_1)_\bullet}}
    \\
    Y_\bullet &\underset{g_\bullet}{\to}& B_\bullet
  }
  \,,
$$

hence the ordinary iterated [[fiber product]] over the [[path space]] Kan complex, as indicated.

=--


###### Higher phases: Homological algebra and abelian $\infty$-groups
 {#DoldKanCorrespondenceInPrequantumFieldTheory}

An important class of examples of [[∞-groupoids]] are those which are presented under the [[Dold-Kan correspondence]] by [[chain complexes]] of abelian groups.

[[Dold-Kan correspondence]]

+-- {: .num_defn }
###### Definition

Write $Ch_{\bullet \geq 0}$ for the [[category of chain complexes]] (of [[abelian groups]] in non-negative degree). 

As usual, for $A \in $ [[Ab]] an [[abelian group]], we write $A[n]$ for the [[chain complex]] with $A$ in degree $n$ and 0 in all other degrees (the _[[suspension of a chain complex]]_).

=--

+-- {: .num_defn }
###### Definition

Write [[sAb]] for the category of [[simplicial abelian groups]], hence [[simplicial objects]] in [[abelian groups]]. Finally write

$$
  N 
    \;\colon\;
  sAb
  \to 
  Ch_\bullet
$$

for the [[normalized chain complex]]-functor, which sends a simplicial abelian group $A_\bullet$ to the chain complex whose $n$-[[chains]] are the non-degenerate elements of $A_n$ and whose [[differential]] is the alternating sum of the face maps of $A_\bullet$:

$$
  d^{N(A)} = \sum_{i = 0}^n (-1)^i d^A_i
  \,.
$$

=--

Of relevance now are the following two standard facts.

+-- {: .num_prop #DoldKanAndMooreTheorem}
###### Proposition

1. [[Dold-Kan correspondence|Dold-Kan]]: The functor $N \colon Ch_{\bullet \geq 0} \to sAb$ is an [[equivalence of categories]]. The inverse functor

   $$
     \Xi \colon Ch_{\bullet \geq 0} \stackrel{\simeq}{\to} sAb
   $$

   sends a chain complex to the simplicial abelian group whose $n$-simplices are the images of the [[normalized chain complex]] $N(\mathbb{Z}(\Delta^n))$ of chains $\mathbb{Z}(\Delta^n)$ the $n$-[[simplex]].

1. [Moore](simplicial+group#MooreTheorem): The [[forgetful functor]] $sAb \to sSet$ which sends a simplicial abelian group to its underlying simplicial set factors through Kan complexes

   $$
     forget \; \colon \; sAb \to KanCplx \hookrightarrow sSet
     \,.
   $$

=--

Taken together, this provides us with the following very useful construction.

+-- {: .num_defn #DoldKanMap}
###### Definition

We write

$$
  DK \;\colon\; 
  Ch_{\bullet \geq 0} 
  \underoverset{\simeq}{\Xi}{\to}
  sAb
  \stackrel{forget}{\to}
  KanCplx
  \hookrightarrow
  sSet
$$

for the composite of the two functors of prop. \ref{DoldKanAndMooreTheorem}. 

=--

We refer to this as the "Dold-Kan map", or say "by Dold-Kan", etc. It provides us with a rich supply of Kan complexes, hence of [[∞-groups]]. In fact, it embeds [[homological algebra]] into the [[homotopy theory]] of [[∞-groupoids]] in that it is a [[homotopical functor]]:

+-- {: .num_prop #DoldKanRespectsWeakEquivalences}
###### Proposition

The Dold-Kan map of def. \ref{DoldKanMap} sends [[quasi-isomorphisms]] of [[chain complexes]] to [[homotopy equivalences]] of [[Kan complexes]], def. \ref{HomotopyEquivalenceOfKanComplexes}.

=-- 

Notably we have the following example


+-- {: .num_defn }
###### Definition

For $n \in \mathbb{N}$ write

$$
  \mathbf{B}^n \flat U(1) \coloneqq DK(\flat U(1)[n])
  \in KanCplx
$$

for the $n$-fold [[suspension of a chain complex|suspension]] of the [[discrete group|discrete]] [[circle group]], regarded by Dold-Kan as the $n$-fold [[delooping]] Kan complex of $\flat U(1)$.

=--

+-- {: .num_example }
###### Example

Since the first [[simplex]] that contains a non-degenerate $n$-cell is $\Delta^n$, it follows that $\mathbf{B}^n\flat U(1)$ is trivial in degrees $\lt n$

$$
  (\mathbf{B}^n \flat U(1))_{k \lt n} = \ast
  \,.
$$

Then since there is a unique non-degenerate $n$-cell in $\Delta^n$ we next have

$$
  (\mathbf{B}^n \flat U(1))_{n} = \flat U(1)
  \,.
$$

Next there are $(n+2)$ non-degenrate $n$-simplices in $\Delta^{n+1}$, but known $n+1$ of their images in $\flat U(1)$ determines the last one (as their oriented product), hence next 

$$
  (\mathbf{B}^n \flat U(1))_{n+1} = (\flat U(1))^{\times^{n+1}}
  \,.
$$

Similarly for arbitary $k$ the set $(\mathbf{B}^n \flat U(1))_k$ is some [[Cartesian product|Cartesian power]] of $\flat U(1)$.
But cince here we are mostly interested in $\mathbf{B}^n \flat U(1)$ as an [[n-groupoid]], hence only for mapping $n$-groupoids into it, it is mostly enough to just know its cells up to degree $(n+1)$.

=--


Below in _[Higher Chern-Simons theory](#HigherChern-SimonsLocalPrequantumFieldTheory)_ the _smooth_ version of the [[circle group]] plays a role. In order to amplify that here we are just dealing with the [[discrete group]] underlying $U(1)$, we write

$$
  \flat U(1) \coloneqq U(1)_{disc}
$$

for it. 

$$
  \mathbf{B}^n \flat U(1) \coloneqq DK([U(1)_{disc}[n]])
  \,.
$$

+-- {: .num_prop }
###### Proposition

By the [[Dold-Kan correspondence]] each $\mathbf{B}^n \flat U(1)$ is
naturally an [[∞-group]] and its [[delooping]] is indeed $\mathbf{B}^{n+1}\flat U(1)$

$$
  \Omega \mathbf{B}^{n+1} \flat U(1) \simeq \mathbf{B}^n \flat U(1)
  \,.
$$

=--



##### Local DW action functionals: Higher group cohomology


+-- {: .num_prop #GroupCohomologyByHomotopyClassesOfMaps}
###### Proposition

For $G$ a [[discrete group]] and $A$ a discrete [[abelian group]], there is a natural isomorphism

$$
  H_{Grp}^n(G,A) \simeq \pi_0 Grpd_\infty(\mathbf{B}G, \mathbf{B}^n A)
$$

between the degree-$n$ [[group cohomology]] of $G$ with [[coefficients]] in $A$ and the connected components of maps of [[∞-groupoids]] from the [[delooping]] of $G$ to the $n$-fold [[delooping]] of $A$. 

=--


This means that local action functionals for higher Dijkgraaf-Witten type theories, hence maps of $\infty$-groupoids of the form 
$\exp(i S_{DW}^n) \colon \mathbf{B} \flat G \to \mathbf{B}^n \flat U(1)$ are equivalently [[cocycles]] $[c] \in H^n_{Grp}(\flat G,\flat U(1))$ in degree-$n$ [[group cohomology]]:

$$
  \exp(i S_{DW}^n) = \mathbf{B}c
  \,.
$$

In particular the original 3d [[Dijkgraaf-Witten theory]] appears this way as the theory of a group 3-cocycle.

(...)


### Higher Chern-Simons local prequantum field theory
 {#HigherChern-SimonsLocalPrequantumFieldTheory}

By def. \ref{LocalPrequantumFieldWithAction}, a local prequantum [[bulk]] field theory in dimension $(n+1)$ is equivalently a morphism of the form 

$$
  \exp(i S) \colon \mathbf{Fields} \to \flat \mathbf{B}^{n+1}U(1)
  \,,
$$

for any object $\mathbf{Fields} \in \mathbf{H}$. 

First we now observe in 

* _[Universal topological Yang-Mills theory](#TopologicalYangMillsLocalPrequantumFieldTheory)_

that there is a fairly canonical such morphism $S^{n+1}_{tYM}$, namely the "[[atlas]] relative to [[manifolds]]" of $\flat \mathbf{B}^{n+1}U(1)$ given by the [[sheaf]] of [[differential forms|closed differential (n+1)-forms]]. Analyzing what this morphism is like, when regarded as a local prequantum field theory by def. \ref{LocalPrequantumFieldWithAction}, shows that it is the "universal" higher [[topological Yang-Mills theory|topological Yang-Mills]] prequantum field theory. What this means becomes clear when we analyze the possible [[boundary field theories]] of this theory. 

* _[Universal boundary condition for $S_{tYM}$:  Differential cohomology and Cheeger-Simons field theory
](#UniversalStYMBoundaryAndDifferentialCohomology)_

* [General boundary conditions: Higher Chern-Weil theory and $\infty$-Chern-Simons theory](#GenralBoundaryForStYMAndHigherChernSimons) 

where we discuss how the boundary theories for $S^{n+1}_{tYM}$ are precisely the prequantum field theories of higher [[Chern-Simons theory]]-type, the _[[schreiber:∞-Chern-Simons theories]]_. These include ordinary 3d [[Chern-Simons theory]], [[higher dimensional Chern-Simons theory]] on ordinary [[gauge fields]] but also higher Chern-Simons theory on [[higher gauge fields]] such as the [[String 2-group]] [[7-dimensional Chern-Simons theory]], the [[AKSZ sigma-models]], and also [[closed string field theory]].

This shows how $\infty$-Chern-Simons theories arise canonically as precisely the local [[boundary field theories]] of the canonical local field theory which exists in any [[differential cohesion|differential]] [[cohesion|cohesive]] [[(∞,1)-topos]].

Continuing in this vein we can then work out what all the further higher [[codimension]] [[boundary field theories]] and [[defect field theories]] of this universal higher [[topological Yang-Mills theory]] and hence of [[schreiber:∞-Chern-Simons theories]] are. We find

* _[Topological Chern-Simons boundaries]()_

which are given by generalized "[[Bohr-Sommerfeld leaf|Bohr-Sommerfeld]] [[isotropic subspaces]]" of the [[moduli stacks]] of $\infty$-Chern-Simons fields.

Then...

(...)


#### $d = n + 1$, Universal topological Yang-Mills theory $S_{tYM}$
 {#TopologicalYangMillsLocalPrequantumFieldTheory}

There is a special and especially simple map to the [[coefficient]] object  $\flat \mathbf{B}^{n+1} U(1)$ for flat [[local action functionals]]/[[prequantum n-bundles]], namely the map

$$
  \array{
    \Omega^{n+1}_{cl} 
    \\
    \downarrow^{\mathrlap{\exp(i S_{tYM})}}
    \\
    \mathbf{B}^{n+1} \flat U(1)
  }
$$

which in components is the inclusion of closed [[differential forms]] into [[de Rham cohomology|de Rham]] [[hypercohomology]] cocoycles. 

We here introduce and describe this map and then regard it as a [[local action functional]] of a local prequantum field theory according to def. \ref{LocalPrequantumFieldWithAction}. Below in _[Higher Chern-Simons prequantum field theory](#HigherChernSimonsPrequantumFieldTheory)_ we find that this field theory is such that close to its boundaries it looks like (higher) [[topological Yang-Mills theory]] for every possible higher gauge group and every possible [[invariant polynomial]] on it, as one considers every possible [[boundary condition]]. Therefore we here refer to this as the "universal topological Yang-Mills theory".

##### Smooth moduli stacks of fields: Smooth $\infty$-groupoids

The notion of a [[sheaf]] of [[chain complexes]] or equivalently of a chain complex of sheaves over a fixed [[topological space]] has a long tradition in [[homological algebra]]. Many sheaves however are naturally considered not on one fixed space, but on "all of them". For instance [[differential forms]] in any degree may be "[[pullback of a differential form|pulled back]]" along any [[smooth function]] between [[smooth manifolds]]. Accordingly if we regard the whole category [[SmoothMfd]] of smooth manifolds as a replacement for and generalization of the [[category of open subsets]] of any given one, then differential forms constitute a sheaf on that [[site]], hence a functor

$$
  \Omega^{n} \colon SmoothMfd^{op} \to Set
  \,.
$$

In particular for $n = 0$ this is just the sheaf of smooth functions

$$  
  \underline{\mathbb{R}} = C^\infty(-,\mathbb{R}) \colon SmoothMfd^{op} \to Set
  \,.
$$

One way to think of this is that this sheaf _is_ the [[real line]] $\mathbb{R}$ first of all as a [[set]] -- which is the value of $\underline{\mathbb{R}}$ on the [[point]] $\ast$ -- and secondly equipped with its canonical [[smooth structure]] which is encoded by the system of _all_ sets $C^\infty(X,\mathbb{R})$ of smooth functions from any smooth manifold $X$, and the information $C^\infty(\phi, \mathbb{R}) \colon C^\infty(Y, \mathbb{R}) \to C^\infty(X,\mathbb{R})$ of how these functions pull back (precompose) along any smooth function of test manifolds $\phi \colon X \to Y$.

Regarding the [[smooth manifold]] $\mathbb{R}$ this way means regarding it as what is sometimes called a [[diffeological space]], and what here more generally call a _[[smooth space]]_.

Therefore we will often just write $\mathbb{R}$ when we really mean the sheaf $\underline{\mathbb{R}}$ [[representable functor|represented]] by it.

The [[Dold-Kan correspondence|Dold-Kan map]] of def.  \ref{DoldKanMap} directly extends to ([[presheaf|pre]]-)[[sheaves]] which regard a (pre-)sheaf of chain complexes as a presheaf of [[Kan complexes]]

$$
  DK
  \;\colon\;
  pSh(SmoothMfd, Ch_\bullet)
  \stackrel{}{\to}
  pSh(SmoothMfd, KanCplx)
  \hookrightarrow
  pSh(SmoothMfd, sSet)
  \,.
$$

By the previous reasoning, a presheaf of Kan complexes on the category of smooth manifolds, we may think of as being a plain Kan complex, hence [[∞-groupoid]] (the value of the presheaf on the point), together with a rule for what the smooth functions into it are, for each smooth testmanifold. Hence we think of it as a _[[smooth ∞-groupoid]]_. 

A basic example is a [[Lie groupoid]] $\mathcal{G}_\bullet \in Grpd(SmoothMfd)$, which represents a presheaf of Kan complexes on smooth manifolds by

$$
  U \mapsto N( C^\infty(U,\mathcal{G}_1) \stackrel{\to}{\to} C^\infty(U,\mathcal{G}_0) )
  \,.
$$


Previously we have considered higher Dijkgraaf-Witten as taking place in the [[homotopy theory]] of plain [[∞-groupoids]] (geometrically [[discrete ∞-groupoids]]). Now we would like to have "a [[homotopy theory]] of [[smooth ∞-groupoids]]".

(A modern term for "a [[homotopy theory]]" is "an [[(∞,1)-category]]", but for a heuristic idea of what is going on some readers may find it helpful to think of "a homotopy theory" instead.)

In order to define "a [[homotopy theory]]" of [[smooth ∞-groupoids]] is, to be denoted [[Smooth∞Grpd]], we need to say what a [[homotopy]] and hence what a [[homotopy equivalence]] is supposed to be. Since [[smooth structure]] should be a local property witnessed on small smooth [[open balls]], we declare that

$$
  Smooth\infty Grpd
  \coloneqq
  L_{lhe} \; pSh(SmoothMfd, KanCplx)
$$

is the [[homotopy theory]] obtained by "universally turning [[stalk]]-wise [[homotopy equivalences]] of [[Kan complexes]], def. \ref{spring}, into actual homotopy equivalences". The formal definition of this idea is called the _[[simplicial localization]]_ of $pSh(SmoothMfd, KanCplx)$ at the stalkwise homotopy equivalences.

We call [[∞Grpd]] also the _[[differential cohesion|differential]] [[cohesive]] [[∞-topos]] of [[smooth ∞-groupoids]]_. For brevity and since most everything we discuss in the following holds for arbitrary _[[differential cohesion|differential]] [[cohesive]] [[(∞,1)-toposes]], we from now on denote it by

$$
  \mathbf{H} \coloneqq Smooth \infty Grpd
  \,.
$$

We now immediately turn to a simple example that illustrates some basic aspects of this construction. 


##### The canonical local action functional: Differential forms in de Rham hypercohomology

As a first example for how to work in the homotopy theory of [[smooth ∞-groupoids]] we have the following.

+-- {: .num_prop }
###### Proposition/Example

The canonical [[chain map]]

$$
  \array{  
    \flat U(1) &\to& 0 &\to& 0 &\to& \cdots &\to& 0
    \\
    \downarrow && \downarrow && \downarrow && \cdots && \downarrow
    \\
    C^\infty(-,U(1)) &\stackrel{d log}{\to}& \Omega^1 &\stackrel{d}{\to}& \Omega^2 &\stackrel{d}{\to}& \cdots &\to& \Omega^n_{cl}
  }
  \,,
$$

where the left map includes the sheaf of (locally) constant $U(1)$-valued functions into that of all $U(1)$-valued smooth functions, is a [[stalk]]-wise [[quasi-isomorphism]]. Hence under the [[Dold-Kan correspondence]], def. \ref{DoldKanMap}, both present the same [[smooth ∞-groupoid]]

$$
  \flat \mathbf{B}^n U(1) \simeq \mathbf{B}^n \flat U(1)
  \in Smooth\infty Grpd
  \,.
$$

=--

+-- {: .proof}
###### Proof

By definition and using prop. \ref{DoldKanRespectsWeakEquivalences} we need to check that over a small enough smooth open ball, the [[chain map]] becomes a [[quasi-isomorphism]]. But on an open ball this is the statement of the [[Poincaré lemma]].

=--

Accordingly we have a canonical inclusion:

+-- {: .num_defn #ClosedFormsInDeRhamCoefficients}
###### Definition

For $n \in \mathbb{N}$, write

$$
  \Omega^{n}_{cl} \in SmoothSpace \hookrightarrow Smooth \infty Grpd
$$

for the [[sheaf]] of closed smooth [[differential forms]] of degree $n$, regarded as a [[smooth space]], regarded as a [[smooth ∞-groupoid]]. Write

$$
  \Omega^{n}_{cl} \to \flat \mathbf{B}^n U(1)
$$

for the image in morphisms of [[Smooth∞Grpd]] under the [[Dold-Kan correspondence]], def. \ref{DoldKanMap}, of the [[chain map]]

$$
  \array{  
    0 &\to& 0 &\to& 0 &\to& \cdots &\to& \Omega^{n}_{cl}
    \\
    \downarrow && \downarrow && \downarrow && \cdots && \downarrow^{\mathrlap{id}}
    \\
    C^\infty(-,U(1)) &\stackrel{d log}{\to}& \Omega^1 &\stackrel{d}{\to}& \Omega^2 &\stackrel{d}{\to}& \cdots &\to& \Omega^n_{cl}
  }
  \,,
$$

=--

+-- {: .num_remark }
###### Remark

The map $\Omega^n_{cl} \to \flat \mathbf{B}^n U(1)$ in def. \ref{ClosedFormsInDeRhamCoefficients} may be characterized more abstractly as follows:

for every [[smooth manifold]] $\Sigma$, theinduced morphism of [[mapping spaces]]

$$
  [\Sigma, \Omega^n_{cl}] \to [\Sigma, \flat \mathbf{B}^n U(1)]
$$

is a [[1-epimorphism]], hence a [[stalk]]-wise [[epimorphism]] on [[connected components]].

=--

+-- {: .num_defn #GeneralHighertYM}
###### Definition

By def. \ref{LocalPrequantumFieldWithAction} we may now regard the map

$$
  \array{
    \Omega^{n+1}_{cl}
    \\
    \downarrow^{\mathrlap{\exp(i S_{tYM})}}
    \\
    \mathbf{B}^{n+1} \flat U(1)
  }
$$

of prop. \ref{ClosedFormsInDeRhamCoefficients} as a local action functional for an $(n+1)$-dimensional local prequantum field theory.
We call this the "universal higher [[topological Yang-Mills theory]]" for reasons that become clear as we anaylize its [[boundary field theories]] now.

=--

#### $d = n + 0$, Higher Chern-Simons field theories
 {#HigherChernSimonsPrequantumFieldTheory}

We consider now the [[boundary field theories]] for the "universal topological Yang-Mills theory" of def. \ref{GeneralHighertYM}.


##### Universal boundary condition for $S_{tYM}$:  Differential cohomology and Cheeger-Simons field theory
 {#UniversalStYMBoundaryAndDifferentialCohomology}


Where the plain [[(∞,n)-category of cobordisms]] $Bord_n$ is freely generated from the point $\ast$ alone, so the $(\infty,n)$-category of cobordisms with possibly a marked boundary is freely generated from the point and one new morphism

$$
  \emptyset \to \ast
$$


which we think of as being the interval $D^1$ with one end "marked". Now a local field theory with local action functional according to def. \ref{LocalPrequantumFieldWithAction} encodes not only the value on the point, which we now take to be

$$
  \exp(i S)
  \colon
  \ast 
  \mapsto
  \left[
  \array{
    \Omega^{n+1}_{cl}
    \\
    \downarrow^{\mathrlap{\exp(i S_{tYM})}}
    \\
    \mathbf{B}^{n+1} \flat U(1)
  }
  \right]
  \,,
$$

but moreover one morphism in $Span_n(\mathbf{H}, \mathbf{B}^{n+1}\flat U(1))$ from the trivial field configuration with trivial action to this data, hence (as amplified in [FV](#FiorenzaValentino)) a diagram in $\mathbf{H}$ of the form

$$
  \array{
     && \mathbf{Fields}^{\partial}
     \\
     & \swarrow && \searrow
     \\
    \ast && \swArrow && \Omega^{n+1}_{cl}
    \\
    & \searrow && \swarrow
    \\
    && \mathbf{B}^{n+1}\flat U(1)
  }
  \,.
$$

Therefore defining such boundary data means defining a [[moduli stack]] $\mathbf{Fields}^{\partial}$ of boundary field configurations, together with a [[homotopy]] filling the above diagram which encodes the relative action functional on this boundary data.

In order to find all possible such boundary data for $\exp(i S_{tYM})$, we can make use of the [[homotopy fiber product]] construction of def. \ref{HomotopyFiberProductOfKanComplexes} to find the _universal_ such boundary data, the one through which any other one factors.


+-- {: .num_prop #DiffCohomologyIsTerminalBoundaryForStYM}
###### Proposition

The universal boudnary condition for $\exp(i S_{tYM})$, hence the [[homotopy fiber product]] $\ast \underset{\mathbf{B}^{n+1}\flat U(1)}{\times} \Omega^{n+1}_{cl}$, is given by the image under the [[Dold-Kan correspondence|Dold-Kan map]], def. \ref{DoldKanMap}, of the [[Deligne complex]]

$$
  \mathbf{B}^n U(1)_{conn}
  \coloneqq
  DK(
  \underline{U}(1) \stackrel{d log}{\to} \Omega^1 \stackrel{d}{\to} \cdots \to \Omega^{n-1} \stackrel{d}{\to} \Omega^n
  )
  \,,
$$ 

hence the universal boundary data is

$$
  \array{
     && \mathbf{B}^n U(1)_{conn}
     \\
     & \swarrow && \searrow^{\mathrlap{F_{(-)}}}
     \\
    \ast && \swArrow && \Omega^{n+1}_{cl}
    \\
    & \searrow && \swarrow
    \\
    && \mathbf{B}^{n+1}\flat U(1)
  }
  \,.
$$

=--


The [[boundary field theory]] defined this way we may call _[[Cheeger-Simons differential character|Cheeger-Simons field theory]]_.



##### General boundary condition for $S_{tYM}$: Higher Chern-Weil theory and $\infty$-Chern-Simons theory
 {#GenralBoundaryForStYMAndHigherChernSimons}


By the [[universal property]] of the [[homotopy fiber product]] we then have the following statement.

+-- {: .num_prop #HigherCSAsBoundaryTheory}
###### Proposition

Boundary field theories for $\exp(i S_{tYM})$ are equivalently 
[[moduli stacks]] $\mathbf{Fields} \in \mathbf{H}$ equipped with maps

$$
  \exp(i S_{CS}) 
    \colon
  \mathbf{Fields} \to \mathbf{B}^n U(1)_{conn}
$$

hence equipped with a [[circle n-bundle with connection]] (the [[prequantum n-bundle]] of the boundary theory).

=--

Moreover, the universal property of the [[Cheeger-Simons differential character|Cheeger-Simons]] field theory identifies all these boundary theories as being of higher Chern-Simons type, in that they have a [[curvature]] associated to them
which is an invariant differential form ([[invariant polynomial]]) on the moduli stack

$$
  \array{
    \mathbf{Fields}
    \\
    {}^{\mathllap{\exp(i S_{CS})}}\downarrow & \searrow^{\mathrlap{\langle F_{(-)} \wedge \cdots F_{(-)}\rangle}}
    \\
    \mathbf{B}^n U(1)_{conn} &\underset{F_{(-)}}{\to}& \Omega^{n+1}_{cl}
  }
  \,.
$$

We call these theories of [[schreiber:∞-Chern-Simons theory]]-type.



+-- {: .num_example }
###### Example

For $G$ a simply connected simple Lie group and

$$
  \mathbf{B}G_{conn} \coloneqq \Omega^1(-,\mathfrak{g})//G
$$

the [[moduli stack]] of $G$-[[principal connections]], the local action functional of ordinary 3d [[Chern-Simons theory]] is of the form

$$
  \mathbf{B}G_{conn} \to \mathbf{B}^3 U(1)_{conn}
  \,.
$$

This [[prequantum n-bundle|prequantum 3-bundle]] is the _[[Chern-Simons circle 3-bundle]]_.

=--

Many more examples... e.g. [[7d Chern-Simons theory]], [[AKSZ sigma-model]], etc....



##### Geometric defects for $S_{tYM}$ from Chern-Simons invariants: Higher holonomy, parallel transport, fiber integration in differential cohomology


While we may think of the [[(∞,n)-category of cobordisms]] $Bord_n$ as built from [[smooth manifolds]], the [[cobordism theorem]] clearly states that these just serve as a presentation of a structure that is not intrinsically related to smooth or even topological structure. This is made manifest by prop. \ref{ValueOfLocalPrequantumFieldTheoryOnCobordism}: the value of a local prequantum field theory on a [[k-morphism]] in $Bord_n$ depends only on the [[homotopy type]] of the $k$-dimensional manifold that presents this $k$-morphism. Of course this is precisely the property that the term "topological" in _[[topological field theory]]_ is referring to.

But boundaries and defects of a topological field theory may add extra structure to the theory which is not "purely topological" in this way. Here we consider a canonical class of defects for universal higher topological Yang-Mills theory, def. \ref{GeneralHighertYM}, and $\infty$-Chern-Simons theory, def. \ref{HigherCSAsBoundaryTheory}, which implements the expected [[higher parallel transport]]/[[higher holonomy]] of the higher Chern-Simons type action functionals over actual [[smooth manifolds]].

+-- {: .num_prop #FiberIntegrationInDiffCohomologyAsDiagram}
###### Proposition

For $k \leq n$ and for $\Sigma_k$ and [[orientation|oriented]] [[closed manifold]], there is a morphism of smooth moduli stacks

$$
  \exp(i \int_{\Sigma_k}(-))
  \colon
  [\Sigma_k, \mathbf{B}^n U(1)_{conn}]
  \to 
  \mathbf{B}^{n-k}U(1)_{conn}
$$

which is compatible with the standard [[fiber integration|fiber]] [[integration of differential forms]] and with [[transgression]] in [[ordinary cohomology]] in that it fits into a commuting diagram

$$
  \array{
    [\Sigma_k, \flat \mathbf{B}^n U(1)]
    &\stackrel{}{\to}&
    \flat \mathbf{B}^n U(1)
    \\
    \downarrow && \downarrow
    \\
    [\Sigma_k, \mathbf{B}^n U(1)_{conn}]
     &\stackrel{\exp(i \int_{\Sigma_k}(-) )}{\to}&
    \mathbf{B}^{n-k} U(1)_{conn}
    \\
    \downarrow && \downarrow
    \\
    [\Sigma_k, \Omega^{n+1}_{cl}]
    &\stackrel{\int_{\Sigma_k}}{\to}&
    \Omega^{n-k+1}_{cl}
  }
  \,.
$$

More generally, if $\Sigma_k$ is a [[manifold with boundary]] then there is a diagram

$$
  \array{
    && [\Sigma_k, \mathbf{B}^n U(1)_{conn}]
    \\
    & {}^{\mathllap{(-)|_{\partial \Sigma}}}\swarrow && \searrow^{\mathrlap{\omega_\Sigma}}
    \\
    [\partial \Sigma_k, \mathbf{B}^n U(1)_{conn}]
    && \swArrow_{\exp(2 \pi i \int_{\Sigma})} && 
    \Omega^{n-k+1} 
    \\
    & {}_{\mathllap{\exp(2 \pi i \int_{\partial \Sigma}(-))}}\searrow && \swarrow
    \\
    && \mathbf{B}^{n-k+1}U(1)_{conn}
  }
  \,,
$$

where the bottom left map is the fiber integration from before, applied to the closed boundary, and where the [[homotopy]] filling the diagram is such that it reproduces this fiber integration in the case that the boundary is empty, in that 


$$
  \array{
    && [\Sigma_k, \mathbf{B}^n U(1)_{conn}]
    \\
    & {}^{\mathllap{(-)|_{\partial \Sigma}}}\swarrow && \searrow^{\mathrlap{\omega_\Sigma}}
    \\
    [\emptyset, \mathbf{B}^n U(1)_{conn}]
    && \swArrow_{\exp(2 \pi i \int_{\Sigma})} && 
    \Omega^{n-k+1} 
    \\
    & {}_{\exp(2 \pi i \int_{\emptyset}(-))}\searrow && \swarrow
    \\
    && \mathbf{B}^{n-k+1}U(1)_{conn}
  }
  \;\;\;
  \simeq
  \;\;\;
  \array{
    && [\Sigma_k, \mathbf{B}^n U(1)_{conn}]
    \\
    &&  \downarrow
    \\
    && \mathbf{B}^{n-k}U(1)_{conn}
    \\
    & {}^{\mathllap{(-)|_{\partial \Sigma}}}\swarrow && \searrow^{\mathrlal{\omega_\Sigma}}
    \\
    \ast
    && \swArrow_{\exp(2 \pi i \int_{\Sigma})} && 
    \Omega^{n-k+1} 
    \\
    & {}_{}\searrow && \swarrow
    \\
    && \mathbf{B}^{n-k+1}U(1)_{conn}
  }
  \,,
$$

=--

+-- {: .proof}
###### Proof

This follows by unwinding the traditional formulas for [[fiber integration in differential cohomology]], reformulating them in [[homotopy theory]] and observing that they are natural in their arguments, hence extend to morphisms of higher stacks, as discussed here.

=--

+-- {: .num_remark }
###### Remark

A homotopy/gauge equivalence between a [[circle n-bundle with connection]] $(P,\nabla)$ and a trivial circle $n$-bundle with connection given by a globally defined differential form $(0,\omega)$ is equivalently a section/trivialization of the underlying [[circle n-bundle]]. Therefore the above says that the fiber integration of an $n$-connection over a manifold with boundary is equivalently a section of the transgression of the underlying bundle to the boundary.

=--

We may combine this with the $\infty$-Chern-Simons action functional:

+-- {: .num_defn }
###### Definition

Let $\exp(i S_{CS}) \colon \mathbf{Fields} \to \mathbf{B}^n U(1)_{conn}$ be an [[schreiber:∞-Chern-Simons theory]] [[local action functional]] as in prop. \ref{HigherCSAsBoundaryTheory}. Then for $\Sigma_k$ an [[orientation|oriented]] [[smooth manifold|smooth]] $k$-[[dimension|dimensional]] [[manifold with boundary]], the corresponding **transgression defect** is the [[pasting]]-composite 

$$
  \array{
    && && [\Sigma, \mathbf{Fields}]
    \\
    && & {}^{\mathllap{(-)|_{\partial \Sigma}}}\swarrow && \searrow^{\mathrlap{[\Sigma_k, \exp(i S_{CS})]}}
    \\
    && [\partial \Sigma, \mathbf{Fields}] && && [\Sigma_k, \mathbf{B}^n U(1)_{conn}]
    \\
    && & \searrow& & {}^{\mathllap{(-)|_{\partial \Sigma}}}\swarrow && \searrow^{\mathrlap{\omega_\Sigma}}
    \\
    && && [\partial \Sigma_k, \mathbf{B}^n U(1)_{conn}]
    && \swArrow_{\exp(2 \pi i \int_{\Sigma}(-))} && 
    \Omega^{n-k+1} 
    \\
    && && & {}_{\exp(2 \pi i \int_{\partial \Sigma}(-))}\searrow && \swarrow
    \\
    && && && \mathbf{B}^{n-k+1}U(1)_{conn}
  }
  \,,
$$

or rather its further pullback to the [[shape modality]]

$$
  \array{
    && [\Pi(\Sigma), \mathbf{Fields}]
    \\
    & \swarrow 
    \\
    [\Pi(\partial \Sigma), \mathbf{Fields}]
  }
  \,.
$$

=--

This is a defect between the boundary transgression, def. \ref{FiberIntegrationInDiffCohomologyAsDiagram}, of the $\infty$-Chern-Simons theory and the tautological higher differential higher Chern-Simons theory. 

We see below that both the [[Wess-Zumino-Witten theory]] as well as [[Wilson lines]] in Chern-Simons theory arise from transgression defects this way.

(...)

#### $d = n-1$, Topological Chern-Simons boundaries

(...)


#### $d = n-1$, Wess-Zumino-Witten field theories

(...)

  defect given by transgression over circle

(...)

#### $d = n-2$, Wilson loop/Wilson surface field theories

(...)

  defect given by transgression over sphere

(...)


## **Prequantum Gauge theory and Gravity**
 {#ActionFunctionalsForChernSimonsTypeGaugeTheories}

In the previous chapters we have set up [[prequantum field theory]] and [[classical field theory]] in generality. Here we discuss examples of such [[field (physics)|field]] [[theory (physics)|theories]] in more detail.


+-- {: bluebox }
###### Contents

1. [Model layer](#GaugeAndGravityModelLayer)

   We introduce a list of important examples of field theories in fairly tradtional terms.

1. [Semantics layer](#GaugeAndGravitySemanticsLayer)

   We study the above physical systems with the tools of of [[cohesive (∞,1)-topos]]-theory as developed in the previous semantics-layers.

1. [Syntax layer](#GaugeAndGravitySyntaxLayer)

=--


### Model layer 
 {#GaugeAndGravityModelLayer}

+-- {: bluebox }
###### Examples

1. [1d Chern-Simons theory](#1dCSTheory)

1. [Nonabelian charged particle and Wilson loops](#ModLayerNonabelianChargedParticle)

1. [2d Chern-Simons theory](#2dCSTheory)

1. [3d Chern-Simons theory](#3dCSTheory)

1. [(4k+3)d U(1)-Chern-Simons theory](#HigherAbelianCSTheory)

1. [7d Chern-Simons theory](#7dCSTheory)

1. [∞-Chern-Simons theory](#InfinityCSTheory)

   * [String field theory](#StringFieldTheory)

     * [Gauge fields and gravity -- Einstein-Maxwell-Yang-Mills theory](#EinsteinYangMillsTheory)

       * [Kaluza-Klein compactification](#KaluzaKleinCompactification)

       * [Standard model of particle physics](#StandardModelParticlePhyiscs)

       * [standard model of cosmology](#StandardModelCosmology)

=--



#### 1d Chern-Simons theory
 {#1dCSTheory}

* [[1d Chern-Simons theory]]

#### 2d Chern-Simons theory
 {#2dCSTheory}

* [[2d Chern-Simons theory]]

#### Nonabelian charged particle and Wilson loops
 {#ModLayerNonabelianChargedParticle}

The [[prequantum field theory]] which describes the gauge interaction of a  single nonabelian charged particle -- a _[[Wilson loop]]_ -- turns out to be equivalent to what in mathematics is called the _[[orbit method]]_. We discuss here the traditional formulation of these matters. Below in 
_[Semantics layer -- Nonabelian charged particle and Wilson loops](#GaugeAndGravityWilsonLoops)_ we then show how all this is naturally understood from a certain [[extended Lagrangian]] which is induced by a regular [[coadjoint orbit]].

A useful review of the following is also in ([Beasley, section 4](#Beasley)).

##### The group and its Lie algebra

Throughout, let $G$ be a [[semisimple Lie group|semisimple]] [[compact topological group|compact]] [[Lie group]]. For some considerations below we furthermore assume it to be [[simply connected topological space|simply connected]].

Write $\mathfrak{g}$ for its [[Lie algebra]]. Its canonical (up to scale) binary [[invariant polynomial]] we write

$$
  \langle -,-\rangle : \mathfrak{g} \otimes \mathfrak{g} \to \mathbb{R}
  \,.
$$

Since this is non-degenerate, we may equivalently think of this as an [[isomorphism]] 

$$
  \mathfrak{g} \simeq \mathfrak{g}^*
$$

that identifies the [[vector space]] underlying the Lie algebra with its [[dual vector space]] $\mathfrak{g}^*$.


##### The coadjoint orbit and the coset space/ flag manifold

We discuss the [[coadjoint orbits]] of $G$ and their relation to the [[coset space]]/[[flag manifolds]] of $G$.

Write 

1. $T \hookrightarrow G$ inclusion of the [[maximal torus]] of $G$.

1 $\mathfrak{t} \hookrightarrow \mathfrak{g}$ the corresponding [[Cartan subalgebra]]


In all of the following we consider an element $\langle\lambda,-\rangle \in \mathfrak{g}^*$.

+-- {: .num_defn }
###### Definition

For $\langle\lambda,-\rangle \in \mathfrak{g}^*$ write

$$
  \mathcal{O}_\lambda \hookrightarrow \mathfrak{g}^*
$$

for its [[coadjoint orbit]]

$$
  \mathcal{O}_{\lambda} = \{ Ad_g^*(\langle\lambda,-\rangle) \in \mathfrak{g}^* | g \in G \}
  \,.
$$

Write $G_\lambda \hookrightarrow G$ for the [[stabilizer subgroup]] of $\langle \lambda,-\rangle$ under the coadjoint action.

=--

+-- {: .num_prop}
###### Proposition

There is an equivalence

$$
  G/G_\lambda \stackrel{\simeq}{\to} \mathcal{O}_\lambda
$$

given by 

$$
  g G_\lambda \mapsto Ad_g^* \langle\lambda,-\rangle
  \,.
$$

=--

+-- {: .num_defn #RegularElement}
###### Definition

An element $\langle\lambda,-\rangle \in \mathfrak{g}^*$ is **regular** if its [[coadjoint action]] [[stabilizer subgroup]] coincides with the [[maximal torus]]: $G_\lambda \simeq T$. 

=--

+-- {: .num_example }
###### Example

For generic values of $\lambda$ it is regular.
The element in $\mathfrak{g}^*$ farthest from regularity is $\lambda = 0$ for which $G_\lambda = G$ instead.

=--

##### The symplectic form

We describe a canonical [[symplectic form]] on the [[coadjoint orbit]]/[[coset]] $\mathcal{O}_\lambda \simeq G/G_\lambda$.

Write $\theta \in \Omega^1(G, \mathfrak{g})$ for the [[Maurer-Cartan form]] on $G$.

+-- {: .num_defn #The2FormOnG}
###### Definition

Write 

$$
  \Theta_\lambda := \langle \lambda, \theta \rangle \in \Omega^1(G)
$$

for the 1-form obtained by pairing the value of the Maurer-Cartan form at each point with the gixed element $\lambda \in \mathfrak{g}^*$.

Write

$$
  \nu_\lambda := d_{dR} \Theta_\lambda
$$

for its [[de Rham differential]].

=--

+-- {: .num_prop #TheSymplecticFormOnTheCoset}
###### Proposition

The 2-form $\nu_\lambda$ from def. \ref{The2FormOnG} 

1. satisfies

   $$
     \nu_\lambda = \frac{1}{2}\langle \lambda, [\theta\wedge \theta]\rangle
     \,.
   $$

1. it descends to a closed $G$-invariant 2-form on the [[coset space]], to be denoted by the same symbol 

   $$
     \nu_\lambda \in \Omega^2_{cl}(G/G_\lambda)^G
     \,.
   $$ 

1. this is non-degenerate and hence defines a [[symplectic form]] on $G/G_\lambda$.

=--

##### The prequantum bundle

We discuss the [[geometric prequantization]] of the [[symplectic manifold]] given by the [[coadjoint orbit]] $\mathcal{O}_\lambda$ equipped with its [[symplectic form]] $\nu_\lambda$ of def. \ref{TheSymplecticFormOnTheCoset}.

Assume now that $G$ is [[simply connected topological space|simply connected]]. 

+-- {: .num_prop #WeightsAndCharacters}
###### Proposition

The [[weight lattice]] $\Gamma_{wt} \subset \mathfrak{t}^* \simeq \mathfrak{t}$ of the Lie group $G$ is [[isomorphism|isomorphic]] to the group of [[group characters]]

$$
  \Gamma_{wt} \stackrel{\simeq}{\to} Hom_{LieGrp}(G,U(1))
$$

where the identification takes $\langle \alpha , -\rangle \in \mathfrak{t}^*$ to $\rho_\alpha : T \to U(1)$ given on $t = \exp(\xi)$ for $\xi \in \mathfrak{t}$ by

$$
  \rho_\alpha : \exp(\xi) \mapsto \exp(i \langle \alpha, \xi\rangle)
  \,.
$$

=--

+-- {: .num_prop }
###### Proposition

The [[symplectic form]] $\nu_\lambda \in \Omega^2_{cl}(G/T)$ of prop. \ref{TheSymplecticFormOnTheCoset} is integral precisely if $\langle \lambda, - \rangle$ is in the [[weight lattice]].

=--

##### The Hamiltonian $G$-action / coadjoint moment map

The group $G$ canonically [[action|acts]] on the [[coset space]] $G/G_{\lambda}$ (by multiplication from the left). We discuss a lift of this action to a [[Hamiltonian action]] with respect to the [[symplectic manifold]] structure $(G/T, \nu_\lambda)$ of prop. \ref{TheSymplecticFormOnTheCoset}, equivalently a [[momentum map]] exhibiting this Hamiltonian action.



##### Wilson loops and 1d Chern-Simons $\sigma$-models with target the coadjoint orbit
 {#WilsonLoopsAnd1DCSSigmaModelWithTargetTheCoadjointOrbit}

Above (...) we discussed how an [[irreducible representation|irreducible]] [[unitary representation]] of $G$ is encoded by the [[prequantization]] of a  [[coadjoint orbit]] $(\mathcal{O}_\lambda, \nu_\lambda)$. Here we discuss how to express [[Wilson loops]]/[[holonomy]] of $G$-[[principal connections]] in this representation as the [[path integral]] of a topological particle charged under this background field, whose [[action functional]] is that of a [[1-dimensional Chern-Simons theory]].

Let $A|_{S^1} \in \Omega^1(S^1, \mathfrak{g})$ be a [[Lie algebra valued 1-form]] on the circle, equivalently a $G$-[[principal connection]] on the circle. 

For 

$$
  \rho : G \to Aut(V)
$$

a [[representation]] of $G$, write

$$
  W_{S^1}^R(A) :=  hol^R_{S^1}(A) := Tr_R( tra_{S^1}(A) )
$$

for the [[holonomy]] of $A$ around the circle in this representation, which is the [[trace]] of its [[parallel transport]] around the circle (for any basepoint). If one thinks of $A$ as a [[background gauge field]] then this is alse called a [[Wilson loop]].

+-- {: .num_defn #ActionFunctionalForTopologicalChargedParticle}
###### Definition

Let the [[action functional]]

$$
  \exp(i CS_\lambda(-)^A) 
  \;\colon\;  
  [S^1, G/T] \to U(1)
$$

be given by sending $g T : S^1 \to G/T$ represented by $g : S^1 \to G$ to

$$
  \exp(i \int_{S^1} \langle \lambda, A^g\rangle )
  \,,
$$

where 

$$
  A^g := Ad_g(A) + g^* \theta
$$

is the [[gauge transformation]] of $A$ under $g$. 

=--

+-- {: .num_prop #WilsonLoopIsPartitionFunctionOf1dCSSigmaModel}
###### Proposition

The [[Wilson loop]] of $A$ over $S^1$ in the unitarry irreducible representation $R$ is proportional to the [[path integral]] of the 1-dimensional [[sigma-model]] with 

1. [[target space]] the [[coadjoint orbit]] $\mathcal{O}_\lambda \simeq G/T$ for $\langle \lambda, - \rangle$ the [[weight (in representation theory)|weight]] corresponding to $R$ under the [[Borel-Weil-Bott theorem]]

1. [[action functional]] the functional of def. \ref{ActionFunctionalForTopologicalChargedParticle}:

$$
  W_{S^1}^R(A)
  \propto
  \int_{[S^1, \mathcal{O}_\lambda]}
  D(g T)
  \exp(i \int_{S^1}  \langle \lambda, A^g\rangle)
  \,.
$$

=--

See for instance ([Beasley, (4.55)](#Beasley)). 

+-- {: .num_remark }
###### Remark

Notice that since $\mathcal{O}_\lambda$ is a [[manifold]] of finite [[dimension]], the [[path integral]] for a point particle with this target space can be and has been defined rigorously, see at _[[path integral]]_.

=--



#### 3d Chern-Simons theory
 {#3dCSTheory}

* [[3d Chern-Simons theory]]

#### $(4k+3)$d $U(1)$-Chern-Simons theory
 {#HigherAbelianCSTheory}

* [[higher dimensional Chern-Simons theory]]

#### 7d Chern-Simons theory
 {#7dCSTheory}
 
* [[7d Chern-Simons theory]]

#### $\infty$-Chern-Simons theory
 {#InfinityCSTheory}

* [[schreiber:infinity-Chern-Simons theory]]

#### String field theory
 {#StringFieldTheory}

* [[string field theory]]

##### Gauge fields and gravity -- Einstein-Maxwell-Yang-Mills theory 
 {#EinsteinYangMillsTheory}

* [[gravity]]

* [[Yang-Mills theory]]
  
  * [[Yang-Mills instanton]] number = [[second Chern class]]

* [[Einstein-Yang-Mills theory]]


##### Kaluza-Klein compactification
 {#KaluzaKleinCompactification}

* [[Kaluza-Klein compactification]]


##### Standard model of particle physics 
 {#StandardModelParticlePhyiscs}

* [[standard model of particle physics]]

##### Standard model of cosmology
 {#StandardModelCosmology}

* [[standard model of cosmology]]


### Semantic Layer
 {#GaugeAndGravitySemanticsLayer}


an exposition and survey is in ([FSS 13](#FiorenzaSatiSchreiberCSIntroAndSurvey)).

+-- {: bluebox }
###### 

1. [1d Chern-Simons theory](#GaugeAndGravity1dCSTheory)

1. [Nonabelian charged particle trajectories -- Wilson loops](#GaugeAndGravityWilsonLoops)

1. [2d CS theory: WZW terms and Chan-Paton gauge fields](#GaugeFieldsSemanticsLayerChanPatonGaugeField)

1. [3d Chern-Simons theory with Wilson loops](#GaugeAndGravity3dCSWithWilson)

1. [Chan-Paton gauge fields on D-branes](#GaugeAndGravityChanPatonGaugeFieldsOnDBranes)

=--

#### 1d Chern-Simons theory
 {#GaugeAndGravity1dCSTheory}

For some $n \in \mathbb{N}$ let 

$$
  det \;\colon\; U(n) \to U(1)
$$

be the [[Lie group]] [[homomorphism]] from the [[unitary group]] to the [[circle group]] which is given by sending a [[unitary matrix]] to its [[determinant]].

Being a Lie group homomorphism, this induces a map of [[deloopings]]/[[moduli stacks]]

$$
  \mathbf{B}det
   \;\colon\; 
  \mathbf{B}U(n) \to \mathbf{B}U(1)
$$

Under [[geometric realization of cohesive infinity-groupoids]] this is the universal [[first Chern class]]

$$
  {\vert \mathbf{B}det\vert}
  \simeq
  c_1 
  \;\colon\;  
  B U(n)  
  \to B U(1) \simeq K(\mathbb{Z},2)
  \,.
$$

Moreiver this has the evident differential refinement

$$
  \widehat {\mathbf{B} det}
  \;\colon\;
  \mathbf{B} U(n)_{conn}
  \to 
  \mathbf{B} U(1)_{conn}
$$

given on [[Lie algebra valued 1-forms]] by taking the [[trace]]

$$
  tr \;\colon\; \mathfrak{u}(n) \to \mathfrak{u}(1)
  \,.
$$

So we get a [[1d Chern-Simons theory]] with $\widehat{\mathbf{B}det}$ 
as its [[extended Lagrangian]].
 

#### Nonabelian charged particle trajectories -- Wilson loops
 {#GaugeAndGravityWilsonLoops}

We consider now [[extended Lagrangians]] defined on [[field (physics)|fields]] as above in _[Nonabelian charged particle trajectories -- Wilson loops](#NonabelianChargedParticle)_. This provides a natural reformulation in [[higher geometry]] of the constructions in the _[[orbit method]]_ as reviewed above in _[Model layer -- Nonabelian charged particle](#ModLayerNonabelianChargedParticle)_.


+-- {: bluebox }
###### 

1. [Survey](#FormulationInHigherGeometrySurvey)

1. [Definitions and constructions](#FormulationInHigherGeometryDefinitions)

1. [Nonabelian charged particle trajectories &#8211; Wilson loops](GaugeAndGravityWilsonLoops)

1. [3d Chern-Simons theory with Wilson loops](#ExtendedChern-SimonsTheoryAndWilsonLoops).

=--


##### Survey 
 {#FormulationInHigherGeometrySurvey}

We discuss how for $\lambda \in \mathfrak{g}$ a regular element, there is a canonical diagram of [[smooth infinity-groupoid|smooth]] [[moduli stacks]] of the form

$$
  \array{
     \mathcal{O}_\lambda &\stackrel{\simeq}{\to}& G/T &\stackrel{\mathbf{\theta}}{\to}& \Omega^1(-,\mathfrak{g})//T &\stackrel{\langle \lambda, - \rangle}{\to}& \mathbf{B} U(1)_{conn}
   \\
    && \downarrow &\swArrow_{\simeq}& \downarrow^{\mathrlap{\mathbf{J}}}
    \\
    && * &\stackrel{}{\to}& \mathbf{B}G_{conn} &\stackrel{\mathbf{c}}{\to}& \mathbf{B}^3 U(1)_{conn}
  }
  \,,
$$

where

1. $\mathbf{J}$ is the canonical [[2-monomorphism]];

1. the left square is a [[homotopy pullback]] square, hence $\mathbf{\theta}$ is the [[homotopy fiber]] of $\mathbf{J}$;

1. the bottom map is the [[extended Lagrangian]] for $G$-[[Chern-Simons theory]], equivalently the universal [[Chern-Simons circle 3-bundle with connection]];

1. the top map denoted $\langle \lambda,- \rangle$ is an [[extended Lagrangian]] for a [[1-dimensional Chern-Simons theory]];

1. the total top composite modulates a [[prequantum circle bundle]] which is a [[prequantization]] of the canonical [[symplectic manifold]] structure on the [[coadjoint orbit]] $\Omega_\lambda \simeq G/T$.


##### Definitions and constructions
 {#FormulationInHigherGeometryDefinitions}



Write $\mathbf{H} = $ [[Smooth∞Grpd]] for the [[cohesive (∞,1)-topos]] of smooth $\infty$-groupoids.


For the following, let $\langle \lambda, - \rangle \in \mathfrak{g}^*$ be a _regular_ element, def. \ref{RegularElement}, so that the [[stabilizer subgroup]] is identified with a [[maximal torus]]: $G_\lambda \simeq T$. 

As usual, write 

$$
  \mathbf{B}G_{conn} \simeq \Omega^1(-,\mathfrak{g})//G
  \in 
  \mathbf{H}
$$

for the [[moduli stack]] of $G$-[[principal connections]]. 

+-- {: .num_defn #InclusionOfModuliStacks}
###### Definition

Write 

$$
  \mathbf{J} := ( \Omega^1(-,\mathfrak{g})//T \to \Omega^1(-,\mathfrak{g})//G \simeq \mathbf{B}G_{conn} )
  \in 
  \mathbf{H}^{\Delta^1}
$$

for the canonical map, as indicated.

=--

+-- {: .num_remark }
###### Remark

The map $\mathbf{J}$ is the differential refinement of the [[delooping]] $\mathbf{B}T \to \mathbf{B}G$ of the defining inclusion. By the general discussion at [[coset space]] we have a [[homotopy fiber sequence]]

$$
  \array{
    \mathcal{O}_\lambda \simeq G/T &\to& \mathbf{B}T
    \\
    && \downarrow
    \\
    && \mathbf{B}G
  }
  \,.
$$

By the discussion at _[[∞-action]]_ this exhibits the canonical [[action]] $\rho$ of $G$ on its [[coset space]]: it is the [[universal associated ∞-bundle|universal rho-associated bundle]].

=--

The following proposition says what happens to this statement under differential refinement


+-- {: .num_prop #ThetaAsHomotopyFiberOfJ}
###### Proposition

The [[homotopy fiber]] of $\mathbf{J}$ in def. \ref{InclusionOfModuliStacks} is 

$$
  \mathbf{\theta} : G/T \stackrel{}{\to} \Omega^1(-,\mathfrak{g})//T
$$

given over a test manifold $U \in $ [[CartSp]] by the map

$$
  \mathbf{\theta}_U : C^\infty(U,G/T) \to \Omega^1(U,\mathfrak{g})
$$

which sends $g \mapsto g^* \theta$, where $\theta$ is the [[Maurer-Cartan form]] on $G$.

=--

+-- {: .proof}
###### Proof

We compute the [[homotopy pullback]] of $\mathbf{J}$ along the point inclusion by the [[factorization lemma]] as discussed at _[homotopy pullback -- Constructions](homotopy%20pullback#ConstructionsGeneral)_.

This says that with $\mathbf{J}$ presented canonically as a map of presheaves of groupoids via the above definitions, its homotopy fiber is presented by the presheaf of groupids $hofib(\mathbf{J})$ which is the [[limit]] [[cone]] in


$$
  \array{
    hofib(\mathbf{J}) &\to& &\to& \Omega^1(-, \mathfrak{g})
    \\
    \downarrow && \downarrow && \downarrow
    \\
    && (\mathbf{B}G_{conn})^I &\to& \mathbf{B}G_{conn}
    \\
    \downarrow && \downarrow
    \\
    * &\stackrel{}{\to}& \mathbf{B}G_{conn}
  }
  \,.
$$ 

Unwinding the definitions shows that $hofib(\mathbf{J})$ has

1. [[objects]] over a $U \in $ [[CartSp]] are equivalently morphisms $0 \stackrel{g}{\to} g^* \theta$ in $\Omega^1(U,\mathfrak{g})//C^\infty(U,G)$, hence equivalently elements $g \in C^\infty(U,G)$;

1. [[morphisms]] are over $U$ [[commuting diagram|commuting triangles]]

   $$
     \array{
       g_1^* \theta &&\stackrel{t}{\to}&& g_2^* \theta
       \\
       & {}_{\mathllap{g_1}}\nwarrow && \nearrow_{\mathrlap{g_2}}
       \\
       && 0
     }
   $$

   in $\Omega^1(U,\mathfrak{g})//C^\infty(U,G)$ with $t \in C^\infty(U,T)$, hence equivalently morphisms

   $$
     g_1 \stackrel{t}{\to} g_2
   $$

   in $C^\infty(U,G)//C^\infty(U,T)$.

1. The canonical map $hofib(\mathbf{J}) \to \Omega^1(-,\mathfrak{g})//T$ picks the top horizontal part of these commuting triangles hence equivalently sends $g$ to $g^* \theta$.

=--

+-- {: .num_prop #Extended1dCSLagrangianFromLambda}
###### Proposition

If $\langle \lambda ,- \rangle \in \Gamma_{wt} \hookrightarrow \mathfrak{g}^*$ is in the [[weight lattice]], then there is a morphism of [[moduli stacks]]

$$
  \langle \lambda, - \rangle
  \;\colon\; 
  \Omega^1(-,\mathfrak{g})//T
  \to
  \mathbf{B}U(1)_{conn}
$$

in $\mathbf{H}$ given over a test manifold $U \in $ [[CartSp]] by the [[functor]]

$$
  \langle \lambda, - \rangle_U 
  \;:\; 
  \Omega^1(U,\mathfrak{g})//C^\infty(U,G) \to \Omega^1(U)//C^\infty(U,U(1))
$$

which is given on objects by

$$
  A \mapsto \langle \lambda, A\rangle
$$

and which maps morphisms labeled by $\exp(\xi) \in T$, $\xi \in C^\infty(-,\mathfrak{t})$ as

$$
  \exp(\xi) \mapsto \exp( i \langle \lambda, \xi \rangle )
  \,.
$$ 


=--

+-- {: .proof}
###### Proof

That this construction defines a map $*//T \to *//U(1)$ is 
the statement of prop. \ref{WeightsAndCharacters}. It remains to check that the differential 1-forms gauge-transform accordingly. 

For this the key point is that since $T \simeq G_\lambda$ stabilizes $\langle \lambda , - \rangle$ under the [[coadjoint action]], the [[gauge transformation]] law for points $A : U \to \mathbf{B}G_{conn}$, which for $g \in C^\infty(U,G)$ is

$$
  A \mapsto Ad_g A + g^* \theta
  \,,
$$

maps for $g = exp( \xi ) \in C^\infty(U,T) \hookrightarrow C^\infty(U,G)$ to the gauge transformation law in $\mathbf{B}U(1)_{conn}$:

$$
  \begin{aligned}
    \langle \lambda, A \rangle 
    & \mapsto
    \langle \lambda, Ad_g A\rangle + \langle \lambda, g^* \theta\rangle
    \\
     & = \langle \lambda, A \rangle + d  \langle\lambda, \xi \rangle
  \end{aligned}
$$

=--


+-- {: .num_remark #ThePrequantumBundleFromCanonicalMaps}
###### Remark

The composite of the canonical maps of prop. \ref{ThetaAsHomotopyFiberOfJ} and prop. \ref{Extended1dCSLagrangianFromLambda} modulates a canonical [[circle bundle with connection]] on the [[coset space]]/[[coadjoint orbit]]:

$$
  \langle \lambda, \mathbf{\theta}\rangle
  : 
  G/T
  \stackrel{\mathbf{\theta}}{\to}
  \Omega^1(-,\mathfrak{g})//T
  \stackrel{\langle \lambda, - \rangle}{\to}
  \mathbf{B}U(1)_{conn}
  \,.
$$ 

=--

+-- {: .num_prop }
###### Proposition

The [[curvature]] 2-form of the circle bundle $\langle \lambda, \mathbf{\theta}\rangle$ from remark \ref{ThePrequantumBundleFromCanonicalMaps} is the [[symplectic form]] of prop. \ref{TheSymplecticFormOnTheCoset}. Therefore $\langle \lambda, \mathbf{\theta}\rangle$ is a [[prequantization]] of the [[coadjoint orbit]] $(\mathcal{O}_\lambda \simeq G/T, \nu_\lambda)$.

=--

+-- {: .proof}
###### Proof

The curvature 2-form is modulated by the composite

$$
  \omega 
  :
  G/T
  \stackrel{\mathbf{\theta}}{\to}
  \Omega^1(-,\mathfrak{g})//T
  \stackrel{\langle \lambda, - \rangle}{\to}
  \mathbf{B}U(1)_{conn}
  \stackrel{F_{(-)}}{\to}
  \Omega^2_{cl}
  \,.
$$ 

Unwinding the above definitions and propositions, one finds that this is given over a test manifold $U \in $ [[CartSp]] by the map

$$
  \omega_U : C^\infty(G/T) \to \Omega^2_{cl}(U)
$$

which sends

$$
  [g] \mapsto d \langle \lambda,  g^* \theta \rangle
  \,.
$$

=--

##### Nonabelian charged particle trajectories &#8211; Wilson loops
{#GaugeAndGravityWilsonLoops}


Let $\Sigma$ be an [[orientation|oriented]] [[closed manifold|closed]] [[smooth manifold]] of [[dimension]] 3 and let 

$$
  C 
  \;\colon\;
  S^1 \hookrightarrow \Sigma
$$

be a [[submanifold]] inclusion of the [[circle]]: a [[knot]] in $\Sigma$.

Let $R$ be an [[irreducible representation|irreducible]] 
[[unitary representation]] of $G$ and let $\langle \lambda,-\rangle$ be a [[weight (in representation theory)|weight]] corresponding to it by the [[Borel-Weil-Bott theorem]].

Regarding the inclusion $C$ as an object in the [[arrow (∞,1)-topos]] $\mathbf{H}^{\Delta^1}$, say that a [[gauge field]] configuration for $G$-[[Chern-Simons theory]] on $\Sigma$ with 
[[Wilson loop]] $C$ and labeled by the [[representation]] $R$ is a map

$$
  \phi 
  \;\colon\;
  C
  \to 
  \mathbf{J}
$$ 

in the [[arrow (∞,1)-topos]] $\mathbf{H}^{(\Delta^1)}$ of the ambient [[cohesive (∞,1)-topos]]. Such a map is equivalently by a square

$$
  \array{
    S^1 &\stackrel{(A|_{S^1})^g}{\to}& \Omega^1(-,\mathfrak{g})//T
    \\
    \downarrow^{\mathrlap{C}} 
    &\swArrow_{g}&   
    \downarrow^{\mathrlap{\mathbf{J}}}
    \\
    \Sigma
    &\stackrel{A}{\to}&
    \mathbf{B}G_{conn}
  }
$$

in $\mathbf{H}$. 
In components this is 

* a $G$-[[principal connection]] $A$ on $\Sigma$;

* a $G$-valued function $g$ on $S^1$

which fixes the field on the circle defect to be $(A|_{S^1})^g$, as indicated. 

Moreover, a _[[gauge transformation]]_ between two such fields $\kappa : \phi \Rightarrow \phi'$ is a $G$-gauge transformation of $A$ and  a $T$-gauge transformation of $A|_{S^1}$ such that these intertwine the component maps $g$ and $g'$. If we keep the bulk gauge field $A$ fixed, then his means that two fields $\phi$ and $\phi'$ as above are gauge equivalent precisely if there is a function $t \;\colon\; S^1 \to T$ such that $g = g' t$, hence gauge [[equivalence classes]] of fields for fixed bulk gauge field $A$ are parameterized by their components $[g] = [g'] \in [S^1, G/T]$ with values in the coset space, hence in the coadjoint orbit.

For every such field configuration we can evaluate two [[action functionals]]: 

1. that of 3d [[Chern-Simons theory]], whose [[extended Lagrangian]] is $\mathbf{c} : \mathbf{B}G_{conn} \to \mathbf{B}^3 U(1)_{conn}$;

1. that of the [[1-dimensional Chern-Simons theory]] discussed [above](#WilsonLoopsAnd1DCSSigmaModelWithTargetTheCoadjointOrbit) whose [[extended Lagrangian]] is $\langle \lambda, -\rangle : \Omega^1(-,\mathfrak{g})//T \to \mathbf{B}U(1)_{conn}$, by prop. \ref{Extended1dCSLagrangianFromLambda}.

These are obtained by postcomposing the above square on the right by these [[extended Lagrangians]] 

$$
  \array{
    S^1 &\stackrel{(A|_{S^1})^g}{\to}& \Omega^1(-,\mathfrak{g})//T
    &\stackrel{\langle \lambda, -\rangle}{\to}&
    \mathbf{B}U(1)_{conn}
    \\
    \downarrow^{\mathrlap{C}} 
    &\swArrow_{g}&   
    \downarrow^{\mathrlap{\mathbf{J}}}
    \\
    \Sigma
    &\stackrel{A}{\to}&
    \mathbf{B}G_{conn}
    &\stackrel{\mathbf{c}}{\to}&
    \mathbf{B}U(1)_{conn}
  }
$$

and then preforming the [[fiber integration in ordinary differential cohomology]] over $S^1$ and over $\Sigma$, respectively. 

For the bottom map this gives the ordinary action functional of [[Chern-Simons theory]]. For the top map inspection of the proof of prop. \ref{Extended1dCSLagrangianFromLambda} shows that this gives the 1d Chern-Simons action whose [[partition function]] is the [[Wilson loop]] observable by prop. \ref{WilsonLoopIsPartitionFunctionOf1dCSSigmaModel} above. 

#### 2d CS-theory, WZW-term and Chan-Paton gauge fields
 {#GaugeFieldsSemanticsLayerChanPatonGaugeField}

In the context of [[string theory]], the [[background gauge field]] for the [[open string]] [[sigma-model]] over a [[D-brane]] in [[bosonic string theory]] or [[type II string theory]] is a unitary [[principal bundle]] [[connection on a bundle|with connection]], or rather, by the Kapustin-part of the [[Freed-Witten-Kapustin anomaly cancellation]] mechanism, a [[twisted bundle|twisted unitary bundle]], whose twist is the restriction of the ambient [[B-field]] to the [[D-brane]]. 

We considered these [[field (physics)|fields]] already [above](#ChanPatonGaugeFields). Here we discuss the corresponding [[action functional]] for the [[open string]] coupled to these fields

The first hint for the existence of such [[background gauge fields]] for the [[open string]] 2d-[[sigma-model]] comes from the fact that the open string's endpoint can naturally be taken to carry labels $i \in \{1, \cdots n\}$. Further analysis then shows that the lowest excitations of these $(i,j)$-strings behave as the quanta of a $U(n)$-[[gauge field]], the $(i,j)$-excitation being the given [[matrix]] element of a $U(n)$-valued connection 1-form $A$.

This original argument goes back work by Chan and Paton. Accordingly one speaks of _Chan-Paton factors_ and _Chan-Paton bundles_ . 


We discuss the Chan-Paton gauge field and its [[quantum anomaly cancellation]] in [[extended prequantum field theory]].

Throughout we write $\mathbf{H} = $ [[Smooth∞Grpd]] for the [[cohesive (∞,1)-topos]] of [[smooth ∞-groupoids]].

+-- {: bluebox }
###### 

1. [The B-field as a prequantum 2-bundle](#TheBFieldAsAPrequantum2Bundle)

1. [The Chan-Paton gauge field](#PrequantumGaugeFieldsTheChanPatonGaugeField)

1. [The open string sigma-model](#TheOpenStringSigmaModel)

1. [The anomaly-free open string coupling to the Chan-Paton gauge field](#TheAnomalyFreeOpenStringCouplingToTheChanPatonGaugeField)

=--


##### The $B$-field as a prequantum 2-bundle
 {#TheBFieldAsAPrequantum2Bundle}

For $X$ a [[type II supergravity]] [[spacetime]], the [[B-field]] is a map

$$
  \nabla_B \;\colon\; X \to \mathbf{B}^2 U(1)
  \,.
$$

If $X = G$ is a [[Lie group]], this is the [[prequantum 2-bundle]] of $G$-[[Chern-Simons theory]]. Viewed as such we are to find a canonical [[∞-action]] of the [[circle 2-group]] $\mathbf{B}U(1)$ on some $V \in \mathbf{H}$, form the corresponding [[associated ∞-bundle]] and regard the [[sections]] of that as the [[prequantum 2-states]] of the theory.

The Chan-Paton gauge field is such a prequantum 2-state.


##### The Chan-Paton gauge field
 {#PrequantumGaugeFieldsTheChanPatonGaugeField}

We discuss the [[Chan-Paton gauge fields]] over [[D-branes]]
in [[bosonic string theory]] and over $Spin^c$-D-branes in [[type II string theory]].

We fix throughout a natural number $n \in \mathbb{N}$, the _[[rank]]_ of the Chan-Paton gauge field.

+-- {: .num_prop #TheLongSequenceOfTheProjectiveUnitaryExtension}
###### Proposition

The [[extension of groups|extension]] of [[Lie groups]]  

$$
  U(1) \to U(n) \to PU(n)
$$ 

exhibiting the [[unitary group]] as a [[circle group]]-extension of the [[projective unitary group]] sits in a long [[homotopy fiber sequence]] of [[smooth ∞-groupoids]] of the form

$$
  U(1) \to U(n) \to PU(n) \to \mathbf{B}U(1)
  \to \mathbf{B}U(n) \to \mathbf{B}PU(n) \stackrel{\mathbf{dd}_n}{\to}
  \mathbf{B}^2 U(1)
  \,,
$$

where for $G$ a [[Lie group]] $\mathbf{B}G$ is its [[delooping]] [[Lie groupoid]], hence the [[moduli stack]] of $G$-[[principal bundles]], and where similarly $\mathbf{B}^2 U(1)$ is the [[moduli ∞-stack|moduli 2-stack]] of [[circle 2-group]] [[principal 2-bundles]] ([[bundle gerbes]]).

=--

+-- {: .num_prop}
###### Proposition

Here 

$$
  \mathbf{dd}_n \;\colon\; \mathbf{B} PU(n) \to \mathbf{B}^2 U(1)
$$

is a smooth refinement of the universal [[Dixmier-Douady class]]

$$
  dd_n \;\colon\; B PU(n) \to K(\mathbb{Z}, 3)
$$

in that under [[geometric realization of cohesive ∞-groupoids]] ${\vert- \vert} \colon$ [[Smooth∞Grpd]] $\to$ [[∞Grpd]] we have

$$
  {\vert \mathbf{dd}_n \vert}
  \simeq
  dd_n
  \,.
$$


=--

+-- {: .num_remark}
###### Remark

By the discussion at _[[∞-action]]_ the [[homotopy fiber sequence]] in prop. \ref{TheLongSequenceOfTheProjectiveUnitaryExtension}

$$
  \array{
    \mathbf{B} U(n)
    &\to&
    \mathbf{B} PU(n)
    \\
    && \downarrow
    \\
    && \mathbf{B}^2 U(1)
  }
$$

in $\mathbf{H}$
exhibits a smooth[[∞-action]] of the [[circle 2-group]] on the [[moduli stack]] $\mathbf{B}U(n)$ and it exhibits an equivalence

$$
  \mathbf{B} PU(n) \simeq (\mathbf{B}U(n))//(\mathbf{B} U(1))
$$

of the moduli stack of projective unitary bundles with the [[∞-quotient]] of this [[∞-action]].

=--

+-- {: .num_prop }
###### Proposition

For $X \in \mathbf{H}$ a [[smooth manifold]] and $\mathbf{c} \;\colon\; X \to \mathbf{B}^2 U(1)$ modulating a [[circle 2-group]]-[[principal 2-bundle]], maps

$$
  \mathbf{c} \to \mathbf{dd}_n
$$

in the [[slice (∞,1)-topos]] $\mathbf{H}_{/\mathbf{B}^2 U(1)}$, hence [[diagrams]] of the form

$$
  \array{
    X &&\stackrel{}{\to}&& \mathbf{B} PU(n)
    \\
    & {}_{\mathllap{\mathbf{c}}}\searrow 
    &\swArrow& 
    \swarrow_{\mathrlap{\mathbf{dd}_n}}
    \\
    && \mathbf{B}^2 U(1)
  }
$$

in $\mathbf{H}$ are equivalently rank-$n$ unitary [[twisted bundles]] on $X$, with the twist being the class $[\mathbf{c}] \in H^3(X, \mathbb{Z})$.

=--

+-- {: .num_prop #DifferentialRefinementOfSMoothDDClass}
###### Proposition

There is a further differential refinement

$$
  \array{
     (\mathbf{B}U(n))//(\mathbf{B}U(1))_{conn}
     &\stackrel{\widehat \mathbf{dd}_n}{\to}&
     \mathbf{B}^2 U(1)_{conn}
     \\
     \downarrow && \downarrow
     \\
     (\mathbf{B}U(n))//(\mathbf{B}U(1))
     &\stackrel{\widehat \mathbf{dd}_n}{\to}&
     \mathbf{B}^2 U(1)
  }
  \,,
$$

where $\mathbf{B}^2 U(1)_{conn}$ is the universal moduli 2-stack of [[circle n-bundle with connection|circle 2-bundles with connection]] ([[bundle gerbes]] with connection).

=--


+-- {: .num_defn}
###### Definition

Write

$$
  \left(
  \left(\mathbf{B}U\left(n\right)//\mathbf{B}U\left(1\right)\right)_{conn}
   \stackrel{\mathbf{Fields}}{\to} 
  \mathbf{B}^2 U\left(1\right)_{conn}
  \right)
  \;\;
  \in \mathbf{H}_{/\mathbf{B}^2 U(1)_{conn}}
$$

for the differential smooth universal Dixmier-Douady class of prop. \ref{DifferentialRefinementOfSMoothDDClass}, regarded as an object in the [[slice (∞,1)-topos]] over $\mathbf{B}^2 U(1)_{conn}$.

=--

+-- {: .num_defn}
###### Definition

Let 

$$
  \iota_X   
    \;\colon\;
  Q \hookrightarrow X 
$$

be an inclusion of [[smooth manifolds]] or of [[orbifolds]], to be thought of as a [[D-brane]] [[worldvolume]] $Q$ inside an ambient [[spacetime]] $X$.

Then a **field configuration** of a _[[B-field]]_ on $X$ together with a compatible rank-$n$ **Chan-Paton gauge field** on the [[D-brane]] is a map

$$
  \phi 
   \;\colon\;
  \iota_X \to \mathbf{Fields}
$$

in the [[arrow (∞,1)-topos]] $\mathbf{H}^{(\Delta^1)}$, hence a [[diagram]] in $\mathbf{H}$ of the form

$$
  \array{
    Q &\stackrel{\nabla_{gauge}}{\to}& (\mathbf{B}U(n)//\mathbf{B}U(1))
    \\
    {}^{\iota_X}\downarrow &\swArrow_{\simeq}& \downarrow^{\mathrlap{\hat \mathbf{dd}_n}}
    \\
    X &\stackrel{\nabla_B}{\to}& \mathbf{B}^2 U(1)_{conn}
  }
$$

=--

This identifies a  [[twisted bundle]] with connection on the D-brane whose twist is the class in $H^3(X, \mathbb{Z})$ of the bulk [[B-field]]. 

This relation is the Kapustin-part of the [[Freed-Witten-Kapustin anomaly]] cancellation for the [[bosonic string]] or else for the [[type II string]] on $Spin^c$ D-branes. ([FSS](#FSS))


+-- {: .num_remark }
###### Remark

If we regard the [[B-field]] as a [[background field]] for the [[Chan-Paton gauge field]], then remark \ref{PullbackAlongGeneralizedLocalDiffeomorphisms} determines along which maps of the B-field the Chan-Paton gauge field may be transformed. 

$$
  \array{
    Y &\stackrel{}{\to}& X &\stackrel{}{\to}& (\mathbf{B}U(n)//\mathbf{B}U(1))_{conn}
    \\
    & \searrow & \downarrow & \swarrow
    \\
    &&\mathbf{B}^2 U(1)_{conn}
  }
  \,.
$$

On the local connection forms this acts as

$$
  A \mapsto A + \alpha
  \,.
$$

$$
  B \mapsto B + d \alpha
$$

This is the famous gauge transformation law known from the string theory literature.

=--

##### The open string sigma-model
 {#TheOpenStringSigmaModel}

+-- {: .num_remark}
###### Remark

The [[D-brane]] inclusion $Q \stackrel{\iota_X}{\to} X$ is the [[target space]] for an [[open string]] with [[worldsheet]] $\partial \Sigma \stackrel{\iota_\Sigma}{\hookrightarrow} \Sigma$: a [[field (physics)|field]] configuration of the open string [[sigma-model]] is a map

$$
  \phi \;\colon\; \iota_\Sigma \to \iota_X
$$

in $\mathbf{H}^{\Delta^1}$, hence a [[diagram]] of the form

$$
  \array{
    \partial \Sigma &\stackrel{\phi_{bdr}}{\to}& Q
    \\
    \downarrow^{\mathrlap{\iota_\Sigma}} 
     &\swArrow& 
    \downarrow^{\mathrlap{\iota_X}}
    \\
    \Sigma &\stackrel{\phi_{bulk}}{\to}& X
  }
  \,.
$$

For $X$ and $Q$ ordinary [[manifolds]] just says that a field configuration is a map $\phi_{bulk} \;\colon\; \Sigma \to X$ subject to the constraint that it takes the [[boundary]] of $\Sigma$ to $Q$. This means that this is a [[trajectory]] of an [[open string]] in $X$ whose endpoints are constrained to sit on the [[D-brane]] $Q \hookrightarrow X$.

If however $X$ is more generally an [[orbifold]], then the [[homotopy]] filling the above diagram imposes this constraint only up to orbifold transformations, hence exhibits what in the physics literature are called "orbifold twisted sectors" of open string configurations.

=--

+-- {: .num_prop #TheTypeIIOpenStringSigmaModelModuliStackOfFields}
###### Proposition

The [[moduli stack]] $[\iota_\Sigma, \iota_X]$ of such field configurations is the [[homotopy pullback]] 

$$
  \array{
    [\iota_{\Sigma}, \iota_X]
    &\to&
    [\Sigma, X]
    \\
    \downarrow &\swArrow& \downarrow
    \\
    [S^1, Q]
    &\to&
    [S^1, X]
  }
  \,.
$$

=--

##### The anomaly-free open string coupling to the Chan-Paton gauge field
 {#TheAnomalyFreeOpenStringCouplingToTheChanPatonGaugeField}

+-- {: .num_prop }
###### Proposition

For $\Sigma$ a [[smooth manifold]] with [[boundary]] $\partial \Sigma$ of [[dimension]] $n$ and for $\nabla \;\colon \; X \to \mathbf{B}^n U(1)_{conn}$ a [[circle n-bundle with connection]] on some $X \in \mathbf{H}$, then the [[transgression]] of $\nabla$ to the [[mapping space]] $[\Sigma, X]$ yields a [[section]] of the [[complex line bundle]] [[associated bundle|associated]] to the pullback of the ordinary transgression over the mapping space out of the boundary: we have a diagram

$$  
  \array{  
    [\Sigma, X]
      &\stackrel{\exp(2 \pi i \int_{\Sigma})}{\to}& 
    \mathbb{C}//U(1)_{conn}
    \\
    \downarrow^{\mathrlap{[\partial \Sigma, X]}} 
    && 
    \downarrow^{\mathrlap{\overline{\rho}}_{conn}}
    \\
    [\partial \Sigma, X]
    &\stackrel{\exp(2 \pi i \int_{\partial \Sigma})}{\to}&
    \mathbf{B} U(1)_{conn}
  }
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

This is the _[[higher parallel transport]]_ of the $n$-connection $\nabla$ over maps $\Sigma \to X$.

=--


+-- {: .num_prop #TheTwistedHolonomyMapOnTwistedUnitaryBundles}
###### Proposition

The operation of forming the [[holonomy]] of a twisted unitary connection around a curve fits into a [[diagram]] in $\mathbf{H}$ of the form

$$
  \array{
    [S^1, (\mathbf{B}U(n))//(\mathbf{B}U(1))_{conn}]
    &\stackrel{hol_{S^1}}{\to}&
    \mathbb{C}//U(1)_{conn}
    \\
    \downarrow^{\mathrlap{[S^1, \widehat\mathbf{dd}_n]}} 
     &\swArrow_{\simeq}& 
    \downarrow^{\mathrlap{\overline{\rho}_{conn}}}
    \\
    [S^1, \mathbf{B}^2 U(1)_{conn}]
    &\stackrel{\exp(2 \pi i \int_{S^1})}{\to}&
    \mathbf{B}U(1)_{conn}
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

By the discussion at _[[∞-action]]_ the diagram in prop. \ref{TheTwistedHolonomyMapOnTwistedUnitaryBundles} says in particular that forming traced [[holonomy]] of twisted unitary bundles constitutes a [[section]] of the [[complex line bundle]] on the [[moduli stack]] of twisted unitary connection on the circle which is the [[associated bundle]] to the [[transgression]] $\exp(2 \pi i \int_{S^1} [S^1, \widehat\mathbf{dd}_n])$ of the universal differential [[Dixmier-Douady class]]. 

=--


It follows that on the moduli space of the open string [[sigma-model]] of prop. \ref{TheTypeIIOpenStringSigmaModelModuliStackOfFields} above there are two $\mathbb{C}//U(1)$-valued [[action functionals]] coming from the bulk field and the boundary field

$$
  \array{
    [\iota_{\Sigma}, \iota_X]
    &\to&
    [\Sigma, X]
    &\stackrel{exp(2 \pi i \int_{\Sigma}[\Sigma, \nabla_B]  ) }{\to}&
    \mathbb{C}//U(1)_{conn}
    \\
    \downarrow &\swArrow& \downarrow
    \\
    [S^1, Q]
    &\to&
    [S^1, X]
    \\
    \downarrow^{\mathrlap{hol_{S^1}([S^1, \nabla_{gauge}])}}
    \\
    \mathbb{C}//U(1)_{conn}
  }
  \,.
$$

Neither is a well-defined $\mathbb{C}$-valued function by itself. But by [[pasting]] the above diagrams, we see that both these constitute [[sections]] of the same [[complex line bundle]] on the moduli stack of fields:

$$
  \array{
    [\iota_{\Sigma}, \iota_X]
    &\to&
    [\Sigma, X]
    &\stackrel{[\Sigma, \nabla_B]}{\to}&
    [S^1, \mathbf{B}^2 U(1)_{conn}]
    &\stackrel{\exp(2 \pi i \int_{\Sigma})}{\to}&
    \mathbb{C}//U(1)_{conn}
    \\
    \downarrow &\swArrow& \downarrow
    && && \downarrow
    \\
    [S^1, Q]
    &\to&
    [S^1, X]
    \\
    \downarrow^{\mathrlap{[S^1, \nabla_{gauge}]}} &&  & \searrow^{\mathrlap{[S^1, \nabla_B]}}
    & && \downarrow
    \\
    [S^1, (\mathbf{B}U(n))//(\mathbf{B}U(1))_{conn}] & &\stackrel{[S^1, \widehat \mathbf{dd}_n]}{\to}& & [S^1, \mathbf{B}^2 U(1)_{conn}]
    \\
    \downarrow^{\mathrlap{hol_{S^1}}} 
      && && &  \searrow^{\mathrlap{\exp(2 \pi i \int_{S^1}(-))}}
    \\
    \mathbb{C}//U(1)_{conn} &\to& &\to& &\to&  \mathbf{B}U(1)_{conn}
  }
  \,.
$$

Therefore the product action functional is a well-defined function

$$
  [\iota_\Sigma, \iota_X]
  \stackrel{
    \exp(2 \pi i \int_{\Sigma} [\Sigma, \nabla_b] )
    \cdot
    hol_{S^1}( [S^1, \widehat {\mathbf{dd}}_n] )^{-1}
  }{\to}
  U(1)
  \,.
$$

This is the [[Freed-Witten-Kapustin anomaly|Kapustin anomaly]]-free [[action functional]] of the [[open string]].



#### 3d Chern-Simons theory with Wilson loops
 {#GaugeAndGravity3dCSWithWilson}
 {#ExtendedChern-SimonsTheoryAndWilsonLoops}

We discuss how an [[extended Lagrangian]] 
for $G$-[[Chern-Simons theory]] with [[Wilson loop]] [[QFT with defects|defects]] is naturally obtained from the [above](#FormulationInHigherGeometryDefinitions) [[higher geometry|higher geometric]] formulation of the orbit method. In particular we discuss how the relation between Wilson loops and [[1-dimensional Chern-Simons theory]] [[sigma-models]] with [[target space]] the [[coadjoint orbit]], as discussed  [above](#WilsonLoopsAnd1DCSSigmaModelWithTargetTheCoadjointOrbit) is naturally obtained this way.


More formally, we have an extended Chern-Simons theory as follows. 

The [[moduli stack]] of fields $\phi : C \to \mathbf{J}$ in $\mathbf{H}^{(\Delta^1)}$ as above is the [[homotopy pullback]]

$$
  \array{
    \mathbf{Fields}(S^1 \hookrightarrow \Sigma)
    &\stackrel{}{\to}&
    [S^1, \Omega^1(-,\mathfrak{g})//T]
    \\
    \downarrow &\swArrow_\simeq& \downarrow 
    \\
    [\Sigma, \mathbf{B}G_{conn}]
    &\to&
    [S^1, \mathbf{B}G_{conn}]
  }
$$

in $\mathbf{H}$, where square brackets indicate the [[internal hom]] in $\mathbf{H}$.

Postcomposing the two projections with the two [[transgressions]] of the [[extended Lagrangians]]

$$
  \exp(2 \pi i \int_\Sigma[\Sigma, \mathbf{c}]) 
  \;\colon\;
  [\Sigma, \mathbf{B}G_{conn}]
  \stackrel{[\Sigma, \mathbf{c}]}{\to}
  [\Sigma, \mathbf{B}^3 U(1)_{conn}]
  \stackrel{\exp(2 \pi i \int_\Sigma (-))}{\to}
  U(1)
$$

and

$$
  \exp(2 \pi i \int_\Sigma[S^1, \langle \lambda, -\rangle]) 
  \;\colon\;
  [S^1, \Omega^1(-,\mathfrak{g})//T]
  \stackrel{[\Sigma, \langle \lambda , -\rangle]}{\to}
  [S^1, \mathbf{B} U(1)_{conn}]
  \stackrel{\exp(2 \pi i \int_{S^1} (-))}{\to}
  U(1)
$$

to yield

$$
  \array{
    \mathbf{Fields}(S^1 \hookrightarrow \Sigma)
    &\stackrel{}{\to}&
    [S^1, \Omega^1(-,\mathfrak{g})//T]
    &\stackrel{\exp(2 \pi i \int_{S^1} [S^1, \langle \lambda, -\rangle] ) }{\to}&
    U(1)
    \\
    \downarrow &\swArrow_\simeq& \downarrow 
    \\
    [\Sigma, \mathbf{B}G_{conn}]
    &\to&
    [S^1, \mathbf{B}G_{conn}]
    \\
    \downarrow^{\mathrlap{\exp(2\pi i \int_{\Sigma_2} [\Sigma_3, \mathbf{c}])}}
    \\
    U(1)
  }
$$

and then forming the product yields the action functional

$$
  \exp(2 \pi i \int_{S^1}[S^1, \langle -\rangle])
   \cdot
  \exp(2 \pi i \int_{\Sigma}[\Sigma, \mathbf{c}])
  \;:\;
  \mathbf{Fields}(S^1 \hookrightarrow \Sigma)
  \to U(1)
  \,.
$$

This is the action functional of 3d $G$-[[Chern-Simons theory]] on $\Sigma$ with Wilson loop $C$ in the representation determined by $\lambda$.

Similarly, in [[codimension]] 1 let $\Sigma_2$ now be a 2-dimensional closed manifold, thought of as a slice of $\Sigma$ above, and let $\coprod_i {*} \to \Sigma_2$ be the inclusion of points, thought of as the punctures of the Wilson line above through this slice. Then we have [[prequantum bundles]] given by [[transgression]] of the extended Lagrangians to codimension 1

$$
  \exp\left(2 \pi i \int_{\Sigma_2}\left[\Sigma, \mathbf{c}\right]\right) 
  \;\colon\;
  \left[\Sigma_2, \mathbf{B}G_{conn}\right]
  \stackrel{\left[\Sigma_2, \mathbf{c}\right]}{\to}
  \left[\Sigma_2, \mathbf{B}^3 U(1)_{conn}\right]
  \stackrel{\exp\left(2 \pi i \int_{\Sigma_2} \left(-\right)\right)}{\to}
  \mathbf{B}U\left(1\right)_{conn}
$$

and

$$
  \exp\left(2 \pi i \int_{\coprod_i {*}}\left[\coprod_i {*}, \left\langle \lambda, -\right\rangle\right]\right) 
  \;\colon\;
  \left[\coprod_i {*}, \Omega^1\left(-,\mathfrak{g}\right)//T\right]
  \stackrel{[\coprod_i {*}, \langle \lambda , -\rangle]}{\to}
  \left[\coprod_i {*}, \mathbf{B} U(1)_{conn}\right]
  \stackrel{\exp\left(2 \pi i \int_{\coprod_i {*}} \left(-\right)\right)}{\to}
  \mathbf{B}U(1)_{conn}
$$

and hence a total prequantum bundle

$$
  \exp\left(2 \pi i \int_{\coprod_i {*}}\left[\coprod_i {*}, \langle \beta, -\rangle\right]\right)
   \otimes
  \exp\left(2 \pi i \int_{\Sigma_2}\left[\Sigma_2, \mathbf{c}\right]\right)
  \;:\;
  \mathbf{Fields}\left(\coprod_i {*} \hookrightarrow \Sigma\right)
  \to \mathbf{B}U\left(1\right)_{conn}
  \,.
$$

One checks that this is indeed the correct prequantization as considered in ([Witten 98, p. 22](#Witten)).





#### Chan-Paton gauge fields on D-branes
 {#GaugeAndGravityChanPatonGaugeFieldsOnDBranes}

### Syntactic Layer
 {#GaugeAndGravitySyntaxLayer}

(...)




## **Quantum mechanics**
 {#QuantumMechanics}

So far we have discussed [[extended prequantum field theory]]: [[Lagrangians]] and their induced [[action functionals]] and [[prequantum n-bundles]]. Now we turn to actual [[quantum field theory]]. A [[prequantum field theory]] is supposed to induce a [[quantum field theory]] under the last step of [[higher geometric quantization]]: a choice of [[polarization]] (or equivalent) and the passage to the corresponding [[space of states]] of polarized [[sections]] of the [[prequantum n-bundles]]. This step that connects [[prequantum field theory]] with [[quantum field theory]] we discuss below in _[Geometric Quantization](#GeometricQuantization)_.

Here we discuss the structure of the _outcome_ of this process 

* [[quantum mechanics]]

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

* [[motivic quantization]]


### Semantics Layer

* [[n-plectic smooth infinity-groupoid]]


### Syntactic Layer

(...)


## **Application to open questions in physics**
 {#ApplicationsToOpenQuestionsInPhysics}

What is it that [[higher geometry]], [[higher gauge theory]], [[extended TQFT|extended]]/local [[field theory]] and generally [[higher category theory and physics|higher category theory in physics]] contribute to open research questions in theoretical physics?

Often when this question is asked the most glaring open question of contemporary theoretical physics is forgotten: 

_What IS [[local quantum field theory]]?_ 

While something going by this name is clearly in use, it is just as clear that the full answer to this question is only being discovered these days, with formalizations such as the [[cobordism theorem]] and constructions such as [[factorization algebras]] in [[BV-quantization]] -- both of which are crucially constructions in [[higher geometry]]/[[higher category theory]].

Despite the huge success of quantum field theory, it it worthwhile to remember that all the fundamental open questions in present day fundamental physics quite likely require a deeper understanding of what quantum field theory actually is, notably non-perturbatively:

* Why is there [[confinement]]/[[chiral symmetry breaking]] in non-perturbative [[QCD]]/[[Yang-Mills theory]]? (The "mass gap problem".)

* What is beyond-the-standard-model physics?

* What is [[quantum gravity]]?

* What is non-perturbative [[string theory]]?

For instance the [[standard model of cosmology]] says that the bulk of all [[energy]] and [[matter]] in the [[observable universe]] is entirely unknown to us ([[dark matter]], "[[dark energy]]"), while at the same time the theoretical prediction what the [[cosmological constant]] [[vacuum energy]] should be is entirely off. How glaring an open question about the nature of quantum field theory this actually is is often forgotten due to the success of [[effective field theory]]-type of reasoning that allows to neatly wrap up all this unknown energy into a single term in some effective equation. Phenomenologically this may be regarded as a success, but for fundamental theoretical physics it is a glaring open question. 

And while there is work going in this direction, it may be worthwhile to recall how relatively primitive the available theoretical tools often still are. For instance it seems clear that "canonical non-covariant quantization" can hardly be an approrpiate tool to approach anything in the direction of [[quantum gravity]]. Even so fundamental a notion as that of _[[covariant phase space]]_ necessary to make progress here is not widely known in the theoretical physics community. Attempts to refine quantization to a "covariant" and "[[local quantum field theory|local]]" formalism via [[multisymplectic geometry]] have mainly got stuck, since local observables just do not form a sensible structure in ordinary [[Lie theory]]. This is resolved only in [[infinity-Lie theory]] and [[higher differential geometry]], as discussed above ([hgp 13](#hgp13), [lo 13](#LocalObservables13)).

If one assumes that [[string theory]] is part of the answer as to what underlies the [[standard model of particle physics]] [[standard model of cosmology|and cosmology]], then this situation becomes more drastic even. The fundamental [[field (physics)|fields]] of string theory are clearly objects in [[higher differential geometry]], such as the [[B-field]], the [[RR-field]], the [[supergravity C-field]] etc. For instance the natural identification of the latter as a [[homotopy fiber product]] of [[moduli stacks]] in ([FSS7dCS](#FSS7dCS), [FSSCField](#FSSCField)) is hardly conceivable when ignoring [[higher differential geometry]]. And this is a structure meant to be at the very heart of what makes up string theory. It is unlikely that the [[landscape of string theory vacua]] and hence the relation of string theory to [[phenomenology]] can really be understood if such basic higher-geometric phenomena of string theory are ignored (see [Distler-Freed-Moore 09](#http://ncatlab.org/schreiber/show/Mathematical+Foundations+of+Quantum+Field+and+Perturbative+String+Theory#ContributionDistlerFreedMoore) on this point).

(...)


## **References**
 {#References}

+-- {: bluebox }
###### 

1. [General](#ReferencesGeneral)

1. [Mathematical quantum field theory](#ReferencesMathematicalQFT)

1. [Topos theory in differential geometry and physics](#ReferencesToposTheory)

1. [Higher category theory in physics](#ReferencesHigherCategoryTheoryInPhysics)

1. [Local prequantum field theory](#ReferencesLocalPrequantumFieldTheory)

1. [Higher geometric prequantum theory](#ReferencesHigherGeometricPrequantumGeometry)

1. [Further details](#ReferencesFurtherDetails)

=--

### General 
 {#ReferencesGeneral}

A textbook with basic introductions to [[differential geometry]] and [[physics]] is

* [[Theodore Frankel]], _[[The Geometry of Physics - An Introduction]]_
 {#Frankel}

A discussion of aspects of quantum field theory with emphasis on the kind of modern tools that we are using here is in 

* [[Frédéric Paugam]], _Towards the mathematics of quantum field theory_ ([pdf](http://people.math.jussieu.fr/~fpaugam/documents/enseignement/master-mathematical-physics.pdf))
 {#Paugam}

The present discussion corresponds to section "1.2 Geometry of phyics" in 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_
 {#SchreiberCohesiveInfinityTopos}

which gives a more comprehensive account.

Another set of lecture notes along the above lines with an emphasis on aspects in [[gravity]] and [[higher gauge theory]] motivated from [[string theory]] is in 

* [[Urs Schreiber]], _[[twisted smooth cohomology in string theory]]_, Lectures notes at _Quantum Fields and twisted K-theory_, ESI (2012)
 {#TwistedCohomologyLecture}

An exposition and survey of matters related to [[Chern-Simons theory]] and [[higher geometric quantization]] is in 

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:A higher stacky perspective on Chern-Simons theory]]_
 {#FiorenzaSatiSchreiberCSIntroAndSurvey}

The syntactic perspective above is laid out further in

* [[Urs Schreiber]], _[[schreiber:Synthetic Quantum Field Theory]]_
 {#SyntheticQuantumFieldTheory}

see also at _[[motivic quantization]]_ the section _[General abstract type theoretic summary](motivic%20quantization#GeneralAbstractTypeTheoreticSummary)_.

### Mathematical quantum field theory
 {#ReferencesMathematicalQFT}

A textbook (really a collection of lecture notes) on [[quantum field theory]] and [[string theory]] that tries to present material in a conceptually clean way is

* [[Pierre Deligne]], [[Pavel Etingof]], [[Dan Freed]], L. Jeffrey, 
[[David Kazhdan]], [[John Morgan]], D.R. Morrison and [[Edward Witten]], eds.   _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))

A collection trying to summarize the state of the art of the formalization of [[QFT]] by [[FQFT]] and [[AQFT]] as of 2011 is 

* [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_, Proceedings of Symposia in Pure Mathematics, volume 83 AMS (2011)
 {#SatiSchreiber}

### Topos theory in differential geometry and physics
 {#ReferencesToposTheory}

One of the central figures of [[topos theory]] and [[categorical logic]], [[William Lawvere]], has motivated his interest in these subject always with intended application to the formalization of [[physics]] (of [[classical mechanics|classical]] [[continuum mechanics]] in his case). 

An influential text is

* [[William Lawvere]], _Toposes of laws of notion_, Toposes of laws of motion , transcript of a talk in Montreal, Sept. 1997 ([pdf](http://www.acsu.buffalo.edu/~wlawvere/ToposMotion.pdf))

which motivates [[synthetic differential geometry]] from [[differential equations]] appearing as [[equations of motion]] in physics. The early text

* [[William Lawvere]], _[[Some Thoughts on the Future of Category Theory]]_ in A. Carboni, M. Pedicchio, G. Rosolini, _Category Theory_  , [[Como|Proceedings of the International Conference held in Como]], Lecture Notes in Mathematics 1488, Springer (1991)

already sketches the formulation of [[cohesive toposes]] and motivates their axioms with heuristics from geometry and physics.

A review by Lawvere is in 

* [[William Lawvere]], _Comments on the Development of Topos Theory_, Development of Mathematics 1950-2000, 715-734 (2000) Birkh&#228;user Basel
 {#Lawvere2000}

Modern accounts of physics in this spirit includes notably also the book ([Paugam](#Paugam)) listed above.

### Higher category theory in physics
 {#ReferencesHigherCategoryTheoryInPhysics}

An early proposal that the [[action functional]] of $n$-dimensional [[quantum field theory]] should refine to a structure involving [[n-vector space|(n-k)-vector spaces]] in [[codimension]] $(n-k)$ is in

* [[Daniel Freed]], _[[Higher Algebraic Structures and Quantization]]_

The full formalization of this for [[extended topological field theory]] is due to 

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_

Related comments on the extended [[quantization]] of [[infinity-Dijkgraaf-Witten theory]] are in

* [[Daniel Freed]], [[Michael Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]] _[[Topological Quantum Field Theories from Compact Lie Groups ]]_

For more pointers see at _[[higher category theory and physics]]_.

### Local prequantum field theory
 {#ReferencesLocalPrequantumFieldTheory}

The idea of formulating local prequantum field theory by spans in a slice over a "space of phases" in [[higher geometry]] has been expressed in the unpublished note

* [[Urs Schreiber]], _[[schreiber:Nonabelian cocycles and their quantum symmetries]]_ (2008)

A formulation of the idea for [[Dijkgraaf-Witten theory]]-type field theories is indicated in section 3 of 

* [[Daniel Freed]], [[Michael Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], _[[Topological Quantum Field Theories from Compact Lie Groups]]_ (2010)
 {#FHLT}

based on the considerations in section 3.2 of 

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_ (2009).
 {#LurieTFT}

Based on the general formulation of the more general [[QFT with defects|field theory with defects]] described in section 4.3 there, in

* [[Domenico Fiorenza]], [[Alessandro Valentino]], _Boundary conditions in local TFTs_ (in preparation)
 {#FiorenzaValentino}

the structure of such [[domain walls]]/defects/[[branes]] are analyzed in the prequantum theory, hence with coefficients in an [[(∞,n)-category of spans]].

The study of local prequantum [[schreiber:∞-Chern-Simons theory]] with its codimension-1 [[schreiber:∞-Wess-Zumino-Witten theory]] and codimension 2-[[Wilson line]]-theory in this fashion, in an ambient [[cohesive (∞,1)-topos]] is discussed in ([lpqft](#lpqft))


Much of the content of this entry here are, or arose as, lecture notes for


* [[Urs Schreiber]], _[[schreiber:Higher Chern-Simons theory Introduction]]_, at the workshop _[Chern-Simons Theory: Geometry, Topology and Physics](http://www.pitt.edu/~jdeblois/CS.html)_ University of Pittsburgh (May 2013)
 {#SchreiberPittLectures}


### Higher geometric prequantum theory
 {#ReferencesHigherGeometricPrequantumGeometry}

* [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher geometric prequantum theory]]_
 {#hgp13} {#FiorenzaRogersSchreiber13a}

* [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:L-∞ algebras of local observables from higher prequantum bundles]]_
 {#LocalObservables13}

* [[Joost Nuiten]], [[Urs Schreiber]], _[[schreiber:Local prequantum field theory]]_
  {#lpqft}

* [[Joost Nuiten]], _[[schreiber:master thesis Nuiten|Cohomological quantization of local boundary prequantum field theory]]_, thesis 2013

### Further details
 {#ReferencesFurtherDetails}

#### Physical fields 
 {#ReferencesPhysicalFields}

For references on the tradtional formulation of [[physical fields]] by sections of _[[field bundles]]_ as discussed [above](#IdeaOfFieldBundlesAndItsProblems) see there references [[field bundle|there]].

The formulation of physical fields as [[cocycles]] in [[twisted cohomology]] in an [[(∞,1)-topos]] as in the _[Definition](#Definition)_-section above originates around

* [[Urs Schreiber]], _[[schreiber:Background fields in twisted differential nonabelian cohomology]]_, talk at _[[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology]]_

Further articles since then are listed at 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

In particular the general notion of fields as [[twisted differential c-structures]] appears in

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Twisted Differential String and Fivebrane Structures]]_ ([arXiv:0910.4001](http://arxiv.org/abs/0910.4001))
 {#SSS}

and the general theory of [[cohomology]] and [[twisted cohomology]] with [[local coefficient ∞-bundles]] as referred to in _[Relation to twisted cohomology](#RelationToTwistedCohomology)_ above as well as the theory of [[associated ∞-bundles]] as in _[Sections of associated ∞-bundles](#SectionsOfAssociatedBundles)_ is laid out in

* [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], _[[schreiber:Principal ∞-bundles -- theory, presentations and applications]]_ ([arXiv:1207.0248](http://arxiv.org/abs/1207.0248))

Some examples of fields in this sense are called "relative fields" in 

* [[Daniel Freed]], [[Constantin Teleman]], _Relative quantum field theory_ ([arXiv:1212.1692](http://arxiv.org/abs/1212.1692))
 {#FreedTeleman}


#### Differential forms and parallel transport
 {#DifferentialFormsAndParallelTransport}

The relation between differential 1-forms and smooth incremental path measures as used above is discussed in 

* [[Urs Schreiber]], [[Konrad Waldorf]], _Parallel transport and functors_, J. Homotopy Relat. Struct. 4, 187-244 ([arXiv:0705.0452](http://arxiv.org/abs/0705.0452))
 {#SchreiberWaldorf}

For a commented list of related literature see [here](http://ncatlab.org/schreiber/show/differential+cohomology+in+a+cohesive+topos+--+references#HistConnAsParTrans).

(...)

#### 3d Chern-Simons theory and Wilson loops

* [[Chris Beasley]], _Localization for Wilson Loops in Chern-Simons Theory_, in J. Andersen, H. Boden, A. Hahn, and B. Himpel (eds.) _Chern-Simons Gauge Theory: 20 Years After_, , AMS/IP Studies in Adv. Math., Vol. 50, AMS, Providence, RI, 2011. ([arXiv:0911.2687](http://arxiv.org/abs/0911.2687))
 {#Beasley}


#### Higher Chern-Simons theories

The discussion of the abelian [[7d Chern-Simons theory]] involved in [AdS7/CFT6 duality](AdS-CFT#AdS7CFT6) is due to ([Witten 98](#AdS-CFT#Witten98)). A discussion of the  non-abelian quantum-corrected and [[extended prequantum field theory|extended]] refinement is in

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:7d Chern-Simons theory and the 5-brane]]_
 {#FSS7dCS}

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The moduli 3-stack of the C-field]]_
 {#FSSCField}

Construction of differential cup-product theories is in 

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Extended higher cup-product Chern-Simons theories]]_
 {#FSSCup}

