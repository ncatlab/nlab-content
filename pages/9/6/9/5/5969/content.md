
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Variational calculus
+-- {: .hide}
[[!include variational calculus - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

# Contents
* table of contents
{: toc}


## Via the variational bicomplex

The following discusses the formulation of conserved currents in terms of [[variational calculus]] and the [[variational bicomplex]].

### The context

Let $X$ be a [[spacetime]] of [[dimension]] $n$, $E \to X$ a [[bundle]], $j:\infty E \to X$ its [[jet bundle]] and 

$$
  \Omega^{\bullet,\bullet}(j_\infty E), (D = \delta + d)
$$ 

the corresponding [[variational bicomplex]] with $\delta$ being the vertical and $d = d_{dR}$ the horizontal [[differential]].


+-- {: .num_prop #VariationOfTheLagrangian}
###### Proposition

For $L \in \Omega^{n,0}(j_\infty E)$ a [[Lagrangian]] we have that 

$$
  \delta L = E(L) + d \Theta
$$

for $E$ the [[Euler-Lagrange equations|Euler-Lagrange operator]].

=--

The [[covariant phase space]] of the Lagrangian is the locus

$$ 
  \{\phi \in \Gamma(E) | E(L)(j_\infty \phi) = 0\}  
  \,.
$$

For $\Sigma \subset X$ any $(n-1)$-dimensional submanifold, 

$$
  \delta \theta := \delta \int_\Sigma \Theta
$$

is the [[presymplectic structure]] on covariant phase space

### Definition

+-- {: .num_defn}
###### Definition

A **conserved current** is an element

$$
  j \in \Omega^{n-1, 0}(j_\infty E)
$$

which is horizontally closed on [[covariant phase space]]

$$
  d j|_{E(L) = 0} = 0
  \,.
$$

=--

+-- {: .num_defn}
###### Definition

For $\Sigma \hookrightarrow X$ a submanifold of dimension $n-1$, the **[[charge]]** of the conserved current $j$ with respect to $\Sigma$ is the [[integral]]

$$
  Q_\Sigma := \int_\Sigma j
  \,.
$$


=--

### Properties

+-- {: .num_prop}
###### Proposition

If $\Sigma, \Sigma' \subset X$ are homologous, the associated charge is the same

$$
  Q_{\Sigma} = Q_{\Sigma'}
  \,.
$$

=-- 

+-- {: .proof}
###### Proof

By [[Stokes' theorem]].

=--


+-- {: .num_theorem}
###### Theorem

Every [[symmetry]] induces a conserved current. 

=--

This is [[Noether's theorem]]. See there for more details.

## In higher prequantum geometry
 {#InHigherPrequantumGeometry}

The following discusses conserved currents in the context of [[higher prequantum geometry]], closely related to [Azcarraga-Izquierdo 95, section 8.1](#AzcarragaIzquierdo95). This follows ([classicalinhigher, section 3.3.](#classicalinhigher), going back to [Schreiber 13](#Schreiber13)). Similar observations have been made by [[Igor Khavkine]].

> this section needs much polishing. For the moment better see [classicalinhigher, section 3.3](#classicalinhigher)


### Context

Let $\mathbf{H}$ be the ambient [[(∞,1)-topos]]. For $\mathbf{Fields} \in \mathbf{H}$ a [[moduli ∞-stack]] of [[field (physics)|fields]] a [[local Lagrangian]] for an $n$-dimensional [[prequantum field theory]] is equivalently a [[prequantum n-bundle]] given by a map

$$
  \mathbf{L} \;\colon\; \mathbf{Fields} \longrightarrow \mathbf{B}^n U(1)_{conn}
$$


to the [[moduli ∞-stack]] of smooth [[circle n-bundles with connection]]. The local connection [[differential n-form]] is the [[local Lagrangian]] itself as in traditional literature, the rest of the data in $\mathcal{L}$ is the [[higher gauge theory|higher]] [[gauge symmetry]] [[equivariance|equivariant]] structure.


The following is effectively the direct higher geometric analog of the [Hamiltonian version of Noether's theorem](Noether's+theorem#HamiltonianNoetherTheorem).

### Symmetries

A transformation of the [[field (physics)|fields]] is an [[equivalence]]

$$
  \mathbf{Fields} 
    \underoverset{\simeq}{\phi}{\longrightarrow}
  \mathbf{Fields}
  \,.
$$

That the [[local Lagrangian]] $\mathcal{L}$ be preserved by this, up to ([[gauge symmetry|gauge]]) equivalence, means that there is a [[diagram]] in $\mathbf{H}$ of the form

$$
  \array{
    \mathbf{Fields} &&\underoverset{\simeq}{\phi}{\longrightarrow}&&
    \mathbf{Fields}
    \\
    & {}_{\mathllap{\mathbf{L}}}\searrow &\swArrow^\simeq_\alpha& \swarrow_{\mathrlap{\mathbf{L}}}
    \\
    && \mathbf{B}^n U(1)_{conn}
  }
  \,.
$$

(With $\mathbf{L}$ equivalently regarded as [[prequantum n-bundle]] this is equivalently a [higher quantomorphism](quantomorphism%20group#InHigherGeometry). These are the transformations studied in ([Fiorenza-Rogers-Schreiber 13](#FiorenzaRogersSchreiber13))) 

For $\phi$ an [[infinitesimal object|infinitesimal]] operation an $L$ locally the Lagrangian $n$-form, this means that the [[Lie derivative]] $\mathcal{L}_{\delta \phi}$ of $L$ has a potential,

$$
  \mathcal{L}_{\delta \phi} L = \mathbf{d} \alpha
$$

hence that the Lagrangian changes under the [[Lie derivative]] by an exact term, hence by a [[divergence]] on the [[worldvolume]] (since the degree of the Lagrangian form is the [[dimension]] of the worldvolume). See also ([Azcarraga-Izquierdo 95 (8.1.13)](#AzcarragaIzquierdo95)).


This is the situation of the [[Noether theorem]] for the general case of "weak" symmetries (see at [Noether theorem -- schematic idea  -- weak symmetries](Noether+theorem#WeakSymmetrySchematicIdea)).
 

By [[Cartan's magic formula]] the above means

$$
  \mathbf{d}\left(
    \alpha - \iota_{\delta\phi} \mathbf{L} 
  \right)
   = 
  \iota_{\delta \phi} \omega  
  \,.
$$


and hence the combination $j \coloneqq \alpha - \iota_{\delta\phi} \mathbf{L}$ (a _[[Hamiltonian form]]_ for $\delta \phi$ with respect to $\omega$) is conserved on trajectories in the kernel of the [[n-plectic form]] $\omega$ (which are indeed the classical trajectories of $\mathbf{L}$, see ([Azcarraga-Izquierdo 95 (8.1.14)](#AzcarragaIzquierdo95))). 

This is the first stage in the [[Poisson bracket Lie n-algebra]], the _[[current algebra]]_ (see there at _[As a homotopy Lie algebra](current%20algebra#AsAHomotopyLieAlgebra)_).

## Examples

### Of Green-Schwarz super $p$-brane sigma models

The WZW term of the [[Green-Schwarz super p-brane sigma models]] is invariant under [[supersymmetry]] only up to a [[divergence]], hence here the general [[Noether theorem]] for "weak" symmetries applies and yields a current algebra which is an [polyvector extension](super+Poincare+Lie+algebra#PolyvectorExtensions) of the [[supersymmetry]] algebra. See at _[Green-Schwarz action functional -- Conserved currents](Green-Schwarz+action+functional#ConservedCurrents)_ for more.

## Related concepts

* [[conservation law]]

* [[current algebra]]

* [[chiral anomaly]]

* [[classical observable]]

* [[Noether theorem]]

* [[charge]]

## References

### Dickey-Lie bracket on currents
 {#ReferencesDickeyBracket}

The [[Dickey Lie bracket]] on conserved currents is due to 

* [[Leonid Dickey]], _Soliton equations and Hamiltonian systems_, Advanced Series in Mathematical Physics, Vol. 12 (World Scientific 1991).

and is reviewed in

* [[Glenn Barnich]], [[Marc Henneaux]],  section 3 of _Isomorphisms between the Batalin-Vilkovisky antibracket and the Poisson bracket_, Journal of Mathematical Physics 37, 5273-5296 (1996) ([arXiv:hep-th/9601124](http://arxiv.org/abs/hep-th/9601124), [DOI 10.1063/1.531726](http://dx.doi.org/10.1063/1.531726))

A lift of the Dickey Lie bracket on equivalence classe of currents (de Rham cohomology classes) to an _[[model structure for L-infinity algebras|L-infinity equivalent]]_ [[L-infinity algebra|L-infinity bracket]] on actual currents (on the [[de Rham complex]]) is constructed, under some assumptions, in

* {#BarnichFulpLadaStasheff97} [[Glenn Barnich]], [[Ronald Fulp]], [[Tom Lada]], [[Jim Stasheff]], _The sh Lie structure of Poisson brackets in field theory_ ([arXiv:hep-th/9702176](http://arxiv.org/abs/hep-th/9702176))


### In variational calculus

A general discussion as above is around definition 9 of

* [[Gregg Zuckerman|G. J. Zuckerman]], _Action Principles and Global Geometry_ , in Mathematical Aspects of String Theory, S. T. Yau (Ed.), World Scientific, Singapore, 1987, pp. 259&#8211;284. ([[ZuckermanVariation.pdf:file]])

The relation of conserved currents to [[moment maps]] in [[symplectic geometry]] is highlighted for instance in 

* Huijun Fan, _Lecture 8, Moment map and symplectic reduction_ ([pdf](http://www.math.pku.edu.cn/teachers/fanhj/courses/symp-8.pdf))
 {#Fan}

### Higher conserved currents

Higher conserved currents are discussed for instance in

* [[Glenn Barnich]], [[Friedemann Brandt]], _Covariant theory of asymptotic symmetries, conservation laws and central charges_,  	Nucl.Phys.B633:3-82, 2002 ([arXiv:hep-th/0111246](http://arxiv.org/abs/hep-th/0111246))

### In higher prequantum theory

Conserved currents for Lagrangians written as [[WZW terms]] are discussed in

* {#AzcarragaIzquierdo95} [[José de Azcárraga]], Jos&#233; M. Izquierdo, section 8.1 of _Lie Groups, Lie Algebras, Cohomology and Some Applications in Physics_ , Cambridge monographs of mathematical physics, (1995)

Building on that, in the context of [[higher prequantum geometry]] conserved currents of the [[WZW model]] and in [[schreiber:∞-Wess-Zumino-Witten theory]] are briefly indicated on the last page of

* {#Schreiber13} [[Urs Schreiber]], _Higher geometric prequantum theory and The Brane Bouquet_, notes for a [[schreiber:The brane bouquet|talk]] at [Bayrischzell 2013](http://hep.itp.tuwien.ac.at/~miw/bzell2013/) ([pdf notes](http://ncatlab.org/schreiber/files/hpqWZWintro.pdf))

* {#classicalinhigher} [[Urs Schreiber]], _[[schreiber:Classical field theory via Cohesive homotopy types]]_ 

The same structure is considered in 

* {#FiorenzaRogersSchreiber13} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher geometric prequantum theory]]_, 2013
  

as higher [[quantomorphisms]] and [[Poisson bracket Lie n-algebras]] of local currents.


[[!redirects conserved current]]
[[!redirects conserved currents]]

[[!redirects current]]
[[!redirects currents]]

[[!redirects local current]]
[[!redirects local currents]]

[[!redirects Noether current]]
[[!redirects Noether currents]]

[[!redirects Noether current algebra]]
[[!redirects Noether current algebras]]

[[!redirects Dickey bracket]]
[[!redirects Dickey brackets]]
[[!redirects Dickey Lie bracket]]
[[!redirects Dickey Lie brackets]]
[[!redirects Dickey Lie-bracket]]
[[!redirects Dickey Lie-brackets]]
[[!redirects Dickey-Lie bracket]]
[[!redirects Dickey-Lie brackets]]