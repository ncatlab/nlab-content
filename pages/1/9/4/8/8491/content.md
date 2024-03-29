

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[Lie n-algebra]] that generalizes the [[Poisson bracket]] from [[symplectic geometry]] to [[n-plectic geometry]]: the _Poisson bracket $L_\infty$-algebra of local observables_ in [[higher prequantum geometry]].

More discussion is [here](n-plectic+geometry#PoissonLInfinityAlgebras) at _[[n-plectic geometry]]_.

Applied to the symplectic current (in the sense of [[covariant phase space]] theory, [[de Donder-Weyl field theory]]) this is the higher [[current algebra]] (see there) of [[conserved currents]] of a [[prequantum field theory]].

## Definition
 {#Definition}

Throughout, Let $X$ be a [[smooth manifold]], let $n \geq 1$ a natural number  and $\omega \in \Omega^{n+1}_{cl}(X)$ a closed [[differential n-form|differential (n+1)-form]] on $X$. The pair $(X,\omega)$ we may regard as a [[pre-n-plectic manifold]].

We define two [[L-∞ algebras]] defined from this data and discuss their [[equivalence]]. Either of the two or any further one equivalent to the two is the _Poisson bracket Lie $n$-albebra_ of $(X,\omega)$. The first definition is due to ([Rogers 10](#Rogers10)), the second due to ([FRS 13b](#FRS13b)). Here in notation we follow ([FRS 13b](#FRS13b)).

+-- {: .num_defn #HamiltonianFormsAndVectorFields}
###### Definition

Write

$$
  Ham^{n-1}(X) \subset Vect(X) \oplus \Omega^{n-1}(X)
$$

for the subspace of the [[direct sum]] of [[vector fields]] $v$ on $X$ and [[differential n-form|differential (n-1)-forms]] $J$ on $X$ satisfying

$$
  \iota_v  \omega + \mathbf{d} J = 0
  \,.
$$

We call these the _pairs of [[Hamiltonian forms]] with their [[Hamiltonian vector fields]]_.

=--

([FRS 13b, def. 2.1.3](#FRS13b))

+-- {: .num_defn #PoissonBracketLienAlgebra}
###### Definition

The [[L-∞ algebra]] $L_\infty(X,\omega)$ has as underlying [[chain complex]] the truncated and modified [[de Rham complex]]

$$
  \Omega^0(X)
  \stackrel{\mathbf{d}}{\to}
  \Omega^1(X)
  \stackrel{\mathbf{d}}{\to}
  \cdots 
  \stackrel{\mathbf{d}}{\to}
  \Omega^{n-2}(X)
  \stackrel{(0,\mathbf{d})}{\longrightarrow}  
  Ham^{n-1}(X)
$$

with the Hamiltonian pairs, def. \ref{HamiltonianFormsAndVectorFields}, in degree 0 and with the 0-forms ([[smooth functions]]) in degree $n-1$, and its non-vanishing $L_\infty$-brackets are as follows:

* $l_1(J) = \mathbf{d}J$

* $l_{k \geq 2}(v_1 + J_1, \cdots, v_k + J_k) = - (-1)^{\left(k+1 \atop 2\right)} \iota_{v_1 \wedge \cdots \wedge v_k}\omega$.

=--

([FRS 13b, prop. 3.1.2](#FRS13b))


+-- {: .num_defn #PoissondgAlgebra}
###### Definition

Let $\overline{A}$ be any [[Cech cohomology|Cech]]-[[Deligne cohomology|Deligne]]-[[cocycle]] relative to an [[open cover]] $\mathcal{U}$ of $X$, which gives a [[prequantum n-bundle]] for $\omega$. The [[L-∞ algebra]] $dgLie_{Qu}(X,\overline{A})$ is the [[dg-Lie algebra]] (regarded as an $L_\infty$-algebra) whose underlying [[chain complex]] is 

$dgLie_{Qu}(X,\overline{A})^0 = \{v+ \overline{\theta}  \in Vect(X)\oplus Tot^{n-1}(\mathcal{U}, \Omega^\bullet) \;\vert\; \mathcal{L}_v \overline{A} = \mathbf{d}_{Tot}\overline{\theta}\}$;

$dgLie_{Qu}(X,\overline{A})^{i \gt 0} = Tot^{n-1-i}(\mathcal{U},\Omega^\bullet)$

with [[differential]] given by $\mathbf{d}_{Tot}$ (where $Tot$ refers to [[total complex]] of the Cech-de Rham [[double complex]]).

The non-vanishing dg-Lie bracket on this complex are defined to be

* $[v_1 + \overline{\theta}_1, v_2 + \overline{\theta}_2] = [v_1, v_2] + \mathcal{L}_{v_1}\overline{\theta}_2 - \mathcal{L}_{v_2}\overline{\theta}_1$;

* $[v+ \overline{\theta}, \overline{\eta}] = - [\eta, v + \overline{\theta}] = \mathcal{L}_v \overline{\eta}$.

=--

([FRS 13b, def./prop. 4.2.1](#FRS13b))



+-- {: .num_prop #ComparisonTheorem}
###### Proposition

There is an [[equivalence]] in the [[model structure for L-∞ algebras|homotopy theory of L-∞ algebras]]

$$
  f
  \colon
  L_\infty(X,\omega)
  \stackrel{\simeq}{\longrightarrow}
  dgLie_{Qu}(X,\overline{A})
$$

between the $L_\infty$-algebras of def. \ref{PoissonBracketLienAlgebra} and def. \ref{PoissondgAlgebra} (in particular def. \ref{PoissondgAlgebra} does not depend on the choice of $\overline{A}$) whose underlying [[chain map]] satisfies

* $f(v + J) = v - J|_{\mathcal{U}} + \sum_{i = 0}^n (-1)^i \iota_v A^{n-i}$.

=--

([FRS 13b, theorem 4.2.2](#FRS13b))

## Properties

### The extension theorem

+-- {: .num_defn #ExtensionTheorem}
###### Proposition

Given a [[pre n-plectic manifold]] $(X,\omega_{n+1})$, then the Poisson bracket Lie $n$-algebra $\mathfrak{Pois}(X,\omega)$ from [above](#Definition) is an [[L-infinity algebra cohomology|extension]] of the [[Lie algebra]] of [[Hamiltonian vector fields]] $Vect_{Ham}(X)$, def. \ref{HamiltonianFormsAndVectorFields} by the [[cocycle]] [[infinity-groupoid]] $\mathbf{H}(X,\flat \mathbf{B}^{n-1} \mathbb{R})$ for [[ordinary cohomology]] with [[real number]] [[coefficients]] in that there is a [[homotopy fiber sequence]] in the [[homotopy theory of L-infinity algebras]] of the form

$$
  \array{
    \mathbf{H}(X,\flat \mathbf{B}^{d-1}\mathbb{R}) 
    &\longrightarrow&
    \mathfrak{Pois}(X,\omega)
    \\
    && \downarrow
    \\
    && Vect_{Ham}(X,\omega)
    &\stackrel{\omega[\bullet]}{\longrightarrow}&
    \mathbf{B} \mathbf{H}(X,\flat \mathbf{B}^{d-1}\mathbb{R})
  }
  \,,
$$

where the [[cocycle]] $\omega[\bullet]$, when realized on the model of def. \ref{PoissonBracketLienAlgebra}, is degreewise given by by contraction with $\omega$.

=--

This is [FRS13b, theorem 3.3.1](#FRS13b).

As a corollary this means that the [[0-truncation]] $\tau_0 \mathfrak{Pois}(X,\omega)$ is a [[Lie algebra extension]] by [[de Rham cohomology]], fitting into a [[short exact sequence]] of [[Lie algebras]]

$$
  0 \to H^{d-1}_{dR}(X) \longrightarrow \tau_0 \mathfrak{Pois}(X,\omega) \longrightarrow Vect_{Ham}(X) \to 0
 \,.
$$

+-- {: .num_remark}
###### Remark

These kinds of extensions are known traditionally form [[current algebras]].

=--


## Related concepts

* [[higher Poisson structure]]

  * [[Poisson n-algebra]]

  * [[Nambu bracket]]

* [[current algebra]]

* [[geometry of physics -- prequantum geometry]]

[[!include slice automorphism groups in higher prequantum geometry - table]]

[[!include geometric quantization extensions - table]]


## References

The Poisson bracket $L_\infty$-algebra $L_\infty(X,\omega)$ was introduced in

* {#Rogers10} [[Chris Rogers]], _$L_\infty$ algebras from multisymplectic geometry_,  Letters in Mathematical Physics April 2012, Volume 100, Issue 1, pp 29-50  ([arXiv:1005.2230](http://arxiv.org/abs/1005.2230), [journal](http://link.springer.com/article/10.1007%2Fs11005-011-0493-x)).

* {#Rogers11} [[Chris Rogers]], _Higher symplectic geometry_ PhD thesis (2011) ([arXiv:1106.4068](http://arxiv.org/abs/1106.4068))
 
Discussion in the broader context of [[higher differential geometry]] and [[higher prequantum geometry]] is in 

* {#FRS13a} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher geometric prequantum theory|Higher $U(1)$-gerbe connections in geometric prequantization]]_, Rev. Math. Phys., Vol. 28, Issue 06, 1650012 (2016) ([arXiv:1304.0236](http://arxiv.org/abs/1304.0236))

* {#FRS13b} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:L-∞ algebras of local observables from higher prequantum bundles]]_, Homology, Homotopy and Applications, Volume 16 (2014) Number 2, p. 107 &#8211; 142 ([arXiv:1304.6292](http://arxiv.org/abs/1304.6292))

* Nestor Leon Delgado, _Lagrangian field theories: ind/pro-approach and L-infinity algebra of local observables_ ([arXiv:1805.10317](https://arxiv.org/abs/1805.10317))

See also

* {#RitterSaemann15} [[Patricia Ritter]], [[Christian Sämann]], _Automorphisms of Strong Homotopy Lie Algebras of Local Observables_ ([arXiv:1507.00972](http://arxiv.org/abs/1507.00972))

[[!redirects Poisson bracket Lie n-algebras]]

[[!redirects Poisson-bracket Lie n-algebra]]
[[!redirects Poisson-bracket Lie n-algebras]]


[[!redirects Poisson Lie n-algebra]]
[[!redirects Poisson Lie n-algebras]]

[[!redirects Poisson L-∞ algebra]]
[[!redirects Poisson L-∞ algebras]]

[[!redirects Poisson bracket L-∞ algebra]]
[[!redirects Poisson brakcet L-∞ algebras]]


[[!redirects Poisson L-infinity algebra]]
[[!redirects Poisson L-infinity algebras]]

[[!redirects Poisson-bracket Lie n-algebra of local observables]]
[[!redirects Poisson-bracket Lie n-algebras of local observables]]

[[!redirects L-∞ algebra of local observables]]
[[!redirects L-∞ algebras of local observables]]

[[!redirects Poisson bracket Lie (p+1)-algebra]]
[[!redirects Poisson bracket Lie (p+1)-algebras]]