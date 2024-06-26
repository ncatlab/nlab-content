
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

By _quantization_ is meant some process that 

1. reads in a system of [[classical mechanics]], or rather of _[[prequantum field theory|prequantum]]_ data in the form of an [[Lagrangian]]/[[action functional]] and or a [[phase space]] equipped with [[symplectic manifold|symplectic structure]]

1. and returns a corresponding system of [[quantum mechanics]].

### Motivation from classical mechanics and Lie theory
 {#MotivationFromClassicalMechanicsAndLieTheory}

We indicate here a systematic motivation of quantization by looking at [[classical mechanics]] formalized as [[symplectic geometry]] from the point of view of [[Lie theory]] ([Fiorenza-Rogers-Schreiber 13](#FiorenzaRogersSchreiber13), [Nuiten 13](#Nuiten13)).

$\,$

Quantization of course was and is motivated by experiment, hence by observation of the [[observable universe]]: it just so happens that [[quantum mechanics]] and [[quantum field theory]] correctly account for experimental observations where [[classical mechanics]] and [[classical field theory]] gives no answer or incorrect answers. A historically important example is the phenomenon called the "[[ultraviolet catastrophe]]", a [[paradox]] predicted by classical [[statistical mechanics]] which is _not_ observed in nature, and which is corrected by [[quantum mechanics]].

But one may also ask, independently of experimental input, if there are good formal mathematical reasons and motivations to pass from [[classical mechanics]] to [[quantum mechanics]]. Could one have been led to [[quantum mechanics]] by just pondering the mathematical formalism of [[classical mechanics]]? (Hence more precisely: is there a natural _[[schreiber:Synthetic Quantum Field Theory]]_?)

The following spells out an argument to this effect. It will work for readers with a background in modern [[mathematics]], notably in [[Lie theory]], and with an understanding of the formalization of classical/prequantum mechanics in terms of [[symplectic geometry]]. 

So to briefly recall, a system of [[classical mechanics]]/[[prequantum field theory|prequantum mechanics]] is a [[phase space]], formalized as a [[symplectic manifold]] $(X, \omega)$. A symplectic manifold is in particular a [[Poisson manifold]], which means that the [[algebra of functions]] on [[phase space]] $X$, hence the algebra of _classical [[observables]]_, is canonically equipped with a compatible [[Lie bracket]]: the _[[Poisson bracket]]_. This Lie bracket is what controls [[dynamics]] in [[classical mechanics]]. For instance if $H \in C^\infty(X)$ is the function on [[phase space]] which is interpreted as assigning to each configuration of the system its [[energy]] -- the [[Hamiltonian]] function -- then the [[Poisson bracket]] with $H$ yields the [[infinitesimal object|infinitesimal]] time evolution of the system: the [[differential equation]] famous as [[Hamilton's equations]].

Something to take notice of here is the _[[infinitesimal space|infinitesimal]]_ nature of the [[Poisson bracket]]. Generally, whenever one has a [[Lie algebra]] $\mathfrak{g}$, then it is to be regarded as the [[infinitesimal object|infinitesimal]] approximation to a globally defined object, the corresponding [[Lie group]] (or generally [[smooth group]]) $G$. One also says that $G$ is a _[[Lie integration]]_ of $\mathfrak{g}$ and that $\mathfrak{g}$ is the [[Lie differentiation]] of $G$.

Therefore a natural question to ask is: _Since the observables in [[classical mechanics]] form a [[Lie algebra]] under [[Poisson bracket]], what then is the corresponding [[Lie group]]?_

The answer to this is of course "well known" in the literature, in the sense that there are relevant monographs which state the answer. But, maybe surprisingly, the answer to this question is not (at time of this writing) a widely advertized fact that has found its way into the basic educational textbooks. The answer is that this [[Lie group]] which integrates the [[Poisson bracket]] is the "[[quantomorphism group]]", an object that seamlessly leads to the [[quantum mechanics]] of the system.

Before we spell this out in more detail, we need a brief technical aside: of course [[Lie integration]] is not quite unique. There may be different global [[Lie group]] objects with the same [[Lie algebra]]. 

The simplest example of this is already one of central importance for the issue of quantization, namely, the Lie integration of the abelian [[line Lie algebra]] $\mathbb{R}$. This has essentially two different [[Lie groups]] associated with it: the [[simply connected topological space|simply connected]] [[translation group]], which is just $\mathbb{R}$ itself again, equipped with its canonical additive [[abelian group]] structure, and the [[discrete space|discrete]] [[quotient]] of this by the group of [[integers]], which is the [[circle group]]

$$
  U(1) = \mathbb{R}/\mathbb{Z}
  \,.
$$

Notice that it is the discrete and hence "quantized" nature of the [[integers]] that makes the [[real line]] become a [[circle]] here. This is not entirely a coincidence of terminology, but can be traced back to the heart of what is "quantized" about [[quantum mechanics]].

Namely, one finds that the [[Poisson bracket]] [[Lie algebra]] $\mathfrak{poiss}(X,\omega)$ of the classical [[observables]] on [[phase space]] is (for $X$ a [[connected topological space|connected]] [[manifold]]) a [[Lie algebra extension]] of the Lie algebra $\mathfrak{ham}(X)$ of [[Hamiltonian vector fields]] on $X$ by the [[line Lie algebra]]:

$$
  \mathbb{R} \longrightarrow \mathfrak{poiss}(X,\omega) \longrightarrow \mathfrak{ham}(X)
  \,.
$$

This means that under [[Lie integration]] the [[Poisson bracket]] turns into an [[central extension]] of the group of [[Hamiltonian symplectomorphisms]] of $(X,\omega)$. And either it is the fairly trivial non-compact extension by $\mathbb{R}$, or it is the interesting [[central extension]] by the [[circle group]] $U(1)$. For this non-trivial [[Lie integration]] to exist, $(X,\omega)$ needs to satisfy a quantization condition which says that it admits a [[prequantum line bundle]]. If so, then this $U(1)$-[[central extension]] of the group $Ham(X,\omega)$ of [[Hamiltonian symplectomorphisms]] exists and is called... the _[[quantomorphism group]]_ $QuantMorph(X,\omega)$:

$$
  U(1) \longrightarrow QuantMorph(X,\omega) \longrightarrow Ham(X,\omega)
  \,.
$$

While important, for some reason this group is not very well known, which is striking because it contains a small [[subgroup]] which is famous in [[quantum mechanics]]: the _[[Heisenberg group]]_.

More precisely, whenever $(X,\omega)$ itself has a [[Hamiltonian action|compatible]] [[group]] structure, notably if $(X,\omega)$ is just a [[symplectic vector space]] (regarded as a group under addition of vectors), then we may ask for the [[subgroup]] of the [[quantomorphism group]] which covers the (left) [[action]] of [[phase space]] $(X,\omega)$ on itself. This is the corresponding [[Heisenberg group]] $Heis(X,\omega)$, which in turn is a $U(1)$-[[central extension]] of the group $X$ itself:

$$
  U(1) \longrightarrow Heis(X,\omega) \longrightarrow X
  \,.
$$

At this point it is worth pausing for a second to note how the hallmark of [[quantum mechanics]] has appeared as if out of nowhere simply by applying [[Lie integration]] to the [[Lie algebra|Lie algebraic]] structures in [[classical mechanics]]:

if we think of [[Lie integration|Lie integrating]] $\mathbb{R}$ to the interesting [[circle group]] $U(1)$ instead of to the uninteresting [[translation group]] $\mathbb{R}$, then the name of its canonical [[basis]] element $1 \in \mathbb{R}$ is canonically "$i$", the imaginary unit. Therefore one often writes the above [[central extension]] instead as follows:

$$
  i \mathbb{R} \longrightarrow \mathfrak{poiss}(X,\omega) \longrightarrow \mathfrak{ham}(X,\omega)
$$

in order to amplify this. But now consider the simple special case where $(X,\omega) = (\mathbb{R}^2, d p \wedge d q)$ is the 2-dimensional [[symplectic vector space]] which is for instance the [[phase space]] of the [[particle]] propagating on the line. Then a canonical set of generators for the corresponding [[Poisson bracket]] [[Lie algebra]] consists of the linear functions $p$ and $q$ of classical mechanics textbook fame, together with the _constant_ function. Under the above Lie theoretic identification, this constant function is the canonical basis element of $i \mathbb{R}$, hence purely Lie theoretically it is to be called "$i$".

With this notation then the [[Poisson bracket]], written in the form that makes its [[Lie integration]] manifest, indeed reads

$$
  [q,p] = i
  \,.
$$

Since the choice of [[basis]] element of $i \mathbb{R}$ is arbitrary, we may rescale here the $i$ by any non-vanishing [[real number]] without changing this statement. If we write "$\hbar$" for this element, then the [[Poisson bracket]] instead reads

$$
  [q,p] = i \hbar
  \,.
$$


This is of course the hallmark equation for [[quantum physics]], if we interpret $\hbar$ here indeed as [[Planck's constant]]. We see it arises here merely by considering the non-trivial (the interesting, the non-simply connected) [[Lie integration]] of the [[Poisson bracket]]. 

This is only the beginning of the story of quantization, naturally understood and indeed "derived" from applying [[Lie theory]] to [[classical mechanics]]. From here the story continues. It is called the story of _[[geometric quantization]]_. We close this motivation section here by some brief outlook.

The [[quantomorphism group]] which is the non-trivial [[Lie integration]] of the [[Poisson bracket]] is naturally constructed as follows: given the [[symplectic form]] $\omega$, it is natural to ask if it is the [[curvature]] 2-form of a $U(1)$-[[principal connection]] $\nabla$ on [[complex line bundle]] $L$ over $X$ (this is directly analogous to [[Dirac charge quantization]] when instead of a [[symplectic form]] on [[phase space]] we consider the  the [[field strength]] 2-form of [[electromagnetism]] on [[spacetime]]). If so, such a connection $(L, \nabla)$ is called a _[[prequantum line bundle]]_ of the [[phase space]] $(X,\omega)$. The [[quantomorphism group]] is simply the [[automorphism group]] of the [[prequantum line bundle]], covering [[diffeomorphisms]] of the phase space (the [[Hamiltonian symplectomorphisms]] mentioned above).

As such, the [[quantomorphism group]] naturally [[action|acts]] on the [[space of sections]] of $L$. Such a [[section]] is like a [[wavefunction]], except that it depends on all of [[phase space]], instead of just on the "[[canonical coordinates]]". For purely abstract mathematical reasons (which we won't discuss here, but see at _[[motivic quantization]]_ for more) it is indeed natural to choose a "[[polarization]]" of [[phase space]] into [[canonical coordinates]] and [[canonical momenta]] and consider only those [[sections]] of the [[prequantum line bundle]] which depend only on the former. These are the actual _[[wavefunctions]]_ of [[quantum mechanics]], hence the _[[quantum states]]_. And the [[subgroup]] of the [[quantomorphism group]] which preserves these polarized sections is the group of exponentiated [[quantum observables]]. For instance in the simple case mentioned before where $(X,\omega)$ is the 2-dimensional [[symplectic vector space]], this is the [[Heisenberg group]] with its famous action by multiplication and differentiation operators on the space of complex-valued functions on the real line.







### Quantization of field theory


An interesting subclass of [[quantum field theory|quantum field theories]], especially of [[perturbative quantum field theories]], is thought to arise from [[prequantum field theory]] via a process of _quantization_.   This process reads in certain -- usually [[differential geometry|differential geometric]] -- data ([[Lagrangian field theory]]), interprets this data as specifying the dynamics of some [[physical system]], and spits out the [[perturbative quantum field theory|perturbative]] [[quantum field theory]] that encodes the time evolution of this system.

For more on this see at _[[Wick algebra]]_ and _[[causal perturbation theory]]_.

Historically, it was an approximation to the true time evolution that was originally found and studied, by Newton, Maxwell, Einstein and others. This is now known as "[[classical physics]]". The true dynamics in turn is "[[quantum physics]]".

In view of this, quantization is often understood as a [[retraction|right inverse]] to the procedure that sends the full quantum dynamics to its [[classical limit]]. As such it is not well defined, i.e. unique, when it exists. Additional structures sometimes make it unique. 

[[!include deformation quantization - table]]


There have been found some formalizations of at least some aspects of quantization, notably there is _[[algebraic deformation quantization]]_ and _[[geometric quantization]]_. 

[[!include Isbell duality - table]]

These traditional formulations are geared towards [[mechanics]] (as opposed to [[field theory]]). Even in that restricted application, it seems that a more comprehensive understanding is still missing

> The goal is to get closer to a systematic theory of [[quantization]].
  
> ([Gukov-Witten 08, p.4](#GukovWitten08))

In the context of [[field theory]] the conceptual issues become even more severe. For example the class of [[field theories]] called _[[Yang-Mills theory]]_ is a core ingredient in the [[standard model of particle physics]] but the _[[quantization of Yang-Mills theory]]_ (see there for more) poses famous open problems -- of which of course that there isn't yet a comprehensive theory of what this even means is not the least.

## Quantization as an index map
 {#QuantizationAsAnIndexMap}

Here we survey aspects of quantization which give rise to an _[[index]]_ map or something similar, that is, a [[push-forward in generalized cohomology]]. More on this is in ([Nuiten 13](#Nuiten13)) and at _[[motivic quantization]]_.

The general pattern here is this:

* The [[kinetic action]] part of the [[action functional]] of a [[prequantum field theory]] is really part of the [[measure]]/[[orientation in generalized cohomology]] on the [[moduli space]] of [[field (physics)|fields]]

* The (gauge coupling-)[[interaction]] in the [[action functional]] of a [[prequantum field theory]] induces a [[cocycle]] in some [[cohomology]] which serves as a [[twisted cohomology|twist]] for the [[generalized cohomology theory]] in which the above [[integration]]/push-forward takes place.

* the [[push-forward in generalized cohomology|push-forward]] itself is the [[path integral quantization]], the construction of [[partition functions]].

### Path integral by integration against the Wiener measure

For instance the archetypical example of the quantization of the [[charged particle]] propagating on a [[Riemannian manifold]] $X$ proceeds (in [[Wick rotation|Wick rotated]] form as it appears in the [[worldline formalism]] for corresponding QFT) like so: write $[\exp(-S_{kin}(\gamma)) D\gamma]$ for the [[Wiener measure]] on paths in $X$, then the [[integral kernel]] of the time evolution propagator of the quantum particle is given by the [[path integral]] (see there for more)

$$
  \int_{\gamma \in P_{x_{in}, x_{out}}X} tra_{\nabla}(\gamma) \; [\exp(- S_{kin}(\gamma)) D\gamma]
$$

which is the [[integration]] of the [[parallel transport]]/[[holonomy]] functional (of the given [[connection on a bundle|connection]] that models the [[background gauge field]]) against the [[Wiener measure]].


### Quantization by partition function/index in supersymmetric quantum mechanics

More generally, for given any [[phase space]] equipped with a [[prequantum line bundle]] $(L_\omega, \nabla)$, the corresponding _[[geometric quantization]]_ is, if $X$ admits a compatible [[spin^c structure]], the [[index]] of the [[spin^c Dirac operator]] coupled to this bundle, hence the [[space of quantum states]] is

$$
  \mathcal{H} = index( D_{\nabla} )
  \,.
$$

For more on this see at _[geometric quantization -- As Index of the Spin^c Dirac operator](geometric%20quantization#AsIndexOfSpinCDiracOperator)_.

Here the [[Dirac operator]] represents a class in [[K-homology]]

$$
  [D] \in KK(X, \mathbb{C})
$$

and this is now the "[[measure]]" against which the [[K-theory]] class

$$
  [L_\omega] \in KK(\mathbb{C}, X)
$$

of the [[prequantum line bundle]] is being integrated, by the [[index]] map hence the [[composition]] in [[KK-theory]]:

$$
  [\mathcal{H}] \simeq 
  (\mathbb{C} \stackrel{L_\omega}{\to} C(X) \stackrel{D}{\to} \mathbb{C} ) \in KK(\mathbb{C}, \mathbb{C})
  \,.
$$

By the discussion at _[[index]]_ this is equivalently the [[partition function]] of an auxiliary [[supersymmetric quantum mechanics]] system with [[background gauge field]] $\nabla$:

$$
  \mathcal{H} \simeq sTr( \exp(-t D^2) ) \;\;\;\; \forall t \gt 0
  \,.
$$

The appearance of an _auxiliary_ and already quantized field theory here may seem circular, but is in fact part of a deeper pattern of quantization by the [[holographic principle]], where rich quantum theories arise as [[boundary field theories]] of higher dimensional [[topological field theories]]. In the above case the higher dimensional theory is secretly the non-perturbative version of the [[Poisson sigma-model]] associated with the original [[phase space]] [[Poisson manifold]]. More details on this are indicated at _[[extended geometric quantization of 2d Chern-Simons theory]]_. In one dimension higher the [[Witten genus]] arises this way as the quantization of the [[heterotic string]] 2d QFT regarded as the [[boundary field theory]] of the [[M2-brane]] in [[Horava-Witten theory]]. (See ([Nuiten13](#Nuiten13)) for more.)

### Cohomological formulation in BV-formalism

The choice of [[spin^c structure]] in the above is really the choice of a [[Poincaré  duality]] (see at [[Poincaré duality algebra]] for more) which exhibits the [[orientation in generalized cohomology]] by a combined [[Atiyah duality]]/[[Thom isomorphism]]. 

The analogue of such a choice of [[Poincaré duality]] between [[cohomology]] and [[homology]] in [[BV-formalism]] is the choice of a [[volume form]] that identified the [[de Rham complex]] with the [[BV-complex]] of [[multivector fields]]. See at _[BV-BRST formalism -- Homological integration](BV-BRST+formalism#HomologicalIntegration)_.

Again, here the [[kinetic action functional]] is part of the [[measure]], now under the duality part of the [[BV-operator]]. The [[quantum master equation]] is now the analog of the orientability condition. Homological BV-quantization is then obtain by assing to the [[homology groups]] of this [[BV-operator]], hence again by "pushing it to the point".

This is the setup in which one can derive [[Feynman diagram]] rules form cohomologicalquantization, see at _[Feynman diagram -- Refereces -- In homological BV-quantization](Feynman+diagram#ReferencesInHomologicalBVQuantization)_.

## Examples

* [[quantum harmonic oscillator]]

* [[quantization of the 2-sphere]]

* [[quantization of Chern-Simons theory]]

* [[quantization of loop groups]]


## Related entries

* **quantization**

  * [[deformation quantization]]

    * [[Moyal quantization]]

  * [[geometric quantization]], [[higher geometric quantization]]

    * [[geometric quantization of symplectic groupoids]]

    * [[geometric quantization by push-forward]]

  * [[Weyl quantization]], [[Born-Jordan quantization]]

  * [[path integral quantization]]

  * [[stochastic quantization]]

  * [[semiclassical approximation]]

  * [[light-cone gauge quantization]]

  * [[quantization via the A-model]]


* [[second quantization]]

* [[fiber bundles in physics]]

* [[motivic quantization]]

* [[perturbation theory]]

  * [[formal deformation quantization]]

  * [[BV quantization]]

* overview: [[reductions deformations resolutions in physics]]

## References 

* [[Nik Weaver]], *Mathematical Quantization*, Routledge (2011) &lbrack;[ISBN 9781584880011](https://www.routledge.com/Mathematical-Quantization/Weaver/p/book/9781584880011)&rbrack;

* S. Twareque Ali, Miroslav Engli&#353;, _Quantization Methods: A Guide for Physicists and Analysts_, Rev. Math. Phys. **17** (2005) 391-490 &lbrack;[arXiv:math-ph/0405065](http://arxiv.org/abs/math-ph/0405065)&rbrack;

Specifically on [[geometric quantization]]:

* {#BatesWeinstein} Sean Bates, [[Alan Weinstein]], _[[Lectures on the geometry of quantization]]_, AMS (1997) &lbrack;[pdf](http://www.math.berkeley.edu/~alanw/GofQ.pdf)&rbrack;
 



See also references at *[[quantum mechanics]]*.

A proposal for a full formalization of the notion of quantization for "finite" theories such as [[Dijkgraaf-Witten theory]] is in

* [[Dan Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], _[[Topological Quantum Field Theories from Compact Lie Groups]]_ ([arXiv:0905.0731](http://arxiv.org/abs/0905.0731))

A historical discussion by [[Zoran Škoda|one]] of the $n$labizants is here: [mathlight:quantization](http://mathlight.wordpress.com/2010/03/19/quantization). See also Urs's manifesto at [[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]].

* {#HenneauxTeitelboim} [[Marc Henneaux]], [[Claudio Teitelboim]], _[[Quantization of Gauge Systems]]_, Princeton University Press 1992

* [[Nikolai Reshetikhin]], _Lectures on quantization of gauge systems_, [arxiv/1008.1411](http://arxiv.org/abs/1008.1411)

The [[quantization via the A-model]]-method is described in

* {#GukovWitten08} [[Sergey Gukov]], [[Edward Witten]], _Branes and quantization_, ([arxiv/0809.0305](http://arxiv.org/abs/0809.0305))
 
 
The perspective of [[geometric quantization|geometric]] pre-quantization as a canonical construction in higher [[Lie theory]] is discussed in 

* [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher geometric prequantum theory]]_ ([arXiv:1304.0236](http://arxiv.org/abs/1304.0236))
  {#FiorenzaRogersSchreiber13}

A discussion of quantization as cohomological/[[motivic quantization]] of [[higher prequantum field theory]] is in 

* [[Joost Nuiten]], _[[schreiber:master thesis Nuiten|Cohomological quantization of local boundary prequantum field theory]]_ Master thesis, Utrecht 2013
 {#Nuiten13}

Some discussion of quantization in terms of [[Bohr toposes]] is in 

* Kunji Nakayama, _Sheaves in Quantum Topos Induced by Quantization_ ([arXiv:1109.1192](http://arxiv.org/abs/1109.1192))

Joint discussion of a variety of quantization schemes:

* [[Joshua Lackman]], *Geometric Quantization Without Polarizations* &lbrack;[arXiv:2405.01513](https://arxiv.org/abs/2405.01513)&rbrack;



[[!redirects quantizations]]

[[!redirects quantisation]]
[[!redirects quantisations]]

