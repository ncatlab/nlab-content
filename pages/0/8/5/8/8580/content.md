
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

A set of lecture notes on [[differential geometry]] and theoretical fundamental [[physics]], combining an introduction to traditional notions with an exposition of their formulation and refinement by [[higher geometry]] and [[extended prequantum field theory]]. With an eye towards [[Hilbert's sixth problem]] approached via [[cohesion]].

Divided into two parts:

* **Part I) [Geometry](#GEOMETRY)**

* **Part II) [Physics](#PHYSICS)**

***

$\,$


The [[nLab:geometry of physics|geometry of fundamental physics]] is _[[nLab:higher differential geometry|higher differential]] [[nLab:supergeometry]]_.

| $\phantom{AA}$ [[nLab:physics]] $\phantom{AA}$ | $\phantom{AA}$ [[nLab:mathematics]] $\phantom{AA}$ |
|---------|--------------|
| $\phantom{AA}$ [[nLab:gauge principle]] $\phantom{AA}$ | $\phantom{AA}$ [[nLab:higher geometry]] $\phantom{AA}$<br/> $\phantom{AA}$ ([[nLab:(infinity,1)-topos theory|geometric homotopy theory]]) $\phantom{AA}$ |
| $\phantom{AA}$ [[nLab:Pauli exclusion principle]] $\phantom{AA}$ | $\phantom{AA}$ [[nLab:supergeometry]] $\phantom{AA}$ |
{: style='margin:auto}


Here:


1. **[[nLab:supergeometry|Supergeometry]]** is [[nLab:geometry]] whose [[nLab:spaces]] may have [[nLab:algebras of functions]] that are $\mathbb{Z}_2$-[[nLab:graded-commutative algebras]]. This is the mathematical reflection of the [[nLab:Pauli exclusion principle]], which says that a [[nLab:fermionic]] [[nLab:wave function]] $\Psi$ on a [[nLab:phase space]] of a [[nLab:physical system]] with [[nLab:fermions]] has to have vanishing square. By linearity this implies that

   $$
     \begin{aligned}
       0 & = (\Psi_1 + \Psi_2)^2 
       \\
       & =
       \underset{ = 0}{\underbrace{ (\Psi_1)^2 }}  
       +
       \underset{ = 0}{\underbrace{ \Psi_1 \Psi_2 + \Psi_2 \Psi_1 }}
       +
       \underset{ = 0}{\underbrace{ (\Psi_2)^2 }}
     \end{aligned}
   $$

   and hence that fermionic [[nLab:wave functions]] _[[nLab:graded commutative algebra|anti-commute]]_, and hence are the odd-graded elements in a _[[nLab:commutative superalgebra]]_ (a _slightly_ [[nLab:noncommutative algebra]]!)

   Ever since the existence of [[nLab:fermions|fermionic]] [[nLab:particles]] was [[nLab:experiment|experimentally]] established, around the time of the [[nLab:Stern-Gerlach experiment]] in the 1920s, it is thus an [[nlab:experiment|experimental]] fact that fundamental physics is described by _[[nLab:supergeometry]]_. (This is _not_ necessarily [[nLab:supersymmetry|super]]-<em>[[nLab:supersymmetry|symmetric]]</em>, though of course there is a [close relation](geometry+of+physics+--+supersymmetry#SupersymmetryFromTheSuperpoint).)


1. **[Higher structures](https://ncatlab.org/schreiber/show/Higher+Structures)** is short for _higher [[nLab:homotopy theory|homotopy theoretic]]_ [[nLab:structures]] and reflects the [[nLab:gauge principle]] of [[nLab:physics]]: This says that, generally, it does not make invariant sense to ask if any two things $x$, $y$ (e.g. [[nLab:field histories]]) are [[nLab:equality|equal]], instead one must ask for a _[[nLab:gauge transformation]]_ between them, mathematically a _[[nLab:homotopy]]_:

   $$
     x \stackrel{\gamma}{\longrightarrow} y
   $$
   
   This principle applies also to [[nLab:gauge transformations]] themselves, and thus leads to [[nLab:gauge-of-gauge transformations]] 

   <center><img src="https://ncatlab.org/nlab/files/2Cell.jpg" width = "200"></center>

   and so on to ever [[nLab:higher gauge transformations]]:

   <center><img src="https://ncatlab.org/nlab/files/3Cell.jpg" width = "200"></center>

   mathematically reflected by [[nLab:higher homotopies]] in _[[nLab:homotopy types|higher homotopy types]]_.

   Ever since the existence of [[nLab:gauge fields]] was understood in the 1920s, it is thus an [[nlab:experiment|experimental]] fact that fundamental physics is described by _[[nLab:higher geometry]]_. 


A striking consequence is that, both in [[nLab:higher geometry]] as well as in [[nLab:supergeometry]] and therefore in the [[nLab:geometry of physics|geometry of fundamental physics]], [[nLab:spaces]] generally are _not_ [[nLab:sets]] of [[nLab:points]], as in the traditional definition of [[nLab:topological spaces]] or [[nLab:differentiable manifolds]].

What, then, _is_ the [[nLab:geometry of physics|geometry of fundamental physics]]?

The right framework to answer questions like this has been _urged_ by [[nLab:Alexander Grothendieck]] already in [Grothendieck 73](functorial+geometry#Grothendieck73) (see [Lawvere 03](functorial+geometry#Lawvere16Quote)) and has been much expanded on by [[nLab:William Lawvere]] (e.g. [[nLab:Toposes of laws of motion|Lawvere 97]], [[nLab:Some Thoughts on the Future of Category Theory|Lawvere 91]]) and has an evident lift to [[nLab:higher geometry]] ([[nLab:Structured Spaces|Lurie 09]], [S. 13](https://ncatlab.org/schreiber/show/differential+cohomology+in+a+cohesive+topos)), but has remained somewhat of a "public secret": 

The answer is known, alternatively, as ([[nLab:higher geometry|higher]]) _[[nLab:functorial geometry]]_ (Grothendieck) or _[[nLab:synthetic differential geometry]] in [[nLab:gros toposes]]_ (Lawvere), or variants thereof.

In this lecture series we try to give a self-contained introduction to [[nLab:higher differential geometry|higher differential]] [[nLab:supergeometry]] this way, following [[schreiber:differential cohomology in a cohesive topos|Schreiber 13]]. We begin at the beginning, with introducing relevant basics of [[nLab:category theory]] and [[nLab:topos theory]] and will provide brief indication of real-world applications to [[nLab:perturbative quantum field theory]] and [[nLab:fundamental super p-branes]].

The [[nLab:higher differential geometry]] which we lay out subsumes various special cases that are discussed separately in the literature:

[[!include geometries of physics -- table]]

Notably [[diffeological spaces]] find home and company here:  We explain how these are equivalently the _[[nLab:concrete objects]]_ among the the [[nLab:bosonic]] [[nLab:smooth set|smooth]] [[nLab:h-sets]]:

$$
  \array{
    \big\{  
      \text{diffeological spaces}  
    \big\}
    \\
    \;\simeq\;
    \\
    \big\{
      \text{concrete bosonic smooth h-sets}  
    \big\}
  }
  \,.
$$

and we discuss how, even if one is initially interested only in ordinary [[nLab:smooth manifolds]] or only in [[nLab:diffeological spaces]], it is useful to work with more general [[nLab:super differential homotopy types]].

<center>
<img src="https://www.ncatlab.org/schreiber/files/GeometriesWithDiffeological.jpg" width="760">
</center>

> graphics taken from _[Higher Prequantum Geometry](https://ncatlab.org/schreiber/show/Higher+Prequantum+Geometry)_

$\,$



$\,$



***



+-- {: bluebox}
###### Table ######
**of chapters**

* [About this text](#AboutThisPage)

* [References](#References)

**Preliminaries**

1. [Categories and Toposes](#CategoriesAndToposes)

**Part I) [Geometry](#GEOMETRY)**

1. [Smooth sets](#SmoothSpaces)

1. [Homotopy types](#HomotopyTypes)

1. [Smooth homotopy types](#SmoothnGroupoids)

1. [Stable homotopy types](#StableHomotopyTypes)

1. [Groups](#NGroups)

1. [Principal bundles](#PrincipalBundles)

1. [Manifolds and Orbifolds](#Orbifolds)

1. [G-Structure and Cartan geometry](#ReductionOfStructureGroups)

1. [Representations and Associated bundles](#AssociatedNBundle)

1. [Modules](#Modules)

1. [Flat connections](#FlatConnections)

1. [de Rham coefficients](#deRhamCoefficients)

1. [Principal connections](#PrincipalConnections)

1. [Integration](#Integration)

1. [Super-geometry](#SupergeometricCoordinateSystems)

**Transition to part II**

1. [Prequantum geometry](#PrequantumGeometry)

1. [WZW terms](#WZWTerms)

1. [BPS charges](#BPSCharges)

**Part II) [Physics](#PHYSICS)**

1. [Perturbative quantum field theory](#AFirstIdeaOfQuantumFieldTheory)

1. [Physics in Higher Geometry: Motivation and Survey](#PhysicsMotivationAndSurvey)

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

Notably, where traditional expositions of [[differential geometry]] proceed by generalizing the [[geometry]] of abstract [[coordinate|coordinate systems]] $\mathbb{R}^n$ to _[[smooth manifolds]]_, here we instead begin by generalizing, in _[Smooth sets -- Model Layer](SmoothSpacesLayerMod)_, coordinate systems right away to _[[smooth sets]]_, which happens to be both more expressive as well as actually much easier. In parallel (and to be read independently or not at all) we discuss in _[Smooth sets -- Semantic Layer](#SmoothSpacesLayerSem)_ how this means that we are working in the _[[sheaf topos]]_ over abstract coordinate systems.  Smooth manifolds are then introduced later as an intermediate notion, together with that of _[[diffeological spaces]]_. (Many of the constructions in [[differential geometry]] applied in [[physics]] do not actually need the notion of a smooth manifold, and, more importantly, for many notions in modern theoretical physics smooth manifolds are not actually sufficiently general.) 

In fact we introduce smooth manifolds only after we introduce _[[smooth groupoids]]_ (below in _[Smooth homotopy type - Model Layer - Smooth groupoids](#SmoothGroupoids))_, which are differential geometric structures that are _still_ simpler than smooth manifolds, and of course even more expressive than smooth sets. Moreover, smooth groupoids are at the very heart of the geometry of physics: modern fundamental physics is all based on the "[[gauge symmetry|gauge principle]]" and in  _[Model Layer -- Gauge transformations in electromagnetism](#GaugeTransformationsInElectromagnetism)_ we explain how, mathematically, this is essentially nothing but the theory of smooth groupoids. As further background information we discuss in _[Smooth homotopy types - Semantic Layer](#SmoothHomotopyTypesSemanticLayer)_ how this means that we are working in a [[(infinity,1)-topos|higher topos]] over abstract coordinate systems, and in _[Smooth homotopy type - Syntactic Layer](#SmoothHomotopyTypesSyntacticLayer)_ how this means that we are reasoning about physics using the _[[natural deduction]]_ rules of _[[homotopy type theory]]_.

From this setup then naturally flow all the many structures and phenomena seen in the geometry of physics:




### Layers of exposition
 {#Layers}

We discuss each topic below in three stages, in three _layers_. 

1. The first layer, called the **Model Layer **, deals with concrete explicit  constructions as familiar from traditional textbooks on differential geometry and physics. This layer is supposed to be readable and useful all in itself and the reader who feels that this is all he or she wants to see can stick to this and ignore the other layers. In particular, while the _Model Layer_ does invoke the basic notion of a _[[category]]_ and of a _[[functor]]_ -- which are as simple as the notions of [[group]] or [[associative algebra|algebra]] --, it does not use any actual _[[category theory]]_. 
 {#LayerMod}

1. The second layer, called the **Semantic Layer**, makes explicit the ([[(infinity,1)-category theory|higher]]) [[category theory]] and ([[(infinity,1)-topos theory|higher]]) [[topos theory]] at work in the background. This puts the concrete constructions of the _Model Layer_ into a more general context and helps to see certain organizational patterns that underlie the seemingly different phenomena. It provides some powerful theorems which the _Model Layer_ is secretly benefitting from. For instance this layer gives a systematic rule for generalizing everything at the beginning Model Layers from ordinary [[differential geometry]] to what is called  _[[supergeometry]]_, which is the context in which [[fermion|fermionic]] [[particles]] are formalized: the [[matter]] constituents of the [[observable universe]].
 {#LayerSem}

1. The third layer, called the **Syntactic Layer**, makes explicit the expression of these phenomena in the [[logical framework|formal]] [[internal language]] of the [[topos]] of [[smooth sets]] -- which is _[[dependent type theory|dependent]] [[type theory]]_ -- and of the [[(infinity,1)-topos|higher topos]] of [[smooth infinity-groupoid|smooth higher groupoids]] -- which is _[[homotopy type theory]]_. This makes more transparent various constructions in ([[(infinity,1)-topos theory|higher]]) [[topos theory]] used in _Semantic Layer_, and in fact it provides 
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
Finally, the fourth columns indicate what this universal construction amounts to when concretely realized in the [[model]] given by [[smooth sets]] and [[smooth ∞-groupoids]]. Finally the rightmost columns point to the chapters in the text below that deal with the given construction.

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
| There is... | $\vdash \ldots$ | (We speak in the context of a ([[(∞,1)-topos|higher]]) [[topos]] $\mathbf{H}$, a _place where things may be_. (For the time being a ([[locally cartesian closed (infinity,1)-category|higher]]) [[locally cartesian closed category]] is sufficient.)) | (A [[topos]] for [[synthetic differential geometry|synthetic]] [[differential geometry]], such as $\mathbf{H} = $ [[sheaf topos|Sh]]$($[[SmthMfd]]$)$. Eventually a [[(∞,1)-topos|higher]] such topos: $\mathbf{H} = $ [[Smooth∞Grpd]] or [[SynthDiff∞Grpd]] or [[SmoothSuper∞Grpd]] or ...) | _[Smooth sets](#SmoothSpaces)_ and _[Smooth homotopy types](#SmoothnGroupoids)_  |
| There is a thing $x$ of type $X$. | $\vdash\; x \colon X$ | An [[element]] $\left(* \stackrel{x}{\to} X\right) \in Mor(\mathbf{H})$ of an [[object]] $X$ of $\mathbf{H}$. | A point $x$ in a [[smooth infinity-groupoid|smooth moduli stack]] $X$. | _[Judgements about types and terms](#Judgments)_ |
| There is a type $X$ of things $x$. | $\vdash\; X \colon Type$ | An [[element]] $(* \stackrel{\vdash X}{\to} Obj) \in Mor(\mathbf{H})$ of the [[small object|small]]-[[object classifier]] $Obj$ of $\mathbf{H}$. | A point in the _[[moduli stack]] of all [[small object|small]] moduli stacks_. | _[Judgements about types and terms](#Judgments)_  |
| Given a thing $x$ of type $X$ there is a thing $a(x)$ of type $A(x).$ | $x \colon X\;\vdash\; a(x) \colon A(x)$ | An [[element]] of a morphism $(A \to X)$ $\left(\array{ X &&\stackrel{a}{\to}&& A \\ & {}_{\mathllap{id}}\searrow &\swArrow& \swarrow_{} \\ && X }\right)$ in the [[slice (infinity,1)-topos|slice topos]] $\mathbf{H}_{/X}$. | An $X$-family  in a moduli stack [[bundle]] $A$ over $X$. | _[Slice categories](#SliceCategories)_ and _[Slice toposes](#SliceToposes)_ and _[Slice ∞-Toposes](#SlicedInfinityToposes)_ |
|  There is the collection of all things $a(x)$ for all $x$. | $\vdash\; \left(\sum_{x \colon X} A\left(x\right)\right) \colon Type$ | The [[dependent sum]]/[[left adjoint]] to the [[product]]: $\array{ \mathbf{H}_{/X} &\stackrel{X_!}{\to} & \mathbf{H} \\ (A \to X) &\mapsto& A \in \mathbf{H}} $ | The total space of a [[bundle]]. | _[Natural deduction rules for dependent sum types](#DependentSumTypes)_ |
| There is a thing $t$ in the collection of all things $a(x)$ for all $x$. | $\vdash\; t \colon \sum_{x \colon X} A(x)$ |  An element $*\stackrel{t}{\to} A$ of the total space object. | A point in the [[moduli stack]] $A$ over $X$. | |  
| There is an assignment $f$ of an $a(x)$ to each $x$. | $\vdash \; f \colon \prod_{x \colon X} A(x)$. | An [[element]] in the [[internal hom|internal]] [[object]] of [[sections]] $* \stackrel{f}{\to} [X,A]_X$  | A [[point]] in the smooth relative [[mapping space]] of smooth [[sections]].  | _[Natural deduction rules for dependent product types](#NaturalDeductionForDependentProduct)_ |   
| There is the collection of assignments of an $a(x)$ to each $x$. | $\vdash\; \left( \prod_{x \colon X} A\left(x\right) \right) \colon Type$ | [[internal hom|internal]] space of [[sections]] $[X,A]_X \in \mathbf{H}$ | A smooth relative [[mapping space]] of smooth [[sections]]. |  |
| In particular, there is the collection of such assignments when $A$ does not depend on $x$, the collection of _functions_ from $X$ to $A$. |  $\vdash \; \left(X \to A\right) \coloneqq \left(\prod_{x \colon X} A\right) \colon Type$ | The [[internal hom]] [[object]] $[X,A] \in \mathbf{H}$.  | A smooth [[mapping space]]. |  _[Smooth mapping spaces and smooth moduli spaces](#SmoothMappingSpaces)_ |
| There is a proof $p$ that it is true that there is $x$ of type $X$. | $ \vdash \;  p \colon [X] $ | An [[element]]  $* \stackrel{p}{\to}\tau_{-1}(X)$ of the [[truncated object of an (infinity,1)-topos|(-1)-truncation]] of the object $X$. | A point in the [[smooth sets]] of [[equivalence classes]] of points in $X$. | _[Subobjects](#Subobjects)_ |
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
| Given $x,x'$, there is the collection of proofs that it is true that $x$ and $x'$ are equivalent. | $x,x' \colon X \;\vdash \; [x \simeq x'] \colon Type$. | The [[truncated object of an (infinity,1)-topos|(-1)-truncation]] fo the [[mapping cocone]]. | The [[smooth set]] of [[equivalence classes]] of [[gauge transformations]] from $x$ to $x'$. | |

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

We begin by laying the foundations of [[differential geometry]]. Doing this in the natural abstract way seamlessly leads over to the foundations of [[higher differential geometry]] (see also _[[motivation for higher differential geometry]]_). Once this is set up, we discuss the fundamental constructions: [[groups]], [[actions]]/[[representations]], [[fiber bundles]], [[connection on a bundle|connections]], [[Chern-Weil theory]].


1. [Smooth sets](#SmoothSpaces)

1. [Homotopy types](#HomotopyTypes)

1. [Smooth homotopy types](#SmoothnGroupoids)

1. [Stable homotopy types](#StableHomotopyTypes)

1. [Groups](#NGroups)

1. [Principal bundles](#PrincipalBundles)

1. [Manifolds and Orbifolds](#Orbifolds)

1. [G-Structure and Cartan geometry](#ReductionOfStructureGroups)

1. [Representations and Associated bundles](#AssociatedNBundle)

1. [Flat connections](#FlatConnections)

1. [de Rham coefficients](#deRhamCoefficients)

1. [Principal connections](#PrincipalConnections)

1. [Integration](#Integration)

1. [Super-geometry](#SupergeometricCoordinateSystems)

1. [Prequantum geometry](#PrequantumGeometry)

1. [WZW terms](#WZWTerms)

1. [BPS charges](#BPSCharges)

=--

## **Categories and Toposes**
 {#CategoriesAndToposes}

This chapter is as _[[geometry of physics -- Categories and Toposes]]_


## **Smooth set**
 {#SmoothSpaces}

This chapter is at _[[geometry of physics -- smooth sets]]_.

## **Homotopy types**
 {#HomotopyTypes}

This chapter is at _[[geometry of physics -- homotopy types]]_.

## **Smooth homotopy types**
 {#SmoothnGroupoids}
 {#SmoothGroupoids}


This chapter is at _[[geometry of physics -- smooth homotopy types]]_.


## **Stable homotopy types**
 {#StableHomotopyTypes}

This chapter is at _[[geometry of physics -- stable homotopy types]]_.

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

this chapter is at _[[geometry of physics -- flat connections]]_


## **de Rham Coefficients**
 {#deRhamCoefficients}

see _[[geometry of physics -- de Rham coefficients]]_

## **Principal connections**
 {#PrincipalConnections}

this chapter is at _[[geometry of physics -- principal connections]]_



## **Integration**
 {#Integration}


this chapter is at _[[geometry of physics -- integration]]_

## **Super-geometry**
 {#SupergeometricCoordinateSystems}

this chapter is at _[[geometry of physics -- supergeometry and superphysics]]_

## **Prequantum geometry**
 {#PrequantumGeometry}

this chapter is at _[[geometry of physics -- prequantum geometry]]_

## **WZW terms**
 {#WZWTerms}

this chapter is at _[[geometry of physics -- WZW terms]]_

## **BPS charges**
 {#BPSCharges}

this chapter is at _[[geometry of physics -- BPS charges]]_

+-- {: bluebox #PHYSICS}
###### Contents

**II) Physics**

1. [Perturbative quantum field theory](#AFirstIdeaOfQuantumFieldTheory)

1. [Physics in Higher Geometry: Motivation and Survey](#PhysicsMotivationAndSurvey)

1. [Classical mechanics via prequantized Lagrangian correspondences](#ClassicalMechanicsByPrequantizedLagrangianCorrespondences)

1. [Local (topological) prequantum field theory](#LocalTopologicalPrequantumFieldTheory)

1. [Prequantum Gauge theory and Gravity](#ActionFunctionalsForChernSimonsTypeGaugeTheories)

1. [Geometric quantization](#GeometricQuantization)

1. [Quantum mechanics](#QuantumMechanics)


=--


## **Perturbative quantum field theory**
 {#AFirstIdeaOfQuantumFieldTheory}

This section is at _[[geometry of physics -- perturbative quantum field theory]]_.


## **Physics in Higher Geometry: Motivation and Survey**
 {#PhysicsMotivationAndSurvey}

Before we discuss technical details starting in the [next chapter](#Fields) here we survey general ideas of [[theory (physics)|theories]] in fundamental [[physics]] and motivate how these are naturally formulated in terms of the [[higher geometry]] that we developed in the [first part](#GEOMETRY).

This chapter is at _[[geometry of physics -- physics in higher geometry]]_.




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

this chapter is at _[[geometry of physics -- prequantum gauge theory and gravity]]_


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

## **Related expositions**

* [[fiber bundles in physics]]

* [[motivation for sheaves, cohomology and higher stacks]]

* [[string theory FAQ]]

* [[higher category theory and physics]]

* [[motivation for higher differential geometry]]

* [[applications of (higher) category theory]]

* [[motivation for cohesion]]

* [[Hilbert's sixth problem]]

* [[motives in physics]]

* [[model theory and physics]]

* [[L-infinity algebras in physics]]



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