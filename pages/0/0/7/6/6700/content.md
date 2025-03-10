+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functorial quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The local data for a [[CFT]] in [[dimension]] $d$ allows to assign to each $d$-[[dimension|dimensional]] [[cobordism]] $\Sigma$ a [[vector space]] of "possible [[correlators]]": those functions on the space of [[conformal structures]] on $\Sigma$ that have the correct behaviour (satisfy the conformal [[Ward identities]]) to qualify as the (chiral) [[correlator]] of a CFT. This is called a space of _[[conformal blocks]]_ $Bl(\Sigma)$. This assignment is [[functor|functorial]] under [[diffeomorphism]]. The corresponding functor is called a **modular functor**. ([Segal 89](#Segal89), [Kriz 03](#Kriz03), [Segal 04, def. 5.1](#Segal04)).

To get an actual collection of correlators one has to choose from each space of conformal blocks $Bl(\Sigma)$ an element such that these choices glue under composition of [[cobordism]]: such that they solve the [[sewing constraints]], see for instance at _[[FRS-theorem on rational 2d CFT]]_.

Dually, under a [[holographic principle]] such as [[AdS3-CFT2 and CS-WZW correspondence|CS3/WZW2]] the space of [[conformal blocks]] on $\Sigma$ is equivalently the [[space of quantum states]] of the [[TQFT]] on $\Sigma$. See at _[[quantization of 3d Chern-Simons theory]]_ for more on this.


## Definition

+-- {: .num_defn #CategoryOfRiemannSurfaces}
###### Definition

For $\Phi$ any [[finite set]] ("of labels") write $\mathcal{S}_{\Phi}$ for the [[category]] whose [[objects]] are [[Riemann surfaces]] with [[boundary]] [[circles]] labeled by elements of $\Phi$, and whose [[morphisms]] are [[holomorphic maps]] $X \to X_{sewed}$, where $X_{sewed}$ is obtained from $X$ by [[sewing constraint|sewing]] along boundary circles carrying the same labels.

=--

([Segal 04, section 4, section 5](#Segal04))

This category, being essentially the total [[Riemann moduli space]] is naturally a [[complex analytic stack]].

For $\Sigma$ a [[topological manifold|topological]] [[surface]] write $\mathcal{S}_\Sigma$ for the component of $\mathcal{S}$ on Riemann surfaces whose underlying topological surface is $\Sigma$.

+-- {: .num_remark}
###### Remark

If $\Sigma$ has at least one hole (boundary component), then the [[fundamental group]] $\pi_1(\mathcal{S}_\Sigma)$ is the [[mapping class group]] of $\Sigma$.

=--


+-- {: .num_defn #ModularFunctor}
###### Definition

A _modular functor_ is a holomorphic functor 

$$
  E \colon \mathcal{S}_\Phi \longrightarrow sVect
$$

(i.e. a morphism of [[complex analytic stacks]] from the [[Riemann moduli space]] to the stack of ([[finite number|finite]]-[[rank of a vector bundle|rank]]) [[holomorphic vector bundles]], in general with [[super vector space]]-[[fibers]])

such that

1. $E$ is [[strong monoidal functor|strong monoidal]]: $E(X \coprod Y) \simeq E(X)\otimes E(Y)$;

1. $E$ respects sewing: if $X_\phi$ is obtained from $X$ by cutting along a circle and giving the same label $\phi \in \Phi$ to both resulting boundaries, then the [[natural transformation]]

   $$
     \underset{\phi \in \Phi}{\oplus} E(X_\phi) \longrightarrow E(X)
   $$

   is a [[natural isomorphism]].

1. normalization: for $X = S^2$ the [[Riemann sphere]] we have $E(S^1) = 1$ (the[[tensor unit]] vector space).

=--

([Segal 04, def.  5.1](#Segal04))


## Properties

### Relation to genus-zero conformal blocks
 {#RelationToGenusZeroConformalBlocks}

For a [[rational CFT|rational]] [[2d CFT]] the modular functor is fully determined by the [[conformal blocks]] on the [[Riemann sphere]] (the *genus=0 conformal blocks*) -- this is proven in [Andersen & Ueno 2012](#AndersenUeno12).

Closely related is the statement that the [[braided monoidal category|braided monoidal structure]] on the [[modular tensor category|modular]] [[representation category]] of the corresponding [[vertex operator algebra]] is fully determined by the genus=0 conformal blocks, a statement that seems to be [[folklore]] (highlighted in [EGNO 15, p. 266](modular+tensor+category#EGNO15), [Runkel, Sec. 4.3](modular+tensor+category#Runkel)).

### Central charge and Central extensions

Any modular functor defines a [[central extension]] of the [[semigroup]] of conformal [[annuli]].  

These correspond precisely to [[group extensions]] of $Diff^+(S^1)$ by $\mathbb{C}^\times$.

([Segal 04, prop. 5.6](#Segal04))


These in turn are classified by $(c,h) \in \mathbb{C} \times \mathbb{C}/\mathbb{Z}$.

([Segal 04, prop. 5.8](#Segal04))

+-- {: .num_defn #CentralCharge}
###### Definition

Here in terms of standard [[2d CFT]] terminology 

*$c$ is the _central charge_ 

*$h$ is the [[eigenvalues]] of $L_0$.

=--


### The Knizhnik&#8211;Zamolodchikov-Hitchin connection

+-- {: .num_prop #TheProjFlatConnection}
###### Proposition

Given a modular functor $E$ as in def. \ref{ModularFunctor} and given a non-[[closed manifold|closed]] [[topological manifold|topological]] labelled [[surface]] $\Sigma$ with $E_\Sigma \to \mathcal{S}_\Sigma$ the resulting [[vector bundle]], then this bundle carries a canonical [[projectively flat connection]] $\nabla_\Sigma$ compatible with the [[sewing constraint|sewing operation]] of def. \ref{CategoryOfRiemannSurfaces}.

=--

([Segal 04, prop. 5.4](#Segal04), see also at [[Knizhnik-Zamolodchikov equation]])

+-- {: .num_remark}
###### Remark

When thinking of the modular functor $E$ as the functor of [[conformal blocks]] of a [[2d CFT]] then the projectively flat connection of prop. \ref{TheProjFlatConnection} would often be called the _[[Knizhnik-Zamolodchikov connection]]_. Thinking of $E$ dually as the functor assigning [[spaces of quantum states]] of [[Chern-Simons theory]] then it would typically be called the [[Hitchin connection]] (see also [Segal 04, p. 44, p. 84](#Segal04)).

=--

+-- {: .num_pro #FlatConnectionForVanishingCentralCharge}
###### Proposition

The connection of prop. \ref{TheProjFlatConnection} is a genuine [[flat connection]] (not projective) precisely if the central charge vanishes, $c = 0$ (Def. \ref{CentralCharge}).

=--

([Segal 04, below prop. 5.4](#Segal04))

### The Verlinde fusion algebra

+-- {: .num_defn}
###### Definition

For $\phi,\chi,\psi \in \Phi$ three labels, write $P_{\phi,\chi,\psi}$ for the three-holed sphere ("pair of pants", "trinion") with inner circles labeled by $\phi$ and $\chi$ and outer circle labeled by $\psi$.

For $E$ a modular functor as in def. \ref{ModularFunctor}, write

$$
  n_{\phi, \chi,\psi} \coloneqq dim(E(P_{\phi,\chi,\psi}))
$$

for the [[dimension]] of the vector space that it assigns to this surface.

Then the [[free abelian group]] $\mathbb{Z}[\Phi]$ on the set of labels inherits the structure of an [[associative algebra]] via

$$
  (\phi,\chi) \mapsto \underset{\psi}{\sum}  n_{\phi,\chi, \psi} \psi
  \,.
$$

The _[[Verlinde algebra]]_.

=--

([Segal 04, section 5, p. 36-37](#Segal04))


### Deprojectivization, Cancelling of central charge, topological modular functor
 {#TopologicalLift}

By prop. \ref{FlatConnectionForVanishingCentralCharge} and prop. \ref{CentralChargeOfDeterminantLine}, if $E$ is a modular functor of central charge $c$ then the [[tensor product]]

$$
  \tilde E \coloneqq E \otimes Det^{\otimes c/2}
$$

with a possibly fractional power of the [[determinant line bundle]], def. \ref{PowerOfDeterminantLine}, produces a modular functor with vanishing central charge.

To make sense of this however one needs to consistently define the fractional power. For that one needs to pass to surfaces equipped with a bit more structure.

+-- {: .num_defn #RiggedSurfaces}
###### Definition

The category of _rigged surfaces_ $\hat {\mathcal{S}}_\Phi$ is the [[central extension]] of that of [[smooth manifold]] [[surfaces]] such that for [[genus of a surface|genus]] $\gt 1$ it gives the universal central extension of the [[diffeomorphism group]].

For instance the category of surfaces equipped with a choice of [[universal covering space]] of the [[circle group]]-[[principal bundle]] underlying the [[determinant line bundle]] over $\mathcal{S}_\Sigma$.

=--

([Segal 04, def. (5.10) and following](#Segal04), also [Bakalov-Kirillov, def. 5.7.5](#BakalovKirillov))

+-- {: .num_prop}
###### Proposition

Given a [[modular functor]] $E$, def. \ref{ModularFunctor} of central charge $c$, def. \ref{CentralCharge}, then the tensor product $\tilde E \coloneqq E \otimes Det^{\otimes c/2}$ is well defined on the category $\hat S_{\phi}$ of rigged surfaces, def. \ref{RiggedSurfaces}.

=--

Of course if one has an extension of the diffeomorphism group by a multiple of the universal extension in def. \ref{RiggedSurfaces}, then this still trivializes the conformal anomaly for all modular functors whose central charge is a corrsponding multiple. In particular:

+-- {: .num_prop #SurfacesWithAtiyah2Framing}
###### Proposition

The category of smooth surfaces equipped with "[[Atiyah 2-framing]]" (hence with a trivialization of the spin lift of the double of their tangent bundle) provides an extension of the diffeomorphic group of level 12.

=--

([Segal 04, p. 46](#Segal04))

+-- {: .num_remark}
###### Remark

There is a natural functor from smooth surfaces $\Sigma$ equipped with [[3-framing]] (trivialization of $T \Sigma\oplus \underline{\mathbb{R}}$) to that equipped with [[Atiyah 2-framing]] in prop. \ref{SurfacesWithAtiyah2Framing}.

=--

> thanks to [[Chris Schommer-Pries]] for highlighting this point.



## Examples

### Powers of the determinant line

+-- {: .num_defn #PowerOfDeterminantLine}
###### Definition

For $n \in \mathbb{Z}$ let $E = Det^{\otimes n}$ be the functor which sends a [[Riemann surface]] to the $c$th power of its [[determinant line]] (i.e. that of its [[Laplace operator]]). 

=--

Super-line, see ([Kriz-Lai 13](#KrizLai13))...

+-- {: .num_defn }
###### Proposition

The determinant lines of def. \ref{PowerOfDeterminantLine} constitute precisely the modular functors, def. \ref{ModularFunctor}, for which $dim(E(X)) = 1$ for all $X$.

=--

([Segal 04, corollary (5.17)](#Segal04))

+-- {: .num_prop #CentralChargeOfDeterminantLine}
###### Proposition

The central charge, def. \ref{CentralCharge}, of the determinant line $E = Det$, def. \ref{PowerOfDeterminantLine}, is

$$
 (c,h ) = (-2,0)
  \,.
$$

=--

([Segal 04, p.43](#Segal04))

## Related concepts

* [[Hitchin connection]]

* [[quantization of Chern-Simons theory]]

## Properties

### Relation to equivariant elliptic cohomology / equivariant $tmf$

The modular functor for $G$-[[Chern-Simons theory]] restricted to [[genus of a surface|genus-1 surfaces]] ([[elliptic curves]]) is essentially what is encoded in the universal $G$-[[equivariant elliptic cohomology]] (equivariant [[tmf]]). In fact equivariant elliptic cohomology remembers also the [[local prequantum field theory|pre-quantum]] incarnation of the modular functor as a systems of [[prequantum line bundles]] over Chern-Simons [[phase spaces]] (which are [[moduli stacks of flat connections]]) and remembers the [[quantization]]-process from there to the actual [[space of quantum states]] by forming holomorphic [[sections]]. See at _[equivariant elliptic cohomology -- Idea -- Interpretation in Quantum field theory](equivariant+elliptic+cohomology#InterpretationInQuantumFieldTheory)_ for more on this.

## References

Original formulations:

* [[Graeme Segal]], *Two-dimensional conformal field theories and modular functors*, in: *IXth International Congress on Mathematical Physics*, Swansea 1988, Adam Hilger, Bristol and New York (1989) 22–37 &lbrack;[pdf](https://dmitripavlov.org/scans/segal-two-dimensional-conformal-field-theories-and-modular-functors.pdf), [[Segal-2dCFTandModularFunctors.pdf:file]]&rbrack;

* [[Graeme Segal]], *The definition of conformal field theory*, in: [[Ulrike Tillmann]] (ed.), *Topology, geometry and quantum field theory* , London Math. Soc. Lect. Note Ser. **308**, Cambridge University Press (2004) 421-577 &lbrack;[doi:10.1017/CBO9780511526398.019](https://doi.org/10.1017/CBO9780511526398.019), [pdf](https://people.maths.ox.ac.uk/segalg/0521540496txt.pdf), [[SegalDefinitionCFT.pdf:file]]&rbrack;


* {#Kriz03} [[Igor Kriz]], _On spin and modularity in conformal field theory_, Ann. Sci. ANS (4) 36 (2003), no. 1, 57112 ([numdam:ASENS_2003_4_36_1_57_0](http://www.numdam.org/item?id=ASENS_2003_4_36_1_57_0))

* {#KrizLai13} [[Igor Kriz]], Luhang Lai, _On the definition and K-theory realization of a modular functor_, ([arxiv/1310.5174](http://arxiv.org/abs/1310.5174)).


Lectures and reviews:

* {#BakalovKirillov} [[Bojko Bakalov]], [[Alexander Kirillov]], chapter 5 of _Lectures on tensor categories and modular functor_ ([web](http://www.math.sunysb.edu/~kirillov/tensor/tensor.html), [[BakalovKirillovChapter5.pdf:file]])

* {#Gawedzki99} [[Krzysztof Gawedzki]], section 5.6 of _Conformal field theory: a case study_ ([arXiv:hep-th/9904145](http://arxiv.org/abs/hep-th/9904145))

* {#Looijenga10} [[Eduard Looijenga]], _From WZW models to Modular Functors_ ([arXiv:1009.2245](http://arxiv.org/abs/1009.2245))

* [[Jürgen Fuchs]], [[Christoph Schweigert]], [[Simon Wood]], [[Yang Yang]], p. 11 of: *Algebraic structures in two-dimensional conformal field theory*, Encyclopedia of Mathematical Physics &lbrack;[arXiv:2305.02773](https://arxiv.org/abs/2305.02773)&rbrack;


Proof that the values of a modular functor at [[genus of a surface|genus]]=0 (ie. the [[conformal blocks]] on the punctured [[Riemann sphere]]) determine the full modular functor:

* {#AndersenUeno12} [[Jørgen Ellegaard Andersen]], [[Kenji Ueno]], *Modular functors are determined by their genus zero data*, Quantum Topology **3** 3/4 (2012) 255-291 $[$[doi:10.4171/QT/29](https://doi.org/10.4171/qt/29)$]$


Discussion in the context of [[(2,1)-dimensional Euclidean field theories and tmf]] is in

* {#StolzTeichner11} [[Stefan Stolz]], [[Peter Teichner]], section 5.2 of _Supersymmetric field theories and generalized cohomology_, in [[Hisham Sati]], [[Urs Schreiber]] (eds.), _[Mathematical foundations of Quantum field theory and String theory](http://ncatlab.org/schreiber/show/Mathematical+Foundations+of+Quantum+Field+and+Perturbative+String+Theory#ContributionStolzTeichner)_, Proceedings of Symposia in Pure Mathematics, Volume 83, AMS (2011)


Discussion in the context of the [[cobordism hypothesis]]:

* {#FiorenzaValentino14} [[Domenico Fiorenza]], [[Alessandro Valentino]], *Boundary Conditions for Topological Quantum Field Theories, Anomalies and Projective Modular Functors*, Commun. Math. Phys. **338** (2015) 1043–1074  $[$[arXiv:1409.5723](http://arxiv.org/abs/1409.5723), [doi:10.1007/s00220-015-2371-3](https://doi.org/10.1007/s00220-015-2371-3)$]$

Constructing [[modular functors]] from [[pivotal category|pivotal]] [[bicategories]] using [[string net models]]:

* [[Jürgen Fuchs]], [[Christoph Schweigert]], [[Yang Yang]], *String-net models for pivotal bicategories* &lbrack;[arXiv:2302.01468](https://arxiv.org/abs/2302.01468)&rbrack;

Relation to [[factorization homology]] of [[surfaces]]:

* [[Adrien Brochier]], [[Lukas Woike]]: *A Classification of Modular Functors via Factorization Homology* &lbrack;[arXiv:2212.11259](https://arxiv.org/abs/2212.11259)&rbrack;



[[!redirects modular functors]]
