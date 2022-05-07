
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Topological physics
+--{: .hide}
[[!include topological physics -- contents]]
=--
=--
=--

{:goal: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

#Contents#
* table of contents
{:toc}

## Idea

The words "Chern--Simons theory" (after [[Shiing-shen Chern]] and [[James Simons]] who have their names attached to the [[Chern-Simons elements]] and [[Chern-Simons forms]] and [[Chern-Simons circle 3-bundle]] involved) can mean various things to various people, but it generally refers to the three-dimensional [[topological quantum field theory]] whose configuration space is the space of $G$-[[principal bundles]] with [[connection on a bundle]] and whose [[Lagrangian]] is given by the [[Chern-Simons form]] of such a connection (for simply connected $G$), or rather, more generally, whose [[action functional]] is given by the [[higher holonomy]] of the [[Chern-Simons circle 3-bundle]].

In other words, for $G$ a [[Lie group]], Chern-Simons theory is a [[sigma-model]] [[TQFT]] whose [[target space]] is the [[smooth infinity-groupoid|smooth]] [[moduli stack]] $\mathbf{B}G_{conn}$ of $G$-[[principal connections]], and whose [[background gauge field]] is a [[circle n-bundle with connection|circle 3-bundle with connection]] on $\mathbf{B}G_{conn}$. The higher [[Chern class]]/[[Dixmier-Douady class]] of this three bundle is the _[[level (Chern-Simons theory)|level]]_ of the Chern-Simons theory.
For $G$ semisimple this is the [[schreiber:∞-Chern-Simons theory]] induced from the canonical [[Chern-Simons element]] on a [[semisimple Lie algebra]] $\mathfrak{g}$.

For the special case that $G$ is a [[discrete group]] the theory reduces to the (much simpler) [[Dijkgraaf-Witten theory]].

The Chern-Simons TQFT was introduced in ([Witten 1989](#Witten)).



## Classical Chern-Simons theory 
 {#ClassicalChern-SimonsTheory}

The properties of the field configuration space of Chern-Simons
theory depends on the properties of its [[gauge group]] $G$. If $G$ is 
a [[simply connected topological space|simply connected]] [[Lie group]], then then configuration space is isomorphic simply to the space of [[Lie algebra valued 1-forms]] on the given base manifold. Generally, though, it is given by $G$-[[principal bundles]] with [[connection on a bundle|connection]]. We discuss the first case separately

1. [for simply connected gauge groups](#ClassicalForSimplyConnectedGaugeGroup)

1. [for general gauge groups](#ClassicalChern-SimonsTheoryGeneral)



### For simply connected gauge groups
 {#ClassicalForSimplyConnectedGaugeGroup}


For $G$ a [[simply connected]] [[Lie group]] 
we describe the basic setup of $G$-Chern-Simons theory

* [Lagrangian and action functional](#LagrangianAndActionFunctional)

* [Covariant phase space](#CovariantPhaseSpace)

#### The Lagrangian and action functional
 {#LagrangianAndActionFunctional}

Let $\mathfrak{g}$ be a [[semisimple Lie algebra]] and write $\langle -,-\rangle \in W(\mathfrak{g})$ for (some multiple of) its [[Killing form]] [[invariant polynomial]] (in the [[Weil algebra]] of $\mathfrak{g}$).

Notice that this is in [[transgression]] via a [[Chern-Simons element]] $cs \in W(\mathfrak{g})$ to (a multiple of) the canonical [[Lie algebra cohomology|Lie algebra]] 3-cocycle

$$
  \mu_3 = \langle -,[-,-]\rangle \in CE(\mathfrak{g})
$$

in the [[Chevalley-Eilenberg algebra]] of $\mathfrak{g}$.

For $\Sigma$ a [[compact space|compact]] [[smooth manifold]] of [[dimension]] 3, write

$$
  Conf_\Sigma := \Omega^1(\Sigma, \mathfrak{g})
   =
  \{
    \Omega^\bullet(\Sigma) \leftarrow W(\mathfrak{g}) : A
  \}
$$

for the [[groupoid of Lie algebra valued 1-forms]] on $\Sigma$, -- we call this the **field configuration space** of $\mathfrak{g}$-Chern-Simons theory over $\Sigma$.  Notice that this is canonically a [[smooth infinity-groupoid|smooth groupoid]], as discussed there. 

By means of the above [[Chern-Simons element]] 
$W(\mathfrak{g}) \leftarrow W(b^2 \mathbb{R}): cs$ there is naturally associated to every field configuration $A$ a 3-form 

$$
  cs(A) \in \Omega^3(\Sigma)
$$

called the [[Chern-Simons form]] of $A$. This 3-form is the [[Lagrangian]] of Chern-Simons theory over $\Sigma$.

+-- {: .num_defn #CSActionFunctional}
###### Definition

The exponentiated **[[action functional]]** of Chern-Simons theory is the morphism

$$
 \exp(i S(-))
  : 
  Conf_\Sigma \to U(1)
$$

to the [[circle group]], which sends a field configuration $A$ to the integral over $\Sigma$ of its Chern-Simons form $CS(A)$.

$$
  A  \mapsto \exp(i \int_\Sigma cs(A))
  \,.
$$

=--

#### The covariant phase space
 {#CovariantPhaseSpace}

Since the above [[action functional]] is a [[local action functional]], its [[covariant phase space]] -- which is the space of solutions of the corresponding [[Euler-Lagrange equation]]s -- naturally carries a [[presymplectic structure]]. 

+-- {: .num_prop}
###### Proposition

The [[Euler-Lagrange equation]]s for the action functional from def. \ref{CSActionFunctional} are

$$
  F_A = 0
  \,,
$$

where $F_A$ is the [[curvature]] 2-form of the [[groupoid of Lie algebra valued 1-forms|Lie algebra valued form]] $A$.

The [[presymplectic structure]] on the space of solutions relative to any 2-[[dimensional]] submanifold $\Sigma_0 \hookrightarrow \Sigma$ is

$$
  \omega(\delta A_1, \delta A_2) \propto
  \int_{\Sigma_0} \langle \delta A_1 \wedge \delta A_2 \rangle
  \,.
$$

=--

The proof can be found spelled out at [[schreiber:∞-Chern-Simons theory]].

The statements for equations of motion and gauge fixed Poisson structure appears for instance as ([Witten89, (2.3), (3,2)](#Witten)) or  ([FreedI, prop. 3.1, prop. 3.17](#FreedI)). The symplectic structure on the moduli space of flat connections is discussed in more detail also in ([Atiyah-Bott](#AtiyahBott)) and in ([Weinstein](#Weinstein)).

The [[presymplectic structure]] on the [[covariant phase space]] has apparently first been discussed in ([Witten86, section 5](#Witten86)) and in ([Zuckerman, section 3, example 2](#Zuckerman)).


Zuckerman states that on the reduced phase space of $GL(2,\mathbb{R})$-Chern-Simons theory the presymplectic form becomes the [[Weil-Petersson symplectic form]].


#### With Wilson line observables
 {#WithWilsonLineObservables}

More generally, configurations of Chern-Simons theory are defined on 3-dimensional manifolds $\Sigma$ with a [[closed manifold|closed]] 1-dimensional [[submanifold]] $\Sigma^{def} \hookrightarrow \Sigma$ where each connected component ([[diffeomorphism|diffeomorphic]] to a [[circle]]) is labeled by an [[irreducible representation|irreducible]] [[unitary representation]] $R_i$ of the [[gauge group]].

In the [[path integral]] formulation of Chern-Simons theory this means that to the integrand is added the [[Wilson loop]] $W(\Sigma^{def},R, A)$ of the principal connection around $\Sigma^def$ 

$$
  Z(\Sigma^{def}, \Sigma)
  \propto
  \int D A \;\; W(\Sigma^{def}, R, A) \exp(i S_{CS}(A))
  \,.
$$

But more fundamentally, the whole [[Wilson loop]] $W(\cdots)$ itself here is to be regarded as the result of a path integral for a [[1-dimensional Chern-Simons theory]] with moduli space a [[coadjoint orbit]] of $G$ and with the representation $R$ arising by the _[[orbit method]]_ (see there for more details).

This means that the [[configuration space]] of Chern-Simons theory over $(\Sigma^{def} \hookrightarrow \Sigma)$ is the space of $G$-[[principal connections]] on $\Sigma$ and of maps to the [[coadjoint orbit]] on $\Sigma^{def}$, with the [[action functional]] now being the sum of 3-dimensional Chern-Simons theory over $\Sigma$ as above and of a [[1-dimensional Chern-Simons theory]] along $\Sigma^{def}$ for which the $G$-principal connection serves as a [[background gauge field]].

This [[orbit method]]-formulation of Wilson loops in Chern-Simons theory was vaguely indicated in ([Witten89, p. 22 ](#Witten)). 
More details were discussed in ([EMSS 89](#EMSS)), but in the context of other [[gauge theories]] ([[Yang-Mills theory]]) the same formulation appears much earlier in ([Balachandran, Borchardt, Stern 78](#BBS)).
A detailed review and further refinements are discussed in section 4 of ([Beasley 09](#Beasley)).
Aspects of the formulation in the context of [[BV-BRST formalism]] are discussed in ([Alekseev-Barmaz-Mnev 12](#AlekseevBarmazMnev)). The formalizations via [[extended Lagrangians]] and [[extended prequantum field theory]] is in ([Fiorenza-Sati-Schreiber 12](#FiorenzaSatiSchreiber)). 


### For general gauge groups
 {#ClassicalChern-SimonsTheoryGeneral}

If the [[Lie group]] $G$ is not [[simply-connected]]
a $G$-[[principal bundle]] on 3-dimensional $\Sigma$
is not necessarily trivializable. (For instance for 
$G = U(1)$ the [[circle group]] the [[circle bundle]]s
on $\Sigma$ are classified by their [[Chern class]], which
can be any element in the [[integral cohomology]]
$H^2(\Sigma,\mathbb{Z})$.)

Therefore in these cases the [[configuration space]] of
Chern-Simons theory is no longer in general just a
[[groupoid of Lie algebra valued forms]] -- which is a [[groupoid]] of [[connection on a bundle|connections]] on trivial [[principal bundles]], but
a [[groupoid]] of more general [[connection on a bundle|connections]] on non-trivial [[principal bundle]]s.

The general formulation of Chern-Simons theory is then this:

let $G$ be a [[compact space|compact]] [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$ and let $\langle-,-\rangle$
be a binary [[invariant polynomial]]. Then the refined
[[Chern-Weil homomorphism]] produces a map

$$
  \hat \mathbf{c} : H^1(\Sigma,G)_{conn} \to 
  H^4(\Sigma)_{diff}
$$

from $G$-bundles with connection to degree-4 [[ordinary differential cohomology]] of $\Sigma$, classifying [[circle n-bundle with connection|circle 3-bundles with connection]] on $\Sigma$: the [[Chern-Simons circle 3-bundle]]s.

The [[action functional]] of Chern-Simons theory is the
[[higher holonomy]] of this circle 3-bundle

$$
  S_CS : \nabla \mapsto \int_\Sigma \hat \mathbf{c}(\nabla)
  \in U(1)
  \,.
$$

#### Abelian case

Let $G = U(1)$ the [[circle group]], and $\langle-,-\rangle$ the canonical [[invariant polynomial]]. 


Then the configuration space is $\mathbf{H}^2(\Sigma)_{diff}$ -- [[ordinary differential cohomology]] in degree 2 -- and the action functional is given by the [[fiber integration in ordinary differential cohomology]] over the [[Beilinson-Deligne cup product]]

$$
  S_{CS} : \hat A \mapsto \int_\Sigma \hat A \cup \hat A
  \,.
$$

(For the moment see [[higher dimensional Chern-Simons theory]] for references on this case.)

## Quantization

We discuss now aspects of the [[quantization]] of Chern-Simons theory. There are two main formalizations for making sense of this, _[[geometric quantization]]_ and _[[algebraic deformation quantization]]_. We discuss these separartely:

* _[Geometric quantization of Chern-Simons theory](#GeometricQuantization)_

* _[Perturbative BV deformation quantization of Chern-Simons theory](#PerurbativeBVDeformationQuantization)_


### Geometric quantization
 {#GeometricQuantization}

Of the existing formalizations of [[quantization]], it is _[[geometric quantization]]_ that is naturally suited for obtaining the [[spaces of states]] of Chern-Simons theory and their identification with the [[conformal blocks]] of the [[holographic principle|holographic dual]] [[WZW model]]. We indicate some aspects.

We discuss the [[space of states (in geometric quantization)]] of quantized $G$-Chern-Simons theory for $G$ a simple, simply connected Lie group, as [above](#ClassicalChern-SimonsTheory).


#### Geometric Prequantization

1. consider Chern-Simons theory on a [[dimension|3-dimensional]] [[smooth manifold]] which is a [[cylinder]] $\Sigma_3 \coloneqq \Sigma_2 \times [0,1]$ over a 2-dimensional manifold;

1. compute the [[covariant phase space]] over $\Sigma_3$ to be that of [[flat connections]] on $\Sigma$, equipped with a certain [[presymplectic form]] (as discussed [above](http://ncatlab.org/nlab/show/Chern-Simons%20theory#CovariantPhaseSpace));

1. after [[gauge reduction]] this becomes a [[symplectic form]], for which there is a [[prequantum circle bundle]] on the phase space;


#### Geometric quantization
 {#GeometricQuantizationQuantizationStep}

1. in order to complete this prequantization to [[geometric quantization]] one needs to choose a [[polarization]] of phase space; it turns out that one naturally obtains such from any choice of [[conformal structure]] $[g]$ on $\Sigma$ (see for instance [Witten-Jeffrey, p. 81](#WittenJeffrey), see also _[self-dual higher gauge theory -- Relation to Chern-Simons -- Conformal structure from polarization](self-dual+higher+gauge+theory#ConformalStructureFromPolarization)_):

   this is provided by the [[Narasimhan-Seshadri theorem]] which establishes that the [[moduli space of flat connections]] on a [[Riemann surface]] is naturally a [[complex manifold]]. This yields a [[Kähler polarization]] (as well as a [[spin^c-structure]] for [[geometric quantization by push-forward]] ([Freed-Hopkins-Teleman 07](#FreedHopkinsTeleman07))).

1. one finds that the resulting [[space of states (in geometric quantization)]] $H_{[g]}$ is naturally isomorphic to the space of [[conformal blocks]] of the 2-dimensional [[WZW model]] on $\Sigma$, regarded with that conformal structure.


So for a 2-dimensional [[manifold]] $\Sigma$, a choice of [[polarization]] of the [[phase space]] of 3d [[Chern-Simons theory]] on $\Sigma$ is naturally induced by a choice $J$ of [[conformal structure]] on $\Sigma$. Once such a choice is made, the resulting [[space of quantum states]] $\mathcal{H}_\Sigma^{(J)}$ of the Chern-Simons theory over $\Sigma$ is naturally identified with the space of [[conformal blocks]] of the [[WZW model]] [[2d CFT]] on the [[Riemann surface]] $(\Sigma, J)$. 

But since from the point of view of the 3d Chern-Simons theory the [[polarization]] $J$ is an arbitrary choice, the [[space of quantum states]] $\mathcal{H}_\Sigma^{(J)}$ should not depend on this choice, up to specified [[equivalence]]. Formally this means that as $J$ varies (over the [[moduli space of conformal structures]] on $\Sigma$) the $\mathcal{H}_{\Sigma}^{(J)}$ should form a [[vector bundle]] on this [[moduli space of conformal structures]] which is equipped with a [[flat connection]] whose [[parallel transport]] hence provides equivalences between between the [[fibers]] $\mathcal{H}_{\Sigma}^{(J)}$ of this vector bundle. 

This flat connection is the _[[Knizhnik-Zamolodchikov connection]]_ / _[[Hitchin connection]]_. This was maybe first realized and explained in ([Witten 89, p. 20](#Witten)) and first actually constructed in ([Axelrod-Pietra-Witten 91](#AxelrodPietraWitten91)).


For more see the references [below](http://ncatlab.org/nlab/show/Chern-Simons+theory#ReferencesGeometricQuantization).

#### Extended / in higher codimension
  {#GeometricQuantHigher}

We discuss aspects of Chern-Simons theory in 
[[extended prequantum field theory]]. For more on this
see at _[[schreiber:Higher Chern-Simons local prequantum field theory]]_.

Let $G$ be a [[simply connected topological space|simply connected]] [[Lie group]], such as the [[spin group]].

Write $\mathbf{B}G \in \mathbf{H}$ for the [[smooth infinity-groupoid|smooth]] [[moduli stack]] of $G$-[[principal bundles]] (as discussed [here](smooth+infinity-groupoid+--+structures#LieGroups)) and write $\mathbf{B}G_{conn} \in \mathbf{H}$ for that of $G$-[[connection on a bundle|principal bundles with connection]]. (Here $\mathbf{H} = $ [[Smooth∞Grpd]] is the [[(∞,1)-topos]] for smooth [[higher geometry]].) Similarly, for $n \in \mathbb{N}$ write $\mathbf{B}^n U(1)_{conn}$ for the [[smooth infinity-groupoid|smooth]] [[moduli infinity-stack|moduli n-stack]] of [[circle n-bundles with connection]]. 

In contrast, write $B G \in $ [[Top]] for the ordinary [[classifying space]] of $G$-principal bundles, the [[geometric realization of simplicial topological spaces|geometric realization]] of $\mathbf{B}G$.

By the discussion at [[Lie group cohomology]] we have 

$$
  H^4(B G, \mathbb{Z}) \simeq \mathbb{Z} \simeq 
  \pi_0 \mathbf{H}^3(\mathbf{B}G, U(1))
  \,.
$$

Write 

$$
  \mathbf{c} : \mathbf{B}G \to \mathbf{B}^3 U(1)
$$

for a morphism in $\mathbf{H}$ representing this class. This modulates the [[circle n-group|cicle 3-group]]=$\mathbf{B}^2 U(1)$-[[principal ∞-bundle]] over $\mathbf{B}G$

$$
  \array{
    P 
    \\
    \downarrow
    \\
    \mathbf{B}G &\stackrel{\mathbf{c}}{\to}& \mathbf{B}^3 U(1)
  }
$$

sometimes called the [[Chern-Simons circle 3-bundle]].

By the discussion at _[[differential String structure]]_ ([FSS](#FiorenzaSchreiberStasheff)) this map has a differential refinement to a morphism of smooth moduli stacks of the form:

$$
  \mathbf{c}_{conn} : \mathbf{B}G_{conn} \to \mathbf{B}^3 U(1)_{conn}
  \,.
$$

Let then $\Sigma_k$ be a compact closed [[orientation|oriented]] [[smooth manifold]] of [[dimension]] $0 \leq k \leq 3$. We can form the [internal hom](%28infinity,1%29-topos#ClosedMonoidalStructure) (mapping $\infty$-stack) $[\Sigma_k,-]$ and produce the morphism

$$
  [\Sigma_k, \mathbf{c}_{conn}]
  : 
  [\Sigma_k, \mathbf{B}G_{conn}]
  \to
  [\Sigma_k, \mathbf{B}^3 U(1)_{conn}]
  \,.
$$

This in turn we may postcompose with the operation of [[fiber integration in ordinary differential cohomology]], refined to a morphism of [[smooth ∞-groupoids]]

$$
  \exp(2 \pi i \int_{\Sigma_k}(-)) : [\Sigma_k, \mathbf{B}^n U(1)_{conn}] \to \mathbf{B}^{n-k}U(1)_{conn}
  \,.
$$

The result is a morphism

$$
  \exp(2 \pi i \int_{\Sigma_k} [\Sigma_k, (-)])
  : 
  [\Sigma_k, \mathbf{B}G_{conn}]
   \stackrel{[\Sigma_k, \mathbf{c}_{conn}]}{\to}
  [\Sigma_k, \mathbf{B}^3 U(1)_{conn}]
    \stackrel{\exp(2 \pi i \int_{\Sigma_k}(-))}{\to}
  \mathbf{B}^{3-k} U(1)_{conn}
  \,.
$$

The result is a [[circle n-bundle with connection|circle (3-k)-bundle with connection]] over the smooth moduli stack of Chern-Simons fields on $\Sigma_k$.  We explain now how, as $k$-varies, there [[transgression|transgressions]] of the differential characteristic map $\mathbf{c}_{conn}$ constitute [[prequantum circle n-bundle|prequantum circle (3-k)-bundles]] for an [[higher geometric quantization]] of Chern-Simons theory, as indicated in the following table.


| [[codimension]] $k= $ |  |  [[prequantum circle n-bundle|prequantum circle (3-k)-bundle]]
|--|--|--|
| 3 | [[differential string structure|differentially refined]] [[first fractional Pontryagin class]] ([[level (Chern-Simons theory)]]) | $\mathbf{c} : \mathbf{B}G_{conn} \to \mathbf{B}^3 U(1)_{conn}$ |
| 2 | [[Wess-Zumino-Witten model]] background [[B-field]] | $G \stackrel{\bar \nabla_{can}}{\to} [S^1, \mathbf{B}G_{conn}] \stackrel{[S^1, \mathbf{c}_{conn}]}{\to} [S^1, \mathbf{B}^3 U(1)_{conn}] \stackrel{\exp(2 \pi i \int_{S^2}(-))}{\to} \mathbf{B}^2 U(1)_{conn} $ |
| 1 | ordinary [[prequantum circle bundle]] of Chern-Simons theory | $[\Sigma_2, \flat\mathbf{B}G] \to [\Sigma_2, \mathbf{B}G_{conn}] \stackrel{[\Sigma_2, \mathbf{c}_{conn}]}{\to} [\Sigma_2, \mathbf{B}^3 U(1)_{conn}] \stackrel{\exp(2 \pi i \int_{\Sigma_2}(-)}{\to}  \mathbf{B} U(1)_{conn}$ |
| 0 | [[action functional]] of Chern-Simons theory | $[\Sigma_3, \mathbf{B}G_{conn}] \stackrel{[\Sigma_3, \mathbf{c}_{conn}]}{\to} [\Sigma_3, \mathbf{B}^3 U(1)_{conn}] \stackrel{\exp(2 \pi i \int_{\Sigma_3}(-))}{\to} U(1)$ |

The first line we have already discussed ([FSS](#FiorenzaSchreiberStasheff)). 
The second line is implicit in ([CJMSW, def. 3.3, prop. 3.4](#CJMSW)). There it is shown that there is a natural $G$-[[principal connection]] on $S^1 \times$, such that the [[fiber integration in ordinary differential cohomology]] of its [[Chern-Simons circle 3-bundle|Chern-Simons circle 3-bundle with connection]] $\nabla_{con}$ over $S^1$ is the [[Wess-Zumino-Witten model]] [[circle n-bundle with connection|circle n-bundle with connection]] on $G$. But in terms of moduli stacks this means that there is a canonical morphism

$$
  \nabla_{can} : G \times S^1 \to \mathbf{B}G_{conn}
$$

such that its [[internal hom]]-[[adjunct]]

$$
  \bar \nabla_{conn} : G \to [S^1 , \mathbf{B}G_{conn}]
$$

has the property that postcomposition with $\exp(2 \pi i \int_{S^1}[S^1, \mathbf{c}_{conn}])$ modulates the WZW 2-bundle. This is precisely the content of the second line in the table above.


### Perturbative quantization
 {#PerturbativeQuantization}

Some pointers regarded the [[perturbative quantum field theory|perturbative]] [[quantization]] of Chern-Simons theory:

#### Feynman perturbation series
 {#FeynmanPerturbationSeries}

The standard [[Feynman perturbation series]] for [[perturbative quantum field theory]] based on the [[Chern-Simons propagator]] (see there for more) was discussed in [Axelrod-Singer 91, 93](#AxelrodSinger), via [[Feynman amplitudes on compactified configuration spaces of points]].

This led [Kontsevich 94](#Kontsevich) to suggest that the perturbative Chern-Simons [[Feynman amplitudes]] serves to exhibit a [[graph complex]]-model for the [[Fulton-MacPherson compactification]] of [[configuration spaces of points]] and for the [[spaces of knots]].

For the first case this was proven in[Lambrechts-Volic 14](#LambrechtsVolic14).

For the second case see [CattaneoCottaRamusinoLongoni02](graph+complex#CattaneoCottaRamusinoLongoni02), [Volić 13](graph+complex#Volic13) and [Bar-Natan 91](#BarNatan91).

Review:

* [[Robbert Dijkgraaf]], _Perturbative topological field theory_, In: *Trieste 1993, Proceedings, String theory, gauge theory and quantum gravity '93* 189-227 ([spire:399223](http://inspirehep.net/record/399223/), [[DijkgraafPerturbativeCS93.pdf:file]])



#### Path integral quantization
 {#PerturbativePathIntegralQuantization}

[Witten (1989), section 2](#Witten) indicates the [[perturbation theory|perturbative]] [[path integral quantization]] of Chern-Simons theory and finds that the result after [[gauge fixing]] by a choice of [[Riemannian metric]] $g$ is the sum over equivalence classes of classical solutions, i.e. of [[flat connections]]/[[local systems]] $\nabla_{fl}$,  of the product of 

1. the exponentiated Chern-Simons action functional $\exp(i k \, S_{CS}(\nabla))$ of the classical solution;

1. the [[analytic torsion]] $T(g,\nabla_{fl})$;

1. the exponentiated [[eta invariant]] $\exp(\pi i\, \eta(\nabla_{fl}))$ ([hence](eta+invariant#OnOddDimensionalManifolds) the [[Selberg zeta function]] twisted by the given [[local system]] $\nabla_{fl}$).

$$
  \underset{}{\int} \exp(i k \, S_{CS}(\nabla)) (D\nabla)
    \;\stackrel{k \to  \infty}{\longrightarrow}\;
  \underset{[\nabla_{fl}]}{\sum}
     \exp\left(i k S_{CS}\left(\nabla_{fl}\right)\right) 
     \exp\left(i \pi \eta\left(\nabla_{fl}\right) \right)
     T\left(g,\nabla_{fl}\right)
  \,.
$$

([Witten 89 (2.17)](#Witten))

For more on this see at _[eta invariant -- Boundaries, determinant line bundles and perturbative Chern-Simons](eta+invariant#OnManifoldsWithBoundary)_.


Now this expression is not independent of the chosen metric $g$. But it becomes indepdendent of it after adding the $SO$-Chern-Simons term of the [[Levi-Civita connection]] of the metric ([Witten 89 (2.23)](#Witten)) (and is then well-defined after choosing an [[Atiyah 2-framing]]).

Notice that here $i k$ is $\tfrac{i}{\hbar}$,so that the [[limit of a sequence|limit]] $k \to \infty$ is the [[semiclassical limit]], i.e. this is perturbation theory in [[Planck's constant]] $\hbar$, as also considered in perturbative [[deformation quantization]].


#### BV deformation quantization
 {#PerurbativeBVDeformationQuantization}

We discuss the [[perturbation theory|perturbative]] [[deformation quantization]] of Chern-Simons theory to a [[factorization algebra of local observables]] along the lines of _[renormalization -- Of theories in BV-CS forms](renormalization#OfTheoriesInBVForm)_ ([Costello](#Costello)).

We first discuss the classical and quantum [[BV-BRST complex]] of the underlying [[free field theory]]

* _[The BV-BRST complex of the underlying free field theory](#TheBVBRSTComplexOfTheUnderlyingFreeFieldTheory)_

and then perturbatively introduce the [[interactions]] by  [[renormalization|renormalizing]] and solving the [[quantum master equation]]:

* _[The renormalized quantum master equation](#TheRenormalizedQuantumMasterEquation)_.

##### The BV-BRST complex of the underlying free field theory
 {#TheBVBRSTComplexOfTheUnderlyingFreeFieldTheory}

Fix $(\mathfrak{g}, \langle -,-\rangle_{\mathfrak{g}})$ a [[Lie algebra]] equipped with a binary and non-degenerate [[invariant polynomial]] (for instance a [[semisimple Lie algebra]] with [[Killing form]]).
Let $\Sigma$ be a [[smooth manifold|smooth]] [[closed manifold]]. 

In [[perturbation theory]] we consider only [[infinitesimal object|infinitesimal]] [[gauge transformations]] between the [[field (physics)|fields]],

In [[perturbation theory]] we regard the [[interaction term]] 

$$
  A \mapsto I(A) \propto \int_\Sigma \langle A \wedge [A \wedge A]\rangle
$$

as a perturbation of the [[free field theory]] with [[kinetic action functional]]

$$
  A \mapsto S_{kin}(A) \propto \int_\Sigma \langle A \wedge d A\rangle
  \,.
$$

The [[BRST complex]] of the full theory is the [[Chevalley-Eilenberg algebra]] $CE(Lie(G\mathbf{Conn}(X)//C^\infty(X,G)))$ of the [[Lie algebroid]] $Lie(\Omega^1_\Sigma(-,\mathfrak{g})//[X,G]$ which is the [[Lie differentiation]] of the [[action groupoid]] of the [[smooth group]] of [[gauge transformations]] acting on the fields, which are the [[Lie algebra valued 1-forms]].

So the [[BRST complex]] of Chern-Simons theory has 

* [[field (physics)|fields]] the 1-forms $\Omega^1(\Sigma, \mathfrak{g})$ 

* and as [[ghosts]] the $\Omega^0(\Sigma, \mathfrak{g})$. 

The corresponding [[BV-BRST complex]] hence has in addition

* [[antifields]] the local duals of the fields, which under the evident [[wedge product]]-and-[[integration of differential forms|integration]] pairing is $\Omega^2(\Sigma, \mathfrak{g})$;

* [[antighosts]] similarly $\Omega^3(\Sigma, \mathfrak{g})$.

In summary the fields, ghosts, antifields and antighists form the [[de Rham complex]] of $\Sigma$ [[tensor product|tensored]] with $\mathfrak{g}$: As a [[free field theory]] (with the notation as dicussed there) Chern-Simons theory on $\Sigma$ has the sheaf of [[sections]] of the [[field bundle]] given by

$$
  \mathcal{E}
  =
  \Omega^\bullet_\Sigma(-, \mathfrak{g})
  \,.
$$

Here we should regard $\mathfrak{g}$ as being [[graded vector space|graded]] and homogeneously of degree $(-1)$ (this is the natural grading on $\mathfrak{g}$ regarded as an [[L-infinity algebra]]. In fact essentially all of the discussion here goes through for general $L_\infty$-algebras equipped with a binary [[invariant polynomial]]). With this the evident total grading on $\Omega^\bullet_\Sigma(-,\mathfrak{g})$ is already the correct BV-BRST grading

| [[field (physics)|field]]: | [[ghost fields]] | genuine [[field (physics)|fields]] | [[antifields]]  |  [[antighost fields]] |
|--| -----------------|----------------------------|-----------------|-----------------------|
| $\phi \in$ | $\Omega_\Sigma^0(-,\mathfrak{g})$ | $\Omega_\Sigma^1(-,\mathfrak{g})$ | $\Omega_\Sigma^2(-,\mathfrak{g})$ | $\Omega_\Sigma^3(-,\mathfrak{g})$ |
| degree | -1 | 0 | 1 | 2 | 

The [[antibracket]] is given by the canonical local pairing obtained by taking the [[wedge product]] of [[differential forms]], then evaluating the [[coefficients]] in $\mathfrak{g} \otimes \mathfrak{g}$ in the [[invariant polynomial]] $\langle-,-\rangle_{\mathfrak{g}}$, then projecting onto the 3-form summand and finally forming the [[integration of differential forms]] over $\Sigma$: for $\phi_1, \phi_2 \in \Omega^\bullet(-,\mathfrak{g})$ we have

$$
  \{\phi_1, \phi_2\}
  = 
  \int_\Sigma \langle \phi_1 \wedge \phi_2\rangle_{\mathfrak{g}}
  \,.
$$

In [[perturbation theory]] we take the [[observables]] to be [[polynomial]] [[linear functions]] on these fields, hence the (graded-)[[symmetric algebra]] $Sym \overline{\mathcal{E}}$ of the [[distributions]] $\overline{\mathcal{E}}$. By the [Atiyah-Bott lemma](elliptic+chain+complex#AtiyahBottLemma) we may in the present situation take the observables equivalently to be the [[compact support|compactly supported]] sections of the dual field bundle, with duality induced by the local pairing $\mathcal{E}_c \otimes \mathcal{E}_c \to Dens_\Sigma$. For instance a monomial local linear function on the genuine fields 

$$
  f \colon \Omega^0(\Sigma,\mathfrak{g}) \to \mathbb{R}
$$

is then presented by an element $\bar f \in \Omega^3(\Sigma,\mathfrak{g})$ via the evaluation map:

$$
  f \;\colon\; \phi \mapsto \int_\Sigma \bar f \wedge \phi
  \,.
$$

With this identification we have in summary the following situation:

| linear local [[observables]]: | [[ghost field]] observables | genuine [[field (physics)|field]] observables | [[antifield]] observables  |  [[antighost field]] observables |
|--| -----------------|----------------------------|-----------------|-----------------------|
| $f \in$ | $\Omega_{cp}^3(\Sigma,\mathfrak{g})$ | $\Omega^2_{cp}(\Sigma,\mathfrak{g})$ | $\Omega_{cp}^1(\Sigma,\mathfrak{g})$ | $\Omega_{cp}^0(\Sigma,\mathfrak{g})$ |
| degree | 1 | 0 | -1 | -2 | 

The [[de Rham differential]] on the sections $\mathcal{E}$ of the [[field bundle]] induces a differential on the observables by dualization.

Hence the [[classical BV-complex]] of the [[free field theory]] is

$$
  Obs^{cl}_{free}
  = 
  \left(
    Sym (\Omega^\bullet_{cp}(\Sigma, \mathfrak{g})), Q = (d_{dR})^\ast, \langle -,-\rangle^\ast = \int_\Sigma (-) \wedge (-)
  \right)
  \,.
$$

Equipped with the standard [[BV-Laplacian]] $\Delta$ discussed at _[free field theory - The quantum observables](free+field+theory#TheQuantumObservables)_ this yields the corrsponding [[quantum BV-complex]] of the [[free field theory]]

$$
  Obs^{q}_{free}
  = 
  \left(
    Sym (\Omega_{cp}^\bullet(\Sigma, \mathfrak{g})[ [\hbar] ], Q = (d_{dR})^\ast + \hbar \Delta, \langle -,-\rangle^\ast = \int_\Sigma (-) \wedge (-)
  \right)
  \,.
$$

##### The renormalized quantum master equation
 {#TheRenormalizedQuantumMasterEquation}

Next we want to add to the above free field theory the [[interaction]] term $I$.
This amounts to changing the [[differential]] $Q + \hbar \Delta$ of $Obs^q_{free}$
to $Q + \{I,-\} + \hbar \Delta$. For this indeed to still be a differential it
must still square to 0, which is the condition expressed by the [[quantum master equation]],
This needs [[renormalization]] in order to be well defined.

This is discussed for instance in ([Costello, section 15](#Costello)).

(...)

## Quantum Chern-Simons theory

### The Reshetikhin-Turaev construction and its equivalence to geometric quantization
 {#RTConstructionAndEquivalenceToGeometricQuantization}

The [[Reshetikhin-Turaev model]] of [[3d TQFT]] had 
traditionally been expected to be quantized Chern-Simons theory.
A proof if this requires showing that the RT-constuction is 
equivalent to the result of the [[geometric quantization]]
from [above](#GeometricQuantization).

The proof of this is not entirely spelled out in the literature, 
but all the ingredients seem to be known, involving 
results such as ([Andersen 12](#Andersen12)).

For more see at _[[quantization of Chern-Simons theory]]_.

See also the MathOverflow-discussion _[Why hasn't anyone proved that the two standard approaches to quantizing Chern-Simons theory are equivalent?](http://mathoverflow.net/questions/86792/why-hasnt-anyone-proved-that-the-two-standard-approaches-to-quantizing-chern-si)_.



### Observables: knot polynomials

The [[Wilson line]]-[[observable]]s in quantum Chern-Simons theory are
given by [[knot invariant]]s.

In [Witten (1989)](#Witten) it was shown  that the new [[knot invariant|polynomial invariant]] of [[knot]]s invented by [[Vaughan Jones]] in the context of [[von Neumann algebra]]s --  the [[Jones polynomial]] -- can be given a heuristic geometric interpretation: the [[Jones polynomial]] V(q) of a [[knot]] $K$ in a 3-manifold $M$ can be viewed as the [[path integral]] over all $SU(2)$-connections on $M$ of the exponential of the [[Chern-Simons form|Chern?Simons]] [[action functional]] $S[A]$:
\[
 V_K(q) = \int_{all\,connections\,A\,on\,M} hol_A(K) \,\, exp(iS[A])
\]
where
\[
S[A] = \frac{k}{4\pi} \int_M Tr (A \wedge dA + \frac{2}{3} A \wedge A \wedge A)
\]
is the integral of the [[Chern-Simons form|Chern?Simons Lagrangian]], 
\[
 Tr Hol_A (K) 
\]
is the trace of the holonomy of the connection around the knot $K$ in the [[fundamental representation]] of $SU(2)$, and  
\[
q = e^{\frac{2 \pi i}{k+2}}.
\]
Said heuristically: the [[Jones polynomial]] of the knot $K$ can be understood as the "average value" over all connections of the _trace of the holonomy of the connection_ around the knot $K$. Note that this idea can be generalized by varying the gauge group $G$ from $SU(2)$ to some other Lie group; the representation in which the trace is evaluated can also be altered. Each of these modifications gives rise to a [[knot invariant]].  



### As an extended TQFT

The beautiful thing about Chern--Simons theory is that Witten was able use the _locality_ property of the [[path integral]] to give a _nonperturbative_ way to actually compute it. In this way Chern--Simons theory has become the 'poster-child' of [[extended topological quantum field theory]] since it exemplifies the main idea: take advantage of the higher gluing laws in order to compute geometric quantities. 

One of the major mathematical projects around Chern--Simons theory has therefore been to try and understand it rigorously as a 3-2-1-0 [[extended topological quantum field theory]]. 

For the abelian case the major paper in this regard is _[[Topological Quantum Field Theories from Compact Lie Groups]]_ by [[Dan Freed|Freed]], [[Mike Hopkins|Hopkins]], [[Jacob Lurie|Lurie]] and [[Constantin Teleman|Teleman]]. No-one has yet made rigorous sense of the nonabelian theory as an extended [[TQFT]]. However, the invariants that the theory assigns to closed [[manifolds]] of dimension 0,1,2 and 3 are heuristically expected to be:

Proposals by other authors include ([Henriques 15](#Henriques15)).


A closed 3-manifold $M$ $\mapsto$ the path integral given above (a number).

A closed 2-manifold $\Sigma$ $\mapsto$ the space of sections of the line bundle over the moduli space of flat [[connection on a bundle|connection]]s on $\Sigma$ (a finite-dimensional [[vector space]]).  (Reshetikhin and Turaev give an alternate quantum-groupy description of this space).

A circle $S^1$ $\mapsto$ the [[category]] of [[positive energy representation]]s of the [[loop group]] $\Omega_k (G)$ at level $k$ (a [[linear category]]).

+-- {: .query}
The R-T construction sticks on the circle the [[modular tensor category]] of representations of a [[quantum group]] at a root of unity, modulo "unphysical representations."  Are these supposed to be the same?  Is this just the Kazhdan-Lusztig equivalence?

[[Urs Schreiber]]: the [[Reshetikhin-Turaev construction]] works with any [[modular tensor category]], I'd say. Using one coming from reps of loops group is expected to produce the Chern--Simons QFT as a cobordism rep. But I think a full proof of that, i.e. a formalization of the CS path integral that would after turning the crank yield the RT construction, is not available to date. There is just lots of "circumstancial evidence".

=--

The 2-category assigned to the point is the most interesting piece of data since in principle all the other invariants can be derived from it using the gluing law. In the paper _[[Topological Quantum Field Theories from Compact Lie Groups]]_, it is proposed that

A point $\mapsto$ the category of skyscraper sheaves on ---, thought of as a 2-category via ---.

+-- {: .query}
Bruce: I've run out of time here and I can't precisely fill in those blanks above.  Any help?

[[Ben Webster]]: My understanding is that nobody is quite sure how to fill in those blanks.  One line of thinking is that it should be an object in a 3-category with is **not** 2Cat.
=--

Other groups have conceptualized this differently (but most likely equivalently at the end of the day as)

A point $\mapsto$ the 2-category of unitary [[2-representation]]s of the [[group]] $G$.

Still others think of the [[2-category]] assigned to the [[point]] in different terms.

## Properties

### Tunneling between vacua -- instanton Floer homology

For $g$ a fixed [[Riemannian metric]] on the 3-dimensional base space $\Sigma$, the [[gradient flow]] of the Chern-Simons theory [[action functional]] $S_{CS} : \Omega^1(\Sigma,\mathfrak{g}) \to \mathbb{R}$ with respect to the respective [[Hodge inner product]] [[metric]] on $\Omega^1(\Sigma,\mathfrak{g})$ characterizes [[Yang-Mills instanton]] solutions of the [[Yang-Mills theory]] on $\Sigma \times \mathbb{R}$ with metric $g \otimes I$. 

This phenomenon is captured by [[instanton Floer homology]].

### As an effective background for topological string theory

In ([Witten94](#Witten94)) an argument was given that Chern-Simons theory can be understood as the effective target space [[string theory]] of the [[A-model]] or [[B-model]] [[TCFT]]. This argument has later been made more precise in the language of [[TCFT]]. See [TCFT -- Effective background theories](TCFT#ActionFunctionals) for more on this.

### As 3-dimensional gravity

The Chern-Simons action functional for the case that the gauge group is the [[Poincare group]] $Iso(2,1)$ (and the [[invariant polynomial]] is taken to be the one that pairs a translation generator with a rotation generator) happens to be equivalent to the [[Einstein-Hilbert action]] in the [[first order formulation of gravity]] in 3-dimensions. 

Moreover, Chern-Simons theory for the groups $Iso(2,2)$ and $Iso(3,1)$ is similarly equivalent to [[gravity]] with [[cosmological constant]] in 3-dimensions.

Since the [[quantization]] of Chern-Simons theory is fairly well understood, these identifications imply indeed a definition of [[quantum gravity]] in 3-dimensions. 

More on this is at [[Chern-Simons gravity]].

Beware that there is a subtlety in the definition of the [[configuration space]]: when the field of gravity is identified with an $Iso(2,1)$-[[connection on a bundle|connection]] then the configuration space naturally contains degenerate [[vielbein]] fields $E$ (notably the 0 vielbein) and hence the induced rank-2 [[tensor]] $g = \langle E \otimes E\rangle$ may also be degenerate. Such degenerate tensors are not technically [[pseudo-Riemannian metric]] tensors, since these are required to be non-degenerate. The genuine non-degenerate metric tensors correspond to precisely those $Iso(2,1)$-[[principal connection]]s which are in fact $(O(2,1) \hookrightarrow Iso(2,1))$-[[Cartan connection]]s.

However, the quantum theory exists nicely if one allows the larger configuration space of possibly degenerate metrics exists nicely, while the constrained one does not. This may be interpreted as saying that at least for purposes of [[quantum gravity]] it is wrong require non-degenerate metric tensors.


### Holographic relation to 2d Wess-Zumino-Witten model

See at _[[AdS3-CFT2 and CS-WZW correspondence]]_.

### Chern--Simons theory and modular forms

Trying to interest your [[number theory]] friends with Chern--Simons theory? How about this: the Chern--Simons [[path integral]] $Z(k)$ above is (in a certain precise sense) a _[[modular form]]_. This correspondence between the Chern--Simons quantum invariants and [[modular form]]s sheds light in both directions, and is a fascinating idea to [[Bruce Bartlett|me]]. The key words here (which I don't understand) are "Eichler integral" and  "[[mock theta function]]". See:

* Lawrence and Zagier, Modular forms and quantum invariants of 3-manifolds, Asian Journal of Mathematics vol 3 no 1 (1999).

* Hikami, Quantum invariant, modular forms, and lattice points, [arXiv](http://arxiv.org/abs/math-ph/0409016). See also the follow ups to this paper. 

### The Morse theory of Chern--Simons theory

In a recent [talk](http://www.math.columbia.edu/~woit/wordpress/?p=2357), Witten outlined a new approach to Chern--Simons theory which perhaps gives an alternative nonperturbative definition of the [[path integral]]. Quoting from [Not Even Wrong](http://www.math.columbia.edu/~woit/wordpress/?p=2357):

> The main new idea that Witten was using was that the contributions of different critical points p (including complex ones), could be calculated by choosing   appropriate contours $\mathcal{C}_p$ using [[Morse theory]] for the Chern--Simons functional. This sort of Morse theory involving holomorphic Morse functions gets used in mathematics in [[Picard-Lefshetz theory]]. The contour is given by the downward flow from the critical point, and the flow equation turns out to be a variant of the self-duality equation that Witten had previously encountered in his work with Kapustin on [[geometric Langlands]]. One tricky aspect of all this is that the contours one needs to integrate over are sums of the $\mathcal{C}_p$ with integral coefficients and these coefficients jump at "Stokes curves" as one varies the parameter in one's integral (in this case, $x=k/n$, $k$ and $n$ are large). In his talk, Witten showed the answer that he gets for the case of the figure-eight knot.

For slides of Witten's talk, click [here](http://www.princeton.edu/~tklose/adscft/EdwardWittenPCTS.pdf) and for video, click [here](http://echo360.princeton.edu:8080/ess/echo/presentation/2730cd4e-39b0-4d97-a825-165e7d4b819f). Pilfering material from the slides, the basic idea is as follows. Consider a general oscillatory integral in $n$ dimensions:
 \[
 I(\lambda) = \int_{\mathbb{R}^n} d^n exp(i\lambda f(x_1, \ldots, x_n)).
\]
We want to make sense of the integral when the function $f$ is allowed to take on imaginary values (naively, the integral diverges). To do this, we use Morse theory: we choose as our Morse function the real part of the exponent, that is $h = \Re(i \lambda f)$. For every critical point $p$ of $h$, the descending manifold $C_p$ is an $n$-cycle in the relative homology group $H_n (X, X_{\ll0})$. (Basically this means that it's a new "contour" for the integral). Moreover Morse theory tells us that the cycles we obtain in this way form a basis for the homology, so we can express our original cycle $C$ (the $\mathbb{R}^n$ appearing in the integral over $\mathbb{R}^n$) as a linear combination of these Morse theory cycles:
 \[
 C = \sum_p n_p C_p
\]
In this way we can make sense of the integral $I$ by {\em defining} it as the integral over these new cycles ("contours"): 
\[
 I(\lambda)  = \sum_{\text{crit. points} p} n_p I_p(\lambda)
\]
This new definition actually converges, and makes sense. Apparantly the same technique can be used to interpret the Chern--Simons path integral in the case of complex $k$. Witten argues that this viewpoint is useful if we try to interpret Chern--Simons theory as a theory of three-dimensional gravity, 

### Traces as a path integral?
 {#TraceAsAPathIntegral}

In ([Witten 89](#Witten)) is the observation that the "[[trace]]" occuring in the "trace of the [[holonomy]] around the knot" term in the path integral should _itself_ be seen as a [[path integral]]. In this way one hopes to obtain a much more unified formalism. The quote is reproduced at  _[[Bruce Bartlett:Geometric quantization and the path integral in Chern-Simons theory]]_. 

For technical details on this see at _[[orbit method]]_.

### Higher dimensional generalizations
 {#HigherDimensionalGeneralization}

One question that's been bugging me (Ben Webster) recently is what fills in the analogy "[[Jones polynomial]] is to Chern--Simons theory as [[Khovanov homology]] is to ??" 

(Urs: Answer now at [[Khovanov homology]].)

Which is to say _What 3/4-dimensional structure is Khovanov homology hinting at?_  I'm inclined to think there must be one, as it seems that all of the knot homologies associated by Chern--Simons theory to representations have categorifications (I have a [mostly finished paper](http://math.mit.edu/~bwebster/KI-HRT.pdf) on this).  Presumably these all glue together into something, possibly by a similar trick to the Reshetikhin-Turaev construction of 3-manifold invariants, but it's not so easy for me to see how.

### Realization in physical systems

Chern-Simons theory has mostly been studied as a test case example for ([[prequantum field theory|pre]]-)[[quantum field theories]] in theoretical physics and mathematics. Also in [[string theory]] it appears in various incarnations and governs the hypothetical physics of [[string]], notably through its [[holographic principle|holographic]] relation to the [[WZW model]] and the higher dimensional generalizations of this.

But there are also [[physical systems]] that one can set up in a laboratory experiment which are described by at least some aspects of Chern-Simons theory at least in some limit. The most prominent such example is the _[[quantum Hall effect]]_ system in [[solid state physics]], which consists of [[electrons]] constrained to an effectively 2-dimensional [[surface]] and subject to perpendicular [[magnetic field]]. This system and its variant are also being proposed as supporting [[topological quantum computing]]. 


## Related concepts

* [[level (Chern-Simons theory)]]

* [[quantization of Chern-Simons theory]]

* [[Spin Chern-Simons theory]]

* [[schreiber:∞-Chern-Simons theory]]

* [[higher dimensional Chern-Simons theory]]

  * [[1d Chern-Simons theory]]

  * [[3d Chern-Simons theory]]

  * [[4d Chern-Simons theory]]

  * [[5d Chern-Simons theory]]

  * [[7d Chern-Simons theory]]

  * [[AKSZ sigma-models]]

  * [[string field theory]]

  * [[infinite-dimensional Chern-Simons theory]]

* [[super Chern-Simons theory]]

* [[holomorphic Chern-Simons theory]]

  * [[semi-holomorphic 4d Chern-Simons theory]]

* [[Chern-Simons theory with complex gauge group]]

* [[analytically continued Chern-Simons theory]]

* [[Rozansky-Witten theory]]

* [[sigma-model]]

  * [[AKSZ sigma-model]]

    * [[Poisson sigma-model]]

      * [[A-model]], [[B-model]]

    * [[Courant sigma-model]]

      * **Chern-Simons theory**

        * [[ABJM theory]]

* [[arithmetic Chern-Simons theory]]





## References  
 {#References}

### General
 {#ReferencesGeneral}

The local Chern-Simons term as an action functional for quantum field theory appears perhaps first in section III of

* [[Stanley Deser]], [[Roman Jackiw]], S. Templeton, _Topologically Massive Gauge Theories_, Annals Phys. 140 (1982) 372-411 ([pdf](http://www.imamu.edu.sa/Scientific_selections/abstracts/Physics/Topologically%20Massive%20Gauge%20Theories.pdf))


The [[geometric quantization]] and [[path integral]] [[quantization]] of Chern-Simons theory and the relation of its [[Wilson line]] [[observables]] to the [[Jones polynomial]] was introduced in

* {#Witten} [[Edward Witten]], _Quantum Field Theory and the Jones Polynomial_ Commun. Math. Phys. 121 (3) (1989) 351&#8211;399. MR0990772 ([euclid:cmp/1104178138](http://projecteuclid.org/euclid.cmp/1104178138))
 
and also, indepndently at the same time

* [[Jürg Fröhlich]], C. King, _The Chern-Simons theory and knot polynomials_, Comm. Math. Phys. Volume 126, Number 1 (1989), 167-199 ([project euclid](https://projecteuclid.org/euclid.cmp/1104179728))

It derives its name from the [[Chern-Simons forms]] that were originally introduced in 

* [[Shiing-shen Chern]], [[James Simons]], _[[Characteristic forms and geometric invariants]]_     The Annals of Mathematics, Second Series, Vol. 99, No. 1 (1974) ([jstor](http://www.jstor.org/stable/1971013)).


A comprehensive and clean account of the classical aspects is in 

* [[Dan Freed]], 

  * _Classical Chern-Simons theory Part I_ , 
    Adv. Math., 113 (1995), 237&#8211;303
    ([arXiv:hep-th/9206021](http://arxiv.org/abs/hep-th/9206021))
   {#FreedI}

  * _Classical Chern-Simons theory, part II_ 
    Houston J. Math., 28 (2002), pp. 293&#8211;310 ([pdf](http://www.ma.utexas.edu/users/dafr/cs2.pdf))

  * _Remarks on Chern-Simons theory_ Bulletin (New Series) of the AMS, Volume 46, Number 2, April 2009, Pages 221&#8211;254S 0273-0979(09)01243-9 ([arXiv:0808.2507](http://arxiv.org/abs/0808.2507))

Relation to [[knot theory]]:

* [[Michael Atiyah]], _The Geometry and Physics of Knots_,  Cambridge University Press 1990 ([doi:10.1017/CBO9780511623868](https://doi.org/10.1017/CBO9780511623868))


See also 

* {#CattaneoMnev08} [[Alberto Cattaneo]], [[Pavel Mnev]], _Remarks on Chern-Simons invariants_, Commun.Math.Phys.293:803-836, 2010 ([arXiv:0811.2045](https://arxiv.org/abs/0811.2045))

Discussion with emphasis on the [[symplectic structure]] on [[phase space]] and the expression of the [[Wilson lines]] by the [[orbit method]] is in

* {#AlekseevMalkin} [[Anton Alekseev]], A. Z. Malkin, _Symplectic Geometry of the Chern-Simons theory_ ESI preprint 80 (1994) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.142.9821))
 

A decent survey of the constructions within Chern-Simons theory is in 

* R. K. Kaul, T. R. Govindarajan, P. Ramadevi, _Schwarz Type Topological Quantum Field Theories_, Encyclopedia of Mathematical Physics (2005) ([arXiv:hep-th/0504100](http://arxiv.org/abs/hep-th/0504100))

The [[covariant phase space]] of Chern-Simons theory with its [[presymplectic structure]] is originally discussed in section 5 of 

* {#Witten86} [[Edward Witten]], _Interacting field theory of open superstrings_ Nuclear Physics B Volume 276, Issue 2, 13 October 1986, Pages 291-324  (1986) ([web](http://dx.doi.org/10.1016/0550-3213%2886%2990298-1))
 

(there in the context of [[string field theory]], but the manipulations of formulas is the same) and in section 3, example 2 of

* {#Zuckerman} [[Gregg Zuckerman|G. J. Zuckerman]], _Action Principles and Global Geometry_ , in Mathematical Aspects of String Theory, S. T. Yau (Ed.), World Scientific, Singapore, 1987, pp. 259&#8364;284. ([[ZuckermanVariation.pdf:file]])
 

A detailed discussion of the symplectic structure on the moduli space of flat connections is in 

* [[Michael Atiyah]], [[Raoul Bott]], _The Yang-Mills equations over Riemann surfaces_, Phil. Trans. R. Soc. Lond. A 308 (1982), 523-615. ([JSTOR](http://www.jstor.org/stable/37156))
 {#AtiyahBott}

* [[Alan Weinstein]], _The symplectic structure on moduli space_, The Floer memorial volume, 627{635, Progr. Math., 133, Birkhauser, Basel, (1995) ([pdf](http://math.berkeley.edu/~alanw/Moduli.pdf))
 {#Weinstein}

A talk about the historical origins of the standard Chern-Simons forms see

* [[Jim Simons]], _Origin of Chern-Simons_ talk at Simons Center for Geometry and Physics (2011) ([video](http://media.scgp.stonybrook.edu/video/video.php?f=20110728_1_qtp.mp4))

A discussion of Chern-Simons theory as a canonical object in [[infinity-Chern-Weil theory]] and its [[higher geometric quantization]] is in

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:A higher stacky perspective on Chern-Simons theory]]_
 {#FiorenzaSatiSchreiber}

* [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:AKSZ Sigma-Models in Higher Chern-Weil Theory]]_

### With Wilson loops, defects and boundaries
 {#ReferencesWithWilsonLoops}

The [[orbit method]]-formulation of [[Wilson loops]] in 3d Chern-Simons theory was vaguely indicated in ([Witten89, p. 22 ](#Witten)). 
More details were discussed in

* S. Elitzur, [[Greg Moore]], A. Schwimmer, and [[Nathan Seiberg]], _Remarks on the Canonical Quantization of the Chern-Simons-Witten Theory_, Nucl. Phys. B 326 (1989) 108&#8211;134.  
 {#EMSS}

In the context of other [[gauge theories]] ([[Yang-Mills theory]]) the same formulation appears much earlier in

* A. P. Balachandran, S. Borchardt, and A. Stern, _Lagrangian And Hamiltonian Descriptions of Yang-Mills Particles_, Phys. Rev. D 17 (1978) 3247&#8211;3256
 {#BBS}

A detailed review and further refinements are discussed in ([Alekseev-Malkin](#AlekseevMalkin)) and in section 4 of 

* [[Chris Beasley]], _Localization for Wilson Loops in Chern-Simons Theory_, in J. Andersen, H. Boden, A. Hahn, and B. Himpel (eds.) _Chern-Simons Gauge Theory: 20 Years After_, AMS/IP Studies in Adv. Math., Vol. 50, AMS, Providence, RI, 2011. ([arXiv:0911.2687](http://arxiv.org/abs/0911.2687))
 {#Beasley}

Aspects of the formulation in the context of [[BV-BRST formalism]] are discussed in ([Alekseev-Barmaz-Mnev](#AlekseevBarmazMnev)).

Discussion of _topological_ boundaries ([[branes]]) and suface [[QFT with defects|defects]] for Chern-Simons theory (as opposed to the non-topoligical [[WZW model]]-boundaries) is in

* [[Anton Kapustin]], [[Natalia Saulina]], _Surface operators in 3d TFT and 2d Rational CFT_ in [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ AMS, 2011
 {#KapustinSaulina11}

* [[Anton Kapustin]], [[Natalia Saulina]], _Topological boundary conditions in abelian Chern-Simons theory_,  	Nucl.Phys.B845:393-435,2011 ([arXiv:1008.0654](http://arxiv.org/abs/1008.0654))
 {#KapustinSaulina12}

* [[Jürgen Fuchs]], [[Christoph Schweigert]], [[Alessandro Valentino]], _Bicategories for boundary conditions and for surface defects in 3-d TFT_ ([arXiv:1203.4568](http://arxiv.org/abs/1203.4568))
 {#FSV}

### Quantization

We list discussions of [[quantization]] of Chern-Simons theory.

#### Geometric quantization
 {#ReferencesGeometricQuantization}

The original method of quantization of Chern-Simons theory used already in ([Witten 89](#Witten)) is _[[geometric quantization]]_.

More discussion of this is in 

* {#WittenJeffrey} [[Edward Witten]] (lecture notes by Lisa Jeffrey), _New results in Chern-Simons theory_, pages 81 onwards  in: [[Simon Donaldson]], C. Thomas (eds.) _Geometry of low dimensional manifolds 2: Symplectic manifolds and Jones-Witten theory_ (1989) ([pdf](http://cs5538.userapi.com/u11728334/docs/06f79688de6f/S_K_Donaldson_Geometry_of_LowDimensional_Ma.pdf))
 
* {#AxelrodPietraWitten91} [[Scott Axelrod]], S. Della Pietra, [[Edward Witten]], _Geometric quantization of Chern-Simons gauge theory_, Jour. Diff. Geom. 33 (1991), 787-902.  ([EUCLID](http://projecteuclid.org/euclid.jdg/1214446565))
 
* [[Scott Axelrod]], _Geometric Quantization of Chern-Simons Gauge Theory_ PhD thesis (1991)

and for the generalization to [[complex Lie groups]] in 

* [[Edward Witten]], _Quantization of Chern-Simons gauge theory with complex gauge group_, Comm. Math. Phys. Volume 137, Number 1 (1991), 29-66. ([Euclid](http://projecteuclid.org/euclid.cmp/1104202513))

The role of the [[metaplectic correction]] is studied in some detail in 

* {#ScheinostSchottenloher96} Peter Scheinost, [[Martin Schottenloher]], _Metaplectic quantization of the moduli spaces of flat and parabolic bundles_, J. reine angew. Mathematik, 466 (1996) ([web](https://eudml.org/doc/153753))
 
Also, from p. 154 (11 of 76) on, this article carefully discusses what is really the non-abelian version of the Griffiths [[intermediate Jacobian]] structure (see there) for $k = 0$.

Detailed discussion with emphasis on [[theta functions]] and the relation to [[Weyl quantization]] and [[skein relations]] is in

* [[Razvan Gelca]], [[Alejandro Uribe]], _From classical theta functions to topological quantum field theory_  ([arXiv:1006.3252](http://arxiv.org/abs/1006.3252), [slides pdf](http://www.math.ttu.edu/~rgelca/berk.pdf))

* [[Razvan Gelca]], [[Alejandro Uribe]], _Quantum mechanics and non-abelian theta functions for the gauge group $SU(2)$_ ([arXiv:1007.2010](http://arxiv.org/abs/1007.2010))


Decent expositions are for instance in 

* M. B. Young, _Chern-Simons theory, knots and moduli spaces of connections_ 2010 ([pdf](http://www.math.sunysb.edu/~myoung/CS.pdf))

and in section 3.3 of

* [[Tudor Dimofte]], [[Sergei Gukov]], _Quantum Field Theory and the Volume Conjecture_, in Andersen, Boden, Hahn, Himpel (eds.)_Chern-Simons gauge theory: 20 years after_, AMS (2011) ([arXiv:1003.4808](http://arxiv.org/abs/1003.4808))

Discussion that relates the geometric quantization of $G$-Chern-Simons theory to the [[Reshetikhin-Turaev construction]] of a 3d-[[TQFT]] from the [[modular tensor category]] induced by $G$ is in 

* {#Andersen12} [[Jørgen Andersen]], _A geometric formula for the Witten-Reshetikhin-Turaev Quantum Invariants and some applications_ ([arXiv:1206.2785](http://arxiv.org/abs/1206.2785))
 

and references cited there.

Discussion in terms of [[geometric quantization by push-forward]] is in 

* {#FreedHopkinsTeleman07} [[Daniel Freed]], [[Michael Hopkins]], [[Constantin Teleman]], _Consistent Orientation of Moduli Spaces_ ([arXiv:0711.1909](http://arxiv.org/abs/0711.1909)), chapter XIX, pages 395-419 in: Oscar Garcia-Prada, Jean Pierre Bourguignon, [[Simon Salamon]] (eds.) _The Many Facets of Geometry: A Tribute to Nigel Hitchin_, Oxford University Press 2010 ([doi:10.1093/acprof:oso/9780199534920.001.0001](http://www.oxfordscholarship.com/view/10.1093/acprof:oso/9780199534920.001.0001/acprof-9780199534920))
 

The "[[prequantum circle n-bundle|prequantum circle 3-bundle]]" in codimension 3, was constructed in 

* [[Domenico Fiorenza]], [[Urs Schreiber]] [[Jim Stasheff]], _[[schreiber:Cech Cocycles for Differential characteristic Classes]]_
  {#FiorenzaSchreiberStasheff}

and in codimension 2 ([[Wess-Zumino-Witten model]]) implicitly in 

* {#CJMSW} [[Alan Carey]], Stuart Johnson, [[Michael Murray]], [[Danny Stevenson]], [[Bai-Ling Wang]], _Bundle gerbes for Chern-Simons and Wess-Zumino-Witten theories_, Commun.Math.Phys. 259 (2005) 577-613 ([arXiv:math/0410013](http://arxiv.org/abs/math/0410013))
 

#### Hamiltonian quantization

* [[Anton Alekseev]], [[Harald Grosse]], [[Volker Schomerus]], _Combinatorial quantization of the Hamiltonian Chern-Simons theory_ ([pdf](http://www.mat.univie.ac.at/~esiprpr/esi079.pdf))



#### Perturbative quantization
 {#ReferencesPerturbativeQuantization}

Discussion of  [[perturbative quantum field theory|perturbative]] [[quantization of Chern-Simons theory]] (yielding [[Vassiliev invariants]]):

* {#BarNatan91} [[Dror Bar-Natan]], _Perturbative aspects of the Chern-Simons topological quantum field theory_, thesis 1991 ([spire:323500](http://inspirehep.net/record/323500), [proquest:303979053](https://search.proquest.com/docview/303979053), [[BarNatanPerturbativeCS91.pdf:file]])

* {#BarNatan95} [[Dror Bar-Natan]], _Perturbative Chern-Simons theory_,  Journal of Knot Theory and Its RamificationsVol. 04, No. 04, pp. 503-547 (1995) ([doi:10.1142/S0218216595000247](https://doi.org/10.1142/S0218216595000247))

* {#AxelrodSinger} [[Scott Axelrod]], [[Isadore Singer]], _Chern-Simons Perturbation Theory_, in S. Catto, A. Rocha (eds.) Proc. XXthe DGM Conf. World Scientific Singapore, 1992, 3-45; ([arXiv:hep-th/9110056](http://arxiv.org/abs/hep-th/9110056))

* [[Scott Axelrod]], [[Isadore Singer]],_Chern--Simons Perturbation Theory II_, J. Diff. Geom. 39 (1994) 173-213 ([arXiv:hep-th/9304087](http://arxiv.org/abs/hep-th/9304087)) 
 
* {#Kontsevich} [[Maxim Kontsevich]], _Feynman diagrams and low-dimensional topology_, in First European Congress of Mathematics, Vol. II (Paris, 1992), volume 120 of Progr. Math., pages 97&#8211;121, Birkh&#228;user, Basel, 1994. ([pdf](https://www.ihes.fr/~maxim/TEXTS/Feynman%20%20diagrams%20and%20low-dimensional%20topology.pdf))
 
* {#LambrechtsVolic14} [[Pascal Lambrechts]], [[Ismar Volić]], sections 6 and 7 of _Formality of the little N-disks operad_, Memoirs of the American Mathematical Society ; no. 1079, 2014  ([arXiv:0808.0457](https://arxiv.org/abs/0808.0457), [doi:10.1090/memo/1079](http://dx.doi.org/10.1090/memo/1079))

See also at _[[correlator as differential form on configuration space of points]]_ and see at _[[graph complex]]_  as a model for the [[spaces of knots]]_.



Perturbative quantization along the lines of _[Renormalization - Of theories in BV-CS form](renormalization#OfTheoriesInBVForm)_ is in

* [[Kevin Costello]], _[[Renormalization and Effective Field Theory]]_ AMS (2011) ([publisher webpage](http://www.ams.org/publications/authors/books/postpub/surv-170))

building on results summarized in section 1.11 and 1.12 and discussed in more detail in section 3 of 

* [[Kevin Costello]], _Renormalisation and the Batalin-Vilkovisky formalism_ ([arXiv:0706.1533](http://arxiv.org/abs/0706.1533))
 {#Costello}

In comparison it says in ([Costello, p. 14](#Costello))

> In the case when $H^\bullet(\mathcal{E})$, [Kontsevich 94](#Kontsevich) and [Axelrod-Singer 92, 94](#AxelrodSinger) (when $dim M = 3$) have already constructed the perturbative Chern-Simons invariants. In some sense, their construction is orthogonal to the construction in this paper.
Because we work modulo constants, the construction in this paper doesn't give anything in the case when $H^\bullet(\mathcal{E}) = 0$. On the other hand, their constructions don't apply in the situations where our construction gives something non-trivial. There seems to be no fundamental reason why a generalisation of the construction to this paper, including the constant term, should not exist. Such a generalisation would also generalise the results of Kontsevich and Axelrod-Singer. However, the problem of constructing such a generalisation does not seem to be amenable to the techniques used in this paper.

The BV-formalism for Chern-Simons theory on manifolds with [[boundary]] is discussed in

* [[Anton Alekseev]], Yves Barmaz, [[Pavel Mnev]], _Chern-Simons Theory with Wilson Lines and Boundary in the BV-BFV Formalism_ ([arXiv:1212.6256](http://arxiv.org/abs/1212.6256))
 {#AlekseevBarmazMnev}

based on 

* [[Alberto Cattaneo]], [[Pavel Mnev]], [[Nicolai Reshetikhin]], _Classical BV theories on manifolds with boundary_ ([arXiv:1201.0290](http://arxiv.org/abs/1201.0290))


On p. 3 there it says:

> There is a consensus that perturbative quantization of the classical Chern-Simons theory gives the same asymptotical expansions as the combinatorial topological field theory based on quantized universal enveloping algebras at roots of unity (45), or, equivalently, on the modular category corresponding to the Wess-Zumino-Witten conformal field theory (56, 42) with the first semiclassical computations involving torsion made in (56). However this conjecture is still open despite a number of important results in this direction, see for example (47, 3).
  
> One of the reasons why the conjecture is still open is that for manifolds with boundary the perturbative quantization of Chern-Simons theory has not been developed yet. On the other hand, for closed manifolds the perturbation theory involving Feynman diagrams was developed in (32, 27, 7) and in (5, 35, 13). For the latest development see (19). Closing this gap and developing the perturbative quantization of Chern-Simons theory for manifolds with boundary is one of the main motivations for the project started in this paper.


#### As second quantization of the A- or B-model

In 

* [[Edward Witten]]. _Chern&#8211;Simons Theory as a String Theory_ Prog. Math. 133: 637&#8211;678. ([arXiv:hep-th/9207094](http://arxiv.org/abs/hep-th/9207094)).
 {#Witten94}

an argument was given that Chern-Simons theory can be understood as the [[effective QFT|effective]] [[target space]] [[string theory]] of the [[A-model]] or [[B-model]] [[TCFT]]. This argument has later been made more precise in the language of [[TCFT]]. See [TCFT -- Effective background theories](#http://nlab.mathforge.org/nlab/show/TCFT#ActionFunctionals) for more on this. 

Discussion of an alternative derivation of this statement is in

* [[Jan de Boer]], Paul de Medeiros, Sheer El-Showk, Annamaria Sinkovics, _Open $G_2$ Strings_ ([arXiv:hep-th/0611080](http://arxiv.org/abs/hep-th/0611080))

A textbook account of this relation is in 

* Marcos Mari&#241;o, _Chern-Simons Theory, Matrix Models, and Topological Strings_, Oxford University Press (2005)

### As a relative extended TQFT

Discussion of quantum Chern-Simons theory as a 3-2-1 [[extended TQFT]] is for instance in 

* R. Gelca, _Topological quantum field theory with corners based on the Kauffman bracket_ ([pdf](http://www.math.ttu.edu/~rgelca/bra3.pdf))

Discussion as a (relative) 3-2-1-0 [[extended TQFT]] is in

* [[Dan Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], _[[Topological Quantum Field Theories from Compact Lie Groups]]_

* [[Dan Freed]], _[[4-3-2 8-7-6]]_, talk at _[ASPECTS of Topology](https://people.maths.ox.ac.uk/tillmann/ASPECTS.html)_ Dec 2012

* {#Henriques15} [[André Henriques]], _What Chern-Simons theory assigns to a point_ ([arXiv:1503.06254](http://arxiv.org/abs/1503.06254))

A gentle introduction leading up to one proposal for what Chern-Simons theory assigns to a point (a category of [[positive energy representations]] of the based [[loop group]]) is in

* [[Andre Henriques]], _Chern-Simons lectures_, Berkeley December 2014, [pdf](http://www.staff.science.uu.nl/~henri105/PDF/Chern-Simons-2014.pdf)

### Computations

* Auclky, _Topological methods to compute Chern-Simons invariants_ ([pdf](http://www.math.ksu.edu/~dav/topmethCS.pdf&#8206;))


Computations of flat Chern-Simons/[[Dijkgraaf-Witten theory]] [[action functionals]] for the complex [[special linear group]] are discused (and discussed to be related to volumes of [[hyperbolic manifold|hyperbolic 3-manifolds]]) in 

* [[Christian Zickert]], _The volume and Chern-Simons invariant of a representation_, Duke Math. J., 150 (3):489-532, 2009 ([arXiv:0710.2049](http://arxiv.org/abs/0710.2049))
 {#Zickert 07}


### Extension to supergroups

* Victor Mikhaylov, _Aspects of Supergroup Chern-Simons Theories_, ([thesis](https://inspirehep.net/record/1466706/))

* Victor Mikhaylov, _Analytic Torsion, 3d Mirror Symmetry,
And Supergroup Chern-Simons Theories_ ([arXiv:1505.03130](https://arxiv.org/abs/1505.03130))

[[!include 3d gravity and Chern-Simons theory -- references]]


### On D-brane worldvolumes
 {#ReferencesOnBraneWorldvolumes}

On 3d [[Chern-Simons theories]] arising from the [[higher WZ term]] on [[super p-brane]] [[worldvolumes]] (notably on [[D2-branes]]):

* {#Brodie00} [[John Brodie]], _D-branes in Massive IIA and Solitons in Chern-Simons Theory_, JHEP 0111:014, 2001 ([arXiv:hep-th/0012068](https://arxiv.org/abs/hep-th/0012068))

* Yosuke Imamura, _A D2-brane realization of Maxwell-Chern-Simons-Higgs systems_, JHEP 0102:035, 2001 ([arXiv:hep-th/0012254](https://arxiv.org/abs/hep-th/0012254))

* Mitsutoshi Fujita, Wei Li, [[Shinsei Ryu]], [[Tadashi Takayanagi]], _Fractional Quantum Hall Effect via Holography: Chern-Simons, Edge States, and Hierarchy_, JHEP 0906:066, 2009 ([arXiv:0901.0924](https://arxiv.org/abs/0901.0924))

* Kristan Jensen, p. 9,10 of: _Chiral anomalies and AdS/CMT in two dimensions_, JHEP 1101:109, 2011 ([arXiv:1012.4831](https://arxiv.org/abs/1012.4831))

* Gyungchoon Go, O-Kab Kwon, D. D. Tolla, _$\mathcal{N}=3$ Supersymmetric Effective Action of D2-branes in Massive IIA String Theory_, Phys. Rev. D 85, 026006, 2012 ([arXiv:1110.3902](https://arxiv.org/abs/1110.3902))

Specifically on [[D8-branes]] in the context of [[geometric engineering of QFT|geometric engineering]] of [[QCD]] ([[AdS/QCD]]):

* Alexander Gorsky, Valentin Zakharov, Ariel Zhitnitsky, _On Classification of QCD defects via holography_, Phys. Rev. D79:106003, 2009 ([arxiv:0902.1842](https://arxiv.org/abs/0902.1842))


and of [[2d QCD]] ([[AdS/QCD]]):

* Ho-Ung Yee, [[Ismail Zahed]], _Holographic two dimensional QCD and Chern-Simons term_, JHEP 1107:033, 2011 ([arXiv:1103.6286](https://arxiv.org/abs/1103.6286))

* Mitsutoshi Fujita, Charles M. Melby-Thompson, Rene Meyer, [[Shigeki Sugimoto]], _Holographic Chern-Simons Defects_, JHEP06 (2016) 163 ([arxiv:1601.00525](https://arxiv.org/abs/1601.00525))




[[!include topological quantum computation with anyons -- references]]






### Workshops and conferences

* [Chern-Simons Gauge Theory: 20 years after](http://www.hausdorff-center.uni-bonn.de/event/2009/gauge_theory/) was a workshop at the Max Planck Institute in Bonn from 3--7 August 2009.



[[!redirects Chern-Simons theory]]
[[!redirects Chern?Simons theory]]
[[!redirects Chern--Simons theory]]

[[!redirects Chern-Simons action functional]]
[[!redirects Chern-Simons theory action functional]]
[[!redirects Chern-Simons functional]]

[[!redirects Chern-Simons field theory]]

[[!redirects Chern-Simons theories]]
