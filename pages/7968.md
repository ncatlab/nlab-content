
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea
 {#Idea}

What is called _Planck's constant_ in [[physics]] and specifically in [[quantum physics]] (after [[Max Planck]]) is a [[physical unit]] of 
"[[action functional|action]]" which sets the [[scale]] at which effects of [[quantum physics]] are genuinely important and physics is no longer well approximated by [[classical mechanics]]/[[classical field theory]]. 

This we discuss below at

* _[As a physical constant](#AsAPhysicalConstant)_

In the [[mathematics|mathematical]] formulation of the [[theory (physics)|theory]], Planck's constant $h$ is the choice of [[unit]] $h \in \mathbb{R}^\times$ in the [[short exact sequence]]  $\mathbb{Z}\stackrel{h\cdot(-)}{\longrightarrow} \mathbb{R} \to U(1)$ 
which governs the [[prequantization]] lift from real ([[differential cohomology|differential]]) [[cohomology]] to ([[differential cohomology|differential]]) [[integral cohomology]]. The [[integer|integrality]] of $\mathbb{Z}$ here is the very "quantum"-ness of quantum theory, and this is what Planck's constant parameterizes. This we discuss below in

* _[In geometric quantization](#InGeometricQuantization)_.


Finally, when infinitesimally approximating this [[quantization]] step in [[perturbation theory]] in $\hbar$ (see at [[formal deformation quantization]]), then Planck's constant is the very [[formal geometry|formal expansion parameter]] of the [[deformation theory|deformation]]. This we discuss below in

* _[In perturbative quantization](#InFormalDeformationQuantization)_.

Applied to the key example of [[perturbative quantum field theory]] it turns out that the powers of $\hbar$ in contributions to the [[Feynman perturbation series]]  essentially correspond to the [[loop order]] of the given [[Feynman diagram]]. This we discuss in

* _[In the Feynman perturbation series](#InFeynmanPerturbationSeries)_


## As a physical constant 
 {#AsAPhysicalConstant}
 
The original __Planck constant__ $h$ is a quantum of [[action functional|action]]. It may be illustrated in the case of the [[electromagnetic field]] by the fact that each of its [[quanta]] -- a [[photon]] -- carries an [[energy]] $E$ that is fixed by its [[frequency]] (cycles per second) $\nu$ according to the relation $E = h\nu$. Thus, the energy emitted by a [[laser]] beam of fixed frequency $\nu$ is an integer multiple $n h \nu$ of a packet of energy $h\nu$, where $n$ is the number of photons emitted. 

As a fundamental physical constant, $h$ has dimension $(mass)(length)^2(time)^{-1}$. In meter-kilogram-second (MKS) [[physical units|units]], its value is exactly

$$h = 6.62607015 \cdot 10^{-34} m^2 kg / s$$ 

by the SI definition of the kilogram. 

The __reduced Planck constant__ or __Dirac constant__ $\hbar = h/2\pi$ is the proportionality constant that relates energy (of a photon) to angular frequency $\omega$ (radians per second as opposed to cycles per second), so that $E = \hbar \omega$. 


## In geometric quantization
 {#InGeometricQuantization}

### Basic definition
 {#BasicDefinition}

The step of [[prequantization]] is about refining data in ([[differential cohomology|differential]]) real [[cohomology]] to ([[differential cohomology|differential]]) [[integral cohomology]]. Often this is understood in terms of the canonical inclusion

$$
  \mathbb{Z} \hookrightarrow \mathbb{R}
$$

of the [[integers]] as an addiditve [[subgroup]] of the [[real numbers]]. But since strictly speaking what appears in [[physics]] is the [[real line]] on which a [[unit]] is chosen as part of the identification of mathematical formalism with physical reality, one should really consider _all_ possible additive group homomorphisms $\mathbb{Z}\to \mathbb{R}$. These are parameterized by 

$$
  h \in (\mathbb{R}- \{0\}) \hookrightarrow \mathbb{R}
$$

$$
  (-)\cdot h \;\colon\; \mathbb{Z} \longrightarrow \mathbb{R}
$$

and this "physical [[unit]]" $h$ is what is called _Planck's constant_. 

In particular the induced [[circle group]] is identified as the [[quotient]] of $\mathbb{R}$ by $h \mathbb{Z}$, in this sense

$$
  U(1) \simeq \mathbb{R}/h \mathbb{Z}
$$

and under this identification its [[quotient]] map is expressed in terms of the [[exponential function]] $\exp \colon z \mapsto  \sum_{k = 0}^\infty \frac{z^k}{k!} \in \mathbb{C}$ as

$$
  \exp(2 \pi \tfrac{i}{h}(-))
  =
  \exp(\tfrac{i}{\hbar} (-)) \;\colon\; \mathbb{R} \longrightarrow U(1)
  \,,
$$

where

$$
  \hbar \coloneqq h/2\pi
  \,.
$$

The resulting [[short exact sequence]] is the real [[exponential exact sequence]]

$$
  0 
   \to 
  \mathbb{Z} 
    \longrightarrow 
  \mathbb{R} 
    \stackrel{\exp\left(\tfrac{i}{\hbar}(-)\right)}{\longrightarrow} 
  U(1) 
    \to 
  0
  \,.
$$

This is the source of the ubiquity of the expression  $\exp(\tfrac{i}{\hbar} (-))$ in [[quantum physics]], say in the [[path integral]], where the exponentiated [[action functional]] appears as $\exp(\tfrac{i}{\hbar} S)$.

### In relation to the symplectic form

In the context of [[geometric quantization]] Planck's constant appears as the inverse scale of the [[symplectic form]]. 

For instance in the simple case that [[phase space]] is $T^* \mathbb{R} \simeq \mathbb{R}^2$ with standard coordinates $\{p,q\}$, then the normalization of the symplectic form $\sim d p \wedge dq$ actually needed in physics is

$$
  \omega = \frac{1}{\hbar} d p \wedge d q
  \,.
$$

This is because after [[geometric quantization]] of this form the [[observables]] will obey

$$
  [\hat q, \hat p] = i (\omega_{p,q})^{-1}
$$

and this is supposed to be

$$
  \cdots = i \hbar
  \,.
$$

Accordingly, it follows that if $(E, \nabla)$ is a [[prequantum line bundle]] for $\omega$, then its $k$-fold [[tensor product]] with itself, for $k \in \mathbb{N}$, is a line bundle $(E^{\otimes k}, \nabla_k)$ with [[curvature]] $k \omega$. By the above this corresponds to rescaling

$$
  \hbar \to \hbar / k
  \,.
$$

This implies in particular

1. a global rescaling of the [[periods]] of the symplectic form may be absorbed in a rescaling of Planck's constant, see at _[[geometric quantization of non-integral forms]]_;

1. for $(E, \nabla)$ a given [[prequantum line bundle]] the limit of the tensor powers $(E^{\otimes k}, \nabla_k)$ as $k$ tends to [[infinity]] roughly corresponds to taking a [[classical limit]]. See also ([Donaldson 00](#Donaldson00)).



### Examples


In [[Chern-Simons theory]] Planck's constant corresponds to the inverse _level_ of the theory, hence the inverse of the [[characteristic class]] that defines the theory, regarded as an element in $\mathbb{Z}$.

Similarly for [[schreiber:infinity-Chern-Simons theory]]. 
For instance ordinary [[spin group]] Chern-Simons theory may be taken to have as the fundamental value $\hbar = 2$, because the [[first Pontryagin class]] that defines the theory is divisible by 2, the [[prequantum circle n-bundle|prequantum 3-bundle]] that defines the theory of the [[moduli stack]] of $Spin$-[[principal connections]] is 

$$
  \tfrac{1}{2}\hat \mathbf{p}_1 : \mathbf{B}Spin_{conn} \to \mathbf{B}^3 U(1)_{conn}
  \,.
$$

Similarly for 7-dimensional [[String 2-group]] [[schreiber:infinity-Chern-Simons theory]] the fundamental value is $\hbar = 6$, with the extended Lagrangian being

$$
  \tfrac{1}{6}\hat \mathbf{p}_2 : \mathbf{B}String_{conn} \to \mathbf{B}^7 U(1)_{conn}
  \,.
$$

See at _[[higher geometric quantization]]_ for more on this.



## In perturbative quantization
 {#InFormalDeformationQuantization}

In [[perturbative quantum field theory]] Planck's constant (together with the [[coupling constant]], which indicates the strength of [[interactions]]) is regarded as tiny, in fact as [[infinitesimal]], in that all [[observables]] are expressed as (generally non-converging, [[asymptotic series|asymptotic]]) [[formal power series]] in the coupling constant.

This is explicitly realized by [[formal deformation quantization]], which regards [[quantization]] as as deformation of the classical [[algebra of observables]] to a non-commutative algebra on [[formal power series]] with [[coefficients]] the original observables.

## In perturbative quantum field theory

In [[perturbative quantum field theory]] the [[scattering amplitudes]] in the [[S-matrix]] are expressed as [[formal power series]] in (the [[coupling constant]] and) in [[Planck's constant]] $\hbar$. This formal power series may be expressed as a formal sum of contributions labeled by [[Feynman diagrams]]. The _loop order_ refers to something like the "number of loops" of [[edges]] in the [[Feynman diagram]] that contibutes to a given [[scattering amplitude]]. It turns out that the loop order corresponds to the order in $\hbar$ that is contributed by this diagram (see [below](#RelationToPowersInPlancksConstant)). 

Therefore contributions of graphs at zero without loops (these are [[trees]], and hence these contributions are referred to as being at "tree level") correspond to the limit of [[classical field theory]] with $\hbar \to 0$. Indeed tree level Feynman diagrams yield [[perturbation theory|perturbative]] solutions of the [[classical field theory|classical]] [[equations of motion]] (see [Helling](#Helling)).

Most predictions of the [[standard model of particle physics]] have very good agreement with [[experiment]] already to very low loop order, first or second; inclusion of third loop order is used (at least in [[QCD]]) to constrain theoretical uncertainties of the result (see [Cacciari 05, slide 5](#Cacciari05), e.g. in [[Higgs field]] computation, see [ADDHM 15](#ADDHM15)). 
In rare cases higher loop orders are used (for instance in the computation of the [[anomalous magnetic moments]] [AHKN 12](#AHKN12), but this is not a scattering experiment).

This usefulness of low loop order is forturnate because

1. the [[S-matrix]] [[formal power series]] for all [[theory (physics)|theories]] of interest has _vanishing_ [[radius of convergence]] ([Dyson 52](perturbation+theory#Dyson52)), hence is at best an [[asymptotic series]] for which the [[sum]] of more than some low order terms is meaningless;

1. the computational effort increases immensely with loop order.


## In the Feynman perturbation series 
 {#InFeynmanPerturbationSeries}

In the computation of [[scattering amplitudes]] for [[field (physics)|fields]]/[[particles]] via [[perturbative quantum field theory]] the [[scattering matrix]] ([[Feynman perturbation series]]) is a [[formal power series]] in (the [[coupling constant]] and) [[Planck's constant]] $\hbar$ whose contributions may be labeled by [[Feynman diagrams]]. Each Feynman diagram $\Gamma$ is a finite labeled [[graph]], and the order in $\hbar$ to which this graph contributes is

$$
  \hbar^{ E(\Gamma) - V(\Gamma) }
$$

where 

1. $V(\Gamma) \in \mathbb{N}$ is the number of [[vertices]] of the graph 

1. $E(\Gamma) \in \mathbb{N}$ is the number of [[edges]] in the graph.

This comes about (see at _[S-matrix -- Feynman diagrams and Renormalization](S-matrix#ExistenceAndRenormalization)_ for details) because 

1. the explicit $\hbar$-dependence of the [[S-matrix]] is 

   $$
     S\left(\tfrac{g}{\hbar} L_{int} \right)
     = 
     \underset{k \in \mathbb{N}}{\sum} \frac{g^k}{\hbar^k k!} T( \underset{k \, \text{factors}}{\underbrace{L_{int} \cdots L_{int}}} )
   $$

1. the further $\hbar$-dependence of the [[time-ordered product]] $T(\cdots)$ is

   $$
     T(L_{int} L_{int}) = prod \circ \exp\left( \hbar \int \omega_{F}(x,y) \frac{\delta}{\delta \phi(x)} \otimes \frac{\delta}{\delta \phi(y)}  \right) ( L_{int} \otimes L_{int} )
     \,,
   $$

where $\omega_F$ denotes the [[Feynman propagator]] and $\phi(x)$ the field observable at point $x$ (where we are notationally suppressing the internal degrees of freedom of the fields for simplicity, writing them as [[scalar fields]], because this is all that affects the counting of the $\hbar$ powers). 

The resulting terms of the S-matrix series are thus labeled by 

1. the number of factors of the [[interaction]] $L_{int}$, these are the [[vertices]] of the corresponding Feynman diagram and hence each contibute with $\hbar^{-1}$ 

1. the number of integrals over the Feynman propagator $\omega_F$, which correspond to the edges of the Feynman diagram, and each contribute with $\hbar^1$.

Now the formula for the [[Euler characteristic of planar graphs]] says that the number of regions in a plane that are encircled by edges, the _faces_ here thought of as the number of "loops", is

$$
  L(\Gamma) =  1 + E(\Gamma) - V(\Gamma)
  \,.
$$

Hence a planar Feynman diagram $\Gamma$ contributes with the "[[loop order]]" $L(\Gamma)$ as

$$
  \hbar^{L(\Gamma)-1}
  \,.
$$

So far this is the discussion for internal edges. An actual scattering matrix element is of the form

$$
  \langle \psi_{out} \vert S\left(\tfrac{g}{\hbar} L_{int} \right)
  \vert \psi_{in} \rangle
  \,,
$$

where 

$$
  \vert \psi_{in}\rangle 
    \propto
  \tfrac{1}{\sqrt{\hbar^{n_{in}}}} 
  \phi^\dagger(k_1) \cdots \phi^\dagger(k_{n_{in}}) \vert vac \rangle
$$

is a state of $n_{in}$ free field quanta and similarly

$$
  \vert \psi_{out}\rangle 
    \propto
  \tfrac{1}{\sqrt{\hbar^{n_{out}}}} 
  \phi^\dagger(k_1) \cdots \phi^\dagger(k_{n_{out}}) \vert vac \rangle
$$

is a state of $n_{out}$ field quanta. The normalization of these states, in view of the commutation relation $[\phi(k), \phi^\dagger(q)] \propto \hbar$, yields the given powers of $\hbar$.

This means that an actual [[scattering amplitude]] given by a [[Feynman diagram]] $\Gamma$ with $E_{ext}(\Gamma)$ external vertices scales as

$$
  \hbar^{L(\Gamma) - 1 + E_{ext}(\Gamma)/2 }
  \,.
$$

(For the analogous discussion of the dependence on the actual [[quantum observables]] on $\hbar$ given by [[Bogoliubov's formula]], see [there](Bogoliubov's+formula#PowersInPlancksConstant).)

## History
 {#History}

[[Max Planck]] introduced the constant named after him in the discussion of [[black body radiation]]. In [[classical field theory]] black body radiation comes out completely wrong ("[[ultraviolet catastrophe]]"). Planck fixed this in an ad-hoc but succesful manner by postulating that [[energy]]/[[frequency]] of the [[harmonic oscillators]] in the black body ([[atoms]], [[molecules]]) is quantized in units measured by some quantum of action. Eventually this ad hoc postulate led to a change of the foundations of physics from [[classical physics]] to [[quantum physics]], which now predicts the quantization of energy/frequency from more conceptual, fundamental principles.

## Related concepts

* [[theory (physics)]]

* [[quantization]]

* [[coupling constant]]

[[!include fundamental scales -- contents]]


## References

* {#Donaldson00} [[Simon Donaldson]], _Planck's constant in complex and almost-complex geometry_, XIIIth International Congress on Mathematical Physics (London,
2000), 63&#8211;72, Int. Press, Boston, MA, 2001
 

* Wikipedia, _[Planck's constant](https://en.wikipedia.org/wiki/Planck_constant)_


[[!redirects Planck constant]]
[[!redirects Planck's constant]]
[[!redirects Planck’s constant]]
[[!redirects Planck\'s constant]]

[[!redirects reduced Planck constant]]
[[!redirects reduced Planck's constant]]
[[!redirects reduced Planck’s constant]]
[[!redirects reduced Planck\'s constant]]

[[!redirects Dirac constant]]
[[!redirects Dirac's constant]]
[[!redirects Dirac’s constant]]
[[!redirects Dirac\'s constant]]
