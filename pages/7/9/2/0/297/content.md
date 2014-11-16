
{:bluebox: .un_remark style="border:solid #000000;background: #E6DF13;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Functorial quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


Functorial quantum field theory_, one of the two approaches of axiomatizing [[quantum field theory]]. The other is [[AQFT]]. FQFT formalizes the _[[Schrödinger picture]]_ of quantum mechanics, while [[AQFT]] formalizes the _[[Heisenberg picture]]_.

### General idea
 {#GeneralIdea}

Much work in quantum field theory is based on arguments using the [[path integral]]. While in the physics literature this is usually not a well defined object, it is generally assumed to satisfy a handful of properties, notably the _sewing laws_. These say, roughly, that the path integral over a domain $\Sigma$ which decomposes into subdomains $\Sigma_1$ and $\Sigma_2$ is the same as the path integral over $\Sigma_1$ composed with that over $\Sigma_2$.

Accordingly it is the _[[S-matrix]]_ that is manifestly incarnated in the Atiyah-Segal picture of functorial QFT:

Here a [[quantum field theory]] is given by a [[functor]] 

$$
 Z \colon Bord_d^S \longrightarrow Vect
$$

from a suitable [[category of cobordisms]] to a suitable [[category]] of [[vector spaces]].

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

Segal's axioms for [[FQFT]] ([[CFT]] in his case) were originally explicitly about the propagators/S-matrices, while Atiyah formulated it in terms of the correlators this way. Both perspectives go over into each other under duality as above.

Notice that this kind of discussion is not restricted to topological field theory. For instance already plain quantum mechanics is usefully formulated this way, that's the point of [[finite quantum mechanics in terms of dagger-compact categories]].

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

Similarly, the categories [[Diff]] or [[Set]] [[smooth manifolds]] or just bare [[sets]] carries a monoidal structure given simply by the [[Cartesian product]] of sets. This is called a [[cartesian monoidal structure]].

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

#### Partition functions and Dual objects

Consider now for simplicity of notation an application in [[quantum computing]]/[[quantum information theory]], where the [[spaces of states]] $V$ involved are [[finite dimensional vector spaces]] (spaces of [[qubits]]), such as for instance in the topological sector of the [[quantum Hall effect|quantum Hall system]].

Then for every space of states $V$ there is the [[dual vector space]]  $V^\ast$. In [[physics]] notation the states in $V$ are the [[kets]] $\vert \Psi \rangle$, while those of $V^\ast$ are the "bra-s" $\langle \Psi \vert$.


| [[physics]] |  [[category theory]] |
|-------------|----------------------|
| [[bra]]/[[ket]]  |  [[dual objects]] |


Essentially all of [[quantum information theory]] has a slick reformulation in terms of [[category theory]] for [[symmetric monoidal category]] [[rigid monoidal category|with dual objects]]. More on this is at _[[finite quantum mechanics in terms of dagger-compact categories]]_.


While the introduction of bra-ket notation by [[Paul Dirac]] was (while just notation) already quite useful for thinking about the subject, the language of monoidal category in fact reflects the actual physical processes involved even better:

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
     & \searrow && \uparrow
     \\
     && \longrightarrow
  }
$$

This is striking, because this _picture_ is an accurate reflection of the physical process that the [[partition function]] describes, for the partition function is the [[correlator]] of a particle with a closed circular [[worldline]].

In fact, the monoidal category theoretic [[string diagram]]-notation is essentially the [[Feynman diagram]]-notation. This we turn to [below](#QMWithInteractionAndFeynmanDiagrams).



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

### Naive generalization: Global 2d TQFT 
 {#Global2dTQFT}

Atiyah-Segal...

... [[2d TQFT]] ... [[Frobenius algebra]] ...

$$
  Bord_2^{\sqcup} \longrightarrow Vect^\otimes
$$

### Local 2d TQFT -- The topological String  
 {#Local2dTQFT}

Curiously, the above does _not_ capture the original motivating examples for [[2d TQFT]] that came from physics, namely it does not capture the "[[cohomological quantum field theory]]" due to [[Edward Witten]], such as the [[topological string]] in its incarnation as the [[A-model]] and [[B-model]] and the [[Landau-Ginzburg model]].

need to 

1. remember [[diffeomorphism]]; 

1. remember locality 

via [[higher category theory]]

...[[TCFT]]...


### Global 3d TQFT -- Chern-Simons theory
 {#Global3dTQFT}

...[[quantization of 3d Chern-Simons theory]]...

...[[Reshetikhin-Turaev construction]]...

### Local 3d TQFT -- Modular functor and Wess-Zumino-Witten theory
 {#Local3dTQFT}

... [[modular functor]] ...

### General local TQFT
 {#IntroductionGeneralFormulation}

... [[(infinity,n)-category of cobordisms]]...

... [[symmetric monoidal (infinity,n)-category]]...

... [[fully dualizable object]]...

... [[cobordism hypothesis]]...


## References

### Formalization of sewing and locality in terms of functoriality##

It was in

* Michael Atiyah, _Topological quantum field theory_, Publications Math&#233;matiques de l'IH&#201;S, 68  (1988), p. 175-186

that it was realized that 

* this means that this property can be taken as the <em>defining</em> property of the path integral, thereby circumventing the problem of constructing it as an actual integral;

* this property can be conveniently axiomatized by saying that the path integral is a [[functor]] from a suitable category whose morphisms are [[cobordism]]s to a category of vector spaces.

(Strictly speaking, Atiyah's original article mentions this functor slightly indirectly only.)

All this was originally formalized in the context of [[TQFT|topological quantum field theory]] only. This is the easiest case that already exhibits all the functoriality that is implied by "FQFT" but by far not the only case (see below).

A pedagogical exposition of how the physicist's way of thinking about the path integral leads to its definition as a functor is given in

* Kevin Walker, _TQFTs_ ([pdf](http://canyon23.net/math/tc.pdf))

A pedagogical exposition of the notion of quantum field theory as a functor on [[cobordism]]s is in 

* {#Baez04} [[John Baez]], _Quantum quandaries: a Category-Theoretic perspective_ ([arXiv](http://arxiv.org/abs/quant-ph/0404040))

and a review of much of the existing material in the literature is in 

* Bruce H. Bartlett, _Categorical Aspects of Topological Quantum Field Theories_ ([arXiv](http://arxiv.org/abs/math/0512103)).

The influential work by Moore and Segal on open-closed 2d TFTs is available as

* [[Greg Moore]], [[Graeme Segal]], _D-branes and K-theory in 2D topological field theory_ ([arXiv](http://arxiv.org/abs/hep-th/0609042))

The same topic is studied by Lazariou:

* [[Calin Lazariou]], _On the structure of open-closed topological field theory in two dimensions_

### Non-topological FQFTs (especially conformal)## 

This mostly concentrates on [[TQFT|topological quantum field theories]], those where the path integral depends only on the diffeomorphism class of the domain it is evaluated on. This is the simplest and by far best understood case. But the idea of functorial FQFT is not restricted to this case.

This was realized in

* Graeme Segal, _The definition of conformal field theory_, in: _Topology, Geometry and quantum field theory_, London. Math. Soc. LNS 308, edited by U. Tillmann, Cambridge Univ. Press 2004, 247-343

There the notion of 2-dimensional [[conformal field theory]] is axiomatized as a functor on a category of 2-dimensional cobordisms with conformal structure.

(Apparently a similar definition has been given by Kontsevich, but never published.) The details of the category of conformal cobordisms can get a bit technical and slight variations of Segal's original definition may be necessary. The work by Huang and Kong can be regarded as a further refinement and maybe completion of Segal's program

* Yi-Zhi Huang, _Geometric interpretation of vertex operator algebras_, Proc. Natl. Acad. Sci. USA, Vol 88. (1991) pp. 9964-9968

* Liang Kong, _Open-closed field algebras_ Commun. Math. Physics. 280, 207-261 (2008) ([arXiv](http://arxiv.org/abs/math/0610293)).

A very concrete construction of functorial CFTs (for the special case of _rational_ CFTs) is provided by the 
[[FFRS-formalism]].

### Extended (multi-tiered) FQFT {#Extended}

But one notices that the formalization of quantum field theory as a [[functor]] on [[cobordism]]s encodes only a small aspect of the full sewing law imagined to be satisfied by the path integral: In a 1-[[category]] of $n$-dimensional [[cobordism]]s these are glued along $(n-1)$-dimensional boundaries. One could imagine more generally a formalization where a given [[cobordism]] is allowed to be chopped into arbitrary parts of arbitrary co-dimension such that the path integral can still consistently be evaluated on each of these parts.

This leads to the notion of _extended quantum field theory_, which is taken to be an $\infty$-functor on an [[higher category theory|infinity category]] of [[extended cobordism]]s. Early ideas about a formalization of this approach were given in

* John Baez and Jim Dolan, _Higher-dimensional algebra and Topological Quantum Field Theory_  ([arXiv](http://arxiv.org/abs/q-alg/9503002)) .

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

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_ 

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

### homological FQFT (and TCFT) ##

As usual, the problem of constructing FQFT becomes much more tractable when linear approximations are applied. In homological FQFT and in [[TCFT]] the Hom-spaces of the cobordism category (the moduli spaces of cobordisms with given punctures/boundaries) are approximated by complexes  of chains on them. This leads to formalization of $\infty$-functorial QFT in the context of [[dg-algebra]].

* [[Ezra Getzler]], ...

  * [[TCFT]]

* [[Maxim Kontsevich]], ...


* [[Kevin Costello]], ...
 
  * [[factorization algebra]]


* etc.

## Related concepts

* [[quantum field theory]]

  * [[AQFT]]

    * [[Haag-Kastler axioms]]

    * [[local net of observables]]

  * **FQFT**

    * [[TQFT]], 
 
      * [[extended topological quantum field theory]], [[0-dimensional TQFT]], [[3d TQFT]] [[4d TQFT]], [[HQFT]]

    * [[(1,1)-dimensional Euclidean field theories and K-theory]]

    * [[(2,1)-dimensional Euclidean field theories and tmf]]

  

[[!include Isbell duality - table]]



[[!redirects FQFTs]]
[[!redirects Functorial quantum field theory]]
[[!redirects Functorial quantum field theories]]
[[!redirects functorial quantum field theory]]
[[!redirects functorial quantum field theories]]