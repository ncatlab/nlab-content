
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

A set of lecture notes on [[differential geometry]] and theoretical fundamental [[physics]], combining an introduction to traditional notions with an exposition of their formulation and refinement by [[higher geometry]] and [[extended prequantum field theory]]. With an eye towards [[Hilbert's sixth problem]] approached via [[cohesion]] ("[[schreiber:Synthetic Quantum Field Theory]]").

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

1. [Homotopy types](#HomotopyTypes)

1. [Smooth homotopy types](#SmoothnGroupoids)

1. [Groups](#NGroups)

1. [Principal bundles](#PrincipalBundles)

1. [Manifolds and Orbifolds](#Orbifolds)

1. [G-Structure and Cartan geometry](#ReductionOfStructureGroups)

1. [Representations and Associated bundles](#AssociatedNBundle)

1. [Modules](#Modules)

1. [Flat connections](#FlatConnections)

1. [de Rham coefficients](#deRhamCoefficients)

1. [Principal connections](#PrincipalConnections)

1. [Characteristic classes](#CharacteristicClasses)

1. [Integration](#Integration)

1. [Super-geometry](#SupergeometricCoordinateSystems)

**Part II) [Physics](#PHYSICS)**

1. [Physics in Higher Geometry: Motivation and Survey](#PhysicsMotivationAndSurvey)

1. [Fields](#Fields)

1. [Lagrangians and Action functionals](#LagrangiansAndActionFunctionals)

1. [Equations of motion](#EquationsOfMotion)

1. [Hamilton-Jacobi-Lagrange mechanics via prequantized Lagrangian correspondences](#ClassicalMechanicsByPrequantizedLagrangianCorrespondences)

1. [Hamilton-de Donder-Weyl field theory via Higher correspondences](#HDWFieldTheoryViaHigherCorrespondences)

1. [Local (topological) prequantum field theory](#LocalTopologicalPrequantumFieldTheory)

1. [Prequantum Gauge theory and Gravity](#ActionFunctionalsForChernSimonsTypeGaugeTheories)

1. [Quantum mechanics](#QuantumMechanics)

1. [Geometric quantization](#GeometricQuantization)

   1. [Geometric quantization with KU-coefficients](#GeometricQuantizationWithKUCoefficients)

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

* [[smooth function|smooth]] [[nonlinear functional|functionals]] -- called _[[action functionals]]_ 

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
| A flat connection $\nabla$ on $X$ is a rule for sending paths $(x \stackrel{\gamma}{\to} y) \in \Pi X$ to group elements, respecting composition. | $transport(\nabla) \colon \underset{x,y \colon \Pi X}{\sum} \left( x \rightsquigarrow y \right) \to \underset{*,*' \colon \mathbf{B}G}{\sum} (* \rightsquigarrow *')  $  |  $\frac{\Pi(X) \stackrel{transport(\nabla)}{\to} \mathbf{B}G}{X \stackrel{\nabla}{\to} \flat \mathbf{B}G}$.| The [[higher parallel transport]] $trans(\nabla)$ of a [[flat connection]] $\nabla$: a ([[higher gauge theory|higher]]) [[gauge field]] with vanishing [[field strength]]. | _[Flat connections](#FlatConnections)_ | 
| A closed differential form $\omega$ is a flat connection $\nabla$ and a trivialization of the underlying bundle. |  $\begin{aligned} & \flat_{dR} \mathbf{B} G  \coloneqq  \\ & \sum_{\nabla \colon \flat \mathbf{B}G} (UnderlyingBundle(\nabla) \simeq *) \end{aligned}$ | $\begin{matrix} \flat_{dR}\mathbf{B}G  & \stackrel{UnderlyingConnection}{\begin{svg} [[!include SVG rightarrow]]\end{svg}}& \flat \mathbf{B}G \\ \begin{svg}[[!include SVG downarrow]]\end{svg} & \mathclap{\array{\arrayopts{\align{bottom}}\;\begin{svg}[[!include SVG pullback]]\end{svg} & \space{10}{0}{30} \\ \space{10}{30}{1} & \swArrow}} & \begin{svg}[[!include SVG downarrow]]\end{svg}{}^{\mathrlap{Underlying \atop Bundle}} \\ * &\stackrel{}{\begin{svg}[[!include SVG rightarrow]]\end{svg}}& \mathbf{B}G \end{matrix}$  | The [[coefficients]] for [[de Rham cohomology|de Rham]] [[hypercohomology]] -- flat [[∞-Lie algebra valued differential forms]]. | _[de Rham coefficients](#deRhamCoefficients)_ |
| A general connection $\nabla$ is the equivalence between the curvature $curv(\mathbf{c})$ of a bundle $\mathbf{c}$ and a closed differential form $\omega$. | $\nabla \colon \underset{{\mathbf{c} \colon \mathbf{B}^n \mathbb{G}} \atop { \omega \colon \Omega^{n+1}_{cl} }}\sum \left( curv\left(\mathbf{c}\right) = \omega\right) $ | $ \begin{matrix} \mathbf{B}^n \mathbb{G}_{conn}  & \stackrel{F_{(-)}}{\begin{svg} [[!include SVG rightarrow]]\end{svg}}& \Omega^{n+1}_{cl} \\ \begin{svg}[[!include SVG downarrow]]\end{svg} & \mathclap{\array{\arrayopts{\align{bottom}}\;\begin{svg}[[!include SVG pullback]]\end{svg} & \space{10}{0}{30} \\ \space{10}{30}{1} & \swArrow}} & \begin{svg}[[!include SVG downarrow]]\end{svg} \\ \mathbf{B}^n \mathbb{G} &\stackrel{curv}{\begin{svg}[[!include SVG rightarrow]]\end{svg}}& \flat_{dR} \mathbf{B}^{n+1}\mathbb{G} \end{matrix} $  | The [[coefficients]] for smooth [[differential cohomology]]: abelian ([[higher gauge theory|higher]]) [[gauge fields]]. | _[Circle principal n-connections](CirclePrincipalConnections)_ |
| There is a cohesive function from $G$-gauge fields to higher $\mathbb{G}$-gauge fields. | $\vdash \; \exp(i S) \colon \mathbf{B}G_{conn} \to \mathbf{B}^n \mathbb{G}_{conn}$ | A [[differential cohomology|differential]] [[universal characteristic class]]. | An extended [[action functional]]/[[prequantum circle n-bundle|prequantum n-bundle]] for extended [[schreiber:infinity-Chern-Simons theory|higher Chern-Simons-type]] [[gauge theory]].   |  |


... and their _[[schreiber:∞-geometric prequantization]]_ (see there for a more comprehensive dictionary):

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

1. [Homotopy types](#HomotopyTypes)

1. [Smooth homotopy types](#SmoothnGroupoids)

1. [Groups](#NGroups)

1. [Principal bundles](#PrincipalBundles)

1. [Manifolds and Orbifolds](#Orbifolds)

1. [G-Structure and Cartan geometry](#ReductionOfStructureGroups)

1. [Representations and Associated bundles](#AssociatedNBundle)

1. [Flat connections](#FlatConnections)

1. [de Rham coefficients](#deRhamCoefficients)

1. [Principal connections](#PrincipalConnections)

1. [Characteristic classes](#CharacteristicClasses)

1. [Integration](#Integration)


1. [Super-geometry](#SupergeometricCoordinateSystems)

=--


## **Coordinate systems**
 {#CoordinateSystems}

This chapter is at _[[geometry of physics -- coordinate systems]]_


## **Smooth spaces**
 {#SmoothSpaces}

This chapter is at _[[geometry of physics -- smooth spaces]]_.


## **Differential forms**
 {#DifferentialForms}


This chapter is at _[[geometry of physics -- differential forms]]_.

## **Differentiation**
 {#Differentiation}

This chapter is at _[[geometry of physics -- differentiation]]_.

## **Homotopy types**
 {#HomotopyTypes}

This chapter is at _[[geometry of physics -- homotopy types]]_.

## **Smooth homotopy types**
 {#SmoothnGroupoids}
 {#SmoothGroupoids}


This chapter is at _[[geometry of physics -- smooth homotopy types]]_.


## **Groups**
 {#NGroups}
 {#Groups}

This chapter is at _[[geometry of physics -- groups]]_.

## **Principal bundles**
 {#PrincipalBundles}
 {#PrincipalNBundles}


This chapter is at _[[geometry of physics -- principal bundles]]_.


## **Manifolds and Orbifolds**
 {#Orbifolds}

this chapter is at _[[geometry of physics -- manifolds and orbifolds]]_

## **$G$-Structure and Cartan geometry**
 {#ReductionOfStructureGroups}

this chapter is at _[[geometry of physics -- G-structure and Cartan geometry]]_


## **Representations and Associated bundles**
 {#AssociatedNBundle}


this chapter is at _[[geometry of physics -- representations and associated bundles]]_

## **Modules**
 {#Modules}

this chapter is at _[[geometry of physics - modules]]_


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

Since $\Pi(X)$ is the [[fundamental infinity-groupoid]] of $X$, this manifestly encodes the [[higher parallel transport]] of the flat connection.

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

see _[[geometry of physics -- de Rham coefficients]]_

## **Principal connections**
 {#PrincipalConnections}

this chapter is at _[[geometry of physics -- principal connections]]_


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

this chapter is at _[[geometry of physics -- supergeometry]]_


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

This chapter is at _[[geometry of physics -- physics in higher geometry]]_.


## **Fields**
 {#Fields}

This chapter is at _[[fields (physics)]]_.


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

## **Hamilton-Jacobi-Lagrange mechanics via prequantized Lagrangian correspondences**
 {#ClassicalMechanicsByPrequantizedLagrangianCorrespondences}

This chapter is at _[[prequantized Lagrangian correspondence]]_.

## **Hamilton-de Donder-Weyl field theory via Higher correspondences**
 {#HDWFieldTheoryViaHigherCorrespondences}

This chapter is at _[[Local field theory via Higher correspondences]]_.



## **Local (topological) prequantum field theory**
 {#LocalTopologicalPrequantumFieldTheory}

This chapter is at _[[geometry of physics -- local prequantum field theory]]_.

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

This section is at _[[geometry of physics -- quantum mechanics]]_

## **Geometric quantization**
 {#GeometricQuantization}

### Model Layer

#### 1-Geometric quantization

* [[geometric quantization]]

#### Geometric quantization with KU-coefficients
 {#GeometricQuantizationWithKUCoefficients}

this is at _[[geometric quantization with KU-coefficients]]_

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

* {#Frankel} [[Theodore Frankel]], _[[The Geometry of Physics - An Introduction]]_
 

A discussion of aspects of quantum field theory with emphasis on the kind of modern tools that we are using here is in 

* {#Paugam} [[Frédéric Paugam]], _Towards the mathematics of quantum field theory_ ([pdf](http://people.math.jussieu.fr/~fpaugam/documents/enseignement/master-mathematical-physics.pdf))
 

The present discussion corresponds to section "1.2 Geometry of phyics" in 

* {#SchreiberCohesiveInfinityTopos} [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_
 

which gives a more comprehensive account.

Another set of lecture notes along the above lines with an emphasis on aspects in [[gravity]] and [[higher gauge theory]] motivated from [[string theory]] is in 

* {#TwistedCohomologyLecture} [[Urs Schreiber]], _[[twisted smooth cohomology in string theory]]_, Lectures notes at _Quantum Fields and twisted K-theory_, ESI (2012)
 

An exposition and survey of matters related to [[Chern-Simons theory]] and [[higher geometric quantization]] is in 

* {#FiorenzaSatiSchreiberCSIntroAndSurvey} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:A higher stacky perspective on Chern-Simons theory]]_
 

The syntactic perspective above is laid out further in

* {#SyntheticQuantumFieldTheory} [[Urs Schreiber]], _[[schreiber:Synthetic Quantum Field Theory]]_
 

see also at _[[motivic quantization]]_ the section _[General abstract type theoretic summary](motivic%20quantization#GeneralAbstractTypeTheoreticSummary)_.

### {#ReferencesMathematicalQFT} Mathematical quantum field theory
 

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