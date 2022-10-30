
{:bluebox: .un_remark style="border:solid #000000;background: #E6DF13;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functorial quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}



## Idea
 {#GeneralIdea}

_Functorial quantum field theory_ or FQFT for short, is one of the two approaches of providing a precise [[mathematics|mathematical]] formulation of and of [[axiom|axiomatizing]] [[quantum field theory]]. FQFT formalizes the _[[Schrödinger picture]]_ of [[quantum mechanics]] (generalized to [[quantum field theory]]) where [[spaces of quantum states]] are assigned to [[space]] and where linear maps are assigned to [[trajectories]]/[[spacetimes]] interpolating between these spaces.


### As an axiomatization of the path integral and S-Matrix

The axioms of FQFT may be understood as formulating the basic properties that the [[path integral]] or [[S-matrix]] involked in [[physics]] ought to satisfy, if they had been given a precise definition.

Much work in [[quantum field theory]] is based on arguments invoking the concept of the [[path integral]]. While in the physics literature this is usually not a well defined object, it is generally assumed to satisfy a handful of properties, notably the _sewing laws_. These say, roughly, that the path integral over a domain $\Sigma$ which decomposes into subdomains $\Sigma_1$ and $\Sigma_2$ is the same as the path integral over $\Sigma_1$ composed with that over $\Sigma_2$.

Accordingly it is the _[[S-matrix]]_ that is manifestly incarnated in the Atiyah-Segal picture of functorial QFT:

Here a [[quantum field theory]] is given by a [[strong monoidal functor|monoidal]] [[functor]] 

$$
 Z \colon Bord_d^S \longrightarrow Vect
$$

from a suitable [[monoidal category|monoidal]] [[category of cobordisms]] to a suitable [[monoidal category]]  of [[vector spaces]].

* To a codimension-1 slice $M_{d-1}$ of space this assigns a vector space $Z(M_{d-1})$ -- the (Hilbert) [[space of quantum states]] over $M_{d-1}$;

* to a [[spacetime]]/[[worldvolume]] manifold $M$ with [[boundaries]] $\partial M$ one assigns the quantum propagator which is the linear map $Z(M) : Z(\partial_{in} M) \to Z(\partial_{out} M)$ that takes incoming states to outgoing states via propagation along the spacetime/worldvolume $M$. This $Z(M)$ is alternatively known as the  the _[[scattering amplitude]]_ or _S-matrix_ for propagation from $\partial_{in}M$ to $\partial_{out}M$ along a process of shape $M$.

Now for genuine [[topological field theories]] all spaces of quantum states are [[finite number|finite]] [[dimension|dimensional]] and hence we can equivalently consider the [[dual vector space]] (using that finite dimensional vector spaces form a [[compact closed category]]). Doing so the propagator map

$$
  Z(M) : Z(\partial_{in}M) \to Z(\partial_{out}M)
$$

equivalently becomes a linear map of the form

$$
  \mathbb{C} \to Z(\partial_{out}M) \otimes Z(\partial_{in}M)^\ast = Z(\partial M)
  \,.
$$

Notice that such a linear map from the canonical 1-dimensional complex vector space $\mathbb{C}$ to some other vector space is equivalently just a choice of element in that vector space. It is in this sense that $Z(M)$ is equivalently a vector in $Z(\partial_{out}M) \otimes Z(\partial_{in}M)^\ast = Z(\partial M)$.

In this form in physics the propagator is usually called the _[[correlator]]_ or _[[n-point function]]_ .  

The axioms of ([Segal 04](#Segal04)) for [[FQFT]] ([[2d CFT]] in this case) were originally explicitly about the propagators/S-matrices, while ([Atiyah 88](#Atiyah88)) formulated it in terms of the correlators this way. Both perspectives go over into each other under duality as above.

Notice that this kind of discussion is not restricted to topological field theory. For instance already plain quantum mechanics is usefully formulated this way, that's the point of [[finite quantum mechanics in terms of dagger-compact categories]].

### As the dual axiomatization to AQFT

Historically older is the proposal for axiomatizing QFT that is known as _[[AQFT]]_, short for _algebraic quantum field theory_. This formalizes the _[[Heisenberg picture]]_ of [[quantum mechanics]], as do modern variants such as [[factorization algebras]]. Here the basic assignment is that of [[algebras of observables]] to regions of [[spacetime]].

In principle [[AQFT]] and FQFT should be two sides of the same medal, and in special cases this has been made precise (see for instance at _[[topological chiral homology]]_) but generally, much as the formulation of FQFT and AQFT themselves remains in progress, so does their precise relation.

[[!include Isbell duality - table]]

### Global ("non-covariant") and local ("covariant") version
 {#AndAndLocalVersion}

Functorial QFT in any dimension $n$ was originally formulated ([Atiyah 88](#Atiyah88), [Segal 04](#Segal04)) as a 1-[[functor]] on a 1-[[category of cobordisms]]. In this formulation there is a [[space of quantum states]] assigned to every global spatial slice of [[spacetime]]/[[worldvolume]], which is then propagated in time/along a parameter. In physics jargon this corresponds to "non-covariant" [[quantization]], in that the slicing of [[spacetime]]/[[worldvolume]] into space and time components breaks [[general covariance]] which is the hallmark specifically of the [[topological quantum field theories]] to which the methods of FQFT apply most immediately.

A local ("[[extended TQFT|extended]]", "multi-tiered") refinement of this is naturally given by passing from 1-functors to [[(∞,n)-functors]] on [[(∞,n)-categories of cobordisms]]. This formulation was vaguely suggested in ([Baez-Dolan 95](#BaezDolan95)) ("[[cobordism hypothesis]]") and formalized in ([Lurie 09](#Luire09)). It captures what in physics jargon would be called "covariant" quantum field theory, in that the "localization down to the point" means that the formalism knows how to glue/propagate in spatial directions just as in time directions, in fact that no such distinction is retained.



## Exposition and Introduction
 {#Introduction}

> under construction

We give here motivation for, introduction to and an exposition of the ideas of [[local quantum field theory|local]] ([[extended TQFT|extended]]) functorial field theory. 

We start in 

* _[Quantum mechanics in Schr&#246;dinger picture](#QuantumMechanicsInSchroedingerPicture)_

by showing how all the basic category-theoretic ideas are already right beneath the surface of the traditional textbook discussion of quantum mechanics. Following that in 

* [Path integral quantization of 1d gauge theory](#PathIntegralQuantizationof1dGaugeTheory)

we show for the simple case of 1-dimensional finite gauge theory how also [[path integral quantization]] of [[prequantum field theory|prequantum]] ([[classical field theory|classical]]) data is naturally organized by monoidal category theory with first bits of [[homotopy theory]] showing up (that will play a more paramount role as one goes upo in dimension).

Then in

* _[Quantum mechanics with interaction and Feynman diagrams](#QMWithInteractionAndFeynmanDiagrams)_

this becomes all the more pronounced when one considers quantum mechanics with interaction as in the [[worldline formalism]] and hence when one considers [[Feynman diagrams]] as diagrams of interactions of [[particles]].

This 1-dimensional functorial description worldline quantum mechanics has an evident generalization to a [[worldsheet]] formulation of [[2d topological field theory]]. This original 1-functorial TQFT axiomatics due to Atiyah and Segal we review in 

* _[Naive generalization: Global 2d TQFT](#Global2dTQFT)_

However, this "naive" generalization is not quite refined enough. Physically one sees this from the fact that the [[topological string]] [[A-model]]/[[B-model]], which is the archetype of a [[2d TQFT]] in physics, is not actually an instance of the Atiyah-Segal axiomatics. Mathematically one sees it from the fact that the 1-category theoretic formulation of 2d [[boundary field theory]] is clearly lacking a "categorical dimension" in order to be satisfactory.

The correct refinement of 2d TQFT to a [[cohomological field theory]] or "[[TCFT]]" with coefficients not just in vector spaces but in [[chain complexes]] of vector spaces we then consider in 

* _[Local2dTQFT -- The topological string](#Local2dTQFT)_

This gives a natural conceptual home to the [[derived categories]] of [[D-branes]] famous from [[homological mirror symmetry]]. But it is still not quite the fully general functorial formalization of quantum field theory.

To get a feeling for what is missing, we next consider [[3d TQFT]] 

* _[Global 3d TQFT -- Chern-Simons theory](#Global3dTQFT)_

* _[Local 3d TQFT -- Modular functor and Wess-Zumino-Witten theory](#Local3dTQFT)_

This finally is enough information to naturally motivate the full formulation of the [[cobordism hypothesis]] in [[symmetric monoidal (infinity,n)-category]] theory in 

* _[General local TQFT](#IntroductionGeneralFormulation)_

### Quantum mechanics in Schr&#246;dinger picture
 {#QuantumMechanicsInSchroedingerPicture}

This section introduces the observation that the basic structures in [[quantum mechanics]] are accurately reflected in [[symmetric monoidal category|symmetric monoidal]] [[category theory]], by explaining the following dictionary:

| [[quantum mechanics]] | [[monoidal category]] [[category theory|theory]] |
|-----------------------|--------------------------------------------------|
| [[space of quantum states]] | [[object]] in a [[category]] |
| [[linear operator]] | [[morphism]] in a [[category]] |
| [[local quantum field theory|local]] [[dynamics|time evolution]] | [[functor]] |
| [[compound system]] [[entanglement]] | [[cartesian monoidal category|non-cartesian]] [[monoidal category|monoidal structure]] |
| [[bra]]/[[ket]] | [[dual objects]] |
| [[Feynman diagram]] | monoidal [[string diagram]] |


#### Time evolution and Functors 
 {#TimeEvolutionAndFunctors}

The basic idea of [[quantum mechanics]] in the "[[Schrödinger picture]]" is to describe a [[quantum mechanical system]] (such as an [[electron]] in the [[electromagnetic field]] of a [[proton]]) by

1. assigning to each time $t \in \mathbb{R}$ a [[vector space]] ([[Hilbert space]]) $V_t$ to be thought of as the [[space of quantum states]] (of [[pure states]], that is) of the system at that time;

1. assigning to each pair $[t_1,t_2]$ of times a [[linear operator]] ([[unitary operator]]) $U(t_1,t_2) \colon V_{t_1} \to V_{t_2}$ to be thought of as encodiding the [[time]] evolution of quantum states

such that 

* this assignment is _local_ in [[time]] in that for all $t_1 \leq t_2 \leq t_3$ one has

  $$
    U(t_1 t_3) = U(t_2, t_3) \circ U(t_1, t_2)
    \,.
  $$

In basic quantum mechanics one also demands that 

$$
  U(t,t) = id
  \,.
$$

(While this looks like the most innocent condition, this has technical subtleties for genuine [[quantum field theory]], for which however there exist established tools to deal with.)
 
The locality condition intuitively says that "all gobal effects arise by integrating up local effects". Indeed, when assuming in addition that $U(-,-)$ depends [[smooth function|smoothly]] on the time arguments, then the locality condition is equivalent to (see at _[[parallel transport]]_) the existence of a [[Hamiltonian]] $H_t$, a [[self-adjoint operator]] depending smoothly on $t$, such that time evolution is given by the [[Dyson formula]]

$$
  U(t_1,t_2)
  =
  P \exp\left(
     \tfrac{i}{\hbar} \int_{t_1}^{t_2}  H_t \, d t
  \right)
  \,.
$$

(Here the notation on the right denotes the "path ordered exponential", see at _[[parallel transport]]_.) In the special case that the Hamiltonian is time-independent,  $H = H_t$, then this reduces to 

$$
  U(t_1,t_2)
  =
  \exp\left(
     \tfrac{i}{\hbar} (t_2-t_2) H 
  \right)
  \,.
$$

This is the way that quantum mechancial time evolution is traditionally introduced in the textbooks.

But the equivalent formulation above in terms of locality of $U(-,-)$ is noteworthy. The condition of locality here is precisely what in [[mathematics]] is called _[[functor|functoriality]]_: the condition that a system of [[homomorphisms]] (here: linear/unitary operator) depends on another system of "directed data" (here: the time intervals $[t_1,t_2]$) such that [[composition]] is respected.

More specifically, one says that the collection [[Vect]] (or [[Hilb]]) of [[vector spaces]] ([[Hilbert spaces]]) forms a _[[category]]_ whose _[[objects]]_ are vector space $V$ and whose _[[morphisms]]_ are linear maps $f \colon V_1 \to V_2$; where the point is that these morphisms may be [[associativity|associatively]] composed whenever their [[codomain]]/[[domain]] matches:

$$
  \array{
    && V_2
    \\
    & {}^{\mathllap{f_1}}\nearrow && \searrow^{\mathrlap{f_2}}
    \\
    V_1 && \stackrel{f_2 \circ f_1}{\longrightarrow} && V_3
  }
  \,.
$$

Similarly, there is a category $Bord_1^{Riem}$ whose [[objects]] are instance of time $t \in \mathbb{R}$, whose [[morphisms]] are time intervals $[t_1,t_2]$, and whose [[composition]] operation is concatenation of time intervals

$$
  \array{
    && t_2
    \\
    & \nearrow && \searrow
    \\
    t_1 && \stackrel{}{\longrightarrow} && t_3
  }
$$

Given two categories like this, then a function that takes morphism of one two morphisms of the other such that [[composition]] is respected is called a _[[functor]]_. 

In this language, the above locality condition of [[quantum mechanics]] says that quantum time evolution is a functor

$$
  U \;\colon\; Bord_1^{Riem} \longrightarrow Vect
$$

that takes

$$
  \array{
    && t_2
    \\
    & \nearrow && \searrow
    \\
    t_1 && \stackrel{}{\longrightarrow} && t_3
  }
  \;\;\;\;\;\;
  \mapsto
  \;\;\;\;\;\;
  \array{
    && V_2
    \\
    & {}^{\mathllap{U(t_1,t_2)}}\nearrow && \searrow^{\mathrlap{U(t_2,t_3)}}
    \\
    V_1 && \stackrel{U(t_1,t_3)}{\longrightarrow} && V_2
  }
$$

If this looks like a trivial reformulation of textbook material, then because it is a trivial reformulation of textbook material. But introducing such category-theoretic language for making the locality principle in quantum mechanics fully manifest turns out to be rather useful for capturing the full locality of [[local quantum field theory]], which is not in the traditional textbooks. This we come to below.

| [[physics]] |  [[category theory]] |
|-------------|----------------------|
| [[local quantum field theory|locality]] of time evolution | [[functor]] |


#### Entanglement and Monoidal structure

Besides the time evolution, there is the theory of [[composite systems]].

Given two [[quantum mechanical systems]] (e.g. of two electrons orbiting the same atomic nucleaus), with [[spaces of quantum states]] ([[pure states]]) $V$ and $\tilde V$, respectively, then the space of quantum states of the compound system is given by the [[tensor product of modules|tensor product of vector spaces]] (of [[Hilbert spaces]])

$$
  V \otimes \tilde V \in Vect
  \,.
$$

This should be compared with the way compound systems are formed in [[classical mechanics]]: for $X_1$ and $X_2$ the [[configuration spaces]]/[[phase spaces]] of two classical [[mechanical systems]], then the configuration space/phase space of their compound is the [[Cartesian product]] $X_1 \times X_2$. 

These Cartesian products and tensor products extend to [[morphisms]]. If $f\colon V \to V$ is a linear operator acting on the first system and $\tilde f \colon \tilde V\to \tilde V$ is one acting on the second system, then there is a tensor product morphism

$$
  (f_1\otimes f_2) 
  \;\colon\;
  V \otimes \tilde V
  \longrightarrow
  V \otimes \tilde V
  \,.
$$

Hence (Cartesian or non-cartesian) [[tensor products]] are something like product operations on sets, but on whole [[categories]]. Since binary associative product operations on sets are sometimes called _[[monoids]]_, one says that the category [[Vect]] of vector spaces when equipped with the tensor product of vector spaces is a _[[monoidal category]]_.

Similarly, the categories [[Diff]] or [[Set]] [[smooth manifolds]] or just bare [[sets]] carries a monoidal structure given simply by the [[Cartesian product]] of sets. This is called a [[cartesian monoidal category|cartesian monoidal structure]].

The characteristic property of Cartesian products $X_1 \times X_2$ is that elements of these are equivalently pairs of elements in $X_1$ and $X_2$, respectively. This reflects in turn the characteristic property of compound classical mechanical systems: a state of these is symply a pair of states of the two subsystems.

The tensor product on [[Vect]] however is not Cartesian: an element  in $\Psi \in V_1 \otimes V_2$ need not be of the form $\psi_1\otimes \psi_2$, for $\psi_i \in V_i$. Instead, in general it is a [[sum]] of such elements

$$
  \Psi = \underset{j}{\sum}  (\Psi_1)_j \otimes (\Psi_2)_j
  \,.
$$

In terms of [[physics]] such non-cartesian vectors are [[quantum states]] that exhibit [[entanglement]]. This hallmark property of quantum mechanics is hence accurately reflected by the abstract property of $(Vect,\otimes)$ being a non-cartesian [[monoidal category]].


| [[physics]] |  [[category theory]] |
|-------------|----------------------|
| [[entanglement]]  |  [[cartesian monoidal category|non-cartesin]] [[monoidal category]] of [[spaces of states]] |

For more exposition of this point see ([Baez 04](#Baez04)).

#### Bra-Kets and Dual objects

Consider now for simplicity of notation an application in [[quantum computing]]/[[quantum information theory]], where the [[spaces of states]] $V$ involved are [[finite dimensional vector spaces]] (spaces of [[qubits]]), such as for instance in the topological sector of the [[quantum Hall effect|quantum Hall system]].

Then for every space of states $V$ there is the [[dual vector space]]  $V^\ast$. In [[physics]] notation the states in $V$ are the [[kets]] $\vert \Psi \rangle$, while those of $V^\ast$ are the "bra-s" $\langle \Psi \vert$.


| [[physics]] |  [[category theory]] |
|-------------|----------------------|
| [[bra]]/[[ket]]  |  [[dual objects]] |


Essentially all of [[quantum information theory]] has a slick reformulation in terms of [[category theory]] for [[symmetric monoidal category]] [[rigid monoidal category|with dual objects]]. More on this is at _[[finite quantum mechanics in terms of dagger-compact categories]]_.


While the introduction of bra-ket notation by [[Paul Dirac]] was (while just notation) already quite useful for thinking about the subject, the language of monoidal category in fact reflects the actual physical processes involved even better.

For instance, in quantum mechanics textbooks one often sees the following manipulation of symbols for expressing a [[trace]] in terms of a sum over [[basis of a vector space|basis]] elements

$$
  \begin{aligned}
    \langle \Psi \vert \exp(\tfrac{i}{\hbar} H t ) \vert \Psi \rangle
    & =
    \langle \Psi \vert \exp(\tfrac{i}{\hbar} H t )  
    \left( \sum_j \vert \Psi_j \rangle \langle \Psi_j \vert \right)
    \vert \Psi \rangle
    \\
    & = 
    \sum_j
     \langle \Psi \vert \exp(\tfrac{i}{\hbar} H t ) \vert \Psi_j \rangle
     \langle \Psi_j \vert \Psi \rangle
    \\
    & = \sum_j
    \langle \Psi_j \vert 
    \left(
    \vert \Psi \rangle
    \langle \Psi \vert \exp(\tfrac{i}{\hbar} H t ) 
    \right)
    \vert \Psi_j \rangle
  \end{aligned}
  \,.
$$

This "rotation" operation where symbols are cyclically permuted reflects the fact that indeed traces as in [[partition functions]] reflect actual physical circular processes.

In "[[string diagram]]"-notation of [[monoidal category]]-theory this is reflected as follows. The unit map

$$
  1 \mapsto \underset{j}{\sum}  \vert \Psi_j \rangle \langle \Psi_j \vert
$$

is depicted as

$$
  \array{
    && \longleftarrow
    \\
    & \swarrow && \nwarrow
    \\
    V && && V^\ast
  }
$$

and the counit map

$$
  \vert \Psi_j \rangle \langle \Psi_k \vert
  \mapsto 
  \langle \Psi_k \vert \Psi_j \rangle
$$

as

$$
  \array{
    V && && V^\ast
    \\
    & \searrow && \nearrow
    \\
    && \longrightarrow
  }
  \,.
$$

#### Partition functions and Monoidal string diagrams


Given a [[Hamiltonian]] $H$, the [[partition function]] of the [[quantum mechanical system]] is the [[trace]]

$$
  Z_t \coloneqq Tr\left(  \exp\left(\tfrac{i}{\hbar} H t \right)  \right)
  \,.
$$

In bra-ket notation this is

$$
  Z_t = \underset{j}{\sum}  
   \left\langle \Psi_j \right\vert
   \exp\left(\tfrac{i}{\hbar} H t \right)  \left| \Psi_j \right\rangle 
$$

In terms of monoidal category-theoretic notation ([[string diagrams]]) this same expression reads as follows

$$
  \array{
     && \longleftarrow
     \\
     & \swarrow && \nwarrow
     \\
     V  && && V^\ast
     \\
     {}^{\mathllap{\exp(\tfrac{i}{\hbar} H t)}}\downarrow && && \uparrow^{\mathrlap{id}}
     \\
     V && && V^\ast
     \\
     & \searrow && \nearrow
     \\
     && \longrightarrow
  }
$$

This is striking, because this _picture_ is an accurate reflection of the physical process that the [[partition function]] describes, for the partition function is the [[correlator]] of a particle with a closed circular [[worldline]].

In fact, the monoidal category theoretic [[string diagram]]-notation is essentially the [[Feynman diagram]]-notation. This we turn to [below](#QMWithInteractionAndFeynmanDiagrams).


For a 1-dimensional [[TQFT]] the Hamiltonian above vanishes. (Or maybe more interestingly: for [[supersymmetric quantum mechanics]] the Hamiltonian may not vanish, but in the [[super trace]] in the [[partition function]] all non-zero energy eigenmodes cancel out by supersymmetry, and only the topological part is left after all).

In this case the partition function reduces to

$$
  \array{
     && \longleftarrow
     \\
     & \swarrow && \nwarrow
     \\
     V && && V^\ast
     \\
     & \searrow && \nearrow
     \\
     && \longrightarrow
  }
$$

which is just the trace on $V$. 

To reflect this in the functorial notation from [above](#TimeEvolutionAndFunctors), notice that also the catefogory $Bord_{1}^{Riem}$ from above is naturally a [[monoidal category]] if we take its objects to consist not just of single point, but of arbitrary collections of points, and to have its morphisms consist of all 1-dimensional [[cobordisms]]. Then a monoidal structure $(Bord_1^{Riem})^\coprod$ is given by [[disjoint union]].

A 1d TQFT with values in vector spaces is then a [[strong monoidal functor]]

$$
  (Bord_1^{Riem})^\corpod \longrightarrow Vect^{\otimes}
  \,.
$$

Other processes that sucj a 1d 1TQFT encodes include

$$
  \array{
    V && && V^\ast
    \\
    & \searrow && \nearrow
    \\
    && \longrightarrow
    \\
     && \longleftarrow
     \\
     & \swarrow && \nwarrow
     \\
     V && && V^\ast
  }
$$

In this way a 1d TQFT is entirely encoded in the operation that exhibit a [[finite dimensional vector space]] $V$ as a [[dualizable object]].

$\{$
  1d TQFT with coefficients in [[Vect]]
$\}$  

$\simeq$ 

$\{$
[[dualizable objects]] in $Vect$
$\}$ 

$\simeq$ 

$\{$
 [[finite dimensional vector spaces]]
$\}$

This is the simplest incarnation of the statement that for higher dimensional [[extended TQFT]] becomes the [[cobordism hypothesis]]. We come to this [below](#IntroductionGeneralFormulation).


### Path integral quantization of 1d Gauge theory
 {#PathIntegralQuantizationof1dGaugeTheory}

The [[path integral]] tends to be as suggestive in [[quantum field theory]] as it is invoked ubiquituously, and FQFT may be understood as being precisely the axiomatics that a would-be path integral ought to satisfy, thereby decoupling its construction as a suitably regularized integral from its operational definition as yielding a consistent [[S-matrix]] for the QFT.

We discuss now the simplest non-trivial example of a [[path integral quantization]], namely for 1-dimensional finite [[gauge theory]], the 1-dimensional [[Dijkgraaf-Witten model]]. This has the two-fold purpose of 

1. indicating how not just the final quantum theory but also its [[prequantum field theory|prequantum data]] is naturally ordganized by monoidal category theory;

1. motivating and introducing elements of [[homotopy theory]] which become crucial for the understanding of FQFT as one moves up in dimension.

A more detailed version of this section is at _[Local prequantum field theory -- id Dijkgraaf-Witten theory](prequantum+field+theory#1dDWTheory)_.

#### Gauge transformation and Groupoids
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
      &\stackrel{\circ}{\longrightarrow}&
      \mathcal{G}_1
      & \stackrel{\overset{t}{\longrightarrow}}{\stackrel{\overset{i}{\leftarrow}}{\underset{s}{\longrightarrow}}}&
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
    {\overset{id}{\longrightarrow}}
    {
      \stackrel{\overset{id}{\longleftarrow}}{\underset{id}{\longrightarrow}}
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
    \stackrel{\overset{\rho}{\longrightarrow}}{\underset{p_1}{\longrightarrow}}
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
     \stackrel{\overset{ev_1}{\longrightarrow}}{\underset{ev_0}{\longrightarrow}}
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


#### Trajectories of fields and Correspondences of groupoids 
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

#### Action functionals and Slice groupoids
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

where the function corresponding to this homotopy is that given by the unique factorization through the [[homotopy fiber product]] $\flat U(1) \simeq \ast \underset{\mathbf{B}\flat U(1)}{\times} \ast$ (example \ref{LoopSpaceGroupoid}) as shown on the right of 

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

In conclusion we may now compute what the 1-dimensional prequantum field theory defined by a group character $c \colon G \to U(1)$ regarded as a local action functional assigns to the [[circle]].

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

+-- {: .num_remark}
###### Remark

It follows that in a discussion of [[quantization]] the [[path integral]] for the [[partition function]] of 1d DW theory is given by the [[Schur inner product|Schur integral]] over the [[group character]] $c$. (...)

=--

In conclusion, [[1-dimensional Dijkgraaf-Witten theory]] as a prequantum field theory comes down to be essentially a geometric interpretation of what [[group characters]] are and do. One may regard this as a simple example of [[geometric representation theory]]. Simple as this example is, it contains in it the seeds of many of the interesting aspects of richer prequantum field theories. 



### Quantum mechanics with interactions and Feynman diagrams
 {#QMWithInteractionAndFeynmanDiagrams}

We saw above that [[symmetric monoidal category]] theory naturally captures all the key aspects of basic [[quantum mechanics]].

This becomes all the more pronounced when one considers quantum mechanics with interaction as in the [[worldline formalism]] and hence when one considers [[Feynman diagrams]] as diagrams of interactions of [[particles]].

#### Spectral triples and Graph representations

Let $R Cob_{1|1}^{Feyn}$ be the [[cobordism category]] of [[Feynman graphs]] for the [[superparticle]] with a single type of interaction along the lines of [[(1,1)-dimensional Euclidean field theories and K-theory]]. So its morphisms are generated from $(1|1)$-dimensional super-Riemannian manifolds (i.e. super-intervals) and from a single interaction vertex

$$
  \array{
    \bullet
    \\
    & \searrow
    \\
    && \bullet & \to
    \\
    & \nearrow
    \\
    \bullet
  }
$$

subject to the obvious associativity condition.

Then a [[spectral triple]] $(A,H,D)$ is the data encoding a sufficiently nice smooth [[functor]] 

$$
  Z_{(A,H,D)} : R Cob_{1|1}^{Feyn}  \to sVect
$$

to the [[category]] of [[super vector space]]s.

Here

* $A = Z_{(A,H,D)}(\bullet)_0$ is the even part of the [[super vector space]] assigned by the functor to the point, equipped with the structure of a [[algebra]] whose product is given by the image of the interaction vertex

  $$
    Z_{(A,H,D)}
    \left(
  \array{
    \bullet
    \\
    & \searrow
    \\
    && \bullet & \to
    \\
    & \nearrow
    \\
    \bullet
  }
    \right)
  $$

* $H$ is some completion of $Z_{(A,H,D)}(\bullet)$  to a [[super Hilbert space]]

* and $D \in End(H)$ is an odd self-adjoint operator on $H$, which gives the value of the functor on the super-interval $(t,\theta)$ by

  $$
    (t,\theta) \mapsto \exp( - t D^2 + \theta D )
    \,.
  $$ 

So this is the [[quantum mechanics]] of a [[superparticle]]. In the simplest case this comes from a spinor particle propagating on a [[spin structure]] [[Riemannian manifold]] $X$in which case

* $H = L^2(S)$ is the space of square integrable spinor sections;

* $D$ is the [[Dirac operator]]

* $A = C^\infty(X)$ is the space of smooth functions on $X$.

One point of a [[spectral triple]] is to take the view of world-line [[quantum mechanics]] as basic and _characterize_ the spin Riemannian geometry of $X$ entirely by this algebraic data. In particular the [[Riemannian metric]] on $X$ is encoded in the [[operator spectrum]] of $D$, which is where the notion "spectral triple" gets its name from.

Then with all the ordinary geoemtry re-encoded algebraically this way, in terms of the 1-dimensional [[quantum field theory]] that _probes_ this geometry, one can then use the same formulas to interpret spectral triple geometrically that do _not_ come from an ordinary geometry as in the above example.

#### Feynman diagram in worldline formalism and Monoidal string diagrams

...[[worldline formalism]]...

...[[Feynman diagram]]...

...[[string diagram]]...

### Quantum topological string
 {#QuantumTopologicalString}

#### Global 2d TQFT and Frobenius algebra
 {#Global2dTQFT}

In view of the above discussion of "topological quantum mechanics", i.e. of 1-dimensional [[TQFT]], it is immediate to pass to a higher dimensional field theory by using [[categories of cobordisms]] of higher dimension and consider [[strong monoidal functors]]

$$
  Z \;\colon\; Bord_n^\sqcup \longrightarrow Vect^\otimes
$$

([Atiyah 88](#Atiyah88), [Segal 04](#Segal04)).

for instance 1-dimensional cobordisms with boundary describe a kind [[2d TQFT]] with [[boundary field theory]].

[[frobenius_algebra.jpg:pic]]

As almost immediate from these picture, such 2d TQFTs are equivalent to [[Frobenius algebras]] $A$. 

In terms of physics: $A$ is the [[space of states]] of a topological [[open string]] and the algebra and coalgebra structure on it encodes its [[n-point function|3-point functions]].

More generally open and [[closed strings]]

[[monoid_laws.jpg:pic]]


Now $Z$ is equivalent to a pair consisting of a Frobenius algebra $A$ and a commutative Frobenius algebra $B$ and a [[homomorphism]] $B \to Z(A)$ to the [[center]] of $A$
 
$$
  Bord_2^{\sqcup} \longrightarrow Vect^\otimes
$$

([Moore-Segal](#MooreSegal06) [Lazaroiu 00](#Lazaroiu00), see also [Lauda-Pfeiffer 05](#LaudaPfeiffer05)).

In physics speak $B$ is the space of states for the topological _[[closed string]]_.

Or rather, it is _some_ topological string model, but not the one originally obtained by [[topological twist]] from the [[2d (2,0)-superconformal QFT]] which is commonly what is understood as the "[[topological string]]" in [[string theory]] ([[A-model]]/[[B-model]]).


#### Cohomological 2d TQFT and Calabi-Yau $A_\infty$-algebras
 {#Local2dTQFT}

Curiously, the above does _not_ capture the original motivating examples for [[2d TQFT]] that came from physics, namely it does not capture the "[[cohomological quantum field theory]]" due to [[Edward Witten]], such as the [[topological string]] in its incarnation as the [[A-model]] and [[B-model]] and the [[Landau-Ginzburg model]].


* Witten [[cohomological field theory]]: [[space of quantum states]] is [[chain complex]], physical quantum states are [[chain homology]]

* Kontsevich: [[homological mirror symmetry]] is equivalence of [[A-∞ categories]]

* Aspinwall, Douglas et al: the [[derived categories]] here are those of topological [[A-branes]] ([[A-branes]]/[[B-branes]])

Hence need to regard [[A-model]]/[[B-model]] open [[topological string]] as having a [[chain complex]] of [[vector spaces]]. Under string composition this yields not just an [[associative algebra]] with [[trace]] but an [[A-∞ algebra]] with suitable trace. 

Examples come from twisting the [[2d (2,0)-CFT]] induced from a [[Calabi-Yau manifold]], hence one speaks of "[[Calabi-Yau A-∞ algebra]]".


remember space of [[diffeomorphism]]

* Getzler, Segal: "[[TCFT]]"

classification by ([Costello 04](#Costello04)) sums it up:

[[Calabi-Yau A-∞ category]] is equivalent to non-compact open topological string with coefficients in $Ch(Vect)$. The [[objects]] of the category are the [[D-branes]], [[hom-spaces]] are the spaces of quantum states of open strings stretching between these. The closed string [[bulk field theory]] sector is given by forming [[Hochschild homology]]. Given a [[Calabi-Yau manifold]], then the [[A-∞ category]] refinement (see at _[[enhanced triangulated category]]_) of its [[derived category of coherent sheaves]] is an example. 


#### Local 2d TQFT and 2-Modules

Given an [[associative algebra]] $A$ then its [[category of modules]] $A Mod$
behaves much like a higher analog of a [[module]]/[[vector space]].

Given an $A$-$B$ [[bimodule]] $N$ then $(-)\otimes_A N \colon A Mod \to B Mod$ behaves like a higher dimensional [[linear operator]].

This is the [[Eilenberg-Watts theorem]].

Hence we speak of a [[2-module]].

Notice that every algebra $A$ is canonically an $A$-$A$-bimodule. This way we see that the above construction naturally localizes

|  | [[cohomological QFT]] | [[local QFT]] |
|--|-----------------------|---------------|
| [[open string]] $\mapsto$ | open string algebra $A$ | open string [[bimodule]] ${}_{A} A_{A}$ |
| point $\mapsto$ |   |  [[2-module]] $A Mod$ |

Hence we regard [[D-Brane]] states as quantum 2-states.

We motivate this further [below](#IntroductionGeneralFormulation). First to record the classification results:

[[!include 2d TQFT -- table]]

Here the trace operation in the CY conditions corresponds to the cobordism which is the "disappearance of a circle".

$$
  \array{
     && \longleftarrow
    \\
    & \swarrow && \nwarrow
    \\
    V && && V^\otimes
    \\
    & \searrow && \nearrow
    \\
    && \longrightarrow
  }
  \;\;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;\;
   \ast
$$

One may view this as exhibiting "higher order duality": where the semi-circles exhibits $V$ as a [[dual object]] to $V^\ast$, this disappearance of a circle exhibits the upper semi-circle as [[adjoint morphism|adjoint]] to the lower semicircle.

(...)


### General local TQFT
 {#IntroductionGeneralFormulation}

#### Covariant quantization and Directed homotopy types

One way to understand from the point of view of [[physics]] why the 1-functorial description of [[2d CFT]] and [[2d TQFT]] [above](#Global2dTQFT) is unsatisfactory is that it breaks what is known as "covariance" in physics, in the sense of "[[general covariance]]" (reflected also in the term "[[covariant phase space]]"): implicit in the concept of a [[category of cobordisms]] is a splitting of a [[spacetimes]]/[[worldvolumes]] into spatial slices (the [[objects]]) of the category and [[trajectories]] between these. 

The standard [[Lagrangian]]-data ("[[prequantum field theory]]") from which [[topological quantum field theories]] are supposed to arise under [[quantization]] do not enforce such a splitting as indeed they are [[general covariance|generally covariant]]. Accordingly, a [[local Lagrangian]] should, after [[quantization]], give rise to a [[local quantum field theory]] that is still "generally covariant" in that it does not require or depend on such a splitting. In physics this plays a crucial role for instance in considerations related to [[quantum gravity]].

We saw [above](#CorrespondencesOfGroupoids) how 1-dimensional ([[prequantum field theory|prequantum]]) field theory is encoded by [[correspondences]] of [[groupoids]].  For instance the process of a particle and its antiparticle appearing out of the vacuum is given by

$$
  \array{
    && \mathbf{Fields}
    \\
    & \swarrow && \searrow^{\mathrlap{\Delta}}
    \\
    \ast && && \mathbf{Fields} \times \mathbf{Fields}
  }
$$

and the reverse process of them disappearing is given by

$$
  \array{
    && \mathbf{Fields}
    \\
    & {}^{\mathllap{\Delta}}\swarrow && \searrow
    \\
    \mathbf{Fields} \times \mathbf{Fields}  && &&  \ast
  }
$$

A particle tracing out a circle is equivalently the composition (via [[homotopy fiber product]]) of these two process.

$$
  \array{
     && && [\Pi(S^1), \mathbf{Fields}]
     \\
     && & \swarrow && \searrow
     \\
     && \mathbf{Fields} && && \mathbf{Fields} 
     \\
     & \swarrow && \searrow && \swarrow && \searrow
     \\
     \ast && && \mathbf{Fields}\times \mathbf{Fields} && && \ast
  }
$$

Then we saw [above](#Local2dTQFT) for [[2d TQFT]] that in higher dimensional general such a circle in turn may appear

$$
  \array{
     && [\Pi(S^1), \mathbf{Fields}]
     \\
     & \swarrow & \uparrow & \searrow
     \\
     \ast && \mathbf{Fields} && \ast
     \\
     & \nwarrow &\downarrow& \nearrow
     \\
     && \ast
  }
$$

and disappear

$$
  \array{
     && \ast
     \\
     & \swarrow & \uparrow & \searrow
     \\
     \ast && \mathbf{Fields} && \ast
     \\
     & \nwarrow &\downarrow& \nearrow
     \\
     && [\Pi(S^1), \mathbf{Fields}]
  }
$$

The 2-dimensional composition of such processes, again by [[homotopy fiber product]] yields values on all higher spheres

$$
  \mathbf{Fields} \underset{[\Pi(S^n)]}{\times} \mathbf{Fields}
  \simeq
  [\Pi(S^{n+1}), \mathbf{Fields}]
$$

and in fact all [[homotopy types]] of [[smooth manifolds]]. For instance the  [[trinion]] process is represented by this correspondence-of-correspondences:

$$
  \array{
      \ast &\longleftarrow& [\Pi(S^1 \coprod S^1), \mathbf{Fields}] &\longrightarrow& \ast
     \\
     \uparrow && \uparrow && \uparrow
     \\
     \ast &\longleftarrow& [\Pi(Fig8), \mathbf{Fields}] &\longrightarrow& \ast
     \\
     \downarrow && \downarrow && \downarrow
     \\
      \ast &\longleftarrow& [\Pi(S^1), \mathbf{Fields}] &\longrightarrow& \ast     
  }
$$

To describe local propagation in higher dimensional field theory this way, evidently we need a higher dimensional calculus that deals both with the [[homotopy theory]] ([[gauge theory]]) involves as well as with the directionality of these processes.

We already saw the first hint of how this works: [[groupoids]] above appeared in two different guises, on the one hand as [[homotopy 1-types]], on the other as special kinds of [[categories]] with directed morphisms.

Now [[homotopy 1-types]] have a classical generalization to general [[homotopy types]], traditionally taken to be represented by [[topological spaces]] regarded up to [[weak homotopy equivalence]]. 

A crucial fact is that one may pair this full homotopy-theoretic aspect with the category-theoretic aspect to get [[(∞,1)-categories|∞-categories]]

$$
  \array{
    && groupoids
    \\
    & \swarrow && \searrow
    \\
    categories && && \infty\text{-}groupoids
    \\
    & \searrow && \swarrow
    \\
    && \infty\text{-}categories
  }
$$

$n$-fold $\infty$-categories $\longrightarrow$ [[(∞,n)-categories]]

[[k-morphisms]] for all $k$, such that for $k \gt n$ they are invertible

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

in particular

* [[(∞,n)-category of cobordisms]] $Bord_n$

* [[(∞,n)-category of correspondences]] $Corr_n$

* [[(∞,n)-category of (∞,n)-modules]] $Mod_n$



#### $n$-Spaces of states and the Cobordism hypothesis

These [[(∞,n)-categories]] are [[symmetric monoidal (∞,n)-categories]] in the same way that their 1-categorical shadows are, only that everything is lifted up to homotopy.

hence one may consider

 [[monoidal (∞,n)-functors]]

[[schreiber:Local prequantum field theory]]

$$
  Bord_n^\sqcup
  \longrightarrow
  Corr_n(\mathbf{H}_{/Phases})^{\otimes_{phased}}
$$

[[local quantum field theory]]

$$
  Bord_n^\sqcup \longrightarrow Mod_n^\otimes
$$

The classification theory of these, the _[[cobordism theorem]]_ says roughly that such local topological field theories assign [[fully dualizable objects]] $V$ to the point and are entirely determined by this assignment in that every higher dimensional manifold is sent to the [[higher dimensional trace]] on the identity on that object, i.e. the higher codimension analogs of the [[partition function]].

$$
  \Sigma \mapsto tr_\Sigma(id_V)
  \,.
$$


(...)

### 3d TQFT
 {#Global3dTQFT}


#### Chern-Simons theory

...[[fusion category]]...


...[[Turaev-Viro construction]]...

...[[modular tensor category]]...

...[[Reshetikhin-Turaev construction]]...



...[[quantization of 3d Chern-Simons theory]]...


#### Modular functor
 {#Local3dTQFT}

... [[modular functor]] ...





## Related concepts

* [[quantum field theory]]

  * **FQFT**

    * [[TQFT]], 
 
      * [[extended topological quantum field theory]], 

      * [[0-dimensional TQFT]], 

      * [[2d TQFT]], [[3d TQFT]] [[4d TQFT]], 

      *  [[HQFT]]

  * [[AQFT]]

    * [[Haag-Kastler axioms]]

    * [[local net of observables]]


## References

### Formalization of sewing and locality in terms of functoriality

It was in

* {#Atiyah88} [[Michael Atiyah]], _Topological quantum field theory_, Publications Math&#233;matiques de l'IH&#201;S, 68  (1988), p. 175-186

that it was realized that 

* this means that this property can be taken as the <em>defining</em> property of the path integral, thereby circumventing the problem of constructing it as an actual integral;

* this property can be conveniently axiomatized by saying that the path integral is a [[functor]] from a suitable category whose morphisms are [[cobordism]]s to a category of vector spaces.

(Strictly speaking, Atiyah's original article mentions this functor slightly indirectly only.)

All this was originally formalized in the context of [[TQFT|topological quantum field theory]] only. This is the easiest case that already exhibits all the functoriality that is implied by "FQFT" but by far not the only case (see below).

A pedagogical exposition of how the physicist's way of thinking about the path integral leads to its definition as a functor is given in

* [[Kevin Walker]], _TQFTs_ ([pdf](http://canyon23.net/math/tc.pdf))

A pedagogical exposition of the notion of quantum field theory as a functor on [[cobordism]]s is in 

* {#Baez04} [[John Baez]], _Quantum quandaries: a Category-Theoretic perspective_ ([arXiv](http://arxiv.org/abs/quant-ph/0404040))

and a review of much of the existing material in the literature is in 

* [[Bruce Bartlett]], _Categorical Aspects of Topological Quantum Field Theories_ ([arXiv](http://arxiv.org/abs/math/0512103)).

The discussion of the open-closed case of 2d TQFT goes back to

* {#MooreSegal06} [[Greg Moore]], [[Graeme Segal]], _D-branes and K-theory in 2D topological field theory_ ([arXiv](http://arxiv.org/abs/hep-th/0609042))

* {#Lazaroiu00} [[Calin Lazaroiu]], _On the structure of open-closed topological field theory in two dimensions_, Nuclear Phys. B 603(3), 497&#8211;530 (2001), ([arXiv:hep-th/0010269](http://arxiv.org/abs/hep-th/0010269))

A picture-rich discussion is in 

* {#LaudaPfeiffer05} [[Aaron Lauda]], [[Hendryk Pfeiffer]], _Open-closed strings: two-dimensional extended TQFTs and Frobenius algebras_ , Topology Appl. 155 (2008) 623-666. ([arXiv:math.AT/0510664](http://arxiv.org/abs/math.AT/0510664))


### Non-topological FQFTs (especially conformal)## 

This mostly concentrates on [[TQFT|topological quantum field theories]], those where the path integral depends only on the diffeomorphism class of the domain it is evaluated on. This is the simplest and by far best understood case. But the idea of functorial FQFT is not restricted to this case.

This was realized in

* {#Segal04} [[Graeme Segal]], _The definition of conformal field theory_, in: _Topology, Geometry and quantum field theory_, London. Math. Soc. LNS 308, edited by [[Ulrike Tillmann]], Cambridge Univ. Press 2004, 247-343

There the notion of 2-dimensional [[conformal field theory]] is axiomatized as a functor on a category of 2-dimensional cobordisms with conformal structure.

(Apparently a similar definition has been given by Kontsevich, but never published.) The details of the category of conformal cobordisms can get a bit technical and slight variations of Segal's original definition may be necessary. The work by Huang and Kong can be regarded as a further refinement and maybe completion of Segal's program

* Yi-Zhi Huang, _Geometric interpretation of vertex operator algebras_, Proc. Natl. Acad. Sci. USA, Vol 88. (1991) pp. 9964-9968

* Liang Kong, _Open-closed field algebras_ Commun. Math. Physics. 280, 207-261 (2008) ([arXiv](http://arxiv.org/abs/math/0610293)).

A very concrete construction of functorial CFTs (for the special case of _rational_ CFTs) is provided by the 
[[FFRS-formalism]].

### Extended (multi-tiered) FQFT {#Extended}

But one notices that the formalization of quantum field theory as a [[functor]] on [[cobordism]]s encodes only a small aspect of the full sewing law imagined to be satisfied by the path integral: In a 1-[[category]] of $n$-dimensional [[cobordism]]s these are glued along $(n-1)$-dimensional boundaries. One could imagine more generally a formalization where a given [[cobordism]] is allowed to be chopped into arbitrary parts of arbitrary co-dimension such that the path integral can still consistently be evaluated on each of these parts.

This leads to the notion of _extended quantum field theory_, which is taken to be an $\infty$-functor on an [[higher category theory|infinity category]] of [[extended cobordism]]s. Early ideas about a formalization of this approach were given in

* {#BaezDolan95} [[John Baez]], [[James Dolan]], _Higher-dimensional algebra and Topological Quantum Field Theory_  ([arXiv](http://arxiv.org/abs/q-alg/9503002)) .

Making this precise involves giving a precise definition of an $\infty$-category of cobordisms. Several approaches exist, such as

* Eugenia Cheng and Nick Gurski, _Towards an $n$-category of cobordisms_,
Theory and Applications of Categories,  Vol. 18, 2007, No. 10, pp 274-302.  ([tac](http://www.tac.mta.ca/tac/volumes/18/10/18-10abs.html))

or

* Marco Grandis, _Collared cospans, cohomotopy and TQFT (Cospans in Algebraic Topology, II)_, Dip. Mat. Univ. Genova, Preprint 555 (2007). ([pdf](http://www.dima.unige.it/~grandis/wCub2.pdf))

There is a long-term project by Stephan Stolz and Peter Teichner which originally tried to refine Segal's 1-functorial formulation of conformal field theory to a 2-functorial extended FQFT, as indicated in

* Stephan Stolz and Peter Teichner, _What is an elliptic object?_ ([pdf](http://math.berkeley.edu/~teichner/Papers/Oxford.pdf)).


More recently, Mike Hopkins and Jacob Lurie claimed 
([Hopkins-Lurie on Baez-Dolan](http://golem.ph.utexas.edu/category/2008/05/hopkinslurie_on_baezdolan.html))
to have found a complete coherent formalization of topological extended FQFT in the context of [[(infinity,1)-category|(infinity,n)-categories]] using an [[(infinity,n)-category of cobordisms]]. This is described in 

* {#Luire09} [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_ ([arXiv:0905.0465](http://arxiv.org/abs/0905.0465))

An explicit account of this for the 2-dimensional case is presented in

* [[Chris Schommer-Pries]], _The Classification of Two-Dimensional Extended Topological Field Theories_, PhD thesis, Berkeley, 2009 ([pdf](http://sites.google.com/site/chrisschommerpriesmath/Home/my-web-documents/Schommer-Pries-Thesis-5-12-09.pdf?attredirects=0))

see also 

* [[extended topological quantum field theory]]


### (extended) FQFT from background fields: $\sigma$-models## 


In this context Dan Freed is picking up again his old work on higher algebraic structures in quantum field theory, as described in

* [[Dan Freed]], _Quantum Groups from Path Integrals_ ([arXiv](http://xxx.lanl.gov/abs/q-alg/9501025))

* [[Dan Freed]], _Higher Algebraic Structures and Quantization_ ([arXiv](http://arxiv.org/abs/hep-th/9212115))

where he argued that and how the path integral should assign $n$-categorical objects to domains of codimension $n$, and is re-expressing this in the $\infty$-functorial context.  (Freed speaks of _multi-tiered_ QFT instead of extended QFT.) 

* [[Dan Freed]], _Remarks on Chern-Simons Theory_ ([arXiv](http://arxiv.org/abs/0808.2507)).

Freed's ideas on how an extended or multi-tiered QFT arises from a path integral coming from a given background field were further formalized in the context of "finite" QFTs in

* Simon Willerton, _The twisted Drinfeld double of a finite group via gerbes and finite groupoids_ ([arXiv](http://arxiv.org/abs/math.QA/0503266))

* Bruce Bartlett, _On unitary 2-representations of finite groups and topological quantum field theory_, PhD thesis, Sheffield (2008) ([arXiv] (http://arxiv.org/abs/0901.3975))

There are indications that a complete picture of this involves [[groupoidification]] 

* Jeffrey Morton, _Extended TQFTs and Quantum Gravity_ ([arXiv](http://arxiv.org/abs/0710.0032))

and, more generally [[geometric function theory]]:

a big advancement in the understanding of extended $\sigma$-model QFTs is the discussion in

* David Ben-Zvi, John Francis, David Nadler,
_Integral Transforms and Drinfeld Centers in Derived Geometry_ ([arXiv](http://arxiv.org/abs/0805.0157))

which realizes $\sigma$-models by homming [[cobordism]] [[cospan]]s into the total spaces (realized as [[infinity-stack homotopically|infinity-stack]]) of background fields and regarding the resulting [[span]]s as pull-push operators on suitable [[geometric function theory|geometric functions]].  

A similar approach to bring the old work by Dan Freed mentioned above in contact with the picture of extended functorial QFT and the Baez-Dolan-Lurie structure theorem is

* [[Dan Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], _[[Topological Quantum Field Theories from Compact Lie Groups]]_ 


### Super QFT

See 

* [[(1,1)-dimensional Euclidean field theories and K-theory]]

* [[(2,1)-dimensional Euclidean field theories and tmf]]

### homological 2d FQFT (and TCFT) ##

As usual, the problem of constructing FQFT becomes much more tractable when linear approximations are applied. In homological FQFT and in [[TCFT]] the Hom-spaces of the cobordism category (the moduli spaces of cobordisms with given punctures/boundaries) are approximated by complexes  of chains on them. This leads to formalization of $\infty$-functorial QFT in the context of [[dg-algebra]]

The concept is essentially a formalization of what used to be called [[cohomological field theory]] in

* {#Witten91} [[Edward Witten]], _Introduction to cohomological field theory_, InternationalJournal of Modern Physics A, Vol. 6,No 6 (1991) 2775-2792 ([[WittenCQFT.pdf:file]])


The definition of [[TCFT]] was given independently by 

* {#Getzler92} [[Ezra Getzler]], _Batalin-Vilkovisky algebras and two-dimensional topological field theories_ , Comm. Math. Phys. 159(2), 265&#8211;285 (1994) ([arXiv:hep-th/9212043](http://arxiv.org/abs/hep-th/9212043))

and 

* [[Graeme Segal]], _Topological field theory_ , (1999), Notes of lectures at Stanford university. ([web](http://www.cgtp.duke.edu/ITP99/segal/)). See in particular [lecture 5](http://www.cgtp.duke.edu/ITP99/segal/stanford/lect5.pdf) ("topological field theory with cochain values").
 
The classification of [[TCFT]]s by [[Calabi-Yau A-∞ categories]] was discussed in

* {#Costello04} [[Kevin Costello]], _Topological conformal field theories and Calabi-Yau categories_ Advances in Mathematics, Volume 210, Issue 1, (2007), ([arXiv:math/0412149](http://arxiv.org/abs/math/0412149))

* [[Kevin Costello]], _The Gromov-Witten potential associated to a TCFT_ ([arXiv:math/0509264](http://arxiv.org/abs/math/0509264))

following conjectures by [[Maxim Kontsevich]], e.g.

* [[Maxim Kontsevich]], _Homological algebra of mirror symmetry_ , in Proceedings of the International Congress of Mathematicians, Vol. 1, 2 (Z&uuml;rich, 1994), pages 120&#8211;139, Basel, 1995, Birkh&#228;user.








[[!redirects FQFTs]]
[[!redirects Functorial quantum field theory]]
[[!redirects Functorial quantum field theories]]
[[!redirects functorial quantum field theory]]
[[!redirects functorial quantum field theories]]