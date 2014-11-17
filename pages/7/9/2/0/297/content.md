
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

A local ("[[extended TQFT|extended]]", "multi-tiered") refinement of this is naturally given by passing from 1-functors to [[(∞,n)-functors]] on [[(∞,n)-categories of cobordisms]]. This formulation was vaguely suggested in ([Baez-Dolan 95](#BaezDolan95)) ("[[cobordism hypothesis]]") and formalized in ([Luire 09](#Luire09)). It captures what in physics jargon would be called "covariant" quantum field theory, in that the "localization down to the point" means that the formalism knows how to glue/propagate in spatial directions just as in time directions, in fact that no such distinction is retained.



## Exposition and Introduction
 {#Introduction}

> under construction

We give here motivation for, introduction to and an exposition of the ideas of [[local quantum field theory|local]] ([[extended TQFT|extended]]) functorial field theory. 

We start in 

* _[Quantum mechanics in Schr&#246;dinger picture](#QuantumMechanicsInSchroedingerPicture)_

by showing how all the basic category-theoretic ideas are already right beneath the surface of the traditional textbook discussion of quantum mechanics. Then in

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
| [[local quantum field theory|local]] [[dynamics|time evolution]] | [[functor]] |
| [[compound system]] [[entanglement]] | [[cartesian monoidal category|non-cartesian]] [[monoidal category]] |
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
     \int_{t_1}^{t_2} \tfrac{i}{\hbar} H_t \, d t
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
  \Psi = \underset{j}{\sum}  (\psi_1)_j \otimes (\Psi_2)_j
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
  Z_t \coloneq Tr\left(  \exp\left(\tfrac{i}{\hbar} H t \right)  \right)
  \,.
$$

In bra-ket notation this is

$$
  Z_t = \underset{\Psi}{\sum}  
   \left\langle \Psi \right\vert
   \exp\left(\tfrac{i}{\hbar} H t \right)  \left| \Psi\right\rangle 
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

* (1d TQFT with coefficients in [[Vect]]) $\leftrightarrow$ ([[dualizable objects]] in $Vect$) $\leftrightarrow$ ([[finite dimensional vector spaces]])

This is the simplest incarnation of the statement that for higher dimensional [[extended TQFT]] becomes the [[cobordism hypothesis]]. We come to this [below](#IntroductionGeneralFormulation).


### Quantum mechanics with interactions and Feynman diagram
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

#### Naive generalization: Global 2d TQFT 
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


#### Local 2d TQFT -- The A/B-model topological String  
 {#Local2dTQFT}

Curiously, the above does _not_ capture the original motivating examples for [[2d TQFT]] that came from physics, namely it does not capture the "[[cohomological quantum field theory]]" due to [[Edward Witten]], such as the [[topological string]] in its incarnation as the [[A-model]] and [[B-model]] and the [[Landau-Ginzburg model]].


* Witten [[cohomological field theory]]: [[space of quantum states]] is [[chain complex]], physical quantum states are [[chain homology]]

* Kontsevich: [[homological mirror symmetry]] is equivalence of [[A-∞ categories]]

* Aspinwall, Douglas et al: the [[derived categories]] here are those of topological [[A-branes]] ([[A-branes]]/[[B-branes]])

Hence need to regard [[A-model]]/[[B-model]] open [[topological string]] as having a [[chain complex]] of [[vector spaces]]. Under string composition this yields not just an [[associative algebra]] with [[trace]] but an [[A-∞ algebra]] with suitable trace. 

Examples come from twisting the [[2d (2,0)-CFT]] induced from a [[Calabi-Yau manifold]], hence one speaks of "[[Calabi-Yau A-∞ algebra]]".


remember space of [[diffeomorphism]]

* Getzler, Segal: [[TCFT]]

classification by ([Costello 04](#Costello04)) sums it up:

[[Calabi-Yau A-∞ category]] is equivalent to non-compact open topological string with coefficients in $Ch(Vect)$. The [[objects]] of the category are the [[D-branes]], [[hom-spaces]] are the spaces of quantum states of open strings stretching between these. The close string [[bulk field theory]] sector is given by forming [[Hochschild homology]]. Given a [[Calabi-Yau manifold]], then the [[A-∞ category]] refinement (see at _[[enhanced triangulated category]]_) of its [[derived category of coherent sheaves]] is an example. (...)



[[!include 2d TQFT -- table]]


(...)


### General local TQFT
 {#IntroductionGeneralFormulation}

#### "Covariance" in physics

One way to understand from the point of view of [[physics]] why the 1-functorial description of [[2d CFT]] and [[2d TQFT]] [above](#Global2dTQFT) is unsatisfactory is that it breaks what is known as "covariance" in physics, in the sense of "[[general covariance]]" (reflected also in the term "[[covariant phase space]]"): implicit in the concept of a [[category of cobordisms]] is a splitting of a [[spacetimes]]/[[worldvolumes]] into spatial slices (the [[objects]]) of the category and [[trajectories]] between these. 

The standard [[Lagrangian]]-data ("[[prequantum field theory]]") from which [[topological quantum field theories]] are supposed to arise under [[quantization]] do not enforce such a splitting as indeed they are [[general covariance|generally covariant]]. Accordingly, a [[local Lagrangian]] should, after [[quantization]], give rise to a [[local quantum field theory]] that is still "generally covariant" in that it does not require or depend on such a splitting. In physics this plays a crucial role for instance in considerations related to [[quantum gravity]].





#### Formalization in higher monoidal category theory

... [[(infinity,n)-category of cobordisms]]...

... [[symmetric monoidal (infinity,n)-category]]...

... [[fully dualizable object]]...

... [[cobordism hypothesis]]...


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

### Formalization of sewing and locality in terms of functoriality##

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