
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

The _Nambu-Goto action_ is an [[action functional]] for [[sigma-models]] with [[target space]] a ([[pseudo-Riemannian manifold|pseudo]]) [[Riemannian manifold]] $(X,g)$: it is the induced volume functional

$$
  S_{NG} 
  \;\colon\; 
  (\Sigma \stackrel{\gamma}{\to} X) 
    \mapsto 
  T \int_\Sigma dvol(\gamma^* g)
  \,,
$$

where $dvol(\gamma^* g)$ is the [[volume form]] of the pullback $\gamma^* g$ of the metric tensor from $X$ to $\Sigma$, and where $T$ (the [[brane]]-"tension", e.g. the [[string tension]] for $dim(\Sigma) = 2$) is an inverse [[unit]] of [[length]] to the power the [[dimension]] $dim(\Sigma)$.

## Definition

Let 

* $p \in \mathbb{N}$ (for [[p-brane]] dynamics);

* $(X,g)$ a [[pseudo-Riemannian manifold]] ([[target spacetime]]);

* $\Sigma$ a [[compact topological space|compact]] [[smooth manifold]] of dimension $(p+1)$ ([[worldvolume]]).

* $[\Sigma,X]$ the [[diffeological space]] of [[smooth functions]] $\Sigma \to X$.

For $\phi \colon \Sigma \longrightarrow X$ the induced "proper volume" or _Nambu-Goto action_ of $\phi$ is the [[integral]] over $\phi$ of the [[volume form]] of the pullback of the target space metric $g$ to $\Sigma$.

$$
  S_{NG}(\phi) \coloneqq \int_{\Sigma} dvol(\phi^\ast(g))
  \,.
$$

Notice that the rank-2 [[tensor]] $\phi^\ast g\in \Gamma(T* \Sigma \oplus T* \Sigma)$ is in general not non-degenerate (unless $\phi$ is an [[embedding]]), hence is in general not, strictly speaking a [[pseudo-Riemannian metric]] on $\Sigma$, but nevertheless it induces a [[volume form]] by the standard formula, only that this allowed to vanish pointwise (and even globally, for instance if $\phi$ is constant on a single point). In the literature $dvol(\phi^\ast g)$ is usually written as $\sqrt{-g}d^{p+1}\sigma$.


## Properties

### Relation to the Polyakov action

The NG is classically equivalent to the [[Polyakov action]] with "[[worldvolume]] [[cosmological constant]]". See at _[Polyakov action -- Relation to Nambu-Goto action](Polyakov+action#RelationToNambuGotoAction)_.

## Applications

The NG-action serves as the kinetic [[action functional]] of the [[sigma-model]] that described a fundamental [[brane]] propagating on $X$. For 
$dim \Sigma = 1$ this is the [[relativistic particle]], for $dim \Sigma = 2$ the [[string]], for $dim \Sigma = 3$ the [[membrane]].

## Related concepts

* [[minimal surface]]

* [[Polyakov action]]

* [[Dirac-Born-Infeld action]]

* [[Veneziano amplitude]]

* [[particle]], [[string]], [[membrane]]

* [[membrane instanton]]

* for more on brane tension see also _[Worldsheet and brane instantons](non-perturbative+effect#WorldsheetAndBraneInstantons)_



## References

The Nambu-Goto action functional originates as a proposal for the dynamics of [[strings]] meant to explain the "dual resonance model" for [[hadron]] [[bound states]] ([[quantum hadrodynamics]], cf. *[[Polyakov gauge-string duality]]*):

* {#Nambu70} [[Yoichiro Nambu]], *Duality and Hadrodynamics*, Notes prepared for the Copenhagen High Energy Symposium (1970) &lbrack;[doi:10.1142/9789812795823_0026](https://doi.org/10.1142/9789812795823_0026), [[Nambu-DualityAndHadrodynamics.pdf:file]]&rbrack;

* {#Gotō71} [[Tetsuo Gotō]], *Relativistic Quantum Mechanics of One-Dimensional Mechanical Continuum and Subsidiary Condition of Dual Resonance Model*, Progress of Theoretical Physics **46** 5 (1971) 1560–1569 &lbrack;[doi:10.1143/PTP.46.1560](https://doi.org/10.1143/PTP.46.1560)&rbrack;

Historical review:

* [[Joël Scherk]], *An introduction to the theory of dual models and strings*, Rev. Mod. Phys. **47** 123 (1975) &lbrack;[doi:10.1103/RevModPhys.47.123](https://doi.org/10.1103/RevModPhys.47.123)&rbrack;

* [[Hiroshi Itoyama]], *Birth of String Theory*, Progress of Theoretical and Experimental Physics **2016** 6 (2016) 06A103 &lbrack;[arXiv:1604.03701](http://arxiv.org/abs/1604.03701), [doi:10.1093/ptep/ptw063](https://doi.org/10.1093/ptep/ptw063)&rbrack;


Detailed discussion of the relation to the [[Polyakov action]] and the [[Dirac-Born-Infeld action]] is in

* {#Nieto01} J. A. Nieto, _Remarks on Weyl invariant p-branes and Dp-branes_ ([arXiv:hep-th/0110227](http://arxiv.org/abs/hep-th/0110227))

One [[string theory]] textbook that deals with the Nambu-Goto action in a bit more detail than usual is

* [[Barton Zwiebach]], _A first course in string theory_ , Cambridge (2009)


Discussion of the Nambu-Goto action and [[Polyakov action]] on [[worldsheets]] with [[manifold with boundary|boundary]] (i.e. in the generality of [[open strings]]) and cast in [[BV-BRST formalism]]:

* {#MartinoliSchiavina22} S. Martinoli, [[Michele Schiavina]], *BV analysis of Polyakov and Nambu–Goto theories with boundary*,  Lett. Math. Phys. **112** 35 (2022) &lbrack;[doi:10.1007/s11005-022-01526-1](https://doi.org/10.1007/s11005-022-01526-1), [arXiv:2106.02983](https://arxiv.org/abs/2106.02983)&rbrack;

Relation of the Nambu-Goto string to [[Liouville theory]]:

* [[Yuri Makeenko]], *The Nambu-Goto string as higher-derivative Liouville theory* &lbrack;[arXiv:2407.01136](https://arxiv.org/abs/2407.01136)&rbrack;

Relation to [[D=3 gravity]]:

* Avik Banerjee, Ayan Mukhopadhyay, [[Giuseppe Policastro]]: *Nambu-Goto equation from three-dimensional gravity* &lbrack;[arXiv:2404.02149](https://arxiv.org/abs/2404.02149)&rbrack;






[[!redirects Nambu-Gotō action]]

[[!redirects tension]]
[[!redirects tensions]]

[[!redirects Nambu-Goto action functional]]
[[!redirects Nambu-Goto action functionals]]

[[!redirects Nambu-Gotō action functional]]
[[!redirects Nambu-Gotō action functionals]]



