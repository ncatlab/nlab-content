

> this entry is going to contain one chapter of _[[geometry of physics]]_


*** 

#Contents#
* table of contents
{:toc}

## Prequantum gauge theory and gravity


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

