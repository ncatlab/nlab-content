
> under construction

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

The _Orbit method_ (or _Kirillov's method_, or _method of coadjoint orbits_) is concerned with identifying [[unitary representations]] of [[Lie groups]] with the canonical $G$-[[actions]] on spaces of [[sections]] of certain [[line bundles]] over [[coadjoint orbits]] of the Lie group.

More in detail, the dual $\mathfrak{g}^*$ of a (say finite-dimensional real) [[Lie algebra]] has a canonical structure of a [[Poisson manifold]] (with the Poisson structure due to [[Alexandre Kirillov]] and [[Jean-Marie Souriau]]), namely for any $a\in \mathfrak{g}^*$, 

$$
\{ f, g\}(a) := \langle [d f_a, d g_a],a\rangle
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

Throughout, let $G$ be a [[semisimple Lie group|semisimple]] [[compact topological group|compact]] [[Lie group]]. 

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


### The coadjoint orbit and the coset / flag manifold

We discuss the [[coadjoint orbits]] of $G$ and their relation to the [[cosets]]/[[flag manifolds]] of $G$.

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

### The symplectic form

We describe a canonical [[symplectic form]] on the [[coadjoint orbit]]/[[coset]] $\mathcal{O}_\lambda \simeq G/G_\lambda$.

Write $\theta \in \Omega^1(G, \mathfrak{g})$ for the [[Maurer-Cartan form]] on $G$.

+-- {: .num_defn #The2FormOnG}
###### Definition

Write 

$$
  \Theta_\lambda := \langle \lambbda, \theta \rangle \in \Omega^1(G)
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
     \nu_\lambda = \frac{1}{2}\langle \lambda, [\theta\wegde \theta]\rangle
     \,.
   $$

1. it descends to a closed $G$-invariant 2-form on the [[coset]], to be denoted by the same symbol 

   $$
     \nu_\lambda \in \Omega^2_{cl}(G/G_\lambda)^G
     \,.
   $$ 

1. this is non-degenerate and hence defines a [[symplectic form]] on $G/G_\lambda$.

=--

### The Hamiltonian $G$-action / coadjoint moment map

The group $G$ canonically [[action|acts]] on the [[coset]] $G/G_{\lambda}$ (by multiplication from the left). We discuss a lift of this action to a [[Hamiltonian action]] with respect to the [[symplectic manifold]] structure $(G/T, \nu_\lambda)$ of prop. \ref{TheSymplecticFormOnTheCoset}, equivalently a [[momentum map]] exhibiting this Hamiltonian action.

(...)


## Formulation in higher geometry
 {#FormulationInHigherGeometry}


We discuss here an equivalent reformulation of the [above](#DefinitionsAndConstructions) ingredients of the orbit method in terms of the [[higher geometry]] of [[smooth ∞-groupoids]]. 

* [Survey](#FormulationInHigherGeometrySurvey)

* [Definitions and constructions](#FormulationInHigherGeometryDefinitions)

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
  \mathbf{J} := ( \Omega^1(-,\mathfrak{g})//T \to \Omega^1(-,\mathfrak{g})//G \simeq \mathbf{B}G_{conn} )
  \in 
  \mathbf{H}^{\Delta^1}
$$

for the canonical map, as indicated.

=--

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

For instance by applying the [[factorization lemma]].

=--

+-- {: .num_prop #Extended1dCSLagrangianFromLambda}
###### Proposition

There is a morphism of [[moduli stacks]]

$$
  \langle \lambda, - \rangle
  : 
  \Omega^1(-,\mathfrak{g})//T
  \to
  \mathbf{B}U(1)_{conn}
$$

in $\nathbf{H}$ given over a test manifold $U \in $ [[CartSp]] by the function on objects

$$
  \langle \lambda, - \rangle_U 
  \;:\; 
  \Omega^1(U,\mathfrak{g}) \to \Omega^1(U)
$$

which in turn is given by sending

$$
  A \mapsto \langle \lambda, A\rangle
$$

and the function on morphisms given by sending $\exp( \sum_i f^i t_i )$ to $\sum_i d f^i \langle \lambda, \t_i\rangle$

=--

+-- {: .proof}
###### Proof

The key point is that since $T \simeq G_\lambda$ stabilizes $\langle \lambda , - \rangle$ under the [[coadjoint action]], the [[gauge transformation]] law for points $A : U \to \mathbf{B}G_{conn}$, which for $g \in C^\infty(U,G)$ is

$$
  A \mapsto Ad_g A + g^* \theta
  \,,
$$

maps for $g = exp(f^i t_i ) \in T \hookrightarrow G$ to the gauge transformation law in $\mathbf{B}U(1)_{conn}$:

$$
  \begin{aligned}
    \langle \lambda, A \rangle 
    & \mapsto
    \langle \lambda, Ad_g A\rangle + \langle \lambda, g^* \theta\rangle
    \\
     & = \langle \lambda, A \rangle + d  \sum_i f^i\langle \lambda, t_i\rangle
  \end{aligned}
$$

=--

(...)

+-- {: .num_remark #ThePrequantumBundleFromCanonicalMaps}
###### Remark

The composite of the canonical maps of prop. \ref{ThetaAsHomotopyFiberOfJ} and prop. \ref{Extended1dCSLagrangianFromLambda} modulates a canonical [[circle bundle with connection]] on the [[coset]]/[[coadjoint orbit]]:

$$
  \langle \lambda, \mathbf{\theta}\rangle
  : 
  G/T
  \stackrel{\mathbf{\lambda}}{\to}
  \Omega^1(-,\mathfrak{g})//T
  \stackrel{\langle \lambda, - \rangle}{\to}
  \mathbf{B}U(1)_{conn}
  \,.
$$ 

=--

+-- {: .num_prop }
###### Proposition

The [[curvature]] 2-form of the circle bundle $\langle \lambda, \mathbf{\theta}\rangle$ from remark \ref{ThePrequantumBundleFromCanonicalMaps} is the [[symplectic form]] of prop. \ref{TheSymplecticFormOnTheCoset}. Therefore $\langle \lambda, \mathbf{\theta}\rangle$ is a [[prequantization]] of the coadjoint orbit $(\mathcal{O}_\lambda \simew G/T, \nu_\lambda)$.

=--

+-- {: .proof}
###### Proof

The curvature 2-form is modulated by the composite

$$
  \omega 
  :
  G/T
  \stackrel{\mathbf{\lambda}}{\to}
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


## Theorems

(...)

* [[Borel-Weil-Bott theorem]]

(...)

## References

Introductions and survey include

* [[Alexandre Kirillov]], _Lectures on the orbit method_ (2004)

  [[David Vogan]], _Review of: Lectures on the orbit method_ ([pdf](http://www.ams.org/journals/bull/2005-42-04/S0273-0979-05-01065-7/S0273-0979-05-01065-7.pdf))

* [[David Vogan]], _Geometry and representations of reductive gorups_ (2007) ([pdf](http://www-math.mit.edu/~dav/rittC.pdf))

* J. Maes, _An introduction to the orbit method_ Master thesis (2011) ([web](http://igitur-archive.library.uu.nl/student-theses/2011-0622-200341/UUindex.html))

* Craig Jackson, _Symplectic manifolds, geometric quantization, and unitary representations of Lie groups_ ([pdf](http://go.owu.edu/~chjackso/Papers/topic.pdf))

* Reyer Sjamaar, _Notes on the orbit method and quantization_ (1997) ([[SjamaarOrbitMethod.pdf:file]])

Original references include

* &#1042;. &#1040;. &#1043;&#1080;&#1085;&#1079;&#1073;&#1091;&#1088;&#1075;, _&#1052;&#1077;&#1090;&#1086;&#1076; &#1086;&#1088;&#1073;&#1080;&#1090; &#1074; &#1090;&#1077;&#1086;&#1088;&#1080;&#1080; &#1087;&#1088;&#1077;&#1076;&#1089;&#1090;&#1072;&#1074;&#1083;&#1077;&#1085;&#1080;&#1081; &#1082;&#1086;&#1084;&#1087;&#1083;&#1077;&#1082;&#1089;&#1085;&#1099;&#1093; &#1075;&#1088;&#1091;&#1087;&#1087; &#1051;&#1080;_, &#1060;&#1091;&#1085;&#1082;&#1094;. &#1072;&#1085;&#1072;&#1083;&#1080;&#1079; &#1080; &#1077;&#1075;&#1086; &#1087;&#1088;&#1080;&#1083;., 1981, &#1090;&#1086;&#1084; 15, &#1074;. 1, &#1089;&#1090;&#1088;. 23&#8211;37,  [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=faa&paperid=1690&what=fullt&option_lang=rus); transl. V. A. Ginzburg, _Method of orbits in the representation theory of complex Lie groups_, Funct. Analysis and Its Appl. __1981__, 15:1, 18&#8211;28, [doi](http://dx.doi.org/10.1007/BF01082375)

* [[Bertram Kostant]], _Orbits and quantization theory_, Proc. ICM Nice 1970, 395-406, [djvu:597 K](http://www.mathunion.org/ICM/ICM1970.2/Main/icm1970.2.0395.0406.ocr.djvu), [pdf:1.1 M](http://www.mathunion.org/ICM/ICM1970.2/Main/icm1970.2.0395.0406.ocr.pdf)

* [[Bertram Kostant]], _Quantization and unitary representations. I. Prequantization_, in: Lectures in Modern Analysis and Applications III, Lec. Notes in Math. __170__, 87&#8211;208, [MR294568](http://www.ams.org/mathscinet-getitem?mr=294568); Russ. transl. by A. Kirillov: Uspehi Mat. Nauk __28__ (1973), no. 1(169), 163&#8211;225, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=rm&paperid=4837&volume=28&year=1973&issue=1&fpage=163&what=fullt&option_lang=eng)

* [[Alexandre Kirillov]], _&#1059;&#1085;&#1080;&#1090;&#1072;&#1088;&#1085;&#1099;&#1077; &#1087;&#1088;&#1077;&#1076;&#1089;&#1090;&#1072;&#1074;&#1083;&#1077;&#1085;&#1080;&#1103; &#1085;&#1080;&#1083;&#1100;&#1087;&#1086;&#1090;&#1077;&#1085;&#1090;&#1085;&#1099;&#1093; &#1075;&#1088;&#1091;&#1087;&#1087; &#1051;&#1080;_, , Uspehi. Mat. Nauk. 17 (1962), 57-110, [Rus. pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=rm&paperid=6513&what=fullt&option_lang=rus); transl. _Unitary representations of nilpotent Lie groups_, Russian Math. Surveys, 1962, 17:4, 53&#8211;104, [doi](http://dx.doi.org/10.1070%2FRM1962v017n04ABEH004118), [MR142001](http://www.ams.org/mathscinet-getitem?mr=142001)

* L. Auslander, [[Bertram Kostant]], _Quantization and representations of solvable Lie groups_, Bull. Amer. Math. Soc. __73__, 1967, 692&#8211;695, [pdf](http://www.ams.org/journals/bull/1967-73-05/S0002-9904-1967-11829-9/S0002-9904-1967-11829-9.pdf); _Polarization and unitary representations of
solvable Lie groups_, Invent. Math. __14__ (1971), 255&#8211;354, [MR293012](http://www.ams.org/mathscinet-getitem?mr=293012), [doi](http://dx.doi.org/10.1007/BF01389744)

* W. Graham, [[David Vogan]], _Geometric quantization for nilpotent coadjoint orbits_, in Geometry and Representation Theory of real and p-adic groups.
Birkh&#228;user, Boston-Basel-Berlin (1998)
 {#GrahamVogan}

* [[David Vogan]], _The method of coadjoint orbits for real reductive groups_, in Representation Theory of Lie Groups. IAS/Park City Mathematics Series 8 (1999), 179&#8211;238
 {#Vogan99}

Discussion with an eye towards application in [[gauge theory]] and in particular for [[Wilson loop]] observables in [[Chern-Simons theory]] (hinted at on p. 22, 23 of [[Edward Witten]]'s _[QFT and the Jones polynomial](http://projecteuclid.org/euclid.cmp/1104178138)_) is in section 4 of 

* [[Chris Beasley]], _Localization for Wilson Loops in Chern-Simons Theory_, in J. Andersen, H. Boden, A. Hahn, and B. Himpel (eds.) _Chern-Simons Gauge Theory: 20 Years After_, , AMS/IP Studies in Adv. Math., Vol. 50, AMS, Providence, RI, 2011. ([arXiv:0911.2687](http://arxiv.org/abs/0911.2687))
 {#Beasley}

referring to 

* S. Elitzur, [[Greg Moore]], A. Schwimmer, and [[Nathan Seiberg]], _Remarks on the Canonical Quantization of the Chern-Simons-Witten Theory_, Nucl. Phys. B 326 (1989) 108&#8211;134.


Generalizations to [[supergeometry]] are discussed in

* Gijs M. Tuynman, _Geometric Quantization of Superorbits: a Case Study_ ([arXiv:0901.1811](http://arxiv.org/abs/0901.1811))

A generalization to [[higher geometry]] and [[2-group]] [[2-representations]] is proposed in 

* [[Bruce Bartlett]], _On unitary 2-representations of finite groups and topological quantum field theory_ ([arXiv:0901.3975](http://arxiv.org/abs/0901.3975))

See also

* wikipedia, _[orbit method](http://en.wikipedia.org/wiki/Orbit_method)_

[[!redirects method of coadjoint orbits]]