

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

This page describes a proposal for a formalization of the concept of [[quantization]] -- supposedly a natural process that turns  the [[higher geometry|higher geometric]] [[local Lagrangian]] data of a [[local prequantum field theory]] into the [[higher algebra|higher algebraic]] data of a [[local quantum field theory]] -- formulated in terms of [[cohomology]] in [[higher differential geometry]], specifically in [[cohesive (∞,1)-toposes]].

The fundamental observation here is that is natural to 

1. (**prequantum fields**) -- identify spaces of [[trajectories]] of [[field (physics)|fields]] as [[correspondences]] of higher [[moduli stacks]], hence correspondences in some suitably [[cohesive (∞,1)-topos|cohesive]] [[base (∞,1)-topos]];

1. (**local action functionals**) -- identify [[local action functionals]] as lifts of these [[correspondences]] to the [[slice (∞,1)-topos|slice]] of the base $\infty$-topos over an [[∞-group of units]] of a suitable [[E-∞ ring]] object $E$;

1. (**path integral**) -- identify the [[path integral]] [[quantization]]/[[partition function]] of these local action functionals on spaces of trajectories as the [[path integral as a pull-push transform|pull-push operation]]  in [[twisted cohomology|twisted]] $E$-[[cohomology theory]] through these correspondences.

This perspective has many precursors, listed in the [references below](#PrevLit). What is described here might be thought of as a proposal for a coherent, general and natural formulation, in the spirit of "[[schreiber:Synthetic Quantum Field Theory]]" formulated in the [[higher differential geometry]] of [[cohesive (∞,1)-toposes]].

Before looking at the details, we indicate some of the characteristic aspects of _motivic quantization_:

* _[The motivic aspect](#TheMotivicAspect)_;

* _[The holographic aspect](#TheHolographicAspect)_

* _[Locality](#Locality)_

* _[Anomalies](#AnomaliesAndOrientation)_

* _[Supersymmetry](#Supersymmetry)_


Then in the main part of the text we first give an exposition and survey of the main ideas in 

* _[Expositional survey](#ExpositionalSummary)_

and then lay out the basic definitions of _motivic quantization_ in detail in 

* _[General theory](#GeneralTheory)_.

Then we consider realizations of this theory in various

* _[Models](#Models)_;

and finally we discuss a list of examples in 

* _[Examples](#Examples)_.


### The motivic aspect
 {#TheMotivicAspect}

As our title indicates, it may be useful to note the analogy of the structures considered here to structures in [[motivic cohomology]] and in [[six operations]]-yoga. (See also at _[[motives in physics]]_.)

First notice the following heuristics: Just as the idea of a category of [[motives]] is to constitute a "linearization" or "abelianization" of a category of [[spaces]], so [[quantization]] is a process that sends (non-linear) spaces of field configurations to linear [[spaces of quantum states]]. This linearization by which [[quantum states]] may be added as elements of an [[abelian group]] encodes the [[superposition principle]] and hence [[quantum interference]], the hallmark of [[quantum physics]].

Concretely, a [[correspondence]] 

$$
  \array{
    && \mathbf{Trajectories}
    \\
    & {}^{\mathllap{i_{in}}}\swarrow && \searrow^{\mathrlap{i_{out}}}
    \\
    \mathbf{Fields}_{in}
    && \swArrow_{\xi} &&
    \mathbf{Fields}_{out}
    \;\;\;\;\;\;\;\;\;\;
    \in \mathbf{H}_{/\mathbf{B}GL_1(E)}
    \\
    & {}_{\chi_{in}}\searrow && \swarrow_{\chi_{out}}
    \\
    && \mathbf{B} GL_1(E)
  }
$$

in the [[slice (∞,1)-topos]] is equivalently 

1. a [[correspondence]] of [[spaces]] $\mathbf{Fields}_{in}$, $\mathbf{Fields}_{out}$ 

1. equipped with a [[cocycle]] $\xi \in H^{\bullet + i_{in}^\ast \chi_{in} + i_{out}^\ast \chi_{out}}(\mathbf{Fields}_{in}, \mathbf{Fields}_{out}; E)$ in [[bivariant cohomology|bivariant]] $(i_{in}^\ast \chi_{in}, i^\ast_{out} \chi_{out})$-[[twisted cohomology|twisted]] $E$-[[cohomology]] on its correspondence space, 

and the quantization step takes this to the [[equivalence class]] of maps of $E$-[[∞-modules]] that it induces under [[fiber integration in generalized cohomology]]:

$$
  \underset{i_{out}}{\int} i_{in}^\ast \xi 
  \;\;\colon \;\;
  \Gamma(\chi_{in})
  \stackrel{\;\;\;\;\;\;\;\;\;\;}{\to}
  \Gamma(\chi_{out})
  \;\;\;\;\;\;\;\;\;
  \in E \mathbf{Mod}
  \,.
$$

This process is analogous to how [[Chow motives]] induce cocycles in [[motivic cohomology]]. For $E = $ [[K-theory spectrum|KU]] and $\mathbf{Fields}$ a [[smooth manifold]] this was amplified in ([Connes-Skandalis 84](#ConnesSkandalis84), [Connes-Consani-Marcolli 05](#ConnesConsaniMarcolli05))), where the [[KK-theory|KK-category]] is regarded as the analog in [[noncommutative topology]] of a category of motives.  This vague analogy becomes precise from the general point of view of [[noncommutative motives]]: according to ([Tabuada 08](#Tabuada08), [Cisinski-Tabuada 11](#CisinskiTabuada11), [Blumberg-Gepner-Tabuada 10](#BlumbergGepnerTabuada10)) these are characterized by the same kind of [[universal properties]] that also characterizes [[KK-theory]], as summarized in the following table:

[[!include noncommutative motives - table]]

Moreover, for the case that $\mathbf{Fields}$ is a [[Deligne-Mumford stack]] (in the context of [[Gromov-Witten theory]], which is the [[path integral as a pull-push transform|pull-push quantization]] of a 2d field theory) the fact that pull-push quantization procceeds via morphisms of motives was amplified in ([Behrend-Manin 95](#BehrendManin95)), see also for instance the introduction of ([To&#235;n 00](#Toen00)).


Therefore it may be generally useful to refer to the process of quantization as discussed here as _[[motive|motivic]] [[quantization]]_. 

In view of this, notice that in the context of _[[formal deformation quantization]]_ (which is roughly an infinitesimal ("[[formal geometry|formal]]") approximation to [[geometric quantization]] as considered here) it is known that a [[quotient]] of the [[motivic Galois group]] (namely the [[Grothendieck-Teichmüller group]]) acts on the space of choices of [[formal deformation quantization]] of a [[Poisson manifold]]. (For details and pointers on this see at _[formal deformation quantization -- Motivic Galois group action on the space of quantizations](deformation%20quantization#MotivicGaloisGroup)_).


### The holographic aspect
 {#TheHolographicAspect}

A priori, motivic quantization applies to _[[topological field theory]]_. However, we consider it in the full generality that includes [[boundary field theory]] (field theory with [[branes]]) and generally [[defect field theory]] (field theory with [[domain walls]] of arbitrary codimension). This induces boundary effects which are not purely topological but encode "physical" field theories.

Concretely, for $Z \colon Bord_n(def)^\otimes \to \mathcal{C}^\otimes$ a topological [[local field theory]] which includes a boundary condition encoded by a generator $(\emptyset \stackrel{\partial}{\to} \ast) \in Mor_1(Bord_n(def))$, then crossing with this yields an $(n-1)$-dimensional field theory $Z((-)\times (\partial))$, the corresponding [[boundary field theory]]. This however now depends on choices of [[orientations in generalized cohomology]] that go along with defining a boundary component for $Z$, and these choices constitute geometric data.

For instance, for $Z$ a 3-dimensional [[Chern-Simons theory]], the relevant choice of orientation is induced by a choice of [[conformal structure]] on the boundary and so the boundary theory is a non-topological [[conformal field theory]]. (For details on this see at _[[AdS3-CFT2 and CS-WZW correspondence]]_.)

In [[physics]] this general kind of relation between $n$-dimensional topological field theories and $(n-1)$-dimensional non-topological field theories on their boundary is has come to be known as the _[[holographic principle]]_.  See there for more background.


### Locality
 {#Locality}


> For the moment see at _[Expositional summary -- Introduction](#ExpositionIntroduction)_ below.


### Anomalies
 {#AnomaliesAndOrientation}

We see that the motivic quantization operation over a [[cohomology theory]] $E$ depends on the existence of, and the choice of, an [[orientation in generalized cohomology|orientation in E-cohomology]]. The conditions that such an orientation exist in the first place turns out to be what in physics are known as the [[quantum anomaly cancellation]] conditions.

| [[theory (physics)|physical theory]] | [[cohomology theory]] |
|--|--|
| [[quantum anomaly]] | [[obstruction]] to [[orientation in generalized cohomology|orientation]] for [[push-forward in generalized cohomology|push-forward]] |
| (geo-)metric structure of [[boundary field theory]] | choice of [[orientation in generalized cohomology|orientation]]  |




### Supersymmetry 
 {#Supersymmetry}

Ever since the recognition of [[supersymmetric quantum mechanics]] in the 1980s, it is a familiar fact that [[index theory]] is naturally formulated in terms of [[superalgebra]] and [[supergeometry]]: indices can be identified with [[partition functions]] in [[supersymmetric quantum mechanics]]. Since [[push-forward in generalized cohomology]] is what generalizes the notion of [[index]] to the "relative case", motivic quantization may be thought of as intrinsically based on indices/partition functions. Accordingly one may expect that [[supersymmetry]] plays not just an optional but an intrinsic role. 

Indeed, one can observe the following seemingly deep relation between supersymmetry and [[higher algebra]]:

1. the $\mathbb{Z}_2$-grading of supersymmetry is a low-degree shadow of $\mathbb{S}$-grading, where $\mathbb{S}$ is the [[sphere spectrum]]; 

1. every [[E-∞ ring]] is canonically $\mathbb{S}$-graded, or at least it [[∞-group of units]] is. 

This is discussed in a bit more detail at _[superalgebra -- Abstract idea](super+algebra#AbstractIdea)_. 

Accordingly, it follows that some kind of ("higher") [[supersymmetry]] is intrinsic in motivic quantization.

A basic example is given by 2-dimensional motivic quantization over [[KU]]. A canonical smooth refinement of its [[∞-group of units]] is given, up to the 3-coskeleton, by the [[smooth super ∞-groupoid]] of [[super line 2-bundles]] (as discussed there). Accordingly, 2-dimensional local field theories, i.e. _[[string]]_ [[sigma-models]] are naturally refined to _[[superstring]]_ $\sigma$-models. See below the example _[The charged particle at the boundary of the superstring](#ChargedParticleAtBoundaryOfSuperstring)_.

But motivic quantization is not restricted to supersymmetric field theories, it is just that the [[phase and phase space in physics|higher phases]] are always naturally super-graded. Notably plain [[quantum mechanics]] encoded by traditional [[symplectic manifolds|symplectic]] or generally [[Poisson manifold|Poisson]] [[phase spaces]] is naturally subsumed. See below the example _[The Poisson manifold at the boundary of 2d Chern-Simons theory](#PoissonManifoldAtTheBoundaryOf2dChernSimonsTheory)_.


## Expositional summary
 {#ExpositionalSummary}

We give here a leisurely exposition of the main ideas of motivic quantization of local prequantum field theory. We follow ([Nuiten 13](#Nuiten13)) in outline.  For more details see there and/or skip ahead to _[General theory](#GeneralTheory).

1. _[Introduction](#ExpositionIntroduction)_

1. _[Local prequantum field theory](ExpositionLocalPrequantumFieldTheory)_

1. _[Linearization in generalized cohomology](#ExpositionLinearizationInGeneralizedCohomology)_

1. _[Quantization by pull-push](#ExpositionCohomologicalQuantization)_

1. _[Examples](#ExpositionExamples)_

### 1. Introduction 
  {#ExpositionIntroduction}

Some words of context. See ([Nuiten 13, section 1](#Nuiten13)).

$\,$


One of the modern cornerstones of [[Hilbert's sixth problem]] applied to the [[physics]] of [[quantum field theory]] is the following definition:

A [[topological field theory|topological]]+[[boundary field theory|boundary]]+[[defect QFT|defect]] _[[local field theory]]_ is a [[monoidal (∞,n)-functor]]

$$
  Z \;\colon\; Bord_n^\otimes \longrightarrow \mathcal{C}^\otimes
$$

from an [[(∞,n)-category of cobordisms]] with [[branes]] and [[domain walls]], to _some_ [[symmetric monoidal (∞,n)-category]].

The point of this [[axiom]] is that the [[higher category theory|higher categorical]] [[(∞,n)-functor|(∞,n)-functoriality]] of $Z$ is what encodes the _[[local quantum field theory|locality]]_ of the [[field theory]]. This in turn encodes a fundamental property of the [[fundamental physics]] of the [[observable universe]] called _[[causal locality]]_ : (spacelike-)separated regions of [[spacetime]]/[[worldvolume]] behave like [[independent subsystems]].

| [[fundamental physics]] | [[foundations|foundational]] [[mathematics]] |  experimental bound on violation |
|---|---|--|
| [[gauge principle]] | [[homotopy theory]]  |     |
| [[causal locality]] | [[higher category theory]] |  $\lessapprox 10^{-17}m$ ([Grigoriev 79](causal+locality#Microcausality)), $\lessapprox 10^{-20}m \simeq 7 TeV$ ([[LHC]]) |


The [[cobordism hypothesis]] provides a good characterization of the space of _all_ such $Z \colon Bord_n^\otimes \to \mathcal{C}^\otimes$. But for modelling _[[physics]]_ there are typically more restrictions to be imposed.

In particular, for actual _[[quantum theory|quantum]]_ (as opposed to [[prequantum field theory|prequantum]] or [[classical field theory|classical]]) [[field theory]], the [[codomain]] $\mathcal{C}$ is to be an [[(∞,n)-category|n-dimensional]] analog of a _[[additive and abelian categories|linear]]_ [[tensor category|tensor]] [[category of modules]], $R Mod^\otimes$, for some [[commutative ring|commutative]] [[ground ring]] $R$ (which in ordinary [[quantum mechanics]] is the [[complex numbers]]).

The [[abelian category|linearity]] of $E Mod$ encodes the [[superposition principle]] of [[quantum physics]], which says that [[quantum states]] may be added and possibly may additively cancel. This cancellation is _[[quantum interference]]_, the very hallmark of [[quantum physics]].

In [[local quantum field theory]]/[[higher category theory]]/[[homotopy theory]] we choose, more generally, a ground _[[E-∞ ring|commutative ∞-ring]]_ $E$. This comes with its [[symmetric monoidal (∞,1)-category|symmetric monoidal]] [[(∞,1)-category of ∞-modules]] $E Mod^\otimes$.

A decent choice for $\mathcal{C}^\otimes$ is then $\mathcal{C}^\otimes = E Mod^{\Box^n}$, the [[symmetric monoidal (∞,n)-category]] of $n$-dimensional [[cubes]] in $E Mod$. With this used as the codomain in the definition of $Z$

$$
  Z \; \colon \;
  Bord_n^\otimes \to (E Mod^{\Box^n})^\otimes
$$

the [[field theory]] assigns [[quantum propagator]] [[linear maps]] between [[spaces of quantum states]] to pieces of [[spacetime]]/[[worldvolume]]:

$$
  \left(
  \array{
   x_{1,1}  &\to& x_{2,1}
   \\
   \downarrow & {world- \atop volume} & \downarrow
   \\
   x_{1,2} & \to & x_{2,2}
  }
  \right)
  \;\;\;\;
  \stackrel{Z}{\mapsto}
  \;\;\;\;
  \left(
  \array{
    V_{1,1} &\stackrel{}{\to}& V_{2,1}
    \\
    \downarrow & {{quantum \atop states} \atop {and \; propagators}} & \downarrow
    \\
    V_{1,2} &\to& V_{2,2}
  }
  \right)
  \,.
$$

But even with $\mathcal{C}$ restricted to be of the form $E Mod^{\Box^n}$ or similar, the notion of $Z$ as above is still much more general than the field theories typically of interest in nature and in theory. The quantum field theories actually of interest both in nature and in theory have the special property that they arise via a process of _[[quantization]]_ from [[higher geometry|higher geometric data]] given by a [[local prequantum field theory]]: a [[local action functional]]/[[local Lagrangian]] on a [[moduli space]] of [[field (physics)|fields]].

This is the process to be indicated in the following:

| [[local prequantum field theory]]  | -- [[quantization]]$\longrightarrow$ | [[local quantum field theory]] |
|---|---|---|
| [[higher geometry]] | --[[motives]]$\longrightarrow$ | [[higher linear algebra]] |
| [[higher prequantum line bundle]] | --space of [[sections]]$\longrightarrow$ | [[∞-module]] of [[quantum states]] |
| [[section]], [[wavefunction]] |   | [[quantum state]] |
| [[correspondences]], [[integral kernels]] | --[[path integral as a pull-push transform|pull-push transform]]$\longrightarrow$ | [[linear maps]]  |
| [[field (physics)|field]] [[trajectories]] | --[[path integral]]$\longrightarrow$ | [[quantum propagators]] |

This process may be thought of as a refinement of _[[geometric quantization]]_ from [[quantum mechanics]] to ([[non-perturbative quantum field theory|non-perturbative]]) [[quantum field theory]]. 


|  |  | [[perturbation theory]] | [[non-perturbative field theory]] |
|--|--|--|--|
| [[quantum mechanics]] |  | [[formal deformation quantization]] |  [[geometric quantization]]  |
| [[quantum field theory]] |  | [[BV quantization]] to [[factorization algebra]] | [[motivic quantization]] to [[FQFT]]  |



### 2. Local prequantum field theory
 {#ExpositionLocalPrequantumFieldTheory}

First we consider [[local prequantum field theory]]. See ([Nuiten 13, section 2](#Nuiten13), [Fiorenza-Rogers-Schreiber 13a](#FiorenzaRogersSchreiber13a), [Nuiten-Schreiber 13](#lpqft)). 

$\,$


The notion of [[field (physics)|field]] in [[physics]] is often said to be [[axiom|axiomatized]] as a [[section]] of a [[fiber bundle]] over [[spacetime]]/[[worldvolume]] whose [[fibers]] are [[manifolds]] -- called the _[[field bundle]]_. This is [[true]] for simple instances of [[scalar fields]] and [[sigma-model]] fields. 

But it is [[false]] for [[gauge fields]] as in [[electromagnetism]] or [[Yang-Mills theory]] (and is ever more false for [[higher gauge fields]], such as the [[B-field]] in [[type II supergravity]] or in the [[6d (2,0)-superconformal QFT]]):

for $G$ a [[Lie group]] regarded as a [[gauge group]], a $G$-[[gauge field]] on $X$ is a [[section]] of a kind of bundle whose fiber is the universal [[moduli stack]] $\mathbf{B}G_{conn}$ of $G$-[[principal connections]] $\nabla$. The underlying [[instanton sector]] $\mathbf{c}(\nabla)$ of the [[gauge field]] is still a section of a bundle whose typical fiber is the [[moduli stack]] $\mathbf{B}G$ of $G$, locally on a [[cover]] $U \to X$ one has:

$$
  \array{
     && \mathbf{B}G_{conn}
     \\
     & {}^{\mathllap{\nabla|_U}}\nearrow & \downarrow
     \\
     U &\stackrel{\mathbf{c}(\nabla|_U)}{\to}&
     \mathbf{B}G
  }
  \,.
$$

Here $\mathbf{B}G$ is not a [[smooth manifold]], but a [[smooth groupoid]] (a [[geometric stack]]), and a $(\mathbf{B}G)$-fiber bundle is a _[[fiber ∞-bundle|fiber 2-bundle]]_, called a _$G$-[[gerbe]]_ over $X$, which itself is a [[connected object in an (∞,1)-category|connected]] [[stack]] of [[groupoids]] over $X$.

Here the [[groupoid]]-nature of $\mathbf{B}G$ is a precise reflection of the [[gauge principle]] governing the [[gauge field]].

Similarly, an abelian [[higher gauge field|n-form gauge field]] (e.g. the [[B-field]], the [[supergravity C-field]]) is locally given by maps into a [[moduli infinity-stack|moduli n-stack]] $\mathbf{B}^n U(1)_{conn}$ of [[circle n-bundles with connection]], which is a [[smooth ∞-groupoid|smooth n-groupoid]]. A [[field bundle]] for these is hence a $U(1)$-[[infinity-gerbe|n-gerbe]].

(All this is true in the complete [[non-perturbative field theory|non-perturbative]] description of [[field theory]]. Often, however, field theory is discussed only in the approximation [[perturbation theory]], where all spaces are linearized by their [[infinitesimal object|infinitesimal]] approximation. Since the [[Lie differentiation]] of a [[smooth ∞-stack|smooth higher stack]] is precisely an [[L-∞ algebra]]/[[L-∞ algebroid]], and since these may be modeled on [[chain complexes]], it follows that in [[perturbation theory]] (only) one may generally assume (mostly) that fields are indeed sections of an ordinary [[field bundle]].)

So in order to formalize [[non-perturbative field theory|non-perturbative]] [[local prequantum field theory]] one needs to pair [[geometry]] with [[homotopy theory]]. Such a combination is called an _[[(∞,1)-topos]]_ of [[∞-stacks]]/[[geometric ∞-groupoids]]:

* [[geometry]] +  [[homotopy theory]] = [[(∞,1)-topos|∞-topos]]

* [[space]] + [[higher gauge theory|higher]] [[gauge transformations]] = [[geometric ∞-groupoid]]/[[∞-stack]] .

We consider now $\mathbf{H}$ to be a suitable such [[(∞,1)-topos]]. The example to keep in mind is

$\mathbf{H} =$ [[SmoothSuper∞Grpd]] $\coloneqq Sh_\infty(SuperManifolds) = L_{lhe} Func(Supermanifolds^{op}, KanComplexes)$

which is the context of [[higher differential geometry]] for the description of [[boson|bosonic]] [[field (physics)|fields]] and of higher [[supergeometry]] (for the description of [[fermion]] [[field (physics)|fields]]).

More generally, for constructing the [[moduli ∞-stacks]] of [[higher gauge fields]] we need an [[(∞,1)-topos]] $\mathbf{H}$ that satisfies an axiom called _[[differential cohesion|differential]] [[cohesion]]_.

Given such $\mathbf{H}$, every object in it serves as a _[[moduli ∞-stack]]_ of [[field (physics)|fields]], so we write here $\mathbf{Fields} \in \mathbf{H}$. This means that if $X \in \mathbf{H}$ is regarded as [[spacetime]]/[[worldvolume]], then 

* a [[field (physics)|field]] on $X$ is a map

  $$
    \phi \;\colon\; X \longrightarrow \mathbf{Fields}
  $$

  in $\mathbf{H}$, 

* a [[gauge transformation]] of such fields is a [[homotopy]] betwen two such maps, 

* and a [[higher gauge transformation]] is a [[higher homotopy]] between those.

With physical fields in hand, next we need to axiomatize [[trajectories]] of such fields.

Now a space of [[trajectories]] of fields is itself a space of fields, together with projections to the incoming and the outgoing fields configurations, hence a [[span]]-shaped [[diagram]] of the form

$$
  \array{
    && \mathbf{Fields}_{\mathrm{trajectories}}
    \\
    &   {}^{\mathllap{(-)|_{in}}}\stackrel{}{\swarrow}
    &&
    \searrow^{\mathrlap{(-)_{out}}}
    \\
    \mathbf{Fields}_{in}
     && &&
    \mathbf{Fields}_{out}
  }
  \,.
$$

We say that this is _[[correspondence]]_ (or in fact a _higher [[relation]]_) between $\mathbf{Fields}_{in}$ and $\mathbf{Fields}_{out}$.

For instance for 

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

a [[cobordism]] with incoming and outgoing [[boundary]] [[manifolds]] as indicated, and for $\mathbf{Fields}$ a given [[moduli stack]] of [[field (physics)|fields]] as above, then forming [[mapping spaces]] ([[mapping stacks]]) yields the [[correspondence]]

$$
  \array{
    && [\Sigma,\, \mathbf{Fields}]
    \\
    & \swarrow && \searrow
    \\
    [\partial_{in}\Sigma,\, \mathbf{Fields}]
    && && 
    [\partial_{out} \Sigma,\, \mathbf{Fields}]
  }
$$

which exhibits field configurations on $\Sigma$ as trajectories along which fields on $\partial_{in} \Sigma$ propagate to $\partial_{out} \Sigma$. 

In the example here, $\mathbf{Fields}$ is the moduli of some [[sigma-model]] field (hence $\mathbf{Fields} = X$ a [[target space]]), then this describes a bunch of [[branes]] of shape the [[connected components]] of $\Sigma_{in}$ coming in, propagating and interacting along a [[worldvolume]] of shape $\Sigma$, and finally emerging as a collection of branes of shape the [[connected components]] of $\Sigma_{out}$. This describes a [[scattering process]]. Its [[quantization]] will be what is called the corresponding _[[scattering amplitude]]_ (the [[probability amplitude]] for the process to take place) or _[[n-point function]]_ or _[[correlator]]_. 

Specifying the example further, suppose that $\Sigma$ is an $n$-[[sphere]] with $(k+1)$ disjoint $n$-[[balls]] marked,  regarded as a [[cobordism]]

$$
  \array{
    && S^d
    \\
    & \nearrow && \nwarrow
    \\
    \coprod_{i = 1}^k D^d 
    && &&
    D^d
  }
  \,,
$$

then For $\mathbf{Fields}$ some [[sigma-model]] fields this may be taken to encode a diagram where $k$ _open $d$-[[branes]]_ come in, merge, and one comes out. For instance for $d = 1$ and $k = 3$ this is a cobordism that when "viewed in time direction" is an inclusion of three small intervals into one larger interval

$$
  \left[
       \;\;\;
       \left[ \;\;\;\;\; \right]_{\Sigma_{in}^1}
       \;\;\;\;\;\;
       \left[ \;\; \right]_{\Sigma_{in}^2}
       \;\;\;\;
       \left[ \;\;\;\; \right]_{\Sigma_{in}^3}
       \;\;\;
  \right]_{\Sigma_{out}}
  \,.
$$

These are of course the operations in the [[little k-cubes operad]]. Hence [[quantization]] of local boundary prequantum field theory restricted to [[cobordisms]] of this form yields what are called topological or _locally constant_ [[factorization algebras]]. 


To capture all this functorially, write then $Corr_n(\mathbf{H})^\otimes$ for the [[(∞,n)-category of n-fold correspondences]] whose [[objects]] are those of $\mathbf{H}$ and whose [[morphisms]] are [[correspondences]] between them, as above. This is [[symmetric monoidal (∞,1)-category|symmetric monoidal]] by objectwise [[Cartesian product]] in $\mathbf{H}$. 

One finds that: 

* _every_ object of $\mathbf{H}$ is self-[[fully dualizable object|fully dualizable]] in $Corr_n(\mathbf{H})^\otimes$;

* the [[higher trace]] $tr_{\Pi(\Sigma)}(\mathbf{Fields})$ of [[shape]] $\Pi(\Sigma)$ of this [[fully dualizable object]] is the [[moduli ∞-stack]] of [[flat modality|flat]] fields on $\Sigma$ -- this is the _[[phase space]]_ of fields (for fields of [[∞-Chern-Simons theory]]-type at least).

This means, by the [[cobordism hypothesis]],  that a choice of [[moduli ∞-stack]] $\mathbf{Fields} \in \mathbf{H}$ is equivalently a choice of [[monoidal (∞,n)-functor]]

$$
  \mathbf{Fields}
  \;\colon\;
  Bord_n^\otimes
    \longrightarrow
  Corr_n(\mathbf{H})^\otimes
$$

which sends [[cobordisms]] to the [[phase space]] [[correspondences]] between in- and out-going flat field configurations over the boundary, given by flat [[trajectories]] over the cobordism:

$$
  \left(
    \array{
      && \Sigma
      \\
      & \nearrow && \nwarrow
      \\
      \Sigma_{in}
      && &&
      \Sigma_{out}
    }
  \right)
  \;\;
    \stackrel{\;\;\;\;\;\;}{\mapsto}
  \;\;
  \left(
    \array{
      && [\Pi(\Sigma), \mathbf{Fields}]
      \\
      & {}^{\mathllap{(-)|_{in}}}\swarrow 
      && 
      \searrow^{\mathrlap{(-)|_{out}}}
      \\
      [\Pi(\Sigma_{in}), \mathbf{Fields}]
      && 
      &&
      [\Pi(\Sigma_{out}), \mathbf{Fields}]
    }
  \right)
  \,.
$$

In this way the [[moduli ∞-stack]] $\mathbf{Fields}$ of [[field (physics)|fields]] encodes the _[[kinematics]]_ of a [[local prequantum field theory]]. 

Next we define the _[[dynamics]]_ by defining a [[local action functional]] which assigns to each [[trajectory]] a [[probability amplitude]] for that trajectory to be "physically realized".

Traditionally, in non-localized [[prequantum field theory]], an (exponentiated) [[action functional]] is a map of the form $\mathbf{Fields}_{traj} \longrightarrow U(1)$. For instance for $\mathbf{Fields}_{traj} \coloneqq [S^1, X]$ the smooth [[loop space]] of a [[manifold]] $X$ that is equipped with a $U(1)$-[[principal connection]] $\nabla \colon X \to \mathbf{B}U(1)_{conn}$ (an [[electromagnetic field]]), then the [[holonomy]] [[nonlinear functional|functional]] $hol_\nabla \colon [S^1, X] \to U(1)$ is the [[interaction]] term for the [[charged particle]] [[sigma model]] [[field theory]] on $X$.

To see how this is axiomatized in _[[local field theory|local]]_ [[field theory]], notice that there is a [[homotopy fiber product]] [[diagram]] of the form

$$
  \array{
   && U(1)
   \\
   & \swarrow && \searrow
   \\
   \ast && \swArrow_\simeq && \ast
   \\
   & {}_{\mathllap{0}}\searrow && \swarrow_{\mathrlap{0}}
   \\
   && \mathbf{B}U(1)
  }
  \,.
$$

in $\mathbf{H}$, which exhibts the [[circle group]] (as a [[Lie group]]!) as the [[loop space object]] of the [[moduli stack]] of $U(1)$-[[principal bundles]]: $U(1)\simeq \Omega \mathbf{B}U(1)$. By the [[universal property]] of the [[homotopy fiber]] construction, this means that maps $\mathbf{Fields}_{traj} \longrightarrow U(1)$ are equivalent to [[diagrams]] of the form

$$
  \array{
    && \mathbf{Fields}_{traj}
    \\
    & \swarrow && \searrow 
    \\
    \mathbf{Fields}_{in}
    && 
     \swArrow 
    &&
    \mathbf{Fields}_{out}
    \\
    & {}_{\mathllap{0}}\searrow && \swarrow_{\mathrlap{0}}
    \\
    && \mathbf{B} U(1)
  }
  \;\;\;\;\;
  \simeq
  \;\;\;\;\;
  \array{
    && \mathbf{Fields}_{traj}
    \\
    & \swarrow &\downarrow^{\mathrlap{\exp(i S)}}& \searrow 
    \\
    \ast
    &\leftarrow& 
      U(1)
    &\rightarrow&
    \ast
    \\
    & {}_{\mathllap{0}}\searrow &\swArrow& \swarrow_{\mathrlap{0}}
    \\
    && \mathbf{B} U(1)
  }
  \,.
$$

More generally, for $[I,X]$ the smooth [[path space]] of $X$, the [[interaction]] term of the [[charged particle]] [[sigma model]] on $(X,\nabla)$ is not in general a $U(1)$-valued [[function]] on $X$, but is a [[section]] of the $U(1)$-[[principal bundle]] $\chi(\nabla) \colon X \to \mathbf{B}U(1)$ which underlies $\nabla$, pulled back to [[path space]] along the two endpoint evaluations. This means that it is a diagram of this form

$$
  \array{
    && [I,X]
    \\
    & {}^{(-)|_0}\swarrow && \searrow^{(-)|_1}
    \\
    X && \swArrow_{\exp(i S)} && X
    \\
    & {}_{\mathllap{\chi(\nabla)}}\searrow && \swarrow_{\mathrlap{\chi(\nabla)}}
    \\
    && \mathbf{B}U(1)
  }
$$

where now the bottom morphisms are non-trivial, given by the [[background gauge field]]. In view of the above, it makes sense to think of this [[background gauge field]] $\nabla \colon X \to \mathbf{B}U(1)_{conn}$ itself as a "higher incarnation" or "local incarnation" of the action functional on path _de-[[transgression|transgressed]]_ from [[path space]] back to the manifold itself.

Therefore, in general we say that a _[[local action functional]]_ for a [[local prequantum field theory]] of [[dimension]] $n$ with [[field (physics)|field]] content $\mathbf{Fields} \in \mathbf{H}$ is a map in $\mathbf{H}$ of the form

$$
  \array{
    \mathbf{Fields}
    \\
    \downarrow^{\mathrlap{\exp(i S)}}
    \\
    \mathbf{B}^n U(1)_{conn}
  }
  \,,
$$

hence is a [[circle n-bundle with connection]] on the universal [[moduli ∞-stack]] $\mathbf{Fields}$.

Exploring this localized [[higher prequantum geometry]] formulation (e.g. [Fiorenza-Rogers-Schreiber 13a](#FiorenzaRogersSchreiber13a)), one finds that the notion of localized action functional coincides with the notion of _[[local Lagrangian]]_ and also coincides with this notion of _[[higher prequantum bundle]]_ -- by _[[transgression]]_ to lower [[codimension]]:

* the [[transgression]] of $\exp(i S)$ to [[codimension]] 0 is the traditional [[action functional]] $[\Sigma_n, \mathbf{Fields}] \to U(1)$. 

* the [[transgression]] of $\exp(i S)$ to [[codimension]] $1$ is the the traditional (off-shell) [[prequantum circle bundle]] $[\Sigma_{n-1}, \mathbf{Fields}] \to \mathbf{B}U(1)_{conn}$;

and so on, for instance if we think of $\exp(i S)$ as an [[schreiber:∞-Chern-Simons theory]], then

* the [[transgression]] of $\exp(i S)$ to [[codimension]] $n-1$ is the corresponding [[schreiber:∞-Wess-Zumino-Witten theory]] 

  (e.g. traditional [[WZW model]] if $\nabla$ is the [[universal Chern-Simons circle 3-connection]]; or the [[M5-brane]] [[worldvolume]] theory (supposedly the [[6d (2,0)-superconformal QFT]]) for $\nabla$ the [[supergravity Lie 6-algebra]] [[L-∞ cocycle]] plus the [[universal Chern-Simons circle 7-connection]] and other terms ([Fiorenza-Sati-Schreiber 12a](#FSS12a), [Fiorenza-Sati-Schreiber 13](#WZWLie)).



Therefore just as the [[(∞,1)-topos]] $\mathbf{H}$ itself is the home of [[moduli ∞-stacks]] of [[field (physics)|fields]] ([[kinematics]]) so the collection of all [[local action functionals]] on such moduli $\infty$-stacks ([[dynamics]]) forms the [[slice (∞,1)-topos]]

$$
  \mathbf{H}_{/\mathbf{B}^n U(1)_{conn}}
$$

whose [[objects]] are maps $\left[\array{\mathbf{Fields} \\ \downarrow^{\mathrlap{exp(i S)}} \\  \mathbf{B}^n U(1)_{conn}}\right]$ and whose [[morphisms]] are [[diagrams]] of the form

$$
  \array{
    \mathbf{Fields}_1
     && \longrightarrow &&
    \mathbf{Fields}_2
    \\
    & {}_{\mathllap{\exp(i S_1)}}\searrow &\swArrow_\simeq& \swarrow_{\mathrlap{\exp(i S_2)}}
    \\
    && \mathbf{B}^{n} U(1)_{conn}
  }
$$

in $\mathbf{H}$. 

The [[automorphism ∞-groups]] in this [[(∞,1)-topos]] of [[local action functionals]] are precisely the [[quantomorphism ∞-groups]] (infinitesimally the [[Poisson L-∞ algebras]]), conaining the [[Heisenberg ∞-groups]] (infinitesimally the [[Heisenberg L-∞ algebras]]) of local [[prequantum observables]] ([Fiorenza-Rogers-Schreiber 13a](FiorenzaRogersSchreiber13a)). Equivalently, they are [[∞-groups]] of [[conserved currents]].

The [[(∞,1)-category]] $Corr_n\left(\mathbf{H}_{/\mathbf{B}^n U(1)_{conn}}\right)$ of [[correspondences]] in the slice contains trajectories equipped with action functionals.

In conclusion, a [[local action functional]] $\exp(i S)$ on a species $\mathbf{Fields}$ of [[field (physics)|physical fields]] is a lift $\exp(i S)$ in

$$
  \array{
    Bord_n^\otimes
     &\stackrel{\exp(i S)}{\to}& 
    Corr_n\left(\mathbf{H}_{/\mathbf{B}^n U(1)}\right)^\otimes
    \\
    & {}_{\mathllap{Fields}}\searrow & \downarrow
    \\
    && Corr_n\left(\mathbf{H}\right)^\otimes
  }
  \,.
$$

Such a diagram defines a _[[local prequantum field theory]]_ ([[topological field theory|topological]]+[[boundary field theory|boundary]]+[[defect field theory|defects]]).

This theory may have boundaries/[[branes]]. Below we find that most [[local quantum field theories]] of interest arise actually as the [[boundary field theories]] of a higher dimensional field theory and that their [[quantization]] is induced from that higher dimensional theory in a "[[holographic principle|holographic]]" way that generalizes the [[AdS3-CFT2 and CS-WZW correspondence]].

If $Bord_n^\otimes$ is generated precisely from one boundary brane of top [[codimension]], then specifying a [[local prequantum field theory]] is equivalent to specifying a boundary [[correspondence]] of the form

$$
  \array{
    && \mathbf{Fields}_{boundary}
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow && \mathbf{Fields}
    \\
    & \searrow && \swarrow_{\mathrlap{\chi}}
    \\
    && \mathbf{B}^n U(1)
  }
  \,.
$$

Such a diagram is equivalently a [[twisted differential c-structure|twisted chi-structure]] and such structures appear all over the place in [[local prequantum field theory]] (e.g. [Fiorenza-Sati-Schreiber 09](#FSS09), [Fiorenza-Sati-Schreiber 12](FSS12)) see for instance the lecture notes at _[[twisted smooth cohomology in string theory]]_



### 3. Linearization in generalized cohomology
 {#ExpositionLinearizationInGeneralizedCohomology}

We now survey the linearization step. See ([Nuiten 13, section 3](#Nuiten13)).

$\,$

Before actually quantizing a [[local prequantum field theory]] $\left[ \array{ \mathbf{Fields} \\ \downarrow^{\mathrlap{\exp(i S)}} \\ \mathbf{B}^n U(1)_{conn}}\right]$ as above, we choose linear [[coefficients]], given by 


1. a choice of ground [[E-∞ ring]] $E$ 

   (playing the role of the [[complex numbers]] in plain [[quantum mechanics]]);


1. a choice of [[∞-group]] homomorphism

   $$
     \rho \;\colon\; \mathbf{B}^{n-1}U(1) \longrightarrow GL_1(E)
   $$


   from the [[∞-group]] of [[phase and phase space in physics|phases]] to the [[∞-group of units]] of $E$, hence an [[∞-representation]] of the [[circle n-group]] on $E$ 

   (playing the role of the canonical $U(1) \hookrightarrow \mathbb{C}^\times$ in plain [[quantum mechanics]]).


Then for $X \longrightarrow \mathbf{B}^n U(1)$ modulating a [[circle n-bundle with connection|circle n-bundle]] on $X$, the composite

$$
  X
   \longrightarrow
  \mathbf{B}^n U(1)
    \stackrel{\rho}{\longrightarrow}
  B GL_1(E)
    \longrightarrow
  E Mod
$$

modulates the [[associated ∞-bundle]], which is an $E$-[[(∞,1)-module bundle]].


Specifically, given the [[higher prequantum bundle]] $\exp(i S) \;\colon\; \mathbf{Fields} \to \mathbf{B}^n U(1)_{conn}$ as above, the composite

$$
  \chi
   \;
   \colon
   \;
  \mathbf{Fields}
    \stackrel{\exp(i S)}{\longrightarrow}
  \mathbf{B}^n U(1)
    \stackrel{\rho}{\longrightarrow}
  \mathbf{B} GL_1(E)
    \stackrel{}{\longrightarrow}
  Pic(E)
    \longrightarrow
  E Mod
$$

modulates the associated _[[higher prequantum line bundle|higher prequantum E-line bundle]]_.

A [[section]] of $\chi$ is a _higher [[wavefunction]]_, hence a _higher [[quantum state]]_.

(At this point this looks un-[[polarization|polarized]], but in fact we will see in the next section that the notion of [[polarization]] in [[higher prequantum geometry]] is automatic, but appears in a [[holography|holographic]]/[[boundary field theory|boundary field theory]] way in [[codimension]] $(n-1)$ instead of here in codimension $n$.)

Accordingly, the [[space of sections]] of $\chi$ is the higher [[space of quantum states]] in [[codimension]] 0. 

If $X$ is a [[discrete ∞-groupoid]] then the space of sections has a particularly nice description, on which we focus for a bit:

The space of co-sections is the [[(∞,1)-colimit]]

$$
  E_{\bullet + \chi}(X) 
  \; \coloneqq\;
  \underset{\to}{\lim}
  \chi
  \;
  \in E Mod
  \,.
$$

This is also known as the _$\chi$-twisted $E$-[[Thom spectrum]]_ of $X$ ([Ando-Blumberg-Gepner 10](#ABG)).

* a map $E \to E_{\bullet + \chi}(X)$ is a [[cycle]] in $\chi$-[[twisted cohomology|twisted]] $E$-[[generalized homology]] of $X$;

* a map $E_{\bullet + \chi}(X) \to E$ is a [[cocycle]] in $\chi$-[[twisted cohomology|twisted]] $E$-[[generalized cohomology]] of $X$

  Hence we write

  $$
    E^{\bullet + \chi}\left(X\right)
    \coloneqq
    \left[
      E_{\bullet + \chi}\left(X\right),
      \,
      E
    \right]
    \,.
  $$

Generally, for $\chi_i \colon X_i \to E Mod$ two $E$-[[(∞,1)-module bundles]] over two spaces, a map

$$
  E_{\bullet + \chi_1}(X_1)
  \longrightarrow
  E_{\bullet + \chi_2}(X_2)
$$

is a [[cocycle]] in $(\chi_1, \chi_2)$-[[twisted cohomology|twisted]] [[bivariant cohomology|bivariant]] $E$-[[cohomology]].

Now given a [[local action functional]] on a space of [[trajectories]], hence a [[correspondence]] as above, this induces an [[integral kernel]] for linear maps between sections of [[higher prequantum line bundles]]:

$$
  \array{
    && \mathbf{Fields}_{traj}
    \\
    & \swarrow && \searrow
    \\
    \mathbf{Fields}_{in}
     && \swArrow_{\rho(\xi)} &&
    \mathbf{Fields}_{out}
    \\
    & {}_{\mathllap{\chi_{in}}}\searrow
    &&
    \swarrow_{\mathrlap{\chi_{out}}}
    \\
    && E Mod
  }
  \;\;\;
  \coloneqq
  \;\;\;
  \array{
    && \mathbf{Fields}_{traj}
    \\
    & \swarrow && \searrow
    \\
    \mathbf{Fields}_{in}
     && \swArrow_\xi &&
    \mathbf{Fields}_{out}
    \\
    & {}_{\mathllap{\exp(i S_{in})}}\searrow
    &&
    \swarrow_{\mathrlap{\exp(i S_{out})}}
    \\
    && \mathbf{B}^n U(1)
    \\
    && \downarrow
    \\
    && B GL_1(E)
    \\
    && \downarrow
    \\
    && Pic(E)
    \\
    && \downarrow
    \\
    && E Mod
  }
$$

This is the [[integral kernel]] induced by the action functional, and acting on spaces of sections of the [[higher prequantum line bundle]].

The [[linear map]] induced by these higher [[integral kernels]] is to be the _[[quantum propagator]]_. This we come to in the next section.

Notice that forming co-sections constitutes an [[(∞,1)-functor]]

$$
  E_{\bullet + (-)}(-)
  \;\colon\;
  \mathbf{H}_{/\mathbf{B}^n U(1)_{conn}}
  \longrightarrow
    E Mod
  \,.
$$

Therefore forming co-sections sends an [[integral kernel]] as above to a [[correspondence]] of $E$-[[(∞,1)-modules]]:

$$
  \array{
    && \mathbf{Fields}_{traj}
    \\
    & {}^{i_{in}}\swarrow && \searrow^{\mathrlap{i_{out}}}
    \\
    \mathbf{Fields}_{in}
     & & \swArrow_{\simeq}  & &
    \mathbf{Fields}_{out}
    \\
    & {}_{\mathllap{\chi_{in}}}\searrow
    &&
    \swarrow_{\mathrlap{\chi_{out}}}
    \\
    && E Mod
    \\
    \,
    \\
    \,
    \\
   E_{\bullet + \chi_{in}}(\mathbf{Fields}_{in})
    & \stackrel{(i_{in})_\ast}{\longleftarrow}&
   \array{
   E_{\bullet + i_{in}^\ast\chi_{in}}(\mathbf{Fields}_{traj})
    \\
    \simeq 
    \\
   E_{\bullet + i_{out}^\ast\chi_{out}}(\mathbf{Fields}_{traj})
    }
    & \stackrel{(i_{out})^\ast}{\longrightarrow}&
   E_{\bullet + \chi_{out}}(\mathbf{Fields}_{out})
  }
  \,.
$$


The actual [[quantization]]/[[path integral as a pull-push transform]] map now consists in forming a [[dual morphism]] in $E Mod$ so as to turn one of the projections of such a correspondence around to produce a [[quantum propagator]]

$$
  E^{\bullet + \chi_{in}}(\mathbf{Fields}_{in})
    \longrightarrow
  E^{\bullet + \chi_{out}}(\mathbf{Fields}_{out})
$$

that maps the incoming [[quantum states]]/[[wavefunctions]] to the outgoing ones.


### 4. Cohomological quantization by pull-push
 {#ExpositionCohomologicalQuantization}

We now survey the cohomological quantization step. See ([Nuiten 13, section 4](#Nuiten13)).

$\,$

What we need now for [[quantization]] is a [[path integral]]
map that adds up the values of the [[action functional]] over the space of trajectories, a functor of the form

$$
  \int (-)
  \;\;
   \colon
  \;\;
   Corr_n\left(\mathbf{H}_{/\mathbf{B}^n U(1)}\right)^\otimes
  \to 
   (E Mod^{\Box^n})^\otimes
$$

As such this will in general only exist for [[schreiber:∞-Dijkgraaf-Witten theory]] where $\mathbf{Fields}$ is a [[discrete ∞-groupoid]] and hence has a "counting measure". This case has been considered in ([Freed-Hopkins-Lurie-Teleman 09](#FreedHopkinsLurieTeleman09), [Morton 10](#Morton10)).

In the general case the path integral requires that we _choose_ a suitable [[measure]]/[[orientation]] on the spaces of fields. 
We see below what this means, for the moment we just write 

$$
  Corr^{or}_n(\mathbf{H}_{/\mathbf{B}^n U(1)})^\otimes
$$ 

(i.e. with an ${(-)}^{or}$-superscript) as a mnemonic for a suitable [[(∞,n)-category]] of suitably oriented/measured spaces of fields with action functional. Then we may consider lifts of the action functional to _measure-valued_ action functionals

$$
  \exp(i S) \, d\mu
  \;\colon\;
  Corr_n^{or}\left(\mathbf{H}_{/\mathbf{B}^n U(1)}\right)^\otimes
  \to
  \left(
   E Mod^{\Box^n}
  \right)^\otimes
  \,.
$$

A [[path integral]] is then to be a monoidal functor of the form

$$
  \int(-) \;\colon\;
  Corr_n^{or}\left(\mathbf{H}_{/\mathbf{B}^n U(1)}\right)^\otimes
  \to 
  \left(
    E Mod^{\Box^n}
  \right)^\otimes
  \,.
$$

This we discuss now below. Once we have such a [[path integral]] functor, the [[quantization]] 
process is its [[composition]] with the given [[prequantum field theory]] $\exp(i S) \, d \mu$ to obtain the genuine quantized [[quantum field theory]]:

$$
  \array{
    \underset{\phi \in \mathbf{Fields}}{\int} 
     \exp(i S(\phi)) \, d \mu(\phi)
    &
    \colon
    &
    Bord_n^\otimes
     &\stackrel{\exp(i S)\, d\mu}{\to}& 
    Corr_n^{or}\left(\mathbf{H}_{/\mathbf{B}^n U(1)}\right)^\otimes
    &\stackrel{\int (-) }{\to}&
    \left(
     E Mod^{\Box^n}
    \right)^\otimes
    \\
    && & {}_{\mathllap{Fields}}\searrow & \downarrow
    \\
    && && Corr_n\left(\mathbf{H}\right)^\otimes
  }
  \,.
$$


We realize this now by [[fiber integration in generalized cohomology]].

While traditionally the definition of [[path integral]] is notoriously elusive, here we make use of general abstract but basic facts of [[higher linear algebra]] in a _[[tensor (∞,1)-category]]_ (a [[stable (∞,1)-category|stable]] and [[symmetric monoidal (∞,1)-category|symmetric monoidal]] [[(∞,1)-category]]): the simple basic idea is that

_Cohomological integration_

1. _Fiber integration of $E$-modules along a map is forming the [[dual morphisms]]_ of pulling back $E$-modules.

1. The choice of _measure_ against which one integrates is the choice of identification of [[dual objects]].

More in detail, given a [[monoidal category]] $\mathcal{C}^\otimes$ and given a [[morphism]]

$$
  f \;\colon\; V_1 \to V_2
$$

in $\mathcal{C}$, a _[[fiber integration]]/[[push-forward in generalized cohomology|push-forward]]/[[index|index map]]_ is just

* forming the [[dual morphism]] $f^\vee \colon V_2^\vee \to V_1^\vee$;

* such that [[equivalences]] $V_i^\vee \simeq V_i$ exhibiting self-[[dual objects]] exist ([[Poincaré duality]]) and have been chosen ([[orientation in generalized cohomology|orientation]]).

This allows in total to have a morphism between the same objects, but in the opposite direction

$$
  f^! 
   \;\colon\;
  V_2
   \stackrel{\;\simeq\;}{\to} 
  V_2^\vee
   \stackrel{\; f^\vee \;}{\to}
  V_1^\vee
    \stackrel{\; \simeq \;}{\to}
  V_1
  \,.
$$

That this is also the mechanism of [[fiber integration in generalized cohomology]] is almost explicit in the literature ([[Alexander-Whitehead-Atiyah duality]]), if maybe not fully clearly so. The statement is discussed explicitly in ([Nuiten 13, section 4.1](#Nuiten13)).

First, the basic example to keep in mind is integration in [[ordinary cohomology]]. Write $E = H R = H \mathbb{C}$ for the [[Eilenberg-MacLane spectrum]] of the [[complex numbers]]. Then for $X$ a manifold, the [[mapping spectrum]] 

$$
  H R^\bullet(X)
  \coloneqq
  [X,H R]
$$

is the [[ordinary cohomology]] of $X$, its dual the [[ordinary homology]], with [[coefficients]] in $R$.

For $X$ a [[closed manifold]], [[Poincaré duality]] asserts that  $H R^\bullet(X) \in H R Mod$ is essentially a self-[[dual object]], except for a shift in degree: a choice of [[orientation]] of $X$ induces an [[equivalence]]

$$
  H R^\bullet\left(X\right)
    \underoverset{\simeq}{\;\; PD_X\;\;}{\to} 
  \left( 
   H R^{\bullet+ dim(X)}\left(X\right)\right)^\vee
  \simeq
  H R_{\bullet + dim(X)}\left(X\right)
  \,.
$$

Using this, for $f \colon X \to Y$ a map of [[closed manifolds]] of [[dimension]] $d$, a compatible choice of [[orientation]] of both $X$ and $Y$ induces from the canonical push-forward map $f_\ast$ on homology the [[Umkehr map]]/push-forward map on cohomology, by the composition

$$
  f^!
  = 
  \int_f
    \;\colon\;
  H R^\bullet(X)
   \underoverset{\simeq}{\;PD_X\;}{\to}
  H R_{\bullet + dim(X)}(X)
   \stackrel{\; f_\ast \;}{\to}
  H R_{\bullet + dim(X)}(Y)
   \underoverset{\simeq}{\;PD_Y^{-1}\;}{\to}
  H R^{n-(dim(X)-dim(Y))}(Y)
  \,.
$$

This is ordinary [[integration]]: if $X$ and $Y$ are [[smooth manifolds]], then $H \mathbb{R}^\bullet(X)$ is modeled by [[differential forms]] on $X$, $PD_X$ is given by a choice of [[volume form]] and $f^! = \int_{f}$ is ordinary [[integration of differential forms]]. 

The shift in degree here seems to somewhat break the simple pattern. In fact this is not so, if only we realize that since we are working over spaces $X$, we should use a _relative/fiberwise_ point of view and regard not duality in $E Mod$ itself, but in the functor categories $Func(X, E Mod)$, which is fiberwise duality in $E Mod$.

Accordingly, given an $E$-[[(∞,1)-module bundle]]

$$
  \chi \;\colon \;  X \to E Mod
$$

we form not just the mapping space $E^\bullet(X) = [X, E]$ as above, but form the space of [[sections]] of this bundle, which we write:

$$
  E^{\bullet + \chi}(X) \coloneqq \Gamma_X(\chi)
$$

Here for $X$ a [[discrete ∞-groupoid]]

$$
  \Gamma_X(\chi) \coloneqq [\underset{\to}{\lim} \chi, E]
  \,.
$$

Consider now a morphism 

$$
  \array{
    X && \stackrel{f}{\to} && Y
    \\
    & {}_{\mathllap{f^\ast \chi}}\searrow &\swArrow& \swarrow_{\mathrlap{\chi}}
    \\
    && E Mod 
  }
$$

along which we want to integrate, whith $\chi$ invertible in $Func(Y, E Mod)$: $\left(\chi^\vee\right)^\vee \simeq \chi$.
 $\left(\chi^\vee\right)^\vee \simeq \chi$.

Observe that we have the pair of [[adjoint triples]] of left/right [[Kan extensions]] and [[colimits]]/[[limits]]

$$  
  \array{
    X &\stackrel{f}{\to}& Y &\stackrel{p}{\to}& \ast
    \\
    \\
    Func(X, E Mod)
     &\stackrel{\overset{f_!}{\to}}{\stackrel{\overset{f^\ast}{\leftarrow}}{\underset{f_\ast}{\to}}}
     &
    Func(Y, E Mod)
     &\stackrel{\overset{p_!}{\to}}{\stackrel{\overset{p^\ast}{\leftarrow}}{\underset{p_\ast}{\to}}}
    &
    E Mod
  }
  \,.
$$

Notice that $f^\ast$ preserves duals, but $f_!$ may not. 

If $f_! f^\ast \chi^\vee$ is a [[dualizable object]], say that a *choice of twisted orientation* of $f$ in $\chi$-[[twisted cohomology]] is a choice of $\beta \colon X \to E Mod$ together with a choice of an [[equivalence]] (if such exists) of the form

$$
  PD 
   \;\colon \;
  \left( f_! f^\ast \chi^\vee
  \right)^\vee
  \simeq
  f_!\left(
    f^\ast \chi + \beta
  \right)
  \,,
$$

hence a choice of correction of $f_!$ preserving the duality of $f^\ast \chi$.
 

Then the $(f_! \dashv f^\ast)$ [[counit of an adjunction|counit]]

$$
  f_! f^\ast \chi^\vee \to  \chi^\vee
$$

induces the [[dual morphism]]

$$
  \chi 
    \longrightarrow
  \left(f_! f^\ast \chi^\vee \right)^\vee 
    \underoverset{\simeq}{PD}{\longrightarrow}
  f_!\left(
    f^\ast \chi + \beta
  \right)
$$

and under $\left[ p_! \left( - \right), E \right]$ this becomes

$$
  \left[p_! f_! \left(f^\ast \chi + \beta\right), E\right]
  \longrightarrow
  \left[p_! \chi , E\right]
$$

which is 

$$
  \int_f
  \;\colon \;
  E^{\bullet + f^\ast \chi + \beta}(X)
  \longrightarrow
  E^{\bullet + \chi}(Y)
  \,.
$$

This we may call the _[[twisted cohomology|twisted]] [[fiber integration in generalized cohomology|fiber integration]] along $f$_ in $E$-[[cohomology]], or the _twisted $E$-[[index]] map_ of $f$_, induced by $(\beta, PD)$. If $\beta = 0$ then we call $PD$ an _[[orientation in generalized cohomology|orientation]]_ of $f$ in $\chi$-twisted cohomology.


Notice that

* Under fiber integration in [[twisted cohomology]], the twist may change.

* Grading in cohomology is just one incarnation of twist. Hence the fact that the twist changes under duality was already seen above in the ordinary case of [[Poincaré duality]] in [[ordinary cohomology]]. 

* For the special case that $X$ is a [[manifold]], [[Atiyah duality]] identifies the dual cohomology spectrum with the [[Thom space]] cohomology spectrum. Then a choice of orientation amounts to a choice of [[Thom isomorphism]], as traditionally considered.






### 5. Examples
 {#ExpositionExamples}

Here we survey some examples of cohomological quantization. See ([Nuiten 13, section 5](#Nuiten13)).

$\,$

The traditional input for [[quantization]] is a  _[[phase space]]_
represented by a [[symplectic manifold]]. In the notation used here this data is an object
$\left[\array{X \\ \downarrow^{\mathrlap{\omega}} \\ \Omega_{cl}^2 }\right]$ in the [[slice (∞,1)-topos]] over the [[sheaf]] of closed [[differential 2-forms]].

The lack of traditional [[geometric quantization]] to act [[functor|functorially]] on such data has become proverbial.
An old proposal for how to deal with this ([H&#246;rmander 71](#Hoermander71), [Weinstein 71](#Weinstein71)) is to consider [[morphisms]] between [[phase spaces]]/[[symplectic manifolds]] $(X_1, \omega_1) \to (X_2, \omega_2)$ to be given by _[[Lagrangian correspondences]]_, hence [[Lagrangian submanifolds]] in $(X_1 \times X_2, p_1^\ast \omega_1 - p_2^\ast \omega_2 )$, or some "perturbation" thereof.

Observe that such [[Lagrangian correspondences]] are indeed [[correspondences]] in the [[slice (∞,1)-topos]] $\mathbf{H}_{/\Omega^2_{cl}}$, namely [[diagrams]] in $\mathbf{H}$ of the form

$$
  \array{
    && Z
    \\
    & {}^{\mathllap{i_1}}\swarrow && \searrow^{\mathrlap{i_2}}
    \\
    X_1 && {i_1^\ast \omega_1 = i_2^\ast \omega_2} && X_2
    \\
    & {}_{\mathllap{\omega_1}}\searrow && \swarrow_{\mathrlap{\omega_2}}
    \\
    && \Omega^2_{cl}
  }
  \,.
$$


Notice that a _[[prequantization]]_ of $(X,\omega)$ is a lift $\nabla$ in

$$
  \array{
    && \mathbf{B}U(1)_{conn}
    \\
    & {}^{\mathllap{\nabla}}\nearrow & \downarrow^{\mathrlap{F_{(-)}}}
    \\
    X &\stackrel{\omega}{\to}& \Omega^2_{cl}
  }
  \,.
$$

Given such for $\omega_1$ and $\omega_2$, we may take a  _prequantized_ Lagrangian correspondence to be a factorization of the above through the [[curvature]] map $F_{(-)}$ 

$$
  \array{
    && Z
    \\
    & {}^{\mathllap{i_1}}\swarrow && \searrow^{\mathrlap{i_2}}
    \\
    X_1 && \swArrow_{\simeq} && X_2
    \\
    & {}_{\mathllap{\nabla_1}}\searrow && \swarrow_{\mathrlap{\nabla_2}}
    \\
    && \mathbf{B}U(1)_{conn}
    \\
    && \downarrow^{\mathrlap{F_{(-)}}}
    \\
    && \Omega^2_{cl}
  }
$$

This now yields a [[correspondence]] in $\mathbf{H}_{/\mathbf{B}U(1)}$. So we might be inclined to apply cohomological quantization to this.

Since by the degree of $\mathbf{B}U(1)$ this is going to be a 1-dimensional theory, one is inclined to linearize in $E = H \mathbb{C}$, the [[ordinary homology]] [[Eilenberg-MacLane spectrum]].

However, [[ordinary cohomology]] does not receive a twist from $\mathbf{B}U(1)$, it receives a twist instead from [[flat connections]] $\flat \mathbf{B}U(1)$

$$
  \flat U(1) \longrightarrow GL_1(H\mathbb{C})
  \,.
$$

This means we could $H\mathbb{C}$-linearize the above prequantized [[Lagrangian correspondence]] only if $\nabla$ is flat. But since $\omega$ is the [[curvature]] of $\nabla$, that is precisely not the case of interest.

What looks like a failure here right away, contains in it the seed of the [[holographic principle|holographic]] aspect of motivic quantization which controls all the typical examples: if we need to quantize over $\mathbf{B}U(1)$-coefficients and cannot in full codimension, then we can maybe make the system a [[boundary field theory]] of a higher dimensional system which we can quantize over $\mathbf{B}^2 U(1)$.

This turns out to be the case, indeed.

The canonical [[2d Chern-Simons theory]] induced by a [[symplectic manifold]], or more generally by a [[Poisson manifold]] $(X,\pi)$, is the [[non-perturbative quantum field theory|non-perturbative]] version of the [[Poisson sigma-model]]. Its [[moduli stack]] of fields is the [[symplectic groupoid]] $\mathbf{2dCSFields}(X,\pi)$. This carries a canonical [[prequantum 2-bundle]]
$
  \left[
    \array{
     \mathbf{2dCSFields}(X,\pi)
     \\
     \downarrow^{\mathrlap{\exp\left(i S_{2dCS}\right)}}
     \\
     \mathbf{B}^2 U(1)
   }
  \right]
  \,,
$ see at _[[extended geometric quantization of 2d Chern-Simons theory]]_.

One finds that the original [[Poisson manifold]] is canonically a boundary [[brane]] for this [[2d Chern-Simons theory]], witnessed by a boundary [[correspondence]] like this:

$$
  \array{
    && X
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow && \mathbf{2dCSFields}(X,\pi)
    \\
    & \searrow && \swarrow
    \\
    && \mathbf{B}^2 U(1)
  }
  \,.
$$

This now is canonically $E$-linearized with $E \coloneqq $ [[KU]] the [[complex K-theory]] spectrum.

$$
  \array{
    && X
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow && \mathbf{2dCSFields}(X,\pi)
    \\
    & \searrow && \swarrow
    \\
    && \mathbf{B}^2 U(1)
    \\
    && \downarrow^{\mathrlap{\rho}}
    \\
    && K U Mod
  }
  \,.
$$

One finds that if $(X, \pi) = (X, \omega^{-1})$ is actually a [[symplectic manifold]], then $\mathbf{2dCSFields}(X,\omega^{-1}) \simeq \ast$. In this symplectic case the above is

$$
  \array{
    && X
    \\
    & \swarrow &\downarrow^{\xi}& \searrow^{p}
    \\
    \ast &\leftarrow & \mathbf{B}U(1) &\rightarrow& \ast
    \\
    & \searrow && \swarrow
    \\
    && K U Mod
  }
$$

and encodes an ordinary [[prequantum line bundle]] $\xi$ on $X$, but now regarded as a boundary condition for the [[2d Chern-Simons theory]]. 

A choice of [[orientation]]/[[measure]] in $E = KU$ [[cohomology theory]], hence a [[K-orientation]],  now is a choice of [[spin^c structure]] on $X$. If in the traditional [[geometric quantization]] step $(X,\omega)$ is equipped with a [[Kähler polarization]], then the underlying [[almost complex structure]] canonically yields such (as discussed there).

With such a [[K-orientation]] chosen, the pull-push/fiber-integration/index-map quantization is then

$$
  KU^\bullet(\ast) 
   \stackrel{\xi}{\to}
  KU^\bullet(X)
   \stackrel{ind_X}{\to}
  KU^\bullet(\ast)
$$

which  is the [[index]] of the [[prequantum line bundle]]. Standard (but maybe not so widely known) facts about [[geometric quantization]] (see there) say that this agrees with the traditional quantization via holomorphic sections of the [[Kähler polarization]].

Hence we accurately recover the modern version of [[geometric quantization]]  of [[symplectic manifolds]] by quantizing a [[boundary]] [[brane]] of the [[2d Chern-Simons theory]] induced from the [[Poisson sigma-model]]. Moreover, by extension we find this way a [[geometric quantization]] of [[Poisson manifolds]], too. Notice that this state of affairs is in complete analogy with the way the [[formal deformation quantization]] of [[Poisson manifolds]] via [[Kontsevich formality]] had been recognized by Cattaneo-Felder to be secretly given by the [[n-point function|3-point function]] of the [[open string]] in the [[perturbation theory]] of the  [[Poisson sigma-model]]. Here we see a [[non-perturbative field theory|non-perturbative]] and non-formal (not just infinitesimal) analog of this situation.

So far this produces just the [[space of quantum states]]. But if there is a [[Hamiltonian action]] of a group $G$ on $X$, then we get instead a similar boundary [[correspondence]], but now of the associated [[quotient stacks]], 

$$
  \array{
    && X//G
    \\
    & \swarrow && \searrow^{i}
    \\
    \ast && \swArrow_{\nabla//G} && \ast//G
    \\
    & \searrow && \swarrow
    \\
    && \mathbf{B}^2 U(1)_{conn^1}
  }
  \,.
$$

Now pull-push is in [[groupoid K-theory]], hence in [[equivariant K-theory]] and lands in the [[representation ring]] of $G$. As such it produces [[space of quantum states]] _equipped_ with an [[action]] of the the $G$-[[quantum observables]]. For more on this see below at _[Quantum observables and equivariant K-theory](#QuantumObservablesAndEquivariantKTheory)_.

Passing away from symplectic manifolds: among non-symplectic [[Poisson manifolds]] of particular interest are the [[Lie-Poisson structures]] on the linear dual $\mathfrak{g}^\ast$ of a [[Lie algebra]] $\mathfrak{g}$. Here the corresponding [[symplectic groupoid]] is

$$
  \mathbf{2dCSFields}(\mathfrak{g}^\ast)
  \simeq
  \mathfrak{g}^\ast//G
$$

the [[quotient stack]] of the [[coadjoint action]] of the [[Lie group]] $G$ on $\mathfrak{g}$. 

This is in a way a "dictionary theory" that contains plenty of interesting [[symplectic manifolds]], namely the regular [[coadjoint orbits]] $\mathcal{O} \hookrightarrow \mathfrak{g}^\ast$.

Taken together this produces a [[defect QFT|defect]] between [[boundary field theories]] for the [[2d Chern-Simons theory]] induced by $\mathfrak{g}^\ast$:

$$
  \array{
    \ast &\leftarrow& \ast &\to& \ast && trivial\,theory
    \\
    \uparrow && \uparrow && \uparrow
    \\
    \mathcal{O}_\lambda//G &\leftarrow& \mathcal{O}_\lambda &\hookrightarrow& \mathfrak{g}^\ast && boundary
    \\
    \downarrow && \downarrow &(pb)& \downarrow
    \\
    \ast//G &\leftarrow& \mathcal{O}_\lambda // G &\hookrightarrow& \mathfrak{g}^\ast//G  && 2d CS 
    \\
    \,
    \\
    2d CS && defect && 2d CS
  }
$$

The higher [[quantum propagator]] given by  pull-push/index quantization through the bottom correspondence here yields the "universal [[orbit method]]". See below at _[Quantization of Lie-Poisson structures](#QuantizationOfLiePoissonStructure)_.

A similar defects-of-boundaries diagram is obtained when we do consider [[Lagrangian correspondences]] ([[QFT with defects|defects]]) between [[symplectic manifolds]] after all, but now with the latter correctly understood as themselves already being boundaries of [[2d Chern-Simons theory]].

Notice that all this quantizes the [[particle]] at the boundary of the [[open string|open]] [[topological string]] given by [[2d Chern-Simons theory]]. 

Therefore it is natural to consider instead the [[open string|open]] [[type II superstring]] on a [[spacetime]] $X$ with [[background gauge field]] a [[B-field]] $\chi \colon X \to \mathbf{B}^2 U(1)$. Then the analogous boundary condition is a [[D-brane]] with [[worldvolume]] $Q \hookrightarrow X$ equipped with a [[Chan-Paton gauge field]] $\xi$, which constitutes a boundary [[correspondence]] of the form

$$
  \array{  
    && Q
    \\
    & \swarrow && \searrow^{\mathrlap{i}}
    \\
    \ast && \swArrow_{\xi} && X
    \\
    & \searrow && \swarrow_{\mathrlap{\chi}}
    \\
    && \mathbf{B}^2 U(1)
  }
  \,.
$$

Here now the twisted [[fiber integration]]/[[index]] map comes out as

$$
  ind_i 
  \;\colon\;
  KU^{\bullet + i^\ast \chi - W_3(N_i Q)}(Q)
  \longrightarrow
  KU^{\bullet + \chi}(X)
$$

where $W_3(N_i Q)$ is the third [[integral Stiefel-Whitney class]] of the [[normal bundle]] of the [[D-brane]] in [[spacetime]]. Regarded as a [[quantum propagator]] this sends the $i^\ast \chi - W_3(N_i Q)$-[[twisted K-theory]] of the D-brane to the $\chi$-twisted K-theory of [[spacetime]]. One recognizes here

* the condition that the domain are [[Chan-Paton gauge fields]] in $i^\ast \chi - W_3(N_i Q)$-[[twisted K-theory]] is the _[[Freed-Witten-Kapustin anomaly]]_ cancellation condition;

* the image of this higher [[quantum propagator]] is the _[[D-brane charge]]_.


Notice that by the above analogous discussion of the [[2d Chern-Simons theory]] we have the slogan:

* [[D-brane charge]] = [[partition function]] of [[charged particle]] at the end of the [[open string]].

In view of this state of affairs one is to go up in dimension and quantize a 2-dimensional field theory, namely the [[string]] [[sigma model]] itself, once we canonically realize it as the boundary of a 3-dimensional field theory which is equipped with a suitable $E$-linearization. 

A natural example for this is the [[heterotic string]] [[sigma model]] on the boundary of the [[M2-brane]] in the [[M9-brane]] inside the [[Hořava-Witten theory]] [[spacetime]] of [[11-dimensional supergravity]], see [below](#HeteroticStringAtBoundaryOfMembrane). 

The [[supergravity C-field]] is now the [[higher prequantum bundle]] and is naturally turned into a [[higher prequantum line bundle|higher prequantum E-line bundle]] for $E = $ [[tmf]].

The corresponding [[orientation]] now is the [[string^c structure]] induced by the [[supergravity C-field]] which is naturally implied by the flux quantization condition in [[11-dimensional supergravity]]. On the [[M9-brane]] this induces the [[twisted differential string structure]] which is the [[Green-Schwarz anomaly]] cancellation condition in [[heterotic string theory]]. The corresponding [[fiber integration]]/[[index]] now is in (twisted) [[tmf]] the (twisted) [[Witten genus]]. This is, by [[Edward Witten]]'s original Fields medal winning discovery, indeed the [[partition function]] of the [[heterotic string]] 2d [[sigma-model]].

In this fashion one can now in principle climb higher up the dimensional ladder and quantize ever higher dimensional field theories, for instance by $E$-linearizing with $E$ a [[Morava K-theory]] (and hence after generalizing the formalism to [[A-infinity rings]]...)  

(Next interesting along these lines might be the holographic motivic quantization analogously of the [[Yang monopole]] at the boundary of the [[M5-brane]] ending on the [[M9-brane]]. )


The earliest and by far best understood example of the [[holographic principle]] is the [[AdS3-CFT2 and CS-WZW correspondence]] between the [[WZW model]] on a [[Lie group]] $G$ and 3d $G$-[[Chern-Simons theory]].

In ([Witten 98](7d+Chern-Simons+theory#Witten98)) it is argued that all examples of the [[AdS-CFT duality]] are governed by the [[schreiber:infinity-Chern-Simons theory|higher Chern-Simons theory]] terms on the gravity side, hence that the corresponding conformal theories are higher analogs of the WZW model: [[schreiber:∞-Wess-Zumino-Witten theory]]-type models.

In particular for [[AdS7-CFT6]] this means that the [[6d (2,0)-superconformal QFT]] on the [[M5-brane]] [[worldvolume]] should be a 6d-dimensional WZW model holographically related to the [[7d Chern-Simons theory]] which appears when [[11-dimensional supergravity]] is [[KK-reduction|KK-reduced]] on a 4-[[sphere]]:

| [[schreiber:∞-Chern-Simons theory]] | $\leftarrow$[[holographic principle]]$\rightarrow$ | [[schreiber:∞-Wess-Zumino-Witten theory]] |
|---|---|---|
| 3d [[Chern-Simons theory]] |  | 2d [[Wess-Zumino-Witten model]] |
| [[7d Chern-Simons theory]] from [[11-dimensional supergravity]] |  | [[6d (2,0)-superconformal QFT]] on [[M5-brane]] |

In ([Witten 96](http://ncatlab.org/nlab/show/7d+Chern-Simons+theory#WittenI)) this is argued, by [[geometric quantization]], for the _bosonic and abelian_  contribution in [[7d Chern-Simons theory]]. (The subtle [[theta characteristic]] involved was later formalized in [[Quadratic Functions in Geometry, Topology, and M-Theory|Hopkins-Singer 02]].) 

In ([Fiorenza-Sati-Schreiber 12a](#FSS12a), [Fiorenza-Sati-Schreiber 12b](#FSS12b)) the bosonic but _non-abelian_ quantum correction to the [[7d Chern-Simons theory]] induced by 11d Sugra is considered, and refined to a [[local action functional]] along the lines considered here. Therefore by ([Witten 98](#Witten98)) the corresponding [[schreiber:∞-Wess-Zumino-Witten theory]] should be the bosonic and nonabelian part of the [[6d (2,0)-superconformal QFT]] on the [[M5-brane]] [[worldvolume]].

To see this, what one needs is evidently a general formalization of [[holography]] for [[local prequantum field theory]] as these. How are [[schreiber:∞-Wess-Zumino-Witten theory]]-models higher holographic boundaries of [[schreiber:∞-Chern-Simons theory]]?

At the level of [[local prequantum field theory]] this is answered in ([Fiorenza-Sati-Schreiber 13](#FiorenzaSatiSchreiber13)):

$$
  \mu \;\colon\; \mathfrak{g} \longrightarrow \mathbb{R}[n]
$$

be a [[super L-∞ algebra]] [[L-∞ cocycle]]. Let 

$$
  \mathbf{c} \;\colon\; \mathbf{B}G \longrightarrow \mathbf{B}^{n+1}(\mathbb{R}/\Gamma)
$$

be its [[Lie integration]] in [[smooth super ∞-groupoids]], according to ([Fiorenza-Schreiber-Stasheff 10](#FiorenzaSchreiberStasheff10)). 

Observe that the [[smooth ∞-group]] $G$ has, by [[cohesion]], a canonical higher [[Maurer-Cartan form]]

$$
  \theta \;\colon \; G \longrightarrow \flat_{dR}\mathbf{B}G
  \,. 
$$

This is a [[cocycle]] in the nonabelian de Rham [[hypercohomology]] of $G$. We want an [[schreiber:∞-Wess-Zumino-Witten theory]] model with a _globally defined_ [[curvature]] $(n+1)$-form. Therefore consider the [[universal construction|universal]] solution $\tilde G$ of making $\theta$ globally well defined, hence the [[homotopy pullback]]

$$
  \array{
    \tilde G &\stackrel{\theta_{global}}{\to}& \Omega_{flat}(-,\mathfrak{g})
    \\
    \downarrow && \downarrow
    \\
    G &\stackrel{\theta_G}{\to}& \flat_{dR} \mathbf{B}G
  }
  \,.
$$

Then one observes that by [[cohesion]] the [[pasting]] diagram on the right of the following exists, and hence defines a [[local action functional]] $\exp(i S_{WZW})$ by the universal factorization on the left. This is the [[schreiber:∞-Wess-Zumino-Witten theory]] induced by the [[L-∞ cocycle]] $\mu$:

$$
  \array{
    && \tilde G
    \\
    & \swarrow &\downarrow^{\exp(i S_{WZW})}& \searrow^{\mathrlap{\mu(\theta_{global})}}
    \\
    \ast &\leftarrow& \mathbf{B}^n U(1)_{conn} &\rightarrow& \Omega_{cl}^{n+1}
    \\
    & {}_{\mathllap{0}}\searrow && \swarrow
    \\
    && \flat \mathbf{B}^{n+1}U(1)
  }
  \;\;\coloneqq\;\;
  \array{
    && && \tilde G
    \\
    && & \swarrow && \searrow^{\mathrlap{\theta_{global}}}
    \\
    && G && && \Omega_{flat}(-,\mathfrak{g})
    \\
    & \swarrow && \searrow^{\mathrlap{\theta_G}} && \swarrow && \searrow^{\mathrlap{\mu}}
    \\
    \ast && && \flat_{dR}\mathbf{B}G && && \Omega^{n+1}_{cl}
    \\
    & \searrow && \swarrow && \searrow^{\mathrlap{\flat_{dR}\mathbf{c}}} && \swarrow
    \\
    && \flat \mathbf{B}G && &&\flat_{dR} \mathbf{B}^{n+1}U(1)
    \\
    && & {}_{\mathllap{\exp(i S_{CS}^{flat})}}\searrow^{\mathrlap{\flat \mathbf{c}}} && \swarrow
    \\
    && && \flat \mathbf{B}^{n+1}U(1)
  }
  \,.
$$

This uses the following general fact about how [[local action functionals]] $\mathbf{Fields} \longrightarrow \mathbf{B}^n U(1)_{conn}$ are themselves boundary conditions for what one might call _universal higher [[topological Yang-Mills theory]]_ ([Nuiten-Schreiber 13](#lpqft)), the theory given by the local action functional

$$
  \exp(i S_{tYM})
  \;\colon\;
  \mathbf{Fields}_{tYM} = \Omega^{n+1}_{cl}
  \longrightarrow 
  \flat \mathbf{B}^{n+1}U(1)
  \,,
$$

which is just the canonical inclusion of closed differential $(n+1)$-forms into the universal moduli stack of flat [[circle n-bundle with connection|circle (n+1)-bundles with connection]]. By the [[universal property]] of [[ordinary differential cohomology]] one finds that boundary conditions for this somewhat degenerate theory are precisely differential cocycles:

$$
  \array{   
    && \mathbf{Fields}_{boundary}
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow && \Omega_{cl}^{n+1}
    \\
    & \searrow && \swarrow
    \\
   && \flat \mathbf{B}^{n+1}U(1)
  }
  \;\;\;
  \simeq
  \;\;\;
  \array{   
    && \mathbf{Fields}_{boundary}
    \\
    & \swarrow &\downarrow^{\exp(i S_{bdr})}& \searrow
    \\
    \ast &\leftarrow& \mathbf{B}^n U(1)_{conn} &\stackrel{F_{(-)}}{\to}& \Omega_{cl}^{n+1}
    \\
    & \searrow && \swarrow
    \\
   && \flat \mathbf{B}^{n+1}U(1)
  }
  \,.
$$


One then shows ([Fiorenza-Sati-Schreiber 13](#FiorenzaSatiSchreiber13)) that for $\mu$ the exceptional  cocycles on the [[super Poincare Lie algebra]] and their higher extensions such as notably the [[supergravity Lie 3-algebra]] and [[supergravity Lie 6-algebra]],
that the [[schreiber:∞-Wess-Zumino-Witten theory]] models obtained this way reproduce the [[Green-Schwarz action functional]] "old [[brane scan]]" including for instance the [[heterotic string]] [[sigma-model]] and the [[M2-brane]] [[sigma-model]], and also encodes the branes with tensor multiplet fields such as the [[D-branes]] and the single (abelian) [[M5-brane]].

So now one just needs to put the pieces toghether with the nonabelian [[7d Chern-Simons theory]] correction  and apply holographic boundary motivic quantization. This however is to be disucssed elsewhere. 




## General abstract type theoretic summary
 {#GeneralAbstractTypeTheoreticSummary}


We give a summary of the central steps of motivic quantization of local prequantum field theory in general abstract terms of [[homotopy type theory]], hence in the [[internal language]] of [[(∞,1)-toposes]], following the idea of _[Synthetic quantum field theory](#SyntheticQuantumFieldTheory)_. This is to bring out the sheer conceptual simplicity underlying the process.

* **(QFT 0)** _The gauge principle_: The ambient [[theory]] is a [[homotopy type theory]] $\mathbf{H}$.

  This encodes the [[gauge principle]].

* **(QFT 1)** _Phases and action functionals_: The [[homotopy type theory]] $\mathbf{H}$ is [[differential cohesion|differentially]] [[cohesive]], hence equipped with [[higher modalities]]  $(\Pi \dashv \flat \dashv \sharp)$ ([[shape modality]], [[flat modality]], [[sharp modality]]) and $(\Re \dashv \Im \dashv \&)$ ([[reduction modality]], [[infinitesimal shape modality]], [[infinitesimal flat modality]]). 

  This induces for every choice of [[abelian ∞-group]] $\mathbb{G}$ the [[moduli ∞-stack|universal moduli]] $\mathbf{B}\mathbb{G}_{conn}$ of $\mathbb{G}$-[[principal ∞-connections]].

  Here $\mathbb{G}$ is a choice of [[phase and phase space in physics|phases]].

   We say that $\mathbf{H}$ is a context for [[local prequantum field theory]].

   The [[context]] of such, hence the the [[slice (∞,1)-topos|slice homotopy theory]] $\mathbf{H}_{/\mathbf{B}\mathbb{G}_{conn}}$, is the context of [[local action functionals]] assigning [[phase and phase space in physics|phases]] in $\mathbb{G}$. 

   A [[type]] in this [[context]] is such a [[local action functional]] $\left[\array{\mathbf{Fields} \\ \downarrow^{\mathrlap{\exp(i S)}} \\ \mathbf{B}\mathbb{G}_{conn} }  \right]$. Its [[dependent sum]] to the ambient context is the [[moduli ∞-stack]] of [[field (physics)|fields]], $\mathbf{Fields} \coloneqq \underset{\mathbf{B}\mathbb{G}_{conn}}{\sum} \exp(i S)$.

   The [[automorphism ∞-groups]] $\mathbf{Aut}(\exp(i S))$ of these [[types]] $\exp(i S) \in \mathbf{H}_{/\mathbf{B}\mathbb{G}}_{conn}$ are equivalently

   * the [[quantomorphism ∞-groups]] containing the [[Heisenberg ∞-groups]], whose [[Lie differentiation]] are the [[Poisson L-∞ algebras]] and [[Heisenberg L-∞ algebras]]; 

   * the [[∞-groups]] of higher [[conserved currents]];

   of the local prequantum field theory $\exp(i S)$.

* **(QFT 2)** _Superposition principle and wavefunctions_: To choose a _[[superposition principle]]_ in the [[context]] $\mathbf{H}_{/\mathbf{B}\mathbb{G}}_{conn}$ is to choose a function [[function]] $\rho \colon \mathbf{B}\mathbb{G} \longrightarrow \mathbf{B}GL_1(E)$ to the [[delooping]] of the [[∞-group of units]] of an  [[E-∞ ring|commutative ring]] type $E \in CRing_\infty(\mathbf{H})$.

   Given a [[superposition principle]] $\rho$, the [[dependent sum]] of a [[local action functional]] along it is the [[higher prequantum line bundle|higher prequantum E-line bundle]] $L \coloneqq \underset{\rho}{\sum} \exp(i S) \in \mathbf{H}_{/\mathbf{B}GL_1(E)}$. 

   A [[section]] of the [[higher prequantum line bundle]] is a [[wavefunction]] and the $E$-[[∞-module]] which is the [[space of sections]] $E^{\bullet + L}(\mathbf{Fields})$ is the [[space of quantum states]].

* **(QFT 3)** _Quantization and path integral_: A [[relation]] $\exp(i S_{traj}) \to \exp(i S_{in}) \times \exp(i S_{out})$ in the local prequantum field theory context $\mathbf{H}_{/\mathbf{B}\mathbb{G}_{conn}}$ is a [[space]] of [[trajectories]] equipped with [[probability amplitudes]]. Its [[dependent sum]] $L_{traj} \to L_{in} \times L_{out}$ along $\rho$ is the corresponding [[integral kernel]], as is its image under $\Gamma$.

   A choice of self-[[dual object|duality]] on the correspondence $E$-module $E^{\bullet + L_{traj}}(\mathbf{Fields}_{traj})$ is  a [[path integral]] [[measure]] $d \mu_{traj}$. The [[obstruction]] to its existence is the [[quantum anomaly]]. 

   A choice of $d\mu_{traj}$ induces a [[linear function]] 

   $$
     \underset{\phi \in \mathbf{Fields}_{traj}}{\int} 
      \exp(i S_{traj}(\phi)) d \mu_{traj}(\phi)
      \;
     \colon  
      \;
     E^{\bullet + L_{in}}(\mathbf{Fields}_{in}) \to E^{\bullet + L_{out}}(\mathbf{Fields}_{out})
   $$ 

   by passing to [[dual morphisms]]. This is the [[quantum propagator]] given by [[path integral as a pull-push transform|pull-push path integral]] [[quantization]] of $\exp(i S_{traj}) d\mu_{traj}$.


## **I)** General theory
 {#GeneralTheory}

Here we describe technical details of motivic quantization.

We first set up some

* _[Basic notions](#BasicNotions)_ 

of [[higher category theory]] that we need. Then we introduce the three steps that constitute motivic quantum theory: 

1. _[Correspondences and local quantum field theory](#CorrespondencesAndLocalPrequantumFieldTheory)_

1. _[Bivariant cohomology and the superposition principle](#BivariantCohomologyAndTheSuperpositionPrinciple)_

1. _[Push-forward in cohomology and path integral quantization](#PushForwardInCohomologyAndPathIntegralQuantization)_ .

Readers already familar with the higher category theory notation that we happen to use may take the following as the lighning summary of the definition: the whole process that we describe is going to be summarized by the following diagram of [[monoidal (∞,n)-categories]].

$$
  \array{
    && Corr^{or}_n(\mathbf{H}_{/\mathbf{B}\mathbf{GL}_1(E)})^\otimes 
    &\stackrel{\underset{}{\int} (-)}{\to}& (E Mod^{\Box^n})^{\otimes}
    \\
    & {}^{\mathllap{exp(i S)}}\nearrow & \downarrow
    \\
    Bord_n(def)^\otimes
    &\stackrel{\mathbf{Fields}}{\to}&
    Corr_n(\mathbf{H})^\otimes
  }
$$

The left part of this diagram constitutes the defintion of a [[local prequantum field theory]]: the [[field (physics)|fields]] $\phi \in \mathbf{Fields}$ and the [[local action functional]] $\exp(i S)$ on them. The morphism $\int$ on the right is the map that sends by a [[path integral as a pull-push transform]] correspondences equipped with cocycles to $E$-linear maps of [[∞-modules]]. The resulting composite 

$$
  \underset{\phi \in \mathbf{Fields}}{\int}
  [D\phi] \exp(i S (\phi))
  \;\; \colon \;\;
  Bord_n(def) \to E Mod
$$

is the [[FQFT]] which is the [[quantization]] of the original [[prequantum field theory]].



### Basic notions
 {#BasicNotion}

#### The ambient $\infty$-topos and algebra inside

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]]. Write $(\Pi \dashv \flat \dashv \sharp)$ for the corresponding [[shape modality]], [[flat modality]], [[sharp modality]], respectively.

Write

* $Grp(\mathbf{H}) \coloneqq E_1 Alg^{grp}(\mathbf{H})$ for the [[(∞,1)-category]] of [[∞-group]] objects in $\mathbf{H}$;

* $AbGrp(\mathbf{H}) \coloneqq E_\infty Alg^{grp}(\mathbf{H})$ for its [[full sub-(∞,1)-category]] of [[abelian ∞-groups]];

* $Sp(\mathbf{H})$ for the [[stable (∞,1)-category]] of [[spectrum objects]] in $\mathbf{H}$;

* $CRing(\mathbf{H}) \coloneqq E_\infty Alg(Sp(\mathbf{H}))$ for the [[(∞,1)-category]] of [[E-∞ ring]] objects in $\mathbf{H}$;

* $E Mod(\mathbf{H})$ for the [[symmetric monoidal (∞,1)-category]] of $E$-[[∞-modules]] in $\mathbf{H}$.


#### Correspondences in monoidal $\infty$-toposes

For $\mathbb{G} \in Grp(\mathbf{G}) \stackrel{forget}{\to} \mathbf{H}$ write $\mathbf{H}_{/\mathbb{G}}$ for the [[slice (∞,1)-topos]] of $\mathbf{H}$ over $\mathbb{G}$. This carries apart from its canonical structure of a [[cartesian monoidal (∞,1)-category]] $(\mathbf{H}_{/\mathbb{G}}, \times_{\mathbb{G}})$ also a second structure of a [[symmetric monoidal (∞,1)-category]] $(\mathbf{H}_{/\mathbb{G}}, \otimes_{\mathbb{G}})$, obtained using the monoid structure on $\mathbb{G}$: 

$$
  \left[
    \array{
      X_1
      \\
      \downarrow^{\mathrlap{\chi_1}}
      \\
      \mathbb{G}
   }
  \right]
  \otimes_{\mathbb{G}}
  \left[
    \array{
      X_2
      \\
      \downarrow^{\mathrlap{\chi_2}}
      \\
      \mathbb{G}
   }
  \right]
  \;\;
  \coloneqq
  \;\;
  \left[
    \array{
      X_1 \times X_2
      \\
      \downarrow^{\mathrlap{(\chi_1, \chi_2)}}
      \\
      \mathbb{G} \times \mathbb{G}
      \\
      \downarrow^{\mathrlap{\cdot}}
      \\
      \mathbb{G}
    }
  \right]
  \,.
$$

This makes $(\mathbf{H}_{/\mathbb{G}}, \otimes_{\mathbb{G}})$ a _[[monoidal topos|monoidal (∞,1)-topos]]_.

For $\mathcal{C}$ any [[(∞,1)-category]] with [[(∞,1)-pullbacks]] write $Corr(\mathcal{C})$ for the [[(∞,1)-category of correspondences]] in $\mathcal{C}$, whose [[objects]] are those of $\mathcal{C}$, whose [[morphisms]] are [[diagrams]] in $\mathcal{C}$ of the form

$$
  X_1 \leftarrow Q \rightarrow X_2
$$

and [[composition]] is given by [[(∞,1)-fiber product]] of such diagrams.

If $\mathcal{C}$ is equipped with the stucture of a [[monoidal (∞,1)-category]] $(\mathcal{C}, \otimes)$, then $Corr(\mathcal{C})$ naturally inherits a monoidal structure, too, given by the objectwise [[tensor product]] in $\mathcal{C}$. 

Notice that even if $(\mathcal{C}, \times)$ is a [[cartesian monoidal (∞,1)-category]] then the induced monoidal structure $(Corr(\mathcal{C}), \otimes)$ is _not_ cartesian. Notice also that if $(\mathcal{C}, \otimes)$ is [[symmetric monoidal (∞,1)-category|symmetric monoidal]], then so is the induced structure on $Corr(\mathcal{C})$.

In the following we consider $Corr(\mathbf{H}_{/\mathbb{G}})$ always equipped with the [[monoidal (∞,1)-category]] structure which is induced by the non-cartesian tensor monoidal structure $\otimes_{\mathbb{G}}$ on $\mathbf{H}_{/\mathbb{G}}$.

For $\mathcal{C}$ any [[(∞,1)-category]], write $\mathcal{C}^{\Box^n}$ for the [[(∞,1)-category]] of $n$-dimensional [[cube]] [[diagrams]] in $\mathcal{C}$. Under [[pasting]] of diagrams this is naturally an [[(∞,n)-category]]. 

We write for short

$$
  Corr_n\left(\mathbf{H}_{/\mathbb{G}}\right)
   \;\coloneqq\;
  Corr\left(\mathbf{H}_{/\mathbb{G}}\right)^{\Box^n}
  \,.
$$

This is a [[symmetric monoidal (∞,n)-category]]. 



### **1.)** Correspondences and local prequantum field theory
 {#CorrespondencesAndLocalPrequantumFieldTheory}


+-- {: .num_prop #GroupOfUnitsAdjunction}
###### Proposition

There is a pair of  [[adjoint (∞,1)-functors]]

$$
  CRing(\mathbf{H})
   \stackrel{\overset{\mathbb{S}[-]}{\leftarrow}}{\underset{\mathbf{GL}_1}{\to}}
  AbGrp(\mathbf{H})
$$

where $\mathbf{GL}_1(-)$ forms the [[∞-group of units]] (see there) of an [[E-∞ ring]] object. 

=--



Choose now once and for all 

* $n \in \mathbb{N}$

* $E \in CRing(\mathbf{H})$. 

Write $Bord_n \coloneqq Bord_n(\{\ast\})$ for the [[(∞,n)-category of cobordisms|(∞,n)-category of framed cobordisms]].

By ([Nuiten-Schreiber 13](#lpqft)), following ([Schreiber 08](#Schreiber08), [Freed-Hopkins-Lurie-Teleman 09, section 3](#FreedHopkinsLurieTeleman09)) we say

* a [[field (physics)|physical field]] of a [[local prequantum field theory]] of [[dimension]] $n$ is a [[monoidal (∞,n)-functor]]

  $$
    \mathbf{Fields} \;\colon \; Bord_n^\otimes \to Corr_n\left(\mathbf{H}\right)^\otimes
  $$

* a [[local prequantum field theory]] of [[dimension]] $n$ with field content $\mathbf{Fields}$ and with _[[phase and phase space in physics|phases]]_ in $\mathbf{GL}_1(E)$ is a lift $\exp(i S)$ in the [[diagram]]

  $$
    \array{
      && Corr_n\left(\mathbf{H}_{/\mathbf{B}\mathbf{GL}_1\left(E\right)}\right)^\otimes
      \\
      & {}^{\exp(i S)}\nearrow \;\;\;\;\; & \downarrow
      \\
      Bord_n^\otimes &\stackrel{\mathbf{Fields}}{\to}& Corr_n\left(\mathbf{H}\right)^\otimes
    }
    \,.
  $$

More generally, let $def$ be a set of [[defect QFT|defect]] data, hence a set of shapes of cells. Write $Bord_n(def)$ for the [[(∞,n)-category of cobordisms]] with this defect structure, hence, by the [[cobordism hypothesis]] theorem, the [[symmetric monoidal (∞,n)-category]] with all [[fully dualizable objects]]  freely generated on $def$. Then a diagram of [[symmetric monoidal (∞,n)-categories]] of the form

  $$
    \array{
      && Corr_n\left(\mathbf{H}_{/\mathbf{B}\mathbf{GL}_1\left(E\right)}\right)^\otimes
      \\
      & {}^{\exp(i S)}\nearrow \;\;\;\;\; & \downarrow
      \\
      Bord_n(def)^\otimes &\stackrel{\mathbf{Fields}}{\to}& Corr_n\left(\mathbf{H}\right)^\otimes
    }
  $$

is a [[boundary field theory|boundary]]/[[defect QFT|defect]] [[local prequantum field theory]]. 

For instance for 

$$
  def \coloneqq \{ \emptyset \stackrel{\partial}{\to} \ast \}
$$ 

such $\exp(i S)$ is equivalently the choice of a [[correspondence]] of the form

$$
  \array{
    && \mathbf{Field}^{\partial}
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow_{\xi} && \mathbf{Fields}
    \\
    & \searrow && \swarrow_{\mathrlap{\chi}}
    \\
    && \mathbb{G}
  }
  \,.
$$

This is the local incarnation of the corresponding _[[boundary condition]]/[[brane]]_.

Or if 

$$
  def \coloneqq 
  \left\{
    \left(
      \array{
         \emptyset &\stackrel{}{\to}& \emptyset
         \\
         \downarrow && \downarrow^{\mathrlap{\partial_1}}
         \\
         \emptyset &\stackrel{\partial_2}{\to}& \ast
      }
    \right)
  \right\}
$$

then $Bord_n(def)$ consists of cobordisms with two different boundary ([[brane]]) types and a [[defect QFT|defect]] where they meet.


### **2.)** Bivariant cohomology and the superposition principle
 {#BivariantCohomologyAndTheSuperpositionPrinciple}


Let $E$ be an [[E-∞ ring]], and write $GL_1(E)$ for its [[∞-group of units]]. With $\mathbf{H}$ the ambient [[(∞,1)-topos]], write $\mathbf{H}_{/\mathbf{B}GL_1(E)}$ for the [[slice (∞,1)-topos]] over the [[delooping]] of this [[abelian ∞-group]]. This is the [[(∞,1)-category]] of [[spaces]] equipped with [[(∞,1)-module bundle|(∞,1)-line bundles]] over $E$. Consider an [[(∞,1)-functor]] 

$$
  \Gamma^\ast \;\colon \; \mathbf{H}_{/\mathbf{B}GL_1(E)} \to E Mod
$$

to the [[(∞,1)-category of (∞,1)-modules]] over $E$, which form $E$-modules of co-sections of $E$-[[(∞,1)-module bundles]] (generalized [[Thom spectra]]). 

This is well understood for $\mathbf{H} = $ [[∞Grpd]] in which case $\Gamma \simeq \underset{\to}{\lim} \circ i$ is the [[(∞,1)-functor]] [[homotopy colimits]] in $E Mod$ under the canonical embedding $\mathbf{B} GL_1(E) \simeq E Line \hookrightarrow E Mod$. But one can consider similar constructions $\Gamma$ for more general ambient [[(∞,1)-toposes]] $\mathbf{H}$.

+-- {: .num_defn #BivariantCohomologyByHomsOfCoSections}
###### Definition

For $\chi_i \colon X_i \to \mathbf{B}GL_1(E)$ two [[objects]] of $\mathbf{H}_{/\mathbf{B}GL_1(E)}$, the _$(\chi_1,\chi_2)$-[[twisted cohomology|twisted]] [[bivariant cohomology|bivariant]] $E$-[[cohomology theory|cohomology]]_ on $(X_1,X_2)$ is 

$$
  E^{\bullet + \chi_2 - \chi_1}(X_1,X_2)
  \;\coloneqq\;
  Hom_{E Mod}\left(\Gamma^\ast_{X_1}\left(\chi_1\right), \Gamma^\ast_{X_2}\left(\chi_2\right)\right)
  \in 
  E Mod
  \,.
$$

=--

+-- {: .num_example}
###### Example

By the general discussion at [[twisted cohomology]], following ([ABG, def. 5.1](#ABG)) we have

* for $X_2 = \ast$ the point, the above bivariant cohomology is the $\chi_1$-twisted $E$-cohomology of $X_1$;

  $$
    E^{\bullet + \chi_1}(X_1, \ast) \simeq E^{\bullet + \chi_1}(X_1)
    \,.
  $$

* for $X_1 = \ast$ the point, the above bivariant cohomology is the $\chi_2$-twisted $E$-[[generalized homology|homology]] of $X_2$;

  $$
    E^{\bullet + \chi_2}(\ast, X_2) \simeq E_{\bullet + \chi_2}(X_2)
    \,.
  $$

=--

+-- {: .num_example}
###### Example

[[KK-theory]] is a model for bivariant twisted [[topological K-theory]] over [[differentiable stacks]] (hence 1-truncated suitably representable objects in $\mathbf{H} = $ [[Smooth∞Grpd]], see [Tu-Xu-LG 03](#TuXuLG03)). According to ([Joachim-Stolz 09, around p. 4](#JoachimStolz09)) the category $KK$ first of all is naturally an [[enriched category]] $\mathbb{KK}$ over the category $\mathcal{S}$ of [[symmetric spectra]]  and as such comes with a symmetric [[monoidal functor|monoidal]] [[enriched functor]]

$$
  \mathbb{KK} \to KU Mod
  \,.
$$


This sends an object to its [[operator K-theory]] spectrum, hence to the $E$-[[dual object|dual]] of the $E$-module of co-sections. 

=--

+-- {: .num_remark}
###### Remark

Generally, one may want to consider in def. \ref{BivariantCohomologyByHomsOfCoSections} the dualized co-section functor

$$
  \Gamma = [\Gamma^\ast(-), E] \;\colon\; \left(\mathbf{H}_{/\mathbf{B}GL_1(E)}\right)^{op} \to E Mod
  \,.
$$

=--

+-- {: .num_example}
###### Example

A [[correspondence]] in $\mathbf{H}_{/\mathbf{B}GL_1(E)}$ 

$$
  \array{
    && Q
    \\
    & {}^{\mathllap{i_1}}\swarrow && \searrow^{\mathrlap{i_2}}
    \\
    X_1 && \swArrow_{\xi} && X_2
    \\
    & {}_{\mathllap{\chi_1}}\searrow && \swarrow_{\mathrlap{\chi_2}}
    \\
    && \mathbf{B}GL_1(E)
  }
$$

is a morphism of "twisted $E$-[[pure motive|motives]]" in that it is a [[correspondence]] in $\mathbf{H}$ between the [[spaces]] $X_1$ and $X_2$ equipped with an $(i_1^\ast \chi_1, i_2^\ast \chi_2)$-twisted bivariant $E$-cohomology [[cocycle]] $\xi$ on the correspondence space $Q$. Under the co-sections / [[Thom spectrum]] functor this is sent to a [[correspondence]]

$$
  \Gamma_{X_1}(\chi_1)
  \stackrel{\xi}{\rightarrow}
  \Gamma_Q(i_2^\ast \chi_2)
  \stackrel{i_2^\ast}{\leftarrow}
  \Gamma_{X_2}(\chi_2)
$$

in $E Mod$. If the wrong-way map of this is [[orientation in generalized cohomology|orientable]] in $E$-cohomology then we may form its [[dual morphism]]/[[Umkehr map]] to obtain the corresponding "[[index]]"

$$
  \Gamma_{X_1}(\chi_1)
   \stackrel{(i_2)_! \xi}{\to}
  \Gamma_{X_2}(\chi_2)
$$

in $E Mod$. Identifying correspondences that yield the same "[[index]]" this way yields a presentation of bivariant cohomology by [[pure motive|motive]]-like structures. 
This is how (equivariant) [[bivariant K-theory]] is presented, at least over manifolds, see at _[KK-theory -- References -- In terms of correspondences](KK-theory#ReferencesInTermsOfCorrespondences)_.

=--

### **3.)** Push-forward in cohomology and path integral quantization
 {#PushForwardInCohomologyAndPathIntegralQuantization}


$$
  \array{
    && \mathbf{Trajectories}
    \\
    & {}^{\mathllap{i_1}}\swarrow && \searrow^{\mathrlap{i_2}}
    \\
    \mathbf{Fields}_{in}
    && \swArrow_{\xi} &&
    \mathbf{Fields}_{out}
    \;\;\;\;\;\;\;\;\;\;
    \in \mathbf{H}_{/\mathbf{B}GL_1(E)}
    \\
    & {}_{\chi_{in}}\searrow && \swarrow_{\chi_{out}}
    \\
    && \mathbf{B} GL_1(E)
    \\
    && \downarrow
    \\
    && E Mod
  }
$$

quantizes to

$$
  \Gamma(\chi_{in})
  \stackrel{\;\;\;\;\; \underset{i_2}{\int} i_1^\ast \xi \;\;\;\;\;}{\to}
  \Gamma(\chi_{out})
  \;\;\;\;\;\;\;\;\;
  \in E \mathbf{Mod}
  \,.
$$

(...)


## **II)** Models
 {#Models}

[[!include genera and partition functions - table]]


### Dimension 1 -- Pull-push over $H\mathbb{C}$ and integration of differential forms

We discuss ([[twisted cohomology|twisted]]) [[ordinary homology]] and [[ordinary cohomology]] in terms of sections of [[(∞,1)-module bundles]] over the [[Eilenberg-MacLane spectrum]].

Let $k$ be a [[commutative ring]]. Write 

$$
  H k \in CRing_\infty
$$

for the [[Eilenberg-MacLane spectrum]] of $k$, canonically regarded as an [[E-∞ ring]]. Write

$$
  (H k) Mod \in (\infty,1)Cat
$$

for the [[(∞,1)-category of (∞,1)-modules]] over $H k$.

+-- {: .num_prop #DoldKan}
###### Proposition

There is an [[equivalence of (∞,1)-categories]]

$$
 (H k)Mod \simeq L_{qi} Ch_\bullet(k Mod)
$$

between the [[(∞,1)-category of (∞,1)-modules]] over the [[Eilenberg-MacLane spectrum]] $H k$ and the [[simplicial localization]] of the [[category of unbounded chain complexes]] of ordinary (1-categorical) $k$-[[modules]].

=--

This is the statement of the _[[stable Dold-Kan correspondence]]_, see at _[(∞,1)-category of (∞,1)-modules -- Properties -- Stable Dold-Kan correspondence](%28infinity%2C1%29-module#StableDoldKanCorrespondence)_.
  
+-- {: .num_defn}
###### Definition

Let $X$ be a [[topological space]] and write $\Pi(X) \in $ [[∞Grpd]] for its underlying [[homotopy type]] (its [[fundamental ∞-groupoid]]). Then we say that an [[(∞,1)-functor]]

$$
  \Pi(X) \to (H k) Mod
$$

is (the [[higher parallel transport]]) a _[[flat (∞,1)-bundle|flat]] [[(∞,1)-module bundle]]_ over $X$, or a _[[local system]]_ of $H k$-[[(∞,1)-modules]] over $X$.

=--


+-- {: .num_prop}
###### Proposition
**([[Riemann-Hilbert correspondence]])**

If $X$ is an [[orientation|oriented]] [[closed manifold]], then there is an [[equivalence of (∞,1)-categories]]

$$
  [\Pi(X), (H k)Mod]
  \simeq
  (T X)Mod
$$

between [[flat (∞,1)-bundle|flat]] [[(∞,1)-module bundles]]/[[local systems]] and [[L-∞ algebroid representations]] of the [[tangent Lie algebroid]] of $X$. From right to left the equivalece is established by sending an [[L-∞ algebroid representation]] given (as discussed there) by a flat $\mathbb{Z}$-graded connection on bundles of chain complexes (via prop. \ref{DoldKan}), to its [[higher holonomy]] defined in terms of [[iterated integrals]].

=--

This is the main theorem in ([Block-Smith 09](#BlockSmith09)).

+-- {: .num_defn}
###### Definition

Write

$$
  \Gamma \;\coloneqq\; \underset{\to}{\lim} \;\colon\;
  [\Pi(X), (H k)Mod]
  \to 
  (H k) Mod
$$

for the [[(∞,1)-colimit]] functor.

=--

+-- {: .num_remark}
###### Remark

We may think of $\Gamma$ equivalently as

* forming flat [[sections]] of a [[flat (∞,1)-bundle|flat]] [[(∞,1)-module bundle]];

* sending a [[flat (∞,1)-bundle|flat]] [[(∞,1)-module bundle]] to its _[[Thom spectrum]]_ (see at _[Thom spectrum -- For (∞,1)-module bundles ](Thom+spectrum#ForInfinityModuleBundles)_).

=--


+-- {: .num_defn}
###### Definition

Write

$$
  \mathbb{I}_X^{H k} \;\colon\; \Pi(X) \to (K k)Mod
$$ 

for the [[flat (∞,1)-bundle|flat]] [[(∞,1)-module bundle]] which is constant on the chain complex concentrated on $k$ in degree 0, the [[tensor unit]] in $[\Pi(X), (H k)Mod] \simeq [\Pi(X), L_{qi}Ch_\bullet(k Mod)]$.

=--

+-- {: .num_prop #SectionsOfTrivialKABundleIsAHomology}
###### Proposition


For $X$ a [[topological space]], we have a [[natural equivalence]] (with the identification of prop. \ref{DoldKan} understood) of the form

$$
  \Gamma(\mathbb{I}_X^{H k})
  \simeq
  C_\bullet(X,k)
  \,,
$$

between the $(H k)$-[[(∞,1)-module]] of sections of the trivial $(H k)$-[[(∞,1)-module bundle]] $\mathbb{I}_X^{H k}$ and the [[singular chain complex]] of $X$ for ordinary homology with [[coefficients]] in $k$.

=--

+-- {: .proof}
###### Proof

This is a classical basic (maybe [[folklore]]) statement. Here is one way to see it in full detail.

First notice that the [[(∞,1)-colimit]] of functors out of [[∞-groupoids]] and constant on the [[tensor unit]] in $(H k)Mod$ is by definition the [[(∞,1)-tensoring]] operation of $(H k)Mod$ over [[∞Grpd]]. Now if we find a [[presentable (∞,1)-category|presentation]] of $(H k)Mod$ by a [[simplicial model category]] the by the dicussion at _[(∞,1)-colomit -- Tensoring and cotensoring -- Models](limit+in+a+quasi-category#ModelsForTensoring)_ this [[(∞,1)-tensoring]] is given by the left [[derived functor]] of the [[sSet]]-[[tensoring]] in that simplicial model category.

To obtain this, use prop. \ref{DoldKan} and then the discussion at _[[model structure on chain complexes]]_ in the section _[Projective model structure on unbounded chain complexes](model%20structure%20on%20chain%20complexes#ProjectiveModelStructureOnUnboundedChainComplexes)_ which says that there is a [[simplicial model category]] structure on the [[category of simplicial objects]] in the [[category of unbounded chain complexes]] which models $L_{qi} Ch_\bullet(k Mod)$, and whose weak equivalences are those morphisms that produce [[quasi-isomorphism]] under the [[total chain complex]] functor.

In summary it follows that with any [[simplicial set]] $(\Pi(X))_\bullet in L_{whe} sSet$ representing $\Pi(X)$ (under the [[homotopy hypothesis]]-theorem) we have

$$
  \underset{\to}{\lim} (\mathbb{I}_X^{H k})
  \simeq
  \int_{[n] \in \Delta}  (\Pi(X))_n \cdot \mathbb{I}
  \,,
$$

where on the right we have the [[coend]] over the [[simplex category]] of the [[tensoring]] (of [[simplicial sets]] with [[simplicial objects]] in the [[category of unbounded chain complexes]]) of the standard cosimplicial simplex with the simplicial diagram constant on the [[tensor unit]] [[chain complex]].

The result on the right is manifestly, by the very definition of [[singular homology]], under the ordinary [[Dold-Kan correspondence]] the [[chain complex of singular simplices]]:

$$
  \int_{[n] \in \Delta}  (\Pi(X))_n \cdot \mathbb{I}
  \simeq
  \Pi(X) \otimes k
  \simeq
  C_\bullet(X,k)
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

If $X \in L_{whe} Top$ is a [[Poincaré duality space]] of [[dimension]] $n$, then $\Gamma(\mathbb{I}_X^{H A}) \in (H A) Mod$ is a [[dualizable object]] which is almost self-dual except for a degree [[twisted cohomology|twist]] of (itself) degree 0:

$$
  \left(
     \Gamma\left(\mathbb{I}_X^{H A}\right)
  \right)^\vee
  \simeq
  \Sigma^{-n}
  \left(
     \Gamma\left(\mathbb{I}_X^{H A}\right)
  \right)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Under the identifications of prop. \ref{DoldKan} and prop. \ref{SectionsOfTrivialKABundleIsAHomology} this is the theorem discussed at _[[Poincaré duality]]_ in the section _[Poincar&#233; duality -- Refinement to homotopy theory](Poincar%C3%A9+duality#RefinementInHomotopyTheory)_.

=--

See also at _[[Dold-Thom theorem]]_.

### Dimension 2 -- Pull-push over $KU$ and $K$-theory indices

#### K-theory of smooth groupoids / stacks
 {#KTheoryOfSmoothGroupoids}

We discuss here aspects of "smooth" (not yet [[differential K-theory|differential]]!) K-theory, namely the refinement of [[K-theory]] to [[smooth groupoids]] (a generalization of [[equivariant K-theory]]).

Write 

$$
  KU \in CRing(\infty Grpd)
$$ 

for the periodic [[complex K-theory spectrum]].

+-- {: .num_prop #SnaithTheorem}
###### Proposition

The [[complex K-theory spectrum]] $KU$ is the localization of the [[∞-group ∞-ring]] of the [[circle 2-group]] at the [[Bott element]]

$$
  KU \simeq \mathbb{S}[B U(1)][\beta^{-1}]
  \,.
$$


=--

This is _[[Snaith's theorem]]_.

+-- {: .num_prop}
###### Proposition

There is a canonical map

$$
  B^2 U(1) \to B GL_1(KU)
  \,.
$$

=--

This is observed in ([Nuiten 13, section 3](#Nuiten13)).

+-- {: .proof}
###### Proof

The [[localization]] map

$$
  \mathbb{S}[B U(1)] \to \mathbb{S}[B U(1)][\beta^{-1}]
$$

in $CRing(\infty Grpd)$ has by prop. \ref{GroupOfUnitsAdjunction} an [[adjunct]] of the form

$$
  B U(1) \to GL_1(\mathbb{S}[B U(1)][\beta^{-1}])
$$

in $AbGrp(\infty Grpd)$. By the [[looping and delooping]] theorem and by prop. \ref{SnaithTheorem} this is equivalently a map

$$
  B^2 U(1) \to B GL_1(KU)
$$

in [[∞Grpd]].

=--

+-- {: .num_remark}
###### Remark

Via the canonical smooth refinement $\mathbf{B}U(1)$ of the [[circle 2-group]] $B U(1)$ the construction in prop. \ref{SnaithTheorem} induces a canonical smooth $E_\infty$-ring

$$
  \mathbf{KU} \coloneqq \mathbb{S}[\mathbf{B} U(1)][\beta^{-1}]
  \;\in
  CRing(Smooth\infty Grpd)
  \,.
$$

Since the [[shape modality]] $\Pi$ preserves all [[(∞,1)-colimits]], it follows that

$$
  \Pi(\mathbf{KU}) \simeq KU
  \,,
$$

hence that $\mathbf{KU}$ is indeed a smooth refinement of [[KU]].

=--

(Thanks to [[Thomas Nikolaus]] for discussion of this point.) 

We expect that for $X \in$ [[Smooth∞Grpd]] a [[Lie groupoid]] that maps $X \to \mathbf{KU}$ represent "smooth" K-theory classes on $X$ as represented by the [[groupoid K-theory]] of $X$ or equivalently the [[operator K-theory]] of its [[groupoid convolution algebra]]. 
This still needs to be show. But motivated by this, we take the following as the linearization functor in K-theory:

+-- {: .num_prop #TheSmoothKTheoryModelFunctor}
###### Proposition

There is a [[lax monoidal functor]]

$$
  \Gamma
   \;\colon\;
  DiffStack^{prop}_{/\mathbf{B}^2 U\left(1\right)}
   \to
  \left( Ho\left( KU Mod \right) \right)^{op}
$$

from the category of [[differentiable stacks]] ([[Lie groupoids]] with [[Morita morphisms]]) equipped with [[circle 2-bundle]] and with [[proper maps]] between them to the [[opposite category|opposite]] of the [[homotopy category]] of [[KU]]-[[∞-modules]] which factors by a [[strong monoidal functor]] through [[KK-theory]] 

$$
  \Gamma
   \;\colon\;
  DiffStack^{prop}_{/\mathbf{B}^2 U(1)}
  \stackrel{C(-)}{\to}
  KK^{op}
   \to
  \left( Ho\left( KU Mod \right) \right)^{op}
$$

and which

* sends a Lie groupoid $X$ with circle 2-bundle $\chi$ first its [[twisted groupoid convolution algebra]] $C_\chi(X) \in $ [[C*Alg]] and then produces the [[operator K-theory]]-[[spectrum]] of that algebra as discussd at _[[KK-theory]]_ in the section _[Triangulated and KU-module structure](KK-theory#TriangulatedAndSpectrumEnrichedStructure)_;

* sends a morphism of Lie groupoids to the [[Hilbert bimodule]] of sections of the corresponding [[Hilsum-Skandalis morphism|Hilsum-Skandalis]] [[bibundle]], regarded as a morphism in [[KK-theory]].

The functor $\Gamma$ is [[strong monoidal functor|strong monoidal]] at least when restricted to [[amenable Lie groupoids]], where moreover it factors through a [[full subcategory|full inclusion]] of the [[KK-bootstrap category]]

$$
  \Gamma
   \;\colon\;
  DiffStack^{amen,\,prop}
  \stackrel{C(-)}{\to}
  KK_{bootstr}^{op}
   \hookrightarrow
  \left(Ho\left( KU Mod\right) \right)^{op}
  \,.
$$


=--

+-- {: .proof}
###### Proof

The functor $C(-) \colon DiffStack_{/\mathbf{B}^2 U(1)}^{prop} \to KK$ is discussed in ([Alldridge-Giansiracusa 06](#AlldridgeGiansiracusa06), [Nuiten 13, section 3](#Nuiten13)), based on ([Tu-Xu-LG 03](#TuXuLG03)). The functor $KK \to Ho(KU Mod)$  is due to ([DEKM 11, section 3](#DEKM11)). The statement about the factorization through the bootstrap category is ([Tu 99](amenable+topological+groupoid#Tu99)) combined with ([DEKM 11, section 3](#DEKM11)).

=--

+-- {: .num_remark}
###### Remark

In particular, on a [[local quotient groupoid]] the functor of prop. \ref{TheSmoothKTheoryModelFunctor} reproduces the [[twisted groupoid K-theory]] defined via [[equivariant vector bundles]] in ([FHT, I, section 3.2](#FHT)) and on general Lie groupoids the [[twisted groupoid K-theory]] of ([Tu-Xu-LG 03](#TuXuLG03)).

=--


#### Beck-Chevalley condition and functoriality of $KU$-motivic quantization
 {#BeckChevalleyConditionForGroupoidKTheory}

Functoriality of

$$
  Corr(\mathbf{H}_{/\mathbf{B}^2 U(1)})^{nice}
  \to 
  KU Mod
$$

requires that pullback in [[twisted K-theory|twisted]] [[groupoid K-theory]] satisfies the [[Beck-Chevalley condition]], which says that push-pull is equivalent to pull-push through the [[fiber product]].

Here we list sufficient conditions for this to be the case

* for untwisted correspondences of manifolds: ([Connes-Skandalis 84](#ConnesSkandalis84))

* for untwisted correspondences of equivariant manifolds: ([Emerson-Meyer 08](#EmersonMeyer08))

* for twisted correspondences of [[moduli stacks of flat connections]]: ([Freed-Hopkins-Teleman 07](#FreedHopkinsTeleman07))

(...)


### Dimension 3 -- Pull-push over $tmf$ and elliptic genera

(...) [[elliptic cohomology]], [[tmf]] (...) [[sigma-orientation]], [[string orientation of tmf]] (..) [[elliptic genus]], [[Witten genus]] (...)

## **III)** Examples and applications
 {#Examples}

We spell out and discuss examples and applications of the general method.

* _[In dimension 1](#ExamplesDimension1)_

* _[In dimension 2](#ExamplesDimension2)_

* _[In dimension 3](#ExamplesDimension3)_


### Dimension 1
 {#ExamplesDimension1}

#### Lagrangian field theory and prequantized Lagrangian correspondences
 {#LagrangianCorrespondences}


##### Idea

Here we discuss the notion of _prequantized Lagrangian correspondences_ and how it serves to embed traditonal [[Hamiltonian mechanics]] and [[Lagrangian mechanics]] into the general context of [[local prequantum field theory]] and its [[motivic quantization]].

A traditional notion is that of a plain _[[Lagrangian correspondence]]_, which is a [[Lagrangian submanifold]] of the [[Cartesian product]] of a [[symplectic manifold]] and another one, with opposite [[symplectic structure]]. As discussed there, plain [[Lagrangian correspondences]] serve to encode [[symplectomorphisms]] -- hence transfomations between [[phase spaces]] in [[physics]] -- via [[correspondences]] of [[symplectic manifolds]].

But in [[prequantum field theory]] proper, and in particular with an eye towards [[geometric quantization]], one considers the [[prequantization]] of these symplectic manifolds by lifting them to [[prequantum circle bundles]] with [[principal connection]]. The notion of _prequantized Lagrangian correspondence_ is the refinement of that of plain [[Lagrangian correspondence]] which does properly respect and reflect this [[prequantization]] information: a prequantized Lagrangian correspondence is a [[Lagrangian subspace]] as before, but now equipped with an explicit [[gauge transformation]] between the pullbacks of the two [[prequantum circle bundles]] to the correspondence space.

We discuss below how the concept of prequantized Lagrangian correspondences neatly unifies  "[[classical mechanics]]" formulated in terms of [[symplectic geometry]] of [[phase space]] with [[Hamiltonian flows]] on them with the [[Hamilton-Jacobi equation]] for such flows. 

Then we show how also the notion of prequantized Lagrangian correspondence is -- still naturally in the context of [[local prequantum field theory]] -- further refined from the context of [[symplectic manifolds]] to that of [[Poisson manifolds]]. Specifically, this is obtained by realizing that prequantized Lagrangian correspondences are really naturally to be regarded as correspondences-of-correspondences in a [[higher category of correspondences|2-category of correspondences]], where now the new lower-order correspondences are instead [[boundary field theories]] for a [[2d Chern-Simons theory]] (a non-perturbative [[Poisson sigma-model]]).  


##### Symplectic manifolds and phase spaces

We write $(X,\omega)$ for a [[symplectic manifold]] with underlying [[smooth manifold]] $X$ and [[symplectic form|symplectic]] [[differential 2-form]] $\omega \in \Omega^2_{cl}(X)$. In [[physics]] this models the [[phase space]] of a [[mechanical system]].

+-- {: .num_example}
###### Example

The [[sigma-model]] describing the propagation of a [[particle]] on the [[real line]] $\mathbb{R}$ has as [[phase space]] the [[plane]] $\mathbb{R}^2 = T^\ast \mathbb{R}$ and as [[symplectic form]] its canonical [[volume form]]. Traditionally the two canonical [[coordinate functions]] on this phase space are denoted $q,p \;\colon\; \mathbb{R}^2 \longrightarrow \mathbb{R}$ (called the "[[canonical coordinate]]" and the "[[canonical momentum]]", respectively), and in terms of these the symplectic form in this example is $\omega = \mathbf{d} q \wedge \mathbf{d} p$.

=--


##### Symplectomorphisms and canonical transformations

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

+-- {: .num_remark}
###### Remark

In [[physics]] [[symplectomorphisms]] are traditionally known as _[[canonical transformations]]_. Or more precisely, a _canonical transformation_ is a [[symplectomorphism]] of the special kind called a _[[Hamiltonian symplectomorphism]]_. This we come to below after [[prequantization]].

=--

For the present purpose it is useful to formulate [[symplectomorphisms]] in the language of the [[topos]] $\mathbf{H}$ of [[smooth spaces]]. This is discussed in much detail at _[[geometry of physics]]_ in the section _[Smooth spaces](geometry%20of%20physics#SmoothSpaces)_. 

In terms of this there is a [[smooth space|smooth]] universal [[moduli space]] $\Omega^2_{cl}$ of closed [[differential 2-forms]], and by the [[Yoneda lemma]] one such $\omega \in \Omega^2_{cl}(X)$ is equivalently a [[homomorphism]] of the form

$$
  \omega \;\colon\; X \longrightarrow \Omega^2_{cl}
$$
 
This is explained in detail at _[[geometry of physics]]_ in the section _[Differential forms](geometry%20of%20physics#DifferentialForms)_.

In this language we have:

+-- {: .num_remark}
###### Remark

A [[symplectomorphism]] $f \colon (X_1, \omega_2) \longrightarrow (X_2, \omega_2)$ as above is equivalently a [[commuting diagram]] of the form

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

Yet another equivalent way to say this is that both $(X_1, \omega_1)$ and $(X_2, \omega_2)$ are naturally [[objects]] in the [[slice topos]] $\mathbf{H}_{/\Omega^2_{cl}}$ and that a [[symplectomorphism]] is equivalently just a [[morphism]] between them, in this [[slice topos]].

=--

##### Lagrangian correspondences

Since this makes the two symplectic manifolds correspond to each other, it is useful to express this as in the formal sense as a  [[correspondence]]. For any [[smooth function]] $f \colon X_1 \to X_2$,  the natural choice of [[correspondence space]] is the [[graph of a function|graph]] of $f$, which we may depict as a [[subobject]] of the [[Cartesian product]]

$$
  graph(f) \hookrightarrow X_1 \times X_2
$$

or better as a [[correspondence]] [[span]] [[diagram]]

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
 \,.
$$


Traditionally one considers now the [[Cartesian product]] [[manifold]] $X_1 \times X_2$ itself as a [[symplectic manifold]] equipped with the [[pullback of differential forms|pullback]] symplectic form

$$
  (X_1 \times X_2 , \; p_1^\ast \omega_1 - p_2^\ast \omega_2)
$$

and observes then that the [[diffeomorphism]] $f$ being a [[symplectomorphism]] is equivalent to its [[graph of a function|graph]] being a [[Lagrangian submanifold]] of this product symplectic manifold. In that case the above [[correspondence]] is called a _[[Lagrangian correspondence]]_ between $(X_1, \omega_1)$ and $(X_2, \omega_2)$.

+-- {: .num_remark}
###### Remark

In the language of the [[topos]] $\mathbf{H}$ of [[smooth spaces]], this has a more evident formulation: that $graph(f)$ is an [[isotropic subspace]] equivalently means that there is a [[commuting diagram]] of [[smooth spaces]] of the following form

$$
  \array{
    && graph(f)
    \\
    & \swarrow && \searrow
    \\
    X_1 && && X_2
    \\
    & {}_{\mathllap{\omega_1}}\searrow && \swarrow_{\mathrlap{\omega_2}}
    \\
   && \Omega^2_{cl}
  }
  \,.
$$

This in turn is equivalent to being a [[correspondence]] in the [[slice topos]] $\mathbf{H}_{/\Omega^2_{cl}}$.

=--


##### Hamiltonian correspondences

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

1. the two projection maps to $X$ send a trajectory to its inital and to its final configuration, respectively.

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

##### Prequantized Lagrangian correspondences

But the reason to consider [[Hamiltonian symplectomorphisms]] instead of general [[symplectomorphisms]] is really because these give [[homomorphisms]] not just between plain [[symplectic manifold]], but between their _prequantizations_. To these we turn now.

+-- {: .num_defn}
###### Definition


A _[[prequantization]]_ of a [[symplectic manifold]] $(X,\omega)$ is -- if it exists -- a choice of [[circle group]]-[[principal connection]] $\nabla$ on $X$ whose [[curvature]] 2-form is the given [[symplectic form]]

$$
  F_\nabla = \omega
  \,.
$$

=--

+-- {: .num_remark}
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

=--

Then for two prequantized symplectic manifolds, it is now clear what a _prequantized correspondence_ between them is: 

+-- {: .num_defn}
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
    & {}_{\mathllap{\nabla_1}}\searrow && \swarrow_{\mathrlap{\nabla_2}}
    \\
   && \Omega^2_{cl}
  }
$$

hence a correspondence in the [[slice (infinity,1)-topos|slice (2,1)-topos]] $\mathbf{H}_{/\mathbf{B}^2 U(1)_{conn}}$.

=--

##### The classical action functional prequantizes Hamiltonian correspondences
 {#TheClassicalActionFunctionalPrequantizesHamiltonianCorrespondences}

The natural question now is which Hamiltonian correspondences may be prequantized and what the corresponding prequantum data is. The following proposition shows that the prequantization of the Hamiltonian correspondence given by a [[Hamiltonian]] $H$ is given by the exponentiated [[action functional]] associated with $H$, namely the exponentiated integral over its [[Lagrangian]] $L$, which is its [[Legendre transform]] $L = p \frac{\partial H}{\partial p} - H$.

Of course all the ingredients in the statement and in the proof od the following proposition are classical. But the notion of prequantized Lagrangian correspondence serves to neatly unify these ingredients and give them a natural place in the context of [[local prequantum field theory]] which later naturally leads to the formulation of [[higher prequantum geometry|higher]] [[local prequantum field theory]] and its [[motivic quantization]].

+-- {: .num_prop #HamiltonianCorrespondenceIsPrequantizedByTheExponentiatedAction}
###### Proposition

Consider the [[phase space]] $(\mathbb{R}^2, \; \omega = \mathbf{d} q \wedge \mathbf{d} p)$ equipped with its canonical [[prequantization]] by $\theta = p \mathbd{d}q$. Then for $H \colon \mathbb{R}^2 \to \mathbb{R}$ a [[Hamiltonian]], and for $t \in \mathbb{R}$ a parameter ("time"), a lift of the [[Lagrangian correspondence]] $\exp(t \{H,-\})$ to a prequantized Lagrangian correspondence is given by

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

+-- {: .num_remark}
###### Remark

In summary,  prop. \ref{HamiltonianCorrespondenceIsPrequantizedByTheExponentiatedAction} 
and remark \ref{HamiltonianCorrespondencesAreSpacesOfTrajectories}
say that a prequantized Lagrangian correspondence is conceptually of the following form

$$
  \array{
    && {{space\,of} \atop {trajectories}}
    \\
    & \swarrow && \searrow
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


##### Quantization of prequantized Lagrangian correspondences

+-- {: .num_remark}
###### Remark

By a naive counting, Lagrangian correpondences, modelling [[mechanics]] and supposed to quantize to [[quantum mechanics]] hence 1-dimensional [[quantum field theory]], should be motivically quantized over [[HC]], the [[ordinary cohomology]] [[spectrum]]. However, $H\mathbb{C}$ does admit twists only by $\flat \mathbf{B}U(1)$ ([[flat connections]]) but not by $\mathbf{B}U(1)_{conn}$ (general $U(1)$-[[principal connections]] with [[curvature]]), see at _[[twisted ordinary cohomology]]_. However the special case where the curvature $\omega$ vanishes no longer corresponds to [[symplectic manifolds]], and even when regarded as a [[Poisson manifold]] it is not interesting.

Below we see that the quantization of [[symplectic manifolds]] and generally [[Poisson manifolds]] is instead to be regarded [[holographic principle|holographically]] as the [[boundary field theory]] of the Poisson-[[2d Chern-Simons theory]].  In this context, [[Lagrangian correspondences]] are to be regared as secretly being 2-dimensional correspondences of the form

$$
  \array{
     \ast &\leftarrow& X_2 &\rightarrow & SymplGrpd(X_2, \omega_2^{-1}) && 2d \, CS
     \\
    \uparrow && \uparrow && \uparrow
    \\
    \ast &\leftarrow& &\rightarrow& && defect
    \\
    \downarrow && \downarrow && \downarrow
    \\
     \ast &\leftarrow& X_1 &\rightarrow & SymplGrpd(X_1, \omega_1^{-1}) && 2d \, CS
    \\
    \\
    trivial\; theory && boundary && 2d\,CS 
  }
  \,.
$$

Here on the right we have the corresponding [[symplectic groupoid]]. See below (...)

=--

For more see at _[[prequantized Lagrangian correspondence]]_.

#### String topology operations

(...) [[string topology]] (...)

### Dimension 2
 {#ExamplesDimension2}


#### The Poisson manifold at the boundary of 2d Chern-Simons theory
 {#PoissonManifoldAtTheBoundaryOf2dChernSimonsTheory}

We show here how the traditional quantization of [[Poisson manifolds]] is reproduced and refined within _motivic quantization_. This proceeds in a [[holographic principle|holographic]] fashion, where the Poisson manifold is regarded as topological boundary/[[brane]] of the [[2d Chern-Simons theory]] which is the [[non-perturbative quantum field theory|non-perturbative]] version of the corresponding  [[Poisson sigma-model]], as discussed in ([Fiorenza-Rogers-Schreiber 13a, section 4](#FiorenzaRogersSchreiber13a)).




(...) [[extended geometric quantization of 2d Chern-Simons theory]] (...)

Let $(X,\pi)$ be a [[Poisson manifold]]. The [[Lie integration]] of the corresponding [[Poisson Lie algebroid]] $\mathfrak{P}$ is called the corresponding _[[symplectic groupoid]]_:

$$
  SymplGrpd(X,\pi) \coloneqq \tau_1 \exp(\mathfrak{P})
  \,.
$$

If the canonical 3-class of $\mathfrak{P}$ is suitably integral, then this carries a [[prequantum 2-bundle]]

$$
  \chi \colon SymplGrpd(X,\pi) \to \mathbf{B}^2 U(1)_{conn}
  \,.
$$

Here $SymplGrpd(X,\pi)$ may be regarded as the [[moduli stack]] of ([[instanton sectors]] of) the [[non-perturbative quantum field theory|non-perturbative]] [[Poisson sigma-model]]. This non-perturbative theory is the "[[2d Chern-Simons theory]]" induced by $\mathfrak{P}$.

There is a canonical inclusion $X \to SymplGrpd(X,\pi)$ and one finds that $\chi$ trivializes when restricted to this inclusion. Therefore the original [[Poisson manifold]] is a topological [[brane]] for the [[2d Chern-Simons theory]], with the boundary condition formally exhibited by a [[correspondence]] of the form

$$
  \array{
     && X 
     \\
     & \swarrow && \searrow^{\mathrlap{i}}
     \\
    \ast && \swArrow_\nabla && SymplGrpd(X,\pi^{-1})
    \\
    & \searrow && \swarrow
    \\
     && \mathbf{B}^2 U(1)_{conn^1}
  }
  \,.
$$

Here $\nabla$ is hence a kind or [[prequantum bundle]] applicable to [[Poisson manifolds]].

Therefore we can quantize the original Poisson manifold by applying motivic quantization to this boundary condition for [[2d Chern-Simons theory]]. The result is an element in the [[K-theory]] of the [[symplectic groupoid]].

We discuss this now for some cases of interest. First we show how this reproduces and refines traditional [[geometric quantization]] of [[symplectic manifolds]]. Then we show how this reproduces in particular the [[orbit method]] for the construciton of [[irreducible representation]] of Lie groups from the [[geometric quantization]] of their [[coadjoint orbits]].

1. _[Geometric quantization of symplectic manifolds](#GeometricQuantizationOfSymplecticManifolds)_

1. _[Quantization of Lie-Poisson structure](#QuantizationOfLiePoissonStructure)_.

##### Geometric quantization of symplectic manifolds
 {#GeometricQuantizationOfSymplecticManifolds}

We consider the special case of the [above](#PoissonManifoldAtTheBoundaryOf2dChernSimonsTheory) motivic quantization of Poisson manifolds where the [[Poisson manifold]] $(X,\pi)$ happens to be a [[symplectic manifold]] $(X,\omega^{-1})$. 

+-- {: .num_prop }
###### Proposition

The [[symplectic groupoid]] of a [[symplectic manifold]] is equivalent to the point

$$
  SymplGrp(X,\omega^{-1}) \simeq \ast
  \,.
$$

Accordingly, the boundary condition for the Poisson [[2d Chern-Simons theory]] induced by a [[Poisson manifold]] which is symplectic is a correspondence of the form

$$
  \array{
    && X
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow_\nabla && \ast
    \\
    & \searrow && \swarrow
    \\
    && \mathbf{B}^2 U(1)_{conn^1}
  }
$$

and so is equivalently given by a [[prequantum bundle]]

$$
  \nabla \; \colon \; X \to \mathbf{B}U(1)_{conn} \simeq \Omega \mathbf{B}^2 U(1)_{conn^1}
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

Traditionally the [[strict deformation quantization]] of a [[symplectic manifold]] with a good [[polarization]] $\mathcal{P}$ is taken to be the [[C*-algebra]] of [[compact operators]] on the [[leaf space]] $X/\mathcal{P}$. In ([EH 06](geometric+quantization+of+symplectic+groupoids#EH)) this is rederived as the polarized [[groupoid convolution algebra]] of the symplectic groupoid of $(X,\omega^{-1})$ naturally presented as the [[pair groupoid]] $SymplGrpd(X,\omega^{-1}) \simeq Pair(X/\mathcal{P})$. 

However, once one passes from [[smooth manifolds]] to [[Lie groupoids]], it is unnatural to essentially distinguish the [[pair groupoid]] from the point, since both are [[Morita equivalence|Morita equivalent]]. Notably, in analogy to this the algebra of [[compact operators]] is of course itself [[Morita equivalence|Morita equivalent]] to the base algebra of [[complex numbers]]. 

As a consequence, the traditional description of the [[strict deformation quantization]] of [[symplectic manifolds]] in the refined perspective of ([EH 06](geometric+quantization+of+symplectic+groupoids#EH)) contains a conundrum: either one unnaturally breaks the natural Morita equivalence or else one arrives at a trivial quantization.

In the following we see that this is resolved in motivic quantization. Here is is not just the symplectic groupoid itself that is quantized, but the [[correspondence]] $\ast \leftarrow X \to SymplGrp(X,\omega^{-1})$ which exhibits the original symplectic manifold as a boundary of the corresponding [[2d Chern-Simons theory]]. While the quantization of $SymplGrpd(X,\omega^{-1})$ itself is trivial when properly regarded in [[higher geometry]], that of $\ast \leftarrow X \to SymplGrpd(X,\omega^{-1})$ is not and in fact yields the correct quantization.

A conceptual way to understand this phenomenon is to recall that the symplectic groupoid of a [[Poisson manifold]] is effectively a stacky model for the [[leaf space]] by [[symplectic leafs]] of the Poisson manifold. Since for symplectic Poisson manifolds the leaf space is the point, accordingly so is the symplectic groupoid, up to equivalence.

=--

In order to motivically quantize, we need an [[orientation in K-theory]] of $X$. This is precisely a [[spin^c structure]], which in turn is induced notably from a [[Kähler polarization]] of $(X,\omega^{-1})$.

One then observes that the push-forward of $\nabla$ to the point in K-theory reproduces the traditional  [[geometric quantization]] of $(X,\omega^{-1})$.

We discuss now the [[space of quantum states]]

* _[Quantum states and K-theory](#QuantumStatesAndKTheory)_

and then the [[quantum observables]]

* _[Quantum observables and equivariant K-theory](#QuantumObservablesAndEquivariantKTheory)_ .


| [[space of quantum states]] | [[quantum observables]] |
|--|--|
| [[index]] in [[K-theory]] | [[Dirac induction]]: index in [[equivariant K-theory]] |

###### Quantum states and K-theory
 {#QuantumStatesAndKTheory}

$(X,\omega)$ a [[symplectic manifold]]


$$
  \array{
    && X
    \\
    & \swarrow && \searrow^{i}
    \\
    \ast && \swArrow_{\nabla} && SymGrpd(X,\omega^{-1}) & \simeq \ast
    \\
    & \searrow && \swarrow
    \\
    && \mathbf{B}^2 U(1)_{conn^1}
  }
$$

A K-orientation on $i$ is equivalently a [[spin^c structure]] on $X$, in particular induced from a [[Kähler polarization]] of $(X,\omega)$.

The corresponding push-forward is

$$
  i_! \;\colon\; K(X) \to K(\ast) \simeq FinHilb
$$

and sends the prequantum bundle to the [[space of quantum states]].

This is discussed in detail at _[geometric quantization -- quantum states](#geometric+quantization#QuantumStates)_.


###### Quantum observables and equivariant K-theory
 {#QuantumObservablesAndEquivariantKTheory}

We now discuss how the traditional quantization of [[observables]] to [[quantum observables]] on [[symplectic manifolds]] is reproduced by motivic quantization of the symplectic manifold regarded as a [[brane]] of its Poisson-[[2d Chern-Simons theory]].


Let $(X,\omega)$ be a [[symplectic manifold]]. 
Let $\nabla \colon X \to \mathbf{B}U(1)_{conn}$ be a [[prequantum bundle]].

A naive infinitesimal [[prequantum observable]] of $X$ is just a smooth function on $X$. An _exponentiated  [[prequantum observable]]_ on $X$ is an element $O \in QuantMorph(X,\nabla)$ of the [[quantomorphism group]] of $(X,\omega)$. As observed in ([Fiorenza-Rogers-Schreiber 13a](#FiorenzaRogersSchreiber13a)), this is an equivalece in the slice

$$
  O
  \;\; \colon
   \;\;\;\;\;\;
  \array{
    X && \stackrel{\simeq}{\to} && X
    \\
    & {}_{\mathllap{\nabla}}\searrow 
    &\swArrow& \swarrow_{\mathrlap{\nabla}}
    \\
    && \mathbf{B}^2 U(1)_{conn^1}
  }
  \,.
$$

A [[Lie group]] $G$ of [[prequantum observables]] is hence a homomorphism

$$
  G \to QuantMorp(X,\nabla)
  \,.
$$

If $\mathfrak{g} = Lie(G)$ is the [[Lie algebra]] of $G$, then this is the [[Lie integration]] of a $\mathfrak{g}$-[[moment map]] hence a  $G$-[[Hamiltonian action]] on $(X,\omega)$.

+-- {: .num_prop}
###### Proposition

A group $G \to QuantMorph(\nabla)$ of exponentiated [[prequantum operators]], hence an integrated $G$-[[Hamiltonian action]] is equivalently an [[equivariant bundle|equivariant]] structure $\nabla//G$ on the [[prequantum bundle]] $\nabla$ given by

$$
  \array{
    X &\stackrel{\nabla}{\to}& \mathbf{B}U(1)_{conn}
    \\
    \downarrow & \nearrow_{\nabla//G}
    \\
    X//G
  }
  \,.
$$

=--

On the level of de Rham cocycles essentially this was observed in ([Atiyah-Bott 84, prop 6.18](#AtiyahBott84)).

If follows that with a $G$-[[Hamiltonian action]] of [[prequantum operators]] given, the [above situation](#GeometricQuantizationOfSymplecticManifolds) refines to a [[brane]] that is given by a [[correspondence]] of [[action groupoids]] of the following form

$$
  \array{
    && X//G
    \\
    & \swarrow && \searrow^{i}
    \\
    \ast && \swArrow_{\nabla//G} && \ast//G
    \\
    & \searrow && \swarrow
    \\
    && \mathbf{B}^2 U(1)_{conn^1}
  }
  \,.
$$

The original [[orientation in K-theory]] extends to an orientation in [[equivariant K-theory]] if it is itself equivariant, hence if the [[prequantum operators]] in $G$ respect the polarization. This is precisely the standard condition for [[prequantum operators]] to qualify as [[quantum operators]]. 

Hence if $X$ carries a $G$-equivariant [[spin^c structure]] then we have a [[push-forward in generalized cohomology]] of the form

$$
  i_! \;\colon\; K(X//G) \simeq K_G(X) \to K_G(\ast) \simeq K(\ast//G) \simeq Rep(G)   
$$

("[[Dirac induction]]"). Here we used on the left that the [[convolution algebra]] of an [[action groupoid]] $X//G$ is equivalently the corresponding [[crossed product C*-algebra]] (as discussed there), and the [[Green-Julg theorem]] which identifies the [[operator K-theory]] of that with the [[equivariant K-theory]] of $X$. On the right we used the same identification and the fact that hence $K(\ast//G)$ is the [[representation ring]] of the group $G$.

So the motivic quantization 

$$
  i_!(\nabla//G) \in Rep(G)
$$

of the $G$-[[Hamiltonian action]] is an element in $Rep(G)$ a [[space of quantum states]] equipped with the $G$-action of [[quantum observables]] in $G$.



##### Quantization of Lie-Poisson structures -- The universal orbit method
 {#QuantizationOfLiePoissonStructure}

A particularly interesting case of [[geometric quantization]] of [[symplectic manifolds]] is the quantization of [[coadjoint orbits]] of suitable [[Lie groups]]. Physically this is the quantization of the "internal degrees of freedom" of [[Wilson loop]] [[QFT with defects|defect]] in [[Chern-Simons theory]] (see at _[orbit method -- Nonabelian charged particle trajectories](orbit+method#GaugeAndGravityWilsonLoops)_). Mathematically this is a process that yields all the [[irreducible representations]] of these Lie groups, as such called the _[[orbit method]]_.

By the [above](#GeometricQuantizationOfSymplecticManifolds) discussion of the motivic holographic quantization of [[symplectic manifolds]], the geometric quantization of any single [[coadjoint orbit]] is naturally described by motivic quantization. But moreover, we discuss now how each such orbit boundary theory is naturally related by a [[QFT with defects|defect]] to the [[2d Chern-Simons theory]] which is given by the dual Lie algebra regarded as a [[Poisson manifold]] with its [[Lie-Poisson structure]]. The motivic quantization of this defect reproduces a map in [[twisted K-theory|twisted]] [[equivariant K-theory]] that appeared as ([Freed-Hopkins-Teleman, part II, theorem 1.28](#FHT)): it is in the quantization language used here a "quantum operator" that sends boundary states of the $\mathfrak{g}^\ast//G$-[[2d Chern-Simons theory]] to states of the coadjoint orbit, respecting the action of the $G$-[[quantum observables]]. As such the quantization of the defects of the $\mathfrak{g}^\ast//G$-2d CS theory is a "universal [[orbit method]]" for $G$ in that it contains the quantization of each [[coadjoint orbit]] to each representation as the quantization of one of its defects.


$\,$

Let $\mathfrak{g}$ be a Lie algebra. Write $\mathfrak{g}^\ast$ for its dual vector space regarded as a [[Poisson manifold]] by its canonical [[Lie-Poisson structure]]. 

The crucial fact that drives the following discussion is the following.

+-- {: .num_prop}
###### Proposition

The [[symplectic groupoid]] of the [[Lie-Poisson structure|Lie-Poisson manifold]] $\mathfrak{g}^\ast$ is the [[action groupoid]] $\mathfrak{g}^\ast //G$ for the [[coadjoint action]]

$$
  SymplGrpd(\mathfrak{g}^\ast) \simeq \mathfrak{g}^\ast//G
  \,.
$$

=--

([Bursztyn-Crainic, example 4.3](symplectic+groupoid#BursztynCrainic))

+-- {: .num_remark}
###### Remark

The manifold of [[morphisms]] of $(\mathfrak{g}^\ast//G)$ in the standard presentation is $\mathfrak{g}^\ast \times G$, which by left translation is naturally identified with the [[cotangent bundle]] of $G$:

$$
  (\mathfrak{g}^\ast//G)_1
    = 
  \mathfrak{g}^\ast 
   \simeq
  T^\ast G
  \,.
$$

=--


The canonical [[prequantum 2-bundle]]

$$
  \chi \colon \mathfrak{g}^\ast//G \to \mathbf{B}^2 U(1)_{conn^1}
$$

is given by the truncated [[Deligne cohomology]] cocycle whose 1-form component is the [[Liouville-Poincaré 1-form]] on the [[cotangent bundle]] $T^\ast G$ under the natural identification

$$
  ((\mathfrak{g}^\ast//G)_1 = \mathfrak{g}^\ast \times G \simeq T^\ast G
  \,.
$$

This trivializes along the canonical inclusion $\mathfrak{g}^\ast \to \mathfrak{g}^\ast //G$ and therefore we have a boundary condition

$$
  \array{
      && \mathfrak{g}^\ast
      \\
      & \swarrow && \searrow
     \\
    \ast && \swArrow_\xi && \mathfrak{g}^\ast // G
     \\
     & \searrow && \swarrow
     \\
     && \mathbf{B}^2 U(1)_{conn^1}
  }
$$

where $\xi$ is a circle bundle with connection, the corresponding "[[prequantum bundle]]".

Assume now that $\mathfrak{g}$ is semisimple with [[Killing form]] [[invariant polynomial]] $\langle -,-\rangle$. Let $\lambda \in \mathfrak{g}$ be a regular weight and $\mathcal{O}_\lambda \hookrightarrow \mathfrak{g}^\ast$ the corresponding [[coadjoint orbit]].

Then the previous boundary condition for the [[2d Chern-Simons theory]] of $\mathfrak{g}^\ast//G$ extends to a [[QFT with defects|defect]] to the 2d CS theory of $\ast //G$ with in turn is the [[symplectic manifold]] $\mathcal{O}_\lambda$ as its [[brane]]. This is exhibited by the diagram

$$
  \array{
    \ast &\leftarrow& \ast &\to& \ast && trivial\,theory
    \\
    \uparrow && \uparrow && \uparrow
    \\
    \mathcal{O}_\lambda//G &\leftarrow& \mathcal{O}_\lambda &\hookrightarrow& \mathfrak{g}^\ast && boundary
    \\
    \downarrow && \downarrow &(pb)& \downarrow
    \\
    \ast//G &\leftarrow& \mathcal{O}_\lambda // G &\hookrightarrow& \mathfrak{g}^\ast//G  && 2d CS 
    \\
    \,
    \\
    2d CS && defect && 2d CS
  }
$$

in $\mathbf{H}$ (where the bottom right square is an [[(∞,1)-pullback]]). All this lives is $\mathbf{H}_{/\mathbf{B}^2 U(1)}$, but we don't try to draw this here.

Here on the left we have an equivariant symplectic case as above

$$
  \array{
    && \mathcal{O}_\lambda // G
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow_\xi && \ast//G
    \\
    & \searrow && \swarrow
    \\
    && \mathbf{B}^2 U(1)_{conn^1}
  }
  \,.
$$

Where $\xi$ now is a $G$-equivariant [[prequantum bundle]] exhibiting a [[moment map]] for a [[Hamiltonian action]] of $G$.

The motivic quantization yields the map in [[equivariant K-theory]]

$$
  i_! \colon K_G(\mathcal{O}_\lambda) \to R(G)
$$

to the [[representation ring]] of $G$, which sends the prequantum bundle + Hamiltonian action $\xi$ to the $G$-representation $i_! \xi$. This is known as _[[Dirac induction]]_. It is the cohomological formulation of the [[orbit method]] for a fixed orbit. 

On the other hand the motivic quantization horizontally of the bottom correspondence of [[2d Chern-Simons theories]] in the above diagram, which is

$$
  \array{
  \ast//G &\leftarrow& \mathcal{O}_\lambda // G &\hookrightarrow& \mathfrak{g}^\ast//G
   }
  \,.
$$

About this, ([FHT II, (1.27), theorem 1.28](#FHT)) says the following.


+-- {: .num_prop}
###### Proposition

For $G$ a [[compact Lie group]] with [[Lie algebra]] $\mathfrak{g}^\ast$, the [[push-forward in generalized cohomology|push-forward]] in compactly supported [[twisted K-theory|twisted]] $G$-[[equivariant K-theory]] to the point (the $G$-equivariant [[index]]) produces the [[Thom isomorphism]]

$$
  ind_{\mathfrak{g}^\ast} 
    \;\colon\; 
  K_G^{\sigma + dim G}(\mathfrak{g}^\ast)_{cpt} 
   \stackrel{\simeq}{\to} 
  K_G^0(\ast) \simeq Rep(G)
  \,.
$$

Moreover, for $i \colon \mathcal{O} \hookrightarrow \mathfrak{g}^\ast$ a regular [[coadjoint orbit]], [[push-forward in generalized cohomology|push-forward]] involves a [[twisted K-theory|twist]] $\sigma$ of the form

$$
  Rep(G) \simeq K_G^0(\ast)
  \stackrel{ind_{\mathcal{O}}}{\leftarrow}
  K_G^{\sigma(\mathcal{O}) + dim(\mathcal{O})}(\mathcal{O})
  \stackrel{i_!}{\to}
  K_G^{\sigma + dim G}(\mathfrak{g}^\ast)_{cpt}
$$

and 

1. $i_!$ is surjective 

1. $ind_{\mathcal{O}} = ind_{\mathfrak{g}^\ast} \circ i_!$.

=--





##### Poisson holography 
 {#PoissonHolography}

The [[trajectory]] space of any [[mechanical system]] carries a natural [[Poisson bracket]]: the "[[off-shell Poisson bracket]]". When one considers this as the [[boundary field theory]] of the corresponding Poisson [[2d Chern-Simons theory]] as above, then one finds the following relation:

the [[field (physics)|fields]] of the 2d [[bulk field theory]] are the [[sources]] of the 1d mechanical system. This relation is one of the characteristic properties of what is called the _[[holographic principle]]_.

More discussion of this formalization of the [[holographic principle]] is at 

* _[off-shell Poisson bracket -- boundary field theory interpretation](off-shell+Poisson+bracket#BoundaryFieldTheoryInterpretation)_

* _[holographic principle -- Poisson holography](holographic+principle#PoissonHolography)_


#### The charged particle at the boundary of the open superstring
 {#ChargedParticleAtBoundaryOfSuperstring}

* $X$ [[spacetime]]

* $\chi \colon X \to \mathbf{B}^2 U(1)$  [[B-field]]

  this is the [[background gauge field]]/[[local action functional]] for the [[type II string]] 2d [[sigma-model]] field theory


* $i \colon Q \hookrightarrow X$ [[D-brane]] [[worldvolume]]

* $\xi \in K^{\bullet + i^\ast \chi}(Q)$ [[Chan-Paton gauge field]]

$$
  \array{
    && Q
    \\
    & \swarrow && \searrow^{\mathrlap{i}}
    \\
    \ast && \swArrow_{\xi} && X
    \\
    & \searrow && \swarrow
    \\
    && \mathbf{B}^2 U(1)
    \\
    && \downarrow
    \\
    && \mathbf{GL}_1(\mathbf{KU})
  }
  \,.
$$

[[Umkehr map]] yields

$$
  \Gamma_Q( i^\ast \chi + W_3(N_i Q) ) \to \Gamma_X(\chi)
  \;\;\;\;\;
  in KU Mod
$$

compatibility is _[[Freed-Witten-Kapustin anomaly cancellation]]_

##### D-Brane charge
 {#DBraneCharge}

We interpret the [[Freed-Witten-Kapustin anomaly]] mechanism in terms of [[push-forward in generalized cohomology]] in [[topological K-theory]] interpreted in terms of [[KK-theory]] with push-forward maps given by [[dual morphisms]] between [[Poincaré duality C*-algebras]] (based on [Brodzki-Mathai-Rosenberg-Szabo 06, section 7](#BrodzkiMathaiRosenbergSzabo06), [Tu 06](#Tu06)):

Let $i \colon Q \to X$ be a map of [[compact topological space|compact]] [[manifolds]] and let $\chi \colon X \to B^2 U(1)$ modulate a [[circle 2-bundle]] regarded as a [[twisted K-theory|twist for K-theory]]. Then forming [[twisted groupoid convolution algebras]] yields a [[KK-theory]] morphism of the form

$$
  C_{i^\ast \chi}(Q)
  \stackrel{i^\ast}{\longleftarrow}
  C_{\chi}(X)
  \,,
$$

with notation as in [this definition](Poincar&#233;+duality+algebra#CStarAlgebraOf2BundleOnManifold). By [this proposition](Poincar&#233;+duality+algebra#DualOfCompactManifoldWithTwist) the [[dual morphism]] is of the form

$$
  C_{\frac{1}{i^\ast \chi \otimes W_3(T Q)}}(Q)
  \stackrel{i_!}{\longrightarrow}
  C_{\frac{1}{\chi \otimes W_3(T X)}}(X)
  \,.
$$

If we redefine the twist on $X$ to absorb this "quantum correction" as $\chi \mapsto \frac{1}{\chi \otimes W_3(T X)}$ then this is

$$
  C_{i^\ast \chi\frac{W_3(i^\ast T X)}{W_3(T Q)}}(Q)
  \stackrel{i_!}{\longrightarrow}
  C_{\chi}(X)
  \,,
$$

where now we may interpret $\frac{W_3(i^\ast \tau_X)}{W_3(\tau_Q)}$ as the third [[integral Stiefel-Whitney class]] of the [[normal bundle]] $N Q$ of $i$ (see [Nuiten](#Nuiten)).

Postcomposition with this map in [[KK-theory]] now yields a map from the $i^\ast \chi \otimes W_3(N Q)$-[[twisted K-theory]] of $Q$ to the $\chi$-[[twisted K-theory]] of $X$:

$$
  i_! \colon K_{\bullet + W_3(N Q) + i^\ast \chi}(Q) \to K_{\bullet +\chi}
  \,.
$$

If we here think of $i \colon Q \hookrightarrow X$ as being the inclusion of a [[D-brane]] [[worldvolume]], then $\chi$ would be the class of the [[background gauge field|background]] [[B-field]] and an element 

$$
  [\xi] \in K_{\bullet + W_3(N Q) + i^\ast \chi}(Q)
$$ 

is called (the K-class of) a _[[Chan-Paton gauge field]]_ on the D-brane satisfying the _[[Freed-Witten-Kapustin anomaly]] cancellation mechanism_. (The orginal _Freed-Witten anomaly cancellation_ assumes $\xi$ given by a [[twisted unitary bundle|twisted line bundle]] in which case it exhibits a [[twisted spin^c structure]] on $Q$.) Finally its [[fiber integration|push-forward]]

$$
  [i_! \xi] \in K_{\bullet + \chi}(X)
$$

is called the corresponding _[[D-brane charge]]_.

##### Topological T-duality

* [[topological T-duality]]

### Dimension 3
 {#ExamplesDimension3}

#### The heterotic string at the boundary of the M2-brane
 {#HeteroticStringAtBoundaryOfMembrane}

In the previous example _[The charged particle at the boundary of the superstring](#ChargedParticleAtBoundaryOfSuperstring)_ we saw -- by analogy with the [particle at the boundary of the 2d Chern-Simons theory](#PoissonManifoldAtTheBoundaryOf2dChernSimonsTheory) -- the motivic quantization with [[coefficients]] in [[KU]] of the 1-dimensional field which is the [[sigma-model]] of a [[charged particle]] at the intersection of a 2-dimensional field theory which is an  [[open string]] [[sigma-model]] ending on a [[D-brane]]. Here we lift all these ingredients up one dimension and consider the motivic quantization with coefficients in [[tmf]] of the 2-dimensional field theory called the _[[heterotic string]]_ [[sigma-model]] as the boundary intersection of the 3d field theory known as the _[[M2-brane]]_ with a [[brane]] called sometimes the _[[M9-brane]]_ or the $O9$-plane of [[Hořava-Witten theory]].

The analog of the $\mathbb{Z}$-valued [[index]]/[[partition function]] in the [[K-theory]] of the point now is the [[Witten genus]] with values in [[topological modular forms]]

* _[The Witten genus](#TheWittenGenus)_

and the analog of the [[D-brane charge]] in the [[K-theory]] of the [[type II supergravity]] [[spacetime]] is

* _[The M9-brane charge](#TheO9PlaneCharge)_ 

in [[tmf]]-[[cohomology theory|cohomology]] of the [[11-dimensional supergravity]] [[spacetime]].

$\,,$

More in detail, the setup is the following.

* Let $X$ be a $\mathbb{Z}_2$-[[orbifold]] equipped with [[spin structure]], to be called the 11-dimensional [[spacetime]] of [[Hořava-Witten theory|Hořava-Witten]] [[11-dimensional supergravity]]/[[M-theory]];

* Let $\chi \colon X \to \mathbf{B}^3 U(1)$ be the ([[instanton sector]] of a) [[circle n-bundle with connection|circle 3-bundle]] on $X$. This is to be called the [[supergravity C-field]];  by the discussion there and at ([FSS 12b](#FSS12b)) this is constrained to satisfy

  $$
    \chi \simeq \tfrac{1}{2}\mathbf{p}_1(X) + 2 \mathbf{a}
    \,,
  $$

  where $\tfrac{1}{2}\mathbf{p}_1$ denotes the [[first fractional Pontryagin class]] and $\mathbf{a}$ the [[second Chern class]] of an auxiliary [[E8]]-[[principal bundle]].

  This is to be called the [[background gauge field]]/[[local action functional]] for the [[M2-brane]] 3d [[sigma-model]] field theory with [[target space]] $X$.

* Write $Q \hookrightarrow X$ for the inclusion of the locus of $\mathbb{Z}_2$-fixed points of $X$. This is to be called the "[[M9-brane]]" [[worldvolume]] or equivalently the [[spacetime]] of [[heterotic string theory]] in [[Hořava-Witten theory]].

* This data is required to constitute a [[higher orientifold]] structure on $X$ which means in particular that there is a trivialization

  $$
    \xi \;\colon\; \chi|_Q \simeq 0
  $$ 

  of the restriction of the background field to the $\mathbb{Z}_2$-fixed points; and hence by the above

  $$
    \xi \;\colon\; \tfrac{1}{2}\mathbf{p}_1(Q)  + 2 \mathbf{a}|_Q \simeq 0
  $$

  By the discussion in ([FSS 09](#FSS09)) this is to be called the twisted [[B-field]] of [[heterotic string theory]] on $Q$, exhibited by the  [[string^c structure]] $\tfrac{1}{2}\mathbf{p}_1(Q) \simeq 2 \mathbf{a}|Q$ on $Q$.

This data is summarized as constituting a [[correspondence]] for a [[boundary field theory|boundary]] [[prequantum field theory]] in dimensions 2, 3 as follows:

$$
  \array{
    && Q
    \\
    & \swarrow && \searrow^{\mathrlap{i}}
    \\
    \ast
    && 
     \swArrow_{\xi }
    &&
    X
    \\
    & \searrow && \swarrow_{\mathrlap{\chi \simeq \tfrac{1}{2}\mathbf{p}_1(X) + 2 \mathbf{a}}}
    \\
    && \mathbf{B}^3 U(1)
  }
$$

By ([ABG](#ABG)) we have:

+-- {: .num_prop }
###### Proposition

Circle 3-bundles canonically twist the [[cohomology theory]] [[tmf]] in that there is a canonical morphism

$$
  B^3 U(1) \to B GL_1(tmf)
  \,.
$$

=--

Therefore we may consider the motivic quantization of the above setup with coefficients in [[tmf]]-[[∞-modules]]:

$$
  \array{
    && Q
    \\
    & \swarrow && \searrow^{\mathrlap{i}}
    \\
    \ast
    && 
     \swArrow_{\xi}
    &&
    X
    \\
    & \searrow && \swarrow_{\mathrlap{\chi}}
    \\
    && \mathbf{B}^3 U(1)
    \\
    && \downarrow
    \\
    && tmf Mod
  }
$$


##### The Witten genus
 {#TheWittenGenus}


If the [[first fractional Pontryagin class]] of $Q$ indeed vanishes on $Q$, hence in the case that $2\mathbf{a}|_Q \simeq 0$, then the [[push-forward in generalized cohomology]] to the point exists in [[tmf]]

$$
  tmf^\bullet(Q) \to tmf^\bullet(\ast)
  \,.
$$

Here $\pi_0(tmf^\bullet(\ast))$ is the ring of [[topological modular forms]]. An element in here can be interpreted as the [[partition function]] of a [[2d super conformal field theory]] in dependence of the modulus of the conformal torus [[worldsheet]]. As such the image of the above map is the [[partition function]] of the heterotic string, called the _[[Witten genus]]_. See there for discussion and references dealing with this relation.

More generally, if $2\mathbf{a}$ does not vanish but is the [[cup product]] square of a [[line bundle]], then a twisted Witten genus still exists ([Chen-Han-Zhang 10](#ChenHanZhang10))).


##### The M9-brane charge
 {#TheO9PlaneCharge}

By ([ABG, (11.2)](#ABG)) we have:

+-- {: .num_prop }
###### Proposition

In the [above situation](#HeteroticStringAtBoundaryOfMembrane) the [[push-forward in generalized cohomology|push-forward]] in [[tmf]] goes form the untwisted [[tmf]]-[[cohomology theory|cohomology]] of the [[heterotic supergravity]] [[spacetime]] $Q$ to the $(-2a)$-[[twisted cohomology|twisted]] [[tmf]]-[[cohomology theory|cohomology]] of the [[11-dimensional supergravity]] [[spacetime]]:

$$
  tmf^\bullet(Q) \to tmf^\bullet(X)_{-2\mathbf{a}}
  \,.
$$

=--

This perspective on the [[Green-Schwarz anomaly cancellation]] condition in [[heterotic string theory]] as an [[orientation in generalized cohomology|orientation]] in [[twisted cohomology|twisted]] [[tmf]] originates in ([Sati 10](#Sati10)).

By analogy with the above discussion of _[D-brane charge](#DBraneCharge)_ the image of this map might be called the _$M9$-brane charge_. 


#### The boundary of 3d Chern-Simons theory

(...)

According to ([Witten 89, around (2.20)](Chern-Simons%20theory#Witten)) the regularization of ordinary $G$-[[Chern-Simons theory]] involves coupling it so an $O(n)$-Chern-Simons theory. Moreover the "framing anomaly" (see at _[[2-framing]]_) requires that $\frac{1}{2}p_1$ vanishes .

We are thus in a situation similar to that of the membrane theory [above](#HeteroticStringAtBoundaryOfMembrane).

(...)




## References
 {#References}

After a pointer to some

* _[Introductions and lecture note](#IntroductionsAndLectureNotes)_

we first list references and notes along the lines of the above discussion in 

* _[Accounts of the above material](#AccountsOfTheAboveMaterial)_

and then give an extensive list of precursors of articles on aspects of the idea of motivic quantization as laid out here in 

* _[Related work on the idea of motivic quantization](#PrevLit)_

### Introductions and lecture notes
 {#IntroductionsAndLectureNotes}

Introductions and lecture notes on material used here include

* _[[geometry of physics|Geometry of physics]]_ 

  (on basics of [[fundamental physics]] formulated naturally in [[higher differential geometry]])

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:A higher stacky perspective on Chern-Simons theory]]_ ([arXiv:1301.2580](http://arxiv.org/abs/1301.2580))

  (on the formulation of [[local action functionals]] in [[higher differential geometry]])

* _[[twisted smooth cohomology in string theory|Twisted smooth cohomology in string theory]]_, [lectures at](http://maths-old.anu.edu.au/esi/2012/program.html#Schreiber)  _[ESI Program on K-Theory and Quantum Fields](http://maths-old.anu.edu.au/esi/2012/)_ (2012)

  (on local/extended/higher structures naturally seen in the [[local prequantum field theory]] involved in [[string theory]]);


section 1 "Introduction" of 

* _[[schreiber:differential cohomology in a cohesive topos]]_

  (on the formulation of [[higher topos theory]]).

* _[[schreiber:Synthetic Quantum Field Theory]]_

  _[geometric of physics -- The full story in a few formal words](geometry%20of%20physics#TabulatedIndex)_

  (a summary and survey of the axiomatics).
   {#SyntheticQuantumFieldTheory}


### Accounts of the above material
 {#AccountsOfTheAboveMaterial}

The discussion of motivic quantization as laid out here appears in 

* [[Joost Nuiten]], _[[schreiber:master thesis Nuiten|Cohomological quantization of local prequantum boundary field theory]]_, master thesis, August 2013
 {#Nuiten13}

* [[Urs Schreiber]], _[[schreiber:Motivic quantization of prequantum field theory]]_, talk at _[GAP XI &#8211; Higher Geometry and Quantum Field Theory](http://www.personal.psu.edu/yuv1/blogs/gap/)_, August 2013

This is based on previous work such as

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Twisted Differential String and Fivebrane Structures]]_ ([arXiv:0910.4001](http://arxiv.org/abs/0910.4001))
 {#FSS09}

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Cech Cocycles for Differential characteristic Classes]]_ ([arXiv:1011.4735](http://arxiv.org/abs/1011.4735))
 {#FiorenzaSchreiberStasheff10}

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:7d Chern-Simons theory and the 5-brane]]_ ([arXiv:1201.5277](http://arxiv.org/abs/1201.5277))
 {#FSS12a}

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]],  _[[schreiber:The moduli 3-stack of the C-field]]_ ([arXiv:1202.2455](http://arxiv.org/abs/1202.2455))
 {#FSS12b}

* [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher geometric prequantum theory]]_ ([arXiv:1304.0236](http://arxiv.org/abs/1304.0236))
 {#FiorenzaRogersSchreiber13a}

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_
 {#WZWLie}

* [[Joost Nuiten]], [[Urs Schreiber]], _[[schreiber:Local prequantum field theory]]_
 {#lpqft}

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet]]_
  {#FiorenzaSatiSchreiber13}


### Related work on the idea of motivic quantization
 {#PrevLit}

The following is a list of "precursors" of aspects of the idea motivic quantization as laid out here.

$\,$

The formulation of [[geometric quantization]] as an [[index]] map in [[K-theory]] is attributed to [[Raoul Bott]].

The proposal that the natural [[domain]] for geometric quantization are [[Lagrangian correspondences]] is due to 

* [[Lars Hörmander]], _Fourier Integral Operators I._,
Acta Math. 127 (1971)
 {#Hoermander71}

* [[Alan Weinstein]], _Symplectic manifolds and their lagrangian submanifolds_, Advances in Math. 6 (1971)
 {#Weinstein71}

With the recognition of [[supersymmetric quantum mechanics]] in the 1980s, [[index theory]] (hence [[push-forward in generalized cohomology]] to the point) was understood to be about [[partition functions]] of systems of [[supersymmetric quantum mechanics]] in 

* [[Luis Alvarez-Gaumé]], _Supersymmetry and the Atiyah-Singer index theorem_, Comm. Math. Phys. Volume 90, Number 2 (1983), 161-173. ([Euclid](http://projecteuclid.org/euclid.cmp/1103940278))
 {#AlvarezGaume83}

* [[Ezra Getzler]], _Pseudodifferential operators on supermanifolds and the Atiyah-Singer index theorem_, Comm. Math. Phys. 92 (1983), 163-178. ([pdf](http://math.northwestern.edu/~getzler/Papers/1103940796.pdf))
 {#Getzler83}

*  [[Ezra Getzler]], _A short proof of the Atiyah-Singer index theorem_, Topology 25 (1986), 111-117 ([pdf](http://math.northwestern.edu/~getzler/Papers/local.pdf))

In higher analogy to this but much more subtly, the [[partition function]] of the [[heterotic string]], hence the [[Witten genus]], was understood to be the [[push-forward in generalized cohomology|push-forward]] to the point in [[tmf]]:

* [[Matthew Ando]], [[Mike Hopkins]], [[Charles Rezk]], _Multiplicative orientations of KO-theory and the spectrum of topological modular forms_, 2010 ([pdf](http://www.math.uiuc.edu/~mando/papers/koandtmf.pdf))
  {#AndoHopkinsRezk}

The general perspective of the [[path integral as a pull-push transform]] was originally laid out, somewhat implicitly, in

* [[Daniel Freed]]

  * _Quantum groups from path integrals_ ([arXiv:q-alg/9501025](http://xxx.lanl.gov/abs/q-alg/9501025))

  * _Higher algebraic structures and quantization_ ([arXiv:hep-th/9212115](http://arxiv.org/abs/hep-th/9212115))

and then fully explicitly in

* [[Daniel Freed]], _Twisted K-theory and the Verlinde ring_, Andrejewski lecture ([html slides](http://www.ma.utexas.edu/users/dafr/Andrejewski%20Lectures.html))

Discussion along these lines of a pull-push quantization over [[KU]] of a 2-dimensional [[Chern-Simons theory]]-like [[gauge theory]] is in 

* {#FreedHopkinsTeleman07} [[Daniel Freed]], [[Michael Hopkins]], [[Constantin Teleman]], _Consistent Orientation of Moduli Spaces_ ([arXiv:0711.1909](http://arxiv.org/abs/0711.1909)), chapter XIX, pages 395-419 in: Oscar Garcia-Prada, Jean Pierre Bourguignon, Simon Salamon (eds.) _The Many Facets of Geometry: A Tribute to Nigel Hitchin_, Oxford University Press 2010 ([doi:10.1093/acprof:oso/9780199534920.001.0001](http://www.oxfordscholarship.com/view/10.1093/acprof:oso/9780199534920.001.0001/acprof-9780199534920))

More in detail a functorial quantization of suitable correspondences of smooth manifolds to [[KK-theory]] by pull-push has been given in ([Connes-Skandalis 84](#ConnesSkandalis84)) and the generalization of that to [[equivariant K-theory]] (hence to [[groupoid K-theory]] of [[action groupoids]]) is in

* [[Heath Emerson]], [[Ralf Meyer]], _Bivariant K-theory via correspondences_, Adv. Math. 225 (2010), 2883-2919 ([arXiv:0812.4949](http://arxiv.org/abs/0812.4949))
 {#EmersonMeyer08}



The point of view that the [[path integral as a pull-push transform|pull-push quantization]] of [[Gromov-Witten theory]] should be thought of as a theory of [[Chow motives]] of [[Deligne-Mumford stacks]] is expressed in 

* [[Kai Behrend]], [[Yuri Manin]], _Stacks of Stable Maps and Gromov-Witten Invariants_ ([arXiv:alg-geom/9506023](http://arxiv.org/abs/alg-geom/9506023))
 {#BehrendManin95}

* [[Bertrand Toën]], _On motives for Deligne-Mumford stacks_, International Mathematics Research Notices 2000, 17 (2000) 909-928 ([arXiv:math/0006160](http://arxiv.org/abs/math/0006160), [web](http://hal.archives-ouvertes.fr/hal-00773027), [pdf](http://hal.archives-ouvertes.fr/docs/00/77/30/27/PDF/motdm.pdf))
 {#Toen00}


The proposal that the natural [[codomain]] for geometric quantization is [[KK-theory]] is due to 

* [[Klaas Landsman]], _Functorial quantization and the Guillemin-Sternberg conjecture_ Proc. Bialowieza 2002 ([arXiv:math-ph/0307059](http://arxiv.org/abs/math-ph/0307059))

* [[Klaas Landsman]], _Functoriality of quantization: a KK-theoretic approach_, talk at ECOAS, ECOAS, Dartmouth College, October 2010 ([web](http://www.academia.edu/1992202/Functoriality_of_quantization_a_KK-theoretic_approach))


The point of view that pull-push along [[correspondences]] equipped with [[operator K-theory]] [[cycles]] in [[KK-theory]] is a [[K-theory]]-analog of [[motives]] was amplified in 

* [[Alain Connes]], [[Georges Skandalis]], _The longitudinal index theorem for foliations_. Publ. Res. Inst. Math. Sci. 20,
no. 6, 1139&#8211;1183 (1984) ([pdf](http://www.alainconnes.org/docs/longitudinal.pdf))
 {#ConnesSkandalis84}

* [[Alain Connes]], Caterina Consani, [[Matilde Marcolli]], _Noncommutative geometry and motives: the thermodynamics of endomotives_ ([arXiv:math/0512138](http://arxiv.org/abs/math/0512138))
 {#ConnesConsaniMarcolli05}

The proof that the [[universal property]] that characterizes [[noncommutative motives]] is the analog in [[noncommutative algebraic geometry]] of the [[universal property]] that characterizes [[KK-theory]] in [[noncommutative topology]] is due to

* [[Gonçalo Tabuada]], _K-theory via universal invariants_, Duke Math. J. 145 (2008), no.1, 121&#8211;206.
 {#Tabuada08}

* [[Denis-Charles Cisinski]], [[Gonçalo Tabuada]], _Non connective K-theory via universal invariants_. Compositio
Mathematica 147 (2011), 1281&#8211;1320 ([arXiv:0903.3717](http://arxiv.org/abs/0903.3717))
 {#CisinskiTabuada11}

* [[Andrew Blumberg]], [[David Gepner]], [[Gonçalo Tabuada]], _A universal characterization of higher algebraic K-theory_,  Geometry and Topology ([arXiv:1001.2282](http://arxiv.org/abs/1001.2282))
 {#BlumbergGepnerTabuada10}

The description of [[string topology]] operations as an [[HQFT]] defined by pull-push transforms in [[ordinary homology]]/[[ordinary cohomology]] was originally realized in 

* [[Ralph Cohen]], [[Veronique Godin]],  _[[A Polarized View of String Topology]]_ ([arXiv:math/0303003](http://arxiv.org/abs/math/0303003))

* Hirotaka Tamanoi, _Loop coproducts in string topology and triviality of higher genus TQFT operations_ (2007) ([arXiv:0706.1276](http://arxiv.org/abs/0706.1276))
 {#Tamanoi07}

A detailed discussion and generalization to [[open strings]] and an open-closed [[HQFT]] in the presence of a single space-filling [[brane]] is in

* [[Veronique Godin]], _Higher string topology operations_ (2007)([arXiv:0711.4859](http://arxiv.org/abs/0711.4859))
 {#Godin}

and for arbitrary [[branes]] in 

* [[Alexander Kupers]], _String topology operations_ MS thesis (2011) ([pdf](http://math.stanford.edu/~kupers/thesis7thjune2011.pdf))

That [[D-brane charge]] and [[T-duality]] is naturally understood in terms of pull-push/[[indices]] along [[correspondences]] in [[noncommutative topology]]/[[KK-theory]] was amplified in 

* [[Jacek Brodzki]], [[Varghese Mathai]], [[Jonathan Rosenberg]], [[Richard Szabo]],  _Noncommutative correspondences, duality and D-branes in bivariant K-theory_, Adv. Theor. Math. Phys.13:497-552,2009 ([arXiv:0708.2648](http://arxiv.org/abs/0708.2648))
 {#BMRS2}

The general analogy between such [[KK-theory]] cocycles and [[pure motives]] is noted explicitly in 

* [[Alain Connes]], Caterina Consani, [[Matilde Marcolli]], _Noncommutative geometry and motives: the thermodynamics of endomotives_ ([arXiv:math/0512138](http://arxiv.org/abs/math/0512138))
 {#ConnesConsaniMarcolli05}

* [[Alain Connes]], [[Matilde Marcolli]], _[[Noncommutative Geometry, Quantum Fields and Motives]]_

This analogy is given a precise form in

*  [[Snigdhayan Mahanta]], _Higher nonunital Quillen $K'$-theory, KK-dualities, and applications to topological T-duality_, ([pdf](http://wwwmath.uni-muenster.de/u/snigdhayan.mahanta/papers/KQ.pdf), [talk notes](http://wwwmath.uni-muenster.de/u/snigdhayan.mahanta/papers/KKTD.pdf))
 {#Mahanta13}

where it is shown that there is a universal functor $KK \longrightarrow NCC_{dg}$ from [[KK-theory]] to the category of [[noncommutative motives]], which is the category of [[dg-categories]] and dg-[[profunctors]] up to homotopy between them. This is given by sending a [[C*-algebra]] to the [[dg-category]] of [[perfect complexes]] of (the unitalization of) its underlying [[associative algebra]].


Linearization of correspondences of [[discrete groupoid|geometrically discrete groupoids]] was considered in 

* [[John Baez]], [[Jim Dolan]], _Groupoidification_, November 2009 ([web](http://math.ucr.edu/home/baez/groupoidification/))

and applied to a pull-push quantization of [[Dijkgraaf-Witten theory]] in 

* [[Jeffrey Morton]], _2-Vector Spaces and Groupoids_ ([arXiv:0810.2361](http://arxiv.org/abs/0810.2361))

* [[Jeffrey Morton]], _Cohomological Twisting of 2-Linearization and Extended TQFT_ ([arXiv:1003.5603v4](http://arxiv.org/abs/1003.5603v4))
 {#Morton10}

following previous work by [[Daniel Freed]] and [[Frank Quinn]].

An unpublished predecessor note on quantization of correspondences of moduli stacks of fields is 

* [[Urs Schreiber]], _[[schreiber:Nonabelian cocycles and their quantum symmetries]]_ (2008)
 {#Schreiber08}

Quantization of [[correspondences]] of [[perfect ∞-stacks]] by pull-push of [[stable (∞,1)-categories]] of [[quasicoherent sheaves]] is discussed in

* [[David Ben-Zvi]], [[John Francis]], [[David Nadler]],
_[[geometric function theory|Integral Transforms and Drinfeld Centers in Derived Algebraic
Geometry]]_, J. Amer. Math. Soc. 23 (2010), no. 4, 909-966,
([arXiv:0805.0157](http://arxiv.org/abs/0805.0157))

Linearization of [[higher correspondences]] of [[discrete ∞-groupoids]] as the quantizaton of [[∞-Dijkgraaf-Witten theories]] is indicated in section 3 and 8 of 

* {#FreedHopkinsLurieTeleman09} [[Daniel Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], _[[Topological Quantum Field Theories from Compact Lie Groups]], in P. Kotiuga (ed.), _A Celebration of the Mathematical Legacy of Raoul Bott,  AMS, (2010) ([arXiv:0905.0731](http://arxiv.org/abs/0905.0731))
 

and in 

* [[Jacob Lurie]], _[[Ambidexterity in K(n)-Local Stable Homotopy Theory]]_, talk at Notre Dame Graduate Summer School on Topology and Field Theories and Harvard lecture 2012 ([pdf](http://www.math.harvard.edu/~lurie/papers/Ambidexterity.pdf))

A clear picture of [[fiber integration]] in [[twisted cohomology]] is developed in 

* [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Twists of K-theory and TMF_, in Robert S. Doran, Greg Friedman, [[Jonathan Rosenberg]], _Superstrings, Geometry, Topology, and $C^*$-algebras_, Proceedings of Symposia in Pure Mathematics [vol 81](http://www.ams.org/bookstore-getitem/item=PSPUM-81), American Mathematical Society ([arXiv:1002.3004](http://arxiv.org/abs/1002.3004))
 {#ABG}

A proposal to axiomatize [[perturbative field theory|perturbative]] [[prequantum field theory]] by functors from [[cobordisms]] to a [[symplectic category]] of [[symplectic manifolds]] and [[Lagrangian correspondences]] is in 

* [[Alberto Cattaneo]], [[Pavel Mnev]], [[Nicolai Reshetikhin]], _Classical and quantum Lagrangian field theories with boundary_ ([arXiv:1207.0239](http://arxiv.org/abs/1207.0239), [pdf slides](http://users.uoa.gr/~iandroul/GAP%202012%20WEBPAGE/GAP2012_Cattaneo.pdf))
 {#CattaneoMnevReshetikhin12}

* [[Damien Calaque]], _Lagrangian structures on mapping stacks and semi-classical TFTs_ ([arXiv:1306.3235](http://arxiv.org/abs/1306.3235))

### On aspects of quantization
 {#ReferencesOnAspectsOfQuantization}

#### General

* [[Michael Atiyah]], [[Raoul Bott]], _The moment map and equivariant cohomology_, Topology, Vol 23, No. 1 (1984) ([pdf](https://www.math.sunysb.edu/~mmovshev/MAT570Spring2008/BOOKS/atiyahbott_moment.pdf))
  {#AtiyahBott84}

#### Orbit method

* [[Daniel Freed]], [[Michael Hopkins]], [[Constantin Teleman]], part II of _[[Loop Groups and Twisted K-Theory]]_
 {#FHT}




### On aspects of generalized cohomology

#### Ordinary cohomology

The [[Riemann-Hilbert correspondence]]/[[de Rham theorem]] for $H A$-modules is established in 

* [[Jonathan Block]], Aaron Smith, _A Riemann--Hilbert correspondence for infinity local systems_ ([arXiv:0908.2843](http://arxiv.org/abs/0908.2843))
 {#BlockSmith09}

#### K-Theory

The refinement of [[operator K-theory]] to a functor to [[KU]]-[[module spectra]] is due to

* [[Ulrich Bunke]], [[Michael Joachim]], [[Stephan Stolz]], _Classifying spaces and spectra representing the K-theory of a graded $C^\ast$-algebra_, High-dimensional manifold topology, World Sci. Publ., River Edge, NJ, 2003, pp. 80&#8211;102
 {#BunkeJoachimStolz03}

* [[Ivo Dell'Ambrogio]], [[Heath Emerson]], [[Tamaz Kandelaki]], [[Ralf Meyer]], _A functorial equivariant K-theory spectrum and an equivariant Lefschetz formula_ ([arXiv:1104.3441](http://arxiv.org/abs/1104.3441))
 {#DEKM11}

The functoriality of [[twisted groupoid K-theory]] is discussed in 

* Alexander Alldridge, [[Jeffrey Giansiracusa]], _Contravariant functoriality for twisted K-theory of stacks_, Oberwolfach Reports no. 46 (2006) 2796 &#8211; 2800 ([pdf](http://maths.swan.ac.uk/staff/jhg/papers/functoriality.pdf))
 {#AlldridgeGiansiracusa06}

and ([Nuiten 13](#Nuiten13)).

The formulation of push-forward in [[KK-theory]] by postcomposition with [[dual morphisms]] is based on the observations in section 7 of 

* Jacek Brodzki, [[Varghese Mathai]], [[Jonathan Rosenberg]], [[Richard Szabo]], _D-Branes, RR-Fields and Duality on Noncommutative Manifolds_, Commun. Math. Phys. 277:643-706,2008 ([arXiv:hep-th/0607020](http://arxiv.org/abs/hep-th/0607020))
 {#BrodzkiMathaiRosenbergSzabo06}

and generalized to [[equivariant K-theory|equivariant]] [[KK-theory]] in

* [[Jean-Louis Tu]], _Twisted K-theory and Poincar&#233; duality_ ([arXiv:math/0609556](http://arxiv.org/abs/math/0609556))
 {#Tu06}



#### Elliptic cohomology and $tmf$


The twisted [[Witten genus]] in the presence of [[background gauge field]] hence for a [[twisted string structure]]/[[string^c structure]] was considered in 

* Qingtao Chen, [[Fei Han]], [[Weiping Zhang]], _Generalized Witten Genus and Vanishing Theorems_ ([arXiv:1003.2325](http://arxiv.org/abs/1003.2325))
 {#ChenHanZhang10}

The identification of the [[Green-Schwarz anomaly cancellation]] condition of [[heterotic string theory]] as a [[string^c structure]] and the proposal that this hence is to be regarded as an [[orientation in generalized cohomology|orientation]] in [[twisted cohomology|twisted]] [[tmf]] is due to 

* [[Hisham Sati]], _[[Geometric and topological structures related to M-branes]]_ ([arXiv:1001.5020](http://arxiv.org/abs/1001.5020))
 {#Sati10}