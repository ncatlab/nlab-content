

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Geometric quantization
+-- {: .hide}
[[!include geometric quantization - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Orbit method_ (or _Kirillov's method_, or _method of coadjoint orbits_) is a method in [[geometric representation theory]] concerned with identifying [[unitary representations]] of [[Lie groups]] with the canonical $G$-[[actions]] on spaces of [[sections]] of certain [[line bundles]] over [[coadjoint orbits]] of the Lie group. In terms of [[quantum physics]] this realizes $G$-[[representations]] as actions of [[global gauge groups]] of [[quantum operators]] on [[spaces of quantum states]] under _[[geometric quantization]]_.

More in detail, the dual $\mathfrak{g}^*$ of a (say finite-dimensional real) [[Lie algebra]] has a canonical structure of a [[Poisson manifold]] -- its _[[Lie-Poisson structure]]_ --, namely for any $a\in \mathfrak{g}^*$, 

$$
\{ f, g\}(a) \coloneqq \langle [d f_a, d g_a],a\rangle
 \,.
$$

This Poisson manifold [[foliation|foliates]] into [[symplectic leaves]] which are the [[coadjoint orbits]]. The [[line bundles]] in question are the _[[prequantum line bundles]]_ of these [[symplectic manifolds]].

Hence, in the language of [[quantum physics]], the orbit methods identifies unitary representations of Lie groups $G$ with the $G$-action on [[spaces of states]] of the [[geometric quantization]] of a [[classical mechanical system]] with a global $G$-[[symmetry]].

Many important classes of unitary representations are obtained by that method. 

Notably in the case of [[compact Lie groups]], co-adjoint orbits are [[flag manifolds]] and the _[[Borel-Weil theorem]]_ says that under certain further conditions the expected unitary representations are obtained.

The case of non-compact Lie groups is much less well understood, see for instance ([Graham-Vogan](#GrahamVogan), [Vogan 99](#Vogan99)).

## Definitions and constructions
 {#DefinitionsAndConstructions}

We list and discuss the basic notions, definitions and constructions in the context of the orbit method. A useful review is also in ([Beasley, section 4](#Beasley)).

### The group and its Lie algebra

Throughout, let $G$ be a [[semisimple Lie group|semisimple]] [[compact topological group|compact]] [[Lie group]]. For some considerations below we furthermore assume it to be [[simply connected topological space|simply connected]].

Write $\mathfrak{g}$ for its [[Lie algebra]]. Its canonical (up to scale) binary [[invariant polynomial]] we write

$$
  \langle -,-\rangle \colon \mathfrak{g} \otimes \mathfrak{g} \to \mathbb{R}
  \,.
$$

Since this is non-degenerate, we may equivalently think of this as an [[isomorphism]] 

$$
  \mathfrak{g} \simeq \mathfrak{g}^*
$$

that identifies the [[vector space]] underlying the Lie algebra with its [[dual vector space]] $\mathfrak{g}^*$.


### The coadjoint orbit and the coset space/ flag manifold
 {#TheCoadjointOrbitAndTheCosetSpaceAndFlagManifold}

We discuss the [[coadjoint orbits]] of $G$ and their relation to the [[coset space]]/[[flag manifolds]] of $G$.

Write 

1. $T \hookrightarrow G$ inclusion of the [[maximal torus]] of $G$.

1. $\mathfrak{t} \hookrightarrow \mathfrak{g}$ the corresponding [[Cartan subalgebra]]


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

### The symplectic form

We describe a canonical [[symplectic form]] on the [[coadjoint orbit]]/[[coset]] $\mathcal{O}_\lambda \simeq G/G_\lambda$.

Write $\theta \in \Omega^1(G, \mathfrak{g})$ for the [[Maurer-Cartan form]] on $G$.

+-- {: .num_defn #The2FormOnG}
###### Definition

Write 

$$
  \Theta_\lambda \coloneqq \langle \lambda, \theta \rangle \in \Omega^1(G)
$$

for the [[differential 1-form]] obtained by pairing the value of the [[Maurer-Cartan form]] at each point with the fixed element $\lambda \in \mathfrak{g}^*$.

Write

$$
  \nu_\lambda \coloneqq d_{dR} \Theta_\lambda
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

### The prequantum bundle

We discuss the [[geometric prequantization]] of the [[symplectic manifold]] given by the [[coadjoint orbit]] $\mathcal{O}_\lambda$ equipped with its [[symplectic form]] $\nu_\lambda$ of def. \ref{TheSymplecticFormOnTheCoset}.

Assume now that $G$ is [[simply connected topological space|simply connected]]. 

+-- {: .num_prop #WeightsAndCharacters}
###### Proposition

The [[weight lattice]] $\Gamma_{wt} \subset \mathfrak{t}^* \simeq \mathfrak{t}$ of the Lie group $G$ is [[isomorphism|isomorphic]] to the group of [[group characters]]

$$
  \Gamma_{wt} \stackrel{\simeq}{\to} Hom_{LieGrp}(T,U(1))
$$

where the identification takes $\langle \alpha , -\rangle \in \mathfrak{t}^*$ to $\rho_\alpha \colon T \to U(1)$ given on $t = \exp(\xi)$ for $\xi \in \mathfrak{t}$ by

$$
  \rho_\alpha \colon \exp(\xi) \mapsto \exp(i \langle \alpha, \xi\rangle)
  \,.
$$

=--

+-- {: .num_prop }
###### Proposition

The [[symplectic form]] $\nu_\lambda \in \Omega^2_{cl}(G/T)$ of prop. \ref{TheSymplecticFormOnTheCoset} is integral precisely if $\langle \lambda, - \rangle$ is in the [[weight lattice]].

=--

Integrality of the symplectic form is known as the [[[[geometric quantization|*Bohr--Sommerfeld condition*]], which is equivalent to the existence of a [[prequantum line bundle]].

### The Hamiltonian $G$-action / coadjoint moment map

The group $G$ canonically [[action|acts]] on the [[coset space]] $G/G_{\lambda}$ (by multiplication from the left). We discuss a lift of this action to a [[Hamiltonian action]] with respect to the [[symplectic manifold]] structure $(G/T, \nu_\lambda)$ of prop. \ref{TheSymplecticFormOnTheCoset}, equivalently a [[momentum map]] exhibiting this Hamiltonian action.



### Wilson loops and 1d Chern-Simons $\sigma$-models with target the coadjoint orbit
 {#WilsonLoopsAnd1DCSSigmaModelWithTargetTheCoadjointOrbit}

[Above](#DefinitionsAndConstructions)  we discussed how an [[irreducible representation|irreducible]] [[unitary representation]] of $G$ is encoded by the [[prequantization]] of a  [[coadjoint orbit]] $(\mathcal{O}_\lambda, \nu_\lambda)$. Here we discuss how to express [[Wilson loops]]/[[holonomy]] of $G$-[[principal connections]] in this representation as the [[path integral]] of a topological particle charged under this background field, whose [[action functional]] is that of a [[1-dimensional Chern-Simons theory]]. 

This was hinted at in [Witten 89, p. 22, 23](#Witten89), details are in ([Beasley, section 4](#Beasley)).

Let $A|_{S^1} \in \Omega^1(S^1, \mathfrak{g})$ be a [[Lie algebra valued 1-form]] on the circle, equivalently a $G$-[[principal connection]] on the circle. 

For 

$$
  \rho \colon G \to Aut(V)
$$

a [[representation]] of $G$, write

$$
  W_{S^1}^R(A) \coloneqq  hol^R_{S^1}(A) \coloneqq Tr_R( tra_{S^1}(A) )
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

be given by sending $g T \colon S^1 \to G/T$ represented by $g \colon S^1 \to G$ to

$$
  \exp(i \int_{S^1} \langle \lambda, A^g\rangle )
  \,,
$$

where 

$$
  A^g \coloneqq Ad_g(A) + g^* \theta
$$

is the [[gauge transformation]] of $A$ under $g$. 

=--

+-- {: .num_prop #WilsonLoopIsPartitionFunctionOf1dCSSigmaModel}
###### Proposition

The [[Wilson loop]] of $A$ over $S^1$ in the unitary irreducible representation $R$ is proportional to the [[path integral]] of the 1-dimensional [[sigma-model]] with 

1. [[target space]] the [[coadjoint orbit]] $\mathcal{O}_\lambda \simeq G/T$ for $\langle \lambda, - \rangle$ the [[weight (in representation theory)|weight]] corresponding to $R$ under the [[Borel-Weil-Bott theorem]]

1. [[action functional]] the functional of def. \ref{ActionFunctionalForTopologicalChargedParticle}:

$$
  W_{S^1}^R(A)
  \propto
  \underset{g T \in [S^1, \mathcal{O}_\lambda]}{\int}
  \exp(i \int_{S^1}  \langle \lambda, A^g\rangle)
  \;
  D(g T)
  \,.
$$

=--

See for instance ([Beasley, (4.55)](#Beasley)). 

+-- {: .num_remark }
###### Remark

Notice that since $\mathcal{O}_\lambda$ is a [[manifold]] of [[finite number|finite]] [[dimension]], the [[path integral]] for a point particle with this target space can be and has been defined rigorously, see at _[[path integral]]_.

=--


## Formulation in higher geometry
 {#FormulationInHigherGeometry}


We discuss here a natural equivalent reformulation of the [above](#DefinitionsAndConstructions) ingredients of the orbit method in terms of the [[higher differential geometry]] of [[smooth ∞-groupoids]], and specifically in terms of the [[extended prequantum field theory]] of [[Chern-Simons theory]] with [[Wilson line]] [[QFT with defects|defects]] ([FSS](#FSS)).

1. [Survey](#FormulationInHigherGeometrySurvey)

1. [Definitions and constructions](#FormulationInHigherGeometryDefinitions)

1. [Nonabelian charged particle trajectories &#8211; Wilson loops](#GaugeAndGravityWilsonLoops)

1. [3d Chern-Simons theory with Wilson loops](#ExtendedChern-SimonsTheoryAndWilsonLoops).


### Survey 
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


### Definitions and constructions
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
  \mathbf{J} 
  \coloneqq 
  \left( \; 
   \Omega^1(-,\mathfrak{g})//T 
     \;\to\; 
     \Omega^1(-,\mathfrak{g})//G \simeq \mathbf{B}G_{conn} 
    \;
  \right)
  \in 
  \mathbf{H}^{(\Delta^1)}
$$

for the canonical map, as indicated.

=--

+-- {: .num_remark }
###### Remark

The map $\mathbf{J}$ is the differential refinement of the [[delooping]] $\mathbf{B}T \to \mathbf{B}G$ of the defining inclusion. By the general discussion at [[coset space]] we have a [[homotopy fiber sequence]]

$$
  \array{
    \mathcal{O}_\lambda \simeq G/T &\to& \mathbf{B}T & \simeq *//T
    \\
    && \downarrow
    \\
    && \mathbf{B}G & \simeq *//G
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
  \mathbf{\theta} \colon G/T \stackrel{}{\to} \Omega^1(-,\mathfrak{g})//T
$$

given over a test manifold $U \in $ [[CartSp]] by the map

$$
  \mathbf{\theta}_U \colon C^\infty(U,G/T) \to \Omega^1(U,\mathfrak{g})
$$

which sends $g \mapsto g^* \theta$, where $\theta$ is the [[Maurer-Cartan form]] on $G$.

=--

+-- {: .num_remark}
###### Remark

This is a general phenomenon in the context of [[Cartan connections]]. See there at _[Definition -- In terms of smooth moduli stacks](Cartan+connection#InTermsOfSmoothModuliStacks)_.

=--

+-- {: .proof}
###### Proof 
**of prop. \ref{ThetaAsHomotopyFiberOfJ}**.

We compute the [[homotopy pullback]] of $\mathbf{J}$ along the point inclusion by the [[factorization lemma]] as discussed at _[homotopy pullback -- Constructions](homotopy%20pullback#ConstructionsGeneral)_.

This says that with $\mathbf{J}$ presented canonically as a map of presheaves of groupoids via the above definitions, its homotopy fiber is presented by the presheaf of groupids $hofib(\mathbf{J})$ which is the [[limit]] [[cone]] in


$$
  \array{
    hofib(\mathbf{J}) &\to& &\to& \Omega^1(-, \mathfrak{g})//T
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

   in $C^\infty(U,G)//C^\infty(U,T)$. This shows that $hofib(\mathbf{J}) \simeq G/T$.

1. The canonical map $hofib(\mathbf{J}) \to \Omega^1(-,\mathfrak{g})//T$ picks the top horizontal part of these commuting triangles hence equivalently sends $g$ to $g^* \theta$.

=--

+-- {: .num_remark }
###### Remark

There is yet one more fiber sequence of similar structure. If we let $L G \coloneqq [S^1, G]$ denote the free [[loop group]], then there is a fiber sequence

$$
  \array{
    G/T &\to& L G / T
    \\
    && \downarrow
    \\
    && L G / G & \simeq \Omega G
  }
  \,.
$$

The [[geometric quantization]] of $L G / T$ yields the [[positive energy representations]] of the [[loop group]] $L G_\mathcal{C}$. See at _[loop group -- Properties -- Representations](loop+group#Representations)_ for more on this.

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
  \Omega^1(U,\mathfrak{g})//C^\infty(U,T) \to \Omega^1(U)//C^\infty(U,U(1))
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

For this the key point is that since $T \simeq G_\lambda$ stabilizes $\langle \lambda , - \rangle$ under the [[coadjoint action]], the [[gauge transformation]] law for points $A \colon U \to \mathbf{B}G_{conn}$, which for $g \in C^\infty(U,G)$ is

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
  \colon 
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
  \colon
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
  \omega_U \colon C^\infty(G/T) \to \Omega^2_{cl}(U)
$$

which sends

$$
  [g] \mapsto d \langle \lambda,  g^* \theta \rangle
  \,.
$$

=--

### Nonabelian charged particle trajectories &#8211; Wilson loops
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

Regarding the inclusion $C$ as an object in the [[arrow category]] $\mathbf{H}^{\Delta^1}$, say that a [[gauge field]] configuration for $G$-[[Chern-Simons theory]] on $\Sigma$ with 
[[Wilson loop]] $C$ and labeled by the [[representation]] $R$ is a map

$$
  \phi 
  \;\colon\;
  C
  \to 
  \mathbf{J}
$$ 

in the [[arrow category]] $\mathbf{H}^{(\Delta^1)}$ of the ambient [[cohesive (∞,1)-topos]]. Such a map is equivalently by a square

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

Moreover, a _[[gauge transformation]]_ between two such fields $\kappa \colon \phi \Rightarrow \phi'$ is a $G$-gauge transformation of $A$ and  a $T$-gauge transformation of $A|_{S^1}$ such that these intertwine the component maps $g$ and $g'$. If we keep the bulk gauge field $A$ fixed, then his means that two fields $\phi$ and $\phi'$ as above are gauge equivalent precisely if there is a function $t \;\colon\; S^1 \to T$ such that $g = g' t$, hence gauge [[equivalence classes]] of fields for fixed bulk gauge field $A$ are parameterized by their components $[g] = [g'] \in [S^1, G/T]$ with values in the coset space, hence in the coadjoint orbit.

For every such field configuration we can evaluate two [[action functionals]]: 

1. that of 3d [[Chern-Simons theory]], whose [[extended Lagrangian]] is $\mathbf{c} \colon \mathbf{B}G_{conn} \to \mathbf{B}^3 U(1)_{conn}$;

1. that of the [[1-dimensional Chern-Simons theory]] discussed [above](#WilsonLoopsAnd1DCSSigmaModelWithTargetTheCoadjointOrbit) whose [[extended Lagrangian]] is $\langle \lambda, -\rangle \colon \Omega^1(-,\mathfrak{g})//T \to \mathbf{B}U(1)_{conn}$, by prop. \ref{Extended1dCSLagrangianFromLambda}.

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

### 3d Chern-Simons theory with Wilson loops
 {#ExtendedChern-SimonsTheoryAndWilsonLoops}


We discuss how an [[extended Lagrangian]] 
for $G$-[[Chern-Simons theory]] with [[Wilson loop]] [[QFT with defects|defects]] is naturally obtained from the [above](#FormulationInHigherGeometryDefinitions) [[higher geometry|higher geometric]] formulation of the orbit method. In particular we discuss how the relation between Wilson loops and [[1-dimensional Chern-Simons theory]] [[sigma-models]] with [[target space]] the [[coadjoint orbit]], as discussed  [above](#WilsonLoopsAnd1DCSSigmaModelWithTargetTheCoadjointOrbit) is naturally obtained this way.


More formally, we have an extended Chern-Simons theory as follows. 

The [[moduli stack]] of fields $\phi \colon C \to \mathbf{J}$ in $\mathbf{H}^{(\Delta^1)}$ as above is the [[homotopy pullback]]

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

One checks that this is indeed the correct prequantization as considered in ([Witten 89, p. 22](#Witten89)).


## Formulation in equivariant K-theory (Dirac induction)
 {#DiracInduction}

+-- {: .num_prop}
###### Proposition

For $G$ a [[compact Lie group]] with [[Lie algebra]] $\mathfrak{g}^\ast$, the [[push-forward in generalized cohomology|push-forward]] in compactly supported [[twisted K-theory|twisted]] $G$-[[equivariant K-theory]] to the point (the $G$-equivariant [[index]]/[[Dirac induction]]) produces the [[Thom isomorphism]]

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

This is ([FHT II, (1.27), theorem 1.28](#FHT)).


## Formulation in equivariant elliptic cohomology

The [above](#DiracInduction) formulation of the orbit method in 
[[equivariant K-theory]] has a higher order generalization where one replaces [[equivariant K-theory]] with [[equivariant cohomology|equivariant]] [[elliptic cohomology]]. Here the "elliptic" orbit method directly knows about the [[representation theory]] of the [[loop group]]. ([Ganter 12](#Ganter12)).



## Theorems

* [[Borel-Weil-Bott theorem]]

## Examples

* [[geometric quantization of the 2-sphere]]

## References
 {#References}

Introductions and surveys include

* [[Alexandre Kirillov]], _[[Lectures on the Orbit Method]]_, Graduate Studies in Mathematics, 64, American Mathematical Society, (2004)

  [[David Vogan]], _Review of: Lectures on the orbit method_ ([pdf](http://www.ams.org/journals/bull/2005-42-04/S0273-0979-05-01065-7/S0273-0979-05-01065-7.pdf))

* [[David Vogan]], _Geometry and representations of reductive groups_ (2007) ([pdf](http://www-math.mit.edu/~dav/rittC.pdf))

* J. Maes, _A introduction to the orbit method_, Master thesis (2011) ([pdf](http://testweb.science.uu.nl/ITF/teaching/2011/Jeroen%20Maes.pdf), [pdf slides](http://www.imus.us.es/FSMYT12/Talk_Jeroen_Maes.pdf), [web](http://igitur-archive.library.uu.nl/student-theses/2011-0622-200341/UUindex.html))

* Craig Jackson, _Symplectic manifolds, geometric quantization, and unitary representations of Lie groups_ ([pdf](http://go.owu.edu/~chjackso/Papers/topic.pdf))

* Reyer Sjamaar, _Notes on the orbit method and quantization_ (1997) ([[SjamaarOrbitMethod.pdf:file]])

Original references include

* &#1042;. &#1040;. &#1043;&#1080;&#1085;&#1079;&#1073;&#1091;&#1088;&#1075;, _&#1052;&#1077;&#1090;&#1086;&#1076; &#1086;&#1088;&#1073;&#1080;&#1090; &#1074; &#1090;&#1077;&#1086;&#1088;&#1080;&#1080; &#1087;&#1088;&#1077;&#1076;&#1089;&#1090;&#1072;&#1074;&#1083;&#1077;&#1085;&#1080;&#1081; &#1082;&#1086;&#1084;&#1087;&#1083;&#1077;&#1082;&#1089;&#1085;&#1099;&#1093; &#1075;&#1088;&#1091;&#1087;&#1087; &#1051;&#1080;_, &#1060;&#1091;&#1085;&#1082;&#1094;. &#1072;&#1085;&#1072;&#1083;&#1080;&#1079; &#1080; &#1077;&#1075;&#1086; &#1087;&#1088;&#1080;&#1083;., 1981, &#1090;&#1086;&#1084; 15, &#1074;. 1, &#1089;&#1090;&#1088;. 23&#8211;37,  [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=faa&paperid=1690&what=fullt&option_lang=rus); transl. V. A. Ginzburg, _Method of orbits in the representation theory of complex Lie groups_, Funct. Analysis and Its Appl. __1981__, 15:1, 18&#8211;28, [doi](http://dx.doi.org/10.1007/BF01082375)

* [[Bertram Kostant]], _Orbits and quantization theory_, Proc. ICM Nice 1970, 395-406, [djvu:597 K](http://www.mathunion.org/ICM/ICM1970.2/Main/icm1970.2.0395.0406.ocr.djvu), [pdf:1.1 M](http://www.mathunion.org/ICM/ICM1970.2/Main/icm1970.2.0395.0406.ocr.pdf)

* [[Bertram Kostant]], _Quantization and unitary representations. I. Prequantization_, in: Lectures in Modern Analysis and Applications III, Lec. Notes in Math. __170__, 87&#8211;208, [MR294568](http://www.ams.org/mathscinet-getitem?mr=294568); Russ. transl. by A. Kirillov: Uspehi Mat. Nauk __28__ (1973), no. 1(169), 163&#8211;225, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=rm&paperid=4837&volume=28&year=1973&issue=1&fpage=163&what=fullt&option_lang=eng)

* [[Alexandre Kirillov]], _&#1059;&#1085;&#1080;&#1090;&#1072;&#1088;&#1085;&#1099;&#1077; &#1087;&#1088;&#1077;&#1076;&#1089;&#1090;&#1072;&#1074;&#1083;&#1077;&#1085;&#1080;&#1103; &#1085;&#1080;&#1083;&#1100;&#1087;&#1086;&#1090;&#1077;&#1085;&#1090;&#1085;&#1099;&#1093; &#1075;&#1088;&#1091;&#1087;&#1087; &#1051;&#1080;_, , Uspehi. Mat. Nauk. 17 (1962), 57-110, [Rus. pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=rm&paperid=6513&what=fullt&option_lang=rus); transl. _Unitary representations of nilpotent Lie groups_, Russian Math. Surveys, 1962, 17:4, 53&#8211;104, [doi](http://dx.doi.org/10.1070%2FRM1962v017n04ABEH004118), [MR142001](http://www.ams.org/mathscinet-getitem?mr=142001)

* L. Auslander, [[Bertram Kostant]], _Quantization and representations of solvable Lie groups_, Bull. Amer. Math. Soc. __73__, 1967, 692&#8211;695, [pdf](http://www.ams.org/journals/bull/1967-73-05/S0002-9904-1967-11829-9/S0002-9904-1967-11829-9.pdf); _Polarization and unitary representations of
solvable Lie groups_, Invent. Math. __14__ (1971), 255&#8211;354, [MR293012](http://www.ams.org/mathscinet-getitem?mr=293012), [doi](http://dx.doi.org/10.1007/BF01389744)

* {#GrahamVogan} W. Graham, [[David Vogan]], _Geometric quantization for nilpotent coadjoint orbits_, in Geometry and Representation Theory of real and p-adic groups.
Birkh&#228;user, Boston-Basel-Berlin (1998)
 

* {#Vogan99} [[David Vogan]], _The method of coadjoint orbits for real reductive groups_, in Representation Theory of Lie Groups. IAS/Park City Mathematics Series 8 (1999), 179&#8211;238
 


Discussion with an eye towards application in [[gauge theory]] and in particular for [[Wilson loop]] observables in [[Chern-Simons theory]], hinted at on  

* {#Witten89} [[Edward Witten]], p. 22, 23 of _Quantum Field Theory and the Jones Polynomial_ Commun. Math. Phys. 121 (3) (1989) 351&#8211;399. MR0990772 ([project EUCLID](http://projecteuclid.org/euclid.cmp/1104178138))
 
is in section 4 of 

* {#Beasley} [[Chris Beasley]], _Localization for Wilson Loops in Chern-Simons Theory_, in J. Andersen, H. Boden, A. Hahn, and B. Himpel (eds.) _Chern-Simons Gauge Theory: 20 Years After_, , AMS/IP Studies in Adv. Math., Vol. 50, AMS, Providence, RI, 2011. ([arXiv:0911.2687](http://arxiv.org/abs/0911.2687))
 
referring to 

* S. Elitzur, [[Greg Moore]], A. Schwimmer, and [[Nathan Seiberg]], _Remarks on the Canonical Quantization of the Chern-Simons-Witten Theory_, Nucl. Phys. B 326 (1989) 108&#8211;134.

A program of applying the orbit method to real nilpotent orbits of real semisimple Lie groups (closely related to [[quantization via the A-model]]) is in 

* Ranee Brylinski, _Geometric Quantization of Real Minimal Nilpotent Orbits_, DGA, vol. 9 (1998), 5-58 ([arXiv:math/9811033](http://arxiv.org/abs/math/9811033))

  * _Quantization of the 4-dimensional nilpotent orbit of $SL(3,\mathbb{R})$_, Canad. J. Math. 49(1997), 916-943 ([web](http://cms.math.ca/cjm/a148867))

  * _Instantons and K&#228;hler Geometry of Nilpotent Orbits_ ([arXiv:math/9811032](http://arxiv.org/abs/math/9811032))

Discussion of the orbit method in terms of [[equivariant K-theory]] and [[Dirac induction]] is in 

* {#HFT} [[Daniel Freed]], [[Michael Hopkins]], [[Constantin Teleman]], part II, section 1 of _[[Loop Groups and Twisted K-Theory]]_
 

* {#Hochs12} [[Peter Hochs]], section 2.2 of _Quantisation of presymplectic manifolds, K-theory and group representations_ ([arXiv:1211.0107](http://arxiv.org/abs/1211.0107))
 

The generalization of this to [[elliptic cohomology]] is discussed in 

* {#Ganter12} [[Nora Ganter]], _The elliptic Weyl character formula_ ([arXiv:1206.0528](http://arxiv.org/abs/1206.0528))
 

Generalization to [[supergeometry]] is discussed in:

* Gijs M. Tuynman, _Geometric Quantization of Superorbits: a Case Study_ ([arXiv:0901.1811](http://arxiv.org/abs/0901.1811))

* Alexander Alldridge, Joachim Hilgert, Tilmann Wurzbacher, _Superorbits_ ([arXiv:1502.04375](https://arxiv.org/abs/1502.04375))


A generalization to [[higher geometry]] and [[2-group]] [[2-representations]] is proposed in 

* [[Bruce Bartlett]], _On unitary 2-representations of finite groups and topological quantum field theory_ ([arXiv:0901.3975](http://arxiv.org/abs/0901.3975))

The above discussion of the interpretation of the orbit method in terms of higher [[moduli stacks]] for [[differential cohomology]] appears in 

* {#FSS} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], section 3.4.5 of _[[schreiber:A higher stacky perspective on Chern-Simons theory]]_, in Damien Calaque et al. (eds.) _Mathematical Aspects of Quantum Field Theories_, Mathematical Physics Studies, Springer 2014 ([arXiv:1301.2580](http://arxiv.org/abs/1301.2580))
 

See also

* wikipedia, _[orbit method](http://en.wikipedia.org/wiki/Orbit_method)_

[[!redirects method of coadjoint orbits]]