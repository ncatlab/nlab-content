

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Give a [[field theory]] (for instance a [[Lagrangian field theory]]) whose [[field bundle]] is a [[vector bundle]], then the [[space of sections]] of the field bundle, hence the [[space of field histories]], is canonically a [[vector space]] and hence it makes sense to consider [[observables]] which are [[linear functions]], or [[quadratic functions]] of the [[field histories]], etc. A [[sum]] of such is a _polynomial observable_.

Since linear smooth observables are [[compactly supported distributions]] (see at _[[distributions are the smooth linear functionals]]_) polynomial observables are sums of [[diagonals]] of [[distributions of several variables]].

If all these distributional coefficients are [[non-singular distributions]] one speaks of _regular observables_.

If all the distributional coefficients at order $k$ satisfy the condition that their [[wave front sets]] exclude the subsets where all $k$ [[wave vectors]] are all in the [[future cone]] or all in the [[past cone]], then one speaks of _[[microcausal observables]]_. 


[[!include perturbative observables -- table]]


## Definition

+-- {: .num_defn #PolynomialObservable}
###### Definition
**([[polynomial observable]])**

Let $E \overset{fb}{\to}$ be [[field bundle]] which is a [[vector bundle]]. An [[off-shell]] _[[polynomial observable]]_ is a [[smooth function]]

$$
  A 
  \;\colon\;
  \Gamma_\Sigma(E)
    \longrightarrow 
  \mathbb{C}
$$

on the [[on-shell]] [[space of sections]] of the [[field bundle]] $E \overset{fb}{\to} \Sigma$ (space of field histories) which may be expressed as

$$
  A(\Phi)
  \;=\;
  \alpha^{(0)}
  +
  \int_\Sigma
    \alpha^{(1)}_a(x) \Phi^a(x)
   \,
  dvol_\Sigma(x)
  +
  \int_\Sigma \int_\Sigma
   \alpha^{(2)}_{a_1 a_2}(x_1, x_2) \Phi^{a_1}(x_1) \Phi^{a_2}(x_2)
  \,dvol_\Sigma(x_1)
  \, dvol_\Sigma(x_2)
  +
  \cdots
  \,,
$$

where 

$$
  \alpha^{(k)} \in \Gamma'_{\Sigma^k}\left((E^\ast)^{\boxtimes^k_{sym}} \right)
$$

is a [[compactly supported distribution]] [[distribution of two variables|of k variables]] on the $k$-fold graded-symmetric [[external tensor product of vector bundles]] of the [[field bundle]] with itself.

Write 

$$
  PolyObs(E) \hookrightarrow Obs(E)
$$

for the [[subspace]] of off-shell polynomial observables onside all off-shell [[observables]].

Let moreover $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] whose [[equations of motion]] are [[Green hyperbolic differential equations]]. Then an _[[on-shell]] polynomial observable_ is the [[restriction]] of an off-shell polynomial observable along the inclusion of the [[on-shell]] [[space of field histories]] $\Gamma_{\Sigma}(E)_{\delta_{EL}\mathbf{L} = 0} \hookrightarrow \Gamma_\Sigma(E)$. Write

$$
  PolyObs(E,\mathbf{L}) \hookrightarrow Obs(E,\mathbf{L})
$$

for the subspace of all on-shell polynomial observables inside all on-shell [[observables]].


By [this prop.](Green+hyperbolic+partial+differential+equation#DistributionsOnSolutionSpaceAreTheGeneralizedPDESolutions) restriction yields an [[isomorphism]] between polynomial on-shell observables and polynomial off-shell observables modulo the image of the [[differential operator]] $P$:

$$
  PolyObs(E,\mathbf{L})
    \underoverset{\simeq}{\text{restriction}}{\longleftarrow}
  PolyObs(E)/im(P)
  \,.
$$

=--

Various special cases:

+-- {: .num_defn #LinearObservable}
###### Definition
**([[linear observable]])**

A _[[linear observable]]_ is a [[polynomial observable]] (def. \ref{PolynomialObservable}) all whose [[coefficients]] except possible for $\alpha^{(1)}$ are [[zero]].

=--

+-- {: .num_defn #RegularObservables}
###### Definition
**([[regular observable]])**

A _[[regular observable]]_ is a [[polynomial observable]] (def. \ref{PolynomialObservable}) all whose [[coefficients]] $\alpha^{(k)}$ are [[non-singular distributions]].

=--

+-- {: .num_defn}
###### Definition
**([[microcausal observable]])**

For $\Sigma$ a [[spacetime]], hence a [[Lorentzian manifold]] with [[time orientation]], then a _[[microcausal observable]]_ is a [[polynomial observable]] (def. \ref{PolynomialObservable}) such that each [[coefficient]] $\alpha^{(k)}$ has [[wave front set]] excluding those points  where all $k$ [[wave vectors]] are in the [[future cone]] or all in the [[past cone]].

=--

## Examples
 {#Examples}

+-- {: .num_example }
###### Example
**([[field observables]])**

If the [[field bundle]] is a [[vector bundle]], then the [[field observables]]

$$
  \mathbf{\Phi}^a(x) \;\colon\; \Phi \mapsto \Phi^a(x)
$$

are [[linear observables]] (def. \ref{LinearObservable}).

=--

+-- {: .num_example #PolynomialLocalObservablesArePolynomialObservables}
###### Example
**([[polynomial]] [[local observables]] are [[polynomial observables]])**

A [[local observable]] which comes form a [[variational differential form|horizontal differential form]] which is a [[polynomial]] in the fields and their jets times the [[volume form]] on [[spacetime]] is a polynomial observable.

These happen to be also [[microcausal observables]] ([this example](microcausal+functional#CompactlySupportedPolynomialLocalDensities)).

=--

## Related concepts

[[polynomial]] [[local observables]] $\hookrightarrow$ [[microcausal observables]] $\hookrightarrow$ [[polynomial observables]] $\hookrightarrow$ [[observables]]

[[!include states and observables -- content]]


## References

See the references at _[[microcausal observable]]_.

[[!redirects polynomial observables]]

[[!redirects linear observable]]
[[!redirects linear observables]]

[[!redirects regular observable]]
[[!redirects regular observables]]

[[!redirects regular linear observable]]
[[!redirects regular linear observables]]

[[!redirects regular polynomial observable]]
[[!redirects regular polynomial observables]]
